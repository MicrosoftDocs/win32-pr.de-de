---
title: Kompilieren eines Effekts (Direct3D 11)
description: Nachdem ein Effekt erstellt wurde, besteht der nächste Schritt darin, den Code zu kompilieren, um auf Syntax Probleme zu überprüfen.
ms.assetid: 7624d55e-6466-4156-8f31-30f0d25a2883
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3df304a7b657af19984008bd90a1be4bfe5219c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948858"
---
# <a name="compile-an-effect-direct3d-11"></a>Kompilieren eines Effekts (Direct3D 11)

Nachdem ein Effekt erstellt wurde, besteht der nächste Schritt darin, den Code zu kompilieren, um auf Syntax Probleme zu überprüfen.

Dies erreichen Sie, indem Sie eine der Kompilierungs-APIs aufrufen ([**D3DX11CompileFromFile**](d3dx11compilefromfile.md), [**D3DX11CompileFromMemory**](d3dx11compilefrommemory.md)oder [**D3DX11CompileFromResource**](d3dx11compilefromresource.md) ). Diese APIs rufen die Auswirkung-Compilerfxc.exe auf, die HLSL-Code kompiliert. Aus diesem Grund sieht die Syntax für Code in einem Effekt sehr ähnlich wie der HLSL-Code aus. (Es gibt einige Ausnahmen, die zu einem späteren Zeitpunkt behandelt werden.) Der Effekt Compiler/HLSL-Compiler (fxc.exe) steht im SDK im Ordner Hilfsprogramme zur Verfügung, damit shaderer (oder Effekte) Offline kompiliert werden können, wenn Sie auswählen. Weitere Informationen finden Sie in der Dokumentation zum Ausführen des Compilers von der Befehlszeile aus.

