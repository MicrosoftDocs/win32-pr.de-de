---
description: IsAdditionalPdpContextProfile
MS-HAID: WWAN\_profile\_v3.element\_IsAdditionalPdpContextProfile
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IsAdditionalPdpContextProfile
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0d4547bd97645ec5f3e378ac53df0f9e1ed78e7
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988713"
---
# <a name="span-idwwan_profile_v3element_isadditionalpdpcontextprofilespanisadditionalpdpcontextprofile"></a><span id="WWAN_profile_v3.element_IsAdditionalPdpContextProfile"></span>IsAdditionalPdpContextProfile

Das **IsAdditionalPdpContextProfile-Element** enthält einen **booleschen Wert,** der **true** ist, wenn dies ein "zusätzlicher PDP(Packet Data Protocol)"-Kontextprofil und **false** ist, andernfalls . Die Standardeinstellung lautet **false**.

Ein Profil mit "zusätzlichem PDP-Kontext" ist ein Profil, das nicht über den Standardport des physischen Adapters aktiviert wird. Durch Festlegen dieses Elements auf TRUE wird sichergestellt, dass dieses Profil nicht unangemessen auf der Benutzeroberfläche angezeigt wird.

Beachten Sie Folgendes, wenn dieses Element auf TRUE festgelegt ist.

-   Das [**IsDefault-Element**](./schema-isdefault-mbnprofile-element.md) muss nicht angegeben oder auf **FALSE** festgelegt sein, damit das Profil gültig ist.
-   Das [**ConnectionMode-Element**](./schema-connectionmode-mbnprofile-element.md) muss nicht angegeben oder auf **manuell** festgelegt sein, damit das Profil gültig ist.

## <a name="element-hierarchy"></a>Elementhierarchie

**&lt;IsAdditionalPdpContextProfile&gt;**

## <a name="syntax"></a>Syntax

``` syntax
<IsAdditionalPdpContextProfile>

  boolean

</IsAdditionalPdpContextProfile>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attribute und Elemente

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Attribute

Keine.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Untergeordnete Elemente

Keine.

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Übergeordnete Elemente

Dieses äußerste Element (Dokument) darf nicht in anderen Elementen enthalten sein.

## <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p>Namespace</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v3</p> | 


 

 
