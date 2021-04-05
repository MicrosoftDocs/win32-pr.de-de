---
title: MicrosoftDNS_WINSType-Klasse
description: Die Unterklasse von MicrosoftDNS \_ resourcerecord, die einen WINS-Datensatz (Windows Internet Name Service) darstellt.
ms.assetid: 8f891d80-ee4d-4641-8a6c-159c78e5cf86
keywords:
- DNS-MicrosoftDNS_WINSType Klasse
- DNS-MicrosoftDNS_WINSType Klasse, beschrieben
topic_type:
- apiref
api_name:
- MicrosoftDNS_WINSType
- MicrosoftDNS_WINSType.CreateInstanceFromPropertyData
- MicrosoftDNS_WINSType.Modify
- MicrosoftDNS_WINSType.MappingFlag
- MicrosoftDNS_WINSType.LookupTimeout
- MicrosoftDNS_WINSType.CacheTimeout
- MicrosoftDNS_WINSType.WinsServers
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce23132073305142948518327ea5b6c7e46f1289
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859040"
---
# <a name="microsoftdns_winstype-class"></a>MicrosoftDNS- \_ winstype-Klasse

Die Unterklasse von [**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md) , die einen WINS-Datensatz (Windows Internet Name Service) darstellt.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
class MicrosoftDNS_WINSType : MicrosoftDNS_ResourceRecord
{
  uint32 MappingFlag;
  uint32 LookupTimeout;
  uint32 CacheTimeout;
  string WinsServers;
};
```

## <a name="members"></a>Member

Die **MicrosoftDNS- \_ winstype** -Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **MicrosoftDNS- \_ winstype** -Klasse verfügt über diese Methoden.



| Methode                             | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                  |
|:-----------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **"Kreateinzustancefrompropertydata"** | Instanziiert einen WINS-Typ von RR basierend auf den Daten in den Eingabe Parametern der Methode: dem DNS-Server Namen des Datensatzes, dem Container Namen, dem Besitzer Namen, der Klasse (Standard = in), dem Wert für die Gültigkeitsdauer und dem WINS-ZuordnungsFlag, dem Such Timeout, dem Cache Timeout und der Liste der IP-Adressen für die Suche. Es wird ein Verweis auf das neue-Objekt als Output-Parameter zurückgegeben. <br/> Qualifizierer: implementiert, statisch<br/> |
| **Modify**                         | Aktualisiert die Gültigkeitsdauer, das ZuordnungsFlag, das Nachschlage Timeout, den Cache Timeout und die WINS-Server auf die Werte, die als Eingabeparameter dieser Methode angegeben sind. Wenn kein neuer Wert für einen Parameter angegeben wird, wird der aktuelle Wert für den Parameter nicht geändert. Die-Methode gibt einen Verweis auf das geänderte-Objekt als Output-Parameter zurück. <br/> Qualifizierer: Implementiert<br/>                      |



 

### <a name="properties"></a>Eigenschaften

Die **MicrosoftDNS- \_ winstype** -Klasse verfügt über diese Eigenschaften.

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

Zeit (in Sekunden), die ein DNS-Server versucht, mithilfe von WINS eine Auflösung durchsuchen zu können.

</dd> <dt>

**Mappingflag**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

WINS-ZuordnungsFlag, das angibt, ob der Datensatz in die Zonen Replikation eingeschlossen werden muss. Sie kann nur zwei Werte aufweisen: 0x80000000 und 0x00010000 bis, die den Replikations-und No-Replication-Flags (local Record) entsprechen. Die folgenden Werte sind gültig.



| Wert                                                                                                                                               | Bedeutung                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="0x80000000"></span><span id="0X80000000"></span><dl> <dt>**0x80000000**</dt> </dl> | Replikationsflag<br/>                   |
| <span id="0x00010000"></span><span id="0X00010000"></span><dl> <dt>**0x00010000**</dt> </dl> | Flag "keine Replikation (lokaler Datensatz)"<br/> |



 

</dd> <dt>

**Windows Server**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Liste mit durch Trennzeichen getrennten IP-Adressen von WINS-Servern, die in WINS-suchen verwendet werden.

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

[**Methode "kreateinzustancefrompropertydata" der MicrosoftDNS- \_ winstype-Klasse**](microsoftdns-winstype-createinstancefrompropertydata.md)
</dt> <dt>

[**Modify-Methode der MicrosoftDNS- \_ winstype-Klasse**](microsoftdns-winstype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





