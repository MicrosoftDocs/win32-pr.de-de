---
title: Emailaction. headerfields (Eigenschaft)
description: Ruft bei der Skripterstellung die Header Informationen in der e-Mail ab, die Sie senden möchten, oder legt diese fest.
ms.assetid: 492c1e7c-805a-4c58-82d3-45c82420c694
keywords:
- Headerfields-Eigenschaft Taskplaner
- Headerfields-Eigenschaft Taskplaner, emailaction-Objekt
- Emailaction-Objekt Taskplaner, headerfields (Eigenschaft)
topic_type:
- apiref
api_name:
- EmailAction.HeaderFields
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96cfb963879e47e51e1096d2559fe4e72c6b2543
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858973"
---
# <a name="emailactionheaderfields-property"></a><span data-ttu-id="c5872-106">Emailaction. headerfields (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="c5872-106">EmailAction.HeaderFields property</span></span>

<span data-ttu-id="c5872-107">\[Dieses Objekt wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c5872-107">\[This object is no longer supported.</span></span> <span data-ttu-id="c5872-108">Verwenden Sie "IExecAction" mit dem PowerShell-Cmdlet " [**Send-Mail Message**](/powershell/module/microsoft.powershell.utility/send-mailmessage) " als Problem Umgehung.\]</span><span class="sxs-lookup"><span data-stu-id="c5872-108">Please use IExecAction with the powershell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) cmdlet as a workaround.\]</span></span>

<span data-ttu-id="c5872-109">Ruft bei der Skripterstellung die Header Informationen in der e-Mail ab, die Sie senden möchten, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="c5872-109">For scripting, gets or sets the header information in the email you want to send.</span></span>

<span data-ttu-id="c5872-110">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="c5872-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5872-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5872-111">Syntax</span></span>


```VB
EmailAction.HeaderFields As TaskNamedValueCollection
```



## <a name="property-value"></a><span data-ttu-id="c5872-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="c5872-112">Property value</span></span>

<span data-ttu-id="c5872-113">Die Header Informationen in der e-Mail, die Sie senden möchten.</span><span class="sxs-lookup"><span data-stu-id="c5872-113">The header information in the email you want to send.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5872-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c5872-114">Requirements</span></span>



| <span data-ttu-id="c5872-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c5872-115">Requirement</span></span> | <span data-ttu-id="c5872-116">Wert</span><span class="sxs-lookup"><span data-stu-id="c5872-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c5872-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c5872-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c5872-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c5872-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="c5872-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c5872-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c5872-120">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c5872-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c5872-121">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="c5872-121">End of client support</span></span><br/>    | <span data-ttu-id="c5872-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c5872-122">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="c5872-123">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="c5872-123">End of server support</span></span><br/>    | <span data-ttu-id="c5872-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c5872-124">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="c5872-125">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="c5872-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="c5872-126"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c5872-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c5872-127">DLL</span><span class="sxs-lookup"><span data-stu-id="c5872-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c5872-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5872-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5872-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c5872-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5872-130">**Emailaction**</span><span class="sxs-lookup"><span data-stu-id="c5872-130">**EmailAction**</span></span>](emailaction.md)
</dt> <dt>

[<span data-ttu-id="c5872-131">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="c5872-131">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

