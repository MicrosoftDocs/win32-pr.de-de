---
title: D2D_PS_ENTRY-Funktion (D2d1effecthelpers. h)
description: Ein Makro, das einen Pixel-Shader-Einstiegspunkt mit dem angegebenen Funktionsnamen definiert.
ms.assetid: 4C87369A-EF51-46BA-9CA4-386630A7F866
keywords:
- D2D_PS_ENTRY-Funktion Direct2D
topic_type:
- apiref
api_name:
- D2D_PS_ENTRY
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7525416eed7700709d02d2ec17823cd57a8c12ba
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355880"
---
# <a name="d2d_ps_entry-function"></a><span data-ttu-id="d6a54-104">D2D \_ PS- \_ Einstiegs Funktion</span><span class="sxs-lookup"><span data-stu-id="d6a54-104">D2D\_PS\_ENTRY function</span></span>

<span data-ttu-id="d6a54-105">Ein Makro, das einen Pixel-Shader-Einstiegspunkt mit dem angegebenen Funktionsnamen definiert.</span><span class="sxs-lookup"><span data-stu-id="d6a54-105">A macro that defines a pixel shader entry point with the given function name.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6a54-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="d6a54-106">Syntax</span></span>

``` syntax
void WINAPI D2D_PS_ENTRY(
  in string Entryname
);
```

## <a name="parameters"></a><span data-ttu-id="d6a54-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="d6a54-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6a54-108">*Entryname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d6a54-108">*Entryname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6a54-109">Der Name des Einstiegs Punkts für den Pixelshader.</span><span class="sxs-lookup"><span data-stu-id="d6a54-109">The pixel shader entry point name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6a54-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d6a54-110">Return value</span></span>

<span data-ttu-id="d6a54-111">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="d6a54-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6a54-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d6a54-112">Remarks</span></span>

<span data-ttu-id="d6a54-113">Verwenden Sie dieses Makro anstelle der normalen Angabe der Eingabe punkteingabe Signatur: alle Parameter sind implizit und werden während der Kompilierung von Direct2D hinzugefügt, abhängig vom Typ der Kompilierungs Ziele (Full Shader oder Export Function).</span><span class="sxs-lookup"><span data-stu-id="d6a54-113">Use this macro instead of specifying the entry point s input signature in the normal manner: all parameters are implicit and added by Direct2D during compilation depending on the compilation target type (full shader or export function).</span></span>

``` syntax
#define D2D_INPUT_COUNT 1 
#define D2D_INPUT0_SIMPLE 
#include  d2d1effectauthor.hlsli  

D2D_PS_ENTRY(LinkingCompatiblePixelShader) 
{ 
    float4 input = D2DGetInput(0);  

    input.rgb *= input.a; 

    return input; 
} 
```

<span data-ttu-id="d6a54-114">Beachten Sie in diesem kurzen Beispiel, dass keine Funktionsparameter deklariert werden, dass die Anzahl der Eingaben und der Typ der einzelnen Eingaben vor der Einstiegs Funktion deklariert wird. die Eingabe wird durch Aufrufen von [D2DGetInput](d2dgetinput.md)abgerufen, und die Präprozessordirektiven müssen vor dem einschließen der Hilfsdatei definiert werden.</span><span class="sxs-lookup"><span data-stu-id="d6a54-114">In this short example note that no function parameters are declared, that the number of inputs and type of each input is declared before the entry function, the input is retrieved by calling [D2DGetInput](d2dgetinput.md), and that preprocessor directives must be defined before the helper file is included.</span></span>

<span data-ttu-id="d6a54-115">Ein Verknüpfungs kompatibler Shader muss sowohl einen regulären Einzelpass-Pixel-Shader als auch eine Export-Shader-Funktion bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="d6a54-115">A linking-compatible shader must provide both a regular single-pass pixel shader and an export shader function.</span></span> <span data-ttu-id="d6a54-116">Mit dem D2D \_ PS- \_ Eintrags Makro können alle diese aus demselben Code generiert werden, wenn Sie in Verbindung mit dem Shader-Kompilierungs Skript verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d6a54-116">The D2D\_PS\_ENTRY macro allows each of these to be generated from the same code, when used in conjunction with the shader compilation script.</span></span>

<span data-ttu-id="d6a54-117">Beim Kompilieren eines vollständigen Shaders werden die Makros in den folgenden Code erweitert, der über eine D2D Effects-kompatible Eingabe Signatur verfügt.</span><span class="sxs-lookup"><span data-stu-id="d6a54-117">When compiling a full shader, the macros are expanded into the following code, which has a D2D Effects-compatible input signature.</span></span>

``` syntax
Texture2D<float4> InputTexture0; 
SamplerState InputSampler0; 

float4 LinkingCompatiblePixelShader(
    float4 pos   : SV_POSITION,   
    float4 posScene : SCENE_POSITION,    
    float4 uv0  : TEXCOORD0 
    ) : SV_Target 
{ 
    float4 input = InputTexture0.Sample(InputSampler0, uv0.xy);  

    input.rgb *= input.a; 

    return input; 
} 
```

<span data-ttu-id="d6a54-118">Wenn eine Export Funktions Version desselben Codes kompiliert wird, wird der folgende Code generiert:</span><span class="sxs-lookup"><span data-stu-id="d6a54-118">When compiling an export function version of the same code, the following code is generated:</span></span>

``` syntax
// Shader function version 
export float4 LinkingCompatiblePixelShader_Function( 
    float4 input0 : INPUT0 
    ) 
{ 
    input.rgb *= input.a; 

    return input; 
} 
```

<span data-ttu-id="d6a54-119">Beachten Sie, dass die Textur Eingabe, die normalerweise durch Sampling eines Texture2D abgerufen wird, durch eine Funktions Eingabe input0 ersetzt wurde.</span><span class="sxs-lookup"><span data-stu-id="d6a54-119">Note that the texture input, normally retrieved by sampling a Texture2D, has been replaced with a function input input0.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6a54-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d6a54-120">Requirements</span></span>



| <span data-ttu-id="d6a54-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d6a54-121">Requirement</span></span> | <span data-ttu-id="d6a54-122">Wert</span><span class="sxs-lookup"><span data-stu-id="d6a54-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6a54-123">Header</span><span class="sxs-lookup"><span data-stu-id="d6a54-123">Header</span></span><br/> | <dl> <span data-ttu-id="d6a54-124"><dt>D2d1effecthelpers. hlsli</dt></span><span class="sxs-lookup"><span data-stu-id="d6a54-124"><dt>D2d1effecthelpers.hlsli</dt></span></span> </dl> |
| <span data-ttu-id="d6a54-125">DLL</span><span class="sxs-lookup"><span data-stu-id="d6a54-125">DLL</span></span><br/>    | <dl> <span data-ttu-id="d6a54-126"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6a54-126"><dt>D2d1.dll</dt></span></span> </dl>                |



## <a name="see-also"></a><span data-ttu-id="d6a54-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d6a54-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6a54-128">Effektshader-Verknüpfung</span><span class="sxs-lookup"><span data-stu-id="d6a54-128">Effect Shader Linking</span></span>](effect-shader-linking.md)
</dt> <dt>

[<span data-ttu-id="d6a54-129">HLSL-Hilfsprogramme</span><span class="sxs-lookup"><span data-stu-id="d6a54-129">HLSL Helpers</span></span>](hlsl-helpers.md)
</dt> </dl>

 

 





