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
# <a name="cryptography-primitive-property-identifiers"></a>Kryptografieprimitive-Eigenschaften Bezeichner

Die folgenden Werte werden mit den Funktionen [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) und [**BCryptSetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetproperty) verwendet, um eine Eigenschaft zu identifizieren.

<dl> <dt>

<span id="BCRYPT_ALGORITHM_NAME"></span><span id="bcrypt_algorithm_name"></span>**bcrypt \_ - \_ Algorithmusname**
</dt> <dd> <dl> <dt>

L "algorithmName"
</dt> <dt>



Eine NULL-terminierte Unicode-Zeichenfolge, die den Namen des Algorithmus enthält.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_AUTH_TAG_LENGTH"></span><span id="bcrypt_auth_tag_length"></span>**bcrypt \_ auth \_ - \_ Taglänge**
</dt> <dd> <dl> <dt>

L "authtaglength"
</dt> <dt>



Die vom Algorithmus unterstützten authentifizierungstag Längen. Diese Eigenschaft ist eine [**bcrypt \_ auth \_ - \_ taglängen \_**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_key_lengths_struct) Struktur Struktur. Diese Eigenschaft gilt nur für Algorithmen.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_BLOCK_LENGTH"></span><span id="bcrypt_block_length"></span>**bcrypt- \_ Block \_ Länge**
</dt> <dd> <dl> <dt>

L "blocklength"
</dt> <dt>



Die Größe eines Chiffre Blocks für den Algorithmus in Byte. Diese Eigenschaft gilt nur für Blockverschlüsselungsalgorithmen. Bei diesem Datentyp handelt es sich um ein **DWORD**.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_BLOCK_SIZE_LIST"></span><span id="bcrypt_block_size_list"></span>**bcrypt- \_ Block \_ Größen \_ Liste**
</dt> <dd> <dl> <dt>

L "blocksizelist"
</dt> <dt>



Eine Liste der Block Längen, die von einem Verschlüsselungsalgorithmus unterstützt werden. Dieser Datentyp ist ein Array von **DWords**. Die Anzahl der Elemente im Array kann bestimmt werden, indem die Anzahl der Bytes geteilt wird, die durch die Größe eines einzelnen **DWORD** abgerufen werden.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_CHAINING_MODE"></span><span id="bcrypt_chaining_mode"></span>**bcrypt- \_ Verkettungs \_ Modus**
</dt> <dd> <dl> <dt>

L "chainingmode"
</dt> <dt>



Ein Zeiger auf eine NULL-terminierte Unicode-Zeichenfolge, die den Verkettungs Modus des Verschlüsselungsalgorithmus darstellt. Diese Eigenschaft kann für ein algorithmushandle oder ein Schlüssel Handle auf einen der folgenden Werte festgelegt werden.



| Bezeichner                   | Wert                         | BESCHREIBUNG                                                                                                                                                                    |
|------------------------------|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **bcrypt- \_ Ketten \_ Modus ( \_ CBC)** | L "chainingmudecbc"<br/> | Legt den Verkettungs Modus des Algorithmus auf [*Chiffre Block Verkettung*](/windows/desktop/SecGloss/c-gly)fest.<br/>            |
| **bcrypt- \_ Ketten \_ Modus- \_ ccm** | L "chainingmodeccm"<br/> | Legt den Verkettungs Modus des Algorithmus auf Counter mit dem CBC-MAC-Modus (CCM) fest. **Windows Vista:** Dieser Wert wird ab Windows Vista mit SP1 unterstützt.<br/> <br/> |
| **bcrypt- \_ Ketten \_ Modus ( \_ CFB)** | L "chainingmudecfb"<br/> | Legt den Verkettungs Modus des Algorithmus auf [*Chiffre Feedback*](/windows/desktop/SecGloss/c-gly)fest.<br/>                              |
| **bcrypt- \_ Ketten \_ Modus- \_ ECB** | L "chainingmodeecb"<br/> | Legt den Verkettungs Modus des Algorithmus auf [*elektronisches Codebook*](/windows/desktop/SecGloss/e-gly)fest.<br/>                  |
| **bcrypt- \_ Ketten \_ Modus- \_ GCM** | L "chainingmodegcm"<br/> | Legt den Verkettungs Modus des Algorithmus auf den Galois/Counter-Modus (GCM) fest. **Windows Vista:** Dieser Wert wird ab Windows Vista mit SP1 unterstützt.<br/> <br/>       |
| **bcrypt- \_ Ketten \_ Modus- \_ na**  | L "chainingmoden/A"<br/> | Der Algorithmus unterstützt keine Verkettung.<br/>                                                                                                                            |



 


