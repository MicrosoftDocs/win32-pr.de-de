---
description: Gibt ein Zertifikate-Objekt zurück, das alle Zertifikate enthält, die den angegebenen Suchkriterien entsprechen.
ms.assetid: a2b8f4d4-dce3-467b-aaa0-a125056a1dd3
title: 'ICertificates2:: Find-Methode'
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
ms.openlocfilehash: 9ea15891c33a0789e5b6746b55dfd0b0eb602afc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358767"
---
# <a name="icertificates2find-method"></a>ICertificates2:: Find-Methode

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509Certificate2Collection-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]

Die **Find** -Methode gibt ein [**Zertifikate**](certificates.md) -Objekt zurück, das alle Zertifikate enthält, die den angegebenen Suchkriterien entsprechen. Diese Methode wurde in CAPICOM 2,0 eingeführt.

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

*FindType* \[ in\]
</dt> <dd>

Ein Wert des [**CAPICOM- \_ Zertifikats \_ Find \_ Type**](capicom-certificate-find-type.md) -Enumeration, die den Typ der Übereinstimmungs Kriterien angibt, die im *varcriteria* -Parameter angegeben sind. In der folgenden Tabelle sind die möglichen Werte aufgeführt.



| Wert                                                                                                                                                                                                                                                        | Bedeutung                                                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATE_FIND_SHA1_HASH"></span><span id="capicom_certificate_find_sha1_hash"></span><dl> <dt>**CAPICOM- \_ Zertifikat \_ Suche SHA1- \_ \_ Hash**</dt> </dl>                              | Gibt Zertifikate mit einem SHA1-Hash zurück, der mit dem im *varcriteria* -Parameter angegebenen SHA1-Hash übereinstimmt.<br/>                                                                                                                              |
| <span id="CAPICOM_CERTIFICATE_FIND_SUBJECT_NAME"></span><span id="capicom_certificate_find_subject_name"></span><dl> <dt>**CAPICOM-Zertifikat suchantrags Teller \_ \_ \_ \_ Name**</dt> </dl>                     | Gibt Zertifikate zurück, deren Antragsteller Name exakt oder teilweise mit dem im *varcriteria* -Parameter angegebenen Antragsteller Namen übereinstimmt. Dieser Befehl durchsucht nur das Feld "Antragsteller Name".<br/>                                                         |
| <span id="CAPICOM_CERTIFICATE_FIND_ISSUER_NAME"></span><span id="capicom_certificate_find_issuer_name"></span><dl> <dt>**CAPICOM- \_ Zertifikat \_ Suchen des \_ Aussteller \_ namens**</dt> </dl>                        | Gibt Zertifikate zurück, deren Aussteller Namen exakt oder teilweise mit dem im *varcriteria* -Parameter angegebenen Aussteller Namen übereinstimmen. Durch diesen Befehl wird nur das Feld "Aussteller Name" durchsucht.<br/>                                                            |
| <span id="CAPICOM_CERTIFICATE_FIND_ROOT_NAME"></span><span id="capicom_certificate_find_root_name"></span><dl> <dt>**CAPICOM- \_ Zertifikat \_ \_ \_ suchstammname**</dt> </dl>                              | Gibt Zertifikate zurück, deren Stamm Antragsteller Name exakt oder teilweise mit dem im *varcriteria* -Parameter angegebenen Namen des Stamm Subjekts übereinstimmt. Mit diesem Befehl wird eine Kette erstellt. Dieser Befehl durchsucht das Feld "Antragsteller Name" des Stamm Zertifikats.<br/> |
| <span id="CAPICOM_CERTIFICATE_FIND_TEMPLATE_NAME"></span><span id="capicom_certificate_find_template_name"></span><dl> <dt>**CAPICOM- \_ Zertifikat \_ Suchen \_ Vorlagen \_ Name**</dt> </dl>                  | Gibt Zertifikate zurück, deren Vorlagen Name mit dem im *varcriteria* -Parameter angegebenen Vorlagen Namen übereinstimmt.<br/>                                                                                                                            |
| <span id="CAPICOM_CERTIFICATE_FIND_EXTENSION"></span><span id="capicom_certificate_find_extension"></span><dl> <dt>**CAPICOM- \_ Zertifikat \_ Suche- \_ Erweiterung**</dt> </dl>                               | Gibt Zertifikate zurück, die eine Erweiterung aufweisen, die der im *varcriteria* -Parameter angegebenen Erweiterung entspricht.<br/>                                                                                                                        |
| <span id="CAPICOM_CERTIFICATE_FIND_EXTENDED_PROPERTY"></span><span id="capicom_certificate_find_extended_property"></span><dl> <dt>**CAPICOM- \_ Zertifikat für \_ \_ Erweiterte \_ Eigenschaft suchen**</dt> </dl>      | Gibt Zertifikate im Speicher zurück, die explizit eine erweiterte Eigenschaft mit dem im *varcriteria* -Parameter angegebenen Wert enthalten.<br/>                                                                                                 |
| <span id="CAPICOM_CERTIFICATE_FIND_APPLICATION_POLICY"></span><span id="capicom_certificate_find_application_policy"></span><dl> <dt>**CAPICOM- \_ Zertifikat \_ Suche- \_ Anwendungs \_ Richtlinie**</dt> </dl>   | Gibt Zertifikate im Speicher zurück, die entweder über eine erweiterte Schlüssel Verwendungs Erweiterung, eine Anwendungsrichtlinien Erweiterung oder eine erweiterte Eigenschaft verfügen, die im *varcriteria* -Parameter angegeben ist.<br/>                                                        |
| <span id="CAPICOM_CERTIFICATE_FIND_CERTIFICATE_POLICY"></span><span id="capicom_certificate_find_certificate_policy"></span><dl> <dt>**CAPICOM- \_ Zertifikat Zertifikat \_ \_ \_ Richtlinie suchen**</dt> </dl>   | Gibt Zertifikate zurück, die die Richtlinien-OID in der Zertifikat Richtlinien Erweiterung enthalten, die im *varcriteria* -Parameter angegeben ist.<br/>                                                                                                          |
| <span id="CAPICOM_CERTIFICATE_FIND_TIME_VALID"></span><span id="capicom_certificate_find_time_valid"></span><dl> <dt>**zulässige Zeit für CAPICOM- \_ Zertifikat \_ Suche \_ \_ gültig**</dt> </dl>                           | Gibt Zertifikate zurück, deren Zeit gültig ist.<br/>                                                                                                                                                                                               |
| <span id="CAPICOM_CERTIFICATE_FIND_TIME_NOT_YET_VALID"></span><span id="capicom_certificate_find_time_not_yet_valid"></span><dl> <dt>**Das CAPICOM- \_ Zertifikat ist \_ \_ \_ \_ noch nicht \_ gültig.**</dt> </dl> | Gibt Zertifikate zurück, deren Zeit noch nicht gültig ist.<br/>                                                                                                                                                                                       |
| <span id="CAPICOM_CERTIFICATE_FIND_TIME_EXPIRED"></span><span id="capicom_certificate_find_time_expired"></span><dl> <dt>**Zeit für das CAPICOM- \_ Zertifikat ist \_ \_ \_ abgelaufen.**</dt> </dl>                     | Gibt Zertifikate zurück, deren Zeit abgelaufen ist.<br/>                                                                                                                                                                                            |
| <span id="CAPICOM_CERTIFICATE_FIND_KEY_USAGE"></span><span id="capicom_certificate_find_key_usage"></span><dl> <dt>**CAPICOM- \_ Zertifikat \_ Suche \_ Schlüssel \_ Verwendung**</dt> </dl>                              | Gibt Zertifikate zurück, die Schlüssel Verwendungen in der im *varcriteria* -Parameter angegebenen KeyUsage-Erweiterung enthalten. Wenn die KeyUsage-Erweiterung nicht vorhanden ist, wird davon ausgegangen, dass alle Schlüssel Verwendungen nicht verfügbar sind.<br/>                           |



 

