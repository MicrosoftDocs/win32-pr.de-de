---
title: Logontype (principaltype)-Element
description: Gibt die Anmelde Methode für die Sicherheit an, die zum Ausführen der dem Prinzipal zugeordneten Tasks erforderlich ist.
ms.assetid: e36a1755-96f3-45dc-8779-8bd0cfde886c
keywords:
- Logontype-Element Taskplaner
topic_type:
- apiref
api_name:
- LogonType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4a382225f526f18731b8b9f0541e617cb31dfb4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341368"
---
# <a name="logontype-principaltype-element"></a><span data-ttu-id="d7819-104">Logontype (principaltype)-Element</span><span class="sxs-lookup"><span data-stu-id="d7819-104">LogonType (principalType) Element</span></span>

<span data-ttu-id="d7819-105">Gibt die Anmelde Methode für die Sicherheit an, die zum Ausführen der dem Prinzipal zugeordneten Tasks erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="d7819-105">Specifies the security logon method required to run those tasks associated with the principal.</span></span>

``` syntax
<xs:element name="LogonType"
    type="logonType"
 />
```

<span data-ttu-id="d7819-106">Das **logontype** -Element wird durch den komplexen Typ [**principaltype**](taskschedulerschema-principaltype-complextype.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="d7819-106">The **LogonType** element is defined by the [**principalType**](taskschedulerschema-principaltype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="d7819-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="d7819-107">Parent element</span></span>



| <span data-ttu-id="d7819-108">Element</span><span class="sxs-lookup"><span data-stu-id="d7819-108">Element</span></span>                                                                  | <span data-ttu-id="d7819-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="d7819-109">Derived from</span></span>                                                           | <span data-ttu-id="d7819-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d7819-110">Description</span></span>                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="d7819-111">**Prinzipal**</span><span class="sxs-lookup"><span data-stu-id="d7819-111">**Principal**</span></span>](taskschedulerschema-principal-principaltype-element.md) | [<span data-ttu-id="d7819-112">**principalType**</span><span class="sxs-lookup"><span data-stu-id="d7819-112">**principalType**</span></span>](taskschedulerschema-principaltype-complextype.md) | <span data-ttu-id="d7819-113">Gibt die Sicherheits Anmelde Informationen für einen Prinzipal an.</span><span class="sxs-lookup"><span data-stu-id="d7819-113">Specifies the security credentials for a principal.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="d7819-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d7819-114">Remarks</span></span>

<span data-ttu-id="d7819-115">Das **logontype** -Element und das [**UserID**](taskschedulerschema-userid-principaltype-element.md) -Element werden verwendet, um den Benutzer zu definieren, der zum Ausführen dieser Aufgaben erforderlich ist, die diesen Prinzipal verwenden.</span><span class="sxs-lookup"><span data-stu-id="d7819-115">The **LogonType** element and the [**UserId**](taskschedulerschema-userid-principaltype-element.md) element are used together to define the user required to run those tasks that use this principal.</span></span>

<span data-ttu-id="d7819-116">Bei der Skripterstellung wird der Anmeldetyp für den Prinzipal durch die Eigenschaft [**Principal. logontype**](principal-logontype.md) angegeben.</span><span class="sxs-lookup"><span data-stu-id="d7819-116">For scripting development, the logon type for the principal is specified by the [**Principal.LogonType**](principal-logontype.md) property.</span></span>

<span data-ttu-id="d7819-117">Bei der C++-Entwicklung wird der Anmeldetyp für den Prinzipal durch die [**IPrincipal:: logontype**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_logontype) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="d7819-117">For C++ development, the logon type for the principal is specified by the [**IPrincipal::LogonType**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_logontype) property.</span></span>

<span data-ttu-id="d7819-118">Dieses Element (definiert durch den einfachen Typ " [**logontype**](taskschedulerschema-logontype-simpletype.md) ") muss einen der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="d7819-118">This element (defined by the [**logonType**](taskschedulerschema-logontype-simpletype.md) simple type) must have one of the following values.</span></span>

-   <span data-ttu-id="d7819-119">S4U: der Benutzer muss sich mithilfe eines Diensts für die Benutzeranmeldung (S4U) anmelden.</span><span class="sxs-lookup"><span data-stu-id="d7819-119">S4U: User must log on using a service for user (S4U) logon.</span></span> <span data-ttu-id="d7819-120">Wenn eine S4U-Anmeldung verwendet wird, wird kein Kennwort vom System gespeichert, und es ist kein Zugriff auf das Netzwerk oder verschlüsselte Dateien vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d7819-120">When an S4U logon is used, no password is stored by the system and there is no access to the network or encrypted files.</span></span>
-   <span data-ttu-id="d7819-121">Kennwort: der Benutzer muss sich mit einem Kennwort anmelden.</span><span class="sxs-lookup"><span data-stu-id="d7819-121">Password: User must log on using a password.</span></span>
-   <span data-ttu-id="d7819-122">Interactivetoken: der Benutzer muss bereits angemeldet sein.</span><span class="sxs-lookup"><span data-stu-id="d7819-122">InteractiveToken: User must already be logged on.</span></span> <span data-ttu-id="d7819-123">Der Task wird nur in einer vorhandenen interaktiven Sitzung ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d7819-123">The task will be run only in an existing interactive session.</span></span>

<span data-ttu-id="d7819-124">Für einen Task, der eine MessageBox-Aktion enthält, wird das Meldungs Feld angezeigt, wenn die Aufgabe aktiviert ist und der Task einen interaktiven Anmeldetyp aufweist.</span><span class="sxs-lookup"><span data-stu-id="d7819-124">For a task, that contains a message box action, the message box will be displayed if the task is activated and the task has an interactive logon type.</span></span> <span data-ttu-id="d7819-125">Um den Aufgaben Anmeldetyp auf interaktiv festzulegen, geben Sie **interactivetoken** im- **<LogonType>** Element des Aufgaben Prinzipals an.</span><span class="sxs-lookup"><span data-stu-id="d7819-125">To set the task logon type to be interactive, specify **InteractiveToken** in the **<LogonType>** element of the task principal.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7819-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d7819-126">Requirements</span></span>



| <span data-ttu-id="d7819-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d7819-127">Requirement</span></span> | <span data-ttu-id="d7819-128">Wert</span><span class="sxs-lookup"><span data-stu-id="d7819-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d7819-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d7819-129">Minimum supported client</span></span><br/> | <span data-ttu-id="d7819-130">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d7819-130">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d7819-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d7819-131">Minimum supported server</span></span><br/> | <span data-ttu-id="d7819-132">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d7819-132">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d7819-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d7819-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7819-134">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="d7819-134">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





