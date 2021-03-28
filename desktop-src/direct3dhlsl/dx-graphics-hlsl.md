---
title: High-Level-Shaderprogrammiersprache (HLSL)
description: HLSL ist die C-ähnliche High-Level-Shader-Sprache, die Sie mit programmierbaren Shadern in DirectX verwenden.
ms.assetid: 09cdd8d6-0cf5-4f7e-b480-f748d2fa9ca9
ms.topic: article
ms.date: 01/11/2021
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.custom: contperf-fy21q3
ms.openlocfilehash: c0876cda302d4c6215b640c210e880795273cd6c
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104981041"
---
# <a name="high-level-shader-language-hlsl"></a><span data-ttu-id="b5fcd-103">High-Level-Shaderprogrammiersprache (HLSL)</span><span class="sxs-lookup"><span data-stu-id="b5fcd-103">High-level shader language (HLSL)</span></span>

<span data-ttu-id="b5fcd-104">HLSL ist die C-ähnliche High-Level-Shader-Sprache, die Sie mit programmierbaren Shadern in DirectX verwenden.</span><span class="sxs-lookup"><span data-stu-id="b5fcd-104">HLSL is the C-like high-level shader language that you use with programmable shaders in DirectX.</span></span>

<span data-ttu-id="b5fcd-105">Beispielsweise können Sie HLSL zum Schreiben eines [Scheitel](../direct3d11/vertex-shader-stage.md)Punkt-Shader oder eines [Pixelshaders](../direct3d11/pixel-shader-stage.md)verwenden und diese Shader in der Implementierung des Renderers in Ihrer [Direct3D](../direct3d12/directx-12-programming-guide.md) -Anwendung verwenden.</span><span class="sxs-lookup"><span data-stu-id="b5fcd-105">For example, you can use HLSL to write a [vertex shader](../direct3d11/vertex-shader-stage.md), or a [pixel shader](../direct3d11/pixel-shader-stage.md), and use those shaders in the implementation of the renderer in your [Direct3D](../direct3d12/directx-12-programming-guide.md) application.</span></span>

<span data-ttu-id="b5fcd-106">Oder Sie können HLSL zum Schreiben eines Compute-Shaders verwenden, vielleicht um eine Physik Simulation zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="b5fcd-106">Or you could use HLSL to write a compute shader, perhaps to implement a physics simulation.</span></span> <span data-ttu-id="b5fcd-107">Wenn Sie z. b. einen eigenen Konvolution-Operator (für die Bildverarbeitung) als HLSL in einem Compute-Shader schreiben möchten, erzielen Sie in diesem Szenario eine bessere Leistung, wenn Sie stattdessen [Direct Machine Learning (directml)](../direct3d12/dml.md) verwenden.</span><span class="sxs-lookup"><span data-stu-id="b5fcd-107">However, if for example you're inclined to write your own convolution operator (for image processing) as HLSL in a compute shader, then you'll get better performance in that scenario if you use [Direct Machine Learning (DirectML)](../direct3d12/dml.md) instead.</span></span>

<span data-ttu-id="b5fcd-108">HLSL wurde erstellt (beginnend mit DirectX 9), um die programmierbare 3D- [Pipeline](../direct3d11/overviews-direct3d-11-graphics-pipeline.md)einzurichten.</span><span class="sxs-lookup"><span data-stu-id="b5fcd-108">HLSL was created (starting with DirectX 9) to set up the programmable 3D [pipeline](../direct3d11/overviews-direct3d-11-graphics-pipeline.md).</span></span> <span data-ttu-id="b5fcd-109">Sie können die gesamte Pipeline mit HLSL-Anweisungen programmieren.</span><span class="sxs-lookup"><span data-stu-id="b5fcd-109">You can program the entire pipeline with HLSL instructions.</span></span>

## <a name="where-to-go-next"></a><span data-ttu-id="b5fcd-110">Nächste Schritt</span><span class="sxs-lookup"><span data-stu-id="b5fcd-110">Where to go next</span></span>

