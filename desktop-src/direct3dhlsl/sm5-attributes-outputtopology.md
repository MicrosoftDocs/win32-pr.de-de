---
title: outputtopology
description: Definiert den primitiven Ausgabetyp für den Mosaik-.
ms.assetid: 4aba65e5-b005-43fd-a844-c7fbb1b7406c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 917a927ff80d4abe1b6509fd41281992a998c945
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103948321"
---
# <a name="outputtopology"></a><span data-ttu-id="4437c-103">outputtopology</span><span class="sxs-lookup"><span data-stu-id="4437c-103">outputtopology</span></span>

<span data-ttu-id="4437c-104">Definiert den primitiven Ausgabetyp für den Mosaik-.</span><span class="sxs-lookup"><span data-stu-id="4437c-104">Defines the output primitive type for the tessellator.</span></span>


```
outputtopology(X)      
```



## <a name="remarks"></a><span data-ttu-id="4437c-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4437c-105">Remarks</span></span>

<span data-ttu-id="4437c-106">X muss entweder [**Point**](dx-graphics-hlsl-geometry-shader.md), **Line**, **Dreieck \_ CW** oder **Dreieck \_ CCW** sein und muss in Anführungszeichen gesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="4437c-106">X must be either [**point**](dx-graphics-hlsl-geometry-shader.md), **line**, **triangle\_cw**, or **triangle\_ccw** and must be inside quotes.</span></span> <span data-ttu-id="4437c-107">Hier sind die gültigen Optionen für dieses Attribut angegeben:</span><span class="sxs-lookup"><span data-stu-id="4437c-107">Here are the valid options for this attribute:</span></span>


```
[outputtopology("point")]
[outputtopology("line")]
[outputtopology("triangle_cw")]
[outputtopology("triangle_ccw")]
```



<span data-ttu-id="4437c-108">Dieses Attribut wird in den folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="4437c-108">This attribute is supported in the following types of shaders:</span></span>



| <span data-ttu-id="4437c-109">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="4437c-109">Vertex</span></span> | <span data-ttu-id="4437c-110">Hülle</span><span class="sxs-lookup"><span data-stu-id="4437c-110">Hull</span></span> | <span data-ttu-id="4437c-111">Domain</span><span class="sxs-lookup"><span data-stu-id="4437c-111">Domain</span></span> | <span data-ttu-id="4437c-112">Geometrie</span><span class="sxs-lookup"><span data-stu-id="4437c-112">Geometry</span></span> | <span data-ttu-id="4437c-113">Pixel</span><span class="sxs-lookup"><span data-stu-id="4437c-113">Pixel</span></span> | <span data-ttu-id="4437c-114">Compute</span><span class="sxs-lookup"><span data-stu-id="4437c-114">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="4437c-115">x</span><span class="sxs-lookup"><span data-stu-id="4437c-115">x</span></span>    |        |          |       |         |



 

## <a name="related-topics"></a><span data-ttu-id="4437c-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4437c-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4437c-117">Shader Model 5-Attribute</span><span class="sxs-lookup"><span data-stu-id="4437c-117">Shader Model 5 Attributes</span></span>](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[<span data-ttu-id="4437c-118">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="4437c-118">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




