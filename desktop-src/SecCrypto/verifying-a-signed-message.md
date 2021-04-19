---
description: Mit diesen Schritten wird die Signatur der signierten Daten überprüft.
ms.assetid: 18246cc1-d3c4-4426-a342-ce3864cc412e
title: Überprüfen einer signierten Nachricht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e8f85a5bcde56df7bb41bb92276123bcd26024e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366165"
---
# <a name="verifying-a-signed-message"></a><span data-ttu-id="1dc63-103">Überprüfen einer signierten Nachricht</span><span class="sxs-lookup"><span data-stu-id="1dc63-103">Verifying a Signed Message</span></span>

<span data-ttu-id="1dc63-104">Mit diesen Schritten wird die Signatur der signierten Daten überprüft.</span><span class="sxs-lookup"><span data-stu-id="1dc63-104">These steps verify the signature of signed data.</span></span> <span data-ttu-id="1dc63-105">In der folgenden Abbildung werden die einzelnen Aufgaben dargestellt, die durchgeführt werden müssen, wie in der nachfolgenden Liste gezeigt.</span><span class="sxs-lookup"><span data-stu-id="1dc63-105">The following illustration depicts the individual tasks that must be accomplished, as shown in the list that follows it.</span></span>

![Überprüfen einer signierten Nachricht](images/verifmsg.png)

<span data-ttu-id="1dc63-107">**So überprüfen Sie die Signatur einer signierten Nachricht**</span><span class="sxs-lookup"><span data-stu-id="1dc63-107">**To verify the signature of a signed message**</span></span>

