---
description: Blobvorgänge werden mit dem Diffie-Hellman-Anbieter verwendet, um Schlüssel aus dem Kryptografiedienstanbieter (CSP) zu exportieren und Schlüssel in zu importieren.
ms.assetid: 052f2108-d402-41a0-b4ac-e93ba6b06b49
title: Diffie-Hellman von schlüsselblobschlüsseln
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9194a9c12542fc0acf36aa0064a2f3e304e25f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348603"
---
# <a name="diffie-hellman-key-blobs"></a><span data-ttu-id="4b9e7-103">Diffie-Hellman von schlüsselblobschlüsseln</span><span class="sxs-lookup"><span data-stu-id="4b9e7-103">Diffie-Hellman Key BLOBs</span></span>

<span data-ttu-id="4b9e7-104">[*BLOB*](../secgloss/b-gly.md) werden mit dem [*Diffie-Hellman-*](../secgloss/d-gly.md) Anbieter verwendet, um Schlüssel aus dem [*Kryptografiedienstanbieter (kryptografischen Service Provider*](../secgloss/c-gly.md) , CSP) zu exportieren und Schlüssel in zu importieren.</span><span class="sxs-lookup"><span data-stu-id="4b9e7-104">[*BLOBs*](../secgloss/b-gly.md) are used with the [*Diffie-Hellman*](../secgloss/d-gly.md) provider to export keys from, and import keys into, the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span>

