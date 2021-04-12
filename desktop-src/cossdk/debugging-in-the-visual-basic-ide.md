---
description: Die Verwendung der integrierten Entwicklungsumgebung (Integrated Development Environment, IDE) von Microsoft Visual Basic für das Debuggen ermöglicht Visual Basic Entwicklern den Zugriff auf vertraute Tools und Benutzerfreundlichkeit.
ms.assetid: d31efc97-c286-434d-93f5-77b34ec16205
title: Debuggen in der Visual Basic IDE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74574fdb289e1ad334337f17943c6961b95bf288
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393002"
---
# <a name="debugging-in-the-visual-basic-ide"></a><span data-ttu-id="0a0ac-103">Debuggen in der Visual Basic IDE</span><span class="sxs-lookup"><span data-stu-id="0a0ac-103">Debugging in the Visual Basic IDE</span></span>

<span data-ttu-id="0a0ac-104">Die Verwendung der integrierten Entwicklungsumgebung (Integrated Development Environment, IDE) von Microsoft Visual Basic für das Debuggen ermöglicht Visual Basic Entwicklern den Zugriff auf vertraute Tools und Benutzerfreundlichkeit.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-104">Using the Microsoft Visual Basic integrated development environment (IDE) for debugging gives Visual Basic developers access to familiar tools and ease-of-use.</span></span> <span data-ttu-id="0a0ac-105">Obwohl viele Komponenten zu einem späteren Zeitpunkt mit der Microsoft Visual C++ Umgebung vollständig debuggt werden müssen, könnte eine Strategie darin bestehen, so viele Funktionen wie möglich mit Visual Basic zu debuggen.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-105">While many components will eventually need to be more fully debugged using the Microsoft Visual C++ environment, one strategy might be to first debug as much functionality as possible with Visual Basic.</span></span> <span data-ttu-id="0a0ac-106">Beispielsweise können Sie die Visual Basic IDE für das Debuggen in com+ verwenden, wenn Sie noch kein Debugging von Multithreading, Komponenten Nachverfolgung, Remote aufrufen oder Prozess Isolation durchführen möchten.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-106">For example, you might want to use the Visual Basic IDE for debugging within COM+ when you aren't yet debugging multithreading, component tracking, remote calls, or process isolation.</span></span>

<span data-ttu-id="0a0ac-107">Wenn Sie die Visual Basic Umgebung für das Debuggen verwenden, kompilieren Sie das Projekt im allgemeinen und fügen die dll einer COM+-Anwendung hinzu.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-107">In general, when using the Visual Basic environment for debugging, you first compile the project and add the DLL to a COM+ application.</span></span> <span data-ttu-id="0a0ac-108">Anschließend legen Sie die binäre Kompatibilität für das Projekt fest, verweisen auf die von Ihnen erstellte DLL und starten das Projekt, um mit dem Debuggen zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-108">Then you set binary compatibility for the project, referencing the DLL you made, and start the project to begin debugging.</span></span>

## <a name="general-guidelines-for-debugging-in-the-visual-basic-environment"></a><span data-ttu-id="0a0ac-109">Allgemeine Richtlinien für das Debuggen in der Visual Basic Umgebung</span><span class="sxs-lookup"><span data-stu-id="0a0ac-109">General Guidelines for Debugging in the Visual Basic Environment</span></span>

-   <span data-ttu-id="0a0ac-110">Beim Debuggen mit Visual Basic behandelt com+ die Visual Basic Komponenten so, als ob Sie zu einer Bibliotheks Anwendung gehören, auch wenn die Komponenten als zu einer Serveranwendung gehörend registriert sind.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-110">While you are debugging using Visual Basic, COM+ treats the Visual Basic components as if they belong to a library application, even if the components are registered as belonging to a server application.</span></span> <span data-ttu-id="0a0ac-111">Da es als Bibliotheks Anwendung ausgeführt wird, werden die Komponenten Symbole im Verwaltungs Programmkomponenten Dienste beim debuggten der Komponenten nicht gedreht.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-111">Because it runs as a library application, the component icons in the Component Services administrative tool do not spin as the components are debugged.</span></span>
-   <span data-ttu-id="0a0ac-112">Wenn Sie während des Debuggens Transaktions Attribute für eine Komponente ändern oder eine Quell Codeänderung vornehmen, bei der Visual Basic eine neue CLSID oder ProgID generieren müssen, müssen Sie die COM+-Anwendung, die die Komponente enthält, löschen und neu installieren.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-112">If you change transaction attributes on a component during debugging or make a source code change that requires Visual Basic to generate a new CLSID or ProgID, be sure to delete and reinstall the COM+ application containing the component.</span></span> <span data-ttu-id="0a0ac-113">Wenn Sie die binäre Kompatibilität für die Komponente festgelegt haben, werden Sie gewarnt, dass Änderungen aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-113">If you have set binary compatibility for the component, you will be warned that changes have occurred.</span></span>

## <a name="notes-on-debugging-within-a-com-application"></a><span data-ttu-id="0a0ac-114">Hinweise zum Debuggen in einer COM+-Anwendung</span><span class="sxs-lookup"><span data-stu-id="0a0ac-114">Notes on Debugging Within a COM+ Application</span></span>

