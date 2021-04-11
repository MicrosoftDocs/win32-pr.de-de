---
description: Anwendungen können einen Aktivierungs Kontext verwalten, indem Sie die Aktivierungs Kontextfunktionen direkt aufrufen.
ms.assetid: 606147a8-435d-43d4-8fb5-79d2d1a8d870
title: Verwenden der Aktivierungs Kontext-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62b3aec5b7840e70e8fae93575e65c2f06668936
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128809"
---
# <a name="using-the-activation-context-api"></a><span data-ttu-id="e12ea-103">Verwenden der Aktivierungs Kontext-API</span><span class="sxs-lookup"><span data-stu-id="e12ea-103">Using the Activation Context API</span></span>

<span data-ttu-id="e12ea-104">Anwendungen können einen [Aktivierungs Kontext](activation-contexts.md) verwalten, indem Sie die Aktivierungs Kontextfunktionen direkt aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e12ea-104">Applications can manage an [activation context](activation-contexts.md) by directly calling the activation context functions.</span></span> <span data-ttu-id="e12ea-105">Aktivierungs Kontexte sind Datenstrukturen im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="e12ea-105">Activation contexts are data structures in memory.</span></span> <span data-ttu-id="e12ea-106">Das System kann die Informationen im Aktivierungs Kontext verwenden, um eine Anwendung so umzuleiten, dass Sie eine bestimmte dll-Version, com-Objektinstanz oder eine benutzerdefinierte Fensterversion lädt.</span><span class="sxs-lookup"><span data-stu-id="e12ea-106">The system can use the information in the activation context to redirect an application to load a particular DLL version, COM object instance, or custom window version.</span></span> <span data-ttu-id="e12ea-107">Weitere Informationen finden Sie unter [Aktivierungs Kontext Referenz](activation-context-reference.md).</span><span class="sxs-lookup"><span data-stu-id="e12ea-107">For more information, see [Activation Context Reference](activation-context-reference.md).</span></span>

<span data-ttu-id="e12ea-108">Die API (Application Programming Interface) kann verwendet werden, um den Aktivierungs Kontext zu verwalten und Versions benannte Objekte mit [Manifesten](manifests.md)zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e12ea-108">The application programming interface (API) can be used to manage the activation context and create version-named objects with [manifests](manifests.md).</span></span> <span data-ttu-id="e12ea-109">Die folgenden beiden Szenarien veranschaulichen, wie eine Anwendung einen Aktivierungs Kontext verwalten kann, indem die Aktivierungs Kontextfunktionen direkt aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="e12ea-109">The following two scenarios illustrate how an application can manage an activation context by directly calling the activation context functions.</span></span> <span data-ttu-id="e12ea-110">In den meisten Fällen wird der Aktivierungs Kontext jedoch vom System verwaltet.</span><span class="sxs-lookup"><span data-stu-id="e12ea-110">In most cases however, the activation context is managed by the system.</span></span> <span data-ttu-id="e12ea-111">Anwendungsentwickler und Assemblyanbieter müssen häufig keine Aufrufe an den Stapel vornehmen, um den Aktivierungs Kontext zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="e12ea-111">Application developers and assembly providers do not commonly need to make calls to the stack to manage the activation context.</span></span>

