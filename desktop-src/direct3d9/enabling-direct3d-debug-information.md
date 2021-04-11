---
description: Versuchen Sie, während des Debuggens Weitere Informationen über Direct3D-Objekte zu erhalten? Der folgende Screenshot zeigt beispielsweise, was Sie in der Regel sehen, wenn Sie eine Direct3D-Schnittstelle im Überwachungs Fenster sehen.
ms.assetid: 365451f8-e93e-4cc4-b688-2e668518c245
title: Aktivieren von Direct3D-Debuginformationen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17bb46cf8658d0417d021faa6bdbefd10822d1dd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123355"
---
# <a name="enabling-direct3d-debug-information-direct3d-9"></a><span data-ttu-id="2ac66-104">Aktivieren von Direct3D-Debuginformationen (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="2ac66-104">Enabling Direct3D Debug Information (Direct3D 9)</span></span>

<span data-ttu-id="2ac66-105">Versuchen Sie, während des Debuggens Weitere Informationen über Direct3D-Objekte zu erhalten?</span><span class="sxs-lookup"><span data-stu-id="2ac66-105">Are you trying to find out more information about Direct3D objects during debug?</span></span> <span data-ttu-id="2ac66-106">Der folgende Screenshot zeigt beispielsweise, was Sie in der Regel sehen, wenn Sie eine Direct3D-Schnittstelle im Überwachungs Fenster sehen.</span><span class="sxs-lookup"><span data-stu-id="2ac66-106">For instance, the following screen shot shows what you typically see when you look at a Direct3D interface in the watch window.</span></span>

![Screenshot einer Direct3D-Schnittstelle im Fenster "überwachen"](images/d3d-debug-info1.png)

<span data-ttu-id="2ac66-108">Sie können die kerndebugobjekte aktivieren, sodass ein gespiegeltes Objekt, das alle Eigenschaften des-Objekts enthält, im Überwachungs Fenster angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="2ac66-108">You can enable the core debug objects so that a mirrored object which contains all of the properties of the object can be viewed in the watch window.</span></span> <span data-ttu-id="2ac66-109">Fügen Sie einfach die folgende \# Definition in Ihren Code vor der Datei d3d9. h ein:</span><span class="sxs-lookup"><span data-stu-id="2ac66-109">Simply include the following \#define in your code before the D3D9.h file:</span></span>


```
#define D3D_DEBUG_INFO
```



<span data-ttu-id="2ac66-110">Um Debuginformationen zu aktivieren, \# muss die Definition vor der Datei d3d9. h erstellt werden (jedes Programm, das dxut verwendet, aktiviert automatisch D3D- \_ Debuginformationen, \_ Wenn das Programm für das Debuggen kompiliert wird).</span><span class="sxs-lookup"><span data-stu-id="2ac66-110">To enable debug information, the \#define must get built before the D3D9.h file (Any program using DXUT will automatically enable D3D\_DEBUG\_INFO when the program is compiled for debug).</span></span> <span data-ttu-id="2ac66-111">Wenn Sie ein SDK-Beispiel ausführen, können Sie dies in "dxstdafx. h" sehen (was sich auf alle C++-Beispiele auswirkt).</span><span class="sxs-lookup"><span data-stu-id="2ac66-111">If you are running a SDK sample, you can see this in DXStdAfx.h (which affects all the C++ samples).</span></span> <span data-ttu-id="2ac66-112">Sie müssen auch die Debug Direct3D Runtime ausführen (die bei Bedarf über die Systemsteuerung aktiviert werden kann).</span><span class="sxs-lookup"><span data-stu-id="2ac66-112">You must also be running the debug Direct3D runtime (which can be enabled from the Control Panel if necessary).</span></span>

