---
description: Wird verwendet, um eine Key Storage-Eigenschaft zu identifizieren.
ms.assetid: 407f0e42-07c8-4ec6-81c6-f8bde005adb0
title: Schlüsselspeicher-Eigenschaften Bezeichner (ncrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 813a15ba106989cb558eba181bc893d75c6d1bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369096"
---
# <a name="key-storage-property-identifiers"></a><span data-ttu-id="ed63a-103">Schlüsselspeicher-Eigenschaften Bezeichner</span><span class="sxs-lookup"><span data-stu-id="ed63a-103">Key Storage Property Identifiers</span></span>

<span data-ttu-id="ed63a-104">Die folgenden Werte werden verwendet, um eine Key Storage-Eigenschaft zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="ed63a-104">The following values are used to identify a key storage property.</span></span>

<dl> <dt>

<span data-ttu-id="ed63a-105"><span id="NCRYPT_ALGORITHM_GROUP_PROPERTY"></span><span id="ncrypt_algorithm_group_property"></span>**ncrypt \_ - \_ \_ algorithmusgruppeneigenschaft**</span><span class="sxs-lookup"><span data-stu-id="ed63a-105"><span id="NCRYPT_ALGORITHM_GROUP_PROPERTY"></span><span id="ncrypt_algorithm_group_property"></span>**NCRYPT\_ALGORITHM\_GROUP\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed63a-106">L "Algorithmusgruppe"</span><span class="sxs-lookup"><span data-stu-id="ed63a-106">L"Algorithm Group"</span></span>
</dt> <dt>



<span data-ttu-id="ed63a-107">Eine NULL-terminierte Unicode-Zeichenfolge, die den Namen der Algorithmusgruppe des Objekts enthält.</span><span class="sxs-lookup"><span data-stu-id="ed63a-107">A null-terminated Unicode string that contains the name of the object's algorithm group.</span></span> <span data-ttu-id="ed63a-108">Diese Eigenschaft gilt nur für Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="ed63a-108">This property only applies to keys.</span></span> <span data-ttu-id="ed63a-109">Die folgenden Bezeichner werden vom Microsoft-Schlüsselspeicher Anbieter zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ed63a-109">The following identifiers are returned by the Microsoft key storage provider.</span></span>



| <span data-ttu-id="ed63a-110">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="ed63a-110">Identifier</span></span>                                     | <span data-ttu-id="ed63a-111">Wert</span><span class="sxs-lookup"><span data-stu-id="ed63a-111">Value</span></span>              | <span data-ttu-id="ed63a-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ed63a-112">Description</span></span>                                                   |
|------------------------------------------------|--------------------|---------------------------------------------------------------|
| <span data-ttu-id="ed63a-113">**ncrypt \_ RSA \_ - \_ Algorithmusgruppe**</span><span class="sxs-lookup"><span data-stu-id="ed63a-113">**NCRYPT\_RSA\_ALGORITHM\_GROUP**</span></span><br/>   | <span data-ttu-id="ed63a-114">RSA</span><span class="sxs-lookup"><span data-stu-id="ed63a-114">"RSA"</span></span><br/>   | <span data-ttu-id="ed63a-115">Die RSA-Algorithmusgruppe.</span><span class="sxs-lookup"><span data-stu-id="ed63a-115">The RSA algorithm group.</span></span><br/>                           |
| <span data-ttu-id="ed63a-116">**ncrypt \_ dh \_ - \_ Algorithmusgruppe**</span><span class="sxs-lookup"><span data-stu-id="ed63a-116">**NCRYPT\_DH\_ALGORITHM\_GROUP**</span></span><br/>    | <span data-ttu-id="ed63a-117">Nenden</span><span class="sxs-lookup"><span data-stu-id="ed63a-117">"DH"</span></span><br/>    | <span data-ttu-id="ed63a-118">Die Diffie-Hellman Algorithmusgruppe.</span><span class="sxs-lookup"><span data-stu-id="ed63a-118">The Diffie-Hellman algorithm group.</span></span><br/>                |
| <span data-ttu-id="ed63a-119">**ncrypt \_ DSA \_ - \_ Algorithmusgruppe**</span><span class="sxs-lookup"><span data-stu-id="ed63a-119">**NCRYPT\_DSA\_ALGORITHM\_GROUP**</span></span><br/>   | <span data-ttu-id="ed63a-120">DSA</span><span class="sxs-lookup"><span data-stu-id="ed63a-120">"DSA"</span></span><br/>   | <span data-ttu-id="ed63a-121">Die DSA-Algorithmusgruppe.</span><span class="sxs-lookup"><span data-stu-id="ed63a-121">The DSA algorithm group.</span></span><br/>                           |
| <span data-ttu-id="ed63a-122">**ncrypt \_ ECDSA \_ - \_ Algorithmusgruppe**</span><span class="sxs-lookup"><span data-stu-id="ed63a-122">**NCRYPT\_ECDSA\_ALGORITHM\_GROUP**</span></span><br/> | <span data-ttu-id="ed63a-123">ECDsa</span><span class="sxs-lookup"><span data-stu-id="ed63a-123">"ECDSA"</span></span><br/> | <span data-ttu-id="ed63a-124">Die DSA-Algorithmusgruppe für die elliptische Kurve.</span><span class="sxs-lookup"><span data-stu-id="ed63a-124">The elliptic curve DSA algorithm group.</span></span><br/>            |
| <span data-ttu-id="ed63a-125">**ncrypt \_ ECDH \_ - \_ Algorithmusgruppe**</span><span class="sxs-lookup"><span data-stu-id="ed63a-125">**NCRYPT\_ECDH\_ALGORITHM\_GROUP**</span></span><br/>  | <span data-ttu-id="ed63a-126">"ECDH"</span><span class="sxs-lookup"><span data-stu-id="ed63a-126">"ECDH"</span></span><br/>  | <span data-ttu-id="ed63a-127">Die elliptische Kurve Diffie-Hellman Algorithmusgruppe.</span><span class="sxs-lookup"><span data-stu-id="ed63a-127">The elliptic curve Diffie-Hellman algorithm group.</span></span><br/> |



 


</dt> </dl> </dd> <dt>

<span data-ttu-id="ed63a-128"><span id="NCRYPT_ALGORITHM_PROPERTY"></span><span id="ncrypt_algorithm_property"></span>**ncrypt \_ - \_ algorithmuseigenschaft**</span><span class="sxs-lookup"><span data-stu-id="ed63a-128"><span id="NCRYPT_ALGORITHM_PROPERTY"></span><span id="ncrypt_algorithm_property"></span>**NCRYPT\_ALGORITHM\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed63a-129">L "Algorithmusname"</span><span class="sxs-lookup"><span data-stu-id="ed63a-129">L"Algorithm Name"</span></span>
</dt> <dt>



<span data-ttu-id="ed63a-130">Eine NULL-terminierte Unicode-Zeichenfolge, die den Namen des Algorithmus des-Objekts enthält.</span><span class="sxs-lookup"><span data-stu-id="ed63a-130">A null-terminated Unicode string that contains the name of the object's algorithm.</span></span> <span data-ttu-id="ed63a-131">Hierbei kann es sich um einen vordefinierten [**CNG-Algorithmusbezeichner**](cng-algorithm-identifiers.md) oder einen anderen registrierten Algorithmusbezeichner handeln.</span><span class="sxs-lookup"><span data-stu-id="ed63a-131">This can be one of the predefined [**CNG Algorithm Identifiers**](cng-algorithm-identifiers.md) or another registered algorithm identifier.</span></span> <span data-ttu-id="ed63a-132">Diese Eigenschaft gilt nur für Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="ed63a-132">This property only applies to keys.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ed63a-133"><span id="NCRYPT_ASSOCIATED_ECDH_KEY"></span><span id="ncrypt_associated_ecdh_key"></span>**ncrypt zugeordneter \_ \_ ECDH- \_ Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="ed63a-133"><span id="NCRYPT_ASSOCIATED_ECDH_KEY"></span><span id="ncrypt_associated_ecdh_key"></span>**NCRYPT\_ASSOCIATED\_ECDH\_KEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed63a-134">L "smartcardassociatedecdhkey"</span><span class="sxs-lookup"><span data-stu-id="ed63a-134">L"SmartCardAssociatedECDHKey"</span></span>
</dt> <dt>



<span data-ttu-id="ed63a-135">Ein **LPWSTR** -Wert, der den Container Namen des ECDH-Schlüssels (Elliptic Curve Diffie-Hellman) angibt, der während der Anmeldung für ein angegebenes Handle eines ECDSA (Elliptic Curve Digital Signature)-Schlüssels verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ed63a-135">An **LPWSTR** value that indicates the container name of the Elliptic Curve Diffie-Hellman (ECDH) key to use during logon for a given handle to an Elliptic Curve Digital Signature Algorithm (ECDSA) key.</span></span> <span data-ttu-id="ed63a-136">Wenn keine ECDH-Schlüssel auf der Karte vorhanden sind, gibt der [*Schlüsselspeicher Anbieter*](/windows/desktop/SecGloss/k-gly) (KSP) die Rückgabe **\_ nicht \_ gefunden** zurück.</span><span class="sxs-lookup"><span data-stu-id="ed63a-136">If there are no ECDH keys on the card, the [*key storage provider*](/windows/desktop/SecGloss/k-gly) (KSP) returns **NTE\_NOT\_FOUND**.</span></span> <span data-ttu-id="ed63a-137">Diese Eigenschaft gilt für ECDSA-Schlüssel für die Anmeldung mit Smartcards.</span><span class="sxs-lookup"><span data-stu-id="ed63a-137">This property applies to ECDSA keys for logon with smart cards.</span></span> <span data-ttu-id="ed63a-138">Die-Eigenschaft wird vom Microsoft-Smartcard-Schlüsselspeicher Anbieter und nicht vom Microsoft-Software Schlüsselspeicher-Anbieter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ed63a-138">The property is supported by the Microsoft Smart Card key storage provider and not by the Microsoft Software key storage provider.</span></span>

<span data-ttu-id="ed63a-139">**Windows Server 2008 und Windows Vista:** Dieser Wert wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ed63a-139">**Windows Server 2008 and Windows Vista:** This value is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ed63a-140"><span id="NCRYPT_BLOCK_LENGTH_PROPERTY"></span><span id="ncrypt_block_length_property"></span>**ncrypt- \_ Block \_ Längen \_ Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="ed63a-140"><span id="NCRYPT_BLOCK_LENGTH_PROPERTY"></span><span id="ncrypt_block_length_property"></span>**NCRYPT\_BLOCK\_LENGTH\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed63a-141">L "Block Länge"</span><span class="sxs-lookup"><span data-stu-id="ed63a-141">L"Block Length"</span></span>
</dt> <dt>



<span data-ttu-id="ed63a-142">Ein **DWORD** -Wert, der die Länge des Verschlüsselungs Blocks in Bytes enthält.</span><span class="sxs-lookup"><span data-stu-id="ed63a-142">A **DWORD** that contains the length, in bytes, of the encryption block.</span></span> <span data-ttu-id="ed63a-143">Diese Eigenschaft gilt nur für Schlüssel, die die Verschlüsselung unterstützen.</span><span class="sxs-lookup"><span data-stu-id="ed63a-143">This property only applies to keys that support encryption.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ed63a-144"><span id="NCRYPT_CERTIFICATE_PROPERTY"></span><span id="ncrypt_certificate_property"></span>**ncrypt- \_ Zertifikat \_ Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="ed63a-144"><span id="NCRYPT_CERTIFICATE_PROPERTY"></span><span id="ncrypt_certificate_property"></span>**NCRYPT\_CERTIFICATE\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed63a-145">L "smartcardkeycertificate"</span><span class="sxs-lookup"><span data-stu-id="ed63a-145">L"SmartCardKeyCertificate"</span></span>
</dt> <dt>



<span data-ttu-id="ed63a-146">Ein [*BLOB*](/windows/desktop/SecGloss/b-gly) , das ein X. 509-Zertifikat enthält, das dem Schlüssel zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="ed63a-146">A [*BLOB*](/windows/desktop/SecGloss/b-gly) that contains an X.509 certificate that is associated with the key.</span></span>

<span data-ttu-id="ed63a-147">**Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista:** Ein [*BLOB*](/windows/desktop/SecGloss/b-gly) , das das [*Smartcard*](/windows/desktop/SecGloss/s-gly) -Schlüssel [*Zertifikat*](/windows/desktop/SecGloss/c-gly)enthält.</span><span class="sxs-lookup"><span data-stu-id="ed63a-147">**Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** A [*BLOB*](/windows/desktop/SecGloss/b-gly) that contains the [*smart card*](/windows/desktop/SecGloss/s-gly) key [*certificate*](/windows/desktop/SecGloss/c-gly).</span></span> <span data-ttu-id="ed63a-148">Diese Eigenschaft wird vom Microsoft-Software Schlüsselspeicher-Anbieter nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ed63a-148">This property is not supported by the Microsoft Software Key Storage Provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ed63a-149"><span id="NCRYPT_DH_PARAMETERS_PROPERTY"></span><span id="ncrypt_dh_parameters_property"></span>**ncrypt \_ dh- \_ Parameter ( \_ Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="ed63a-149"><span id="NCRYPT_DH_PARAMETERS_PROPERTY"></span><span id="ncrypt_dh_parameters_property"></span>**NCRYPT\_DH\_PARAMETERS\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed63a-150">L "dhparameters"</span><span class="sxs-lookup"><span data-stu-id="ed63a-150">L"DHParameters"</span></span>
</dt> <dt>



<span data-ttu-id="ed63a-151">Gibt Parameter an, die mit einem Diffie-Hellman Schlüssel verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ed63a-151">Specifies parameters to use with a Diffie-Hellman key.</span></span> <span data-ttu-id="ed63a-152">Dieser Datentyp ist ein Zeiger auf eine [**bcrypt \_ dh- \_ Parameter \_ Header**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_parameter_header) Struktur.</span><span class="sxs-lookup"><span data-stu-id="ed63a-152">This data type is a pointer to a [**BCRYPT\_DH\_PARAMETER\_HEADER**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_parameter_header) structure.</span></span> <span data-ttu-id="ed63a-153">Diese Eigenschaft kann nur festgelegt werden und muss für den Schlüssel festgelegt werden, bevor der Schlüssel abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="ed63a-153">This property can only be set and must be set for the key before the key is completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ed63a-154"><span id="NCRYPT_EXPORT_POLICY_PROPERTY"></span><span id="ncrypt_export_policy_property"></span>**ncrypt- \_ Export \_ Richtlinien \_ Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="ed63a-154"><span id="NCRYPT_EXPORT_POLICY_PROPERTY"></span><span id="ncrypt_export_policy_property"></span>**NCRYPT\_EXPORT\_POLICY\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed63a-155">L "Richtlinie exportieren"</span><span class="sxs-lookup"><span data-stu-id="ed63a-155">L"Export Policy"</span></span>
</dt> <dt>



<span data-ttu-id="ed63a-156">Ein **DWORD** , das einen Satz von Flags enthält, die die Export Richtlinie für einen persistenten Schlüssel angeben.</span><span class="sxs-lookup"><span data-stu-id="ed63a-156">A **DWORD** that contains a set of flags that specify the export policy for a persisted key.</span></span> <span data-ttu-id="ed63a-157">Diese Eigenschaft gilt nur für Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="ed63a-157">This property only applies to keys.</span></span> <span data-ttu-id="ed63a-158">Diese kann NULL oder eine Kombination aus einem oder mehreren der folgenden Werte enthalten.</span><span class="sxs-lookup"><span data-stu-id="ed63a-158">This can contain zero or a combination of one or more of the following values.</span></span>



| <span data-ttu-id="ed63a-159">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="ed63a-159">Identifier</span></span>                                    | <span data-ttu-id="ed63a-160">Wert</span><span class="sxs-lookup"><span data-stu-id="ed63a-160">Value</span></span>      | <span data-ttu-id="ed63a-161">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ed63a-161">Description</span></span>                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed63a-162">**ncrypt \_ Allow \_ - \_ exportflag**</span><span class="sxs-lookup"><span data-stu-id="ed63a-162">**NCRYPT\_ALLOW\_EXPORT\_FLAG**</span></span>               | <span data-ttu-id="ed63a-163">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ed63a-163">0x00000001</span></span> | <span data-ttu-id="ed63a-164">Der private Schlüssel kann exportiert werden.</span><span class="sxs-lookup"><span data-stu-id="ed63a-164">The private key can be exported.</span></span>                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="ed63a-165">**ncrypt, nur-Text- \_ Export Kennzeichen zulassen \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ed63a-165">**NCRYPT\_ALLOW\_PLAINTEXT\_EXPORT\_FLAG**</span></span>    | <span data-ttu-id="ed63a-166">0x00000002</span><span class="sxs-lookup"><span data-stu-id="ed63a-166">0x00000002</span></span> | <span data-ttu-id="ed63a-167">Der private Schlüssel kann im Klartext-Format exportiert werden.</span><span class="sxs-lookup"><span data-stu-id="ed63a-167">The private key can be exported in plaintext form.</span></span>                                                                                                                                                                                                                                                               |
| <span data-ttu-id="ed63a-168">**ncrypt \_ - \_ Flag zum Archivieren zulassen \_**</span><span class="sxs-lookup"><span data-stu-id="ed63a-168">**NCRYPT\_ALLOW\_ARCHIVING\_FLAG**</span></span>            | <span data-ttu-id="ed63a-169">0x00000004</span><span class="sxs-lookup"><span data-stu-id="ed63a-169">0x00000004</span></span> | <span data-ttu-id="ed63a-170">Der private Schlüssel kann für Archivierungszwecke einmal exportiert werden.</span><span class="sxs-lookup"><span data-stu-id="ed63a-170">The private key can be exported once for archiving purposes.</span></span> <span data-ttu-id="ed63a-171">Dieses Flag gilt nur für den ursprünglichen Schlüssel handle, für den es festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="ed63a-171">This flag only applies to the original key handle on which it is set.</span></span> <span data-ttu-id="ed63a-172">Diese Richtlinie kann nur auf das ursprüngliche Schlüssel handle angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="ed63a-172">This policy can only be applied to the original key handle.</span></span> <span data-ttu-id="ed63a-173">Nachdem das Schlüssel Handle geschlossen wurde, kann der Schlüssel nicht mehr zu Archivierungszwecken exportiert werden.</span><span class="sxs-lookup"><span data-stu-id="ed63a-173">After the key handle has been closed, the key can no longer be exported for archiving purposes.</span></span>                   |
| <span data-ttu-id="ed63a-174">**ncrypt \_ - \_ Flag zum Archivieren von Klartext zulassen \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ed63a-174">**NCRYPT\_ALLOW\_PLAINTEXT\_ARCHIVING\_FLAG**</span></span> | <span data-ttu-id="ed63a-175">0x00000008</span><span class="sxs-lookup"><span data-stu-id="ed63a-175">0x00000008</span></span> | <span data-ttu-id="ed63a-176">Der private Schlüssel kann für Archivierungszwecke einmal im Klartext-Format exportiert werden.</span><span class="sxs-lookup"><span data-stu-id="ed63a-176">The private key can be exported once in plaintext form for archiving purposes.</span></span> <span data-ttu-id="ed63a-177">Dieses Flag gilt nur für den ursprünglichen Schlüssel handle, für den es festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="ed63a-177">This flag only applies to the original key handle on which it is set.</span></span> <span data-ttu-id="ed63a-178">Diese Richtlinie kann nur auf das ursprüngliche Schlüssel handle angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="ed63a-178">This policy can only be applied to the original key handle.</span></span> <span data-ttu-id="ed63a-179">Nachdem das Schlüssel Handle geschlossen wurde, kann der Schlüssel nicht mehr zu Archivierungszwecken exportiert werden.</span><span class="sxs-lookup"><span data-stu-id="ed63a-179">After the key handle has been closed, the key can no longer be exported for archiving purposes.</span></span> |



 


</dt> </dl> </dd> <dt>

<span data-ttu-id="ed63a-180"><span id="NCRYPT_IMPL_TYPE_PROPERTY"></span><span id="ncrypt_impl_type_property"></span>**ncrypt \_ impl \_ Type ( \_ Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="ed63a-180"><span id="NCRYPT_IMPL_TYPE_PROPERTY"></span><span id="ncrypt_impl_type_property"></span>**NCRYPT\_IMPL\_TYPE\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed63a-181">L "Impl Type"</span><span class="sxs-lookup"><span data-stu-id="ed63a-181">L"Impl Type"</span></span>
</dt> <dt>



<span data-ttu-id="ed63a-182">Ein **DWORD** -Wert, der einen Satz von Flags enthält, die Implementierungsdetails des Anbieters definieren.</span><span class="sxs-lookup"><span data-stu-id="ed63a-182">A **DWORD** that contains a set of flags that define implementation details of the provider.</span></span> <span data-ttu-id="ed63a-183">Diese Eigenschaft gilt nur für Schlüsselspeicher Anbieter.</span><span class="sxs-lookup"><span data-stu-id="ed63a-183">This property only applies to key storage providers.</span></span> <span data-ttu-id="ed63a-184">Diese kann NULL oder eine Kombination aus einem oder mehreren der folgenden Werte enthalten.</span><span class="sxs-lookup"><span data-stu-id="ed63a-184">This can contain zero or a combination of one or more of the following values.</span></span>



| <span data-ttu-id="ed63a-185">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="ed63a-185">Identifier</span></span>                            | <span data-ttu-id="ed63a-186">Wert</span><span class="sxs-lookup"><span data-stu-id="ed63a-186">Value</span></span>      | <span data-ttu-id="ed63a-187">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ed63a-187">Description</span></span>                                               |
|---------------------------------------|------------|-----------------------------------------------------------|
| <span data-ttu-id="ed63a-188">**ncrypt \_ impl- \_ hardwareflag \_**</span><span class="sxs-lookup"><span data-stu-id="ed63a-188">**NCRYPT\_IMPL\_HARDWARE\_FLAG**</span></span>      | <span data-ttu-id="ed63a-189">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ed63a-189">0x00000001</span></span> | <span data-ttu-id="ed63a-190">Der Anbieter ist Hardware basiert.</span><span class="sxs-lookup"><span data-stu-id="ed63a-190">The provider is hardware based.</span></span>                           |
| <span data-ttu-id="ed63a-191">**ncrypt \_ impl \_ - \_ softwareflag**</span><span class="sxs-lookup"><span data-stu-id="ed63a-191">**NCRYPT\_IMPL\_SOFTWARE\_FLAG**</span></span>      | <span data-ttu-id="ed63a-192">0x00000002</span><span class="sxs-lookup"><span data-stu-id="ed63a-192">0x00000002</span></span> | <span data-ttu-id="ed63a-193">Der Anbieter ist Software basiert.</span><span class="sxs-lookup"><span data-stu-id="ed63a-193">The provider is software based.</span></span>                           |
| <span data-ttu-id="ed63a-194">**ncrypt \_ impl-Wechsel \_ \_ Flag**</span><span class="sxs-lookup"><span data-stu-id="ed63a-194">**NCRYPT\_IMPL\_REMOVABLE\_FLAG**</span></span>     | <span data-ttu-id="ed63a-195">0x00000008</span><span class="sxs-lookup"><span data-stu-id="ed63a-195">0x00000008</span></span> | <span data-ttu-id="ed63a-196">Der Anbieter ist austauschbar.</span><span class="sxs-lookup"><span data-stu-id="ed63a-196">The provider is removable.</span></span>                                |
| <span data-ttu-id="ed63a-197">**RNG-Flag für NCrypt \_ impl- \_ Hardware \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ed63a-197">**NCRYPT\_IMPL\_HARDWARE\_RNG\_FLAG**</span></span> | <span data-ttu-id="ed63a-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ed63a-198">0x00000010</span></span> | <span data-ttu-id="ed63a-199">Der Anbieter ist ein hardwarebasierter Zufallszahlengenerator.</span><span class="sxs-lookup"><span data-stu-id="ed63a-199">The provider is a hardware based random number generator.</span></span> |



 


</dt> </dl> </dd> <dt>

<span data-ttu-id="ed63a-200"><span id="NCRYPT_KEY_TYPE_PROPERTY"></span><span id="ncrypt_key_type_property"></span>**ncrypt \_ - \_ Schlüsseltyp \_ Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="ed63a-200"><span id="NCRYPT_KEY_TYPE_PROPERTY"></span><span id="ncrypt_key_type_property"></span>**NCRYPT\_KEY\_TYPE\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed63a-201">L "Schlüsseltyp"</span><span class="sxs-lookup"><span data-stu-id="ed63a-201">L"Key Type"</span></span>
</dt> <dt>



<span data-ttu-id="ed63a-202">Ein **DWORD** , das einen Satz von Flags enthält, die den Schlüsseltyp definieren.</span><span class="sxs-lookup"><span data-stu-id="ed63a-202">A **DWORD** that contains a set of flags that define the key type.</span></span> <span data-ttu-id="ed63a-203">Diese Eigenschaft gilt nur für Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="ed63a-203">This property only applies to keys.</span></span> <span data-ttu-id="ed63a-204">Dieser Wert kann NULL oder den folgenden Wert enthalten.</span><span class="sxs-lookup"><span data-stu-id="ed63a-204">This can contain zero or the following value.</span></span>



| <span data-ttu-id="ed63a-205">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="ed63a-205">Identifier</span></span>                     | <span data-ttu-id="ed63a-206">Wert</span><span class="sxs-lookup"><span data-stu-id="ed63a-206">Value</span></span>      | <span data-ttu-id="ed63a-207">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ed63a-207">Description</span></span>                                                                                              |
|--------------------------------|------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed63a-208">**ncrypt \_ - \_ computerschlüsselflag \_**</span><span class="sxs-lookup"><span data-stu-id="ed63a-208">**NCRYPT\_MACHINE\_KEY\_FLAG**</span></span> | <span data-ttu-id="ed63a-209">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ed63a-209">0x00000001</span></span> | <span data-ttu-id="ed63a-210">Der Schlüssel gilt für den lokalen Computer.</span><span class="sxs-lookup"><span data-stu-id="ed63a-210">The key applies to the local computer.</span></span> <span data-ttu-id="ed63a-211">Wenn dieses Flag nicht vorhanden ist, gilt der Schlüssel für den aktuellen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="ed63a-211">If this flag is not present, the key applies to the current user.</span></span> |



 


</dt> </dl> </dd> <dt>

<span data-ttu-id="ed63a-212"><span id="NCRYPT_KEY_USAGE_PROPERTY"></span><span id="ncrypt_key_usage_property"></span>**ncrypt- \_ Schlüssel \_ Verwendungs \_ Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="ed63a-212"><span id="NCRYPT_KEY_USAGE_PROPERTY"></span><span id="ncrypt_key_usage_property"></span>**NCRYPT\_KEY\_USAGE\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed63a-213">L "Schlüssel Verwendung"</span><span class="sxs-lookup"><span data-stu-id="ed63a-213">L"Key Usage"</span></span>
</dt> <dt>



<span data-ttu-id="ed63a-214">Ein **DWORD** -Wert, der einen Satz von Flags enthält, mit denen die Verwendungs Details für einen Schlüssel definiert werden.</span><span class="sxs-lookup"><span data-stu-id="ed63a-214">A **DWORD** that contains a set of flags that define the usage details for a key.</span></span> <span data-ttu-id="ed63a-215">Diese Eigenschaft gilt nur für Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="ed63a-215">This property only applies to keys.</span></span> <span data-ttu-id="ed63a-216">Diese kann NULL oder eine Kombination aus einem oder mehreren der folgenden Werte enthalten.</span><span class="sxs-lookup"><span data-stu-id="ed63a-216">This can contain zero or a combination of one or more of the following values.</span></span>



| <span data-ttu-id="ed63a-217">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="ed63a-217">Identifier</span></span>                              | <span data-ttu-id="ed63a-218">Wert</span><span class="sxs-lookup"><span data-stu-id="ed63a-218">Value</span></span>      | <span data-ttu-id="ed63a-219">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ed63a-219">Description</span></span>                                          |
|-----------------------------------------|------------|------------------------------------------------------|
| <span data-ttu-id="ed63a-220">**ncrypt \_ ' \_ entschlüsselungsflag zulassen ' \_**</span><span class="sxs-lookup"><span data-stu-id="ed63a-220">**NCRYPT\_ALLOW\_DECRYPT\_FLAG**</span></span>        | <span data-ttu-id="ed63a-221">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ed63a-221">0x00000001</span></span> | <span data-ttu-id="ed63a-222">Der Schlüssel kann für die Entschlüsselung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ed63a-222">The key can be used for decryption.</span></span>                  |
| <span data-ttu-id="ed63a-223">**ncrypt \_ - \_ Flag zum Signieren zulassen \_**</span><span class="sxs-lookup"><span data-stu-id="ed63a-223">**NCRYPT\_ALLOW\_SIGNING\_FLAG**</span></span>        | <span data-ttu-id="ed63a-224">0x00000002</span><span class="sxs-lookup"><span data-stu-id="ed63a-224">0x00000002</span></span> | <span data-ttu-id="ed63a-225">Der Schlüssel kann zum Signieren verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ed63a-225">The key can be used for signing.</span></span>                     |
| <span data-ttu-id="ed63a-226">**ncrypt- \_ Flag zum gewähren der \_ Schlüssel \_ Vereinbarung \_**</span><span class="sxs-lookup"><span data-stu-id="ed63a-226">**NCRYPT\_ALLOW\_KEY\_AGREEMENT\_FLAG**</span></span> | <span data-ttu-id="ed63a-227">0x00000004</span><span class="sxs-lookup"><span data-stu-id="ed63a-227">0x00000004</span></span> | <span data-ttu-id="ed63a-228">Der Schlüssel kann für die Verschlüsselung von geheimen Schlüsseln verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ed63a-228">The key can be used for secret agreement encryption.</span></span> |
| <span data-ttu-id="ed63a-229">**ncrypt \_ \_ alle \_ Verwendungszwecke zulassen**</span><span class="sxs-lookup"><span data-stu-id="ed63a-229">**NCRYPT\_ALLOW\_ALL\_USAGES**</span></span>          | <span data-ttu-id="ed63a-230">0x00ffffff</span><span class="sxs-lookup"><span data-stu-id="ed63a-230">0x00ffffff</span></span> | <span data-ttu-id="ed63a-231">Der Schlüssel kann für beliebige Zwecke verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ed63a-231">The key can be used for any purpose.</span></span>                 |



 


</dt> </dl> </dd> <dt>

<span data-ttu-id="ed63a-232"><span id="NCRYPT_LAST_MODIFIED_PROPERTY"></span><span id="ncrypt_last_modified_property"></span>**ncrypt- \_ Eigenschaft "zuletzt \_ geändert" \_**</span><span class="sxs-lookup"><span data-stu-id="ed63a-232"><span id="NCRYPT_LAST_MODIFIED_PROPERTY"></span><span id="ncrypt_last_modified_property"></span>**NCRYPT\_LAST\_MODIFIED\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed63a-233">L "geändert"</span><span class="sxs-lookup"><span data-stu-id="ed63a-233">L"Modified"</span></span>
</dt> <dt>



<span data-ttu-id="ed63a-234">Gibt an, wann der Schlüssel zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="ed63a-234">Indicates when the key was last modified.</span></span> <span data-ttu-id="ed63a-235">Dieser Datentyp ist ein Zeiger auf eine [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="ed63a-235">This data type is a pointer to a [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) structure.</span></span> <span data-ttu-id="ed63a-236">Diese Eigenschaft gilt nur für persistente Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="ed63a-236">This property only applies to persisted keys.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ed63a-237"><span id="NCRYPT_LENGTH_PROPERTY"></span><span id="ncrypt_length_property"></span>**ncrypt \_ length ( \_ Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="ed63a-237"><span id="NCRYPT_LENGTH_PROPERTY"></span><span id="ncrypt_length_property"></span>**NCRYPT\_LENGTH\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed63a-238">L "Länge"</span><span class="sxs-lookup"><span data-stu-id="ed63a-238">L"Length"</span></span>
</dt> <dt>



<span data-ttu-id="ed63a-239">Ein **DWORD** , das die Länge des Schlüssels in Bits enthält.</span><span class="sxs-lookup"><span data-stu-id="ed63a-239">A **DWORD** that contains the length, in bits, of the key.</span></span> <span data-ttu-id="ed63a-240">Diese Eigenschaft gilt nur für Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="ed63a-240">This property only applies to keys.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ed63a-241"><span id="NCRYPT_LENGTHS_PROPERTY"></span><span id="ncrypt_lengths_property"></span>**ncrypt- \_ Längen \_ Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="ed63a-241"><span id="NCRYPT_LENGTHS_PROPERTY"></span><span id="ncrypt_lengths_property"></span>**NCRYPT\_LENGTHS\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed63a-242">L "Längen"</span><span class="sxs-lookup"><span data-stu-id="ed63a-242">L"Lengths"</span></span>
</dt> <dt>



<span data-ttu-id="ed63a-243">Gibt die Schlüsselgrößen an, die vom Schlüssel unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="ed63a-243">Indicates the key sizes that are supported by the key.</span></span> <span data-ttu-id="ed63a-244">Dieser Datentyp ist ein Zeiger auf eine [**NCrypt- \_ unterstützte \_ Längen**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncrypt_supported_lengths) Struktur, die diese Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="ed63a-244">This data type is a pointer to an [**NCRYPT\_SUPPORTED\_LENGTHS**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncrypt_supported_lengths) structure that contains this information.</span></span> <span data-ttu-id="ed63a-245">Diese Eigenschaft gilt nur für Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="ed63a-245">This property only applies to keys.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ed63a-246"><span id="NCRYPT_MAX_NAME_LENGTH_PROPERTY"></span><span id="ncrypt_max_name_length_property"></span>**maximale NCrypt- \_ \_ namens \_ Länge ( \_ Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="ed63a-246"><span id="NCRYPT_MAX_NAME_LENGTH_PROPERTY"></span><span id="ncrypt_max_name_length_property"></span>**NCRYPT\_MAX\_NAME\_LENGTH\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed63a-247">L "maximale namens Länge"</span><span class="sxs-lookup"><span data-stu-id="ed63a-247">L"Max Name Length"</span></span>
</dt> <dt>



<span data-ttu-id="ed63a-248">Ein **DWORD** , das die maximale Länge (in Zeichen) des Namens eines permanenten Schlüssels enthält.</span><span class="sxs-lookup"><span data-stu-id="ed63a-248">A **DWORD** that contains the maximum length, in characters, of the name of a persistent key.</span></span> <span data-ttu-id="ed63a-249">Diese Eigenschaft gilt nur für einen Anbieter.</span><span class="sxs-lookup"><span data-stu-id="ed63a-249">This property only applies to a provider.</span></span>

<span data-ttu-id="ed63a-250">Diese Eigenschaft ist in erster Linie für die Verwendung durch Schlüsselspeicher Anbieter vorgesehen, die Ihre Schlüssel auf einem Gerät speichern, das nur über eine begrenzte Menge an verfügbarem Arbeitsspeicher verfügt, z. b. eine Smartcard.</span><span class="sxs-lookup"><span data-stu-id="ed63a-250">This property is primarily intended to be used by key storage providers that store their keys on a device that has a limited amount of available memory, such as a smart card.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ed63a-251"><span id="NCRYPT_NAME_PROPERTY"></span><span id="ncrypt_name_property"></span>**ncrypt- \_ Name ( \_ Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="ed63a-251"><span id="NCRYPT_NAME_PROPERTY"></span><span id="ncrypt_name_property"></span>**NCRYPT\_NAME\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed63a-252">L "Name"</span><span class="sxs-lookup"><span data-stu-id="ed63a-252">L"Name"</span></span>
</dt> <dt>



<span data-ttu-id="ed63a-253">Ein Zeiger auf eine NULL-terminierte Unicode-Zeichenfolge, die den Namen des-Objekts enthält.</span><span class="sxs-lookup"><span data-stu-id="ed63a-253">A pointer to a null-terminated Unicode string that contains the name of the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ed63a-254"><span id="NCRYPT_PIN_PROMPT_PROPERTY"></span><span id="ncrypt_pin_prompt_property"></span>**ncrypt \_ PIN-Eingabe Aufforderungs \_ \_ Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="ed63a-254"><span id="NCRYPT_PIN_PROMPT_PROPERTY"></span><span id="ncrypt_pin_prompt_property"></span>**NCRYPT\_PIN\_PROMPT\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed63a-255">L "smartcardpinprompt"</span><span class="sxs-lookup"><span data-stu-id="ed63a-255">L"SmartCardPinPrompt"</span></span>
</dt> <dt>



<span data-ttu-id="ed63a-256">Dieser Wert wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ed63a-256">This value is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ed63a-257"><span id="NCRYPT_PIN_PROPERTY"></span><span id="ncrypt_pin_property"></span>**ncrypt- \_ Pin- \_ Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="ed63a-257"><span id="NCRYPT_PIN_PROPERTY"></span><span id="ncrypt_pin_property"></span>**NCRYPT\_PIN\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed63a-258">L "Smartcardpin"</span><span class="sxs-lookup"><span data-stu-id="ed63a-258">L"SmartCardPin"</span></span>
</dt> <dt>



<span data-ttu-id="ed63a-259">Ein Zeiger auf eine NULL-terminierte Unicode-Zeichenfolge, die die PIN enthält.</span><span class="sxs-lookup"><span data-stu-id="ed63a-259">A pointer to a null-terminated Unicode string that contains the PIN.</span></span> <span data-ttu-id="ed63a-260">Die PIN wird für einen Smartcardschlüssel oder das Kennwort für einen Kenn Wort geschützten Schlüssel verwendet, der in einem softwarebasierten KSP gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="ed63a-260">The PIN is used for a smart card key or the password for a password-protected key stored in a software-based KSP.</span></span> <span data-ttu-id="ed63a-261">Diese Eigenschaft kann nur festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="ed63a-261">This property can only be set.</span></span> <span data-ttu-id="ed63a-262">Der Wert wird von Microsoft-kSPS zwischengespeichert, sodass der Benutzer nur einmal pro Prozess aufgefordert wird.</span><span class="sxs-lookup"><span data-stu-id="ed63a-262">Microsoft KSPs will cache this value so that the user is only prompted once per process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ed63a-263"><span id="NCRYPT_PROVIDER_HANDLE_PROPERTY"></span><span id="ncrypt_provider_handle_property"></span>**ncrypt- \_ Anbieter \_ handle ( \_ Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="ed63a-263"><span id="NCRYPT_PROVIDER_HANDLE_PROPERTY"></span><span id="ncrypt_provider_handle_property"></span>**NCRYPT\_PROVIDER\_HANDLE\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed63a-264">L "Anbieter Handle"</span><span class="sxs-lookup"><span data-stu-id="ed63a-264">L"Provider Handle"</span></span>
</dt> <dt>



<span data-ttu-id="ed63a-265">Ein **NCrypt- \_ Prov- \_ handle** , das das Handle des CNG-Schlüsselspeicher Anbieters enthält.</span><span class="sxs-lookup"><span data-stu-id="ed63a-265">An **NCRYPT\_PROV\_HANDLE** that contains the handle of the CNG key storage provider.</span></span> <span data-ttu-id="ed63a-266">Wenn Sie mit der Verwendung des Handles fertig sind, müssen Sie [**ncryptfreobject**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptfreeobject) aufrufen, um es freizugeben.</span><span class="sxs-lookup"><span data-stu-id="ed63a-266">When you are finished using the handle, you must call [**NCryptFreeObject**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptfreeobject) to release it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ed63a-267"><span id="NCRYPT_READER_PROPERTY"></span><span id="ncrypt_reader_property"></span>**ncrypt- \_ Reader- \_ Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="ed63a-267"><span id="NCRYPT_READER_PROPERTY"></span><span id="ncrypt_reader_property"></span>**NCRYPT\_READER\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed63a-268">L "smartcardreader"</span><span class="sxs-lookup"><span data-stu-id="ed63a-268">L"SmartCardReader"</span></span>
</dt> <dt>



<span data-ttu-id="ed63a-269">Ein Zeiger auf eine NULL-terminierte Unicode-Zeichenfolge, die den Namen des smartcardreaders enthält.</span><span class="sxs-lookup"><span data-stu-id="ed63a-269">A pointer to a null-terminated Unicode string that contains the name of the smart card reader.</span></span> <span data-ttu-id="ed63a-270">Diese Eigenschaft kann nur festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="ed63a-270">This property can only be set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ed63a-271"><span id="NCRYPT_ROOT_CERTSTORE_PROPERTY"></span><span id="ncrypt_root_certstore_property"></span>**ncrypt-Stamm \_ \_ Eigenschaft "certstore" \_**</span><span class="sxs-lookup"><span data-stu-id="ed63a-271"><span id="NCRYPT_ROOT_CERTSTORE_PROPERTY"></span><span id="ncrypt_root_certstore_property"></span>**NCRYPT\_ROOT\_CERTSTORE\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed63a-272">L "smartcardrootcertstore"</span><span class="sxs-lookup"><span data-stu-id="ed63a-272">L"SmartcardRootCertStore"</span></span>
</dt> <dt>



<span data-ttu-id="ed63a-273">Ein **HCERTSTORE** , der den Zertifikat Speicher der Smartcard darstellt.</span><span class="sxs-lookup"><span data-stu-id="ed63a-273">An **HCERTSTORE** that represents the smart card root certificate store.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ed63a-274"><span id="_NCRYPT_SCARD_PIN_ID"></span><span id="_ncrypt_scard_pin_id"></span>**NCrypt \_ Card- \_ Pin- \_ ID**</span><span class="sxs-lookup"><span data-stu-id="ed63a-274"><span id="_NCRYPT_SCARD_PIN_ID"></span><span id="_ncrypt_scard_pin_id"></span> **NCRYPT\_SCARD\_PIN\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed63a-275">L "smartcardpinid"</span><span class="sxs-lookup"><span data-stu-id="ed63a-275">L"SmartCardPinId"</span></span>
</dt> <dt>



<span data-ttu-id="ed63a-276">Ein Zeiger auf den **Pin- \_ ID** -Wert, der einem bestimmten [*Kryptografieschlüssel*](/windows/desktop/SecGloss/c-gly) auf einer [*Smartcard*](/windows/desktop/SecGloss/s-gly)zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="ed63a-276">A pointer to the **PIN\_ID** value associated with a given [*cryptographic key*](/windows/desktop/SecGloss/c-gly) on a [*smart card*](/windows/desktop/SecGloss/s-gly).</span></span> <span data-ttu-id="ed63a-277">Dies ist eine schreibgeschützte Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="ed63a-277">This is a read-only property.</span></span> <span data-ttu-id="ed63a-278">Der Datentyp der **Pin- \_ ID** ist in cardmod. h definiert.</span><span class="sxs-lookup"><span data-stu-id="ed63a-278">The **PIN\_ID** data type is defined in Cardmod.h.</span></span>

<span data-ttu-id="ed63a-279">**Windows Server 2008 und Windows Vista:** Dieser Wert wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ed63a-279">**Windows Server 2008 and Windows Vista:** This value is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ed63a-280"><span id="NCRYPT_SCARD_PIN_INFO"></span><span id="ncrypt_scard_pin_info"></span>**ncrypt-anheft \_ \_ \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="ed63a-280"><span id="NCRYPT_SCARD_PIN_INFO"></span><span id="ncrypt_scard_pin_info"></span>**NCRYPT\_SCARD\_PIN\_INFO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed63a-281">L "smartcardpininfo"</span><span class="sxs-lookup"><span data-stu-id="ed63a-281">L"SmartCardPinInfo"</span></span>
</dt> <dt>



<span data-ttu-id="ed63a-282">Ein Zeiger auf [**die \_ Info**](/windows/desktop/api/mbnapi/ns-mbnapi-mbn_pin_info) -Struktur der PIN, die einem bestimmten Kryptografieschlüssel auf der Smartcard zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="ed63a-282">A pointer to [**PIN\_INFO**](/windows/desktop/api/mbnapi/ns-mbnapi-mbn_pin_info) structure of the PIN associated with a given cryptographic key on the smart card.</span></span> <span data-ttu-id="ed63a-283">Der Aufrufer stellt das Schlüssel Handle bereit.</span><span class="sxs-lookup"><span data-stu-id="ed63a-283">The caller provides the key handle.</span></span> <span data-ttu-id="ed63a-284">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="ed63a-284">This property is a read-only property.</span></span> <span data-ttu-id="ed63a-285">Die **Pin- \_ Informations** Struktur ist in cardmod. h definiert.</span><span class="sxs-lookup"><span data-stu-id="ed63a-285">The **PIN\_INFO** structure is defined in Cardmod.h.</span></span>

<span data-ttu-id="ed63a-286">**Windows Server 2008 und Windows Vista:** Dieser Wert wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ed63a-286">**Windows Server 2008 and Windows Vista:** This value is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ed63a-287"><span id="NCRYPT_SECURE_PIN_PROPERTY"></span><span id="ncrypt_secure_pin_property"></span>**ncrypt \_ Secure \_ PIN ( \_ Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="ed63a-287"><span id="NCRYPT_SECURE_PIN_PROPERTY"></span><span id="ncrypt_secure_pin_property"></span>**NCRYPT\_SECURE\_PIN\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed63a-288">L "smartcardsecurepin"</span><span class="sxs-lookup"><span data-stu-id="ed63a-288">L"SmartCardSecurePin"</span></span>
</dt> <dt>



<span data-ttu-id="ed63a-289">Ein Zeiger auf eine NULL-terminierte Unicode-Zeichenfolge, die die PIN der Smartcard-Sitzung enthält.</span><span class="sxs-lookup"><span data-stu-id="ed63a-289">A pointer to a null-terminated Unicode string that contains the smart card session PIN.</span></span> <span data-ttu-id="ed63a-290">Diese Eigenschaft kann nur festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="ed63a-290">This property can only be set.</span></span>

<span data-ttu-id="ed63a-291">**Windows Vista:** Diese Eigenschaft wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ed63a-291">**Windows Vista:** This property is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ed63a-292"><span id="NCRYPT_SECURITY_DESCR_PROPERTY"></span><span id="ncrypt_security_descr_property"></span>**ncrypt \_ Security \_ descr ( \_ Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="ed63a-292"><span id="NCRYPT_SECURITY_DESCR_PROPERTY"></span><span id="ncrypt_security_descr_property"></span>**NCRYPT\_SECURITY\_DESCR\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed63a-293">L "Sicherheit-descr"</span><span class="sxs-lookup"><span data-stu-id="ed63a-293">L"Security Descr"</span></span>
</dt> <dt>



<span data-ttu-id="ed63a-294">Ein Zeiger auf eine [**Sicherheits \_ deskriptorstruktur**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) , die Zugriffs Steuerungsinformationen für den Schlüssel enthält.</span><span class="sxs-lookup"><span data-stu-id="ed63a-294">A pointer to a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure that contains access control information for the key.</span></span> <span data-ttu-id="ed63a-295">Diese Eigenschaft gilt nur für persistente Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="ed63a-295">This property only applies to persistent keys.</span></span> <span data-ttu-id="ed63a-296">Der *dwFlags* -Parameter der [**ncryptgetproperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) -oder [**ncryptsetproperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty) -Funktion identifiziert den Teil der Sicherheits Beschreibung, der abgerufen oder festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ed63a-296">The *dwFlags* parameter of the [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) or [**NCryptSetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty) function identifies the part of the security descriptor to get or set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ed63a-297"><span id="NCRYPT_SECURITY_DESCR_SUPPORT_PROPERTY"></span><span id="ncrypt_security_descr_support_property"></span>**ncrypt \_ Security \_ descr \_ Support ( \_ Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="ed63a-297"><span id="NCRYPT_SECURITY_DESCR_SUPPORT_PROPERTY"></span><span id="ncrypt_security_descr_support_property"></span>**NCRYPT\_SECURITY\_DESCR\_SUPPORT\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed63a-298">L "Unterstützung der Sicherheits Abstützung"</span><span class="sxs-lookup"><span data-stu-id="ed63a-298">L"Security Descr Support"</span></span>
</dt> <dt>



<span data-ttu-id="ed63a-299">Gibt an, ob der Anbieter Sicherheits Deskriptoren für Schlüssel unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ed63a-299">Indicates whether the provider supports security descriptors for keys.</span></span> <span data-ttu-id="ed63a-300">Diese Eigenschaft ist ein **DWORD** , das 1 enthält, wenn der Anbieter Sicherheits Deskriptoren für Schlüssel unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ed63a-300">This property is a **DWORD** that contains 1 if the provider supports security descriptors for keys.</span></span> <span data-ttu-id="ed63a-301">Wenn diese Eigenschaft einen anderen Wert enthält oder wenn die [**ncryptgetproperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) -Funktion den Wert "" **\_ nicht \_ unterstützt** zurückgibt, unterstützt der Anbieter keine Sicherheits Deskriptoren für Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="ed63a-301">If this property contains any other value, or if the [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) function returns **NTE\_NOT\_SUPPORTED**, then the provider does not support security descriptors for keys.</span></span> <span data-ttu-id="ed63a-302">Diese Eigenschaft gilt nur für-Anbieter.</span><span class="sxs-lookup"><span data-stu-id="ed63a-302">This property only applies to providers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ed63a-303"><span id="NCRYPT_SMARTCARD_GUID_PROPERTY"></span><span id="ncrypt_smartcard_guid_property"></span>**ncrypt- \_ Smartcard- \_ GUID- \_ Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="ed63a-303"><span id="NCRYPT_SMARTCARD_GUID_PROPERTY"></span><span id="ncrypt_smartcard_guid_property"></span>**NCRYPT\_SMARTCARD\_GUID\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed63a-304">L "smartcardguid"</span><span class="sxs-lookup"><span data-stu-id="ed63a-304">L"SmartCardGuid"</span></span>
</dt> <dt>



<span data-ttu-id="ed63a-305">Ein BLOB, das den Bezeichner der Smartcard enthält.</span><span class="sxs-lookup"><span data-stu-id="ed63a-305">A BLOB that contains the identifier of the smart card.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ed63a-306"><span id="NCRYPT_UI_POLICY_PROPERTY"></span><span id="ncrypt_ui_policy_property"></span>**ncrypt- \_ UI- \_ Richtlinien \_ Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="ed63a-306"><span id="NCRYPT_UI_POLICY_PROPERTY"></span><span id="ncrypt_ui_policy_property"></span>**NCRYPT\_UI\_POLICY\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed63a-307">L "UI-Richtlinie"</span><span class="sxs-lookup"><span data-stu-id="ed63a-307">L"UI Policy"</span></span>
</dt> <dt>



<span data-ttu-id="ed63a-308">Bei Verwendung mit der [**ncryptsetproperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty) -Funktion oder der [**ncryptgetproperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) -Funktion handelt es sich hierbei um einen Zeiger auf eine [**NCrypt- \_ UI- \_ Richtlinien**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncrypt_ui_policy) Struktur, die die Richtlinie für die starke Schlüssel Benutzeroberfläche für den Schlüssel enthält.</span><span class="sxs-lookup"><span data-stu-id="ed63a-308">If used with the [**NCryptSetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty) or [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) function, this is a pointer to an [**NCRYPT\_UI\_POLICY**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncrypt_ui_policy) structure that contains the strong key user interface policy for the key.</span></span> <span data-ttu-id="ed63a-309">Diese Eigenschaft gilt nur für persistente Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="ed63a-309">This property only applies to persistent keys.</span></span> <span data-ttu-id="ed63a-310">Diese Eigenschaft kann nur festgelegt werden, wenn der Schlüssel generiert wird.</span><span class="sxs-lookup"><span data-stu-id="ed63a-310">This property can only be set when the key is being generated.</span></span> <span data-ttu-id="ed63a-311">Nachdem die [**ncryptfinalizekey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptfinalizekey) -Funktion für diesen Schlüssel aufgerufen wurde, wird diese Eigenschaft schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="ed63a-311">Once the [**NCryptFinalizeKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptfinalizekey) function has been called for this key, this property becomes read-only.</span></span>

<span data-ttu-id="ed63a-312">Ein Schlüsselspeicher Anbieter kann diesen Parameter über eine [**ncryptsetpropertyfn**](https://www.bing.com/search?q=**NCryptSetPropertyFn**) -Rückruffunktion empfangen.</span><span class="sxs-lookup"><span data-stu-id="ed63a-312">A key storage provider can receive this parameter through an [**NCryptSetPropertyFn**](https://www.bing.com/search?q=**NCryptSetPropertyFn**) callback function.</span></span> <span data-ttu-id="ed63a-313">Der Parameterwert ist eine NCrypt- \_ UI- \_ Richtlinien- \_ BLOB-Struktur, die die gleichen Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="ed63a-313">The parameter value is an NCRYPT\_UI\_POLICY\_BLOB structure that contains the same information.</span></span> <span data-ttu-id="ed63a-314">Wenn eine Anwendung eine Anforderung über ncryptsetpropertyfn an den Anbieter sendet, damit diese Eigenschaft zurückgegeben wird, wird davon ausgegangen, dass der Anbieter die \_ blobstruktur der NCrypt-UI- \_ Richtlinie zurückgibt \_ .</span><span class="sxs-lookup"><span data-stu-id="ed63a-314">Similarly, when an application makes a request through NCryptSetPropertyFn to the provider to return this property, the provider is expected to return an NCRYPT\_UI\_POLICY\_BLOB structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ed63a-315"><span id="NCRYPT_UNIQUE_NAME_PROPERTY"></span><span id="ncrypt_unique_name_property"></span>**eindeutige NCrypt- \_ \_ Name- \_ Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="ed63a-315"><span id="NCRYPT_UNIQUE_NAME_PROPERTY"></span><span id="ncrypt_unique_name_property"></span>**NCRYPT\_UNIQUE\_NAME\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed63a-316">L "eindeutiger Name"</span><span class="sxs-lookup"><span data-stu-id="ed63a-316">L"Unique Name"</span></span>
</dt> <dt>



<span data-ttu-id="ed63a-317">Ein Zeiger auf eine NULL-terminierte Unicode-Zeichenfolge, die den eindeutigen Namen des-Objekts enthält.</span><span class="sxs-lookup"><span data-stu-id="ed63a-317">A pointer to a null-terminated Unicode string that contains the unique name of the object.</span></span> <span data-ttu-id="ed63a-318">Dies ist ein alternativer Name, der beim Zugriff auf den Schlüssel verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="ed63a-318">This is an alternate name that can be used when accessing the key.</span></span> <span data-ttu-id="ed63a-319">Diese Eigenschaft wird verwendet, wenn der Schlüssel Name, der ursprünglich an [**ncryptkreatepersistedkey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptcreatepersistedkey) übergeben wurde, nicht eindeutig genug ist, um den persistenten Schlüssel zuverlässig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="ed63a-319">This property is used when it is thought that the key name originally passed to [**NCryptCreatePersistedKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptcreatepersistedkey) is not unique enough to reliably identify the persisted key.</span></span> <span data-ttu-id="ed63a-320">Der Microsoft-Schlüsselspeicher Anbieter gibt den Dateinamen des Schlüssels als diese Eigenschaft zurück.</span><span class="sxs-lookup"><span data-stu-id="ed63a-320">The Microsoft key storage provider will return the file name of the key as this property.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ed63a-321"><span id="NCRYPT_USE_CONTEXT_PROPERTY"></span><span id="ncrypt_use_context_property"></span>**ncrypt \_ - \_ Kontext \_ Eigenschaft verwenden**</span><span class="sxs-lookup"><span data-stu-id="ed63a-321"><span id="NCRYPT_USE_CONTEXT_PROPERTY"></span><span id="ncrypt_use_context_property"></span>**NCRYPT\_USE\_CONTEXT\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed63a-322">L "Kontext verwenden"</span><span class="sxs-lookup"><span data-stu-id="ed63a-322">L"Use Context"</span></span>
</dt> <dt>



<span data-ttu-id="ed63a-323">Ein Zeiger auf eine NULL-terminierte Unicode-Zeichenfolge, die den Kontext des Vorgangs beschreibt.</span><span class="sxs-lookup"><span data-stu-id="ed63a-323">A pointer to a null-terminated Unicode string that describes the context of the operation.</span></span> <span data-ttu-id="ed63a-324">Diese Eigenschaft ist nicht persistent und kann entweder für einen Anbieter oder einen Schlüssel festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="ed63a-324">This property is not persistent and can be set on either a provider or a key.</span></span> <span data-ttu-id="ed63a-325">Ein Schlüssel hat keinen Zugriff auf die **NCrypt- \_ Eigenschaft \_ Kontext \_ Eigenschaft** des Anbieters, da die Eigenschaft nur für das Handle spezifisch ist, für das Sie festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ed63a-325">A key does not have access to the **NCRYPT\_USE\_CONTEXT\_PROPERTY** property of the provider because the property is specific only to the handle it is set for.</span></span>

<span data-ttu-id="ed63a-326">Ein Beispiel, in dem diese Eigenschaft im Kontext eines Anbieters verwendet wird, ist ein Schlüsselspeicher Anbieter, der den Benutzer während eines [**ncryptopenkey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) -Aufforderungs Aufforderungs (z. b. "Einfügen Ihrer Smartcard in den Reader") auffordern muss.</span><span class="sxs-lookup"><span data-stu-id="ed63a-326">An example where this property would be used in the context of a provider is a key storage provider that needs to prompt the user during a call to [**NCryptOpenKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) (for example, "Insert your smart card in the reader.").</span></span> <span data-ttu-id="ed63a-327">Da das Schlüssel handle erst verfügbar ist, nachdem **ncryptopenkey** zurückgegeben wurde, sollte die Anwendung diese Eigenschaft für das Anbieter handle vor dem Aufrufen von **ncryptopenkey** festlegen.</span><span class="sxs-lookup"><span data-stu-id="ed63a-327">Because the key handle is not available until after **NCryptOpenKey** returns, the application should set this property on the provider handle prior to calling **NCryptOpenKey**.</span></span>

<span data-ttu-id="ed63a-328">Ein Beispiel für die Verwendung dieser Eigenschaft im Kontext eines Schlüssel Handles ist ein Schlüsselspeicher Anbieter, der den Benutzer während eines Vorgangs mithilfe des Schlüssels auffordern muss (z. b. "diese Anwendung muss diesen Schlüssel zum Signieren eines Dokuments verwenden").</span><span class="sxs-lookup"><span data-stu-id="ed63a-328">An example where this property would be used in the context of a key handle is a key storage provider that needs to prompt the user during an operation using the key (for example, "This application needs to use this key to sign a document.").</span></span> <span data-ttu-id="ed63a-329">Der Anbieter könnte diese Kontextinformationen dann an den Benutzer in jeder Benutzeroberfläche weiterleiten, die während des Vorgangs angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="ed63a-329">The provider could then relay this context information to the user in any user interface shown during the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ed63a-330"><span id="NCRYPT_USE_COUNT_ENABLED_PROPERTY"></span><span id="ncrypt_use_count_enabled_property"></span>**ncrypt \_ - \_ Eigenschaft "Anzahl \_ aktivierte Elemente" \_**</span><span class="sxs-lookup"><span data-stu-id="ed63a-330"><span id="NCRYPT_USE_COUNT_ENABLED_PROPERTY"></span><span id="ncrypt_use_count_enabled_property"></span>**NCRYPT\_USE\_COUNT\_ENABLED\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed63a-331">L "aktivierte Verwendungs Anzahl"</span><span class="sxs-lookup"><span data-stu-id="ed63a-331">L"Enabled Use Count"</span></span>
</dt> <dt>



<span data-ttu-id="ed63a-332">Gibt an, ob der Anbieter die Verwendungs Zählung für Schlüssel unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ed63a-332">Indicates whether the provider supports usage counting for keys.</span></span> <span data-ttu-id="ed63a-333">Diese Eigenschaft ist ein **DWORD** -Wert, der 1 enthält, wenn der Anbieter die Verwendungs Zählung für Schlüssel unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ed63a-333">This property is a **DWORD** that contains 1 if the provider supports usage counting for keys.</span></span> <span data-ttu-id="ed63a-334">Wenn diese Eigenschaft einen anderen Wert enthält oder wenn die [**ncryptgetproperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) -Funktion die Funktion "die Funktion wird **\_ nicht \_ unterstützt**" zurückgibt, unterstützt der Anbieter keine Verwendungs Zählung für Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="ed63a-334">If this property contains any other value, or if the [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) function returns **NTE\_NOT\_SUPPORTED**, then the provider does not support usage counting for keys.</span></span> <span data-ttu-id="ed63a-335">Diese Eigenschaft gilt nur für-Anbieter.</span><span class="sxs-lookup"><span data-stu-id="ed63a-335">This property only applies to providers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ed63a-336"><span id="NCRYPT_USE_COUNT_PROPERTY"></span><span id="ncrypt_use_count_property"></span>**ncrypt, \_ Verwendung der \_ Count- \_ Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="ed63a-336"><span id="NCRYPT_USE_COUNT_PROPERTY"></span><span id="ncrypt_use_count_property"></span>**NCRYPT\_USE\_COUNT\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed63a-337">L "Verwendung der Anzahl"</span><span class="sxs-lookup"><span data-stu-id="ed63a-337">L"Use Count"</span></span>
</dt> <dt>



<span data-ttu-id="ed63a-338">Eine [**\_ ganzzahlige ularge**](https://docs.microsoft.com/windows/win32/api/winnt/ns-winnt-ularge_integer~r1) -Variable, die die Anzahl der Vorgänge enthält, die der angegebene [*private Schlüssel*](/windows/desktop/SecGloss/p-gly) ausgeführt hat.</span><span class="sxs-lookup"><span data-stu-id="ed63a-338">A [**ULARGE\_INTEGER**](https://docs.microsoft.com/windows/win32/api/winnt/ns-winnt-ularge_integer~r1) variable that contains the number of operations that the specified [*private key*](/windows/desktop/SecGloss/p-gly) has performed.</span></span> <span data-ttu-id="ed63a-339">Diese Eigenschaft ist optional und wird möglicherweise nicht von allen Anbietern unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ed63a-339">This property is optional and may not be supported by all providers.</span></span> <span data-ttu-id="ed63a-340">Anbieter, die diese Eigenschaft für Schlüssel unterstützen, sollten auch die **Eigenschaften Eigenschaft NCrypt- \_ \_ \_ aktivierte \_ Eigenschaft** für das Anbieter handle unterstützen.</span><span class="sxs-lookup"><span data-stu-id="ed63a-340">Providers that support this property on keys should also support the **NCRYPT\_USE\_COUNT\_ENABLED\_PROPERTY** property on the provider handle.</span></span> <span data-ttu-id="ed63a-341">Der Microsoft-Schlüsselspeicher Anbieter unterstützt diese Eigenschaft nicht.</span><span class="sxs-lookup"><span data-stu-id="ed63a-341">The Microsoft key storage provider does not support this property.</span></span> <span data-ttu-id="ed63a-342">Diese Eigenschaft gilt nur für persistente Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="ed63a-342">This property only applies to persistent keys.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ed63a-343"><span id="NCRYPT_USER_CERTSTORE_PROPERTY"></span><span id="ncrypt_user_certstore_property"></span>**ncrypt \_ - \_ benutzercertstore ( \_ Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="ed63a-343"><span id="NCRYPT_USER_CERTSTORE_PROPERTY"></span><span id="ncrypt_user_certstore_property"></span>**NCRYPT\_USER\_CERTSTORE\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed63a-344">L "smartcardusercertstore"</span><span class="sxs-lookup"><span data-stu-id="ed63a-344">L"SmartCardUserCertStore"</span></span>
</dt> <dt>



<span data-ttu-id="ed63a-345">Ein **HCERTSTORE** , der den Smartcard-Benutzerzertifikat Speicher darstellt.</span><span class="sxs-lookup"><span data-stu-id="ed63a-345">An **HCERTSTORE** that represents the smart card user certificate store.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ed63a-346"><span id="NCRYPT_VERSION_PROPERTY"></span><span id="ncrypt_version_property"></span>**ncrypt- \_ Version ( \_ Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="ed63a-346"><span id="NCRYPT_VERSION_PROPERTY"></span><span id="ncrypt_version_property"></span>**NCRYPT\_VERSION\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed63a-347">L "Version"</span><span class="sxs-lookup"><span data-stu-id="ed63a-347">L"Version"</span></span>
</dt> <dt>



<span data-ttu-id="ed63a-348">Ein **DWORD** , das die Softwareversion des Anbieters enthält.</span><span class="sxs-lookup"><span data-stu-id="ed63a-348">A **DWORD** that contains the software version of the provider.</span></span> <span data-ttu-id="ed63a-349">Das hohe Wort enthält die Hauptversion, und das niedrige Wort enthält die neben Version.</span><span class="sxs-lookup"><span data-stu-id="ed63a-349">The high word contains the major version and the low word contains the minor version.</span></span> <span data-ttu-id="ed63a-350">Beispiel: 0x00030033 = 3,51.</span><span class="sxs-lookup"><span data-stu-id="ed63a-350">For example, 0x00030033 = 3.51.</span></span> <span data-ttu-id="ed63a-351">Diese Eigenschaft gilt nur für-Anbieter.</span><span class="sxs-lookup"><span data-stu-id="ed63a-351">This property only applies to providers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ed63a-352"><span id="NCRYPT_WINDOW_HANDLE_PROPERTY"></span><span id="ncrypt_window_handle_property"></span>**ncrypt- \_ Fenster \_ handle ( \_ Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="ed63a-352"><span id="NCRYPT_WINDOW_HANDLE_PROPERTY"></span><span id="ncrypt_window_handle_property"></span>**NCRYPT\_WINDOW\_HANDLE\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed63a-353">L "hWnd Handle"</span><span class="sxs-lookup"><span data-stu-id="ed63a-353">L"HWND Handle"</span></span>
</dt> <dt>



<span data-ttu-id="ed63a-354">Ein Zeiger auf das Fenster Handle (**HWND**), das als übergeordnetes Element der angezeigten Benutzeroberfläche verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ed63a-354">A pointer to the window handle (**HWND**) to be used as the parent of any user interface that is displayed.</span></span>

<span data-ttu-id="ed63a-355">Da ein unerwünschtes Verhalten auftreten kann, wenn eine Benutzeroberfläche mit einem **null** -Fenster Handle für das übergeordnete Element angezeigt wird, wird dringend empfohlen, dass ein Schlüsselspeicher Anbieter keine Benutzeroberfläche anzeigt, es sei denn, diese Eigenschaft ist festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ed63a-355">Because undesirable behavior can happen when a user interface is shown by using a **NULL** window handle for the parent, we strongly recommend that a key storage provider not display a user interface unless this property is set.</span></span>


</dt> </dl> </dd> </dl>

<span data-ttu-id="ed63a-356">Die folgenden Werte werden verwendet, um Grenzwerte für Eigenschafts Daten zu definieren.</span><span class="sxs-lookup"><span data-stu-id="ed63a-356">The following values are used to define limits of property data.</span></span>



| <span data-ttu-id="ed63a-357">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="ed63a-357">Constant/value</span></span>                                                                                                                                                                                                                                                 | <span data-ttu-id="ed63a-358">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ed63a-358">Description</span></span>                                                              |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------|
| <span id="NCRYPT_MAX_PROPERTY_DATA"></span><span id="ncrypt_max_property_data"></span><dl> <span data-ttu-id="ed63a-359"><dt>**NCrypt \_ Maximale \_ Eigenschafts \_ Daten**</dt> <dt>0x100000</dt></span><span class="sxs-lookup"><span data-stu-id="ed63a-359"><dt>**NCRYPT\_MAX\_PROPERTY\_DATA**</dt> <dt>0x100000</dt></span></span> </dl> | <span data-ttu-id="ed63a-360">Gibt die maximale Größe eines Eigenschafts Werts in Bytes an.</span><span class="sxs-lookup"><span data-stu-id="ed63a-360">Specifies the maximum size of a property value, in bytes.</span></span><br/>     |
| <span id="NCRYPT_MAX_PROPERTY_NAME"></span><span id="ncrypt_max_property_name"></span><dl> <span data-ttu-id="ed63a-361"><dt>**NCrypt \_ Maximaler \_ Eigenschafts \_ Name**</dt> <dt>64</dt></span><span class="sxs-lookup"><span data-stu-id="ed63a-361"><dt>**NCRYPT\_MAX\_PROPERTY\_NAME**</dt> <dt>64</dt></span></span> </dl>       | <span data-ttu-id="ed63a-362">Gibt die maximale Größe eines Eigenschafts namens in Zeichen an.</span><span class="sxs-lookup"><span data-stu-id="ed63a-362">Specifies the maximum size of a property name, in characters.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="ed63a-363">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ed63a-363">Requirements</span></span>



| <span data-ttu-id="ed63a-364">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ed63a-364">Requirement</span></span> | <span data-ttu-id="ed63a-365">Wert</span><span class="sxs-lookup"><span data-stu-id="ed63a-365">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ed63a-366">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ed63a-366">Minimum supported client</span></span><br/> | <span data-ttu-id="ed63a-367">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ed63a-367">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="ed63a-368">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ed63a-368">Minimum supported server</span></span><br/> | <span data-ttu-id="ed63a-369">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ed63a-369">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ed63a-370">Header</span><span class="sxs-lookup"><span data-stu-id="ed63a-370">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed63a-371"><dt>Ncrypt. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed63a-371"><dt>Ncrypt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed63a-372">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ed63a-372">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed63a-373">**Ncryptgetproperty**</span><span class="sxs-lookup"><span data-stu-id="ed63a-373">**NCryptGetProperty**</span></span>](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty)
</dt> <dt>

[<span data-ttu-id="ed63a-374">**Ncryptsetproperty**</span><span class="sxs-lookup"><span data-stu-id="ed63a-374">**NCryptSetProperty**</span></span>](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty)
</dt> </dl>

 

