---
title: MicrosoftDNS_ResourceRecord-Klasse
description: Die MicrosoftDNS \_ ResourceRecord-Klasse stellt die allgemeinen Eigenschaften einer DNS-RR dar. Die folgende Syntax wird durch MOF-Code vereinfacht.
ms.assetid: 84d6d106-fcc9-44ae-8db2-181c60489aec
keywords:
- MicrosoftDNS_ResourceRecord DNS-Klasse
- MicrosoftDNS_ResourceRecord DNS-Klasse , beschrieben
topic_type:
- apiref
api_name:
- MicrosoftDNS_ResourceRecord
- MicrosoftDNS_ResourceRecord.CreateInstanceFromTextRepresentation
- MicrosoftDNS_ResourceRecord.GetObjectByTextRepresentation
- MicrosoftDNS_ResourceRecord.DnsServerName
- MicrosoftDNS_ResourceRecord.ContainerName
- MicrosoftDNS_ResourceRecord.DomainName
- MicrosoftDNS_ResourceRecord.OwnerName
- MicrosoftDNS_ResourceRecord.RecordClass 1
- MicrosoftDNS_ResourceRecord.TTL
- MicrosoftDNS_ResourceRecord.TimeStamp
- MicrosoftDNS_ResourceRecord.RecordData
- MicrosoftDNS_ResourceRecord.TextRepresentation
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b54d23ae522291a2a38ad5d3f046fc444efdefd4d270519fbc3a2ee5739ba47
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874800"
---
# <a name="microsoftdns_resourcerecord-class"></a>MicrosoftDNS \_ ResourceRecord-Klasse

Die **MicrosoftDNS \_ ResourceRecord-Klasse** stellt die allgemeinen Eigenschaften einer DNS-RR dar.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
class MicrosoftDNS_ResourceRecord : CIM_LogicalElement
{
  string DnsServerName;
  string ContainerName;
  string DomainName;
  string OwnerName;
  uint16 RecordClass=1;
  uint32 TTL;
  uint32 TimeStamp;
  string RecordData;
  string TextRepresentation;
};
```

## <a name="members"></a>Member

Die **MicrosoftDNS \_ ResourceRecord-Klasse** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **MicrosoftDNS \_ ResourceRecord-Klasse** verfügt über diese Methoden.



| Methode                                   | BESCHREIBUNG                                                                                                                                                                                                                                                            |
|:-----------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromTextRepresentation** | Analysiert die RR in der TextRepresentation-Zeichenfolge und mit den EINGABE-DNS-Server- und Containernamen, definiert und instanziiert ein ResourceRecord-Objekt. Die -Methode gibt einen Verweis auf das neue -Objekt als Ausgabeparameter zurück. <br/> Qualifizierer: keine<br/> |
| **GetObjectByTextRepresentation**        | Ruft eine vorhandene Instanz der MicrosoftDns ResourceRecord-Unterklasse ab, die durch die TextRepresentation-Zeichenfolge zusammen mit dem \_ DNS-Server und dem Containernamen dargestellt wird. <br/> Qualifizierer: keine<br/>                                                        |



 

### <a name="properties"></a>Eigenschaften

Die **MicrosoftDNS \_ ResourceRecord-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**ContainerName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den Namen des Containers für die Zone-, Cache- oder RootHints-Instanz an, die die RR enthält.

</dd> <dt>

**DnsServerName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den FQDN oder die IP-Adresse des DNS-Servers an, der die RR enthält.

</dd> <dt>

**DomainName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Stellt den FQDN der Domäne dar, die die RR enthält. Diese Eigenschaft kann die Zeichenfolgen \\ enthalten. Cache \\ oder \\ . RootHints, \\ wenn der interne Cache bzw. RootHints die RR enthalten.

</dd> <dt>

**OwnerName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Besitzername für die RR.

</dd> <dt>

**RecordClass=1**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**Windows Server 2003: **

Diese Zeichenfolge stellt die Klasse des Ressourcendatensatz dar. Gültige Werte:

1: IN (Internet)

2: CS (CSNET)

3: CH (CHAOS)

4: HS (Hesiod)

</dd> <dt>

**RecordData**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ressourcendatensatzdaten.

</dd> <dt>

**TextRepresentation**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Textdarstellung der gesamten RR.

</dd> <dt>

**Timestamp**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Zeitpunkt der letzten Aktualisierung der RR, ausgedrückt in verstrichenen Stunden seit dem 1. Januar 1601, Greenwich Mean Time (GMT).

</dd> <dt>

**TTL**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Zeit in Sekunden, die die RR von einem DNS-Resolver [*zwischengespeichert werden kann.*](r-gly.md)

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Namespace<br/>                | \\MicrosoftDNS-Stamm<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov.mof</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CreateInstanceFromTextRepresentation-Methode der MicrosoftDNS \_ ResourceRecord-Klasse**](microsoftdns-resourcerecord-createinstancefromtextrepresentation.md)
</dt> <dt>

[**GetObjectByTextRepresentation-Methode der MicrosoftDNS \_ ResourceRecord-Klasse**](microsoftdns-resourcerecord-getobjectbytextrepresentation.md)
</dt> </dl>

 

 





