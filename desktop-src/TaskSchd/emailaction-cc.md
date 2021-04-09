---
title: EmailAction.CC-Eigenschaft
description: Dient zum Abrufen oder Festlegen der e-Mail-Adresse oder der Adressen, die Sie in der e-Mail-Nachricht für CC festlegen möchten.
ms.assetid: 4ad67064-3e6b-4666-a3ce-66e4dcc3f873
keywords:
- Taskplaner der CC-Eigenschaft
- CC-Eigenschaft Taskplaner, emailaction-Objekt
- Emailaction-Objekt Taskplaner, CC-Eigenschaft
topic_type:
- apiref
api_name:
- EmailAction.Cc
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00f05d7fbd1883aa38ba972eba1eb14767349357
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741897"
---
# <a name="emailactioncc-property"></a><span data-ttu-id="ce34f-106">EmailAction.CC-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ce34f-106">EmailAction.Cc property</span></span>

<span data-ttu-id="ce34f-107">\[Dieses Objekt wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ce34f-107">\[This object is no longer supported.</span></span> <span data-ttu-id="ce34f-108">Verwenden Sie "IExecAction" mit dem PowerShell-Cmdlet " [**Send-Mail Message**](/powershell/module/microsoft.powershell.utility/send-mailmessage) " als Problem Umgehung.\]</span><span class="sxs-lookup"><span data-stu-id="ce34f-108">Please use IExecAction with the powershell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) cmdlet as a workaround.\]</span></span>

<span data-ttu-id="ce34f-109">Dient zum Abrufen oder Festlegen der e-Mail-Adresse oder der Adressen, die Sie in der e-Mail-Nachricht für CC festlegen möchten.</span><span class="sxs-lookup"><span data-stu-id="ce34f-109">For scripting, gets or sets the email address or addresses that you want to Cc in the email message.</span></span>

<span data-ttu-id="ce34f-110">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="ce34f-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce34f-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="ce34f-111">Syntax</span></span>


```VB
EmailAction.Cc As String
```



## <a name="property-value"></a><span data-ttu-id="ce34f-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="ce34f-112">Property value</span></span>

<span data-ttu-id="ce34f-113">Die e-Mail-Adresse oder Adressen, die Sie in der e-Mail-Nachricht CC angeben möchten.</span><span class="sxs-lookup"><span data-stu-id="ce34f-113">The email address or addresses that you want to Cc in the email message.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce34f-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ce34f-114">Requirements</span></span>



| <span data-ttu-id="ce34f-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ce34f-115">Requirement</span></span> | <span data-ttu-id="ce34f-116">Wert</span><span class="sxs-lookup"><span data-stu-id="ce34f-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ce34f-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ce34f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ce34f-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ce34f-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="ce34f-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ce34f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ce34f-120">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ce34f-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ce34f-121">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="ce34f-121">End of client support</span></span><br/>    | <span data-ttu-id="ce34f-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ce34f-122">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="ce34f-123">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="ce34f-123">End of server support</span></span><br/>    | <span data-ttu-id="ce34f-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ce34f-124">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="ce34f-125">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="ce34f-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="ce34f-126"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ce34f-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ce34f-127">DLL</span><span class="sxs-lookup"><span data-stu-id="ce34f-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ce34f-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ce34f-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce34f-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ce34f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce34f-130">**Emailaction**</span><span class="sxs-lookup"><span data-stu-id="ce34f-130">**EmailAction**</span></span>](emailaction.md)
</dt> <dt>

[<span data-ttu-id="ce34f-131">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="ce34f-131">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

