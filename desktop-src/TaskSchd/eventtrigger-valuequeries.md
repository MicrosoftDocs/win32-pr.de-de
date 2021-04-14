---
title: EventTrigger. valuequeries (Eigenschaft)
description: Ruft bei der Skripterstellung eine Auflistung von benannten XPath-Abfragen ab oder legt diese fest. Jede Abfrage in der Auflistung wird auf das letzte übereinstimmende Ereignis-XML angewendet, das von der Abonnement Abfrage zurückgegeben wird, die in der Abonnement-Eigenschaft angegeben ist.
ms.assetid: 9ff92b66-f63c-4736-b086-df7dd8cd2b10
keywords:
- Valuequeries-Eigenschaft Taskplaner
- Valuequeries-Eigenschaft Taskplaner, EventTrigger-Objekt
- EventTrigger-Objekt Taskplaner, valuequeries-Eigenschaft
topic_type:
- apiref
api_name:
- EventTrigger.ValueQueries
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd2061f9d910e67855cc0dcb6d64248067fcb9e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518509"
---
# <a name="eventtriggervaluequeries-property"></a><span data-ttu-id="6f6e2-107">EventTrigger. valuequeries (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="6f6e2-107">EventTrigger.ValueQueries property</span></span>

<span data-ttu-id="6f6e2-108">Ruft bei der Skripterstellung eine Auflistung von benannten XPath-Abfragen ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="6f6e2-108">For scripting, gets or sets a collection of named XPath queries.</span></span> <span data-ttu-id="6f6e2-109">Jede Abfrage in der Auflistung wird auf das letzte übereinstimmende Ereignis-XML angewendet, das von der Abonnement Abfrage zurückgegeben wird, die in der [**Abonnement**](eventtrigger-subscription.md) -Eigenschaft angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="6f6e2-109">Each query in the collection is applied to the last matching event XML that is returned from the subscription query specified in the [**Subscription**](eventtrigger-subscription.md) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f6e2-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="6f6e2-110">Syntax</span></span>


```VB
EventTrigger.ValueQueries As String
```



## <a name="property-value"></a><span data-ttu-id="6f6e2-111">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="6f6e2-111">Property value</span></span>

