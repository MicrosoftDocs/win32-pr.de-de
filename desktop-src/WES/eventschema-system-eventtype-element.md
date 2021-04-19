---
title: System (EventType)-Element
description: Enthält Informationen, die den Anbieter und die Art der Aktivierung, das Ereignis, den Kanal, in den das Ereignis geschrieben wurde, und Systeminformationen, wie z. b. den Prozess und die Thread-IDs, identifiziert.
ms.assetid: c532cfa3-b722-4227-a403-5c050d62a92c
keywords:
- System Element-Ereignisprotokoll
topic_type:
- apiref
api_name:
- System
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4fef0f9f9e24a855564a8d3df2f94610ff9a8248
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341772"
---
# <a name="system-eventtype-element"></a>System (EventType)-Element

Enthält Informationen, die den Anbieter und die Art der Aktivierung, das Ereignis, den Kanal, in den das Ereignis geschrieben wurde, und Systeminformationen, wie z. b. den Prozess und die Thread-IDs, identifiziert.

``` syntax
<xs:element name="System"
    type="SystemPropertiesType"
 />
```

Das **System** Element wird durch den komplexen [**eventType**](eventschema-eventtype-complextype.md) -Typ definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Übergeordnetes Element**
</dt> <dt>

[**event**](eventschema-event-element.md)
</dt> </dl>

 

 