-   <span data-ttu-id="e12ea-112">Prozesse und Anwendungen, die Dereferenzierungs-oder Dispatch-Ebenen implementieren.</span><span class="sxs-lookup"><span data-stu-id="e12ea-112">Processes and applications that implement indirection or dispatch layers.</span></span>

    <span data-ttu-id="e12ea-113">Beispielsweise ein Benutzer, der Aktivierungs Kontexte in der Ereignisschleife verwaltet.</span><span class="sxs-lookup"><span data-stu-id="e12ea-113">For example, a user managing activation contexts in the event loop.</span></span> <span data-ttu-id="e12ea-114">Jedes Mal, wenn auf das Fenster zugegriffen wird, z. b. durch Bewegen des Mauszeigers über das Fenster, wird [**activateactctx**](/windows/desktop/api/Winbase/nf-winbase-activateactctx) aufgerufen, das den aktuellen Aktivierungs Kontext für die Ressource aktiviert, wie im folgenden Code Fragment dargestellt.</span><span class="sxs-lookup"><span data-stu-id="e12ea-114">Each time the window is accessed, such as by moving the mouse over the window, [**ActivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-activateactctx) is called, which activates the current activation context for the resource, as shown in the following code fragment.</span></span>

    <dl> <span data-ttu-id="e12ea-115">Handle von hactctx;</span><span class="sxs-lookup"><span data-stu-id="e12ea-115">HANDLE hActCtx;</span></span>  
    <span data-ttu-id="e12ea-116">"Kreatewindow ();"</span><span class="sxs-lookup"><span data-stu-id="e12ea-116">CreateWindow();</span></span>  
    <span data-ttu-id="e12ea-117">...</span><span class="sxs-lookup"><span data-stu-id="e12ea-117">...</span></span>  
    <span data-ttu-id="e12ea-118">Getcurrentactctx (&ActCtx);</span><span class="sxs-lookup"><span data-stu-id="e12ea-118">GetCurrentActCtx(&ActCtx);</span></span>  
    <span data-ttu-id="e12ea-119">...</span><span class="sxs-lookup"><span data-stu-id="e12ea-119">...</span></span>  
    <span data-ttu-id="e12ea-120">Releaseactctx (&ActCtx);</span><span class="sxs-lookup"><span data-stu-id="e12ea-120">ReleaseActCtx(&ActCtx);</span></span>  
    </dl>

    <span data-ttu-id="e12ea-121">Im folgenden Code Fragment werden die entsprechenden Aktivierungs Kontexte von der API-Funktion aktiviert, bevor [**callwindowproc**](/windows/win32/api/winuser/nf-winuser-callwindowproca)aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="e12ea-121">In the following code fragment, the API function activates the appropriate activation contexts before calling [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca).</span></span> <span data-ttu-id="e12ea-122">Wenn **callwindowproc** aufgerufen wird, wird dieser Kontext verwendet, um eine Nachricht an Windows zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="e12ea-122">When **CallWindowProc** is called, it uses this context to pass a message to Windows.</span></span> <span data-ttu-id="e12ea-123">Wenn alle Ressourcen Vorgänge abgeschlossen sind, deaktiviert die Funktion den Kontext.</span><span class="sxs-lookup"><span data-stu-id="e12ea-123">When all resource operations have completed, the function will deactivate the context.</span></span>

    <dl> <span data-ttu-id="e12ea-124">ULONG \_ ptr ulpcookie;</span><span class="sxs-lookup"><span data-stu-id="e12ea-124">ULONG\_PTR ulpCookie;</span></span>  
    <span data-ttu-id="e12ea-125">Handle von hactctx;</span><span class="sxs-lookup"><span data-stu-id="e12ea-125">HANDLE hActCtx;</span></span>  
    <span data-ttu-id="e12ea-126">if (activateactctx (hactctx, &ulpcookie))</span><span class="sxs-lookup"><span data-stu-id="e12ea-126">if(ActivateActCtx(hActCtx, &ulpCookie))</span></span>  
    <span data-ttu-id="e12ea-127">{</span><span class="sxs-lookup"><span data-stu-id="e12ea-127">{</span></span>  
    <span data-ttu-id="e12ea-128">...</span><span class="sxs-lookup"><span data-stu-id="e12ea-128">...</span></span>  
    <span data-ttu-id="e12ea-129">Callwindowproc (...);</span><span class="sxs-lookup"><span data-stu-id="e12ea-129">CallWindowProc(...);</span></span>  
    <span data-ttu-id="e12ea-130">...</span><span class="sxs-lookup"><span data-stu-id="e12ea-130">...</span></span>  
    <span data-ttu-id="e12ea-131">Deactivateactctx (0, ulpcookie);</span><span class="sxs-lookup"><span data-stu-id="e12ea-131">DeactivateActCtx(0, ulpCookie);</span></span>  
    <span data-ttu-id="e12ea-132">}</span><span class="sxs-lookup"><span data-stu-id="e12ea-132">}</span></span>  
    </dl>

