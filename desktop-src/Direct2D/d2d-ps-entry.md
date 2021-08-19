---
title: D2D_PS_ENTRY -Funktion (D2d1effecthelpers.h)
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
ms.openlocfilehash: 26369ef5be8c9dea81bf95e60c09ca0041d4275114c8892b85b6b5525f45504b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087784"
---
# <a name="d2d_ps_entry-function"></a>D2D \_ PS \_ ENTRY-Funktion

Ein Makro, das einen Pixel-Shader-Einstiegspunkt mit dem angegebenen Funktionsnamen definiert.

## <a name="syntax"></a>Syntax

``` syntax
void WINAPI D2D_PS_ENTRY(
  in string Entryname
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Entryname* \[ In\]
</dt> <dd>

Der Name des Pixelschatteneinstiegspunkts.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Verwenden Sie dieses Makro, anstatt die Eingabesignatur des Einstiegspunkts auf normale Weise anzugeben: Alle Parameter werden implizit und von Direct2D während der Kompilierung hinzugefügt, je nach Kompilierungszieltyp (vollständiger Shader oder Exportfunktion).

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

Beachten Sie in diesem kurzen Beispiel, dass keine Funktionsparameter deklariert werden, dass die Anzahl der Eingaben und der Typ jeder Eingabe vor der Eingabefunktion deklariert, die Eingabe durch Aufrufen von [D2DGetInput](d2dgetinput.md)abgerufen wird und dass präprozessordirektiven definiert werden müssen, bevor die Hilfsdatei eingeschlossen wird.

Ein mit Verknüpfungen kompatibler Shader muss sowohl einen regulären Einzelpasspixel-Shader als auch eine Export-Shaderfunktion bereitstellen. Das D2D PS ENTRY-Makro ermöglicht es, jede dieser Makros aus demselben Code zu erstellen, wenn sie in Verbindung mit dem \_ \_ Shaderkompilierungsskript verwendet wird.

Beim Kompilieren eines vollständigen Shaders werden die Makros in den folgenden Code erweitert, der über eine D2D Effects-kompatible Eingabesignatur verfügt.

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

Beim Kompilieren einer Exportfunktionsversion desselben Codes wird der folgende Code generiert:

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

Beachten Sie, dass die Textureingabe, die normalerweise durch Sampling eines Texture2D abgerufen wird, durch eine Funktionseingabe input0 ersetzt wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D2d1effecthelpers.hlsli</dt> </dl> |
| DLL<br/>    | <dl> <dt>D2d1.dll</dt> </dl>                |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Effektshader-Verknüpfung](effect-shader-linking.md)
</dt> <dt>

[HLSL-Hilfsatoren](hlsl-helpers.md)
</dt> </dl>

 

 





