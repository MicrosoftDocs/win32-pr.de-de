---
description: Alle Zeiger, die die Peerinfrastrukturfunktionen zurückgeben, müssen mithilfe von PeerGraphFreeData oder PeerFreeData freigegeben werden.
ms.assetid: c7669404-2550-4f0d-908e-540d9a34008f
title: Freigeben von Peerdaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9492fec9a22da8252188a75d6d4cee73d2055d29f47e25fc7d55a26cc7909c70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117794577"
---
# <a name="freeing-peer-data"></a>Freigeben von Peerdaten

Alle Zeiger, die die Peerinfrastrukturfunktionen zurückgeben, müssen mithilfe von [**PeerGraphFreeData**](/windows/desktop/api/P2P/nf-p2p-peergraphfreedata) oder [**PeerFreeData**](/windows/desktop/api/P2P/nf-p2p-peerfreedata)freigegeben werden. Diese Funktionen dürfen nur für Strukturen aufgerufen werden, die direkt von einer Peerinfrastrukturfunktion zurückgegeben werden. Rufen Sie keine andere FreeData-Funktion auf, um geschachtelte Zeiger freizu geben. Rufen Sie beispielsweise keine FreeData-Funktion für die Zeiger in einer [**PEER \_ RECORD-Struktur**](/windows/desktop/api/P2P/ns-p2p-peer_record) auf.

## <a name="example-of-freeing-data"></a>Beispiel für das Freigeben von Daten

Der folgende Codeausschnitt zeigt, wie Sie die einem Diagramm zugeordneten Eigenschaften abrufen und dann die zurückgegebenen Daten freigeben.


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



 

 



