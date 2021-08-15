---
description: Bei Verwendung von Peer Graphing oder der Peer grouping Infrastructures werden die Informationen (Datensätze), die Peers in einem Diagramm oder einer Gruppe veröffentlichen, als Datenbank auf jedem Peercomputer gespeichert.
ms.assetid: 1412b2eb-c97d-4415-998c-5f21eaadcc66
title: Datenbankimport und -export
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acc047e6f58c7aeab07f6d13f8f7364f3f2f1191e50320513bc153e34c4c042c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119979060"
---
# <a name="database-import-and-export"></a>Datenbankimport und -export

Bei Verwendung von Peer Graphing oder der Peer grouping Infrastructures werden die Informationen (Datensätze), die Peers in einem Diagramm oder einer Gruppe veröffentlichen, als Datenbank auf jedem Peercomputer gespeichert. Um eine Anwendung von einem Computer zu einem anderen Computer zu migrieren, können Sie eine Peer Graphing- oder Peergringdatenbank von einem Computer exportieren und dann auf einen anderen importieren.

In der folgenden Liste sind wichtige Informationen zum Arbeiten mit Datenbanken aufgeführt:

-   Sie können nur eine Datenbank importieren, die über denselben Graphen und dieselbe Peer-ID verfügt.
-   Sie können die Import- und Exportfunktionen nicht aufrufen, wenn [**PeerGraphListen,**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten) [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect)oder [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect) aufgerufen wurden.

**Die Peer graphing-Infrastruktur** verwendet die folgenden Aufrufe zum Importieren und Exportieren einer Datensatzdatenbank:

-   [**PeerGraphExportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergraphexportdatabase)
-   [**PeerGraphImportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergraphimportdatabase)

**Die Peergruppeninfrastruktur verwendet** die folgenden Aufrufe zum Importieren und Exportieren einer Datensatzdatenbank:

-   [**PeerGroupExportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergroupexportdatabase)
-   [**PeerGroupImportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergroupimportdatabase)

 

 



