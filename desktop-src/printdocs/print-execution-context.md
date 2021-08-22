---
description: Stellt den Ausführungskontext dar, wenn GetPrintExecutionData aufgerufen wird.
ms.assetid: b6c026b2-8519-45d3-9614-b502eec23cde
title: PRINT_EXECUTION_CONTEXT-Enumeration (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINT_EXECUTION_CONTEXT
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 78e4afb29b75c0a73799302ddb76e270b18ca2c38cb6325b59ebae5041d5f99e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119033958"
---
# <a name="print_execution_context-enumeration"></a>PRINT \_ EXECUTION \_ CONTEXT-Enumeration

Stellt den Ausführungskontext dar, wenn [**GetPrintExecutionData**](getprintexecutiondata.md) aufgerufen wird.

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  PRINT_EXECUTION_CONTEXT_APPLICATION             = 0,
  PRINT_EXECUTION_CONTEXT_SPOOLER_SERVICE         = 1,
  PRINT_EXECUTION_CONTEXT_SPOOLER_ISOLATION_HOST  = 2,
  PRINT_EXECUTION_CONTEXT_FILTER_PIPELINE         = 3,
  PRINT_EXECUTION_CONTEXT_WOW64                   = 4
} PRINT_EXECUTION_CONTEXT;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="PRINT_EXECUTION_CONTEXT_APPLICATION"></span><span id="print_execution_context_application"></span>**\_ \_ DRUCKAUSFÜHRUNGSKONTEXTANWENDUNG \_**
</dt> <dd>

Der Aufrufer wird in einer Anwendung ausgeführt.

</dd> <dt>

<span id="PRINT_EXECUTION_CONTEXT_SPOOLER_SERVICE"></span><span id="print_execution_context_spooler_service"></span>**\_ \_ \_ DRUCKAUSFÜHRUNGSKONTEXT-SPOOLERDIENST \_**
</dt> <dd>

Der Aufrufer wird im Spoolerdienst (spoolsv.exe) ausgeführt.

</dd> <dt>

<span id="PRINT_EXECUTION_CONTEXT_SPOOLER_ISOLATION_HOST"></span><span id="print_execution_context_spooler_isolation_host"></span>**\_ \_ \_ DRUCKAUSFÜHRUNGSKONTEXTSPOOLERISOLATIONSHOST \_ \_**
</dt> <dd>

Der Aufrufer wird auf dem Druckisolationshost (PrintIsolationHost.exe) ausgeführt.

</dd> <dt>

<span id="PRINT_EXECUTION_CONTEXT_FILTER_PIPELINE"></span><span id="print_execution_context_filter_pipeline"></span>**\_ \_ \_ DRUCKAUSFÜHRUNGSKONTEXTFILTERPIPELINE \_**
</dt> <dd>

Der Aufrufer wird in der Druckfilterpipeline (printfilterpipelinesvc.exe) ausgeführt.

</dd> <dt>

<span id="PRINT_EXECUTION_CONTEXT_WOW64"></span><span id="print_execution_context_wow64"></span>**\_DRUCKAUSFÜHRUNGSKONTEXT \_ \_ WOW64**
</dt> <dd>

Der Aufrufer wird in splwow64.exe

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                                   |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**GetPrintExecutionData**](getprintexecutiondata.md)
</dt> <dt>

[**\_ \_ DRUCKAUSFÜHRUNGSDATEN**](print-execution-data.md)
</dt> </dl>

 

 




