---
description: Ruft Informationen aus dem Zertifikat ab.
ms.assetid: 57f1c6f9-f06d-4ac7-9070-2a2e6afe93d2
title: 'ICertificate2:: GetInfo-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.GetInfo
- ICertificate2.GetInfo
- ICertificate.GetInfo
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 41b3cb6cde796f64ee3a5953ed848d105a10bc5e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373653"
---
# <a name="icertificate2getinfo-method"></a>ICertificate2:: GetInfo-Methode

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509Certificate2-Klasse**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]

Die **GetInfo** -Methode ruft Informationen aus dem [*Zertifikat*](../secgloss/c-gly.md)ab.

## <a name="syntax"></a>Syntax


```VB
Certificate.GetInfo( _
  ByVal InfoType _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*InfoType* \[ in\]
</dt> <dd>

Ein Wert der [**CAPICOM \_ CERT \_ Info \_ Type**](capicom-cert-info-type.md) -Enumeration, der angibt, welcher Datentyp aus dem Zertifikat abgerufen wird. In der folgenden Tabelle sind die möglichen Werte aufgeführt.



| Wert                                                                                                                                                                                                                                     | Bedeutung                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERT_INFO_SUBJECT_SIMPLE_NAME"></span><span id="capicom_cert_info_subject_simple_name"></span><dl> <dt>**CAPICOM \_ CERT \_ Info \_ Subject \_ Simple \_ Name**</dt> </dl> | Gibt den anzeigen amen des Zertifikats Antragstellers zurück.<br/>                            |
| <span id="CAPICOM_CERT_INFO_ISSUER_SIMPLE_NAME"></span><span id="capicom_cert_info_issuer_simple_name"></span><dl> <dt>**Name der von CAPICOM \_ CERT \_ Info \_ Aussteller \_ einfacher \_**</dt> </dl>    | Gibt den anzeigen amen des Zertifikats Ausstellers zurück.<br/>                        |
| <span id="CAPICOM_CERT_INFO_SUBJECT_EMAIL_NAME"></span><span id="capicom_cert_info_subject_email_name"></span><dl> <dt>**Name der "CAPICOM \_ CERT \_ Info \_ Subject \_ Email \_ "**</dt> </dl>    | Gibt die e-Mail-Adresse des Zertifikat Antragstellers zurück.<br/>                             |
| <span id="CAPICOM_CERT_INFO_ISSUER_EMAIL_NAME"></span><span id="capicom_cert_info_issuer_email_name"></span><dl> <dt>**Name der \_ \_ \_ Aussteller \_ -e-Mail \_ des CAPICOM-Zertifikats**</dt> </dl>       | Gibt die e-Mail-Adresse des Zertifikats Ausstellers zurück.<br/>                       |
| <span id="CAPICOM_CERT_INFO_SUBJECT_UPN"></span><span id="capicom_cert_info_subject_upn"></span><dl> <dt>**Antragsteller \_ - \_ \_ \_ UPN für CAPICOM CERT Info**</dt> </dl>                          | Gibt den UPN des Zertifikat Antragstellers zurück. Eingeführt in CAPICOM 2,0.<br/>            |
| <span id="CAPICOM_CERT_INFO_ISSUER_UPN"></span><span id="capicom_cert_info_issuer_upn"></span><dl> <dt>**-UPN des CAPICOM \_ CERT \_ Info- \_ Ausstellers \_**</dt> </dl>                             | Gibt den UPN des Zertifikats Ausstellers zurück. Eingeführt in CAPICOM 2,0.<br/>      |
| <span id="CAPICOM_CERT_INFO_SUBJECT_DNS_NAME"></span><span id="capicom_cert_info_subject_dns_name"></span><dl> <dt>**"CAPICOM \_ CERT \_ Info \_ Subject \_ DNS \_ Name"**</dt> </dl>          | Gibt den DNS-Namen des Zertifikat Antragstellers zurück. Eingeführt in CAPICOM 2,0.<br/>       |
| <span id="CAPICOM_CERT_INFO_ISSUER_DNS_NAME"></span><span id="capicom_cert_info_issuer_dns_name"></span><dl> <dt>**Name des CAPICOM \_ CERT \_ Info-Aussteller- \_ \_ DNS \_**</dt> </dl>             | Gibt den DNS-Namen des Zertifikats Ausstellers zurück. Eingeführt in CAPICOM 2,0.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Zeichenfolge, die die angeforderten Informationen enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Kryptografieobjekte](cryptography-objects.md)
</dt> <dt>

[**Stellt**](certificate.md)
</dt> </dl>

 

 
