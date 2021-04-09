---
title: Undvtaskpluginnotifysink deleteschedule-Methode
description: Wird vom Task-Agent aufgerufen, um einen geplanten Task zu löschen.
ms.assetid: 67a9493e-367a-48c9-8f94-276d696406b7
ms.tgt_platform: multiple
keywords:
- Deleteschedule-Methode Remotedesktopdienste
- Deleteschedule-Methode Remotedesktopdienste, undvtaskpluginnotifysink-Schnittstelle
- Undvtaskpluginnotifysink-Schnittstelle Remotedesktopdienste, deleteschedule-Methode
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink.DeleteSchedule
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f00bcc740f87acb7f051decd5f2fc9b55ffbf642
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106167"
---
# <a name="irdvtaskpluginnotifysinkdeleteschedule-method"></a><span data-ttu-id="199cf-106">Undvtaskpluginnotifysink::D eleteschedule-Methode</span><span class="sxs-lookup"><span data-stu-id="199cf-106">IRDVTaskPluginNotifySink::DeleteSchedule method</span></span>

<span data-ttu-id="199cf-107">Wird vom Task-Agent aufgerufen, um einen geplanten Task zu löschen.</span><span class="sxs-lookup"><span data-stu-id="199cf-107">Called by the task agent to delete a scheduled task.</span></span>

## <a name="syntax"></a><span data-ttu-id="199cf-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="199cf-108">Syntax</span></span>


```C++
HRESULT DeleteSchedule(
  [in] BSTR bstrIdentifier
);
```



## <a name="parameters"></a><span data-ttu-id="199cf-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="199cf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="199cf-110">*bstridentifier* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="199cf-110">*bstrIdentifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="199cf-111">Der Bezeichner des geplanten Tasks.</span><span class="sxs-lookup"><span data-stu-id="199cf-111">The identifier of the scheduled task.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="199cf-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="199cf-112">Return value</span></span>

<span data-ttu-id="199cf-113">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="199cf-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="199cf-114">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="199cf-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="199cf-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="199cf-115">Requirements</span></span>



| <span data-ttu-id="199cf-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="199cf-116">Requirement</span></span> | <span data-ttu-id="199cf-117">Wert</span><span class="sxs-lookup"><span data-stu-id="199cf-117">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="199cf-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="199cf-118">Minimum supported client</span></span><br/> | <span data-ttu-id="199cf-119">Windows 7 Enterprise</span><span class="sxs-lookup"><span data-stu-id="199cf-119">Windows 7 Enterprise</span></span><br/>   |
| <span data-ttu-id="199cf-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="199cf-120">Minimum supported server</span></span><br/> | <span data-ttu-id="199cf-121">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="199cf-121">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="199cf-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="199cf-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="199cf-123">**"Undvtaskpluginnotifysink"**</span><span class="sxs-lookup"><span data-stu-id="199cf-123">**IRDVTaskPluginNotifySink**</span></span>](irdvtaskpluginnotifysink.md)
</dt> </dl>

 

 





