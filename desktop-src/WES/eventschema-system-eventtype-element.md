---
title: System (EventType)-Element
description: Enthält Informationen, die den Anbieter und seine Aktivierung, das Ereignis, den Kanal, in den das Ereignis geschrieben wurde, und Systeminformationen wie prozess- und thread-IDs identifizieren.
ms.assetid: c532cfa3-b722-4227-a403-5c050d62a92c
keywords:
- Systemelement EventLog
topic_type:
- apiref
api_name:
- System
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 85f20b364998fb34f3fe9eb6973770b414de501b60e34df6f97a607acb494947
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118588183"
---
# <a name="system-eventtype-element"></a>System (EventType)-Element

Enthält Informationen, die den Anbieter und seine Aktivierung, das Ereignis, den Kanal, in den das Ereignis geschrieben wurde, und Systeminformationen wie prozess- und thread-IDs identifizieren.

``` syntax
<xs:element name="System"
    type="SystemPropertiesType"
 />
```

Das **System** -Element wird durch den komplexen [**EventType-Typ**](eventschema-eventtype-complextype.md) definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Übergeordnetes Element**
</dt> <dt>

[**event**](eventschema-event-element.md)
</dt> </dl>

 

 





