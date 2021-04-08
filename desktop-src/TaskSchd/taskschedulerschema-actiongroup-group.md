---
title: Gruppe "Gruppe"
description: Definiert die Gruppe von Aktionen, die von einer Aufgabe durchgeführt werden können.
ms.assetid: a43ba021-4a40-4e2c-a57f-bd6ee17706ba
keywords:
- Gruppe "Aktionsgruppe" Taskplaner
- Aktionsgruppen Taskplaner
topic_type:
- apiref
api_name:
- actionGroup
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: af06598c6eca092f474467bea16a7d7b95a9563f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740833"
---
# <a name="actiongroup-group"></a><span data-ttu-id="af98a-105">Gruppe "Gruppe"</span><span class="sxs-lookup"><span data-stu-id="af98a-105">actionGroup Group</span></span>

<span data-ttu-id="af98a-106">Definiert die Gruppe von Aktionen, die von einer Aufgabe durchgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="af98a-106">Defines the group of actions that a task can perform.</span></span>

``` syntax
<xs:group name="actionGroup">
    <xs:choice>
        <xs:element name="Exec"
            type="execType"
         />
        <xs:element name="ComHandler"
            type="comHandlerType"
         />
        <xs:element name="SendEmail"
            type="sendEmailType"
         />
        <xs:element name="ShowMessage"
            type="showMessageType"
         />
    </xs:choice>
</xs:group>
```

## <a name="child-elements"></a><span data-ttu-id="af98a-107">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="af98a-107">Child elements</span></span>



| <span data-ttu-id="af98a-108">Element</span><span class="sxs-lookup"><span data-stu-id="af98a-108">Element</span></span>                                                                    | <span data-ttu-id="af98a-109">type</span><span class="sxs-lookup"><span data-stu-id="af98a-109">Type</span></span>                                                                       | <span data-ttu-id="af98a-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="af98a-110">Description</span></span>                                                             |
|----------------------------------------------------------------------------|----------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="af98a-111">**Comhandler**</span><span class="sxs-lookup"><span data-stu-id="af98a-111">**ComHandler**</span></span>](taskschedulerschema-comhandler-actiongroup-element.md)   | [<span data-ttu-id="af98a-112">**comhandlertype**</span><span class="sxs-lookup"><span data-stu-id="af98a-112">**comHandlerType**</span></span>](taskschedulerschema-comhandlertype-complextype.md)   | <span data-ttu-id="af98a-113">Stellt eine Aktion dar, die einen Handler auslöst.</span><span class="sxs-lookup"><span data-stu-id="af98a-113">Represents an action that fires a handler.</span></span><br/>                   |
| [<span data-ttu-id="af98a-114">**Exec**</span><span class="sxs-lookup"><span data-stu-id="af98a-114">**Exec**</span></span>](taskschedulerschema-exec-actiongroup-element.md)               | [<span data-ttu-id="af98a-115">**exectype**</span><span class="sxs-lookup"><span data-stu-id="af98a-115">**execType**</span></span>](taskschedulerschema-exectype-complextype.md)               | <span data-ttu-id="af98a-116">Stellt eine Aktion dar, die einen Befehlszeilen Vorgang ausführt.</span><span class="sxs-lookup"><span data-stu-id="af98a-116">Represents an action that executes a command-line operation.</span></span><br/> |
| [<span data-ttu-id="af98a-117">**SendEmail**</span><span class="sxs-lookup"><span data-stu-id="af98a-117">**SendEmail**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md)     | [<span data-ttu-id="af98a-118">**sendemailtype**</span><span class="sxs-lookup"><span data-stu-id="af98a-118">**sendEmailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md)     | <span data-ttu-id="af98a-119">Stellt eine Aktion dar, die eine e-Mail-Nachricht sendet.</span><span class="sxs-lookup"><span data-stu-id="af98a-119">Represents an action that sends an email message.</span></span><br/>            |
| [<span data-ttu-id="af98a-120">**ShowMessage**</span><span class="sxs-lookup"><span data-stu-id="af98a-120">**ShowMessage**</span></span>](taskschedulerschema-showmessage-actiongroup-element.md) | [<span data-ttu-id="af98a-121">**showmessagetype**</span><span class="sxs-lookup"><span data-stu-id="af98a-121">**showMessageType**</span></span>](taskschedulerschema-showmessagetype-complextype.md) | <span data-ttu-id="af98a-122">Stellt eine Aktion dar, die ein Meldungs Feld anzeigt.</span><span class="sxs-lookup"><span data-stu-id="af98a-122">Represents an action that shows a message box.</span></span><br/>               |



## <a name="remarks"></a><span data-ttu-id="af98a-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="af98a-123">Remarks</span></span>

<span data-ttu-id="af98a-124">Beim Lesen oder Schreiben von XML sind die Elemente, die von dieser Gruppe definiert werden, die untergeordneten Elemente des [**Actions**](taskschedulerschema-actions-tasktype-element.md) -Elements.</span><span class="sxs-lookup"><span data-stu-id="af98a-124">When reading or writing XML, the elements that are defined by this group are the child elements of the [**Actions**](taskschedulerschema-actions-tasktype-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="af98a-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="af98a-125">Requirements</span></span>



| <span data-ttu-id="af98a-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="af98a-126">Requirement</span></span> | <span data-ttu-id="af98a-127">Wert</span><span class="sxs-lookup"><span data-stu-id="af98a-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="af98a-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="af98a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="af98a-129">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="af98a-129">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="af98a-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="af98a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="af98a-131">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="af98a-131">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="af98a-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="af98a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af98a-133">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="af98a-133">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