</dt> </dl> </dd> <dt>

<span id="BCRYPT_DH_PARAMETERS"></span><span id="bcrypt_dh_parameters"></span>**bcrypt \_ dh- \_ Parameter**
</dt> <dd> <dl> <dt>

L "dhparameters"
</dt> <dt>



Gibt Parameter an, die mit einem Diffie-Hellman Schlüssel verwendet werden sollen. Dieser Datentyp ist ein Zeiger auf eine [**bcrypt \_ dh- \_ Parameter \_ Header**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_parameter_header) Struktur. Diese Eigenschaft kann nur festgelegt werden und muss für den Schlüssel festgelegt werden, bevor der Schlüssel abgeschlossen ist.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_DSA_PARAMETERS"></span><span id="bcrypt_dsa_parameters"></span>**bcrypt- \_ DSA- \_ Parameter**
</dt> <dd> <dl> <dt>

L "DSAParameters"
</dt> <dt>



Gibt Parameter an, die mit einem DSA-Schlüssel verwendet werden sollen. Diese Eigenschaft ist ein [**bcrypt \_ DSA- \_ Parameter \_ Header**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header) oder eine [**bcrypt DSA- \_ \_ Parameter Header- \_ \_ v2**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header_v2) -Struktur. Diese Eigenschaft kann nur festgelegt werden und muss für den Schlüssel festgelegt werden, bevor der Schlüssel abgeschlossen ist.

**Windows 8:** Ab Windows 8 kann diese Eigenschaft eine [**bcrypt \_ DSA- \_ Parameter Header- \_ \_ v2**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header_v2) -Struktur sein. Verwenden Sie diese Struktur, wenn die Schlüsselgröße 1024 Bits überschreitet und kleiner oder gleich 3072 Bits ist. Wenn die Schlüsselgröße größer oder gleich 512, aber kleiner oder gleich 1024 Bits ist, verwenden Sie die Struktur des [**bcrypt \_ DSA- \_ Parameter \_ Headers**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header) .


</dt> </dl> </dd> <dt>

<span id="BCRYPT_EFFECTIVE_KEY_LENGTH"></span><span id="bcrypt_effective_key_length"></span>**effektive bcrypt- \_ \_ Schlüssel \_ Länge**
</dt> <dd> <dl> <dt>

L "effectivekeylength"
</dt> <dt>



Die Größe der effektiven Länge eines RC2-Schlüssels in Bits. Bei diesem Datentyp handelt es sich um ein **DWORD**.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_HASH_BLOCK_LENGTH"></span><span id="bcrypt_hash_block_length"></span>**bcrypt- \_ Hash \_ Block \_ Länge**
</dt> <dd> <dl> <dt>

L "hashblock length"
</dt> <dt>



Die Größe (in Bytes) des Blocks für einen Hash. Diese Eigenschaft gilt nur für Hash Algorithmen. Bei diesem Datentyp handelt es sich um ein **DWORD**.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_HASH_LENGTH"></span><span id="bcrypt_hash_length"></span>**bcrypt \_ - \_ Hashlänge**
</dt> <dd> <dl> <dt>

L "hashdigestlength"
</dt> <dt>



