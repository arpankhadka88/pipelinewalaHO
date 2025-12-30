node 
{
    def SF_USERNAME='arpankhadka88@cunning-panda-o148fn.com'
    def SF_INSTANCE_URL = "https://login.salesforce.com"

  withCredentials([file(credentialsId: 'PLKoKey', variable:'jwt_key_file' , string(credentialsId: 'PLKoConsumerID', variable:'cq_consumer_secret')])
        {   

          stage('Authorize DevHub') 
          {
                sh "sf org login jwt --instance-url ${INSTANCE_URL} --jwt-key-file ${jwt_key_file} --client-id  ${cq_consumer_secret} --username ${SF_USERNAME}"
 
                
            }
}
  
