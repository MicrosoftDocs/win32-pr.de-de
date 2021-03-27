---
description: Wird vom Browser implementiert. Macht Methoden verfügbar, die verwalten, welcher Monitor die Windows-Taskleiste in einem System mit mehreren Monitoren enthält.
title: Imultimonitordockingsite-Schnittstelle
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
ms.openlocfilehash: 3aa1ccb1c25fd2896ce9e18ba52ea3f46b1882af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104995198"
---
# <a name="imultimonitordockingsite-interface"></a><span data-ttu-id="691a8-104">Imultimonitordockingsite-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="691a8-104">IMultiMonitorDockingSite interface</span></span>

<span data-ttu-id="691a8-105">Wird vom Browser implementiert.</span><span class="sxs-lookup"><span data-stu-id="691a8-105">Implemented by the browser.</span></span> <span data-ttu-id="691a8-106">Macht Methoden verfügbar, die verwalten, welcher Monitor die Windows-Taskleiste in einem System mit mehreren Monitoren enthält.</span><span class="sxs-lookup"><span data-stu-id="691a8-106">Exposes methods that manage which monitor contains the Windows taskbar on a multiple monitor system.</span></span>

## <a name="members"></a><span data-ttu-id="691a8-107">Member</span><span class="sxs-lookup"><span data-stu-id="691a8-107">Members</span></span>

<span data-ttu-id="691a8-108">Die **imultimonitordockingsite** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="691a8-108">The **IMultiMonitorDockingSite** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="691a8-109">**Imultimonitordockingsite** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="691a8-109">**IMultiMonitorDockingSite** also has these types of members:</span></span>

-   [<span data-ttu-id="691a8-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="691a8-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="691a8-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="691a8-111">Methods</span></span>

<span data-ttu-id="691a8-112">Die **imultimonitordockingsite** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="691a8-112">The **IMultiMonitorDockingSite** interface has these methods.</span></span>



| <span data-ttu-id="691a8-113">Methode</span><span class="sxs-lookup"><span data-stu-id="691a8-113">Method</span></span>                                                            | <span data-ttu-id="691a8-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="691a8-114">Description</span></span>                                                                                |
|:------------------------------------------------------------------|:-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="691a8-115">**Getmonitor**</span><span class="sxs-lookup"><span data-stu-id="691a8-115">**GetMonitor**</span></span>](imultimonitordockingsite-getmonitor.md)         | <span data-ttu-id="691a8-116">Ruft den aktuellen Standard Monitor ab.</span><span class="sxs-lookup"><span data-stu-id="691a8-116">Gets the current default monitor.</span></span><br/>                                               |
| [<span data-ttu-id="691a8-117">**RequestMonitor**</span><span class="sxs-lookup"><span data-stu-id="691a8-117">**RequestMonitor**</span></span>](imultimonitordockingsite-requestmonitor.md) | <span data-ttu-id="691a8-118">Überprüft, ob der Monitor aktiv und verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="691a8-118">Verifies that the monitor is active and available.</span></span><br/>                              |
| [<span data-ttu-id="691a8-119">**Setmonitor**</span><span class="sxs-lookup"><span data-stu-id="691a8-119">**SetMonitor**</span></span>](imultimonitordockingsite-setmonitor.md)         | <span data-ttu-id="691a8-120">Ändert, welcher Monitor für angedockte Symbolleisten in einem System mit mehreren Monitoren verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="691a8-120">Changes which monitor is used for docked toolbars on a multiple monitor system.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="691a8-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="691a8-121">Remarks</span></span>

<span data-ttu-id="691a8-122">Sie implementieren die **imultimonitordockingsite** -Schnittstelle in der Regel nicht.</span><span class="sxs-lookup"><span data-stu-id="691a8-122">You do not typically implement the **IMultiMonitorDockingSite** interface.</span></span> <span data-ttu-id="691a8-123">Der ShellBrowser implementiert diese Schnittstelle, um mehrere Monitore zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="691a8-123">The Shell browser implements this interface to support multiple monitors.</span></span>

## <a name="requirements"></a><span data-ttu-id="691a8-124">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="691a8-124">Requirements</span></span>



| <span data-ttu-id="691a8-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="691a8-125">Requirement</span></span> | <span data-ttu-id="691a8-126">Wert</span><span class="sxs-lookup"><span data-stu-id="691a8-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="691a8-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="691a8-127">Minimum supported client</span></span><br/> | <span data-ttu-id="691a8-128">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="691a8-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="691a8-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="691a8-129">Minimum supported server</span></span><br/> | <span data-ttu-id="691a8-130">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="691a8-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                   |



 

 
