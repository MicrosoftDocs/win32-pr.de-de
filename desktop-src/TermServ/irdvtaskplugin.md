---
title: Undvtaskplugin-Schnittstelle
description: Die Schnittstelle "iridvtaskplugin" wird von einem Task-Agent für virtuelle Computer Updates implementiert, damit der Task-Agent Systemupdates für einen virtuellen Computer verwalten kann.
ms.assetid: e06eb707-be78-4d1f-96d3-21526b167e61
ms.tgt_platform: multiple
keywords:
- Undvtaskplugin-Schnittstelle Remotedesktopdienste
- Undvtaskplugin-Schnittstelle Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- IRDVTaskPlugin
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 59e90e899e8084f7fbc6b0b6f11067061eaa807b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957153"
---
# <a name="irdvtaskplugin-interface"></a><span data-ttu-id="b2ada-105">Undvtaskplugin-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="b2ada-105">IRDVTaskPlugin interface</span></span>

<span data-ttu-id="b2ada-106">Die Schnittstelle " **iridvtaskplugin** " wird von einem *Task-Agent* für virtuelle Computer Updates implementiert, damit der Task-Agent Systemupdates für einen virtuellen Computer verwalten kann.</span><span class="sxs-lookup"><span data-stu-id="b2ada-106">The **IRDVTaskPlugin** interface is implemented by a virtual machine update *task agent* to allow the task agent to manage system updates for a virtual machine.</span></span> <span data-ttu-id="b2ada-107">Diese Schnittstelle wird vom- *Agent* verwendet, der vom Host System implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="b2ada-107">This interface is used by the *trigger agent*, which is implemented by the host system.</span></span>

## <a name="members"></a><span data-ttu-id="b2ada-108">Member</span><span class="sxs-lookup"><span data-stu-id="b2ada-108">Members</span></span>

<span data-ttu-id="b2ada-109">Die Schnittstelle " **iridvtaskplugin** " erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="b2ada-109">The **IRDVTaskPlugin** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="b2ada-110">" **Iridvtaskplugin** " verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="b2ada-110">**IRDVTaskPlugin** also has these types of members:</span></span>

