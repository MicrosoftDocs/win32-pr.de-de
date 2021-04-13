---
title: Aktioncollection. Create-Methode
description: Bei der Skripterstellung wird von eine neue Aktion erstellt und der Auflistung hinzugefügt.
ms.assetid: f33542e1-ee49-4696-b2ab-c48a9b5440d4
keywords:
- Create-Methode Taskplaner
- Create Method Taskplaner, Aktions Sammlungsobjekt
- Aktions Sammlungsobjekt Taskplaner, Create-Methode
topic_type:
- apiref
api_name:
- ActionCollection.Create
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50ec2ede228a27e753316860ac44e604d39e2e4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518233"
---
# <a name="actioncollectioncreate-method"></a><span data-ttu-id="c7c0d-106">Aktioncollection. Create-Methode</span><span class="sxs-lookup"><span data-stu-id="c7c0d-106">ActionCollection.Create method</span></span>

<span data-ttu-id="c7c0d-107">Bei der Skripterstellung wird von eine neue Aktion erstellt und der Auflistung hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c7c0d-107">For scripting, creates and adds a new action to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7c0d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c7c0d-108">Syntax</span></span>


```VB
ActionCollection.Create( _
  ByVal type _
)
```



## <a name="parameters"></a><span data-ttu-id="c7c0d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c7c0d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7c0d-110">*Typ* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c7c0d-110">*type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7c0d-111">Dieser Parameter ist auf eine der folgenden [**\_ \_ Aufgabentyp**](/windows/desktop/api/taskschd/ne-taskschd-task_action_type) -Enumerationskonstanten für Aufgaben festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c7c0d-111">This parameter is set to one of the following [**TASK\_ACTION\_TYPE**](/windows/desktop/api/taskschd/ne-taskschd-task_action_type) enumeration constants.</span></span>



| <span data-ttu-id="c7c0d-112">Wert</span><span class="sxs-lookup"><span data-stu-id="c7c0d-112">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="c7c0d-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c7c0d-113">Meaning</span></span>                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_ACTION_EXEC"></span><span id="task_action_exec"></span><dl> <span data-ttu-id="c7c0d-114"><dt>**Aufgabe \_ Aktion \_ exec**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c7c0d-114"><dt>**TASK\_ACTION\_EXEC**</dt> <dt>0</dt></span></span> </dl>                          | <span data-ttu-id="c7c0d-115">Die Aktion führt einen Befehlszeilen Vorgang aus.</span><span class="sxs-lookup"><span data-stu-id="c7c0d-115">The action performs a command-line operation.</span></span> <span data-ttu-id="c7c0d-116">Beispielsweise könnte die Aktion ein Skript ausführen, eine ausführbare Datei starten oder, wenn der Name eines Dokuments bereitgestellt wird, die zugehörige Anwendung suchen und die Anwendung mit dem Dokument starten.</span><span class="sxs-lookup"><span data-stu-id="c7c0d-116">For example, the action could run a script, launch an executable, or, if the name of a document is provided, find its associated application and launch the application with the document.</span></span><br/> |
| <span id="TASK_ACTION_COM_HANDLER"></span><span id="task_action_com_handler"></span><dl> <span data-ttu-id="c7c0d-117"><dt>**Aufgabe \_ Aktions- \_ com- \_ Handler**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="c7c0d-117"><dt>**TASK\_ACTION\_COM\_HANDLER**</dt> <dt>5</dt></span></span> </dl>    | <span data-ttu-id="c7c0d-118">Die Aktion löst einen Handler aus.</span><span class="sxs-lookup"><span data-stu-id="c7c0d-118">The action fires a handler.</span></span><br/>                                                                                                                                                                                                              |
| <span id="TASK_ACTION_SEND_EMAIL"></span><span id="task_action_send_email"></span><dl> <span data-ttu-id="c7c0d-119"><dt>**Aufgabe \_ Aktion \_ \_ e-Mail senden**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="c7c0d-119"><dt>**TASK\_ACTION\_SEND\_EMAIL**</dt> <dt>6</dt></span></span> </dl>       | <span data-ttu-id="c7c0d-120">Diese Aktion sendet eine e-Mail-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="c7c0d-120">This action sends email message.</span></span><br/>                                                                                                                                                                                                         |
| <span id="TASK_ACTION_SHOW_MESSAGE"></span><span id="task_action_show_message"></span><dl> <span data-ttu-id="c7c0d-121"><dt>**Aufgabe \_ Aktion \_ zeigt \_ Meldung**</dt> <dt>7</dt> an</span><span class="sxs-lookup"><span data-stu-id="c7c0d-121"><dt>**TASK\_ACTION\_SHOW\_MESSAGE**</dt> <dt>7</dt></span></span> </dl> | <span data-ttu-id="c7c0d-122">Diese Aktion zeigt ein Meldungs Feld an.</span><span class="sxs-lookup"><span data-stu-id="c7c0d-122">This action shows a message box.</span></span><br/>                                                                                                                                                                                                         |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7c0d-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c7c0d-123">Return value</span></span>

