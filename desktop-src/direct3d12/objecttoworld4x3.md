---
description: 'ObjectToWorld4x3: Eine Matrix für die Transformation vom Objektraum in den Weltraum.'
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
ms.openlocfilehash: bc91c6e98aceb13af3f589f873a4b96c2b1843c4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098298"
---
# <a name="objecttoworld4x3"></a><span data-ttu-id="64e91-103">ObjectToWorld4x3</span><span class="sxs-lookup"><span data-stu-id="64e91-103">ObjectToWorld4x3</span></span>

<span data-ttu-id="64e91-104">Eine Matrix für die Transformation von Objektraum in Raum.</span><span class="sxs-lookup"><span data-stu-id="64e91-104">A matrix for transforming from object-space to world-space.</span></span> <span data-ttu-id="64e91-105">Objektraum bezieht sich auf den Raum der aktuellen Beschleunigungsstruktur auf unterer Ebene.</span><span class="sxs-lookup"><span data-stu-id="64e91-105">Object-space refers to the space of the current bottom-level acceleration structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="64e91-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="64e91-106">Syntax</span></span>

```
void ObjectToWorld4x3();

```




## <a name="remarks"></a><span data-ttu-id="64e91-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="64e91-107">Remarks</span></span>

<span data-ttu-id="64e91-108">Die Matrix ist ein Teil der **ObjectToWorld3x4-Matrix.**</span><span class="sxs-lookup"><span data-stu-id="64e91-108">The matrix is a transposition of **ObjectToWorld3x4** matrix.</span></span>

<span data-ttu-id="64e91-109">Diese Funktion kann von den folgenden Raytracing-Shadertypen aufgerufen werden:</span><span class="sxs-lookup"><span data-stu-id="64e91-109">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="64e91-110">**Any Hit-Shader**</span><span class="sxs-lookup"><span data-stu-id="64e91-110">**Any Hit Shader**</span></span>](any-hit-shader.md)
* [<span data-ttu-id="64e91-111">**Closest Hit-Shader**</span><span class="sxs-lookup"><span data-stu-id="64e91-111">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="64e91-112">**Intersection-Shader**</span><span class="sxs-lookup"><span data-stu-id="64e91-112">**Intersection Shader**</span></span>](intersection-shader.md)





## <a name="see-also"></a><span data-ttu-id="64e91-113">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="64e91-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64e91-114">Direct3D 12-Raytracing, HLSL-Referenz</span><span class="sxs-lookup"><span data-stu-id="64e91-114">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




