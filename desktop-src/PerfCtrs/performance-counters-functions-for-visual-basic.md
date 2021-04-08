---
description: Sie können die folgenden Funktionen verwenden, um in Visual Basic mit Leistungsdaten zu arbeiten.
ms.assetid: c78eeb43-c713-42cc-a38f-f8aaa04f8dae
title: Leistungsindikator Funktionen für Visual Basic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c777aa887b9dc42a061de95fb6f33dbf9d3dff7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865103"
---
# <a name="performance-counters-functions-for-visual-basic"></a><span data-ttu-id="56c87-103">Leistungsindikator Funktionen für Visual Basic</span><span class="sxs-lookup"><span data-stu-id="56c87-103">Performance Counters Functions for Visual Basic</span></span>

> [!IMPORTANT]
> <span data-ttu-id="56c87-104">Die Funktionen, die in diesem Thema beschrieben werden, können in Zukunft geändert oder nicht mehr verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="56c87-104">The functions that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="56c87-105">Stattdessen empfiehlt Microsoft die Verwendung der Funktionen, die unter [Funktionen von Leistungsindikatoren](performance-counters-functions.md)beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="56c87-105">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="56c87-106">Sie können die folgenden Funktionen verwenden, um in Visual Basic mit Leistungsdaten zu arbeiten.</span><span class="sxs-lookup"><span data-stu-id="56c87-106">You can use the following functions to work with performance data in Visual Basic.</span></span>

- [<span data-ttu-id="56c87-107">**Pdhclosequery**</span><span class="sxs-lookup"><span data-stu-id="56c87-107">**PdhCloseQuery**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhclosequery)
- [<span data-ttu-id="56c87-108">**Pdhcollectquerydata**</span><span class="sxs-lookup"><span data-stu-id="56c87-108">**PdhCollectQueryData**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata)
- [<span data-ttu-id="56c87-109">**PdhRemoveCounter**</span><span class="sxs-lookup"><span data-stu-id="56c87-109">**PdhRemoveCounter**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhremovecounter)
- [<span data-ttu-id="56c87-110">**Pdhvbaddcounter**</span><span class="sxs-lookup"><span data-stu-id="56c87-110">**PdhVbAddCounter**</span></span>](pdhvbaddcounter.md)
- [<span data-ttu-id="56c87-111">**Pdhvbkreatecounterpathlist**</span><span class="sxs-lookup"><span data-stu-id="56c87-111">**PdhVbCreateCounterPathList**</span></span>](pdhvbcreatecounterpathlist.md)
- [<span data-ttu-id="56c87-112">**Pdhvbgetcounterpathelements**</span><span class="sxs-lookup"><span data-stu-id="56c87-112">**PdhVbGetCounterPathElements**</span></span>](pdhvbgetcounterpathelements.md)
- [<span data-ttu-id="56c87-113">**Pdhvbgetcounterpathfromlist**</span><span class="sxs-lookup"><span data-stu-id="56c87-113">**PdhVbGetCounterPathFromList**</span></span>](pdhvbgetcounterpathfromlist.md)
- [<span data-ttu-id="56c87-114">**Pdhvbgetdoublecountervalue**</span><span class="sxs-lookup"><span data-stu-id="56c87-114">**PdhVbGetDoubleCounterValue**</span></span>](pdhvbgetdoublecountervalue.md)
- [<span data-ttu-id="56c87-115">**Pdhvbgetlogfilesize**</span><span class="sxs-lookup"><span data-stu-id="56c87-115">**PdhVbGetLogFileSize**</span></span>](pdhvbgetlogfilesize.md)
- [<span data-ttu-id="56c87-116">**Pdhvbgetonecounterpath**</span><span class="sxs-lookup"><span data-stu-id="56c87-116">**PdhVbGetOneCounterPath**</span></span>](pdhvbgetonecounterpath.md)
- [<span data-ttu-id="56c87-117">**Pdhvbisgoodstatus**</span><span class="sxs-lookup"><span data-stu-id="56c87-117">**PdhVbIsGoodStatus**</span></span>](pdhvbisgoodstatus.md)
- [<span data-ttu-id="56c87-118">**Pdhvbopenlog**</span><span class="sxs-lookup"><span data-stu-id="56c87-118">**PdhVbOpenLog**</span></span>](pdhvbopenlog.md)
- [<span data-ttu-id="56c87-119">**Pdhvbopenquery**</span><span class="sxs-lookup"><span data-stu-id="56c87-119">**PdhVbOpenQuery**</span></span>](pdhvbopenquery.md)
- [<span data-ttu-id="56c87-120">**Pdhvbupdatelog**</span><span class="sxs-lookup"><span data-stu-id="56c87-120">**PdhVbUpdateLog**</span></span>](pdhvbupdatelog.md)

> [!NOTE]
> <span data-ttu-id="56c87-121">Die `PdhVb***` -Funktionen funktionieren in einer Prozess internen Sitzung und sind nicht Thread sicher.</span><span class="sxs-lookup"><span data-stu-id="56c87-121">The `PdhVb***` functions work on a per-process session and are not thread-safe.</span></span> <span data-ttu-id="56c87-122">Diese Funktionen sollten nur von einfachen Single Thread-Anwendungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="56c87-122">These functions should only be used from simple single-threaded applications.</span></span>
