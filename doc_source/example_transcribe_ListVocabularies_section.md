# List custom Amazon Transcribe vocabularies using an AWS SDK<a name="example_transcribe_ListVocabularies_section"></a>

The following code example shows how to list custom Amazon Transcribe vocabularies\.

**Note**  
The source code for these examples is in the [AWS Code Examples GitHub repository](https://github.com/awsdocs/aws-doc-sdk-examples)\. Have feedback on a code example? [Create an Issue](https://github.com/awsdocs/aws-doc-sdk-examples/issues/new/choose) in the code examples repo\. 

------
#### [ Python ]

**SDK for Python \(Boto3\)**  
 To learn how to set up and run this example, see [GitHub](https://github.com/awsdocs/aws-doc-sdk-examples/tree/main/python/example_code/transcribe#code-examples)\. 
  

```
def list_vocabularies(vocabulary_filter, transcribe_client):
    """
    Lists the custom vocabularies created for this AWS account.

    :param vocabulary_filter: The returned vocabularies must contain this string in
                              their names.
    :param transcribe_client: The Boto3 Transcribe client.
    :return: The list of retrieved vocabularies.
    """
    try:
        response = transcribe_client.list_vocabularies(
            NameContains=vocabulary_filter)
        vocabs = response['Vocabularies']
        next_token = response.get('NextToken')
        while next_token is not None:
            response = transcribe_client.list_vocabularies(
                NameContains=vocabulary_filter, NextToken=next_token)
            vocabs += response['Vocabularies']
            next_token = response.get('NextToken')
        logger.info(
            "Got %s vocabularies with filter %s.", len(vocabs), vocabulary_filter)
    except ClientError:
        logger.exception(
            "Couldn't list vocabularies with filter %s.", vocabulary_filter)
        raise
    else:
        return vocabs
```
+  For API details, see [ListVocabularies](https://docs.aws.amazon.com/goto/boto3/transcribe-2017-10-26/ListVocabularies) in *AWS SDK for Python \(Boto3\) API Reference*\. 

------

For a complete list of AWS SDK developer guides and code examples, see [Using this service with an AWS SDK](getting-started-sdk.md#sdk-general-information-section)\. This topic also includes information about getting started and details about previous SDK versions\.