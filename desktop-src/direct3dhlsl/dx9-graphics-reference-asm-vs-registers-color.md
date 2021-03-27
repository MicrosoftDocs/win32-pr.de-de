---
title: Farb Register
description: Diese Ausgabe Register des Vertex-Shader enthalten einen Farbwert.
ms.assetid: fd36e207-7312-4c7e-b664-b2de9ba1ebcf
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 38ee29ebafd9e7374fa868c6d84ad45f6c07dedf
ms.sourcegitcommit: 3f366316c02c411c4c5e14620a699f6f30608634
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2021
ms.locfileid: "104350869"
---
# <a name="color-register"></a><span data-ttu-id="1ba2b-103">Farb Register</span><span class="sxs-lookup"><span data-stu-id="1ba2b-103">Color Register</span></span>

<span data-ttu-id="1ba2b-104">Diese Ausgabe Register des Vertex-Shader enthalten einen Farbwert.</span><span class="sxs-lookup"><span data-stu-id="1ba2b-104">These vertex shader output registers contain a color value.</span></span> 

| <span data-ttu-id="1ba2b-105">Register</span><span class="sxs-lookup"><span data-stu-id="1ba2b-105">Register</span></span> | <span data-ttu-id="1ba2b-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1ba2b-106">Description</span></span>              |
|----------|--------------------------|
| <span data-ttu-id="1ba2b-107">oD0</span><span class="sxs-lookup"><span data-stu-id="1ba2b-107">oD0</span></span>      | <span data-ttu-id="1ba2b-108">diffuses Farbregister.</span><span class="sxs-lookup"><span data-stu-id="1ba2b-108">diffuse color register.</span></span>  |
| <span data-ttu-id="1ba2b-109">oD1</span><span class="sxs-lookup"><span data-stu-id="1ba2b-109">oD1</span></span>      | <span data-ttu-id="1ba2b-110">Glanz Farben Register.</span><span class="sxs-lookup"><span data-stu-id="1ba2b-110">specular color register.</span></span> |



 

<span data-ttu-id="1ba2b-111">Der oD0-Wert wird interpoliert und in die Pixel-Shader-Farbregister 0 (V0) geschrieben.</span><span class="sxs-lookup"><span data-stu-id="1ba2b-111">The oD0 value is interpolated and is written to the pixel shader color register 0 (v0).</span></span> <span data-ttu-id="1ba2b-112">Der oD1-Wert wird interpoliert und in die Pixel-Shader-Farbregister 1 (v1) geschrieben.</span><span class="sxs-lookup"><span data-stu-id="1ba2b-112">The oD1 value is interpolated and written to the pixel shader color register 1 (v1).</span></span> <span data-ttu-id="1ba2b-113">Weitere Informationen zu Pixel-Shader-Farb Registern finden Sie im Thema Pixel Shader- [Eingabe Farbregistrierung](dx9-graphics-reference-asm-ps-registers-input-color.md) .</span><span class="sxs-lookup"><span data-stu-id="1ba2b-113">For more information about pixel shader color registers, see the pixel shader [Input Color Register](dx9-graphics-reference-asm-ps-registers-input-color.md) topic.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ba2b-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1ba2b-114">Remarks</span></span>

<span data-ttu-id="1ba2b-115">Beispiel</span><span class="sxs-lookup"><span data-stu-id="1ba2b-115">Example</span></span>


```
min oD0, r0, c1.x    
```



## <a name="related-topics"></a><span data-ttu-id="1ba2b-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1ba2b-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ba2b-117">Vertex-Shader-Register</span><span class="sxs-lookup"><span data-stu-id="1ba2b-117">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




