---
title: MicrosoftDNS_WINSRType-Klasse
description: Die Unterklasse von MicrosoftDNS \_ resourcerecord, die einen WINS-Reverse-Nachschlage Eintrag (WINSR) darstellt.
ms.assetid: e611dc63-838f-4a79-baca-febd27612111
keywords:
- DNS-MicrosoftDNS_WINSRType Klasse
- DNS-MicrosoftDNS_WINSRType Klasse, beschrieben
topic_type:
- apiref
api_name:
- MicrosoftDNS_WINSRType
- MicrosoftDNS_WINSRType.CreateInstanceFromPropertyData
- MicrosoftDNS_WINSRType.Modify
- MicrosoftDNS_WINSRType.MappingFlag
- MicrosoftDNS_WINSRType.LookupTimeout
- MicrosoftDNS_WINSRType.CacheTimeout
- MicrosoftDNS_WINSRType.ResultDomain
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9500c6a36a1c3a7cc243f1cbcfbc0edca6cecf2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392184"
---
# <a name="microsoftdns_winsrtype-class"></a>MicrosoftDNS \_ winsrtype-Klasse

Die Unterklasse von [**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md) , die einen WINS-Reverse-Nachschlage Eintrag (WINSR) darstellt.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
class MicrosoftDNS_WINSRType : MicrosoftDNS_ResourceRecord
{
  uint32 MappingFlag;
  uint32 LookupTimeout;
  uint32 CacheTimeout;
  string ResultDomain;
};
```

## <a name="members"></a>Member

Die **MicrosoftDNS \_ winsrtype** -Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **MicrosoftDNS \_ winsrtype** -Klasse verfügt über diese Methoden.



| Methode                             | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                     |
|:-----------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **"Kreateinzustancefrompropertydata"** | Instanziiert einen WINSR-Typ von RR auf der Grundlage der Daten in den Eingabe Parametern der Methode: dem DNS-Server Namen des Datensatzes, dem Container Namen, dem Besitzer Namen, der Klasse (Standard = in), dem Gültigkeitsdauer Wert und dem WINS-ZuordnungsFlag, dem Reverse-Nachschlage Timeout, dem WINS-Cache Timeout und dem anzufügende Domänen Namen Es wird ein Verweis auf das neue-Objekt als Output-Parameter zurückgegeben. <br/> Qualifizierer: implementiert, statisch<br/> |
| **Modify**                         | Aktualisiert die Gültigkeitsdauer, das ZuordnungsFlag, das Nachschlage Timeout, den Cache Timeout und die Ergebnis Domäne auf die Werte, die als Eingabeparameter dieser Methode angegeben sind. Wenn kein neuer Wert für einen Parameter angegeben wird, wird der aktuelle Wert für den Parameter nicht geändert. Die-Methode gibt einen Verweis auf das geänderte-Objekt als Output-Parameter zurück. <br/> Qualifizierer: Implementiert<br/>                        |



 

### <a name="properties"></a>Eigenschaften

Die **MicrosoftDNS \_ winsrtype** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**CacheTimeout**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Zeit in Sekunden, für die ein DNS-Server mit WINS-Suche die Antwort des WINS-Servers zwischenspeichern kann.

</dd> <dt>

**Lookuptimeout**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Timeout (in Sekunden) für einen DNS-Server mit umgekehrter WINS-Suche.

</dd> <dt>

**Mappingflag**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das WINSR-ZuordnungsFlag, das angibt, ob der Datensatz in die Zonen Replikation eingeschlossen werden muss. Sie kann nur zwei Werte aufweisen: 0x80000000 und 0x00010000 bis, die den Replikations-und No-Replication-Flags (local Record) entsprechen.

</dd> <dt>

**Resultdomain**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Domänen Name, der an zurückgegebene NetBIOS-Namen angehängt werden soll.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Namespace<br/>                | \\MicrosoftDNS-Stamm<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov. MOF</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Die Methode "kreateinstancefrompropertydata" der MicrosoftDNS- \_ Klasse "winsrtype"**](microsoftdns-winsrtype-createinstancefrompropertydata.md)
</dt> <dt>

[**Modify-Methode der MicrosoftDNS \_ winsrtype-Klasse**](microsoftdns-winsrtype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





