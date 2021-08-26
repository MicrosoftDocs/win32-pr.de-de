---
title: MicrosoftDNS_NSType-Klasse
description: Die Unterklasse von MicrosoftDNS \_ ResourceRecord, die einen NS-Eintrag (Name Server) darstellt.
ms.assetid: 8d229acd-bc47-4a32-b6f1-b784a48dc91a
keywords:
- dns der MicrosoftDNS_NSType-Klasse
- MicrosoftDNS_NSType DNS-Klasse beschrieben
topic_type:
- apiref
api_name:
- MicrosoftDNS_NSType
- MicrosoftDNS_NSType.CreateInstanceFromPropertyData
- MicrosoftDNS_NSType.Modify
- MicrosoftDNS_NSType.NSHost
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85142770587813d4d8533a22817ad3dc1980be7e30d1894668573cc24eeabdf7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104030"
---
# <a name="microsoftdns_nstype-class"></a>MicrosoftDNS \_ NSType-Klasse

Die Unterklasse von [**MicrosoftDNS \_ ResourceRecord,**](microsoftdns-resourcerecord.md) die einen NS-Eintrag (Name Server) darstellt.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
class MicrosoftDNS_NSType : MicrosoftDNS_ResourceRecord
{
  string NSHost;
};
```

## <a name="members"></a>Member

Die **MicrosoftDNS \_ NSType-Klasse** verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **MicrosoftDNS \_ NSType-Klasse** verfügt über diese Methoden.



| Methode                             | Beschreibung                                                                                                                                                                                                                                                                                                                                                      |
|:-----------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Instanziiert einen DNS-NS-Ressourceneintrag basierend auf den Daten in den Eingabeparametern der Methode: DNS-Servername des Eintrags, Containername, Besitzername, Klasse (Standard = IN), Wert für die Lebenszeit und Host mit Autorität für die Domäne. Es gibt einen Verweis auf das neue Objekt als Ausgabeparameter zurück. <br/> Qualifizierer: Implementiert, statisch<br/> |
| **Änderung**                         | Aktualisiert die Gültigkeitsdauer und den NS-Host auf die Werte, die als Eingabeparameter dieser Methode angegeben sind. Wenn kein neuer Wert für einen Parameter angegeben wird, wird der aktuelle Wert für den Parameter nicht geändert. Die -Methode gibt einen Verweis auf das geänderte Objekt als Ausgabeparameter zurück. <br/> Qualifizierer: Implementiert<br/>                               |



 

### <a name="properties"></a>Eigenschaften

Die **MicrosoftDNS \_ NSType-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**NSHost**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Autoritativer Host für die Domäne.

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

[**CreateInstanceFromPropertyData-Methode der \_ MicrosoftDNS-NSType-Klasse**](microsoftdns-nstype-createinstancefrompropertydata.md)
</dt> <dt>

[**Modify-Methode der \_ MicrosoftDNS-NSType-Klasse**](microsoftdns-nstype-modify.md)
</dt> <dt>

[**\_MicrosoftDNS-RessourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