Die Größe (in Bytes) des Hashwerts eines Hash Anbieters. Bei diesem Datentyp handelt es sich um ein **DWORD**.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_HASH_OID_LIST"></span><span id="bcrypt_hash_oid_list"></span>**bcrypt- \_ Hash- \_ OID- \_ Liste**
</dt> <dd> <dl> <dt>

L "hashuidlist"
</dt> <dt>



Die Liste der von [*der*](/windows/desktop/SecGloss/d-gly)-codierten Hash [*Objekt*](/windows/desktop/SecGloss/o-gly) -IDs (OIDs). Diese Eigenschaft ist eine [**bcrypt- \_ OID- \_ Listen**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_oid_list) Struktur. Diese Eigenschaft kann nur gelesen werden.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_INITIALIZATION_VECTOR"></span><span id="bcrypt_initialization_vector"></span>**bcrypt- \_ Initialisierungs \_ Vektor**
</dt> <dd> <dl> <dt>

L "IV"
</dt> <dt>



Enthält den [*Initialisierungs Vektor*](/windows/desktop/SecGloss/i-gly) (IV) für einen Schlüssel. Diese Eigenschaft gilt nur für Schlüssel.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_KEY_LENGTH"></span><span id="bcrypt_key_length"></span>**bcrypt- \_ Schlüssel \_ Länge**
</dt> <dd> <dl> <dt>

L "keylength"
</dt> <dt>



Die Größe des Schlüssel Werts eines symmetrischen Schlüssel Anbieters in Bits. Bei diesem Datentyp handelt es sich um ein **DWORD**.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_KEY_LENGTHS"></span><span id="bcrypt_key_lengths"></span>**bcrypt- \_ Schlüssel \_ Längen**
</dt> <dd> <dl> <dt>

L "keylängen"
</dt> <dt>



Die vom Algorithmus unterstützten Schlüssellängen. Diese Eigenschaft ist eine Struktur der [**bcrypt- \_ Schlüssel \_ Längen \_**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_key_lengths_struct) Struktur. Diese Eigenschaft gilt nur für Algorithmen.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_KEY_OBJECT_LENGTH"></span><span id="bcrypt_key_object_length"></span>**bcrypt- \_ Schlüssel \_ Objekt \_ Länge**
</dt> <dd> <dl> <dt>

L "keyobjectlength"
</dt> <dt>



Diese Eigenschaft wird nicht verwendet. Die Eigenschaft **bcrypt- \_ Objekt \_ Länge** wird verwendet, um diese Informationen zu erhalten.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_KEY_STRENGTH"></span><span id="bcrypt_key_strength"></span>**bcrypt- \_ Schlüssel \_ Stärke**
</dt> <dd> <dl> <dt>

L "keystärke"
</dt> <dt>



Die Anzahl der Bits im Schlüssel. Bei diesem Datentyp handelt es sich um ein **DWORD**. Diese Eigenschaft gilt nur für Schlüssel.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_MESSAGE_BLOCK_LENGTH"></span><span id="bcrypt_message_block_length"></span>**bcrypt- \_ Nachrichten \_ Block \_ Länge**
</dt> <dd> <dl> <dt>

L "messageblocklength"
</dt> <dt>



Dies kann für jedes Schlüssel handle festgelegt werden, für das der CFB-Verkettungs Modus festgelegt wurde. Standardmäßig ist diese Eigenschaft für 8-Bit-CFB auf 1 festgelegt. Das Festlegen auf die Blockgröße in Bytes bewirkt, dass der CFB-vollblock verwendet wird. Bei XTS-Schlüsseln wird diese verwendet, um die Größe der XTS-Dateneinheit (in der Regel 512 oder 4096) in Byte festzulegen.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_MULTI_OBJECT_LENGTH"></span><span id="bcrypt_multi_object_length"></span>**bcrypt \_ - \_ multiobjektlänge \_**
</dt> <dd> <dl> <dt>

L "multiobjectlength"
</dt> <dt>



