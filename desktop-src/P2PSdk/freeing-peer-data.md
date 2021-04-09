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
# <a name="freeing-peer-data"></a>Freigeben von Peer Daten

Alle Zeiger, die von den Peer Infrastrukturfunktionen zurückgegeben werden, müssen mithilfe von [**peergraphfredata**](/windows/desktop/api/P2P/nf-p2p-peergraphfreedata) oder [**peerfredata**](/windows/desktop/api/P2P/nf-p2p-peerfreedata)freigegeben werden. Diese Funktionen dürfen nur für Strukturen aufgerufen werden, die direkt von einer Peer Infrastruktur Funktion zurückgegeben werden. Wenn Sie keine andere freedata-Funktion zum Freigeben von verknüpften Zeigern verwenden, können Sie z. b. keine freedata-Funktion für die Zeiger in einer [**Peer \_ Daten Satz**](/windows/desktop/api/P2P/ns-p2p-peer_record) Struktur aufzurufen.

## <a name="example-of-freeing-data"></a>Beispiel für das Freigeben von Daten

Der folgende Code Ausschnitt zeigt, wie Sie die einem Diagramm zugeordneten Eigenschaften abrufen und dann die zurückgegebenen Daten freigeben.


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



 

 



