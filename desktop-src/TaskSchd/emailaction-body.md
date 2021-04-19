---
title: Emailaction. Body (Eigenschaft)
description: Ruft bei der Skripterstellung den Text der e-Mail ab, die die e-Mail-Nachricht enthält, oder legt diesen fest
ms.assetid: 0015c2b9-9278-407b-b3cf-492f2d95bcb6
keywords:
- Body-Eigenschafts Taskplaner
- Body-Eigenschaften Taskplaner, emailaction-Objekt
- Emailaction-Objekt Taskplaner, Text-Eigenschaft
topic_type:
- apiref
api_name:
- EmailAction.Body
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84be176fcf63c7a5191588dc0a68ccaf06c69f94
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337936"
---
# <a name="emailactionbody-property"></a><span data-ttu-id="6d7a5-106">Emailaction. Body (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="6d7a5-106">EmailAction.Body property</span></span>

<span data-ttu-id="6d7a5-107">\[Dieses Objekt wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6d7a5-107">\[This object is no longer supported.</span></span> <span data-ttu-id="6d7a5-108">Verwenden Sie "IExecAction" mit dem PowerShell-Cmdlet " [**Send-Mail Message**](/powershell/module/microsoft.powershell.utility/send-mailmessage) " als Problem Umgehung.\]</span><span class="sxs-lookup"><span data-stu-id="6d7a5-108">Please use IExecAction with the powershell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) cmdlet as a workaround.\]</span></span>

<span data-ttu-id="6d7a5-109">Ruft bei der Skripterstellung den Text der e-Mail ab, die die e-Mail-Nachricht enthält, oder legt diesen fest</span><span class="sxs-lookup"><span data-stu-id="6d7a5-109">For scripting, gets or sets the body of the email that contains the email message.</span></span>

<span data-ttu-id="6d7a5-110">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="6d7a5-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d7a5-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="6d7a5-111">Syntax</span></span>


```VB
EmailAction.Body As String
```



## <a name="property-value"></a><span data-ttu-id="6d7a5-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="6d7a5-112">Property value</span></span>

<span data-ttu-id="6d7a5-113">Der Text der e-Mail, in der die e-Mail-Nachricht enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="6d7a5-113">The body of the email that contains the email message.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d7a5-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6d7a5-114">Remarks</span></span>

<span data-ttu-id="6d7a5-115">Beim Festlegen dieses Eigenschafts Werts kann der Wert aus Text bestehen, der aus einer DLL-Datei der Ressource abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="6d7a5-115">When setting this property value, the value can be text that is retrieved from a resource .dll file.</span></span> <span data-ttu-id="6d7a5-116">Eine spezialisierte Zeichenfolge wird verwendet, um auf den Text aus der Ressourcen Datei zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="6d7a5-116">A specialized string is used to reference the text from the resource file.</span></span> <span data-ttu-id="6d7a5-117">Das Format der Zeichenfolge ist $ (@ \[ dll \] , \[ ResourceId \] ), wobei \[ dll \] der Pfad zur DLL-Datei, die die Ressource enthält, und \[ ResourceId der \] Bezeichner für den Ressourcen Text ist.</span><span class="sxs-lookup"><span data-stu-id="6d7a5-117">The format of the string is $(@ \[Dll\], \[ResourceID\]) where \[Dll\] is the path to the .dll file that contains the resource and \[ResourceID\] is the identifier for the resource text.</span></span> <span data-ttu-id="6d7a5-118">Wenn z. b. der Wert dieser Eigenschaft auf $ (@% systemroot% \\ system32 \\ResourceName.dll,-101) festgelegt wird, wird die-Eigenschaft auf den Wert des Ressourcen Texts mit einem Bezeichner gleich-101 in der Datei% SystemRoot% \\ system32ResourceName.dll festgelegt \\ .</span><span class="sxs-lookup"><span data-stu-id="6d7a5-118">For example, the setting this property value to $(@ %SystemRoot%\\System32\\ResourceName.dll, -101) will set the property to the value of the resource text with an identifier equal to -101 in the %SystemRoot%\\System32\\ResourceName.dll file.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d7a5-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6d7a5-119">Requirements</span></span>



| <span data-ttu-id="6d7a5-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6d7a5-120">Requirement</span></span> | <span data-ttu-id="6d7a5-121">Wert</span><span class="sxs-lookup"><span data-stu-id="6d7a5-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6d7a5-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6d7a5-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6d7a5-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6d7a5-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="6d7a5-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6d7a5-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6d7a5-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6d7a5-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6d7a5-126">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="6d7a5-126">End of client support</span></span><br/>    | <span data-ttu-id="6d7a5-127">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6d7a5-127">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="6d7a5-128">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="6d7a5-128">End of server support</span></span><br/>    | <span data-ttu-id="6d7a5-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6d7a5-129">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="6d7a5-130">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="6d7a5-130">Type library</span></span><br/>             | <dl> <span data-ttu-id="6d7a5-131"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6d7a5-131"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6d7a5-132">DLL</span><span class="sxs-lookup"><span data-stu-id="6d7a5-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6d7a5-133"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d7a5-133"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d7a5-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6d7a5-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d7a5-135">**Emailaction**</span><span class="sxs-lookup"><span data-stu-id="6d7a5-135">**EmailAction**</span></span>](emailaction.md)
</dt> <dt>

[<span data-ttu-id="6d7a5-136">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="6d7a5-136">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

