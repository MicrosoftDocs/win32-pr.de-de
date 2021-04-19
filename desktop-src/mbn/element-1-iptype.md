---
description: "\"Fidemdmconfigprofile\" \\/ ... \\/ Iptype (v4)"
MS-HAID: WWAN\_profile\_v4.element\_1\_IPType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Iptype (v4)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ec57fbe0bbcb4c633ddb8485f048ce4230e0ca5
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/05/2021
ms.locfileid: "106388805"
---
# <a name="span-idwwan_profile_v4element_1_iptypespanmodemdmconfigprofileiptype-v4"></a><span id="WWAN_profile_v4.element_1_IPType"></span>"Fidemdmconfigprofile" \/ ... \/ Iptype (v4)

Gibt den IP-Typ an, der für diese Datenverbindung verwendet werden soll.

Dieses Element ist neu in v4 des Schemas. Das-Element kann einen der folgenden Werte aufweisen.

| Wert   | Bedeutung                                       |
|---------|-----------------------------------------------|
| Standard | Der IP-Typ muss von niedrigeren Ebenen ausgewählt werden.     |
| IPv4    | IPv4 verwenden                                      |
| IPv6    | IPv6 verwenden                                      |
| IPv4v6  | Verwenden Sie IPv4 und/oder IPv6 als verfügbar.           |
| Xlat    | Verwenden von 464xlat zum Tunneln von IPv4 über IPv6-Netzwerke |

 

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

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Übergeordnetes Element</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="element-1-context.md">Context</a></td>
<td><p>Gibt die Parameter an, die zum Herstellen einer Datenverbindung erforderlich sind.</p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a>Anforderungen

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Namespace</p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



