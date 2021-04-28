---
description: 'ObjectToWorld3x4: Eine Matrix zum Transformieren vom Objektbereich in den Weltraum.'
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
ms.openlocfilehash: 947676c25bd5cac50749c737afd7e4ff75426c0a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107738"
---
# <a name="objecttoworld3x4"></a><span data-ttu-id="9cd8e-103">ObjectToWorld3x4</span><span class="sxs-lookup"><span data-stu-id="9cd8e-103">ObjectToWorld3x4</span></span>

<span data-ttu-id="9cd8e-104">Eine Matrix zum Transformieren vom Objektraum in den Weltraum.</span><span class="sxs-lookup"><span data-stu-id="9cd8e-104">A matrix for transforming from object-space to world-space.</span></span> <span data-ttu-id="9cd8e-105">Objektbereich bezieht sich auf den Raum der aktuellen Beschleunigungsstruktur der unteren Ebene.</span><span class="sxs-lookup"><span data-stu-id="9cd8e-105">Object-space refers to the space of the current bottom-level acceleration structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="9cd8e-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="9cd8e-106">Syntax</span></span>

```
void ObjectToWorld3x4();

```




## <a name="remarks"></a><span data-ttu-id="9cd8e-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9cd8e-107">Remarks</span></span>

<span data-ttu-id="9cd8e-108">Die Matrix ist eine Verwechsung der **ObjectToWorld4x3-Matrix.**</span><span class="sxs-lookup"><span data-stu-id="9cd8e-108">The matrix is a transposition of **ObjectToWorld4x3** matrix.</span></span>

<span data-ttu-id="9cd8e-109">Diese Funktion kann von den folgenden Raytracing-Shadertypen aufgerufen werden:</span><span class="sxs-lookup"><span data-stu-id="9cd8e-109">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="9cd8e-110">**Any Hit-Shader**</span><span class="sxs-lookup"><span data-stu-id="9cd8e-110">**Any Hit Shader**</span></span>](any-hit-shader.md)
* [<span data-ttu-id="9cd8e-111">**Closest Hit-Shader**</span><span class="sxs-lookup"><span data-stu-id="9cd8e-111">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="9cd8e-112">**Intersection-Shader**</span><span class="sxs-lookup"><span data-stu-id="9cd8e-112">**Intersection Shader**</span></span>](intersection-shader.md)





## <a name="see-also"></a><span data-ttu-id="9cd8e-113">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9cd8e-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cd8e-114">Direct3D 12-Raytracing, HLSL-Referenz</span><span class="sxs-lookup"><span data-stu-id="9cd8e-114">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




