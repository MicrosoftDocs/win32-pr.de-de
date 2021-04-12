---
description: Direct3D 10 Set-Funktionen enthalten keinen Verweis auf ein Gerät-untergeordnetes Objekt.
ms.assetid: 4f4e1af8-5830-4b2d-ba2e-dc2ec4e74a19
title: Verweis Zählung (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6482918601f163bdea92291eb3927899ca797d29
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523227"
---
# <a name="reference-counting-direct3d-10"></a>Verweis Zählung (Direct3D 10)

Direct3D 10 Set-Funktionen enthalten keinen Verweis auf ein Gerät-untergeordnetes Objekt. Dies bedeutet, dass jede Anwendung einen Verweis auf ein Gerät untergeordnetes Objekt enthalten muss, solange das Objekt an die Pipeline gebunden werden muss. Wenn der Verweis Zähler eines Objekts auf 0 (null) fällt, wird das Objekt an die Pipeline gebunden und zerstört. Diese Art der Verweis Speicherung wird auch als schwache Verweis Aufbewahrung bezeichnet, da jeder Pipeline Bindungs Speicherort einen schwachen Verweis auf die Schnittstelle/das Objekt enthält, das an ihn gebunden ist.

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





|                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterschiede zwischen Direct3D 9 und Direct3D 10:<br/> In Direct3D 9 enthalten Set-Funktionen einen Verweis auf die Geräte Objekte. in Direct3D 10 enthalten Set-Funktionen keinen Verweis auf die untergeordneten Geräte Objekte.<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[API-Features (Direct3D 10)](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 




