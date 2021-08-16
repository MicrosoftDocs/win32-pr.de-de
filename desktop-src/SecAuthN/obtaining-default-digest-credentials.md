---
description: Sowohl Clients als auch Server müssen Anmeldeinformationen abrufen, bevor sie einen Sicherheitskontext für den Nachrichtenaustausch einrichten können.
ms.assetid: a72404b8-1ec9-4f58-b3a6-09811070ea29
title: Abrufen von Standard-Digestanmeldeinformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93d5a0bb39f59680f2b5232dae1e6cc5c83673cf31c7cc3e0aa1325d5641e161
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117786588"
---
# <a name="obtaining-default-digest-credentials"></a>Abrufen von Standard-Digestanmeldeinformationen

Sowohl Clients als auch Server müssen [*Anmeldeinformationen abrufen,*](../secgloss/c-gly.md) bevor sie einen [*Sicherheitskontext*](../secgloss/s-gly.md) für den Nachrichtenaustausch einrichten können. Das Standardverhalten der [**AcquireCredentialsHandle-Funktion**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) besteht in der Bereitstellung von Anmeldeinformationen für den Sicherheitsprinzipal, der der aktuellen Anmeldesitzung zugeordnet [*ist.*](../secgloss/s-gly.md)

Im folgenden Beispiel wird ein serverseitiger Aufruf zum Abrufen der Standardanmeldeinformationen veranschaulicht.


```C++
SECURITY_STATUS SecStatus; 
TimeStamp tsLifetime; 
CredHandle hCred;
SecStatus = AcquireCredentialsHandle (
       NULL,                  // Default principal.
       WDIGEST_SP_NAME,       // Microsoft Digest SSP. 
       SECPKG_CRED_INBOUND,   // Server will use the credentials.
       NULL,                  // Use the current LOGON id.
       NULL,                  // Default credentials.
       NULL,                  // Not used with Digest SSP.
       NULL,                  // Not used with Digest SSP.
       &hCred,                // Receives the credential handle.
       &tsLifetime            // Receives the credential time limit.
);
```



Der clientseitige Aufruf für Standardanmeldeinformationen ist identisch, mit der Ausnahme, dass der dritte Parameter SECPKG CRED OUTBOUND angeben muss, um anzugeben, dass der Client das von der Funktion zurückgegebene Anmeldeinformationenhand handle \_ \_ verwendet.

Ein Beispiel, das das Abrufen von Anmeldeinformationen für einen anderen Sicherheitsprinzipal als den angemeldeten Benutzer veranschaulicht, finden Sie unter [Abrufen alternativer Anmeldeinformationen.](obtaining-alternate-digest-credentials.md)

 

 