</dd> <dt>

*varcriteria* \[ in, optional\]
</dt> <dd>

Eine Variante, die die Suchkriterien enthält. Diese Daten müssen mit dem Typ der im *FindType* -Parameter angegebenen Daten identisch sein. Wenn der Wert des *FindType* -Parameters "CAPICOM \_ Certificate \_ Find \_ time \_ valid", "CAPICOM \_ Certificate Find Time" \_ \_ \_ \_ noch nicht gültig ist oder die \_ CAPICOM \_ \_ -Zertifikat Suche \_ Zeit abgelaufen ist \_ und Sie keinen Wert an diesen Parameter übergeben, wird die aktuelle Zeit angenommen. Beispiele für jeden Datentyp finden Sie unter "Hinweise". Der Standardwert ist 0.

</dd> <dt>

*bfindvalidonly* \[ in, optional\]
</dt> <dd>

Ein boolescher Wert, der angibt, ob nur gültige Zertifikate zurückgegeben werden. Der Standardwert ist false. Dies gibt an, dass alle Zertifikate zurückgegeben werden, die mit den Suchkriterien übereinstimmen.

True gibt an, dass bei der Suche nicht die folgenden Zertifikat Typen zurückgegeben werden:

-   Zertifikate, deren Zeit abgelaufen ist oder noch nicht gültig ist.
-   Zertifikate sind nicht ordnungsgemäß verkettet.
-   Zertifikate, die über Signatur Probleme verfügen.
-   Zertifikate, die widerrufen werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Ein [**Zertifikate**](certificates.md) -Objekt, das die Ergebnisse der Suche enthält.

