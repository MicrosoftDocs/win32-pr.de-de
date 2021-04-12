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
# <a name="reference-counting-direct3d-10"></a><span data-ttu-id="466f2-103">Verweis Zählung (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="466f2-103">Reference Counting (Direct3D 10)</span></span>

<span data-ttu-id="466f2-104">Direct3D 10 Set-Funktionen enthalten keinen Verweis auf ein Gerät-untergeordnetes Objekt.</span><span class="sxs-lookup"><span data-stu-id="466f2-104">Direct3D 10 set functions do not hold a reference to a device-child object.</span></span> <span data-ttu-id="466f2-105">Dies bedeutet, dass jede Anwendung einen Verweis auf ein Gerät untergeordnetes Objekt enthalten muss, solange das Objekt an die Pipeline gebunden werden muss.</span><span class="sxs-lookup"><span data-stu-id="466f2-105">This means that each application must hold a reference to a device-child object for as long as the object needs to be bound to the pipeline.</span></span> <span data-ttu-id="466f2-106">Wenn der Verweis Zähler eines Objekts auf 0 (null) fällt, wird das Objekt an die Pipeline gebunden und zerstört.</span><span class="sxs-lookup"><span data-stu-id="466f2-106">When the reference count of an object drops to zero, the object will be unbound from the pipeline and destroyed.</span></span> <span data-ttu-id="466f2-107">Diese Art der Verweis Speicherung wird auch als schwache Verweis Aufbewahrung bezeichnet, da jeder Pipeline Bindungs Speicherort einen schwachen Verweis auf die Schnittstelle/das Objekt enthält, das an ihn gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="466f2-107">This style of reference holding is also known as weak-reference holding because each pipeline binding location holds a weak reference to the interface/object that is bound to it.</span></span>

<span data-ttu-id="466f2-108">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="466f2-108">For example:</span></span>


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
| <span data-ttu-id="466f2-109">Unterschiede zwischen Direct3D 9 und Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="466f2-109">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="466f2-110">In Direct3D 9 enthalten Set-Funktionen einen Verweis auf die Geräte Objekte. in Direct3D 10 enthalten Set-Funktionen keinen Verweis auf die untergeordneten Geräte Objekte.</span><span class="sxs-lookup"><span data-stu-id="466f2-110">In Direct3D 9, set functions hold a reference to the device objects; in Direct3D 10 set functions do not hold a reference to the device-child objects.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="466f2-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="466f2-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="466f2-112">API-Features (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="466f2-112">API Features (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 




