---
title: Registeredtask. RunEx-Methode
description: Führt bei der Skripterstellung die registrierte Aufgabe sofort mithilfe der angegebenen Flags und einer Sitzungs-ID aus.
ms.assetid: 427bb51b-ddb1-4e47-9313-297366ba5ab7
keywords:
- RunEx-Methode Taskplaner
- RunEx-Methode Taskplaner, registeredtask-Objekt
- Registeredtask-Objekt Taskplaner, RunEx-Methode
topic_type:
- apiref
api_name:
- RegisteredTask.RunEx
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d88eb8bb651929c905f080f97a9eaefd3b4dace
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104661"
---
# <a name="registeredtaskrunex-method"></a><span data-ttu-id="b86b6-106">Registeredtask. RunEx-Methode</span><span class="sxs-lookup"><span data-stu-id="b86b6-106">RegisteredTask.RunEx method</span></span>

<span data-ttu-id="b86b6-107">Führt bei der Skripterstellung die registrierte Aufgabe sofort mithilfe der angegebenen Flags und einer Sitzungs-ID aus.</span><span class="sxs-lookup"><span data-stu-id="b86b6-107">For scripting, runs the registered task immediately using specified flags and a session identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="b86b6-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b86b6-108">Syntax</span></span>


```VB
RegisteredTask.RunEx( _
  ByVal params, _
  ByVal flags, _
  ByVal sessionID, _
  ByRef runningTask _
)
```



## <a name="parameters"></a><span data-ttu-id="b86b6-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="b86b6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b86b6-110"> Parameter \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b86b6-110">*params* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b86b6-111">Die Parameter, die als Werte in den Aufgaben Aktionen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b86b6-111">The parameters used as values in the task actions.</span></span> <span data-ttu-id="b86b6-112">Wenn Sie keine Parameterwerte für die Task Aktionen angeben möchten, legen Sie diesen Parameter auf " **Nothing**" fest.</span><span class="sxs-lookup"><span data-stu-id="b86b6-112">To not specify any parameter values for the task actions, set this parameter to **Nothing**.</span></span> <span data-ttu-id="b86b6-113">Andernfalls kann ein einzelner Zeichen folgen Wert oder ein Array von Zeichen folgen Werten angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b86b6-113">Otherwise, a single string value or an array of string values can be specified.</span></span>

<span data-ttu-id="b86b6-114">Die Zeichen folgen Werte, die Sie angeben, werden mit Namen gekoppelt und als Name-Wert-Paare gespeichert.</span><span class="sxs-lookup"><span data-stu-id="b86b6-114">The string values that you specify are paired with names and stored as name-value pairs.</span></span> <span data-ttu-id="b86b6-115">Wenn Sie einen einzelnen Zeichen folgen Wert angeben, ist Arg0 der Name, der dem Wert zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="b86b6-115">If you specify a single string value, then Arg0 will be the name assigned to the value.</span></span> <span data-ttu-id="b86b6-116">Der Wert kann in der Task Aktion verwendet werden, bei der die $ (Arg0)-Variable in den Aktions Eigenschaften verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b86b6-116">The value can be used in the task action where the $(Arg0) variable is used in the action properties.</span></span>

<span data-ttu-id="b86b6-117">Wenn Sie Werte wie z. b. "0", "100" und "250" als Array von Zeichen folgen Werten übergeben, ersetzt "0" die Variablen "$ (Arg0)", "100" ersetzt die Variablen "$ (arg1)", und "250" ersetzt die $ (arg2)-Variablen, die in den Aktions Eigenschaften verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b86b6-117">If you pass in values such as "0", "100", and "250" as an array of string values, then "0" will replace the $(Arg0) variables, "100" will replace the $(Arg1) variables, and "250" will replace the $(Arg2) variables used in the action properties.</span></span>

<span data-ttu-id="b86b6-118">Es können maximal 32 Zeichen folgen Werte angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b86b6-118">A maximum of 32 string values can be specified.</span></span>

<span data-ttu-id="b86b6-119">Weitere Informationen und eine Liste der Aktions Eigenschaften, die die Variablen $ (Arg0), $ (arg1),..., $ (Arg32) in ihren Werten verwenden können, finden Sie unter [Task Actions](task-actions.md).</span><span class="sxs-lookup"><span data-stu-id="b86b6-119">For more information and a list of action properties that can use $(Arg0), $(Arg1), ..., $(Arg32) variables in their values, see [Task Actions](task-actions.md).</span></span>

</dd> <dt>

<span data-ttu-id="b86b6-120">*Flags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b86b6-120">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b86b6-121">Eine [ \_ \_ tasktestflags](/windows/desktop/api/taskschd/ne-taskschd-task_run_flags) -Konstante, die definiert, wie die Aufgabe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b86b6-121">A [TASK\_RUN\_FLAGS](/windows/desktop/api/taskschd/ne-taskschd-task_run_flags) constant that defines how the task is run.</span></span>

</dd> <dt>

