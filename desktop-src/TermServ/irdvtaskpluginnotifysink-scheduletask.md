---
title: Undvtaskpluginnotifysink ScheduleTask-Methode
description: Wird vom Task-Agent zum Planen einer Aufgabe aufgerufen.
ms.assetid: 06793439-cf16-40ca-8a91-08acc22c73ed
ms.tgt_platform: multiple
keywords:
- ScheduleTask-Methode Remotedesktopdienste
- ScheduleTask-Methode Remotedesktopdienste, undvtaskpluginnotifysink-Schnittstelle
- Undvtaskpluginnotifysink-Schnittstelle Remotedesktopdienste, ScheduleTask-Methode
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink.ScheduleTask
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c9bde92992eec9c4ab3d4151c59e6d687ec2f3fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859247"
---
# <a name="irdvtaskpluginnotifysinkscheduletask-method"></a><span data-ttu-id="bf180-106">Undvtaskpluginnotifysink:: ScheduleTask-Methode</span><span class="sxs-lookup"><span data-stu-id="bf180-106">IRDVTaskPluginNotifySink::ScheduleTask method</span></span>

<span data-ttu-id="bf180-107">Wird vom Task-Agent zum Planen einer Aufgabe aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="bf180-107">Called by the task agent to schedule a task.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf180-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="bf180-108">Syntax</span></span>


```C++
HRESULT ScheduleTask(
  [in] FILETIME        ftStartTime,
  [in] FILETIME        ftEndTime,
  [in] FILETIME        ftDeadline,
  [in] BSTR            bstrLabel,
  [in] BSTR            bstrIdentifier,
  [in] SAFEARRAY(BYTE) saContext
);
```



## <a name="parameters"></a><span data-ttu-id="bf180-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="bf180-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf180-110">*ftstarttime* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bf180-110">*ftStartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf180-111">Typ: **[ **FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)**</span><span class="sxs-lookup"><span data-stu-id="bf180-111">Type: **[**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)**</span></span>

<span data-ttu-id="bf180-112">Die früheste Startzeit der Aufgabe in UTC.</span><span class="sxs-lookup"><span data-stu-id="bf180-112">The earliest task start time, in UTC.</span></span>

</dd> <dt>

<span data-ttu-id="bf180-113">"- *Zeit* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="bf180-113">*ftEndTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf180-114">Typ: **[ **FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)**</span><span class="sxs-lookup"><span data-stu-id="bf180-114">Type: **[**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)**</span></span>

<span data-ttu-id="bf180-115">Die Endzeit der Aufgabe in UTC.</span><span class="sxs-lookup"><span data-stu-id="bf180-115">The task end time, in UTC.</span></span> <span data-ttu-id="bf180-116">Übergibt eine [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) -Menge auf alle Nullen, wenn keine Endzeit angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="bf180-116">Pass a [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) set to all zeros if no end time is specified.</span></span>

</dd> <dt>

<span data-ttu-id="bf180-117">*ftstichtag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bf180-117">*ftDeadline* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf180-118">Typ: **[ **FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)**</span><span class="sxs-lookup"><span data-stu-id="bf180-118">Type: **[**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)**</span></span>

<span data-ttu-id="bf180-119">Der Task Stichtag in UTC.</span><span class="sxs-lookup"><span data-stu-id="bf180-119">The task deadline, in UTC.</span></span> <span data-ttu-id="bf180-120">Hiermit wird die Priorität für mehrere Aufgaben festgelegt, die sich innerhalb des Start Fensters befinden.</span><span class="sxs-lookup"><span data-stu-id="bf180-120">This is used to set priority for multiple tasks that are within their start window.</span></span> <span data-ttu-id="bf180-121">Wenn mehr als eine Aufgabe gestartet werden soll, wird die mit dem frühesten Stichtag zuerst gestartet.</span><span class="sxs-lookup"><span data-stu-id="bf180-121">If more than one task should be started, the one with the earliest deadline will be started first.</span></span>

</dd> <dt>

<span data-ttu-id="bf180-122">*bstraulabel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bf180-122">*bstrLabel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf180-123">Typ: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="bf180-123">Type: **BSTR**</span></span>

<span data-ttu-id="bf180-124">Die Bezeichnung für den Task.</span><span class="sxs-lookup"><span data-stu-id="bf180-124">The label for the task.</span></span> <span data-ttu-id="bf180-125">Diese wird an die [**Starttask**](irdvtaskplugin-starttask.md) -Methode übermittelt.</span><span class="sxs-lookup"><span data-stu-id="bf180-125">This is passed to the [**StartTask**](irdvtaskplugin-starttask.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="bf180-126">*bstridentifier* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bf180-126">*bstrIdentifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf180-127">Typ: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="bf180-127">Type: **BSTR**</span></span>

<span data-ttu-id="bf180-128">Der Bezeichner des Tasks.</span><span class="sxs-lookup"><span data-stu-id="bf180-128">The identifier of the task.</span></span> <span data-ttu-id="bf180-129">Diese wird an die [**Starttask**](irdvtaskplugin-starttask.md) -Methode übermittelt.</span><span class="sxs-lookup"><span data-stu-id="bf180-129">This is passed to the [**StartTask**](irdvtaskplugin-starttask.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="bf180-130">*sacontext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bf180-130">*saContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf180-131">Typ: **SafeArray (Byte)**</span><span class="sxs-lookup"><span data-stu-id="bf180-131">Type: **SAFEARRAY(BYTE)**</span></span>

<span data-ttu-id="bf180-132">Optionale Daten für den Task.</span><span class="sxs-lookup"><span data-stu-id="bf180-132">Optional data for the task.</span></span> <span data-ttu-id="bf180-133">Diese wird an die [**Starttask**](irdvtaskplugin-starttask.md) -Methode übermittelt.</span><span class="sxs-lookup"><span data-stu-id="bf180-133">This is passed to the [**StartTask**](irdvtaskplugin-starttask.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf180-134">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bf180-134">Return value</span></span>

<span data-ttu-id="bf180-135">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="bf180-135">Type: **HRESULT**</span></span>

<span data-ttu-id="bf180-136">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="bf180-136">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bf180-137">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bf180-137">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf180-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bf180-138">Requirements</span></span>



| <span data-ttu-id="bf180-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bf180-139">Requirement</span></span> | <span data-ttu-id="bf180-140">Wert</span><span class="sxs-lookup"><span data-stu-id="bf180-140">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="bf180-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bf180-141">Minimum supported client</span></span><br/> | <span data-ttu-id="bf180-142">Windows 7 Enterprise</span><span class="sxs-lookup"><span data-stu-id="bf180-142">Windows 7 Enterprise</span></span><br/>   |
| <span data-ttu-id="bf180-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bf180-143">Minimum supported server</span></span><br/> | <span data-ttu-id="bf180-144">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bf180-144">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bf180-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bf180-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf180-146">**"Undvtaskpluginnotifysink"**</span><span class="sxs-lookup"><span data-stu-id="bf180-146">**IRDVTaskPluginNotifySink**</span></span>](irdvtaskpluginnotifysink.md)
</dt> </dl>

 

