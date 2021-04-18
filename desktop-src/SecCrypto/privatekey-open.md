---
description: Greift auf einen vorhandenen Schlüssel Container zu. Diese Methode ordnet dem Zertifikat, das dem privaten Schlüssel entspricht, den Schlüssel Container zu, indem die \_ Eigenschaft "CERT Key \_ Prov \_ Info \_ Prop ID" unter \_ Verwendung der angegebenen Informationen hinzugefügt wird.
ms.assetid: e5e19452-bfdc-4427-ac1d-cf8aa349bb89
title: PrivateKey. Open-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.Open
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 7e39738a6e28ebbaffbc867f3098270d5043887a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371058"
---
# <a name="privatekeyopen-method"></a>PrivateKey. Open-Methode

\[Die **Open** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Verwenden Sie stattdessen die [**X509Certificate2. PrivateKey-Eigenschaft**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]

Die **Open** -Methode greift auf einen vorhandenen [*Schlüssel Container*](../secgloss/k-gly.md)zu. Diese Methode ordnet dem [*Zertifikat*](../secgloss/c-gly.md) , das dem [*privaten Schlüssel*](../secgloss/p-gly.md) entspricht, den Schlüssel Container zu, indem die \_ Eigenschaft "CERT Key \_ Prov \_ Info Prop ID" unter \_ \_ Verwendung der angegebenen Informationen hinzugefügt wird.

## <a name="syntax"></a>Syntax


```VB
PrivateKey.Open( _
  ByVal ContainerName, _
  [ ByVal ProviderName ], _
  [ ByVal ProviderType ], _
  [ ByVal KeySpec ], _
  [ ByVal StoreLocation ], _
  [ ByVal bCheckExistence ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Containername* \[ in\]
</dt> <dd>

Eine Zeichenfolge, die den Namen des Schlüssel Containers enthält.

</dd> <dt>

*ProviderName* \[ in, optional\]
</dt> <dd>

Eine Zeichenfolge, die den Namen des Anbieters enthält. Der Standardwert ist "CAPICOM \_ Prov \_ MS \_ Enhanced \_ Prov". Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                                                                      | Bedeutung                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="CAPICOM_PROV_MS_DEF_PROV"></span><span id="capicom_prov_ms_def_prov"></span><dl> <dt>**CAPICOM \_ Prov \_ MS \_ DEF \_ Prov**</dt> </dl>                                          | Microsoft-Basis-Kryptografieanbieter.<br/>                            |
| <span id="CAPICOM_PROV_MS_ENHANCED_PROV"></span><span id="capicom_prov_ms_enhanced_prov"></span><dl> <dt>**von CAPICOM \_ Prov \_ MS \_ Enhanced \_ Prov**</dt> </dl>                           | Microsoft Enhanced kryptografischen Provider.<br/>                        |
| <span id="CAPICOM_PROV_MS_STRONG_PROV"></span><span id="capicom_prov_ms_strong_prov"></span><dl> <dt>**CAPICOM \_ Prov \_ MS \_ Strong \_ Prov**</dt> </dl>                                 | Microsoft starker Kryptografieanbieter.<br/>                          |
| <span id="CAPICOM_PROV_MS_DEF_RSA_SIG_PROV"></span><span id="capicom_prov_ms_def_rsa_sig_prov"></span><dl> <dt>**CAPICOM \_ Prov \_ MS \_ DEF \_ RSA \_ sig \_ Prov**</dt> </dl>                | Kryptografieanbieter für Microsoft RSA Signature.<br/>                   |
| <span id="CAPICOM_PROV_MS_DEF_RSA_SCHANNEL_PROV"></span><span id="capicom_prov_ms_def_rsa_schannel_prov"></span><dl> <dt>**CAPICOM \_ Prov \_ MS \_ DEF \_ RSA \_ SChannel \_ Prov**</dt> </dl> | Kryptografieanbieter für Microsoft RSA SChannel.<br/>                    |
| <span id="CAPICOM_PROV_MS_DEF_DSS_PROV"></span><span id="capicom_prov_ms_def_dss_prov"></span><dl> <dt>**CAPICOM \_ Prov \_ MS \_ DEF \_ DSS \_ Prov**</dt> </dl>                             | Microsoft Base DSS-Kryptografieanbieter.<br/>                        |
| <span id="CAPICOM_PROV_MS_DEF_DSS_DH_PROV"></span><span id="capicom_prov_ms_def_dss_dh_prov"></span><dl> <dt>**CAPICOM \_ Prov \_ MS \_ DEF \_ DSS \_ dh \_ Prov**</dt> </dl>                   | Microsoft Base DSS und Diffie-Hellman Kryptografieanbieter.<br/>     |
| <span id="CAPICOM_PROV_MS_ENH_DSS_DH_PROV"></span><span id="capicom_prov_ms_enh_dss_dh_prov"></span><dl> <dt>**CAPICOM \_ Prov \_ MS \_ th \_ DSS \_ dh \_ Prov**</dt> </dl>                   | Microsoft Enhanced DSS und Diffie-Hellman Kryptografieanbieter.<br/> |
| <span id="CAPICOM_PROV_MS_DEF_DH_SCHANNEL_PROV"></span><span id="capicom_prov_ms_def_dh_schannel_prov"></span><dl> <dt>**CAPICOM \_ Prov \_ MS \_ DEF \_ dh \_ SChannel \_ Prov**</dt> </dl>    | Microsoft DH SChannel-Kryptografieanbieter.<br/>                     |
| <span id="CAPICOM_PROV_MS_SCARD_PROV"></span><span id="capicom_prov_ms_scard_prov"></span><dl> <dt>**CAPICOM \_ Prov \_ MS \_ SCard \_ Prov**</dt> </dl>                                    | Microsoft Basis Smartcard-Kryptografieanbieter.<br/>                 |
| <span id="CAPICOM_PROV_MS_ENH_RSA_AES_PROV"></span><span id="capicom_prov_ms_enh_rsa_aes_prov"></span><dl> <dt>**CAPICOM \_ Prov \_ MS-Version \_ \_ RSA \_ AES \_ Prov**</dt> </dl>                | Microsoft Enhanced RSA und AES kryptografischen Provider.<br/>            |



 

</dd> <dt>

*ProviderType* \[ in, optional\]
</dt> <dd>

Ein Wert der [**CAPICOM \_ Prov \_ Type**](capicom-prov-type.md) -Enumeration, die einen Anbietertyp angibt. Der Standardwert ist CAPICOM \_ Prov \_ RSA \_ Full. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                                   | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_PROV_RSA_FULL"></span><span id="capicom_prov_rsa_full"></span><dl> <dt>**CAPICOM \_ Prov \_ RSA \_ Full**</dt> </dl>                 | Der vollständige [*RSA*](../secgloss/r-gly.md) - [*Kryptografiedienstanbieter*](../secgloss/c-gly.md) (CSP). Dieser Anbietertyp unterstützt sowohl [*digitale Signaturen*](../secgloss/d-gly.md) als auch Daten [*Verschlüsselung*](../secgloss/e-gly.md).<br/> |
| <span id="CAPICOM_PROV_RSA_SIG"></span><span id="capicom_prov_rsa_sig"></span><dl> <dt>**CAPICOM \_ Prov \_ RSA \_ sig**</dt> </dl>                    | Die Teilmenge des RSA-CSP, die nur die Funktionen und Algorithmen unterstützt, die für [*Hashes*](../secgloss/h-gly.md) und [*digitale Signaturen*](../secgloss/d-gly.md)erforderlich sind.<br/>                                                                                                                                                                              |
| <span id="CAPICOM_PROV_DSS"></span><span id="capicom_prov_dss"></span><dl> <dt>**CAPICOM \_ Prov \_ DSS**</dt> </dl>                                 | Der DSS-CSP ( [*Digital Signature Standard*](../secgloss/d-gly.md) ). Dieser Anbietertyp unterstützt nur Hashes und digitale Signaturen. DSS verwendet den [*Digital Signature-Algorithmus*](../secgloss/d-gly.md) (DSA).<br/>                                                                                     |
| <span id="CAPICOM_PROV_FORTEZZA"></span><span id="capicom_prov_fortezza"></span><dl> <dt>**CAPICOM \_ Prov \_ Fortezza**</dt> </dl>                  | Der CSP, der die Kryptografieprotokolle und-Algorithmen im Besitz des [*National Institute of Standards and Technology*](../secgloss/n-gly.md) (NIST) enthält.<br/>                                                                                                                                                                          |
| <span id="CAPICOM_PROV_MS_EXCHANGE"></span><span id="capicom_prov_ms_exchange"></span><dl> <dt>**CAPICOM \_ Prov \_ MS \_ Exchange**</dt> </dl>        | Der CSP, der die Microsoft Exchange-e-Mail-Anwendung und andere Anwendungen unterstützt, die mit Microsoft Mail kompatibel sind.<br/>                                                                                                                                                                                                                                                                                                                               |
| <span id="CAPICOM_PROV_SSL"></span><span id="capicom_prov_ssl"></span><dl> <dt>**CAPICOM \_ Prov \_ SSL**</dt> </dl>                                 | Der CSP, der das [*Secure Sockets Layer*](../secgloss/s-gly.md) (SSL)-Protokoll unterstützt.<br/>                                                                                                                                                                                                                                                                                  |
| <span id="CAPICOM_PROV_RSA_SCHANNEL"></span><span id="capicom_prov_rsa_schannel"></span><dl> <dt>**CAPICOM \_ Prov \_ RSA \_ SChannel**</dt> </dl>     | Der CSP, der sowohl RSA-als auch [*SChannel*](../secgloss/s-gly.md) -Protokolle unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                    |
| <span id="CAPICOM_PROV_DSS_DH"></span><span id="capicom_prov_dss_dh"></span><dl> <dt>**CAPICOM \_ Prov \_ DSS \_ dh**</dt> </dl>                       | Der CSP, der sowohl DSS-als auch [*Diffie-Hellman-*](../secgloss/d-gly.md) Protokolle unterstützt.<br/>                                                                                                                                                                                                                                                                                              |
| <span id="CAPICOM_PROV_EC_ECDSA_SIG"></span><span id="capicom_prov_ec_ecdsa_sig"></span><dl> <dt>**CAPICOM \_ Prov \_ EC \_ ECDSA \_ sig**</dt> </dl>    | Der CSP, der die ECDSA (Elliptic Curve Digital Signature Algorithmus)-Funktionen und-Algorithmen unterstützt, die für digitale Signaturen erforderlich sind.<br/>                                                                                                                                                                                                                                                                                                                      |
| <span id="CAPICOM_PROV_EC_ECNRA_SIG"></span><span id="capicom_prov_ec_ecnra_sig"></span><dl> <dt>**CAPICOM \_ Prov \_ EC \_ ecnra \_ sig**</dt> </dl>    | Der CSP, der die ecnra-Funktionen (Elliptic Curve Nyberg-Rueppel analog) und die für digitale Signaturen erforderlichen Algorithmen unterstützt.<br/>                                                                                                                                                                                                                                                                                                                            |
| <span id="CAPICOM_PROV_EC_ECDSA_FULL"></span><span id="capicom_prov_ec_ecdsa_full"></span><dl> <dt>**CAPICOM \_ Prov \_ EC \_ ECDSA \_ vollständig**</dt> </dl> | Der CSP, der den vollständigen ECDSA unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="CAPICOM_PROV_EC_ECNRA_FULL"></span><span id="capicom_prov_ec_ecnra_full"></span><dl> <dt>**CAPICOM \_ Prov \_ EC \_ ecnra \_ Full**</dt> </dl> | Der CSP, der den vollständigen ecnra-unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="CAPICOM_PROV_DH_SCHANNEL"></span><span id="capicom_prov_dh_schannel"></span><dl> <dt>**CAPICOM \_ Prov \_ dh \_ SChannel**</dt> </dl>        | Der CSP, der sowohl [*Diffie-Hellman-*](../secgloss/d-gly.md) als auch [*SChannel*](../secgloss/s-gly.md) -Protokolle unterstützt.<br/>                                                                                                                                                                                                                       |
| <span id="CAPICOM_PROV_SPYRUS_LYNKS"></span><span id="capicom_prov_spyrus_lynks"></span><dl> <dt>**CAPICOM \_ Prov \_ spyrus \_ Lynchs**</dt> </dl>     | Der CSP, der das spyrus lynert-Karten Gerät unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="CAPICOM_PROV_RNG"></span><span id="capicom_prov_rng"></span><dl> <dt>**CAPICOM \_ Prov \_ RNG**</dt> </dl>                                 | Der CSP, der die Zufallszahlengenerierung verarbeitet.<br/>                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="CAPICOM_PROV_INTEL_SEC"></span><span id="capicom_prov_intel_sec"></span><dl> <dt>**CAPICOM \_ Prov \_ Intel \_ sec**</dt> </dl>              | Der CSP, der Intel Security bereitstellt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="CAPICOM_PROV_REPLACE_OWF"></span><span id="capicom_prov_replace_owf"></span><dl> <dt>**CAPICOM \_ Prov \_ Replace \_ owf**</dt> </dl>        | Der CSP, der die Ersetzung der Art und Weise unterstützt, in der unidirektionale Formate von Kenn Wörtern generiert werden.<br/>                                                                                                                                                                                                                                                                                                                                                      |
| <span id="CAPICOM_PROV_RSA_AES"></span><span id="capicom_prov_rsa_aes"></span><dl> <dt>**CAPICOM \_ Prov \_ RSA \_ AES**</dt> </dl>                    | Der CSP, der sowohl digitale Signaturen als auch Datenverschlüsselung unterstützt, mithilfe des-Advanced Encryption Standard ([*AES*](../secgloss/a-gly.md))-Algorithmus.<br/>                                                                                                                                                                                                                                                                           |



 

</dd> <dt>

*KeySpec* \[ in, optional\]
</dt> <dd>

Ein Wert der [**CAPICOM- \_ schlüsselspezifikations \_**](capicom-key-spec.md) Enumeration, der den Typ des privaten Schlüssels angibt. Der Standardwert ist CAPICOM \_ Key \_ spec \_ Signature. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                                        | Bedeutung                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="CAPICOM_KEY_SPEC_KEYEXCHANGE"></span><span id="capicom_key_spec_keyexchange"></span><dl> <dt>**CAPICOM- \_ Schlüssel \_ Spezifikation \_ keyexchange**</dt> </dl> | Der Schlüssel kann für die Verschlüsselung und Signierung verwendet werden.<br/> |
| <span id="CAPICOM_KEY_SPEC_SIGNATURE"></span><span id="capicom_key_spec_signature"></span><dl> <dt>**CAPICOM \_ Key \_ spec- \_ Signatur**</dt> </dl>       | Der Schlüssel kann nur für die Signierung verwendet werden.<br/>           |



 

</dd> <dt>

*Storeloation* \[ in, optional\]
</dt> <dd>

Ein Wert der [**CAPICOM \_ Store \_ Location**](capicom-store-location.md) -Enumeration, der den Speicherort des Stores angibt, in dem sich der Schlüssel befindet. Der Standardwert ist "CAPICOM \_ Current \_ User \_ Store". Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                                                              | Bedeutung                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_MEMORY_STORE"></span><span id="capicom_memory_store"></span><dl> <dt>**CAPICOM- \_ Speicher Speicher \_**</dt> </dl>                                                | Der Speicher ist ein Speicher Speicher. Alle Änderungen im Inhalt des Stores werden nicht persistent gespeichert.<br/>                                                                                                                                                                                |
| <span id="CAPICOM_LOCAL_MACHINE_STORE"></span><span id="capicom_local_machine_store"></span><dl> <dt>**lokaler CAPICOM- \_ \_ Computer \_ Speicher**</dt> </dl>                          | Der Speicher ist ein lokaler Computerspeicher. Lokale Computerspeicher können nur Lese-/Schreibspeicher sein, wenn der Benutzer über Lese-/Schreibberechtigungen verfügt. Wenn der Benutzer über Lese-/Schreibberechtigungen verfügt und der Speicher mit Lese-/Schreibzugriff geöffnet wird, werden Änderungen im Inhalt des Stores beibehalten.<br/> |
| <span id="CAPICOM_CURRENT_USER_STORE"></span><span id="capicom_current_user_store"></span><dl> <dt>**CAPICOM \_ aktueller \_ Benutzer \_ Speicher**</dt> </dl>                             | Der Speicher ist ein aktueller Benutzerspeicher. Ein aktueller Benutzerspeicher kann ein Lese-/Schreibspeicher sein. Wenn dies der Fall ist, werden Änderungen am Inhalt des Stores persistent gespeichert.<br/>                                                                                                                        |
| <span id="CAPICOM_ACTIVE_DIRECTORY_USER_STORE"></span><span id="capicom_active_directory_user_store"></span><dl> <dt>**CAPICOM \_ Active \_ Directory- \_ Benutzer \_ Speicher**</dt> </dl> | Der Speicher ist ein Active Directory Speicher. Active Directory Stores können nur im schreibgeschützten Modus geöffnet werden. Zertifikate können Active Directory speichern nicht hinzugefügt oder daraus entfernt werden.<br/>                                                                                          |
| <span id="CAPICOM_SMART_CARD_USER_STORE"></span><span id="capicom_smart_card_user_store"></span><dl> <dt>**CAPICOM \_ - \_ Smartcard- \_ Benutzer \_ Speicher**</dt> </dl>                   | Der Speicher ist die Gruppe der vorhandenen Smartcards. Eingeführt in CAPICOM 2,0.<br/>                                                                                                                                                                                               |



 

</dd> <dt>

*bcheckexistenz* \[ in, optional\]
</dt> <dd>

Ein boolescher Wert, der angibt, ob CAPICOM versucht, auf den Schlüssel zuzugreifen. **True** gibt an, dass CAPICOM versucht, auf den Schlüssel zuzugreifen. Wenn der Schlüssel Benutzer geschützt ist oder auf einer Smartcard oder einem anderen Gerät angezeigt wird, kann ein Dialogfeld generiert werden. Der Standardwert ist **False**.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode gibt CAPICOM \_ E \_ nicht \_ zulässig zurück, wenn ein Skript aus einer webbasierten Anwendung erstellt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**PrivateKey**](privatekey.md)
</dt> <dt>

[**Certificate. HasPrivateKey**](certificate-hasprivatekey.md)
</dt> </dl>

 

 
