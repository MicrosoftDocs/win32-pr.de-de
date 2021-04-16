---
description: Laden eines Diagramms aus einem externen Prozess
ms.assetid: 1c657c7f-46d7-4feb-88a7-4a3227c9070b
title: Laden eines Diagramms aus einem externen Prozess
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eac42db3a87b00b1cb8f3a9ae5297215ae9bd3fa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104551414"
---
# <a name="loading-a-graph-from-an-external-process"></a><span data-ttu-id="2f269-103">Laden eines Diagramms aus einem externen Prozess</span><span class="sxs-lookup"><span data-stu-id="2f269-103">Loading a Graph From an External Process</span></span>

<span data-ttu-id="2f269-104">GraphEdit kann ein von einem externen Prozess erstelltes Filter Diagramm laden.</span><span class="sxs-lookup"><span data-stu-id="2f269-104">GraphEdit can load a filter graph created by an external process.</span></span> <span data-ttu-id="2f269-105">Mit dieser Funktion können Sie genau sehen, welches Filter Diagramm für Ihre Anwendung erstellt wird, und zwar nur über einen minimalen zusätzlichen Code in Ihrer Anwendung.</span><span class="sxs-lookup"><span data-stu-id="2f269-105">With this feature, you can see exactly what filter graph your application builds, with only a minimal amount of additional code in your application.</span></span>

> [!Note]  
> <span data-ttu-id="2f269-106">Für dieses Feature ist Windows 2000, Windows XP oder höher erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2f269-106">This feature requires Windows 2000, Windows XP, or later.</span></span>

 

> [!Note]  
> <span data-ttu-id="2f269-107">Ab Windows Vista müssen Sie proppage.dll registrieren, um dieses Feature zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="2f269-107">Starting in Windows Vista, you must register proppage.dll to enable this feature.</span></span> <span data-ttu-id="2f269-108">Proppage.dll ist im Windows SDK enthalten.</span><span class="sxs-lookup"><span data-stu-id="2f269-108">Proppage.dll is included in the Windows SDK.</span></span>

 

<span data-ttu-id="2f269-109">Die Anwendung muss die Filter Diagramm Instanz in der laufenden Objekttabelle (rot) registrieren.</span><span class="sxs-lookup"><span data-stu-id="2f269-109">The application must register the filter graph instance in the Running Object Table (ROT).</span></span> <span data-ttu-id="2f269-110">Die rot ist eine Global zugängliche Nachschlage Tabelle, in der die Ausführung von Objekten nachverfolgt wird.</span><span class="sxs-lookup"><span data-stu-id="2f269-110">The ROT is a globally accessible look-up table that keeps track of running objects.</span></span> <span data-ttu-id="2f269-111">Objekte werden im Rot von Moniker registriert.</span><span class="sxs-lookup"><span data-stu-id="2f269-111">Objects are registered in the ROT by moniker.</span></span> <span data-ttu-id="2f269-112">Um eine Verbindung mit dem Diagramm herzustellen, durchsucht GraphEdit die rot nach Monikern, deren Anzeige Name mit einem bestimmten Format übereinstimmt:</span><span class="sxs-lookup"><span data-stu-id="2f269-112">To connect to the graph, GraphEdit searches the ROT for monikers whose display name matches a particular format:</span></span>


```C++
!FilterGraph X pid Y
```



<span data-ttu-id="2f269-113">Dabei steht *X* für die hexadezimale Adresse des Filter Graph-Managers, und *Y* für die Prozess-ID, auch als hexadezimal.</span><span class="sxs-lookup"><span data-stu-id="2f269-113">where *X* is the hexadecimal address of the Filter Graph Manager, and *Y* is the process id, also in hexadecimal.</span></span>

<span data-ttu-id="2f269-114">Wenn Ihre Anwendung das Filter Diagramm erstmalig erstellt, müssen Sie die folgende Funktion aufzurufen:</span><span class="sxs-lookup"><span data-stu-id="2f269-114">When your application first creates the filter graph, call the following function:</span></span>


