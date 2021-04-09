---
description: Die imonitoreventer-Schnittstelle stellt Methoden zum Übermitteln von Ereignissen und zum Zuweisen und Freigeben von Monitor Ressourcen bereit.
ms.assetid: d59a8b42-cce3-410b-a62e-97d66d058d90
title: Imonitoreventer-Schnittstelle (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitorEventer
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: 7d4ca58b5a0787638eee54b7733b4e1a8fbf7ffe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862411"
---
# <a name="imonitoreventer-interface"></a><span data-ttu-id="5d289-103">Imonitoreventer-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="5d289-103">IMonitorEventer interface</span></span>

<span data-ttu-id="5d289-104">Die **imonitoreventer** -Schnittstelle stellt Methoden zum Übermitteln von Ereignissen und zum Zuweisen und Freigeben von Monitor Ressourcen bereit.</span><span class="sxs-lookup"><span data-stu-id="5d289-104">The **IMonitorEventer** interface provides methods for submitting events and allocating and freeing monitor resources.</span></span>

## <a name="members"></a><span data-ttu-id="5d289-105">Member</span><span class="sxs-lookup"><span data-stu-id="5d289-105">Members</span></span>

<span data-ttu-id="5d289-106">Die **imonitoreventer** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="5d289-106">The **IMonitorEventer** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="5d289-107">**Imonitoreventer** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="5d289-107">**IMonitorEventer** also has these types of members:</span></span>

-   [<span data-ttu-id="5d289-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="5d289-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5d289-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="5d289-109">Methods</span></span>

<span data-ttu-id="5d289-110">Die **imonitoreventer** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="5d289-110">The **IMonitorEventer** interface has these methods.</span></span>



| <span data-ttu-id="5d289-111">Methode</span><span class="sxs-lookup"><span data-stu-id="5d289-111">Method</span></span>                                                 | <span data-ttu-id="5d289-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5d289-112">Description</span></span>                                        |
|:-------------------------------------------------------|:---------------------------------------------------|
| [<span data-ttu-id="5d289-113">**Freieventdata**</span><span class="sxs-lookup"><span data-stu-id="5d289-113">**FreeEventData**</span></span>](imonitoreventer-freeeventdata.md) | <span data-ttu-id="5d289-114">Gibt den zugeordneten Speicherplatz für Überwachungsdaten frei.</span><span class="sxs-lookup"><span data-stu-id="5d289-114">Frees space allocated for monitor data.</span></span><br/> |
| [<span data-ttu-id="5d289-115">**GetEventData**</span><span class="sxs-lookup"><span data-stu-id="5d289-115">**GetEventData**</span></span>](imonitoreventer-geteventdata.md)   | <span data-ttu-id="5d289-116">Weist Speicherplatz für Überwachungsdaten zu.</span><span class="sxs-lookup"><span data-stu-id="5d289-116">Allocates space for monitor data.</span></span><br/>       |
| [<span data-ttu-id="5d289-117">**Sendnmevent**</span><span class="sxs-lookup"><span data-stu-id="5d289-117">**SendNMEvent**</span></span>](imonitoreventer-sendnmevent.md)     | <span data-ttu-id="5d289-118">Übermittelt Ereignisse an WMI.</span><span class="sxs-lookup"><span data-stu-id="5d289-118">Submits events to WMI.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="5d289-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5d289-119">Requirements</span></span>



| <span data-ttu-id="5d289-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5d289-120">Requirement</span></span> | <span data-ttu-id="5d289-121">Wert</span><span class="sxs-lookup"><span data-stu-id="5d289-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5d289-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5d289-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5d289-123">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5d289-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="5d289-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5d289-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5d289-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5d289-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="5d289-126">Header</span><span class="sxs-lookup"><span data-stu-id="5d289-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d289-127"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d289-127"><dt>Netmon.h</dt></span></span> </dl> |



 

