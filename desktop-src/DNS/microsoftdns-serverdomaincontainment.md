---
title: MicrosoftDNS_ServerDomainContainment-Klasse
description: Jede Instanz der WMI-Klasse MicrosoftDNS \_ Server Association kann mehrere Instanzen der MicrosoftDNS- \_ Domänen Klasse enthalten.
ms.assetid: a16a11fb-65fc-4f12-903c-b3a61f6a4720
keywords:
- DNS-MicrosoftDNS_ServerDomainContainment Klasse
- DNS-MicrosoftDNS_ServerDomainContainment Klasse, beschrieben
topic_type:
- apiref
api_name:
- MicrosoftDNS_ServerDomainContainment
- MicrosoftDNS_ServerDomainContainment.GroupComponent
- MicrosoftDNS_ServerDomainContainment.PartComponent
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55d160176b51fc518ff2d00ef87bf08a812ee4d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740265"
---
# <a name="microsoftdns_serverdomaincontainment-class"></a>MicrosoftDNS \_ serverdomaincontainment-Klasse

Jede Instanz der WMI-Klasse [**MicrosoftDNS \_ Server**](microsoftdns-server.md) Association kann mehrere Instanzen der [**MicrosoftDNS- \_ Domänen**](microsoftdns-domain.md) Klasse enthalten. Jede Instanz der **MicrosoftDNS- \_ Domänen** Klasse gehört zu einer einzelnen Instanz der **MicrosoftDNS- \_ Server** Klasse und ist so definiert, dass Sie für diesen Server schwach ist.

Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.

## <a name="syntax"></a>Syntax

``` syntax
class MicrosoftDNS_ServerDomainContainment : CIM_Component
{
  MicrosoftDNS_Server REF GroupComponent;
  MicrosoftDNS_Domain REF PartComponent;
};
```

## <a name="members"></a>Member

Die **MicrosoftDNS \_ serverdomaincontainment** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MicrosoftDNS \_ serverdomaincontainment** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Datentyp: **MicrosoftDNS- \_ Server**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Qualifizierer: Key, override ("GroupComponent"), min (1), Max (1)

Beschreibung: der DNS-Server.

Geerbt von **CIM- \_ Komponente**.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Datentyp: **MicrosoftDNS \_ Domain**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Qualifizierer: Key, override ("PartComponent")

Beschreibung: Domäne, Zone, Cache oder roothints, die vom DNS-Server verwaltet werden.

Geerbt von **CIM- \_ Komponente**.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **MicrosoftDNS \_ serverdomaincontainment** -Klasse wird von der **CIM- \_ Komponenten** Klasse abgeleitet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Namespace<br/>                | \\MicrosoftDNS-Stamm<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov. MOF</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MicrosoftDNS \_ domaindomaincontainment**](microsoftdns-domaindomaincontainment.md)
</dt> <dt>

[**MicrosoftDNS \_ domainresourcerecordcontainment**](microsoftdns-domainresourcerecordcontainment.md)
</dt> <dt>

[**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





