---
description: Identifiziert die APN-oder Dial-Zeichenfolge, die zum Herstellen einer Datenverbindung verwendet werden soll.
ms.assetid: e791ffa1-b417-480c-adb8-b1dda7547d89
title: Accessstring (ContextType)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AccessString
api_type:
- Schema
ms.openlocfilehash: 8cf0d37b8a1870011ae6ae3ea6febf22a98cdeb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355489"
---
# <a name="accessstring-contexttype-element"></a>Accessstring (ContextType)-Element

Das **accessstring-Element (ContextType)** identifiziert die APN-oder Dial-Zeichenfolge, die zum Herstellen einer Datenverbindung verwendet werden soll.

Dieses Element kann eine maximale Länge von 100 Zeichen aufweisen.

Dieses Element ist optional.

``` syntax
<xs:element name="AccessString">
    <xs:simpleType>
        <xs:restriction
            base="token"
        >
            <xs:minLength
                value="1"
             />
            <xs:maxLength
                value="100"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

Das **accessstring** -Element wird durch den komplexen [**ContextType**](schema-contexttype-complextype.md) -Typ definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ -Desktop-Apps \| UWP-apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitions Kontext des Elements im Schema**
</dt> <dt>

[**contextType**](schema-contexttype-complextype.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**
</dt> <dt>

[**Kontext (mbnprofile)**](schema-context-mbnprofile-element.md)
</dt> </dl>

 

 




