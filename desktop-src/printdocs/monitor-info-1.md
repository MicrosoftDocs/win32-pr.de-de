---
description: Die Struktur von Monitor \_ Info \_ 1 identifiziert einen installierten Monitor.
ms.assetid: 7a4660bd-5df8-49dd-92f6-9574f451f10d
title: MONITOR_INFO_1 Struktur (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MONITOR_INFO_1
- _MONITOR_INFO_1A
- _MONITOR_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: b6af1e1b9111ac6221273f2faf68fc6ed70e07a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353448"
---
# <a name="monitor_info_1-structure"></a><span data-ttu-id="56cd0-103">Überwachen der \_ Info \_ 1-Struktur</span><span class="sxs-lookup"><span data-stu-id="56cd0-103">MONITOR\_INFO\_1 structure</span></span>

<span data-ttu-id="56cd0-104">Die Struktur von **Monitor \_ Info \_ 1** identifiziert einen installierten Monitor.</span><span class="sxs-lookup"><span data-stu-id="56cd0-104">The **MONITOR\_INFO\_1** structure identifies an installed monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="56cd0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="56cd0-105">Syntax</span></span>


```C++
typedef struct _MONITOR_INFO_1 {
  LPTSTR pName;
} MONITOR_INFO_1, *PMONITOR_INFO_1;
```



## <a name="members"></a><span data-ttu-id="56cd0-106">Member</span><span class="sxs-lookup"><span data-stu-id="56cd0-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="56cd0-107">**pName**</span><span class="sxs-lookup"><span data-stu-id="56cd0-107">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="56cd0-108">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die einen installierten Monitor identifiziert.</span><span class="sxs-lookup"><span data-stu-id="56cd0-108">A pointer to a null-terminated string that identifies an installed monitor.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="56cd0-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="56cd0-109">Requirements</span></span>



| <span data-ttu-id="56cd0-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="56cd0-110">Requirement</span></span> | <span data-ttu-id="56cd0-111">Wert</span><span class="sxs-lookup"><span data-stu-id="56cd0-111">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56cd0-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="56cd0-112">Minimum supported client</span></span><br/> | <span data-ttu-id="56cd0-113">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="56cd0-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="56cd0-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="56cd0-114">Minimum supported server</span></span><br/> | <span data-ttu-id="56cd0-115">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="56cd0-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="56cd0-116">Header</span><span class="sxs-lookup"><span data-stu-id="56cd0-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="56cd0-117"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="56cd0-117"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="56cd0-118">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="56cd0-118">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="56cd0-119">**\_ Überwachen von \_ Informationen \_ 1W** (Unicode) und **\_ Überwachen von \_ Informationen \_ 1a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="56cd0-119">**\_MONITOR\_INFO\_1W** (Unicode) and **\_MONITOR\_INFO\_1A** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="56cd0-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="56cd0-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56cd0-121">Drucken</span><span class="sxs-lookup"><span data-stu-id="56cd0-121">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="56cd0-122">Druck Spooler-API-Strukturen</span><span class="sxs-lookup"><span data-stu-id="56cd0-122">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="56cd0-123">**Enumüberwachungen**</span><span class="sxs-lookup"><span data-stu-id="56cd0-123">**EnumMonitors**</span></span>](enummonitors.md)
</dt> <dt>

[<span data-ttu-id="56cd0-124">**Überwachen von \_ Informationen \_ 2**</span><span class="sxs-lookup"><span data-stu-id="56cd0-124">**MONITOR\_INFO\_2**</span></span>](monitor-info-2.md)
</dt> </dl>

 

 




