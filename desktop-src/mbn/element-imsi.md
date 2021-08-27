---
description: IMSI
MS-HAID: WWAN\_profile\_v4.element\_IMSI
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IMSI
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c5e8c0fa64a19f7c2966672d3bc4ab5b2162861
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477126"
---
# <a name="span-idwwan_profile_v4element_imsispanimsi"></a><span id="WWAN_profile_v4.element_IMSI"></span>IMSI

Gibt an, dass dieses Profil nur dann aktiv ist, wenn das aktuelle IMSI, das in DER IDid verwendet wird, das angegebene ist. Andernfalls ist das Profil nicht anwendbar und kann nicht zum Aktivieren eines PDP-Kontexts (Packet Data Protocol) verwendet werden.

## <a name="element-hierarchy"></a>Elementhierarchie

[<MBNProfileExt>](element-mbnprofileext.md)  
[<ProfileConditionedOn>](element-profileconditionedon.md)  
**<IMSI>**

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
| <a href="element-profileconditionedon.md">ProfileConditionedOn</a> | <p>Gibt die Bedingungen an, die erfüllt sein müssen, damit ein Profil anwendbar ist.</p><p>Dieses Element ist neu für v4. Sie können mehrere Profile angeben, die unter verschiedenen Bedingungen gelten, und das richtige Profil automatisch verwenden, wenn es anwendbar ist. Dieses Element ist optional. Wenn Sie es nicht angeben, ist das Profil immer in Bezug auf die aufgeführten Bedingungen anwendbar.</p> | 


 

## <a name="requirements"></a>Anforderungen


| | | <p>Namespace</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v4</p> | 


 

 



