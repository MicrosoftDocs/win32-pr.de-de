---
description: Enthalten entweder den Namen oder die Beschreibung eines WLAN-Profils.
ms.assetid: cb30d76f-051f-4b90-a0e0-24088a99ca9b
title: einfacher nametype-Typ (LAN_policy) (Profil)
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
ms.openlocfilehash: e73e8bd013836767e2a943616407aea9f563fea2
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2021
ms.locfileid: "106360470"
---
# <a name="nametype-simple-type-lan_policy-for-profileschema"></a>nametype Simple Type (LAN_policy) für profileschema

Der einfache nametype-Typ kann entweder den Namen oder eine Beschreibung eines WLAN-Profils enthalten. Dieser Zeichen folgen Wert muss zwischen 1 und 255 Zeichen lang sein.

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
|-------------------------------------|---------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista, Windows XP mit SP3 \[ Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                |
| Verteilbare Komponente<br/>          | Drahtlose LAN-API für Windows XP mit SP2<br/>                 |



 

 




