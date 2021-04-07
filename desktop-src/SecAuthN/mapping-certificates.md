---
description: Zuordnung von Zertifikaten
ms.assetid: 4139f927-54f4-4968-a9eb-020401bb536d
title: Zuordnung von Zertifikaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 397a9ef8822d4f191ae37cdb998166fa54c2b12d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758257"
---
# <a name="mapping-certificates"></a><span data-ttu-id="f4fd6-103">Zuordnung von Zertifikaten</span><span class="sxs-lookup"><span data-stu-id="f4fd6-103">Mapping Certificates</span></span>

> [!Note]  
> <span data-ttu-id="f4fd6-104">Die Informationen in diesem Thema gelten nur für Server, für die eine Client Authentifizierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="f4fd6-104">The information in this topic is valid only for servers that require client authentication.</span></span>

 

<span data-ttu-id="f4fd6-105">Wenn eine Serveranwendung eine Clientauthentifizierung durchführen muss, versucht Schannel automatisch, das vom Client angebotene Zertifikat einem Benutzerkonto zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="f4fd6-105">When a server application requires client authentication, Schannel automatically attempts to map the certificate supplied by the client to a user account.</span></span>

<span data-ttu-id="f4fd6-106">Nachdem der [*Sicherheitskontext*](../secgloss/s-gly.md) eingerichtet wurde, kann die Serveranwendung die [**querysecuritycontexttoken**](/windows/desktop/api/Sspi/nf-sspi-querysecuritycontexttoken) -Funktion verwenden, um ein [*Zugriffs Token*](../secgloss/a-gly.md) für das Benutzerkonto abzurufen, dem das [*Client Zertifikat*](../secgloss/c-gly.md) zugeordnet wurde.</span><span class="sxs-lookup"><span data-stu-id="f4fd6-106">After the [*security context*](../secgloss/s-gly.md) has been established, the server application can use the [**QuerySecurityContextToken**](/windows/desktop/api/Sspi/nf-sspi-querysecuritycontexttoken) function to obtain an [*access token*](../secgloss/a-gly.md) for the user account to which the [*client certificate*](../secgloss/c-gly.md) was mapped.</span></span> <span data-ttu-id="f4fd6-107">Der Server kann die Identität des Clients auch mit der Identität [**atesecuritycontext**](/windows/desktop/api/Sspi/nf-sspi-impersonatesecuritycontext) -Funktion annehmen.</span><span class="sxs-lookup"><span data-stu-id="f4fd6-107">Also, the server can use the [**ImpersonateSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-impersonatesecuritycontext) function to impersonate the client.</span></span>

<span data-ttu-id="f4fd6-108">Weitere Informationen zur Authentifizierung finden Sie unter [Durchführen der Authentifizierung mithilfe von SChannel](performing-authentication-using-schannel.md).</span><span class="sxs-lookup"><span data-stu-id="f4fd6-108">For more information on authentication, see [Performing Authentication Using Schannel](performing-authentication-using-schannel.md).</span></span>

 

 
