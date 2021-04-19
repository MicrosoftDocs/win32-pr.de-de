---
description: Eine Matrix zum Transformieren von Objekt Raum in Raum.
ms.assetid: ''
title: ObjectToWorld4x3
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObjectToWorld4x3
api_type:
- NA
ms.openlocfilehash: 613b4c403f235819845114e7019e07051a25ec80
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342986"
---
# <a name="objecttoworld4x3"></a><span data-ttu-id="cc16f-103">ObjectToWorld4x3</span><span class="sxs-lookup"><span data-stu-id="cc16f-103">ObjectToWorld4x3</span></span>

<span data-ttu-id="cc16f-104">Eine Matrix zum Transformieren von Objekt Raum in Raum.</span><span class="sxs-lookup"><span data-stu-id="cc16f-104">A matrix for transforming from object-space to world-space.</span></span> <span data-ttu-id="cc16f-105">Objekt-Space bezieht sich auf den Raum der aktuellen Beschleunigungs Struktur der untersten Ebene.</span><span class="sxs-lookup"><span data-stu-id="cc16f-105">Object-space refers to the space of the current bottom-level acceleration structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc16f-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="cc16f-106">Syntax</span></span>

```
void ObjectToWorld4x3();

```




## <a name="remarks"></a><span data-ttu-id="cc16f-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cc16f-107">Remarks</span></span>

<span data-ttu-id="cc16f-108">Die Matrix ist eine Umsetzung der **ObjectToWorld3x4** -Matrix.</span><span class="sxs-lookup"><span data-stu-id="cc16f-108">The matrix is a transposition of **ObjectToWorld3x4** matrix.</span></span>

<span data-ttu-id="cc16f-109">Diese Funktion kann von den folgenden Raytracing-shadertypen aufgerufen werden:</span><span class="sxs-lookup"><span data-stu-id="cc16f-109">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="cc16f-110">**Any Hit-Shader**</span><span class="sxs-lookup"><span data-stu-id="cc16f-110">**Any Hit Shader**</span></span>](any-hit-shader.md)
* [<span data-ttu-id="cc16f-111">**Closest Hit-Shader**</span><span class="sxs-lookup"><span data-stu-id="cc16f-111">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="cc16f-112">**Intersection-Shader**</span><span class="sxs-lookup"><span data-stu-id="cc16f-112">**Intersection Shader**</span></span>](intersection-shader.md)





## <a name="see-also"></a><span data-ttu-id="cc16f-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cc16f-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc16f-114">Direct3D 12-Raytracing, HLSL-Referenz</span><span class="sxs-lookup"><span data-stu-id="cc16f-114">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




