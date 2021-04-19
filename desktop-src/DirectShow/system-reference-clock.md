---
description: Systemverweisuhr
ms.assetid: 0247dcb9-64ee-4562-944a-44bcfae80f2d
title: Systemverweisuhr
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67fab63c4ba8bfd6a7db9c476179d6e649869fb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368903"
---
# <a name="system-reference-clock"></a><span data-ttu-id="61a6b-103">Systemverweisuhr</span><span class="sxs-lookup"><span data-stu-id="61a6b-103">System Reference Clock</span></span>

<span data-ttu-id="61a6b-104">Das System Reference Clock-Objekt implementiert eine Referenzuhr, die die System Zeit zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="61a6b-104">The System Reference Clock object implements a reference clock that returns the system time.</span></span> <span data-ttu-id="61a6b-105">Wenn keiner der Filter im Diagramm eine Referenzuhr bereitstellt, verwendet der Filter Graph-Manager diese Komponente, um das Diagramm zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="61a6b-105">If none of the filters in the graph provides a reference clock, the filter graph manager uses this component to synchronize the graph.</span></span> <span data-ttu-id="61a6b-106">Erstellen Sie dieses Objekt durch Aufrufen von **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="61a6b-106">Create this object by calling **CoCreateInstance**.</span></span>



|                  |                                                                                                                                                          |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61a6b-107">Klassen Bezeichner</span><span class="sxs-lookup"><span data-stu-id="61a6b-107">Class Identifier</span></span> | <span data-ttu-id="61a6b-108">CLSID- \_ Systemuhr</span><span class="sxs-lookup"><span data-stu-id="61a6b-108">CLSID\_SystemClock</span></span>                                                                                                                                       |
| <span data-ttu-id="61a6b-109">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="61a6b-109">Interfaces</span></span>       | <span data-ttu-id="61a6b-110">[**Iamclocksettings**](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust), [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock), [**ireferenceclocktimercontrol**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclocktimercontrol)</span><span class="sxs-lookup"><span data-stu-id="61a6b-110">[**IAMClockAdjust**](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust), [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock), [**IReferenceClockTimerControl**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclocktimercontrol)</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="61a6b-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="61a6b-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61a6b-112">DirectShow-Objekte</span><span class="sxs-lookup"><span data-stu-id="61a6b-112">DirectShow Objects</span></span>](directshow-objects.md)
</dt> <dt>

[<span data-ttu-id="61a6b-113">Referenzuhren</span><span class="sxs-lookup"><span data-stu-id="61a6b-113">Reference Clocks</span></span>](reference-clocks.md)
</dt> <dt>

[<span data-ttu-id="61a6b-114">Uhrzeit und Uhren in DirectShow</span><span class="sxs-lookup"><span data-stu-id="61a6b-114">Time and Clocks in DirectShow</span></span>](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



