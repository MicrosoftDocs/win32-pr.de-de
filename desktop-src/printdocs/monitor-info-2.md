---
description: Die Struktur von Monitor \_ Info \_ 2 identifiziert einen Monitor.
ms.assetid: 4dd1ca15-6983-403e-8159-1a6d35a88162
title: MONITOR_INFO_2 Struktur (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MONITOR_INFO_2
- _MONITOR_INFO_2A
- _MONITOR_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 9d3ad70a0728ca6e73c4dbefb248df58e858a996
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759655"
---
# <a name="monitor_info_2-structure"></a><span data-ttu-id="a726b-103">Überwachen der \_ Info \_ 2-Struktur</span><span class="sxs-lookup"><span data-stu-id="a726b-103">MONITOR\_INFO\_2 structure</span></span>

<span data-ttu-id="a726b-104">Die Struktur von **Monitor \_ Info \_ 2** identifiziert einen Monitor.</span><span class="sxs-lookup"><span data-stu-id="a726b-104">The **MONITOR\_INFO\_2** structure identifies a monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="a726b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a726b-105">Syntax</span></span>


```C++
typedef struct _MONITOR_INFO_2 {
  LPTSTR pName;
  LPTSTR pEnvironment;
  LPTSTR pDLLName;
} MONITOR_INFO_2, *PMONITOR_INFO_2;
```



## <a name="members"></a><span data-ttu-id="a726b-106">Member</span><span class="sxs-lookup"><span data-stu-id="a726b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="a726b-107">**pName**</span><span class="sxs-lookup"><span data-stu-id="a726b-107">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="a726b-108">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des Monitors ist.</span><span class="sxs-lookup"><span data-stu-id="a726b-108">A pointer to a null-terminated string that is the name of the monitor.</span></span>

</dd> <dt>

<span data-ttu-id="a726b-109">**nach-oben**</span><span class="sxs-lookup"><span data-stu-id="a726b-109">**pEnvironment**</span></span>
</dt> <dd>

<span data-ttu-id="a726b-110">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die die Umgebung angibt, für die der Monitor geschrieben wurde (z. b. Windows NT x86, Windows ia64, Windows x64).</span><span class="sxs-lookup"><span data-stu-id="a726b-110">A pointer to a null-terminated string that specifies the environment for which the monitor was written (for example, Windows NT x86, Windows IA64, Windows x64).</span></span>

</dd> <dt>

<span data-ttu-id="a726b-111">**pdllname**</span><span class="sxs-lookup"><span data-stu-id="a726b-111">**pDLLName**</span></span>
</dt> <dd>

<span data-ttu-id="a726b-112">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die der Name der Monitor-dll ist.</span><span class="sxs-lookup"><span data-stu-id="a726b-112">A pointer to a null-terminated string that is the name of the monitor DLL.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a726b-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a726b-113">Requirements</span></span>



| <span data-ttu-id="a726b-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a726b-114">Requirement</span></span> | <span data-ttu-id="a726b-115">Wert</span><span class="sxs-lookup"><span data-stu-id="a726b-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a726b-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a726b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a726b-117">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a726b-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a726b-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a726b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a726b-119">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a726b-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a726b-120">Header</span><span class="sxs-lookup"><span data-stu-id="a726b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a726b-121"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a726b-121"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="a726b-122">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="a726b-122">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="a726b-123">**\_ Monitor \_ Info \_ 2W** (Unicode) und **\_ Monitor \_ Info \_ 2a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="a726b-123">**\_MONITOR\_INFO\_2W** (Unicode) and **\_MONITOR\_INFO\_2A** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="a726b-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a726b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a726b-125">Drucken</span><span class="sxs-lookup"><span data-stu-id="a726b-125">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="a726b-126">Druck Spooler-API-Strukturen</span><span class="sxs-lookup"><span data-stu-id="a726b-126">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="a726b-127">**Addmonitor**</span><span class="sxs-lookup"><span data-stu-id="a726b-127">**AddMonitor**</span></span>](addmonitor.md)
</dt> <dt>

[<span data-ttu-id="a726b-128">**Enumüberwachungen**</span><span class="sxs-lookup"><span data-stu-id="a726b-128">**EnumMonitors**</span></span>](enummonitors.md)
</dt> <dt>

[<span data-ttu-id="a726b-129">**Überwachen von \_ Informationen \_ 1**</span><span class="sxs-lookup"><span data-stu-id="a726b-129">**MONITOR\_INFO\_1**</span></span>](monitor-info-1.md)
</dt> </dl>

 

 




