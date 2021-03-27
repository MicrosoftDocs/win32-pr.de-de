---
title: 'Texture2DArray:: Texture2DArray Gather-Methoden'
description: Führt eine Texture2DArray aus und gibt alle vier Komponenten zurück.
ms.assetid: eea1dd00-0061-4601-a218-979eb0ecd36d
keywords:
- Gather-Methoden HLSL
topic_type:
- apiref
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
api_location: ''
ms.openlocfilehash: cd10959490a85583cab01814f9cdb012859317a4
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104981024"
---
# <a name="texture2darraygather-methods"></a><span data-ttu-id="c2268-104">Texture2DArray:: Gather-Methoden</span><span class="sxs-lookup"><span data-stu-id="c2268-104">Texture2DArray::Gather methods</span></span>

<span data-ttu-id="c2268-105">Gibt die vier texelwerte eines [**Texture2DArray**](sm5-object-texture2darray.md) zurück, die in einem bilinearen Filter Vorgang verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c2268-105">Returns the four texel values of a [**Texture2DArray**](sm5-object-texture2darray.md) that would be used in a bi-linear filtering operation.</span></span>

<span data-ttu-id="c2268-106">Weitere Informationen zum Beschreiben der zugrunde liegenden dxbc-Anweisung finden Sie in der Dokumentation zu [gather4](./gather4--sm5---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="c2268-106">See the documentation on [gather4](./gather4--sm5---asm-.md) for more information describing the underlying DXBC instruction.</span></span>

### <a name="overload-list"></a><span data-ttu-id="c2268-107">Überladeliste</span><span class="sxs-lookup"><span data-stu-id="c2268-107">Overload list</span></span>



| <span data-ttu-id="c2268-108">Methode</span><span class="sxs-lookup"><span data-stu-id="c2268-108">Method</span></span>                                                                | <span data-ttu-id="c2268-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c2268-109">Description</span></span>                                                                                                               |
|:----------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c2268-110">**Gather (S, float, int)**</span><span class="sxs-lookup"><span data-stu-id="c2268-110">**Gather(S,float,int)**</span></span>](sm5-object-texture2darray-gather.md)        | <span data-ttu-id="c2268-111">Gibt die vier texelwerte zurück, die in einem bilinearen Filter Vorgang verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c2268-111">Returns the four texel values that would be used in a bi-linear filtering operation.</span></span><br/>                                 |
| [<span data-ttu-id="c2268-112">**Gather (S, float, int, uint)**</span><span class="sxs-lookup"><span data-stu-id="c2268-112">**Gather(S,float,int,uint)**</span></span>](t2darray-gather-s-float-int-uint-.md)  | <span data-ttu-id="c2268-113">Gibt die vier texelwerte zurück, die in einem bilinearen Filter Vorgang zusammen mit dem Status der Kachel Zuordnung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c2268-113">Returns the four texel values that would be used in a bi-linear filtering operation, along with tile-mapping status.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c2268-114">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c2268-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2268-115">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="c2268-115">Texture2DArray</span></span>](sm5-object-texture2darray.md)
</dt> </dl>

 

