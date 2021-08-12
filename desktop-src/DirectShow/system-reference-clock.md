---
description: Systemreferenzuhr
ms.assetid: 0247dcb9-64ee-4562-944a-44bcfae80f2d
title: Systemreferenzuhr
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9b3b4fa69b2ff9b74b937dd38d8be83203d5cdd43ba9a26d2cac4077c40c811
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118651840"
---
# <a name="system-reference-clock"></a>Systemreferenzuhr

Das Systemverweisuhr-Objekt implementiert eine Verweisuhr, die die Systemzeit zurückgibt. Wenn keiner der Filter im Diagramm eine Referenzuhr bereitstellt, verwendet der Filtergraph-Manager diese Komponente, um das Diagramm zu synchronisieren. Erstellen Sie dieses Objekt, indem **Sie CoCreateInstance** aufrufen.



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

[Uhrzeit und Uhren in DirectShow](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



