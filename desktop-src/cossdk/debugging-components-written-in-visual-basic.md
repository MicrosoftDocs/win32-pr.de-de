---
description: In Visual Basic geschriebene debuggingkomponenten
ms.assetid: 2b00ed29-8b48-4a54-83e8-d5e69e5f883e
title: In Visual Basic geschriebene debuggingkomponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 085dd1d6f45cc7f6665851b232402ecee01c069f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344626"
---
# <a name="debugging-components-written-in-visual-basic"></a><span data-ttu-id="fe29a-103">In Visual Basic geschriebene debuggingkomponenten</span><span class="sxs-lookup"><span data-stu-id="fe29a-103">Debugging Components Written in Visual Basic</span></span>

<span data-ttu-id="fe29a-104">In bestimmten Szenarien können Sie die Entwicklungsumgebung von Microsoft Visual Basic 6,0 zum Debuggen verwenden.</span><span class="sxs-lookup"><span data-stu-id="fe29a-104">You can use the Microsoft Visual Basic 6.0 development environment for debugging within certain scenarios.</span></span> <span data-ttu-id="fe29a-105">Die Verwendung von Visual Basic für das Debugging ermöglicht den Zugriff auf Tools, die Visual Basic Programmierern vertraut sind</span><span class="sxs-lookup"><span data-stu-id="fe29a-105">Using Visual Basic for debugging allows access to tools familiar to Visual Basic programmers.</span></span> <span data-ttu-id="fe29a-106">Da hingegen während des Debuggens Visual Basic Komponenten innerhalb des Prozesses der Visual Basic Umgebung ausgeführt werden, kann es erforderlich sein, die Komponente zu debuggen, nachdem Sie mithilfe der Microsoft Visual C++ Entwicklungsumgebung kompiliert wurde.</span><span class="sxs-lookup"><span data-stu-id="fe29a-106">On the other hand, because during debugging Visual Basic components run within the Visual Basic environment's process, it may be necessary to debug your component after it has been compiled by using the Microsoft Visual C++ development environment.</span></span>

<span data-ttu-id="fe29a-107">Weitere Informationen zum Debuggen in der Visual Basic integrierten Entwicklungsumgebung (Integrated Development Environment, IDE) finden Sie unter [Debuggen in der Visual Basic IDE](debugging-in-the-visual-basic-ide.md).</span><span class="sxs-lookup"><span data-stu-id="fe29a-107">For more information about debugging within the Visual Basic integrated development environment (IDE), see [Debugging in the Visual Basic IDE](debugging-in-the-visual-basic-ide.md).</span></span> <span data-ttu-id="fe29a-108">Weitere Informationen zum Debuggen Visual Basic Komponenten, nachdem diese mithilfe der Visual C++ Entwicklungsumgebung kompiliert wurden, finden Sie unter [Debuggen von kompilierten Visual Basic Komponenten](debugging-compiled-visual-basic-components.md)</span><span class="sxs-lookup"><span data-stu-id="fe29a-108">For more on debugging Visual Basic components after they're compiled using the Visual C++ development environment, see [Debugging Compiled Visual Basic Components](debugging-compiled-visual-basic-components.md).</span></span>

<span data-ttu-id="fe29a-109">Außerdem wurden verschiedene Einschränkungen im Zusammenhang mit der Verwendung der Visual Basic Umgebung zum Debuggen von Komponenten mit MTS für com+ aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="fe29a-109">Also, several limitations associated with using the Visual Basic environment to debug components with MTS have been resolved for COM+.</span></span> <span data-ttu-id="fe29a-110">Weitere Informationen finden Sie [unter com+-Visual Basic Debuggingunterstützung gegen MTS](com--visual-basic-debugging-support-contrasted-with-mts.md).</span><span class="sxs-lookup"><span data-stu-id="fe29a-110">For more information, see [COM+ Visual Basic Debugging Support Contrasted with MTS](com--visual-basic-debugging-support-contrasted-with-mts.md).</span></span>

> [!Note]  
> <span data-ttu-id="fe29a-111">Wenn Sie Visual Basic bereits auf demselben Computer wie com+ verwendet haben, haben Sie möglicherweise bemerkt, dass das Add-in für Komponenten Dienste in der Visual Basic-Umgebung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="fe29a-111">If you have already used Visual Basic on the same computer as COM+, you may have noticed the Component Services add-in available in the Visual Basic environment.</span></span> <span data-ttu-id="fe29a-112">Diese Funktion wurde ursprünglich in MTS entworfen, um die Registrierung jedes Mal zu aktualisieren, wenn Sie eine Komponente in einer COM+-Anwendung neu kompiliert haben.</span><span class="sxs-lookup"><span data-stu-id="fe29a-112">Originally in MTS, this feature was designed to update the registry each time you recompiled a component in a COM+ application.</span></span> <span data-ttu-id="fe29a-113">Aufgrund der Art der Interaktion der Microsoft Windows-Registrierung und der COM+-Registrierungsdatenbank werden einige Einstellungen jedoch möglicherweise nicht vollständig aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="fe29a-113">However, given the nature of the interaction of the Microsoft Windows Registry and the COM+ registration database, some settings may not be completely updated.</span></span> <span data-ttu-id="fe29a-114">Anstatt die Befehle zu verwenden, die mit diesem Add-in verfügbar sind, sollten Sie daher die Komponenten entfernen und neu installieren, um die Einstellungen nach der erneuten Kompilierung zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="fe29a-114">Therefore, instead of using the commands available with this add-in, you should remove and reinstall your components to update settings after recompiling.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="fe29a-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fe29a-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe29a-116">In Visual C++ geschriebene debuggingkomponenten</span><span class="sxs-lookup"><span data-stu-id="fe29a-116">Debugging Components Written in Visual C++</span></span>](debugging-components-written-in-visual-c--.md)
</dt> </dl>

 

 



