pipeline {
   agent any
   environment {
       registry = "gotwasin/hello-go"
       GOCACHE = "/tmp"
       KUBECONFIG = "
apiVersion: v1
clusters:
- cluster:
    certificate-authority-data: LS0tLS1CRUdJTiBDRVJUSUZJQ0FURS0tLS0tCk1JSUN5RENDQWJDZ0F3SUJBZ0lCQURBTkJna3Foa2lHOXcwQkFRc0ZBREFWTVJNd0VRWURWUVFERXdwcmRXSmwKY201bGRHVnpNQjRYRFRJd01ETXdOakEzTlRrME1sb1hEVE13TURNd05EQTNOVGswTWxvd0ZURVRNQkVHQTFVRQpBeE1LYTNWaVpYSnVaWFJsY3pDQ0FTSXdEUVlKS29aSWh2Y05BUUVCQlFBRGdnRVBBRENDQVFvQ2dnRUJBSzd0CllxK3VKQmNJMVpiNEU3elhCQ2twV0J4WWJmUmYxMTZudW1DTWs1R05KM1VTaHFSa0xqMndpSm1ERXk4VS9uQXUKQ2k2UjdLTXBycUk0MDgwYllKZko5UTE3R01ia0l2R0c2eTN5VEVYd0JBVitmckpWV3JqemlvUW5rdm1tb05MeQp5eW9HbmkvSHZOOGhhVVN5Tm5Dd0UxaEZQWkxZMUtKL2lhVE84NU00OFBXR21HRExZYU1kOHkzM01GSGlJeXBMCi9sZ3Z4b0gyd2tQTmlHMTM0WWtydTVNZW1xTXkzQWJXZjVldThkYkMvY3FDNUlyYTFwTW12Y0l6SDF0RmVkM0IKYWZOTlg3MG8weGdYS0J3S2FUWjUvbVpNaFZSVjhvSEN0VkFtUXNSanhmaDdscEFtOVo3elpsb1k1RUJ4QXBSawp0OHcvNG5qWitaQTJPejJ5L0Y4Q0F3RUFBYU1qTUNFd0RnWURWUjBQQVFIL0JBUURBZ0trTUE4R0ExVWRFd0VCCi93UUZNQU1CQWY4d0RRWUpLb1pJaHZjTkFRRUxCUUFEZ2dFQkFJQ004dDZ1U29kMldENkswZEJnL2lFb09vangKdEN5ak9qRmZBcmpVSERMWnNzTktrcW5QblNxYUtLNUZ5QmdwU3ZtUjFOeUpsSHRsamxnblJTcVRtL0VNblZhSwpPa0FhdEZOU3VBVmcwMmtLb3BNTGZ3Tkd5TlhCdnN2bU54eUc5MUpNam5RVCtYdXJwc2VOem1XR2RzNHVRcUdiCi9uQTB4eFU5ekgzMXd0SXRzODJrZFJHc25IcC92bit5Z0Q2b1pnUXJXak9ZUGxOc1FDTW1KdlVkWWFrSDQ4bXoKR3hiZ1FyN3hxY2NoVTBiT0dRcUJkMGtoUzV4bHYrRnIzOEJwclZqTjA3WmhrODVBd1JyVGNIT0J6QzNHME9QQwp6RkczY3VueFcwYmd1K1NPZlkxWjhScG1sSDRIVDRMbHFYeXdMTUdsODRnN29tWmVwSllTOUx6a3RIdz0KLS0tLS1FTkQgQ0VSVElGSUNBVEUtLS0tLQo=
    server: https://kubernetes.docker.internal:6443
  name: docker-desktop
contexts:
- context:
    cluster: docker-desktop
    user: docker-desktop
  name: docker-desktop
- context:
    cluster: docker-desktop
    user: docker-desktop
  name: docker-for-desktop
current-context: docker-desktop
kind: Config
preferences: {}
users:
- name: docker-desktop
  user:
    client-certificate-data: LS0tLS1CRUdJTiBDRVJUSUZJQ0FURS0tLS0tCk1JSUM5RENDQWR5Z0F3SUJBZ0lJZWxGdTRlL1gvQ013RFFZSktvWklodmNOQVFFTEJRQXdGVEVUTUJFR0ExVUUKQXhNS2EzVmlaWEp1WlhSbGN6QWVGdzB5TURBek1EWXdOelU1TkRKYUZ3MHlNVEF6TVRBd05qTTBOVGhhTURZeApGekFWQmdOVkJBb1REbk41YzNSbGJUcHRZWE4wWlhKek1Sc3dHUVlEVlFRREV4SmtiMk5yWlhJdFptOXlMV1JsCmMydDBiM0F3Z2dFaU1BMEdDU3FHU0liM0RRRUJBUVVBQTRJQkR3QXdnZ0VLQW9JQkFRRFRWY0ViRHZ4VUxBTXgKZ2FXeklCdDZCQlBPRkgzZVRKeUwxa01WaEdEVytOVTl2bDYyM2RwZXBTV1g4a0hNcGh3S3Y4Q29MOUtPem40WApYSE9wclJPTGEwWm1nNkhYRnliZFdhd3E2Z3ZHa0hFYWdNc01CeFZETXUzZFlCb1BKaUdhY1BPOHlScDVjZkJ1CjJnWjJRajg0UnJoUHk4Mmp4ZVBqQ0RkZnUxVEI3c0NqUDc3eWFGcGdMcEhaTE4zanJiTURVb0wyZ3MwVVcvSWEKb1Bnc0h0aC9CUUZubXFJaVVhaSt1RExJK1htaEVyTkhTMTZGVHRYSm15TVpmOWZkVDJjaFptT1NrUzhkYkZSUwpLSnRRRXZFVDJZRi95NXg5N2ZoNVQ4ZHZ1Z25lL1RRMFlnUzFUQlZLTVdLQ1M3ZHpQTmk2S0xLQnZkVmVWVGJGCkhNMXlzWFNyQWdNQkFBR2pKekFsTUE0R0ExVWREd0VCL3dRRUF3SUZvREFUQmdOVkhTVUVEREFLQmdnckJnRUYKQlFjREFqQU5CZ2txaGtpRzl3MEJBUXNGQUFPQ0FRRUFrQzk4RU03WXpzZTdINjN0VmlhbTUxeTBSQWJMYWVHTAord3BlQnQzRGZucDVrVWlodWFwRUFnS2YzY2hnbkd5Syt6RUp5TEVySGpyV0JlUHRLR0lGUnRmU3JoZStRa2tDCmpjVkJxQTZUdGYwTUlmN09UREQ0RDkzZVNOSDJlZ0pLRlpPTVlxaXB4WXd3ZUF5bjlEeHlZQm8vekMwVkRaYVcKeEozK0FZK2pBblpwc3NydGJoaENJTStHRis5c2h3Yyt0TU9LcjJqRDg0Qk1UR2h2dXFvQnpFdU9RVzJvMEw2ZAplQm9LQXV5SnpWUThlTUV4SWxNTElPVnFvQk5weEU5bThTY3BGQWVHa1gwbXRzeHc4a1BMN3ZvU0JYVmZzT2tTCllQd0RWY3h4ZjJycVkvczVqaVh0blI0c2pZK1RROThHR1lpZE55WlFrQUJLc0piUHVWeU5yUT09Ci0tLS0tRU5EIENFUlRJRklDQVRFLS0tLS0K
    client-key-data: LS0tLS1CRUdJTiBSU0EgUFJJVkFURSBLRVktLS0tLQpNSUlFcFFJQkFBS0NBUUVBMDFYQkd3NzhWQ3dETVlHbHN5QWJlZ1FUemhSOTNreWNpOVpERllSZzF2alZQYjVlCnR0M2FYcVVsbC9KQnpLWWNDci9BcUMvU2pzNStGMXh6cWEwVGkydEdab09oMXhjbTNWbXNLdW9MeHBCeEdvREwKREFjVlF6THQzV0FhRHlZaG1uRHp2TWthZVhId2J0b0dka0kvT0VhNFQ4dk5vOFhqNHdnM1g3dFV3ZTdBb3orKwo4bWhhWUM2UjJTemQ0NjJ6QTFLQzlvTE5GRnZ5R3FENExCN1lmd1VCWjVxaUlsR292cmd5eVBsNW9SS3pSMHRlCmhVN1Z5WnNqR1gvWDNVOW5JV1pqa3BFdkhXeFVVaWliVUJMeEU5bUJmOHVjZmUzNGVVL0hiN29KM3YwME5HSUUKdFV3VlNqRmlna3UzY3p6WXVpaXlnYjNWWGxVMnhSek5jckYwcXdJREFRQUJBb0lCQVFDYUVrUFZXVWlHaVF2Two5T2o3dldXcXYvdzhXdDRreWcrN052cnpYZTVINjJOelB5M0gvZGZzOWxPQkFrSU1VL0hQdUZwWmczdnJWd25BCk9FdXVvUnJGb3ZEUlhoZ0lPcjIvMUZkYmRnUWR3RUpsQXc2RTkwaitFOHdzZjVxZi9ybXk0YlFncHpDZzUzdFYKSmFoZVlRKzhGSHJjMmdWUzU3dXJVZHNrOU9ybThyaVY5V2FtalEyaFJVR3daQVJIMGxjYmx0Y1grNzlCdDhYagpDSjQ4OWgxT0p0SW43NjZuRTJxcWYwWVB5cnRqeEt5dEl0N2NCeVczdkxYYktTNVB2N2R3L0RCRWd5ZUdrbjY5CllJNW1XU1RuVEpvTHlMMWhZbFJzYzRxbFFaNk9TM0VHNHBQekd4d0oyb0duak5IRElZMzJZQzlXdmtkZ0RCTEIKd0xGaUpjVEJBb0dCQVBLSkJ5a1FmVzkyVDJOVy9iUGt6RHp3S2VGeFQ0M3FDNmlOa2UvUzRvOWliVjA2ZFAySApNS3JWaHh2WDlkeCtKVHEyVFFGY0VFeEZiNWZPcDZIMGxrbHlvZVJ0cG1rUEFLVWhENXl5Vkp5NktxOFVFcWI2CjdydDVhNURlMXM3SEZCZUViRnQxQ2JhQ1lDa2hZV1N2b2ZPWGpReVQvNUxPbk1aSEZVT1gwNytoQW9HQkFOOFIKVE04RlBwcHlBaStMWlc2QkFIZm0vTlM2U2NLQTVoYWxTazZHUzEzdjAxZ0krenlTS01ISXEwUGc4UE52WXM4UAp4dTkyUDl5cGttK2VkTHlhc2NJbDduaEsvU0ZGdmUyU0FaanV1ZzF0N3ZYejk0akZOOWRjQkdNdTRncllWU0lOCjUxR1RDT09KTk1NcmhwRDdRY1pnRWFDbXhJNFdDRS90WTBSSytJRExBb0dCQU1QOHhTT0M1c29PZ2VLVnBsZ2IKZUl0NXkyNFpJWjlkVk9SMDJreEJUc0Z0V1ZEdjd4LzhnZkJhc2w1bXFvL3VBK21vN1JzL0tSQnBQOThkcU1xdwpHazNwNnpickFJRi9GUmRiV3dGVi9oZlVQSy9UK2FxanRnMGE5amhRU3FjM3FsM0NyY2xPRDNaRGJxOXVBUVRiCkJIVVNyM0ZObTBZbjNmby84TWY1UmF4aEFvR0FBZzFyc24vdTJvYndCRFg1SWZJbjZmS0RJd1h2eGMxZjBKZUcKdm9BMzAwNXdtRi9FeUFMa1F4d3dqemhUbnpuSUkvV1dNLy9YaUpVNjFySVRpdVMxZS83VFdlSCt3RDZmQjcrUApLalFRSEMyRnhGZVJVSDNZRExBNURoeVJVZDQ1c2syRWNsaXkvVHoyOGxERk5USktvYU9pcGVMQzdqZS9yZFNXClZEdUlXODhDZ1lFQWlTSXNwa2xtanVHa0ptOGJITHIwQ3NKdjFJdzRrbG90OFd0OG1wTjl5cVpVcUcxYUQvTUEKZFQxd0hUbDVSc1ZrbVE0S1pZcmhUanhrMzAvZkh6aENXNFc3aE9xSXFubk5pd080a3QwOEVUVGUyKzVKTDZQVQovQ05zYzVJV2xNVlRNRS85ak9tSWx3QzZpeTM5T0x3SjdDb0ZZYy83amhDNVpqcWFBbnA2bm1zPQotLS0tLUVORCBSU0EgUFJJVkFURSBLRVktLS0tLQo="
   }
   stages {
       stage('Build') {
           agent {
               docker {
                   image 'golang'
               }
           }
           steps {
               // Create our project directory.
               sh 'cd ${GOPATH}/src'
               sh 'mkdir -p ${GOPATH}/src/hello-world'
               // Copy all files in our Jenkins workspace to our project directory.               
               sh 'cp -r ${WORKSPACE}/* ${GOPATH}/src/hello-world'
               // Build the app.
               sh 'go build'              
           }    
       }
       stage('Test') {
           agent {
               docker {
                   image 'golang'
               }
           }
           steps {                
               // Create our project directory.
               sh 'cd ${GOPATH}/src'
               sh 'mkdir -p ${GOPATH}/src/hello-world'
               // Copy all files in our Jenkins workspace to our project directory.               
               sh 'cp -r ${WORKSPACE}/* ${GOPATH}/src/hello-world'
               // Remove cached test results.
               sh 'go clean -cache'
               // Run Unit Tests.
               sh 'go test ./... -v -short'           
           }
       }
       stage('Publish') {
           environment {
               registryCredential = 'gotwasin'
           }
           steps{
               script {
                   def appimage = docker.build registry + ":$BUILD_NUMBER"
                   docker.withRegistry( '', registryCredential ) {
                       appimage.push()
                       appimage.push('latest')
                   }
               }
           }
       }
       stage ('Deploy') {
           steps {
               script{
                //    def image_id = registry + ":$BUILD_NUMBER"
                //    sh "ansible-playbook  playbook.yml --extra-vars \"image_id=${image_id}\""
                   sh ""
                   sh "kubectl apply --kubeconfig=$(KUBECONFIG) -f deployment.yml -f service.yml"
               }
           }
       }
   }
}
