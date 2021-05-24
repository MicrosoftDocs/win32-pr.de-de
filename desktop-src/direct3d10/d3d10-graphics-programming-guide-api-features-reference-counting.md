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
# <a name="reference-counting-direct3d-10"></a><span data-ttu-id="e6920-103">Verweiszählung (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="e6920-103">Reference Counting (Direct3D 10)</span></span>

<span data-ttu-id="e6920-104">Direct3D 10-Set-Funktionen besitzen keinen Verweis auf ein vom Gerät untergeordnetes Objekt.</span><span class="sxs-lookup"><span data-stu-id="e6920-104">Direct3D 10 set functions do not hold a reference to a device-child object.</span></span> <span data-ttu-id="e6920-105">Dies bedeutet, dass jede Anwendung einen Verweis auf ein vom Gerät untergeordnetes Objekt so lange speichern muss, wie das Objekt an die Pipeline gebunden werden muss.</span><span class="sxs-lookup"><span data-stu-id="e6920-105">This means that each application must hold a reference to a device-child object for as long as the object needs to be bound to the pipeline.</span></span> <span data-ttu-id="e6920-106">Wenn die Verweisanzahl eines Objekts auf 0 (null) fällt, wird das Objekt von der Pipeline entfernt und zerstört.</span><span class="sxs-lookup"><span data-stu-id="e6920-106">When the reference count of an object drops to zero, the object will be unbound from the pipeline and destroyed.</span></span> <span data-ttu-id="e6920-107">Diese Art der Referenzspeicherung wird auch als Schwache-Verweis-Holding bezeichnet, da jede Pipelinebindungsposition einen schwachen Verweis auf die Schnittstelle bzw. das Objekt enthält, die bzw. das an sie gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="e6920-107">This style of reference holding is also known as weak-reference holding because each pipeline binding location holds a weak reference to the interface/object that is bound to it.</span></span>

<span data-ttu-id="e6920-108">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="e6920-108">For example:</span></span>


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





<span data-ttu-id="e6920-109">Unterschiede zwischen Direct3D 9 und Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="e6920-109">Differences between Direct3D 9 and Direct3D 10:</span></span>

- <span data-ttu-id="e6920-110">In Direct3D 9 enthalten set-Funktionen einen Verweis auf die Geräteobjekte. In Direct3D 10 enthalten Set-Funktionen keinen Verweis auf die untergeordneten Geräteobjekte.</span><span class="sxs-lookup"><span data-stu-id="e6920-110">In Direct3D 9, set functions hold a reference to the device objects; in Direct3D 10 set functions do not hold a reference to the device-child objects.</span></span>



 

## <a name="related-topics"></a><span data-ttu-id="e6920-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e6920-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6920-112">API-Features (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="e6920-112">API Features (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 




