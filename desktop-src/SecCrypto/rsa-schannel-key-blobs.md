---
description: Blobvorgänge werden mit dem RSA/SChannel-Anbieter verwendet, um Schlüssel aus dem Kryptografiedienstanbieter (kryptografischen Service Provider, CSP) zu exportieren und Schlüssel in zu importieren.
ms.assetid: 97d5ee6d-4687-4cd2-b122-36f8ea3c93ca
title: RSA/SChannel-schlüsselblobzugriff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cea26a98e9c2925442166eb28245ebc471b1749e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862831"
---
# <a name="rsaschannel-key-blobs"></a><span data-ttu-id="da428-103">RSA/SChannel-schlüsselblobzugriff</span><span class="sxs-lookup"><span data-stu-id="da428-103">RSA/Schannel Key BLOBs</span></span>

<span data-ttu-id="da428-104">[*Blobvorgänge*](../secgloss/b-gly.md) werden mit dem [*RSA*](../secgloss/r-gly.md) / [*SChannel*](../secgloss/s-gly.md) -Anbieter verwendet, um Schlüssel aus dem [*Kryptografiedienstanbieter (kryptografischen Service Provider*](../secgloss/c-gly.md) , CSP) zu exportieren und Schlüssel in zu importieren.</span><span class="sxs-lookup"><span data-stu-id="da428-104">[*BLOBs*](../secgloss/b-gly.md) are used with the [*RSA*](../secgloss/r-gly.md)/[*Schannel*](../secgloss/s-gly.md) provider to export keys from, and import keys into, the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span>

