---
description: Direct3D 10-Set-Funktionen besitzen keinen Verweis auf ein vom Gerät untergeordnetes Objekt.
ms.assetid: 4f4e1af8-5830-4b2d-ba2e-dc2ec4e74a19
title: Verweiszählung (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b3587466aa3ecaea5f3a77332c77654b0725bb1
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335454"
---
# <a name="reference-counting-direct3d-10"></a>Verweiszählung (Direct3D 10)

Direct3D 10-Set-Funktionen besitzen keinen Verweis auf ein vom Gerät untergeordnetes Objekt. Dies bedeutet, dass jede Anwendung einen Verweis auf ein vom Gerät untergeordnetes Objekt so lange speichern muss, wie das Objekt an die Pipeline gebunden werden muss. Wenn die Verweisanzahl eines Objekts auf 0 (null) fällt, wird das Objekt von der Pipeline entfernt und zerstört. Diese Art der Referenzspeicherung wird auch als Schwache-Verweis-Holding bezeichnet, da jede Pipelinebindungsposition einen schwachen Verweis auf die Schnittstelle bzw. das Objekt enthält, die bzw. das an sie gebunden ist.

Beispiel:


```
pDevice->CreateRasterizerState( ..., &pRasterizerState );
pDevice->RSSetState( pRasterizerState );
 
pDevice->RSGetState( &pCurRasterizerState );
// pCurRasterizerState will be equal to pRasterizerState.
pCurRasterizerState->Release();
 
pRasterizerState->Release();
// Following the final release, the object is unbound.
pDevice->RSGetState( &pCurRasterizerState );
// pCurRasterizerState will be equal to NULL.
```





Unterschiede zwischen Direct3D 9 und Direct3D 10:

- In Direct3D 9 enthalten set-Funktionen einen Verweis auf die Geräteobjekte. In Direct3D 10 enthalten Set-Funktionen keinen Verweis auf die untergeordneten Geräteobjekte.



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[API-Features (Direct3D 10)](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 




