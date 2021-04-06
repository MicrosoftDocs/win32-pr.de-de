---
title: Emailaction. ReplyTo-Eigenschaft
description: Ruft bei der Skripterstellung die e-Mail-Adresse ab, der Sie antworten möchten, oder legt diese fest.
ms.assetid: 2b267e6e-c0c9-42ca-bc4a-cc18af5bcb9c
keywords:
- ReplyTo-Eigenschaft Taskplaner
- ReplyTo-Eigenschaft Taskplaner, emailaction-Objekt
- Emailaction-Objekt Taskplaner, ReplyTo-Eigenschaft
topic_type:
- apiref
api_name:
- EmailAction.ReplyTo
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc7ed1fd84245e4d938d329f0e9773271efec45b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858972"
---
# <a name="emailactionreplyto-property"></a><span data-ttu-id="6bd9d-106">Emailaction. ReplyTo-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6bd9d-106">EmailAction.ReplyTo property</span></span>

<span data-ttu-id="6bd9d-107">\[Dieses Objekt wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6bd9d-107">\[This object is no longer supported.</span></span> <span data-ttu-id="6bd9d-108">Verwenden Sie "IExecAction" mit dem PowerShell-Cmdlet " [**Send-Mail Message**](/powershell/module/microsoft.powershell.utility/send-mailmessage) " als Problem Umgehung.\]</span><span class="sxs-lookup"><span data-stu-id="6bd9d-108">Please use IExecAction with the powershell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) cmdlet as a workaround.\]</span></span>

<span data-ttu-id="6bd9d-109">Ruft bei der Skripterstellung die e-Mail-Adresse ab, der Sie antworten möchten, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="6bd9d-109">For scripting, gets or sets the email address that you want to reply to.</span></span>

<span data-ttu-id="6bd9d-110">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="6bd9d-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6bd9d-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="6bd9d-111">Syntax</span></span>


```VB
EmailAction.ReplyTo As String
```



## <a name="property-value"></a><span data-ttu-id="6bd9d-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="6bd9d-112">Property value</span></span>

<span data-ttu-id="6bd9d-113">Die e-Mail-Adresse, der Sie antworten möchten.</span><span class="sxs-lookup"><span data-stu-id="6bd9d-113">The email address that you want to reply to.</span></span>

## <a name="requirements"></a><span data-ttu-id="6bd9d-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6bd9d-114">Requirements</span></span>



| <span data-ttu-id="6bd9d-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6bd9d-115">Requirement</span></span> | <span data-ttu-id="6bd9d-116">Wert</span><span class="sxs-lookup"><span data-stu-id="6bd9d-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6bd9d-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6bd9d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6bd9d-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6bd9d-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="6bd9d-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6bd9d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6bd9d-120">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6bd9d-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6bd9d-121">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="6bd9d-121">End of client support</span></span><br/>    | <span data-ttu-id="6bd9d-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6bd9d-122">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="6bd9d-123">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="6bd9d-123">End of server support</span></span><br/>    | <span data-ttu-id="6bd9d-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6bd9d-124">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="6bd9d-125">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="6bd9d-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="6bd9d-126"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6bd9d-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6bd9d-127">DLL</span><span class="sxs-lookup"><span data-stu-id="6bd9d-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6bd9d-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6bd9d-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6bd9d-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6bd9d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bd9d-130">**Emailaction**</span><span class="sxs-lookup"><span data-stu-id="6bd9d-130">**EmailAction**</span></span>](emailaction.md)
</dt> <dt>

[<span data-ttu-id="6bd9d-131">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="6bd9d-131">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

