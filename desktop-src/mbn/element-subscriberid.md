---
description: Subscriberid
MS-HAID: WWAN\_profile\_v4.element\_SubscriberID
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Subscriberid
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71a97eb32d38e058189a6523b0c8c77fb5b006d2
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985403"
---
# <a name="span-idwwan_profile_v4element_subscriberidspansubscriberid"></a><span id="WWAN_profile_v4.element_SubscriberID"></span>Subscriberid

Identifiziert den eindeutigen Bezeichner des Profils.

Für ein GSM-Netzwerk sollte dieses das IMSI (International Mobile Subscriber Identity) der SIM und für CDMA-Geräte die MIN (Mobile Identification Number) des Geräts enthalten.

Weitere Informationen finden Sie in der Dokumentation zum v1 [**SubscriberID-Element.**](./schema-subscriberid-mbnprofile-element.md)

## <a name="element-hierarchy"></a>Elementhierarchie

[&lt;MBNProfileExt&gt;](element-mbnprofileext.md)  
**&lt;Subscriberid&gt;**

## <a name="syntax"></a>Syntax

``` syntax
<SubscriberID>

  subscriberIdType

</SubscriberID>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attribute und Elemente

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Attribute

Keine.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Untergeordnete Elemente

Keine.

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Übergeordnete Elemente


| Übergeordnetes Element | BESCHREIBUNG | 
|----------------|-------------|
| <a href="element-mbnprofileext.md">MBNProfileExt</a> | <p>Das <strong>MBNProfileExt-Element</strong> ist eine Erweiterung des früheren MBNProfile-Elements. Es identifiziert ein Mobile Broadband-Profil mit einem vielfältigeren Satz von Optionen als das MBNProfile-Element.</p><p>Es kann mehrere MbnProfileExt-Elemente in einem Profil geben, die Profileinstellungen für einen bestimmten Satz von Betriebsbedingungen beschreiben. Verwenden Sie <a href="element-profileconditionedon.md"><strong>das untergeordnete ProfileConditionedOn-Element</strong></a> von <strong>MBNProfileExt,</strong> um anzugeben, welche Betriebsbedingungen ein bestimmtes Profil zum aktiven Profil machen.</p> | 


 

## <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p>Namespace</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v4</p> | 


 

 
