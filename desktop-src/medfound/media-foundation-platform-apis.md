---
description: Media Foundation Plattform-APIs
ms.assetid: 1eb20c44-58cb-4e34-a108-1b3c27d54ff1
title: Media Foundation Plattform-APIs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed1e8d8aa0dcd5d7b1184a406e09910a98892f4f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106371822"
---
# <a name="media-foundation-platform-apis"></a><span data-ttu-id="f5069-103">Media Foundation Plattform-APIs</span><span class="sxs-lookup"><span data-stu-id="f5069-103">Media Foundation Platform APIs</span></span>

<span data-ttu-id="f5069-104">Die Platt Form Ebene Media Foundation enthält primitive und Hilfsobjekte, die von den anderen Ebenen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f5069-104">The platform layer of Media Foundation contains primitives and helper objects used by the other layers.</span></span>

<span data-ttu-id="f5069-105">Dieser Abschnitt enthält die folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="f5069-105">This section contains the following topics:</span></span>



| <span data-ttu-id="f5069-106">Thema</span><span class="sxs-lookup"><span data-stu-id="f5069-106">Topic</span></span>                                                                           | <span data-ttu-id="f5069-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f5069-107">Description</span></span>                                                                                                                                                       |
|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f5069-108">Initialisieren der Media Foundation Plattform</span><span class="sxs-lookup"><span data-stu-id="f5069-108">Initializing the Media Foundation Platform</span></span>](initializing-media-foundation.md) | <span data-ttu-id="f5069-109">Initialisieren der Media Foundation Plattform.</span><span class="sxs-lookup"><span data-stu-id="f5069-109">How to initialize the Media Foundation platform.</span></span>                                                                                                                  |
| [<span data-ttu-id="f5069-110">Media Foundation und com</span><span class="sxs-lookup"><span data-stu-id="f5069-110">Media Foundation and COM</span></span>](media-foundation-and-com.md)                        | <span data-ttu-id="f5069-111">Beschreibt die Interaktion zwischen com und Microsoft Media Foundation und definiert einige bewährte Methoden für die Entwicklung von Media Foundation-Plug-in-Komponenten.</span><span class="sxs-lookup"><span data-stu-id="f5069-111">Describes the interaction between COM and Microsoft Media Foundation, and defines some best practices to use when developing Media Foundation plug-in components.</span></span> |
| [<span data-ttu-id="f5069-112">Asynchrone Rückruf Methoden</span><span class="sxs-lookup"><span data-stu-id="f5069-112">Asynchronous Callback Methods</span></span>](asynchronous-callback-methods.md)              | <span data-ttu-id="f5069-113">Wie asynchrone Methoden aufgerufen werden und wie asynchrone Vorgänge in Media Foundation implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="f5069-113">How to call asynchronous methods and how to implement asynchronous operations in Media Foundation.</span></span>                                                                |
| [<span data-ttu-id="f5069-114">Arbeits Warteschlangen</span><span class="sxs-lookup"><span data-stu-id="f5069-114">Work Queues</span></span>](work-queues.md)                                                  | <span data-ttu-id="f5069-115">Eine Arbeits Warteschlange ist eine effiziente Möglichkeit, um asynchrone Vorgänge in einem anderen Thread auszuführen.</span><span class="sxs-lookup"><span data-stu-id="f5069-115">A work queue is an efficient way to perform asynchronous operations on another thread.</span></span>                                                                            |
| [<span data-ttu-id="f5069-116">Medienereignis Generatoren</span><span class="sxs-lookup"><span data-stu-id="f5069-116">Media Event Generators</span></span>](media-event-generators.md)                            | <span data-ttu-id="f5069-117">So empfangen Sie asynchrone Ereignisse und wie Ereignisse in Media Foundation ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f5069-117">How to receive asynchronous events and how to raise events in Media Foundation.</span></span>                                                                                   |
| [<span data-ttu-id="f5069-118">Dienst Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="f5069-118">Service Interfaces</span></span>](service-interfaces.md)                                    | <span data-ttu-id="f5069-119">Eine Dienst Schnittstelle ist eine COM-Schnittstelle, die von einem Objekt bereitgestellt wird, aber für die Anwendung über ein anderes Objekt verfügbar gemacht wird</span><span class="sxs-lookup"><span data-stu-id="f5069-119">A service interface is a COM interface provided by one object, but exposed to the application through another object.</span></span>                                             |
| [<span data-ttu-id="f5069-120">Aktivierungs Objekte</span><span class="sxs-lookup"><span data-stu-id="f5069-120">Activation Objects</span></span>](activation-objects.md)                                    | <span data-ttu-id="f5069-121">Ein Aktivierungs Objekt ist ein Objekt, das ein anderes Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="f5069-121">An activation object is an object that creates another object.</span></span>                                                                                                    |
| [<span data-ttu-id="f5069-122">Präsentations Uhr</span><span class="sxs-lookup"><span data-stu-id="f5069-122">Presentation Clock</span></span>](presentation-clock.md)                                    | <span data-ttu-id="f5069-123">Die Präsentations Uhr generiert die Uhrzeit, die zum Steuern der Wiedergabe verwendet wird, sowie synchrone Audiodaten und Videostreams.</span><span class="sxs-lookup"><span data-stu-id="f5069-123">The presentation clock generates the clock time that is used to control playback, and also to synchronous audio and video streams.</span></span>                                |



 

## <a name="related-topics"></a><span data-ttu-id="f5069-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f5069-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5069-125">Media Foundation-Architektur</span><span class="sxs-lookup"><span data-stu-id="f5069-125">Media Foundation Architecture</span></span>](media-foundation-architecture.md)
</dt> <dt>

[<span data-ttu-id="f5069-126">Media Foundation-Programmier Handbuch</span><span class="sxs-lookup"><span data-stu-id="f5069-126">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
</dt> </dl>

 

 



