# What is Amazon Transcribe?<a name="what-is"></a>

* Amazon Transcribe
  * == automatic speech recognition service /
    * 👀convert audio -- via, machine learning models, to -- text👀 /
      * you can
        * filter content,
        * analyze content | multi-channel audio,
        * split the speech of individual speakers 
      * transcription types
        * streaming
          * == real-time
        * batch
          * == media files / located | Amazon S3 bucket
  * uses
    * standalone transcription service
    * add speech-to-text capabilities | ANY application
  * see
    * [Supported languages and language\-specific features](supported-languages.md) table
    * [youtube video](https://www.youtube.com/watch?v=zD8NMw4T1TI)
    * [How Amazon Transcribe works](how-it-works.md)
    * [Getting started with Amazon Transcribe](getting-started.md)
    * [API Reference](https://docs.aws.amazon.com/transcribe/latest/APIReference/Welcome.html)

**Topics**
+ [Amazon Transcribe and HIPAA eligibility](#transcribe-hippa)
+ [Pricing](#transcribe-pricing)
+ [Endpoints and quotas](#endpoints-quotas)

## Amazon Transcribe and HIPAA eligibility<a name="transcribe-hippa"></a>

* Amazon Transcribe -- is covered under -- 
  * AWS’s HIPAA eligibility &
    * see [ HIPAA eligibility and BAA](http://aws.amazon.com/compliance/hipaa-compliance/)
  * BAA
    * requirements
      * BAA customers / encrypt 
        * ALL PHI 
          * | rest
          * and in transit | use it
* Automatic [PHI identification](phi-id.md) is available
  * 👀NO additional charge 👀 
  * | ALL regions / Amazon Transcribe operates

## Pricing<a name="transcribe-pricing"></a>

* pay-as-you-go service /
  * -- based on -- seconds of transcribed audio
  * billed | monthly basis
* TODO: Usage is billed in one\-second increments, with a minimum per request charge of 15 seconds\. 
* NO additional charges for features
  * _Example:_
    * PII content redaction
    * custom language models
* see [Amazon Transcribe Pricing / AWS Region](http://aws.amazon.com/transcribe/pricing/)

## Endpoints and quotas<a name="endpoints-quotas"></a>

* list of AWS Regions & endpoints available for Amazon Transcribe
  * see [Service endpoints](https://docs.aws.amazon.com/general/latest/gr/transcribe.html#transcribe_region)
* list of quotas / pertain to your transcriptions
  * see [Service quotas](https://docs.aws.amazon.com/general/latest/gr/transcribe.html#limits-amazon-transcribe)
  * SOME quotas -- can be changed -- upon request
    * check the **Adjustable** column