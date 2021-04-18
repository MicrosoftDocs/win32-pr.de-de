---
description: Erläutert die Verwendung der SSPI-Nachrichten Unterstützung.
ms.assetid: 14d4813e-413e-4ef9-85f0-96986c3c1eca
title: Verwenden der Nachrichten Unterstützung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d75a2475609afed1647d99552a3719479d84fbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352230"
---
# <a name="using-message-support"></a><span data-ttu-id="f79aa-103">Verwenden der Nachrichten Unterstützung</span><span class="sxs-lookup"><span data-stu-id="f79aa-103">Using Message Support</span></span>

<span data-ttu-id="f79aa-104">Nachdem ein Hand Shake Vorgang abgeschlossen und eine sichere Verbindung hergestellt wurde, kann eine Anwendung die Funktionen [**makesignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature), [**verschlüsseltmessage (allgemein)**](/windows/win32/api/sspi/nf-sspi-encryptmessage), [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature)und [**DecryptMessage (allgemein)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) zum Austauschen von signierten oder verschlüsselten Anwendungsdaten mit dem Remote Computer verwenden.</span><span class="sxs-lookup"><span data-stu-id="f79aa-104">After a handshake has been completed and a secure connection has been established, an application can use the [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature), [**EncryptMessage (General)**](/windows/win32/api/sspi/nf-sspi-encryptmessage), [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature), and [**DecryptMessage (General)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) functions to exchange signed or encrypted application data with the remote computer.</span></span>

<span data-ttu-id="f79aa-105">Beispiele, die diese Funktionen verwenden, nachdem ein [*Sicherheitskontext*](../secgloss/s-gly.md) eingerichtet wurde, werden in den folgenden Abschnitten veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="f79aa-105">Examples that use these functions after a [*security context*](../secgloss/s-gly.md) has been established are demonstrated in the following sections:</span></span>

-   [<span data-ttu-id="f79aa-106">Signieren einer Nachricht</span><span class="sxs-lookup"><span data-stu-id="f79aa-106">Signing a Message</span></span>](signing-a-message.md)
-   [<span data-ttu-id="f79aa-107">Überprüfen einer Nachricht</span><span class="sxs-lookup"><span data-stu-id="f79aa-107">Verifying a Message</span></span>](verifying-a-message.md)
-   [<span data-ttu-id="f79aa-108">Verschlüsseln einer Nachricht</span><span class="sxs-lookup"><span data-stu-id="f79aa-108">Encrypting a Message</span></span>](encrypting-a-message.md)
-   [<span data-ttu-id="f79aa-109">Entschlüsseln einer Nachricht</span><span class="sxs-lookup"><span data-stu-id="f79aa-109">Decrypting a Message</span></span>](decrypting-a-message.md)

 

 
