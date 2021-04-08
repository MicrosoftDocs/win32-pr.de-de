---
description: BLOB werden mit dem Diffie-Hellman/SChannel-Anbieter verwendet, um Schlüssel aus dem Kryptografiedienstanbieter (kryptografischen Service Provider, CSP) zu exportieren und Schlüssel in zu importieren.
ms.assetid: ebb85b7c-204d-4b1c-86dc-5a03c8eda47b
title: Diffie-Hellman/SChannel-Schlüsselblob
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65a76869c6c6239e17a5ae14921805a076c9381c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756535"
---
# <a name="diffie-hellmanschannel-key-blobs"></a><span data-ttu-id="2bec5-103">Diffie-Hellman/SChannel-Schlüsselblob</span><span class="sxs-lookup"><span data-stu-id="2bec5-103">Diffie-Hellman/Schannel Key BLOBs</span></span>

<span data-ttu-id="2bec5-104">[*BLOB*](../secgloss/b-gly.md) werden mit dem [*Diffie-Hellman*](../secgloss/d-gly.md) / [*SChannel*](../secgloss/s-gly.md) -Anbieter verwendet, um Schlüssel aus dem [*Kryptografiedienstanbieter (kryptografischen Service Provider*](../secgloss/c-gly.md) , CSP) zu exportieren und Schlüssel in zu importieren.</span><span class="sxs-lookup"><span data-stu-id="2bec5-104">[*BLOBs*](../secgloss/b-gly.md) are used with the [*Diffie-Hellman*](../secgloss/d-gly.md)/[*Schannel*](../secgloss/s-gly.md) provider to export keys from, and import keys into, the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span>

