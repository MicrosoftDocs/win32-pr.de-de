---
description: Eine Liste von BEREICHSbezeichnern (Network Access Identifier, NAI).
ms.assetid: e77802ee-4017-4f04-ae71-5d6d0de8fcf3
title: NAIRealm-Element (Hotspot2)
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
ms.openlocfilehash: 084ee3ce04a560ce50c3ab0391f808bc09aed1bb90da6a34b86755b9b64ae772
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684210"
---
# <a name="nairealm-hotspot2-element"></a>NAIRealm-Element (Hotspot2)

Eine Liste von BEREICHSbezeichnern (Network Access Identifier, NAI). Einträge in dieser Liste haben in der Regel das Formular `user@domain` . Die LISTE DES BEREICHS ist die bevorzugte Methode, um die meisten Nicht-Mobilfunkanbieter wie MSOs, Wirelineoperatoren und öffentliche Veranstaltungsorte zu identifizieren.

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

Das -Element wird durch das [**Hotspot2-Element**](wlan-profileschema-hotspot2-element.md) definiert.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element | Typ | Beschreibung                                                   |
|---------|------|---------------------------------------------------------------|
| name    |      | Ein einzelner Bereichsbezeichner. In der Regel im Formular `user@domain` . |



 

 



