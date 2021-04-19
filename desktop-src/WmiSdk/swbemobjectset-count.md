---
description: Verwenden Sie die Count-Eigenschaft des "errbemubjectset"-Objekts, um zu bestimmen, wie viele Elemente in einer Auflistung von "errbemubjectset" vorliegen. Diese Eigenschaft ist schreibgeschützt.
ms.assetid: ad3d1265-a11e-4962-b1f3-60092d2f79ef
ms.tgt_platform: multiple
title: Errbemubjectset. Count-Eigenschaft (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectSet.Count
- ISWbemObjectSet.Count
- ISWbemObjectSet.get_Count
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3154e22bbdbc75080ceebdf8b1eef602cf5c3be3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352738"
---
# <a name="swbemobjectsetcount-property"></a><span data-ttu-id="54491-104">Errbemubjectset. Count-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="54491-104">SWbemObjectSet.Count property</span></span>

<span data-ttu-id="54491-105">Verwenden Sie die **count** -Eigenschaft des " [**errbemubjectset**](swbemobjectset.md) "-Objekts, um zu bestimmen, wie viele Elemente in einer Auflistung von " **errbemubjectset** " vorliegen.</span><span class="sxs-lookup"><span data-stu-id="54491-105">Use the **Count** property of the [**SWbemObjectSet**](swbemobjectset.md) object to determine how many items are in an **SWbemObjectSet** collection.</span></span> <span data-ttu-id="54491-106">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="54491-106">This property is read-only.</span></span>

<span data-ttu-id="54491-107">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="54491-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="54491-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="54491-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="54491-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="54491-109">Syntax</span></span>


```VB
SWbemObjectSet.Count As Integer
```



## <a name="property-value"></a><span data-ttu-id="54491-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="54491-110">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="54491-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="54491-111">Remarks</span></span>

<span data-ttu-id="54491-112">Bei der Verwendung von count muss bei der Verwendung von "count" nicht darauf geachtet werden, dass die Anzahl der Elemente in einer Auflistung mit der Anzahl der Elemente übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="54491-112">One thing to be careful of when using Count is that WMI does not keep a running tally of the number of items in a collection.</span></span> <span data-ttu-id="54491-113">Wenn Sie die Anzahl für eine Sammlung anfordern, kann WMI nicht sofort mit einer Zahl Antworten. Stattdessen muss Sie die Elemente wirklich zählen und die gesamte Auflistung auflisten.</span><span class="sxs-lookup"><span data-stu-id="54491-113">If you request Count for a collection, WMI cannot instantly respond with a number; instead, it must literally count the items, enumerating the entire collection.</span></span> <span data-ttu-id="54491-114">Für eine Auflistung, die relativ wenige Elemente enthält, z. b. Dienste, dauert diese Enumeration wahrscheinlich weniger als eine Sekunde.</span><span class="sxs-lookup"><span data-stu-id="54491-114">For a collection that has relatively few items, such as services, this enumeration likely takes less than a second.</span></span> <span data-ttu-id="54491-115">Das zählen der Anzahl von Ereignissen in einer Ereignisprotokoll Sammlung kann jedoch erheblich länger dauern.</span><span class="sxs-lookup"><span data-stu-id="54491-115">Counting the number of events in an event log collection, however, can take considerably longer.</span></span>

<span data-ttu-id="54491-116">Angenommen, Sie möchten die Eigenschaftswerte für jedes Ereignis in der Sammlung anzeigen.</span><span class="sxs-lookup"><span data-stu-id="54491-116">And then suppose you want to display the property values for every event in the collection.</span></span> <span data-ttu-id="54491-117">Wenn dies der Fall ist, muss WMI die gesamte Auflistung ein zweites Mal auflisten.</span><span class="sxs-lookup"><span data-stu-id="54491-117">If so, WMI will have to enumerate the entire collection a second time.</span></span>

> [!Note]  
> <span data-ttu-id="54491-118">Wenn Sie versuchen, diese Eigenschaft von einem von einer Methode zurückgegebenen " [**errbemubjectset**](swbemobjectset.md) "-Objekt zu erhalten, bei dem die angegebenen Flags das wbemFlagForwardOnly-Flag enthalten, erhalten Sie einen wbemErrFailed-Fehler.</span><span class="sxs-lookup"><span data-stu-id="54491-118">If you attempt to get this property from an [**SWbemObjectSet**](swbemobjectset.md) object that is returned from a method where the specified flags are included the wbemFlagForwardOnly flag, you will get an wbemErrFailed error.</span></span>

 

## <a name="examples"></a><span data-ttu-id="54491-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="54491-119">Examples</span></span>

<span data-ttu-id="54491-120">Der einzige Schritt, den Sie jemals mit einem "errbemubjectset" ausführen, ist das Auflisten aller Objekte, die in der Auflistung enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="54491-120">For the most part, the only thing you will ever do with an SWbemObjectSet is enumerate all the objects contained within the collection itself.</span></span> <span data-ttu-id="54491-121">Die Anzahl der Zähler, die bei der Skripterstellung für die System Administration nützlich sein können.</span><span class="sxs-lookup"><span data-stu-id="54491-121">However, the Count Count that can be useful in system administration scripting.</span></span> <span data-ttu-id="54491-122">Wie der Name schon sagt, gibt count die Anzahl der Elemente in der Auflistung an.</span><span class="sxs-lookup"><span data-stu-id="54491-122">As the name implies, Count tells you the number of items in the collection.</span></span> <span data-ttu-id="54491-123">Dieses Skript ruft z. b. eine Sammlung aller auf einem Computer installierten Dienste ab und gibt dann die Gesamtzahl der gefundenen Dienste wieder:</span><span class="sxs-lookup"><span data-stu-id="54491-123">For example, this script retrieves a collection of all the services installed on a computer and then echoes the total number of services found:</span></span>


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colSWbemObjectSet = objSWbemServices.InstancesOf("Win32_Service")
Wscript.Echo "Services installed on target computer: " & colSWbemObjectSet.Count

```



<span data-ttu-id="54491-124">Die Anzahl ist hilfreich, wenn Sie erkennen können, ob eine bestimmte Instanz auf einem Computer verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="54491-124">What makes Count useful is that it can tell you whether a specific instance is available on a computer.</span></span> <span data-ttu-id="54491-125">Dieses Skript ruft z. b. eine Sammlung aller Dienste auf einem Computer ab, die den Namen W3SVC haben.</span><span class="sxs-lookup"><span data-stu-id="54491-125">For example, this script retrieves a collection of all the services on a computer that have the Name W3SVC.</span></span> <span data-ttu-id="54491-126">Wenn die Anzahl 0 beträgt (und es für Sammlungen zulässig ist, keine Instanzen zu haben), bedeutet dies, dass der W3SVC-Dienst nicht auf dem Computer installiert ist.</span><span class="sxs-lookup"><span data-stu-id="54491-126">If the Count is 0 (and it is valid for collections to have no instances), that means the W3SVC service is not installed on the computer.</span></span>


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colSWbemObjectSet = objSWbemServices.ExecQuery _
    ("SELECT * FROM Win32_Service WHERE Name='w3svc'")
If colSWbemObjectSet.Count = 0 Then
    Wscript.Echo "W3SVC service is not installed on target computer."
Else
    For Each objSWbemObject In colSWbemObjectSet
        ' Perform task on World Wide Web Publishing service.
    Next
End If
```



## <a name="requirements"></a><span data-ttu-id="54491-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="54491-127">Requirements</span></span>



| <span data-ttu-id="54491-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="54491-128">Requirement</span></span> | <span data-ttu-id="54491-129">Wert</span><span class="sxs-lookup"><span data-stu-id="54491-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="54491-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="54491-130">Minimum supported client</span></span><br/> | <span data-ttu-id="54491-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="54491-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="54491-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="54491-132">Minimum supported server</span></span><br/> | <span data-ttu-id="54491-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="54491-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="54491-134">Header</span><span class="sxs-lookup"><span data-stu-id="54491-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="54491-135"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="54491-135"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="54491-136">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="54491-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="54491-137"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="54491-137"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="54491-138">DLL</span><span class="sxs-lookup"><span data-stu-id="54491-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54491-139"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54491-139"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="54491-140">CLSID</span><span class="sxs-lookup"><span data-stu-id="54491-140">CLSID</span></span><br/>                    | <span data-ttu-id="54491-141">CLSID- \_ Swap-Objekt Satz</span><span class="sxs-lookup"><span data-stu-id="54491-141">CLSID\_SWbemObjectSet</span></span><br/>                                                        |
| <span data-ttu-id="54491-142">IID</span><span class="sxs-lookup"><span data-stu-id="54491-142">IID</span></span><br/>                      | <span data-ttu-id="54491-143">IID \_ iswbemubjectset</span><span class="sxs-lookup"><span data-stu-id="54491-143">IID\_ISWbemObjectSet</span></span><br/>                                                         |



 

 




