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
# <a name="key-storage-property-identifiers"></a>Schlüsselspeicher-Eigenschaften Bezeichner

Die folgenden Werte werden verwendet, um eine Key Storage-Eigenschaft zu identifizieren.

<dl> <dt>

<span id="NCRYPT_ALGORITHM_GROUP_PROPERTY"></span><span id="ncrypt_algorithm_group_property"></span>**ncrypt \_ - \_ \_ algorithmusgruppeneigenschaft**
</dt> <dd> <dl> <dt>

L "Algorithmusgruppe"
</dt> <dt>



Eine NULL-terminierte Unicode-Zeichenfolge, die den Namen der Algorithmusgruppe des Objekts enthält. Diese Eigenschaft gilt nur für Schlüssel. Die folgenden Bezeichner werden vom Microsoft-Schlüsselspeicher Anbieter zurückgegeben.



| Bezeichner                                     | Wert              | BESCHREIBUNG                                                   |
|------------------------------------------------|--------------------|---------------------------------------------------------------|
| **ncrypt \_ RSA \_ - \_ Algorithmusgruppe**<br/>   | RSA<br/>   | Die RSA-Algorithmusgruppe.<br/>                           |
| **ncrypt \_ dh \_ - \_ Algorithmusgruppe**<br/>    | Nenden<br/>    | Die Diffie-Hellman Algorithmusgruppe.<br/>                |
| **ncrypt \_ DSA \_ - \_ Algorithmusgruppe**<br/>   | DSA<br/>   | Die DSA-Algorithmusgruppe.<br/>                           |
| **ncrypt \_ ECDSA \_ - \_ Algorithmusgruppe**<br/> | ECDsa<br/> | Die DSA-Algorithmusgruppe für die elliptische Kurve.<br/>            |
| **ncrypt \_ ECDH \_ - \_ Algorithmusgruppe**<br/>  | "ECDH"<br/>  | Die elliptische Kurve Diffie-Hellman Algorithmusgruppe.<br/> |



 


</dt> </dl> </dd> <dt>

<span id="NCRYPT_ALGORITHM_PROPERTY"></span><span id="ncrypt_algorithm_property"></span>**ncrypt \_ - \_ algorithmuseigenschaft**
</dt> <dd> <dl> <dt>

L "Algorithmusname"
</dt> <dt>



Eine NULL-terminierte Unicode-Zeichenfolge, die den Namen des Algorithmus des-Objekts enthält. Hierbei kann es sich um einen vordefinierten [**CNG-Algorithmusbezeichner**](cng-algorithm-identifiers.md) oder einen anderen registrierten Algorithmusbezeichner handeln. Diese Eigenschaft gilt nur für Schlüssel.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_ASSOCIATED_ECDH_KEY"></span><span id="ncrypt_associated_ecdh_key"></span>**ncrypt zugeordneter \_ \_ ECDH- \_ Schlüssel**
</dt> <dd> <dl> <dt>

L "smartcardassociatedecdhkey"
</dt> <dt>



Ein **LPWSTR** -Wert, der den Container Namen des ECDH-Schlüssels (Elliptic Curve Diffie-Hellman) angibt, der während der Anmeldung für ein angegebenes Handle eines ECDSA (Elliptic Curve Digital Signature)-Schlüssels verwendet werden soll. Wenn keine ECDH-Schlüssel auf der Karte vorhanden sind, gibt der [*Schlüsselspeicher Anbieter*](/windows/desktop/SecGloss/k-gly) (KSP) die Rückgabe **\_ nicht \_ gefunden** zurück. Diese Eigenschaft gilt für ECDSA-Schlüssel für die Anmeldung mit Smartcards. Die-Eigenschaft wird vom Microsoft-Smartcard-Schlüsselspeicher Anbieter und nicht vom Microsoft-Software Schlüsselspeicher-Anbieter unterstützt.

**Windows Server 2008 und Windows Vista:** Dieser Wert wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_BLOCK_LENGTH_PROPERTY"></span><span id="ncrypt_block_length_property"></span>**ncrypt- \_ Block \_ Längen \_ Eigenschaft**
</dt> <dd> <dl> <dt>

L "Block Länge"
</dt> <dt>



