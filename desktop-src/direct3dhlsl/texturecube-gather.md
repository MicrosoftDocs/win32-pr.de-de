---
title: 'Texturecube:: texturecube Gather-Methoden'
description: 'Gibt die vier texelwerte zurück, die in einem bilinearen Filter Vorgang verwendet werden. | Texturecube:: texturecube Gather-Methoden'
ms.assetid: 4891A62A-9D54-4F7E-92C2-9CDDF1453671
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
ms.openlocfilehash: ce58acc01ef87e6d53d829a5c84e7c9c0ff6afb9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981449"
---
# <a name="texturecubegather-methods"></a><span data-ttu-id="523bc-105">Texturecube:: Gather-Methoden</span><span class="sxs-lookup"><span data-stu-id="523bc-105">TextureCube::Gather methods</span></span>

<span data-ttu-id="523bc-106">Gibt die vier texelwerte zurück, die in einem bilinearen Filter Vorgang verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="523bc-106">Returns the four texel values that would be used in a bi-linear filtering operation.</span></span>

<span data-ttu-id="523bc-107">Weitere Informationen zum Beschreiben der zugrunde liegenden dxbc-Anweisung finden Sie in der Dokumentation zu [gather4](./gather4--sm5---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="523bc-107">See the documentation on [gather4](./gather4--sm5---asm-.md) for more information describing the underlying DXBC instruction.</span></span>

### <a name="overload-list"></a><span data-ttu-id="523bc-108">Überladeliste</span><span class="sxs-lookup"><span data-stu-id="523bc-108">Overload list</span></span>



| <span data-ttu-id="523bc-109">Methode</span><span class="sxs-lookup"><span data-stu-id="523bc-109">Method</span></span>                                                     | <span data-ttu-id="523bc-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="523bc-110">Description</span></span>                                                                                                              |
|:-----------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="523bc-111">**Erfassen (S, float)**</span><span class="sxs-lookup"><span data-stu-id="523bc-111">**Gather(S,float)**</span></span>](dx-graphics-hlsl-to-gather.md)      | <span data-ttu-id="523bc-112">Führt eine Stichprobe einer Textur aus und gibt die vier Stichproben (nur rote Komponente) zurück, die für die bilineare interpolung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="523bc-112">Samples a texture and returns the four samples (red component only) that are used for bilinear interpolation.</span></span><br/> |
| [<span data-ttu-id="523bc-113">**Gather (S, float, uint)**</span><span class="sxs-lookup"><span data-stu-id="523bc-113">**Gather(S,float,uint)**</span></span>](tcube-gather-s-float-uint-.md) | <span data-ttu-id="523bc-114">Prüft eine Textur und gibt alle vier Komponenten zusammen mit dem Status des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="523bc-114">Samples a texture and returns all four components along with status about the operation.</span></span><br/>                      |



## <a name="see-also"></a><span data-ttu-id="523bc-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="523bc-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="523bc-116">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="523bc-116">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

