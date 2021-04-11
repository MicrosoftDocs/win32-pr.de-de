---
title: MicrosoftDNS_Domain-Klasse
description: Die MicrosoftDNS- \_ Domänen Klasse stellt eine Domäne in einer DNS-Hierarchie dar.
ms.assetid: 4b3124d6-aa5c-4950-b461-c6dd7bc96945
keywords:
- DNS-MicrosoftDNS_Domain Klasse
- DNS-MicrosoftDNS_Domain Klasse, beschrieben
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
ms.openlocfilehash: 108badc046e22f27d9bb02abd0d8f26314da456c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103707"
---
# <a name="microsoftdns_domain-class"></a>MicrosoftDNS- \_ Domänen Klasse

Die **MicrosoftDNS- \_ Domänen** Klasse stellt eine Domäne in einer DNS-Hierarchie dar.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

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

Die **MicrosoftDNS- \_ Domänen** Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **MicrosoftDNS- \_ Domänen** Klasse verfügt über diese Methoden.



| Methode                   | BESCHREIBUNG                                                                                |
|:-------------------------|:-------------------------------------------------------------------------------------------|
| **Getchilshedname** | Ruft den Distinguished Name DS für die Zone ab. <br/> Qualifizierer: Implementiert<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **MicrosoftDNS- \_ Domänen** Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Container Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name des Containers der Domäne, bei dem es sich um eine Zone, einen Cache oder einen roothin handelt.

In Fällen, in denen es sich bei dem Container um eine Zone (eine Instanz der [**MicrosoftDNS- \_ Zonen**](microsoftdns-zone.md) Klasse) handelt, enthält diese Eigenschaft den voll qualifizierten Namen der Zone.

Wenn der Container die Stammzone ist, sollte die Zeichenfolge \\ . \\ verwendet werden.

In Fällen, in denen es sich bei dem Container um den DNS-Cache von Ressourcen Einträgen handelt (eine Instanz der [**MicrosoftDNS- \_ Cache**](microsoftdns-cache.md) Klasse), wird diese Eigenschaft auf \\ die Zeichenfolge festgelegt. Cache \\ .

Wenn es sich bei dem Container um roothints handelt (eine Instanz der [**MicrosoftDNS-Klasse \_ roothints**](microsoftdns-roothints.md) ), sollte diese Eigenschaft auf festgelegt werden. \\ Roothints \\ .

</dd> <dt>

**Dnsservername**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der voll qualifizierte Domänen Name oder die IP-Adresse des DNS-Servers, der die Domäne enthält.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der voll qualifizierte Domänen Name der Domäne.

Für Instanzen von DNS-Cache oder roothints werden die Zeichen folgen \\ . Cache \\ und \\ .. Es sollten roothints \\ verwendet werden.

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

[**Geterkennbar shedname-Methode der MicrosoftDNS- \_ Domänen Klasse**](microsoftdns-domain-getdistinguishedname.md)
</dt> </dl>

 

 





