---
description: Bietet semisynchrone Zugriffs Funktionen und ein Codebeispiel für die Ausführung eines semisynchronen Methoden Aufrufes.
ms.assetid: 3eae38e8-6a63-45c0-99b0-94e25ddbc5a8
ms.tgt_platform: multiple
title: Erstellen eines semisynchronen Aufrufes mit VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e875a269d2cf1cd4e3b40d5c84d42ffb97dc35a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356298"
---
# <a name="making-a-semisynchronous-call-with-vbscript"></a><span data-ttu-id="dd55f-103">Erstellen eines semisynchronen Aufrufes mit VBScript</span><span class="sxs-lookup"><span data-stu-id="dd55f-103">Making a Semisynchronous Call with VBScript</span></span>

<span data-ttu-id="dd55f-104">Einige WMI-Methoden können große Auflistungen zurückgeben, sodass Skripts nicht mehr reagieren.</span><span class="sxs-lookup"><span data-stu-id="dd55f-104">Some WMI methods can return large collections, causing scripts to stop responding.</span></span> <span data-ttu-id="dd55f-105">In Skripts ist der semisynchrone Zugriff der Standard, und in Windows-Verwaltungsinstrumentation (WMI) wird **wbemFlagReturnImmediately** für Aufrufe festgelegt, die große Objekt Auflistungen zurückgeben können, wie z. b. die folgenden [**Swap Services**](swbemservices.md) -Methoden: [**InstancesOf**](swbemservices-instancesof.md), [**SubclassesOf**](swbemservices-subclassesof.md), [**ExecQuery**](swbemservices-execquery.md), [**associatorsof**](swbemservices-associatorsof.md)und [**referencesto**](swbemservices-referencesto.md).</span><span class="sxs-lookup"><span data-stu-id="dd55f-105">In script, semisynchronous access is the default, and Windows Management Instrumentation (WMI) sets **wbemFlagReturnImmediately** for calls that can return large object collections such as the following [**SWbemServices**](swbemservices.md) methods: [**InstancesOf**](swbemservices-instancesof.md), [**SubclassesOf**](swbemservices-subclassesof.md), [**ExecQuery**](swbemservices-execquery.md), [**AssociatorsOf**](swbemservices-associatorsof.md), and [**ReferencesTo**](swbemservices-referencesto.md).</span></span>

<span data-ttu-id="dd55f-106">Der semisynchrone Zugriff, bei dem **wbemFlagReturnImmediately** im *IFlags* -Parameter festgelegt ist, ist auch die Standardeinstellung für Aufrufe, die große Objekt Sätze für die folgenden " [**errbewbject**](swbemobject.md) "-Methoden zurückgeben können: [**Instanzen \_**](swbemobject-instances-.md), [**Unterklassen \_**](swbemobject-subclasses-.md), [**assoziatoren \_**](swbemobject-associators-.md)und [**Verweise \_**](swbemobject-references-.md).</span><span class="sxs-lookup"><span data-stu-id="dd55f-106">Semisynchronous access that uses **wbemFlagReturnImmediately** set in the *IFlags* parameter is also the default for calls that can return large object sets for the following [**SWbemObject**](swbemobject.md) methods: [**Instances\_**](swbemobject-instances-.md), [**Subclasses\_**](swbemobject-subclasses-.md), [**Associators\_**](swbemobject-associators-.md), and [**References\_**](swbemobject-references-.md).</span></span>

<span data-ttu-id="dd55f-107">Um die Verwendung der WMI-Speicher Ressource bei der Verarbeitung einer großen Auflistung von Objekten zu reduzieren, schließen Sie den Wert von **wbemFlagForwardOnly** in den *IFlags* -Parameter ein.</span><span class="sxs-lookup"><span data-stu-id="dd55f-107">To reduce the WMI memory resource usage when processing a large collection of objects, include the value of **wbemFlagForwardOnly** in the *IFlags* parameter.</span></span> <span data-ttu-id="dd55f-108">Die Verwendung von **wbemFlagForwardOnly** bewirkt, dass WMI einen vorwärts-Enumerator erstellt, der das erneute Auffüllen der Auflistung und das erneute zugreifen auf Elemente nicht zulässt.</span><span class="sxs-lookup"><span data-stu-id="dd55f-108">Using **wbemFlagForwardOnly** causes WMI to create a forward-only enumerator that does not allow rewinding the collection and accessing items again.</span></span>

<span data-ttu-id="dd55f-109">WMI entfernt den Arbeitsspeicher für jedes Objekt, da die **for each** -Anweisung ein-Objekt verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="dd55f-109">WMI eliminates the memory for each object as the **For Each** statement processes an object.</span></span> <span data-ttu-id="dd55f-110">Die **count** -Methode kann nicht für eine Auflistung aufgerufen werden, wenn das **wbemFlagForwardOnly** -Flag für den-Befehl festgelegt wurde, der die Auflistung abgerufen hat.</span><span class="sxs-lookup"><span data-stu-id="dd55f-110">You cannot call the **Count** method for a collection when the **wbemFlagForwardOnly** flag was set on the call that obtained the collection.</span></span> <span data-ttu-id="dd55f-111">Beachten Sie, dass für den *IFlags* -Parameter **wbemFlagReturnImmediately** und **wbemFlagForwardOnly** standardmäßig für die [**SWbemServices.Execnotificationquery**](swbemservices-execnotificationquery.md) -Methode festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="dd55f-111">Note that the *IFlags* parameter has **wbemFlagReturnImmediately** and **wbemFlagForwardOnly** set by default for the [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) method.</span></span>

