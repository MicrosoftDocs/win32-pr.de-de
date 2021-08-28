---
description: ModemDMConfigProfile \/ ... \/ IPType (v4)
MS-HAID: WWAN\_profile\_v4.element\_1\_IPType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPType (v4)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f655d2f8592613fdb4953cbda32841dc9beaec0d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479976"
---
# <a name="span-idwwan_profile_v4element_1_iptypespanmodemdmconfigprofileiptype-v4"></a><span id="WWAN_profile_v4.element_1_IPType"></span>ModemDMConfigProfile \/ ... \/ IPType (v4)

Gibt den IP-Typ an, der für diese Datenverbindung verwendet werden soll.

Dieses Element ist neu in v4 des Schemas. Das -Element kann einen der folgenden Werte haben.

| Wert   | Bedeutung                                       |
|---------|-----------------------------------------------|
| Standard | Der IP-Typ muss von einer niedrigeren Ebene(n)     |
| IPv4    | Verwenden von IPv4                                      |
| IPv6    | IPv6 verwenden                                      |
| IPv4v6  | Verwenden Sie IPv4 und/oder IPv6, wie verfügbar.           |
| XLAT    | Verwenden von 464XLAT zum Tunneln von IPv4 über IPv6-Netzwerke |

 

## <a name="element-hierarchy"></a>Elementhierarchie

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;[\<Context\>](element-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;**\<IPType\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;[\<Context\>](element-1-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;**\<IPType\>**

## <a name="syntax"></a>Syntax

``` syntax
<IPType>

  "Default" | "IPv4" | "IPv6" | "IPv4v6" | "XLAT"

</IPType>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attribute und Elemente

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Attribute

Keine.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Untergeordnete Elemente

Keine.

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Übergeordnete Elemente


| Übergeordnetes Element | BESCHREIBUNG | 
|----------------|-------------|
| <a href="element-1-context.md">Context</a> | <p>Gibt die Parameter an, die zum Herstellen einer Datenverbindung erforderlich sind.</p> | 


 

## <a name="requirements"></a>Anforderungen


| | | <p>Namespace</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v4</p> | 


 

 



