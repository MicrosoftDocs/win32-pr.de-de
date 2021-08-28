---
description: ProfileConditionedOn
MS-HAID: WWAN\_profile\_v4.element\_ProfileConditionedOn
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ProfileConditionedOn
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01a3ead4edb14cc7d9164ca834d154c2623c03b4
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477076"
---
# <a name="span-idwwan_profile_v4element_profileconditionedonspanprofileconditionedon"></a><span id="WWAN_profile_v4.element_ProfileConditionedOn"></span>ProfileConditionedOn

Gibt die Bedingungen an, die erfüllt sein müssen, damit ein Profil anwendbar ist.

Dieses Element ist neu für v4. Sie ermöglicht es Ihnen, mehrere Profile anzugeben, die unter verschiedenen Bedingungen gelten, und damit das richtige Profil automatisch verwendet wird, wenn es anwendbar ist. Dieses Element ist optional. Wenn Sie sie nicht angeben, gilt das Profil immer in Bezug auf die aufgeführten Bedingungen.

## <a name="element-hierarchy"></a>Elementhierarchie

[<MBNProfileExt>](element-mbnprofileext.md)  
**<ProfileConditionedOn>**

## <a name="syntax"></a>Syntax

``` syntax
<ProfileConditionedOn>

  <!-- Child elements -->
  CellularClass?,
  RATApplicability?,
  RoamApplicability?,
  IMSI?,
  IwlanApplicability?

</ProfileConditionedOn>
```

### <a name="key"></a>Schlüssel

`?`   optional (null oder eins)

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attribute und Elemente

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Attribute

Keine.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Untergeordnete Elemente


| Untergeordnetes Element | BESCHREIBUNG | 
|---------------|-------------|
| <a href="element-cellularclass.md">CellularClass</a> | <p>Gibt an, dass dieses Profil nur aktiv ist, wenn die aktuelle Mobilfunkklasse die angegebene ist. Andernfalls ist das Profil nicht anwendbar und kann nicht zum Aktivieren eines PDP-Kontexts (Packet Data Protocol) verwendet werden.</p> | 
| <a href="element-imsi.md">IMSI</a> | <p>Gibt an, dass dieses Profil nur aktiv ist, wenn die aktuelle IMSI, die in der CABID verwendet wird, das angegebene Profil ist. Andernfalls ist das Profil nicht anwendbar und kann nicht zum Aktivieren eines PDP-Kontexts (Packet Data Protocol) verwendet werden.</p> | 
| <a href="element-iwlanapplicability.md">IwlanApplicability</a> | <p>Gibt an, dass dieses Profil nur aktiv ist, wenn es mit einem IWLAN-Netzwerk verbunden ist. Andernfalls ist das Profil nicht anwendbar und kann nicht zum Aktivieren eines PDP-Kontexts (Packet Data Protocol) verwendet werden. Der Wert dieses Elements muss ein gültiger <a href="simpletype-iwlanapplicabilitytype.md"><strong>iwlanApplicabilityType-Wert</strong></a> sein.</p> | 
| <a href="element-ratapplicability.md">RATAnwendung</a> | <p>Gibt an, dass dieses Profil nur aktiv ist, wenn der RAT-Typ der angegebene ist. Andernfalls ist das Profil nicht anwendbar und kann nicht zum Aktivieren eines PDP-Kontexts (Packet Data Protocol) verwendet werden.</p> | 
| <a href="element-roamapplicability.md">RoamApplicability</a> | <p>Gibt an, dass dieses Profil nur aktiv ist, wenn die aktuelle Roamingbedingung die angegebene ist. Andernfalls ist das Profil nicht anwendbar und kann nicht zum Aktivieren eines PDP-Kontexts (Packet Data Protocol) verwendet werden. Der Wert dieses Elements muss ein gültiger <a href="simpletype-roamapplicabilitytype.md"><strong>roamApplicabilityType-Wert</strong></a> sein.</p> | 


 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Übergeordnete Elemente


| Übergeordnetes Element | BESCHREIBUNG | 
|----------------|-------------|
| <a href="element-mbnprofileext.md">MBNProfileExt</a> | <p>Das <strong>MBNProfileExt-Element</strong> ist eine Erweiterung des früheren MBNProfile-Elements. Es identifiziert ein mobiles Breitbandprofil mit einem umfangreicheren Satz von Optionen als das MBNProfile-Element.</p><p>Ein Profil kann mehrere MbnProfileExt-Elemente enthalten, die Profileinstellungen für einen bestimmten Satz von Betriebsbedingungen beschreiben. Verwenden Sie das untergeordnete <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn-Element</strong></a> von <strong>MBNProfileExt,</strong> um anzugeben, welche Betriebsbedingungen ein bestimmtes Profil zum aktiven Profil machen.</p> | 


 

## <a name="requirements"></a>Anforderungen


| | | <p>Namespace</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v4</p> | 


 

 



