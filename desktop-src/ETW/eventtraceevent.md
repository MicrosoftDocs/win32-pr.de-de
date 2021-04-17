---
description: Die übergeordnete Klasse für Protokoll Header Ereignisse. Diese Klasse ist immer die erste Ereignis Ablauf Verfolgungs Klasse, die an einen Consumer gesendet wird (dieses Ereignis wird nicht an Echt Zeit Consumer gesendet). Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: fb507d9a-6ed2-4cb1-8cea-85c0a3832e51
title: Eventtraceevent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EventTraceEvent
api_type:
- NA
api_location: ''
ms.openlocfilehash: 0036ee0a49225568aac066735824fe55ce8f0fa6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977672"
---
# <a name="eventtraceevent-class"></a>Eventtraceevent-Klasse

Die übergeordnete Klasse für Protokoll Header Ereignisse. Diese Klasse ist immer die erste Ereignis Ablauf Verfolgungs Klasse, die an einen Consumer gesendet wird (dieses Ereignis wird nicht an Echt Zeit Consumer gesendet).

Die folgende Syntax wird durch den MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[Guid("{68fdd900-4a3e-11d1-84f4-0000f80464e3}")]
class EventTraceEvent : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Member

Die **eventtraceevent** -Klasse definiert keine Member.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MSNT \_ systemtrace**](msnt-systemtrace.md)
</dt> <dt>

[**EventTrace- \_ Header**](eventtrace-header.md)
</dt> </dl>

 

 




