---
description: Wird vom Browser implementiert. Macht Methoden verfügbar, die verwalten, welcher Monitor die Windows-Taskleiste auf einem System mit mehreren Monitoren enthält.
title: IMultiMonitorDockingSite-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMultiMonitorDockingSite
api_type:
- COM
api_location: ''
ms.assetid: af9a7a9e-bd7c-4b17-9cb6-008df5c820d8
ms.openlocfilehash: 5ea3461d00c16f7384d7396e2f03946d517c460f
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841891"
---
# <a name="imultimonitordockingsite-interface"></a><span data-ttu-id="6a294-104">IMultiMonitorDockingSite-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="6a294-104">IMultiMonitorDockingSite interface</span></span>

<span data-ttu-id="6a294-105">Wird vom Browser implementiert.</span><span class="sxs-lookup"><span data-stu-id="6a294-105">Implemented by the browser.</span></span> <span data-ttu-id="6a294-106">Macht Methoden verfügbar, die verwalten, welcher Monitor die Windows-Taskleiste auf einem System mit mehreren Monitoren enthält.</span><span class="sxs-lookup"><span data-stu-id="6a294-106">Exposes methods that manage which monitor contains the Windows taskbar on a multiple monitor system.</span></span>

## <a name="members"></a><span data-ttu-id="6a294-107">Member</span><span class="sxs-lookup"><span data-stu-id="6a294-107">Members</span></span>

<span data-ttu-id="6a294-108">Die **IMultiMonitorDockingSite-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown)</span><span class="sxs-lookup"><span data-stu-id="6a294-108">The **IMultiMonitorDockingSite** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="6a294-109">**IMultiMonitorDockingSite** verfügt auch über diese Membertypen:</span><span class="sxs-lookup"><span data-stu-id="6a294-109">**IMultiMonitorDockingSite** also has these types of members:</span></span>

-   [<span data-ttu-id="6a294-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="6a294-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6a294-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="6a294-111">Methods</span></span>

<span data-ttu-id="6a294-112">Die **IMultiMonitorDockingSite-Schnittstelle** verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="6a294-112">The **IMultiMonitorDockingSite** interface has these methods.</span></span>



| <span data-ttu-id="6a294-113">Methode</span><span class="sxs-lookup"><span data-stu-id="6a294-113">Method</span></span>                                                            | <span data-ttu-id="6a294-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6a294-114">Description</span></span>                                                                                |
|:------------------------------------------------------------------|:-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6a294-115">**GetMonitor**</span><span class="sxs-lookup"><span data-stu-id="6a294-115">**GetMonitor**</span></span>](imultimonitordockingsite-getmonitor.md)         | <span data-ttu-id="6a294-116">Ruft den aktuellen Standardmonitor ab.</span><span class="sxs-lookup"><span data-stu-id="6a294-116">Gets the current default monitor.</span></span><br/>                                               |
| [<span data-ttu-id="6a294-117">**RequestMonitor**</span><span class="sxs-lookup"><span data-stu-id="6a294-117">**RequestMonitor**</span></span>](imultimonitordockingsite-requestmonitor.md) | <span data-ttu-id="6a294-118">Überprüft, ob der Monitor aktiv und verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="6a294-118">Verifies that the monitor is active and available.</span></span><br/>                              |
| [<span data-ttu-id="6a294-119">**SetMonitor**</span><span class="sxs-lookup"><span data-stu-id="6a294-119">**SetMonitor**</span></span>](imultimonitordockingsite-setmonitor.md)         | <span data-ttu-id="6a294-120">Änderungen, die für angedockte Symbolleisten auf einem System mit mehreren Monitoren verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6a294-120">Changes which monitor is used for docked toolbars on a multiple monitor system.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6a294-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6a294-121">Remarks</span></span>

<span data-ttu-id="6a294-122">In der Regel implementieren Sie die **IMultiMonitorDockingSite-Schnittstelle** nicht.</span><span class="sxs-lookup"><span data-stu-id="6a294-122">You do not typically implement the **IMultiMonitorDockingSite** interface.</span></span> <span data-ttu-id="6a294-123">Der Shell-Browser implementiert diese Schnittstelle, um mehrere Monitore zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="6a294-123">The Shell browser implements this interface to support multiple monitors.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a294-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6a294-124">Requirements</span></span>



| <span data-ttu-id="6a294-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6a294-125">Requirement</span></span> | <span data-ttu-id="6a294-126">Wert</span><span class="sxs-lookup"><span data-stu-id="6a294-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="6a294-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6a294-127">Minimum supported client</span></span><br/> | <span data-ttu-id="6a294-128">Nur Windows 2000 Professional- und Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6a294-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="6a294-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6a294-129">Minimum supported server</span></span><br/> | <span data-ttu-id="6a294-130">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6a294-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                   |



 

 
