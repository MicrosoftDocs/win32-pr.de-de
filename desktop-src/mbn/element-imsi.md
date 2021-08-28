---
description: IMSI
MS-HAID: WWAN\_profile\_v4.element\_IMSI
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IMSI
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5322ba1059a3c7ba4ae60f921cf4a33a3720b8fc
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988783"
---
# <a name="span-idwwan_profile_v4element_imsispanimsi"></a><span id="WWAN_profile_v4.element_IMSI"></span>IMSI

Gibt an, dass dieses Profil nur aktiv ist, wenn die aktuelle IMSI, die in der CABID verwendet wird, das angegebene Profil ist. Andernfalls ist das Profil nicht anwendbar und kann nicht zum Aktivieren eines PDP-Kontexts (Packet Data Protocol) verwendet werden.

## <a name="element-hierarchy"></a>Elementhierarchie

[&lt;MBNProfileExt&gt;](element-mbnprofileext.md)  
[&lt;ProfileConditionedOn&gt;](element-profileconditionedon.md)  
**&lt;IMSI&gt;**

## <a name="syntax"></a>Syntax

``` syntax
<IMSI>

  subscriberIdType

</IMSI>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attribute und Elemente

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Attribute

Keine.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Untergeordnete Elemente

Keine.

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Übergeordnete Elemente


| Übergeordnetes Element | BESCHREIBUNG | 
|----------------|-------------|
| <a href="element-profileconditionedon.md">ProfileConditionedOn</a> | <p>Gibt die Bedingungen an, die erfüllt sein müssen, damit ein Profil anwendbar ist.</p><p>Dieses Element ist neu für v4. Sie ermöglicht es Ihnen, mehrere Profile anzugeben, die unter verschiedenen Bedingungen gelten, und damit das richtige Profil automatisch verwendet wird, wenn es anwendbar ist. Dieses Element ist optional. Wenn Sie sie nicht angeben, gilt das Profil immer in Bezug auf die aufgeführten Bedingungen.</p> | 


 

## <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p>Namespace</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v4</p> | 


 

 



