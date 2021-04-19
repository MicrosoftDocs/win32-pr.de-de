---
description: Zum Verwalten von Datensätzen können Sie mit Informationen arbeiten, die in Peer \_ Datensatzstrukturen gespeichert werden.
ms.assetid: d38ea2d3-5cfb-4c4a-a63f-b274aa0dfe71
title: Daten Satz Verwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c762689263e4a012bbdfad726b13e3ee8c79397e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364066"
---
# <a name="record-management"></a><span data-ttu-id="eaef1-103">Daten Satz Verwaltung</span><span class="sxs-lookup"><span data-stu-id="eaef1-103">Record Management</span></span>

<span data-ttu-id="eaef1-104">Zum Verwalten von Datensätzen können Sie mit Informationen arbeiten, die in [**Peer \_ Daten Satz**](/windows/desktop/api/P2P/ns-p2p-peer_record) Strukturen gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="eaef1-104">To manage records, you can work with information that is stored in [**PEER\_RECORD**](/windows/desktop/api/P2P/ns-p2p-peer_record) structures.</span></span> <span data-ttu-id="eaef1-105">Wenn Datensätze erstellt, aktualisiert oder gelöscht werden, werden die an einem Diagramm vorgenommenen Änderungen auf allen Knoten repliziert.</span><span class="sxs-lookup"><span data-stu-id="eaef1-105">When records are created, updated, or deleted, the changes made to a graph are replicated to all nodes.</span></span> <span data-ttu-id="eaef1-106">In der folgenden Tabelle sind die Regeln zum Aktualisieren und automatischen Aktualisieren von Datensätzen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="eaef1-106">The following table identifies the rules for updating and automatically refreshing records.</span></span>



| <span data-ttu-id="eaef1-107">Verwaltungstask</span><span class="sxs-lookup"><span data-stu-id="eaef1-107">Management Task</span></span>     | <span data-ttu-id="eaef1-108">Regel</span><span class="sxs-lookup"><span data-stu-id="eaef1-108">Rule</span></span>                                                                                                                                                                                                            |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eaef1-109">Aktualisieren eines Datensatzes</span><span class="sxs-lookup"><span data-stu-id="eaef1-109">Updating a record</span></span>   | <span data-ttu-id="eaef1-110">Behalten Sie die Ablaufzeit bei, oder erhöhen Sie Sie.</span><span class="sxs-lookup"><span data-stu-id="eaef1-110">Keep the expiration time the same or increase it.</span></span> <span data-ttu-id="eaef1-111">Die Ablaufzeit kann nicht verringert werden.</span><span class="sxs-lookup"><span data-stu-id="eaef1-111">You cannot decrease the expiration time.</span></span>                                                                                                                      |
| <span data-ttu-id="eaef1-112">Aktualisieren eines Datensatzes</span><span class="sxs-lookup"><span data-stu-id="eaef1-112">Refreshing a record</span></span> | <span data-ttu-id="eaef1-113">Verwenden Sie zum automatischen Aktualisieren eines Datensatzes das Flag " [**\_ \_ \_ autoefresh" des Peer Datensatzes**](/windows/desktop/api/P2P/ns-p2p-peer_record) .</span><span class="sxs-lookup"><span data-stu-id="eaef1-113">Use the [**PEER\_RECORD\_FLAG\_AUTOREFRESH**](/windows/desktop/api/P2P/ns-p2p-peer_record) flag to automatically refresh a record.</span></span> <span data-ttu-id="eaef1-114">Verwenden Sie dieses Flag nur, wenn der Knoten, der einen Datensatz veröffentlicht, Online ist.</span><span class="sxs-lookup"><span data-stu-id="eaef1-114">Only use this flag when the node that is publishing a record is online.</span></span> <span data-ttu-id="eaef1-115">Verwenden Sie andernfalls das Flag nicht.</span><span class="sxs-lookup"><span data-stu-id="eaef1-115">Otherwise, do not use this flag.</span></span> |



 

 

 



