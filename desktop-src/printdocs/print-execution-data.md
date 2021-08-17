---
description: Enthält den Ausführungskontext des Druckertreibers, der GetPrintExecutionData aufruft.
ms.assetid: 1fd25ed9-6f28-48f9-8132-d48fffc956ec
title: PRINT_EXECUTION_DATA-Struktur (Winspool.h)
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
ms.openlocfilehash: e67b43089c275baf59295f15e84d9bf38d1a3a5ff6e2adfaf2d270b02e2ad967
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119447140"
---
# <a name="print_execution_data-structure"></a>PRINT \_ EXECUTION \_ DATA-Struktur

Enthält den Ausführungskontext des Druckertreibers, der [**GetPrintExecutionData aufruft.**](getprintexecutiondata.md)

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

Der [**PRINT \_ EXECUTION \_ CONTEXT-Wert,**](print-execution-context.md) der den aktuellen Ausführungskontext des Druckertreibers darstellt.

</dd> <dt>

**clientAppPID**
</dt> <dd>

Wenn der Wert des **Kontexts** **PRINT EXECUTION CONTEXT \_ \_ \_ WOW64** lautet, identifiziert **clientAppPID** die Clientanwendung, in deren Auftrag der splwow64.exe Prozess den Druckertreiber geladen hat. Wenn der Wert von **context** nicht **PRINT EXECUTION CONTEXT \_ \_ \_ WOW64** ist, ist **clientAppPID** 0 (null).

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                                   |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**GetPrintExecutionData**](getprintexecutiondata.md)
</dt> <dt>

[**\_ \_ DRUCKAUSFÜHRUNGSKONTEXT**](print-execution-context.md)
</dt> </dl>

 

 