**CAPICOM 2,1:** Das [**Zertifikat**](certificates.md) Objekt, das zurückgegeben wird, enthält Verweise auf die Zertifikate in der Sammlung, in der die Suche durchgeführt wurde. Alle Änderungen, die an den Zertifikaten im zurückgegebenen **Zertifikat** Objekt vorgenommen werden, werden in dieser Sammlung widergespiegelt.

**CAPICOM 2,0, CAPICOM 2.0.0.1, CAPICOM 2.0.0.2 und CAPICOM 2.0.0.3:** Das [**Zertifikat**](certificates.md) Objekt, das zurückgegeben wird, enthält Kopien der Zertifikate in der Sammlung, in der die Suche durchgeführt wurde. Alle Änderungen, die an den Zertifikaten im zurückgegebenen **Zertifikat** Objekt vorgenommen werden, werden in dieser Sammlung nicht widergespiegelt.

## <a name="remarks"></a>Bemerkungen

In den folgenden Beispielen werden mögliche Suchkriterien für die verschiedenen Typen von Suchkriterien angezeigt.



| *FindType* -Parameter                              | *varcriteria* -Parameter                                                                                                            |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| CAPICOM- \_ Zertifikat \_ Suche SHA1- \_ \_ Hash            | 33f362434b577f844bb7226be36f7d72ef9d9393                                                                                           |
| CAPICOM-Zertifikat suchantrags Teller \_ \_ \_ \_ Name         | "Nameof"                                                                                                                     |
| CAPICOM- \_ Zertifikat \_ Suchen des \_ Aussteller \_ namens          | VeriSign                                                                                                                         |
| CAPICOM- \_ Zertifikat \_ \_ \_ suchstammname            | "Microsoft Root Authority"                                                                                                         |
| CAPICOM- \_ Zertifikat \_ Suchen \_ Vorlagen \_ Name        | "Autoeinschreibung"<br/> 1.3.6.1.4.1.311.21.8.3692315854.1256661383.1690418588.4201632533.1741915387.2177932052<br/>       |
| CAPICOM- \_ Zertifikat \_ Suche- \_ Erweiterung             | "2.5.29.31"<br/> Erweiterung "CAPICOM \_ OID \_ Key \_ Usage \_ "<br/> "CRL-Verteilerliste"<br/>                           |
| CAPICOM- \_ Zertifikat für \_ \_ Erweiterte \_ Eigenschaft suchen    | Proxy Informationen zu CAPICOM \_ PROPID \_ Key \_ \_                                                                                                   |
| CAPICOM- \_ Zertifikat \_ Suche- \_ Anwendungs \_ Richtlinie   | 1.3.6.1.5.5.7.3.3<br/> 1.3.6.1.5.5.7.3.4<br/> CAPICOM \_ OID \_ Server \_ auth \_ EKU<br/> "Code Signatur"<br/> |
| CAPICOM- \_ Zertifikat Zertifikat \_ \_ \_ Richtlinie suchen   | "1.3.6.1.5.5.7.3.4.3.5"<br/> "Corporate High Assurance"<br/>                                                           |
| zulässige Zeit für CAPICOM- \_ Zertifikat \_ Suche \_ \_ gültig           | \#04/15/2002, 6:00 Uhr\#                                                                                                            |
| Das CAPICOM- \_ Zertifikat ist \_ \_ \_ \_ noch nicht \_ gültig. | \#04/15/2002, 6:00 Uhr\#                                                                                                            |
| Zeit für das CAPICOM- \_ Zertifikat ist \_ \_ \_ abgelaufen.         | \#04/15/2002, 6:00 Uhr\#                                                                                                            |
| CAPICOM- \_ Zertifikat \_ Suche \_ Schlüssel \_ Verwendung            | nur CAPICOM- \_ \_ \_ Schlüssel \_ Verwendung                                                                                                |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Zertifikate**](certificates.md)
</dt> <dt>

[**CAPICOM- \_ OID**](capicom-oid.md)
</dt> </dl>

 

 
