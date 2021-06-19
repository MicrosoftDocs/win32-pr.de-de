---
title: Direct3D 12-Raytracing, HLSL-Shader
description: Hier finden Sie Links zu Artikeln, die HLSL-Shader (High-Level Shader Language) beschreiben, die die Direct3D 12-Raytracingpipeline unterstützen.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ca19081b1ea963851e82d18912153434c3e38d1
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112394835"
---
# <a name="direct3d-12-raytracing-hlsl-shaders"></a><span data-ttu-id="a1e64-103">Direct3D 12-Raytracing, HLSL-Shader</span><span class="sxs-lookup"><span data-stu-id="a1e64-103">Direct3D 12 Raytracing HLSL Shaders</span></span>

<span data-ttu-id="a1e64-104">Die folgenden HLSL-Shader unterstützen die Direct3D 12-Raytracingpipeline.</span><span class="sxs-lookup"><span data-stu-id="a1e64-104">The following HLSL shaders support the Direct3D 12 raytracing pipeline.</span></span> <span data-ttu-id="a1e64-105">Bei diesen Shadern handelt es sich um Funktionen, die in eine Bibliothek kompiliert werden, wobei das Zielmodell lib_6_3 und durch ein Attribut *[shader("shadertype")]* in der Shaderfunktion identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="a1e64-105">These shaders are functions compiled into a library, with target model lib_6_3, and identified by an attribute *[shader("shadertype")]* on the shader function.</span></span> <span data-ttu-id="a1e64-106">Informationen dazu, was für jeden Shadertyp zulässig ist, finden Sie unter **Systeminterne** Funktionen und **Systemwerte.**</span><span class="sxs-lookup"><span data-stu-id="a1e64-106">See **Intrinsics** and **System Values** to see what is allowed for each shader type.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="a1e64-107">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="a1e64-107">In this section</span></span>



| <span data-ttu-id="a1e64-108">Thema</span><span class="sxs-lookup"><span data-stu-id="a1e64-108">Topic</span></span>                                                                                                       | <span data-ttu-id="a1e64-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a1e64-109">Description</span></span>                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a1e64-110">**Any Hit-Shader**</span><span class="sxs-lookup"><span data-stu-id="a1e64-110">**Any Hit Shader**</span></span>](any-hit-shader.md)<br/>                              | <span data-ttu-id="a1e64-111">Ein Shader, der aufgerufen wird, wenn Strahlschnittmengen nicht deckend sind.</span><span class="sxs-lookup"><span data-stu-id="a1e64-111">A shader that is invoked when ray intersections are not opaque.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="a1e64-112">**Callable-Shader**</span><span class="sxs-lookup"><span data-stu-id="a1e64-112">**Callable Shader**</span></span>](callable-shader.md)<br/>                              | <span data-ttu-id="a1e64-113">Ein Shader, der von einem anderen Shader mit der systeminternen **CallShader-Eigenschaft** aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="a1e64-113">A shader that is invoked from another shader with the **CallShader** intrinsic.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="a1e64-114">**Closest Hit-Shader**</span><span class="sxs-lookup"><span data-stu-id="a1e64-114">**Closest Hit Shader**</span></span>](closest-hit-shader.md)<br/>                              | <span data-ttu-id="a1e64-115">Ein Shader, der aufgerufen wird, wenn er aktiviert ist und der nächste Treffer bestimmt wurde oder die Suche nach Strahlschnitten beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="a1e64-115">A shader that is invoked when it is enabled and the closest hit has been determined or ray intersection search ended.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="a1e64-116">**Intersection-Shader**</span><span class="sxs-lookup"><span data-stu-id="a1e64-116">**Intersection Shader**</span></span>](intersection-shader.md)<br/>                              | <span data-ttu-id="a1e64-117">Ein Shader, der verwendet wird, um benutzerdefinierte Schnittmengenprimitive für Lichtstrahl zu implementieren, der ein zugeordnetes umgebendes Volumen (begrenzungsfeld) überschneidet.</span><span class="sxs-lookup"><span data-stu-id="a1e64-117">A shader that is used to implement custom intersection primitives for rays intersecting an associated bounding volume (bounding box).</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="a1e64-118">**Miss-Shader**</span><span class="sxs-lookup"><span data-stu-id="a1e64-118">**Miss Shader**</span></span>](miss-shader.md)<br/>                              | <span data-ttu-id="a1e64-119">Ein Shader, der aufgerufen wird, wenn keine Strahlkreuzungen gefunden oder akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="a1e64-119">A shader that is invoked when no ray intersections are found or accepted.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="a1e64-120">**Ray Generation-Shader**</span><span class="sxs-lookup"><span data-stu-id="a1e64-120">**Ray Generation Shader**</span></span>](ray-generation-shader.md)<br/>                              | <span data-ttu-id="a1e64-121">Ein Shader, der [**TraceRay**](traceray-function.md) aufruft, um Lichtstrahl zu generieren.</span><span class="sxs-lookup"><span data-stu-id="a1e64-121">A shader that calls [**TraceRay**](traceray-function.md) to generate rays.</span></span><br/>                                                                                                                                                                                                                                              |

## <a name="related-topics"></a><span data-ttu-id="a1e64-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a1e64-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1e64-123">Kernreferenz</span><span class="sxs-lookup"><span data-stu-id="a1e64-123">Core Reference</span></span>](direct3d-12-core-reference.md)
</dt> <dt>

[<span data-ttu-id="a1e64-124">Referenz für Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="a1e64-124">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
</dt> </dl>

 

 