<span data-ttu-id="2ac66-113">Im folgenden finden Sie ein Beispiel für die Verwendung des [basichlsl](https://msdn.microsoft.com/library/Ee416223(v=VS.85).aspx)-Beispiels.</span><span class="sxs-lookup"><span data-stu-id="2ac66-113">Here's an example using the [BasicHLSL Sample](https://msdn.microsoft.com/library/Ee416223(v=VS.85).aspx).</span></span>

1.  <span data-ttu-id="2ac66-114">Fügen Sie die \# Definition der Datei "dxstdafx. h" vor Zeile 37 hinzu.</span><span class="sxs-lookup"><span data-stu-id="2ac66-114">Add the \#define to the Dxstdafx.h file before line 37.</span></span>
2.  <span data-ttu-id="2ac66-115">Erstellen Sie ein debugprojekt.</span><span class="sxs-lookup"><span data-stu-id="2ac66-115">Build a debug project.</span></span>
3.  <span data-ttu-id="2ac66-116">Festlegen eines Breakpoints in Zeile 307 in basichlsl. cpp</span><span class="sxs-lookup"><span data-stu-id="2ac66-116">Set a breakpoint at line 307 in BasicHLSL.cpp</span></span>
4.  <span data-ttu-id="2ac66-117">Führen Sie den Debugger aus.</span><span class="sxs-lookup"><span data-stu-id="2ac66-117">Run the debugger.</span></span>

<span data-ttu-id="2ac66-118">Der folgende Screenshot zeigt die Art detaillierter Informationen, die Sie über ein Direct3D-Textur Objekt aus dem Fenster Überwachen erhalten können.</span><span class="sxs-lookup"><span data-stu-id="2ac66-118">The following screen shot shows the kind of detailed information you can get about a Direct3D texture object from the watch window.</span></span>

![Screenshot eines Direct3D-Textur Objekts im Fenster "überwachen"](images/d3d-debug-info2.png)

> [!Note]
>
> <span data-ttu-id="2ac66-120">Die Objekt Eigenschaftsnamen sind sichtbar, und die Werte sind nur dann korrekt, wenn die Debug-Laufzeit aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="2ac66-120">The object property names are visible and the values are correct only when the debug runtime is enabled.</span></span> <span data-ttu-id="2ac66-121">Bei der Ausführung für die Einzelhandels Laufzeit sind die Werte ungültig.</span><span class="sxs-lookup"><span data-stu-id="2ac66-121">When running against the retail runtime, the values are invalid.</span></span>

 

## <a name="use-the-call-stack-for-extended-debug"></a><span data-ttu-id="2ac66-122">Verwenden der aufrufsstapel für erweitertes Debuggen</span><span class="sxs-lookup"><span data-stu-id="2ac66-122">Use the Call Stack for Extended Debug</span></span>

<span data-ttu-id="2ac66-123">Wenn Direct3D Debug aktiviert ist, können Sie sich auch bei jeder Erstellung eines Objekts einen Aufruf Stapel ansehen.</span><span class="sxs-lookup"><span data-stu-id="2ac66-123">With Direct3D debug enabled, you can also look at a call stack each time an object is created.</span></span> <span data-ttu-id="2ac66-124">Dadurch wird die Anwendung sehr langsam, kann jedoch verwendet werden, um nach Ressourcenverlusten zu suchen.</span><span class="sxs-lookup"><span data-stu-id="2ac66-124">This will make your application very slow, but can be used to check for resource leaks.</span></span> <span data-ttu-id="2ac66-125">Legen Sie den folgenden Registrierungsschlüssel auf 1 fest, um die-aufrufsstapel zu schreiben:</span><span class="sxs-lookup"><span data-stu-id="2ac66-125">To write out the call stack, set the following registry key to 1:</span></span>


```
\\HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\Direct3D\\
D3D9Debugging\\EnableCreationStack
```



<span data-ttu-id="2ac66-126">Wenn Sie Ihre Anwendung mit aktiviertem Debuggen entwickeln, erhalten Sie Zugriff auf diese zusätzliche Variable:</span><span class="sxs-lookup"><span data-stu-id="2ac66-126">Building your application with debug enabled will give you access to this additional variable:</span></span>


```
  LPCWSTR CreationCallStack;
```



<span data-ttu-id="2ac66-127">Diese Variable speichert die Aufruf Stapel jedes Mal, wenn ein Objekt erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="2ac66-127">This variable will store the call stack each time that an object is created.</span></span> <span data-ttu-id="2ac66-128">Dadurch wird die Anwendung sehr langsam, kann jedoch zum Debuggen von Ressourcenverlusten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2ac66-128">This will make your application very slow, but can be used to debug resource leaks.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2ac66-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2ac66-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ac66-130">Programmiertipps</span><span class="sxs-lookup"><span data-stu-id="2ac66-130">Programming Tips</span></span>](programming-tips.md)
</dt> </dl>

 

 



