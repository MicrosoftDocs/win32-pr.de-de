---
description: Verbinden von topologieknoten und Trennen der Verbindung
ms.assetid: b2f70989-f0a8-4a11-baeb-18f026afaeab
title: Verbinden von topologieknoten und Trennen der Verbindung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08057eba74314ae6b87da418b743a089506a3b26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344235"
---
# <a name="connecting-and-disconnecting-topology-nodes"></a>Verbinden von topologieknoten und Trennen der Verbindung

Damit eine Topologie funktionsfähig ist, müssen der Quellknoten und der Ausgabe Knoten verbunden sein. Um zwei topologieknoten zu verbinden, ziehen Sie die Knoten Ausgabe eines Knotens auf die Knoten Eingabe des anderen Knotens. In topoedit wird die Knoten Verbindung als schwarze Linie angezeigt. Dies entspricht dem Verbinden von topologieknoten durch Aufrufen der [**imftopologynode:: ConnectOutput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput) -Methode.

Die Topologie kann nur aufgelöst werden, wenn die Knoten Verbindung gültig ist. Das heißt, wenn die Medientypen der beiden Knoten kompatibel sind. Informationen zum Auflösen von Topologien finden Sie unter [Auflösen einer Topologie mit topoedit](resolving-a-topology-with-topoedit.md).

Wenn Sie versuchen, eine Verbindung von einem bereits verbundenen Knoten herzustellen, ersetzt die neue Knoten Verbindung die alte Knoten Verbindung.

Um eine Verbindung zu löschen, wählen Sie die Knoten Verbindung aus, und drücken Sie die ENTF-Taste, oder wählen Sie **Löschen** aus dem Menü **Topologie** .

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwickeln von Topologien mithilfe von topoedit](building-topologies-by-using-topoedit.md)
</dt> <dt>

[Topoedit](topoedit.md)
</dt> </dl>

 

 