Ein **DWORD** -Wert, der die Länge des Verschlüsselungs Blocks in Bytes enthält. Diese Eigenschaft gilt nur für Schlüssel, die die Verschlüsselung unterstützen.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_CERTIFICATE_PROPERTY"></span><span id="ncrypt_certificate_property"></span>**ncrypt- \_ Zertifikat \_ Eigenschaft**
</dt> <dd> <dl> <dt>

L "smartcardkeycertificate"
</dt> <dt>



Ein [*BLOB*](/windows/desktop/SecGloss/b-gly) , das ein X. 509-Zertifikat enthält, das dem Schlüssel zugeordnet ist.

**Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista:** Ein [*BLOB*](/windows/desktop/SecGloss/b-gly) , das das [*Smartcard*](/windows/desktop/SecGloss/s-gly) -Schlüssel [*Zertifikat*](/windows/desktop/SecGloss/c-gly)enthält. Diese Eigenschaft wird vom Microsoft-Software Schlüsselspeicher-Anbieter nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_DH_PARAMETERS_PROPERTY"></span><span id="ncrypt_dh_parameters_property"></span>**ncrypt \_ dh- \_ Parameter ( \_ Eigenschaft)**
</dt> <dd> <dl> <dt>

L "dhparameters"
</dt> <dt>



Gibt Parameter an, die mit einem Diffie-Hellman Schlüssel verwendet werden sollen. Dieser Datentyp ist ein Zeiger auf eine [**bcrypt \_ dh- \_ Parameter \_ Header**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_parameter_header) Struktur. Diese Eigenschaft kann nur festgelegt werden und muss für den Schlüssel festgelegt werden, bevor der Schlüssel abgeschlossen ist.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_EXPORT_POLICY_PROPERTY"></span><span id="ncrypt_export_policy_property"></span>**ncrypt- \_ Export \_ Richtlinien \_ Eigenschaft**
</dt> <dd> <dl> <dt>

L "Richtlinie exportieren"
</dt> <dt>



Ein **DWORD** , das einen Satz von Flags enthält, die die Export Richtlinie für einen persistenten Schlüssel angeben. Diese Eigenschaft gilt nur für Schlüssel. Diese kann NULL oder eine Kombination aus einem oder mehreren der folgenden Werte enthalten.



| Bezeichner                                    | Wert      | BESCHREIBUNG                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ncrypt \_ Allow \_ - \_ exportflag**               | 0x00000001 | Der private Schlüssel kann exportiert werden.                                                                                                                                                                                                                                                                                 |
| **ncrypt, nur-Text- \_ Export Kennzeichen zulassen \_ \_ \_**    | 0x00000002 | Der private Schlüssel kann im Klartext-Format exportiert werden.                                                                                                                                                                                                                                                               |
| **ncrypt \_ - \_ Flag zum Archivieren zulassen \_**            | 0x00000004 | Der private Schlüssel kann für Archivierungszwecke einmal exportiert werden. Dieses Flag gilt nur für den ursprünglichen Schlüssel handle, für den es festgelegt wurde. Diese Richtlinie kann nur auf das ursprüngliche Schlüssel handle angewendet werden. Nachdem das Schlüssel Handle geschlossen wurde, kann der Schlüssel nicht mehr zu Archivierungszwecken exportiert werden.                   |
| **ncrypt \_ - \_ Flag zum Archivieren von Klartext zulassen \_ \_** | 0x00000008 | Der private Schlüssel kann für Archivierungszwecke einmal im Klartext-Format exportiert werden. Dieses Flag gilt nur für den ursprünglichen Schlüssel handle, für den es festgelegt wurde. Diese Richtlinie kann nur auf das ursprüngliche Schlüssel handle angewendet werden. Nachdem das Schlüssel Handle geschlossen wurde, kann der Schlüssel nicht mehr zu Archivierungszwecken exportiert werden. |



 


</dt> </dl> </dd> <dt>

<span id="NCRYPT_IMPL_TYPE_PROPERTY"></span><span id="ncrypt_impl_type_property"></span>**ncrypt \_ impl \_ Type ( \_ Eigenschaft)**
</dt> <dd> <dl> <dt>

L "Impl Type"
</dt> <dt>



Ein **DWORD** -Wert, der einen Satz von Flags enthält, die Implementierungsdetails des Anbieters definieren. Diese Eigenschaft gilt nur für Schlüsselspeicher Anbieter. Diese kann NULL oder eine Kombination aus einem oder mehreren der folgenden Werte enthalten.



