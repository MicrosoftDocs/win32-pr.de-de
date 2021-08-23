---
title: MicrosoftDNS_ServerDomainContainment-Klasse
description: Jede Instanz der WMI-Klasse für die \_ MicrosoftDNS-Serverzuordnung kann mehrere Instanzen der MicrosoftDNS-Domänenklasse \_ enthalten.
ms.assetid: a16a11fb-65fc-4f12-903c-b3a61f6a4720
keywords:
- dns-Klasse MicrosoftDNS_ServerDomainContainment
- MicrosoftDNS_ServerDomainContainment Dns-Klasse beschrieben
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
ms.openlocfilehash: bdc747cae72ac4733ad9bec7288858731b6250312d43476a000d2f99a989267d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119527250"
---
# <a name="microsoftdns_serverdomaincontainment-class"></a>MicrosoftDNS \_ ServerDomainContainment-Klasse

Jede Instanz der WMI-Klasse für die [**MicrosoftDNS-Serverzuordnung \_**](microsoftdns-server.md) kann mehrere Instanzen der [**MicrosoftDNS-Domänenklasse \_**](microsoftdns-domain.md) enthalten. Jede Instanz der **MicrosoftDNS \_ Domain-Klasse** gehört zu einer einzelnen Instanz der **MicrosoftDNS-Serverklasse \_** und ist für diesen Server als schwach definiert.

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

Die **MicrosoftDNS \_ ServerDomainContainment-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MicrosoftDNS \_ ServerDomainContainment-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Datentyp: **MicrosoftDNS \_ Server**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Qualifizierer: Schlüssel, Außerkraftsetzung ("GroupComponent"), Min (1), Max (1)

Beschreibung: Der DNS-Server.

Geerbt von **der \_ CIM-Komponente**.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Datentyp: **\_ MicrosoftDNS-Domäne**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Qualifizierer: Key, Override("PartComponent")

Beschreibung: Eine Domäne, Zone, ein Cache oder RootHints, die vom DNS-Server verwaltet werden.

Geerbt von **der \_ CIM-Komponente**.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **MicrosoftDNS \_ ServerDomainContainment-Klasse** wird von der **\_ CIM-Komponentenklasse** abgeleitet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Namespace<br/>                | \\Stamm-MicrosoftDNS<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov.mof</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MicrosoftDNS \_ DomainDomainContainment**](microsoftdns-domaindomaincontainment.md)
</dt> <dt>

[**MicrosoftDNS \_ DomainResourceRecordContainment**](microsoftdns-domainresourcerecordcontainment.md)
</dt> <dt>

[**\_MicrosoftDNS-RessourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





