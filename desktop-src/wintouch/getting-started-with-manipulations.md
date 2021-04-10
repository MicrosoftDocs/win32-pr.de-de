---
title: Manipulationen
description: In diesem Abschnitt wird die Objekt Bearbeitung für Windows-Fingerabdruck erläutert.
ms.assetid: 7f905c36-7804-422c-8a60-a281e03c5e15
keywords:
- Windows-Fingereingabe, Manipulationen
- Manipulationen, Informationen zu
- Manipulationen, Gesten Unterschiede
- Gesten, Manipulations Unterschiede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10fe65494de990305e4268aa4191b5dabaa267f4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309348"
---
# <a name="manipulations"></a><span data-ttu-id="21a64-107">Manipulationen</span><span class="sxs-lookup"><span data-stu-id="21a64-107">Manipulations</span></span>

<span data-ttu-id="21a64-108">In diesem Abschnitt wird die Objekt Bearbeitung für Windows-Fingerabdruck erläutert.</span><span class="sxs-lookup"><span data-stu-id="21a64-108">This section explains object manipulation for Windows Touch.</span></span>

## <a name="manipulation-overview"></a><span data-ttu-id="21a64-109">Übersicht über Manipulationen</span><span class="sxs-lookup"><span data-stu-id="21a64-109">Manipulation Overview</span></span>

<span data-ttu-id="21a64-110">Eine praktische Möglichkeit, Manipulationen zu berücksichtigen, besteht darin, Sie als eine Reihe von Gesten zu betrachten.</span><span class="sxs-lookup"><span data-stu-id="21a64-110">A convenient way to think about manipulations is to consider them a superset of gestures.</span></span> <span data-ttu-id="21a64-111">Mit Gesten können Sie mehr Flexibilität und eine präzisere Genauigkeit durch die Verwendung von Manipulationen erreichen.</span><span class="sxs-lookup"><span data-stu-id="21a64-111">What you can do with gestures, you can do with more flexibility and with finer precision by using manipulations.</span></span> <span data-ttu-id="21a64-112">Der Unterschied zwischen Manipulationen und Gesten wird am besten anhand eines einfachen Beispiels veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="21a64-112">The difference between manipulations and gestures is best demonstrated with a simple example.</span></span> <span data-ttu-id="21a64-113">Sie können ein Objekt erweitern und gleichzeitig mithilfe von Manipulationen übersetzen. mit Gesten können Sie nur eine gleichzeitig ausführen.</span><span class="sxs-lookup"><span data-stu-id="21a64-113">You can expand an object and at the same time translate it using manipulations; with gestures, you can do only one at a time.</span></span> <span data-ttu-id="21a64-114">Diese Möglichkeit, ein Objekt in Echtzeit zu manipulieren, macht Anwendungen intuitiver für Benutzer, indem es eine realistischere Benutzerfreundlichkeit ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="21a64-114">This ability to manipulate an object in real time makes applications more intuitive to users by enabling a more realistic experience.</span></span>

<span data-ttu-id="21a64-115">Die Manipulations-APIs werden verwendet, um Transformations Vorgänge für Objekte für Anwendungen mit aktiviertem Touchscreen zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="21a64-115">The Manipulation APIs are used to simplify transformation operations on objects for touch-enabled applications.</span></span> <span data-ttu-id="21a64-116">Manipulationen werden in Windows 7 durch das Manipulationen-com-Objekt durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="21a64-116">Manipulations are performed in Windows 7 through the manipulations COM object.</span></span> <span data-ttu-id="21a64-117">Mithilfe von Manipulationen können Entwickler die Trägheit (Objekt Physik) leichter unterstützen und problemlos Transformationen für Objekte auf eine Weise durchführen, die mit anderen Anwendungen konsistent ist.</span><span class="sxs-lookup"><span data-stu-id="21a64-117">By using manipulations, developers can more easily support inertia (object physics) and can easily perform transformations on objects in a way that is consistent with other applications.</span></span> <span data-ttu-id="21a64-118">In den folgenden Abschnitten werden verschiedene Möglichkeiten erläutert, wie Sie Manipulationen durchführen können.</span><span class="sxs-lookup"><span data-stu-id="21a64-118">The following sections explain various ways that you can perform manipulations.</span></span>



| <span data-ttu-id="21a64-119">`Section`</span><span class="sxs-lookup"><span data-stu-id="21a64-119">Section</span></span>                                                                                            | <span data-ttu-id="21a64-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="21a64-120">Description</span></span>                                                                                                                                          |
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="21a64-121">Hinzufügen von Manipulations Unterstützung zu nicht verwaltetem Code</span><span class="sxs-lookup"><span data-stu-id="21a64-121">Adding Manipulation Support to Unmanaged Code</span></span>](adding-manipulation-support-in-unmanaged-code.md) | <span data-ttu-id="21a64-122">Erläutert das Implementieren einer Ereignis Senke für die [**\_ imanipulationevents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) -Schnittstelle und das Hinzufügen von Ereignis Handlern zu Ihrem Code.</span><span class="sxs-lookup"><span data-stu-id="21a64-122">Explains how to implement an event sink for the [**\_IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) interface and add event handlers to your code.</span></span> |
| [<span data-ttu-id="21a64-123">Erweiterte Manipulationen</span><span class="sxs-lookup"><span data-stu-id="21a64-123">Advanced Manipulations</span></span>](advanced-manipulations.md)                                               | <span data-ttu-id="21a64-124">Erläutert, wie komplexe Manipulationen durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="21a64-124">Explains how to perform complex manipulations.</span></span>                                                                                                       |
| [<span data-ttu-id="21a64-125">Drehung mit einem Finger</span><span class="sxs-lookup"><span data-stu-id="21a64-125">Single Finger Rotation</span></span>](single-finger-rotation.md)                                               | <span data-ttu-id="21a64-126">Erläutert, wie ein Objekt mithilfe eines pivotpunkts und des Manipulations Prozessors gedreht wird.</span><span class="sxs-lookup"><span data-stu-id="21a64-126">Explains how to rotate an object by using a pivot point and the manipulation processor.</span></span>                                                              |



 

## <a name="related-topics"></a><span data-ttu-id="21a64-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="21a64-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="21a64-128">Manipulationen und Trägheit</span><span class="sxs-lookup"><span data-stu-id="21a64-128">Manipulations and Inertia</span></span>](manipulation-and-inertia.md)
</dt> </dl>

 

 




