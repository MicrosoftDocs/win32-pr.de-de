---
description: Erstellen von Topologien
ms.assetid: afd1e646-9bb6-4265-a225-6aaaf1a7bb2a
title: Erstellen von Topologien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a9ec738c82ea2b85bcae7d4c05627b81ad939db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393294"
---
# <a name="creating-topologies"></a>Erstellen von Topologien

In diesem Abschnitt werden einige der allgemeinen Verfahren zum Erstellen einer Topologie beschrieben.

Die allgemeinen Schritte zum Erstellen einer Topologie lauten wie folgt:

1.  Erstellen Sie ein neues Topologieobjekt durch Aufrufen von [**mfcreatetopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology). Diese Funktion gibt einen Zeiger auf die [**imftopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) -Schnittstelle der Topologie zurück.

2.  Anfänglich enthält die Topologie keine Knoten. Um Knoten für die Topologie zu erstellen, rufen Sie [**mfkreatetopologynode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode)auf. Diese Funktion gibt einen Zeiger auf die [**imftopologynode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode) -Schnittstelle des Knotens zurück. Beim Erstellen des Knotens müssen Sie den Knotentyp angeben:

    -   Quellknoten.

    -   Knoten transformieren.

    -   Ausgabe Knoten.

    -   Tee-Knoten.

3.  Initialisieren Sie jeden Knoten. Der Initialisierungs Prozess hängt vom Knotentyp ab, wie in den folgenden Themen beschrieben.

4.  Fügen Sie jeden Knoten der Topologie hinzu, indem Sie [**imftopology:: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode)aufrufen.

5.  Verbinden Sie die Knoten. Um einen Knoten zu verbinden, nennen Sie [**imftopologynode:: ConnectOutput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput) auf dem upstreamknoten, und übergeben Sie einen Zeiger auf den downstreamknoten.

In den folgenden Themen werden die spezifischen Schritte für die einzelnen Knoten Typen beschrieben.



| Thema                                                    | BESCHREIBUNG                     |
|----------------------------------------------------------|---------------------------------|
| [Erstellen von Quellknoten](creating-source-nodes.md)       | Erstellen eines Quell Knotens    |
| [Erstellen von Transformations Knoten](creating-transform-nodes.md) | So erstellen Sie einen Transformations Knoten. |
| [Erstellen von Ausgabe Knoten](creating-output-nodes.md)       | So erstellen Sie einen Ausgabe Knoten.   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Topologien](topologies.md)
</dt> </dl>

 

 



