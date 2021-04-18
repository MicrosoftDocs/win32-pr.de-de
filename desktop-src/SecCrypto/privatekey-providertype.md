---
description: Ruft einen Wert der CAPICOM \_ Prov Type- \_ Enumeration ab, der den Typ des Anbieters angibt.
ms.assetid: bc6a579f-5532-45e3-97f4-adcde2cd29e5
title: PrivateKey. ProviderType (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.ProviderType
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b38cc9a030bc27a30a66624f1faeca080104e7fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371990"
---
# <a name="privatekeyprovidertype-property"></a>PrivateKey. ProviderType (Eigenschaft)

\[Die **ProviderType** -Eigenschaft ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Verwenden Sie stattdessen die [**X509Certificate2. PrivateKey-Eigenschaft**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]

Die **ProviderType** -Eigenschaft ruft einen Wert der [**CAPICOM \_ Prov \_ Type**](capicom-prov-type.md) -Enumeration ab, der den Typ des Anbieters angibt.

## <a name="syntax"></a>Syntax


```VB
PrivateKey.ProviderType As CAPICOM_PROV_TYPE
```



## <a name="property-value"></a>Eigenschaftswert

Ein Wert der [**CAPICOM \_ Prov \_ Type**](capicom-prov-type.md) -Enumeration, der den Typ des Anbieters angibt. In der folgenden Tabelle sind die möglichen Werte aufgeführt.



| Wert                                                                                                                                                                                                   | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_PROV_RSA_FULL"></span><span id="capicom_prov_rsa_full"></span><dl> <dt>**CAPICOM \_ Prov \_ RSA \_ Full**</dt> </dl>                 | Der vollständige [*RSA*](../secgloss/r-gly.md) - [*Kryptografiedienstanbieter*](../secgloss/c-gly.md) (CSP). Dieser Anbietertyp unterstützt sowohl [*digitale Signaturen*](../secgloss/d-gly.md) als auch Daten [*Verschlüsselung*](../secgloss/e-gly.md).<br/> |
| <span id="CAPICOM_PROV_RSA_SIG"></span><span id="capicom_prov_rsa_sig"></span><dl> <dt>**CAPICOM \_ Prov \_ RSA \_ sig**</dt> </dl>                    | Die Teilmenge des RSA-CSP, die nur die Funktionen und Algorithmen unterstützt, die für Hashes und digitale Signaturen erforderlich sind.<br/>                                                                                                                                                                                                                                                                                                                                     |
| <span id="CAPICOM_PROV_DSS"></span><span id="capicom_prov_dss"></span><dl> <dt>**CAPICOM \_ Prov \_ DSS**</dt> </dl>                                 | Der DSS-CSP ( [*Digital Signature Standard*](../secgloss/d-gly.md) ). Dieser Anbietertyp unterstützt nur Hashes und digitale Signaturen. DSS verwendet den [*Digital Signature-Algorithmus*](../secgloss/d-gly.md) (DSA).<br/>                                                                                     |
| <span id="CAPICOM_PROV_FORTEZZA"></span><span id="capicom_prov_fortezza"></span><dl> <dt>**CAPICOM \_ Prov \_ Fortezza**</dt> </dl>                  | Der CSP, der die Kryptografieprotokolle und-Algorithmen im Besitz des [*National Institute of Standards and Technology*](../secgloss/n-gly.md) (NIST) enthält.<br/>                                                                                                                                                                          |
| <span id="CAPICOM_PROV_MS_EXCHANGE"></span><span id="capicom_prov_ms_exchange"></span><dl> <dt>**CAPICOM \_ Prov \_ MS \_ Exchange**</dt> </dl>        | Der CSP, der für die kryptografischen Anforderungen der Microsoft Exchange-e-Mail-Anwendung und anderer mit Microsoft Mail kompatibler Anwendungen entworfen wurde.<br/>                                                                                                                                                                                                                                                                                                              |
| <span id="CAPICOM_PROV_SSL"></span><span id="capicom_prov_ssl"></span><dl> <dt>**CAPICOM \_ Prov \_ SSL**</dt> </dl>                                 | Der CSP, der das [*Secure Sockets Layer*](../secgloss/s-gly.md) (SSL)-Protokoll unterstützt.<br/>                                                                                                                                                                                                                                                                                  |
| <span id="CAPICOM_PROV_RSA_SCHANNEL"></span><span id="capicom_prov_rsa_schannel"></span><dl> <dt>**CAPICOM \_ Prov \_ RSA \_ SChannel**</dt> </dl>     | Der CSP, der sowohl RSA-als auch [*SChannel*](../secgloss/s-gly.md) -Protokolle unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                    |
| <span id="CAPICOM_PROV_DSS_DH"></span><span id="capicom_prov_dss_dh"></span><dl> <dt>**CAPICOM \_ Prov \_ DSS \_ dh**</dt> </dl>                       | Der CSP, der sowohl den [*Digital Signature Standard*](../secgloss/d-gly.md) (DSS)-als auch das [*Diffie-Hellman-*](../secgloss/d-gly.md) Protokoll unterstützt.<br/>                                                                                                                                                           |
| <span id="CAPICOM_PROV_EC_ECDSA_SIG"></span><span id="capicom_prov_ec_ecdsa_sig"></span><dl> <dt>**CAPICOM \_ Prov \_ EC \_ ECDSA \_ sig**</dt> </dl>    | Der CSP, der die ECDSA (Elliptic Curve Digital Signature Algorithmus)-Funktionen und-Algorithmen unterstützt, die für digitale Signaturen erforderlich sind.<br/>                                                                                                                                                                                                                                                                                                                      |
| <span id="CAPICOM_PROV_EC_ECNRA_SIG"></span><span id="capicom_prov_ec_ecnra_sig"></span><dl> <dt>**CAPICOM \_ Prov \_ EC \_ ecnra \_ sig**</dt> </dl>    | Der CSP, der die ecnra-Funktionen (Elliptic Curve Nyberg-Rueppel analog) und die für digitale Signaturen erforderlichen Algorithmen unterstützt.<br/>                                                                                                                                                                                                                                                                                                                            |
| <span id="CAPICOM_PROV_EC_ECDSA_FULL"></span><span id="capicom_prov_ec_ecdsa_full"></span><dl> <dt>**CAPICOM \_ Prov \_ EC \_ ECDSA \_ vollständig**</dt> </dl> | Der CSP, der den vollständigen ECDSA unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="CAPICOM_PROV_EC_ECNRA_FULL"></span><span id="capicom_prov_ec_ecnra_full"></span><dl> <dt>**CAPICOM \_ Prov \_ EC \_ ecnra \_ Full**</dt> </dl> | Der CSP, der den vollständigen ecnra-unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="CAPICOM_PROV_DH_SCHANNEL"></span><span id="capicom_prov_dh_schannel"></span><dl> <dt>**CAPICOM \_ Prov \_ dh \_ SChannel**</dt> </dl>        | Der CSP, der sowohl [*Diffie-Hellman-*](../secgloss/d-gly.md) als auch [*SChannel*](../secgloss/s-gly.md) -Protokolle unterstützt.<br/>                                                                                                                                                                                                                       |
| <span id="CAPICOM_PROV_SPYRUS_LYNKS"></span><span id="capicom_prov_spyrus_lynks"></span><dl> <dt>**CAPICOM \_ Prov \_ spyrus \_ Lynchs**</dt> </dl>     | Der CSP, der das spyrus lynert-Karten Gerät unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="CAPICOM_PROV_RNG"></span><span id="capicom_prov_rng"></span><dl> <dt>**CAPICOM \_ Prov \_ RNG**</dt> </dl>                                 | Der CSP, der die Zufallszahlengenerierung verarbeitet.<br/>                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="CAPICOM_PROV_INTEL_SEC"></span><span id="capicom_prov_intel_sec"></span><dl> <dt>**CAPICOM \_ Prov \_ Intel \_ sec**</dt> </dl>              | Der CSP, der Intel Security bereitstellt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="CAPICOM_PROV_REPLACE_OWF"></span><span id="capicom_prov_replace_owf"></span><dl> <dt>**CAPICOM \_ Prov \_ Replace \_ owf**</dt> </dl>        | Der CSP, der die Ersetzung der Art und Weise unterstützt, in der unidirektionale Formate (owfs) aus Kenn Wörtern generiert werden.<br/>                                                                                                                                                                                                                                                                                                                                               |
| <span id="CAPICOM_PROV_RSA_AES"></span><span id="capicom_prov_rsa_aes"></span><dl> <dt>**CAPICOM \_ Prov \_ RSA \_ AES**</dt> </dl>                    | Der CSP, der sowohl digitale Signaturen als auch Datenverschlüsselung unterstützt, mithilfe des- [*Advanced Encryption Standard*](../secgloss/a-gly.md) (AES)-Algorithmus.<br/>                                                                                                                                                                                                                                                                           |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**PrivateKey**](privatekey.md)
</dt> </dl>

 

 
