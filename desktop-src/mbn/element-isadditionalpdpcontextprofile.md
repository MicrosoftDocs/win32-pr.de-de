---
description: Isadditionalpdpcontextprofile
MS-HAID: WWAN\_profile\_v3.element\_IsAdditionalPdpContextProfile
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Isadditionalpdpcontextprofile
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 169aa9a34a561f65eed5dfc315e7711ef6bb9bf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343358"
---
# <a name="span-idwwan_profile_v3element_isadditionalpdpcontextprofilespanisadditionalpdpcontextprofile"></a><span id="WWAN_profile_v3.element_IsAdditionalPdpContextProfile"></span>Isadditionalpdpcontextprofile

Das **isadditionalpdpcontextprofile** -Element enthält einen **booleschen** Wert, der **true** ist, wenn es sich um ein "zusätzliches PDP (Packet Data Protocol)"-Kontext Profil handelt, andernfalls " **false**". Die Standardeinstellung lautet **false**.

Ein "zusätzliches PDP-Kontext Profil" ist ein Profil, das nicht über den Standardport des physischen Adapters aktiviert wird. Wenn dieses Element auf "true" festgelegt wird, wird sichergestellt, dass dieses Profil nicht unpassend in der Benutzeroberfläche angezeigt wird.

Beachten Sie Folgendes: Wenn dieses Element auf "true" festgelegt ist, muss Folgendes ebenfalls zutreffen:

-   Das [**IsDefault**](./schema-isdefault-mbnprofile-element.md) -Element muss nicht angegeben werden, oder es muss auf **false** festgelegt werden, damit das Profil gültig ist.
-   Das [**ConnectionMode**](./schema-connectionmode-mbnprofile-element.md) -Element muss nicht angegeben werden oder auf " **Manual** " festgelegt sein, damit das Profil gültig ist.

## <a name="element-hierarchy"></a>Elementhierarchie

**<IsAdditionalPdpContextProfile>**

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

Dieses äußerste (Dokument-) Element darf nicht in anderen Elementen enthalten sein.

## <a name="requirements"></a>Anforderungen

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Namespace</p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v3</p></td>
</tr>
</tbody>
</table>

 

 
