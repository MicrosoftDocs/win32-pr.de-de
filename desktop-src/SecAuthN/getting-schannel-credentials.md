---
description: Im folgenden Beispiel wird veranschaulicht, wie ein typischer Client SChannel-Anmelde Informationen erhält.
ms.assetid: 8f912af8-fd64-467a-b154-28c60cb14929
title: Erhalten von SChannel-Anmelde Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c2594b808387943cd2fc645a459dfbcd66ebc54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104345918"
---
# <a name="getting-schannel-credentials"></a>Erhalten von SChannel-Anmelde Informationen

Im folgenden Beispiel wird veranschaulicht, wie ein typischer Client SChannel-Anmelde Informationen erhält. Im Beispiel wird die empfohlene Vorgehensweise für die Verwendung der System Standardwerte für Chiffren und Verschlüsselungs stärken befolgt. Dadurch kann das SChannel-Paket die bestmöglichen Algorithmen verwenden, um den Kanal zu sichern.


```C++
#include <windows.h>
#include <ntsecapi.h>
#include <stdio.h>
#include <sspi.h>
#include <schnlsp.h>

void getSchannelClientHandle(PCredHandle ppClientCred)
{
  SECURITY_STATUS SecStatus;
  TimeStamp Lifetime;
  CredHandle hCred;
  SCHANNEL_CRED credData;

  ZeroMemory(&credData, sizeof(credData));
  credData.dwVersion = SCHANNEL_CRED_VERSION;

  //-------------------------------------------------------
  // Specify the TLS V1.0 (client-side) security protocol.
  credData.grbitEnabledProtocols = SP_PROT_TLS1_CLIENT; 
    
  SecStatus = AcquireCredentialsHandle (
       NULL,                  // default principal
       UNISP_NAME,            // name of the SSP
       SECPKG_CRED_OUTBOUND,  // client will use the credentials
       NULL,                  // use the current LOGON id
       &credData,             // protocol-specific data
       NULL,                  // default
       NULL,                  // default
       &hCred,                // receives the credential handle
       &Lifetime              // receives the credential time limit
  );
  printf("Client credentials status: 0x%x\n", SecStatus);
  // Return the handle to the caller.
  if(ppClientCred != NULL)
      *ppClientCred = hCred;

  return;
  //-------------------------------------------------------
  // When you have finished with this handle,
  // free the handle by calling the 
  // FreeCredentialsHandle function.
}
```



Der Hauptunterschied zwischen Client-und serverseitiger Anforderung für Anmelde Informationen besteht darin, dass der Server ein Zertifikat mit einer Zertifikat [**\_ Kontext**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) Struktur wie folgt bereitstellen muss:


```C++
  PCCERT_CONTEXT serverCert; // server-side certificate
  //-------------------------------------------------------
  // Get the server certificate. 

  if (! (serverCert = getServerCertificate())) return;

  // getServerCertificate is a placeholder function.
  credData.paCred = &serverCert;
```



Die Beispiel Funktion " *getservercertificate* " ist eine Platzhalter Funktion für diese anwendungsspezifische Aktivität. Ein Beispiel für die Implementierung der *getservercertificate* -Funktion finden Sie unter [Get a Certificate](getting-a-certificate-for-schannel.md).

> [!Note]  
> Ändern Sie beim Anfordern von Anmelde Informationen, die vom Server verwendet werden sollen, den dritten Parameter (*fkredentialuse*) der [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) -Funktion von secpkg- \_ \_ outd ausgehend zu secpkg \_ -Daten Eingangsdaten \_ .

 

 

 
