---
title: MicrosoftDNS_DomainResourceRecordContainment-Klasse
description: Die MicrosoftDNS- \_ domainresourcerecordcontainment-Klasse wird für die RR-Kapselung verwendet; jede Instanz der MicrosoftDNS- \_ Domäne kann mehrere Instanzen der MicrosoftDNS \_ resourcerecord-Klasse enthalten.
ms.assetid: 556c5e8d-58a1-4cb4-b4e9-eebdd86ed6a0
keywords:
- DNS-MicrosoftDNS_DomainResourceRecordContainment Klasse
- DNS-MicrosoftDNS_DomainResourceRecordContainment Klasse, beschrieben
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
ms.openlocfilehash: fddf172c3e320fd5c3a3b04d85d766a0252abd97
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476755"
---
# <a name="microsoftdns_domainresourcerecordcontainment-class"></a>MicrosoftDNS- \_ domainresourcerecordcontainment-Klasse

Die **MicrosoftDNS- \_ domainresourcerecordcontainment** -Klasse wird für die RR-Kapselung verwendet; jede Instanz der [**MicrosoftDNS- \_ Domäne**](microsoftdns-domain.md) kann mehrere Instanzen der [**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md) -Klasse enthalten. Jede Instanz der **MicrosoftDNS \_ resourcerecord** -Klasse gehört zu einer einzelnen Instanz der **MicrosoftDNS- \_ Domänen** Klasse und ist so definiert, dass Sie für diese Instanz schwach ist.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
class MicrosoftDNS_DomainResourceRecordContainment : CIM_Component
{
  MicrosoftDNS_Domain         REF GroupComponent;
  MicrosoftDNS_ResourceRecord REF PartComponent;
};
```

## <a name="members"></a>Member

Die **MicrosoftDNS- \_ domainresourcerecordcontainment** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MicrosoftDNS- \_ domainresourcerecordcontainment** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Datentyp: **MicrosoftDNS \_ Domain**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Qualifizierer: Key, override ("GroupComponent")

Beschreibung: Zone, Cache, roothints oder Domäne, die direkt den Ressourcen Daten Satz enthält.

Von CIM- \_ Komponente geerbt

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Datentyp: **MicrosoftDNS \_ resourcerecord**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Qualifizierer: Key, override ("PartComponent")

Beschreibung: der Ressourcen Daten Satz in Domäne, Zone, Cache oder roothints.

Geerbt von CIM- \_ Komponente.

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

[**MicrosoftDNS \_ serverdomaincontainment**](microsoftdns-serverdomaincontainment.md)
</dt> <dt>

[**MicrosoftDNS \_ domaindomaincontainment**](microsoftdns-domaindomaincontainment.md)
</dt> <dt>

[**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





