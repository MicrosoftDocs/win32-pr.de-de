---
description: Nachdem ein Effekt erstellt wurde, besteht der erste Schritt darin, den Code zu kompilieren, um auf Syntax Probleme zu überprüfen.
ms.assetid: b8d8a0b7-b520-44e4-8691-6eb46202c092
title: Kompilieren eines Effekts (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab6183f2f71b07c482fa24efc4f9fed199216d75
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214084"
---
# <a name="compile-an-effect-direct3d-10"></a>Kompilieren eines Effekts (Direct3D 10)

Nachdem ein Effekt erstellt wurde, besteht der erste Schritt darin, den Code zu kompilieren, um auf Syntax Probleme zu überprüfen. Dies erfolgt durch Aufrufen einer der Kompilierungs-APIs (z. b. D3DX10CompileEffectFromFile, D3DX10CompileEffectFromResource, D3DX10CompileEffectFromMemory). Diese API ruft den Effekt Compiler auf fxc.exe der der Compiler ist, der zum Kompilieren von HLSL-Code verwendet wird. Aus diesem Grund sieht die Syntax für Code in einem Effekt sehr ähnlich wie der HLSL-Code aus (es gibt einige Ausnahmen, die später behandelt werden). Auf diese Weise befindet sich der Effekt Compiler/HLSL Compiler (fxc.exe) im SDK im Ordner Hilfsprogramme, sodass Sie Ihre Shader (oder Effekte) Offline kompilieren können, wenn Sie auswählen. Weitere Informationen finden Sie in der Dokumentation zum Ausführen des Compilers von der Befehlszeile aus.

-   [Includes](#includes)
-   [Makros](#macros)
-   [HLSL-shaderflags](#hlsl-shader-flags)
-   [FX-Flags](#fx-flags)
-   [Überprüfen von Fehlern](#checking-errors)
-   [Zugehörige Themen](#related-topics)

Im folgenden finden Sie ein Beispiel für das Kompilieren einer Effekt Datei (aus dem BasicHLSL10-Beispiel).


```
WCHAR str[MAX_PATH];
DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL10.fx" );

hr = D3DX10CompileEffectFromFile( str, NULL, NULL, "fx_4_0", 
    D3D10_SHADER_ENABLE_STRICTNESS, 0, pd3dDevice, NULL, NULL, 
    &l_pBlob_Effect, &l_pBlob_Errors, NULL );
```



## <a name="includes"></a>Includes

Ein Parameter ist eine include-Schnittstelle. Generieren Sie eine dieser Dateien, wenn Sie ein angepasstes Verhalten beim Lesen einer Includedatei einschließen möchten. Dieses benutzerdefinierte Verhalten wird jedes Mal ausgeführt, wenn ein Effekt (der den Include-Zeiger verwendet) erstellt wird oder wenn ein Effekt (der den Include-Zeiger verwendet) kompiliert wird. Um das angepasste include-Verhalten zu implementieren, leiten Sie eine Klasse von der include-Schnittstelle ab Dies bietet zwei Methoden für die Klasse: Öffnen und schließen. Implementieren Sie das benutzerdefinierte Verhalten in den Open-und Close-Methoden.

## <a name="macros"></a>Makros

Die Effekt Kompilierung kann auch einen Zeiger auf Makros annehmen, die an anderer Stelle definiert sind. Nehmen Sie beispielsweise an, dass Sie den Effekt in BasicHLSL10 ändern, um zwei Makros zu verwenden: NULL und eins. Der Effekt Code, der die beiden Makros verwendet, wird hier dargestellt.


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



Die Makros sind ein mit Null endendes Array von Makros. Dabei ist jedes Makro mit einer [**D3D \_ Shader- \_ Makro**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) Struktur definiert.

Ändern Sie abschließend den Kompilierungs Effekt-Befehl, um einen Zeiger auf die Makros zu übernehmen.


```
D3DX10CreateEffectFromFile( str, Shader_Macros, NULL, 
    D3D10_SHADER_ENABLE_STRICTNESS, 0, pd3dDevice, NULL, NULL, 
    &g_pEffect10, NULL );
```



## <a name="hlsl-shader-flags"></a>HLSL-shaderflags

Shaderflags geben Shader-Einschränkungen für den HLSL-Compiler an. Diese Flags wirken sich auf den vom Shader-Compiler generierten Code aus, einschließlich:

-   Überlegungen zur Größe: Optimieren Sie den Code.
-   Überlegungen zum Debuggen: einschließlich Debuginformationen, verhindern der Fluss Steuerung
-   Überlegungen zur Hardware: das Kompilierungs Ziel und ob ein Shader auf Legacy Hardware ausgeführt werden kann.

Im Allgemeinen können diese Flags logisch kombiniert werden, vorausgesetzt, dass Sie nicht zwei widersprüchliche Merkmale angegeben haben. Eine Auflistung der Flags finden Sie unter [Effect-Konstanten (Direct3D 10)](d3d10-graphics-reference-effect-constants.md).

## <a name="fx-flags"></a>FX-Flags

Diese Flags werden beim Erstellen eines Effekts verwendet, um entweder das Kompilierungs Verhalten oder das Lauf Zeit Effekt Verhalten zu definieren. Eine Auflistung der Flags finden Sie unter [Effect-Konstanten (Direct3D 10)](d3d10-graphics-reference-effect-constants.md).

## <a name="checking-errors"></a>Überprüfen von Fehlern

Wenn während der Kompilierung ein Fehler auftritt, gibt die API eine Schnittstelle zurück, die die vom Effekt Compiler zurückgegebenen Fehler enthält. Diese Schnittstelle wird als ID3D10Blob bezeichnet. Er ist jedoch nicht direkt lesbar. durch Zurückgeben eines Zeigers auf den Puffer, der die Daten enthält (eine Zeichenfolge), können alle Kompilierungsfehler angezeigt werden.

In diesem Beispiel wurde ein Fehler in die basichlsl. FX-Auswirkung eingefügt, indem die erste Variablen Deklaration zweimal kopiert wurde.


```
//-------------------------------------------------------------------
// Global variables
//-------------------------------------------------------------------
float4 g_MaterialAmbientColor;      // Material's ambient color

// Declare the same variable twice
float4 g_MaterialAmbientColor;      // Material's ambient color
```



Dieser Fehler hat bewirkt, dass der Compiler den folgenden Fehler zurückgibt, wie im folgenden Screenshot des Fensters Überwachen in Microsoft Visual Studio gezeigt.

![Screenshot des Fensters "Überwachen von Visual Studio"](images/effect-compile-errors-2.jpg)

Da der Fehler in einem LPVOID-Zeiger zurückgegeben wird, wandeln Sie ihn in eine Zeichenfolge im Überwachungs Fenster um.

Hier ist der Code, mit dem der Fehler aus der fehlgeschlagenen Kompilierung zurückgegeben wird.


```
// Read the D3DX effect file
WCHAR str[MAX_PATH];
ID3D10Blob* l_pBlob_Effect = NULL;
ID3D10Blob* l_pBlob_Errors = NULL;
hr = DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL10.fx" );
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

 

 



