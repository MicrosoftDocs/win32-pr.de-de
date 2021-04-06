---
title: Undvtaskpluginnotifysink-Schnittstelle
description: Die Schnittstelle "" wird vom Task-Agent verwendet, um mit dem auslöseragent zu kommunizieren.
ms.assetid: ccf19693-d3cc-4cf7-af35-947be047beeb
ms.tgt_platform: multiple
keywords:
- Undvtaskpluginnotifysink-Schnittstelle Remotedesktopdienste
- Undvtaskpluginnotifysink-Schnittstelle Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0dadaf387fcf6e8381404440e0d31dd210b9f8a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742072"
---
# <a name="irdvtaskpluginnotifysink-interface"></a><span data-ttu-id="be710-105">Undvtaskpluginnotifysink-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="be710-105">IRDVTaskPluginNotifySink interface</span></span>

<span data-ttu-id="be710-106">Die **Schnittstelle** "" wird vom Task-Agent verwendet, um mit dem auslöseragent zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="be710-106">The **IRDVTaskPluginNotifySink** interface is used by the task agent to communicate with the trigger agent.</span></span> <span data-ttu-id="be710-107">Ein Zeiger auf diese Schnittstelle wird in der Methode " [**iridvtaskplugin:: Initialize**](irdvtaskplugin-initialize.md) " an den Task-Agent übermittelt.</span><span class="sxs-lookup"><span data-stu-id="be710-107">A pointer to this interface is passed to the task agent in the [**IRDVTaskPlugin::Initialize**](irdvtaskplugin-initialize.md) method.</span></span>

## <a name="members"></a><span data-ttu-id="be710-108">Member</span><span class="sxs-lookup"><span data-stu-id="be710-108">Members</span></span>

<span data-ttu-id="be710-109">Die " **iridvtaskpluginnotifysink** "-Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="be710-109">The **IRDVTaskPluginNotifySink** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="be710-110">" **Iridvtaskpluginnotifysink** " verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="be710-110">**IRDVTaskPluginNotifySink** also has these types of members:</span></span>

-   [<span data-ttu-id="be710-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="be710-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="be710-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="be710-112">Methods</span></span>

<span data-ttu-id="be710-113">Die " **iridvtaskpluginnotifysink** "-Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="be710-113">The **IRDVTaskPluginNotifySink** interface has these methods.</span></span>



| <span data-ttu-id="be710-114">Methode</span><span class="sxs-lookup"><span data-stu-id="be710-114">Method</span></span>                                                                  | <span data-ttu-id="be710-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="be710-115">Description</span></span>                                                                       |
|:------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| [<span data-ttu-id="be710-116">**DeleteSchedule**</span><span class="sxs-lookup"><span data-stu-id="be710-116">**DeleteSchedule**</span></span>](irdvtaskpluginnotifysink-deleteschedule.md)       | <span data-ttu-id="be710-117">Wird vom Task-Agent aufgerufen, um einen geplanten Task zu löschen.</span><span class="sxs-lookup"><span data-stu-id="be710-117">Called by the task agent to delete a scheduled task.</span></span><br/>                   |
| [<span data-ttu-id="be710-118">**Ontaskstatechange**</span><span class="sxs-lookup"><span data-stu-id="be710-118">**OnTaskStateChange**</span></span>](irdvtaskpluginnotifysink-ontaskstatechange.md) | <span data-ttu-id="be710-119">Wird verwendet, um den Agent zu benachrichtigen, dass sich der Zustand einer Aufgabe geändert hat.</span><span class="sxs-lookup"><span data-stu-id="be710-119">Used to notify the trigger agent that the state of a task has changed.</span></span><br/> |
| [<span data-ttu-id="be710-120">**Onterminiert**</span><span class="sxs-lookup"><span data-stu-id="be710-120">**OnTerminated**</span></span>](irdvtaskpluginnotifysink-onterminated.md)           | <span data-ttu-id="be710-121">Wird vom Task-Agent aufgerufen, um anzufordern, dass der Task-Agent heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="be710-121">Called by the task agent to request that the task agent be shut down.</span></span><br/>  |
| [<span data-ttu-id="be710-122">**ScheduleTask**</span><span class="sxs-lookup"><span data-stu-id="be710-122">**ScheduleTask**</span></span>](irdvtaskpluginnotifysink-scheduletask.md)           | <span data-ttu-id="be710-123">Wird vom Task-Agent zum Planen einer Aufgabe aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="be710-123">Called by the task agent to schedule a task.</span></span><br/>                           |



 

## <a name="remarks"></a><span data-ttu-id="be710-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="be710-124">Remarks</span></span>

<span data-ttu-id="be710-125">Diese Schnittstelle wird zwar von den in den folgenden Anforderungen identifizierten Betriebssystemen unterstützt, Sie wird jedoch nur verwendet, wenn der virtuelle Computer unter Windows Server 2012 gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="be710-125">Although this interface is supported on the operating systems identified in the Requirements below, it will only be used if the virtual machine is hosted on Windows Server 2012.</span></span>

## <a name="requirements"></a><span data-ttu-id="be710-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="be710-126">Requirements</span></span>



| <span data-ttu-id="be710-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="be710-127">Requirement</span></span> | <span data-ttu-id="be710-128">Wert</span><span class="sxs-lookup"><span data-stu-id="be710-128">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="be710-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="be710-129">Minimum supported client</span></span><br/> | <span data-ttu-id="be710-130">Windows 7 Enterprise</span><span class="sxs-lookup"><span data-stu-id="be710-130">Windows 7 Enterprise</span></span><br/>   |
| <span data-ttu-id="be710-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="be710-131">Minimum supported server</span></span><br/> | <span data-ttu-id="be710-132">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="be710-132">Windows Server 2008 R2</span></span><br/> |



 

