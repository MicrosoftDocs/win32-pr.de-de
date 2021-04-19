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
# <a name="system-reference-clock"></a>Systemverweisuhr

Das System Reference Clock-Objekt implementiert eine Referenzuhr, die die System Zeit zurückgibt. Wenn keiner der Filter im Diagramm eine Referenzuhr bereitstellt, verwendet der Filter Graph-Manager diese Komponente, um das Diagramm zu synchronisieren. Erstellen Sie dieses Objekt durch Aufrufen von **CoCreateInstance**.



|                  |                                                                                                                                                          |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Klassen Bezeichner | CLSID- \_ Systemuhr                                                                                                                                       |
| Schnittstellen       | [**Iamclocksettings**](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust), [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock), [**ireferenceclocktimercontrol**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclocktimercontrol) |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Objekte](directshow-objects.md)
</dt> <dt>

[Referenzuhren](reference-clocks.md)
</dt> <dt>

[Uhrzeit und Uhren in DirectShow](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



