---
description: Die Richtung des Objekt Raums für das aktuelle Ray.
ms.assetid: ''
title: Objectraydirection
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObjectRayDirection
api_type:
- NA
ms.openlocfilehash: 1cc291a33f91bf7fc0565596bdd075a86e193246
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346017"
---
# <a name="objectraydirection"></a><span data-ttu-id="cf85b-103">Objectraydirection</span><span class="sxs-lookup"><span data-stu-id="cf85b-103">ObjectRayDirection</span></span>

<span data-ttu-id="cf85b-104">Die Richtung des Objekt Raums für das aktuelle Ray.</span><span class="sxs-lookup"><span data-stu-id="cf85b-104">The object-space direction for the current ray.</span></span> <span data-ttu-id="cf85b-105">Objekt-Space bezieht sich auf den Raum der aktuellen Beschleunigungs Struktur der untersten Ebene.</span><span class="sxs-lookup"><span data-stu-id="cf85b-105">Object-space refers to the space of the current bottom-level acceleration structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf85b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="cf85b-106">Syntax</span></span>

```
float3 ObjectRayDirection();

```



## <a name="remarks"></a><span data-ttu-id="cf85b-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cf85b-107">Remarks</span></span>

<span data-ttu-id="cf85b-108">Diese Funktion kann von den folgenden Raytracing-shadertypen aufgerufen werden:</span><span class="sxs-lookup"><span data-stu-id="cf85b-108">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="cf85b-109">**Any Hit-Shader**</span><span class="sxs-lookup"><span data-stu-id="cf85b-109">**Any Hit Shader**</span></span>](any-hit-shader.md)
* [<span data-ttu-id="cf85b-110">**Closest Hit-Shader**</span><span class="sxs-lookup"><span data-stu-id="cf85b-110">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="cf85b-111">**Intersection-Shader**</span><span class="sxs-lookup"><span data-stu-id="cf85b-111">**Intersection Shader**</span></span>](intersection-shader.md)





## <a name="see-also"></a><span data-ttu-id="cf85b-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cf85b-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf85b-113">Direct3D 12-Raytracing, HLSL-Referenz</span><span class="sxs-lookup"><span data-stu-id="cf85b-113">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