```C++
HRESULT AddToRot(IUnknown *pUnkGraph, DWORD *pdwRegister) 
{
    IMoniker * pMoniker = NULL;
    IRunningObjectTable *pROT = NULL;

    if (FAILED(GetRunningObjectTable(0, &pROT))) 
    {
        return E_FAIL;
    }
    
    const size_t STRING_LENGTH = 256;

    WCHAR wsz[STRING_LENGTH];
 
   StringCchPrintfW(
        wsz, STRING_LENGTH, 
        L"FilterGraph %08x pid %08x", 
        (DWORD_PTR)pUnkGraph, 
        GetCurrentProcessId()
        );
    
    HRESULT hr = CreateItemMoniker(L"!", wsz, &pMoniker);
    if (SUCCEEDED(hr)) 
    {
        hr = pROT->Register(ROTFLAGS_REGISTRATIONKEEPSALIVE, pUnkGraph,
            pMoniker, pdwRegister);
        pMoniker->Release();
    }
    pROT->Release();
    
    return hr;
}
```



<span data-ttu-id="2f269-115">Diese Funktion erstellt einen Moniker und einen neuen rot-Eintrag für das Filter Diagramm.</span><span class="sxs-lookup"><span data-stu-id="2f269-115">This function creates a moniker and a new ROT entry for the filter graph.</span></span> <span data-ttu-id="2f269-116">Der erste Parameter ist ein Zeiger auf das Filter Diagramm.</span><span class="sxs-lookup"><span data-stu-id="2f269-116">The first parameter is a pointer to the filter graph.</span></span> <span data-ttu-id="2f269-117">Der zweite Parameter erhält einen Wert, der den neuen rot-Eintrag identifiziert.</span><span class="sxs-lookup"><span data-stu-id="2f269-117">The second parameter receives a value that identifies the new ROT entry.</span></span> <span data-ttu-id="2f269-118">Bevor die Anwendung das Filter Diagramm freigibt, wird die folgende Funktion aufgerufen, um den rot-Eintrag zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="2f269-118">Before the application releases the filter graph, call the following function to remove the ROT entry.</span></span> <span data-ttu-id="2f269-119">Der *pdwregister* -Parameter ist der Bezeichner, der von der addtorot-Funktion zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="2f269-119">The *pdwRegister* parameter is the identifier returned by the AddToRot function.</span></span>


```C++
void RemoveFromRot(DWORD pdwRegister)
{
    IRunningObjectTable *pROT;
    if (SUCCEEDED(GetRunningObjectTable(0, &pROT))) {
        pROT->Revoke(pdwRegister);
        pROT->Release();
    }
}
```



<span data-ttu-id="2f269-120">Im folgenden Codebeispiel wird gezeigt, wie diese Funktionen aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="2f269-120">The following code example shows how to call these functions.</span></span> <span data-ttu-id="2f269-121">In diesem Beispiel wird der Code, mit dem rot-Einträge hinzugefügt und entfernt werden, bedingt kompiliert, sodass er nur in Debugbuilds enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="2f269-121">In this example, the code that adds and removes ROT entries is conditionally compiled, so that it is included only in debug builds.</span></span>


```C++
IGraphBuilder *pGraph;
DWORD dwRegister;
    
// Create the filter graph manager.
CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER,
                        IID_IGraphBuilder, (void **)&pGraph);
#ifdef _DEBUG
hr = AddToRot(pGraph, &dwRegister);
#endif

// Rest of the application (not shown).

#ifdef _DEBUG
RemoveFromRot(dwRegister);
#endif
pGraph->Release();
```



