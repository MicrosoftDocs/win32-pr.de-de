---
description: 'Im Unterschied zur Cryptography API (CryptoAPI) trennt Cryptography API: Next Generation (CNG) Kryptografieanbieter von Schlüsselspeicher Anbietern.'
ms.assetid: ce29bc97-049e-4c82-979f-4c805a318ba0
title: CNG-kryptografiealgorithmusanbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bc64926236157e581ce6406d95681bd8d4add14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347718"
---
# <a name="cng-cryptographic-algorithm-providers"></a><span data-ttu-id="7740d-103">CNG-kryptografiealgorithmusanbieter</span><span class="sxs-lookup"><span data-stu-id="7740d-103">CNG Cryptographic Algorithm Providers</span></span>

<span data-ttu-id="7740d-104">Im Unterschied zur Cryptography API (CryptoAPI) trennt Cryptography API: Next Generation (CNG) Kryptografieanbieter von Schlüsselspeicher Anbietern.</span><span class="sxs-lookup"><span data-stu-id="7740d-104">Unlike Cryptography API (CryptoAPI), Cryptography API: Next Generation (CNG) separates cryptographic providers from key storage providers.</span></span> <span data-ttu-id="7740d-105">Grundlegende Vorgänge für kryptografische Algorithmen, z. b. Hashs und Signierung, werden als primitive Vorgänge oder einfach als primitive bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="7740d-105">Basic cryptographic algorithm operations such as hashing and signing are called primitive operations or simply primitives.</span></span> <span data-ttu-id="7740d-106">CNG enthält einen Anbieter, der die folgenden Algorithmen implementiert.</span><span class="sxs-lookup"><span data-stu-id="7740d-106">CNG includes a provider that implements the following algorithms.</span></span>

