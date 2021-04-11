---
description: Sowohl Clients als auch Server müssen Anmelde Informationen abrufen, bevor Sie einen Sicherheitskontext für den Nachrichtenaustausch einrichten können.
ms.assetid: a72404b8-1ec9-4f58-b3a6-09811070ea29
title: Abrufen der standardmäßigen Hashwert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12e870d6bad1c3b4ef9e889a91444e98159bc758
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215885"
---
# <a name="obtaining-default-digest-credentials"></a><span data-ttu-id="da1b0-103">Abrufen der standardmäßigen Hashwert</span><span class="sxs-lookup"><span data-stu-id="da1b0-103">Obtaining Default Digest Credentials</span></span>

<span data-ttu-id="da1b0-104">Sowohl Clients als auch Server müssen [*Anmelde*](../secgloss/c-gly.md) Informationen abrufen, bevor Sie einen [*Sicherheitskontext*](../secgloss/s-gly.md) für den Nachrichtenaustausch einrichten können.</span><span class="sxs-lookup"><span data-stu-id="da1b0-104">Both clients and servers must obtain [*credentials*](../secgloss/c-gly.md) before they can establish a [*security context*](../secgloss/s-gly.md) for message exchange.</span></span> <span data-ttu-id="da1b0-105">Das Standardverhalten der [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) -Funktion besteht darin, Anmelde Informationen für den Sicherheits Prinzipal bereitzustellen, der der aktuellen Anmelde [*Sitzung*](../secgloss/s-gly.md)zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="da1b0-105">The default behavior of the [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) function is to provide credentials for the security principal associated with the current logon [*session*](../secgloss/s-gly.md).</span></span>

<span data-ttu-id="da1b0-106">Im folgenden Beispiel wird ein serverseitiger-Abruf zum Abrufen der Standard Anmelde Informationen veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="da1b0-106">The following example demonstrates a server-side call to obtain the default credentials.</span></span>


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



<span data-ttu-id="da1b0-107">Der Client seitige-Befehl für die Standard Anmelde Informationen ist identisch, mit dem Unterschied, dass der dritte Parameter secpkg-Daten ausgehend angeben muss, \_ \_ um anzugeben, dass der Client den von der Funktion zurückgegebenen Anmelde Informations Handle verwendet.</span><span class="sxs-lookup"><span data-stu-id="da1b0-107">The client-side call for default credentials is identical, except the third parameter must specify SECPKG\_CRED\_OUTBOUND to indicate that the client will use the credentials handle returned by the function.</span></span>

<span data-ttu-id="da1b0-108">Ein Beispiel für das Abrufen von Anmelde Informationen für einen Sicherheits Prinzipal, der nicht der angemeldete Benutzer ist, finden Sie unter Abrufen [alternativer Anmelde](obtaining-alternate-digest-credentials.md)Informationen.</span><span class="sxs-lookup"><span data-stu-id="da1b0-108">For an example that demonstrates obtaining credentials for a security principal other than the logged on user, see [Obtaining Alternate Credentials](obtaining-alternate-digest-credentials.md).</span></span>

 

 