<span data-ttu-id="b86b6-122">*SessionID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b86b6-122">*sessionID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b86b6-123">Die Terminal Server Sitzung, in der die Aufgabe gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b86b6-123">The terminal server session in which you want to launch the task.</span></span>

<span data-ttu-id="b86b6-124">Wenn die aufgabenrun- \_ \_ Sitzungs-ID- \_ \_ Konstante (0x4) nicht an den *Flags* -Parameter übergeben wird, wird der in diesem Parameter angegebene Wert ignoriert.</span><span class="sxs-lookup"><span data-stu-id="b86b6-124">If the TASK\_RUN\_USE\_SESSION\_ID constant (0x4) is not passed into the *flags* parameter, then the value specified in this parameter is ignored.</span></span> <span data-ttu-id="b86b6-125">Wenn die Task Ausführungs- \_ \_ ID der \_ Sitzungs \_ -ID an den *Flags* -Parameter übergeben wird und der SessionID-Wert kleiner oder gleich 0 ist, wird ein ungültiger Argument Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b86b6-125">If the TASK\_RUN\_USE\_SESSION\_ID constant is passed into the *flags* parameter and the sessionID value is less than or equal to 0, then an invalid argument error will be returned.</span></span>

<span data-ttu-id="b86b6-126">Wenn die \_ \_ \_ aufgabenrun-Sitzungs- \_ ID-Konstante in den *Flags* -Parameter übergeben wird und der SessionID-Wert eine gültige Sitzungs-ID größer als 0 ist und kein Wert für den *User* -Parameter angegeben wird, versucht der Taskplaner Dienst, die Aufgabe interaktiv zu starten, als der Benutzer, der bei der angegebenen Sitzung angemeldet ist.</span><span class="sxs-lookup"><span data-stu-id="b86b6-126">If the TASK\_RUN\_USE\_SESSION\_ID constant is passed into the *flags* parameter and the sessionID value is a valid session ID greater than 0 and if no value is specified for the *user* parameter, then the Task Scheduler service will try to launch the task interactively as the user who is logged on to the specified session.</span></span>

<span data-ttu-id="b86b6-127">Wenn die \_ \_ \_ aufgabenrun-Sitzungs- \_ ID-Konstante in den *Flags* -Parameter übergeben wird und der SessionID-Wert eine gültige Sitzungs-ID ist, die größer als 0 ist, und wenn ein Benutzer im *Benutzer* Parameter angegeben wird, versucht der Taskplaner Dienst, die Aufgabe interaktiv zu starten, als der Benutzer, der im *Benutzer* Parameter angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="b86b6-127">If the TASK\_RUN\_USE\_SESSION\_ID constant is passed into the *flags* parameter and the sessionID value is a valid session ID greater than 0 and if a user is specified in the *user* parameter, then the Task Scheduler service will try to launch the task interactively as the user who is specified in the *user* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="b86b6-128">*runningtask* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b86b6-128">*runningTask* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b86b6-129">Ein [**runningtask**](runningtask.md) -Objekt, das die neue Instanz der Aufgabe definiert.</span><span class="sxs-lookup"><span data-stu-id="b86b6-129">A [**RunningTask**](runningtask.md) object that defines the new instance of the task.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b86b6-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b86b6-130">Return value</span></span>

<span data-ttu-id="b86b6-131">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b86b6-131">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b86b6-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b86b6-132">Remarks</span></span>

<span data-ttu-id="b86b6-133">Diese Methode wird ohne Fehler zurückgegeben, aber die Aufgabe wird nicht ausgeführt, wenn die [**Task Settings. allowdemandstart**](tasksettings-allowdemandstart.md) -Eigenschaft für die registrierte Aufgabe auf false festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="b86b6-133">This method will return without error, but the task will not run if the [**TaskSettings.AllowDemandStart**](tasksettings-allowdemandstart.md) property is set to false for the registered task.</span></span>

## <a name="requirements"></a><span data-ttu-id="b86b6-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b86b6-134">Requirements</span></span>



| <span data-ttu-id="b86b6-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b86b6-135">Requirement</span></span> | <span data-ttu-id="b86b6-136">Wert</span><span class="sxs-lookup"><span data-stu-id="b86b6-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b86b6-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b86b6-137">Minimum supported client</span></span><br/> | <span data-ttu-id="b86b6-138">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b86b6-138">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="b86b6-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b86b6-139">Minimum supported server</span></span><br/> | <span data-ttu-id="b86b6-140">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b86b6-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b86b6-141">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="b86b6-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="b86b6-142"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b86b6-142"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b86b6-143">DLL</span><span class="sxs-lookup"><span data-stu-id="b86b6-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b86b6-144"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b86b6-144"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b86b6-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b86b6-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b86b6-146">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="b86b6-146">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="b86b6-147">**Registeredtask**</span><span class="sxs-lookup"><span data-stu-id="b86b6-147">**RegisteredTask**</span></span>](registeredtask.md)
</dt> </dl>

 

 





