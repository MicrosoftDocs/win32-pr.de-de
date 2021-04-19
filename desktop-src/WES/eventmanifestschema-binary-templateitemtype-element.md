---
title: Binary (templateitemtype)-Element
description: Enthält die Binärdaten, die von der Ereignisprotokoll-API bereitgestellt werden.
ms.assetid: 3ad9c119-9395-49d3-b920-9a071bcc6a04
keywords:
- Ereignisprotokoll für das binäre Element
topic_type:
- apiref
api_name:
- binary
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3c3e281da662b4cdd0ecacc81a88f1a5728f90da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338783"
---
# <a name="binary-templateitemtype-element"></a>Binary (templateitemtype)-Element

Enthält die Binärdaten, die von der [Ereignisprotokoll](/windows/desktop/EventLog/event-logging) -API bereitgestellt werden.

``` syntax
<xs:element name="binary">
    <xs:complexType>
        <xs:attribute name="name"
            type="string"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

Das **Binary** -Element wird durch den komplexen Typ [**templateitemtype**](eventmanifestschema-templateitemtype-complextype.md) definiert.

## <a name="attributes"></a>Attributes



| Name | type   | BESCHREIBUNG                                          |
|------|--------|------------------------------------------------------|
| name | Zeichenfolge | Der Name, der den Binärdaten zugeordnet ist.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Übergeordnetes Element**
</dt> <dt>

[**Vorlage (templatelisttype)**](eventmanifestschema-template-templatelisttype-element.md)
</dt> </dl>

 

