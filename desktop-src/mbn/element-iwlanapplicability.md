---
description: IwlanApplicability
MS-HAID: WWAN\_profile\_v4.element\_IwlanApplicability
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IwlanApplicability
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dac7d44d5bae50a899e3d32c4e421b4c8d2cd80e
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882073"
---
# <a name="span-idwwan_profile_v4element_iwlanapplicabilityspaniwlanapplicability"></a><span id="WWAN_profile_v4.element_IwlanApplicability"></span>IwlanApplicability

Gibt an, dass dieses Profil nur aktiv ist, wenn es mit einem IWLAN-Netzwerk verbunden ist. Andernfalls ist das Profil nicht anwendbar und kann nicht zum Aktivieren eines PDP-Kontexts (Packet Data Protocol) verwendet werden. Der Wert dieses Elements muss ein gültiger [**iwlanApplicabilityType-Wert**](simpletype-iwlanapplicabilitytype.md) sein.

## <a name="element-hierarchy"></a>Elementhierarchie

[&lt;MBNProfileExt&gt;](element-mbnprofileext.md)  
[&lt;ProfileConditionedOn&gt;](element-profileconditionedon.md)  
**&lt;IwlanApplicability&gt;**

## <a name="syntax"></a>Syntax

``` syntax
<IwlanApplicability>

  "CellularOnly" | "CellularAndIwlan" | "IwlanOnly"

</IwlanApplicability>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attribute und Elemente

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Attribute

Keine.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Untergeordnete Elemente

Keine.

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Übergeordnete Elemente


| Übergeordnetes Element | Beschreibung | 
|----------------|-------------|
| <a href="element-profileconditionedon.md">ProfileConditionedOn</a> | <p>Gibt die Bedingungen an, die erfüllt sein müssen, damit ein Profil anwendbar ist.</p><p>Dieses Element ist neu für v4. Sie ermöglicht es Ihnen, mehrere Profile anzugeben, die unter verschiedenen Bedingungen gelten, und damit das richtige Profil automatisch verwendet wird, wenn es anwendbar ist. Dieses Element ist optional. Wenn Sie sie nicht angeben, gilt das Profil immer in Bezug auf die aufgeführten Bedingungen.</p> | 


 

## <a name="requirements"></a>Requirements (Anforderungen)


| | | <p>Namespace</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v4</p> | 


 

 



