---
title: Monikeranbieter
description: Monikeranbieter
ms.assetid: 4d4820d2-bf5f-4543-b318-59481dcc51de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fde584e12daddacbc940b23b21a0386aa37de2c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710350"
---
# <a name="moniker-providers"></a>Monikeranbieter

Im Allgemeinen sollte eine Komponente ein monikeranbieter sein, wenn Sie den Zugriff auf eines ihrer Objekte zulässt, während der Speicher des Objekts weiterhin gesteuert wird. Wenn eine Komponente Moniker weitergibt, die ihre Objekte identifizieren, muss Sie in der Lage sein, die folgenden Aufgaben auszuführen:

-   Erstellen Sie bei der Anforderung einen Moniker, der ein Objekt identifiziert.
-   Aktivieren Sie den Moniker, der gebunden werden soll, wenn ein Client [**IMoniker:: bindjeobject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) darauf aufruft.

Ein monikeranbieter muss einen Moniker einer entsprechenden *Monikerklasse* erstellen, um ein Objekt zu identifizieren. Die Monikerklasse verweist auf eine bestimmte Implementierung der [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) -Schnittstelle, die den Typ des erstellten Monikers definiert. Obwohl Sie **IMoniker** implementieren können, um eine neue Monikerklasse zu erstellen, ist dies häufig unnötig, da OLE Implementierungen mehrerer unterschiedlicher Moniker-Klassen bereitstellt, die jeweils über eine eigene CLSID verfügen. Unter [OLE-Monikerimplementierungen](ole-moniker-implementations.md) finden Sie Beschreibungen der Monikerklassen, die von OLE bereitstellt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Monikerclients](moniker-clients.md)
</dt> <dt>

[OLE-Monikerimplementierungen](ole-moniker-implementations.md)
</dt> </dl>

 

 




