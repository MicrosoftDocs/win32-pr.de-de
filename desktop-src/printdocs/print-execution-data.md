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
# <a name="print_execution_data-structure"></a><span data-ttu-id="70a68-103">\_ \_ Datenstruktur der Druck Ausführung</span><span class="sxs-lookup"><span data-stu-id="70a68-103">PRINT\_EXECUTION\_DATA structure</span></span>

<span data-ttu-id="70a68-104">Enthält den Ausführungs Kontext des Druckertreibers, der [**getprintexecutiondata**](getprintexecutiondata.md)aufruft.</span><span class="sxs-lookup"><span data-stu-id="70a68-104">Contains the execution context of the printer driver that calls [**GetPrintExecutionData**](getprintexecutiondata.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="70a68-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="70a68-105">Syntax</span></span>


```C++
typedef struct _PRINT_EXECUTION_DATA {
  PRINT_EXECUTION_CONTEXT  context;
  DWORD                    clientAppPID;
} PRINT_EXECUTION_DATA;
```



## <a name="members"></a><span data-ttu-id="70a68-106">Member</span><span class="sxs-lookup"><span data-stu-id="70a68-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="70a68-107">**context**</span><span class="sxs-lookup"><span data-stu-id="70a68-107">**context**</span></span>
</dt> <dd>

<span data-ttu-id="70a68-108">Der [**\_ \_ Kontextwert der Druck Ausführung**](print-execution-context.md) , der den aktuellen Ausführungs Kontext des Druckertreibers darstellt.</span><span class="sxs-lookup"><span data-stu-id="70a68-108">The [**PRINT\_EXECUTION\_CONTEXT**](print-execution-context.md) value that represents the current execution context of the printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="70a68-109">**clientapppid**</span><span class="sxs-lookup"><span data-stu-id="70a68-109">**clientAppPID**</span></span>
</dt> <dd>

<span data-ttu-id="70a68-110">Wenn der Wert des **Kontexts** " **Druck \_ Ausführungs \_ Kontext \_ WOW64**" ist, identifiziert **clientapppid** die Client Anwendung, in deren Auftrag der splwow64.exe Prozess den Druckertreiber geladen hat.</span><span class="sxs-lookup"><span data-stu-id="70a68-110">If the value of **context** is **PRINT\_EXECUTION\_CONTEXT\_WOW64**, **clientAppPID** identifies the client application on whose behalf the splwow64.exe process loaded the printer driver.</span></span> <span data-ttu-id="70a68-111">Wenn der Wert des **Kontexts** nicht der **Druck \_ Ausführungs \_ Kontext \_ WOW64** ist, ist **clientapppid** gleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="70a68-111">If the value of **context** is not **PRINT\_EXECUTION\_CONTEXT\_WOW64**, **clientAppPID** is zero.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="70a68-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="70a68-112">Requirements</span></span>



| <span data-ttu-id="70a68-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="70a68-113">Requirement</span></span> | <span data-ttu-id="70a68-114">Wert</span><span class="sxs-lookup"><span data-stu-id="70a68-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70a68-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="70a68-115">Minimum supported client</span></span><br/> | <span data-ttu-id="70a68-116">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="70a68-116">Windows 7 \[desktop apps only\]</span></span><br/>                                                                |
| <span data-ttu-id="70a68-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="70a68-117">Minimum supported server</span></span><br/> | <span data-ttu-id="70a68-118">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="70a68-118">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="70a68-119">Header</span><span class="sxs-lookup"><span data-stu-id="70a68-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="70a68-120"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="70a68-120"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70a68-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="70a68-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70a68-122">**Getprintexecutiondata**</span><span class="sxs-lookup"><span data-stu-id="70a68-122">**GetPrintExecutionData**</span></span>](getprintexecutiondata.md)
</dt> <dt>

[<span data-ttu-id="70a68-123">**Druck \_ Ausführungs \_ Kontext**</span><span class="sxs-lookup"><span data-stu-id="70a68-123">**PRINT\_EXECUTION\_CONTEXT**</span></span>](print-execution-context.md)
</dt> </dl>

 

 




