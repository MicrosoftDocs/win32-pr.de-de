---
title: MicrosoftDNS_Domain-Klasse
description: Die MicrosoftDNS \_ Domain-Klasse stellt eine Domäne in einer DNS-Hierarchie dar.
ms.assetid: 4b3124d6-aa5c-4950-b461-c6dd7bc96945
keywords:
- MicrosoftDNS_Domain DNS-Klasse
- MicrosoftDNS_Domain DNS-Klasse , beschrieben
topic_type:
- apiref
api_name:
- MicrosoftDNS_Domain
- MicrosoftDNS_Domain.GetDistinguishedName
- MicrosoftDNS_Domain.DnsServerName
- MicrosoftDNS_Domain.ContainerName
- MicrosoftDNS_Domain.Name
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a30b171777e6c8a99ddadcfb39c8cdfdd90b09a43ae255c9bbcc026db09bdb1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118163318"
---
# <a name="microsoftdns_domain-class"></a>MicrosoftDNS-Domänenklasse \_

Die **MicrosoftDNS \_ Domain-Klasse** stellt eine Domäne in einer DNS-Hierarchie dar.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
class MicrosoftDNS_Domain : CIM_LogicalElement
{
  string DnsServerName;
  string ContainerName;
  string Name;
};
```

## <a name="members"></a>Member

Die **MicrosoftDNS \_ Domain-Klasse** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **MicrosoftDNS \_ Domain-Klasse** verfügt über diese Methoden.



| Methode                   | Beschreibung                                                                                |
|:-------------------------|:-------------------------------------------------------------------------------------------|
| **GetDistinguishedName** | Erhält den DS-Distinguished Name für die Zone. <br/> Qualifizierer: Implementiert<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **MicrosoftDNS \_ Domain-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**ContainerName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name des Containers der Domäne, der eine Zone, ein Cache oder RootHints sein kann.

In Fällen, in denen der Container eine Zone (eine Instanz der [**MicrosoftDNS-Zone-Klasse) \_**](microsoftdns-zone.md) ist, enthält diese Eigenschaft den FQDN der Zone.

Wenn der Container die Stammzone ist, sollte die Zeichenfolge \\ \\ verwendet werden.

In Fällen, in denen der Container der DNS-Cache von Ressourceneinträgen (eine Instanz der [**MicrosoftDNS \_ Cache-Klasse)**](microsoftdns-cache.md) ist, wird diese Eigenschaft auf die Zeichenfolge \\ festgelegt. Cache \\ .

Wenn der Container RootHints (eine Instanz der [**MicrosoftDNS \_ RootHints-Klasse)**](microsoftdns-roothints.md) ist, sollte diese Eigenschaft auf festgelegt \\ werden. RootHints \\ .

</dd> <dt>

**DnsServerName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

FQDN oder IP-Adresse des DNS-Servers, der die Domäne enthält.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

FQDN der Domäne.

Für Instanzen von DNS Cache oder RootHints die \\ Zeichenfolgen .. Cache \\ und \\ .. RootHints \\ sollten verwendet werden.

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

[**GetDistinguishedName-Methode der \_ MicrosoftDNS-Domänenklasse**](microsoftdns-domain-getdistinguishedname.md)
</dt> </dl>

 

 





