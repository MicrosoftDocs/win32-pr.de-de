---
title: MicrosoftDNS_ResourceRecord-Klasse
description: Die MicrosoftDNS \_ resourcerecord-Klasse stellt die allgemeinen Eigenschaften eines DNS RR dar. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 84d6d106-fcc9-44ae-8db2-181c60489aec
keywords:
- DNS-MicrosoftDNS_ResourceRecord Klasse
- DNS-MicrosoftDNS_ResourceRecord Klasse, beschrieben
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
ms.openlocfilehash: abe546ceabb5590ccd4907448af5efd5e2d4fe2f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956622"
---
# <a name="microsoftdns_resourcerecord-class"></a>MicrosoftDNS \_ resourcerecord-Klasse

Die **MicrosoftDNS \_ resourcerecord** -Klasse stellt die allgemeinen Eigenschaften eines DNS RR dar.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

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

Die **MicrosoftDNS \_ resourcerecord** -Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **MicrosoftDNS \_ resourcerecord** -Klasse verfügt über diese Methoden.



| Methode                                   | BESCHREIBUNG                                                                                                                                                                                                                                                            |
|:-----------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **"Kreateingestancefromtextrepresentation"** | Analysiert den RR in der textrepresentation-Zeichenfolge und mit dem eingegebenen DNS-Server und den Container Namen, definiert und instanziiert ein resourcerecord-Objekt. Die-Methode gibt einen Verweis auf das neue-Objekt als Ausgabeparameter zurück. <br/> Qualifizierer: keine<br/> |
| **Getobjectbytextrepresentation**        | Ruft eine vorhandene Instanz der MicrosoftDNS \_ resourcerecord-Unterklasse ab, die von der textrepresentation-Zeichenfolge zusammen mit dem DNS-Server und dem Container Namen dargestellt wird. <br/> Qualifizierer: keine<br/>                                                        |



 

### <a name="properties"></a>Eigenschaften

Die **MicrosoftDNS \_ resourcerecord** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Container Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den Namen des Containers für die Zone, den Cache oder die roothints-Instanz an, die das RR enthält.

</dd> <dt>

**Dnsservername**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den voll qualifizierten Namen oder die IP-Adresse des DNS-Servers an, der den RR enthält.

</dd> <dt>

**DomainName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Stellt den voll qualifizierten Domänen Namen der Domäne dar, die den RR enthält. Diese Eigenschaft kann die Zeichen folgen enthalten \\ . Cache \\ oder \\ .. Roothints \\ , wenn der interne Cache oder die roothints den RR-bzw. den RR enthalten.

</dd> <dt>

**OwnerName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Besitzer Name für die RR.

</dd> <dt>

**Recordclass = 1**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

* * Windows Server 2003: * *

Diese Zeichenfolge stellt die Klasse des Ressourcen Datensatzes dar. Gültige Werte:

1: in (Internet)

2: CS (CSNET)

3: ch (Chaos)

4: HS (Hesiod)

</dd> <dt>

**Recorddata**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ressourcen Daten Satz Daten.

</dd> <dt>

**Textrepresentation**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Text Darstellung des gesamten RR-Werts.

</dd> <dt>

**Zeitstempel**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Zeitpunkt, zu dem die RR zuletzt aktualisiert wurde, ausgedrückt in verstrichenen Stunden seit dem 1. Januar 1601, Greenwich Mean Time (GMT).

</dd> <dt>

**TTL**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Zeit (in Sekunden), die der RR von einem DNS- [*Konflikt Löser*](r-gly.md)zwischengespeichert werden kann.

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

[**Methode "kreateinzustancefromtextrepresentation" der MicrosoftDNS \_ resourcerecord-Klasse**](microsoftdns-resourcerecord-createinstancefromtextrepresentation.md)
</dt> <dt>

[**Getobjectbytextrepresentation-Methode der MicrosoftDNS \_ resourcerecord-Klasse**](microsoftdns-resourcerecord-getobjectbytextrepresentation.md)
</dt> </dl>

 

 