Diese Eigenschaft gibt eine [**bcrypt- \_ Struktur mit mehreren \_ Objekt \_ Längen \_**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_multi_object_length_struct)zurück, die erforderliche Informationen zum Berechnen der Größe eines Objekt Puffers enthält. Diese Eigenschaft wird nur für Betriebssystemversionen unterstützt, die die Funktion " [**bcryptkreatemultihash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatemultihash) " unterstützen.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_OBJECT_LENGTH"></span><span id="bcrypt_object_length"></span>**bcrypt- \_ Objekt \_ Länge**
</dt> <dd> <dl> <dt>

L "objectlength"
</dt> <dt>



Die Größe (in Bytes) des untergeordneten Objekts eines Anbieters. Bei diesem Datentyp handelt es sich um ein **DWORD**. Derzeit verwenden die Anbieter von Hash-und symmetrischen Chiffre Algorithmen zum Speichern Ihrer unter Objekte die vom Aufrufer zugewiesenen Puffer. Beispielsweise erfordert der Hash Anbieter, dass Sie Speicher für das Hash Objekt belegen, das mit der Funktion " [**bcryptkreatehash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) " abgerufen wurde. Diese Eigenschaft stellt die Puffergröße für das-Objekt eines Anbieters bereit, sodass Sie Speicher für das vom Anbieter erstellte Objekt zuweisen können.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_PADDING_SCHEMES"></span><span id="bcrypt_padding_schemes"></span>**bcrypt- \_ \_ Paddingschemas**
</dt> <dd> <dl> <dt>

L "Paddingschemas"
</dt> <dt>



Stellt das Auffüll Schema des RSA-Algorithmus-Anbieters dar. Bei diesem Datentyp handelt es sich um ein **DWORD**. Dies kann einer der folgenden Werte sein:



| Bezeichner                             | Wert      | BESCHREIBUNG                                                |
|----------------------------------------|------------|------------------------------------------------------------|
| **bcrypt- \_ unterstützter Auffüll \_ \_ Router**     | 0x00000001 | Der Anbieter unterstützt die durch den Router hinzugefügten Auffüll Zeichen.         |
| **Unterstützte bcrypt- \_ \_ Pad \_ PKCS1 \_** | 0x00000002 | Der Anbieter unterstützt das PKCS1 Encryption Auffüllung Schema. |
| **Unterstützte bcrypt- \_ \_ Pad \_ PKCS1 \_ sig** | 0x00000004 | Der Anbieter unterstützt das Auffüll Schema der PKCS1-Signatur.  |
| **bcrypt \_ unterstützte \_ Pad \_ OAEP**       | 0x00000008 | Der Anbieter unterstützt das OAEP-Auffüll Schema.             |
| **bcrypt \_ unterstützte \_ Pad- \_ PSS**        | 0x00000010 | Der Anbieter unterstützt das PSS-Auffüll Schema.              |



 


</dt> </dl> </dd> <dt>

<span id="BCRYPT_PROVIDER_HANDLE"></span><span id="bcrypt_provider_handle"></span>**bcrypt- \_ Anbieter \_ handle**
</dt> <dd> <dl> <dt>

L "ProviderHandle"
</dt> <dt>



Das Handle des CNG-Anbieters, von dem das Objekt erstellt wurde, das im *hobject* -Parameter übergeben wurde. Dieser Datentyp ist ein **bcrypt- \_ ALG- \_ handle**. Diese Eigenschaft kann nur abgerufen werden. der Wert kann nicht festgelegt werden.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_SIGNATURE_LENGTH"></span><span id="bcrypt_signature_length"></span>**bcrypt- \_ Signatur \_ Länge**
</dt> <dd> <dl> <dt>

L "SignatureLength"
</dt> <dt>



Die Größe (in Bytes) der Länge einer Signatur für einen Schlüssel. Bei diesem Datentyp handelt es sich um ein **DWORD**. Diese Eigenschaft gilt nur für Schlüssel. Diese Eigenschaft kann nur abgerufen werden. der Wert kann nicht festgelegt werden.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Bcrypt. h</dt> </dl> |



 

