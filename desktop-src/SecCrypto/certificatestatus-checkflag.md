---
description: Legt die Validierungsflags für ein Zertifikat fest oder ruft Sie ab.
ms.assetid: c80c95a0-8a9b-441d-b243-7ee0552731e4
title: CertificateStatus. checkflag (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.CheckFlag
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 00b0c648de17f6aca931ab3f3417d9ecb53ac558
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367601"
---
# <a name="certificatestatuscheckflag-property"></a>CertificateStatus. checkflag (Eigenschaft)

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509ChainStatus-Struktur**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]

Die **checkflag** -Eigenschaft legt die Gültigkeits kontrollflags für ein Zertifikat fest oder ruft Sie ab.

## <a name="syntax"></a>Syntax


```VB
CertificateStatus.CheckFlag As CAPICOM_CHECK_FLAG
```



## <a name="property-value"></a>Eigenschaftswert

Ein Wert der [**CAPICOM- \_ Check- \_ Flag**](capicom-check-flag.md) -Enumeration, die die Gültigkeits Prüfungen für das Zertifikat beschreibt. Der Standardwert lautet **CAPICOM \_ Check \_ Online \_ all**.

**CAPICOM 2.0.0.3/2.0.0.2/2.0.0.1:** Der Standardwert ist [**CAPICOM- \_ Überprüfung \_ Signatur \_ Gültigkeit**](capicom-check-flag.md), [**CAPICOM- \_ \_ \_ Gültigkeitsdauer Gültigkeit**](capicom-check-flag.md), [**CAPICOM \_ Check \_ Trusted \_ root**](capicom-check-flag.md)und [**CAPICOM \_ Check \_ Complete \_ Chain**](capicom-check-flag.md).

**CAPICOM 2,0 und früher:** Der Standardwert ist [**CAPICOM- \_ Überprüfung \_ Signatur \_ Gültigkeit**](capicom-check-flag.md), [**CAPICOM- \_ \_ \_ Gültigkeitsdauer Gültigkeit**](capicom-check-flag.md)und [**CAPICOM- \_ Überprüfung \_ vertrauenswürdiger \_**](capicom-check-flag.md)Stamm.

In der folgenden Tabelle sind die möglichen Werte aufgeführt.



| Wert                                                                                                                                                                                                                                          | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_CHECK_BASIC_CONSTRAINTS"></span><span id="capicom_check_basic_constraints"></span><dl> <dt>**grundeinschränkungen für CAPICOM- \_ Überprüfung \_ \_**</dt> </dl>                          | Überprüft grundlegende Einschränkungen. Eingeführt in CAPICOM 2,0.<br/>                                                                                                                                                                                                                                                                                                                                    |
| <span id="CAPICOM_CHECK_COMPLETE_CHAIN"></span><span id="capicom_check_complete_chain"></span><dl> <dt>**CAPICOM- \_ Überprüfung, \_ komplette \_ Kette**</dt> </dl>                                   | Überprüft die gesamte Kette. Eingeführt in CAPICOM 2,0.<br/>                                                                                                                                                                                                                                                                                                                                   |
| <span id="CAPICOM_CHECK_NAME_CONSTRAINTS"></span><span id="capicom_check_name_constraints"></span><dl> <dt>**Einschränkungen für "CAPICOM \_ Check \_ Name" \_**</dt> </dl>                             | Überprüft namens Einschränkungen. Eingeführt in CAPICOM 2,0.<br/>                                                                                                                                                                                                                                                                                                                                     |
| <span id="CAPICOM_CHECK_NESTED_VALIDITY_PERIOD"></span><span id="capicom_check_nested_validity_period"></span><dl> <dt>**Überprüfung der in der zwischen \_ Zeit überprüfen \_ \_ \_**</dt> </dl>          | Überprüft die eingesterte Gültigkeit. Eingeführt in CAPICOM 2,0.<br/>                                                                                                                                                                                                                                                                                                                                      |
| <span id="CAPICOM_CHECK_NONE"></span><span id="capicom_check_none"></span><dl> <dt>**CAPICOM- \_ Überprüfung nicht \_**</dt> </dl>                                                                  | Keine Gültigkeits Überprüfung erfolgt.<br/>                                                                                                                                                                                                                                                                                                                                                           |
| <span id="CAPICOM_CHECK_OFFLINE_ALL"></span><span id="capicom_check_offline_all"></span><dl> <dt>**CAPICOM \_ - \_ Prüfung \_ alle Offline**</dt> </dl>                                            | Prüft alle offline. Sperr Überprüfungen werden für alle Zertifikate in der Kette mit Ausnahme des Stamm Zertifikats durchgeführt. Eingeführt in CAPICOM 2,0.<br/>                                                                                                                                                                                                                                        |
| <span id="CAPICOM_CHECK_ONLINE_ALL"></span><span id="capicom_check_online_all"></span><dl> <dt>**CAPICOM \_ \_ Online \_ alle überprüfen**</dt> </dl>                                               | Überprüft alle Online. Sperr Überprüfungen werden für alle Zertifikate in der Kette mit Ausnahme des Stamm Zertifikats durchgeführt. Eingeführt in CAPICOM 2,0.<br/>                                                                                                                                                                                                                                         |
| <span id="CAPICOM_CHECK_OFFLINE_REVOCATION_STATUS"></span><span id="capicom_check_offline_revocation_status"></span><dl> <dt>**CAPICOM- \_ Überprüfung des \_ Offline Sperr \_ \_ Status**</dt> </dl> | Überprüft den Sperr Status aller Zertifikate in der Kette, die ausschließlich offline-CRLs verwenden.<br/>                                                                                                                                                                                                                                                                                                  |
| <span id="CAPICOM_CHECK_ONLINE_REVOCATION_STATUS"></span><span id="capicom_check_online_revocation_status"></span><dl> <dt>**CAPICOM \_ \_ -Online \_ Sperr \_ Status überprüfen**</dt> </dl>    | Überprüft den Sperr Status aller Zertifikate in der Kette mithilfe der Online verfügbaren CRLs. CRLs werden mithilfe der CDP-Erweiterung im Zertifikat heruntergeladen.<br/> Wenn die CRL heruntergeladen wurde und noch nicht abgelaufen ist, wird Sie von CAPICOM verwendet und nicht online geschaltet.<br/> Wenn eine Zertifikat Sperr Liste nicht heruntergeladen wurde oder veraltet ist, wechselt CAPICOM zum Versuch, die CRL herunterzuladen.<br/> |
| <span id="CAPICOM_CHECK_SIGNATURE_VALIDITY"></span><span id="capicom_check_signature_validity"></span><dl> <dt>**CAPICOM- \_ Überprüfung der \_ Signatur \_ Gültigkeit**</dt> </dl>                       | Prüft auf gültige Signaturen für alle Zertifikate in der Kette.<br/>                                                                                                                                                                                                                                                                                                                           |
| <span id="CAPICOM_CHECK_TIME_VALIDITY"></span><span id="capicom_check_time_validity"></span><dl> <dt>**\_ \_ Gültigkeitsdauer für CAPICOM-Prüfung \_**</dt> </dl>                                      | Überprüft die Gültigkeitsdauer aller Zertifikate in der Kette.<br/>                                                                                                                                                                                                                                                                                                                              |
| <span id="CAPICOM_CHECK_TRUSTED_ROOT"></span><span id="capicom_check_trusted_root"></span><dl> <dt>**CAPICOM- \_ Überprüfung \_ vertrauenswürdiger Stamm \_**</dt> </dl>                                         | Überprüft, ob ein vertrauenswürdiger Stamm der Zertifikat Kette besteht.<br/>                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