| Bezeichner                            | Wert      | BESCHREIBUNG                                               |
|---------------------------------------|------------|-----------------------------------------------------------|
| **ncrypt \_ impl- \_ hardwareflag \_**      | 0x00000001 | Der Anbieter ist Hardware basiert.                           |
| **ncrypt \_ impl \_ - \_ softwareflag**      | 0x00000002 | Der Anbieter ist Software basiert.                           |
| **ncrypt \_ impl-Wechsel \_ \_ Flag**     | 0x00000008 | Der Anbieter ist austauschbar.                                |
| **RNG-Flag für NCrypt \_ impl- \_ Hardware \_ \_** | 0x00000010 | Der Anbieter ist ein hardwarebasierter Zufallszahlengenerator. |



 


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_TYPE_PROPERTY"></span><span id="ncrypt_key_type_property"></span>**ncrypt \_ - \_ Schlüsseltyp \_ Eigenschaft**
</dt> <dd> <dl> <dt>

L "Schlüsseltyp"
</dt> <dt>



Ein **DWORD** , das einen Satz von Flags enthält, die den Schlüsseltyp definieren. Diese Eigenschaft gilt nur für Schlüssel. Dieser Wert kann NULL oder den folgenden Wert enthalten.



| Bezeichner                     | Wert      | BESCHREIBUNG                                                                                              |
|--------------------------------|------------|----------------------------------------------------------------------------------------------------------|
| **ncrypt \_ - \_ computerschlüsselflag \_** | 0x00000001 | Der Schlüssel gilt für den lokalen Computer. Wenn dieses Flag nicht vorhanden ist, gilt der Schlüssel für den aktuellen Benutzer. |



 


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_USAGE_PROPERTY"></span><span id="ncrypt_key_usage_property"></span>**ncrypt- \_ Schlüssel \_ Verwendungs \_ Eigenschaft**
</dt> <dd> <dl> <dt>

L "Schlüssel Verwendung"
</dt> <dt>



Ein **DWORD** -Wert, der einen Satz von Flags enthält, mit denen die Verwendungs Details für einen Schlüssel definiert werden. Diese Eigenschaft gilt nur für Schlüssel. Diese kann NULL oder eine Kombination aus einem oder mehreren der folgenden Werte enthalten.



| Bezeichner                              | Wert      | BESCHREIBUNG                                          |
|-----------------------------------------|------------|------------------------------------------------------|
| **ncrypt \_ ' \_ entschlüsselungsflag zulassen ' \_**        | 0x00000001 | Der Schlüssel kann für die Entschlüsselung verwendet werden.                  |
| **ncrypt \_ - \_ Flag zum Signieren zulassen \_**        | 0x00000002 | Der Schlüssel kann zum Signieren verwendet werden.                     |
| **ncrypt- \_ Flag zum gewähren der \_ Schlüssel \_ Vereinbarung \_** | 0x00000004 | Der Schlüssel kann für die Verschlüsselung von geheimen Schlüsseln verwendet werden. |
| **ncrypt \_ \_ alle \_ Verwendungszwecke zulassen**          | 0x00ffffff | Der Schlüssel kann für beliebige Zwecke verwendet werden.                 |



 


</dt> </dl> </dd> <dt>

<span id="NCRYPT_LAST_MODIFIED_PROPERTY"></span><span id="ncrypt_last_modified_property"></span>**ncrypt- \_ Eigenschaft "zuletzt \_ geändert" \_**
</dt> <dd> <dl> <dt>

L "geändert"
</dt> <dt>



Gibt an, wann der Schlüssel zuletzt geändert wurde. Dieser Datentyp ist ein Zeiger auf eine [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) -Struktur. Diese Eigenschaft gilt nur für persistente Schlüssel.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_LENGTH_PROPERTY"></span><span id="ncrypt_length_property"></span>**ncrypt \_ length ( \_ Eigenschaft)**
</dt> <dd> <dl> <dt>

L "Länge"
</dt> <dt>



Ein **DWORD** , das die Länge des Schlüssels in Bits enthält. Diese Eigenschaft gilt nur für Schlüssel.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_LENGTHS_PROPERTY"></span><span id="ncrypt_lengths_property"></span>**ncrypt- \_ Längen \_ Eigenschaft**
</dt> <dd> <dl> <dt>

L "Längen"
</dt> <dt>



