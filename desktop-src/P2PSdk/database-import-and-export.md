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
# <a name="database-import-and-export"></a><span data-ttu-id="d12e8-103">Daten Bank Import und-Export</span><span class="sxs-lookup"><span data-stu-id="d12e8-103">Database Import and Export</span></span>

<span data-ttu-id="d12e8-104">Bei der Verwendung des Peer Diagramms oder der Peer Gruppierungs Infrastrukturen werden die Informationen (Datensätze), die Peers in einem Diagramm oder einer Gruppe veröffentlichen, als Datenbank auf jedem Peer Computer gespeichert.</span><span class="sxs-lookup"><span data-stu-id="d12e8-104">When using the Peer Graphing or the Peer Grouping Infrastructures, the information (records) that peers publish to a graph or group is stored as a database on each peer computer.</span></span> <span data-ttu-id="d12e8-105">Wenn Sie eine Anwendung von einem Computer auf einen anderen Computer migrieren möchten, können Sie eine Peer Diagramm-oder Peer Gruppierungs Datenbank von einem Computer exportieren und dann in einen anderen importieren.</span><span class="sxs-lookup"><span data-stu-id="d12e8-105">To migrate an application from one computer to another computer, you can export a Peer Graphing or Peer Grouping database from one computer, and then import it to another.</span></span>

<span data-ttu-id="d12e8-106">In der folgenden Liste sind wichtige Informationen zum Arbeiten mit Datenbanken aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="d12e8-106">The following list identifies important information about working with databases:</span></span>

-   <span data-ttu-id="d12e8-107">Sie können nur eine Datenbank importieren, die das gleiche Diagramm und die gleiche Peer-ID aufweist.</span><span class="sxs-lookup"><span data-stu-id="d12e8-107">You can only import a database that has the same graph and peer ID.</span></span>
-   <span data-ttu-id="d12e8-108">Sie können die Import-und Exportfunktionen nicht aufrufen, wenn " [**Peer Diagramm**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten)", " [**Peer groupconnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect)" oder " [**Peer Name Connect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect) " aufgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="d12e8-108">You cannot call the import and export functions if [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten), [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect), or [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect) have been called.</span></span>

<span data-ttu-id="d12e8-109">Die **Peer-graphinginfrastruktur** verwendet die folgenden Aufrufe zum Importieren und Exportieren einer datensatzdatenbank:</span><span class="sxs-lookup"><span data-stu-id="d12e8-109">**Peer Graphing Infrastructure** uses the following calls to import and export a record database:</span></span>

-   [<span data-ttu-id="d12e8-110">**Peer graphexportdatabase**</span><span class="sxs-lookup"><span data-stu-id="d12e8-110">**PeerGraphExportDatabase**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergraphexportdatabase)
-   [<span data-ttu-id="d12e8-111">**Peer graphimportdatabase**</span><span class="sxs-lookup"><span data-stu-id="d12e8-111">**PeerGraphImportDatabase**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergraphimportdatabase)

<span data-ttu-id="d12e8-112">Die **Peer Gruppierungs Infrastruktur** verwendet die folgenden Aufrufe zum Importieren und Exportieren einer datensatzdatenbank:</span><span class="sxs-lookup"><span data-stu-id="d12e8-112">**Peer Grouping Infrastructure** uses the following calls to import and export a record database:</span></span>

-   [<span data-ttu-id="d12e8-113">**"Peer groupexportdatabase"**</span><span class="sxs-lookup"><span data-stu-id="d12e8-113">**PeerGroupExportDatabase**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupexportdatabase)
-   [<span data-ttu-id="d12e8-114">**"Peer groupimportdatabase"**</span><span class="sxs-lookup"><span data-stu-id="d12e8-114">**PeerGroupImportDatabase**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupimportdatabase)

 

 



