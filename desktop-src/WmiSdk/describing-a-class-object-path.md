---
description: Ein Klassenobjekt Pfad beschreibt den Speicherort einer Klasse innerhalb eines Namespace.
ms.assetid: 5ae95707-d023-4102-9b41-140c54b0c5b7
ms.tgt_platform: multiple
title: Beschreiben eines Klassenobjekt Pfads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1cfd603ea3b6de151d297a7f4b6fc8a2a27dfda
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362381"
---
# <a name="describing-a-class-object-path"></a><span data-ttu-id="16720-103">Beschreiben eines Klassenobjekt Pfads</span><span class="sxs-lookup"><span data-stu-id="16720-103">Describing a Class Object Path</span></span>

<span data-ttu-id="16720-104">Ein Klassenobjekt Pfad beschreibt den Speicherort einer Klasse innerhalb eines Namespace.</span><span class="sxs-lookup"><span data-stu-id="16720-104">A class object path describes the location of a class within a namespace.</span></span>

<span data-ttu-id="16720-105">Mit den folgenden Methoden können Sie einen Objekt Pfad angeben:</span><span class="sxs-lookup"><span data-stu-id="16720-105">You can use the following methods to specify an object path:</span></span>

-   <span data-ttu-id="16720-106">Ein vollständiger Objekt Pfad zu einer Klasse fügt den Klassennamen an einen Namespace Pfad an.</span><span class="sxs-lookup"><span data-stu-id="16720-106">A full object path to a class appends the class name to a namespace path.</span></span>

    <span data-ttu-id="16720-107">Im folgenden Beispiel wird der Speicherort der [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) -Klasse im \\ root \\ CIMV2-Namespace auf dem Server mit dem Namen admin gezeigt.</span><span class="sxs-lookup"><span data-stu-id="16720-107">The following example shows the location of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class within the \\root\\cimv2 namespace on the server named Admin.</span></span>

    ``` syntax
    \\Admin\Root\CimV2:Win32_LogicalDisk
    ```

-   <span data-ttu-id="16720-108">Ein relativer Objekt Pfad stellt eine Klasse dar, die sich im aktuellen Namespace befindet.</span><span class="sxs-lookup"><span data-stu-id="16720-108">A relative object path represents a class that resides in the current namespace.</span></span> <span data-ttu-id="16720-109">Ein relativer Objekt Pfad zu einer Klasse enthält nur den Klassennamen.</span><span class="sxs-lookup"><span data-stu-id="16720-109">A relative object path to a class contains only the class name.</span></span>

    <span data-ttu-id="16720-110">Das folgende Beispiel zeigt den relativen Pfad zur [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="16720-110">The following example shows the relative path to the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class.</span></span>

    ``` syntax
    Win32_LogicalDisk
    ```

<span data-ttu-id="16720-111">Wenn Sie einen Klassennamen Abfragen, aber keine Instanzen angeben, gibt WMI die Klassendefinition zurück.</span><span class="sxs-lookup"><span data-stu-id="16720-111">When you query for a class name but specify no instances, WMI returns the class definition.</span></span> <span data-ttu-id="16720-112">Im folgenden Verfahren wird beschrieben, wie eine Klassendefinition in VBScript abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="16720-112">The following procedure describes how to retrieve a class definition in VBScript.</span></span>

<span data-ttu-id="16720-113">**So rufen Sie eine Klassendefinition in VBScript ab**</span><span class="sxs-lookup"><span data-stu-id="16720-113">**To retrieve a class definition in VBScript**</span></span>

-   <span data-ttu-id="16720-114">Sie können die monikerverbindung entweder mit einer Abfrage oder einem [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx)-Objekt verwenden.</span><span class="sxs-lookup"><span data-stu-id="16720-114">You can use the moniker connection either with a query or [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx).</span></span> <span data-ttu-id="16720-115">Sie können auch " [**Swap Services. Get**](swbemservices-get.md)" verwenden.</span><span class="sxs-lookup"><span data-stu-id="16720-115">You can also use [**SWbemServices.Get**](swbemservices-get.md).</span></span>

    <span data-ttu-id="16720-116">Im folgenden Beispiel wird gezeigt, wie [GetObject](/previous-versions//kdccchxa(v=vs.85)) verwendet wird, um eine Klassendefinition zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="16720-116">The following example shows how to use [GetObject](/previous-versions//kdccchxa(v=vs.85)) to get a class definition.</span></span>

    ```VB
    strComputer = "."
    Set objWMIService = GetObject("winmgmts:" _
       & "{impersonationLevel=impersonate}!\\" _
       & strComputer & "\root\cimv2:Win32_Printer")
    ```

    

    <span data-ttu-id="16720-117">Im folgenden Beispiel wird gezeigt, wie eine-Klassendefinition abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="16720-117">The following example shows how to query for a class definition.</span></span>

    ```VB
    strComputer = "."
    Set objWMIService = GetObject("winmgmts:" _
        & "{impersonationLevel=impersonate}!\\" _
        & strComputer & "\root\cimv2")
    Set colInstalledPrinters =  objWMIService.ExecQuery _
        ("Select * from Win32_Printer")
    ```

    

<span data-ttu-id="16720-118">Sie können eine Klassendefinition in C++ abrufen, indem Sie nur den Klassennamen und keinen Pfad zu einer bestimmten Instanz angeben.</span><span class="sxs-lookup"><span data-stu-id="16720-118">You can retrieve a class definition in C++ by specifying only the class name and no path to a particular instance.</span></span> <span data-ttu-id="16720-119">Im folgenden Verfahren wird beschrieben, wie eine Klassendefinition in C++ abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="16720-119">The following procedure describes how to retrieve a class definition in C++.</span></span>

<span data-ttu-id="16720-120">**So rufen Sie eine Klassendefinition in C++ ab**</span><span class="sxs-lookup"><span data-stu-id="16720-120">**To retrieve a class definition in C++**</span></span>

-   <span data-ttu-id="16720-121">Aufrufen der Funktionen [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) oder [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) .</span><span class="sxs-lookup"><span data-stu-id="16720-121">Make a call to the [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) or [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) functions.</span></span>

    <span data-ttu-id="16720-122">Im folgenden Beispiel wird gezeigt, wie die [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) -Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="16720-122">The following example shows how to call the [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) function.</span></span>

    ```C++
    IWbemServices* pSvcs = 0;

    BSTR Path = SysAllocString(L"Win32_LogicalDisk");
    IWbemClassObject *pDiskClass = 0;
    pSvcs->GetObject(Path, 0, 0, &pDiskClass, 0);
    ```

    

    <span data-ttu-id="16720-123">Das vorherige Codebeispiel erfordert, dass die folgende \# include-Anweisung ordnungsgemäß kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="16720-123">The previous code example requires the following \#include statement to compile correctly.</span></span>

    ```C++
    #include <wbemidl.h>
    ```

    

 

 