<span data-ttu-id="dd55f-112">Im folgenden Verfahren wird beschrieben, wie VBScript zum Ausführen eines semisynchronen Aufrufes verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dd55f-112">The following procedure describes how to use VBScript to make a semisynchronous call.</span></span>

<span data-ttu-id="dd55f-113">**So führen Sie einen semisynchronen-Befehl in VBScript aus**</span><span class="sxs-lookup"><span data-stu-id="dd55f-113">**To make a semisynchronous call in VBScript**</span></span>

1.  <span data-ttu-id="dd55f-114">Legen Sie den *IFlags* -Parameter auf den Wert von [wbemFlagReturnImmediately](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum)fest.</span><span class="sxs-lookup"><span data-stu-id="dd55f-114">Set the *IFlags* parameter to the value of [wbemFlagReturnImmediately](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum).</span></span>
2.  <span data-ttu-id="dd55f-115">Führen Sie den normalen synchronen Aufruf für [**SWbemServices.Execquery**](swbemservices-execquery.md) oder [**SWbemServices.Execnotificationquery**](swbemservices-execnotificationquery.md) mit dem *IFlags* -Wert aus.</span><span class="sxs-lookup"><span data-stu-id="dd55f-115">Make the normal synchronous call for [**SWbemServices.ExecQuery**](swbemservices-execquery.md) or [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) with the *iFlags* value.</span></span>
3.  <span data-ttu-id="dd55f-116">Wenn Sie die vom-Befehl zurückgegebenen Objekte als Auflistung behandeln möchten, verwenden Sie **jeweils** eine Enumerationssyntax, z. b. VBScript.</span><span class="sxs-lookup"><span data-stu-id="dd55f-116">If you want to treat the objects returned by the call as a collection, use an enumeration syntax such as VBScript **For Each**.</span></span> <span data-ttu-id="dd55f-117">Da jedes Objekt zurückgegeben wird, wird es als das nächste Element in der Auflistung verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="dd55f-117">As each object is returned, it is processed as the next item in the collection.</span></span>
4.  <span data-ttu-id="dd55f-118">Erstellen Sie einen vorwärts-Enumerator, indem Sie den Wert von **wbemFlagReturnImmediately** mit dem Wert von **wbemFlagForwardOnly** kombinieren.</span><span class="sxs-lookup"><span data-stu-id="dd55f-118">Create a forward-only enumerator by combining the value of **wbemFlagReturnImmediately** with the value of **wbemFlagForwardOnly**.</span></span> <span data-ttu-id="dd55f-119">Der Dezimalwert dieses or-Vorgangs ist 48.</span><span class="sxs-lookup"><span data-stu-id="dd55f-119">The decimal value of this OR operation is 48.</span></span> <span data-ttu-id="dd55f-120">Diese Konstanten werden in der wbemdisp. tlb-Typbibliothek für Visual Basic definiert.</span><span class="sxs-lookup"><span data-stu-id="dd55f-120">These constants are defined in the wbemdisp.tlb type library for Visual Basic.</span></span> <span data-ttu-id="dd55f-121">Die meisten Skriptsprachen verwenden den numerischen Wert oder definieren eine Konstante.</span><span class="sxs-lookup"><span data-stu-id="dd55f-121">Most scripting languages use the numeric value or define a constant.</span></span> <span data-ttu-id="dd55f-122">Weitere Informationen finden Sie unter [wbemflagenum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum).</span><span class="sxs-lookup"><span data-stu-id="dd55f-122">For more information, see [WbemFlagEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum).</span></span>

<span data-ttu-id="dd55f-123">Im folgenden Codebeispiel wird gezeigt, wie Sie einen semisynchronen Methoden aufrufmachen.</span><span class="sxs-lookup"><span data-stu-id="dd55f-123">The following code example shows how to make a semisynchronous method call.</span></span> <span data-ttu-id="dd55f-124">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="dd55f-124">For more information, see [Calling a Method](calling-a-method.md).</span></span>


```VB
wbemFlagReturnImmediately = 16
wbemFlagForwardOnly = 32
IFlags = wbemFlagReturnImmediately + wbemFlagForwardOnly
WScript.Echo IFlags
Set objWMIService = GetObject("winmgmts:root\cimv2")
' Query for all the Win32_Process objects on the 
'     local computer and use forward-only enumerator
Set colProcesses = objWMIService.ExecQuery("SELECT Name FROM Win32_Process",,IFlags)
' Receive each object as it arrives
For Each objProcess in colProcesses
    WScript.Echo objProcess.Name
Next
```



## <a name="related-topics"></a><span data-ttu-id="dd55f-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="dd55f-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd55f-126">Aufrufen einer Methode</span><span class="sxs-lookup"><span data-stu-id="dd55f-126">Calling a Method</span></span>](calling-a-method.md)
</dt> </dl>

 

 



