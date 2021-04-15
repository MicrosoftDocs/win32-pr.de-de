---
title: "\"Undvtaskplugin\"-Starttask-Methode"
description: Wird aufgerufen, um den Aktualisierungs Task auf dem virtuellen Computer zu starten.
ms.assetid: c1e9f18b-1e83-4a29-8646-8adde94e8c14
ms.tgt_platform: multiple
keywords:
- Starttask-Methode Remotedesktopdienste
- Starttask-Methode Remotedesktopdienste, undvtaskplugin-Schnittstelle
- Undvtaskplugin-Schnittstelle Remotedesktopdienste, Starttask-Methode
topic_type:
- apiref
api_name:
- IRDVTaskPlugin.StartTask
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 51c499549378700a90d8fc78d075bc07c1f874cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477427"
---
# <a name="irdvtaskpluginstarttask-method"></a><span data-ttu-id="c36fa-106">Undvtaskplugin:: Starttask-Methode</span><span class="sxs-lookup"><span data-stu-id="c36fa-106">IRDVTaskPlugin::StartTask method</span></span>

<span data-ttu-id="c36fa-107">Wird aufgerufen, um den Aktualisierungs Task auf dem virtuellen Computer zu starten.</span><span class="sxs-lookup"><span data-stu-id="c36fa-107">Called to start the update task on the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="c36fa-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c36fa-108">Syntax</span></span>


```C++
HRESULT StartTask(
  [in] BSTR            Label,
  [in] BSTR            Identifier,
  [in] SAFEARRAY(BYTE) *Context
);
```



## <a name="parameters"></a><span data-ttu-id="c36fa-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c36fa-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c36fa-110">*Bezeichnung* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c36fa-110">*Label* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c36fa-111">Die Bezeichnung für den Task.</span><span class="sxs-lookup"><span data-stu-id="c36fa-111">The label for the task.</span></span> <span data-ttu-id="c36fa-112">Dies ist die Bezeichnung, die in der [**ScheduleTask**](irdvtaskpluginnotifysink-scheduletask.md) -Methode an den Auslöse-Agent übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="c36fa-112">This is the label that was passed to the trigger agent in the [**ScheduleTask**](irdvtaskpluginnotifysink-scheduletask.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="c36fa-113">*Bezeichner* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c36fa-113">*Identifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c36fa-114">Der Bezeichner des Tasks.</span><span class="sxs-lookup"><span data-stu-id="c36fa-114">The identifier of the task.</span></span> <span data-ttu-id="c36fa-115">Dies ist der Bezeichner, der in der [**ScheduleTask**](irdvtaskpluginnotifysink-scheduletask.md) -Methode an den Auslöse-Agent übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="c36fa-115">This is the identifier that was passed to the trigger agent in the [**ScheduleTask**](irdvtaskpluginnotifysink-scheduletask.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="c36fa-116">*Kontext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c36fa-116">*Context* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c36fa-117">Optionale Daten für den Task.</span><span class="sxs-lookup"><span data-stu-id="c36fa-117">Optional data for the task.</span></span> <span data-ttu-id="c36fa-118">Dies sind die Daten, die in der [**ScheduleTask**](irdvtaskpluginnotifysink-scheduletask.md) -Methode an den Auslöse-Agent übergeben wurden.</span><span class="sxs-lookup"><span data-stu-id="c36fa-118">This is the data that was passed to the trigger agent in the [**ScheduleTask**](irdvtaskpluginnotifysink-scheduletask.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c36fa-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c36fa-119">Return value</span></span>

<span data-ttu-id="c36fa-120">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="c36fa-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c36fa-121">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c36fa-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c36fa-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c36fa-122">Requirements</span></span>



| <span data-ttu-id="c36fa-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c36fa-123">Requirement</span></span> | <span data-ttu-id="c36fa-124">Wert</span><span class="sxs-lookup"><span data-stu-id="c36fa-124">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="c36fa-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c36fa-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c36fa-126">Windows 7 Enterprise</span><span class="sxs-lookup"><span data-stu-id="c36fa-126">Windows 7 Enterprise</span></span><br/>   |
| <span data-ttu-id="c36fa-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c36fa-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c36fa-128">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c36fa-128">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c36fa-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c36fa-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c36fa-130">**"Undvtaskplugin"**</span><span class="sxs-lookup"><span data-stu-id="c36fa-130">**IRDVTaskPlugin**</span></span>](irdvtaskplugin.md)
</dt> </dl>

 

 