-   [<span data-ttu-id="4b9e7-105">Blobschlüssel für öffentliche Schlüssel</span><span class="sxs-lookup"><span data-stu-id="4b9e7-105">Public Key BLOBs</span></span>](#public-key-blobs)
-   [<span data-ttu-id="4b9e7-106">Blobschlüssel für private Schlüssel</span><span class="sxs-lookup"><span data-stu-id="4b9e7-106">Private Key BLOBs</span></span>](#private-key-blobs)

## <a name="public-key-blobs"></a><span data-ttu-id="4b9e7-107">Blobschlüssel für öffentliche Schlüssel</span><span class="sxs-lookup"><span data-stu-id="4b9e7-107">Public Key BLOBs</span></span>

<span data-ttu-id="4b9e7-108">Geben Sie Diffie-Hellman [*BLOBs für öffentliche Schlüssel*](../secgloss/p-gly.md)den Wert **PublicKeyBlob** ein, mit dem der (G ^ X) mod P-Wert in einem Diffie-Hellman-Schlüsselaustausch ausgetauscht wird.</span><span class="sxs-lookup"><span data-stu-id="4b9e7-108">Diffie-Hellman [*public key BLOBs*](../secgloss/p-gly.md), type **PUBLICKEYBLOB**, are used to exchange the (G^X) mod P value in a Diffie-Hellman key exchange.</span></span> <span data-ttu-id="4b9e7-109">Diese Schlüssel werden als Bytefolge im folgenden Format exportiert und importiert.</span><span class="sxs-lookup"><span data-stu-id="4b9e7-109">These keys are exported and imported as a sequence of bytes with the following format.</span></span>

``` syntax
PUBLICKEYSTRUC  publickeystruc; 
DHPUBKEY dhpubkey;
BYTE y[dhpubkey.bitlen/8]; // Where y = (G^X) mod P
```

<span data-ttu-id="4b9e7-110">In der folgenden Tabelle werden die einzelnen Komponenten des [*Schlüssel-BLOBs*](../secgloss/k-gly.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="4b9e7-110">The following table describes each component of the [*key BLOB*](../secgloss/k-gly.md).</span></span>



| <span data-ttu-id="4b9e7-111">Feld</span><span class="sxs-lookup"><span data-stu-id="4b9e7-111">Field</span></span>          | <span data-ttu-id="4b9e7-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4b9e7-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b9e7-113">dhpubkey</span><span class="sxs-lookup"><span data-stu-id="4b9e7-113">dhpubkey</span></span>       | <span data-ttu-id="4b9e7-114">Eine [**dhpubkey**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="4b9e7-114">A [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) structure.</span></span> <span data-ttu-id="4b9e7-115">Der **Magic** -Member sollte auf 0x31484400 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="4b9e7-115">The **magic** member should be set to 0x31484400.</span></span> <span data-ttu-id="4b9e7-116">Dieser Hexadezimalwert ist die [*ASCII*](../secgloss/a-gly.md) -Codierung von "DH1".</span><span class="sxs-lookup"><span data-stu-id="4b9e7-116">This hexadecimal value is the [*ASCII*](../secgloss/a-gly.md) encoding of "DH1".</span></span>                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="4b9e7-117">publickeystruc</span><span class="sxs-lookup"><span data-stu-id="4b9e7-117">publickeystruc</span></span> | <span data-ttu-id="4b9e7-118">Eine [**publickeystruc**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="4b9e7-118">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="4b9e7-119">Y</span><span class="sxs-lookup"><span data-stu-id="4b9e7-119">y</span></span>              | <span data-ttu-id="4b9e7-120">Eine **Byte** Sequenz.</span><span class="sxs-lookup"><span data-stu-id="4b9e7-120">A **BYTE** sequence.</span></span> <span data-ttu-id="4b9e7-121">Der Y-Wert (G ^ X) mod P befindet sich direkt hinter der [**dhpubkey**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) -Struktur und sollte immer die Länge (in Byte) des bitlen-Felds von **dhpubkey** (Bit-Länge von P) dividiert durch acht sein.</span><span class="sxs-lookup"><span data-stu-id="4b9e7-121">The Y value, (G^X) mod P, is located directly after the [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) structure, and should always be the length, in bytes, of the **DHPUBKEY bitlen** field (bit length of P) divided by eight.</span></span> <span data-ttu-id="4b9e7-122">Wenn die Länge der Daten, die sich aus der Berechnung von (G ^ X) mod P ergeben, mindestens ein Byte kürzer als P ist, das durch acht geteilt wird, müssen die Daten mit den erforderlichen Bytes (von NULL Wert) aufgefüllt werden, damit die Daten die gewünschte Länge haben ([*Little-Endian-*](../secgloss/l-gly.md) Format).</span><span class="sxs-lookup"><span data-stu-id="4b9e7-122">If the length of the data that results from the calculation of (G^X) mod P is one or more bytes shorter than P divided by eight, the data must be padded with the necessary bytes (of zero value) to make the data the desired length ([*little-endian*](../secgloss/l-gly.md) format).</span></span> |



 

## <a name="private-key-blobs"></a><span data-ttu-id="4b9e7-123">Blobschlüssel für private Schlüssel</span><span class="sxs-lookup"><span data-stu-id="4b9e7-123">Private Key BLOBs</span></span>

<span data-ttu-id="4b9e7-124">Geben Sie Diffie-Hellman [*privaten Schlüsselblobs*](../secgloss/p-gly.md) **privatekeyblob** ein, die zum Speichern der öffentlichen/privaten Informationen eines Diffie-Hellman Schlüssels verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4b9e7-124">Diffie-Hellman [*private key BLOBs*](../secgloss/p-gly.md), type **PRIVATEKEYBLOB**, are used to store the public/private information of a Diffie-Hellman key.</span></span> <span data-ttu-id="4b9e7-125">Diese Schlüssel werden als Bytefolge im folgenden Format exportiert und importiert.</span><span class="sxs-lookup"><span data-stu-id="4b9e7-125">These keys are exported and imported as a sequence of bytes with the following format.</span></span>

``` syntax
PUBLICKEYSTRUC  publickeystruc; 
DHPUBKEY        dhpubkey;
BYTE            prime[dhpubkey.bitlen/8];
BYTE            generator[dhpubkey.bitlen/8];
BYTE            secret[dhpubkey.bitlen/8];
```

<span data-ttu-id="4b9e7-126">In der folgenden Tabelle werden die einzelnen Komponenten des Schlüssel-BLOBs beschrieben.</span><span class="sxs-lookup"><span data-stu-id="4b9e7-126">The following table describes each component of the key BLOB.</span></span>



| <span data-ttu-id="4b9e7-127">Feld</span><span class="sxs-lookup"><span data-stu-id="4b9e7-127">Field</span></span>          | <span data-ttu-id="4b9e7-128">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4b9e7-128">Description</span></span>                                                                                                                                                                                                  |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b9e7-129">dhpubkey</span><span class="sxs-lookup"><span data-stu-id="4b9e7-129">dhpubkey</span></span>       | <span data-ttu-id="4b9e7-130">Eine [**dhpubkey**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="4b9e7-130">A [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) structure.</span></span> <span data-ttu-id="4b9e7-131">Der **Magic** -Member muss auf 0x32484400 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="4b9e7-131">The **magic** member must be set to 0x32484400.</span></span> <span data-ttu-id="4b9e7-132">Dieser Hexadezimalwert ist die [*ASCII*](../secgloss/a-gly.md) -Codierung von "DH2".</span><span class="sxs-lookup"><span data-stu-id="4b9e7-132">This hexadecimal value is the [*ASCII*](../secgloss/a-gly.md) encoding of "DH2".</span></span> |
| <span data-ttu-id="4b9e7-133">Generator</span><span class="sxs-lookup"><span data-stu-id="4b9e7-133">generator</span></span>      | <span data-ttu-id="4b9e7-134">Eine **Byte** Sequenz.</span><span class="sxs-lookup"><span data-stu-id="4b9e7-134">A **BYTE** sequence.</span></span> <span data-ttu-id="4b9e7-135">Der Generator, G.</span><span class="sxs-lookup"><span data-stu-id="4b9e7-135">The generator, G.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="4b9e7-136">publickeystruc</span><span class="sxs-lookup"><span data-stu-id="4b9e7-136">publickeystruc</span></span> | <span data-ttu-id="4b9e7-137">Eine [**publickeystruc**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="4b9e7-137">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                        |
| <span data-ttu-id="4b9e7-138">wichtigsten</span><span class="sxs-lookup"><span data-stu-id="4b9e7-138">prime</span></span>          | <span data-ttu-id="4b9e7-139">Eine **Byte** Sequenz.</span><span class="sxs-lookup"><span data-stu-id="4b9e7-139">A **BYTE** sequence.</span></span> <span data-ttu-id="4b9e7-140">Der primmodulus (P). Diese Daten müssen immer das signifikanteste Bit aufweisen, das auf eins festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="4b9e7-140">The prime modulus, P. This data must always have the most significant bit of the most significant byte set to one.</span></span>                                                                      |
| <span data-ttu-id="4b9e7-141">secret</span><span class="sxs-lookup"><span data-stu-id="4b9e7-141">secret</span></span>         | <span data-ttu-id="4b9e7-142">Eine **Byte** Sequenz.</span><span class="sxs-lookup"><span data-stu-id="4b9e7-142">A **BYTE** sequence.</span></span> <span data-ttu-id="4b9e7-143">Der geheime Exponent, X.</span><span class="sxs-lookup"><span data-stu-id="4b9e7-143">The secret exponent, X.</span></span>                                                                                                                                                                 |



 

> [!Note]  
> <span data-ttu-id="4b9e7-144">Der Generator und der geheime Schlüssel müssen immer dieselbe Länge haben (in Bytes).</span><span class="sxs-lookup"><span data-stu-id="4b9e7-144">The generator and secret must always have the same length, in bytes.</span></span> <span data-ttu-id="4b9e7-145">Wenn ein Byte oder kürzer als das andere ist, muss es mit der erforderlichen Anzahl von 0 (null) Byte aufgefüllt werden, damit die Werte identisch sind.</span><span class="sxs-lookup"><span data-stu-id="4b9e7-145">If either is one byte or more shorter than the other, it must be padded with the necessary number of zero value bytes to make them the same.</span></span> <span data-ttu-id="4b9e7-146">Der Generator und der geheime Schlüssel sind im [*Little-Endian-*](../secgloss/l-gly.md) Format.</span><span class="sxs-lookup"><span data-stu-id="4b9e7-146">Both the generator and the secret are in [*little-endian*](../secgloss/l-gly.md) format.</span></span>

 

 

 
