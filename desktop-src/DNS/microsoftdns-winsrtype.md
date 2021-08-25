---
title: MicrosoftDNS_WINSRType-Klasse
description: Die Unterklasse von MicrosoftDNS \_ ResourceRecord, die einen WINS Reverse Look-up-Datensatz (WINSR) darstellt.
ms.assetid: e611dc63-838f-4a79-baca-febd27612111
keywords:
- dns-Klasse MicrosoftDNS_WINSRType
- MicrosoftDNS_WINSRType Dns-Klasse beschrieben
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
ms.openlocfilehash: a89c9545c73a4dbd5a01ff401c7b5587cf448553fcafcf4d698e3aeb17ed8722
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912820"
---
# <a name="microsoftdns_winsrtype-class"></a>MicrosoftDNS \_ WINSRType-Klasse

Die Unterklasse von [**MicrosoftDNS \_ ResourceRecord,**](microsoftdns-resourcerecord.md) die einen WINS Reverse Look-up-Datensatz (WINSR) darstellt.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

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

Die **MicrosoftDNS \_ WINSRType-Klasse** verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **MicrosoftDNS \_ WINSRType-Klasse** verfügt über diese Methoden.



| Methode                             | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                     |
|:-----------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Instanziiert einen WINSR-Typ von RR basierend auf den Daten in den Eingabeparametern der Methode: DNS-Servername des Eintrags, Containername, Besitzername, Klasse (Standard = IN), Time-to-Live-Wert und WINS-Zuordnungsflag, Reverse-Look-Up-Time out, WINS-Cachetime out und Domänenname zum Anfügen. Es gibt einen Verweis auf das neue Objekt als Ausgabeparameter zurück. <br/> Qualifizierer: Implementiert, statisch<br/> |
| **Änderung**                         | Aktualisiert die Gültigkeitsdauer, das Zuordnungsflag, das Suchtime out, das Cachetime out und die Ergebnisdomäne auf die Werte, die als Eingabeparameter dieser Methode angegeben sind. Wenn kein neuer Wert für einen Parameter angegeben wird, wird der aktuelle Wert für den Parameter nicht geändert. Die -Methode gibt einen Verweis auf das geänderte Objekt als Ausgabeparameter zurück. <br/> Qualifizierer: Implementiert<br/>                        |



 

### <a name="properties"></a>Eigenschaften

Die **MicrosoftDNS \_ WINSRType-Klasse** verfügt über diese Eigenschaften.

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

Time out in Sekunden für einen DNS-Server mit WINS Reverse Look up.

</dd> <dt>

**MappingFlag**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

WINSR-Zuordnungsflag, das angibt, ob der Datensatz in die Zonenreplikation eingeschlossen werden muss. Sie kann nur zwei Werte aufweisen: 0x80000000 und 0x00010000 entsprechend den Replikationsflags bzw. Flags ohne Replikation (lokaler Datensatz).

</dd> <dt>

**ResultDomain**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Domänenname, der an zurückgegebene NetBIOS-Namen angefügt werden soll.

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

[**CreateInstanceFromPropertyData-Methode der MicrosoftDNS \_ WINSRType-Klasse**](microsoftdns-winsrtype-createinstancefrompropertydata.md)
</dt> <dt>

[**Modify-Methode der MicrosoftDNS \_ WINSRType-Klasse**](microsoftdns-winsrtype-modify.md)
</dt> <dt>

[**\_MicrosoftDNS-RessourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





