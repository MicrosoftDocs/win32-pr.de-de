---
description: Nachdem ein Effekt erstellt wurde, besteht der erste Schritt im Kompilieren des Codes, um nach Syntaxproblemen zu suchen.
ms.assetid: b8d8a0b7-b520-44e4-8691-6eb46202c092
title: Kompilieren eines Effekts (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6e0c4364fab67b0e0e7c97b7478a023f6394b5515e6f1d16cf2d352172af6c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128427"
---
# <a name="compile-an-effect-direct3d-10"></a>Kompilieren eines Effekts (Direct3D 10)

Nachdem ein Effekt erstellt wurde, besteht der erste Schritt im Kompilieren des Codes, um nach Syntaxproblemen zu suchen. Dies erfolgt durch Aufrufen einer der Kompilierungs-APIs (z.B. D3DX10CompileEffectFromFile, D3DX10CompileEffectFromResource, D3DX10CompileEffectFromMemory). Diese APIs rufen den Effektcompiler fxc.exe, bei dem es sich um den Compiler handelt, der zum Kompilieren von HLSL-Code verwendet wird. Aus diesem Grund sieht die Syntax für Code in einem Effekt sehr ähnlich wie HLSL-Code aus (es gibt einige Ausnahmen, die später behandelt werden). Der Effektcompiler/hlsl-Compiler (fxc.exe) befindet sich im SDK im Ordner utilities, sodass Sie Ihre Shader (oder Effekte) bei Wahl offline kompilieren können. Weitere Informationen finden Sie in der Dokumentation zum Ausführen des Compilers über die Befehlszeile.

-   [Enthält](#includes)
-   [Makros](#macros)
-   [HLSL-Shaderflags](#hlsl-shader-flags)
-   [FX-Flags](#fx-flags)
-   [Überprüfen von Fehlern](#checking-errors)
-   [Zugehörige Themen](#related-topics)

Hier ist ein Beispiel für das Kompilieren einer Effektdatei (aus dem BasicHLSL10-Beispiel).


```
WCHAR str[MAX_PATH];
DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL10.fx" );

hr = D3DX10CompileEffectFromFile( str, NULL, NULL, "fx_4_0", 
    D3D10_SHADER_ENABLE_STRICTNESS, 0, pd3dDevice, NULL, NULL, 
    &l_pBlob_Effect, &l_pBlob_Errors, NULL );
```



## <a name="includes"></a>Includes

Ein Parameter ist eine Includeschnittstelle. Generieren Sie eine dieser Einstellungen, wenn Sie beim Lesen einer Includedatei ein benutzerdefiniertes Verhalten verwenden möchten. Dieses benutzerdefinierte Verhalten wird jedes Mal ausgeführt, wenn ein Effekt (der den Includezeiger verwendet) erstellt wird oder wenn ein Effekt (der den Includezeiger verwendet) kompiliert wird. Um benutzerdefiniertes Includeverhalten zu implementieren, leiten Sie eine Klasse von der Include-Schnittstelle ab. Dies bietet Ihrer Klasse zwei Methoden: Open und Close. Implementieren Sie das benutzerdefinierte Verhalten in den Open- und Close-Methoden.

## <a name="macros"></a>Makros

Die Effektkompilierung kann auch einen Zeiger auf Makros verwenden, die an anderer Stelle definiert sind. Angenommen, Sie sollten den Effekt in BasicHLSL10 ändern, um zwei Makros zu verwenden: null und eins. Der Effektcode, der die beiden Makros verwendet, wird hier gezeigt.


```
if( bAnimate )
    vAnimatedPos += float4(vNormal, zero) *  
        (sin(g_fTime+5.5)+0.5)*5;
        
    Output.Diffuse.a = one;         
```



Hier ist die Deklaration für die beiden Makros.


```
D3D_SHADER_MACRO Shader_Macros[3] = { "zero", "0", "one", "1.0f", NULL, NULL };
```



Die Makros sind ein mit NULL beendetes Array von Makros. wobei jedes Makro mit einer [**D3D-SHADER-MAKRO-Struktur \_ \_**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) definiert wird.

Ändern Sie abschließend den Compile Effect-Aufruf, um einen Zeiger auf die Makros zu verwenden.


```
D3DX10CreateEffectFromFile( str, Shader_Macros, NULL, 
    D3D10_SHADER_ENABLE_STRICTNESS, 0, pd3dDevice, NULL, NULL, 
    &g_pEffect10, NULL );
```



## <a name="hlsl-shader-flags"></a>HLSL-Shaderflags

Shaderflags geben Shadereinschränkungen für den HLSL-Compiler an. Diese Flags wirken sich auf den vom Shadercompiler generierten Code aus, einschließlich:

-   Überlegungen zur Größe: Optimieren Sie den Code.
-   Überlegungen zum Debuggen: Einschließlich Debuginformationen, Verhindern der Flusssteuerung.
-   Hardwareüberlegungen: das Kompilierungsziel und ob ein Shader auf Legacyhardware ausgeführt werden kann.

Im Allgemeinen können diese Flags logisch kombiniert werden, vorausgesetzt, Sie haben nicht zwei in Konflikt stehende Merkmale angegeben. Eine Liste der Flags finden Sie unter [Effect Constants (Direct3D 10)](d3d10-graphics-reference-effect-constants.md).

## <a name="fx-flags"></a>FX-Flags

Diese Flags werden beim Erstellen eines Effekts verwendet, um das Kompilierungsverhalten oder das Laufzeiteffektverhalten zu definieren. Eine Liste der Flags finden Sie unter [Effect Constants (Direct3D 10)](d3d10-graphics-reference-effect-constants.md).

## <a name="checking-errors"></a>Überprüfen von Fehlern

Wenn während der Kompilierung ein Fehler auftritt, gibt die API eine Schnittstelle zurück, die die vom Effektcompiler zurückgegebenen Fehler enthält. Diese Schnittstelle heißt ID3D10Blob. Es ist nicht direkt lesbar, aber durch zurückgeben eines Zeigers auf den Puffer, der die Daten enthält (eine Zeichenfolge), können Kompilierungsfehler angezeigt werden.

In diesem Beispiel wurde ein Fehler in den Effekt BasicHLSL.fx eingeführt, indem die erste Variablendeklaration zweimal kopiert wurde.


```
//-------------------------------------------------------------------
// Global variables
//-------------------------------------------------------------------
float4 g_MaterialAmbientColor;      // Material's ambient color

// Declare the same variable twice
float4 g_MaterialAmbientColor;      // Material's ambient color
```



Durch diesen Fehler hat der Compiler den folgenden Fehler zurückgegeben, wie im folgenden Screenshot des Fensters "Watch" in Microsoft Visual Studio.

![Screenshot des Visual Studio-Fensters "Watch"](images/effect-compile-errors-2.jpg)

Da der Fehler in einem LPVOID-Zeiger zurückgegeben wird, können Sie ihn im Fenster "Watch&quot; in eine Zeichenfolge casten.

Hier ist der Code, mit dem der Fehler aus der fehlgeschlagenen Kompilierung zurückgegeben wird.


```
// Read the D3DX effect file
WCHAR str[MAX_PATH];
ID3D10Blob* l_pBlob_Effect = NULL;
ID3D10Blob* l_pBlob_Errors = NULL;
hr = DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L&quot;BasicHLSL10.fx" );
hr = D3DX10CompileEffectFromFile( str, NULL, NULL, 
    D3D10_SHADER_ENABLE_STRICTNESS, 0, NULL, 
    &l_pBlob_Effect, &l_pBlob_Errors );

LPVOID l_pError = NULL;
if( l_pBlob_Errors )
{
    l_pError = l_pBlob_Errors->GetBufferPointer();
    // then cast to a char* to see it in the locals window
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Rendern eines Effekts (Direct3D 10)](d3d10-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 