<span data-ttu-id="c7c0d-124">Ein [**Aktions**](action.md) Objekt, das die neue Aktion darstellt.</span><span class="sxs-lookup"><span data-stu-id="c7c0d-124">An [**Action**](action.md) object that represents the new action.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7c0d-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c7c0d-125">Remarks</span></span>

<span data-ttu-id="c7c0d-126">Der Sammlung können nicht mehr als 32 Aktionen hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="c7c0d-126">You cannot add more than 32 actions to the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7c0d-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c7c0d-127">Requirements</span></span>



| <span data-ttu-id="c7c0d-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c7c0d-128">Requirement</span></span> | <span data-ttu-id="c7c0d-129">Wert</span><span class="sxs-lookup"><span data-stu-id="c7c0d-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c7c0d-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c7c0d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="c7c0d-131">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c7c0d-131">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="c7c0d-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c7c0d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="c7c0d-133">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c7c0d-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c7c0d-134">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="c7c0d-134">Type library</span></span><br/>             | <dl> <span data-ttu-id="c7c0d-135"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c7c0d-135"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c7c0d-136">DLL</span><span class="sxs-lookup"><span data-stu-id="c7c0d-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7c0d-137"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7c0d-137"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7c0d-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c7c0d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7c0d-139">**Task \_ \_ Aktionstyp**</span><span class="sxs-lookup"><span data-stu-id="c7c0d-139">**TASK\_ACTION\_TYPE**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_action_type)
</dt> <dt>

[<span data-ttu-id="c7c0d-140">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="c7c0d-140">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="c7c0d-141">**ActionCollection**</span><span class="sxs-lookup"><span data-stu-id="c7c0d-141">**ActionCollection**</span></span>](actioncollection.md)
</dt> <dt>

[<span data-ttu-id="c7c0d-142">**Aktion**</span><span class="sxs-lookup"><span data-stu-id="c7c0d-142">**Action**</span></span>](action.md)
</dt> <dt>

[<span data-ttu-id="c7c0d-143">**Execaction**</span><span class="sxs-lookup"><span data-stu-id="c7c0d-143">**ExecAction**</span></span>](execaction.md)
</dt> <dt>

[<span data-ttu-id="c7c0d-144">**Emailaction**</span><span class="sxs-lookup"><span data-stu-id="c7c0d-144">**EmailAction**</span></span>](emailaction.md)
</dt> <dt>

[<span data-ttu-id="c7c0d-145">**Showmessageaction**</span><span class="sxs-lookup"><span data-stu-id="c7c0d-145">**ShowMessageAction**</span></span>](showmessageaction.md)
</dt> <dt>

[<span data-ttu-id="c7c0d-146">**Comhandleraction**</span><span class="sxs-lookup"><span data-stu-id="c7c0d-146">**ComHandlerAction**</span></span>](comhandleraction.md)
</dt> </dl>

 

 





