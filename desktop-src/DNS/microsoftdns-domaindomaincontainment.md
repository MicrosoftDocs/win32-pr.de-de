---
title: MicrosoftDNS_DomainDomainContainment-Klasse
description: Die MicrosoftDNS- \_ domaindomaincontainment-Klasse wird für die Domänen Kapselung verwendet. DNS-Domänen können andere DNS-Domänen enthalten.
ms.assetid: 43faa046-30bf-4fb3-9698-98d09c424fad
keywords:
- DNS-MicrosoftDNS_DomainDomainContainment Klasse
- DNS-MicrosoftDNS_DomainDomainContainment Klasse, beschrieben
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
ms.openlocfilehash: a55c5b67ee8026055bc2fa8098cb33e8c767528f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040853"
---
# <a name="microsoftdns_domaindomaincontainment-class"></a>MicrosoftDNS- \_ domaindomaincontainment-Klasse

Die **MicrosoftDNS- \_ domaindomaincontainment** -Klasse wird für die Domänen Kapselung verwendet. DNS-Domänen können andere DNS-Domänen enthalten. Jede Instanz der [**MicrosoftDNS- \_ Domänen**](microsoftdns-domain.md) Klasse kann mehrere andere Instanzen der **MicrosoftDNS- \_ Domäne** enthalten. Eine Instanz eines **MicrosoftDNS- \_ Domänen** Objekts ist direkt in höchstens einer **MicrosoftDNS- \_ Domäne** der höheren Ebene enthalten.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
class MicrosoftDNS_DomainDomainContainment : CIM_Component
{
  MicrosoftDNS_Domain REF GroupComponent;
  MicrosoftDNS_Domain REF PartComponent;
};
```

## <a name="members"></a>Member

Die **MicrosoftDNS- \_ domaindomaincontainment** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MicrosoftDNS- \_ domaindomaincontainment** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Datentyp: **MicrosoftDNS \_ Domain**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Qualifizierer: Key, Max (1), override ("GroupComponent")

Beschreibung: eine Domäne, eine Zone, ein Cache oder eine roothints auf höherer Ebene.

Von CIM- \_ Komponente geerbt

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Datentyp: **MicrosoftDNS \_ Domain**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Qualifizierer: Key, override ("PartComponent")

Beschreibung: die Domäne, die sich in einer Domäne, Zone, einem Cache oder in einer höheren Ebene befindet.

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

[**MicrosoftDNS \_ domainresourcerecordcontainment**](microsoftdns-domainresourcerecordcontainment.md)
</dt> <dt>

[**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md)
</dt> <dt>

[**MicrosoftDNS \_ serverdomaincontainment**](microsoftdns-serverdomaincontainment.md)
</dt> </dl>

 

 





