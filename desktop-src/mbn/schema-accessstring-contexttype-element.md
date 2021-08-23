---
description: Identifiziert den APN oder die Wählzeichenfolge, der bzw. die zum Herstellen einer Datenverbindung verwendet werden soll.
ms.assetid: e791ffa1-b417-480c-adb8-b1dda7547d89
title: AccessString (contextType)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AccessString
api_type:
- Schema
ms.openlocfilehash: 603c4aa04bb3e86891ec121233474fa96ffd792cbcb6880bad9e76599003d979
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975279"
---
# <a name="accessstring-contexttype-element"></a>AccessString (contextType)-Element

Das **AccessString-Element (contextType)** identifiziert den APN oder die Wählzeichenfolge, der bzw. die zum Herstellen einer Datenverbindung verwendet werden soll.

Dieses Element kann eine maximale Länge von 100 Zeichen haben.

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

Das **AccessString-Element** wird durch den komplexen [**contextType-Typ**](schema-contexttype-complextype.md) definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps \| UWP-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitionskontext des Elements im Schema**
</dt> <dt>

[**contextType**](schema-contexttype-complextype.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schemainstanz**
</dt> <dt>

[**Context (MBNProfile)**](schema-context-mbnprofile-element.md)
</dt> </dl>

 

 




