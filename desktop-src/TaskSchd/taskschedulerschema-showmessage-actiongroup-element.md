---
title: ShowMessage-Element (Aktionsgruppe)
description: Stellt eine Aktion dar, die ein Meldungs Feld anzeigt.
ms.assetid: 33c6e437-b993-4b5e-b75a-fb3fda9b24df
keywords:
- ShowMessage-Element Taskplaner
topic_type:
- apiref
api_name:
- ShowMessage
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a1344aadfa5fe67e411048bac2a83330ea704c50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340497"
---
# <a name="showmessage-actiongroup-element"></a><span data-ttu-id="85b88-104">ShowMessage-Element (Aktionsgruppe)</span><span class="sxs-lookup"><span data-stu-id="85b88-104">ShowMessage (actionGroup) Element</span></span>

<span data-ttu-id="85b88-105">Stellt eine Aktion dar, die ein Meldungs Feld anzeigt.</span><span class="sxs-lookup"><span data-stu-id="85b88-105">Represents an action that shows a message box.</span></span>

``` syntax
<xs:element name="ShowMessage"
    type="showMessageType"
 />
```

<span data-ttu-id="85b88-106">Das **ShowMessage** -Element wird von der [**Aktionsgruppe**](taskschedulerschema-actiongroup-group.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="85b88-106">The **ShowMessage** element is defined by the [**actionGroup**](taskschedulerschema-actiongroup-group.md) .</span></span>

## <a name="parent-element"></a><span data-ttu-id="85b88-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="85b88-107">Parent element</span></span>



| <span data-ttu-id="85b88-108">Element</span><span class="sxs-lookup"><span data-stu-id="85b88-108">Element</span></span>                                                                    | <span data-ttu-id="85b88-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="85b88-109">Derived from</span></span>                                                       | <span data-ttu-id="85b88-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="85b88-110">Description</span></span>                                            |
|----------------------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="85b88-111">**Aktionen (TaskType)**</span><span class="sxs-lookup"><span data-stu-id="85b88-111">**Actions (taskType)**</span></span>](taskschedulerschema-actions-tasktype-element.md) | [<span data-ttu-id="85b88-112">**Aktions sType**</span><span class="sxs-lookup"><span data-stu-id="85b88-112">**actionsType**</span></span>](taskschedulerschema-actionstype-complextype.md) | <span data-ttu-id="85b88-113">Enthält die Aktionen, die vom Task ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="85b88-113">Contains the actions performed by the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="85b88-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="85b88-114">Child elements</span></span>



| <span data-ttu-id="85b88-115">Element</span><span class="sxs-lookup"><span data-stu-id="85b88-115">Element</span></span>                                                            | <span data-ttu-id="85b88-116">type</span><span class="sxs-lookup"><span data-stu-id="85b88-116">Type</span></span>           | <span data-ttu-id="85b88-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="85b88-117">Description</span></span>                                                               |
|--------------------------------------------------------------------|----------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="85b88-118">**Text**</span><span class="sxs-lookup"><span data-stu-id="85b88-118">**Body**</span></span>](taskschedulerschema-body-showmessagetype-element.md)   | <span data-ttu-id="85b88-119">nonEmptyString</span><span class="sxs-lookup"><span data-stu-id="85b88-119">nonEmptyString</span></span> | <span data-ttu-id="85b88-120">Gibt den Text an, der im Textkörper des Meldungs Felds angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="85b88-120">Specifies the text to display in the body of the message box.</span></span> <br/> |
| [<span data-ttu-id="85b88-121">**Titel**</span><span class="sxs-lookup"><span data-stu-id="85b88-121">**Title**</span></span>](taskschedulerschema-title-showmessagetype-element.md) | <span data-ttu-id="85b88-122">nonEmptyString</span><span class="sxs-lookup"><span data-stu-id="85b88-122">nonEmptyString</span></span> | <span data-ttu-id="85b88-123">Gibt den Titel des Meldungs Felds an.</span><span class="sxs-lookup"><span data-stu-id="85b88-123">Specifies the title of the message box.</span></span> <br/>                       |



## <a name="remarks"></a><span data-ttu-id="85b88-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="85b88-124">Remarks</span></span>

<span data-ttu-id="85b88-125">Bei der Skripterstellung wird eine MessageBox-Aktion mithilfe des [**showmessageaction**](showmessageaction.md) -Objekts angegeben.</span><span class="sxs-lookup"><span data-stu-id="85b88-125">For scripting development, a message box action is specified using the [**ShowMessageAction**](showmessageaction.md) object.</span></span>

<span data-ttu-id="85b88-126">Bei der C++-Entwicklung wird eine MessageBox-Aktion mithilfe der [**ishowmessageaction**](/windows/desktop/api/taskschd/nn-taskschd-ishowmessageaction) -Schnittstelle angegeben.</span><span class="sxs-lookup"><span data-stu-id="85b88-126">For C++ development, a message box action is specified using the [**IShowMessageAction**](/windows/desktop/api/taskschd/nn-taskschd-ishowmessageaction) interface.</span></span>

<span data-ttu-id="85b88-127">**Windows 8 und Windows Server 2012:** Dieses Element wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="85b88-127">**Windows 8 and Windows Server 2012:** This element has been removed.</span></span> <span data-ttu-id="85b88-128">Sie können IExecAction mit der Windows Scripting [**MsgBox-Funktion**](/previous-versions/sfw6660x(v=vs.80)) verwenden, um eine Meldung in der Benutzersitzung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="85b88-128">You can use IExecAction with the Windows scripting [**MsgBox function**](/previous-versions/sfw6660x(v=vs.80)) to show a message in the user session.</span></span>

## <a name="examples"></a><span data-ttu-id="85b88-129">Beispiele</span><span class="sxs-lookup"><span data-stu-id="85b88-129">Examples</span></span>

<span data-ttu-id="85b88-130">Ein umfassendes Beispiel für den XML-Code für eine Aufgabe, die eine Meldungs Feld Aktion verwendet, finden Sie unter [Message Box example (XML)](/previous-versions//aa381917(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="85b88-130">For a complete example of the XML for a task that uses a message box action, see [Message Box Example (XML)](/previous-versions//aa381917(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="85b88-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="85b88-131">Requirements</span></span>



| <span data-ttu-id="85b88-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="85b88-132">Requirement</span></span> | <span data-ttu-id="85b88-133">Wert</span><span class="sxs-lookup"><span data-stu-id="85b88-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="85b88-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="85b88-134">Minimum supported client</span></span><br/> | <span data-ttu-id="85b88-135">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="85b88-135">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="85b88-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="85b88-136">Minimum supported server</span></span><br/> | <span data-ttu-id="85b88-137">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="85b88-137">Windows Server 2008 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="85b88-138">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="85b88-138">End of client support</span></span><br/>    | <span data-ttu-id="85b88-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="85b88-139">Windows 7</span></span><br/>                                 |
| <span data-ttu-id="85b88-140">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="85b88-140">End of server support</span></span><br/>    | <span data-ttu-id="85b88-141">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="85b88-141">Windows Server 2008 R2</span></span><br/>                    |



 

