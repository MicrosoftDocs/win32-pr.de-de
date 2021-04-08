---
title: Emailaction. Attachments (Eigenschaft)
description: Dient zum Abrufen oder Festlegen eines Arrays von Anhängen, das mit der e-Mail-Nachricht gesendet wird.
ms.assetid: 59bcb8c4-8b8c-4f09-94d6-3a65f1e8c0a8
keywords:
- Eigenschaften Taskplaner "Anlagen"
- Anlagen Eigenschaft Taskplaner, emailaction-Objekt
- Emailaction-Objekt Taskplaner, Eigenschaft "Anhänge"
topic_type:
- apiref
api_name:
- EmailAction.Attachments
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ae620321f9dca7a5c38decf7de661d713989c88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741904"
---
# <a name="emailactionattachments-property"></a><span data-ttu-id="b9828-106">Emailaction. Attachments (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="b9828-106">EmailAction.Attachments property</span></span>

<span data-ttu-id="b9828-107">\[Dieses Objekt wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b9828-107">\[This object is no longer supported.</span></span> <span data-ttu-id="b9828-108">Verwenden Sie "IExecAction" mit dem PowerShell-Cmdlet " [**Send-Mail Message**](/powershell/module/microsoft.powershell.utility/send-mailmessage) " als Problem Umgehung.\]</span><span class="sxs-lookup"><span data-stu-id="b9828-108">Please use IExecAction with the powershell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) cmdlet as a workaround.\]</span></span>

<span data-ttu-id="b9828-109">Dient zum Abrufen oder Festlegen eines Arrays von Anhängen, das mit der e-Mail-Nachricht gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="b9828-109">For scripting, gets or sets an array of attachments that is sent with the email message.</span></span>

<span data-ttu-id="b9828-110">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="b9828-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9828-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="b9828-111">Syntax</span></span>


```VB
EmailAction.Attachments As String
```



## <a name="property-value"></a><span data-ttu-id="b9828-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="b9828-112">Property value</span></span>

<span data-ttu-id="b9828-113">Ein Array von Anlagen, das mit der e-Mail-Nachricht gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="b9828-113">An array of attachments that is sent with the email message.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9828-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b9828-114">Remarks</span></span>

<span data-ttu-id="b9828-115">Es können maximal acht Anhänge im Array von Anlagen vorliegen.</span><span class="sxs-lookup"><span data-stu-id="b9828-115">A maximum of eight attachments can be in the array of attachments.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9828-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b9828-116">Requirements</span></span>



| <span data-ttu-id="b9828-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b9828-117">Requirement</span></span> | <span data-ttu-id="b9828-118">Wert</span><span class="sxs-lookup"><span data-stu-id="b9828-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b9828-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b9828-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b9828-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b9828-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="b9828-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b9828-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b9828-122">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b9828-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b9828-123">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="b9828-123">End of client support</span></span><br/>    | <span data-ttu-id="b9828-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b9828-124">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="b9828-125">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="b9828-125">End of server support</span></span><br/>    | <span data-ttu-id="b9828-126">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b9828-126">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="b9828-127">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="b9828-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="b9828-128"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b9828-128"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b9828-129">DLL</span><span class="sxs-lookup"><span data-stu-id="b9828-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9828-130"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b9828-130"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9828-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b9828-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9828-132">**Emailaction**</span><span class="sxs-lookup"><span data-stu-id="b9828-132">**EmailAction**</span></span>](emailaction.md)
</dt> <dt>

[<span data-ttu-id="b9828-133">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="b9828-133">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