-   [<span data-ttu-id="b2ada-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="b2ada-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="b2ada-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b2ada-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b2ada-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="b2ada-113">Methods</span></span>

<span data-ttu-id="b2ada-114">Die Schnittstelle " **iridvtaskplugin** " verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="b2ada-114">The **IRDVTaskPlugin** interface has these methods.</span></span>



| <span data-ttu-id="b2ada-115">Methode</span><span class="sxs-lookup"><span data-stu-id="b2ada-115">Method</span></span>                                          | <span data-ttu-id="b2ada-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b2ada-116">Description</span></span>                                                        |
|:------------------------------------------------|:-------------------------------------------------------------------|
| [<span data-ttu-id="b2ada-117">**Initialisieren**</span><span class="sxs-lookup"><span data-stu-id="b2ada-117">**Initialize**</span></span>](irdvtaskplugin-initialize.md) | <span data-ttu-id="b2ada-118">Wird aufgerufen, um den Task-Agent zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="b2ada-118">Called to initialize the task agent.</span></span><br/>                    |
| [<span data-ttu-id="b2ada-119">**StartTask**</span><span class="sxs-lookup"><span data-stu-id="b2ada-119">**StartTask**</span></span>](irdvtaskplugin-starttask.md)   | <span data-ttu-id="b2ada-120">Wird aufgerufen, um den Aktualisierungs Task auf dem virtuellen Computer zu starten.</span><span class="sxs-lookup"><span data-stu-id="b2ada-120">Called to start the update task on the virtual machine.</span></span><br/> |
| [<span data-ttu-id="b2ada-121">**Terminate**</span><span class="sxs-lookup"><span data-stu-id="b2ada-121">**Terminate**</span></span>](irdvtaskplugin-terminate.md)   | <span data-ttu-id="b2ada-122">Wird aufgerufen, wenn der Task-Agent heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="b2ada-122">Called when the task agent is being shut down.</span></span><br/>          |



 

### <a name="properties"></a><span data-ttu-id="b2ada-123">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b2ada-123">Properties</span></span>

<span data-ttu-id="b2ada-124">Die Schnittstelle " **iridvtaskplugin** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b2ada-124">The **IRDVTaskPlugin** interface has these properties.</span></span>



| <span data-ttu-id="b2ada-125">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b2ada-125">Property</span></span>                                                   | <span data-ttu-id="b2ada-126">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="b2ada-126">Access type</span></span>          | <span data-ttu-id="b2ada-127">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b2ada-127">Description</span></span>                                             |
|:-----------------------------------------------------------|:---------------------|:--------------------------------------------------------|
| [<span data-ttu-id="b2ada-128">**PluginName**</span><span class="sxs-lookup"><span data-stu-id="b2ada-128">**PluginName**</span></span>](irdvtaskplugin-pluginname.md)<br/> | <span data-ttu-id="b2ada-129">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b2ada-129">Read-only</span></span><br/> | <span data-ttu-id="b2ada-130">Enthält den anzeigen amen des Task-Agents.</span><span class="sxs-lookup"><span data-stu-id="b2ada-130">Contains the display name of the task agent.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b2ada-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b2ada-131">Remarks</span></span>

<span data-ttu-id="b2ada-132">Der Task-Agent wird auf dem virtuellen Computer ausgeführt, wenn der virtuelle Computer für ein System Update geplant ist.</span><span class="sxs-lookup"><span data-stu-id="b2ada-132">The task agent is run on the virtual machine when that virtual machine is scheduled for a system update.</span></span> <span data-ttu-id="b2ada-133">Der Task-Agent aktualisiert die virtuelle Maschine, wenn die [**Starttask**](irdvtaskplugin-starttask.md) -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="b2ada-133">The task agent updates the virtual machine when the [**StartTask**](irdvtaskplugin-starttask.md) method is called.</span></span>

<span data-ttu-id="b2ada-134">Fügen Sie der Registrierung des virtuellen Computers den folgenden Schlüssel hinzu, um den Task-Agent zu registrieren:</span><span class="sxs-lookup"><span data-stu-id="b2ada-134">To register the task agent, add the following key to the registry of the virtual machine:</span></span>

<span data-ttu-id="b2ada-135">**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Terminal Server** \\ **Task** \\ **Plugins** \\ **taskagentname**</span><span class="sxs-lookup"><span data-stu-id="b2ada-135">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Windows NT**\\**CurrentVersion**\\**Terminal Server**\\**Task**\\**Plugins**\\**TaskAgentName**</span></span>

<span data-ttu-id="b2ada-136">Fügen Sie unter diesem Registrierungsschlüssel die folgenden Werte hinzu:</span><span class="sxs-lookup"><span data-stu-id="b2ada-136">Under this registry key, add the following values:</span></span>



| <span data-ttu-id="b2ada-137">Name</span><span class="sxs-lookup"><span data-stu-id="b2ada-137">Name</span></span>                     | <span data-ttu-id="b2ada-138">type</span><span class="sxs-lookup"><span data-stu-id="b2ada-138">Type</span></span>                      | <span data-ttu-id="b2ada-139">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b2ada-139">Description</span></span>                                                                   |
|--------------------------|---------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="b2ada-140">**CLSID**</span><span class="sxs-lookup"><span data-stu-id="b2ada-140">**CLSID**</span></span><br/>     | <span data-ttu-id="b2ada-141">**REG- \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="b2ada-141">**REG\_SZ**</span></span><br/>    | <span data-ttu-id="b2ada-142">Eine Zeichenfolge, die die **CLSID** des Task-Agents darstellt.</span><span class="sxs-lookup"><span data-stu-id="b2ada-142">A string that represents the **CLSID** of the task agent.</span></span><br/>          |
| <span data-ttu-id="b2ada-143">**IsEnabled**</span><span class="sxs-lookup"><span data-stu-id="b2ada-143">**IsEnabled**</span></span><br/> | <span data-ttu-id="b2ada-144">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="b2ada-144">**REG\_DWORD**</span></span><br/> | <span data-ttu-id="b2ada-145">0, wenn der Task-Agent deaktiviert ist, oder 1, wenn der Task-Agent aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="b2ada-145">0 if the task agent is disabled or 1 if the task agent is enabled.</span></span><br/> |



 

> [!Note]  
> <span data-ttu-id="b2ada-146">Es können mehr als ein Task-Agent registriert werden, es wird jedoch nur ein Task-Agent verwendet.</span><span class="sxs-lookup"><span data-stu-id="b2ada-146">More than one task agent can be registered, but only one task agent will be used.</span></span> <span data-ttu-id="b2ada-147">Wenn mehr als ein Task-Agent aktiviert ist, wird nur der erste gefundene verwendet.</span><span class="sxs-lookup"><span data-stu-id="b2ada-147">If more than one task agent is enabled, only the first one found will be used.</span></span>

 

<span data-ttu-id="b2ada-148">Diese Schnittstelle wird zwar von den in den folgenden Anforderungen identifizierten Betriebssystemen unterstützt, Sie wird jedoch nur verwendet, wenn der virtuelle Computer unter Windows Server 2012 gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="b2ada-148">Although this interface is supported on the operating systems identified in the Requirements below, it will only be used if the virtual machine is hosted on Windows Server 2012.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2ada-149">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b2ada-149">Requirements</span></span>



| <span data-ttu-id="b2ada-150">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b2ada-150">Requirement</span></span> | <span data-ttu-id="b2ada-151">Wert</span><span class="sxs-lookup"><span data-stu-id="b2ada-151">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="b2ada-152">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b2ada-152">Minimum supported client</span></span><br/> | <span data-ttu-id="b2ada-153">Windows 7 Enterprise</span><span class="sxs-lookup"><span data-stu-id="b2ada-153">Windows 7 Enterprise</span></span><br/>   |
| <span data-ttu-id="b2ada-154">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b2ada-154">Minimum supported server</span></span><br/> | <span data-ttu-id="b2ada-155">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b2ada-155">Windows Server 2008 R2</span></span><br/> |



 

