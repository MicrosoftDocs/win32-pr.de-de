---
description: Systemreferenzuhr
ms.assetid: 0247dcb9-64ee-4562-944a-44bcfae80f2d
title: Systemreferenzuhr
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c8de8b208e32b6ea4772f3183c38a816ea43bb6
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909488"
---
# <a name="system-reference-clock"></a><span data-ttu-id="61f21-103">Systemreferenzuhr</span><span class="sxs-lookup"><span data-stu-id="61f21-103">System Reference Clock</span></span>

<span data-ttu-id="61f21-104">Das Systemverweisuhr-Objekt implementiert eine Verweisuhr, die die Systemzeit zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="61f21-104">The System Reference Clock object implements a reference clock that returns the system time.</span></span> <span data-ttu-id="61f21-105">Wenn keiner der Filter im Diagramm eine Referenzuhr enthält, verwendet der Filterdiagramm-Manager diese Komponente, um das Diagramm zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="61f21-105">If none of the filters in the graph provides a reference clock, the filter graph manager uses this component to synchronize the graph.</span></span> <span data-ttu-id="61f21-106">Erstellen Sie dieses Objekt, indem Sie **CoCreateInstance aufrufen.**</span><span class="sxs-lookup"><span data-stu-id="61f21-106">Create this object by calling **CoCreateInstance**.</span></span>



| <span data-ttu-id="61f21-107">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="61f21-107">Label</span></span> | <span data-ttu-id="61f21-108">Wert</span><span class="sxs-lookup"><span data-stu-id="61f21-108">Value</span></span> |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61f21-109">Klassenbezeichner</span><span class="sxs-lookup"><span data-stu-id="61f21-109">Class Identifier</span></span> | <span data-ttu-id="61f21-110">CLSID \_ SystemClock</span><span class="sxs-lookup"><span data-stu-id="61f21-110">CLSID\_SystemClock</span></span>                                                                                                                                       |
| <span data-ttu-id="61f21-111">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="61f21-111">Interfaces</span></span>       | <span data-ttu-id="61f21-112">[**IAMClockAdjust**](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust), [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock), [**IReferenceClockTimerControl**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclocktimercontrol)</span><span class="sxs-lookup"><span data-stu-id="61f21-112">[**IAMClockAdjust**](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust), [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock), [**IReferenceClockTimerControl**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclocktimercontrol)</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="61f21-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="61f21-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61f21-114">DirectShow-Objekte</span><span class="sxs-lookup"><span data-stu-id="61f21-114">DirectShow Objects</span></span>](directshow-objects.md)
</dt> <dt>

[<span data-ttu-id="61f21-115">Referenzuhren</span><span class="sxs-lookup"><span data-stu-id="61f21-115">Reference Clocks</span></span>](reference-clocks.md)
</dt> <dt>

[<span data-ttu-id="61f21-116">Zeit und Uhren in DirectShow</span><span class="sxs-lookup"><span data-stu-id="61f21-116">Time and Clocks in DirectShow</span></span>](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