<span data-ttu-id="6f6e2-112">Eine Auflistung von Name-Wert-Paaren.</span><span class="sxs-lookup"><span data-stu-id="6f6e2-112">A collection of of name-value pairs.</span></span> <span data-ttu-id="6f6e2-113">Jedes Name/Wert-Paar in der Auflistung definiert einen eindeutigen Namen für einen Eigenschafts Wert des Ereignisses, das den Ereignis Trigger auslöst.</span><span class="sxs-lookup"><span data-stu-id="6f6e2-113">Each name-value pair in the collection defines a unique name for a property value of the event that triggers the event trigger.</span></span> <span data-ttu-id="6f6e2-114">Der Eigenschafts Wert des Ereignisses wird als XPath-Ereignis Abfrage definiert.</span><span class="sxs-lookup"><span data-stu-id="6f6e2-114">The property value of the event is defined as an XPath event query.</span></span> <span data-ttu-id="6f6e2-115">Weitere Informationen zu XPath-Ereignis Abfragen finden Sie unter [Ereignis Auswahl](/previous-versions//aa385231(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6f6e2-115">For more information about XPath event queries, see [Event Selection](/previous-versions//aa385231(v=vs.85)).</span></span>

## <a name="remarks"></a><span data-ttu-id="6f6e2-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6f6e2-116">Remarks</span></span>

<span data-ttu-id="6f6e2-117">Der Name der Abfrage kann in den folgenden Aktions Eigenschaften als Variable verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="6f6e2-117">The name of the query can be used as a variable in the following action properties:</span></span>

-   [<span data-ttu-id="6f6e2-118">**Showmessageaction. MessageBody**</span><span class="sxs-lookup"><span data-stu-id="6f6e2-118">**ShowMessageAction.MessageBody**</span></span>](showmessageaction-messagebody.md)
-   [<span data-ttu-id="6f6e2-119">**Showmessageaction. Title**</span><span class="sxs-lookup"><span data-stu-id="6f6e2-119">**ShowMessageAction.Title**</span></span>](showmessageaction-title.md)
-   [<span data-ttu-id="6f6e2-120">**Execaction. Arguments**</span><span class="sxs-lookup"><span data-stu-id="6f6e2-120">**ExecAction.Arguments**</span></span>](execaction-arguments.md)
-   [<span data-ttu-id="6f6e2-121">**Execaction. WorkingDirectory**</span><span class="sxs-lookup"><span data-stu-id="6f6e2-121">**ExecAction.WorkingDirectory**</span></span>](execaction-workingdirectory.md)
-   [<span data-ttu-id="6f6e2-122">**Emailaction. Server**</span><span class="sxs-lookup"><span data-stu-id="6f6e2-122">**EmailAction.Server**</span></span>](emailaction-server.md)
-   [<span data-ttu-id="6f6e2-123">**Emailaction. Subject**</span><span class="sxs-lookup"><span data-stu-id="6f6e2-123">**EmailAction.Subject**</span></span>](emailaction-subject.md)
-   [<span data-ttu-id="6f6e2-124">**EmailAction.To**</span><span class="sxs-lookup"><span data-stu-id="6f6e2-124">**EmailAction.To**</span></span>](emailaction-to.md)
-   [<span data-ttu-id="6f6e2-125">**EmailAction.Cc**</span><span class="sxs-lookup"><span data-stu-id="6f6e2-125">**EmailAction.Cc**</span></span>](emailaction-cc.md)
-   [<span data-ttu-id="6f6e2-126">**Emailaction. BCC**</span><span class="sxs-lookup"><span data-stu-id="6f6e2-126">**EmailAction.Bcc**</span></span>](emailaction-bcc.md)
-   [<span data-ttu-id="6f6e2-127">**Emailaction. ReplyTo**</span><span class="sxs-lookup"><span data-stu-id="6f6e2-127">**EmailAction.ReplyTo**</span></span>](emailaction-replyto.md)
-   [<span data-ttu-id="6f6e2-128">**Emailaction. from**</span><span class="sxs-lookup"><span data-stu-id="6f6e2-128">**EmailAction.From**</span></span>](emailaction-from.md)
-   [<span data-ttu-id="6f6e2-129">**Emailaction. Body**</span><span class="sxs-lookup"><span data-stu-id="6f6e2-129">**EmailAction.Body**</span></span>](emailaction-body.md)
-   [<span data-ttu-id="6f6e2-130">**Comhandleraction. Data**</span><span class="sxs-lookup"><span data-stu-id="6f6e2-130">**ComHandlerAction.Data**</span></span>](comhandleraction-data.md)

<span data-ttu-id="6f6e2-131">In den folgenden Codebeispiel Zeichenfolgen werden zwei Name-Wert-Paare angezeigt, die in einer Name/Wert-Auflistung verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="6f6e2-131">The following code example strings show two name value pairs that can be used in a name-value collection.</span></span> <span data-ttu-id="6f6e2-132">Die von den XPath-Abfragen zurückgegebenen Werte können Variablen in der-Eigenschaft einer Aktion ersetzen.</span><span class="sxs-lookup"><span data-stu-id="6f6e2-132">The values returned by the XPath queries can replace variables in an action's property.</span></span> <span data-ttu-id="6f6e2-133">Auf die Werte wird anhand des Namens mit `$(user)` und `$(machine)` in der Action-Eigenschaft verwiesen.</span><span class="sxs-lookup"><span data-stu-id="6f6e2-133">The values are referenced by name, with `$(user)` and `$(machine)`, in the action property.</span></span> <span data-ttu-id="6f6e2-134">Wenn beispielsweise die `$(user)` Variablen und `$(machine)` in der Zeichenfolge [**showmessageaction. MessageBody**](showmessageaction-messagebody.md) verwendet werden, ersetzt der Wert der XPath-Abfragen die Variablen in der Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="6f6e2-134">For example, if the `$(user)` and `$(machine)` variables are used in the [**ShowMessageAction.MessageBody**](showmessageaction-messagebody.md) string, then the value of the XPath queries will replace the variables in the string.</span></span>

``` syntax
name: user
value: Event/UserData/SubjectUserName

name: machine
value: Event/UserData/MachineName
```

<span data-ttu-id="6f6e2-135">Weitere Informationen zum Schreiben einer Abfrage Zeichenfolge für bestimmte Ereignisse finden Sie unter [Ereignis Auswahl](/previous-versions//aa385231(v=vs.85)) und [Abonnieren von Ereignissen](../wes/subscribing-to-events.md).</span><span class="sxs-lookup"><span data-stu-id="6f6e2-135">For more information about writing a query string for certain events, see [Event Selection](/previous-versions//aa385231(v=vs.85)) and [Subscribing to Events](../wes/subscribing-to-events.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6f6e2-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6f6e2-136">Requirements</span></span>



| <span data-ttu-id="6f6e2-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6f6e2-137">Requirement</span></span> | <span data-ttu-id="6f6e2-138">Wert</span><span class="sxs-lookup"><span data-stu-id="6f6e2-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f6e2-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6f6e2-139">Minimum supported client</span></span><br/> | <span data-ttu-id="6f6e2-140">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6f6e2-140">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="6f6e2-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6f6e2-141">Minimum supported server</span></span><br/> | <span data-ttu-id="6f6e2-142">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6f6e2-142">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6f6e2-143">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="6f6e2-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="6f6e2-144"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6f6e2-144"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6f6e2-145">DLL</span><span class="sxs-lookup"><span data-stu-id="6f6e2-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f6e2-146"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f6e2-146"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f6e2-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6f6e2-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f6e2-148">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="6f6e2-148">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="6f6e2-149">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="6f6e2-149">**EventTrigger**</span></span>](eventtrigger.md)
</dt> </dl>

 

