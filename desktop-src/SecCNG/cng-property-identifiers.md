---
description: Wird mit den Funktionen BCryptGetProperty und BCryptSetProperty verwendet, um eine Eigenschaft zu identifizieren.
ms.assetid: ebcc8202-94b4-47ad-9918-e5bc843a258f
title: Primitive Kryptografieeigenschaftsbezeichner (Bcrypt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5452c6a55388998a08577cb19ef2fba6905faddbdf28f5f8051b7bc8d9d1c375
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118908221"
---
# <a name="cryptography-primitive-property-identifiers"></a>Primitive Kryptografieeigenschaftsbezeichner

Die folgenden Werte werden mit den [**Funktionen BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) und [**BCryptSetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetproperty) verwendet, um eine Eigenschaft zu identifizieren.

<dl> <dt>

<span id="BCRYPT_ALGORITHM_NAME"></span><span id="bcrypt_algorithm_name"></span>**\_BCRYPT-ALGORITHMUSNAME \_**
</dt> <dd> <dl> <dt>

L"AlgorithmName"
</dt> <dt>



Eine auf NULL beendete Unicode-Zeichenfolge, die den Namen des Algorithmus enthält.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_AUTH_TAG_LENGTH"></span><span id="bcrypt_auth_tag_length"></span>**LÄNGE DES \_ BCRYPT-AUTHENTIFIZIERUNGSTAGS \_ \_**
</dt> <dd> <dl> <dt>

L"AuthTagLength"
</dt> <dt>



Die Längen von Authentifizierungstags, die vom Algorithmus unterstützt werden. Diese Eigenschaft ist eine [**BCRYPT \_ AUTH \_ TAG \_ \_ LENGTHS-Struktur.**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_key_lengths_struct) Diese Eigenschaft gilt nur für Algorithmen.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_BLOCK_LENGTH"></span><span id="bcrypt_block_length"></span>**\_BCRYPT-BLOCKLÄNGE \_**
</dt> <dd> <dl> <dt>

L"BlockLength"
</dt> <dt>



Die Größe eines Verschlüsselungsblocks für den Algorithmus in Bytes. Diese Eigenschaft gilt nur für Blockchiffrenalgorithmen. Dieser Datentyp ist ein **DWORD-Datentyp.**


</dt> </dl> </dd> <dt>

<span id="BCRYPT_BLOCK_SIZE_LIST"></span><span id="bcrypt_block_size_list"></span>**\_ \_ BCRYPT-BLOCKGRÖßENLISTE \_**
</dt> <dd> <dl> <dt>

L"BlockSizeList"
</dt> <dt>



Eine Liste der Blocklängen, die von einem Verschlüsselungsalgorithmus unterstützt werden. Dieser Datentyp ist ein Array von **DWORDs.** Die Anzahl der Elemente im Array kann bestimmt werden, indem die Anzahl der abgerufenen Bytes durch die Größe eines einzelnen **DWORD-Elements dividiert wird.**


</dt> </dl> </dd> <dt>

<span id="BCRYPT_CHAINING_MODE"></span><span id="bcrypt_chaining_mode"></span>**\_BCRYPT-VERKETTUNGSMODUS \_**
</dt> <dd> <dl> <dt>

L"ChainingMode"
</dt> <dt>



Ein Zeiger auf eine auf NULL beendete Unicode-Zeichenfolge, die den Verkettungsmodus des Verschlüsselungsalgorithmus darstellt. Diese Eigenschaft kann für ein Algorithmushand handle oder ein Schlüsselhandy auf einen der folgenden Werte festgelegt werden.



| Bezeichner                   | Wert                         | BESCHREIBUNG                                                                                                                                                                    |
|------------------------------|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **BCRYPT \_ CHAIN \_ MODE \_ CBC** | L"ChainingModeCBC"<br/> | Legt den Verkettungsmodus des Algorithmus auf [*die Verschlüsselungsblockkette fest.*](/windows/desktop/SecGloss/c-gly)<br/>            |
| **BCRYPT \_ CHAIN \_ MODE \_ CCM** | L"ChainingModeCCM"<br/> | Legt den Verkettungsmodus des Algorithmus auf counter mit dem CBC-MAC-Modus (CCM) fest. **Windows Vista:** Dieser Wert wird ab Windows Vista mit SP1 unterstützt.<br/> <br/> |
| **BCRYPT \_ CHAIN \_ MODE \_ CFB** | L"ChainingModeCFB"<br/> | Legt den Verkettungsmodus des Algorithmus auf [*Verschlüsselungsfeedback fest.*](/windows/desktop/SecGloss/c-gly)<br/>                              |
| **BCRYPT \_ CHAIN \_ MODE \_ VERKETTET** | L"ChainingModeECB"<br/> | Legt den Verkettungsmodus des Algorithmus auf das [*elektronische Codebook fest.*](/windows/desktop/SecGloss/e-gly)<br/>                  |
| **BCRYPT \_ CHAIN \_ MODE \_ GCM** | L"ChainingModeGCM"<br/> | Legt den Verkettungsmodus des Algorithmus auf galois/counter mode (GCM) fest. **Windows Vista:** Dieser Wert wird ab Windows Vista mit SP1 unterstützt.<br/> <br/>       |
| **BCRYPT \_ CHAIN \_ MODE \_ NA**  | L"ChainingModeN/A"<br/> | Der Algorithmus unterstützt keine Verkettung.<br/>                                                                                                                            |



 


</dt> </dl> </dd> <dt>

<span id="BCRYPT_DH_PARAMETERS"></span><span id="bcrypt_dh_parameters"></span>**BCRYPT \_ DH \_ PARAMETERS**
</dt> <dd> <dl> <dt>

L"DHParameters"
</dt> <dt>



Gibt Parameter an, die mit einem Schlüssel Diffie-Hellman werden. Dieser Datentyp ist ein Zeiger auf eine [**BCRYPT \_ DH PARAMETER \_ \_ HEADER-Struktur.**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_parameter_header) Diese Eigenschaft kann nur festgelegt werden und muss für den Schlüssel festgelegt werden, bevor der Schlüssel abgeschlossen wird.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_DSA_PARAMETERS"></span><span id="bcrypt_dsa_parameters"></span>**\_BCRYPT-DSA-PARAMETER \_**
</dt> <dd> <dl> <dt>

L"DSAParameters"
</dt> <dt>



Gibt Parameter an, die mit einem DSA-Schlüssel verwendet werden. Diese Eigenschaft ist ein [**BCRYPT \_ DSA \_ PARAMETER HEADER \_ oder**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header) eine [**BCRYPT \_ DSA PARAMETER HEADER \_ \_ \_ V2-Struktur.**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header_v2) Diese Eigenschaft kann nur festgelegt werden und muss für den Schlüssel festgelegt werden, bevor der Schlüssel abgeschlossen wird.

**Windows 8:** Ab Windows 8 kann diese Eigenschaft eine [**BCRYPT \_ DSA \_ PARAMETER HEADER \_ \_ V2-Struktur**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header_v2) sein. Verwenden Sie diese Struktur, wenn die Schlüsselgröße 1024 Bits überschreitet und kleiner oder gleich 3072 Bits ist. Wenn die Schlüsselgröße größer oder gleich 512, aber kleiner oder gleich 1024 Bits ist, verwenden Sie die [**BCRYPT \_ DSA \_ PARAMETER \_ HEADER-Struktur.**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header)


</dt> </dl> </dd> <dt>

<span id="BCRYPT_EFFECTIVE_KEY_LENGTH"></span><span id="bcrypt_effective_key_length"></span>**EFFEKTIVE \_ \_ BCRYPT-SCHLÜSSELLÄNGE \_**
</dt> <dd> <dl> <dt>

L"EffectiveKeyLength"
</dt> <dt>



Die Größe der effektiven Länge eines RC2-Schlüssels in Bits. Dieser Datentyp ist ein **DWORD-Datentyp.**


</dt> </dl> </dd> <dt>

<span id="BCRYPT_HASH_BLOCK_LENGTH"></span><span id="bcrypt_hash_block_length"></span>**LÄNGE DES \_ \_ BCRYPT-HASHBLOCKS \_**
</dt> <dd> <dl> <dt>

L"HashBlockLength"
</dt> <dt>



Die Größe des Blocks für einen Hash in Bytes. Diese Eigenschaft gilt nur für Hashalgorithmen. Dieser Datentyp ist ein **DWORD-Datentyp.**


</dt> </dl> </dd> <dt>

<span id="BCRYPT_HASH_LENGTH"></span><span id="bcrypt_hash_length"></span>**\_BCRYPT-HASHLÄNGE \_**
</dt> <dd> <dl> <dt>

L"HashDigestLength"
</dt> <dt>



Die Größe des Hashwerts eines Hashanbieters in Bytes. Dieser Datentyp ist ein **DWORD-Datentyp.**


</dt> </dl> </dd> <dt>

<span id="BCRYPT_HASH_OID_LIST"></span><span id="bcrypt_hash_oid_list"></span>**\_ \_ BCRYPT-HASHOIDLISTE \_**
</dt> <dd> <dl> <dt>

L"HashOIDList"
</dt> <dt>



Die Liste [](/windows/desktop/SecGloss/d-gly)der DER-codierten [*Hashobjektbezeichner*](/windows/desktop/SecGloss/o-gly) (OIDs). Diese Eigenschaft ist eine [**\_ BCRYPT-OID-LIST-Struktur. \_**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_oid_list) Diese Eigenschaft kann nur gelesen werden.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_INITIALIZATION_VECTOR"></span><span id="bcrypt_initialization_vector"></span>**\_BCRYPT-INITIALISIERUNGSVEKTOR \_**
</dt> <dd> <dl> <dt>

L"IV"
</dt> <dt>



Enthält den [*Initialisierungsvektor*](/windows/desktop/SecGloss/i-gly) (IV) für einen Schlüssel. Diese Eigenschaft gilt nur für Schlüssel.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_KEY_LENGTH"></span><span id="bcrypt_key_length"></span>**\_BCRYPT-SCHLÜSSELLÄNGE \_**
</dt> <dd> <dl> <dt>

L"KeyLength"
</dt> <dt>



Die Größe des Schlüsselwerts eines symmetrischen Schlüsselanbieters in Bits. Dieser Datentyp ist ein **DWORD-Datentyp.**


</dt> </dl> </dd> <dt>

<span id="BCRYPT_KEY_LENGTHS"></span><span id="bcrypt_key_lengths"></span>**\_ \_ BCRYPT-SCHLÜSSELLÄNGEN**
</dt> <dd> <dl> <dt>

L"KeyLengths"
</dt> <dt>



Die Schlüssellängen, die vom Algorithmus unterstützt werden. Diese Eigenschaft ist eine [**BCRYPT \_ KEY \_ \_ LENGTHS-Struktur.**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_key_lengths_struct) Diese Eigenschaft gilt nur für Algorithmen.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_KEY_OBJECT_LENGTH"></span><span id="bcrypt_key_object_length"></span>**LÄNGE DES \_ \_ BCRYPT-SCHLÜSSELOBJEKTS \_**
</dt> <dd> <dl> <dt>

L"KeyObjectLength"
</dt> <dt>



Diese Eigenschaft wird nicht verwendet. Die **BCRYPT \_ OBJECT \_ LENGTH-Eigenschaft** wird verwendet, um diese Informationen zu erhalten.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_KEY_STRENGTH"></span><span id="bcrypt_key_strength"></span>**\_BCRYPT-SCHLÜSSELSTÄRKE \_**
</dt> <dd> <dl> <dt>

L"KeyStrength"
</dt> <dt>



Die Anzahl der Bits im Schlüssel. Dieser Datentyp ist ein **DWORD-Datentyp.** Diese Eigenschaft gilt nur für Schlüssel.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_MESSAGE_BLOCK_LENGTH"></span><span id="bcrypt_message_block_length"></span>**LÄNGE DES \_ BCRYPT-NACHRICHTENBLOCKS \_ \_**
</dt> <dd> <dl> <dt>

L"MessageBlockLength"
</dt> <dt>



Dies kann für jedes Schlüsselhandle festgelegt werden, für das der CFB-Verkettungsmodus festgelegt ist. Standardmäßig ist diese Eigenschaft für 8-Bit-CFB auf 1 festgelegt. Wenn sie auf die Blockgröße in Bytes festgelegt wird, wird cfb für vollständige Blöcke verwendet. Für XTS-Schlüssel wird sie verwendet, um die Größe der XTS-Dateneinheit (üblicherweise 512 oder 4096) in Bytes festzulegen.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_MULTI_OBJECT_LENGTH"></span><span id="bcrypt_multi_object_length"></span>**BCRYPT \_ MULTI \_ OBJECT \_ LENGTH**
</dt> <dd> <dl> <dt>

L"MultiObjectLength"
</dt> <dt>



Diese Eigenschaft gibt eine [**BCRYPT \_ MULTI OBJECT \_ \_ \_ LENGTH-STRUKTUR**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_multi_object_length_struct)zurück, die Informationen enthält, die zum Berechnen der Größe eines Objektpuffers erforderlich sind. Diese Eigenschaft wird nur für Betriebssystemversionen unterstützt, die die [**BCryptCreateMultiHash-Funktion**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatemultihash) unterstützen.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_OBJECT_LENGTH"></span><span id="bcrypt_object_length"></span>**\_BCRYPT-OBJEKTLÄNGE \_**
</dt> <dd> <dl> <dt>

L"ObjectLength"
</dt> <dt>



Die Größe des Unterobjekts eines Anbieters in Bytes. Dieser Datentyp ist ein **DWORD-Datentyp.** Derzeit verwenden die Hash- und symmetrischen Verschlüsselungsalgorithmusanbieter vom Aufrufer zugeordnete Puffer, um ihre Unterobjekte zu speichern. Der Hashanbieter erfordert beispielsweise, dass Sie Arbeitsspeicher für das Hashobjekt zuordnen, das mit der [**BCryptCreateHash-Funktion**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) abgerufen wurde. Diese Eigenschaft stellt die Puffergröße für das -Objekt eines Anbieters bereit, sodass Sie Arbeitsspeicher für das vom Anbieter erstellte Objekt zuordnen können.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_PADDING_SCHEMES"></span><span id="bcrypt_padding_schemes"></span>**\_BCRYPT-AUFFÜLLUNGSSCHEMAS \_**
</dt> <dd> <dl> <dt>

L"PaddingSchemes"
</dt> <dt>



Stellt das Auffüllschema des RSA-Algorithmusanbieters dar. Dieser Datentyp ist ein **DWORD-Datentyp.** Dies kann einer der folgenden Werte sein.



| Bezeichner                             | Wert      | BESCHREIBUNG                                                |
|----------------------------------------|------------|------------------------------------------------------------|
| **VON BCRYPT \_ \_ UNTERSTÜTZTER \_ PAD-ROUTER**     | 0x00000001 | Der Anbieter unterstützt die vom Router hinzugefügte Auffüllung.         |
| **VON BCRYPT \_ UNTERSTÜTZTE \_ \_ PAD-PKCS1-ENC \_** | 0x00000002 | Der Anbieter unterstützt das PKCS1-Verschlüsselungsauffüllungsschema. |
| **VON BCRYPT \_ \_ UNTERSTÜTZTES PAD \_ PKCS1 \_ SIG** | 0x00000004 | Der Anbieter unterstützt das PKCS1-Signaturauffüllungsschema.  |
| **VON BCRYPT \_ UNTERSTÜTZTER \_ \_ PAD-OAEP**       | 0x00000008 | Der Anbieter unterstützt das OAEP-Auffüllschema.             |
| **VON BCRYPT \_ UNTERSTÜTZTE \_ \_ PAD-PSS**        | 0x00000010 | Der Anbieter unterstützt das PSS-Auffüllschema.              |



 


</dt> </dl> </dd> <dt>

<span id="BCRYPT_PROVIDER_HANDLE"></span><span id="bcrypt_provider_handle"></span>**\_ \_ BCRYPT-ANBIETERHANDLE**
</dt> <dd> <dl> <dt>

L"ProviderHandle"
</dt> <dt>



Das Handle des CNG-Anbieters, der das im *hObject-Parameter* übergebene Objekt erstellt hat. Dieser Datentyp ist ein **\_ BCRYPT-ALG-HANDLE. \_** Diese Eigenschaft kann nur abgerufen werden. sie kann nicht festgelegt werden.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_SIGNATURE_LENGTH"></span><span id="bcrypt_signature_length"></span>**BCRYPT \_ SIGNATURE \_ LENGTH**
</dt> <dd> <dl> <dt>

L"SignatureLength"
</dt> <dt>



Die Größe einer Signatur für einen Schlüssel in Bytes. Dieser Datentyp ist ein **DWORD-Datentyp.** Diese Eigenschaft gilt nur für Schlüssel. Diese Eigenschaft kann nur abgerufen werden. sie kann nicht festgelegt werden.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Bcrypt.h</dt> </dl> |



 

