---
title: Emailaction. Subject (Eigenschaft)
description: Ruft bei der Skripterstellung den Betreff der e-Mail-Nachricht ab oder legt diesen fest.
ms.assetid: ea398af1-9ae6-4bcf-9618-bb840b15127e
keywords:
- Eigenschaft "Betreff" Taskplaner
- Subject-Eigenschaft Taskplaner, emailaction-Objekt
- Emailaction-Objekt Taskplaner, Subject-Eigenschaft
topic_type:
- apiref
api_name:
- EmailAction.Subject
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6236ded39993c4cb2499e64ba2e31959df91449e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343597"
---
# <a name="emailactionsubject-property"></a><span data-ttu-id="e14ce-106">Emailaction. Subject (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e14ce-106">EmailAction.Subject property</span></span>

<span data-ttu-id="e14ce-107">\[Dieses Objekt wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e14ce-107">\[This object is no longer supported.</span></span> <span data-ttu-id="e14ce-108">Verwenden Sie "IExecAction" mit dem PowerShell-Cmdlet " [**Send-Mail Message**](/powershell/module/microsoft.powershell.utility/send-mailmessage?view=powershell-7&preserve-view=true) " als Problem Umgehung.\]</span><span class="sxs-lookup"><span data-stu-id="e14ce-108">Please use IExecAction with the powershell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage?view=powershell-7&preserve-view=true) cmdlet as a workaround.\]</span></span>

<span data-ttu-id="e14ce-109">Ruft bei der Skripterstellung den Betreff der e-Mail-Nachricht ab oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="e14ce-109">For scripting, gets or sets the subject of the email message.</span></span>

<span data-ttu-id="e14ce-110">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="e14ce-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e14ce-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="e14ce-111">Syntax</span></span>


```VB
EmailAction.Subject As String
```



## <a name="property-value"></a><span data-ttu-id="e14ce-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="e14ce-112">Property value</span></span>

<span data-ttu-id="e14ce-113">Der Betreff der e-Mail-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="e14ce-113">The subject of the email message.</span></span>

## <a name="remarks"></a><span data-ttu-id="e14ce-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e14ce-114">Remarks</span></span>

<span data-ttu-id="e14ce-115">Beim Festlegen dieses Eigenschafts Werts kann der Wert aus Text bestehen, der aus einer DLL-Datei der Ressource abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="e14ce-115">When setting this property value, the value can be text that is retrieved from a resource .dll file.</span></span> <span data-ttu-id="e14ce-116">Eine spezialisierte Zeichenfolge wird verwendet, um auf den Text aus der Ressourcen Datei zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="e14ce-116">A specialized string is used to reference the text from the resource file.</span></span> <span data-ttu-id="e14ce-117">Das Format der Zeichenfolge ist $ (@ \[ dll \] , \[ ResourceId \] ), wobei \[ dll \] der Pfad zur DLL-Datei, die die Ressource enthält, und \[ ResourceId der \] Bezeichner für den Ressourcen Text ist.</span><span class="sxs-lookup"><span data-stu-id="e14ce-117">The format of the string is $(@ \[Dll\], \[ResourceID\]) where \[Dll\] is the path to the .dll file that contains the resource and \[ResourceID\] is the identifier for the resource text.</span></span> <span data-ttu-id="e14ce-118">Wenn z. b. der Wert dieser Eigenschaft auf $ (@% systemroot% \\ system32 \\ResourceName.dll,-101) festgelegt wird, wird die-Eigenschaft auf den Wert des Ressourcen Texts mit einem Bezeichner gleich-101 in der Datei% SystemRoot% \\ system32ResourceName.dll festgelegt \\ .</span><span class="sxs-lookup"><span data-stu-id="e14ce-118">For example, the setting this property value to $(@ %SystemRoot%\\System32\\ResourceName.dll, -101) will set the property to the value of the resource text with an identifier equal to -101 in the %SystemRoot%\\System32\\ResourceName.dll file.</span></span>

## <a name="requirements"></a><span data-ttu-id="e14ce-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e14ce-119">Requirements</span></span>



| <span data-ttu-id="e14ce-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e14ce-120">Requirement</span></span> | <span data-ttu-id="e14ce-121">Wert</span><span class="sxs-lookup"><span data-stu-id="e14ce-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e14ce-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e14ce-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e14ce-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e14ce-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="e14ce-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e14ce-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e14ce-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e14ce-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e14ce-126">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="e14ce-126">End of client support</span></span><br/>    | <span data-ttu-id="e14ce-127">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e14ce-127">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="e14ce-128">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="e14ce-128">End of server support</span></span><br/>    | <span data-ttu-id="e14ce-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e14ce-129">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="e14ce-130">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="e14ce-130">Type library</span></span><br/>             | <dl> <span data-ttu-id="e14ce-131"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e14ce-131"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e14ce-132">DLL</span><span class="sxs-lookup"><span data-stu-id="e14ce-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e14ce-133"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e14ce-133"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e14ce-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e14ce-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e14ce-135">**Emailaction**</span><span class="sxs-lookup"><span data-stu-id="e14ce-135">**EmailAction**</span></span>](emailaction.md)
</dt> <dt>

[<span data-ttu-id="e14ce-136">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="e14ce-136">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

