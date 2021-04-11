---
description: Das Skript Objekt von WS-Objekten ist das generische WMI-Objekt, das die Eigenschaften und Methoden definiert, die unabhängig von dem spezifischen WMI-Objekt verwendet werden können, an das das errbemubject-Objekt gebunden ist.
ms.assetid: 33252b49-00d4-4c43-8abe-9368ed82f34b
ms.tgt_platform: multiple
title: Skripterstellung mit "errbemuject"
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3ce9a48779b13f1b1917ad189b2297b60329ba04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131008"
---
# <a name="scripting-with-swbemobject"></a><span data-ttu-id="f5f2e-103">Skripterstellung mit "errbemuject"</span><span class="sxs-lookup"><span data-stu-id="f5f2e-103">Scripting with SWbemObject</span></span>

<span data-ttu-id="f5f2e-104">Das [**Skript Objekt**](swbemobject.md) von WS-Objekten ist das generische WMI-Objekt, das die Eigenschaften und Methoden definiert, die unabhängig von dem spezifischen WMI-Objekt verwendet werden können, an das das **errbemubject** -Objekt gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="f5f2e-104">The [**SWbemObject**](swbemobject.md) scripting object is the generic WMI object, defining properties and methods that can be used regardless of the specific WMI object to which the **SWbemObject** object is bound.</span></span> <span data-ttu-id="f5f2e-105">Alle WMI-Objekte, wie z. b. eine Instanz des [**Win32- \_ Prozesses**](/windows/desktop/CIMWin32Prov/win32-process) oder eine beliebige andere WMI-Datenklasse, werden von " [**errbewbject**](swbemobject.md) " dargestellt und können zusätzlich zu ihren eigenen speziellen Eigenschaften und Methoden die allgemeinen Eigenschaften und Methoden von " **errbemubject** " verwenden.</span><span class="sxs-lookup"><span data-stu-id="f5f2e-105">All WMI objects, such as an instance of [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) or any other WMI data class, are represented by [**SWbemObject**](swbemobject.md) and can use the **SWbemObject** common properties and methods in addition to their own particular properties and methods.</span></span>

<span data-ttu-id="f5f2e-106">Verwenden Sie z. b. das folgende Skript, um alle Instanzen eines [**Win32- \_ Prozesses**](/windows/desktop/CIMWin32Prov/win32-process) zu erhalten, indem Sie die Methode " [**\_ errbemubject. Instance**](swbemobject-instances-.md) " aufrufen.</span><span class="sxs-lookup"><span data-stu-id="f5f2e-106">For example, use the following script to obtain all of the instances of a [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) by calling the [**SWbemObject.Instances\_**](swbemobject-instances-.md) method.</span></span> <span data-ttu-id="f5f2e-107">Der clsobjprocess stellt sowohl die **Win32- \_ Prozess** Klassendefinition als auch ein- [**Austausch Objekt**](swbemobject.md)dar.</span><span class="sxs-lookup"><span data-stu-id="f5f2e-107">The clsobjProcess represents both the **Win32\_Process** class definition and an [**SWbemObject**](swbemobject.md).</span></span>


```VB
strComputer = "."
Set objWMIServices = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
Set clsobjProcess = objWMIServices.Get("Win32_Process")
Set colProcesses = clsobjProcess.Instances_()
For Each Process in colProcesses
    WScript.Echo Process.Name
Next
```



<span data-ttu-id="f5f2e-108">Im folgenden Beispiel wird eine bestimmte Instanz des [**Win32- \_ Dienstanbieter**](/windows/desktop/CIMWin32Prov/win32-service) abgerufen, die den alingdienst darstellt und in objalder gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="f5f2e-108">The following example obtains a specific instance of [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) that represents the Alerter service and stores it in objAlerter.</span></span> <span data-ttu-id="f5f2e-109">Sie können dann entweder die " [**errbewbject**](swbemobject.md) "-Methoden (z. b. "Wscript. Echo objalken. Path") \_ oder die von der Datenklasse definierten Methoden (z. b. WScript. Echo objalen. State) aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="f5f2e-109">You can then call either [**SWbemObject**](swbemobject.md) methods, such as WScript.Echo objAlerter.Path\_, or methods defined by the data class, such as WScript.Echo objAlerter.State.</span></span> <span data-ttu-id="f5f2e-110">objalken, der sowohl eine Instanz des Win32 \_ -Dienstanbieter als auch ein **errbefubject** darstellt.</span><span class="sxs-lookup"><span data-stu-id="f5f2e-110">objAlerter which represents both an instance of Win32\_Service and an **SWbemObject**.</span></span>


```VB
strComputer = "." 
Set objWMIServices = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
Set objAlerter = objWMIServices.Get("Win32_Service.Name='Alerter'")
WScript.Echo objAlerter.Path_
objAlerter.StopService()
WScript.Echo objAlerter.State
```




```VB
For each Prop in myObject.Properties_
    Wscript.Echo Prop.Name
Next
```



<span data-ttu-id="f5f2e-111">Der Aufrufen von " [**errbewbject. \_ instance**](swbemobject-instances-.md) " erhält ein anderes generisches WMI-Skript Objekt, " [**errbewbjectset**](swbemobjectset.md)".</span><span class="sxs-lookup"><span data-stu-id="f5f2e-111">The call to [**SWbemObject.Instances\_**](swbemobject-instances-.md) obtains another generic WMI scripting object, [**SWbemObjectSet**](swbemobjectset.md).</span></span> <span data-ttu-id="f5f2e-112">Wie gezeigt, kann das Objekt " **errbemubjectset** " als [Sammlung](accessing-a-collection.md)behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="f5f2e-112">As shown, the **SWbemObjectSet** object can be treated as a [collection](accessing-a-collection.md).</span></span>


