---
description: Gibt die Liste der bevorzugten Netzwerkanbieter zum Zeitpunkt des Roamings an.
ms.assetid: 5873fcd7-8e89-4edd-8dc5-f43675919c55
title: Dataroamingpartners (mbnprofile)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DataRoamingPartners
api_type:
- Schema
ms.openlocfilehash: 7f721abd608dd241c399f16eee90369ebcf19594
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353102"
---
# <a name="dataroamingpartners-mbnprofile-element"></a>Dataroamingpartners (mbnprofile)-Element

Das **dataroamingpartners (mbnprofile)** -Element gibt die Liste der bevorzugten Netzwerkanbieter zum Zeitpunkt des Roamings an.

Der Mobile Breitbanddienst verwendet dieses Element, um beim Roaming das bevorzugte Netzwerk auszuwählen.

Das-Element hat das folgende untergeordnete Element, das mindestens einmal definiert werden muss, aber mehrmals definiert werden kann.

-   [**Anbieter**](schema-provider-dataroamingpartners-element.md)

Dieses Element kann maximal ein Vorkommen aufweisen.

Dieses Element ist optional.

``` syntax
<xs:element name="DataRoamingPartners">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="Provider"
                type="providerType"
                maxOccurs="unbounded"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

Das **dataroamingpartners** -Element wird durch das [**mbnprofile**](schema-mbnprofile-element.md) -Element definiert.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                         | type                                                    | BESCHREIBUNG                                            |
|-----------------------------------------------------------------|---------------------------------------------------------|--------------------------------------------------------|
| [**Anbieter**](schema-provider-dataroamingpartners-element.md) | [**Provider Type**](schema-providertype-complextype.md) | Der Name und die Anbieter-ID eines Mobil Funk Netzwerks.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ -Desktop-Apps \| UWP-apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitions Kontext des Elements im Schema**
</dt> <dt>

[**Mbnprofile**](schema-mbnprofile-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**
</dt> <dt>

[**Mbnprofile**](schema-mbnprofile-element.md)
</dt> </dl>

 

 




