---
description: Auf dieser Seite erfahren Sie, wie Sie einen Effekt generieren und verwenden.
ms.assetid: d9fdafed-5958-4995-a1b5-8881feca1291
title: Verwenden eines Effekts (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d240148c8817a3e480099a3ad1acb81bbff60803b0d0a8327e3a77cba681b5b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119856100"
---
# <a name="using-an-effect-direct3d-9"></a>Verwenden eines Effekts (Direct3D 9)

Auf dieser Seite erfahren Sie, wie Sie einen Effekt generieren und verwenden. Die behandelten Themen umfassen Folgendes:

-   [Erstellen eines Effekts](#create-an-effect)
-   [Rendern eines Effekts](#render-an-effect)
-   [Verwenden von Semantik zum Suchen von Effektparametern](#use-semantics-to-find-effect-parameters)
-   [Effizientes Abrufen und Festlegen von Parametern mithilfe von Handles](#use-handles-to-get-and-set-parameters-efficiently)
-   [Hinzufügen von Parameterinformationen mit Anmerkungen](#add-parameter-information-with-annotations)
-   [Share Effect-Parameter](#share-effect-parameters)
-   [Offlinekompilieren eines Effekts](#compile-an-effect-offline)
-   [Verbessern der Leistung mit Preshadern](#improve-performance-with-preshaders)
-   [Verwenden von Parameterblöcken zum Verwalten von Effektparametern](#use-parameter-blocks-to-manage-effect-parameters)

## <a name="create-an-effect"></a>Erstellen eines Effekts

Im Folgenden finden Sie ein Beispiel für das Erstellen eines Effekts aus dem [BasicHLSL-Beispiel.](../directx-sdk--august-2009-.md) Der Effekterstellungscode zum Erstellen eines Debug-Shaders stammt aus **OnCreateDevice:**


```
ID3DXEffect* g_pEffect = NULL;
DWORD dwShaderFlags = 0;

    dwShaderFlags |= D3DXSHADER_FORCE_VS_SOFTWARE_NOOPT;
    dwShaderFlags |= D3DXSHADER_FORCE_PS_SOFTWARE_NOOPT;
    dwShaderFlags |= D3DXSHADER_NO_PRESHADER;

    // Read the D3DX effect file
    WCHAR str[MAX_PATH];
    DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL.fx" );

    D3DXCreateEffectFromFile( 
        pd3dDevice, 
        str, 
        NULL, // CONST D3DXMACRO* pDefines,
        NULL, // LPD3DXINCLUDE pInclude,
        dwShaderFlags, 
        NULL, // LPD3DXEFFECTPOOL pPool,
        &g_pEffect, 
        NULL );
```



Diese Funktion verwendet die folgenden Argumente:

-   Das Gerät.
-   Der Dateiname der Effektdatei.
-   Ein Zeiger auf eine auf NULL endende Liste von \# definiert, die beim Analysieren des Shaders verwendet werden soll.
-   Ein optionaler Zeiger auf einen vom Benutzer geschriebenen Includehandler. Der Handler wird immer dann vom Prozessor aufgerufen, wenn er ein Include auflösen \# muss.
-   Ein Shaderkompilierungsflag, das dem Compiler Hinweise zur Verwendung des Shaders gibt. Die Optionen lauten:
    -   Überspringen der Validierung, wenn als gut bekannte Shader kompiliert werden.
    -   Überspringen der Optimierung (wird manchmal verwendet, wenn das Debuggen durch Optimierungen erschwert wird).
    -   Anfordern von Debuginformationen, die in den Shader eingeschlossen werden sollen, damit sie debuggen werden können.
-   Der Effektpool. Wenn mehrere Effekte denselben Speicherpoolzeiger verwenden, werden die globalen Variablen in den Effekten gemeinsam verwendet. Wenn keine Auswirkungsvariablen freigegeben werden müssen, kann der Speicherpool auf **NULL** festgelegt werden.
-   Ein Zeiger auf den neuen Effekt.
-   Ein Zeiger auf einen Puffer, an den Validierungsfehler gesendet werden können. In diesem Beispiel wurde der -Parameter auf **NULL** festgelegt und nicht verwendet.

> [!Note]  
> Ab dem SDK vom Dezember 2006 ist der DirectX 10 HLSL-Compiler jetzt sowohl in DirectX 9 als auch in DirectX 10 der Standardcompiler. Weitere Informationen finden Sie [unter Effektcompilertool.](../direct3dtools/fxc.md)

 

## <a name="render-an-effect"></a>Rendern eines Effekts

Die Reihenfolge der Aufrufe zum Anwenden des Effektzustands auf ein Gerät lautet:

-   [**ID3DXEffect::Begin**](id3dxeffect--begin.md) legt die aktive Technik fest.
-   [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md) legt den aktiven Pass fest.
-   [**ID3DXEffect::CommitChanges**](id3dxeffect--commitchanges.md) aktualisiert Änderungen an allen festgelegten Aufrufen im Durchlauf. Dies sollte vor einem Draw-Aufruf aufgerufen werden.
-   [**ID3DXEffect::EndPass**](id3dxeffect--endpass.md) beendet einen Pass.
-   [**ID3DXEffect::End**](id3dxeffect--end.md) beendet die aktive Technik.

Der Effektrenderingcode ist auch einfacher als der entsprechende Rendercode ohne Effekt. Hier ist der Rendercode mit einem Effekt:


```
// Apply the technique contained in the effect 
g_pEffect->Begin(&cPasses, 0);

for (iPass = 0; iPass < cPasses; iPass++)
{
    g_pEffect->BeginPass(iPass);

    // Only call CommitChanges if any state changes have happened
    // after BeginPass is called
    g_pEffect->CommitChanges();

    // Render the mesh with the applied technique
    g_pMesh->DrawSubset(0);

    g_pEffect->EndPass();
}
g_pEffect->End();
```



Die Renderschleife besteht aus dem Abfragen des Effekts, um zu sehen, wie viele Durchläufe darin enthalten sind, und anschließendes Aufrufen aller Durchläufe für eine Technik. Die Renderschleife kann erweitert werden, um mehrere Techniken mit jeweils mehreren Durchläufen aufzurufen.

## <a name="use-semantics-to-find-effect-parameters"></a>Verwenden von Semantik zum Suchen von Effektparametern

Eine Semantik ist ein Bezeichner, der an einen Effect-Parameter angefügt ist, damit eine Anwendung nach dem Parameter suchen kann. Ein Parameter kann höchstens eine Semantik aufweisen. Die Semantik befindet sich nach einem Doppelpunkt (:) nach dem Parameternamen. Zum Beispiel:


```
float4x4 matWorldViewProj : WORLDVIEWPROJ;
```



Wenn Sie die globale Auswirkungsvariable deklariert haben, ohne eine Semantik zu verwenden, würde sie stattdessen wie folgt aussehen:


```
float4x4 matWorldViewProj;
```



Die Effektschnittstelle kann eine Semantik verwenden, um ein Handle für einen bestimmten Effektparameter abzurufen. Beispielsweise gibt Folgendes das Handle der Matrix zurück:


```
D3DHANDLE handle = 
    m_pEffect->GetParameterBySemantic(NULL, "WORLDVIEWPROJ");
```



Neben der Suche nach semantischem Namen verfügt die Effect-Schnittstelle über viele andere Methoden, um nach Parametern zu suchen.

## <a name="use-handles-to-get-and-set-parameters-efficiently"></a>Effizientes Abrufen und Festlegen von Parametern mithilfe von Handles

Handles stellen eine effiziente Möglichkeit zum Verweisen auf Effektparameter, Techniken, Durchläufe und Anmerkungen mit einem Effekt bereit. Handles (vom Typ D3DXHANDLE) sind Zeichenfolgenzeiger. Die Handles, die an Funktionen wie GetParameterxxx oder GetAnnotationxxx übergeben werden, können in einer von drei Formen vorliegen:

-   Ein handle, das von einer Funktion wie GetParameterxxx zurückgegeben wird.
-   Eine Zeichenfolge, die den Namen des Parameters, der Technik, des Durchlaufs oder der Anmerkung enthält.
-   Ein Handle, das auf **NULL** festgelegt ist.

In diesem Beispiel wird ein Handle für den Parameter zurückgegeben, an den die WORLDVIEWPROJ-Semantik angefügt ist:


```
D3DHANDLE handle = 
    m_pEffect->GetParameterBySemantic(NULL, "WORLDVIEWPROJ");
```



## <a name="add-parameter-information-with-annotations"></a>Hinzufügen von Parameterinformationen mit Anmerkungen

Anmerkungen sind benutzerspezifische Daten, die an jede technik-, pass- oder parameter-Methode angefügt werden können. Eine Anmerkung ist eine flexible Möglichkeit zum Hinzufügen von Informationen zu einzelnen Parametern. Die Informationen können auf beliebige Weise von der Anwendung gelesen und verwendet werden. Eine Anmerkung kann einen beliebigen Datentyp aufweisen und dynamisch hinzugefügt werden. Anmerkungsdeklarationen werden durch spitzen Klammern getrennt. Eine Anmerkung enthält Folgendes:

-   Ein -Datentyp.
-   Ein Variablenname.
-   Ein Gleichheitszeichen (=).
-   Der Datenwert.
-   Ein endendes Semikolon (;).

Beispielsweise enthalten die beiden vorherigen Beispiele in diesem Artikel diese Anmerkung:


```
texture Tex0 < string name = "tiger.bmp"; >;
```



Die Anmerkung wird an das Texturobjekt angefügt und gibt die Texturdatei an, die zum Initialisieren des Texturobjekts verwendet werden soll. Die Anmerkung initialisiert das Texturobjekt nicht. Es handelt sich lediglich um benutzerbezogene Informationen, die an die Variable angefügt sind. Eine Anwendung kann die Anmerkung entweder mit [**ID3DXBaseEffect::GetAnnotation**](id3dxbaseeffect--getannotation.md) oder [**ID3DXBaseEffect::GetAnnotationByName**](id3dxbaseeffect--getannotationbyname.md) lesen, um die Zeichenfolge zurückzugeben. Anmerkungen können auch von der Anwendung hinzugefügt werden.

Jede Anmerkung:

-   Muss entweder numerisch oder Zeichenfolgen sein.
-   Muss immer mit einem Standardwert initialisiert werden.
-   Kann Techniken [und Durchläufen (Direct3D 9)](techniques-and-passes.md) und [Effektparametern](/previous-versions/windows/desktop/ee417539(v=vs.85))der obersten Ebene zugeordnet werden.
-   Kann mit [**ID3DXEffect**](id3dxeffect.md) oder [**ID3DXEffectCompiler**](id3dxeffectcompiler.md)in geschrieben und daraus gelesen werden.
-   Kann mit [**ID3DXEffect**](id3dxeffect.md)hinzugefügt werden.
-   Innerhalb des Effekts kann nicht darauf verwiesen werden.
-   Kann keine Untersemantik oder untergeordnete Anmerkungen aufweisen.

## <a name="share-effect-parameters"></a>Share Effect-Parameter

Effektparameter sind alle nicht statischen Variablen, die in einem Effekt deklariert werden. Dies kann globale Variablen und Anmerkungen enthalten. Effektparameter können von verschiedenen Effekten gemeinsam verwendet werden, indem Parameter mit dem Schlüsselwort "shared" deklariert und dann der Effekt mit einem Effektpool erstellt wird.

Ein Effektpool enthält Parameter für gemeinsame Effekte. Der Pool wird durch Aufrufen von [**D3DXCreateEffectPool**](d3dxcreateeffectpool.md)erstellt, der eine [**ID3DXEffectPool-Schnittstelle**](id3dxeffectpool.md) zurückgibt. Die -Schnittstelle kann als Eingabe für jede der D3DXCreateEffectxxx-Funktionen bereitgestellt werden, wenn ein Effekt erstellt wird. Damit ein Parameter für mehrere Effekte freigegeben werden kann, muss der Parameter in jedem der freigegebenen Effekte denselben Namen, Typ und dieselbe Semantik aufweisen.


```
ID3DXEffectPool* g_pEffectPool = NULL;   // Effect pool for sharing parameters

    D3DXCreateEffectPool( &g_pEffectPool );
```



Effekte, die Parameter gemeinsam nutzen, müssen dasselbe Gerät verwenden. Dies wird erzwungen, um die gemeinsame Nutzung von geräteabhängigen Parametern (z. B. Shadern oder Texturen) auf verschiedenen Geräten zu verhindern. Parameter werden immer dann aus dem Pool gelöscht, wenn die Auswirkungen, die die freigegebenen Parameter enthalten, freigegeben werden. Wenn keine Freigabeparameter erforderlich sind, stellen Sie **NULL** für den Auswirkungspool beim Erstellen eines Effekts zur Verfügung.

Geklonte Effekte verwenden denselben Effektpool wie der Effekt, aus dem sie geklont werden. Beim Klonen eines Effekts wird eine genaue Kopie eines Effekts erstellt, einschließlich globaler Variablen, Techniken, Durchläufe und Anmerkungen.

## <a name="compile-an-effect-offline"></a>Offlinekompilieren eines Effekts

Sie können einen Effekt zur Laufzeit mit [**D3DXCreateEffect**](d3dxcreateeffect.md)kompilieren, oder Sie können einen Effekt offline mit dem Befehlszeilencompilertool fxc.exe kompilieren. Der Effekt im [CompiledEffect-Beispiel](https://msdn.microsoft.com/library/Ee416326(v=VS.85).aspx) enthält einen Vertex-Shader, einen Pixel-Shader und eine Technik:


```
// File: CompiledEffect.fx

// Global variables
float4 g_MaterialAmbientColor;    // Material's ambient color
...

// Texture samplers
sampler RenderTargetSampler = 
   ...

// Type: Vertex shader                                      
VS_OUTPUT RenderSceneVS( float4 vPos : POSITION, 
                         float3 vNormal : NORMAL,
                         float2 vTexCoord0 : TEXCOORD0 )
{
   ...
};
// Type: Pixel shader
PS_OUTPUT RenderScenePS( VS_OUTPUT In ) 
{ 
   ...
}

// Type: Technique                                     
technique RenderScene
{
    pass P0
    {          
        ZENABLE = true;
        VertexShader = compile vs_1_1 RenderSceneVS();
        PixelShader  = compile ps_1_1 RenderScenePS();
    }
}
```



Mithilfe des [Effektcompilertools](../direct3dtools/fxc.md) zum Kompilieren des Shaders für \_ Vs. \_ 1 1 wurden die folgenden Assembly-Shaderanweisungen generiert:


```
//
// Generated by Microsoft (R) D3DX9 Shader Compiler 4.09.02.1188
//
//   fxc /T vs_1_1 /E RenderSceneVS /Fc CompiledEffect.txt CompiledEffect.fx
//
//
// Parameters:
//
//   float4 g_LightAmbient;
//   float4 g_LightDiffuse;
//   float3 g_LightDir;
//   float4 g_MaterialAmbientColor;
//   float4 g_MaterialDiffuseColor;
//   float g_fTime;
//   float4x4 g_mWorld;
//   float4x4 g_mWorldViewProjection;
//
//
// Registers:
//
//   Name                   Reg   Size
//   ---------------------- ----- ----
//   g_mWorldViewProjection c0       4
//   g_mWorld               c4       3
//   g_MaterialAmbientColor c7       1
//   g_MaterialDiffuseColor c8       1
//   g_LightDir             c9       1
//   g_LightAmbient         c10      1
//   g_LightDiffuse         c11      1
//   g_fTime                c12      1
//
//
// Default values:
//
//   g_LightDir
//     c9   = { 0.57735, 0.57735, 0.57735, 0 };
//
//   g_LightAmbient
//     c10  = { 1, 1, 1, 1 };
//
//   g_LightDiffuse
//     c11  = { 1, 1, 1, 1 };
//

    vs_1_1
    def c13, 0.159154937, 0.25, 6.28318548, -3.14159274
    def c14, -2.52398507e-007, 2.47609005e-005, -0.00138883968, 0.0416666418
    def c15, -0.5, 1, 0.5, 0
    dcl_position v0
    dcl_normal v1
    dcl_texcoord v2
    mov r0.w, c12.x
    mad r0.w, r0.w, c13.x, c13.y
    expp r3.y, r0.w
    mov r0.w, r3.y
    mad r0.w, r0.w, c13.z, c13.w
    mul r0.w, r0.w, r0.w
    mad r1.w, r0.w, c14.x, c14.y
    mad r1.w, r0.w, r1.w, c14.z
    mad r1.w, r0.w, r1.w, c14.w
    mad r1.w, r0.w, r1.w, c15.x
    mad r0.w, r0.w, r1.w, c15.y
    mul r0.w, r0.w, v0.x
    mul r0.x, r0.w, c15.z
    dp3 r1.x, v1, c4
    dp3 r1.y, v1, c5
    dp3 r1.z, v1, c6
    mov r0.yzw, c15.w
    dp3 r2.x, r1, r1
    add r0, r0, v0
    rsq r1.w, r2.x
    dp4 oPos.x, r0, c0
    mul r1.xyz, r1, r1.w
    dp4 oPos.y, r0, c1
    dp3 r1.x, r1, c9
    dp4 oPos.z, r0, c2
    max r1.w, r1.x, c15.w
    mov r1.xyz, c8
    mul r1.xyz, r1, c11
    mov r2.xyz, c7
    mul r2.xyz, r2, c10
    dp4 oPos.w, r0, c3
    mad oD0.xyz, r1, r1.w, r2
    mov oD0.w, c15.y
    mov oT0.xy, v2

// approximately 34 instruction slots used
```



## <a name="improve-performance-with-preshaders"></a>Verbessern der Leistung mit Preshadern

Ein Preshader ist eine Technik zur Steigerung der Shadereffizienz durch Vorabberechnung konstanter Shaderausdrücke. Der Effektcompiler pullt automatisch Shaderberechnungen aus dem Text eines Shaders und führt sie auf der CPU aus, bevor der Shader ausgeführt wird. Folglich funktionieren Preshader nur mit Effekten. Beispielsweise können diese beiden Ausdrücke außerhalb des Shaders ausgewertet werden, bevor sie ausgeführt werden.


```
mul(World,mul(View, Projection));
sin(time)
```



Shaderberechnungen, die verschoben werden können, sind solche, die einheitlichen Parametern zugeordnet sind. Das heißt, die Berechnungen ändern sich nicht für jeden Scheitelpunkt oder jedes Pixel. Wenn Sie Effekte verwenden, generiert der Effektcompiler automatisch einen Preshader und führt diesen aus. Es sind keine zu aktivierenden Flags vorhanden. Preshader können die Anzahl der Anweisungen pro Shader reduzieren und auch die Anzahl konstanter Register reduzieren, die ein Shader nutzt.

Stellen Sie sich den Effektcompiler als eine Art Compiler mit mehreren Prozessoren vor, da er Shadercode für zwei Arten von Prozessoren kompiliert: eine CPU und eine GPU. Darüber hinaus wurde der Effektcompiler entwickelt, um Code von der GPU auf die CPU zu verschieben und somit die Shaderleistung zu verbessern. Dies ähnelt dem Pullen eines statischen Ausdrucks aus einer Schleife. Ein Shader, der die Position vom Weltraum in den Projektionsbereich transformiert und Texturkoordinaten kopiert, würde in HLSL wie folgt aussehen:


```
float4x4 g_mWorldViewProjection;    // World * View * Projection matrix
float4x4 g_mWorldInverse;           // Inverse World matrix
float3 g_LightDir;                  // Light direction in world space
float4 g_LightDiffuse;              // Diffuse color of the light

struct VS_OUTPUT
{
    float4 Position   : POSITION;   // vertex position 
    float2 TextureUV  : TEXCOORD0;  // vertex texture coords 
    float4 Diffuse    : COLOR0;     // vertex diffuse color
};

VS_OUTPUT RenderSceneVS( float4 vPos : POSITION, 
                         float3 vNormal : NORMAL,
                         float2 vTexCoord0 : TEXCOORD0)
{
    VS_OUTPUT Output;
    
    // Transform the position from object space to projection space
    Output.Position = mul(vPos, g_mWorldViewProjection);

    // Transform the light from world space to object space    
    float3 vLightObjectSpace = normalize(mul(g_LightDir, (float3x3)g_mWorldInverse)); 

    // N dot L lighting
    Output.Diffuse = max(0,dot(vNormal, vLightObjectSpace));
    
    // Copy the texture coordinate
    Output.TextureUV = vTexCoord0; 
    
    return Output;    
}
technique RenderVS
{
    pass P0
    {          
        VertexShader = compile vs_1_1 RenderSceneVS();
    }
}
```



Mithilfe des [Effektcompilertools](../direct3dtools/fxc.md) zum Kompilieren des Shaders für \_ Vs. \_ 1 1 werden die folgenden Assemblyanweisungen generiert:


```
technique RenderVS
{
    pass P0
    {
        vertexshader = 
            asm {
            //
            // Generated by Microsoft (R) D3DX9 Shader Compiler 9.15.779.0000
            //
            // Parameters:
            //
            //   float3 g_LightDir;
            //   float4x4 g_mWorldInverse;
            //   float4x4 g_mWorldViewProjection;
            //
            //
            // Registers:
            //
            //   Name                   Reg   Size
            //   ---------------------- ----- ----
            //   g_mWorldViewProjection c0       4
            //   g_mWorldInverse        c4       3
            //   g_LightDir             c7       1
            //
            
                vs_1_1
                def c8, 0, 0, 0, 0
                dcl_position v0
                dcl_normal v1
                dcl_texcoord v2
                mov r1.xyz, c7
                dp3 r0.x, r1, c4
                dp3 r0.y, r1, c5
                dp3 r0.z, r1, c6
                dp4 oPos.x, v0, c0
                dp3 r1.x, r0, r0
                dp4 oPos.y, v0, c1
                rsq r0.w, r1.x
                dp4 oPos.z, v0, c2
                mul r0.xyz, r0, r0.w
                dp4 oPos.w, v0, c3
                dp3 r0.x, v1, r0
                max oD0, r0.x, c8.x
                mov oT0.xy, v2
            
            // approximately 14 instruction slots used
            };

        //No embedded pixel shader
    }
}
```



Dies verbraucht ungefähr 14 Slots und 9 Konstantenregister. Mit einem Preshader verschiebt der Compiler die statischen Ausdrücke aus dem Shader und in den Preshader. Der gleiche Shader würde wie folgt mit einem Preshader aussehen:


```
technique RenderVS
{
    pass P0
    {
        vertexshader = 
            asm {
            //
            // Generated by Microsoft (R) D3DX9 Shader Compiler 9.15.779.0000
            //
            // Parameters:
            //
            //   float3 g_LightDir;
            //   float4x4 g_mWorldInverse;
            //
            //
            // Registers:
            //
            //   Name            Reg   Size
            //   --------------- ----- ----
            //   g_mWorldInverse c0       3
            //   g_LightDir      c3       1
            //
            
                preshader
                dot r0.x, c3.xyz, c0.xyz
                dot r0.y, c3.xyz, c1.xyz
                dot r0.z, c3.xyz, c2.xyz
                dot r1.w, r0.xyz, r0.xyz
                rsq r0.w, r1.w
                mul c4.xyz, r0.w, r0.xyz
            
            // approximately 6 instructions used
            //
            // Generated by Microsoft (R) D3DX9 Shader Compiler 9.15.779.0000
            //
            // Parameters:
            //
            //   float4x4 g_mWorldViewProjection;
            //
            //
            // Registers:
            //
            //   Name                   Reg   Size
            //   ---------------------- ----- ----
            //   g_mWorldViewProjection c0       4
            //
            
                vs_1_1
                def c5, 0, 0, 0, 0
                dcl_position v0
                dcl_normal v1
                dcl_texcoord v2
                dp4 oPos.x, v0, c0
                dp4 oPos.y, v0, c1
                dp4 oPos.z, v0, c2
                dp4 oPos.w, v0, c3
                dp3 r0.x, v1, c4
                max oD0, r0.x, c5.x
                mov oT0.xy, v2
            
            // approximately 7 instruction slots used
            };

        //No embedded pixel shader
    }
}
```



Ein Effekt führt einen Preshader direkt vor dem Ausführen eines Shaders aus. Das Ergebnis ist die gleiche Funktionalität mit höherer Shaderleistung, da die Anzahl der auszuführenden Anweisungen (je nach Shadertyp für jeden Scheitelpunkt oder jedes Pixel) reduziert wurde. Darüber hinaus werden weniger konstante Register vom Shader als Ergebnis der statischen Ausdrücke genutzt, die in den Preshader verschoben werden. Dies bedeutet, dass Shader, die zuvor durch die Anzahl der erforderlichen Konstantenregister begrenzt waren, jetzt möglicherweise kompiliert werden können, da sie weniger Konstantenregister erfordern. Es ist sinnvoll, von Preshadern eine Leistungsverbesserung von 5 Prozent und einer Leistungsverbesserung von 20 Prozent zu erwarten.

Beachten Sie, dass sich die Eingabekonstanten von den Ausgabekonstanten in einem Preshader unterscheiden. Die Ausgabe c1 entspricht nicht dem C1-Eingaberegister. Das Schreiben in ein Konstantenregister in einem Preshader schreibt tatsächlich in den Eingabeslot (Konstanten) des entsprechenden Shaders.


```
// BaseDelta c0 1
// Refinements c1 1
preshader
mul c1.x, c0.x, (-2)
add c0.x, c0.x, c0.x
cmp c5.x, c1.x, (1), (0)
```



Die obige cmp-Anweisung liest den Preshader c1-Wert, während die mul-Anweisung in die Hardwareshaderregister schreibt, die vom Vertexshader verwendet werden sollen.

## <a name="use-parameter-blocks-to-manage-effect-parameters"></a>Verwenden von Parameterblöcken zum Verwalten von Effektparametern

Parameterblöcke sind Blöcke mit Auswirkungszustandsänderungen. Ein Parameterblock kann Zustandsänderungen aufzeichnen, sodass sie später mit einem einzigen Aufruf angewendet werden können. Erstellen Sie einen Parameterblock, indem [**Sie ID3DXEffect::BeginParameterBlock**](id3dxeffect--beginparameterblock.md)aufrufen:


```
    m_pEffect->SetTechnique( "RenderScene" );

    m_pEffect->BeginParameterBlock();
    D3DXVECTOR4 v4( Diffuse.r, Diffuse.g, Diffuse.b, Diffuse.a );
    m_pEffect->SetVector( "g_vDiffuse", &v4 );
    m_pEffect->SetFloat( "g_fReflectivity", fReflectivity );
    m_pEffect->SetFloat( "g_fAnimSpeed", fAnimSpeed );
    m_pEffect->SetFloat( "g_fSizeMul", fSize );
    m_hParameters = m_pEffect->EndParameterBlock();
```



Der Parameterblock speichert vier Änderungen, die von den API-Aufrufen angewendet werden. Der Aufruf [**von ID3DXEffect::BeginParameterBlock**](id3dxeffect--beginparameterblock.md) beginnt mit der Aufzeichnung der Zustandsänderungen. [**ID3DXEffect::EndParameterBlock**](id3dxeffect--endparameterblock.md) beendet das Hinzufügen der Änderungen zum Parameterblock und gibt ein Handle zurück. Das Handle wird beim Aufrufen von [**ID3DXEffect::ApplyParameterBlock**](id3dxeffect--applyparameterblock.md)verwendet.

Im [EffectParam-Beispiel](https://msdn.microsoft.com/library/Ee417535(v=VS.85).aspx)wird der Parameterblock in der Rendersequenz angewendet:


```
CObj g_aObj[NUM_OBJS];       // Object instances

    if( SUCCEEDED( pd3dDevice->BeginScene() ) )
    {
        // Set the shared parameters using the first mesh's effect.

        // Render the mesh objects
        for( int i = 0; i < NUM_OBJS; ++i )
        {
            ID3DXEffect *pEffect = g_aObj[i].m_pEffect;

            // Apply the parameters
            pEffect->ApplyParameterBlock( g_aObj[i].m_hParameters );

            ...

            pEffect->Begin( &cPasses, 0 );
            for( iPass = 0; iPass < cPasses; iPass++ )
            {
              ...
            }
            pEffect->End();
        }

        ...
        pd3dDevice->EndScene();
    }
```



Der Parameterblock legt den Wert aller vier Zustandsänderungen unmittelbar vor dem Aufruf von [**ID3DXEffect::Begin**](id3dxeffect--begin.md) fest. Parameterblöcke sind eine praktische Möglichkeit, mehrere Zustandsänderungen mit einem einzelnen API-Aufruf festzulegen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Effekte](effects.md)
</dt> </dl>

 

 
