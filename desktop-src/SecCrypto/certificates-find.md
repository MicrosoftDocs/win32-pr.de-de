---
description: Gibt ein Certificates-Objekt zurück, das alle Zertifikate enthält, die den angegebenen Suchkriterien entsprechen.
ms.assetid: a2b8f4d4-dce3-467b-aaa0-a125056a1dd3
title: ICertificates2::Find-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Find
- ICertificates2.Find
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 51e3d19348f0bff9cdbe0b4211d648a25025b2a3ab8feee9df6f804486265857
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100990"
---
# <a name="icertificates2find-method"></a>ICertificates2::Find-Methode

\[CAPICOM ist eine nur 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509Certificate2Collection-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) im [**Namespace System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Die **Find-Methode** gibt ein [**Certificates-Objekt**](certificates.md) zurück, das alle Zertifikate enthält, die den angegebenen Suchkriterien entsprechen. Diese Methode wurde in CAPICOM 2.0 eingeführt.

## <a name="syntax"></a>Syntax


```VB
Certificates.Find( _
  ByVal FindType, _
  [ ByVal varCriteria ], _
  [ ByVal bFindValidOnly ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*FindType* \[ In\]
</dt> <dd>

Ein Wert der [**CAPICOM \_ CERTIFICATE FIND \_ \_ TYPE-Enumeration,**](capicom-certificate-find-type.md) der den Typ der im *varCriteria-Parameter* angegebenen Übereinstimmungskriterien angibt. In der folgenden Tabelle sind die möglichen Werte aufgeführt.



| Wert                                                                                                                                                                                                                                                        | Bedeutung                                                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATE_FIND_SHA1_HASH"></span><span id="capicom_certificate_find_sha1_hash"></span><dl> <dt>**CAPICOM \_ CERTIFICATE \_ FIND \_ SHA1 \_ HASH**</dt> </dl>                              | Gibt Zertifikate mit einem SHA1-Hash zurück, der dem im *varCriteria-Parameter* angegebenen SHA1-Hash entspricht.<br/>                                                                                                                              |
| <span id="CAPICOM_CERTIFICATE_FIND_SUBJECT_NAME"></span><span id="capicom_certificate_find_subject_name"></span><dl> <dt>**NAME \_ DES ANTRAGSTELLERS FÜR CAPICOM-ZERTIFIKATSUCHE \_ \_ \_**</dt> </dl>                     | Gibt Zertifikate zurück, deren Antragstellername genau oder teilweise mit dem im *varCriteria-Parameter* angegebenen Antragstellernamen übereinstimmt. Dieser Aufruf durchsucht nur das Feld "Antragstellername".<br/>                                                         |
| <span id="CAPICOM_CERTIFICATE_FIND_ISSUER_NAME"></span><span id="capicom_certificate_find_issuer_name"></span><dl> <dt>**NAME \_ DES \_ CAPICOM-ZERTIFIKATS ZUM SUCHEN \_ DES \_ AUSSTELLERS**</dt> </dl>                        | Gibt Zertifikate zurück, deren Ausstellername genau oder teilweise mit dem im *varCriteria-Parameter* angegebenen Ausstellernamen übereinstimmt. Dieser Aufruf durchsucht nur das Feld ausstellername.<br/>                                                            |
| <span id="CAPICOM_CERTIFICATE_FIND_ROOT_NAME"></span><span id="capicom_certificate_find_root_name"></span><dl> <dt>**CAPICOM \_ CERTIFICATE \_ FIND \_ ROOT \_ NAME**</dt> </dl>                              | Gibt Zertifikate zurück, deren Name des Stammsubjekts genau oder teilweise mit dem im *varCriteria-Parameter* angegebenen Stammsubjektnamen übereinstimmt. Dieser Aufruf erstellt eine Kette. Dieser Aufruf durchsucht das Feld antragstellername des Stammzertifikats.<br/> |
| <span id="CAPICOM_CERTIFICATE_FIND_TEMPLATE_NAME"></span><span id="capicom_certificate_find_template_name"></span><dl> <dt>**NAME DER \_ \_ \_ CAPICOM-ZERTIFIKATSUCHEVORLAGE \_**</dt> </dl>                  | Gibt Zertifikate zurück, deren Vorlagenname mit dem im *varCriteria-Parameter* angegebenen Vorlagennamen übereinstimmt.<br/>                                                                                                                            |
| <span id="CAPICOM_CERTIFICATE_FIND_EXTENSION"></span><span id="capicom_certificate_find_extension"></span><dl> <dt>**ERWEITERUNG FÜR DIE \_ CAPICOM-ZERTIFIKATSUCHE \_ \_**</dt> </dl>                               | Gibt Zertifikate zurück, die über eine Erweiterung verfügen, die mit der im *varCriteria-Parameter* angegebenen Erweiterung übereinstimmt.<br/>                                                                                                                        |
| <span id="CAPICOM_CERTIFICATE_FIND_EXTENDED_PROPERTY"></span><span id="capicom_certificate_find_extended_property"></span><dl> <dt>**CAPICOM \_ CERTIFICATE \_ FIND \_ EXTENDED \_ PROPERTY**</dt> </dl>      | Gibt Zertifikate im Speicher zurück, die explizit eine erweiterte Eigenschaft mit dem im *varCriteria-Parameter* angegebenen Wert enthalten.<br/>                                                                                                 |
| <span id="CAPICOM_CERTIFICATE_FIND_APPLICATION_POLICY"></span><span id="capicom_certificate_find_application_policy"></span><dl> <dt>**CAPICOM \_ CERTIFICATE \_ FIND \_ APPLICATION \_ POLICY**</dt> </dl>   | Gibt Zertifikate im Speicher zurück, die entweder eine erweiterte Schlüsselverwendungserweiterung, eine Anwendungsrichtlinienerweiterung oder eine erweiterte Eigenschaft aufweisen, die im *varCriteria-Parameter* angegeben ist.<br/>                                                        |
| <span id="CAPICOM_CERTIFICATE_FIND_CERTIFICATE_POLICY"></span><span id="capicom_certificate_find_certificate_policy"></span><dl> <dt>**\_ZERTIFIKATSSUCHE-RICHTLINIE FÜR \_ CAPICOM-ZERTIFIKATE \_ \_**</dt> </dl>   | Gibt Zertifikate zurück, die die Richtlinien-OID in der im *varCriteria-Parameter* angegebenen Zertifikatrichtlinienerweiterung enthalten.<br/>                                                                                                          |
| <span id="CAPICOM_CERTIFICATE_FIND_TIME_VALID"></span><span id="capicom_certificate_find_time_valid"></span><dl> <dt>**CAPICOM \_ CERTIFICATE \_ FIND \_ TIME \_ VALID**</dt> </dl>                           | Gibt Zertifikate zurück, deren Zeit gültig ist.<br/>                                                                                                                                                                                               |
| <span id="CAPICOM_CERTIFICATE_FIND_TIME_NOT_YET_VALID"></span><span id="capicom_certificate_find_time_not_yet_valid"></span><dl> <dt>**CAPICOM \_ CERTIFICATE FIND TIME NOT YET VALID (CAPICOM-ZERTIFIKATSSUCHEZEIT \_ NOCH NICHT \_ \_ \_ \_ GÜLTIG)**</dt> </dl> | Gibt Zertifikate zurück, deren Zeit noch nicht gültig ist.<br/>                                                                                                                                                                                       |
| <span id="CAPICOM_CERTIFICATE_FIND_TIME_EXPIRED"></span><span id="capicom_certificate_find_time_expired"></span><dl> <dt>**ABGELAUFENE ZEIT FÜR \_ CAPICOM-ZERTIFIKATSUCHE \_ \_ \_**</dt> </dl>                     | Gibt Zertifikate zurück, deren Zeit abgelaufen ist.<br/>                                                                                                                                                                                            |
| <span id="CAPICOM_CERTIFICATE_FIND_KEY_USAGE"></span><span id="capicom_certificate_find_key_usage"></span><dl> <dt>**VERWENDUNG DES \_ CAPICOM-ZERTIFIKATS \_ ZUR \_ \_ SCHLÜSSELSUCHE**</dt> </dl>                              | Gibt Zertifikate zurück, die Schlüsselverwendungen in der im *varCriteria-Parameter* angegebenen KeyUsage-Erweiterung enthalten. Wenn die KeyUsage-Erweiterung nicht vorhanden ist, wird davon ausgegangen, dass alle Schlüsselverwendungen nicht verfügbar sind.<br/>                           |



 

</dd> <dt>

*varCriteria* \[ in, optional\]
</dt> <dd>

Eine Variante, die die Suchkriterien enthält. Diese Daten müssen mit dem Im *FindType-Parameter* angegebenen Datentyp übereinstimmen. Wenn der Wert des *FindType-Parameters* CAPICOM \_ CERTIFICATE FIND TIME \_ \_ \_ VALID, CAPICOM \_ CERTIFICATE FIND TIME NOT YET VALID oder \_ \_ \_ \_ \_ CAPICOM CERTIFICATE FIND TIME EXPIRED lautet und Sie \_ keinen Wert an diesen \_ Parameter \_ \_ übergeben, wird die aktuelle Zeit angenommen. Beispiele für jeden Datentyp finden Sie unter Hinweise. Der Standardwert ist 0.

</dd> <dt>

*bFindValidOnly* \[ in, optional\]
</dt> <dd>

Ein boolescher Wert, der angibt, ob nur gültige Zertifikate zurückgegeben werden. Der Standardwert ist "false". gibt an, dass alle Zertifikate zurückgegeben werden, die den Suchkriterien entsprechen.

True gibt bei der Suche nicht die folgenden Zertifikattypen zurück:

-   Zertifikate, deren Zeit abgelaufen ist oder noch nicht gültig ist.
-   Zertifikate werden nicht ordnungsgemäß verkettet.
-   Zertifikate mit Signaturproblemen.
-   Zertifikate, die widerrufen werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

[**Certificates-Objekt,**](certificates.md) das die Ergebnisse der Suche enthält.

**CAPICOM 2.1:** Das [**zurückgegebene Certificates-Objekt**](certificates.md) enthält Verweise auf die Zertifikate in der Auflistung, in der die Suche durchgeführt wurde. Alle Änderungen, die an den Zertifikaten im **zurückgegebenen Certificates-Objekt** vorgenommen werden, werden in dieser Auflistung widergespiegelt.

**CAPICOM 2.0, CAPICOM 2.0.0.1, CAPICOM 2.0.0.2 und CAPICOM 2.0.0.3:** Das [**zurückgegebene Certificates-Objekt**](certificates.md) enthält Kopien der Zertifikate in der Auflistung, in der die Suche durchgeführt wurde. Änderungen an den Zertifikaten im **zurückgegebenen Certificates-Objekt** werden in dieser Auflistung nicht widergespiegelt.

## <a name="remarks"></a>Hinweise

Die folgenden Beispiele zeigen mögliche Suchkriterien für die verschiedenen Suchkriterientypen.



| *FindType-Parameter*                              | *varCriteria-Parameter*                                                                                                            |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| CAPICOM \_ CERTIFICATE \_ FIND \_ SHA1 \_ HASH            | 33F362434B577F844BB7226BE36F7D72EF9D9393                                                                                           |
| NAME \_ DES ANTRAGSTELLERS FÜR CAPICOM-ZERTIFIKATSUCHE \_ \_ \_         | "NameOfPerson"                                                                                                                     |
| NAME \_ DES \_ CAPICOM-ZERTIFIKATS ZUM SUCHEN \_ DES \_ AUSSTELLERS          | "VeriSign"                                                                                                                         |
| CAPICOM \_ CERTIFICATE \_ FIND \_ ROOT \_ NAME            | "Microsoft-Stammzertifizierungsstelle"                                                                                                         |
| NAME DER \_ \_ \_ CAPICOM-ZERTIFIKATSUCHEVORLAGE \_        | "AutoEnrollEFS"<br/> 1.3.6.1.4.1.311.21.8.3692315854.1256661383.1690418588.4201632533.1741915387.2177932052<br/>       |
| ERWEITERUNG FÜR DIE \_ CAPICOM-ZERTIFIKATSUCHE \_ \_             | "2.5.29.31"<br/> \_ \_ \_ CAPICOM-OIDSCHLÜSSELVERWENDUNGSERWEITERUNG \_<br/> "CRL-Verteilerliste"<br/>                           |
| CAPICOM \_ CERTIFICATE \_ FIND \_ EXTENDED \_ PROPERTY    | CAPICOM \_ PROPID \_ KEY \_ PROV \_ INFO                                                                                                   |
| CAPICOM \_ CERTIFICATE \_ FIND \_ APPLICATION \_ POLICY   | "1.3.6.1.5.5.7.3.3"<br/> "1.3.6.1.5.5.7.3.4"<br/> CAPICOM \_ OID \_ SERVER \_ AUTH \_ EKU<br/> "Codesignierung"<br/> |
| \_ZERTIFIKATSSUCHE-RICHTLINIE FÜR \_ CAPICOM-ZERTIFIKATE \_ \_   | "1.3.6.1.5.5.7.3.4.3.5"<br/> "Corporate High Assurance"<br/>                                                           |
| CAPICOM \_ CERTIFICATE \_ FIND \_ TIME \_ VALID           | \#15.04.2002, 18:00 Uhr\#                                                                                                            |
| CAPICOM \_ CERTIFICATE FIND TIME NOT YET VALID (CAPICOM-ZERTIFIKATSSUCHEZEIT \_ NOCH NICHT \_ \_ \_ \_ GÜLTIG) | \#15.04.2002, 18:00 Uhr\#                                                                                                            |
| ABGELAUFENE ZEIT FÜR \_ CAPICOM-ZERTIFIKATSUCHE \_ \_ \_         | \#15.04.2002, 18:00 Uhr\#                                                                                                            |
| CAPICOM \_ CERTIFICATE \_ FIND \_ KEY \_ USAGE            | NUR \_ CAPICOM-ENCIPHER-SCHLÜSSELVERWENDUNG \_ \_ \_                                                                                                |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Zertifikate**](certificates.md)
</dt> <dt>

[**\_CAPICOM-OID**](capicom-oid.md)
</dt> </dl>

 

 
