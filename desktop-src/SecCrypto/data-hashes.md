---
description: Ein Hash eines Texts oder einer anderen Byte Zeichenfolge ist ein zugeordneter, statistisch eindeutiger Wert mit fester Länge.
ms.assetid: e54d5a3b-cae1-47dd-a565-7bf1ccef7f52
title: Datenhashes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed785c79bef67f5a54b0d91c0c2686f8fd1b967f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868427"
---
# <a name="data-hashes"></a><span data-ttu-id="87a08-103">Datenhashes</span><span class="sxs-lookup"><span data-stu-id="87a08-103">Data Hashes</span></span>

<span data-ttu-id="87a08-104">Ein [*Hash*](../secgloss/h-gly.md) eines Texts oder einer anderen Byte Zeichenfolge ist ein zugeordneter, statistisch eindeutiger Wert mit fester Länge.</span><span class="sxs-lookup"><span data-stu-id="87a08-104">A [*hash*](../secgloss/h-gly.md) of a text or other string of bytes is an associated, statistically unique, fixed-length value.</span></span> <span data-ttu-id="87a08-105">In einigen Dokumenten wird ein *Hashwert* eines Texts auch als Digest bezeichnet. in dieser Dokumentation wird jedoch immer der Begriff Hash verwendet.</span><span class="sxs-lookup"><span data-stu-id="87a08-105">In some documents, a *hash* of a text is also called a digest; however, in this documentation the term hash will always be used.</span></span> <span data-ttu-id="87a08-106">CryptoAPI-Funktionen bieten die Möglichkeit, einen Hashwert für beliebige Text oder andere Zeichen folgen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="87a08-106">CryptoAPI functions provide a means to create a hash for any text or other string of bytes.</span></span> <span data-ttu-id="87a08-107">Dieser Hash kann dann als eindeutiger Bezeichner der zugehörigen Daten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="87a08-107">That hash, then, can be used as a unique identifier of its associated data.</span></span>

<span data-ttu-id="87a08-108">Um die [*Integrität*](../secgloss/i-gly.md) eines Texts sicherzustellen, kann ein [*Hash*](../secgloss/h-gly.md) eines Texts an den Text gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="87a08-108">To ensure the [*integrity*](../secgloss/i-gly.md) of a text, a [*hash*](../secgloss/h-gly.md) of a text can be sent to accompany the text.</span></span> <span data-ttu-id="87a08-109">Der Empfänger kann dann einen Hashwert für die empfangenen Daten berechnen und den mit dem empfangenen Hash berechneten Hash vergleichen.</span><span class="sxs-lookup"><span data-stu-id="87a08-109">The receiver can then compute a hash on the data received and compare the hash computed with the hash received.</span></span> <span data-ttu-id="87a08-110">Wenn die beiden Übereinstimmungen vorliegen, müssen die empfangenen Daten mit den Daten übereinstimmen, aus denen der empfangene Hash erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="87a08-110">If the two match, the data received must be the same as the data from which the received hash was created.</span></span>

<span data-ttu-id="87a08-111">Um einen Hashwert zu erhalten, erstellen Sie mithilfe von " [**cryptkreatehash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash)" ein Hash Objekt.</span><span class="sxs-lookup"><span data-stu-id="87a08-111">To obtain a hash value, create a hash object using [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash).</span></span> <span data-ttu-id="87a08-112">Mit diesem Objekt werden die zu überprüfenden Daten gesammelt.</span><span class="sxs-lookup"><span data-stu-id="87a08-112">This object will accumulate the data to be verified.</span></span> <span data-ttu-id="87a08-113">Die Daten werden dann mit der [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) -Funktion dem Hash Objekt hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="87a08-113">The data is then added to the hash object with the [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) function.</span></span>

<span data-ttu-id="87a08-114">Nachdem der letzte Datenblock dem Hash hinzugefügt wurde, wird die [**cryptgethashparam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgethashparam) -Funktion verwendet, um den Hashwert der Daten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="87a08-114">After the last block of data is added to the hash, the [**CryptGetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgethashparam) function is used to obtain the hash value of the data.</span></span>

<span data-ttu-id="87a08-115">Eine bessere Sicherheit wird gewährleistet, indem das Hash Objekt mit [**cryptdestroyhash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash) zerstört wird, sobald der Hashwert abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="87a08-115">Better security is provided by destroying the hash object with [**CryptDestroyHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash) as soon as the hash value has been obtained.</span></span>

 

 
