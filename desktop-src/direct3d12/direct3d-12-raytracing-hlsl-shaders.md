---
title: Direct3D 12-Raytracing, HLSL-Shader
description: Die folgenden HLSL-Shader unterstützen die Direct3D 12-Raytracing-Pipeline.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe1dd545532208095781f6fbca25480a6dbfd31e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106340554"
---
# <a name="direct3d-12-raytracing-hlsl-shaders"></a><span data-ttu-id="94f47-103">Direct3D 12-Raytracing, HLSL-Shader</span><span class="sxs-lookup"><span data-stu-id="94f47-103">Direct3D 12 Raytracing HLSL Shaders</span></span>

<span data-ttu-id="94f47-104">Die folgenden HLSL-Shader unterstützen die Direct3D 12-Raytracing-Pipeline.</span><span class="sxs-lookup"><span data-stu-id="94f47-104">The following HLSL shaders support the Direct3D 12 raytracing pipeline.</span></span> <span data-ttu-id="94f47-105">Diese Shader sind Funktionen, die in eine Bibliothek kompiliert werden, mit Zielmodell lib_6_3 und durch ein Attribut *[Shader ("shadertype")] in der shaderfunktion* identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="94f47-105">These shaders are functions compiled into a library, with target model lib_6_3, and identified by an attribute *[shader("shadertype")]* on the shader function.</span></span> <span data-ttu-id="94f47-106">Siehe System interne Funktionen und **System Werte** , um **zu sehen,** was für die einzelnen shadertypen zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="94f47-106">See **Intrinsics** and **System Values** to see what is allowed for each shader type.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="94f47-107">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="94f47-107">In this section</span></span>



| <span data-ttu-id="94f47-108">Thema</span><span class="sxs-lookup"><span data-stu-id="94f47-108">Topic</span></span>                                                                                                       | <span data-ttu-id="94f47-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="94f47-109">Description</span></span>                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="94f47-110">**Any Hit-Shader**</span><span class="sxs-lookup"><span data-stu-id="94f47-110">**Any Hit Shader**</span></span>](any-hit-shader.md)<br/>                              | <span data-ttu-id="94f47-111">Ein Shader, der aufgerufen wird, wenn Ray-Schnittmengen nicht deckend sind.</span><span class="sxs-lookup"><span data-stu-id="94f47-111">A shader that is invoked when ray intersections are not opaque.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="94f47-112">**Callable-Shader**</span><span class="sxs-lookup"><span data-stu-id="94f47-112">**Callable Shader**</span></span>](callable-shader.md)<br/>                              | <span data-ttu-id="94f47-113">Ein Shader, der von einem anderen Shader mit der systeminternen Funktion **callshader** aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="94f47-113">A shader that is invoked from another shader with the **CallShader** intrinsic.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="94f47-114">**Closest Hit-Shader**</span><span class="sxs-lookup"><span data-stu-id="94f47-114">**Closest Hit Shader**</span></span>](closest-hit-shader.md)<br/>                              | <span data-ttu-id="94f47-115">Ein Shader, der aufgerufen wird, wenn er aktiviert ist, und der nächstgelegene Treffer wurde ermittelt oder die Überprüfung der Ray-Schnittmenge wurde beendet.</span><span class="sxs-lookup"><span data-stu-id="94f47-115">A shader that is invoked when it is enabled and the closest hit has been determined or ray intersection search ended.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="94f47-116">**Intersection-Shader**</span><span class="sxs-lookup"><span data-stu-id="94f47-116">**Intersection Shader**</span></span>](intersection-shader.md)<br/>                              | <span data-ttu-id="94f47-117">Ein Shader, der verwendet wird, um benutzerdefinierte Schnittmengen primitive für Strahlen zu implementieren, die ein zugeordnetes Begrenzungs Volume (Begrenzungsfeld) überschneiden.</span><span class="sxs-lookup"><span data-stu-id="94f47-117">A shader that is used to implement custom intersection primitives for rays intersecting an associated bounding volume (bounding box).</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="94f47-118">**Miss-Shader**</span><span class="sxs-lookup"><span data-stu-id="94f47-118">**Miss Shader**</span></span>](miss-shader.md)<br/>                              | <span data-ttu-id="94f47-119">Ein Shader, der aufgerufen wird, wenn keine Ray-Schnittmengen gefunden oder akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="94f47-119">A shader that is invoked when no ray intersections are found or accepted.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="94f47-120">**Ray Generation-Shader**</span><span class="sxs-lookup"><span data-stu-id="94f47-120">**Ray Generation Shader**</span></span>](ray-generation-shader.md)<br/>                              | <span data-ttu-id="94f47-121">Ein Shader, der [**traceray**](traceray-function.md) aufruft, um Strahlen zu generieren.</span><span class="sxs-lookup"><span data-stu-id="94f47-121">A shader that calls [**TraceRay**](traceray-function.md) to generate rays.</span></span><br/>                                                                                                                                                                                                                                              |

## <a name="related-topics"></a><span data-ttu-id="94f47-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="94f47-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94f47-123">Kern Referenz</span><span class="sxs-lookup"><span data-stu-id="94f47-123">Core Reference</span></span>](direct3d-12-core-reference.md)
</dt> <dt>

[<span data-ttu-id="94f47-124">Referenz für Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="94f47-124">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
</dt> </dl>

 

 





