---
description: IsAdditionalPdpContextProfile
MS-HAID: WWAN\_profile\_v3.element\_IsAdditionalPdpContextProfile
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IsAdditionalPdpContextProfile
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a075916144971196433d1a490a9076c4d40ddb86b363d2904d1affce63a5995
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118745122"
---
# <a name="span-idwwan_profile_v3element_isadditionalpdpcontextprofilespanisadditionalpdpcontextprofile"></a><span id="WWAN_profile_v3.element_IsAdditionalPdpContextProfile"></span>IsAdditionalPdpContextProfile

Das **IsAdditionalPdpContextProfile-Element** enthält einen  booleschen Wert, der true ist, wenn es sich um ein "zusätzliches PDP -Kontextprofil (Packet Data Protocol)" handelt, andernfalls **false.**  Die Standardeinstellung lautet **false**.

Ein "zusätzliches PDP-Kontextprofil" ist ein Profil, das nicht über den Standardport des physischen Adapters aktiviert wird. Wenn Sie dieses Element auf TRUE festlegen, wird sichergestellt, dass dieses Profil in der Benutzeroberfläche nicht falsch angezeigt wird.

Beachten Sie Folgendes: Wenn dieses Element auf TRUE festgelegt ist, muss auch Folgendes zutreffen.

-   Das [**IsDefault-Element**](./schema-isdefault-mbnprofile-element.md) muss nicht angegeben oder auf **FALSE** festgelegt sein, damit das Profil gültig ist.
-   Das [**ConnectionMode-Element**](./schema-connectionmode-mbnprofile-element.md) muss nicht angegeben oder auf manuell festgelegt **sein,** damit das Profil gültig ist.

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

Dieses äußerste Element (Dokument) darf nicht in anderen Elementen enthalten sein.

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

 

 
