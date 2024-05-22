# Reference implementation and Azure Policy samples for a secured Azure OpenAI application
Reference architecture of a secure Azure OpenAI service.
![image](https://github.com/karlgots/openai/assets/4255248/e8770eea-c257-489b-b06f-d77ce738d26b)


Included in this repository:
- Policy initiative definition OAIPolicyInitiative.json, with policies covering Azure OpenAI service.
- Policy initiative definition RefAppPolicyInitiative.json, with policies covering the Azure services in the reference application. These include Azure OpenAI service, App Service Web App and Azure Blob storage.
- Custom policy OAIPolicy.json, which modifies a built-in policy [Azure AI Services resources should have key access disabled disable local authentication](https://www.azadvertizer.net/azpolicyadvertizer/71ef260a-8f18-47b7-abcb-62d0673d94dc.html) to only apply to Azure OpenAI services, excluding false positives from other Microsoft.CognitiveServices services.

             {
                "field": "kind",
                "equals": "OpenAI"
             }

