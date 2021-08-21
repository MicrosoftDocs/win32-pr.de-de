---
title: MicrosoftDNS_RTType-Klasse
description: Die Unterklasse von MicrosoftDNS \_ ResourceRecord, die einen RT-Eintrag (Route Through) darstellt.
ms.assetid: 986e2bbf-4f45-4611-906e-66079fda7f4c
keywords:
- MicrosoftDNS_RTType DNS-Klasse
- MicrosoftDNS_RTType DNS-Klasse , beschrieben
topic_type:
- apiref
api_name:
- MicrosoftDNS_RTType
- MicrosoftDNS_RTType.CreateInstanceFromPropertyData
- MicrosoftDNS_RTType.Modify
- MicrosoftDNS_RTType.Preference
- MicrosoftDNS_RTType.IntermediateHost
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 287dc3d80370f812b6ee721b9556f906df289c67a17048aa326efc3b80de5954
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077060"
---
# <a name="microsoftdns_rttype-class"></a>MicrosoftDNS \_ RTType-Klasse

Die Unterklasse von [**MicrosoftDNS \_ ResourceRecord,**](microsoftdns-resourcerecord.md) die einen RT-Eintrag (Route Through) darstellt.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
class MicrosoftDNS_RTType : MicrosoftDNS_ResourceRecord
{
  uint16 Preference;
  string IntermediateHost;
};
```

## <a name="members"></a>Member

Die **MicrosoftDNS \_ RTType-Klasse** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **MicrosoftDNS \_ RTType-Klasse** verfügt über diese Methoden.



| Methode                             | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                      |
|:-----------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Instanziiert einen RT-Typ von RR basierend auf den Daten in den Eingabeparametern der Methode: DNS-Servername des Datensatzes, Containername, Besitzer-/Hostname, Klasse (Standard = IN), Lebzeitwert, Datensatzpräferenz und Zwischenhostname. Sie gibt einen Verweis auf das neue Objekt als Ausgabeparameter zurück. <br/> Qualifizierer: Implementiert, statisch<br/> |
| **Änderung**                         | Aktualisiert TTL, Preference und Intermediate Host auf die Werte, die als Eingabeparameter dieser Methode angegeben sind. Wenn kein neuer Wert für einen Parameter angegeben wird, wird der aktuelle Wert für den Parameter nicht geändert. Die -Methode gibt einen Verweis auf das geänderte Objekt als Ausgabeparameter zurück. <br/> Qualifizierer: Implementiert<br/>        |



 

### <a name="properties"></a>Eigenschaften

Die **MicrosoftDNS \_ RTType-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**IntermediateHost**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

FQDN, der einen Host an, der als Zwischenziel beim Erreichen des vom Besitzer angegebenen Hosts dienen soll.

</dd> <dt>

**Einstellung**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese RR wird unter anderem beim gleichen Besitzer bevorzugt. Niedrigere Werte werden bevorzugt.

</dd> </dl>

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Namespace<br/>                | \\MicrosoftDNS-Stamm<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov.mof</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CreateInstanceFromPropertyData-Methode der MicrosoftDNS \_ RTType-Klasse**](microsoftdns-rttype-createinstancefrompropertydata.md)
</dt> <dt>

[**Modify-Methode der MicrosoftDNS \_ RTType-Klasse**](microsoftdns-rttype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





