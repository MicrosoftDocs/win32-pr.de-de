---
description: Gibt die Einstellung für die automatische Verbindung an, die für ein mobiles Breitband Gerät verwendet werden soll.
ms.assetid: 789016d5-47f1-4506-bcb9-1a4019d236fd
title: ConnectionMode (mbnprofile)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConnectionMode
api_type:
- Schema
ms.openlocfilehash: d9c92227e26bb8858aef28d2f030ac2f84bed06d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958909"
---
# <a name="connectionmode-mbnprofile-element"></a>ConnectionMode (mbnprofile)-Element

Das **ConnectionMode (mbnprofile)** -Element gibt die Einstellung für die automatische Verbindung an, die für ein mobiles Breitband Gerät verwendet werden soll.

Dieses Element kann einen der folgenden Werte aufweisen.



| Wert       | Bedeutung                                                                |
|-------------|------------------------------------------------------------------------|
| Manual    | Nie automatisch eine Verbindung mit dem Netzwerk herstellen.                            |
| automatisch      | Immer automatisch eine Verbindung mit dem Netzwerk herstellen.                           |
| "Auto-Home" | Automatische Verbindung mit dem Netzwerk, außer wenn es sich um ein roamingnetzwerk handelt. |



 

Dieses Element kann maximal ein Vorkommen aufweisen.

Dies ist ein erforderliches Element.

``` syntax
<xs:element name="ConnectionMode">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="manual"
             />
            <xs:enumeration
                value="auto"
             />
            <xs:enumeration
                value="auto-home"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

Das **ConnectionMode** -Element wird durch das [**mbnprofile**](schema-mbnprofile-element.md) -Element definiert.

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

 

 




