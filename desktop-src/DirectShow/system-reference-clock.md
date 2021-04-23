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
# <a name="system-reference-clock"></a>Systemreferenzuhr

Das Systemverweisuhr-Objekt implementiert eine Verweisuhr, die die Systemzeit zurückgibt. Wenn keiner der Filter im Diagramm eine Referenzuhr enthält, verwendet der Filterdiagramm-Manager diese Komponente, um das Diagramm zu synchronisieren. Erstellen Sie dieses Objekt, indem Sie **CoCreateInstance aufrufen.**



| Bezeichnung | Wert |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Klassenbezeichner | CLSID \_ SystemClock                                                                                                                                       |
| Schnittstellen       | [**IAMClockAdjust**](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust), [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock), [**IReferenceClockTimerControl**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclocktimercontrol) |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Objekte](directshow-objects.md)
</dt> <dt>

[Referenzuhren](reference-clocks.md)
</dt> <dt>

[Zeit und Uhren in DirectShow](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