Gibt die Schlüsselgrößen an, die vom Schlüssel unterstützt werden. Dieser Datentyp ist ein Zeiger auf eine [**NCrypt- \_ unterstützte \_ Längen**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncrypt_supported_lengths) Struktur, die diese Informationen enthält. Diese Eigenschaft gilt nur für Schlüssel.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_MAX_NAME_LENGTH_PROPERTY"></span><span id="ncrypt_max_name_length_property"></span>**maximale NCrypt- \_ \_ namens \_ Länge ( \_ Eigenschaft)**
</dt> <dd> <dl> <dt>

L "maximale namens Länge"
</dt> <dt>



Ein **DWORD** , das die maximale Länge (in Zeichen) des Namens eines permanenten Schlüssels enthält. Diese Eigenschaft gilt nur für einen Anbieter.

Diese Eigenschaft ist in erster Linie für die Verwendung durch Schlüsselspeicher Anbieter vorgesehen, die Ihre Schlüssel auf einem Gerät speichern, das nur über eine begrenzte Menge an verfügbarem Arbeitsspeicher verfügt, z. b. eine Smartcard.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_NAME_PROPERTY"></span><span id="ncrypt_name_property"></span>**ncrypt- \_ Name ( \_ Eigenschaft)**
</dt> <dd> <dl> <dt>

L "Name"
</dt> <dt>



Ein Zeiger auf eine NULL-terminierte Unicode-Zeichenfolge, die den Namen des-Objekts enthält.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_PIN_PROMPT_PROPERTY"></span><span id="ncrypt_pin_prompt_property"></span>**ncrypt \_ PIN-Eingabe Aufforderungs \_ \_ Eigenschaft**
</dt> <dd> <dl> <dt>

L "smartcardpinprompt"
</dt> <dt>



Dieser Wert wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_PIN_PROPERTY"></span><span id="ncrypt_pin_property"></span>**ncrypt- \_ Pin- \_ Eigenschaft**
</dt> <dd> <dl> <dt>

L "Smartcardpin"
</dt> <dt>



Ein Zeiger auf eine NULL-terminierte Unicode-Zeichenfolge, die die PIN enthält. Die PIN wird für einen Smartcardschlüssel oder das Kennwort für einen Kenn Wort geschützten Schlüssel verwendet, der in einem softwarebasierten KSP gespeichert ist. Diese Eigenschaft kann nur festgelegt werden. Der Wert wird von Microsoft-kSPS zwischengespeichert, sodass der Benutzer nur einmal pro Prozess aufgefordert wird.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_PROVIDER_HANDLE_PROPERTY"></span><span id="ncrypt_provider_handle_property"></span>**ncrypt- \_ Anbieter \_ handle ( \_ Eigenschaft)**
</dt> <dd> <dl> <dt>

L "Anbieter Handle"
</dt> <dt>



Ein **NCrypt- \_ Prov- \_ handle** , das das Handle des CNG-Schlüsselspeicher Anbieters enthält. Wenn Sie mit der Verwendung des Handles fertig sind, müssen Sie [**ncryptfreobject**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptfreeobject) aufrufen, um es freizugeben.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_READER_PROPERTY"></span><span id="ncrypt_reader_property"></span>**ncrypt- \_ Reader- \_ Eigenschaft**
</dt> <dd> <dl> <dt>

L "smartcardreader"
</dt> <dt>



Ein Zeiger auf eine NULL-terminierte Unicode-Zeichenfolge, die den Namen des smartcardreaders enthält. Diese Eigenschaft kann nur festgelegt werden.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_ROOT_CERTSTORE_PROPERTY"></span><span id="ncrypt_root_certstore_property"></span>**ncrypt-Stamm \_ \_ Eigenschaft "certstore" \_**
</dt> <dd> <dl> <dt>

L "smartcardrootcertstore"
</dt> <dt>



Ein **HCERTSTORE** , der den Zertifikat Speicher der Smartcard darstellt.


</dt> </dl> </dd> <dt>

<span id="_NCRYPT_SCARD_PIN_ID"></span><span id="_ncrypt_scard_pin_id"></span>**NCrypt \_ Card- \_ Pin- \_ ID**
</dt> <dd> <dl> <dt>

L "smartcardpinid"
</dt> <dt>



