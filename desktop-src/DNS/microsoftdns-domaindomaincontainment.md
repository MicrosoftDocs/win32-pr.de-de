---
title: MicrosoftDNS_DomainDomainContainment-Klasse
description: Die MicrosoftDNS \_ DomainDomainContainment-Klasse wird für die Domäneninklassierung verwendet. DNS-Domänen können andere DNS-Domänen enthalten.
ms.assetid: 43faa046-30bf-4fb3-9698-98d09c424fad
keywords:
- MicrosoftDNS_DomainDomainContainment DNS-Klasse
- MicrosoftDNS_DomainDomainContainment DNS-Klasse , beschrieben
topic_type:
- apiref
api_name:
- MicrosoftDNS_DomainDomainContainment
- MicrosoftDNS_DomainDomainContainment.GroupComponent
- MicrosoftDNS_DomainDomainContainment.PartComponent
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8f96d03f007af463fb4c4f672eb0d1374867636f4a4224469589563b9c5882e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084750"
---
# <a name="microsoftdns_domaindomaincontainment-class"></a>MicrosoftDNS \_ DomainDomainContainment-Klasse

Die **MicrosoftDNS \_ DomainDomainContainment-Klasse** wird für die Domäneninklassierung verwendet. DNS-Domänen können andere DNS-Domänen enthalten. Jede Instanz der [**MicrosoftDNS-Domänenklasse \_**](microsoftdns-domain.md) kann mehrere andere Instanzen der **MicrosoftDNS-Domäne \_ enthalten.** Eine Instanz eines **MicrosoftDNS-Domänenobjekts \_** ist direkt in nicht mehr als einer **höheren MicrosoftDNS-Domäne \_ enthalten.**

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
class MicrosoftDNS_DomainDomainContainment : CIM_Component
{
  MicrosoftDNS_Domain REF GroupComponent;
  MicrosoftDNS_Domain REF PartComponent;
};
```

## <a name="members"></a>Member

Die **MicrosoftDNS \_ DomainDomainContainment-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MicrosoftDNS \_ DomainDomainContainment-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Datentyp: **MicrosoftDNS-Domäne \_**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Qualifizierer: Key, Max(1), Override("GroupComponent")

Beschreibung: Eine Domäne, Zone, Ein Cache oder RootHints auf höherer Ebene.

Geerbt von \_ CIM-Komponente

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Datentyp: **MicrosoftDNS-Domäne \_**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Qualifizierer: Key, Override("PartComponent")

Beschreibung: Die Domäne, die in einer Domäne, Zone, einem Cache oder RootHints auf höherer Ebene enthalten ist.

Geerbt von \_ CIM-Komponente.

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

[**MicrosoftDNS \_ DomainResourceRecordContainment**](microsoftdns-domainresourcerecordcontainment.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> <dt>

[**MicrosoftDNS \_ ServerDomainContainment**](microsoftdns-serverdomaincontainment.md)
</dt> </dl>

 

 





