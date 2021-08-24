---
description: Erstellen von Topologien
ms.assetid: afd1e646-9bb6-4265-a225-6aaaf1a7bb2a
title: Erstellen von Topologien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4048200055066a601f9044ff109f173cb00fc4449a71ea1331b29c8be1a59b8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777620"
---
# <a name="creating-topologies"></a>Erstellen von Topologien

In diesem Abschnitt werden einige der allgemeinen Verfahren zum Erstellen einer Topologie beschrieben.

Die allgemeinen Schritte zum Erstellen einer Topologie sind wie folgt:

1.  Erstellen Sie ein neues Topologieobjekt, indem Sie [**MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology)aufrufen. Diese Funktion gibt einen Zeiger auf [**dieTOPTOPOLOGY-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) der Topologie zurück.

2.  Anfänglich enthält die Topologie keine Knoten. Um Knoten für die Topologie zu erstellen, rufen [**Sie MFCreateTopologyNode auf.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) Diese Funktion gibt einen Zeiger auf die [**NODESTopologyNode-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode) des Knotens zurück. Sie müssen den Knotentyp angeben, wenn Sie den Knoten erstellen:

    -   Quellknoten.

    -   Knoten transformieren.

    -   Ausgabeknoten.

    -   Tee-Knoten.

3.  Initialisieren Sie jeden Knoten. Der Initialisierungsprozess hängt vom Knotentyp ab, wie in den folgenden Themen beschrieben.

4.  Fügen Sie jeden Knoten der Topologie hinzu, indem Sie [**DIE KNOTENTOPTOPOLOGIE::AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode)aufrufen.

5.  Verbinden die Knoten. Um eine Verbindung mit einem Knoten herzustellen, rufen Sie [**AUFTOPTOPOLOGYNode::ConnectOutput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput) auf dem Upstreamknoten auf, und übergeben Sie einen Zeiger auf den Downstreamknoten.

In den folgenden Themen werden die spezifischen Schritte für jeden Knotentyp beschrieben.



| Thema                                                    | Beschreibung                     |
|----------------------------------------------------------|---------------------------------|
| [Erstellen von Quellknoten](creating-source-nodes.md)       | Erstellen eines Quellknotens    |
| [Erstellen von Transformationsknoten](creating-transform-nodes.md) | Erstellen eines Transformationsknotens. |
| [Erstellen von Ausgabeknoten](creating-output-nodes.md)       | Erstellen eines Ausgabeknotens.   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Topologien](topologies.md)
</dt> </dl>

 

 



