---
description: Identifiziert den Stammknoten des Leistungsindikatorabschnitts eines Instrumentierungsmanifests.
ms.assetid: f16f432b-466f-4a3c-bc1b-e80b876a2511
title: counters-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d76707f662e756353f215872264cfa3703686fd06d0840fde858d75d26c9693f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119380850"
---
# <a name="counters-element"></a>counters-Element

Identifiziert den Stammknoten des Leistungsindikatorabschnitts eines Instrumentierungsmanifests.

``` syntax
<xs:element name="counters"
    type="man:counters"
>
    <xs:key name="uniqueprovGUID">
        <xs:selector
            xpath="./man:provider"
         />
        <xs:field
            xpath="@providerGuid"
         />
    </xs:key>
    <xs:key name="uniqueCounterSetGUID">
        <xs:selector
            xpath="./man:provider/man:counterSet"
         />
        <xs:field
            xpath="@guid"
         />
    </xs:key>
    <xs:key name="uniqueCounterSetURI">
        <xs:selector
            xpath="./man:provider/man:counterSet"
         />
        <xs:field
            xpath="@uri"
         />
    </xs:key>
    <xs:key name="uniqueCounterSetName">
        <xs:selector
            xpath="./man:provider/man:counterSet"
         />
        <xs:field
            xpath="@name"
         />
    </xs:key>
    <xs:key name="uniqueCounterSetSymbol">
        <xs:selector
            xpath="./man:provider/man:counterSet"
         />
        <xs:field
            xpath="@symbol"
         />
    </xs:key>
    <xs:unique name="uniqueCounterSymbol">
        <xs:selector
            xpath="./man:provider/man:counterSet/man:counter"
         />
        <xs:field
            xpath="@symbol"
         />
    </xs:unique>
    <xs:key name="uniqueCounterURI">
        <xs:selector
            xpath="./man:provider/man:counterSet/man:counter"
         />
        <xs:field
            xpath="@uri"
         />
    </xs:key>
</xs:element>
```

## <a name="remarks"></a>Hinweise

Der übergeordnete Knoten dieses Elements ist das [**Instrumentierungselement**](/windows/desktop/WES/eventmanifestschema-instrumentationtype-complextype) des Manifests.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

