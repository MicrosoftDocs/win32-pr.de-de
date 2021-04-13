---
title: Showmessageaction-Objekt
description: Stellt bei der Skripterstellung eine Aktion dar, die ein Meldungs Feld anzeigt, wenn eine Aufgabe aktiviert wird.
ms.assetid: fdd22eef-965c-4a81-954c-66011c435ab9
keywords:
- Showmessageaction-Objekt Taskplaner
- Showmessageaction-Objekt Taskplaner, beschrieben
topic_type:
- apiref
api_name:
- ShowMessageAction
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef1e500f0492ad010e88719a467fda38f85e184c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391698"
---
# <a name="showmessageaction-object"></a><span data-ttu-id="b1fbc-105">Showmessageaction-Objekt</span><span class="sxs-lookup"><span data-stu-id="b1fbc-105">ShowMessageAction object</span></span>

<span data-ttu-id="b1fbc-106">\[Dieses Objekt wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b1fbc-106">\[This object is no longer supported.</span></span> <span data-ttu-id="b1fbc-107">Sie können IExecAction mit der Windows Scripting [**MsgBox-Funktion**](/previous-versions/sfw6660x(v=vs.80)) verwenden, um eine Meldung in der Benutzersitzung anzuzeigen.\]</span><span class="sxs-lookup"><span data-stu-id="b1fbc-107">You can use IExecAction with the Windows scripting [**MsgBox function**](/previous-versions/sfw6660x(v=vs.80)) to show a message in the user session.\]</span></span>

<span data-ttu-id="b1fbc-108">Stellt bei der Skripterstellung eine Aktion dar, die ein Meldungs Feld anzeigt, wenn eine Aufgabe aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="b1fbc-108">For scripting, represents an action that shows a message box when a task is activated.</span></span>

## <a name="members"></a><span data-ttu-id="b1fbc-109">Member</span><span class="sxs-lookup"><span data-stu-id="b1fbc-109">Members</span></span>

<span data-ttu-id="b1fbc-110">Das **showmessageaction** -Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="b1fbc-110">The **ShowMessageAction** object has these types of members:</span></span>

-   [<span data-ttu-id="b1fbc-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b1fbc-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b1fbc-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b1fbc-112">Properties</span></span>

<span data-ttu-id="b1fbc-113">Das **showmessageaction** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b1fbc-113">The **ShowMessageAction** object has these properties.</span></span>



| <span data-ttu-id="b1fbc-114">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b1fbc-114">Property</span></span>                                                        | <span data-ttu-id="b1fbc-115">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="b1fbc-115">Access type</span></span>           | <span data-ttu-id="b1fbc-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b1fbc-116">Description</span></span>                                                                                               |
|:----------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b1fbc-117">**Name**</span><span class="sxs-lookup"><span data-stu-id="b1fbc-117">**Id**</span></span>](action-id.md)<br/>                              | <span data-ttu-id="b1fbc-118">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b1fbc-118">Read/write</span></span><br/> | <span data-ttu-id="b1fbc-119">Wird vom [**Action**](action.md) -Objekt geerbt.</span><span class="sxs-lookup"><span data-stu-id="b1fbc-119">Inherited from the [**Action**](action.md) object.</span></span> <span data-ttu-id="b1fbc-120">Ruft den Bezeichner der Aktion ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="b1fbc-120">Gets or sets the identifier of the action.</span></span><br/> |
| [<span data-ttu-id="b1fbc-121">**MessageBody**</span><span class="sxs-lookup"><span data-stu-id="b1fbc-121">**MessageBody**</span></span>](showmessageaction-messagebody.md)<br/> | <span data-ttu-id="b1fbc-122">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b1fbc-122">Read/write</span></span><br/> | <span data-ttu-id="b1fbc-123">Ruft den Meldungs Text ab, der im Textkörper des Meldungs Felds angezeigt wird, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="b1fbc-123">Gets or sets the message text that is displayed in the body of the message box.</span></span><br/>                |
| [<span data-ttu-id="b1fbc-124">**Titel**</span><span class="sxs-lookup"><span data-stu-id="b1fbc-124">**Title**</span></span>](showmessageaction-title.md)<br/>             | <span data-ttu-id="b1fbc-125">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b1fbc-125">Read/write</span></span><br/> | <span data-ttu-id="b1fbc-126">Ruft den Titel des Meldungs Felds ab oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="b1fbc-126">Gets or sets the title of the message box.</span></span><br/>                                                     |
| [<span data-ttu-id="b1fbc-127">**type**</span><span class="sxs-lookup"><span data-stu-id="b1fbc-127">**Type**</span></span>](action-type.md)<br/>                          | <span data-ttu-id="b1fbc-128">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b1fbc-128">Read-only</span></span><br/>  | <span data-ttu-id="b1fbc-129">Wird vom [**Action**](action.md) -Objekt geerbt.</span><span class="sxs-lookup"><span data-stu-id="b1fbc-129">Inherited from the [**Action**](action.md) object.</span></span> <span data-ttu-id="b1fbc-130">Ruft den Typ der Aktion ab.</span><span class="sxs-lookup"><span data-stu-id="b1fbc-130">Gets the type of the action.</span></span><br/>               |



 

## <a name="remarks"></a><span data-ttu-id="b1fbc-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b1fbc-131">Remarks</span></span>

<span data-ttu-id="b1fbc-132">Für einen Task, der eine MessageBox-Aktion enthält, wird das Meldungs Feld angezeigt, wenn die Aufgabe aktiviert ist und der Task einen interaktiven Anmeldetyp aufweist.</span><span class="sxs-lookup"><span data-stu-id="b1fbc-132">For a task, that contains a message box action, the message box will be displayed if the task is activated and the task has an interactive logon type.</span></span> <span data-ttu-id="b1fbc-133">Wenn Sie den Anmeldetyp für die Aufgabe interaktiv festlegen möchten, geben Sie in der [**logontype**](principal-logontype.md) -Eigenschaft des Task Prinzipals oder im *logontype* -Parameter von [**taskfolder. RegisterTask**](taskfolder-registertask.md) oder [**taskfolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md)den Wert 3 an.**\_ \_ \_\*\*\*\*\_ \_**</span><span class="sxs-lookup"><span data-stu-id="b1fbc-133">To set the task logon type to interactive, specify 3 (**TASK\_LOGON\_INTERACTIVE\_TOKEN**) or 4 (**TASK\_LOGON\_GROUP**) in the [**LogonType**](principal-logontype.md) property of the task principal, or in the *logonType* parameter of [**TaskFolder.RegisterTask**](taskfolder-registertask.md) or [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md).</span></span>

<span data-ttu-id="b1fbc-134">Beim Lesen oder schreiben Ihrer eigenen XML-Daten für eine Aufgabe wird eine Meldungs Feld Aktion mit dem [**ShowMessage**](taskschedulerschema-showmessage-actiongroup-element.md) -Element des Taskplaner-Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="b1fbc-134">When reading or writing your own XML for a task, a message box action is specified using the [**ShowMessage**](taskschedulerschema-showmessage-actiongroup-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="b1fbc-135">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b1fbc-135">Examples</span></span>

<span data-ttu-id="b1fbc-136">Weitere Informationen und Beispielcode für dieses Skript Objekt finden Sie unter Beispiel für Meldungs Felder [(Skripterstellung)](/previous-versions//aa381916(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b1fbc-136">For more information and example code for this scripting object, see [Message Box Example (Scripting)](/previous-versions//aa381916(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="b1fbc-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b1fbc-137">Requirements</span></span>



| <span data-ttu-id="b1fbc-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b1fbc-138">Requirement</span></span> | <span data-ttu-id="b1fbc-139">Wert</span><span class="sxs-lookup"><span data-stu-id="b1fbc-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1fbc-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b1fbc-140">Minimum supported client</span></span><br/> | <span data-ttu-id="b1fbc-141">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b1fbc-141">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="b1fbc-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b1fbc-142">Minimum supported server</span></span><br/> | <span data-ttu-id="b1fbc-143">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b1fbc-143">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b1fbc-144">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="b1fbc-144">End of client support</span></span><br/>    | <span data-ttu-id="b1fbc-145">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b1fbc-145">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="b1fbc-146">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="b1fbc-146">End of server support</span></span><br/>    | <span data-ttu-id="b1fbc-147">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b1fbc-147">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="b1fbc-148">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="b1fbc-148">Type library</span></span><br/>             | <dl> <span data-ttu-id="b1fbc-149"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b1fbc-149"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b1fbc-150">DLL</span><span class="sxs-lookup"><span data-stu-id="b1fbc-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1fbc-151"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1fbc-151"><dt>Taskschd.dll</dt></span></span> </dl> |



 

