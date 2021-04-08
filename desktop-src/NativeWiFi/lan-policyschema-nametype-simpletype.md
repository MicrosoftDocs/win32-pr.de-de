---
description: Definiert einen Zeichen foltentyp für den Namen oder die Beschreibung eines Richtlinien Profils für ein kabelgebundenes LAN.
ms.assetid: 89de1e7a-618d-4501-a134-c7a37f9c552d
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
ms.openlocfilehash: 702ee6340fa3d03217c884a48625d3a38be4ad9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960145"
---
# <a name="nametype-simple-type-lan_policy"></a>einfacher nametype-Typ (LAN_policy)

Der einfache nametype-Typ definiert einen Zeichen foltentyp für den Namen oder die Beschreibung eines Richtlinien Profils für ein kabelgebundenes LAN. Namen und Beschreibungen sind Zeichen folgen, die mindestens ein Zeichen lang und höchstens 255 Zeichen lang sind.

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



 

 




