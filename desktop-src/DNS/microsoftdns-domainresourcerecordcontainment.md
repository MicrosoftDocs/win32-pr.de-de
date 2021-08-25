---
title: MicrosoftDNS_DomainResourceRecordContainment-Klasse
description: Die MicrosoftDNS DomainResourceRecordContainment-Klasse wird für die RR-Aufzeichnung verwendet. Jede Instanz der MicrosoftDNS-Domäne kann mehrere Instanzen der \_ \_ MicrosoftDNS \_ ResourceRecord-Klasse enthalten.
ms.assetid: 556c5e8d-58a1-4cb4-b4e9-eebdd86ed6a0
keywords:
- MicrosoftDNS_DomainResourceRecordContainment DNS-Klasse
- MicrosoftDNS_DomainResourceRecordContainment DNS-Klasse , beschrieben
topic_type:
- apiref
api_name:
- MicrosoftDNS_DomainResourceRecordContainment
- MicrosoftDNS_DomainResourceRecordContainment.GroupComponent
- MicrosoftDNS_DomainResourceRecordContainment.PartComponent
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 498d9b953895ebece94dc77edb587045d1cfdd45c29f04c202756bd1080dc9f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795610"
---
# <a name="microsoftdns_domainresourcerecordcontainment-class"></a>MicrosoftDNS \_ DomainResourceRecordContainment-Klasse

Die **MicrosoftDNS \_ DomainResourceRecordContainment-Klasse** wird für die RR-Aufzeichnung verwendet. Jede Instanz der [**MicrosoftDNS-Domäne \_**](microsoftdns-domain.md) kann mehrere Instanzen der [**MicrosoftDNS \_ ResourceRecord-Klasse**](microsoftdns-resourcerecord.md) enthalten. Jede Instanz der **MicrosoftDNS \_ ResourceRecord-Klasse** gehört zu einer einzelnen Instanz der **MicrosoftDNS \_ Domain-Klasse** und ist für diese Instanz als schwach definiert.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
class MicrosoftDNS_DomainResourceRecordContainment : CIM_Component
{
  MicrosoftDNS_Domain         REF GroupComponent;
  MicrosoftDNS_ResourceRecord REF PartComponent;
};
```

## <a name="members"></a>Member

Die **MicrosoftDNS \_ DomainResourceRecordContainment-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MicrosoftDNS \_ DomainResourceRecordContainment-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Datentyp: **MicrosoftDNS-Domäne \_**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Qualifizierer: Key, Override("GroupComponent")

Beschreibung: Zone, Cache, RootHints oder Domäne, die den Ressourcendatensatz direkt enthält.

Geerbt von \_ CIM-Komponente

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Datentyp: **MicrosoftDNS \_ ResourceRecord**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Qualifizierer: Key, Override("PartComponent")

Beschreibung: Der Ressourcendatensatz, der in einer Domäne, Zone, einem Cache oder rootHints enthalten ist.

Geerbt von \_ CIM-Komponente.

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

[**MicrosoftDNS \_ ServerDomainContainment**](microsoftdns-serverdomaincontainment.md)
</dt> <dt>

[**MicrosoftDNS \_ DomainDomainContainment**](microsoftdns-domaindomaincontainment.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





