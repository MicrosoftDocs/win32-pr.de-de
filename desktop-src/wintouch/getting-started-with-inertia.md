---
title: Trägheit
description: In diesem Abschnitt wird Trägheit für Windows-Fingereingabe erläutert.
ms.assetid: c33dda89-c715-4da0-a7af-aa0010dfd88b
keywords:
- Windows-Fingereingabe, Trägheit
- Trägheit, Info
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3b69ad31ec4a61f8723c9e52f87883dc4af3772
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036447"
---
# <a name="inertia"></a><span data-ttu-id="9e9cb-105">Trägheit</span><span class="sxs-lookup"><span data-stu-id="9e9cb-105">Inertia</span></span>

<span data-ttu-id="9e9cb-106">In diesem Abschnitt wird Trägheit für Windows-Fingereingabe erläutert.</span><span class="sxs-lookup"><span data-stu-id="9e9cb-106">This section explains inertia for Windows Touch.</span></span>

<span data-ttu-id="9e9cb-107">Die in Windows 7 enthaltene Trägheit-API ermöglicht ein konsistentes Objekt Verhalten in Windows-Finger eingabeanwendungen durch Bereitstellen eines einfachen Physik Modells.</span><span class="sxs-lookup"><span data-stu-id="9e9cb-107">The inertia API included in Windows 7 enables consistent object behavior in Windows Touch applications by providing a simple physics model.</span></span> <span data-ttu-id="9e9cb-108">Trägheit wird mithilfe des Trägheits Prozessor aktiviert, einer Klasse, die Funktionen kapselt.</span><span class="sxs-lookup"><span data-stu-id="9e9cb-108">Inertia is enabled by using the inertia processor, a class that encapsulates functionality.</span></span> <span data-ttu-id="9e9cb-109">Der Trägheits Prozessor verarbeitet Ereignisse, die an ihn weitergeleitet werden, wenn Objekt Manipulationen abgeschlossen werden, und indem Objekt Verarbeitungen auf eine Weise verarbeitet werden, die mit anderen Anwendungen konsistent ist.</span><span class="sxs-lookup"><span data-stu-id="9e9cb-109">The inertia processor works by processing events that are passed to it when object manipulations finish and by handling object trajectories in a way that is consistent with other applications.</span></span> <span data-ttu-id="9e9cb-110">Beachten Sie, dass der Trägheits Prozessor eng an den Manipulations Prozessor gekoppelt ist, um das Hinzufügen von Trägheit-Unterstützung für Anwendungen zu vereinfachen</span><span class="sxs-lookup"><span data-stu-id="9e9cb-110">Note that the inertia processor is tightly coupled to the manipulation processor to simplify adding inertia support to applications that use manipulations.</span></span> <span data-ttu-id="9e9cb-111">Tatsächlich löst der Trägheits Prozessor dieselben Ereignisse wie der Manipulations Prozessor aus.</span><span class="sxs-lookup"><span data-stu-id="9e9cb-111">In fact, the inertia processor raises the same events that the manipulation processor does.</span></span> <span data-ttu-id="9e9cb-112">Im folgenden Abschnitt werden die ersten Schritte mit Trägheit erläutert.</span><span class="sxs-lookup"><span data-stu-id="9e9cb-112">The following section explains how to get started with inertia.</span></span>



| <span data-ttu-id="9e9cb-113">`Section`</span><span class="sxs-lookup"><span data-stu-id="9e9cb-113">Section</span></span>                                                                      | <span data-ttu-id="9e9cb-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9e9cb-114">Description</span></span>                                                                                                              |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9e9cb-115">Trägheit-Mechanik</span><span class="sxs-lookup"><span data-stu-id="9e9cb-115">Inertia Mechanics</span></span>](inertia-mechanics.md)                                   | <span data-ttu-id="9e9cb-116">Erläutert die Grundlagen der Trägheits Berechnungen.</span><span class="sxs-lookup"><span data-stu-id="9e9cb-116">Explains the basics of inertia calculations.</span></span>                                                                             |
| [<span data-ttu-id="9e9cb-117">Behandeln von Trägheit in nicht verwaltetem Code</span><span class="sxs-lookup"><span data-stu-id="9e9cb-117">Handling Inertia in Unmanaged Code</span></span>](handling-inertia-in-unmanaged-code.md) | <span data-ttu-id="9e9cb-118">Erläutert, wie die [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) -Schnittstelle für die Handhabung von Trägheit in nicht verwaltetem Code verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9e9cb-118">Explains how to use the [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) interface for handling inertia in unmanaged code.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="9e9cb-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9e9cb-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9e9cb-120">Manipulationen und Trägheit</span><span class="sxs-lookup"><span data-stu-id="9e9cb-120">Manipulations and Inertia</span></span>](manipulation-and-inertia.md)
</dt> </dl>

 

 




