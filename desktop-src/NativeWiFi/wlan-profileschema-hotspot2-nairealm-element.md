---
description: Eine Liste von NAI-Bereichs Bezeichnern (Network Access Identifier).
ms.assetid: e77802ee-4017-4f04-ae71-5d6d0de8fcf3
title: Nairealm-Element (Hotspot2)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NAIRealm
api_type:
- Schema
api_location: ''
ms.openlocfilehash: a7c8fcf85bd23c13f0e7501d59c3db62c2bf82f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527791"
---
# <a name="nairealm-hotspot2-element"></a>Nairealm-Element (Hotspot2)

Eine Liste von NAI-Bereichs Bezeichnern (Network Access Identifier). Einträge in dieser Liste sind normalerweise in der Form `user@domain` . Die Liste der NAI-Bereiche ist die bevorzugte Methode, um die meisten nicht mobilen Operatoren wie MSOs, Wireline-Operatoren und öffentliche Veranstaltungsorte zu identifizieren.

``` syntax
<xs:element name="NAIRealm"
    minOccurs="0"
>
    <xs:complexType>
        <xs:sequence>
            <xs:element name="name"
                maxOccurs="256"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:minLength
                            value="1"
                         />
                        <xs:maxLength
                            value="255"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

Das-Element wird durch das [**Hotspot2**](wlan-profileschema-hotspot2-element.md) -Element definiert.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element | type | BESCHREIBUNG                                                   |
|---------|------|---------------------------------------------------------------|
| name    |      | Ein einzelner Bereichs Bezeichner. Normalerweise das Formular `user@domain` . |



 

 



