---
description: Definiert einen Zeichen foltentyp für den Namen oder die Beschreibung eines Drahtlos-LAN-Richtlinien Profils.
ms.assetid: a01e8789-3401-4e58-b733-2ec95fc895b6
title: einfacher nametype-Typ (LAN_policy)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- nameType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 8a2c0bdf281e27ba7a85271fe7777076ada9ff2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363751"
---
# <a name="nametype-simple-type-lan_policy"></a>einfacher nametype-Typ (LAN_policy)

Der einfache nametype-Typ definiert einen Zeichen foltentyp für den Namen oder die Beschreibung eines Drahtlos-LAN-Richtlinien Profils. Namen und Beschreibungen sind Zeichen folgen, die mindestens ein Zeichen lang und höchstens 255 Zeichen lang sind.

``` syntax
<xs:simpleType name="nameType">
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
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 




