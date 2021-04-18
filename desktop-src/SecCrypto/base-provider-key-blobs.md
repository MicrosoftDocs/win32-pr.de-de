---
description: Der Basis Anbieter und der erweiterte Anbieter verwenden dieselben Schlüsselblob.
ms.assetid: b4592036-0fa3-4b7e-beed-78cf1d2f39a9
title: Schlüssel-BLOB des Basis Anbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c763f97fe6e7868246e0bce30ee2a741e8bd212f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345751"
---
# <a name="base-provider-key-blobs"></a><span data-ttu-id="9baaf-103">Schlüssel-BLOB des Basis Anbieters</span><span class="sxs-lookup"><span data-stu-id="9baaf-103">Base Provider Key BLOBs</span></span>

<span data-ttu-id="9baaf-104">Der Basis Anbieter und der erweiterte Anbieter verwenden dieselben [*Schlüsselblob*](../secgloss/k-gly.md).</span><span class="sxs-lookup"><span data-stu-id="9baaf-104">The Base Provider and Extended Provider use the same [*key BLOBs*](../secgloss/k-gly.md).</span></span>

-   [<span data-ttu-id="9baaf-105">Blobschlüssel für öffentliche Schlüssel</span><span class="sxs-lookup"><span data-stu-id="9baaf-105">Public Key BLOBs</span></span>](#public-key-blobs)
-   [<span data-ttu-id="9baaf-106">Blobschlüssel für private Schlüssel</span><span class="sxs-lookup"><span data-stu-id="9baaf-106">Private Key BLOBs</span></span>](#private-key-blobs)
-   [<span data-ttu-id="9baaf-107">Einfache Schlüsselblob</span><span class="sxs-lookup"><span data-stu-id="9baaf-107">Simple Key BLOBs</span></span>](#simple-key-blobs)

## <a name="public-key-blobs"></a><span data-ttu-id="9baaf-108">Blobschlüssel für öffentliche Schlüssel</span><span class="sxs-lookup"><span data-stu-id="9baaf-108">Public Key BLOBs</span></span>

<span data-ttu-id="9baaf-109">[*Öffentliche Schlüssel-BLOBs*](../secgloss/p-gly.md), geben Sie **PublicKeyBlob** ein, die verwendet werden, um [*öffentliche Schlüssel*](../secgloss/p-gly.md) außerhalb eines [*Kryptografiedienstanbieters*](../secgloss/c-gly.md) (CSP) zu speichern.</span><span class="sxs-lookup"><span data-stu-id="9baaf-109">[*Public key BLOBs*](../secgloss/p-gly.md), type **PUBLICKEYBLOB**, are used to store [*public keys*](../secgloss/p-gly.md) outside a [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span> <span data-ttu-id="9baaf-110">BLOB für öffentliche Schlüssel des Basis Anbieters haben das folgende Format:</span><span class="sxs-lookup"><span data-stu-id="9baaf-110">Base provider public key BLOBs have the following format.</span></span>

``` syntax
PUBLICKEYSTRUC  publickeystruc;
RSAPUBKEY rsapubkey;
BYTE modulus[rsapubkey.bitlen/8];
```

<span data-ttu-id="9baaf-111">In der folgenden Tabelle werden die einzelnen öffentlichen Schlüsselkomponenten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="9baaf-111">The following table describes each public key component.</span></span> <span data-ttu-id="9baaf-112">Alle Werte liegen im [*Little-Endian-*](../secgloss/l-gly.md) Format vor.</span><span class="sxs-lookup"><span data-stu-id="9baaf-112">All values are in [*little-endian*](../secgloss/l-gly.md) format.</span></span>



| <span data-ttu-id="9baaf-113">Feld</span><span class="sxs-lookup"><span data-stu-id="9baaf-113">Field</span></span>          | <span data-ttu-id="9baaf-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9baaf-114">Description</span></span>                                                                                                                                                                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9baaf-115">modulus</span><span class="sxs-lookup"><span data-stu-id="9baaf-115">modulus</span></span>        | <span data-ttu-id="9baaf-116">Die Daten des Datasets mit öffentlichem Schlüssel befinden sich direkt nach der [**rsapubkey**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="9baaf-116">The public key modulus data is located directly after the [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) structure.</span></span> <span data-ttu-id="9baaf-117">Die Größe dieser Daten hängt von der Größe des öffentlichen Schlüssels ab.</span><span class="sxs-lookup"><span data-stu-id="9baaf-117">The size of this data will vary, depending on the size of the public key.</span></span> <span data-ttu-id="9baaf-118">Die Anzahl der Bytes kann bestimmt werden, indem der Wert des Felds **rsapubkey bitlen** durch acht dividiert wird.</span><span class="sxs-lookup"><span data-stu-id="9baaf-118">The number of bytes can be determined by dividing the value of the **RSAPUBKEY bitlen** field by eight.</span></span> |
| <span data-ttu-id="9baaf-119">publickeystruc</span><span class="sxs-lookup"><span data-stu-id="9baaf-119">publickeystruc</span></span> | <span data-ttu-id="9baaf-120">Eine [**publickeystruc**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="9baaf-120">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="9baaf-121">rsapubkey</span><span class="sxs-lookup"><span data-stu-id="9baaf-121">rsapubkey</span></span>      | <span data-ttu-id="9baaf-122">Eine [**rsapubkey**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="9baaf-122">A [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) structure.</span></span> <span data-ttu-id="9baaf-123">Der **Magic** -Member muss auf 0x31415352 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="9baaf-123">The **magic** member must be set to 0x31415352.</span></span> <span data-ttu-id="9baaf-124">Dieser Hexadezimalwert ist die [*ASCII*](../secgloss/a-gly.md) -Codierung von RSA1.</span><span class="sxs-lookup"><span data-stu-id="9baaf-124">This hexadecimal value is the [*ASCII*](../secgloss/a-gly.md) encoding of RSA1.</span></span>                                                                         |



 

> [!Note]  
> <span data-ttu-id="9baaf-125">Blobblobschlüssel für öffentliche Schlüssel werden nicht verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="9baaf-125">Public key BLOBs are not encrypted.</span></span> <span data-ttu-id="9baaf-126">Sie enthalten öffentliche Schlüssel als [*Klartext*](../secgloss/p-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="9baaf-126">They contain public keys in [*plaintext*](../secgloss/p-gly.md) form.</span></span>

 

## <a name="private-key-blobs"></a><span data-ttu-id="9baaf-127">Blobschlüssel für private Schlüssel</span><span class="sxs-lookup"><span data-stu-id="9baaf-127">Private Key BLOBs</span></span>

<span data-ttu-id="9baaf-128">[*Private Schlüsselblobs*](../secgloss/p-gly.md), Typ **privatekeyblob**, werden zum Speichern [*privater Schlüssel*](../secgloss/p-gly.md) außerhalb eines CSP verwendet.</span><span class="sxs-lookup"><span data-stu-id="9baaf-128">[*Private key BLOBs*](../secgloss/p-gly.md), type **PRIVATEKEYBLOB**, are used to store [*private keys*](../secgloss/p-gly.md) outside a CSP.</span></span> <span data-ttu-id="9baaf-129">Die BLOB des privaten Schlüssels des Basis Anbieters haben das folgende Format.</span><span class="sxs-lookup"><span data-stu-id="9baaf-129">Base provider private key BLOBs have the following format.</span></span>

``` syntax
PUBLICKEYSTRUC  publickeystruc;
RSAPUBKEY rsapubkey;
BYTE modulus[rsapubkey.bitlen/8];
BYTE prime1[rsapubkey.bitlen/16];
BYTE prime2[rsapubkey.bitlen/16];
BYTE exponent1[rsapubkey.bitlen/16];
BYTE exponent2[rsapubkey.bitlen/16];
BYTE coefficient[rsapubkey.bitlen/16];
BYTE privateExponent[rsapubkey.bitlen/8];
```

<span data-ttu-id="9baaf-130">In der folgenden Tabelle wird die BLOB-Komponente des privaten Schlüssels beschrieben.</span><span class="sxs-lookup"><span data-stu-id="9baaf-130">The following table describes the private key BLOB component.</span></span>

> [!Note]  
> <span data-ttu-id="9baaf-131">Diese Felder entsprechen den im Abschnitt 7,2 von [*Public Key Cryptography Standards*](../secgloss/p-gly.md) (PKCS) 1 beschriebenen Feldern \# mit geringfügigen Unterschieden.</span><span class="sxs-lookup"><span data-stu-id="9baaf-131">These fields correspond to the fields described in section 7.2 of [*Public Key Cryptography Standards*](../secgloss/p-gly.md) (PKCS) \#1 with minor differences.</span></span>

 



| <span data-ttu-id="9baaf-132">Feld</span><span class="sxs-lookup"><span data-stu-id="9baaf-132">Field</span></span>           | <span data-ttu-id="9baaf-133">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9baaf-133">Description</span></span>                                                                                                                                                                                                   |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9baaf-134">Fak</span><span class="sxs-lookup"><span data-stu-id="9baaf-134">coefficient</span></span>     | <span data-ttu-id="9baaf-135">Fak.</span><span class="sxs-lookup"><span data-stu-id="9baaf-135">Coefficient.</span></span> <span data-ttu-id="9baaf-136">Dies hat den numerischen Wert (inverse of q) mod p.</span><span class="sxs-lookup"><span data-stu-id="9baaf-136">This has a numeric value of (inverse of q) mod p.</span></span>                                                                                                                                                |
| <span data-ttu-id="9baaf-137">exponent1</span><span class="sxs-lookup"><span data-stu-id="9baaf-137">exponent1</span></span>       | <span data-ttu-id="9baaf-138">Exponent 1.</span><span class="sxs-lookup"><span data-stu-id="9baaf-138">Exponent 1.</span></span> <span data-ttu-id="9baaf-139">Dies hat den numerischen Wert d mod (p – 1).</span><span class="sxs-lookup"><span data-stu-id="9baaf-139">This has a numeric value of d mod (p – 1).</span></span>                                                                                                                                                        |
| <span data-ttu-id="9baaf-140">exponent2</span><span class="sxs-lookup"><span data-stu-id="9baaf-140">exponent2</span></span>       | <span data-ttu-id="9baaf-141">Exponent 2.</span><span class="sxs-lookup"><span data-stu-id="9baaf-141">Exponent 2.</span></span> <span data-ttu-id="9baaf-142">Dies hat den numerischen Wert d mod (q – 1).</span><span class="sxs-lookup"><span data-stu-id="9baaf-142">This has a numeric value of d mod (q – 1).</span></span>                                                                                                                                                        |
| <span data-ttu-id="9baaf-143">Modulus</span><span class="sxs-lookup"><span data-stu-id="9baaf-143">Modulus</span></span>         | <span data-ttu-id="9baaf-144">Der Modulus.</span><span class="sxs-lookup"><span data-stu-id="9baaf-144">The modulus.</span></span> <span data-ttu-id="9baaf-145">Dies hat den Wert *Prime1*×*Prime2* und wird häufig als n bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="9baaf-145">This has a value of *Prime1*×*Prime2* and is often known as n.</span></span>                                                                                                                                   |
| <span data-ttu-id="9baaf-146">prime1</span><span class="sxs-lookup"><span data-stu-id="9baaf-146">prime1</span></span>          | <span data-ttu-id="9baaf-147">Primzahl 1, häufig auch als p bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="9baaf-147">Prime number 1, often known as p.</span></span>                                                                                                                                                                             |
| <span data-ttu-id="9baaf-148">prime2</span><span class="sxs-lookup"><span data-stu-id="9baaf-148">prime2</span></span>          | <span data-ttu-id="9baaf-149">Primzahl 2, häufig auch als q bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="9baaf-149">Prime number 2, often known as q.</span></span>                                                                                                                                                                             |
| <span data-ttu-id="9baaf-150">privateexponent</span><span class="sxs-lookup"><span data-stu-id="9baaf-150">privateExponent</span></span> | <span data-ttu-id="9baaf-151">Privater Exponent, der häufig als "d" bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="9baaf-151">Private exponent, often known as d.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="9baaf-152">publickeystruc</span><span class="sxs-lookup"><span data-stu-id="9baaf-152">publickeystruc</span></span>  | <span data-ttu-id="9baaf-153">Eine [**publickeystruc**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="9baaf-153">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                         |
| <span data-ttu-id="9baaf-154">rsapubkey</span><span class="sxs-lookup"><span data-stu-id="9baaf-154">rsapubkey</span></span>       | <span data-ttu-id="9baaf-155">Eine [**rsapubkey**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="9baaf-155">A [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) structure.</span></span> <span data-ttu-id="9baaf-156">Der **Magic** -Member muss auf 0x32415352 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="9baaf-156">The **magic** member must be set to 0x32415352.</span></span> <span data-ttu-id="9baaf-157">Dieser Hexadezimalwert ist die [*ASCII*](../secgloss/a-gly.md) -Codierung von RSA2.</span><span class="sxs-lookup"><span data-stu-id="9baaf-157">This hexadecimal value is the [*ASCII*](../secgloss/a-gly.md) encoding of RSA2.</span></span> |



 

> [!Note]  
> <span data-ttu-id="9baaf-158">Blobblobschlüssel für private Schlüssel werden nicht verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="9baaf-158">Private key BLOBs are not encrypted.</span></span> <span data-ttu-id="9baaf-159">Sie enthalten private Schlüssel in Klartext.</span><span class="sxs-lookup"><span data-stu-id="9baaf-159">They contain private keys in plaintext form.</span></span>

 

<span data-ttu-id="9baaf-160">Wenn Sie [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)aufrufen, kann der Entwickler auswählen, ob der Schlüssel verschlüsselt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9baaf-160">When calling [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), the developer can choose whether to encrypt the key.</span></span> <span data-ttu-id="9baaf-161">Der **privatekeyblob** wird verschlüsselt, wenn der *hexpkey* -Parameter ein gültiges Handle für einen Sitzungsschlüssel enthält.</span><span class="sxs-lookup"><span data-stu-id="9baaf-161">The **PRIVATEKEYBLOB** is encrypted if the *hExpKey* parameter contains a valid handle to a session key.</span></span> <span data-ttu-id="9baaf-162">Alles außer dem [**publickeystruc**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) -Teil des BLOBs wird verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="9baaf-162">Everything but the [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) portion of the BLOB is encrypted.</span></span>

> [!Note]  
> <span data-ttu-id="9baaf-163">Der Verschlüsselungsalgorithmus und die Verschlüsselungsschlüssel Parameter werden nicht zusammen mit dem BLOB für den privaten Schlüssel gespeichert.</span><span class="sxs-lookup"><span data-stu-id="9baaf-163">The encryption algorithm and encryption key parameters are not stored along with the private key BLOB.</span></span> <span data-ttu-id="9baaf-164">Diese Informationen müssen von der Anwendung verwaltet und gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="9baaf-164">The application must manage and store this information.</span></span> <span data-ttu-id="9baaf-165">Wenn 0 (null) für *hexpkey* übermittelt wird, wird der private Schlüssel ohne Verschlüsselung exportiert.</span><span class="sxs-lookup"><span data-stu-id="9baaf-165">If zero is passed for *hExpKey*, the private key will be exported without encryption.</span></span>

 

> [!Caution]  
> <span data-ttu-id="9baaf-166">Es ist gefährlich, private Schlüssel ohne Verschlüsselung zu exportieren, da Sie dann anfällig für das Abfangen und die Verwendung durch nicht autorisierte Entitäten sind.</span><span class="sxs-lookup"><span data-stu-id="9baaf-166">It is dangerous to export private keys without encryption because they are then vulnerable to interception and use by unauthorized entities.</span></span>

 

## <a name="simple-key-blobs"></a><span data-ttu-id="9baaf-167">Einfache Schlüsselblob</span><span class="sxs-lookup"><span data-stu-id="9baaf-167">Simple Key BLOBs</span></span>

<span data-ttu-id="9baaf-168">[*Einfache Schlüsselblobs*](../secgloss/s-gly.md), geben Sie **simpleblob** ein, die zum Speichern und transportieren von Sitzungs Schlüsseln außerhalb eines CSP verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9baaf-168">[*Simple key BLOBs*](../secgloss/s-gly.md), type **SIMPLEBLOB**, are used to store and transport session keys outside a CSP.</span></span> <span data-ttu-id="9baaf-169">Einfache Schlüssel-BLOB des Basis Anbieters werden immer mit einem [*öffentlichen Schlüsselaustausch*](../secgloss/k-gly.md)Schlüssel verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="9baaf-169">Base provider simple key BLOBs are always encrypted with a [*key exchange public key*](../secgloss/k-gly.md).</span></span> <span data-ttu-id="9baaf-170">Der **pbData** -Member von **simpleblob** ist eine Folge von Bytes im folgenden Format.</span><span class="sxs-lookup"><span data-stu-id="9baaf-170">The **pbData** member of the **SIMPLEBLOB** is a sequence of bytes in the following format.</span></span>

``` syntax
PUBLICKEYSTRUC  publickeystruc;
ALG_ID algid;
BYTE encryptedkey[rsapubkey.bitlen/8];
```

<span data-ttu-id="9baaf-171">In der folgenden Tabelle werden die einzelnen Komponenten des **pbData** -Members von **simpleblob** beschrieben.</span><span class="sxs-lookup"><span data-stu-id="9baaf-171">The following table describes each component of the **pbData** member of the **SIMPLEBLOB**.</span></span>



| <span data-ttu-id="9baaf-172">Feld</span><span class="sxs-lookup"><span data-stu-id="9baaf-172">Field</span></span>          | <span data-ttu-id="9baaf-173">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9baaf-173">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9baaf-174">algid</span><span class="sxs-lookup"><span data-stu-id="9baaf-174">algid</span></span>          | <span data-ttu-id="9baaf-175">Eine [**ALG- \_ ID**](alg-id.md) -Struktur, die den Verschlüsselungsalgorithmus angibt, mit dem die Sitzungsschlüssel Daten verschlüsselt werden.</span><span class="sxs-lookup"><span data-stu-id="9baaf-175">An [**ALG\_ID**](alg-id.md) structure that specifies the encryption algorithm used to encrypt the session key data.</span></span> <span data-ttu-id="9baaf-176">Dabei handelt es sich in der Regel um den Wert calg \_ RSA \_ Keyx, der angibt, dass die Sitzungsschlüssel Daten mit einem öffentlichen Schlüsselaustausch Schlüssel mithilfe des [*RSA-Algorithmus für öffentliche Schlüssel*](../secgloss/r-gly.md)verschlüsselt wurden.</span><span class="sxs-lookup"><span data-stu-id="9baaf-176">This typically has a value of CALG\_RSA\_KEYX, which indicates that the session key data was encrypted with a key exchange public key using the [*RSA Public Key algorithm*](../secgloss/r-gly.md).</span></span>                                                                                                                           |
| <span data-ttu-id="9baaf-177">EncryptedKey</span><span class="sxs-lookup"><span data-stu-id="9baaf-177">encryptedkey</span></span>   | <span data-ttu-id="9baaf-178">Eine **Byte** Sequenz, die die verschlüsselten Sitzungsschlüssel Daten in Form eines PKCS 1- \# , Typ-2-Verschlüsselungs Blocks darstellt.</span><span class="sxs-lookup"><span data-stu-id="9baaf-178">A **BYTE** sequence that represents the encrypted session key data in the form of a PKCS \#1, type 2 encryption block.</span></span> <span data-ttu-id="9baaf-179">Weitere Informationen zu diesem Datenformat finden Sie unter Public Key Cryptography Standards (PKCS) \# 1, veröffentlicht von RSA Data Security, Inc. Diese Daten haben immer die gleiche Größe wie der Modulo des öffentlichen Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="9baaf-179">For information about this data format, see the Public Key Cryptography Standards (PKCS) \#1, published by RSA Data Security, Inc. This data is always the same size as the modulus of the public key.</span></span> <span data-ttu-id="9baaf-180">Beispielsweise können öffentliche Schlüssel, die vom Microsoft RSA-Basis Anbieter generiert werden, 512 Bits (64 Bytes) sein, sodass die verschlüsselten Sitzungsschlüssel Daten auch immer 512 Bits (64 Bytes) sind.</span><span class="sxs-lookup"><span data-stu-id="9baaf-180">For example, public keys generated by the Microsoft RSA Base Provider can be 512 bits (64 bytes) in length, so the encrypted session key data is also always 512 bits (64 bytes).</span></span><br/> |
| <span data-ttu-id="9baaf-181">publickeystruc</span><span class="sxs-lookup"><span data-stu-id="9baaf-181">publickeystruc</span></span> | <span data-ttu-id="9baaf-182">Eine [**publickeystruc**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="9baaf-182">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

 

 
