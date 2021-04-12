---
description: Stellt die Aufgaben dar, die zum Erstellen einer signierten Nachricht durchgeführt werden müssen.
ms.assetid: 61896022-28c2-4f70-977a-c990b4b23c55
title: Erstellen einer signierten Nachricht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f68511c41a10fc0f690574e71c1dfe8a354efbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216715"
---
# <a name="creating-a-signed-message"></a><span data-ttu-id="80d0b-103">Erstellen einer signierten Nachricht</span><span class="sxs-lookup"><span data-stu-id="80d0b-103">Creating a Signed Message</span></span>

<span data-ttu-id="80d0b-104">Die folgende Abbildung zeigt die Aufgaben, die zum Erstellen einer signierten Nachricht durchgeführt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="80d0b-104">The following illustration depicts the tasks that must be accomplished to create a signed message.</span></span> <span data-ttu-id="80d0b-105">Die Schritte werden nach der Abbildung aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="80d0b-105">The steps are listed following the illustration.</span></span>

![Signieren einer Nachricht](images/signdmsg.png)

<span data-ttu-id="80d0b-107">**So erstellen Sie eine signierte Nachricht**</span><span class="sxs-lookup"><span data-stu-id="80d0b-107">**To create a signed message**</span></span>

1.  <span data-ttu-id="80d0b-108">Erstellen Sie die Daten (falls erforderlich), und rufen Sie einen Zeiger darauf ab.</span><span class="sxs-lookup"><span data-stu-id="80d0b-108">Create the data (if necessary) and get a pointer to it.</span></span>
2.  <span data-ttu-id="80d0b-109">Öffnen Sie einen [*Zertifikat Speicher*](../secgloss/c-gly.md) , der das Zertifikat des Signatur Gebers enthält.</span><span class="sxs-lookup"><span data-stu-id="80d0b-109">Open a [*certificate store*](../secgloss/c-gly.md) that contains the signer's certificate.</span></span>
3.  <span data-ttu-id="80d0b-110">Den [*privaten Schlüssel*](../secgloss/p-gly.md) für das Zertifikat erhalten.</span><span class="sxs-lookup"><span data-stu-id="80d0b-110">Get the [*private key*](../secgloss/p-gly.md) for the certificate.</span></span> <span data-ttu-id="80d0b-111">Eine Eigenschaft muss für das Zertifikat festgelegt werden, bevor Sie verwendet werden kann, um ein Zertifikat mit einem bestimmten [*CSP*](../secgloss/c-gly.md)und innerhalb des CSP an einen bestimmten privaten Schlüssel zu binden.</span><span class="sxs-lookup"><span data-stu-id="80d0b-111">A property must be set on the certificate before using it, to tie a certificate to a particular [*CSP*](../secgloss/c-gly.md), and, within that CSP, to a particular private key.</span></span> <span data-ttu-id="80d0b-112">Diese muss einmal festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="80d0b-112">This needs to be set once.</span></span>
4.  <span data-ttu-id="80d0b-113">Wählen Sie einen Hash Algorithmus für den Digest-Vorgang aus.</span><span class="sxs-lookup"><span data-stu-id="80d0b-113">Choose a hashing algorithm for the digest operation.</span></span> <span data-ttu-id="80d0b-114">Es wird empfohlen, dass der Hash Algorithmus an einem konfigurierbaren Speicherort ausgewählt wird, der anschließend aktualisiert werden kann, ohne dass Codeänderungen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="80d0b-114">We recommend that the hashing algorithm be selected from a configurable location that can be subsequently updated without requiring changes to code.</span></span>
5.  <span data-ttu-id="80d0b-115">Senden Sie die Daten über die Hash Funktion mithilfe des Hash Algorithmus, und erstellen Sie dadurch einen [*Hash*](../secgloss/h-gly.md) (Digest) der Daten.</span><span class="sxs-lookup"><span data-stu-id="80d0b-115">Send the data through the hashing function by using the hashing algorithm, thus creating a [*hash*](../secgloss/h-gly.md) (digest) of the data.</span></span>
6.  <span data-ttu-id="80d0b-116">Verschlüsseln Sie den Digest mithilfe des [*privaten Schlüssels*](../secgloss/p-gly.md) , der über die-Eigenschaft des Zertifikats abgerufen wurde, und erstellen Sie die Signatur.</span><span class="sxs-lookup"><span data-stu-id="80d0b-116">Using the [*private key*](../secgloss/p-gly.md) obtained through the property on the certificate, encrypt the digest, creating the signature.</span></span>
7.  <span data-ttu-id="80d0b-117">Fügen Sie Folgendes in die signierte Nachricht ein:</span><span class="sxs-lookup"><span data-stu-id="80d0b-117">Include the following in the signed message:</span></span>

    -   <span data-ttu-id="80d0b-118">Die signierten Daten</span><span class="sxs-lookup"><span data-stu-id="80d0b-118">The signed data</span></span>
    -   <span data-ttu-id="80d0b-119">Der Hash Algorithmus</span><span class="sxs-lookup"><span data-stu-id="80d0b-119">The hash algorithm</span></span>
    -   <span data-ttu-id="80d0b-120">Die Signatur</span><span class="sxs-lookup"><span data-stu-id="80d0b-120">The signature</span></span>
    -   <span data-ttu-id="80d0b-121">Der Signatur Geber Bezeichner (Zertifikat Aussteller und Seriennummer)</span><span class="sxs-lookup"><span data-stu-id="80d0b-121">The signer identifier (certificate issuer and serial number)</span></span>
    -   <span data-ttu-id="80d0b-122">Zertifikat des Signatur Gebers (optional)</span><span class="sxs-lookup"><span data-stu-id="80d0b-122">The signer's certificate (optional)</span></span>

<span data-ttu-id="80d0b-123">Ein ausführliches Verfahren und ein Beispiel finden Sie unter Vorgehensweise: [Signieren von Daten](procedure-for-signing-data.md) und [Beispiel-C-Programm: Signieren einer Nachricht und Überprüfen einer Nachrichten Signatur](example-c-program-signing-a-message-and-verifying-a-message-signature.md).</span><span class="sxs-lookup"><span data-stu-id="80d0b-123">For a detailed procedure and example, see [Procedure for Signing Data](procedure-for-signing-data.md) and [Example C Program: Signing a Message and Verifying a Message Signature](example-c-program-signing-a-message-and-verifying-a-message-signature.md).</span></span>

 

 
