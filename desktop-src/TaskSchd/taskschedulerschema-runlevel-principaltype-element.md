---
title: Runlevel (runleveltype)-Element
description: Enthält einen Wert, der die Sicherheitskontext Ebene zum Ausführen des Tasks angibt.
ms.assetid: dc113ffa-8ac9-4dcd-a106-45295da42f46
keywords:
- Runlevel-Element Taskplaner
topic_type:
- apiref
api_name:
- RunLevel
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d374f5b9ad388f3ad0a626e1b99ecae96eeef1a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341307"
---
# <a name="runlevel-runleveltype-element"></a><span data-ttu-id="8964b-104">Runlevel (runleveltype)-Element</span><span class="sxs-lookup"><span data-stu-id="8964b-104">RunLevel (runLevelType) Element</span></span>

<span data-ttu-id="8964b-105">Enthält einen Wert, der die Sicherheitskontext Ebene zum Ausführen des Tasks angibt.</span><span class="sxs-lookup"><span data-stu-id="8964b-105">Contains a value that specifies the security context level for running the task.</span></span> <span data-ttu-id="8964b-106">Sie können angeben, dass eine Aufgabe mit den geringsten Rechten oder erhöhten Rechten ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8964b-106">You can specify to run a task using least privileges or elevated privileges.</span></span> <span data-ttu-id="8964b-107">Der Wert 0 gibt an, dass der Task mit den niedrigsten Berechtigungen ausgeführt wird, und der Wert 1 gibt an, dass der Task mit erhöhten Rechten ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8964b-107">A value of 0 specifies to run the task with lowest privileges, and a value of 1 specifies to run the task with elevated privileges.</span></span>

``` syntax
<xs:element name="RunLevel"
    type="runLevelType"
 />
```

<span data-ttu-id="8964b-108">Das **Runlevel** -Element wird durch den einfachen [**runleveltype**](taskschedulerschema-runleveltype-simpletype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="8964b-108">The **RunLevel** element is defined by the [**runLevelType**](taskschedulerschema-runleveltype-simpletype.md) simple type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="8964b-109">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="8964b-109">Parent element</span></span>



| <span data-ttu-id="8964b-110">Element</span><span class="sxs-lookup"><span data-stu-id="8964b-110">Element</span></span>                                                                                  | <span data-ttu-id="8964b-111">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="8964b-111">Derived from</span></span>                                                           | <span data-ttu-id="8964b-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8964b-112">Description</span></span>                                                                                                                           |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8964b-113">**Prinzipal (principaltype)**</span><span class="sxs-lookup"><span data-stu-id="8964b-113">**Principal (principalType)**</span></span>](taskschedulerschema-principal-principaltype-element.md) | [<span data-ttu-id="8964b-114">**principalType**</span><span class="sxs-lookup"><span data-stu-id="8964b-114">**principalType**</span></span>](taskschedulerschema-principaltype-complextype.md) | <span data-ttu-id="8964b-115">Gibt die Sicherheits Anmelde Informationen für einen Prinzipal an.</span><span class="sxs-lookup"><span data-stu-id="8964b-115">Specifies the security credentials for a principal.</span></span> <span data-ttu-id="8964b-116">Mit diesen Anmelde Informationen wird der Sicherheitskontext definiert, unter dem eine Aufgabe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8964b-116">These credentials define the security context that a task runs under.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="8964b-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8964b-117">Remarks</span></span>

<span data-ttu-id="8964b-118">Informationen zur C++-Entwicklung finden Sie unter [**Runlevel-Eigenschaft von IPrincipal**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel).</span><span class="sxs-lookup"><span data-stu-id="8964b-118">For C++ development, see [**RunLevel Property of IPrincipal**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel).</span></span>

<span data-ttu-id="8964b-119">Informationen zur Skript Entwicklung finden Sie unter [**Principal. Runlevel**](principal-runlevel.md).</span><span class="sxs-lookup"><span data-stu-id="8964b-119">For script development, see [**Principal.RunLevel**](principal-runlevel.md).</span></span>

<span data-ttu-id="8964b-120">Wenn eine Aufgabe mit dem integrierten **\\ Administrator** Konto oder den Konten " [LocalSystem](/windows/desktop/Services/localsystem-account) " oder " [LocalService](/windows/desktop/Services/localservice-account) " registriert wird, wird die [**Runlevel**](principal-runlevel.md) -Eigenschaft ignoriert.</span><span class="sxs-lookup"><span data-stu-id="8964b-120">If a task is registered using the **Builtin\\Administrator** account or the [LocalSystem](/windows/desktop/Services/localsystem-account) or [LocalService](/windows/desktop/Services/localservice-account) accounts, the [**RunLevel**](principal-runlevel.md) property is ignored.</span></span> <span data-ttu-id="8964b-121">Der Attribut Wert wird auch ignoriert, wenn die [Benutzerkontensteuerung (User Account Control](/windows/desktop/SecAuthZ/user-account-control) , UAC) ausgeschaltet ist.</span><span class="sxs-lookup"><span data-stu-id="8964b-121">The attribute value will also be ignored if [User Account Control](/windows/desktop/SecAuthZ/user-account-control) (UAC) is turned off.</span></span>

<span data-ttu-id="8964b-122">Wenn eine Aufgabe mithilfe der Gruppe " **Administratoren** " für den Sicherheitskontext der Aufgabe registriert wird, müssen Sie die [**Runlevel**](principal-runlevel.md) -Eigenschaft auch auf "highestAvailable" festlegen, um die Aufgabe auszuführen.</span><span class="sxs-lookup"><span data-stu-id="8964b-122">If a task is registered using the **Administrators** group for the security context of the task, then you must also set the [**RunLevel**](principal-runlevel.md) property to "HighestAvailable" to run the task.</span></span> <span data-ttu-id="8964b-123">Weitere Informationen finden Sie unter [Sicherheits Kontexte für Aufgaben](security-contexts-for-running-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="8964b-123">For more information, see [Security Contexts for Tasks](security-contexts-for-running-tasks.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8964b-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8964b-124">Requirements</span></span>



| <span data-ttu-id="8964b-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8964b-125">Requirement</span></span> | <span data-ttu-id="8964b-126">Wert</span><span class="sxs-lookup"><span data-stu-id="8964b-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8964b-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8964b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="8964b-128">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8964b-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8964b-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8964b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="8964b-130">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8964b-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

