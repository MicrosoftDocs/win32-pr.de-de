---
description: Enthält den Ausführungs Kontext des Druckertreibers, der getprintexecutiondata aufruft.
ms.assetid: 1fd25ed9-6f28-48f9-8132-d48fffc956ec
title: PRINT_EXECUTION_DATA Struktur (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINT_EXECUTION_DATA
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 0e33f77a3140c62a1f472fc27948ec26a7ecf3ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217391"
---
# <a name="print_execution_data-structure"></a>\_ \_ Datenstruktur der Druck Ausführung

Enthält den Ausführungs Kontext des Druckertreibers, der [**getprintexecutiondata**](getprintexecutiondata.md)aufruft.

## <a name="syntax"></a>Syntax


```C++
typedef struct _PRINT_EXECUTION_DATA {
  PRINT_EXECUTION_CONTEXT  context;
  DWORD                    clientAppPID;
} PRINT_EXECUTION_DATA;
```



## <a name="members"></a>Member

<dl> <dt>

**context**
</dt> <dd>

Der [**\_ \_ Kontextwert der Druck Ausführung**](print-execution-context.md) , der den aktuellen Ausführungs Kontext des Druckertreibers darstellt.

</dd> <dt>

**clientapppid**
</dt> <dd>

Wenn der Wert des **Kontexts** " **Druck \_ Ausführungs \_ Kontext \_ WOW64**" ist, identifiziert **clientapppid** die Client Anwendung, in deren Auftrag der splwow64.exe Prozess den Druckertreiber geladen hat. Wenn der Wert des **Kontexts** nicht der **Druck \_ Ausführungs \_ Kontext \_ WOW64** ist, ist **clientapppid** gleich 0 (null).

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                                                   |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Getprintexecutiondata**](getprintexecutiondata.md)
</dt> <dt>

[**Druck \_ Ausführungs \_ Kontext**](print-execution-context.md)
</dt> </dl>

 

 




