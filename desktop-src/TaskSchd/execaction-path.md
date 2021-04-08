---
title: Execaction. Path-Eigenschaft
description: Bei der Skripterstellung wird der Pfad zu einer ausführbaren Datei abgerufen oder festgelegt.
ms.assetid: 00fea05f-4f57-47ac-9812-8cd352fe02a8
keywords:
- Pfadeigenschaft Taskplaner
- Pfadeigenschaft Taskplaner, execaction-Objekt
- Execaction-Objekt Taskplaner, Path-Eigenschaft
topic_type:
- apiref
api_name:
- ExecAction.Path
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b20e1dcd8cd9700f961eb944c7be3168582b8c55
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740857"
---
# <a name="execactionpath-property"></a><span data-ttu-id="da19c-106">Execaction. Path-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="da19c-106">ExecAction.Path property</span></span>

<span data-ttu-id="da19c-107">Bei der Skripterstellung wird der Pfad zu einer ausführbaren Datei abgerufen oder festgelegt.</span><span class="sxs-lookup"><span data-stu-id="da19c-107">For scripting, gets or sets the path to an executable file.</span></span>

## <a name="syntax"></a><span data-ttu-id="da19c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="da19c-108">Syntax</span></span>


```VB
ExecAction.Path As String
```



## <a name="property-value"></a><span data-ttu-id="da19c-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="da19c-109">Property value</span></span>

<span data-ttu-id="da19c-110">Der Pfad zu der ausführbaren Datei, die von der Aktion ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="da19c-110">The path to the executable file to be run by the action.</span></span>

## <a name="remarks"></a><span data-ttu-id="da19c-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="da19c-111">Remarks</span></span>

<span data-ttu-id="da19c-112">Diese Aktion führt einen Befehlszeilen Vorgang aus.</span><span class="sxs-lookup"><span data-stu-id="da19c-112">This action performs a command-line operation.</span></span> <span data-ttu-id="da19c-113">Beispielsweise könnte die Aktion ein Skript ausführen oder eine ausführbare Datei starten.</span><span class="sxs-lookup"><span data-stu-id="da19c-113">For example, the action could run a script or launch an executable.</span></span>

<span data-ttu-id="da19c-114">Beim Lesen oder Schreiben von XML wird der Befehlszeilen-Vorgangs Pfad im [**Command**](taskschedulerschema-command-exectype-element.md) -Element des Taskplaner-Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="da19c-114">When reading or writing XML, the command-line operation path is specified in the [**Command**](taskschedulerschema-command-exectype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="da19c-115">Der Pfad wird geprüft, um sicherzustellen, dass er gültig ist, wenn die Aufgabe registriert wird, und nicht, wenn diese Eigenschaft festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="da19c-115">The path is checked to make sure it is valid when the task is registered, not when this property is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="da19c-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="da19c-116">Requirements</span></span>



| <span data-ttu-id="da19c-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="da19c-117">Requirement</span></span> | <span data-ttu-id="da19c-118">Wert</span><span class="sxs-lookup"><span data-stu-id="da19c-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="da19c-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="da19c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="da19c-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="da19c-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="da19c-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="da19c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="da19c-122">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="da19c-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="da19c-123">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="da19c-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="da19c-124"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="da19c-124"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="da19c-125">DLL</span><span class="sxs-lookup"><span data-stu-id="da19c-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da19c-126"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da19c-126"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da19c-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="da19c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da19c-128">**Execaction**</span><span class="sxs-lookup"><span data-stu-id="da19c-128">**ExecAction**</span></span>](execaction.md)
</dt> <dt>

[<span data-ttu-id="da19c-129">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="da19c-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





