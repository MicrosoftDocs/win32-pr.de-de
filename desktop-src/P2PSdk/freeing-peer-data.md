---
description: Alle Zeiger, die von den Peer Infrastrukturfunktionen zurückgegeben werden, müssen mithilfe von peergraphfredata oder peerfredata freigegeben werden.
ms.assetid: c7669404-2550-4f0d-908e-540d9a34008f
title: Freigeben von Peer Daten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1addb0533d5d05e329e19bfe27a89f5616473a51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042267"
---
# <a name="freeing-peer-data"></a><span data-ttu-id="2a328-103">Freigeben von Peer Daten</span><span class="sxs-lookup"><span data-stu-id="2a328-103">Freeing Peer Data</span></span>

<span data-ttu-id="2a328-104">Alle Zeiger, die von den Peer Infrastrukturfunktionen zurückgegeben werden, müssen mithilfe von [**peergraphfredata**](/windows/desktop/api/P2P/nf-p2p-peergraphfreedata) oder [**peerfredata**](/windows/desktop/api/P2P/nf-p2p-peerfreedata)freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2a328-104">All pointers that the Peer Infrastructure functions return must be freed by using [**PeerGraphFreeData**](/windows/desktop/api/P2P/nf-p2p-peergraphfreedata) or [**PeerFreeData**](/windows/desktop/api/P2P/nf-p2p-peerfreedata).</span></span> <span data-ttu-id="2a328-105">Diese Funktionen dürfen nur für Strukturen aufgerufen werden, die direkt von einer Peer Infrastruktur Funktion zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2a328-105">These functions must only be called for structures that are directly returned by a Peer Infrastructure function.</span></span> <span data-ttu-id="2a328-106">Wenn Sie keine andere freedata-Funktion zum Freigeben von verknüpften Zeigern verwenden, können Sie z. b. keine freedata-Funktion für die Zeiger in einer [**Peer \_ Daten Satz**](/windows/desktop/api/P2P/ns-p2p-peer_record) Struktur aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="2a328-106">Do not call a different FreeData function to free nested pointers, for example, do not call a FreeData function on the pointers in a [**PEER\_RECORD**](/windows/desktop/api/P2P/ns-p2p-peer_record) structure.</span></span>

## <a name="example-of-freeing-data"></a><span data-ttu-id="2a328-107">Beispiel für das Freigeben von Daten</span><span class="sxs-lookup"><span data-stu-id="2a328-107">Example of Freeing Data</span></span>

<span data-ttu-id="2a328-108">Der folgende Code Ausschnitt zeigt, wie Sie die einem Diagramm zugeordneten Eigenschaften abrufen und dann die zurückgegebenen Daten freigeben.</span><span class="sxs-lookup"><span data-stu-id="2a328-108">The following code snippet shows you how to retrieve the properties associated with a graph, and then free the data that is returned.</span></span>


```C++
PEER_GRAPH_PROPERTIES  * pGraphProperties = NULL;
HRESULT hr = PeerGraphGetProperties(hGraph, &pGraphProperties);
if (SUCCEEDED(hr) && (NULL != pGraphProperties))
{
  // use pGraphProperties
  wprintf(L"%d\n", pGraphProperties->pwzGraphId);

  // release the data
  PeerGraphFreeData(pGraphProperties);
}
```



 

 



