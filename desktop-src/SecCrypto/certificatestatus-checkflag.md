---
description: Legt die Gültigkeitsprüfungsflags für ein Zertifikat fest oder ruft sie ab.
ms.assetid: c80c95a0-8a9b-441d-b243-7ee0552731e4
title: CertificateStatus.CheckFlag (Eigenschaft)
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
ms.openlocfilehash: 1c47d7f1c59ecd629db1d6fc735f61b8d1fe59c864ffa8a5a9f013c86bd30faa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877450"
---
# <a name="certificatestatuscheckflag-property"></a>CertificateStatus.CheckFlag (Eigenschaft)

\[CAPICOM ist eine 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509ChainStatus-Struktur**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) im [**Namespace System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Die **CheckFlag-Eigenschaft** legt die Gültigkeitsprüfungsflags für ein Zertifikat fest oder ruft sie ab.

## <a name="syntax"></a>Syntax


```VB
CertificateStatus.CheckFlag As CAPICOM_CHECK_FLAG
```



## <a name="property-value"></a>Eigenschaftswert

Ein Wert der [**CAPICOM \_ CHECK \_ FLAG-Enumeration,**](capicom-check-flag.md) der die Gültigkeitsprüfungen für das Zertifikat beschreibt. Der Standardwert ist **CAPICOM \_ CHECK ONLINE \_ \_ ALL.**

**CAPICOM 2.0.0.3/2.0.0.2/2.0.0.1:** Der Standardwert ist [**CAPICOM \_ CHECK SIGNATURE \_ \_ VALIDITY,**](capicom-check-flag.md) [**CAPICOM \_ CHECK TIME \_ \_ VALIDITY,**](capicom-check-flag.md) [**CAPICOM \_ CHECK TRUSTED \_ \_ ROOT**](capicom-check-flag.md)UND [**CAPICOM \_ CHECK COMPLETE \_ \_ CHAIN.**](capicom-check-flag.md)

**CAPICOM 2.0 und früher:** Der Standardwert ist [**CAPICOM \_ CHECK SIGNATURE \_ \_ VALIDITY,**](capicom-check-flag.md) [**CAPICOM \_ CHECK TIME \_ \_ VALIDITY**](capicom-check-flag.md)und [**CAPICOM \_ CHECK TRUSTED \_ \_ ROOT.**](capicom-check-flag.md)

In der folgenden Tabelle sind die möglichen Werte aufgeführt.



| Wert                                                                                                                                                                                                                                          | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_CHECK_BASIC_CONSTRAINTS"></span><span id="capicom_check_basic_constraints"></span><dl> <dt>**CAPICOM \_ CHECK \_ BASIC \_ CONSTRAINTS**</dt> </dl>                          | Überprüft grundlegende Einschränkungen. Eingeführt in CAPICOM 2.0.<br/>                                                                                                                                                                                                                                                                                                                                    |
| <span id="CAPICOM_CHECK_COMPLETE_CHAIN"></span><span id="capicom_check_complete_chain"></span><dl> <dt>**CAPICOM \_ CHECK \_ COMPLETE \_ CHAIN**</dt> </dl>                                   | Überprüft die gesamte Kette. Eingeführt in CAPICOM 2.0.<br/>                                                                                                                                                                                                                                                                                                                                   |
| <span id="CAPICOM_CHECK_NAME_CONSTRAINTS"></span><span id="capicom_check_name_constraints"></span><dl> <dt>**CAPICOM \_ CHECK \_ NAME \_ CONSTRAINTS**</dt> </dl>                             | Überprüft Namenseinschränkungen. Eingeführt in CAPICOM 2.0.<br/>                                                                                                                                                                                                                                                                                                                                     |
| <span id="CAPICOM_CHECK_NESTED_VALIDITY_PERIOD"></span><span id="capicom_check_nested_validity_period"></span><dl> <dt>**CAPICOM \_ CHECK \_ NESTED \_ VALIDITY \_ PERIOD**</dt> </dl>          | Überprüft die geschachtelte Gültigkeit. Eingeführt in CAPICOM 2.0.<br/>                                                                                                                                                                                                                                                                                                                                      |
| <span id="CAPICOM_CHECK_NONE"></span><span id="capicom_check_none"></span><dl> <dt>**CAPICOM \_ CHECK \_ NONE**</dt> </dl>                                                                  | Es wird keine Gültigkeitsprüfung durchgeführt.<br/>                                                                                                                                                                                                                                                                                                                                                           |
| <span id="CAPICOM_CHECK_OFFLINE_ALL"></span><span id="capicom_check_offline_all"></span><dl> <dt>**CAPICOM \_ CHECK \_ OFFLINE \_ ALL**</dt> </dl>                                            | Überprüft alle offline. Sperrprüfungen werden für alle Zertifikate in der Kette mit Ausnahme des Stammzertifikats ausgeführt. Eingeführt in CAPICOM 2.0.<br/>                                                                                                                                                                                                                                        |
| <span id="CAPICOM_CHECK_ONLINE_ALL"></span><span id="capicom_check_online_all"></span><dl> <dt>**CAPICOM \_ CHECK \_ ONLINE \_ ALL**</dt> </dl>                                               | Überprüft alle Online-. Sperrprüfungen werden für alle Zertifikate in der Kette mit Ausnahme des Stammzertifikats ausgeführt. Eingeführt in CAPICOM 2.0.<br/>                                                                                                                                                                                                                                         |
| <span id="CAPICOM_CHECK_OFFLINE_REVOCATION_STATUS"></span><span id="capicom_check_offline_revocation_status"></span><dl> <dt>**CAPICOM \_ CHECK \_ OFFLINE \_ REVOCATION \_ STATUS**</dt> </dl> | Überprüft den Sperrstatus aller Zertifikate in der Kette nur mithilfe von Offline-CRLs.<br/>                                                                                                                                                                                                                                                                                                  |
| <span id="CAPICOM_CHECK_ONLINE_REVOCATION_STATUS"></span><span id="capicom_check_online_revocation_status"></span><dl> <dt>**CAPICOM \_ CHECK \_ ONLINE \_ REVOCATION \_ STATUS**</dt> </dl>    | Überprüft den Sperrstatus aller Zertifikate in der Kette mithilfe online verfügbarer Zertifikatsperrlisten. Zertifikatsperrlisten werden mithilfe der CDP-Erweiterung im Zertifikat heruntergeladen.<br/> Wenn die Zertifikatsperrliste heruntergeladen wurde und noch nicht abgelaufen ist, verwendet CAPICOM sie und geht nicht online.<br/> Wenn eine Zertifikatsperrliste nicht heruntergeladen wurde oder veraltet ist, geht CAPICOM online, um zu versuchen, die Zertifikatsperrliste herunterzuladen.<br/> |
| <span id="CAPICOM_CHECK_SIGNATURE_VALIDITY"></span><span id="capicom_check_signature_validity"></span><dl> <dt>**CAPICOM \_ CHECK \_ SIGNATURE \_ VALIDITY**</dt> </dl>                       | Überprüft auf gültige Signaturen für alle Zertifikate in der Kette.<br/>                                                                                                                                                                                                                                                                                                                           |
| <span id="CAPICOM_CHECK_TIME_VALIDITY"></span><span id="capicom_check_time_validity"></span><dl> <dt>**CAPICOM CHECK TIME VALIDITY (GÜLTIGKEIT \_ \_ DER \_ CAPICOM-ÜBERPRÜFUNGSZEIT)**</dt> </dl>                                      | Überprüft die Gültigkeit aller Zertifikate in der Kette.<br/>                                                                                                                                                                                                                                                                                                                              |
| <span id="CAPICOM_CHECK_TRUSTED_ROOT"></span><span id="capicom_check_trusted_root"></span><dl> <dt>**CAPICOM \_ CHECK \_ TRUSTED \_ ROOT**</dt> </dl>                                         | Sucht nach einem vertrauenswürdigen Stamm der Zertifikatkette.<br/>                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
