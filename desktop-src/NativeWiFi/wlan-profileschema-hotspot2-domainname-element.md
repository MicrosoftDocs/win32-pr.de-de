---
description: Der Domänen Name für den Heimnetzwerk Anbieter des Geräts, der den Netzwerk Operator identifiziert.
ms.assetid: 7676e1d8-a414-401f-989c-9f60068b92d8
title: Domain Name (Hotspot2)-Element
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
ms.openlocfilehash: 670fc91771ee0a47cd7f16f617d052df2e567b2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354519"
---
# <a name="domainname-hotspot2-element"></a>Domain Name (Hotspot2)-Element

Der Domänen Name für den Heimnetzwerk Anbieter des Geräts, der den Netzwerk Operator identifiziert.

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

Das-Element wird durch das [**Hotspot2**](wlan-profileschema-hotspot2-element.md) -Element definiert.

 

 