* [<span data-ttu-id="b5fcd-111">Programmier Handbuch für HLSL</span><span class="sxs-lookup"><span data-stu-id="b5fcd-111">Programming guide for HLSL</span></span>](./dx-graphics-hlsl-pguide.md)
* [<span data-ttu-id="b5fcd-112">Verweis für HLSL</span><span class="sxs-lookup"><span data-stu-id="b5fcd-112">Reference for HLSL</span></span>](./dx-graphics-hlsl-reference.md)

### <a name="programming-guide-for-hlsl"></a><span data-ttu-id="b5fcd-113">Programmier Handbuch für HLSL</span><span class="sxs-lookup"><span data-stu-id="b5fcd-113">Programming guide for HLSL</span></span>

<span data-ttu-id="b5fcd-114">Eine konzeptionelle Einführung in HLSL finden Sie im [Programmier Handbuch für HLSL](./dx-graphics-hlsl-pguide.md).</span><span class="sxs-lookup"><span data-stu-id="b5fcd-114">For a conceptual introduction to HLSL, see the [Programming guide for HLSL](./dx-graphics-hlsl-pguide.md).</span></span>

<span data-ttu-id="b5fcd-115">Im Programmier Handbuch werden die unterschiedlichen Arten von Shader-Stufen erläutert, und es wird erläutert, wie Shaders erstellt, kompiliert, optimiert, gebunden und verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="b5fcd-115">The programming guide discusses the different kinds of shader stages, and how to create, compile, optimize, bind, and link shaders.</span></span>

<span data-ttu-id="b5fcd-116">Dort finden Sie auch Übersichten und Anmerkungen zu den aufeinander folgenden Generierungen der shadermodellversion, die veröffentlicht wurden, bis hin zu HLSL-Shader-Modell 5.</span><span class="sxs-lookup"><span data-stu-id="b5fcd-116">There you'll also find overviews of, and release notes about, the successive generations of shader model version that have been released, going back as far as HLSL shader model 5.</span></span>

### <a name="reference-for-hlsl"></a><span data-ttu-id="b5fcd-117">Verweis für HLSL</span><span class="sxs-lookup"><span data-stu-id="b5fcd-117">Reference for HLSL</span></span>

<span data-ttu-id="b5fcd-118">Die HLSL-Referenz Dokumentation finden Sie in der [Referenz für HLSL](./dx-graphics-hlsl-reference.md).</span><span class="sxs-lookup"><span data-stu-id="b5fcd-118">For HLSL reference documentation, see the [Reference for HLSL](./dx-graphics-hlsl-reference.md).</span></span>

<span data-ttu-id="b5fcd-119">Der Referenz Abschnitt enthält eine komplette Liste der Sprachsyntax und der intrinsischen Funktionen, die in HLSL integriert sind, um Ihre Codierungs Anforderungen zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="b5fcd-119">The reference section has a complete listing of the language syntax and of the intrinsic functions that are built into HLSL in order to simplify your coding requirements.</span></span>

<span data-ttu-id="b5fcd-120">Außerdem finden Sie eine Erörterung von shadermodellen und Profilen, und der Shader-Modell Verweis Inhalt wird so weit wie das HLSL-Shader-Modell 1 zurückkehren.</span><span class="sxs-lookup"><span data-stu-id="b5fcd-120">There also you'll find a discussion of shader models versus profiles, and shader model reference content going back as far as HLSL shader model 1.</span></span> <span data-ttu-id="b5fcd-121">Es gibt auch Inhalte, die Assemblyanweisungen, das D3DCompiler-Tool und Informationen zu den Fehlern und Warnungen enthält, die ein Shader zurückgeben kann.</span><span class="sxs-lookup"><span data-stu-id="b5fcd-121">There's also content covering assembly instructions, the D3DCompiler tool, and info about the errors and warnings that a shader can return.</span></span>