-   [<span data-ttu-id="da428-105">Blobschlüssel für öffentliche Schlüssel</span><span class="sxs-lookup"><span data-stu-id="da428-105">Public Key BLOBs</span></span>](#public-key-blobs)
-   [<span data-ttu-id="da428-106">Blobschlüssel für private Schlüssel</span><span class="sxs-lookup"><span data-stu-id="da428-106">Private Key BLOBs</span></span>](#private-key-blobs)
-   [<span data-ttu-id="da428-107">Einfache Schlüsselblob</span><span class="sxs-lookup"><span data-stu-id="da428-107">Simple Key BLOBs</span></span>](#simple-key-blobs)

## <a name="public-key-blobs"></a><span data-ttu-id="da428-108">Blobschlüssel für öffentliche Schlüssel</span><span class="sxs-lookup"><span data-stu-id="da428-108">Public Key BLOBs</span></span>

<span data-ttu-id="da428-109">[*Öffentliche Schlüssel-BLOBs*](../secgloss/p-gly.md), geben Sie **PublicKeyBlob** ein, die zum Speichern [*öffentlicher Schlüssel*](../secgloss/p-gly.md)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="da428-109">[*Public key BLOBs*](../secgloss/p-gly.md), type **PUBLICKEYBLOB**, are used to store [*public keys*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="da428-110">Diese Schlüssel werden als Bytefolge im folgenden Format exportiert und importiert.</span><span class="sxs-lookup"><span data-stu-id="da428-110">These keys are exported and imported as a sequence of bytes with the following format.</span></span>

``` syntax
PUBLICKEYSTRUC  publickeystruc ;
RSAPUBKEY       rsapubkey;
BYTE            modulus[rsapubkey.bitlen/8];
```

<span data-ttu-id="da428-111">In der folgenden Tabelle werden die einzelnen öffentlichen Schlüsselkomponenten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="da428-111">The following table describes each public key component.</span></span> <span data-ttu-id="da428-112">Alle Werte liegen im [*Little-Endian-*](../secgloss/l-gly.md) Format vor.</span><span class="sxs-lookup"><span data-stu-id="da428-112">All values are in [*little-endian*](../secgloss/l-gly.md) format.</span></span>



| <span data-ttu-id="da428-113">Feld</span><span class="sxs-lookup"><span data-stu-id="da428-113">Field</span></span>          | <span data-ttu-id="da428-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="da428-114">Description</span></span>                                                                                                                                                                                                                                                                                        |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da428-115">modulus</span><span class="sxs-lookup"><span data-stu-id="da428-115">modulus</span></span>        | <span data-ttu-id="da428-116">Eine **Byte** Sequenz.</span><span class="sxs-lookup"><span data-stu-id="da428-116">A **BYTE** sequence.</span></span> <span data-ttu-id="da428-117">Die Daten des Datasets mit öffentlichem Schlüssel befinden sich direkt nach der **rsapubkey** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="da428-117">The public key modulus data is located directly after the **RSAPUBKEY** structure.</span></span> <span data-ttu-id="da428-118">Die Länge dieser Daten hängt von der Länge des öffentlichen Schlüssels ab.</span><span class="sxs-lookup"><span data-stu-id="da428-118">The length of this data varies, depending on the length of the public key.</span></span> <span data-ttu-id="da428-119">Die Anzahl der Bytes kann bestimmt werden, indem der Wert des **bitlen** -Members von **rsapubkey** um acht dividiert wird.</span><span class="sxs-lookup"><span data-stu-id="da428-119">The number of bytes can be determined by dividing the value of the **bitlen** member of **RSAPUBKEY** by eight.</span></span> |
| <span data-ttu-id="da428-120">publickeystruc</span><span class="sxs-lookup"><span data-stu-id="da428-120">publickeystruc</span></span> | <span data-ttu-id="da428-121">Eine [**publickeystruc**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="da428-121">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                                                                                                              |
| <span data-ttu-id="da428-122">rsapubkey</span><span class="sxs-lookup"><span data-stu-id="da428-122">rsapubkey</span></span>      | <span data-ttu-id="da428-123">Eine [**rsapubkey**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="da428-123">A [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) structure.</span></span> <span data-ttu-id="da428-124">Der **Magic** -Member muss auf 0x31415352 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="da428-124">The **magic** member must be set to 0x31415352.</span></span> <span data-ttu-id="da428-125">Dieser Hexadezimalwert ist die [*ASCII*](../secgloss/a-gly.md) -Codierung von RSA1.</span><span class="sxs-lookup"><span data-stu-id="da428-125">This hexadecimal value is the [*ASCII*](../secgloss/a-gly.md) encoding of RSA1.</span></span>                                                                                      |



 

> [!Note]  
> <span data-ttu-id="da428-126">Blobblobschlüssel für öffentliche Schlüssel werden nicht verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="da428-126">Public key BLOBs are not encrypted.</span></span> <span data-ttu-id="da428-127">Sie enthalten öffentliche Schlüssel als [*Klartext*](../secgloss/p-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="da428-127">They contain public keys in [*plaintext*](../secgloss/p-gly.md) form.</span></span>

 

## <a name="private-key-blobs"></a><span data-ttu-id="da428-128">Blobschlüssel für private Schlüssel</span><span class="sxs-lookup"><span data-stu-id="da428-128">Private Key BLOBs</span></span>

<span data-ttu-id="da428-129">[*Private Schlüsselblobs*](../secgloss/p-gly.md), Typ **privatekeyblob**, werden zum Speichern von [*Paaren aus öffentlichem und privatem Schlüssel*](../secgloss/p-gly.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="da428-129">[*Private key BLOBs*](../secgloss/p-gly.md), type **PRIVATEKEYBLOB**, are used to store [*public/private key pairs*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="da428-130">Diese Schlüssel werden als Bytefolge im folgenden Format exportiert und importiert.</span><span class="sxs-lookup"><span data-stu-id="da428-130">These keys are exported and imported as a sequence of bytes with the following format.</span></span>

``` syntax
PUBLICKEYSTRUC  publickeystruc ;
RSAPUBKEY       rsapubkey;
BYTE            modulus[rsapubkey.bitlen/8];
BYTE            prime1[rsapubkey.bitlen/16];
BYTE            prime2[rsapubkey.bitlen/16];
BYTE            exponent1[rsapubkey.bitlen/16];
BYTE            exponent2[rsapubkey.bitlen/16];
BYTE            coefficient[rsapubkey.bitlen/16];
BYTE            privateExponent[rsapubkey.bitlen/8];
```

<span data-ttu-id="da428-131">Wenn das [*Schlüsselblob*](../secgloss/k-gly.md) verschlüsselt ist, wird alles, aber der [**publickeystruc**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) -Teil des BLOBs verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="da428-131">If the [*key BLOB*](../secgloss/k-gly.md) is encrypted, then everything but the [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) portion of the BLOB is encrypted.</span></span>

> [!Note]  
> <span data-ttu-id="da428-132">Der Verschlüsselungsalgorithmus und die Verschlüsselungsschlüssel Parameter werden nicht zusammen mit dem BLOB für den privaten Schlüssel gespeichert.</span><span class="sxs-lookup"><span data-stu-id="da428-132">The encryption algorithm and encryption key parameters are not stored along with the private key BLOB.</span></span> <span data-ttu-id="da428-133">Es liegt in der Verantwortung der Anwendung, diese Informationen zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="da428-133">It is the responsibility of the application to manage this information.</span></span>

 

<span data-ttu-id="da428-134">In der folgenden Tabelle werden die einzelnen BLOB-Komponenten des privaten Schlüssels beschrieben.</span><span class="sxs-lookup"><span data-stu-id="da428-134">The following table describes each private key BLOB component.</span></span>

> [!Note]  
> <span data-ttu-id="da428-135">Diese Felder entsprechen den im Abschnitt 7,2 von [*Public Key Cryptography Standards*](../secgloss/p-gly.md) (PKCS) 1 beschriebenen Feldern \# mit geringfügigen Unterschieden.</span><span class="sxs-lookup"><span data-stu-id="da428-135">These fields correspond to the fields described in section 7.2 of [*Public Key Cryptography Standards*](../secgloss/p-gly.md) (PKCS) \#1 with minor differences.</span></span>

 



| <span data-ttu-id="da428-136">Feld</span><span class="sxs-lookup"><span data-stu-id="da428-136">Field</span></span>           | <span data-ttu-id="da428-137">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="da428-137">Description</span></span>                                                                                                                                                                                                   |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da428-138">exponent1</span><span class="sxs-lookup"><span data-stu-id="da428-138">exponent1</span></span>       | <span data-ttu-id="da428-139">Eine **Byte** Sequenz.</span><span class="sxs-lookup"><span data-stu-id="da428-139">A **BYTE** sequence.</span></span> <span data-ttu-id="da428-140">Der erste Exponent.</span><span class="sxs-lookup"><span data-stu-id="da428-140">The first exponent.</span></span> <span data-ttu-id="da428-141">Dies hat den numerischen Wert d mod (p – 1).</span><span class="sxs-lookup"><span data-stu-id="da428-141">This has a numeric value of d mod (p – 1).</span></span>                                                                                                                           |
| <span data-ttu-id="da428-142">exponent2</span><span class="sxs-lookup"><span data-stu-id="da428-142">exponent2</span></span>       | <span data-ttu-id="da428-143">Eine **Byte** Sequenz.</span><span class="sxs-lookup"><span data-stu-id="da428-143">A **BYTE** sequence.</span></span> <span data-ttu-id="da428-144">Der zweite Exponent.</span><span class="sxs-lookup"><span data-stu-id="da428-144">The second exponent.</span></span> <span data-ttu-id="da428-145">Dies hat den numerischen Wert d mod (q – 1).</span><span class="sxs-lookup"><span data-stu-id="da428-145">This has a numeric value of d mod (q – 1).</span></span>                                                                                                                          |
| <span data-ttu-id="da428-146">Fak</span><span class="sxs-lookup"><span data-stu-id="da428-146">coefficient</span></span>     | <span data-ttu-id="da428-147">Eine **Byte** Sequenz.</span><span class="sxs-lookup"><span data-stu-id="da428-147">A **BYTE** sequence.</span></span> <span data-ttu-id="da428-148">Fak.</span><span class="sxs-lookup"><span data-stu-id="da428-148">Coefficient.</span></span> <span data-ttu-id="da428-149">Dies hat den numerischen Wert (inverse of q) mod p.</span><span class="sxs-lookup"><span data-stu-id="da428-149">This has a numeric value of (inverse of q) mod p.</span></span>                                                                                                                           |
| <span data-ttu-id="da428-150">Modulus</span><span class="sxs-lookup"><span data-stu-id="da428-150">Modulus</span></span>         | <span data-ttu-id="da428-151">Eine **Byte** Sequenz.</span><span class="sxs-lookup"><span data-stu-id="da428-151">A **BYTE** sequence.</span></span> <span data-ttu-id="da428-152">Der Modulus.</span><span class="sxs-lookup"><span data-stu-id="da428-152">The modulus.</span></span> <span data-ttu-id="da428-153">Diese verfügt über eine Zeichenfolge, die *Prime1* \* *Prime2* enthält.</span><span class="sxs-lookup"><span data-stu-id="da428-153">This has a string that contains *Prime1* \* *Prime2*.</span></span> <span data-ttu-id="da428-154">Dies wird häufig als n bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="da428-154">It is often known as n.</span></span>                                                                                               |
| <span data-ttu-id="da428-155">prime1</span><span class="sxs-lookup"><span data-stu-id="da428-155">prime1</span></span>          | <span data-ttu-id="da428-156">Eine **Byte** Sequenz.</span><span class="sxs-lookup"><span data-stu-id="da428-156">A **BYTE** sequence.</span></span> <span data-ttu-id="da428-157">Primzahl 1, häufig auch als p bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="da428-157">Prime number 1, often known as p.</span></span>                                                                                                                                                        |
| <span data-ttu-id="da428-158">prime2</span><span class="sxs-lookup"><span data-stu-id="da428-158">prime2</span></span>          | <span data-ttu-id="da428-159">Eine **Byte** Sequenz.</span><span class="sxs-lookup"><span data-stu-id="da428-159">A **BYTE** sequence.</span></span> <span data-ttu-id="da428-160">Primzahl 2, häufig auch als q bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="da428-160">Prime number 2, often known as q.</span></span>                                                                                                                                                        |
| <span data-ttu-id="da428-161">publickeystruc</span><span class="sxs-lookup"><span data-stu-id="da428-161">publickeystruc</span></span>  | <span data-ttu-id="da428-162">Eine [**publickeystruc**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="da428-162">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                         |
| <span data-ttu-id="da428-163">privateexponent</span><span class="sxs-lookup"><span data-stu-id="da428-163">privateExponent</span></span> | <span data-ttu-id="da428-164">Eine **Byte** Sequenz.</span><span class="sxs-lookup"><span data-stu-id="da428-164">A **BYTE** sequence.</span></span> <span data-ttu-id="da428-165">Der private Exponent, der häufig als "d" bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="da428-165">The private exponent, often known as d.</span></span>                                                                                                                                                  |
| <span data-ttu-id="da428-166">rsapubkey</span><span class="sxs-lookup"><span data-stu-id="da428-166">rsapubkey</span></span>       | <span data-ttu-id="da428-167">Eine [**rsapubkey**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="da428-167">A [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) structure.</span></span> <span data-ttu-id="da428-168">Der **Magic** -Member muss auf 0x32415352 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="da428-168">The **magic** member must be set to 0x32415352.</span></span> <span data-ttu-id="da428-169">Dieser Hexadezimalwert ist die [*ASCII*](../secgloss/a-gly.md) -Codierung von RSA2.</span><span class="sxs-lookup"><span data-stu-id="da428-169">This hexadecimal value is the [*ASCII*](../secgloss/a-gly.md) encoding of RSA2.</span></span> |



 

> [!Note]  
> <span data-ttu-id="da428-170">Blobblobschlüssel für private Schlüssel werden nicht verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="da428-170">Private key BLOBs are not encrypted.</span></span> <span data-ttu-id="da428-171">Sie enthalten private Schlüssel in Klartext.</span><span class="sxs-lookup"><span data-stu-id="da428-171">They contain private keys in plaintext form.</span></span>

 

<span data-ttu-id="da428-172">Wenn Sie [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)aufrufen, kann der Entwickler auswählen, ob der Schlüssel verschlüsselt werden soll.</span><span class="sxs-lookup"><span data-stu-id="da428-172">When calling [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), the developer can choose whether to encrypt the key.</span></span> <span data-ttu-id="da428-173">Der **privatekeyblob** wird verschlüsselt, wenn der *hexpkey* -Parameter ein gültiges Handle für einen Sitzungsschlüssel enthält.</span><span class="sxs-lookup"><span data-stu-id="da428-173">The **PRIVATEKEYBLOB** is encrypted if the *hExpKey* parameter contains a valid handle to a session key.</span></span> <span data-ttu-id="da428-174">Alles außer dem [**publickeystruc**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) -Teil des BLOBs wird verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="da428-174">Everything but the [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) portion of the BLOB is encrypted.</span></span>

> [!Note]  
> <span data-ttu-id="da428-175">Der Verschlüsselungsalgorithmus und die Verschlüsselungsschlüssel Parameter werden nicht zusammen mit dem BLOB für den privaten Schlüssel gespeichert.</span><span class="sxs-lookup"><span data-stu-id="da428-175">The encryption algorithm and encryption key parameters are not stored along with the private key BLOB.</span></span> <span data-ttu-id="da428-176">Diese Informationen müssen von der Anwendung verwaltet und gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="da428-176">The application must manage and store this information.</span></span> <span data-ttu-id="da428-177">Wenn 0 (null) für *hexpkey* übermittelt wird, wird der private Schlüssel ohne Verschlüsselung exportiert.</span><span class="sxs-lookup"><span data-stu-id="da428-177">If zero is passed for *hExpKey*, the private key will be exported without encryption.</span></span>

 

> [!Caution]  
> <span data-ttu-id="da428-178">Es ist gefährlich, private Schlüssel ohne Verschlüsselung zu exportieren, da Sie dann anfällig für das Abfangen und die Verwendung durch nicht autorisierte Entitäten sind.</span><span class="sxs-lookup"><span data-stu-id="da428-178">It is dangerous to export private keys without encryption because they are then vulnerable to interception and use by unauthorized entities.</span></span>

 

## <a name="simple-key-blobs"></a><span data-ttu-id="da428-179">Einfache Schlüsselblob</span><span class="sxs-lookup"><span data-stu-id="da428-179">Simple Key BLOBs</span></span>

<span data-ttu-id="da428-180">[*Einfache Schlüsselblobs*](../secgloss/s-gly.md), geben Sie **simpleblob** ein, die zum Speichern und transportieren von Sitzungs Schlüsseln verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="da428-180">[*Simple key BLOBs*](../secgloss/s-gly.md), type **SIMPLEBLOB**, are used to store and transport session keys.</span></span> <span data-ttu-id="da428-181">Diese werden immer mit einem [*öffentlichen Schlüsselaustausch Schlüssel*](../secgloss/k-gly.md)verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="da428-181">These are always encrypted with a [*key exchange public key*](../secgloss/k-gly.md).</span></span> <span data-ttu-id="da428-182">Diese Schlüssel werden als Bytefolge im folgenden Format exportiert und importiert.</span><span class="sxs-lookup"><span data-stu-id="da428-182">These keys are exported and imported as a sequence of bytes with the following format.</span></span>

``` syntax
PUBLICKEYSTRUC  publickeystruc ;
ALG_ID          algid;
BYTE            encryptedkey[rsapubkey.bitlen/8];
```

<span data-ttu-id="da428-183">In der folgenden Tabelle wird jede einfache BLOB-Komponente beschrieben.</span><span class="sxs-lookup"><span data-stu-id="da428-183">The following table describes each simple BLOB component.</span></span>



| <span data-ttu-id="da428-184">Feld</span><span class="sxs-lookup"><span data-stu-id="da428-184">Field</span></span>          | <span data-ttu-id="da428-185">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="da428-185">Description</span></span>                                                                                                                                                                                                                                                                                                                   |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da428-186">algid</span><span class="sxs-lookup"><span data-stu-id="da428-186">algid</span></span>          | <span data-ttu-id="da428-187">Eine [**ALG- \_ ID**](alg-id.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="da428-187">An [**ALG\_ID**](alg-id.md) structure.</span></span> <span data-ttu-id="da428-188">Dies gibt in der Regel den calg \_ RSA \_ Keyx-Algorithmus an, der angibt, dass die Sitzungsschlüssel Daten mit einem öffentlichen Schlüsselaustausch Schlüssel mithilfe des [*RSA-Algorithmus für öffentliche Schlüssel*](../secgloss/r-gly.md)verschlüsselt wurden.</span><span class="sxs-lookup"><span data-stu-id="da428-188">This typically specifies the CALG\_RSA\_KEYX algorithm, which indicates that the session key data was encrypted with a key exchange public key, using the [*RSA Public Key algorithm*](../secgloss/r-gly.md).</span></span> |
| <span data-ttu-id="da428-189">EncryptedKey</span><span class="sxs-lookup"><span data-stu-id="da428-189">encryptedkey</span></span>   | <span data-ttu-id="da428-190">Eine **Byte** Sequenz.</span><span class="sxs-lookup"><span data-stu-id="da428-190">A **BYTE** sequence.</span></span> <span data-ttu-id="da428-191">Die verschlüsselten Sitzungsschlüssel Daten haben das Format PKCS \# 1, Typ 2-Verschlüsselungs Block.</span><span class="sxs-lookup"><span data-stu-id="da428-191">The encrypted session key data is in the form of a PKCS \#1, type 2 encryption block.</span></span> <span data-ttu-id="da428-192">Weitere Informationen zu diesem Datenformat finden Sie unter Public Key Cryptography Standards (PKCS), veröffentlicht von RSA Data Security, Inc.</span><span class="sxs-lookup"><span data-stu-id="da428-192">For information about this data format, see the Public Key Cryptography Standards (PKCS), published by RSA Data Security, Inc.</span></span>                                                                                     |
| <span data-ttu-id="da428-193">publickeystruc</span><span class="sxs-lookup"><span data-stu-id="da428-193">publickeystruc</span></span> | <span data-ttu-id="da428-194">Eine [**publickeystruc**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="da428-194">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                                                                                                                                         |



 

<span data-ttu-id="da428-195">Diese Daten haben immer die gleiche Größe wie der Modulo des öffentlichen Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="da428-195">This data is always the same size as the modulus of the public key.</span></span> <span data-ttu-id="da428-196">Öffentliche Schlüssel, die vom Microsoft-Basis Kryptografieanbieter generiert werden, sind z. b. immer 512 Bits (64 Bytes), sodass die verschlüsselten Sitzungsschlüssel Daten immer 64 Bytes sind.</span><span class="sxs-lookup"><span data-stu-id="da428-196">For example, public keys generated by the Microsoft Base Cryptographic Provider are always 512 bits (64 bytes) in length, so the encrypted session key data is also always 64 bytes.</span></span>

 

 
