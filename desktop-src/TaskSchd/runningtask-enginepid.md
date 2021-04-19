---
title: Runningtask. enginepid (Eigenschaft)
description: Ruft bei der Skripterstellung die Prozess-ID für die Engine (Prozess) ab, die die Aufgabe ausführen soll.
ms.assetid: cb8a0f2f-ebe3-4f52-8fbd-b0cebb539728
keywords:
- Enginepid-Eigenschaft Taskplaner
- Enginepid-Eigenschaft Taskplaner, runningtask-Objekt
- Runningtask-Objekt Taskplaner, enginepid-Eigenschaft
topic_type:
- apiref
api_name:
- RunningTask.EnginePID
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bd725c44fc85e82d3693d9467956d3040aad2bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339166"
---
# <a name="runningtaskenginepid-property"></a><span data-ttu-id="b5de2-106">Runningtask. enginepid (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="b5de2-106">RunningTask.EnginePID property</span></span>

<span data-ttu-id="b5de2-107">Ruft bei der Skripterstellung die Prozess-ID für die Engine (Prozess) ab, die die Aufgabe ausführen soll.</span><span class="sxs-lookup"><span data-stu-id="b5de2-107">For scripting, gets the process ID for the engine (process) which is running the task.</span></span>

<span data-ttu-id="b5de2-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="b5de2-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5de2-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="b5de2-109">Syntax</span></span>


```VB
RunningTask.EnginePID As Integer
```



## <a name="property-value"></a><span data-ttu-id="b5de2-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="b5de2-110">Property value</span></span>

<span data-ttu-id="b5de2-111">Die Prozess-ID für die Engine, die die Aufgabe ausführen soll.</span><span class="sxs-lookup"><span data-stu-id="b5de2-111">The process ID for the engine which is running the task.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5de2-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b5de2-112">Remarks</span></span>

<span data-ttu-id="b5de2-113">Die von dieser Eigenschaft zurückgegebene Prozess-ID kann nicht direkt an eine Zeichenfolge angehängt werden.</span><span class="sxs-lookup"><span data-stu-id="b5de2-113">The process ID returned by this property cannot be appended directly to a string.</span></span> <span data-ttu-id="b5de2-114">Der zurückgegebene Wert muss zuerst in einen ganzzahligen Wert konvertiert werden, indem die [CInt](/previous-versions//fctcwhw9(v=vs.85)) -Funktion für den zurückgegebenen Wert aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="b5de2-114">The returned value needs to be converted to an integer value first by calling the [CInt](/previous-versions//fctcwhw9(v=vs.85)) function on the returned value.</span></span>


```VB
ProcessId = cint(RunningTask.EnginePID)
wscript.echo "Process Id of Engine is " & "ProcessId
```



## <a name="requirements"></a><span data-ttu-id="b5de2-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b5de2-115">Requirements</span></span>



| <span data-ttu-id="b5de2-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b5de2-116">Requirement</span></span> | <span data-ttu-id="b5de2-117">Wert</span><span class="sxs-lookup"><span data-stu-id="b5de2-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5de2-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b5de2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b5de2-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b5de2-119">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="b5de2-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b5de2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b5de2-121">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b5de2-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b5de2-122">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="b5de2-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="b5de2-123"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b5de2-123"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b5de2-124">DLL</span><span class="sxs-lookup"><span data-stu-id="b5de2-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5de2-125"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5de2-125"><dt>Taskschd.dll</dt></span></span> </dl> |



 

