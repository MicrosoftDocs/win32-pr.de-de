---
description: Wird mit dem DSS-Anbieter (Digital Signature Standard) zum Exportieren von Schlüsseln aus und Importieren von Schlüsseln in den Kryptografiedienstanbieter (kryptografischen Service Provider, CSP) verwendet.
ms.assetid: a0a266ef-0830-4a3f-9bf6-6b64c95c3d03
title: Schlüssel-blobschlüssel des DSS-Anbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f27a73e35cccd6fad672f4c94d589d754f970c0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958838"
---
# <a name="dss-provider-key-blobs"></a><span data-ttu-id="98a68-103">Schlüssel-blobschlüssel des DSS-Anbieters</span><span class="sxs-lookup"><span data-stu-id="98a68-103">DSS Provider Key BLOBs</span></span>

<span data-ttu-id="98a68-104">[*Blobvorgänge*](../secgloss/b-gly.md) werden mit dem DSS-Anbieter ( [*Digital Signature Standard*](../secgloss/d-gly.md) ) zum Exportieren von Schlüsseln und Importieren von Schlüsseln in den [*Kryptografiedienstanbieter (kryptografischen Service Provider*](../secgloss/c-gly.md) , CSP) verwendet.</span><span class="sxs-lookup"><span data-stu-id="98a68-104">[*BLOBs*](../secgloss/b-gly.md) are used with the [*Digital Signature Standard*](../secgloss/d-gly.md) (DSS) provider to export keys from, and import keys into, the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span>

