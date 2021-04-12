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
# <a name="print_execution_context-enumeration"></a><span data-ttu-id="c8b78-103">\_Enumeration des druckausführungs \_ Kontexts</span><span class="sxs-lookup"><span data-stu-id="c8b78-103">PRINT\_EXECUTION\_CONTEXT enumeration</span></span>

<span data-ttu-id="c8b78-104">Stellt den Ausführungs Kontext dar, wenn [**getprintexecutiondata**](getprintexecutiondata.md) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="c8b78-104">Represents the execution context when [**GetPrintExecutionData**](getprintexecutiondata.md) is called.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8b78-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c8b78-105">Syntax</span></span>


```C++
typedef enum  { 
  PRINT_EXECUTION_CONTEXT_APPLICATION             = 0,
  PRINT_EXECUTION_CONTEXT_SPOOLER_SERVICE         = 1,
  PRINT_EXECUTION_CONTEXT_SPOOLER_ISOLATION_HOST  = 2,
  PRINT_EXECUTION_CONTEXT_FILTER_PIPELINE         = 3,
  PRINT_EXECUTION_CONTEXT_WOW64                   = 4
} PRINT_EXECUTION_CONTEXT;
```



## <a name="constants"></a><span data-ttu-id="c8b78-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="c8b78-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="c8b78-107"><span id="PRINT_EXECUTION_CONTEXT_APPLICATION"></span><span id="print_execution_context_application"></span>**Druck \_ Ausführungs \_ Kontext- \_ Anwendung**</span><span class="sxs-lookup"><span data-stu-id="c8b78-107"><span id="PRINT_EXECUTION_CONTEXT_APPLICATION"></span><span id="print_execution_context_application"></span>**PRINT\_EXECUTION\_CONTEXT\_APPLICATION**</span></span>
</dt> <dd>

<span data-ttu-id="c8b78-108">Der Aufrufer wird in einer-Anwendung ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c8b78-108">The caller is running in an application.</span></span>

</dd> <dt>

<span data-ttu-id="c8b78-109"><span id="PRINT_EXECUTION_CONTEXT_SPOOLER_SERVICE"></span><span id="print_execution_context_spooler_service"></span>**\_ \_ \_ Spoolerdienst für Druck Ausführungs Kontext \_**</span><span class="sxs-lookup"><span data-stu-id="c8b78-109"><span id="PRINT_EXECUTION_CONTEXT_SPOOLER_SERVICE"></span><span id="print_execution_context_spooler_service"></span>**PRINT\_EXECUTION\_CONTEXT\_SPOOLER\_SERVICE**</span></span>
</dt> <dd>

<span data-ttu-id="c8b78-110">Der Aufrufer wird im Spoolerdienst (spoolsv.exe) ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c8b78-110">The caller is running in the spooler service (spoolsv.exe).</span></span>

</dd> <dt>

<span data-ttu-id="c8b78-111"><span id="PRINT_EXECUTION_CONTEXT_SPOOLER_ISOLATION_HOST"></span><span id="print_execution_context_spooler_isolation_host"></span>**\_ \_ \_ \_ Isolations Host für Spooler für Druck Ausführungs Kontext \_**</span><span class="sxs-lookup"><span data-stu-id="c8b78-111"><span id="PRINT_EXECUTION_CONTEXT_SPOOLER_ISOLATION_HOST"></span><span id="print_execution_context_spooler_isolation_host"></span>**PRINT\_EXECUTION\_CONTEXT\_SPOOLER\_ISOLATION\_HOST**</span></span>
</dt> <dd>

<span data-ttu-id="c8b78-112">Der Aufrufer wird auf dem druckisolations Host ausgeführt (PrintIsolationHost.exe).</span><span class="sxs-lookup"><span data-stu-id="c8b78-112">The caller is running in the print isolation host (PrintIsolationHost.exe)</span></span>

</dd> <dt>

<span data-ttu-id="c8b78-113"><span id="PRINT_EXECUTION_CONTEXT_FILTER_PIPELINE"></span><span id="print_execution_context_filter_pipeline"></span>**Druck \_ Ausführungs \_ Kontext- \_ Filter \_ Pipeline**</span><span class="sxs-lookup"><span data-stu-id="c8b78-113"><span id="PRINT_EXECUTION_CONTEXT_FILTER_PIPELINE"></span><span id="print_execution_context_filter_pipeline"></span>**PRINT\_EXECUTION\_CONTEXT\_FILTER\_PIPELINE**</span></span>
</dt> <dd>

<span data-ttu-id="c8b78-114">Der Aufrufer wird in der Druckfilter Pipeline ausgeführt (printfilterpipelinesvc.exe).</span><span class="sxs-lookup"><span data-stu-id="c8b78-114">The caller is running in the print filter pipeline (printfilterpipelinesvc.exe)</span></span>

</dd> <dt>

<span data-ttu-id="c8b78-115"><span id="PRINT_EXECUTION_CONTEXT_WOW64"></span><span id="print_execution_context_wow64"></span>**Druck \_ Ausführungs \_ Kontext \_ WOW64**</span><span class="sxs-lookup"><span data-stu-id="c8b78-115"><span id="PRINT_EXECUTION_CONTEXT_WOW64"></span><span id="print_execution_context_wow64"></span>**PRINT\_EXECUTION\_CONTEXT\_WOW64**</span></span>
</dt> <dd>

<span data-ttu-id="c8b78-116">Der Aufrufer wird in splwow64.exe</span><span class="sxs-lookup"><span data-stu-id="c8b78-116">The caller is running in splwow64.exe</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c8b78-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c8b78-117">Requirements</span></span>



| <span data-ttu-id="c8b78-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c8b78-118">Requirement</span></span> | <span data-ttu-id="c8b78-119">Wert</span><span class="sxs-lookup"><span data-stu-id="c8b78-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8b78-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c8b78-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c8b78-121">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c8b78-121">Windows 7 \[desktop apps only\]</span></span><br/>                                                                |
| <span data-ttu-id="c8b78-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c8b78-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c8b78-123">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c8b78-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="c8b78-124">Header</span><span class="sxs-lookup"><span data-stu-id="c8b78-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8b78-125"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c8b78-125"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8b78-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c8b78-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8b78-127">**Getprintexecutiondata**</span><span class="sxs-lookup"><span data-stu-id="c8b78-127">**GetPrintExecutionData**</span></span>](getprintexecutiondata.md)
</dt> <dt>

[<span data-ttu-id="c8b78-128">**\_Ausführungs \_ Daten drucken**</span><span class="sxs-lookup"><span data-stu-id="c8b78-128">**PRINT\_EXECUTION\_DATA**</span></span>](print-execution-data.md)
</dt> </dl>

 

 




