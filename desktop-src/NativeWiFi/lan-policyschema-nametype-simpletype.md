---
description: Definiert einen Zeichenfolgentyp für den Namen oder die Beschreibung eines kabelgebundenen LAN-Richtlinienprofils.
ms.assetid: 89de1e7a-618d-4501-a134-c7a37f9c552d
title: nameType simple type (LAN_policy)
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
ms.openlocfilehash: 3b3d558717777c9b2bead2fd7e141dee38b22491af4142d4948c7f1f76aadfd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065110"
---
# <a name="nametype-simple-type-lan_policy"></a>nameType simple type (LAN_policy)

Der einfache NameType-Typ definiert einen Zeichenfolgentyp für den Namen oder die Beschreibung eines kabelgebundenen LAN-Richtlinienprofils. Namen und Beschreibungen sind Zeichenfolgen, die mindestens ein Zeichen lang und mindestens 255 Zeichen lang sind.

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
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 




