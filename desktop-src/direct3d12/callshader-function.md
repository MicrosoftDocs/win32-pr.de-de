---
description: Ruft einen anderen Shader innerhalb eines Shaders auf.
ms.assetid: ''
title: CallShader-Funktion
ms.date: 05/31/2018
ms.localizationpriority: low
ms.topic: reference
topic_type:
- APIRef
- kbSyntax
api_name:
- CallShader
api_type:
- NA
ms.openlocfilehash: 8c5cdf4e0a71430d6375fd75ca553f92ca9539b9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342754"
---
# <a name="callshader-function"></a><span data-ttu-id="b90c0-103">CallShader-Funktion</span><span class="sxs-lookup"><span data-stu-id="b90c0-103">CallShader function</span></span>

<span data-ttu-id="b90c0-104">Ruft einen anderen Shader innerhalb eines Shaders auf.</span><span class="sxs-lookup"><span data-stu-id="b90c0-104">Invokes another shader from within a shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="b90c0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b90c0-105">Syntax</span></span>
<span data-ttu-id="b90c0-106">Diese intrinsische Funktionsdefinition entspricht der folgenden Funktions Vorlage:</span><span class="sxs-lookup"><span data-stu-id="b90c0-106">This intrinsic function definition is equivalent to the following function template:</span></span>

```
template<param_t>
void CallShader(uint ShaderIndex, inout param_t Parameter);
```



## <a name="parameters"></a><span data-ttu-id="b90c0-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="b90c0-107">Parameters</span></span>

`ShaderIndex`

<span data-ttu-id="b90c0-108">Eine ganze Zahl ohne Vorzeichen, die den Index in die Aufruf [Bare shadertabelle](callable-shader.md) darstellt, die im Aufruf von [**dispatchrays**] angegeben ist (/Windows/Desktop/API/d3d12/NF-d3d12-id3d12graphicscommandlist4-dispatchrays.</span><span class="sxs-lookup"><span data-stu-id="b90c0-108">An unsigned integer representing the index into the [callable shader](callable-shader.md) table specified in the call to [**DispatchRays**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-dispatchrays.</span></span>

`Parameter`

<span data-ttu-id="b90c0-109">Die benutzerdefinierten Parameter, die an den Aufruf baren Shader übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="b90c0-109">The user-defined parameters to pass to the callable shader.</span></span>  <span data-ttu-id="b90c0-110">Diese Parameter Struktur muss der Parameter Struktur entsprechen, die in dem Aufruf baren Shader verwendet wird, auf den in der Shader-Tabelle verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="b90c0-110">This parameter structure must match the parameter structure used in the callable shader pointed to in the shader table.</span></span>


## <a name="return-value"></a><span data-ttu-id="b90c0-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b90c0-111">Return Value</span></span>

<span data-ttu-id="b90c0-112">**void**</span><span class="sxs-lookup"><span data-stu-id="b90c0-112">**void**</span></span>

## <a name="remarks"></a><span data-ttu-id="b90c0-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b90c0-113">Remarks</span></span>

<span data-ttu-id="b90c0-114">Diese Funktion kann von den folgenden Raytracing-shadertypen aufgerufen werden:</span><span class="sxs-lookup"><span data-stu-id="b90c0-114">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="b90c0-115">**Callable-Shader**</span><span class="sxs-lookup"><span data-stu-id="b90c0-115">**Callable Shader**</span></span>](callable-shader.md)
* [<span data-ttu-id="b90c0-116">**Closest Hit-Shader**</span><span class="sxs-lookup"><span data-stu-id="b90c0-116">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="b90c0-117">**Miss-Shader**</span><span class="sxs-lookup"><span data-stu-id="b90c0-117">**Miss Shader**</span></span>](miss-shader.md)
* [<span data-ttu-id="b90c0-118">**Ray Generation-Shader**</span><span class="sxs-lookup"><span data-stu-id="b90c0-118">**Ray Generation Shader**</span></span>](ray-generation-shader.md)



## <a name="see-also"></a><span data-ttu-id="b90c0-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b90c0-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b90c0-120">Direct3D 12-Raytracing, HLSL-Referenz</span><span class="sxs-lookup"><span data-stu-id="b90c0-120">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




