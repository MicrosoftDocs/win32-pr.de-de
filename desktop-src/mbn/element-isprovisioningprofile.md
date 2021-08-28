---
description: IsProvisioningProfile
MS-HAID: WWAN\_profile\_v4.element\_IsProvisioningProfile
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IsProvisioningProfile
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0bacf17e9f9e73f4e442cff7c00acab79454e05
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883533"
---
# <a name="span-idwwan_profile_v4element_isprovisioningprofilespanisprovisioningprofile"></a><span id="WWAN_profile_v4.element_IsProvisioningProfile"></span>IsProvisioningProfile

Gibt an, dass dieses Profil nur für die Bereitstellung verwendet werden soll. Andernfalls ist das Profil nicht anwendbar und kann nicht zum Aktivieren eines PDP-Kontexts (Packet Data Protocol) verwendet werden. Dieses Element ist neu für v4.

Wenn **IsProvisioningProfile** true ist, [**muss IsDefault**](element-isdefault.md) false und [**ConnectionMode**](element-connectionmode.md) manuell sein.

## <a name="element-hierarchy"></a>Elementhierarchie

[&lt;MBNProfileExt&gt;](element-mbnprofileext.md)  
**&lt;IsProvisioningProfile&gt;**

## <a name="syntax"></a>Syntax

``` syntax
<IsProvisioningProfile>

  boolean

</IsProvisioningProfile>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attribute und Elemente

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Attribute

Keine.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Untergeordnete Elemente

Keine.

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Übergeordnete Elemente


| Übergeordnetes Element | Beschreibung | 
|----------------|-------------|
| <a href="element-mbnprofileext.md">MBNProfileExt</a> | <p>Das <strong>MBNProfileExt-Element</strong> ist eine Erweiterung des früheren MBNProfile-Elements. Es identifiziert ein Mobile Broadband-Profil mit einem vielfältigeren Satz von Optionen als das MBNProfile-Element.</p><p>Es kann mehrere MbnProfileExt-Elemente in einem Profil geben, die Profileinstellungen für einen bestimmten Satz von Betriebsbedingungen beschreiben. Verwenden Sie <a href="element-profileconditionedon.md"><strong>das untergeordnete ProfileConditionedOn-Element</strong></a> von <strong>MBNProfileExt,</strong> um anzugeben, welche Betriebsbedingungen ein bestimmtes Profil zum aktiven Profil machen.</p> | 


 

## <a name="requirements"></a>Requirements (Anforderungen)


| | | <p>Namespace</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v4</p> | 


 

 



