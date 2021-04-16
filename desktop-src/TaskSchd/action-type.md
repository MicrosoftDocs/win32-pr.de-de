---
title: Action. Type-Eigenschaft
description: Ruft bei der Skripterstellung den Typ der Aktion ab.
ms.assetid: 6a0bca3d-9016-4167-9f6e-2cc95bafdb95
keywords:
- Type-Eigenschafts Taskplaner
- Type-Eigenschafts Taskplaner, Aktions Objekt
- Aktions Objekt Taskplaner, Typeigenschaft
topic_type:
- apiref
api_name:
- Action.Type
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3db8ca46a80503136c5fbbe1240cba6c664bc1a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477811"
---
# <a name="actiontype-property"></a><span data-ttu-id="0f9f2-106">Action. Type-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="0f9f2-106">Action.Type property</span></span>

<span data-ttu-id="0f9f2-107">Ruft bei der Skripterstellung den Typ der Aktion ab.</span><span class="sxs-lookup"><span data-stu-id="0f9f2-107">For scripting, gets the type of the action.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f9f2-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0f9f2-108">Syntax</span></span>


```VB
Action.Type As Integer
```



## <a name="property-value"></a><span data-ttu-id="0f9f2-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="0f9f2-109">Property value</span></span>

<span data-ttu-id="0f9f2-110">Diese Eigenschaft gibt eine der folgenden Aufzählungstyp-Enumerationskonstanten zurück. [**\_ \_**](/windows/desktop/api/taskschd/ne-taskschd-task_action_type)</span><span class="sxs-lookup"><span data-stu-id="0f9f2-110">This property returns one of the following [**TASK\_ACTION\_TYPE**](/windows/desktop/api/taskschd/ne-taskschd-task_action_type) enumeration constants.</span></span>



| <span data-ttu-id="0f9f2-111">Wert</span><span class="sxs-lookup"><span data-stu-id="0f9f2-111">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="0f9f2-112">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="0f9f2-112">Meaning</span></span>                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_ACTION_EXEC"></span><span id="task_action_exec"></span><dl> <span data-ttu-id="0f9f2-113"><dt>**Aufgabe \_ Aktion \_ exec**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="0f9f2-113"><dt>**TASK\_ACTION\_EXEC**</dt> <dt>0</dt></span></span> </dl>                          | <span data-ttu-id="0f9f2-114">Diese Aktion führt einen Befehlszeilen Vorgang aus.</span><span class="sxs-lookup"><span data-stu-id="0f9f2-114">This action performs a command-line operation.</span></span> <span data-ttu-id="0f9f2-115">Beispielsweise könnte die Aktion ein Skript ausführen, eine ausführbare Datei starten oder, wenn der Name eines Dokuments bereitgestellt wird, die zugehörige Anwendung suchen und die Anwendung mit dem Dokument starten.</span><span class="sxs-lookup"><span data-stu-id="0f9f2-115">For example, the action could run a script, launch an executable, or, if the name of a document is provided, find its associated application and launch the application with the document.</span></span><br/> |
| <span id="TASK_ACTION_COM_HANDLER"></span><span id="task_action_com_handler"></span><dl> <span data-ttu-id="0f9f2-116"><dt>**Aufgabe \_ Aktions- \_ com- \_ Handler**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="0f9f2-116"><dt>**TASK\_ACTION\_COM\_HANDLER**</dt> <dt>5</dt></span></span> </dl>    | <span data-ttu-id="0f9f2-117">Durch diese Aktion wird ein Handler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="0f9f2-117">This action fires a handler.</span></span><br/>                                                                                                                                                                                                              |
| <span id="TASK_ACTION_SEND_EMAIL"></span><span id="task_action_send_email"></span><dl> <span data-ttu-id="0f9f2-118"><dt>**Aufgabe \_ Aktion \_ \_ e-Mail senden**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="0f9f2-118"><dt>**TASK\_ACTION\_SEND\_EMAIL**</dt> <dt>6</dt></span></span> </dl>       | <span data-ttu-id="0f9f2-119">Mit dieser Aktion wird eine e-Mail-Nachricht gesendet.</span><span class="sxs-lookup"><span data-stu-id="0f9f2-119">This action sends an email message.</span></span><br/>                                                                                                                                                                                                       |
| <span id="TASK_ACTION_SHOW_MESSAGE"></span><span id="task_action_show_message"></span><dl> <span data-ttu-id="0f9f2-120"><dt>**Aufgabe \_ Aktion \_ zeigt \_ Meldung**</dt> <dt>7</dt> an</span><span class="sxs-lookup"><span data-stu-id="0f9f2-120"><dt>**TASK\_ACTION\_SHOW\_MESSAGE**</dt> <dt>7</dt></span></span> </dl> | <span data-ttu-id="0f9f2-121">Diese Aktion zeigt ein Meldungs Feld an.</span><span class="sxs-lookup"><span data-stu-id="0f9f2-121">This action shows a message box.</span></span><br/>                                                                                                                                                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="0f9f2-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0f9f2-122">Remarks</span></span>

<span data-ttu-id="0f9f2-123">Der Aktionstyp wird definiert, wenn die Aktion erstellt wird, und kann später nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="0f9f2-123">The action type is defined when the action is created and cannot be changed later.</span></span> <span data-ttu-id="0f9f2-124">Weitere Informationen zum Erstellen einer Aktion finden Sie unter " [**Action Collection. Create**](actioncollection-create.md)".</span><span class="sxs-lookup"><span data-stu-id="0f9f2-124">For information on creating an action, see [**ActionCollection.Create**](actioncollection-create.md).</span></span>

<span data-ttu-id="0f9f2-125">Informationen zur Zusammenarbeit von Aktionen und Aufgaben finden Sie unter [Aufgaben Aktionen](task-actions.md).</span><span class="sxs-lookup"><span data-stu-id="0f9f2-125">For information on how actions and tasks work together, see [Task Actions](task-actions.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0f9f2-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0f9f2-126">Requirements</span></span>



| <span data-ttu-id="0f9f2-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0f9f2-127">Requirement</span></span> | <span data-ttu-id="0f9f2-128">Wert</span><span class="sxs-lookup"><span data-stu-id="0f9f2-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0f9f2-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0f9f2-129">Minimum supported client</span></span><br/> | <span data-ttu-id="0f9f2-130">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0f9f2-130">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="0f9f2-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0f9f2-131">Minimum supported server</span></span><br/> | <span data-ttu-id="0f9f2-132">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0f9f2-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0f9f2-133">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="0f9f2-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="0f9f2-134"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0f9f2-134"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0f9f2-135">DLL</span><span class="sxs-lookup"><span data-stu-id="0f9f2-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f9f2-136"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f9f2-136"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f9f2-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0f9f2-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f9f2-138">**Task \_ \_ Aktionstyp**</span><span class="sxs-lookup"><span data-stu-id="0f9f2-138">**TASK\_ACTION\_TYPE**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_action_type)
</dt> <dt>

[<span data-ttu-id="0f9f2-139">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="0f9f2-139">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="0f9f2-140">**Aktion**</span><span class="sxs-lookup"><span data-stu-id="0f9f2-140">**Action**</span></span>](action.md)
</dt> </dl>

 

 





