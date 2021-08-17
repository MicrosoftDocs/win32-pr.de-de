---
description: Diese Klasse ist die Ereignistypklasse für Threadendereignisse. Die folgende Syntax wird durch einen MOF-Code vereinfacht.
ms.assetid: c495bf22-04ce-4285-8e7e-152e4ab65823
title: Thread_V1_TypeGroup2-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread_V1_TypeGroup2
- Thread_V1_TypeGroup2.ProcessId
- Thread_V1_TypeGroup2.TThreadId
api_type:
- NA
api_location: ''
ms.openlocfilehash: d00e2d535cdc0fe14d2ae0f48fb7809f627b24fe19cdaff5d63750ee9b5f2c42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117814237"
---
# <a name="thread_v1_typegroup2-class"></a>Thread \_ V1 \_ TypeGroup2-Klasse

Diese Klasse ist die Ereignistypklasse für Threadendereignisse.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[EventType{2, 4}, EventTypeName{"End", "DCEnd"}]
class Thread_V1_TypeGroup2 : Thread_V1
{
  uint32 ProcessId;
  uint32 TThreadId;
};
```

## <a name="members"></a>Member

Die **Klasse Thread \_ V1 \_ TypeGroup2** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Klasse Thread \_ V1 \_ TypeGroup2** verfügt über diese Eigenschaften.

<dl> <dt>

ProcessId
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(1)
</dt> </dl>

Prozessbezeichner des threads, der am Ereignis beteiligt ist.

**Windows Server 2003:** Enthält den Format("x")-Qualifizierer.

</dd> <dt>

TThreadId
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(2)
</dt> </dl>

Threadbezeichner des Threads, der am Ereignis beteiligt ist.

**Windows Server 2003:** Enthält den Format("x")-Qualifizierer.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Thread \_ V1**](thread-v1.md)
</dt> </dl>

 

 




