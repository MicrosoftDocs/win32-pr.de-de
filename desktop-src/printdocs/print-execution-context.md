---
description: Stellt den Ausführungs Kontext dar, wenn getprintexecutiondata aufgerufen wird.
ms.assetid: b6c026b2-8519-45d3-9614-b502eec23cde
title: PRINT_EXECUTION_CONTEXT-Enumeration (winspool. h)
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
ms.openlocfilehash: 20b1050edc0088fb629ee10cf63dc9cffa07228a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215968"
---
# <a name="print_execution_context-enumeration"></a>\_Enumeration des druckausführungs \_ Kontexts

Stellt den Ausführungs Kontext dar, wenn [**getprintexecutiondata**](getprintexecutiondata.md) aufgerufen wird.

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

<span id="PRINT_EXECUTION_CONTEXT_APPLICATION"></span><span id="print_execution_context_application"></span>**Druck \_ Ausführungs \_ Kontext- \_ Anwendung**
</dt> <dd>

Der Aufrufer wird in einer-Anwendung ausgeführt.

</dd> <dt>

<span id="PRINT_EXECUTION_CONTEXT_SPOOLER_SERVICE"></span><span id="print_execution_context_spooler_service"></span>**\_ \_ \_ Spoolerdienst für Druck Ausführungs Kontext \_**
</dt> <dd>

Der Aufrufer wird im Spoolerdienst (spoolsv.exe) ausgeführt.

</dd> <dt>

<span id="PRINT_EXECUTION_CONTEXT_SPOOLER_ISOLATION_HOST"></span><span id="print_execution_context_spooler_isolation_host"></span>**\_ \_ \_ \_ Isolations Host für Spooler für Druck Ausführungs Kontext \_**
</dt> <dd>

Der Aufrufer wird auf dem druckisolations Host ausgeführt (PrintIsolationHost.exe).

</dd> <dt>

<span id="PRINT_EXECUTION_CONTEXT_FILTER_PIPELINE"></span><span id="print_execution_context_filter_pipeline"></span>**Druck \_ Ausführungs \_ Kontext- \_ Filter \_ Pipeline**
</dt> <dd>

Der Aufrufer wird in der Druckfilter Pipeline ausgeführt (printfilterpipelinesvc.exe).

</dd> <dt>

<span id="PRINT_EXECUTION_CONTEXT_WOW64"></span><span id="print_execution_context_wow64"></span>**Druck \_ Ausführungs \_ Kontext \_ WOW64**
</dt> <dd>

Der Aufrufer wird in splwow64.exe

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

[**\_Ausführungs \_ Daten drucken**](print-execution-data.md)
</dt> </dl>

 

 