-   <span data-ttu-id="0a0ac-115">Wenn Sie Änderungen an der Visual Basic IDE in den Schnittstellen der Komponente, Klassennamen, Projektnamen, Transaktionsunterstützung oder anderen Einstellungen vornehmen, treten möglicherweise Konflikte zwischen den Konfigurationsdaten im Komponenten Dienst-Explorer und der eigentlichen Konfiguration auf, die im Visual Basic Debugger ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-115">If you make changes in the Visual Basic IDE in your component's interfaces, class names, project names, transactional support or other settings, there may be mismatches between the configuration data in the Component Services explorer and the actual configuration running in the Visual Basic debugger.</span></span>
-   <span data-ttu-id="0a0ac-116">Exportieren Sie eine COM+-Anwendung nicht, während Sie eine Komponente in der Anwendung debuggen.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-116">Do not export a COM+ application while you are debugging a component in the application.</span></span> <span data-ttu-id="0a0ac-117">Com+ behandelt die Visual Basic Entwicklungsumgebung als Komponente.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-117">COM+ will treat the Visual Basic development environment as the component.</span></span>
-   <span data-ttu-id="0a0ac-118">Wenn Sie eine Komponente außerhalb des Debuggers ausführen und dann das Debuggen starten möchten, wird eine Instanz der Komponente möglicherweise weiterhin in com+ ausgeführt, wenn Sie Sie im Debugger starten.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-118">If you are running a component outside the debugger and then decide to begin debugging, an instance of the component may still be running in COM+ when you start it in the debugger.</span></span> <span data-ttu-id="0a0ac-119">Com+ erkennt diese Bedingung und versucht, die Instanz, die Sie steuert, automatisch herunterzufahren.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-119">COM+ will detect this condition and attempt to silently shut down the instance it controls.</span></span> <span data-ttu-id="0a0ac-120">Um dieses Problem zu vermeiden, entfernen Sie die Komponente aus dem Verwaltungs Programmkomponenten Dienste, bevor Sie mit dem Debuggen beginnen.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-120">To avoid this problem, remove the component from the Component Services administrative tool before you begin debugging.</span></span>

<span data-ttu-id="0a0ac-121">**So debuggen Sie mithilfe der Visual Basic Umgebung**</span><span class="sxs-lookup"><span data-stu-id="0a0ac-121">**To debug using the Visual Basic environment**</span></span>

1.  <span data-ttu-id="0a0ac-122">Öffnen Sie das Komponenten Projekt in Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-122">Open the component project in Visual Basic.</span></span>

2.  <span data-ttu-id="0a0ac-123">Kompilieren Sie die Komponente, und legen Sie dann die binäre Kompatibilität in Ihrem Projekt auf die kompilierte Komponente fest.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-123">Compile your component, and then set binary compatibility in your project to the compiled component.</span></span>

3.  <span data-ttu-id="0a0ac-124">Legen Sie die mtstransaktionmode-Eigenschaft auf einen anderen Wert als 0-notanmtsobject fest.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-124">Set the MTSTransactionMode property to a value other than 0 - NotAnMTSObject.</span></span> <span data-ttu-id="0a0ac-125">Wenn Sie das Projekt starten, werden Visual Basic durch diese Einstellung aufgefordert, Ihre Komponente in com+ zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-125">When you start the project, this setting prompts Visual Basic to activate your component within COM+.</span></span>

4.  <span data-ttu-id="0a0ac-126">Klicken Sie im Menü **Projekt** auf **Eigenschaften**, und geben Sie dann das Programmstart auf der Registerkarte **Debuggen** ein. Das Start Programm ist die ausführbare Client Datei, die diese Komponente aufruft.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-126">From the **Project** menu, click **Properties**, and then enter the start program on the **Debugging** tab. The start program is the client executable that calls this component.</span></span>

    > [!Note]  
    > <span data-ttu-id="0a0ac-127">Das Start Programm muss für die Komponente, die Sie Debuggen, lokal sein.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-127">The start program must be local to the component you are debugging.</span></span>

     

5.  <span data-ttu-id="0a0ac-128">Drücken Sie F5, um mit dem Debuggen der Komponente zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-128">Press the F5 key to begin debugging the component.</span></span>

<span data-ttu-id="0a0ac-129">Nachdem Sie F5 drücken, wird Visual Basic die Client Anwendung starten und die Komponente im Debugmodus ausführen.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-129">After you press F5, Visual Basic launches the client application and runs the component in debug mode.</span></span> <span data-ttu-id="0a0ac-130">Sie können Haltepunkte im Code der Komponente platzieren und Uhren für Variablen festlegen.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-130">You can place breakpoints in the component's code and set watches on variables.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0a0ac-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0a0ac-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a0ac-132">Com+-Visual Basic Debugunterstützung im Vergleich zu MTS</span><span class="sxs-lookup"><span data-stu-id="0a0ac-132">COM+ Visual Basic Debugging Support Contrasted with MTS</span></span>](com--visual-basic-debugging-support-contrasted-with-mts.md)
</dt> <dt>

[<span data-ttu-id="0a0ac-133">Debuggen kompilierter Visual Basic Komponenten</span><span class="sxs-lookup"><span data-stu-id="0a0ac-133">Debugging Compiled Visual Basic Components</span></span>](debugging-compiled-visual-basic-components.md)
</dt> </dl>

 

 



