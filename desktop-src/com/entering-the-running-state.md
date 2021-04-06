---
title: Eingeben des Status "wird ausgeführt"
description: Eingeben des Status "wird ausgeführt"
ms.assetid: 2173eaa9-0e60-4411-81e4-dbabc5fe89b2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 959038c8f64fe8750ab1bcf0f06b753371f04136
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947655"
---
# <a name="entering-the-running-state"></a>Eingeben des Status "wird ausgeführt"

Wenn ein eingebettetes Objekt den Übergang in den Status "wird ausgeführt" durchführt, muss der Objekt Handler die Serveranwendung suchen und ausführen, um die Dienste zu nutzen, die nur der Server bereitstellt. Eingebettete Objekte werden entweder explizit durch eine Anforderung durch den Container in den Zustand wird ausgeführt versetzt, z. b. das Zeichnen eines Formats, das derzeit nicht zwischengespeichert ist, oder implizit durch OLE als Reaktion auf das Aufrufen eines Vorgangs, z. b. Wenn ein Benutzer des Containers auf das Objekt doppelklickt.

Wenn ein verknüpftes Objekt den Übergang in den Status "wird ausgeführt" versetzt, wird der Prozess als *Bindung* bezeichnet. Beim Bindungs Vorgang fragt der Objekt Handler seinen gespeicherten Moniker ab, um die Daten des Links zu finden, und führt dann die Serveranwendung aus.

Auf den ersten Blick scheint das Binden eines verknüpften Objekts nicht komplizierter als das Ausführen eines eingebetteten Objekts zu sein. Die folgenden Punkte erschweren jedoch den Prozess:

-   Ein Link kann auf ein Objekt oder einen Teil davon verweisen, das in einen anderen Container eingebettet ist. Diese Funktion impliziert ein Potenzial für eingefügte Einbettungen. Das Auflösen von Verweisen auf eine solche Hierarchie erfordert rekursiv durchlaufen eines zusammen *gesetzten Monikers*, beginnend mit dem äußersten rechten Member.
-   Wenn die Verknüpfungs Quelle ausgeführt wird, bindet OLE an die laufende Instanz des Objekts, anstatt eine andere Instanz zu betreiben. Im Fall von in einer Tabelle eingebetteten eingebetteten Objekten, von denen eine die Verknüpfungs Quelle ist, muss OLE an einem beliebigen Punkt an ein bereits laufendes Objekt gebunden werden können.
-   Das Ausführen eines Objekts erfordert den Zugriff auf den Speicherbereich für das Objekt. Wenn ein eingebettetes Objekt ausgeführt wird, empfängt OLE einen Zeiger auf den Speicher während des Ladevorgangs, der an die OLE-Serveranwendung weitergeleitet wird. Für verknüpfte Objekte gibt es jedoch keine Standardschnittstelle für den Zugriff auf den Speicher. Die OLE Server-Anwendung kann die Dateisystem Schnittstelle oder einen anderen Mechanismus verwenden.

 

 




