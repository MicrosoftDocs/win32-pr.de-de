---
description: Das folgende Beispiel zeigt die Schritte zum Abrufen einer CERT \_ -Kontext Struktur, die ein Zertifikat enthält. Sie sollten ein Zertifikat und einen Zertifikat Speicher auswählen, die für Ihre Anwendung geeignet sind.
ms.assetid: 31d7a8bd-729f-4db7-8e22-25d14296c0c4
title: Erhalten eines Zertifikats für SChannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5bf7f311ac31fe2ff033d4b57f7d04bd1f42424
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372982"
---
# <a name="getting-a-certificate-for-schannel"></a>Erhalten eines Zertifikats für SChannel

Das folgende Beispiel zeigt die Schritte zum Abrufen einer [**CERT- \_ Kontext**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) Struktur, die ein Zertifikat enthält. Sie sollten ein Zertifikat und einen Zertifikat Speicher auswählen, die für Ihre Anwendung geeignet sind.

Dieses Beispiel veranschaulicht das Öffnen eines [*Zertifikat Speicher*](/windows/desktop/SecGloss/c-gly) und das Suchen eines Zertifikats, das mithilfe der [**SChannel- \_ Kred-**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) Struktur an die [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) -Funktion übergeben wird.


```C++
#include <windows.h>
#include <stdio.h>
#pragma comment(lib, "crypt32.lib")

#define MACHINE_NAME "example server"

PCCERT_CONTEXT getServerCertificate ()
{
  HCERTSTORE hMyCertStore = NULL;
  PCCERT_CONTEXT aCertContext = NULL;
  
  //-------------------------------------------------------
  // Open the My store, also called the personal store.
  // This call to CertOpenStore opens the Local_Machine My 
  // store as opposed to the Current_User's My store.

    hMyCertStore = CertOpenStore(CERT_STORE_PROV_SYSTEM,
                                 X509_ASN_ENCODING,
                                 0,
                                 CERT_SYSTEM_STORE_LOCAL_MACHINE,
                                 L"MY");

  if (hMyCertStore == NULL) 
  {
    printf("Error opening MY store for server.\n");
    goto cleanup;
  }
  //-------------------------------------------------------
  // Search for a certificate with some specified
  // string in it. This example attempts to find
  // a certificate with the string "example server" in
  // its subject string. Substitute an appropriate string
  // to find a certificate for a specific user.

  aCertContext = CertFindCertificateInStore(hMyCertStore, 
                  X509_ASN_ENCODING, 
                  0,
                  CERT_FIND_SUBJECT_STR_A,
                  MACHINE_NAME, // use appropriate subject name
                  NULL
  );
  
  if (aCertContext == NULL)
  {
    printf("Error retrieving server certificate.");
    goto cleanup;
  }
cleanup:
  if(hMyCertStore)
  {
      CertCloseStore(hMyCertStore,0);
  }
  return aCertContext;
}
```



 

 
