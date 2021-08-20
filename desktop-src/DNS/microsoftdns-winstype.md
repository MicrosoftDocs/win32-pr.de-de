---
title: MicrosoftDNS_WINSType-Klasse
description: Die Unterklasse von MicrosoftDNS \_ ResourceRecord, die einen Windows WINS-Eintrag (Internet Name Service) darstellt.
ms.assetid: 8f891d80-ee4d-4641-8a6c-159c78e5cf86
keywords:
- dns der MicrosoftDNS_WINSType-Klasse
- MicrosoftDNS_WINSType Dns-Klasse beschrieben
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
ms.openlocfilehash: 089faa6fa3cda6780b600dbf6c296fd1ce71f902428e6c2abe16f92dada1e219
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118162840"
---
# <a name="microsoftdns_winstype-class"></a>MicrosoftDNS \_ WINSType-Klasse

Die Unterklasse von [**MicrosoftDNS \_ ResourceRecord,**](microsoftdns-resourcerecord.md) die einen Windows WINS-Eintrag (Internet Name Service) darstellt.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

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

Die **MicrosoftDNS \_ WINSType-Klasse** verfügt über folgende Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **MicrosoftDNS \_ WINSType-Klasse** verfügt über diese Methoden.



| Methode                             | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                  |
|:-----------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Instanziiert einen WINS-Typ von RR basierend auf den Daten in den Eingabeparametern der Methode: DNS-Servername des Eintrags, Containername, Besitzername, Klasse (Standard = IN), Time-to-Live-Wert und WINS-Zuordnungsflag, Suchtime out, Cachetime out und Liste der IP-Adressen für die Suche. Es gibt einen Verweis auf das neue Objekt als Ausgabeparameter zurück. <br/> Qualifizierer: Implementiert, statisch<br/> |
| **Änderung**                         | Aktualisiert TTL, Zuordnungsflag, Suchtime out, Cachetime out und Wins Servers auf die Werte, die als Eingabeparameter dieser Methode angegeben sind. Wenn kein neuer Wert für einen Parameter angegeben wird, wird der aktuelle Wert für den Parameter nicht geändert. Die -Methode gibt einen Verweis auf das geänderte Objekt als Ausgabeparameter zurück. <br/> Qualifizierer: Implementiert<br/>                      |



 

### <a name="properties"></a>Eigenschaften

Die **MicrosoftDNS \_ WINSType-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**CacheTimeout**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Zeit in Sekunden, in der ein DNS-Server, der WINS Look up verwendet, die Antwort des WINS-Servers zwischenspeichern kann.

</dd> <dt>

**LookupTimeout**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Zeit in Sekunden, in der ein DNS-Server versucht, die Auflösung mithilfe der WINS-Suche zu lösen.

</dd> <dt>

**MappingFlag**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

WINS-Zuordnungsflag, das angibt, ob der Datensatz in die Zonenreplikation eingeschlossen werden muss. Sie kann nur zwei Werte aufweisen: 0x80000000 und 0x00010000 entsprechend den Replikationsflags bzw. Flags ohne Replikation (lokaler Datensatz). Die folgenden Werte sind gültig.



| Wert                                                                                                                                               | Bedeutung                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="0x80000000"></span><span id="0X80000000"></span><dl> <dt>**0x80000000**</dt> </dl> | Replikationsflag<br/>                   |
| <span id="0x00010000"></span><span id="0X00010000"></span><dl> <dt>**0x00010000**</dt> </dl> | Flag "No-Replication (local record)" (Keine Replikation (lokaler Datensatz))<br/> |



 

</dd> <dt>

**WinsServers**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Liste der durch Kommas getrennten IP-Adressen von WINS-Servern, die in WINS-Suchläufen verwendet werden.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Namespace<br/>                | \\Stamm-MicrosoftDNS<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov.mof</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CreateInstanceFromPropertyData-Methode der MicrosoftDNS \_ WINSType-Klasse**](microsoftdns-winstype-createinstancefrompropertydata.md)
</dt> <dt>

[**Modify-Methode der MicrosoftDNS \_ WINSType-Klasse**](microsoftdns-winstype-modify.md)
</dt> <dt>

[**\_MicrosoftDNS-RessourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





