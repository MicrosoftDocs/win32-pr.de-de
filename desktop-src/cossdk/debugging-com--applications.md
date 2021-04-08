---
description: Die Debuggingtechniken für COM+-Anwendungen hängen von der Sprache ab, in der Sie Ihre Komponente schreiben möchten.
ms.assetid: 781a0b3f-2bd0-435b-b6fe-4469cc02e8b6
title: Com+-Anwendungen debuggen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db096ceb525cd988afa55e49cc88fda0ddf52549
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748865"
---
# <a name="debugging-com-applications"></a><span data-ttu-id="33f60-103">Com+-Anwendungen debuggen</span><span class="sxs-lookup"><span data-stu-id="33f60-103">Debugging COM+ Applications</span></span>

<span data-ttu-id="33f60-104">Die Debuggingtechniken für COM+-Anwendungen hängen von der Sprache ab, in der Sie Ihre Komponente schreiben möchten.</span><span class="sxs-lookup"><span data-stu-id="33f60-104">Debugging techniques for COM+ applications depend on the language in which you choose to write your component.</span></span>

<span data-ttu-id="33f60-105">Wenn Sie in Microsoft Visual C++ programmieren, können Sie den Debugger in C++ starten, oder Sie können mit einem Remote Client debuggen, indem Sie das OLE-Remote Prozedur Steuerelement (RPC) und das Just-in-time (JIT)-Debuggen verwenden.</span><span class="sxs-lookup"><span data-stu-id="33f60-105">If you code in Microsoft Visual C++, you can launch the debugger in C++ or, with a remote client, you can debug by using OLE remote procedure control (RPC) and just-in-time (JIT) debugging.</span></span> <span data-ttu-id="33f60-106">Mit dem Verwaltungs Programmkomponenten Dienste können Sie die Komponente jederzeit mithilfe der com+-Einstellung **in debuggerstart** auf der Registerkarte **erweitert** im Dialogfeld **Eigenschaften** der com+-Anwendung debuggen.</span><span class="sxs-lookup"><span data-stu-id="33f60-106">You can always use the Component Services administrative tool to debug your component with the COM+ **Launch in debugger** setting on the **Advanced** tab of the COM+ application's **Properties** dialog box.</span></span> <span data-ttu-id="33f60-107">Weitere Informationen zum Debuggen von Komponenten, die in C++ codiert sind, finden Sie unter [Debugging Components in Visual C++](debugging-components-written-in-visual-c--.md).</span><span class="sxs-lookup"><span data-stu-id="33f60-107">For more information on debugging components coded in C++, see [Debugging Components Written in Visual C++](debugging-components-written-in-visual-c--.md).</span></span>

<span data-ttu-id="33f60-108">Sie können die Microsoft Visual Basic-Umgebung zu Debuggingzwecken verwenden, es sei denn, Sie Debuggen Multithreading, Komponenten Nachverfolgung, Remote Aufrufe oder Prozess Isolation.</span><span class="sxs-lookup"><span data-stu-id="33f60-108">Unless you are currently debugging multithreading, component tracking, remote calls, or process isolation, you can use the Microsoft Visual Basic environment for debugging purposes.</span></span> <span data-ttu-id="33f60-109">[Debuggingkomponenten, die in Visual Basic geschrieben](debugging-components-written-in-visual-basic.md) werden, beschreiben den Debugprozess in einer Visual Basic</span><span class="sxs-lookup"><span data-stu-id="33f60-109">[Debugging Components Written in Visual Basic](debugging-components-written-in-visual-basic.md) describes the debugging process within a Visual Basic environment.</span></span>

<span data-ttu-id="33f60-110">Das Thema [Debuggen in der Visual Basic IDE](debugging-in-the-visual-basic-ide.md) bietet eine allgemeine Übersicht über Richtlinien, Tipps und ein Verfahren zum Debuggen in der integrierten Entwicklungsumgebung (Integrated Development Environment, IDE).</span><span class="sxs-lookup"><span data-stu-id="33f60-110">The topic [Debugging in the Visual Basic IDE](debugging-in-the-visual-basic-ide.md) provides a general overview with guidelines, tips and a procedure on debugging in the integrated development environment (IDE).</span></span>

<span data-ttu-id="33f60-111">Weitere Informationen zum Debuggen erweiterter Prozesse finden Sie unter [Debuggen von kompilierten Visual Basic-Komponenten](debugging-compiled-visual-basic-components.md).</span><span class="sxs-lookup"><span data-stu-id="33f60-111">To view more information about debugging advanced processes, see [Debugging Compiled Visual Basic Components](debugging-compiled-visual-basic-components.md).</span></span>

> [!Note]  
> <span data-ttu-id="33f60-112">Mehrere Einschränkungen im Zusammenhang mit der Verwendung der Visual Basic Umgebung zum Debuggen von Komponenten mit MTS wurden für com+ aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="33f60-112">Several limitations associated with using the Visual Basic environment to debug components with MTS have been resolved for COM+.</span></span> <span data-ttu-id="33f60-113">Weitere Informationen finden Sie [unter com+-Visual Basic Debuggingunterstützung gegen MTS](com--visual-basic-debugging-support-contrasted-with-mts.md).</span><span class="sxs-lookup"><span data-stu-id="33f60-113">For more information, see [COM+ Visual Basic Debugging Support Contrasted with MTS](com--visual-basic-debugging-support-contrasted-with-mts.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="33f60-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="33f60-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33f60-115">Behandeln von Fehlern in com+</span><span class="sxs-lookup"><span data-stu-id="33f60-115">Handling Errors in COM+</span></span>](handling-errors-in-com-.md)
</dt> </dl>

 

 



