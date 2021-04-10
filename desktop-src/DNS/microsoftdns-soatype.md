---
title: MicrosoftDNS_SOAType-Klasse
description: Die Unterklasse von MicrosoftDNS \_ resourcerecord, die einen Start of Authority (SOA)-Datensatz darstellt.
ms.assetid: a5e6b6d3-7f5d-42e2-b3ed-2786f7aafb14
keywords:
- DNS-MicrosoftDNS_SOAType Klasse
- DNS-MicrosoftDNS_SOAType Klasse, beschrieben
topic_type:
- apiref
api_name:
- MicrosoftDNS_SOAType
- MicrosoftDNS_SOAType.Modify
- MicrosoftDNS_SOAType.SerialNumber
- MicrosoftDNS_SOAType.PrimaryServer
- MicrosoftDNS_SOAType.ResponsibleParty
- MicrosoftDNS_SOAType.RefreshInterval
- MicrosoftDNS_SOAType.RetryDelay
- MicrosoftDNS_SOAType.ExpireLimit
- MicrosoftDNS_SOAType.MinimumTTL
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a3e7cb617514e2ed7c8692a866cc80dfc639391
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040226"
---
# <a name="microsoftdns_soatype-class"></a>MicrosoftDNS- \_ soatype-Klasse

Die Unterklasse von [**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md) , die einen Start of Authority (SOA)-Datensatz darstellt.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
class MicrosoftDNS_SOAType : MicrosoftDNS_ResourceRecord
{
  uint32 SerialNumber;
  string PrimaryServer;
  string ResponsibleParty;
  uint32 RefreshInterval;
  uint32 RetryDelay;
  uint32 ExpireLimit;
  uint32 MinimumTTL;
};
```

## <a name="members"></a>Member

Die **MicrosoftDNS- \_ soatype** -Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **MicrosoftDNS- \_ soatype** -Klasse verfügt über diese Methoden.



| Methode     | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|:-----------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Modify** | Aktualisiert die TTL, die SOA-Seriennummer, den primären Server, die verantwortliche Partei, das Aktualisierungs Intervall, die Wiederholungs Verzögerung, das Ablauf Limit und die minimale Gültigkeitsdauer (für die Zone) auf die Werte, die als Eingabeparameter dieser Methode angegeben werden. Wenn kein neuer Wert für einen Parameter angegeben wird, wird der aktuelle Wert für den Parameter nicht geändert. Die-Methode gibt einen Verweis auf das geänderte-Objekt als Output-Parameter zurück. <br/> Qualifizierer: Implementiert<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **MicrosoftDNS- \_ soatype** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Expirelimit**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Zeit in Sekunden, bevor eine nicht reagierende Zone nicht mehr autorisierend ist.

</dd> <dt>

**Minimumttl**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Niedrigerer Grenzwert für die Zeit (in Sekunden), die ein DNS-Server oder ein cacheresolver einen beliebigen Ressourcen Daten Satz aus der Zone Zwischenspeichern darf, zu der dieser Datensatz gehört.

</dd> <dt>

**PrimaryServer**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Autorisierender DNS-Server für die Zone, zu der der Datensatz gehört.

</dd> <dt>

**RefreshInterval**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Zeit in Sekunden, bevor die Zone, in der dieser Datensatz enthalten ist, aktualisiert werden soll.

</dd> <dt>

**Verantwortliche Partei**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name der verantwortlichen Partei für die Zone, zu der der Datensatz gehört.

</dd> <dt>

**RetryDelay**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Zeit (in Sekunden) vor dem erneuten Versuch einer fehlgeschlagenen Aktualisierung der Zone, zu der dieser Datensatz gehört.

</dd> <dt>

**SerialNumber**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Seriennummer des SOA-Datensatzes.

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

[**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md)
</dt> <dt>

[**Modify-Methode der MicrosoftDNS- \_ soatype-Klasse**](microsoftdns-soatype-modify.md)
</dt> </dl>

 

 





