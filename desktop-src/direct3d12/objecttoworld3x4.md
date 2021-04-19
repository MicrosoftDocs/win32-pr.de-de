---
description: Eine Matrix zum Transformieren von Objekt Raum in Raum.
ms.assetid: ''
title: ObjectToWorld3x4
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObjectToWorld3x4
api_type:
- NA
ms.openlocfilehash: 04f80dde64984010c6e015f6e885565396d3b9c9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344821"
---
# <a name="objecttoworld3x4"></a><span data-ttu-id="da0c6-103">ObjectToWorld3x4</span><span class="sxs-lookup"><span data-stu-id="da0c6-103">ObjectToWorld3x4</span></span>

<span data-ttu-id="da0c6-104">Eine Matrix zum Transformieren von Objekt Raum in Raum.</span><span class="sxs-lookup"><span data-stu-id="da0c6-104">A matrix for transforming from object-space to world-space.</span></span> <span data-ttu-id="da0c6-105">Objekt-Space bezieht sich auf den Raum der aktuellen Beschleunigungs Struktur der untersten Ebene.</span><span class="sxs-lookup"><span data-stu-id="da0c6-105">Object-space refers to the space of the current bottom-level acceleration structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="da0c6-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="da0c6-106">Syntax</span></span>

```
void ObjectToWorld3x4();

```




## <a name="remarks"></a><span data-ttu-id="da0c6-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="da0c6-107">Remarks</span></span>

<span data-ttu-id="da0c6-108">Die Matrix ist eine Umsetzung der **ObjectToWorld4x3** -Matrix.</span><span class="sxs-lookup"><span data-stu-id="da0c6-108">The matrix is a transposition of **ObjectToWorld4x3** matrix.</span></span>

<span data-ttu-id="da0c6-109">Diese Funktion kann von den folgenden Raytracing-shadertypen aufgerufen werden:</span><span class="sxs-lookup"><span data-stu-id="da0c6-109">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="da0c6-110">**Any Hit-Shader**</span><span class="sxs-lookup"><span data-stu-id="da0c6-110">**Any Hit Shader**</span></span>](any-hit-shader.md)
* [<span data-ttu-id="da0c6-111">**Closest Hit-Shader**</span><span class="sxs-lookup"><span data-stu-id="da0c6-111">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="da0c6-112">**Intersection-Shader**</span><span class="sxs-lookup"><span data-stu-id="da0c6-112">**Intersection Shader**</span></span>](intersection-shader.md)





## <a name="see-also"></a><span data-ttu-id="da0c6-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="da0c6-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da0c6-114">Direct3D 12-Raytracing, HLSL-Referenz</span><span class="sxs-lookup"><span data-stu-id="da0c6-114">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




