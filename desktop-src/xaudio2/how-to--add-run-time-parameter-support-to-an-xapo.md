---
description: Sie können die Unterstützung von Lauf Zeitparametern zu einem xapo hinzufügen, indem Sie die ixapoparameters-Schnittstelle implementieren. Durch die Unterstützung von Lauf Zeitparametern kann ein xapo sein Verhalten basierend auf den Parametern ändern, die ihm zur Laufzeit übergeben werden.
ms.assetid: 13f974ec-fcf5-1749-e69d-88de79b7d82b
title: "So wird's gemacht: Hinzufügen der Laufzeitparameterunterstützung zu einem XAPO"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 582f51b3dfbdc6d31422494906d5f945f77ccb03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485179"
---
# <a name="how-to-add-run-time-parameter-support-to-an-xapo"></a><span data-ttu-id="26503-104">So wird's gemacht: Hinzufügen der Laufzeitparameterunterstützung zu einem XAPO</span><span class="sxs-lookup"><span data-stu-id="26503-104">How to: Add Run-time Parameter Support to an XAPO</span></span>

<span data-ttu-id="26503-105">Sie können die Unterstützung von Lauf Zeitparametern zu einem xapo hinzufügen, indem Sie die [**ixapoparameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters) -Schnittstelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="26503-105">You can add run-time parameter support to an XAPO by implementing the [**IXAPOParameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters) interface.</span></span> <span data-ttu-id="26503-106">Durch die Unterstützung von Lauf Zeitparametern kann ein xapo sein Verhalten basierend auf den Parametern ändern, die ihm zur Laufzeit übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="26503-106">Run-time parameter support allows an XAPO to change its behavior based on the parameters passed to it at run time.</span></span>

1.  <span data-ttu-id="26503-107">Führen Sie die Schritte unter Gewusst [wie: Erstellen eines xapo](how-to--create-an-xapo.md)aus.</span><span class="sxs-lookup"><span data-stu-id="26503-107">Follow the steps in [How to: Create an XAPO](how-to--create-an-xapo.md).</span></span>
2.  <span data-ttu-id="26503-108">Ändern Sie den xapo-Wert, um von [**cxapoparametersbase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) und [**cxapobase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase)abgeleitet zu werden.</span><span class="sxs-lookup"><span data-stu-id="26503-108">Change the XAPO to derive from [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) and [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase).</span></span>
3.  <span data-ttu-id="26503-109">Fügen Sie den-Methoden [**cxapoparametersbase:: beginprocess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-beginprocess) und [**cxapoparametersbase:: endprocess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-endprocess) Aufrufe der-Implementierung von [**ixapo::P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process)hinzu.</span><span class="sxs-lookup"><span data-stu-id="26503-109">Add calls to the methods [**CXAPOParametersBase::BeginProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-beginprocess) and [**CXAPOParametersBase::EndProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-endprocess) to the implementation of [**IXAPO::Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process).</span></span>

    > [!Note]  
    > <span data-ttu-id="26503-110">Das Hinzufügen dieser Methoden zu [ixapo::P rocess](how-to--build-a-basic-audio-processing-graph.md) ermöglicht [**cxapoparametersbase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) , seine Kopien der Effektparameter in einem Thread sicheren Zustand zu belassen.</span><span class="sxs-lookup"><span data-stu-id="26503-110">Adding these methods to [IXAPO::Process](how-to--build-a-basic-audio-processing-graph.md) allows [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) to keep its copies of the effect parameters in a thread-safe state.</span></span> <span data-ttu-id="26503-111">Aufrufen von [**cxapoparametersbase:: beginprocess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-beginprocess) am Anfang von [**ixapo::P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process)und [**cxapoparametersbase:: endprocess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-endprocess) am Ende von **ixapo::P rocess**.</span><span class="sxs-lookup"><span data-stu-id="26503-111">Call [**CXAPOParametersBase::BeginProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-beginprocess) at the beginning of [**IXAPO::Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process), and [**CXAPOParametersBase::EndProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-endprocess) at the end of **IXAPO::Process**.</span></span>

     

4.  <span data-ttu-id="26503-112">Fügen Sie der [**ixapo::P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process) -Implementierung weiteren Code hinzu, um das Verhalten entsprechend den Werten zu ändern, die von der [**SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) -Methode gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="26503-112">Add more code to the [**IXAPO::Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process) implementation to change its behavior according to values stored by the [**SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) method.</span></span>

    > [!Note]  
    > <span data-ttu-id="26503-113">Wenn Sie der [**ixapo::P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process) -Methode Code hinzufügen, um die von [**SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) angegebenen Parameter zu verwenden, kann das xapo-Verhalten während des gesamten Lebenszyklus geändert werden.</span><span class="sxs-lookup"><span data-stu-id="26503-113">Adding code to the [**IXAPO::Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process) method to use the parameters specified by [**SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) allows the XAPO's behavior to be changed throughout its life.</span></span>

     

5.  <span data-ttu-id="26503-114">Wenn Sie eine Instanz des Effekts erstellen, weisen Sie einen Puffer mit drei der Strukturen zu, die die Parameter des Effekts darstellen, und übergeben Sie ihn an den [**cxapoparametersbase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) -Konstruktor.</span><span class="sxs-lookup"><span data-stu-id="26503-114">When you create an instance of the effect, allocate a buffer of three of the structures that will represent the effect's parameters, and pass it to the [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) constructor.</span></span>

    > [!Note]  
    > <span data-ttu-id="26503-115">Die [**cxapoparametersbase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) -Instanz verwendet diesen Puffer intern zum Verwalten von Effekt Parametern, die an Sie übergeben werden, wenn [**SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters)aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="26503-115">The [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) instance internally uses this buffer to manage effect parameters passed to it when you call [**SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters).</span></span> <span data-ttu-id="26503-116">Sie müssen alle Prozessparameter Blöcke in *pparameterblocks* auf denselben Standardwert initialisieren, bevor Sie eine der Methoden [**ixapo::P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process), [**ixapoparameters:: GetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-getparameters)und **ixapoparameters:: SetParameters** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="26503-116">You must initialize all the process parameter blocks in *pParameterBlocks* to the same default value before you call any of the [**IXAPO::Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process), [**IXAPOParameters::GetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-getparameters), and **IXAPOParameters::SetParameters** methods.</span></span> <span data-ttu-id="26503-117">Normalerweise wird diese Initialisierung in [**ixapo:: Initialize**](/windows/win32/api/xapo/nf-xapo-ixapo-initialize) oder [**ixapo:: lockforprocess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess)behandelt.</span><span class="sxs-lookup"><span data-stu-id="26503-117">Usually this initialization is handled in [**IXAPO::Initialize**](/windows/win32/api/xapo/nf-xapo-ixapo-initialize) or in [**IXAPO::LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess).</span></span>

     

## <a name="related-topics"></a><span data-ttu-id="26503-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="26503-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26503-119">Audioeffekte</span><span class="sxs-lookup"><span data-stu-id="26503-119">Audio Effects</span></span>](audio-effects.md)
</dt> <dt>

[<span data-ttu-id="26503-120">Übersicht über xapo</span><span class="sxs-lookup"><span data-stu-id="26503-120">XAPO Overview</span></span>](xapo-overview.md)
</dt> </dl>

 

 