-   [Beispiel](#example)
-   [Includes](#includes)
-   [Suchen nach Includedateien](#searching-for-include-files)
-   [Makros](#macros)
-   [HLSL-shaderflags](#hlsl-shader-flags)
-   [FX-Flags](#fx-flags)
-   [Überprüfen von Fehlern](#checking-errors)
-   [Zugehörige Themen](#related-topics)

## <a name="example"></a>Beispiel

Im folgenden finden Sie ein Beispiel für das Kompilieren einer Effekt Datei.


```
WCHAR str[MAX_PATH];
DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL10.fx" );

hr = D3DX11CompileFromFile( str, NULL, NULL, pFunctionName, pProfile, D3D10_SHADER_ENABLE_STRICTNESS, NULL, NULL, &pBlob, &pErrorBlob, NULL );
```



## <a name="includes"></a>Includes

Ein Parameter der Compile-APIs ist eine include-Schnittstelle. Generieren Sie eine dieser Optionen, wenn Sie ein angepasstes Verhalten einschließen möchten, wenn der Compiler eine include-Datei liest. Der Compiler führt dieses benutzerdefinierte Verhalten jedes Mal aus, wenn er einen Effekt erstellt oder kompiliert (der den Include-Zeiger verwendet). Um das angepasste include-Verhalten zu implementieren, leiten Sie eine Klasse von der [**ID3DInclude**](/windows/desktop/api/D3Dcommon/nn-d3dcommon-id3dinclude) -Schnittstelle ab Dadurch wird die-Klasse mit zwei Methoden bereitstellt: [**Öffnen**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-open) und [**Schließen**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-close). Implementieren Sie das benutzerdefinierte Verhalten in diesen Methoden.

## <a name="searching-for-include-files"></a>Suchen nach Includedateien

Der Zeiger, den der Compiler im *PPARa entdata* -Parameter an die [**Open**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-open) -Methode Ihres include-Handlers übergibt, verweist möglicherweise nicht auf den Container, der die Includedatei enthält \# , die der Compiler zum Kompilieren Ihres shadercodes benötigt. Das heißt, der Compiler kann **null** in *pparameentdata* übergeben. Daher wird empfohlen, dass der include-Handler eine eigene Liste von include-Speicherorten für Inhalt durchsucht. Der include-Handler kann neue include-Speicherorte dynamisch hinzufügen, da diese Speicherorte in Aufrufen der **geöffneten** Methode empfangen.

Nehmen Sie im folgenden Beispiel an, dass die Includedateien des Shader-Codes beide im Verzeichnis " *Somewhere else* " gespeichert werden. Wenn der Compiler die [**Open**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-open) -Methode des include-Handlers aufruft, um den Inhalt von *Somewhere \\ foo. h* zu öffnen und zu lesen, kann der include-Handler den Speicherort des Verzeichnisses " **Somewhere else** " speichern. Wenn der Compiler später die **Open** -Methode des includehandlers aufruft, um den Inhalt von *Bar. h* zu öffnen und zu lesen, kann der include-Handler automatisch im Verzeichnis " *Somewhere else* " nach " *Bar. h*" suchen.


```
Main.hlsl:
#include "somewhereelse\foo.h"

Foo.h:
#include "bar.h"
```



## <a name="macros"></a>Makros

Die Effekt Kompilierung kann auch einen Zeiger auf Makros annehmen, die an anderer Stelle definiert sind. Nehmen Sie beispielsweise an, Sie möchten die Auswirkung in BasicHLSL10 ändern, um zwei Makros zu verwenden: NULL und eins. Der Effekt Code, der die beiden Makros verwendet, wird hier dargestellt.


```
if( bAnimate )
    vAnimatedPos += float4(vNormal, zero) *  
        (sin(g_fTime+5.5)+0.5)*5;
        
    Output.Diffuse.a = one;         
```



Hier ist die Deklaration für die beiden Makros.


```
D3D10_SHADER_MACRO Shader_Macros[3] = { "zero", "0", "one", "1.0f", NULL, NULL };
```



Die Makros sind ein mit Null endendes Array von Makros. , wobei jedes Makro mithilfe einer d3d10- [**\_ Shader- \_ Makro**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) Struktur definiert wird.

Ändern Sie den Kompilierungs Effekt-Befehl, um einen Zeiger auf die Makros zu übernehmen.


```
D3DX11CompileFromFile( str, Shader_Macros, NULL, pFunctionName, 
                       pProfile, D3D10_SHADER_ENABLE_STRICTNESS, NULL, 
                       NULL, &pBlob, &pErrorBlob, NULL );    
```



## <a name="hlsl-shader-flags"></a>HLSL-shaderflags

Shaderflags geben Shader-Einschränkungen für den HLSL-Compiler an. Diese Flags wirken sich auf den vom Shader-Compiler generierten Code auf folgende Weise aus:

-   Optimieren Sie die Codegröße.
-   Einschließlich der Debuginformationen, die die Fluss Steuerung verhindern.
-   Wirkt sich auf das Kompilierungs Ziel und darauf aus, ob ein Shader auf älterer Hardware ausgeführt werden kann.

Diese Flags können logisch kombiniert werden, wenn Sie nicht zwei widersprüchliche Merkmale angegeben haben. Eine Auflistung der Flags finden Sie unter [d3d10 \_ Shader Konstanten](/windows/desktop/direct3d10/d3d10-shader).

## <a name="fx-flags"></a>FX-Flags

Verwenden Sie diese Flags bei der Erstellung eines Effekts, um entweder das Kompilierungs Verhalten oder das Lauf Zeit Effekt Verhalten zu definieren. Eine Auflistung der Flags finden Sie unter [d3d10 \_ Effect Konstanten](/windows/desktop/direct3d10/d3d10-effect).

## <a name="checking-errors"></a>Überprüfen von Fehlern

Wenn während der Kompilierung ein Fehler auftritt, gibt die API eine Schnittstelle zurück, die die Fehler vom Effekt Compiler enthält. Diese Schnittstelle wird als [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))bezeichnet. Er ist nicht direkt lesbar. Wenn Sie jedoch einen Zeiger auf den Puffer zurückgeben, der die Daten enthält (eine Zeichenfolge), können Sie alle Kompilierungsfehler sehen.

Dieses Beispiel enthält einen Fehler in basichlsl. FX, die erste Variablen Deklaration wird zweimal ausgeführt.


```
//-------------------------------------------------------------------
// Global variables
//-------------------------------------------------------------------
float4 g_MaterialAmbientColor;      // Material's ambient color

// Declare the same variable twice
float4 g_MaterialAmbientColor;      // Material's ambient color
```



Dieser Fehler bewirkt, dass der Compiler den folgenden Fehler zurückgibt, wie im folgenden Screenshot der Überwachungsfenster in Microsoft Visual Studio gezeigt.

![Screenshot des Fensters "Visual Studio-Überwachung" mit dem Fehler "0x01997sb8"](images/effect-compile-errors-2.jpg)

Da der Compiler den Fehler in einem LPVOID-Zeiger zurückgibt, wandeln Sie ihn in eine Zeichenfolge in der Überwachungsfenster um.

Hier ist der Code angegeben, der den Fehler von der fehlgeschlagenen Kompilierung zurückgibt.


```
// Read the D3DX effect file
WCHAR str[MAX_PATH];
ID3DBlob*   l_pBlob_Effect = NULL;
ID3DBlob*   l_pBlob_Errors = NULL;
hr = DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL10.fx" );
hr = D3DX11CompileFromFile( str, NULL, NULL, pFunctionName, 
                       pProfile, D3D10_SHADER_ENABLE_STRICTNESS, NULL, 
                       NULL, &pBlob, &pErrorBlob, NULL );      

LPVOID l_pError = NULL;
if( pErrorBlob )
{
    l_pError = pErrorBlob->GetBufferPointer();
    // then cast to a char* to see it in the locals window
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Rendern eines Effekts (Direct3D 11)](d3d11-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 