-   <span data-ttu-id="e12ea-133">Delegatschutzschicht.</span><span class="sxs-lookup"><span data-stu-id="e12ea-133">Delegator dispatch layer.</span></span>

    <span data-ttu-id="e12ea-134">Dieses Szenario gilt für Manager, die mehrere Entitäten mit einer gemeinsamen API-Schicht verwalten, z. b. Treiber-Manager.</span><span class="sxs-lookup"><span data-stu-id="e12ea-134">This scenario applies to managers that manage multiple entities with a common API layer, such as a driver manager.</span></span> <span data-ttu-id="e12ea-135">Obwohl es noch nicht implementiert wurde, wäre dies ein Beispiel für den ODBC-Treiber.</span><span class="sxs-lookup"><span data-stu-id="e12ea-135">Although it has not yet been implemented, an example of this would be the ODBC driver.</span></span>

    <span data-ttu-id="e12ea-136">In diesem Szenario kann die mittlere Ebene Assemblybindungen verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="e12ea-136">In this scenario, the middle layer becomes capable of processing assembly bindings.</span></span> <span data-ttu-id="e12ea-137">Um den Versions spezifischen Bindungs Treiber zu erhalten, müssen die Verleger ein Manifest bereitstellen und Abhängigkeiten für bestimmte Komponenten in diesem Manifest angeben.</span><span class="sxs-lookup"><span data-stu-id="e12ea-137">To get the version-specific binding driver, publishers must provide a manifest and specify dependencies on specific components in that manifest.</span></span> <span data-ttu-id="e12ea-138">Die Basisanwendung bindet nicht dynamisch an die-Komponenten. zur Laufzeit verwaltet der Treiber-Manager die Aufrufe.</span><span class="sxs-lookup"><span data-stu-id="e12ea-138">The base application does not dynamically bind to the components; at run time, the driver manager manages the calls.</span></span> <span data-ttu-id="e12ea-139">Wenn der ODBC-Treiber auf der Grundlage der Verbindungs Zeichenfolge aufgerufen wird, wird der entsprechende Treiber geladen.</span><span class="sxs-lookup"><span data-stu-id="e12ea-139">When the ODBC driver is called based on the connect string it loads the appropriate driver.</span></span> <span data-ttu-id="e12ea-140">Anschließend wird der Aktivierungs Kontext mithilfe der Informationen in der Assembly Manifest-Datei erstellt.</span><span class="sxs-lookup"><span data-stu-id="e12ea-140">It then creates the activation context using the information in the assembly manifest file.</span></span>

    <span data-ttu-id="e12ea-141">Ohne das Manifest ist die Standardaktion für den Treiber die Verwendung desselben Kontexts, der von der Anwendung angegeben wird – in diesem Beispiel Version 2 von msvcrt.</span><span class="sxs-lookup"><span data-stu-id="e12ea-141">Without the manifest, the default action for the driver is to use the same context as that specified by the application—in this example, version 2 of MSVCRT.</span></span> <span data-ttu-id="e12ea-142">Da ein Manifest vorhanden ist, wird ein separater Aktivierungs Kontext eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="e12ea-142">Since a manifest does exist, a separate activation context is established.</span></span> <span data-ttu-id="e12ea-143">Wenn der ODBC-Treiber ausgeführt wird, wird er an Version 1 der msvcrt-Assembly gebunden.</span><span class="sxs-lookup"><span data-stu-id="e12ea-143">When the ODBC driver runs, it binds to version 1 of the MSVCRT assembly.</span></span>

    <span data-ttu-id="e12ea-144">Jedes Mal, wenn der Treiber-Manager die Dispatch-Schicht aufruft – beispielsweise, um den nächsten Satz von Daten zu erhalten – verwendet er die entsprechenden Assemblys basierend auf dem Aktivierungs Kontext.</span><span class="sxs-lookup"><span data-stu-id="e12ea-144">Each time the driver manager calls the dispatch layer—for example, to get the next set of data—it uses the appropriate assemblies based on the activation context.</span></span> <span data-ttu-id="e12ea-145">Dies wird im folgenden Code Fragment veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="e12ea-145">The following code fragment illustrates this.</span></span>

    <dl> <span data-ttu-id="e12ea-146">Handle von hactctx;</span><span class="sxs-lookup"><span data-stu-id="e12ea-146">HANDLE hActCtx;</span></span>  
    <span data-ttu-id="e12ea-147">ULONG \_ ptr ulpcookie;</span><span class="sxs-lookup"><span data-stu-id="e12ea-147">ULONG\_PTR ulpCookie;</span></span>  
    <span data-ttu-id="e12ea-148">ActCtx actctxdecreate = {...};</span><span class="sxs-lookup"><span data-stu-id="e12ea-148">ACTCTX ActCtxToCreate = {...};</span></span>  
    <span data-ttu-id="e12ea-149">hactctx = kreateactctx (&actctxdecreate);</span><span class="sxs-lookup"><span data-stu-id="e12ea-149">hActCtx = CreateActCtx(&ActCtxToCreate);</span></span>  
    <span data-ttu-id="e12ea-150">...;</span><span class="sxs-lookup"><span data-stu-id="e12ea-150">...;</span></span>  
    <span data-ttu-id="e12ea-151">if (activateactctx (hactctx, &ulpcookie))</span><span class="sxs-lookup"><span data-stu-id="e12ea-151">if (ActivateActCtx(hActCtx, &ulpCookie))</span></span>  
    <span data-ttu-id="e12ea-152">{</span><span class="sxs-lookup"><span data-stu-id="e12ea-152">{</span></span>  
    <span data-ttu-id="e12ea-153">...</span><span class="sxs-lookup"><span data-stu-id="e12ea-153">...</span></span>  
    <span data-ttu-id="e12ea-154">ConnectDB (...);</span><span class="sxs-lookup"><span data-stu-id="e12ea-154">ConnectDb(...);</span></span>  
    <span data-ttu-id="e12ea-155">Deactivateactctx (0, ulpcookie);</span><span class="sxs-lookup"><span data-stu-id="e12ea-155">DeactivateActCtx(0, ulpCookie);</span></span>  
    <span data-ttu-id="e12ea-156">}</span><span class="sxs-lookup"><span data-stu-id="e12ea-156">}</span></span>  
    <span data-ttu-id="e12ea-157">...</span><span class="sxs-lookup"><span data-stu-id="e12ea-157">...</span></span>  
    <span data-ttu-id="e12ea-158">Releaseactctx (hactctx);</span><span class="sxs-lookup"><span data-stu-id="e12ea-158">ReleaseActCtx(hActCtx);</span></span>  
    </dl>

 

 
