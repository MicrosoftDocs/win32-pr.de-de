---
title: Raytracing HLSL-Strukturen (Direct3D 12)
description: Die folgenden HLSL-Strukturen unterstützen die Direct3D 12-Raytracing-Pipeline.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c48ad6bac76e200587ec76d42dfa9c86b23cd23
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/23/2019
ms.locfileid: "106342326"
---
# <a name="raytracing-hlsl-structures-direct3d-12"></a><span data-ttu-id="9b1b3-103">Raytracing HLSL-Strukturen (Direct3D 12)</span><span class="sxs-lookup"><span data-stu-id="9b1b3-103">Raytracing HLSL structures (Direct3D 12)</span></span>

<span data-ttu-id="9b1b3-104">Die folgenden HLSL-Strukturen unterstützen die Direct3D 12-Raytracing-Pipeline.</span><span class="sxs-lookup"><span data-stu-id="9b1b3-104">The following HLSL structures support the Direct3D 12 raytracing pipeline.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9b1b3-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="9b1b3-105">In this section</span></span>



| <span data-ttu-id="9b1b3-106">Thema</span><span class="sxs-lookup"><span data-stu-id="9b1b3-106">Topic</span></span>                                                                                                       | <span data-ttu-id="9b1b3-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9b1b3-107">Description</span></span>                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9b1b3-108">**Struktur von Aufrufparametern**</span><span class="sxs-lookup"><span data-stu-id="9b1b3-108">**Call Parameter Structure**</span></span>](call-parameter-structure.md)<br/>                              | <span data-ttu-id="9b1b3-109">Eine benutzerdefinierte Struktur, die als ein INOUT-Argument für einen callshader-Aufruf bereitgestellt wird, und als INOUT-Parameter für den Aufruf baren Shader.</span><span class="sxs-lookup"><span data-stu-id="9b1b3-109">A user-defined structure provided as an inout argument to a CallShader call, and as an inout parameter for the callable shader.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="9b1b3-110">**Struktur von Schnittmengenattributen**</span><span class="sxs-lookup"><span data-stu-id="9b1b3-110">**Intersection Attributes Structure**</span></span>](intersection-attributes.md)<br/>                              | <span data-ttu-id="9b1b3-111">Eine benutzerdefinierte Struktur, die als ein INOUT-Argument in einem [**traceray**](traceray-function.md) -Befehl bereitgestellt wird, und als INOUT-Parameter in den shadertypen, die möglicherweise auf die Ray-Nutzlast zugreifen.</span><span class="sxs-lookup"><span data-stu-id="9b1b3-111">A user-defined structure that is provided as an inout argument in a [**TraceRay**](traceray-function.md) call, and as an inout parameter in the shader types that may access the ray payload.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="9b1b3-112">**Struktur von Ray-Nutzlast**</span><span class="sxs-lookup"><span data-stu-id="9b1b3-112">**Ray Payload Structure**</span></span>](ray-payload.md)<br/>                              | <span data-ttu-id="9b1b3-113">Eine benutzerdefinierte Struktur, die als ein INOUT-Argument in einem [**traceray**](traceray-function.md) -Befehl bereitgestellt wird, und als INOUT-Parameter in den shadertypen, die möglicherweise auf die Ray-Nutzlast zugreifen.</span><span class="sxs-lookup"><span data-stu-id="9b1b3-113">A user-defined structure that is provided as an inout argument in a [**TraceRay**](traceray-function.md) call, and as an inout parameter in the shader types that may access the ray payload.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="9b1b3-114">**RayDesc-Struktur**</span><span class="sxs-lookup"><span data-stu-id="9b1b3-114">**RayDesc Structure**</span></span>](raydesc.md)<br/>                              | <span data-ttu-id="9b1b3-115">Flags, die an die [**traceray**](traceray-function.md) -Funktion übergeben werden, um Transparenz, Vererbung und frühe Ausgabeverhalten zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="9b1b3-115">Flags passed to the [**TraceRay**](traceray-function.md) function to override transparency, culling, and early-out behavior.</span></span><br/>                                                                                                                                                                                                                                              |





 

## <a name="related-topics"></a><span data-ttu-id="9b1b3-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9b1b3-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b1b3-117">Kern Referenz</span><span class="sxs-lookup"><span data-stu-id="9b1b3-117">Core Reference</span></span>](direct3d-12-core-reference.md)
</dt> <dt>

[<span data-ttu-id="9b1b3-118">Referenz für Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="9b1b3-118">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
</dt> </dl>

 

 





