---
description: Gibt an, ob die Komprimierung für den Daten Link für die Kopfzeile und die Datenübertragung verwendet wird.
ms.assetid: 2aee93e4-d124-43cb-b974-19f00eb4d6a6
title: Compression (ContextType)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Compression
api_type:
- Schema
ms.openlocfilehash: 0da6665f69c2791669f75b91e847081dbcc351e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862763"
---
# <a name="compression-contexttype-element"></a>Compression (ContextType)-Element

Das **Compression (ContextType)** -Element gibt an, ob die Komprimierung für den Daten Link für den Header und die Datenübertragung verwendet wird.

Bei diesem Element kann es sich um einen der folgenden Werte handeln:

| Wert     | Bedeutung                       |
|-----------|-------------------------------|
| Fähigen  | Die Komprimierung wird verwendet.     |
| Ier | Die Komprimierung wird nicht verwendet. |



 

Dieses Element ist optional. Wenn dieses Element nicht angegeben ist, verwendet das Mobile Breitbandsystem keine Komprimierung.

``` syntax
<xs:element name="Compression">
    <xs:simpleType>
        <xs:restriction
            base="token"
        >
            <xs:enumeration
                value="DISABLE"
             />
            <xs:enumeration
                value="ENABLE"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

Das **Komprimierungs** Element wird durch den komplexen [**ContextType**](schema-contexttype-complextype.md) -Typ definiert.

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

 

 




