---
title: Principal. Runlevel-Eigenschaft
description: Ruft bei der Skripterstellung den Bezeichner ab, der zum Ausführen der dem Prinzipal zugeordneten Aufgaben verwendet wird, oder legt ihn fest.
ms.assetid: 2ec3d93e-9eef-4590-842c-edfc9232bcdf
keywords:
- Taskplaner der Runlevel-Eigenschaft
- Runlevel-Eigenschaften Taskplaner, Prinzipal Objekt
- Principal-Objekt Taskplaner, Runlevel-Eigenschaft
topic_type:
- apiref
api_name:
- Principal.RunLevel
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9acb6c4c86215312b2df73f7bf85847ef61a4b96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517906"
---
# <a name="principalrunlevel-property"></a><span data-ttu-id="adb98-106">Principal. Runlevel-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="adb98-106">Principal.RunLevel property</span></span>

<span data-ttu-id="adb98-107">Ruft bei der Skripterstellung den Bezeichner ab, der zum Ausführen der dem Prinzipal zugeordneten Aufgaben verwendet wird, oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="adb98-107">For scripting, gets or sets the identifier that is used to specify the privilege level that is required to run the tasks that are associated with the principal.</span></span>

<span data-ttu-id="adb98-108">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="adb98-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="adb98-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="adb98-109">Syntax</span></span>


```VB
Principal.RunLevel As Integer
```



## <a name="property-value"></a><span data-ttu-id="adb98-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="adb98-110">Property value</span></span>

<span data-ttu-id="adb98-111">Der Bezeichner, der verwendet wird, um die Berechtigungsebene anzugeben, die zum Ausführen der Aufgaben erforderlich ist, die dem Prinzipal zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="adb98-111">The identifier that is used to specify the privilege level that is required to run the tasks that are associated with the principal.</span></span>



| <span data-ttu-id="adb98-112">Wert</span><span class="sxs-lookup"><span data-stu-id="adb98-112">Value</span></span>                                                                                                                                                                                                                                         | <span data-ttu-id="adb98-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="adb98-113">Meaning</span></span>                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="TASK_RUNLEVEL_LUA"></span><span id="task_runlevel_lua"></span><dl> <span data-ttu-id="adb98-114"><dt>**Aufgabe \_ Runlevel \_ Lua**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="adb98-114"><dt>**TASK\_RUNLEVEL\_LUA**</dt> <dt>0</dt></span></span> </dl>             | <span data-ttu-id="adb98-115">Tasks werden mit den geringsten Berechtigungen (LUA) ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="adb98-115">Tasks will be run with the least privileges (LUA).</span></span><br/> |
| <span id="TASK_RUNLEVEL_HIGHEST"></span><span id="task_runlevel_highest"></span><dl> <span data-ttu-id="adb98-116"><dt>**Aufgabe \_ \_Höchste Runlevel**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="adb98-116"><dt>**TASK\_RUNLEVEL\_HIGHEST**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="adb98-117">Tasks werden mit den höchsten Berechtigungen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="adb98-117">Tasks will be run with the highest privileges.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="adb98-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="adb98-118">Remarks</span></span>

<span data-ttu-id="adb98-119">Wenn ein Task mit dem integrierten \\ Administrator Konto oder dem lokalen System Konto oder dem lokalen Dienst Konto registriert wird, wird die **Runlevel** -Eigenschaft ignoriert.</span><span class="sxs-lookup"><span data-stu-id="adb98-119">If a task is registered using the Builtin\\Administrator account or the Local System or Local Service accounts, then the **RunLevel** property will be ignored.</span></span> <span data-ttu-id="adb98-120">Der Eigenschafts Wert wird auch ignoriert, wenn die Benutzerkontensteuerung (User Account Control, UAC) ausgeschaltet ist.</span><span class="sxs-lookup"><span data-stu-id="adb98-120">The property value will also be ignored if User Account Control (UAC) is turned off.</span></span>

<span data-ttu-id="adb98-121">Wenn eine Aufgabe mithilfe der Gruppe "Administratoren" für den Sicherheitskontext der Aufgabe registriert wird, müssen Sie die [**Runlevel**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel) -Eigenschaft auch auf " **Task \_ Runlevel \_** " festlegen, wenn Sie die Aufgabe ausführen möchten.</span><span class="sxs-lookup"><span data-stu-id="adb98-121">If a task is registered using the Administrators group for the security context of the task, then you must also set the [**RunLevel**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel) property to **TASK\_RUNLEVEL\_HIGHEST** if you want to run the task.</span></span> <span data-ttu-id="adb98-122">Weitere Informationen finden Sie unter [Sicherheits Kontexte für Aufgaben](security-contexts-for-running-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="adb98-122">For more information, see [Security Contexts for Tasks](security-contexts-for-running-tasks.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="adb98-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="adb98-123">Requirements</span></span>



| <span data-ttu-id="adb98-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="adb98-124">Requirement</span></span> | <span data-ttu-id="adb98-125">Wert</span><span class="sxs-lookup"><span data-stu-id="adb98-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="adb98-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="adb98-126">Minimum supported client</span></span><br/> | <span data-ttu-id="adb98-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="adb98-127">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="adb98-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="adb98-128">Minimum supported server</span></span><br/> | <span data-ttu-id="adb98-129">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="adb98-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="adb98-130">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="adb98-130">Type library</span></span><br/>             | <dl> <span data-ttu-id="adb98-131"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="adb98-131"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="adb98-132">DLL</span><span class="sxs-lookup"><span data-stu-id="adb98-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="adb98-133"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="adb98-133"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="adb98-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="adb98-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adb98-135">**Prinzipal**</span><span class="sxs-lookup"><span data-stu-id="adb98-135">**Principal**</span></span>](principal.md)
</dt> </dl>

 

 