-   [<span data-ttu-id="98a68-105">Blobschlüssel für öffentliche Schlüssel</span><span class="sxs-lookup"><span data-stu-id="98a68-105">Public Key BLOBs</span></span>](#public-key-blobs)
-   [<span data-ttu-id="98a68-106">Blobschlüssel für private Schlüssel</span><span class="sxs-lookup"><span data-stu-id="98a68-106">Private Key BLOBs</span></span>](#private-key-blobs)

## <a name="public-key-blobs"></a><span data-ttu-id="98a68-107">Blobschlüssel für öffentliche Schlüssel</span><span class="sxs-lookup"><span data-stu-id="98a68-107">Public Key BLOBs</span></span>

<span data-ttu-id="98a68-108">Ein öffentlicher DSS- [*Schlüssel*](../secgloss/p-gly.md) wird exportiert und als BLOB importiert, eine Folge von Bytes, die wie folgt strukturiert ist.</span><span class="sxs-lookup"><span data-stu-id="98a68-108">A DSS [*public key*](../secgloss/p-gly.md) is exported and imported as a BLOB, a sequence of bytes structured as follows.</span></span>

``` syntax
PUBLICKEYSTRUC    publickeystruc;
DSSPUBKEY         dsspubkey;
BYTE              p[dsspubkey.bitlen/8];
BYTE              q[20];
BYTE              g[dsspubkey.bitlen/8];
BYTE              y[dsspubkey.bitlen/8];
DSSSEED           seedstruct;
```

<span data-ttu-id="98a68-109">In der folgenden Tabelle werden diese Komponenten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="98a68-109">The following table describes these components.</span></span> <span data-ttu-id="98a68-110">Alle Werte liegen im [*Little-Endian-*](../secgloss/l-gly.md) Format vor.</span><span class="sxs-lookup"><span data-stu-id="98a68-110">All values are in [*little-endian*](../secgloss/l-gly.md) format.</span></span>



| <span data-ttu-id="98a68-111">Feld</span><span class="sxs-lookup"><span data-stu-id="98a68-111">Field</span></span>          | <span data-ttu-id="98a68-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="98a68-112">Description</span></span>                                                                                                                                                                                                          |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98a68-113">dsspubkey</span><span class="sxs-lookup"><span data-stu-id="98a68-113">dsspubkey</span></span>      | <span data-ttu-id="98a68-114">Eine [**dsspubkey**](/previous-versions/windows/desktop/legacy/aa381982(v=vs.85)) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="98a68-114">A [**DSSPUBKEY**](/previous-versions/windows/desktop/legacy/aa381982(v=vs.85)) structure.</span></span> <span data-ttu-id="98a68-115">Der **magische** Member muss den Wert 0x31535344 aufweisen.</span><span class="sxs-lookup"><span data-stu-id="98a68-115">The **magic** member must have a value of 0x31535344.</span></span> <span data-ttu-id="98a68-116">Diese hexadezimal Zahl ist die [*ASCII*](../secgloss/a-gly.md) -Codierung von DSS1.</span><span class="sxs-lookup"><span data-stu-id="98a68-116">This hexadecimal number is the [*ASCII*](../secgloss/a-gly.md) encoding of DSS1.</span></span> |
| <span data-ttu-id="98a68-117">g</span><span class="sxs-lookup"><span data-stu-id="98a68-117">g</span></span>              | <span data-ttu-id="98a68-118">Eine **Byte** Sequenz.</span><span class="sxs-lookup"><span data-stu-id="98a68-118">A **BYTE** sequence.</span></span> <span data-ttu-id="98a68-119">Der Generator, g.</span><span class="sxs-lookup"><span data-stu-id="98a68-119">The generator, g.</span></span> <span data-ttu-id="98a68-120">Muss dieselbe Länge wie p aufweisen.</span><span class="sxs-lookup"><span data-stu-id="98a68-120">Must be the same length as p.</span></span> <span data-ttu-id="98a68-121">Wenn Sie nicht die gleiche Länge wie p hat, muss Sie mit 0x00 Bytes aufgefüllt werden.</span><span class="sxs-lookup"><span data-stu-id="98a68-121">If it is not the same length as p, then it must be padded with 0x00 bytes.</span></span>                                                                      |
| <span data-ttu-id="98a68-122">p</span><span class="sxs-lookup"><span data-stu-id="98a68-122">p</span></span>              | <span data-ttu-id="98a68-123">Eine **Byte** Sequenz.</span><span class="sxs-lookup"><span data-stu-id="98a68-123">A **BYTE** sequence.</span></span> <span data-ttu-id="98a68-124">Der primmodulus (p).</span><span class="sxs-lookup"><span data-stu-id="98a68-124">The prime modulus, p.</span></span> <span data-ttu-id="98a68-125">Das signifikanteste Bit des signifikantesten muss auf 1 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="98a68-125">The most significant bit of the most significant byte must be set to one.</span></span>                                                                                                 |
| <span data-ttu-id="98a68-126">publickeystruc</span><span class="sxs-lookup"><span data-stu-id="98a68-126">publickeystruc</span></span> | <span data-ttu-id="98a68-127">Eine [**publickeystruc**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="98a68-127">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                                |
| <span data-ttu-id="98a68-128">q</span><span class="sxs-lookup"><span data-stu-id="98a68-128">q</span></span>              | <span data-ttu-id="98a68-129">Eine **Byte** Sequenz.</span><span class="sxs-lookup"><span data-stu-id="98a68-129">A **BYTE** sequence.</span></span> <span data-ttu-id="98a68-130">Die Länge von Primzahlen, q, 20 Bytes.</span><span class="sxs-lookup"><span data-stu-id="98a68-130">The prime, q, 20 bytes in length.</span></span> <span data-ttu-id="98a68-131">Das signifikanteste Bit des signifikantesten muss auf 1 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="98a68-131">The most significant bit of the most significant byte must be set to one.</span></span>                                                                                     |
| <span data-ttu-id="98a68-132">seedstruct</span><span class="sxs-lookup"><span data-stu-id="98a68-132">seedstruct</span></span>     | <span data-ttu-id="98a68-133">Eine [**dssseed**](/windows/desktop/api/Wincrypt/ns-wincrypt-dssseed) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="98a68-133">A [**DSSSEED**](/windows/desktop/api/Wincrypt/ns-wincrypt-dssseed) structure.</span></span> <span data-ttu-id="98a68-134">Seed-und Counter-Werte zum Überprüfen von primes.</span><span class="sxs-lookup"><span data-stu-id="98a68-134">Seed and counter values for verifying primes.</span></span>                                                                                                                                |
| <span data-ttu-id="98a68-135">Y</span><span class="sxs-lookup"><span data-stu-id="98a68-135">y</span></span>              | <span data-ttu-id="98a68-136">Eine **Byte** Sequenz.</span><span class="sxs-lookup"><span data-stu-id="98a68-136">A **BYTE** sequence.</span></span> <span data-ttu-id="98a68-137">Der öffentliche Schlüssel y.</span><span class="sxs-lookup"><span data-stu-id="98a68-137">The public key, y.</span></span> <span data-ttu-id="98a68-138">Muss dieselbe Länge wie p aufweisen.</span><span class="sxs-lookup"><span data-stu-id="98a68-138">Must be same length as p.</span></span> <span data-ttu-id="98a68-139">Wenn Sie nicht die gleiche Länge wie p hat, muss Sie mit 0x00 Bytes aufgefüllt werden.</span><span class="sxs-lookup"><span data-stu-id="98a68-139">If it is not the same length as p, then it must be padded with 0x00 bytes.</span></span>                                                                         |



 

> [!Note]  
> <span data-ttu-id="98a68-140">[*Blobblobschlüssel für öffentliche Schlüssel*](../secgloss/p-gly.md) werden nicht verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="98a68-140">[*Public key BLOBs*](../secgloss/p-gly.md) are not encrypted.</span></span> <span data-ttu-id="98a68-141">Sie enthalten öffentliche Schlüssel als [*Klartext*](../secgloss/p-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="98a68-141">They contain public keys in [*plaintext*](../secgloss/p-gly.md) form.</span></span>

 

## <a name="private-key-blobs"></a><span data-ttu-id="98a68-142">Blobschlüssel für private Schlüssel</span><span class="sxs-lookup"><span data-stu-id="98a68-142">Private Key BLOBs</span></span>

<span data-ttu-id="98a68-143">Ein privater DSS- [*Schlüssel*](../secgloss/p-gly.md) wird exportiert und als Sequenz von Bytes importiert, die wie folgt strukturiert ist.</span><span class="sxs-lookup"><span data-stu-id="98a68-143">A DSS [*private key*](../secgloss/p-gly.md) is exported and imported as a sequence of bytes structured as follows.</span></span>

``` syntax
PUBLICKEYSTRUC    publickeystruc;
DSSPUBKEY         dsspubkey;
BYTE              p[dsspubkey.bitlen/8];
BYTE              q[20];
BYTE              g[dsspubkey.bitlen/8];
BYTE              x[20];
DSSSEED           seedstruct;
```

<span data-ttu-id="98a68-144">In der folgenden Tabelle werden die einzelnen Komponenten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="98a68-144">The following table describes each component.</span></span> <span data-ttu-id="98a68-145">Alle Werte liegen im [*Little-Endian-*](../secgloss/l-gly.md) Format vor.</span><span class="sxs-lookup"><span data-stu-id="98a68-145">All values are in [*little-endian*](../secgloss/l-gly.md) format.</span></span>



| <span data-ttu-id="98a68-146">Feld</span><span class="sxs-lookup"><span data-stu-id="98a68-146">Field</span></span>          | <span data-ttu-id="98a68-147">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="98a68-147">Description</span></span>                                                                                                                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98a68-148">dsspubkey</span><span class="sxs-lookup"><span data-stu-id="98a68-148">dsspubkey</span></span>      | <span data-ttu-id="98a68-149">Eine [**dsspubkey**](/previous-versions/windows/desktop/legacy/aa381982(v=vs.85)) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="98a68-149">A [**DSSPUBKEY**](/previous-versions/windows/desktop/legacy/aa381982(v=vs.85)) structure.</span></span> <span data-ttu-id="98a68-150">Der **Magic** -Member muss auf 0x32535344 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="98a68-150">The **magic** member must be set to 0x32535344.</span></span> <span data-ttu-id="98a68-151">Diese hexadezimal Zahl ist die [*ASCII*](../secgloss/a-gly.md) -Codierung von DSS2.</span><span class="sxs-lookup"><span data-stu-id="98a68-151">This hexadecimal number is the [*ASCII*](../secgloss/a-gly.md) encoding of DSS2.</span></span> |
| <span data-ttu-id="98a68-152">g</span><span class="sxs-lookup"><span data-stu-id="98a68-152">g</span></span>              | <span data-ttu-id="98a68-153">Eine **Byte** Sequenz.</span><span class="sxs-lookup"><span data-stu-id="98a68-153">A **BYTE** sequence.</span></span> <span data-ttu-id="98a68-154">Der Generator, g.</span><span class="sxs-lookup"><span data-stu-id="98a68-154">The generator, g.</span></span> <span data-ttu-id="98a68-155">Muss dieselbe Länge wie p aufweisen.</span><span class="sxs-lookup"><span data-stu-id="98a68-155">Must be the same length as p.</span></span> <span data-ttu-id="98a68-156">Wenn Sie nicht die gleiche Länge wie p hat, muss Sie mit 0x00 Bytes aufgefüllt werden.</span><span class="sxs-lookup"><span data-stu-id="98a68-156">If it is not the same length as p, then it must be padded with 0x00 bytes.</span></span>                                                                |
| <span data-ttu-id="98a68-157">publickeystruc</span><span class="sxs-lookup"><span data-stu-id="98a68-157">publickeystruc</span></span> | <span data-ttu-id="98a68-158">Eine [**publickeystruc**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="98a68-158">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                          |
| <span data-ttu-id="98a68-159">p</span><span class="sxs-lookup"><span data-stu-id="98a68-159">p</span></span>              | <span data-ttu-id="98a68-160">Eine **Byte** Sequenz.</span><span class="sxs-lookup"><span data-stu-id="98a68-160">A **BYTE** sequence.</span></span> <span data-ttu-id="98a68-161">Der primmodulus (p).</span><span class="sxs-lookup"><span data-stu-id="98a68-161">The prime modulus, p.</span></span> <span data-ttu-id="98a68-162">Das signifikanteste Bit des signifikantesten muss auf 1 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="98a68-162">The most significant bit of the most significant byte must be set to one.</span></span>                                                                                           |
| <span data-ttu-id="98a68-163">q</span><span class="sxs-lookup"><span data-stu-id="98a68-163">q</span></span>              | <span data-ttu-id="98a68-164">Eine **Byte** Sequenz.</span><span class="sxs-lookup"><span data-stu-id="98a68-164">A **BYTE** sequence.</span></span> <span data-ttu-id="98a68-165">Die Primzahl, f.</span><span class="sxs-lookup"><span data-stu-id="98a68-165">The prime, q.</span></span> <span data-ttu-id="98a68-166">q ist eine Länge von 20 Bytes.</span><span class="sxs-lookup"><span data-stu-id="98a68-166">q is 20 bytes in length.</span></span> <span data-ttu-id="98a68-167">Das signifikanteste Bit des signifikantesten muss auf 1 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="98a68-167">The most significant bit of the most significant byte must be set to one.</span></span>                                                                          |
| <span data-ttu-id="98a68-168">seedstruct</span><span class="sxs-lookup"><span data-stu-id="98a68-168">seedstruct</span></span>     | <span data-ttu-id="98a68-169">Eine [**dssseed**](/windows/desktop/api/Wincrypt/ns-wincrypt-dssseed) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="98a68-169">A [**DSSSEED**](/windows/desktop/api/Wincrypt/ns-wincrypt-dssseed) structure.</span></span> <span data-ttu-id="98a68-170">Seed-und Counter-Werte zum Überprüfen von primes.</span><span class="sxs-lookup"><span data-stu-id="98a68-170">Seed and counter values for verifying primes.</span></span>                                                                                                                          |
| <span data-ttu-id="98a68-171">x</span><span class="sxs-lookup"><span data-stu-id="98a68-171">x</span></span>              | <span data-ttu-id="98a68-172">Eine **Byte** Sequenz.</span><span class="sxs-lookup"><span data-stu-id="98a68-172">A **BYTE** sequence.</span></span> <span data-ttu-id="98a68-173">Der geheime Exponent, x.</span><span class="sxs-lookup"><span data-stu-id="98a68-173">The secret exponent, x.</span></span> <span data-ttu-id="98a68-174">Muss immer 20 Byte lang sein.</span><span class="sxs-lookup"><span data-stu-id="98a68-174">Must always be 20 bytes in length.</span></span> <span data-ttu-id="98a68-175">Wenn x kleiner als 20 Bytes ist, muss es mit 0x00 aufgefüllt werden.</span><span class="sxs-lookup"><span data-stu-id="98a68-175">If x is smaller than 20 bytes in length, then it must be padded with 0x00.</span></span>                                                     |



 

<span data-ttu-id="98a68-176">Wenn Sie [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)aufrufen, kann der Entwickler auswählen, ob der Schlüssel verschlüsselt werden soll.</span><span class="sxs-lookup"><span data-stu-id="98a68-176">When calling [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), the developer can choose whether to encrypt the key.</span></span> <span data-ttu-id="98a68-177">Der **privatekeyblob** wird verschlüsselt, wenn der *hexpkey* -Parameter ein gültiges Handle für einen Sitzungsschlüssel enthält.</span><span class="sxs-lookup"><span data-stu-id="98a68-177">The **PRIVATEKEYBLOB** is encrypted if the *hExpKey* parameter contains a valid handle to a session key.</span></span> <span data-ttu-id="98a68-178">Alles außer dem [**publickeystruc**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) -Teil des BLOBs wird verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="98a68-178">Everything but the [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) portion of the BLOB is encrypted.</span></span>

> [!Note]  
> <span data-ttu-id="98a68-179">Der Verschlüsselungsalgorithmus und die Verschlüsselungsschlüssel Parameter werden nicht zusammen mit dem BLOB für den privaten Schlüssel gespeichert.</span><span class="sxs-lookup"><span data-stu-id="98a68-179">The encryption algorithm and encryption key parameters are not stored along with the private key BLOB.</span></span> <span data-ttu-id="98a68-180">Diese Informationen müssen von der Anwendung verwaltet und gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="98a68-180">The application must manage and store this information.</span></span> <span data-ttu-id="98a68-181">Wenn 0 (null) für *hexpkey* übermittelt wird, wird der private Schlüssel ohne Verschlüsselung exportiert.</span><span class="sxs-lookup"><span data-stu-id="98a68-181">If zero is passed for *hExpKey*, the private key will be exported without encryption.</span></span>

 

> [!Caution]  
> <span data-ttu-id="98a68-182">Es ist gefährlich, private Schlüssel ohne Verschlüsselung zu exportieren, da Sie dann anfällig für das Abfangen und die Verwendung durch nicht autorisierte Entitäten sind.</span><span class="sxs-lookup"><span data-stu-id="98a68-182">It is dangerous to export private keys without encryption because they are then vulnerable to interception and use by unauthorized entities.</span></span>

 

 

 
