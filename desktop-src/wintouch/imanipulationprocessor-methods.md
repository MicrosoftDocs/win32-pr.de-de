---
title: Methoden (IInertiaProcessor)
description: Dieser Abschnitt enthält die Methoden für die IInertiaProcessor-Schnittstelle.
ms.assetid: e4acfcac-06c1-42a5-9722-4534a4492ab8
keywords:
- Windows-Berührungs-, IInertiaProcessor-Schnittstelle
- Windows-Berührungs Schnittstellen Methoden
- Trägheit, IInertiaProcessor-Schnittstelle
- IInertiaProcessor-Schnittstelle, Methoden
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 662bb9aaa51400c4fd302f56bfec7c845ce57645
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106337485"
---
# <a name="methods-iinertiaprocessor"></a><span data-ttu-id="dbf83-107">Methoden (IInertiaProcessor)</span><span class="sxs-lookup"><span data-stu-id="dbf83-107">Methods (IInertiaProcessor)</span></span>

<span data-ttu-id="dbf83-108">Dieser Abschnitt enthält die Methoden für die [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="dbf83-108">This section contains the methods for the [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) interface.</span></span>



| <span data-ttu-id="dbf83-109">Methode</span><span class="sxs-lookup"><span data-stu-id="dbf83-109">Method</span></span>                                                 | <span data-ttu-id="dbf83-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dbf83-110">Description</span></span>                                                                                                                                                                                                                |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dbf83-111">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="dbf83-111">**Reset**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-reset)               | <span data-ttu-id="dbf83-112">Initialisiert den Prozessor mit dem anfänglichen Zeitstempel und startet die Trägheit neu.</span><span class="sxs-lookup"><span data-stu-id="dbf83-112">Initializes the processor with initial time stamp and restarts inertia.</span></span>                                                                                                                                                    |
| [<span data-ttu-id="dbf83-113">**Prozess**</span><span class="sxs-lookup"><span data-stu-id="dbf83-113">**Process**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-process)           | <span data-ttu-id="dbf83-114">Führt Berechnungen für den aktuellen Tick aus und kann je nachdem, ob die extrapolierungs Methode abgeschlossen ist, das **Delta** -oder **abgeschlossene** Ereignis erhöhen.</span><span class="sxs-lookup"><span data-stu-id="dbf83-114">Performs calculations for the current tick and can raise the **Delta** or **Completed** event depending on whether extrapolation is completed or not.</span></span> <span data-ttu-id="dbf83-115">Wenn die extrapolierungs Methode zum vorherigen Tick abgeschlossen wurde, ist die Methode No-op.</span><span class="sxs-lookup"><span data-stu-id="dbf83-115">If extrapolation finished at the previous tick, the method is no-op.</span></span> |
| [<span data-ttu-id="dbf83-116">**ProcessTime**</span><span class="sxs-lookup"><span data-stu-id="dbf83-116">**ProcessTime**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-processtime)   | <span data-ttu-id="dbf83-117">Führt Berechnungen für den angegebenen Tick aus und kann je nachdem, ob die extrapolierungs Methode abgeschlossen ist, das **Delta** -oder **abgeschlossene** Ereignis erhöhen.</span><span class="sxs-lookup"><span data-stu-id="dbf83-117">Performs calculations for the given tick and can raise the **Delta** or **Completed** event depending on whether extrapolation is completed or not.</span></span>                                                                        |
| [<span data-ttu-id="dbf83-118">**Abgeschlossen**</span><span class="sxs-lookup"><span data-stu-id="dbf83-118">**Complete**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-complete)         | <span data-ttu-id="dbf83-119">Beendet die aktuelle Bearbeitung und beendet die Trägheit des trägheitprozessors.</span><span class="sxs-lookup"><span data-stu-id="dbf83-119">Finishes the current manipulation and stops inertia on the inertia processor.</span></span>                                                                                                                                              |
| [<span data-ttu-id="dbf83-120">**Completetime**</span><span class="sxs-lookup"><span data-stu-id="dbf83-120">**CompleteTime**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-completetime) | <span data-ttu-id="dbf83-121">Schließt die aktuelle Bearbeitung am angegebenen Tick ab, hält die Trägheit des Trägheits Prozessors an und löst das Ereignis "manipulationabgeschlossene" aus.</span><span class="sxs-lookup"><span data-stu-id="dbf83-121">Finishes the current manipulation at the given tick, stops inertia on the inertia processor, and raises the ManipulationCompleted event.</span></span>                                                                                   |



 

## <a name="related-topics"></a><span data-ttu-id="dbf83-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="dbf83-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dbf83-123">**IInertiaProcessor**</span><span class="sxs-lookup"><span data-stu-id="dbf83-123">**IInertiaProcessor**</span></span>](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor)
</dt> </dl>

 

 