-   [<span data-ttu-id="7740d-107">Symmetrische Algorithmen</span><span class="sxs-lookup"><span data-stu-id="7740d-107">Symmetric Algorithms</span></span>](#symmetric-algorithms)
-   [<span data-ttu-id="7740d-108">Asymmetrische Algorithmen</span><span class="sxs-lookup"><span data-stu-id="7740d-108">Asymmetric Algorithms</span></span>](#asymmetric-algorithms)
-   [<span data-ttu-id="7740d-109">Hashalgorithmen</span><span class="sxs-lookup"><span data-stu-id="7740d-109">Hashing Algorithms</span></span>](#hashing-algorithms)
-   [<span data-ttu-id="7740d-110">Schlüsselaustausch Algorithmen</span><span class="sxs-lookup"><span data-stu-id="7740d-110">Key Exchange Algorithms</span></span>](#key-exchange-algorithms)
-   [<span data-ttu-id="7740d-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7740d-111">Related topics</span></span>](#related-topics)

## <a name="symmetric-algorithms"></a><span data-ttu-id="7740d-112">Symmetrische Algorithmen</span><span class="sxs-lookup"><span data-stu-id="7740d-112">Symmetric Algorithms</span></span>



| <span data-ttu-id="7740d-113">Name</span><span class="sxs-lookup"><span data-stu-id="7740d-113">Name</span></span>                                   | <span data-ttu-id="7740d-114">Unterstützte Modi</span><span class="sxs-lookup"><span data-stu-id="7740d-114">Supported modes</span></span>                                                                                                                                                                                                 | <span data-ttu-id="7740d-115">Schlüsselgröße in Bits (Standard/min/max)</span><span class="sxs-lookup"><span data-stu-id="7740d-115">Key size in bits (Default/Min/Max)</span></span> |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------|
| <span data-ttu-id="7740d-116">Advanced Encryption Standard (AES)</span><span class="sxs-lookup"><span data-stu-id="7740d-116">Advanced Encryption Standard (AES)</span></span>     | <span data-ttu-id="7740d-117">ECB, CBC, CFB8, CFB128, GCM, ccm, GMAC, CMAC, AES Key Wrap, XTS</span><span class="sxs-lookup"><span data-stu-id="7740d-117">ECB, CBC, CFB8, CFB128, GCM, CCM, GMAC, CMAC, AES Key Wrap, XTS</span></span><br/> <span data-ttu-id="7740d-118">**Windows 8:** Die Unterstützung für die CFB128-und CMAC-Modi beginnt.</span><span class="sxs-lookup"><span data-stu-id="7740d-118">**Windows 8:** Support for the CFB128 and CMAC modes begins.</span></span><br/> <span data-ttu-id="7740d-119">**Windows 10:** Die Unterstützung für den XTS-AES-Modus beginnt.</span><span class="sxs-lookup"><span data-stu-id="7740d-119">**Windows 10:** Support for XTS-AES mode begins.</span></span><br/> | <span data-ttu-id="7740d-120">128/192/256</span><span class="sxs-lookup"><span data-stu-id="7740d-120">128/192/256</span></span>                        |
| <span data-ttu-id="7740d-121">Data Encryption Standard (des)</span><span class="sxs-lookup"><span data-stu-id="7740d-121">Data Encryption Standard (DES)</span></span>         | <span data-ttu-id="7740d-122">ECB, CBC, CFB8, CFB64</span><span class="sxs-lookup"><span data-stu-id="7740d-122">ECB, CBC, CFB8, CFB64</span></span><br/> <span data-ttu-id="7740d-123">**Windows 8:** Die Unterstützung für den CFB64-Modus beginnt.</span><span class="sxs-lookup"><span data-stu-id="7740d-123">**Windows 8:** Support for the CFB64 mode begins.</span></span><br/>                                                                                                                   | <span data-ttu-id="7740d-124">56/56/56</span><span class="sxs-lookup"><span data-stu-id="7740d-124">56/56/56</span></span>                           |
| <span data-ttu-id="7740d-125">Data Encryption Standard XoReD (DESX)</span><span class="sxs-lookup"><span data-stu-id="7740d-125">Data Encryption Standard XORed(DESX)</span></span>   | <span data-ttu-id="7740d-126">ECB, CBC, CFB8, CFB64</span><span class="sxs-lookup"><span data-stu-id="7740d-126">ECB, CBC, CFB8, CFB64</span></span> <br/> <span data-ttu-id="7740d-127">**Windows 8:** Die Unterstützung für den CFB64-Modus beginnt.</span><span class="sxs-lookup"><span data-stu-id="7740d-127">**Windows 8:** Support for the CFB64 mode begins.</span></span><br/>                                                                                                                  | <span data-ttu-id="7740d-128">192/192/192</span><span class="sxs-lookup"><span data-stu-id="7740d-128">192/192/192</span></span>                        |
| <span data-ttu-id="7740d-129">Triple Data Encryption Standard (3DES)</span><span class="sxs-lookup"><span data-stu-id="7740d-129">Triple Data Encryption Standard (3DES)</span></span> | <span data-ttu-id="7740d-130">ECB, CBC, CFB8, CFB64</span><span class="sxs-lookup"><span data-stu-id="7740d-130">ECB, CBC, CFB8, CFB64</span></span> <br/> <span data-ttu-id="7740d-131">**Windows 8:** Die Unterstützung für den CFB64-Modus beginnt.</span><span class="sxs-lookup"><span data-stu-id="7740d-131">**Windows 8:** Support for the CFB64 mode begins.</span></span><br/>                                                                                                                  | <span data-ttu-id="7740d-132">112/168</span><span class="sxs-lookup"><span data-stu-id="7740d-132">112/168</span></span>                            |
| <span data-ttu-id="7740d-133">RSA Data Security 2 (RC2)</span><span class="sxs-lookup"><span data-stu-id="7740d-133">RSA Data Security 2 (RC2)</span></span>              | <span data-ttu-id="7740d-134">Die Modi ECB, CBC, CFB8 und CFB64 werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7740d-134">ECB, CBC, CFB8, CFB64 modes are supported.</span></span><br/> <span data-ttu-id="7740d-135">**Windows 8:** Die Unterstützung für den CFB64-Modus beginnt.</span><span class="sxs-lookup"><span data-stu-id="7740d-135">**Windows 8:** Support for the CFB64 mode begins.</span></span><br/>                                                                                              | <span data-ttu-id="7740d-136">16 bis 128 in 8-Bit-Inkrementen</span><span class="sxs-lookup"><span data-stu-id="7740d-136">16 to 128 in 8 bit increments</span></span>      |
| <span data-ttu-id="7740d-137">RSA Data Security 4 (RC4)</span><span class="sxs-lookup"><span data-stu-id="7740d-137">RSA Data Security 4 (RC4)</span></span>              |                                                                                                                                                                                                                 | <span data-ttu-id="7740d-138">8 bis 512, in 8-Bit-Inkrementen</span><span class="sxs-lookup"><span data-stu-id="7740d-138">8 to 512, in 8-bit increments</span></span>      |



 

## <a name="asymmetric-algorithms"></a><span data-ttu-id="7740d-139">Asymmetrische Algorithmen</span><span class="sxs-lookup"><span data-stu-id="7740d-139">Asymmetric Algorithms</span></span>



| <span data-ttu-id="7740d-140">Name</span><span class="sxs-lookup"><span data-stu-id="7740d-140">Name</span></span>                              | <span data-ttu-id="7740d-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="7740d-141">Notes</span></span>                                                                                                                                                                             | <span data-ttu-id="7740d-142">Schlüsselgröße in Bits (Standard/min/max)</span><span class="sxs-lookup"><span data-stu-id="7740d-142">Key size in bits (Default/Min/Max)</span></span>                                                                            |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7740d-143">Digital Signature-Algorithmus (DSA)</span><span class="sxs-lookup"><span data-stu-id="7740d-143">Digital Signature Algorithm (DSA)</span></span> | <span data-ttu-id="7740d-144">Die Implementierung entspricht dem Wert von "fps 186-3" für Schlüsselgrößen zwischen 1024 und 3072 Bits.</span><span class="sxs-lookup"><span data-stu-id="7740d-144">Implementation conforms to FIPS 186-3 for key sizes between 1024 and 3072 bits.</span></span> <br/> <span data-ttu-id="7740d-145">Die Implementierung entspricht dem Wert von "fps 186-2" für Schlüsselgrößen von 512 bis 1024 Bits.</span><span class="sxs-lookup"><span data-stu-id="7740d-145">Implementation conforms to FIPS 186-2 for key sizes from 512 to 1024 bits.</span></span><br/> | <span data-ttu-id="7740d-146">512 bis 3072, in 64-Bit-Inkrementen</span><span class="sxs-lookup"><span data-stu-id="7740d-146">512 to 3072, in 64-bit increments</span></span><br/> <span data-ttu-id="7740d-147">**Windows 8:** Die Unterstützung für die 3072-Bit-Taste beginnt.</span><span class="sxs-lookup"><span data-stu-id="7740d-147">**Windows 8:** Support for the a 3072 bit key begins.</span></span><br/> |
| <span data-ttu-id="7740d-148">RSA</span><span class="sxs-lookup"><span data-stu-id="7740d-148">RSA</span></span>                               | <span data-ttu-id="7740d-149">Schließt RSA-Algorithmen ein, die PKCS1, optimale OAEP (asymmetrisch Encryption Auffüllung)-Codierung oder-Auffüll-oder Auffüll-und Auffüll-und Auffüll Text Auffüll Zeichen verwenden.</span><span class="sxs-lookup"><span data-stu-id="7740d-149">Includes RSA algorithms that use PKCS1, Optimal Asymmetric Encryption Padding (OAEP) encoding or padding, or Probabilistic Signature Scheme (PSS) plaintext padding</span></span>               | <span data-ttu-id="7740d-150">512 bis 16384, in 64-Bit-Inkrementen</span><span class="sxs-lookup"><span data-stu-id="7740d-150">512 to 16384, in 64-bit increments</span></span>                                                                            |



 

## <a name="hashing-algorithms"></a><span data-ttu-id="7740d-151">Hashalgorithmen</span><span class="sxs-lookup"><span data-stu-id="7740d-151">Hashing Algorithms</span></span>



| <span data-ttu-id="7740d-152">Name</span><span class="sxs-lookup"><span data-stu-id="7740d-152">Name</span></span>                               | <span data-ttu-id="7740d-153">Notizen</span><span class="sxs-lookup"><span data-stu-id="7740d-153">Notes</span></span>               | <span data-ttu-id="7740d-154">Schlüsselgröße in Bits (Standard/min/max)</span><span class="sxs-lookup"><span data-stu-id="7740d-154">Key size in bits (Default/Min/Max)</span></span> |
|------------------------------------|---------------------|------------------------------------|
| <span data-ttu-id="7740d-155">Secure-Hash-Algorithmus 1 (SHA1)</span><span class="sxs-lookup"><span data-stu-id="7740d-155">Secure Hash Algorithm 1 (SHA1)</span></span>     | <span data-ttu-id="7740d-156">Umfasst HmacSha1</span><span class="sxs-lookup"><span data-stu-id="7740d-156">Includes HmacSha1</span></span>   | <span data-ttu-id="7740d-157">160/160/160</span><span class="sxs-lookup"><span data-stu-id="7740d-157">160/160/160</span></span>                        |
| <span data-ttu-id="7740d-158">Secure Hash-Algorithmus 256 (SHA256)</span><span class="sxs-lookup"><span data-stu-id="7740d-158">Secure Hash Algorithm 256 (SHA256)</span></span> | <span data-ttu-id="7740d-159">Umfasst HmacSha256</span><span class="sxs-lookup"><span data-stu-id="7740d-159">Includes HmacSha256</span></span> | <span data-ttu-id="7740d-160">256/256/256</span><span class="sxs-lookup"><span data-stu-id="7740d-160">256/256/256</span></span>                        |
| <span data-ttu-id="7740d-161">Secure Hash-Algorithmus 384 (SHA384)</span><span class="sxs-lookup"><span data-stu-id="7740d-161">Secure Hash Algorithm 384 (SHA384)</span></span> | <span data-ttu-id="7740d-162">Umfasst HmacSha384</span><span class="sxs-lookup"><span data-stu-id="7740d-162">Includes HmacSha384</span></span> | <span data-ttu-id="7740d-163">384/384/384</span><span class="sxs-lookup"><span data-stu-id="7740d-163">384/384/384</span></span>                        |
| <span data-ttu-id="7740d-164">Secure Hash-Algorithmus 512 (SHA512)</span><span class="sxs-lookup"><span data-stu-id="7740d-164">Secure Hash Algorithm 512 (SHA512)</span></span> | <span data-ttu-id="7740d-165">Umfasst HmacSha512</span><span class="sxs-lookup"><span data-stu-id="7740d-165">Includes HmacSha512</span></span> | <span data-ttu-id="7740d-166">512/512/512</span><span class="sxs-lookup"><span data-stu-id="7740d-166">512/512/512</span></span>                        |
| <span data-ttu-id="7740d-167">Message Digest 2 (MD2)</span><span class="sxs-lookup"><span data-stu-id="7740d-167">Message Digest 2 (MD2)</span></span>             | <span data-ttu-id="7740d-168">Umfasst HmacMd2</span><span class="sxs-lookup"><span data-stu-id="7740d-168">Includes HmacMd2</span></span>    | <span data-ttu-id="7740d-169">128/128/128</span><span class="sxs-lookup"><span data-stu-id="7740d-169">128/128/128</span></span>                        |
| <span data-ttu-id="7740d-170">Message Digest 4 (MD4)</span><span class="sxs-lookup"><span data-stu-id="7740d-170">Message Digest 4 (MD4)</span></span>             | <span data-ttu-id="7740d-171">Umfasst HmacMd4</span><span class="sxs-lookup"><span data-stu-id="7740d-171">Includes HmacMd4</span></span>    | <span data-ttu-id="7740d-172">128/128/128</span><span class="sxs-lookup"><span data-stu-id="7740d-172">128/128/128</span></span>                        |
| <span data-ttu-id="7740d-173">Message Digest 5 (MD5)</span><span class="sxs-lookup"><span data-stu-id="7740d-173">Message Digest 5 (MD5)</span></span>             | <span data-ttu-id="7740d-174">Umfasst HmacMd5</span><span class="sxs-lookup"><span data-stu-id="7740d-174">Includes HmacMd5</span></span>    | <span data-ttu-id="7740d-175">128/128/128</span><span class="sxs-lookup"><span data-stu-id="7740d-175">128/128/128</span></span>                        |



 

## <a name="key-exchange-algorithms"></a><span data-ttu-id="7740d-176">Schlüsselaustausch Algorithmen</span><span class="sxs-lookup"><span data-stu-id="7740d-176">Key Exchange Algorithms</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7740d-177">Algorithmusname</span><span class="sxs-lookup"><span data-stu-id="7740d-177">Algorithm name</span></span></th>
<th><span data-ttu-id="7740d-178">Notizen</span><span class="sxs-lookup"><span data-stu-id="7740d-178">Notes</span></span></th>
<th><span data-ttu-id="7740d-179">Schlüsselgröße in Bits (Standard/min/max)</span><span class="sxs-lookup"><span data-stu-id="7740d-179">Key size in bits (Default/Min/Max)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7740d-180">Diffie-Hellman Schlüsselaustausch Algorithmus</span><span class="sxs-lookup"><span data-stu-id="7740d-180">Diffie-Hellman Key Exchange Algorithm</span></span></td>

<td><span data-ttu-id="7740d-181">512 bis 4096, in 64-Bit-Inkrementen</span><span class="sxs-lookup"><span data-stu-id="7740d-181">512 to 4096, in 64-bit increments</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7740d-182">ECDH (Elliptic Curve Diffie-Hellman)</span><span class="sxs-lookup"><span data-stu-id="7740d-182">Elliptic Curve Diffie-Hellman (ECDH)</span></span></td>
<td><span data-ttu-id="7740d-183">Schließt Kurven ein, die die öffentlichen Schlüssel 256, 384 und 521 Bit verwenden, wie in SP800-56a angegeben.</span><span class="sxs-lookup"><span data-stu-id="7740d-183">Includes curves that use 256, 384 and 521 bit public keys as specified in SP800-56A.</span></span></td>
<td><span data-ttu-id="7740d-184">256/384/521</span><span class="sxs-lookup"><span data-stu-id="7740d-184">256/384/521</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7740d-185">ECDSA (Elliptic Curve Digital Signature-Algorithmus)</span><span class="sxs-lookup"><span data-stu-id="7740d-185">Elliptic Curve Digital Signature Algorithm (ECDSA)</span></span></td>
<td><span data-ttu-id="7740d-186">Schließt Kurven ein, die die öffentlichen Schlüssel 256, 384 und 521 Bit verwenden, wie in "fps 186-3" angegeben.</span><span class="sxs-lookup"><span data-stu-id="7740d-186">Includes curves that use 256, 384 and 521 bit public keys as specified in FIPS 186-3.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="7740d-187">Verwenden Sie <strong>certutil displayecccurve</strong>, um alle benannten elliptischen Kurven anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="7740d-187">To display all named elliptic curves, use <strong>certutil  displayEccCurve</strong>.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="7740d-188">256/384/521</span><span class="sxs-lookup"><span data-stu-id="7740d-188">256/384/521</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="7740d-189">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7740d-189">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7740d-190">**CNG-Algorithmusbezeichner**</span><span class="sxs-lookup"><span data-stu-id="7740d-190">**CNG Algorithm Identifiers**</span></span>](/windows/desktop/SecCNG/cng-algorithm-identifiers)
</dt> <dt>

[<span data-ttu-id="7740d-191">Kryptografische CNG-Funktionen</span><span class="sxs-lookup"><span data-stu-id="7740d-191">CNG Cryptographic Primitive Functions</span></span>](/windows/desktop/SecCNG/cng-cryptographic-primitive-functions)
</dt> <dt>

[<span data-ttu-id="7740d-192">Grundlegendes zu Kryptografieanbietern</span><span class="sxs-lookup"><span data-stu-id="7740d-192">Understanding Cryptographic Providers</span></span>](understanding-cryptographic-providers.md)
</dt> </dl>

 

