---
title: Eingeben des Status "Wird ausgeführt"
description: Eingeben des Status "Wird ausgeführt"
ms.assetid: 2173eaa9-0e60-4411-81e4-dbabc5fe89b2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e91261df578697afef0e33dd8c8ea847eb50cfd546dd96ee0a0085d67100bfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119501060"
---
# <a name="entering-the-running-state"></a>Eingeben des Status "Wird ausgeführt"

Wenn ein eingebettetes Objekt den Übergang in den Ausführungszustand vor sich geht, muss der Objekthandler die Serveranwendung suchen und ausführen, um die Dienste zu nutzen, die nur vom Server zur Verfügung stellen. Eingebettete Objekte werden entweder explizit über eine Anforderung des Containers in den Ausführungszustand gesetzt, z. B. durch die Notwendigkeit, ein Format zu zeichnen, das derzeit nicht zwischengespeichert ist, oder implizit von OLE als Reaktion auf den Aufruf eines Vorgangs, z. B. wenn ein Benutzer des Containers auf das Objekt doppelklickt.

Wenn ein verknüpftes Objekt den Übergang in den Ausführungszustand vor sich geht, wird der Prozess als Bindung *bezeichnet.* Während der Bindung fordert der Objekthandler seinen gespeicherten Moniker auf, die Daten des Links zu suchen, und führt dann die Serveranwendung aus.

Auf den ersten Blick scheint das Binden eines verknüpften Objekts nicht komplizierter als das Ausführen eines eingebetteten Objekts zu sein. Die folgenden Punkte erschweren jedoch den Prozess:

-   Ein Link kann auf ein Objekt oder einen Teil davon verweisen, das in einen anderen Container eingebettet ist. Diese Funktion impliziert ein Potenzial für geschachtelte Einbettungen. Das Auflösen von Verweisen auf eine solche Hierarchie erfordert das rekursive Durchlaufen eines zusammengesetzten *Monikers,* beginnend mit dem äußersten rechten Member.
-   Wenn die Linkquelle ausgeführt wird, wird OLE an die ausgeführte Instanz des -Objekts gebunden, anstatt eine andere Instanz ausführen zu müssen. Bei geschachtelten eingebetteten Objekten, von denen eines die Linkquelle ist, muss OLE jederzeit eine Bindung an ein bereits ausgeführtes Objekt erstellen können.
-   Das Ausführen eines Objekts erfordert den Zugriff auf den Speicherbereich für das Objekt. Wenn ein eingebettetes Objekt ausgeführt wird, empfängt OLE während des Ladevorgangs einen Zeiger auf den Speicher, den es an die OLE-Serveranwendung weitergibt. Für verknüpfte Objekte gibt es jedoch keine Standardschnittstelle für den Zugriff auf Speicher. Die OLE-Serveranwendung kann die Dateisystemschnittstelle oder einen anderen Mechanismus verwenden.

 

 




