---
description: 'WorldToObject4x3: Eine Matrix für die Transformation vom Weltraum in den Objektraum.'
ms.assetid: ''
title: WorldToObject4x3
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WorldToObject4x3
api_type:
- NA
ms.openlocfilehash: 334a79352345fb35fbbafe68248a221bdaab9f6d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105247"
---
# <a name="worldtoobject4x3"></a><span data-ttu-id="cf784-103">WorldToObject4x3</span><span class="sxs-lookup"><span data-stu-id="cf784-103">WorldToObject4x3</span></span>

<span data-ttu-id="cf784-104">Eine Matrix zum Transformieren vom Weltraum in den Objektraum.</span><span class="sxs-lookup"><span data-stu-id="cf784-104">A matrix for transforming from world-space to object-space.</span></span> <span data-ttu-id="cf784-105">Objektbereich bezieht sich auf den Raum der aktuellen Beschleunigungsstruktur der unteren Ebene.</span><span class="sxs-lookup"><span data-stu-id="cf784-105">Object-space refers to the space of the current bottom-level acceleration structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf784-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="cf784-106">Syntax</span></span>

```
void WorldToObject4x3();

```




## <a name="remarks"></a><span data-ttu-id="cf784-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cf784-107">Remarks</span></span>

<span data-ttu-id="cf784-108">Die Matrix ist eine Füge der **WorldToObject3x4-Matrix.**</span><span class="sxs-lookup"><span data-stu-id="cf784-108">The matrix is a transposition of **WorldToObject3x4** matrix.</span></span>

<span data-ttu-id="cf784-109">Diese Funktion kann von den folgenden Raytracing-Shadertypen aufgerufen werden:</span><span class="sxs-lookup"><span data-stu-id="cf784-109">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="cf784-110">**Any Hit-Shader**</span><span class="sxs-lookup"><span data-stu-id="cf784-110">**Any Hit Shader**</span></span>](any-hit-shader.md)
* [<span data-ttu-id="cf784-111">**Closest Hit-Shader**</span><span class="sxs-lookup"><span data-stu-id="cf784-111">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="cf784-112">**Intersection-Shader**</span><span class="sxs-lookup"><span data-stu-id="cf784-112">**Intersection Shader**</span></span>](intersection-shader.md)





## <a name="see-also"></a><span data-ttu-id="cf784-113">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="cf784-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf784-114">Direct3D 12-Raytracing, HLSL-Referenz</span><span class="sxs-lookup"><span data-stu-id="cf784-114">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




