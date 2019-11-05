pipeline {
    agent any
    environment{
        COUNTRY=""
    }
    stages{
        stage("USA"){
            when{
                equals expected:"usa",actual: "$COUNTRY"
            }
            steps{
                script{
                    def response=httpRequest "https://api.darksky.net/forecast/api-tokend/40.7128,74.0060"
                    println("Content: "+response.content)
                }
            }
        }
        stage("UK"){
            when{
                equals expected:"uk",actual: "$COUNTRY"
            }
            steps{
                script{
                    def response=httpRequest "https://api.darksky.net/forecast/apit-token/51.5074,0.1278"
                    println("Content: "+response.content)
                }
            }
        }
        stage("SPAIN"){
            when{
                equals expected:"spain",actual: "$COUNTRY"
            }
            steps{
                script{
                    def response=httpRequest "https://api.darksky.net/forecast/api-token/40.4168,3.7038"
                    println("Content: "+response.content)
                }
            }
        }
    }
}
