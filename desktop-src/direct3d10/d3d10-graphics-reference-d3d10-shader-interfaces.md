---
description: 'Dieser Abschnitt enthält Informationen zu den folgenden Shader-Schnittstellen:'
ms.assetid: d8770b45-a05c-4dd8-9fa7-08fb4330d734
title: Shader-Schnittstellen (Direct3D 10-Grafiken)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 838a65d263533d0b2225515664e21c2d93114495
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483398"
---
# <a name="shader-interfaces-direct3d-10-graphics"></a><span data-ttu-id="0a4ee-103">Shader-Schnittstellen (Direct3D 10-Grafiken)</span><span class="sxs-lookup"><span data-stu-id="0a4ee-103">Shader Interfaces (Direct3D 10 Graphics)</span></span>

<span data-ttu-id="0a4ee-104">Dieser Abschnitt enthält Informationen zu den folgenden Shader-Schnittstellen:</span><span class="sxs-lookup"><span data-stu-id="0a4ee-104">This section contains information about the following shader interfaces:</span></span>

<span data-ttu-id="0a4ee-105">Jede dieser shaderschnittstellen verwaltet einen kompilierten Shader.</span><span class="sxs-lookup"><span data-stu-id="0a4ee-105">Each of these shader interfaces manages a compiled shader.</span></span> <span data-ttu-id="0a4ee-106">Die-Schnittstelle wird erstellt, wenn ein Shader kompiliert wird, und wird dann an verschiedene APIs weitergegeben, die Zugriff auf einen kompilierten Shader benötigen. Dies ist beispielsweise der Fall, wenn ein Shader an eine Pipeline Phase gebunden oder eine shadersignatur erhalten wird.</span><span class="sxs-lookup"><span data-stu-id="0a4ee-106">The interface is created when a shader is compiled, and is then passed to various APIs that need access to a compiled shader; such as when binding a shader to a pipeline stage or getting a shader signature.</span></span>



| <span data-ttu-id="0a4ee-107">Pipeline-Stage Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="0a4ee-107">Pipeline-Stage Interfaces</span></span>                                      | <span data-ttu-id="0a4ee-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0a4ee-108">Description</span></span>                                                                                                                                 |
|----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0a4ee-109">**ID3D10GeometryShader-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="0a4ee-109">**ID3D10GeometryShader Interface**</span></span>](/windows/win32/api/d3d10/nn-d3d10-id3d10geometryshader) | <span data-ttu-id="0a4ee-110">Ein Geometry-Shader implementiert pro primitiver Verarbeitung in der [Geometry-Shader-Stufe](d3d10-graphics-programming-guide-pipeline-stages.md).</span><span class="sxs-lookup"><span data-stu-id="0a4ee-110">A geometry-shader implements per-primitive processing in the [geometry-shader stage](d3d10-graphics-programming-guide-pipeline-stages.md).</span></span> |
| [<span data-ttu-id="0a4ee-111">**ID3D10PixelShader-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="0a4ee-111">**ID3D10PixelShader Interface**</span></span>](/windows/win32/api/d3d10/nn-d3d10-id3d10pixelshader)       | <span data-ttu-id="0a4ee-112">Ein Pixel-Shader implementiert die Verarbeitung pro Pixel in der [Pixel-Shader-Stufe](d3d10-graphics-programming-guide-pipeline-stages.md).</span><span class="sxs-lookup"><span data-stu-id="0a4ee-112">A pixel-shader implements per-pixel processing in the [pixel-shader stage](d3d10-graphics-programming-guide-pipeline-stages.md).</span></span>           |
| [<span data-ttu-id="0a4ee-113">**ID3D10VertexShader-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="0a4ee-113">**ID3D10VertexShader Interface**</span></span>](/windows/win32/api/d3d10/nn-d3d10-id3d10vertexshader)     | <span data-ttu-id="0a4ee-114">Ein Vertex-Shader implementiert die Verarbeitung pro Scheitelpunkt in der [Vertex-Shader-Stufe](d3d10-graphics-programming-guide-pipeline-stages.md).</span><span class="sxs-lookup"><span data-stu-id="0a4ee-114">A vertex-shader implements per-vertex processing in the [vertex-shader stage](d3d10-graphics-programming-guide-pipeline-stages.md).</span></span>        |



 

<span data-ttu-id="0a4ee-115">Shader-reflektionsschnittstellen ermöglichen einer Anwendung, den Inhalt eines Shaders zur Entwurfs-/Schreibzeit zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="0a4ee-115">Shader-reflection interfaces allow an application to inspect the contents of a shader at design/author time.</span></span> <span data-ttu-id="0a4ee-116">Die Shader-Reflektion ist für das Festlegen von Variablen zur Laufzeit nicht sinnvoll, da es sich um einen Spiegel der shaderdaten handelt, und unterstützt daher keine Methoden zum Festlegen von Daten.</span><span class="sxs-lookup"><span data-stu-id="0a4ee-116">Shader reflection is not useful for setting variables at runtime as it is a mirror of the shader data, and therefore supports no methods for setting data.</span></span>



