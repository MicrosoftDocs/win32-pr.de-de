---
description: Bei der Verwendung des Peer Diagramms oder der Peer Gruppierungs Infrastrukturen werden die Informationen (Datensätze), die Peers in einem Diagramm oder einer Gruppe veröffentlichen, als Datenbank auf jedem Peer Computer gespeichert.
ms.assetid: 1412b2eb-c97d-4415-998c-5f21eaadcc66
title: Daten Bank Import und-Export
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b48fc09259c06e6ebaf537d26c7288d0ad09c501
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959788"
---
# <a name="database-import-and-export"></a>Daten Bank Import und-Export

Bei der Verwendung des Peer Diagramms oder der Peer Gruppierungs Infrastrukturen werden die Informationen (Datensätze), die Peers in einem Diagramm oder einer Gruppe veröffentlichen, als Datenbank auf jedem Peer Computer gespeichert. Wenn Sie eine Anwendung von einem Computer auf einen anderen Computer migrieren möchten, können Sie eine Peer Diagramm-oder Peer Gruppierungs Datenbank von einem Computer exportieren und dann in einen anderen importieren.

In der folgenden Liste sind wichtige Informationen zum Arbeiten mit Datenbanken aufgeführt:

-   Sie können nur eine Datenbank importieren, die das gleiche Diagramm und die gleiche Peer-ID aufweist.
-   Sie können die Import-und Exportfunktionen nicht aufrufen, wenn " [**Peer Diagramm**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten)", " [**Peer groupconnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect)" oder " [**Peer Name Connect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect) " aufgerufen wurden.

Die **Peer-graphinginfrastruktur** verwendet die folgenden Aufrufe zum Importieren und Exportieren einer datensatzdatenbank:

-   [**Peer graphexportdatabase**](/windows/desktop/api/P2P/nf-p2p-peergraphexportdatabase)
-   [**Peer graphimportdatabase**](/windows/desktop/api/P2P/nf-p2p-peergraphimportdatabase)

Die **Peer Gruppierungs Infrastruktur** verwendet die folgenden Aufrufe zum Importieren und Exportieren einer datensatzdatenbank:

-   [**"Peer groupexportdatabase"**](/windows/desktop/api/P2P/nf-p2p-peergroupexportdatabase)
-   [**"Peer groupimportdatabase"**](/windows/desktop/api/P2P/nf-p2p-peergroupimportdatabase)

 

 