<span data-ttu-id="2f269-122">Um das Filter Diagramm in GraphEdit anzuzeigen, führen Sie Ihre Anwendung und GraphEdit gleichzeitig aus.</span><span class="sxs-lookup"><span data-stu-id="2f269-122">To view the filter graph in GraphEdit, run your application and GraphEdit at the same time.</span></span> <span data-ttu-id="2f269-123">Klicken Sie im Menü "GraphEdit- **Datei** " auf **mit Remote Diagramm verbinden...** Wählen Sie im Dialogfeld **Verbindung mit Graph herstellen** die Prozess-ID (PID) Ihrer Anwendung aus, und klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="2f269-123">In the GraphEdit **File** menu, click **Connect to Remote Graph...** In the **Connect To Graph** dialog box, select the process id (pid) of your application and click **OK**.</span></span> <span data-ttu-id="2f269-124">GraphEdit lädt das Filter Diagramm und zeigt es an.</span><span class="sxs-lookup"><span data-stu-id="2f269-124">GraphEdit loads the filter graph and displays it.</span></span> <span data-ttu-id="2f269-125">Verwenden Sie in diesem Diagramm keine anderen GraphEdit-Funktionen – Dies kann zu unerwarteten Ergebnissen führen.</span><span class="sxs-lookup"><span data-stu-id="2f269-125">Don't use any other GraphEdit features on this graph—it might cause unexpected results.</span></span> <span data-ttu-id="2f269-126">Fügen Sie z. b. keine Filter hinzu, oder entfernen Sie die Filter, und starten Sie das Diagramm nicht.</span><span class="sxs-lookup"><span data-stu-id="2f269-126">For example, don't add or remove filters, or stop and start the graph.</span></span> <span data-ttu-id="2f269-127">Schließen Sie GraphEdit, bevor Sie die Anwendung verlassen.</span><span class="sxs-lookup"><span data-stu-id="2f269-127">Close GraphEdit before exiting your application.</span></span>

> [!Note]  
> <span data-ttu-id="2f269-128">Die Anwendung kann beim Beenden verschiedene Bestätigungen erreichen.</span><span class="sxs-lookup"><span data-stu-id="2f269-128">Your application might hit various asserts when it exits.</span></span> <span data-ttu-id="2f269-129">Sie können diese Fehler ignorieren.</span><span class="sxs-lookup"><span data-stu-id="2f269-129">You can ignore these.</span></span>

 

<span data-ttu-id="2f269-130">Die folgende Abbildung zeigt das Dialogfeld **Verbindung mit Graph herstellen** .</span><span class="sxs-lookup"><span data-stu-id="2f269-130">The following illustration shows the **Connect To Graph** dialog box.</span></span>

![mit Diagramm verbinden](images/gedit-spy.png)

<span data-ttu-id="2f269-132">Wenn GraphEdit das Diagramm lädt, wird es im Kontext der Zielanwendung ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2f269-132">When GraphEdit loads the graph, it executes in the context of the target application.</span></span> <span data-ttu-id="2f269-133">Daher kann GraphEdit blockieren, weil es auf den Thread wartet.</span><span class="sxs-lookup"><span data-stu-id="2f269-133">Therefore, GraphEdit might block because it is waiting for the thread.</span></span> <span data-ttu-id="2f269-134">Dies kann z. b. vorkommen, wenn Sie den Code im Debugger schrittweise durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="2f269-134">For example, this can occur if you are stepping through your code in the debugger.</span></span>

<span data-ttu-id="2f269-135">Diese Funktion sollte nur in Debugbuilds der Anwendung und nicht in Einzelhandels Builds verwendet werden, da es anderen Anwendungen ermöglicht, das Filter Diagramm anzuzeigen oder zu steuern.</span><span class="sxs-lookup"><span data-stu-id="2f269-135">This feature should be used only in debug builds of your application, not retail builds, because it enables other applications to view or control the filter graph.</span></span>

## <a name="connecting-to-a-remote-graph-from-the-command-line"></a><span data-ttu-id="2f269-136">Herstellen einer Verbindung mit einem Remote Diagramm über die Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="2f269-136">Connecting to a Remote Graph from the Command Line</span></span>

<span data-ttu-id="2f269-137">GraphEdit unterstützt eine Befehlszeilenoption zum automatischen Laden eines Remote Diagramms beim Start.</span><span class="sxs-lookup"><span data-stu-id="2f269-137">GraphEdit supports a command-line option to load a remote graph automatically on startup.</span></span> <span data-ttu-id="2f269-138">Die Syntax lautet:</span><span class="sxs-lookup"><span data-stu-id="2f269-138">The syntax is:</span></span>


```C++
GraphEdt -a moniker
```



<span data-ttu-id="2f269-139">Dabei ist der *Moniker* ein Moniker, der mithilfe der zuvor beschriebenen addtorot-Funktion erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="2f269-139">where *moniker* is a moniker created using the AddToRot function, described previously.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2f269-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2f269-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f269-141">Simulieren der Diagramm Erstellung mit GraphEdit</span><span class="sxs-lookup"><span data-stu-id="2f269-141">Simulating Graph Building with GraphEdit</span></span>](simulating-graph-building-with-graphedit.md)
</dt> </dl>

 

 



