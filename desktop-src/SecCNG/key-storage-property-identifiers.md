---
description: Wird verwendet, um eine Schlüsselspeichereigenschaft zu identifizieren.
ms.assetid: 407f0e42-07c8-4ec6-81c6-f8bde005adb0
title: Key Storage-Eigenschaftsbezeichner (Ncrypt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20b8fca27591837a555e4f75040ba16056c42e16ce488c0bb99f2d8f7de70bd1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118907614"
---
# <a name="key-storage-property-identifiers"></a>Key Storage-Eigenschaftsbezeichner

Die folgenden Werte werden verwendet, um eine Schlüsselspeichereigenschaft zu identifizieren.

<dl> <dt>

<span id="NCRYPT_ALGORITHM_GROUP_PROPERTY"></span><span id="ncrypt_algorithm_group_property"></span>**NCRYPT \_ ALGORITHM \_ \_ GROUP-EIGENSCHAFT**
</dt> <dd> <dl> <dt>

L"Algorithm Group"
</dt> <dt>



Eine auf NULL endende Unicode-Zeichenfolge, die den Namen der Algorithmusgruppe des Objekts enthält. Diese Eigenschaft gilt nur für Schlüssel. Die folgenden Bezeichner werden vom Microsoft-Schlüsselspeicheranbieter zurückgegeben.



| Bezeichner                                     | Wert              | BESCHREIBUNG                                                   |
|------------------------------------------------|--------------------|---------------------------------------------------------------|
| **NCRYPT \_ RSA \_ ALGORITHM \_ GROUP**<br/>   | "RSA"<br/>   | Die RSA-Algorithmusgruppe.<br/>                           |
| **NCRYPT \_ DH \_ ALGORITHM \_ GROUP**<br/>    | "DH"<br/>    | Die Diffie-Hellman Algorithmusgruppe.<br/>                |
| **NCRYPT \_ DSA \_ ALGORITHM \_ GROUP**<br/>   | "DSA"<br/>   | Die DSA-Algorithmusgruppe.<br/>                           |
| **NCRYPT \_ ECDSA \_ ALGORITHM \_ GROUP**<br/> | "ECDSA"<br/> | Die DSA-Algorithmusgruppe der elliptischen Kurve.<br/>            |
| **NCRYPT \_ ECDH \_ ALGORITHM \_ GROUP**<br/>  | "ECDH"<br/>  | Die elliptische Kurve Diffie-Hellman Algorithmusgruppe.<br/> |



 


</dt> </dl> </dd> <dt>

<span id="NCRYPT_ALGORITHM_PROPERTY"></span><span id="ncrypt_algorithm_property"></span>**\_NCRYPT-ALGORITHMUSEIGENSCHAFT \_**
</dt> <dd> <dl> <dt>

L"Algorithmusname"
</dt> <dt>



Eine auf NULL endende Unicode-Zeichenfolge, die den Namen des Algorithmus des Objekts enthält. Dies kann einer der vordefinierten [**CNG-Algorithmusbezeichner**](cng-algorithm-identifiers.md) oder ein anderer registrierter Algorithmusbezeichner sein. Diese Eigenschaft gilt nur für Schlüssel.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_ASSOCIATED_ECDH_KEY"></span><span id="ncrypt_associated_ecdh_key"></span>**ZUGEORDNETER \_ \_ NCRYPT-ECDH-SCHLÜSSEL \_**
</dt> <dd> <dl> <dt>

L"SmartCardAssociatedECDHKey"
</dt> <dt>



Ein **LPWSTR-Wert,** der den Containernamen des ECDH-Schlüssels (Elliptic Curve Diffie-Hellman) angibt, der während der Anmeldung für ein bestimmtes Handle für einen ECDSA-Schlüssel (Elliptic Curve Digital Signature Algorithm) verwendet werden soll. Wenn auf der Karte keine ECDH-Schlüssel vorhanden sind, gibt der [*Schlüsselspeicheranbieter (Key Storage Provider,*](/windows/desktop/SecGloss/k-gly) KSP) **NTE \_ NOT FOUND \_ zurück.** Diese Eigenschaft gilt für ECDSA-Schlüssel für die Anmeldung mit Smartcards. Die -Eigenschaft wird vom Microsoft Smart Card-Schlüsselspeicheranbieter und nicht vom Microsoft Software-Schlüsselspeicheranbieter unterstützt.

**Windows Server 2008 und Windows Vista:** Dieser Wert wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_BLOCK_LENGTH_PROPERTY"></span><span id="ncrypt_block_length_property"></span>**NCRYPT \_ BLOCK \_ \_ LENGTH-EIGENSCHAFT**
</dt> <dd> <dl> <dt>

L"Block Length"
</dt> <dt>



Ein **DWORD,das** die Länge des Verschlüsselungsblocks in Bytes enthält. Diese Eigenschaft gilt nur für Schlüssel, die die Verschlüsselung unterstützen.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_CERTIFICATE_PROPERTY"></span><span id="ncrypt_certificate_property"></span>**\_NCRYPT-ZERTIFIKATEIGENSCHAFT \_**
</dt> <dd> <dl> <dt>

L"SmartCardKeyCertificate"
</dt> <dt>



Ein [*BLOB,*](/windows/desktop/SecGloss/b-gly) das ein X.509-Zertifikat enthält, das dem Schlüssel zugeordnet ist.

**Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista:** Ein [*BLOB,*](/windows/desktop/SecGloss/b-gly) das das [*Smartcard-Schlüsselzertifikat*](/windows/desktop/SecGloss/s-gly) enthält. [](/windows/desktop/SecGloss/c-gly) Diese Eigenschaft wird vom Microsoft Software Key Storage Provider nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_DH_PARAMETERS_PROPERTY"></span><span id="ncrypt_dh_parameters_property"></span>**NCRYPT \_ DH \_ \_ PARAMETERS-EIGENSCHAFT**
</dt> <dd> <dl> <dt>

L"DHParameters"
</dt> <dt>



Gibt Parameter an, die mit einem Diffie-Hellman Schlüssel verwendet werden sollen. Dieser Datentyp ist ein Zeiger auf eine [**BCRYPT \_ DH PARAMETER \_ \_ HEADER-Struktur.**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_parameter_header) Diese Eigenschaft kann nur festgelegt werden und muss für den Schlüssel festgelegt werden, bevor der Schlüssel abgeschlossen wird.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_EXPORT_POLICY_PROPERTY"></span><span id="ncrypt_export_policy_property"></span>**NCRYPT \_ EXPORT \_ \_ POLICY-EIGENSCHAFT**
</dt> <dd> <dl> <dt>

L"Exportrichtlinie"
</dt> <dt>



Ein **DWORD,** das einen Satz von Flags enthält, die die Exportrichtlinie für einen persistenten Schlüssel angeben. Diese Eigenschaft gilt nur für Schlüssel. Dies kann 0 (null) oder eine Kombination aus einem oder mehreren der folgenden Werte enthalten.



| Bezeichner                                    | Wert      | BESCHREIBUNG                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **NCRYPT \_ ALLOW \_ EXPORT \_ FLAG**               | 0x00000001 | Der private Schlüssel kann exportiert werden.                                                                                                                                                                                                                                                                                 |
| **NCRYPT \_ ALLOW \_ PLAINTEXT \_ EXPORT \_ FLAG**    | 0x00000002 | Der private Schlüssel kann in Klartextform exportiert werden.                                                                                                                                                                                                                                                               |
| **NCRYPT \_ ALLOW \_ ARCHIVING \_ FLAG**            | 0x00000004 | Der private Schlüssel kann einmal zu Archivierungszwecken exportiert werden. Dieses Flag gilt nur für das ursprüngliche Schlüsselhandle, für das es festgelegt ist. Diese Richtlinie kann nur auf das ursprüngliche Schlüsselhandle angewendet werden. Nachdem das Schlüsselhandle geschlossen wurde, kann der Schlüssel nicht mehr zu Archivierungszwecken exportiert werden.                   |
| **NCRYPT \_ ALLOW \_ PLAINTEXT \_ ARCHIVING \_ FLAG** | 0x00000008 | Der private Schlüssel kann einmal im Klartextformat zu Archivierungszwecken exportiert werden. Dieses Flag gilt nur für das ursprüngliche Schlüsselhandle, für das es festgelegt ist. Diese Richtlinie kann nur auf das ursprüngliche Schlüsselhandle angewendet werden. Nachdem das Schlüsselhandle geschlossen wurde, kann der Schlüssel nicht mehr zu Archivierungszwecken exportiert werden. |



 


</dt> </dl> </dd> <dt>

<span id="NCRYPT_IMPL_TYPE_PROPERTY"></span><span id="ncrypt_impl_type_property"></span>**\_NCRYPT-IMPL-TYPEIGENSCHAFT \_ \_**
</dt> <dd> <dl> <dt>

L"Impl Type"
</dt> <dt>



Ein **DWORD,** das einen Satz von Flags enthält, die Implementierungsdetails des Anbieters definieren. Diese Eigenschaft gilt nur für Schlüsselspeicheranbieter. Dies kann 0 (null) oder eine Kombination aus einem oder mehreren der folgenden Werte enthalten.



| Bezeichner                            | Wert      | BESCHREIBUNG                                               |
|---------------------------------------|------------|-----------------------------------------------------------|
| **NCRYPT \_ IMPL \_ HARDWARE \_ FLAG**      | 0x00000001 | Der Anbieter ist hardwarebasiert.                           |
| **NCRYPT \_ IMPL \_ SOFTWARE \_ FLAG**      | 0x00000002 | Der Anbieter ist softwarebasiert.                           |
| **NCRYPT \_ IMPL \_ REMOVABLE \_ FLAG**     | 0x00000008 | Der Anbieter kann entfernt werden.                                |
| **NCRYPT \_ IMPL \_ HARDWARE \_ RNG \_ FLAG** | 0x00000010 | Der Anbieter ist ein hardwarebasierter Zufallszahlengenerator. |



 


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_TYPE_PROPERTY"></span><span id="ncrypt_key_type_property"></span>**NCRYPT \_ KEY \_ \_ TYPE-EIGENSCHAFT**
</dt> <dd> <dl> <dt>

L"Schlüsseltyp"
</dt> <dt>



Ein **DWORD,** das einen Satz von Flags enthält, die den Schlüsseltyp definieren. Diese Eigenschaft gilt nur für Schlüssel. Dieser kann 0 (null) oder den folgenden Wert enthalten.



| Bezeichner                     | Wert      | BESCHREIBUNG                                                                                              |
|--------------------------------|------------|----------------------------------------------------------------------------------------------------------|
| **\_ \_ NCRYPT-COMPUTERSCHLÜSSELFLAG \_** | 0x00000001 | Der Schlüssel gilt für den lokalen Computer. Wenn dieses Flag nicht vorhanden ist, gilt der Schlüssel für den aktuellen Benutzer. |



 


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_USAGE_PROPERTY"></span><span id="ncrypt_key_usage_property"></span>**\_ \_ NCRYPT-SCHLÜSSELVERWENDUNGSEIGENSCHAFT \_**
</dt> <dd> <dl> <dt>

L"Schlüsselverwendung"
</dt> <dt>



Ein **DWORD,** das eine Reihe von Flags enthält, die die Verwendungsdetails für einen Schlüssel definieren. Diese Eigenschaft gilt nur für Schlüssel. Dies kann 0 (null) oder eine Kombination aus mindestens einem der folgenden Werte enthalten.



| Bezeichner                              | Wert      | BESCHREIBUNG                                          |
|-----------------------------------------|------------|------------------------------------------------------|
| **NCRYPT \_ ALLOW \_ DECRYPT \_ FLAG**        | 0x00000001 | Der Schlüssel kann für die Entschlüsselung verwendet werden.                  |
| **NCRYPT-FLAG \_ \_ "SIGNIERUNG \_ ZULASSEN"**        | 0x00000002 | Der Schlüssel kann zum Signieren verwendet werden.                     |
| **FLAG FÜR \_ \_ NCRYPT-SCHLÜSSELVEREINBARUNG \_ \_ ZULASSEN** | 0x00000004 | Der Schlüssel kann für die Verschlüsselung des Geheimvertrags verwendet werden. |
| **NCRYPT ALLOW ALL USAGES (ALLE \_ \_ \_ NUTZUNGEN ZULASSEN)**          | 0x00ffffff | Der Schlüssel kann für jeden Zweck verwendet werden.                 |



 


</dt> </dl> </dd> <dt>

<span id="NCRYPT_LAST_MODIFIED_PROPERTY"></span><span id="ncrypt_last_modified_property"></span>**NCRYPT \_ LAST \_ \_ MODIFIED-EIGENSCHAFT**
</dt> <dd> <dl> <dt>

L"Modified"
</dt> <dt>



Gibt an, wann der Schlüssel zuletzt geändert wurde. Dieser Datentyp ist ein Zeiger auf eine [**FILETIME-Struktur.**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) Diese Eigenschaft gilt nur für persistente Schlüssel.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_LENGTH_PROPERTY"></span><span id="ncrypt_length_property"></span>**NCRYPT \_ \_ LENGTH-EIGENSCHAFT**
</dt> <dd> <dl> <dt>

L"Length"
</dt> <dt>



Ein **DWORD,** das die Länge des Schlüssels in Bits enthält. Diese Eigenschaft gilt nur für Schlüssel.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_LENGTHS_PROPERTY"></span><span id="ncrypt_lengths_property"></span>**NCRYPT \_ \_ LENGTHS-EIGENSCHAFT**
</dt> <dd> <dl> <dt>

L"Lengths"
</dt> <dt>



Gibt die Schlüsselgrößen an, die vom Schlüssel unterstützt werden. Dieser Datentyp ist ein Zeiger auf eine [**NCRYPT \_ SUPPORTED \_ LENGTHS-Struktur,**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncrypt_supported_lengths) die diese Informationen enthält. Diese Eigenschaft gilt nur für Schlüssel.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_MAX_NAME_LENGTH_PROPERTY"></span><span id="ncrypt_max_name_length_property"></span>**NCRYPT \_ MAX \_ NAME \_ \_ LENGTH-EIGENSCHAFT**
</dt> <dd> <dl> <dt>

L"Max Name Length"
</dt> <dt>



Ein **DWORD,** das die maximale Länge des Namens eines persistenten Schlüssels in Zeichen enthält. Diese Eigenschaft gilt nur für einen Anbieter.

Diese Eigenschaft ist in erster Linie für die Verwendung durch Schlüsselspeicheranbieter vorgesehen, die ihre Schlüssel auf einem Gerät speichern, das über eine begrenzte Menge an verfügbarem Arbeitsspeicher verfügt, z. B. eine Smartcard.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_NAME_PROPERTY"></span><span id="ncrypt_name_property"></span>**NCRYPT \_ \_ NAME-EIGENSCHAFT**
</dt> <dd> <dl> <dt>

L"Name"
</dt> <dt>



Ein Zeiger auf eine auf NULL beendete Unicode-Zeichenfolge, die den Namen des Objekts enthält.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_PIN_PROMPT_PROPERTY"></span><span id="ncrypt_pin_prompt_property"></span>**NCRYPT \_ PIN \_ \_ PROMPT-EIGENSCHAFT**
</dt> <dd> <dl> <dt>

L"SmartCardPinPrompt"
</dt> <dt>



Dieser Wert wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_PIN_PROPERTY"></span><span id="ncrypt_pin_property"></span>**NCRYPT \_ \_ PIN-EIGENSCHAFT**
</dt> <dd> <dl> <dt>

L"SmartCardPin"
</dt> <dt>



Ein Zeiger auf eine auf NULL beendete Unicode-Zeichenfolge, die die PIN enthält. Die PIN wird für einen Smartcardschlüssel oder das Kennwort für einen kennwortgeschützten Schlüssel verwendet, der in einem softwarebasierten KSP gespeichert ist. Diese Eigenschaft kann nur festgelegt werden. Microsoft-KSPs speichern diesen Wert zwischen, sodass der Benutzer pro Prozess nur einmal dazu aufgefordert wird.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_PROVIDER_HANDLE_PROPERTY"></span><span id="ncrypt_provider_handle_property"></span>**HANDLE-EIGENSCHAFT DES \_ NCRYPT-ANBIETERS \_ \_**
</dt> <dd> <dl> <dt>

L"Provider Handle"
</dt> <dt>



Ein **NCRYPT \_ PROV \_ HANDLE,** das das Handle des CNG-Schlüsselspeicheranbieters enthält. Wenn Sie das Handle nicht mehr verwenden, müssen Sie [**NCryptFreeObject aufrufen,**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptfreeobject) um es frei zu geben.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_READER_PROPERTY"></span><span id="ncrypt_reader_property"></span>**NCRYPT \_ \_ READER-EIGENSCHAFT**
</dt> <dd> <dl> <dt>

L"SmartCardReader"
</dt> <dt>



Ein Zeiger auf eine auf NULL beendete Unicode-Zeichenfolge, die den Namen des Smartcardlesers enthält. Diese Eigenschaft kann nur festgelegt werden.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_ROOT_CERTSTORE_PROPERTY"></span><span id="ncrypt_root_certstore_property"></span>**NCRYPT \_ ROOT \_ CERTSTORE-EIGENSCHAFT \_**
</dt> <dd> <dl> <dt>

L"SmartcardRootCertStore"
</dt> <dt>



Ein **HCERTSTORE,** der den Smartcard-Stammzertifikatspeicher darstellt.


</dt> </dl> </dd> <dt>

<span id="_NCRYPT_SCARD_PIN_ID"></span><span id="_ncrypt_scard_pin_id"></span>**NCRYPT \_ \_SCARD-PIN-ID \_**
</dt> <dd> <dl> <dt>

L"SmartCardPinId"
</dt> <dt>



Ein Zeiger auf den **\_ PIN-ID-Wert,** der einem angegebenen [*kryptografischen Schlüssel auf*](/windows/desktop/SecGloss/c-gly) einer [*Smartcard zugeordnet ist.*](/windows/desktop/SecGloss/s-gly) Dies ist eine schreibgeschützte Eigenschaft. Der **\_ PIN-ID-Datentyp** wird in Cardmod.h definiert.

**Windows Server 2008 und Windows Vista:** Dieser Wert wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_SCARD_PIN_INFO"></span><span id="ncrypt_scard_pin_info"></span>**PIN-INFORMATIONEN ZUR \_ NCRYPT-SCARD \_ \_**
</dt> <dd> <dl> <dt>

L"SmartCardPinInfo"
</dt> <dt>



Ein Zeiger auf die [**\_ PIN-INFO-Struktur**](/windows/desktop/api/mbnapi/ns-mbnapi-mbn_pin_info) der PIN, die einem angegebenen kryptografischen Schlüssel auf der Smartcard zugeordnet ist. Der Aufrufer stellt das Schlüsselhand handle zur Hand. Diese Eigenschaft ist schreibgeschützt. Die **PIN \_ INFO-Struktur** ist in Cardmod.h definiert.

**Windows Server 2008 und Windows Vista:** Dieser Wert wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_SECURE_PIN_PROPERTY"></span><span id="ncrypt_secure_pin_property"></span>**NCRYPT SECURE \_ \_ \_ PIN-EIGENSCHAFT**
</dt> <dd> <dl> <dt>

L"SmartCardSecurePin"
</dt> <dt>



Ein Zeiger auf eine auf NULL beendete Unicode-Zeichenfolge, die die SMARTCARD-Sitzungs-PIN enthält. Diese Eigenschaft kann nur festgelegt werden.

**Windows Vista:** Diese Eigenschaft wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_SECURITY_DESCR_PROPERTY"></span><span id="ncrypt_security_descr_property"></span>**NCRYPT \_ SECURITY \_ \_ DESCR-EIGENSCHAFT**
</dt> <dd> <dl> <dt>

L"Security Descr"
</dt> <dt>



Ein Zeiger auf eine [**SECURITY \_ DESCRIPTOR-Struktur,**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) die Zugriffssteuerungsinformationen für den Schlüssel enthält. Diese Eigenschaft gilt nur für persistente Schlüssel. Der *dwFlags-Parameter* der [**NCryptGetProperty-**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) oder [**NCryptSetProperty-Funktion**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty) identifiziert den Teil des Sicherheitsdeskriptors, der ermittelt oder festgelegt werden soll.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_SECURITY_DESCR_SUPPORT_PROPERTY"></span><span id="ncrypt_security_descr_support_property"></span>**NCRYPT \_ SECURITY \_ DESCR \_ \_ SUPPORT-EIGENSCHAFT**
</dt> <dd> <dl> <dt>

L"Security Descr Support"
</dt> <dt>



Gibt an, ob der Anbieter Sicherheitsdeskriptoren für Schlüssel unterstützt. Diese Eigenschaft ist ein **DWORD,** das 1 enthält, wenn der Anbieter Sicherheitsdeskriptoren für Schlüssel unterstützt. Wenn diese Eigenschaft einen anderen Wert enthält oder die [**NCryptGetProperty-Funktion**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) **NTE \_ NOT \_ SUPPORTED** zurückgibt, unterstützt der Anbieter keine Sicherheitsbeschreibungen für Schlüssel. Diese Eigenschaft gilt nur für Anbieter.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_SMARTCARD_GUID_PROPERTY"></span><span id="ncrypt_smartcard_guid_property"></span>**\_ \_ NCRYPT-SMARTCARD-GUID-EIGENSCHAFT \_**
</dt> <dd> <dl> <dt>

L"SmartCardGuid"
</dt> <dt>



Ein BLOB, das den Bezeichner der Smartcard enthält.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_UI_POLICY_PROPERTY"></span><span id="ncrypt_ui_policy_property"></span>**NCRYPT \_ UI \_ \_ POLICY-EIGENSCHAFT**
</dt> <dd> <dl> <dt>

L"UI-Richtlinie"
</dt> <dt>



Bei Verwendung mit [**der NCryptSetProperty-**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty) oder [**NCryptGetProperty-Funktion**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) ist dies ein Zeiger auf eine [**NCRYPT \_ UI \_ POLICY-Struktur,**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncrypt_ui_policy) die die Richtlinie für die Benutzeroberfläche mit starkem Schlüssel für den Schlüssel enthält. Diese Eigenschaft gilt nur für persistente Schlüssel. Diese Eigenschaft kann nur festgelegt werden, wenn der Schlüssel generiert wird. Sobald die [**NCryptFinalizeKey-Funktion**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptfinalizekey) für diesen Schlüssel aufgerufen wurde, wird diese Eigenschaft schreibgeschützt.

Ein Schlüsselspeicheranbieter kann diesen Parameter über eine [**NCryptSetPropertyFn-Rückruffunktion**](https://www.bing.com/search?q=**NCryptSetPropertyFn**) empfangen. Der Parameterwert ist eine NCRYPT \_ UI \_ \_ POLICY-BLOB-Struktur, die die gleichen Informationen enthält. Wenn eine Anwendung eine Anforderung über NCryptSetPropertyFn an den Anbieter zum Zurückgeben dieser Eigenschaft stellt, wird erwartet, dass der Anbieter eine NCRYPT \_ UI \_ \_ POLICY-BLOB-Struktur zurück gibt.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_UNIQUE_NAME_PROPERTY"></span><span id="ncrypt_unique_name_property"></span>**EIGENSCHAFT "EINDEUTIGER \_ \_ NCRYPT-NAME" \_**
</dt> <dd> <dl> <dt>

L"Eindeutiger Name"
</dt> <dt>



Ein Zeiger auf eine mit NULL beendete Unicode-Zeichenfolge, die den eindeutigen Namen des Objekts enthält. Dies ist ein alternativer Name, der beim Zugriff auf den Schlüssel verwendet werden kann. Diese Eigenschaft wird verwendet, wenn angenommen wird, dass der ursprünglich an [**NCryptCreatePersistedKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptcreatepersistedkey) übergebene Schlüsselname nicht eindeutig genug ist, um den persistenten Schlüssel zuverlässig zu identifizieren. Der Microsoft-Schlüsselspeicheranbieter gibt den Dateinamen des Schlüssels als diese Eigenschaft zurück.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_USE_CONTEXT_PROPERTY"></span><span id="ncrypt_use_context_property"></span>**NCRYPT \_ USE \_ \_ CONTEXT-EIGENSCHAFT**
</dt> <dd> <dl> <dt>

L"Use Context"
</dt> <dt>



Ein Zeiger auf eine auf NULL beendete Unicode-Zeichenfolge, die den Kontext des Vorgangs beschreibt. Diese Eigenschaft ist nicht persistent und kann für einen Anbieter oder einen Schlüssel festgelegt werden. Ein Schlüssel hat keinen Zugriff auf die **NCRYPT \_ USE \_ CONTEXT \_ PROPERTY-Eigenschaft** des Anbieters, da die Eigenschaft nur für das Handle spezifisch ist, für das sie festgelegt ist.

Ein Beispiel, in dem diese Eigenschaft im Kontext eines Anbieters verwendet wird, ist ein Schlüsselspeicheranbieter, der den Benutzer während eines Aufrufs von [**NCryptOpenKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) auffordern muss (z. B. "Smartcard in den Reader einfügen"). Da das Schlüsselhand handle erst verfügbar ist, nachdem **NCryptOpenKey** zurückgegeben wurde, sollte die Anwendung diese Eigenschaft auf dem Anbieterhand handle festlegen, bevor **NCryptOpenKey aufruft.**

Ein Beispiel, in dem diese Eigenschaft im Kontext eines Schlüsselhandpunkts verwendet wird, ist ein Schlüsselspeicheranbieter, der den Benutzer während eines Vorgangs mithilfe des Schlüssels zur Eingabe auffordern muss (z. B. "Diese Anwendung muss diesen Schlüssel zum Signieren eines Dokuments verwenden."). Der Anbieter kann diese Kontextinformationen dann über eine benutzeroberfläche, die während des Vorgangs angezeigt wird, an den Benutzer weiterleiten.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_USE_COUNT_ENABLED_PROPERTY"></span><span id="ncrypt_use_count_enabled_property"></span>**NCRYPT \_ USE COUNT ENABLED \_ \_ \_ -EIGENSCHAFT**
</dt> <dd> <dl> <dt>

L"Anzahl aktivierter Verwendungen"
</dt> <dt>



Gibt an, ob der Anbieter die Nutzungszählung für Schlüssel unterstützt. Diese Eigenschaft ist ein **DWORD,** das 1 enthält, wenn der Anbieter die Verwendungszählung für Schlüssel unterstützt. Wenn diese Eigenschaft einen anderen Wert enthält oder die [**NCryptGetProperty-Funktion**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) **NTE \_ NICHT \_ UNTERSTÜTZT** zurückgibt, unterstützt der Anbieter die Verwendungszählung für Schlüssel nicht. Diese Eigenschaft gilt nur für Anbieter.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_USE_COUNT_PROPERTY"></span><span id="ncrypt_use_count_property"></span>**NCRYPT USE \_ \_ \_ COUNT-EIGENSCHAFT**
</dt> <dd> <dl> <dt>

L"Anzahl verwenden"
</dt> <dt>



Eine [**ULARGE \_ INTEGER-Variable,**](https://docs.microsoft.com/windows/win32/api/winnt/ns-winnt-ularge_integer~r1) die die Anzahl von Vorgängen enthält, die der angegebene [*private Schlüssel*](/windows/desktop/SecGloss/p-gly) ausgeführt hat. Diese Eigenschaft ist optional und wird möglicherweise nicht von allen Anbietern unterstützt. Anbieter, die diese Eigenschaft für Schlüssel unterstützen, sollten auch die **NCRYPT \_ USE COUNT ENABLED \_ \_ \_ PROPERTY-Eigenschaft** auf dem Anbieterhand handle unterstützen. Der Microsoft-Schlüsselspeicheranbieter unterstützt diese Eigenschaft nicht. Diese Eigenschaft gilt nur für persistente Schlüssel.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_USER_CERTSTORE_PROPERTY"></span><span id="ncrypt_user_certstore_property"></span>**NCRYPT \_ USER \_ CERTSTORE-EIGENSCHAFT \_**
</dt> <dd> <dl> <dt>

L"SmartCardUserCertStore"
</dt> <dt>



Ein **HCERTSTORE,** der den Smartcard-Benutzerzertifikatspeicher darstellt.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_VERSION_PROPERTY"></span><span id="ncrypt_version_property"></span>**\_NCRYPT-VERSIONSEIGENSCHAFT \_**
</dt> <dd> <dl> <dt>

L"Version"
</dt> <dt>



Ein **DWORD,** das die Softwareversion des Anbieters enthält. Das hohe Wort enthält die Hauptversion und das niedrige Wort die Nebenversion. Beispiel: 0x00030033 = 3,51. Diese Eigenschaft gilt nur für Anbieter.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_WINDOW_HANDLE_PROPERTY"></span><span id="ncrypt_window_handle_property"></span>**NCRYPT WINDOW \_ \_ \_ HANDLE-EIGENSCHAFT**
</dt> <dd> <dl> <dt>

L"HWND Handle"
</dt> <dt>



Ein Zeiger auf das Fensterhand handle (**HWND**), das als übergeordnetes Element einer beliebigen angezeigten Benutzeroberfläche verwendet werden soll.

Da unerwünschtes Verhalten passieren kann, wenn  eine Benutzeroberfläche mit einem NULL-Fensterhand handle für das übergeordnete Element angezeigt wird, wird dringend empfohlen, dass ein Schlüsselspeicheranbieter keine Benutzeroberfläche angibt, es sei denn, diese Eigenschaft ist festgelegt.


</dt> </dl> </dd> </dl>

Die folgenden Werte werden verwendet, um Grenzwerte für Eigenschaftsdaten zu definieren.



| Konstante/Wert                                                                                                                                                                                                                                                 | BESCHREIBUNG                                                              |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------|
| <span id="NCRYPT_MAX_PROPERTY_DATA"></span><span id="ncrypt_max_property_data"></span><dl> <dt>**NCRYPT \_ MAX \_ PROPERTY \_ DATA**</dt> <dt>0x100000</dt> </dl> | Gibt die maximale Größe eines Eigenschaftswerts in Bytes an.<br/>     |
| <span id="NCRYPT_MAX_PROPERTY_NAME"></span><span id="ncrypt_max_property_name"></span><dl> <dt>**NCRYPT \_ MAX \_ PROPERTY \_ NAME**</dt> <dt>64</dt> </dl>       | Gibt die maximale Größe eines Eigenschaftsnamens in Zeichen an.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Ncrypt.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty)
</dt> <dt>

[**NCryptSetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty)
</dt> </dl>

 

