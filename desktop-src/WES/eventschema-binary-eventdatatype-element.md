---
title: Binary (eventdatatype)-Element
description: Ein binäres Daten-BLOB für Ereignisse, die mithilfe der Ereignisprotokollierung geschrieben werden.
ms.assetid: aec2557f-6d63-48e7-b4d7-584e99dfcce3
keywords:
- Ereignisprotokoll für das binäre Element
topic_type:
- apiref
api_name:
- Binary
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cdfd00e2d25f3178ab44081f76725b3189f1010b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040118"
---
# <a name="binary-eventdatatype-element"></a>Binary (eventdatatype)-Element

Ein binäres Daten-BLOB für Ereignisse, die mithilfe der [Ereignisprotokollierung](/windows/desktop/EventLog/event-logging)geschrieben werden.

``` syntax
<xs:element name="Binary"
    type="hexBinary"
 />
```

Das **Binary** -Element wird durch den komplexen [**eventdatatype**](eventschema-eventdatatype-complextype.md) -Typ definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Übergeordnetes Element**
</dt> <dt>

[**EVENTDATA (EventType)**](eventschema-eventdata-eventtype-element.md)
</dt> </dl>

 

