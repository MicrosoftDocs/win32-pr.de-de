---
title: Registeredtask. Run-Methode
description: Führt bei der Skripterstellung die registrierte Aufgabe sofort aus.
ms.assetid: 99c8f6ea-6dcf-4f9a-bf61-5191df5958c6
keywords:
- Run-Methode Taskplaner
- Run-Methode Taskplaner, registeredtask-Objekt
- Registeredtask-Objekt Taskplaner, Run-Methode
topic_type:
- apiref
api_name:
- RegisteredTask.Run
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd10539518b22f596e42afd56324c90b881412b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106343045"
---
# <a name="registeredtaskrun-method"></a><span data-ttu-id="e7890-106">Registeredtask. Run-Methode</span><span class="sxs-lookup"><span data-stu-id="e7890-106">RegisteredTask.Run method</span></span>

<span data-ttu-id="e7890-107">Führt bei der Skripterstellung die registrierte Aufgabe sofort aus.</span><span class="sxs-lookup"><span data-stu-id="e7890-107">For scripting, runs the registered task immediately.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7890-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e7890-108">Syntax</span></span>


```VB
RegisteredTask.Run( _
  ByVal params, _
  ByRef ppRunningTask _
)
```



## <a name="parameters"></a><span data-ttu-id="e7890-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="e7890-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7890-110"> Parameter \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e7890-110">*params* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7890-111">Die Parameter, die als Werte in den Aufgaben Aktionen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e7890-111">The parameters used as values in the task actions.</span></span> <span data-ttu-id="e7890-112">Wenn Sie keine Parameterwerte für die Task Aktionen angeben möchten, legen Sie diesen Parameter auf " **Nothing**" fest.</span><span class="sxs-lookup"><span data-stu-id="e7890-112">To not specify any parameter values for the task actions, set this parameter to **Nothing**.</span></span> <span data-ttu-id="e7890-113">Andernfalls kann ein einzelner Zeichen folgen Wert oder ein Array von Zeichen folgen Werten angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e7890-113">Otherwise, a single string value or an array of string values can be specified.</span></span>

<span data-ttu-id="e7890-114">Die Zeichen folgen Werte, die Sie angeben, werden mit Namen gekoppelt und als Name-Wert-Paare gespeichert.</span><span class="sxs-lookup"><span data-stu-id="e7890-114">The string values that you specify are paired with names and stored as name-value pairs.</span></span> <span data-ttu-id="e7890-115">Wenn Sie einen einzelnen Zeichen folgen Wert angeben, ist Arg0 der Name, der dem Wert zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="e7890-115">If you specify a single string value, then Arg0 will be the name assigned to the value.</span></span> <span data-ttu-id="e7890-116">Der Wert kann in der Task Aktion verwendet werden, bei der die $ (Arg0)-Variable in den Aktions Eigenschaften verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e7890-116">The value can be used in the task action where the $(Arg0) variable is used in the action properties.</span></span>

<span data-ttu-id="e7890-117">Wenn Sie Werte wie z. b. "0", "100" und "250" als Array von Zeichen folgen Werten übergeben, ersetzt "0" die Variablen "$ (Arg0)", "100" ersetzt die Variablen "$ (arg1)", und "250" ersetzt die $ (arg2)-Variablen, die in den Aktions Eigenschaften verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e7890-117">If you pass in values such as "0", "100", and "250" as an array of string values, then "0" will replace the $(Arg0) variables, "100" will replace the $(Arg1) variables, and "250" will replace the $(Arg2) variables used in the action properties.</span></span>

<span data-ttu-id="e7890-118">Es können maximal 32 Zeichen folgen Werte angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e7890-118">A maximum of 32 string values can be specified.</span></span>

<span data-ttu-id="e7890-119">Weitere Informationen und eine Liste der Aktions Eigenschaften, die die Variablen $ (Arg0), $ (arg1),..., $ (Arg32) in ihren Werten verwenden können, finden Sie unter [Task Actions](task-actions.md).</span><span class="sxs-lookup"><span data-stu-id="e7890-119">For more information and a list of action properties that can use $(Arg0), $(Arg1), ..., $(Arg32) variables in their values, see [Task Actions](task-actions.md).</span></span>

</dd> <dt>

<span data-ttu-id="e7890-120">*pprunningtask* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e7890-120">*ppRunningTask* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e7890-121">Ein [**runningtask**](runningtask.md) -Objekt, das die neue Instanz der Aufgabe definiert.</span><span class="sxs-lookup"><span data-stu-id="e7890-121">A [**RunningTask**](runningtask.md) object that defines the new instance of the task.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7890-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e7890-122">Return value</span></span>

<span data-ttu-id="e7890-123">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="e7890-123">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7890-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e7890-124">Remarks</span></span>

<span data-ttu-id="e7890-125">Die **registeredtask. Run** -Funktion entspricht der [**registeredtask. RunEx**](registeredtask-runex.md) -Funktion, wobei der Flags-Parameter gleich 0 und für den User-Parameter nichts angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="e7890-125">The **RegisteredTask.Run** function is equivalent to the [**RegisteredTask.RunEx**](registeredtask-runex.md) function with the flags parameter equal to 0 and nothing specified for the user parameter.</span></span>

<span data-ttu-id="e7890-126">Diese Methode wird ohne Fehler zurückgegeben, aber die Aufgabe wird nicht ausgeführt, wenn die [**Task Settings. allowdemandstart**](tasksettings-allowdemandstart.md) -Eigenschaft für die registrierte Aufgabe auf false festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e7890-126">This method will return without error, but the task will not run if the [**TaskSettings.AllowDemandStart**](tasksettings-allowdemandstart.md) property is set to false for the registered task.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7890-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e7890-127">Requirements</span></span>



| <span data-ttu-id="e7890-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e7890-128">Requirement</span></span> | <span data-ttu-id="e7890-129">Wert</span><span class="sxs-lookup"><span data-stu-id="e7890-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7890-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e7890-130">Minimum supported client</span></span><br/> | <span data-ttu-id="e7890-131">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e7890-131">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="e7890-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e7890-132">Minimum supported server</span></span><br/> | <span data-ttu-id="e7890-133">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e7890-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e7890-134">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="e7890-134">Type library</span></span><br/>             | <dl> <span data-ttu-id="e7890-135"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e7890-135"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e7890-136">DLL</span><span class="sxs-lookup"><span data-stu-id="e7890-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7890-137"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7890-137"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7890-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e7890-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7890-139">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="e7890-139">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="e7890-140">**Registeredtask**</span><span class="sxs-lookup"><span data-stu-id="e7890-140">**RegisteredTask**</span></span>](registeredtask.md)
</dt> </dl>

 

 





