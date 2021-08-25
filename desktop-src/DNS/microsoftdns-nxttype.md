---
title: MicrosoftDNS_NXTType-Klasse
description: Unterklasse von MicrosoftDNS \_ ResourceRecord, die eine Next (NXT) RR darstellt.
ms.assetid: bb24509e-083b-4432-89e3-501167f12299
keywords:
- dns der MicrosoftDNS_NXTType-Klasse
- MicrosoftDNS_NXTType Dns-Klasse beschrieben
topic_type:
- apiref
api_name:
- MicrosoftDNS_NXTType
- MicrosoftDNS_NXTType.CreateInstanceFromPropertyData
- MicrosoftDNS_NXTType.Modify
- MicrosoftDNS_NXTType.NextDomainName
- MicrosoftDNS_NXTType.Types
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36fa67d3d1ab60aa4af6c0be7269f068edaf42a64fa9cf1cfea68ca23d82ef7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913100"
---
# <a name="microsoftdns_nxttype-class"></a>MicrosoftDNS \_ NXTType-Klasse

Unterklasse von [**MicrosoftDNS \_ ResourceRecord,**](microsoftdns-resourcerecord.md) die eine Next (NXT) RR darstellt.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
class MicrosoftDNS_NXTType : MicrosoftDNS_ResourceRecord
{
  string NextDomainName;
  string Types;
};
```

## <a name="members"></a>Member

Die **MicrosoftDNS \_ NXTType-Klasse** verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **MicrosoftDNS \_ NXTType-Klasse** verfügt über diese Methoden.



| Methode                             | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Instanziiert einen NXT-Ressourcendatensatz basierend auf den Daten in den Eingabeparametern der Methode: DNS-Servername des Eintrags, Containername, Besitzername, Klasse (Standard = IN), Time-to-Live-Wert und WINS-Zuordnungsflag, Reverse-Look-Up-Time out, WINS-Cachetime out und Anzufügen des Domänennamens. Es gibt einen Verweis auf das neue Objekt als Ausgabeparameter zurück. <br/> Qualifizierer: Implementiert, statisch<br/>                                                                                                                                           |
| **Änderung**                         | Aktualisiert die Gültigkeitsdauer, das Zuordnungsflag, das Suchtime out, das Cachetime out und die Ergebnisdomäne auf die Werte, die als Eingabeparameter dieser Methode angegeben sind. Wenn kein neuer Wert für einen Parameter angegeben wird, wird der aktuelle Wert für den Parameter nicht geändert. Die -Methode gibt einen Verweis auf das geänderte Objekt als Ausgabeparameter zurück. <br/> Qualifizierer: Implementiert<br/> **Windows Server 2003:** Diese Methode aktualisiert auch nextDomainName und Types auf die Werte, die als Eingabeparameter dieser Methode angegeben sind.<br/> <br/> |



 

### <a name="properties"></a>Eigenschaften

Die **MicrosoftDNS \_ NXTType-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**NextDomainName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Nächster Domänenname.

</dd> <dt>

**Typen**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Durch Leerzeichen getrennte Liste der Mnemonics vom RR-Typ für den Besitzernamen des NXT-Ressourcendatensatzes.

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

[**CreateInstanceFromPropertyData-Methode der MicrosoftDNS \_ NXTType-Klasse**](microsoftdns-nxttype-createinstancefrompropertydata.md)
</dt> <dt>

[**Modify-Methode der \_ MicrosoftDNS-NXTType-Klasse**](microsoftdns-nxttype-modify.md)
</dt> <dt>

[**\_MicrosoftDNS-RessourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





