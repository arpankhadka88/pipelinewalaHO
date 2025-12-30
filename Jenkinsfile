node 
{
    def SF_USERNAME='arpankhadka88@cunning-panda-o148fn.com'
    def SF_INSTANCE_URL = "https://login.salesforce.com"

withCredentials([
    file(credentialsId: 'PLKoKey', variable: 'JWT_KEY_FILE'),
    string(credentialsId: 'PLKoConsumerID', variable: 'CQ_CONSUMER_SECRET')
]) {
    stage('Authorize DevHub') {
        sh """
          sf org login jwt \
            --instance-url ${SF_INSTANCE_URL} \
            --jwt-key-file ${JWT_KEY_FILE} \
            --client-id ${CQ_CONSUMER_SECRET} \
            --username ${SF_USERNAME}
        """
    }
}

                   }
  
