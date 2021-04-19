---
description: Erläutert, wie Nachrichten mithilfe von Microsoft Digest geschützt werden.
ms.assetid: 15509d51-80c0-4d5c-aa24-4dc17de3f12c
title: Schützen von Nachrichten mit Microsoft Digest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 573eafcf66e23188546abd3acd316095ec100187
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362544"
---
# <a name="protecting-messages-using-microsoft-digest"></a><span data-ttu-id="09296-103">Schützen von Nachrichten mit Microsoft Digest</span><span class="sxs-lookup"><span data-stu-id="09296-103">Protecting Messages Using Microsoft Digest</span></span>

## <a name="http-and-sasl"></a><span data-ttu-id="09296-104">HTTP und SASL</span><span class="sxs-lookup"><span data-stu-id="09296-104">HTTP and SASL</span></span>

<span data-ttu-id="09296-105">Um bestimmte Arten von Sicherheitsverletzungen zu erkennen, verwenden der Client und der Server die SSPI ( [Security Support Provider Interface](sspi.md) )-Nachrichten [*Integritäts*](../secgloss/i-gly.md) Funktionen [**makesignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) und [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) zum Schützen von Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="09296-105">As a means of detecting certain types of security violations, the client and server use the [security support provider interface](sspi.md) (SSPI) message [*integrity*](../secgloss/i-gly.md) functions [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) and [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) to protect messages.</span></span>

<span data-ttu-id="09296-106">Ein Client ruft die [**makesignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) -Funktion auf, um eine Nachricht mithilfe Ihres [*Sicherheits Kontexts*](../secgloss/s-gly.md)zu signieren.</span><span class="sxs-lookup"><span data-stu-id="09296-106">A client calls the [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) function to sign a message using its [*security context*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="09296-107">Der Server verwendet die [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) -Funktion, um den Ursprung der Nachricht zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="09296-107">The server uses the [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) function to verify the message's origin.</span></span> <span data-ttu-id="09296-108">Zusätzlich zur Überprüfung der [*Signatur*](../secgloss/d-gly.md) , die die Nachricht begleitet, prüft die **VerifySignature** -Funktion auch, ob die [*Nonce*](../secgloss/n-gly.md) -Anzahl (angegeben durch die NC-Direktive) eine höhere als die letzte für die Nonce gesendete Anzahl ist.</span><span class="sxs-lookup"><span data-stu-id="09296-108">In addition to verifying the [*signature*](../secgloss/d-gly.md) that accompanies the message, the **VerifySignature** function also checks that the [*nonce*](../secgloss/n-gly.md) count (specified by the nc directive) is one greater than the last count sent for the nonce.</span></span> <span data-ttu-id="09296-109">Wenn dies nicht der Fall ist, gibt die **VerifySignature** -Funktion einen SEK \_ . aus dem Sequenz- \_ \_ Fehlercode zurück.</span><span class="sxs-lookup"><span data-stu-id="09296-109">If this is not the case, the **VerifySignature** function returns an SEC\_OUT\_OF\_SEQUENCE error code.</span></span>

## <a name="sasl-only"></a><span data-ttu-id="09296-110">Nur SASL</span><span class="sxs-lookup"><span data-stu-id="09296-110">SASL Only</span></span>

<span data-ttu-id="09296-111">Die Funktionen [**verschlüsseltmessage (allgemein)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) und [**DecryptMessage (allgemein)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) geben Vertraulichkeit für Nachrichten nach der Authentifizierung zwischen Client und Server an.</span><span class="sxs-lookup"><span data-stu-id="09296-111">The [**EncryptMessage (General)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) and [**DecryptMessage (General)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) functions supply confidentiality for post-authentication messages exchanged between client and server.</span></span>

<span data-ttu-id="09296-112">Um die Nachrichten Vertraulichkeits Funktionen zu verwenden, muss der Server und der Client einen [*Sicherheitskontext*](../secgloss/s-gly.md) mit den folgenden Attributen eingerichtet haben:</span><span class="sxs-lookup"><span data-stu-id="09296-112">In order to use the message confidentiality functions, the server and client must have established a [*security context*](../secgloss/s-gly.md) with the following attributes:</span></span>

-   <span data-ttu-id="09296-113">Die von der QoP-Direktive angegebene Qualität des Schutzes muss "auth-conf" lauten.</span><span class="sxs-lookup"><span data-stu-id="09296-113">Quality of protection, specified by the qop directive, must be "auth-conf".</span></span>
-   <span data-ttu-id="09296-114">Ein Verschlüsselungsmechanismus muss mithilfe der Chiffre Direktive angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="09296-114">An encryption mechanism must have been specified by means of the cipher directive.</span></span>

 

 
