---
description: Die Verschlüsselung ist der Prozess der Übersetzung von Klartext-Daten (Klartext) in etwas, das zufällig und bedeutungslos erscheint (Chiffre Text). Bei der Entschlüsselung handelt es sich um den Prozess, bei dem Chiffre Text zurück in Klartext umgerechnet wird.
ms.assetid: 6a4b5c82-f74c-4cc8-b824-690f165453bd
title: Verschlüsselung und Entschlüsselung von Daten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfa6f9633cabf4a41aec59d9224c2579acb7a983
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128792"
---
# <a name="data-encryption-and-decryption"></a><span data-ttu-id="4ec7a-104">Verschlüsselung und Entschlüsselung von Daten</span><span class="sxs-lookup"><span data-stu-id="4ec7a-104">Data Encryption and Decryption</span></span>

<span data-ttu-id="4ec7a-105">Die Verschlüsselung ist der Prozess der Übersetzung von Klartext-[*Daten (Klartext*](../secgloss/p-gly.md)) in etwas, das zufällig und bedeutungslos erscheint ([*Chiffre Text*](../secgloss/c-gly.md)).</span><span class="sxs-lookup"><span data-stu-id="4ec7a-105">Encryption is the process of translating plain text data ([*plaintext*](../secgloss/p-gly.md)) into something that appears to be random and meaningless ([*ciphertext*](../secgloss/c-gly.md)).</span></span> <span data-ttu-id="4ec7a-106">Bei der Entschlüsselung handelt es sich um den Prozess, bei dem Chiffre Text zurück in Klartext umgerechnet wird.</span><span class="sxs-lookup"><span data-stu-id="4ec7a-106">Decryption is the process of converting ciphertext back to plaintext.</span></span>

<span data-ttu-id="4ec7a-107">Zum Verschlüsseln von mehr als einer kleinen Datenmenge wird die [*symmetrische Verschlüsselung*](../secgloss/s-gly.md) verwendet.</span><span class="sxs-lookup"><span data-stu-id="4ec7a-107">To encrypt more than a small amount of data, [*symmetric encryption*](../secgloss/s-gly.md) is used.</span></span> <span data-ttu-id="4ec7a-108">Ein [*symmetrischer Schlüssel*](../secgloss/s-gly.md) wird während der Verschlüsselungs-und Entschlüsselungs Prozesse verwendet.</span><span class="sxs-lookup"><span data-stu-id="4ec7a-108">A [*symmetric key*](../secgloss/s-gly.md) is used during both the encryption and decryption processes.</span></span> <span data-ttu-id="4ec7a-109">Zum Entschlüsseln eines bestimmten Chiffre Texts muss der Schlüssel verwendet werden, der zum Verschlüsseln der Daten verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="4ec7a-109">To decrypt a particular piece of ciphertext, the key that was used to encrypt the data must be used.</span></span>

<span data-ttu-id="4ec7a-110">Das Ziel der einzelnen Verschlüsselungsalgorithmen besteht darin, den generierten Chiffre Text ohne Verwendung des Schlüssels so schwierig wie möglich zu entschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="4ec7a-110">The goal of every encryption algorithm is to make it as difficult as possible to decrypt the generated ciphertext without using the key.</span></span> <span data-ttu-id="4ec7a-111">Wenn ein wirklich guter Verschlüsselungsalgorithmus verwendet wird, gibt es keine Technik, die wesentlich besser ist als methodisch versucht, jeden möglichen Schlüssel zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="4ec7a-111">If a really good encryption algorithm is used, there is no technique significantly better than methodically trying every possible key.</span></span> <span data-ttu-id="4ec7a-112">Bei einem solchen Algorithmus ist der Schlüssel umso schwieriger, wenn ein Teil des Chiffre Texts entschlüsselt wird, ohne den Schlüssel zu besitzen.</span><span class="sxs-lookup"><span data-stu-id="4ec7a-112">For such an algorithm, the longer the key, the more difficult it is to decrypt a piece of ciphertext without possessing the key.</span></span>

<span data-ttu-id="4ec7a-113">Es ist schwierig, die Qualität eines Verschlüsselungsalgorithmus zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="4ec7a-113">It is difficult to determine the quality of an encryption algorithm.</span></span> <span data-ttu-id="4ec7a-114">Algorithmen, die vielversprechend aussehen, werden bei einem angemessenen Angriff manchmal sehr einfach zu unterbrechen.</span><span class="sxs-lookup"><span data-stu-id="4ec7a-114">Algorithms that look promising sometimes turn out to be very easy to break, given the proper attack.</span></span> <span data-ttu-id="4ec7a-115">Wenn Sie einen Verschlüsselungsalgorithmus auswählen, empfiehlt es sich, einen Wert auszuwählen, der bereits seit mehreren Jahren verwendet wurde, und sich erfolgreich gegen alle Angriffe gewehrt hat.</span><span class="sxs-lookup"><span data-stu-id="4ec7a-115">When selecting an encryption algorithm, it is a good idea to choose one that has been in use for several years and has successfully resisted all attacks.</span></span>

<span data-ttu-id="4ec7a-116">Weitere Informationen finden Sie unter [Datenverschlüsselungs-und Entschlüsselungs Funktionen](cryptography-functions.md).</span><span class="sxs-lookup"><span data-stu-id="4ec7a-116">For more information, see [Data Encryption and Decryption Functions](cryptography-functions.md).</span></span>

 

 