Ein Zeiger auf den **Pin- \_ ID** -Wert, der einem bestimmten [*Kryptografieschlüssel*](/windows/desktop/SecGloss/c-gly) auf einer [*Smartcard*](/windows/desktop/SecGloss/s-gly)zugeordnet ist. Dies ist eine schreibgeschützte Eigenschaft. Der Datentyp der **Pin- \_ ID** ist in cardmod. h definiert.

**Windows Server 2008 und Windows Vista:** Dieser Wert wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_SCARD_PIN_INFO"></span><span id="ncrypt_scard_pin_info"></span>**ncrypt-anheft \_ \_ \_ Informationen**
</dt> <dd> <dl> <dt>

L "smartcardpininfo"
</dt> <dt>



Ein Zeiger auf [**die \_ Info**](/windows/desktop/api/mbnapi/ns-mbnapi-mbn_pin_info) -Struktur der PIN, die einem bestimmten Kryptografieschlüssel auf der Smartcard zugeordnet ist. Der Aufrufer stellt das Schlüssel Handle bereit. Diese Eigenschaft ist schreibgeschützt. Die **Pin- \_ Informations** Struktur ist in cardmod. h definiert.

**Windows Server 2008 und Windows Vista:** Dieser Wert wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_SECURE_PIN_PROPERTY"></span><span id="ncrypt_secure_pin_property"></span>**ncrypt \_ Secure \_ PIN ( \_ Eigenschaft)**
</dt> <dd> <dl> <dt>

L "smartcardsecurepin"
</dt> <dt>



Ein Zeiger auf eine NULL-terminierte Unicode-Zeichenfolge, die die PIN der Smartcard-Sitzung enthält. Diese Eigenschaft kann nur festgelegt werden.

**Windows Vista:** Diese Eigenschaft wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_SECURITY_DESCR_PROPERTY"></span><span id="ncrypt_security_descr_property"></span>**ncrypt \_ Security \_ descr ( \_ Eigenschaft)**
</dt> <dd> <dl> <dt>

L "Sicherheit-descr"
</dt> <dt>



Ein Zeiger auf eine [**Sicherheits \_ deskriptorstruktur**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) , die Zugriffs Steuerungsinformationen für den Schlüssel enthält. Diese Eigenschaft gilt nur für persistente Schlüssel. Der *dwFlags* -Parameter der [**ncryptgetproperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) -oder [**ncryptsetproperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty) -Funktion identifiziert den Teil der Sicherheits Beschreibung, der abgerufen oder festgelegt werden soll.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_SECURITY_DESCR_SUPPORT_PROPERTY"></span><span id="ncrypt_security_descr_support_property"></span>**ncrypt \_ Security \_ descr \_ Support ( \_ Eigenschaft)**
</dt> <dd> <dl> <dt>

L "Unterstützung der Sicherheits Abstützung"
</dt> <dt>



Gibt an, ob der Anbieter Sicherheits Deskriptoren für Schlüssel unterstützt. Diese Eigenschaft ist ein **DWORD** , das 1 enthält, wenn der Anbieter Sicherheits Deskriptoren für Schlüssel unterstützt. Wenn diese Eigenschaft einen anderen Wert enthält oder wenn die [**ncryptgetproperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) -Funktion den Wert "" **\_ nicht \_ unterstützt** zurückgibt, unterstützt der Anbieter keine Sicherheits Deskriptoren für Schlüssel. Diese Eigenschaft gilt nur für-Anbieter.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_SMARTCARD_GUID_PROPERTY"></span><span id="ncrypt_smartcard_guid_property"></span>**ncrypt- \_ Smartcard- \_ GUID- \_ Eigenschaft**
</dt> <dd> <dl> <dt>

L "smartcardguid"
</dt> <dt>



Ein BLOB, das den Bezeichner der Smartcard enthält.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_UI_POLICY_PROPERTY"></span><span id="ncrypt_ui_policy_property"></span>**ncrypt- \_ UI- \_ Richtlinien \_ Eigenschaft**
</dt> <dd> <dl> <dt>

L "UI-Richtlinie"
</dt> <dt>



Bei Verwendung mit der [**ncryptsetproperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty) -Funktion oder der [**ncryptgetproperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) -Funktion handelt es sich hierbei um einen Zeiger auf eine [**NCrypt- \_ UI- \_ Richtlinien**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncrypt_ui_policy) Struktur, die die Richtlinie für die starke Schlüssel Benutzeroberfläche für den Schlüssel enthält. Diese Eigenschaft gilt nur für persistente Schlüssel. Diese Eigenschaft kann nur festgelegt werden, wenn der Schlüssel generiert wird. Nachdem die [**ncryptfinalizekey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptfinalizekey) -Funktion für diesen Schlüssel aufgerufen wurde, wird diese Eigenschaft schreibgeschützt.

