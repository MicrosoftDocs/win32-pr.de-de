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
# <a name="d2d_ps_entry-function"></a>D2D \_ PS- \_ Einstiegs Funktion

Ein Makro, das einen Pixel-Shader-Einstiegspunkt mit dem angegebenen Funktionsnamen definiert.

## <a name="syntax"></a>Syntax

``` syntax
void WINAPI D2D_PS_ENTRY(
  in string Entryname
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Entryname* \[ in\]
</dt> <dd>

Der Name des Einstiegs Punkts für den Pixelshader.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie dieses Makro anstelle der normalen Angabe der Eingabe punkteingabe Signatur: alle Parameter sind implizit und werden während der Kompilierung von Direct2D hinzugefügt, abhängig vom Typ der Kompilierungs Ziele (Full Shader oder Export Function).

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

Beachten Sie in diesem kurzen Beispiel, dass keine Funktionsparameter deklariert werden, dass die Anzahl der Eingaben und der Typ der einzelnen Eingaben vor der Einstiegs Funktion deklariert wird. die Eingabe wird durch Aufrufen von [D2DGetInput](d2dgetinput.md)abgerufen, und die Präprozessordirektiven müssen vor dem einschließen der Hilfsdatei definiert werden.

Ein Verknüpfungs kompatibler Shader muss sowohl einen regulären Einzelpass-Pixel-Shader als auch eine Export-Shader-Funktion bereitstellen. Mit dem D2D \_ PS- \_ Eintrags Makro können alle diese aus demselben Code generiert werden, wenn Sie in Verbindung mit dem Shader-Kompilierungs Skript verwendet werden.

Beim Kompilieren eines vollständigen Shaders werden die Makros in den folgenden Code erweitert, der über eine D2D Effects-kompatible Eingabe Signatur verfügt.

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

Wenn eine Export Funktions Version desselben Codes kompiliert wird, wird der folgende Code generiert:

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

Beachten Sie, dass die Textur Eingabe, die normalerweise durch Sampling eines Texture2D abgerufen wird, durch eine Funktions Eingabe input0 ersetzt wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D2d1effecthelpers. hlsli</dt> </dl> |
| DLL<br/>    | <dl> <dt>D2d1.dll</dt> </dl>                |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Effektshader-Verknüpfung](effect-shader-linking.md)
</dt> <dt>

[HLSL-Hilfsprogramme](hlsl-helpers.md)
</dt> </dl>

 

 





