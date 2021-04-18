---
description: Gibt einen Algorithmusbezeichner an.
ms.assetid: 557436b4-f7f1-4708-acc7-c6b47e6322ad
title: ALG_ID (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ab1eb6dc262faae76d38f2b96c9e6191a313390
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366237"
---
# <a name="alg_id"></a><span data-ttu-id="bfc75-103">ALG_ID</span><span class="sxs-lookup"><span data-stu-id="bfc75-103">ALG_ID</span></span>

<span data-ttu-id="bfc75-104">Der **ALG_ID** -Datentyp gibt einen Algorithmusbezeichner an.</span><span class="sxs-lookup"><span data-stu-id="bfc75-104">The **ALG_ID** data type specifies an algorithm identifier.</span></span> <span data-ttu-id="bfc75-105">Parameter dieses Datentyps werden an die meisten Funktionen in CryptoAPI übermittelt.</span><span class="sxs-lookup"><span data-stu-id="bfc75-105">Parameters of this data type are passed to most of the functions in CryptoAPI.</span></span>


```C++
typedef unsigned int ALG_ID;
```



<span data-ttu-id="bfc75-106">In der folgenden Tabelle werden die zurzeit definierten Algorithmusbezeichner aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="bfc75-106">The following table lists the algorithm identifiers that are currently defined.</span></span> <span data-ttu-id="bfc75-107">Autoren von benutzerdefinierten [*Kryptografiedienstanbietern*](../secgloss/c-gly.md) (CSPs) können neue Werte definieren.</span><span class="sxs-lookup"><span data-stu-id="bfc75-107">Authors of custom [*cryptographic service providers*](../secgloss/c-gly.md) (CSPs) can define new values.</span></span> <span data-ttu-id="bfc75-108">Außerdem sind die **ALG_ID** , die von benutzerdefinierten CSPs für die Schlüssel Spezifikationen **AT_KEYEXCHANGE** und **AT_SIGNATURE** verwendet werden, vom Anbieter abhängig.</span><span class="sxs-lookup"><span data-stu-id="bfc75-108">Also, the **ALG_ID** used by custom CSPs for the key specifications **AT_KEYEXCHANGE** and **AT_SIGNATURE** are provider dependent.</span></span> <span data-ttu-id="bfc75-109">Aktuelle Zuordnungen Folgen der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="bfc75-109">Current mappings follow the table.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bfc75-110">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="bfc75-110">Identifier</span></span></th>
<th><span data-ttu-id="bfc75-111">Wert</span><span class="sxs-lookup"><span data-stu-id="bfc75-111">Value</span></span></th>
<th><span data-ttu-id="bfc75-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bfc75-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bfc75-113">CALG_3DES</span><span class="sxs-lookup"><span data-stu-id="bfc75-113">CALG_3DES</span></span></td>
<td><span data-ttu-id="bfc75-114">0x00006603</span><span class="sxs-lookup"><span data-stu-id="bfc75-114">0x00006603</span></span></td>
<td><span data-ttu-id="bfc75-115"><a href="/windows/desktop/SecGloss/t-gly"><em>Triple des</em></a> -Verschlüsselungsalgorithmus.</span><span class="sxs-lookup"><span data-stu-id="bfc75-115"><a href="/windows/desktop/SecGloss/t-gly"><em>Triple DES</em></a> encryption algorithm.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bfc75-116">CALG_3DES_112</span><span class="sxs-lookup"><span data-stu-id="bfc75-116">CALG_3DES_112</span></span></td>
<td><span data-ttu-id="bfc75-117">0x00006609</span><span class="sxs-lookup"><span data-stu-id="bfc75-117">0x00006609</span></span></td>
<td><span data-ttu-id="bfc75-118">Die zwei-Schlüssel- <a href="/windows/desktop/SecGloss/t-gly"><em>Triple-des</em></a> -Verschlüsselung mit einer effektiven Schlüssellänge von 112 Bits.</span><span class="sxs-lookup"><span data-stu-id="bfc75-118">Two-key <a href="/windows/desktop/SecGloss/t-gly"><em>triple DES</em></a> encryption with effective key length equal to 112 bits.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bfc75-119">CALG_AES</span><span class="sxs-lookup"><span data-stu-id="bfc75-119">CALG_AES</span></span></td>
<td><span data-ttu-id="bfc75-120">0x00006611</span><span class="sxs-lookup"><span data-stu-id="bfc75-120">0x00006611</span></span></td>
<td><span data-ttu-id="bfc75-121">Advanced Encryption Standard (AES).</span><span class="sxs-lookup"><span data-stu-id="bfc75-121">Advanced Encryption Standard (AES).</span></span> <span data-ttu-id="bfc75-122">Dieser Algorithmus wird vom <a href="microsoft-aes-cryptographic-provider.md">Microsoft AES-Kryptografieanbieter</a>unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bfc75-122">This algorithm is supported by the <a href="microsoft-aes-cryptographic-provider.md">Microsoft AES Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bfc75-123">CALG_AES_128</span><span class="sxs-lookup"><span data-stu-id="bfc75-123">CALG_AES_128</span></span></td>
<td><span data-ttu-id="bfc75-124">0x0000660e</span><span class="sxs-lookup"><span data-stu-id="bfc75-124">0x0000660e</span></span></td>
<td><span data-ttu-id="bfc75-125">128-Bit-AES.</span><span class="sxs-lookup"><span data-stu-id="bfc75-125">128 bit AES.</span></span> <span data-ttu-id="bfc75-126">Dieser Algorithmus wird vom <a href="microsoft-aes-cryptographic-provider.md">Microsoft AES-Kryptografieanbieter</a>unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bfc75-126">This algorithm is supported by the <a href="microsoft-aes-cryptographic-provider.md">Microsoft AES Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bfc75-127">CALG_AES_192</span><span class="sxs-lookup"><span data-stu-id="bfc75-127">CALG_AES_192</span></span></td>
<td><span data-ttu-id="bfc75-128">0x0000660f</span><span class="sxs-lookup"><span data-stu-id="bfc75-128">0x0000660f</span></span></td>
<td><span data-ttu-id="bfc75-129">192-Bit-AES.</span><span class="sxs-lookup"><span data-stu-id="bfc75-129">192 bit AES.</span></span> <span data-ttu-id="bfc75-130">Dieser Algorithmus wird vom <a href="microsoft-aes-cryptographic-provider.md">Microsoft AES-Kryptografieanbieter</a>unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bfc75-130">This algorithm is supported by the <a href="microsoft-aes-cryptographic-provider.md">Microsoft AES Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bfc75-131">CALG_AES_256</span><span class="sxs-lookup"><span data-stu-id="bfc75-131">CALG_AES_256</span></span></td>
<td><span data-ttu-id="bfc75-132">0x00006610</span><span class="sxs-lookup"><span data-stu-id="bfc75-132">0x00006610</span></span></td>
<td><span data-ttu-id="bfc75-133">256-Bit-AES.</span><span class="sxs-lookup"><span data-stu-id="bfc75-133">256 bit AES.</span></span> <span data-ttu-id="bfc75-134">Dieser Algorithmus wird vom <a href="microsoft-aes-cryptographic-provider.md">Microsoft AES-Kryptografieanbieter</a>unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bfc75-134">This algorithm is supported by the <a href="microsoft-aes-cryptographic-provider.md">Microsoft AES Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bfc75-135">CALG_AGREEDKEY_ANY</span><span class="sxs-lookup"><span data-stu-id="bfc75-135">CALG_AGREEDKEY_ANY</span></span></td>
<td><span data-ttu-id="bfc75-136">0x0000aa03</span><span class="sxs-lookup"><span data-stu-id="bfc75-136">0x0000aa03</span></span></td>
<td><span data-ttu-id="bfc75-137">Temporärer Algorithmusbezeichner für Handles von Diffie-Hellman – vereinbarten Schlüsseln.</span><span class="sxs-lookup"><span data-stu-id="bfc75-137">Temporary algorithm identifier for handles of Diffie-Hellman–agreed keys.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bfc75-138">CALG_CYLINK_MEK</span><span class="sxs-lookup"><span data-stu-id="bfc75-138">CALG_CYLINK_MEK</span></span></td>
<td><span data-ttu-id="bfc75-139">0x0000660c</span><span class="sxs-lookup"><span data-stu-id="bfc75-139">0x0000660c</span></span></td>
<td><span data-ttu-id="bfc75-140">Ein Algorithmus zum Erstellen eines 40-Bit-des-Schlüssels, der Paritätsbits und NULL-Bit-Schlüssel Bits enthält, um die Schlüssellänge 64 Bits zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="bfc75-140">An algorithm to create a 40-bit DES key that has parity bits and zeroed key bits to make its key length 64 bits.</span></span> <span data-ttu-id="bfc75-141">Dieser Algorithmus wird vom Microsoft- <a href=""></a> <a href="microsoft-base-cryptographic-provider.md">Basis-Kryptografieanbieter</a>unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bfc75-141">This algorithm is supported by the <a href=""></a><a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bfc75-142">CALG_DES</span><span class="sxs-lookup"><span data-stu-id="bfc75-142">CALG_DES</span></span></td>
<td><span data-ttu-id="bfc75-143">0x00006601</span><span class="sxs-lookup"><span data-stu-id="bfc75-143">0x00006601</span></span></td>
<td><span data-ttu-id="bfc75-144">DES-Verschlüsselungsalgorithmus.</span><span class="sxs-lookup"><span data-stu-id="bfc75-144">DES encryption algorithm.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bfc75-145">CALG_DESX</span><span class="sxs-lookup"><span data-stu-id="bfc75-145">CALG_DESX</span></span></td>
<td><span data-ttu-id="bfc75-146">0x00006604</span><span class="sxs-lookup"><span data-stu-id="bfc75-146">0x00006604</span></span></td>
<td><span data-ttu-id="bfc75-147">DESX-Verschlüsselungsalgorithmus.</span><span class="sxs-lookup"><span data-stu-id="bfc75-147">DESX encryption algorithm.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bfc75-148">CALG_DH_EPHEM</span><span class="sxs-lookup"><span data-stu-id="bfc75-148">CALG_DH_EPHEM</span></span></td>
<td><span data-ttu-id="bfc75-149">0x0000aa02</span><span class="sxs-lookup"><span data-stu-id="bfc75-149">0x0000aa02</span></span></td>
<td><span data-ttu-id="bfc75-150">Diffie-Hellman kurzlebigen Algorithmus für den Schlüsselaustausch.</span><span class="sxs-lookup"><span data-stu-id="bfc75-150">Diffie-Hellman ephemeral key exchange algorithm.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bfc75-151">CALG_DH_SF</span><span class="sxs-lookup"><span data-stu-id="bfc75-151">CALG_DH_SF</span></span></td>
<td><span data-ttu-id="bfc75-152">0x0000aa01</span><span class="sxs-lookup"><span data-stu-id="bfc75-152">0x0000aa01</span></span></td>
<td><span data-ttu-id="bfc75-153">Diffie-Hellman den Algorithmus zum Speichern und Weiterleiten eines Schlüssel Austauschs.</span><span class="sxs-lookup"><span data-stu-id="bfc75-153">Diffie-Hellman store and forward key exchange algorithm.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bfc75-154">CALG_DSS_SIGN</span><span class="sxs-lookup"><span data-stu-id="bfc75-154">CALG_DSS_SIGN</span></span></td>
<td><span data-ttu-id="bfc75-155">0x00002200</span><span class="sxs-lookup"><span data-stu-id="bfc75-155">0x00002200</span></span></td>
<td><span data-ttu-id="bfc75-156">DSA-Algorithmus für die <a href="/windows/desktop/SecGloss/p-gly"><em>öffentliche Schlüssel</em></a> Signatur.</span><span class="sxs-lookup"><span data-stu-id="bfc75-156">DSA <a href="/windows/desktop/SecGloss/p-gly"><em>public key</em></a> signature algorithm.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bfc75-157">CALG_ECDH</span><span class="sxs-lookup"><span data-stu-id="bfc75-157">CALG_ECDH</span></span></td>
<td><span data-ttu-id="bfc75-158">0x0000aa05</span><span class="sxs-lookup"><span data-stu-id="bfc75-158">0x0000aa05</span></span></td>
<td><span data-ttu-id="bfc75-159">Elliptische Kurve Diffie-Hellman Algorithmus für den Schlüsselaustausch.</span><span class="sxs-lookup"><span data-stu-id="bfc75-159">Elliptic curve Diffie-Hellman key exchange algorithm.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="bfc75-160">Dieser Algorithmus wird nur über die <a href="/windows/desktop/SecCNG/cng-portal">kryptografieapi: Next Generation</a>unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bfc75-160">This algorithm is supported only through <a href="/windows/desktop/SecCNG/cng-portal">Cryptography API: Next Generation</a>.</span></span>
</blockquote>
<br/> <span data-ttu-id="bfc75-161"><strong>Windows Server 2003 und Windows XP:</strong> Dieser Algorithmus wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bfc75-161"><strong>Windows Server 2003 and Windows XP:</strong> This algorithm is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bfc75-162">CALG_ECDH_EPHEM</span><span class="sxs-lookup"><span data-stu-id="bfc75-162">CALG_ECDH_EPHEM</span></span></td>
<td><span data-ttu-id="bfc75-163">0x0000ae06</span><span class="sxs-lookup"><span data-stu-id="bfc75-163">0x0000ae06</span></span></td>
<td><span data-ttu-id="bfc75-164">Kurzlebige elliptische Kurve Diffie-Hellman Algorithmus für den Schlüsselaustausch.</span><span class="sxs-lookup"><span data-stu-id="bfc75-164">Ephemeral elliptic curve Diffie-Hellman key exchange algorithm.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="bfc75-165">Dieser Algorithmus wird nur über die <a href="/windows/desktop/SecCNG/cng-portal">kryptografieapi: Next Generation</a>unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bfc75-165">This algorithm is supported only through <a href="/windows/desktop/SecCNG/cng-portal">Cryptography API: Next Generation</a>.</span></span>
</blockquote>
<br/> <span data-ttu-id="bfc75-166"><strong>Windows Server 2003 und Windows XP:</strong> Dieser Algorithmus wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bfc75-166"><strong>Windows Server 2003 and Windows XP:</strong> This algorithm is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bfc75-167">CALG_ECDSA</span><span class="sxs-lookup"><span data-stu-id="bfc75-167">CALG_ECDSA</span></span></td>
<td><span data-ttu-id="bfc75-168">0x00002203</span><span class="sxs-lookup"><span data-stu-id="bfc75-168">0x00002203</span></span></td>
<td><span data-ttu-id="bfc75-169">Digitaler Signatur Algorithmus für elliptische Kurve.</span><span class="sxs-lookup"><span data-stu-id="bfc75-169">Elliptic curve digital signature algorithm.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="bfc75-170">Dieser Algorithmus wird nur über die <a href="/windows/desktop/SecCNG/cng-portal">kryptografieapi: Next Generation</a>unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bfc75-170">This algorithm is supported only through <a href="/windows/desktop/SecCNG/cng-portal">Cryptography API: Next Generation</a>.</span></span>
</blockquote>
<br/> <span data-ttu-id="bfc75-171"><strong>Windows Server 2003 und Windows XP:</strong> Dieser Algorithmus wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bfc75-171"><strong>Windows Server 2003 and Windows XP:</strong> This algorithm is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bfc75-172">CALG_ECMQV</span><span class="sxs-lookup"><span data-stu-id="bfc75-172">CALG_ECMQV</span></span></td>
<td><span data-ttu-id="bfc75-173">0x0000a001</span><span class="sxs-lookup"><span data-stu-id="bfc75-173">0x0000a001</span></span></td>
<td><span data-ttu-id="bfc75-174">Schlüsselaustausch Algorithmus für die elliptische Kurve "Menezes", "Qu" und "Vanstone" (mqv).</span><span class="sxs-lookup"><span data-stu-id="bfc75-174">Elliptic curve Menezes, Qu, and Vanstone (MQV) key exchange algorithm.</span></span> <span data-ttu-id="bfc75-175">Dieser Algorithmus wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bfc75-175">This algorithm is not supported.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bfc75-176">CALG_HASH_REPLACE_OWF</span><span class="sxs-lookup"><span data-stu-id="bfc75-176">CALG_HASH_REPLACE_OWF</span></span></td>
<td><span data-ttu-id="bfc75-177">0x0000800b</span><span class="sxs-lookup"><span data-stu-id="bfc75-177">0x0000800b</span></span></td>
<td><span data-ttu-id="bfc75-178">Ein unidirektionaler Funktions Hash Algorithmus.</span><span class="sxs-lookup"><span data-stu-id="bfc75-178">One way function hashing algorithm.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bfc75-179">CALG_HUGHES_MD5</span><span class="sxs-lookup"><span data-stu-id="bfc75-179">CALG_HUGHES_MD5</span></span></td>
<td><span data-ttu-id="bfc75-180">0x0000a003</span><span class="sxs-lookup"><span data-stu-id="bfc75-180">0x0000a003</span></span></td>
<td><span data-ttu-id="bfc75-181">Hughes MD5-Hash Algorithmus.</span><span class="sxs-lookup"><span data-stu-id="bfc75-181">Hughes MD5 hashing algorithm.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bfc75-182">CALG_HMAC</span><span class="sxs-lookup"><span data-stu-id="bfc75-182">CALG_HMAC</span></span></td>
<td><span data-ttu-id="bfc75-183">0x00008009</span><span class="sxs-lookup"><span data-stu-id="bfc75-183">0x00008009</span></span></td>
<td><span data-ttu-id="bfc75-184">HMAC-verschlüsselter Hash Algorithmus.</span><span class="sxs-lookup"><span data-stu-id="bfc75-184">HMAC keyed hash algorithm.</span></span> <span data-ttu-id="bfc75-185">Dieser Algorithmus wird vom Microsoft- <a href="microsoft-base-cryptographic-provider.md">Basis-Kryptografieanbieter</a>unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bfc75-185">This algorithm is supported by the <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bfc75-186">CALG_KEA_KEYX</span><span class="sxs-lookup"><span data-stu-id="bfc75-186">CALG_KEA_KEYX</span></span></td>
<td><span data-ttu-id="bfc75-187">0x0000aa04</span><span class="sxs-lookup"><span data-stu-id="bfc75-187">0x0000aa04</span></span></td>
<td><span data-ttu-id="bfc75-188">KEA-Schlüsselaustausch Algorithmus (Fortezza).</span><span class="sxs-lookup"><span data-stu-id="bfc75-188">KEA key exchange algorithm (FORTEZZA).</span></span> <span data-ttu-id="bfc75-189">Dieser Algorithmus wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bfc75-189">This algorithm is not supported.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bfc75-190">CALG_MAC</span><span class="sxs-lookup"><span data-stu-id="bfc75-190">CALG_MAC</span></span></td>
<td><span data-ttu-id="bfc75-191">0x00008005</span><span class="sxs-lookup"><span data-stu-id="bfc75-191">0x00008005</span></span></td>
<td><span data-ttu-id="bfc75-192"><a href="/windows/desktop/SecGloss/m-gly"><em>Mac</em></a> -verschlüsselter Hash Algorithmus.</span><span class="sxs-lookup"><span data-stu-id="bfc75-192"><a href="/windows/desktop/SecGloss/m-gly"><em>MAC</em></a> keyed hash algorithm.</span></span> <span data-ttu-id="bfc75-193">Dieser Algorithmus wird vom Microsoft- <a href="microsoft-base-cryptographic-provider.md">Basis-Kryptografieanbieter</a>unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bfc75-193">This algorithm is supported by the <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bfc75-194">CALG_MD2</span><span class="sxs-lookup"><span data-stu-id="bfc75-194">CALG_MD2</span></span></td>
<td><span data-ttu-id="bfc75-195">0x00008001</span><span class="sxs-lookup"><span data-stu-id="bfc75-195">0x00008001</span></span></td>
<td><span data-ttu-id="bfc75-196">MD2-Hashalgorithmus</span><span class="sxs-lookup"><span data-stu-id="bfc75-196">MD2 hashing algorithm.</span></span> <span data-ttu-id="bfc75-197">Dieser Algorithmus wird vom Microsoft- <a href="microsoft-base-cryptographic-provider.md">Basis-Kryptografieanbieter</a>unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bfc75-197">This algorithm is supported by the <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bfc75-198">CALG_MD4</span><span class="sxs-lookup"><span data-stu-id="bfc75-198">CALG_MD4</span></span></td>
<td><span data-ttu-id="bfc75-199">0x00008002</span><span class="sxs-lookup"><span data-stu-id="bfc75-199">0x00008002</span></span></td>
<td><span data-ttu-id="bfc75-200">MD4-Hashalgorithmus</span><span class="sxs-lookup"><span data-stu-id="bfc75-200">MD4 hashing algorithm.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bfc75-201">CALG_MD5</span><span class="sxs-lookup"><span data-stu-id="bfc75-201">CALG_MD5</span></span></td>
<td><span data-ttu-id="bfc75-202">0x00008003</span><span class="sxs-lookup"><span data-stu-id="bfc75-202">0x00008003</span></span></td>
<td><span data-ttu-id="bfc75-203">MD5-Hashalgorithmus</span><span class="sxs-lookup"><span data-stu-id="bfc75-203">MD5 hashing algorithm.</span></span> <span data-ttu-id="bfc75-204">Dieser Algorithmus wird vom Microsoft- <a href="microsoft-base-cryptographic-provider.md">Basis-Kryptografieanbieter</a>unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bfc75-204">This algorithm is supported by the <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bfc75-205">CALG_NO_SIGN</span><span class="sxs-lookup"><span data-stu-id="bfc75-205">CALG_NO_SIGN</span></span></td>
<td><span data-ttu-id="bfc75-206">0x00002000</span><span class="sxs-lookup"><span data-stu-id="bfc75-206">0x00002000</span></span></td>
<td><span data-ttu-id="bfc75-207">Kein Signatur Algorithmus.</span><span class="sxs-lookup"><span data-stu-id="bfc75-207">No signature algorithm.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bfc75-208">CALG_OID_INFO_CNG_ONLY</span><span class="sxs-lookup"><span data-stu-id="bfc75-208">CALG_OID_INFO_CNG_ONLY</span></span></td>
<td><span data-ttu-id="bfc75-209">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="bfc75-209">0xffffffff</span></span></td>
<td><span data-ttu-id="bfc75-210">Der Algorithmus ist nur in CNG implementiert.</span><span class="sxs-lookup"><span data-stu-id="bfc75-210">The algorithm is only implemented in CNG.</span></span> <span data-ttu-id="bfc75-211">Das-Makro, IS_SPECIAL_OID_INFO_ALGID, kann verwendet werden, um zu bestimmen, ob ein Kryptografiealgorithmus nur mithilfe der CNG-Funktionen unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="bfc75-211">The macro, IS_SPECIAL_OID_INFO_ALGID, can be used to determine whether a cryptography algorithm is only supported by using the CNG functions.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bfc75-212">CALG_OID_INFO_PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bfc75-212">CALG_OID_INFO_PARAMETERS</span></span></td>
<td><span data-ttu-id="bfc75-213">0xfffffffe</span><span class="sxs-lookup"><span data-stu-id="bfc75-213">0xfffffffe</span></span></td>
<td><span data-ttu-id="bfc75-214">Der Algorithmus wird in den codierten Parametern definiert.</span><span class="sxs-lookup"><span data-stu-id="bfc75-214">The algorithm is defined in the encoded parameters.</span></span> <span data-ttu-id="bfc75-215">Der Algorithmus wird nur durch die Verwendung von CNG unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bfc75-215">The algorithm is only supported by using CNG.</span></span> <span data-ttu-id="bfc75-216">Das-Makro, IS_SPECIAL_OID_INFO_ALGID, kann verwendet werden, um zu bestimmen, ob ein Kryptografiealgorithmus nur mithilfe der CNG-Funktionen unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="bfc75-216">The macro, IS_SPECIAL_OID_INFO_ALGID, can be used to determine whether a cryptography algorithm is only supported by using the CNG functions.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bfc75-217">CALG_PCT1_MASTER</span><span class="sxs-lookup"><span data-stu-id="bfc75-217">CALG_PCT1_MASTER</span></span></td>
<td><span data-ttu-id="bfc75-218">0x00004c04</span><span class="sxs-lookup"><span data-stu-id="bfc75-218">0x00004c04</span></span></td>
<td><span data-ttu-id="bfc75-219">Wird vom Schannel.dll-Betriebssystem verwendet.</span><span class="sxs-lookup"><span data-stu-id="bfc75-219">Used by the Schannel.dll operations system.</span></span> <span data-ttu-id="bfc75-220">Diese <strong>ALG_ID</strong> sollte von Anwendungen nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bfc75-220">This <strong>ALG_ID</strong> should not be used by applications.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bfc75-221">CALG_RC2</span><span class="sxs-lookup"><span data-stu-id="bfc75-221">CALG_RC2</span></span></td>
<td><span data-ttu-id="bfc75-222">0x00006602</span><span class="sxs-lookup"><span data-stu-id="bfc75-222">0x00006602</span></span></td>
<td><span data-ttu-id="bfc75-223">RC2-Block Verschlüsselungsalgorithmus.</span><span class="sxs-lookup"><span data-stu-id="bfc75-223">RC2 block encryption algorithm.</span></span> <span data-ttu-id="bfc75-224">Dieser Algorithmus wird vom Microsoft- <a href="microsoft-base-cryptographic-provider.md">Basis-Kryptografieanbieter</a>unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bfc75-224">This algorithm is supported by the <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bfc75-225">CALG_RC4</span><span class="sxs-lookup"><span data-stu-id="bfc75-225">CALG_RC4</span></span></td>
<td><span data-ttu-id="bfc75-226">0x00006801</span><span class="sxs-lookup"><span data-stu-id="bfc75-226">0x00006801</span></span></td>
<td><span data-ttu-id="bfc75-227">RC4-Stream-Verschlüsselungsalgorithmus.</span><span class="sxs-lookup"><span data-stu-id="bfc75-227">RC4 stream encryption algorithm.</span></span> <span data-ttu-id="bfc75-228">Dieser Algorithmus wird vom Microsoft- <a href="microsoft-base-cryptographic-provider.md">Basis-Kryptografieanbieter</a>unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bfc75-228">This algorithm is supported by the <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bfc75-229">CALG_RC5</span><span class="sxs-lookup"><span data-stu-id="bfc75-229">CALG_RC5</span></span></td>
<td><span data-ttu-id="bfc75-230">0x0000660d</span><span class="sxs-lookup"><span data-stu-id="bfc75-230">0x0000660d</span></span></td>
<td><span data-ttu-id="bfc75-231">RC5 Block Verschlüsselungsalgorithmus.</span><span class="sxs-lookup"><span data-stu-id="bfc75-231">RC5 block encryption algorithm.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bfc75-232">CALG_RSA_KEYX</span><span class="sxs-lookup"><span data-stu-id="bfc75-232">CALG_RSA_KEYX</span></span></td>
<td><span data-ttu-id="bfc75-233">0x0000a400</span><span class="sxs-lookup"><span data-stu-id="bfc75-233">0x0000a400</span></span></td>
<td><span data-ttu-id="bfc75-234">RSA-Algorithmus für den öffentlichen Schlüsselaustausch.</span><span class="sxs-lookup"><span data-stu-id="bfc75-234">RSA public key exchange algorithm.</span></span> <span data-ttu-id="bfc75-235">Dieser Algorithmus wird vom Microsoft- <a href="microsoft-base-cryptographic-provider.md">Basis-Kryptografieanbieter</a>unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bfc75-235">This algorithm is supported by the <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bfc75-236">CALG_RSA_SIGN</span><span class="sxs-lookup"><span data-stu-id="bfc75-236">CALG_RSA_SIGN</span></span></td>
<td><span data-ttu-id="bfc75-237">0x00002400</span><span class="sxs-lookup"><span data-stu-id="bfc75-237">0x00002400</span></span></td>
<td><span data-ttu-id="bfc75-238">RSA-Algorithmus für die öffentliche Schlüssel Signatur.</span><span class="sxs-lookup"><span data-stu-id="bfc75-238">RSA public key signature algorithm.</span></span> <span data-ttu-id="bfc75-239">Dieser Algorithmus wird vom Microsoft- <a href="microsoft-base-cryptographic-provider.md">Basis-Kryptografieanbieter</a>unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bfc75-239">This algorithm is supported by the <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bfc75-240">CALG_SCHANNEL_ENC_KEY</span><span class="sxs-lookup"><span data-stu-id="bfc75-240">CALG_SCHANNEL_ENC_KEY</span></span></td>
<td><span data-ttu-id="bfc75-241">0x00004c07</span><span class="sxs-lookup"><span data-stu-id="bfc75-241">0x00004c07</span></span></td>
<td><span data-ttu-id="bfc75-242">Wird vom Schannel.dll-Betriebssystem verwendet.</span><span class="sxs-lookup"><span data-stu-id="bfc75-242">Used by the Schannel.dll operations system.</span></span> <span data-ttu-id="bfc75-243">Diese <strong>ALG_ID</strong> sollte von Anwendungen nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bfc75-243">This <strong>ALG_ID</strong> should not be used by applications.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bfc75-244">CALG_SCHANNEL_MAC_KEY</span><span class="sxs-lookup"><span data-stu-id="bfc75-244">CALG_SCHANNEL_MAC_KEY</span></span></td>
<td><span data-ttu-id="bfc75-245">0x00004c03</span><span class="sxs-lookup"><span data-stu-id="bfc75-245">0x00004c03</span></span></td>
<td><span data-ttu-id="bfc75-246">Wird vom Schannel.dll-Betriebssystem verwendet.</span><span class="sxs-lookup"><span data-stu-id="bfc75-246">Used by the Schannel.dll operations system.</span></span> <span data-ttu-id="bfc75-247">Diese <strong>ALG_ID</strong> sollte von Anwendungen nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bfc75-247">This <strong>ALG_ID</strong> should not be used by applications.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bfc75-248">CALG_SCHANNEL_MASTER_HASH</span><span class="sxs-lookup"><span data-stu-id="bfc75-248">CALG_SCHANNEL_MASTER_HASH</span></span></td>
<td><span data-ttu-id="bfc75-249">0x00004c02</span><span class="sxs-lookup"><span data-stu-id="bfc75-249">0x00004c02</span></span></td>
<td><span data-ttu-id="bfc75-250">Wird vom Schannel.dll-Betriebssystem verwendet.</span><span class="sxs-lookup"><span data-stu-id="bfc75-250">Used by the Schannel.dll operations system.</span></span> <span data-ttu-id="bfc75-251">Diese <strong>ALG_ID</strong> sollte von Anwendungen nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bfc75-251">This <strong>ALG_ID</strong> should not be used by applications.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bfc75-252">CALG_SEAL</span><span class="sxs-lookup"><span data-stu-id="bfc75-252">CALG_SEAL</span></span></td>
<td><span data-ttu-id="bfc75-253">0x00006802</span><span class="sxs-lookup"><span data-stu-id="bfc75-253">0x00006802</span></span></td>
<td><span data-ttu-id="bfc75-254">Versiegelt den Verschlüsselungsalgorithmus.</span><span class="sxs-lookup"><span data-stu-id="bfc75-254">SEAL encryption algorithm.</span></span> <span data-ttu-id="bfc75-255">Dieser Algorithmus wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bfc75-255">This algorithm is not supported.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bfc75-256">CALG_SHA</span><span class="sxs-lookup"><span data-stu-id="bfc75-256">CALG_SHA</span></span></td>
<td><span data-ttu-id="bfc75-257">0x00008004</span><span class="sxs-lookup"><span data-stu-id="bfc75-257">0x00008004</span></span></td>
<td><span data-ttu-id="bfc75-258">SHA-Hashalgorithmus</span><span class="sxs-lookup"><span data-stu-id="bfc75-258">SHA hashing algorithm.</span></span> <span data-ttu-id="bfc75-259">Dieser Algorithmus wird vom Microsoft- <a href="microsoft-base-cryptographic-provider.md">Basis-Kryptografieanbieter</a>unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bfc75-259">This algorithm is supported by the <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bfc75-260">CALG_SHA1</span><span class="sxs-lookup"><span data-stu-id="bfc75-260">CALG_SHA1</span></span></td>
<td><span data-ttu-id="bfc75-261">0x00008004</span><span class="sxs-lookup"><span data-stu-id="bfc75-261">0x00008004</span></span></td>
<td><span data-ttu-id="bfc75-262">Identisch mit <strong>CALG_SHA</strong>.</span><span class="sxs-lookup"><span data-stu-id="bfc75-262">Same as <strong>CALG_SHA</strong>.</span></span> <span data-ttu-id="bfc75-263">Dieser Algorithmus wird vom Microsoft- <a href="microsoft-base-cryptographic-provider.md">Basis-Kryptografieanbieter</a>unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bfc75-263">This algorithm is supported by the <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bfc75-264">CALG_SHA_256</span><span class="sxs-lookup"><span data-stu-id="bfc75-264">CALG_SHA_256</span></span></td>
<td><span data-ttu-id="bfc75-265">0x0000800c</span><span class="sxs-lookup"><span data-stu-id="bfc75-265">0x0000800c</span></span></td>
<td><span data-ttu-id="bfc75-266">256-Bit-SHA-Hash Algorithmus.</span><span class="sxs-lookup"><span data-stu-id="bfc75-266">256 bit SHA hashing algorithm.</span></span> <span data-ttu-id="bfc75-267">Dieser Algorithmus wird von Microsoft Enhanced RSA und AES Cryptographic Provider unterstützt. <strong>Windows XP mit SP3:</strong> Dieser Algorithmus wird von Microsoft Enhanced RSA und AES Cryptographic Provider (Prototype) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bfc75-267">This algorithm is supported by Microsoft Enhanced RSA and AES Cryptographic Provider..<strong>Windows XP with SP3:</strong> This algorithm is supported by the Microsoft Enhanced RSA and AES Cryptographic Provider (Prototype).</span></span><br/> <span data-ttu-id="bfc75-268"><strong>Windows XP mit SP2, Windows XP mit SP1 und Windows XP:</strong> Dieser Algorithmus wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bfc75-268"><strong>Windows XP with SP2, Windows XP with SP1 and Windows XP:</strong> This algorithm is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bfc75-269">CALG_SHA_384</span><span class="sxs-lookup"><span data-stu-id="bfc75-269">CALG_SHA_384</span></span></td>
<td><span data-ttu-id="bfc75-270">0x0000800d</span><span class="sxs-lookup"><span data-stu-id="bfc75-270">0x0000800d</span></span></td>
<td><span data-ttu-id="bfc75-271">384-Bit-SHA-Hash Algorithmus.</span><span class="sxs-lookup"><span data-stu-id="bfc75-271">384 bit SHA hashing algorithm.</span></span> <span data-ttu-id="bfc75-272">Dieser Algorithmus wird von Microsoft Enhanced RSA und AES Cryptographic Provider unterstützt. <strong>Windows XP mit SP3:</strong> Dieser Algorithmus wird von Microsoft Enhanced RSA und AES Cryptographic Provider (Prototype) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bfc75-272">This algorithm is supported by Microsoft Enhanced RSA and AES Cryptographic Provider.<strong>Windows XP with SP3:</strong> This algorithm is supported by the Microsoft Enhanced RSA and AES Cryptographic Provider (Prototype).</span></span><br/> <span data-ttu-id="bfc75-273"><strong>Windows XP mit SP2, Windows XP mit SP1 und Windows XP:</strong> Dieser Algorithmus wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bfc75-273"><strong>Windows XP with SP2, Windows XP with SP1 and Windows XP:</strong> This algorithm is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bfc75-274">CALG_SHA_512</span><span class="sxs-lookup"><span data-stu-id="bfc75-274">CALG_SHA_512</span></span></td>
<td><span data-ttu-id="bfc75-275">0x0000800e</span><span class="sxs-lookup"><span data-stu-id="bfc75-275">0x0000800e</span></span></td>
<td><span data-ttu-id="bfc75-276">512-Bit-SHA-Hash Algorithmus.</span><span class="sxs-lookup"><span data-stu-id="bfc75-276">512 bit SHA hashing algorithm.</span></span> <span data-ttu-id="bfc75-277">Dieser Algorithmus wird von Microsoft Enhanced RSA und AES Cryptographic Provider unterstützt. <strong>Windows XP mit SP3:</strong> Dieser Algorithmus wird von Microsoft Enhanced RSA und AES Cryptographic Provider (Prototype) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bfc75-277">This algorithm is supported by Microsoft Enhanced RSA and AES Cryptographic Provider.<strong>Windows XP with SP3:</strong> This algorithm is supported by the Microsoft Enhanced RSA and AES Cryptographic Provider (Prototype).</span></span><br/> <span data-ttu-id="bfc75-278"><strong>Windows XP mit SP2, Windows XP mit SP1 und Windows XP:</strong> Dieser Algorithmus wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bfc75-278"><strong>Windows XP with SP2, Windows XP with SP1 and Windows XP:</strong> This algorithm is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bfc75-279">CALG_SKIPJACK</span><span class="sxs-lookup"><span data-stu-id="bfc75-279">CALG_SKIPJACK</span></span></td>
<td><span data-ttu-id="bfc75-280">0x0000660a</span><span class="sxs-lookup"><span data-stu-id="bfc75-280">0x0000660a</span></span></td>
<td><span data-ttu-id="bfc75-281">Skipjack-Block Verschlüsselungsalgorithmus (Fortezza).</span><span class="sxs-lookup"><span data-stu-id="bfc75-281">Skipjack block encryption algorithm (FORTEZZA).</span></span> <span data-ttu-id="bfc75-282">Dieser Algorithmus wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bfc75-282">This algorithm is not supported.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bfc75-283">CALG_SSL2_MASTER</span><span class="sxs-lookup"><span data-stu-id="bfc75-283">CALG_SSL2_MASTER</span></span></td>
<td><span data-ttu-id="bfc75-284">0x00004c05</span><span class="sxs-lookup"><span data-stu-id="bfc75-284">0x00004c05</span></span></td>
<td><span data-ttu-id="bfc75-285">Wird vom Schannel.dll-Betriebssystem verwendet.</span><span class="sxs-lookup"><span data-stu-id="bfc75-285">Used by the Schannel.dll operations system.</span></span> <span data-ttu-id="bfc75-286">Diese <strong>ALG_ID</strong> sollte von Anwendungen nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bfc75-286">This <strong>ALG_ID</strong> should not be used by applications.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bfc75-287">CALG_SSL3_MASTER</span><span class="sxs-lookup"><span data-stu-id="bfc75-287">CALG_SSL3_MASTER</span></span></td>
<td><span data-ttu-id="bfc75-288">0x00004c01</span><span class="sxs-lookup"><span data-stu-id="bfc75-288">0x00004c01</span></span></td>
<td><span data-ttu-id="bfc75-289">Wird vom Schannel.dll-Betriebssystem verwendet.</span><span class="sxs-lookup"><span data-stu-id="bfc75-289">Used by the Schannel.dll operations system.</span></span> <span data-ttu-id="bfc75-290">Diese <strong>ALG_ID</strong> sollte von Anwendungen nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bfc75-290">This <strong>ALG_ID</strong> should not be used by applications.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bfc75-291">CALG_SSL3_SHAMD5</span><span class="sxs-lookup"><span data-stu-id="bfc75-291">CALG_SSL3_SHAMD5</span></span></td>
<td><span data-ttu-id="bfc75-292">0x00008008</span><span class="sxs-lookup"><span data-stu-id="bfc75-292">0x00008008</span></span></td>
<td><span data-ttu-id="bfc75-293">Wird vom Schannel.dll-Betriebssystem verwendet.</span><span class="sxs-lookup"><span data-stu-id="bfc75-293">Used by the Schannel.dll operations system.</span></span> <span data-ttu-id="bfc75-294">Diese <strong>ALG_ID</strong> sollte von Anwendungen nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bfc75-294">This <strong>ALG_ID</strong> should not be used by applications.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bfc75-295">CALG_TEK</span><span class="sxs-lookup"><span data-stu-id="bfc75-295">CALG_TEK</span></span></td>
<td><span data-ttu-id="bfc75-296">0x0000660b</span><span class="sxs-lookup"><span data-stu-id="bfc75-296">0x0000660b</span></span></td>
<td><span data-ttu-id="bfc75-297">Tek (Fortezza).</span><span class="sxs-lookup"><span data-stu-id="bfc75-297">TEK (FORTEZZA).</span></span> <span data-ttu-id="bfc75-298">Dieser Algorithmus wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bfc75-298">This algorithm is not supported.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bfc75-299">CALG_TLS1_MASTER</span><span class="sxs-lookup"><span data-stu-id="bfc75-299">CALG_TLS1_MASTER</span></span></td>
<td><span data-ttu-id="bfc75-300">0x00004c06</span><span class="sxs-lookup"><span data-stu-id="bfc75-300">0x00004c06</span></span></td>
<td><span data-ttu-id="bfc75-301">Wird vom Schannel.dll-Betriebssystem verwendet.</span><span class="sxs-lookup"><span data-stu-id="bfc75-301">Used by the Schannel.dll operations system.</span></span> <span data-ttu-id="bfc75-302">Diese <strong>ALG_ID</strong> sollte von Anwendungen nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bfc75-302">This <strong>ALG_ID</strong> should not be used by applications.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bfc75-303">CALG_TLS1PRF</span><span class="sxs-lookup"><span data-stu-id="bfc75-303">CALG_TLS1PRF</span></span></td>
<td><span data-ttu-id="bfc75-304">0x0000800a</span><span class="sxs-lookup"><span data-stu-id="bfc75-304">0x0000800a</span></span></td>
<td><span data-ttu-id="bfc75-305">Wird vom Schannel.dll-Betriebssystem verwendet.</span><span class="sxs-lookup"><span data-stu-id="bfc75-305">Used by the Schannel.dll operations system.</span></span> <span data-ttu-id="bfc75-306">Diese <strong>ALG_ID</strong> sollte von Anwendungen nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bfc75-306">This <strong>ALG_ID</strong> should not be used by applications.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="bfc75-307">Für den [Kryptografieanbieter](microsoft-base-cryptographic-provider.md)Microsoft, den [starken Kryptografieanbieter](microsoft-strong-cryptographic-provider.md)von Microsoft und den [erweiterten Kryptografieanbieter von Microsoft](microsoft-enhanced-cryptographic-provider.md), werden die **ALG_IDs** für die Schlüssel Spezifikationen **AT_KEYEXCHANGE** und **AT_SIGNATURE** wie folgt verwendet:</span><span class="sxs-lookup"><span data-stu-id="bfc75-307">For the [Microsoft Base Cryptographic Provider](microsoft-base-cryptographic-provider.md), the [Microsoft Strong Cryptographic Provider](microsoft-strong-cryptographic-provider.md), and the [Microsoft Enhanced Cryptographic Provider](microsoft-enhanced-cryptographic-provider.md), the **ALG_IDs** used for the key specifications **AT_KEYEXCHANGE** and **AT_SIGNATURE** are as follows:</span></span>

-   <span data-ttu-id="bfc75-308">**CALG_RSA_KEYX** wird für **AT_KEYEXCHANGE** verwendet.</span><span class="sxs-lookup"><span data-stu-id="bfc75-308">**CALG_RSA_KEYX** is used for **AT_KEYEXCHANGE**.</span></span>
-   <span data-ttu-id="bfc75-309">**CALG_RSA_SIGN** wird für **AT_SIGNATURE** verwendet.</span><span class="sxs-lookup"><span data-stu-id="bfc75-309">**CALG_RSA_SIGN** is used for **AT_SIGNATURE**.</span></span>

<span data-ttu-id="bfc75-310">Für den [Microsoft Base DSS und den Diffie-Hellman Kryptografieanbieter](microsoft-base-dss-and-diffie-hellman-cryptographic-provider.md)lauten die **ALG_IDs** , die für die Schlüssel Spezifikationen **AT_KEYEXCHANGE** und **AT_SIGNATURE** verwendet werden, wie folgt:</span><span class="sxs-lookup"><span data-stu-id="bfc75-310">For the [Microsoft Base DSS and Diffie-Hellman Cryptographic Provider](microsoft-base-dss-and-diffie-hellman-cryptographic-provider.md), the **ALG_IDs** used for the key specifications **AT_KEYEXCHANGE** and **AT_SIGNATURE** are as follows:</span></span>

-   <span data-ttu-id="bfc75-311">**CALG_DH_SF** wird für **AT_KEYEXCHANGE** verwendet.</span><span class="sxs-lookup"><span data-stu-id="bfc75-311">**CALG_DH_SF** is used for **AT_KEYEXCHANGE**.</span></span>
-   <span data-ttu-id="bfc75-312">**CALG_DSS_SIGN** wird für **AT_SIGNATURE** verwendet.</span><span class="sxs-lookup"><span data-stu-id="bfc75-312">**CALG_DSS_SIGN** is used for **AT_SIGNATURE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="bfc75-313">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bfc75-313">Requirements</span></span>



| <span data-ttu-id="bfc75-314">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bfc75-314">Requirement</span></span> | <span data-ttu-id="bfc75-315">Wert</span><span class="sxs-lookup"><span data-stu-id="bfc75-315">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bfc75-316">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bfc75-316">Minimum supported client</span></span><br/> | <span data-ttu-id="bfc75-317">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bfc75-317">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="bfc75-318">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bfc75-318">Minimum supported server</span></span><br/> | <span data-ttu-id="bfc75-319">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bfc75-319">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bfc75-320">Header</span><span class="sxs-lookup"><span data-stu-id="bfc75-320">Header</span></span><br/>                   | <dl> <span data-ttu-id="bfc75-321"><dt>WinCrypt. h</dt></span><span class="sxs-lookup"><span data-stu-id="bfc75-321"><dt>Wincrypt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bfc75-322">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bfc75-322">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfc75-323">Kryptografiefunktionen</span><span class="sxs-lookup"><span data-stu-id="bfc75-323">Cryptography Functions</span></span>](cryptography-functions.md)
</dt> <dt>

[<span data-ttu-id="bfc75-324">**CRYPT_ALGORITHM_IDENTIFIER**</span><span class="sxs-lookup"><span data-stu-id="bfc75-324">**CRYPT_ALGORITHM_IDENTIFIER**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_algorithm_identifier)
</dt> <dt>

[<span data-ttu-id="bfc75-325">**Cryptfindoidinfo**</span><span class="sxs-lookup"><span data-stu-id="bfc75-325">**CryptFindOIDInfo**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfindoidinfo)
</dt> </dl>

 

 
