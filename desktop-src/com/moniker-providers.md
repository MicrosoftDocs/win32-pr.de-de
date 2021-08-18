---
title: Monikeranbieter
description: Monikeranbieter
ms.assetid: 4d4820d2-bf5f-4543-b318-59481dcc51de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8fab6c5a84d7020b8bcb02979471cb2fbd76df7e66fc9909eec2121926827df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130102"
---
# <a name="moniker-providers"></a>Monikeranbieter

Im Allgemeinen sollte eine Komponente ein Monikeranbieter sein, wenn sie den Zugriff auf eines ihrer Objekte zulässt und gleichzeitig den Speicher des Objekts steuert. Wenn eine Komponente Moniker ausgibt, die ihre Objekte identifizieren, muss sie in der Lage sein, die folgenden Aufgaben auszuführen:

-   Erstellen Sie auf Anforderung einen Moniker, der ein Objekt identifiziert.
-   Aktivieren Sie die Bindung des Monikers, wenn ein Client [**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) dafür aufruft.

Ein Monikeranbieter muss einen Moniker einer geeigneten *Monikerklasse* erstellen, um ein Objekt zu identifizieren. Die Monikerklasse bezieht sich auf eine bestimmte Implementierung der [**IMoniker-Schnittstelle,**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) die den Typ des erstellten Monikers definiert. Obwohl Sie **IMoniker** implementieren können, um eine neue Monikerklasse zu erstellen, ist dies häufig unnötig, da OLE Implementierungen mehrerer verschiedener Monikerklassen bereitstellt, die jeweils eine eigene CLSID haben. Beschreibungen von Monikerklassen, die OLE bereitstellt, finden Sie unter [OLE-Monikerimplementierungen.](ole-moniker-implementations.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Monikerclients](moniker-clients.md)
</dt> <dt>

[OLE-Monikerimplementierungen](ole-moniker-implementations.md)
</dt> </dl>

 

 