| <span data-ttu-id="0a4ee-117">Shader-Reflection Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="0a4ee-117">Shader-Reflection Interfaces</span></span>                                                                   | <span data-ttu-id="0a4ee-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0a4ee-118">Description</span></span>                                                                        |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="0a4ee-119">**ID3D10ShaderReflection-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="0a4ee-119">**ID3D10ShaderReflection Interface**</span></span>](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflection)                             | <span data-ttu-id="0a4ee-120">Eine COM-Schnittstelle zum Lesen von Informationen aus einem kompilierten Shader zur Autor Zeit.</span><span class="sxs-lookup"><span data-stu-id="0a4ee-120">A COM interface for reading information from a compiled shader at author time.</span></span>     |
| [<span data-ttu-id="0a4ee-121">**ID3D10ShaderReflectionConstantBuffer-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="0a4ee-121">**ID3D10ShaderReflectionConstantBuffer Interface**</span></span>](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflectionconstantbuffer) | <span data-ttu-id="0a4ee-122">Eine Hilfsschnittstelle zum erhalten einer Shader-Reflection-Konstante für den Puffer.</span><span class="sxs-lookup"><span data-stu-id="0a4ee-122">A helper interface for getting a shader-reflection constant-buffer interface.</span></span>      |
| [<span data-ttu-id="0a4ee-123">**ID3D10ShaderReflectionType-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="0a4ee-123">**ID3D10ShaderReflectionType Interface**</span></span>](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflectiontype)                     | <span data-ttu-id="0a4ee-124">Eine Hilfsschnittstelle zum erhalten einer Shader-Reflektionstyp-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="0a4ee-124">A helper interface for getting a shader-reflection-type interface.</span></span>                 |
| [<span data-ttu-id="0a4ee-125">**ID3D10ShaderReflectionVariable-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="0a4ee-125">**ID3D10ShaderReflectionVariable Interface**</span></span>](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflectionvariable)             | <span data-ttu-id="0a4ee-126">Eine Hilfsschnittstelle zum erhalten einer Shader-Reflection-Variable-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="0a4ee-126">A helper interface for getting a shader-reflection-variable interface.</span></span>             |
| [<span data-ttu-id="0a4ee-127">**ID3D10ShaderResourceView-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="0a4ee-127">**ID3D10ShaderResourceView Interface**</span></span>](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)                         | <span data-ttu-id="0a4ee-128">Eine Shader-reflektionssschnittstelle zum Lesen von Informationen aus einer Shader-Ressourcen Ansicht.</span><span class="sxs-lookup"><span data-stu-id="0a4ee-128">A shader-reflection interface for reading information from a shader-resource view.</span></span> |



 

<span data-ttu-id="0a4ee-129">Shader Reflection-APIs implementieren eine com-Shader-reflektionsanschnittstelle ([**ID3D10ShaderReflection Interface**](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflection)) und mehrere nicht-com-Hilfsobjekte (die restlichen Schnittstellen).</span><span class="sxs-lookup"><span data-stu-id="0a4ee-129">Shader reflection APIs implement one COM shader reflection interface ([**ID3D10ShaderReflection Interface**](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflection)) and several non-COM helper interfaces (the rest of the interfaces).</span></span> <span data-ttu-id="0a4ee-130">**ID3D10ShaderReflection Interface** wird erstellt, wenn ein Shader-Reflektionsobjekt erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="0a4ee-130">**ID3D10ShaderReflection Interface** is created when a shader reflection object is created.</span></span> <span data-ttu-id="0a4ee-131">Es folgt den Standard-com-Regeln. das Erstellen der-Schnittstelle erhöht den Verweis Zähler, und die Schnittstelle muss freigegeben werden, wenn Sie nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="0a4ee-131">It follows standard COM rules; creating the interface increases a reference count and the interface must be released when it is no longer needed.</span></span> <span data-ttu-id="0a4ee-132">Die verbleibenden Shader-Reflection-Schnittstellen sind hilfsschnittstellen, die nicht von IUnknown erben.</span><span class="sxs-lookup"><span data-stu-id="0a4ee-132">The remaining shader-reflection interfaces are helper interfaces that do not inherit from IUnknown.</span></span> <span data-ttu-id="0a4ee-133">Dies bedeutet, dass Sie bei der Erstellung keinen Verweis Zähler ändern und nicht zerstört werden müssen, wenn Sie damit fertig sind.</span><span class="sxs-lookup"><span data-stu-id="0a4ee-133">This means that they do not change any reference count when they are created, and they do not need to be destroyed when you are finished with them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0a4ee-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0a4ee-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a4ee-135">Shader-Referenz</span><span class="sxs-lookup"><span data-stu-id="0a4ee-135">Shader Reference</span></span>](d3d10-graphics-reference-d3d10-shader.md)
</dt> </dl>

 

 
