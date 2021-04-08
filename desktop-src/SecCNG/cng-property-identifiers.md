---
description: Wird mit den Funktionen "BCryptGetProperty" und "BCryptSetProperty" verwendet, um eine Eigenschaft zu identifizieren.
ms.assetid: ebcc8202-94b4-47ad-9918-e5bc843a258f
title: Kryptografieprimitive-Eigenschaften Bezeichner (bcrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71f4996a216fbc4fbf63216f99b5f630c4769e97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861971"
---
# <a name="cryptography-primitive-property-identifiers"></a><span data-ttu-id="1be0a-103">Kryptografieprimitive-Eigenschaften Bezeichner</span><span class="sxs-lookup"><span data-stu-id="1be0a-103">Cryptography Primitive Property Identifiers</span></span>

<span data-ttu-id="1be0a-104">Die folgenden Werte werden mit den Funktionen [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) und [**BCryptSetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetproperty) verwendet, um eine Eigenschaft zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="1be0a-104">The following values are used with the [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) and [**BCryptSetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetproperty) functions to identify a property.</span></span>

<dl> <dt>

<span data-ttu-id="1be0a-105"><span id="BCRYPT_ALGORITHM_NAME"></span><span id="bcrypt_algorithm_name"></span>**bcrypt \_ - \_ Algorithmusname**</span><span class="sxs-lookup"><span data-stu-id="1be0a-105"><span id="BCRYPT_ALGORITHM_NAME"></span><span id="bcrypt_algorithm_name"></span>**BCRYPT\_ALGORITHM\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1be0a-106">L "algorithmName"</span><span class="sxs-lookup"><span data-stu-id="1be0a-106">L"AlgorithmName"</span></span>
</dt> <dt>



<span data-ttu-id="1be0a-107">Eine NULL-terminierte Unicode-Zeichenfolge, die den Namen des Algorithmus enthält.</span><span class="sxs-lookup"><span data-stu-id="1be0a-107">A null-terminated Unicode string that contains the name of the algorithm.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1be0a-108"><span id="BCRYPT_AUTH_TAG_LENGTH"></span><span id="bcrypt_auth_tag_length"></span>**bcrypt \_ auth \_ - \_ Taglänge**</span><span class="sxs-lookup"><span data-stu-id="1be0a-108"><span id="BCRYPT_AUTH_TAG_LENGTH"></span><span id="bcrypt_auth_tag_length"></span>**BCRYPT\_AUTH\_TAG\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1be0a-109">L "authtaglength"</span><span class="sxs-lookup"><span data-stu-id="1be0a-109">L"AuthTagLength"</span></span>
</dt> <dt>



<span data-ttu-id="1be0a-110">Die vom Algorithmus unterstützten authentifizierungstag Längen.</span><span class="sxs-lookup"><span data-stu-id="1be0a-110">The authentication tag lengths that are supported by the algorithm.</span></span> <span data-ttu-id="1be0a-111">Diese Eigenschaft ist eine [**bcrypt \_ auth \_ - \_ taglängen \_**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_key_lengths_struct) Struktur Struktur.</span><span class="sxs-lookup"><span data-stu-id="1be0a-111">This property is a [**BCRYPT\_AUTH\_TAG\_LENGTHS\_STRUCT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_key_lengths_struct) structure.</span></span> <span data-ttu-id="1be0a-112">Diese Eigenschaft gilt nur für Algorithmen.</span><span class="sxs-lookup"><span data-stu-id="1be0a-112">This property only applies to algorithms.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1be0a-113"><span id="BCRYPT_BLOCK_LENGTH"></span><span id="bcrypt_block_length"></span>**bcrypt- \_ Block \_ Länge**</span><span class="sxs-lookup"><span data-stu-id="1be0a-113"><span id="BCRYPT_BLOCK_LENGTH"></span><span id="bcrypt_block_length"></span>**BCRYPT\_BLOCK\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1be0a-114">L "blocklength"</span><span class="sxs-lookup"><span data-stu-id="1be0a-114">L"BlockLength"</span></span>
</dt> <dt>



<span data-ttu-id="1be0a-115">Die Größe eines Chiffre Blocks für den Algorithmus in Byte.</span><span class="sxs-lookup"><span data-stu-id="1be0a-115">The size, in bytes, of a cipher block for the algorithm.</span></span> <span data-ttu-id="1be0a-116">Diese Eigenschaft gilt nur für Blockverschlüsselungsalgorithmen.</span><span class="sxs-lookup"><span data-stu-id="1be0a-116">This property only applies to block cipher algorithms.</span></span> <span data-ttu-id="1be0a-117">Bei diesem Datentyp handelt es sich um ein **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="1be0a-117">This data type is a **DWORD**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1be0a-118"><span id="BCRYPT_BLOCK_SIZE_LIST"></span><span id="bcrypt_block_size_list"></span>**bcrypt- \_ Block \_ Größen \_ Liste**</span><span class="sxs-lookup"><span data-stu-id="1be0a-118"><span id="BCRYPT_BLOCK_SIZE_LIST"></span><span id="bcrypt_block_size_list"></span>**BCRYPT\_BLOCK\_SIZE\_LIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1be0a-119">L "blocksizelist"</span><span class="sxs-lookup"><span data-stu-id="1be0a-119">L"BlockSizeList"</span></span>
</dt> <dt>



<span data-ttu-id="1be0a-120">Eine Liste der Block Längen, die von einem Verschlüsselungsalgorithmus unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="1be0a-120">A list of the block lengths supported by an encryption algorithm.</span></span> <span data-ttu-id="1be0a-121">Dieser Datentyp ist ein Array von **DWords**.</span><span class="sxs-lookup"><span data-stu-id="1be0a-121">This data type is an array of **DWORDs**.</span></span> <span data-ttu-id="1be0a-122">Die Anzahl der Elemente im Array kann bestimmt werden, indem die Anzahl der Bytes geteilt wird, die durch die Größe eines einzelnen **DWORD** abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="1be0a-122">The number of elements in the array can be determined by dividing the number of bytes retrieved by the size of a single **DWORD**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1be0a-123"><span id="BCRYPT_CHAINING_MODE"></span><span id="bcrypt_chaining_mode"></span>**bcrypt- \_ Verkettungs \_ Modus**</span><span class="sxs-lookup"><span data-stu-id="1be0a-123"><span id="BCRYPT_CHAINING_MODE"></span><span id="bcrypt_chaining_mode"></span>**BCRYPT\_CHAINING\_MODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1be0a-124">L "chainingmode"</span><span class="sxs-lookup"><span data-stu-id="1be0a-124">L"ChainingMode"</span></span>
</dt> <dt>



<span data-ttu-id="1be0a-125">Ein Zeiger auf eine NULL-terminierte Unicode-Zeichenfolge, die den Verkettungs Modus des Verschlüsselungsalgorithmus darstellt.</span><span class="sxs-lookup"><span data-stu-id="1be0a-125">A pointer to a null-terminated Unicode string that represents the chaining mode of the encryption algorithm.</span></span> <span data-ttu-id="1be0a-126">Diese Eigenschaft kann für ein algorithmushandle oder ein Schlüssel Handle auf einen der folgenden Werte festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="1be0a-126">This property can be set on an algorithm handle or a key handle to one of the following values.</span></span>



| <span data-ttu-id="1be0a-127">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="1be0a-127">Identifier</span></span>                   | <span data-ttu-id="1be0a-128">Wert</span><span class="sxs-lookup"><span data-stu-id="1be0a-128">Value</span></span>                         | <span data-ttu-id="1be0a-129">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1be0a-129">Description</span></span>                                                                                                                                                                    |
|------------------------------|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1be0a-130">**bcrypt- \_ Ketten \_ Modus ( \_ CBC)**</span><span class="sxs-lookup"><span data-stu-id="1be0a-130">**BCRYPT\_CHAIN\_MODE\_CBC**</span></span> | <span data-ttu-id="1be0a-131">L "chainingmudecbc"</span><span class="sxs-lookup"><span data-stu-id="1be0a-131">L"ChainingModeCBC"</span></span><br/> | <span data-ttu-id="1be0a-132">Legt den Verkettungs Modus des Algorithmus auf [*Chiffre Block Verkettung*](/windows/desktop/SecGloss/c-gly)fest.</span><span class="sxs-lookup"><span data-stu-id="1be0a-132">Sets the algorithm's chaining mode to [*cipher block chaining*](/windows/desktop/SecGloss/c-gly).</span></span><br/>            |
| <span data-ttu-id="1be0a-133">**bcrypt- \_ Ketten \_ Modus- \_ ccm**</span><span class="sxs-lookup"><span data-stu-id="1be0a-133">**BCRYPT\_CHAIN\_MODE\_CCM**</span></span> | <span data-ttu-id="1be0a-134">L "chainingmodeccm"</span><span class="sxs-lookup"><span data-stu-id="1be0a-134">L"ChainingModeCCM"</span></span><br/> | <span data-ttu-id="1be0a-135">Legt den Verkettungs Modus des Algorithmus auf Counter mit dem CBC-MAC-Modus (CCM) fest. **Windows Vista:** Dieser Wert wird ab Windows Vista mit SP1 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1be0a-135">Sets the algorithm's chaining mode to counter with CBC-MAC mode (CCM).**Windows Vista:** This value is supported beginning with Windows Vista with SP1.</span></span><br/> <br/> |
| <span data-ttu-id="1be0a-136">**bcrypt- \_ Ketten \_ Modus ( \_ CFB)**</span><span class="sxs-lookup"><span data-stu-id="1be0a-136">**BCRYPT\_CHAIN\_MODE\_CFB**</span></span> | <span data-ttu-id="1be0a-137">L "chainingmudecfb"</span><span class="sxs-lookup"><span data-stu-id="1be0a-137">L"ChainingModeCFB"</span></span><br/> | <span data-ttu-id="1be0a-138">Legt den Verkettungs Modus des Algorithmus auf [*Chiffre Feedback*](/windows/desktop/SecGloss/c-gly)fest.</span><span class="sxs-lookup"><span data-stu-id="1be0a-138">Sets the algorithm's chaining mode to [*cipher feedback*](/windows/desktop/SecGloss/c-gly).</span></span><br/>                              |
| <span data-ttu-id="1be0a-139">**bcrypt- \_ Ketten \_ Modus- \_ ECB**</span><span class="sxs-lookup"><span data-stu-id="1be0a-139">**BCRYPT\_CHAIN\_MODE\_ECB**</span></span> | <span data-ttu-id="1be0a-140">L "chainingmodeecb"</span><span class="sxs-lookup"><span data-stu-id="1be0a-140">L"ChainingModeECB"</span></span><br/> | <span data-ttu-id="1be0a-141">Legt den Verkettungs Modus des Algorithmus auf [*elektronisches Codebook*](/windows/desktop/SecGloss/e-gly)fest.</span><span class="sxs-lookup"><span data-stu-id="1be0a-141">Sets the algorithm's chaining mode to [*electronic codebook*](/windows/desktop/SecGloss/e-gly).</span></span><br/>                  |
| <span data-ttu-id="1be0a-142">**bcrypt- \_ Ketten \_ Modus- \_ GCM**</span><span class="sxs-lookup"><span data-stu-id="1be0a-142">**BCRYPT\_CHAIN\_MODE\_GCM**</span></span> | <span data-ttu-id="1be0a-143">L "chainingmodegcm"</span><span class="sxs-lookup"><span data-stu-id="1be0a-143">L"ChainingModeGCM"</span></span><br/> | <span data-ttu-id="1be0a-144">Legt den Verkettungs Modus des Algorithmus auf den Galois/Counter-Modus (GCM) fest. **Windows Vista:** Dieser Wert wird ab Windows Vista mit SP1 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1be0a-144">Sets the algorithm's chaining mode to Galois/counter mode (GCM).**Windows Vista:** This value is supported beginning with Windows Vista with SP1.</span></span><br/> <br/>       |
| <span data-ttu-id="1be0a-145">**bcrypt- \_ Ketten \_ Modus- \_ na**</span><span class="sxs-lookup"><span data-stu-id="1be0a-145">**BCRYPT\_CHAIN\_MODE\_NA**</span></span>  | <span data-ttu-id="1be0a-146">L "chainingmoden/A"</span><span class="sxs-lookup"><span data-stu-id="1be0a-146">L"ChainingModeN/A"</span></span><br/> | <span data-ttu-id="1be0a-147">Der Algorithmus unterstützt keine Verkettung.</span><span class="sxs-lookup"><span data-stu-id="1be0a-147">The algorithm does not support chaining.</span></span><br/>                                                                                                                            |



 


</dt> </dl> </dd> <dt>

<span data-ttu-id="1be0a-148"><span id="BCRYPT_DH_PARAMETERS"></span><span id="bcrypt_dh_parameters"></span>**bcrypt \_ dh- \_ Parameter**</span><span class="sxs-lookup"><span data-stu-id="1be0a-148"><span id="BCRYPT_DH_PARAMETERS"></span><span id="bcrypt_dh_parameters"></span>**BCRYPT\_DH\_PARAMETERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1be0a-149">L "dhparameters"</span><span class="sxs-lookup"><span data-stu-id="1be0a-149">L"DHParameters"</span></span>
</dt> <dt>



<span data-ttu-id="1be0a-150">Gibt Parameter an, die mit einem Diffie-Hellman Schlüssel verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1be0a-150">Specifies parameters to use with a Diffie-Hellman key.</span></span> <span data-ttu-id="1be0a-151">Dieser Datentyp ist ein Zeiger auf eine [**bcrypt \_ dh- \_ Parameter \_ Header**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_parameter_header) Struktur.</span><span class="sxs-lookup"><span data-stu-id="1be0a-151">This data type is a pointer to a [**BCRYPT\_DH\_PARAMETER\_HEADER**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_parameter_header) structure.</span></span> <span data-ttu-id="1be0a-152">Diese Eigenschaft kann nur festgelegt werden und muss für den Schlüssel festgelegt werden, bevor der Schlüssel abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="1be0a-152">This property can only be set and must be set for the key before the key is completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1be0a-153"><span id="BCRYPT_DSA_PARAMETERS"></span><span id="bcrypt_dsa_parameters"></span>**bcrypt- \_ DSA- \_ Parameter**</span><span class="sxs-lookup"><span data-stu-id="1be0a-153"><span id="BCRYPT_DSA_PARAMETERS"></span><span id="bcrypt_dsa_parameters"></span>**BCRYPT\_DSA\_PARAMETERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1be0a-154">L "DSAParameters"</span><span class="sxs-lookup"><span data-stu-id="1be0a-154">L"DSAParameters"</span></span>
</dt> <dt>



<span data-ttu-id="1be0a-155">Gibt Parameter an, die mit einem DSA-Schlüssel verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1be0a-155">Specifies parameters to use with a DSA key.</span></span> <span data-ttu-id="1be0a-156">Diese Eigenschaft ist ein [**bcrypt \_ DSA- \_ Parameter \_ Header**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header) oder eine [**bcrypt DSA- \_ \_ Parameter Header- \_ \_ v2**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header_v2) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="1be0a-156">This property is a [**BCRYPT\_DSA\_PARAMETER\_HEADER**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header) or a [**BCRYPT\_DSA\_PARAMETER\_HEADER\_V2**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header_v2) structure.</span></span> <span data-ttu-id="1be0a-157">Diese Eigenschaft kann nur festgelegt werden und muss für den Schlüssel festgelegt werden, bevor der Schlüssel abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="1be0a-157">This property can only be set and must be set for the key before the key is completed.</span></span>

<span data-ttu-id="1be0a-158">**Windows 8:** Ab Windows 8 kann diese Eigenschaft eine [**bcrypt \_ DSA- \_ Parameter Header- \_ \_ v2**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header_v2) -Struktur sein.</span><span class="sxs-lookup"><span data-stu-id="1be0a-158">**Windows 8:** Beginning with Windows 8, this property can be a [**BCRYPT\_DSA\_PARAMETER\_HEADER\_V2**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header_v2) structure.</span></span> <span data-ttu-id="1be0a-159">Verwenden Sie diese Struktur, wenn die Schlüsselgröße 1024 Bits überschreitet und kleiner oder gleich 3072 Bits ist.</span><span class="sxs-lookup"><span data-stu-id="1be0a-159">Use this structure if the key size exceeds 1024 bits and is less than or equal to 3072 bits.</span></span> <span data-ttu-id="1be0a-160">Wenn die Schlüsselgröße größer oder gleich 512, aber kleiner oder gleich 1024 Bits ist, verwenden Sie die Struktur des [**bcrypt \_ DSA- \_ Parameter \_ Headers**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header) .</span><span class="sxs-lookup"><span data-stu-id="1be0a-160">If the key size is greater than or equal to 512 but less than or equal to 1024 bits, use the [**BCRYPT\_DSA\_PARAMETER\_HEADER**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header) structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1be0a-161"><span id="BCRYPT_EFFECTIVE_KEY_LENGTH"></span><span id="bcrypt_effective_key_length"></span>**effektive bcrypt- \_ \_ Schlüssel \_ Länge**</span><span class="sxs-lookup"><span data-stu-id="1be0a-161"><span id="BCRYPT_EFFECTIVE_KEY_LENGTH"></span><span id="bcrypt_effective_key_length"></span>**BCRYPT\_EFFECTIVE\_KEY\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1be0a-162">L "effectivekeylength"</span><span class="sxs-lookup"><span data-stu-id="1be0a-162">L"EffectiveKeyLength"</span></span>
</dt> <dt>



<span data-ttu-id="1be0a-163">Die Größe der effektiven Länge eines RC2-Schlüssels in Bits.</span><span class="sxs-lookup"><span data-stu-id="1be0a-163">The size, in bits, of the effective length of an RC2 key.</span></span> <span data-ttu-id="1be0a-164">Bei diesem Datentyp handelt es sich um ein **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="1be0a-164">This data type is a **DWORD**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1be0a-165"><span id="BCRYPT_HASH_BLOCK_LENGTH"></span><span id="bcrypt_hash_block_length"></span>**bcrypt- \_ Hash \_ Block \_ Länge**</span><span class="sxs-lookup"><span data-stu-id="1be0a-165"><span id="BCRYPT_HASH_BLOCK_LENGTH"></span><span id="bcrypt_hash_block_length"></span>**BCRYPT\_HASH\_BLOCK\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1be0a-166">L "hashblock length"</span><span class="sxs-lookup"><span data-stu-id="1be0a-166">L"HashBlockLength"</span></span>
</dt> <dt>



<span data-ttu-id="1be0a-167">Die Größe (in Bytes) des Blocks für einen Hash.</span><span class="sxs-lookup"><span data-stu-id="1be0a-167">The size, in bytes, of the block for a hash.</span></span> <span data-ttu-id="1be0a-168">Diese Eigenschaft gilt nur für Hash Algorithmen.</span><span class="sxs-lookup"><span data-stu-id="1be0a-168">This property only applies to hash algorithms.</span></span> <span data-ttu-id="1be0a-169">Bei diesem Datentyp handelt es sich um ein **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="1be0a-169">This data type is a **DWORD**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1be0a-170"><span id="BCRYPT_HASH_LENGTH"></span><span id="bcrypt_hash_length"></span>**bcrypt \_ - \_ Hashlänge**</span><span class="sxs-lookup"><span data-stu-id="1be0a-170"><span id="BCRYPT_HASH_LENGTH"></span><span id="bcrypt_hash_length"></span>**BCRYPT\_HASH\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1be0a-171">L "hashdigestlength"</span><span class="sxs-lookup"><span data-stu-id="1be0a-171">L"HashDigestLength"</span></span>
</dt> <dt>



<span data-ttu-id="1be0a-172">Die Größe (in Bytes) des Hashwerts eines Hash Anbieters.</span><span class="sxs-lookup"><span data-stu-id="1be0a-172">The size, in bytes, of the hash value of a hash provider.</span></span> <span data-ttu-id="1be0a-173">Bei diesem Datentyp handelt es sich um ein **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="1be0a-173">This data type is a **DWORD**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1be0a-174"><span id="BCRYPT_HASH_OID_LIST"></span><span id="bcrypt_hash_oid_list"></span>**bcrypt- \_ Hash- \_ OID- \_ Liste**</span><span class="sxs-lookup"><span data-stu-id="1be0a-174"><span id="BCRYPT_HASH_OID_LIST"></span><span id="bcrypt_hash_oid_list"></span>**BCRYPT\_HASH\_OID\_LIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1be0a-175">L "hashuidlist"</span><span class="sxs-lookup"><span data-stu-id="1be0a-175">L"HashOIDList"</span></span>
</dt> <dt>



<span data-ttu-id="1be0a-176">Die Liste der von [*der*](/windows/desktop/SecGloss/d-gly)-codierten Hash [*Objekt*](/windows/desktop/SecGloss/o-gly) -IDs (OIDs).</span><span class="sxs-lookup"><span data-stu-id="1be0a-176">The list of [*DER*](/windows/desktop/SecGloss/d-gly)-encoded hashing [*object identifiers*](/windows/desktop/SecGloss/o-gly) (OIDs).</span></span> <span data-ttu-id="1be0a-177">Diese Eigenschaft ist eine [**bcrypt- \_ OID- \_ Listen**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_oid_list) Struktur.</span><span class="sxs-lookup"><span data-stu-id="1be0a-177">This property is a [**BCRYPT\_OID\_LIST**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_oid_list) structure.</span></span> <span data-ttu-id="1be0a-178">Diese Eigenschaft kann nur gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="1be0a-178">This property can only be read.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1be0a-179"><span id="BCRYPT_INITIALIZATION_VECTOR"></span><span id="bcrypt_initialization_vector"></span>**bcrypt- \_ Initialisierungs \_ Vektor**</span><span class="sxs-lookup"><span data-stu-id="1be0a-179"><span id="BCRYPT_INITIALIZATION_VECTOR"></span><span id="bcrypt_initialization_vector"></span>**BCRYPT\_INITIALIZATION\_VECTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1be0a-180">L "IV"</span><span class="sxs-lookup"><span data-stu-id="1be0a-180">L"IV"</span></span>
</dt> <dt>



<span data-ttu-id="1be0a-181">Enthält den [*Initialisierungs Vektor*](/windows/desktop/SecGloss/i-gly) (IV) für einen Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="1be0a-181">Contains the [*initialization vector*](/windows/desktop/SecGloss/i-gly) (IV) for a key.</span></span> <span data-ttu-id="1be0a-182">Diese Eigenschaft gilt nur für Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="1be0a-182">This property only applies to keys.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1be0a-183"><span id="BCRYPT_KEY_LENGTH"></span><span id="bcrypt_key_length"></span>**bcrypt- \_ Schlüssel \_ Länge**</span><span class="sxs-lookup"><span data-stu-id="1be0a-183"><span id="BCRYPT_KEY_LENGTH"></span><span id="bcrypt_key_length"></span>**BCRYPT\_KEY\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1be0a-184">L "keylength"</span><span class="sxs-lookup"><span data-stu-id="1be0a-184">L"KeyLength"</span></span>
</dt> <dt>



<span data-ttu-id="1be0a-185">Die Größe des Schlüssel Werts eines symmetrischen Schlüssel Anbieters in Bits.</span><span class="sxs-lookup"><span data-stu-id="1be0a-185">The size, in bits, of the key value of a symmetric key provider.</span></span> <span data-ttu-id="1be0a-186">Bei diesem Datentyp handelt es sich um ein **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="1be0a-186">This data type is a **DWORD**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1be0a-187"><span id="BCRYPT_KEY_LENGTHS"></span><span id="bcrypt_key_lengths"></span>**bcrypt- \_ Schlüssel \_ Längen**</span><span class="sxs-lookup"><span data-stu-id="1be0a-187"><span id="BCRYPT_KEY_LENGTHS"></span><span id="bcrypt_key_lengths"></span>**BCRYPT\_KEY\_LENGTHS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1be0a-188">L "keylängen"</span><span class="sxs-lookup"><span data-stu-id="1be0a-188">L"KeyLengths"</span></span>
</dt> <dt>



<span data-ttu-id="1be0a-189">Die vom Algorithmus unterstützten Schlüssellängen.</span><span class="sxs-lookup"><span data-stu-id="1be0a-189">The key lengths that are supported by the algorithm.</span></span> <span data-ttu-id="1be0a-190">Diese Eigenschaft ist eine Struktur der [**bcrypt- \_ Schlüssel \_ Längen \_**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_key_lengths_struct) Struktur.</span><span class="sxs-lookup"><span data-stu-id="1be0a-190">This property is a [**BCRYPT\_KEY\_LENGTHS\_STRUCT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_key_lengths_struct) structure.</span></span> <span data-ttu-id="1be0a-191">Diese Eigenschaft gilt nur für Algorithmen.</span><span class="sxs-lookup"><span data-stu-id="1be0a-191">This property only applies to algorithms.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1be0a-192"><span id="BCRYPT_KEY_OBJECT_LENGTH"></span><span id="bcrypt_key_object_length"></span>**bcrypt- \_ Schlüssel \_ Objekt \_ Länge**</span><span class="sxs-lookup"><span data-stu-id="1be0a-192"><span id="BCRYPT_KEY_OBJECT_LENGTH"></span><span id="bcrypt_key_object_length"></span>**BCRYPT\_KEY\_OBJECT\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1be0a-193">L "keyobjectlength"</span><span class="sxs-lookup"><span data-stu-id="1be0a-193">L"KeyObjectLength"</span></span>
</dt> <dt>



<span data-ttu-id="1be0a-194">Diese Eigenschaft wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="1be0a-194">This property is not used.</span></span> <span data-ttu-id="1be0a-195">Die Eigenschaft **bcrypt- \_ Objekt \_ Länge** wird verwendet, um diese Informationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="1be0a-195">The **BCRYPT\_OBJECT\_LENGTH** property is used to obtain this information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1be0a-196"><span id="BCRYPT_KEY_STRENGTH"></span><span id="bcrypt_key_strength"></span>**bcrypt- \_ Schlüssel \_ Stärke**</span><span class="sxs-lookup"><span data-stu-id="1be0a-196"><span id="BCRYPT_KEY_STRENGTH"></span><span id="bcrypt_key_strength"></span>**BCRYPT\_KEY\_STRENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1be0a-197">L "keystärke"</span><span class="sxs-lookup"><span data-stu-id="1be0a-197">L"KeyStrength"</span></span>
</dt> <dt>



<span data-ttu-id="1be0a-198">Die Anzahl der Bits im Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="1be0a-198">The number of bits in the key.</span></span> <span data-ttu-id="1be0a-199">Bei diesem Datentyp handelt es sich um ein **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="1be0a-199">This data type is a **DWORD**.</span></span> <span data-ttu-id="1be0a-200">Diese Eigenschaft gilt nur für Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="1be0a-200">This property only applies to keys.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1be0a-201"><span id="BCRYPT_MESSAGE_BLOCK_LENGTH"></span><span id="bcrypt_message_block_length"></span>**bcrypt- \_ Nachrichten \_ Block \_ Länge**</span><span class="sxs-lookup"><span data-stu-id="1be0a-201"><span id="BCRYPT_MESSAGE_BLOCK_LENGTH"></span><span id="bcrypt_message_block_length"></span>**BCRYPT\_MESSAGE\_BLOCK\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1be0a-202">L "messageblocklength"</span><span class="sxs-lookup"><span data-stu-id="1be0a-202">L"MessageBlockLength"</span></span>
</dt> <dt>



<span data-ttu-id="1be0a-203">Dies kann für jedes Schlüssel handle festgelegt werden, für das der CFB-Verkettungs Modus festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="1be0a-203">This can be set on any key handle that has the CFB chaining mode set.</span></span> <span data-ttu-id="1be0a-204">Standardmäßig ist diese Eigenschaft für 8-Bit-CFB auf 1 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1be0a-204">By default, this property is set to 1 for 8-bit CFB.</span></span> <span data-ttu-id="1be0a-205">Das Festlegen auf die Blockgröße in Bytes bewirkt, dass der CFB-vollblock verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1be0a-205">Setting it to the block size in bytes causes full-block CFB to be used.</span></span> <span data-ttu-id="1be0a-206">Bei XTS-Schlüsseln wird diese verwendet, um die Größe der XTS-Dateneinheit (in der Regel 512 oder 4096) in Byte festzulegen.</span><span class="sxs-lookup"><span data-stu-id="1be0a-206">For XTS keys it is used to set the size, in bytes, of the XTS Data Unit (commonly 512 or 4096).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1be0a-207"><span id="BCRYPT_MULTI_OBJECT_LENGTH"></span><span id="bcrypt_multi_object_length"></span>**bcrypt \_ - \_ multiobjektlänge \_**</span><span class="sxs-lookup"><span data-stu-id="1be0a-207"><span id="BCRYPT_MULTI_OBJECT_LENGTH"></span><span id="bcrypt_multi_object_length"></span>**BCRYPT\_MULTI\_OBJECT\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1be0a-208">L "multiobjectlength"</span><span class="sxs-lookup"><span data-stu-id="1be0a-208">L"MultiObjectLength"</span></span>
</dt> <dt>



<span data-ttu-id="1be0a-209">Diese Eigenschaft gibt eine [**bcrypt- \_ Struktur mit mehreren \_ Objekt \_ Längen \_**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_multi_object_length_struct)zurück, die erforderliche Informationen zum Berechnen der Größe eines Objekt Puffers enthält.</span><span class="sxs-lookup"><span data-stu-id="1be0a-209">This property returns a [**BCRYPT\_MULTI\_OBJECT\_LENGTH\_STRUCT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_multi_object_length_struct), which contains information necessary to calculate the size of an object buffer.</span></span> <span data-ttu-id="1be0a-210">Diese Eigenschaft wird nur für Betriebssystemversionen unterstützt, die die Funktion " [**bcryptkreatemultihash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatemultihash) " unterstützen.</span><span class="sxs-lookup"><span data-stu-id="1be0a-210">This property is only supported on operating system versions that support the [**BCryptCreateMultiHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatemultihash) function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1be0a-211"><span id="BCRYPT_OBJECT_LENGTH"></span><span id="bcrypt_object_length"></span>**bcrypt- \_ Objekt \_ Länge**</span><span class="sxs-lookup"><span data-stu-id="1be0a-211"><span id="BCRYPT_OBJECT_LENGTH"></span><span id="bcrypt_object_length"></span>**BCRYPT\_OBJECT\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1be0a-212">L "objectlength"</span><span class="sxs-lookup"><span data-stu-id="1be0a-212">L"ObjectLength"</span></span>
</dt> <dt>



<span data-ttu-id="1be0a-213">Die Größe (in Bytes) des untergeordneten Objekts eines Anbieters.</span><span class="sxs-lookup"><span data-stu-id="1be0a-213">The size, in bytes, of the subobject of a provider.</span></span> <span data-ttu-id="1be0a-214">Bei diesem Datentyp handelt es sich um ein **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="1be0a-214">This data type is a **DWORD**.</span></span> <span data-ttu-id="1be0a-215">Derzeit verwenden die Anbieter von Hash-und symmetrischen Chiffre Algorithmen zum Speichern Ihrer unter Objekte die vom Aufrufer zugewiesenen Puffer.</span><span class="sxs-lookup"><span data-stu-id="1be0a-215">Currently, the hash and symmetric cipher algorithm providers use caller-allocated buffers to store their subobjects.</span></span> <span data-ttu-id="1be0a-216">Beispielsweise erfordert der Hash Anbieter, dass Sie Speicher für das Hash Objekt belegen, das mit der Funktion " [**bcryptkreatehash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) " abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="1be0a-216">For example, the hash provider requires you to allocate memory for the hash object obtained with the [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) function.</span></span> <span data-ttu-id="1be0a-217">Diese Eigenschaft stellt die Puffergröße für das-Objekt eines Anbieters bereit, sodass Sie Speicher für das vom Anbieter erstellte Objekt zuweisen können.</span><span class="sxs-lookup"><span data-stu-id="1be0a-217">This property provides the buffer size for a provider's object so you can allocate memory for the object created by the provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1be0a-218"><span id="BCRYPT_PADDING_SCHEMES"></span><span id="bcrypt_padding_schemes"></span>**bcrypt- \_ \_ Paddingschemas**</span><span class="sxs-lookup"><span data-stu-id="1be0a-218"><span id="BCRYPT_PADDING_SCHEMES"></span><span id="bcrypt_padding_schemes"></span>**BCRYPT\_PADDING\_SCHEMES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1be0a-219">L "Paddingschemas"</span><span class="sxs-lookup"><span data-stu-id="1be0a-219">L"PaddingSchemes"</span></span>
</dt> <dt>



<span data-ttu-id="1be0a-220">Stellt das Auffüll Schema des RSA-Algorithmus-Anbieters dar.</span><span class="sxs-lookup"><span data-stu-id="1be0a-220">Represents the padding scheme of the RSA algorithm provider.</span></span> <span data-ttu-id="1be0a-221">Bei diesem Datentyp handelt es sich um ein **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="1be0a-221">This data type is a **DWORD**.</span></span> <span data-ttu-id="1be0a-222">Dies kann einer der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="1be0a-222">This can be one of the following values.</span></span>



| <span data-ttu-id="1be0a-223">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="1be0a-223">Identifier</span></span>                             | <span data-ttu-id="1be0a-224">Wert</span><span class="sxs-lookup"><span data-stu-id="1be0a-224">Value</span></span>      | <span data-ttu-id="1be0a-225">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1be0a-225">Description</span></span>                                                |
|----------------------------------------|------------|------------------------------------------------------------|
| <span data-ttu-id="1be0a-226">**bcrypt- \_ unterstützter Auffüll \_ \_ Router**</span><span class="sxs-lookup"><span data-stu-id="1be0a-226">**BCRYPT\_SUPPORTED\_PAD\_ROUTER**</span></span>     | <span data-ttu-id="1be0a-227">0x00000001</span><span class="sxs-lookup"><span data-stu-id="1be0a-227">0x00000001</span></span> | <span data-ttu-id="1be0a-228">Der Anbieter unterstützt die durch den Router hinzugefügten Auffüll Zeichen.</span><span class="sxs-lookup"><span data-stu-id="1be0a-228">The provider supports padding added by the router.</span></span>         |
| <span data-ttu-id="1be0a-229">**Unterstützte bcrypt- \_ \_ Pad \_ PKCS1 \_**</span><span class="sxs-lookup"><span data-stu-id="1be0a-229">**BCRYPT\_SUPPORTED\_PAD\_PKCS1\_ENC**</span></span> | <span data-ttu-id="1be0a-230">0x00000002</span><span class="sxs-lookup"><span data-stu-id="1be0a-230">0x00000002</span></span> | <span data-ttu-id="1be0a-231">Der Anbieter unterstützt das PKCS1 Encryption Auffüllung Schema.</span><span class="sxs-lookup"><span data-stu-id="1be0a-231">The provider supports the PKCS1 encryption padding scheme.</span></span> |
| <span data-ttu-id="1be0a-232">**Unterstützte bcrypt- \_ \_ Pad \_ PKCS1 \_ sig**</span><span class="sxs-lookup"><span data-stu-id="1be0a-232">**BCRYPT\_SUPPORTED\_PAD\_PKCS1\_SIG**</span></span> | <span data-ttu-id="1be0a-233">0x00000004</span><span class="sxs-lookup"><span data-stu-id="1be0a-233">0x00000004</span></span> | <span data-ttu-id="1be0a-234">Der Anbieter unterstützt das Auffüll Schema der PKCS1-Signatur.</span><span class="sxs-lookup"><span data-stu-id="1be0a-234">The provider supports the PKCS1 signature padding scheme.</span></span>  |
| <span data-ttu-id="1be0a-235">**bcrypt \_ unterstützte \_ Pad \_ OAEP**</span><span class="sxs-lookup"><span data-stu-id="1be0a-235">**BCRYPT\_SUPPORTED\_PAD\_OAEP**</span></span>       | <span data-ttu-id="1be0a-236">0x00000008</span><span class="sxs-lookup"><span data-stu-id="1be0a-236">0x00000008</span></span> | <span data-ttu-id="1be0a-237">Der Anbieter unterstützt das OAEP-Auffüll Schema.</span><span class="sxs-lookup"><span data-stu-id="1be0a-237">The provider supports the OAEP padding scheme.</span></span>             |
| <span data-ttu-id="1be0a-238">**bcrypt \_ unterstützte \_ Pad- \_ PSS**</span><span class="sxs-lookup"><span data-stu-id="1be0a-238">**BCRYPT\_SUPPORTED\_PAD\_PSS**</span></span>        | <span data-ttu-id="1be0a-239">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1be0a-239">0x00000010</span></span> | <span data-ttu-id="1be0a-240">Der Anbieter unterstützt das PSS-Auffüll Schema.</span><span class="sxs-lookup"><span data-stu-id="1be0a-240">The provider supports the PSS padding scheme.</span></span>              |



 


</dt> </dl> </dd> <dt>

<span data-ttu-id="1be0a-241"><span id="BCRYPT_PROVIDER_HANDLE"></span><span id="bcrypt_provider_handle"></span>**bcrypt- \_ Anbieter \_ handle**</span><span class="sxs-lookup"><span data-stu-id="1be0a-241"><span id="BCRYPT_PROVIDER_HANDLE"></span><span id="bcrypt_provider_handle"></span>**BCRYPT\_PROVIDER\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1be0a-242">L "ProviderHandle"</span><span class="sxs-lookup"><span data-stu-id="1be0a-242">L"ProviderHandle"</span></span>
</dt> <dt>



<span data-ttu-id="1be0a-243">Das Handle des CNG-Anbieters, von dem das Objekt erstellt wurde, das im *hobject* -Parameter übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="1be0a-243">The handle of the CNG provider that created the object passed in the *hObject* parameter.</span></span> <span data-ttu-id="1be0a-244">Dieser Datentyp ist ein **bcrypt- \_ ALG- \_ handle**.</span><span class="sxs-lookup"><span data-stu-id="1be0a-244">This data type is a **BCRYPT\_ALG\_HANDLE**.</span></span> <span data-ttu-id="1be0a-245">Diese Eigenschaft kann nur abgerufen werden. der Wert kann nicht festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="1be0a-245">This property can only be retrieved; it cannot be set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1be0a-246"><span id="BCRYPT_SIGNATURE_LENGTH"></span><span id="bcrypt_signature_length"></span>**bcrypt- \_ Signatur \_ Länge**</span><span class="sxs-lookup"><span data-stu-id="1be0a-246"><span id="BCRYPT_SIGNATURE_LENGTH"></span><span id="bcrypt_signature_length"></span>**BCRYPT\_SIGNATURE\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1be0a-247">L "SignatureLength"</span><span class="sxs-lookup"><span data-stu-id="1be0a-247">L"SignatureLength"</span></span>
</dt> <dt>



<span data-ttu-id="1be0a-248">Die Größe (in Bytes) der Länge einer Signatur für einen Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="1be0a-248">The size, in bytes, of the length of a signature for a key.</span></span> <span data-ttu-id="1be0a-249">Bei diesem Datentyp handelt es sich um ein **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="1be0a-249">This data type is a **DWORD**.</span></span> <span data-ttu-id="1be0a-250">Diese Eigenschaft gilt nur für Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="1be0a-250">This property only applies to keys.</span></span> <span data-ttu-id="1be0a-251">Diese Eigenschaft kann nur abgerufen werden. der Wert kann nicht festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="1be0a-251">This property can only be retrieved; it cannot be set.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1be0a-252">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1be0a-252">Requirements</span></span>



| <span data-ttu-id="1be0a-253">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1be0a-253">Requirement</span></span> | <span data-ttu-id="1be0a-254">Wert</span><span class="sxs-lookup"><span data-stu-id="1be0a-254">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1be0a-255">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1be0a-255">Minimum supported client</span></span><br/> | <span data-ttu-id="1be0a-256">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1be0a-256">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="1be0a-257">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1be0a-257">Minimum supported server</span></span><br/> | <span data-ttu-id="1be0a-258">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1be0a-258">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="1be0a-259">Header</span><span class="sxs-lookup"><span data-stu-id="1be0a-259">Header</span></span><br/>                   | <dl> <span data-ttu-id="1be0a-260"><dt>Bcrypt. h</dt></span><span class="sxs-lookup"><span data-stu-id="1be0a-260"><dt>Bcrypt.h</dt></span></span> </dl> |



 

