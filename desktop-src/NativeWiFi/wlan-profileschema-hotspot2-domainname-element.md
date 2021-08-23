---
description: Der Domänenname für den Heimnetzwerkanbieter des Geräts, der den Betreiber des Netzwerks identifiziert.
ms.assetid: 7676e1d8-a414-401f-989c-9f60068b92d8
title: DomainName (Hotspot2)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DomainName
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 216d29e578b3e6f86942df4eaac33112de27759984b384a5fd548221513e00f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684240"
---
# <a name="domainname-hotspot2-element"></a>DomainName (Hotspot2)-Element

Der Domänenname für den Heimnetzwerkanbieter des Geräts, der den Betreiber des Netzwerks identifiziert.

``` syntax
<xs:element name="DomainName"
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
```

Das -Element wird durch das [**Hotspot2-Element**](wlan-profileschema-hotspot2-element.md) definiert.

 

 



