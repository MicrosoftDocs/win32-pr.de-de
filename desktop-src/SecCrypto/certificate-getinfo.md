---
description: Ruft Informationen aus dem Zertifikat ab.
ms.assetid: 57f1c6f9-f06d-4ac7-9070-2a2e6afe93d2
title: ICertificate2::GetInfo-Methode
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
ms.openlocfilehash: 401aa077e5f736449e0638fd5cf368224485ec8393b8bddaed1f62296ad90297
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127020"
---
# <a name="icertificate2getinfo-method"></a>ICertificate2::GetInfo-Methode

\[CAPICOM ist eine 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509Certificate2-Klasse**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) im [**Namespace System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Die **GetInfo-Methode** ruft Informationen aus dem Zertifikat [*ab.*](../secgloss/c-gly.md)

## <a name="syntax"></a>Syntax


```VB
Certificate.GetInfo( _
  ByVal InfoType _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*InfoType* \[ In\]
</dt> <dd>

Ein Wert der [**CAPICOM \_ CERT \_ INFO \_ TYPE-Enumeration,**](capicom-cert-info-type.md) der angibt, welcher Datentyp aus dem Zertifikat abgerufen wird. In der folgenden Tabelle sind die möglichen Werte aufgeführt.



| Wert                                                                                                                                                                                                                                     | Bedeutung                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERT_INFO_SUBJECT_SIMPLE_NAME"></span><span id="capicom_cert_info_subject_simple_name"></span><dl> <dt>**CAPICOM \_ CERT \_ INFO \_ SUBJECT \_ SIMPLE \_ NAME**</dt> </dl> | Gibt den Anzeigenamen aus dem Zertifikatssubjekt zurück.<br/>                            |
| <span id="CAPICOM_CERT_INFO_ISSUER_SIMPLE_NAME"></span><span id="capicom_cert_info_issuer_simple_name"></span><dl> <dt>**CAPICOM \_ CERT \_ INFO \_ ISSUER \_ SIMPLE \_ NAME**</dt> </dl>    | Gibt den Anzeigenamen des Zertifikatausstellers zurück.<br/>                        |
| <span id="CAPICOM_CERT_INFO_SUBJECT_EMAIL_NAME"></span><span id="capicom_cert_info_subject_email_name"></span><dl> <dt>**CAPICOM \_ CERT \_ INFO \_ SUBJECT \_ EMAIL \_ NAME**</dt> </dl>    | Gibt die E-Mail-Adresse des Zertifikatsubjekts zurück.<br/>                             |
| <span id="CAPICOM_CERT_INFO_ISSUER_EMAIL_NAME"></span><span id="capicom_cert_info_issuer_email_name"></span><dl> <dt>**CAPICOM \_ CERT \_ INFO \_ ISSUER \_ EMAIL \_ NAME**</dt> </dl>       | Gibt die E-Mail-Adresse des Zertifikatausstellers zurück.<br/>                       |
| <span id="CAPICOM_CERT_INFO_SUBJECT_UPN"></span><span id="capicom_cert_info_subject_upn"></span><dl> <dt>**CAPICOM \_ CERT \_ INFO \_ SUBJECT \_ UPN**</dt> </dl>                          | Gibt den UPN des Zertifikatssubjekts zurück. Eingeführt in CAPICOM 2.0.<br/>            |
| <span id="CAPICOM_CERT_INFO_ISSUER_UPN"></span><span id="capicom_cert_info_issuer_upn"></span><dl> <dt>**CAPICOM \_ CERT \_ INFO \_ ISSUER \_ UPN**</dt> </dl>                             | Gibt den UPN des Zertifikatausstellers zurück. Eingeführt in CAPICOM 2.0.<br/>      |
| <span id="CAPICOM_CERT_INFO_SUBJECT_DNS_NAME"></span><span id="capicom_cert_info_subject_dns_name"></span><dl> <dt>**DNS-NAME DES \_ SUBJEKTS FÜR CAPICOM-ZERTIFIKATINFORMATIONEN \_ \_ \_ \_**</dt> </dl>          | Gibt den DNS-Namen des Zertifikatsubjekts zurück. Eingeführt in CAPICOM 2.0.<br/>       |
| <span id="CAPICOM_CERT_INFO_ISSUER_DNS_NAME"></span><span id="capicom_cert_info_issuer_dns_name"></span><dl> <dt>**CAPICOM \_ CERT \_ INFO \_ ISSUER \_ DNS \_ NAME**</dt> </dl>             | Gibt den DNS-Namen des Zertifikatausstellers zurück. Eingeführt in CAPICOM 2.0.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Zeichenfolge, die die angeforderten Informationen enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Kryptografieobjekte](cryptography-objects.md)
</dt> <dt>

[**Zertifikat**](certificate.md)
</dt> </dl>

 

 
