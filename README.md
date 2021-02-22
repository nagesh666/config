apiVersion: v1
baseDomain: < >
compute:
- hyperthreading: Enabled   
  name: worker
  replicas: 0 
controlPlane:
  hyperthreading: Enabled   
  name: master 
  replicas: 3 
metadata:
  name: test 
networking:
  clusterNetwork:
  - cidr: 10.128.0.0/14 
    hostPrefix: 23 
  networkType: OpenShiftSDN
  serviceNetwork: 
  - 172.30.0.0/16
platform:
  none: {} 
fips: false 
pullSecret: '{"auths":{"cloud.openshift.com":{"auth":"b3BlbnNoaWZ0LXJlbGVhc2UtZGV2K29jbV9hY2Nlc3NfMzdmNmU5NDEzOThiNDQzMmFjNjU2ZGNjNWIzYjdiYjQ6VVNYT05KUktTSk9DTjlPMFJFWENORU5TRVlTRUZERkVITE5VWkhVNFUwN0VHVlVLN0hPQkdCQjNXQTlLR09PRw==","email":"abhilash.sebastian1@tcs.com"},"quay.io":{"auth":"b3BlbnNoaWZ0LXJlbGVhc2UtZGV2K29jbV9hY2Nlc3NfMzdmNmU5NDEzOThiNDQzMmFjNjU2ZGNjNWIzYjdiYjQ6VVNYT05KUktTSk9DTjlPMFJFWENORU5TRVlTRUZERkVITE5VWkhVNFUwN0VHVlVLN0hPQkdCQjNXQTlLR09PRw==","email":"abhilash.sebastian1@tcs.com"},"registry.connect.redhat.com":{"auth":"fHVoYy1wb29sLTkzZmNlZTE1LTMyYzUtNDFjZS04MWQwLWU4YzlmZDAyNzc5MTpleUpoYkdjaU9pSlNVelV4TWlKOS5leUp6ZFdJaU9pSmhaak5qWmpoaVlXUmxZbVEwWVdRd09XRTNNbUV6WW1VNE1XUm1OekF3WkNKOS5kalpjeUpTUDQ0SWlUSE4yN1BwNWY2NmJTNV9uZ3BXRjBnOU44MEVhQXFoREx5VzgwbHJBOEN4YU5rYjdqR1RnT1RjVV83RjFqNXkyczN0V2ZINDJPNnhKVm8tcms3YXRUNF9zVloyWGhUaHRYWnBzc3RGQlBLU0xoOWN2ejZSYThkMHZhSTRqemY1Q0hETE1jaXdKUUhuWmI1M3lHZHVyRGs3NzU3NmVKbGlLWGJSZDk1MmdUMEFpMUhWU3RMTXhZV2hTMl85d1NJdDY4V1lVbm9NTHlsYTRhcFY4bEV0ZkVUNjhQcFZqaE1LSUxTMHprOVVEZFJOQ0NUMm1lRERFWDVxZ01NbkdEZklodzlaR2R2TjVKOTlyWDNkbTFDTGNMUkYzc1I4X2daRnBUZUNGRjhQQkdkTkJOSnhucjA1NWo5T2FfYjBDWU1jTThIUmNHMzZQRzd0aUxzeW5YdlV3dEtTVVkyb2xBYjdwMEJlUnEyWEUtdDBaSVVBcFJINFRMSXdvci1vOTFfcklxRURMNDItSE9UQTgtMGI5b2xjbFp2Njhfd0c3cy1UM2gwcGlhMnBndFhSRmJkMGpMUS1pbUxzRWtWZWN6RGhVaTBMaUF5dEtJcXB2T1JyVFQ4dmQ3U1VTVmVOQURJUzFzTXZhZ3FiMW83Z3JPQnVKX21JRE9Pb3FqQTdWaGwzZkZYWldkcnVBaUwwUTRxSTZUM3hTYTBPX1RLb25wSnYzWmFHM3FzekFMcmI5T0VCUkl4Q0JMVTlhY1NRVURVdDlaVGNFUFZoUXF0SUM1RWZJcTIxblJManNvOXEtRm8yYTBVZmRUSURKd2ZENXpua19NZV9rLTN5dVcyYUlEY0p6UnZNMEpINko0UnhySzdPSFlKaVR5Q0VOVmdpeXBIYw==","email":"abhilash.sebastian1@tcs.com"},"registry.redhat.io":{"auth":"fHVoYy1wb29sLTkzZmNlZTE1LTMyYzUtNDFjZS04MWQwLWU4YzlmZDAyNzc5MTpleUpoYkdjaU9pSlNVelV4TWlKOS5leUp6ZFdJaU9pSmhaak5qWmpoaVlXUmxZbVEwWVdRd09XRTNNbUV6WW1VNE1XUm1OekF3WkNKOS5kalpjeUpTUDQ0SWlUSE4yN1BwNWY2NmJTNV9uZ3BXRjBnOU44MEVhQXFoREx5VzgwbHJBOEN4YU5rYjdqR1RnT1RjVV83RjFqNXkyczN0V2ZINDJPNnhKVm8tcms3YXRUNF9zVloyWGhUaHRYWnBzc3RGQlBLU0xoOWN2ejZSYThkMHZhSTRqemY1Q0hETE1jaXdKUUhuWmI1M3lHZHVyRGs3NzU3NmVKbGlLWGJSZDk1MmdUMEFpMUhWU3RMTXhZV2hTMl85d1NJdDY4V1lVbm9NTHlsYTRhcFY4bEV0ZkVUNjhQcFZqaE1LSUxTMHprOVVEZFJOQ0NUMm1lRERFWDVxZ01NbkdEZklodzlaR2R2TjVKOTlyWDNkbTFDTGNMUkYzc1I4X2daRnBUZUNGRjhQQkdkTkJOSnhucjA1NWo5T2FfYjBDWU1jTThIUmNHMzZQRzd0aUxzeW5YdlV3dEtTVVkyb2xBYjdwMEJlUnEyWEUtdDBaSVVBcFJINFRMSXdvci1vOTFfcklxRURMNDItSE9UQTgtMGI5b2xjbFp2Njhfd0c3cy1UM2gwcGlhMnBndFhSRmJkMGpMUS1pbUxzRWtWZWN6RGhVaTBMaUF5dEtJcXB2T1JyVFQ4dmQ3U1VTVmVOQURJUzFzTXZhZ3FiMW83Z3JPQnVKX21JRE9Pb3FqQTdWaGwzZkZYWldkcnVBaUwwUTRxSTZUM3hTYTBPX1RLb25wSnYzWmFHM3FzekFMcmI5T0VCUkl4Q0JMVTlhY1NRVURVdDlaVGNFUFZoUXF0SUM1RWZJcTIxblJManNvOXEtRm8yYTBVZmRUSURKd2ZENXpua19NZV9rLTN5dVcyYUlEY0p6UnZNMEpINko0UnhySzdPSFlKaVR5Q0VOVmdpeXBIYw==","email":"abhilash.sebastian1@tcs.com"}}}' 
sshKey: 'ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAICex8EhlQAykQJrLvE4xy2r5Y+mFHl9PbMnVjSRKtJRl root@CUSTCAASJMP012' 
