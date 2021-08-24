---
description: Direct3D 10-Set-Funktionen enthalten keinen Verweis auf ein geräte untergeordnetes Objekt.
ms.assetid: 4f4e1af8-5830-4b2d-ba2e-dc2ec4e74a19
title: Verweiszählung (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80745c7af251294dca279a023f541b6485d2c3e01da22d2b8432e7220ac9bbd3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793260"
---
# <a name="reference-counting-direct3d-10"></a>Verweiszählung (Direct3D 10)

Direct3D 10-Set-Funktionen enthalten keinen Verweis auf ein geräte untergeordnetes Objekt. Dies bedeutet, dass jede Anwendung einen Verweis auf ein gerät-untergeordnetes Objekt enthalten muss, solange das Objekt an die Pipeline gebunden werden muss. Wenn der Verweiszähler eines Objekts auf 0 (null) fällt, wird das Objekt von der Pipeline ungebunden und zerstört. Diese Art der Verweisaufbewahrung wird auch als "weak-reference holding" bezeichnet, da jede Pipelinebindungsposition einen schwachen Verweis auf die Schnittstelle bzw. das Objekt enthält, die bzw. das an sie gebunden ist.

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

- In Direct3D 9 enthalten set-Funktionen einen Verweis auf die Geräteobjekte. In Direct3D 10 enthalten set-Funktionen keinen Verweis auf die geräte untergeordneten Objekte.



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[API-Features (Direct3D 10)](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 




