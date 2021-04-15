---
description: Zeigt, wie eine verschlüsselte Nachricht gesendet wird.
ms.assetid: 928b1863-7a54-4bf0-b447-85b8c2868bcd
title: Manueller Austausch von Sitzungs Schlüsseln
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0114f8173084126a72519d291158f15f3e1c171
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104556173"
---
# <a name="manual-session-key-exchanges"></a><span data-ttu-id="fb6ec-103">Manueller Austausch von Sitzungs Schlüsseln</span><span class="sxs-lookup"><span data-stu-id="fb6ec-103">Manual Session Key Exchanges</span></span>

> [!Note]  
> <span data-ttu-id="fb6ec-104">Bei dem in diesem Abschnitt beschriebenen Verfahren wird davon ausgegangen, dass die Benutzer (oder CryptoAPI-Clients) bereits über einen eigenen Satz von [*öffentlichen/privaten Schlüsselpaaren*](../secgloss/p-gly.md) verfügen und auch die [*öffentlichen Schlüssel*](../secgloss/p-gly.md)der anderen abgerufen haben.</span><span class="sxs-lookup"><span data-stu-id="fb6ec-104">The procedure described in this section assumes that the users (or CryptoAPI clients) already possess their own set of [*public/private key pairs*](../secgloss/p-gly.md) and have also obtained each other's [*public keys*](../secgloss/p-gly.md).</span></span>

 

<span data-ttu-id="fb6ec-105">In der folgenden Abbildung wird gezeigt, wie Sie mit diesem Verfahren eine verschlüsselte Nachricht senden.</span><span class="sxs-lookup"><span data-stu-id="fb6ec-105">The following illustration shows how to use this procedure to send an encrypted message.</span></span>

![Senden einer verschlüsselten Nachricht](images/capi04.png)

<span data-ttu-id="fb6ec-107">Diese Vorgehensweise ist anfällig für mindestens eine gängige Angriffs Form.</span><span class="sxs-lookup"><span data-stu-id="fb6ec-107">This approach is vulnerable to at least one common form of attack.</span></span> <span data-ttu-id="fb6ec-108">Ein eavesdroppergerät kann Kopien von mindestens einer verschlüsselten Nachricht und den verschlüsselten Schlüsseln abrufen.</span><span class="sxs-lookup"><span data-stu-id="fb6ec-108">An eavesdropper can acquire copies of one or more encrypted messages and the encrypted keys.</span></span> <span data-ttu-id="fb6ec-109">Zu einem späteren Zeitpunkt kann der eavesdropperdienst eine dieser Nachrichten an den Empfänger senden, und der Empfänger hat keine Möglichkeit zu wissen, dass die Nachricht nicht direkt vom ursprünglichen Absender stammt.</span><span class="sxs-lookup"><span data-stu-id="fb6ec-109">Then, at some later time, the eavesdropper can send one of these messages to the receiver and the receiver will have no way of knowing the message did not come directly from the original sender.</span></span> <span data-ttu-id="fb6ec-110">Dieses Risiko kann durch ein Zeitstempel aller Nachrichten oder durch die Verwendung von Seriennummern verringert werden.</span><span class="sxs-lookup"><span data-stu-id="fb6ec-110">This risk can be reduced by time-stamping all messages or by using serial numbers.</span></span>

<span data-ttu-id="fb6ec-111">Die einfachste Möglichkeit zum Senden verschlüsselter Nachrichten an einen anderen Benutzer besteht darin, die Nachricht, die mit einem zufälligen Sitzungsschlüssel verschlüsselt ist, zusammen mit dem Sitzungsschlüssel zu senden, der mit dem [*öffentlichen Schlüsselaustausch*](../secgloss/k-gly.md)Schlüssel des Empfängers verschlüsselt ist</span><span class="sxs-lookup"><span data-stu-id="fb6ec-111">The easiest way to send encrypted messages to another user is to send the message encrypted with a random session key along with the session key encrypted with the receiver's [*key exchange public key*](../secgloss/k-gly.md).</span></span>

<span data-ttu-id="fb6ec-112">Im folgenden werden die Schritte zum Senden eines verschlüsselten Sitzungsschlüssels beschrieben.</span><span class="sxs-lookup"><span data-stu-id="fb6ec-112">Following are the steps for sending an encrypted session key.</span></span>

<span data-ttu-id="fb6ec-113">**So senden Sie einen verschlüsselten Sitzungsschlüssel**</span><span class="sxs-lookup"><span data-stu-id="fb6ec-113">**To send an encrypted session key**</span></span>

1.  <span data-ttu-id="fb6ec-114">Erstellen Sie einen zufälligen [*Sitzungsschlüssel*](../secgloss/s-gly.md) mithilfe der [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="fb6ec-114">Create a random [*session key*](../secgloss/s-gly.md) by using the [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) function.</span></span>
2.  <span data-ttu-id="fb6ec-115">Verschlüsseln Sie die Nachricht mit dem Sitzungsschlüssel.</span><span class="sxs-lookup"><span data-stu-id="fb6ec-115">Encrypt the message by using the session key.</span></span> <span data-ttu-id="fb6ec-116">Dieses Verfahren wird unter [Datenverschlüsselung und Entschlüsselung](data-encryption-and-decryption.md)erläutert.</span><span class="sxs-lookup"><span data-stu-id="fb6ec-116">This procedure is discussed in [Data Encryption and Decryption](data-encryption-and-decryption.md).</span></span>
3.  <span data-ttu-id="fb6ec-117">Exportieren Sie den Sitzungsschlüssel in ein [*Schlüssel-BLOB*](../secgloss/k-gly.md) mit der [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) -Funktion, und geben Sie dabei an, dass der Schlüssel mit dem öffentlichen Schlüsselaustausch Schlüssel des Ziel Benutzers verschlüsselt werden soll.</span><span class="sxs-lookup"><span data-stu-id="fb6ec-117">Export the session key into a [*key BLOB*](../secgloss/k-gly.md) with the [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) function, specifying that the key be encrypted with the destination user's key exchange public key.</span></span>
4.  <span data-ttu-id="fb6ec-118">Senden Sie sowohl die verschlüsselte Nachricht als auch das verschlüsselte Schlüsselblob an den Ziel Benutzer.</span><span class="sxs-lookup"><span data-stu-id="fb6ec-118">Send both the encrypted message and the encrypted key BLOB to the destination user.</span></span>
5.  <span data-ttu-id="fb6ec-119">Der Ziel Benutzer importiert das Schlüsselblob mithilfe der [**cryptimportkey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) -Funktion in seinen CSP.</span><span class="sxs-lookup"><span data-stu-id="fb6ec-119">The destination user imports the key BLOB into his or her CSP by using the [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) function.</span></span> <span data-ttu-id="fb6ec-120">Dadurch wird der Sitzungsschlüssel automatisch entschlüsselt, sofern der öffentliche Schlüssel für den Schlüsselaustausch des Ziel Benutzers in Schritt 3 angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="fb6ec-120">This will automatically decrypt the session key, provided the destination user's key exchange public key was specified in step 3.</span></span>
6.  <span data-ttu-id="fb6ec-121">Der Ziel Benutzer kann die Nachricht anschließend mithilfe des Sitzungsschlüssels entschlüsseln. Befolgen Sie hierzu das unter [Datenverschlüsselung und Entschlüsselung](data-encryption-and-decryption.md)beschriebene Verfahren.</span><span class="sxs-lookup"><span data-stu-id="fb6ec-121">The destination user can then decrypt the message by using the session key, following the procedure discussed in [Data Encryption and Decryption](data-encryption-and-decryption.md).</span></span>

 

 