1.  <span data-ttu-id="1dc63-108">Einen Zeiger auf die signierte Nachricht erhalten.</span><span class="sxs-lookup"><span data-stu-id="1dc63-108">Get a pointer to the signed message.</span></span>
2.  <span data-ttu-id="1dc63-109">Öffnen Sie einen [*Zertifikat Speicher*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="1dc63-109">Open a [*certificate store*](../secgloss/c-gly.md).</span></span>
3.  <span data-ttu-id="1dc63-110">Verwenden Sie die in der Nachricht enthaltene Signatur Geber-ID, um das Zertifikat des Absenders zu erhalten und ein Handle für seinen [*öffentlichen Schlüssel*](../secgloss/p-gly.md)zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="1dc63-110">Using the signer ID contained in the message, get the sender's certificate and get a handle to its [*public key*](../secgloss/p-gly.md).</span></span>

    <span data-ttu-id="1dc63-111">Als Alternative zu den Schritten 2 und 3 können Sie das in der Nachricht enthaltene Zertifikat verwenden, um den öffentlichen Schlüssel des Signatur Gebers abzurufen.</span><span class="sxs-lookup"><span data-stu-id="1dc63-111">As an alternative to steps 2 and 3, you can use the certificate contained in the message to retrieve the signer's public key.</span></span>

4.  <span data-ttu-id="1dc63-112">Entschlüsseln Sie die digitale Signatur mithilfe des öffentlichen Schlüssels des Signatur Gebers, und erzeugen Sie den ursprünglichen Digest der Daten in der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="1dc63-112">Using the signer's public key, decrypt the digital signature, producing the original digest of the data in the message.</span></span>
5.  <span data-ttu-id="1dc63-113">Verwenden Sie den in der Nachricht enthaltenen Hash Algorithmus, um einen [*Hashwert*](../secgloss/h-gly.md) für die in der Nachricht enthaltenen Daten zu erhalten, wodurch ein neuer Digest ergibt.</span><span class="sxs-lookup"><span data-stu-id="1dc63-113">Using the hash algorithm contained in the message, [*hash*](../secgloss/h-gly.md) the data contained in the message, yielding a new digest.</span></span>
6.  <span data-ttu-id="1dc63-114">Vergleichen Sie den Digest, der aus der Nachricht abgerufen wurde, mit dem neuen soeben erstellten Digest.</span><span class="sxs-lookup"><span data-stu-id="1dc63-114">Compare the digest retrieved from the message with the new digest just created.</span></span>
7.  <span data-ttu-id="1dc63-115">Wenn die beiden Digests Stimmen, wird die Signatur überprüft.</span><span class="sxs-lookup"><span data-stu-id="1dc63-115">If the two digests match, the signature is verified.</span></span> <span data-ttu-id="1dc63-116">Dies bedeutet, dass der [*private Schlüssel*](../secgloss/p-gly.md) , der zum Signieren der Daten verwendet wurde, mit dem öffentlichen Schlüssel übereinstimmt, der nur zum Entschlüsseln der Signatur verwendet wurde, und dass die Daten seit der Signierung der Daten nicht geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="1dc63-116">This means that the [*private key*](../secgloss/p-gly.md) that was used to sign the data matches the public key just used to decrypt the signature, and that the data has not changed since the data was signed.</span></span>

    <span data-ttu-id="1dc63-117">Wenn die beiden Digests nicht stimmen, wird die Signatur nicht überprüft, und entweder Stimmen die privaten/öffentlichen Schlüssel nicht ab, oder die Daten wurden seit der Signierung der Daten geändert.</span><span class="sxs-lookup"><span data-stu-id="1dc63-117">If the two digests do not match, the signature is not verified, and either the private/public keys do not match, or the data has been changed since the data was signed, or both.</span></span>

<span data-ttu-id="1dc63-118">Eine einzelne Funktion ( [**cryptverifymessagesignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifymessagesignature)) kann zum Überprüfen einer Signatur verwendet werden, wie im folgenden Verfahren gezeigt.</span><span class="sxs-lookup"><span data-stu-id="1dc63-118">A single function, [**CryptVerifyMessageSignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifymessagesignature), can be used to verify a signature, as shown in the following procedure.</span></span>

<span data-ttu-id="1dc63-119">**So überprüfen Sie eine signierte Nachricht**</span><span class="sxs-lookup"><span data-stu-id="1dc63-119">**To verify a signed message**</span></span>

1.  <span data-ttu-id="1dc63-120">Einen Zeiger auf die signierte Nachricht erhalten.</span><span class="sxs-lookup"><span data-stu-id="1dc63-120">Get a pointer to the signed message.</span></span>
2.  <span data-ttu-id="1dc63-121">Gibt die Größe der signierten Nachricht an.</span><span class="sxs-lookup"><span data-stu-id="1dc63-121">Get the size of the signed message.</span></span>
3.  <span data-ttu-id="1dc63-122">Erhalten Sie ein Handle für einen Kryptografieanbieter.</span><span class="sxs-lookup"><span data-stu-id="1dc63-122">Get a handle on a cryptographic provider.</span></span>
4.  <span data-ttu-id="1dc63-123">Initialisieren Sie die " [**crypt \_ Verify \_ Message \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_verify_message_para) "-Struktur.</span><span class="sxs-lookup"><span data-stu-id="1dc63-123">Initialize the [**CRYPT\_VERIFY\_MESSAGE\_PARA**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_verify_message_para) structure.</span></span>
5.  <span data-ttu-id="1dc63-124">Um die Signatur zu überprüfen, können Sie [**cryptverifymessagesignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifymessagesignature) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="1dc63-124">Call [**CryptVerifyMessageSignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifymessagesignature) to verify the signature.</span></span>

<span data-ttu-id="1dc63-125">Code, der diese Prozedur implementiert, ist im [Beispiel C-Programm: Signieren einer Nachricht und Überprüfen einer Nachrichten Signatur](example-c-program-signing-a-message-and-verifying-a-message-signature.md)enthalten.</span><span class="sxs-lookup"><span data-stu-id="1dc63-125">Code that implements this procedure is included in [Example C Program: Signing a Message and Verifying a Message Signature](example-c-program-signing-a-message-and-verifying-a-message-signature.md).</span></span>

 

 