-   [<span data-ttu-id="2bec5-105">Blobschlüssel für öffentliche Schlüssel</span><span class="sxs-lookup"><span data-stu-id="2bec5-105">Public Key BLOBs</span></span>](#public-key-blobs)
-   [<span data-ttu-id="2bec5-106">Blobschlüssel für private Schlüssel</span><span class="sxs-lookup"><span data-stu-id="2bec5-106">Private Key BLOBs</span></span>](#private-key-blobs)

## <a name="public-key-blobs"></a><span data-ttu-id="2bec5-107">Blobschlüssel für öffentliche Schlüssel</span><span class="sxs-lookup"><span data-stu-id="2bec5-107">Public Key BLOBs</span></span>

<span data-ttu-id="2bec5-108">Geben Sie Diffie-Hellman [*BLOBs für öffentliche Schlüssel*](../secgloss/p-gly.md)den Wert **PublicKeyBlob** ein, mit dem der (G ^ X) mod P-Wert in einem Diffie-Hellman-Schlüsselaustausch ausgetauscht wird.</span><span class="sxs-lookup"><span data-stu-id="2bec5-108">Diffie-Hellman [*public key BLOBs*](../secgloss/p-gly.md), type **PUBLICKEYBLOB**, are used to exchange the (G^X) mod P value in a Diffie-Hellman key exchange.</span></span> <span data-ttu-id="2bec5-109">Diese Schlüssel werden als Bytefolge im folgenden Format exportiert und importiert.</span><span class="sxs-lookup"><span data-stu-id="2bec5-109">These keys are exported and imported as a sequence of bytes with the following format.</span></span>

``` syntax
PUBLICKEYSTRUC  publickeystruc;
DHPUBKEY        dhpubkey;
BYTE            y[dhpubkey.bitlen/8]; // Where y = (G^X) mod P
```

<span data-ttu-id="2bec5-110">In der folgenden Tabelle werden die einzelnen Komponenten des [*Schlüssel-BLOBs*](../secgloss/k-gly.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="2bec5-110">The following table describes each component of the [*key BLOB*](../secgloss/k-gly.md).</span></span>



| <span data-ttu-id="2bec5-111">Feld</span><span class="sxs-lookup"><span data-stu-id="2bec5-111">Field</span></span>          | <span data-ttu-id="2bec5-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2bec5-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2bec5-113">dhpubkey</span><span class="sxs-lookup"><span data-stu-id="2bec5-113">dhpubkey</span></span>       | <span data-ttu-id="2bec5-114">Eine [**dhpubkey**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="2bec5-114">A [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) structure.</span></span> <span data-ttu-id="2bec5-115">Der **Magic** -Member muss auf 0x31484400 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="2bec5-115">The **magic** member must be set to 0x31484400.</span></span> <span data-ttu-id="2bec5-116">Dieser Hexadezimalwert ist die [*ASCII*](../secgloss/a-gly.md) -Codierung von DH1.</span><span class="sxs-lookup"><span data-stu-id="2bec5-116">This hexadecimal value is the [*ASCII*](../secgloss/a-gly.md) encoding of DH1.</span></span>                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="2bec5-117">publickeystruc</span><span class="sxs-lookup"><span data-stu-id="2bec5-117">publickeystruc</span></span> | <span data-ttu-id="2bec5-118">Eine [**publickeystruc**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="2bec5-118">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="2bec5-119">Y</span><span class="sxs-lookup"><span data-stu-id="2bec5-119">y</span></span>              | <span data-ttu-id="2bec5-120">Eine **Byte** Sequenz.</span><span class="sxs-lookup"><span data-stu-id="2bec5-120">A **BYTE** sequence.</span></span> <span data-ttu-id="2bec5-121">Der y-Wert (G ^ X) mod P befindet sich direkt hinter der [**dhpubkey**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="2bec5-121">The y value, (G^X) mod P, is located directly after the [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) structure.</span></span> <span data-ttu-id="2bec5-122">Die Länge (in Byte) der Sequenz ist das **bitlen** -Element von **dhpubkey** , dividiert durch acht.</span><span class="sxs-lookup"><span data-stu-id="2bec5-122">The length, in bytes, of the sequence is the **bitlen** member of **DHPUBKEY** divided by eight.</span></span> <span data-ttu-id="2bec5-123">Wenn die Länge der Daten, die sich aus der Berechnung von (G ^ X) mod P ergeben, mindestens ein Byte kürzer als P ist, das durch acht geteilt wird, müssen die Daten mit den erforderlichen Bytes (von NULL Wert) aufgefüllt werden, damit die Daten die gewünschte Länge haben ([*Little-Endian-*](../secgloss/l-gly.md) Format).</span><span class="sxs-lookup"><span data-stu-id="2bec5-123">If the length of the data that results from the calculation of (G^X) mod P is one or more bytes shorter than P divided by eight, the data must be padded with the necessary bytes (of zero value) to make the data the desired length ([*little-endian*](../secgloss/l-gly.md) format).</span></span> |



 

## <a name="private-key-blobs"></a><span data-ttu-id="2bec5-124">Blobschlüssel für private Schlüssel</span><span class="sxs-lookup"><span data-stu-id="2bec5-124">Private Key BLOBs</span></span>

<span data-ttu-id="2bec5-125">[*BLOBs für private Schlüssel*](../secgloss/p-gly.md)von d-h, Typ **privatekeyblob**, werden zum Exportieren und importieren privater Informationen eines D-H-Schlüssels verwendet.</span><span class="sxs-lookup"><span data-stu-id="2bec5-125">D-H [*private key BLOBs*](../secgloss/p-gly.md), type **PRIVATEKEYBLOB**, are used to export and import private information of a D-H key.</span></span> <span data-ttu-id="2bec5-126">Diese Schlüssel werden als Bytefolge im folgenden Format exportiert und importiert.</span><span class="sxs-lookup"><span data-stu-id="2bec5-126">These keys are exported and imported as a sequence of bytes with the following format.</span></span>

``` syntax
PUBLICKEYSTRUC  publickeystruc;
DHPUBKEY        dhpubkey;
BYTE            prime[dhpubkey.bitlen/8];
BYTE            generator[dhpubkey.bitlen/8];
BYTE            secret[dhpubkey.bitlen/8];
```

<span data-ttu-id="2bec5-127">In der folgenden Tabelle werden die einzelnen Komponenten des Schlüssel-BLOBs beschrieben.</span><span class="sxs-lookup"><span data-stu-id="2bec5-127">The following table describes each component of the key BLOB.</span></span>



| <span data-ttu-id="2bec5-128">Feld</span><span class="sxs-lookup"><span data-stu-id="2bec5-128">Field</span></span>          | <span data-ttu-id="2bec5-129">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2bec5-129">Description</span></span>                                                                                                                                                                                                |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2bec5-130">dhpubkey</span><span class="sxs-lookup"><span data-stu-id="2bec5-130">dhpubkey</span></span>       | <span data-ttu-id="2bec5-131">Eine [**dhpubkey**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="2bec5-131">A [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) structure.</span></span> <span data-ttu-id="2bec5-132">Der **Magic** -Member muss auf 0x32484400 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="2bec5-132">The **magic** member must be set to 0x32484400.</span></span> <span data-ttu-id="2bec5-133">Dieser Hexadezimalwert ist die [*ASCII*](../secgloss/a-gly.md) -Codierung von DH2.</span><span class="sxs-lookup"><span data-stu-id="2bec5-133">This hexadecimal value is the [*ASCII*](../secgloss/a-gly.md) encoding of DH2.</span></span> |
| <span data-ttu-id="2bec5-134">Generator</span><span class="sxs-lookup"><span data-stu-id="2bec5-134">generator</span></span>      | <span data-ttu-id="2bec5-135">Eine **Byte** Sequenz.</span><span class="sxs-lookup"><span data-stu-id="2bec5-135">A **BYTE** sequence.</span></span> <span data-ttu-id="2bec5-136">Der Generator G.</span><span class="sxs-lookup"><span data-stu-id="2bec5-136">The generator G.</span></span>                                                                                                                                                                      |
| <span data-ttu-id="2bec5-137">publickeystruc</span><span class="sxs-lookup"><span data-stu-id="2bec5-137">publickeystruc</span></span> | <span data-ttu-id="2bec5-138">Eine [**publickeystruc**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="2bec5-138">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                      |
| <span data-ttu-id="2bec5-139">wichtigsten</span><span class="sxs-lookup"><span data-stu-id="2bec5-139">prime</span></span>          | <span data-ttu-id="2bec5-140">Eine **Byte** Sequenz.</span><span class="sxs-lookup"><span data-stu-id="2bec5-140">A **BYTE** sequence.</span></span> <span data-ttu-id="2bec5-141">Der primmodulus (P). Diese Daten müssen immer das signifikanteste Bit aufweisen, das auf eins festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="2bec5-141">The prime modulus, P. This data must always have the most significant bit of the most significant byte set to one.</span></span>                                                                    |
| <span data-ttu-id="2bec5-142">secret</span><span class="sxs-lookup"><span data-stu-id="2bec5-142">secret</span></span>         | <span data-ttu-id="2bec5-143">Eine **Byte** Sequenz.</span><span class="sxs-lookup"><span data-stu-id="2bec5-143">A **BYTE** sequence.</span></span> <span data-ttu-id="2bec5-144">Der geheime Exponent X.</span><span class="sxs-lookup"><span data-stu-id="2bec5-144">The secret exponent X.</span></span>                                                                                                                                                                |



 

> [!Note]  
> <span data-ttu-id="2bec5-145">Der primwert, der Generator und der geheime Wert müssen immer dieselbe Länge haben (in Bytes).</span><span class="sxs-lookup"><span data-stu-id="2bec5-145">The prime, generator, and secret values must always have the same length, in bytes.</span></span> <span data-ttu-id="2bec5-146">Wenn ein Wert ein Byte oder kürzer als der andere Wert ist, muss er mit der erforderlichen Anzahl von 0 Bytes aufgefüllt werden, damit diese identisch sind.</span><span class="sxs-lookup"><span data-stu-id="2bec5-146">If any value is one byte or more shorter than the others, it must be padded with the necessary number of zero bytes to make them the same.</span></span> <span data-ttu-id="2bec5-147">Die Primzahl, der Generator und das Geheimnis liegen im [*Little-Endian-*](../secgloss/l-gly.md) Format vor.</span><span class="sxs-lookup"><span data-stu-id="2bec5-147">The prime, generator, and secret are in [*little-endian*](../secgloss/l-gly.md) format.</span></span>

 

 

 
