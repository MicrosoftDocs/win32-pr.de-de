---
title: Emailaction. BCC (Eigenschaft)
description: Dient zum Abrufen oder Festlegen der e-Mail-Adresse oder-Adressen, die Sie in der e-Mail-Nachricht für Bcc benötigen.
ms.assetid: ab340cd7-d6ce-4dce-8474-fdbbc02bd65b
keywords:
- BCC-Eigenschaft Taskplaner
- BCC-Eigenschaften Taskplaner, emailaction-Objekt
- Emailaction-Objekt Taskplaner, BCC-Eigenschaft
topic_type:
- apiref
api_name:
- EmailAction.Bcc
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bded5e88c236123832956ce42413352348ea535
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339158"
---
# <a name="emailactionbcc-property"></a><span data-ttu-id="a373b-106">Emailaction. BCC (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="a373b-106">EmailAction.Bcc property</span></span>

<span data-ttu-id="a373b-107">\[Dieses Objekt wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a373b-107">\[This object is no longer supported.</span></span> <span data-ttu-id="a373b-108">Verwenden Sie "IExecAction" mit dem PowerShell-Cmdlet " [**Send-Mail Message**](/powershell/module/microsoft.powershell.utility/send-mailmessage) " als Problem Umgehung.\]</span><span class="sxs-lookup"><span data-stu-id="a373b-108">Please use IExecAction with the powershell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) cmdlet as a workaround.\]</span></span>

<span data-ttu-id="a373b-109">Dient zum Abrufen oder Festlegen der e-Mail-Adresse oder-Adressen, die Sie in der e-Mail-Nachricht für Bcc benötigen.</span><span class="sxs-lookup"><span data-stu-id="a373b-109">For scripting, gets or sets the email address or addresses that you want to Bcc in the email message.</span></span>

<span data-ttu-id="a373b-110">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a373b-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a373b-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="a373b-111">Syntax</span></span>


```VB
EmailAction.Bcc As String
```



## <a name="property-value"></a><span data-ttu-id="a373b-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="a373b-112">Property value</span></span>

<span data-ttu-id="a373b-113">Die e-Mail-Adressen, die Sie in der e-Mail-Nachricht für Bcc angeben möchten.</span><span class="sxs-lookup"><span data-stu-id="a373b-113">The email address or addresses that you want to Bcc in the email message.</span></span>

## <a name="requirements"></a><span data-ttu-id="a373b-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a373b-114">Requirements</span></span>



| <span data-ttu-id="a373b-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a373b-115">Requirement</span></span> | <span data-ttu-id="a373b-116">Wert</span><span class="sxs-lookup"><span data-stu-id="a373b-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a373b-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a373b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a373b-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a373b-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="a373b-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a373b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a373b-120">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a373b-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a373b-121">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="a373b-121">End of client support</span></span><br/>    | <span data-ttu-id="a373b-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a373b-122">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="a373b-123">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="a373b-123">End of server support</span></span><br/>    | <span data-ttu-id="a373b-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a373b-124">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="a373b-125">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="a373b-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="a373b-126"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a373b-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a373b-127">DLL</span><span class="sxs-lookup"><span data-stu-id="a373b-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a373b-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a373b-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a373b-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a373b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a373b-130">**Emailaction**</span><span class="sxs-lookup"><span data-stu-id="a373b-130">**EmailAction**</span></span>](emailaction.md)
</dt> <dt>

[<span data-ttu-id="a373b-131">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="a373b-131">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