```VB
Set clsobjProcess = objWMIServices.Get("Win32_Process")
```



<span data-ttu-id="f5f2e-113">Sie können die " [**errbemubject**](swbemobject.md) "-Methoden ermitteln, da Sie alle auf einen Unterstrich ( \_ ) enden, z. b. " [**errbemubject. Instance \_**](swbemobject-instances-.md)".</span><span class="sxs-lookup"><span data-stu-id="f5f2e-113">You can identify the [**SWbemObject**](swbemobject.md) methods because they all end with an underscore (\_), for example, [**SWbemObject.Instances\_**](swbemobject-instances-.md).</span></span>

<span data-ttu-id="f5f2e-114">Die Eigenschaften von "errbemubject" [](swbemobject.md)werden von " [**errbemubjectex**](swbemobjectex.md) " erweitert.</span><span class="sxs-lookup"><span data-stu-id="f5f2e-114">[**SWbemObjectEx**](swbemobjectex.md) extends the properties of [**SWbemObject**](swbemobject.md).</span></span> <span data-ttu-id="f5f2e-115">Beispielsweise können Sie jetzt die Daten eines beliebigen WMI-Objekts (z. b. eine Instanz des [**Win32- \_ Prozesses**](/windows/desktop/CIMWin32Prov/win32-process)) durch einen Aufrufen von " [**errbewbjectex. Refresh \_**](swbemobjectex-refresh-.md)" aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="f5f2e-115">For example, you can now update the data of any WMI object, such as an instance of [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process), by a call to [**SWbemObjectEx.Refresh\_**](swbemobjectex-refresh-.md).</span></span>

<span data-ttu-id="f5f2e-116">Im folgenden Beispiel wird gezeigt, wie die Fehler Daten der System Prozess Seite alle fünf Sekunden aktualisiert werden können.</span><span class="sxs-lookup"><span data-stu-id="f5f2e-116">The following example shows how the system process page fault data can be refreshed every five seconds.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2")
Set colProcesses = objWMIService.ExecQuery("SELECT * FROM Win32_Process WHERE Name = 'System'",,48) 
For Each Process in colProcesses
        i = 0
        Do Until i = 5
            i = i + 1
            Wscript.Echo "PageFaults = " & Process.PageFaults 
            Wscript.Sleep 10000
            Process.Refresh_
        Loop
Next
```



<span data-ttu-id="f5f2e-117">Weitere Informationen zum Aktualisieren von Daten mit einem " [**Swap**](swbemrefresher.md) "-Objekt finden Sie unter Aktualisieren von [WMI-Daten in Skripts](refreshing-wmi-data-in-scripts.md).</span><span class="sxs-lookup"><span data-stu-id="f5f2e-117">For more information about refreshing data using an [**SWbemRefresher**](swbemrefresher.md) object, see [Refreshing WMI Data in Scripts](refreshing-wmi-data-in-scripts.md).</span></span>

<span data-ttu-id="f5f2e-118">Mit " [**Swap. Put \_**](swbemobject-put-.md) " und " [**putasync \_**](swbemobject-putasync-.md) " können Sie Änderungen zurück in ein beliebiges WMI-Objekt schreiben.</span><span class="sxs-lookup"><span data-stu-id="f5f2e-118">The [**SWbemObject.Put\_**](swbemobject-put-.md) and [**PutAsync\_**](swbemobject-putasync-.md) allow you to write changes back to any WMI object.</span></span> <span data-ttu-id="f5f2e-119">Diese Methoden übertragen nur Änderungen an einem Objekt im Namespace, in dem das Objekt erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="f5f2e-119">These methods only commit changes to an object in the namespace where the object was created.</span></span> <span data-ttu-id="f5f2e-120">Sie können das Objekt mithilfe von " [**scobemservicesex. Put**](swbemservicesex-put.md) " oder " [**scobemservicesex. putasync**](swbemservicesex-putasync.md)" in einen anderen Namespace schreiben.</span><span class="sxs-lookup"><span data-stu-id="f5f2e-120">You can write the object to a different namespace using [**SWbemServicesEx.Put**](swbemservicesex-put.md) or [**SWbemServicesEx.PutAsync**](swbemservicesex-putasync.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f5f2e-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f5f2e-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5f2e-122">Skript-API für WMI</span><span class="sxs-lookup"><span data-stu-id="f5f2e-122">Scripting API for WMI</span></span>](scripting-api-for-wmi.md)
</dt> <dt>

[<span data-ttu-id="f5f2e-123">Erstellen eines WMI-Skripts</span><span class="sxs-lookup"><span data-stu-id="f5f2e-123">Creating a WMI Script</span></span>](creating-a-wmi-script.md)
</dt> <dt>

[<span data-ttu-id="f5f2e-124">Aktualisieren einer gesamten Instanz</span><span class="sxs-lookup"><span data-stu-id="f5f2e-124">Updating an Entire Instance</span></span>](updating-an-entire-instance.md)
</dt> <dt>

[<span data-ttu-id="f5f2e-125">Aufrufen einer Methode</span><span class="sxs-lookup"><span data-stu-id="f5f2e-125">Calling a Method</span></span>](calling-a-method.md)
</dt> </dl>

 

 