Ein Schlüsselspeicher Anbieter kann diesen Parameter über eine [**ncryptsetpropertyfn**](https://www.bing.com/search?q=**NCryptSetPropertyFn**) -Rückruffunktion empfangen. Der Parameterwert ist eine NCrypt- \_ UI- \_ Richtlinien- \_ BLOB-Struktur, die die gleichen Informationen enthält. Wenn eine Anwendung eine Anforderung über ncryptsetpropertyfn an den Anbieter sendet, damit diese Eigenschaft zurückgegeben wird, wird davon ausgegangen, dass der Anbieter die \_ blobstruktur der NCrypt-UI- \_ Richtlinie zurückgibt \_ .


</dt> </dl> </dd> <dt>

<span id="NCRYPT_UNIQUE_NAME_PROPERTY"></span><span id="ncrypt_unique_name_property"></span>**eindeutige NCrypt- \_ \_ Name- \_ Eigenschaft**
</dt> <dd> <dl> <dt>

L "eindeutiger Name"
</dt> <dt>



Ein Zeiger auf eine NULL-terminierte Unicode-Zeichenfolge, die den eindeutigen Namen des-Objekts enthält. Dies ist ein alternativer Name, der beim Zugriff auf den Schlüssel verwendet werden kann. Diese Eigenschaft wird verwendet, wenn der Schlüssel Name, der ursprünglich an [**ncryptkreatepersistedkey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptcreatepersistedkey) übergeben wurde, nicht eindeutig genug ist, um den persistenten Schlüssel zuverlässig zu identifizieren. Der Microsoft-Schlüsselspeicher Anbieter gibt den Dateinamen des Schlüssels als diese Eigenschaft zurück.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_USE_CONTEXT_PROPERTY"></span><span id="ncrypt_use_context_property"></span>**ncrypt \_ - \_ Kontext \_ Eigenschaft verwenden**
</dt> <dd> <dl> <dt>

L "Kontext verwenden"
</dt> <dt>



Ein Zeiger auf eine NULL-terminierte Unicode-Zeichenfolge, die den Kontext des Vorgangs beschreibt. Diese Eigenschaft ist nicht persistent und kann entweder für einen Anbieter oder einen Schlüssel festgelegt werden. Ein Schlüssel hat keinen Zugriff auf die **NCrypt- \_ Eigenschaft \_ Kontext \_ Eigenschaft** des Anbieters, da die Eigenschaft nur für das Handle spezifisch ist, für das Sie festgelegt ist.

Ein Beispiel, in dem diese Eigenschaft im Kontext eines Anbieters verwendet wird, ist ein Schlüsselspeicher Anbieter, der den Benutzer während eines [**ncryptopenkey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) -Aufforderungs Aufforderungs (z. b. "Einfügen Ihrer Smartcard in den Reader") auffordern muss. Da das Schlüssel handle erst verfügbar ist, nachdem **ncryptopenkey** zurückgegeben wurde, sollte die Anwendung diese Eigenschaft für das Anbieter handle vor dem Aufrufen von **ncryptopenkey** festlegen.

Ein Beispiel für die Verwendung dieser Eigenschaft im Kontext eines Schlüssel Handles ist ein Schlüsselspeicher Anbieter, der den Benutzer während eines Vorgangs mithilfe des Schlüssels auffordern muss (z. b. "diese Anwendung muss diesen Schlüssel zum Signieren eines Dokuments verwenden"). Der Anbieter könnte diese Kontextinformationen dann an den Benutzer in jeder Benutzeroberfläche weiterleiten, die während des Vorgangs angezeigt wird.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_USE_COUNT_ENABLED_PROPERTY"></span><span id="ncrypt_use_count_enabled_property"></span>**ncrypt \_ - \_ Eigenschaft "Anzahl \_ aktivierte Elemente" \_**
</dt> <dd> <dl> <dt>

L "aktivierte Verwendungs Anzahl"
</dt> <dt>



Gibt an, ob der Anbieter die Verwendungs Zählung für Schlüssel unterstützt. Diese Eigenschaft ist ein **DWORD** -Wert, der 1 enthält, wenn der Anbieter die Verwendungs Zählung für Schlüssel unterstützt. Wenn diese Eigenschaft einen anderen Wert enthält oder wenn die [**ncryptgetproperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) -Funktion die Funktion "die Funktion wird **\_ nicht \_ unterstützt**" zurückgibt, unterstützt der Anbieter keine Verwendungs Zählung für Schlüssel. Diese Eigenschaft gilt nur für-Anbieter.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_USE_COUNT_PROPERTY"></span><span id="ncrypt_use_count_property"></span>**ncrypt, \_ Verwendung der \_ Count- \_ Eigenschaft**
</dt> <dd> <dl> <dt>

L "Verwendung der Anzahl"
</dt> <dt>



Eine [**\_ ganzzahlige ularge**](https://docs.microsoft.com/windows/win32/api/winnt/ns-winnt-ularge_integer~r1) -Variable, die die Anzahl der Vorgänge enthält, die der angegebene [*private Schlüssel*](/windows/desktop/SecGloss/p-gly) ausgeführt hat. Diese Eigenschaft ist optional und wird möglicherweise nicht von allen Anbietern unterstützt. Anbieter, die diese Eigenschaft für Schlüssel unterstützen, sollten auch die **Eigenschaften Eigenschaft NCrypt- \_ \_ \_ aktivierte \_ Eigenschaft** für das Anbieter handle unterstützen. Der Microsoft-Schlüsselspeicher Anbieter unterstützt diese Eigenschaft nicht. Diese Eigenschaft gilt nur für persistente Schlüssel.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_USER_CERTSTORE_PROPERTY"></span><span id="ncrypt_user_certstore_property"></span>**ncrypt \_ - \_ benutzercertstore ( \_ Eigenschaft)**
</dt> <dd> <dl> <dt>

L "smartcardusercertstore"
</dt> <dt>



Ein **HCERTSTORE** , der den Smartcard-Benutzerzertifikat Speicher darstellt.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_VERSION_PROPERTY"></span><span id="ncrypt_version_property"></span>**ncrypt- \_ Version ( \_ Eigenschaft)**
</dt> <dd> <dl> <dt>

L "Version"
</dt> <dt>



Ein **DWORD** , das die Softwareversion des Anbieters enthält. Das hohe Wort enthält die Hauptversion, und das niedrige Wort enthält die neben Version. Beispiel: 0x00030033 = 3,51. Diese Eigenschaft gilt nur für-Anbieter.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_WINDOW_HANDLE_PROPERTY"></span><span id="ncrypt_window_handle_property"></span>**ncrypt- \_ Fenster \_ handle ( \_ Eigenschaft)**
</dt> <dd> <dl> <dt>

L "hWnd Handle"
</dt> <dt>



Ein Zeiger auf das Fenster Handle (**HWND**), das als übergeordnetes Element der angezeigten Benutzeroberfläche verwendet werden soll.

Da ein unerwünschtes Verhalten auftreten kann, wenn eine Benutzeroberfläche mit einem **null** -Fenster Handle für das übergeordnete Element angezeigt wird, wird dringend empfohlen, dass ein Schlüsselspeicher Anbieter keine Benutzeroberfläche anzeigt, es sei denn, diese Eigenschaft ist festgelegt.


</dt> </dl> </dd> </dl>

Die folgenden Werte werden verwendet, um Grenzwerte für Eigenschafts Daten zu definieren.



| Konstante/Wert                                                                                                                                                                                                                                                 | BESCHREIBUNG                                                              |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------|
| <span id="NCRYPT_MAX_PROPERTY_DATA"></span><span id="ncrypt_max_property_data"></span><dl> <dt>**NCrypt \_ Maximale \_ Eigenschafts \_ Daten**</dt> <dt>0x100000</dt> </dl> | Gibt die maximale Größe eines Eigenschafts Werts in Bytes an.<br/>     |
| <span id="NCRYPT_MAX_PROPERTY_NAME"></span><span id="ncrypt_max_property_name"></span><dl> <dt>**NCrypt \_ Maximaler \_ Eigenschafts \_ Name**</dt> <dt>64</dt> </dl>       | Gibt die maximale Größe eines Eigenschafts namens in Zeichen an.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Ncrypt. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ncryptgetproperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty)
</dt> <dt>

[**Ncryptsetproperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty)
</dt> </dl>

 

