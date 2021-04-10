---
description: Auf dieser Seite erfahren Sie, wie Sie einen Effekt generieren und verwenden.
ms.assetid: d9fdafed-5958-4995-a1b5-8881feca1291
title: Verwenden eines Effekts (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1170fde625e5eee5e9665f0759d302b5f5450a41
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125575"
---
# <a name="using-an-effect-direct3d-9"></a>Verwenden eines Effekts (Direct3D 9)

Auf dieser Seite erfahren Sie, wie Sie einen Effekt generieren und verwenden. Die behandelten Themen umfassen Folgendes:

-   [Erstellen eines Effekts](#create-an-effect)
-   [Einen Effekt Rendering](#render-an-effect)
-   [Verwenden der Semantik zum Suchen von Effekt Parametern](#use-semantics-to-find-effect-parameters)
-   [Verwenden von Handles zum effizienten erhalten und Festlegen von Parametern](#use-handles-to-get-and-set-parameters-efficiently)
-   [Hinzufügen von Parameter Informationen mit Anmerkungen](#add-parameter-information-with-annotations)
-   [Parameter für Freigabe Effekte](#share-effect-parameters)
-   [Einen Effekt Offline kompilieren](#compile-an-effect-offline)
-   [Verbessern der Leistung durch preshaders](#improve-performance-with-preshaders)
-   [Verwenden von Parameter Blöcken zum Verwalten von Effekt Parametern](#use-parameter-blocks-to-manage-effect-parameters)

## <a name="create-an-effect"></a>Erstellen eines Effekts

Hier ist ein Beispiel für das Erstellen eines Effekts, der aus dem [basichlsl-Beispiel](../directx-sdk--august-2009-.md)stammt. Der Effekt Erstellungs Code zum Erstellen eines debugshaders ist von **onkreatedevice**:


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



Diese Funktion übernimmt die folgenden Argumente:

-   Das Gerät.
-   Der Dateiname der Effekt Datei.
-   Ein Zeiger auf eine mit NULL endende Liste von \# definiert, die beim Durchführen des Shaders verwendet werden soll.
-   Ein optionaler Zeiger auf einen Benutzer geschriebenen include-Handler. Der-Handler wird vom Prozessor aufgerufen, wenn er eine include auflösen muss \# .
-   Ein Shader-kompilierungsflag, das die compilerhinweise darüber gibt, wie der Shader verwendet wird. Die Optionen lauten:
    -   Die Validierung wird übersprungen, wenn bekannte gute Shader kompiliert werden.
    -   Die Optimierung wird übersprungen (manchmal verwendet, wenn Optimierungen das Debuggen erschweren).
    -   Anfordern von Debuginformationen, die in den Shader eingeschlossen werden sollen, damit Sie gedebuggt werden können.
-   Der Effekt Pool. Wenn mehr als ein Effekt denselben Speicherpool Zeiger verwendet, werden die globalen Variablen in den Effekten gemeinsam genutzt. Wenn Sie keine Auswirkung-Variablen freigeben müssen, kann der Speicherpool auf **null** festgelegt werden.
-   Ein Zeiger auf den neuen Effekt.
-   Ein Zeiger auf einen Puffer, an den Validierungs Fehler gesendet werden können. In diesem Beispiel wurde der-Parameter auf **null** festgelegt und nicht verwendet.

> [!Note]  
> Ab dem SDK vom Dezember 2006 ist der DirectX 10 HLSL-Compiler nun der Standard Compiler in DirectX 9 und DirectX 10. Ausführliche Informationen finden Sie unter [Effect-Compiler-Tool](../direct3dtools/fxc.md) .

 

## <a name="render-an-effect"></a>Einen Effekt Rendering

Die Abfolge der Aufrufe zum Anwenden des Wirkungs Zustands auf ein Gerät lautet wie folgt:

-   [**ID3DXEffect:: begin**](id3dxeffect--begin.md) legt die aktive Technik fest.
-   [**ID3DXEffect:: beginpass**](id3dxeffect--beginpass.md) legt den aktiven Durchlauf fest.
-   [**ID3DXEffect:: CommitChanges**](id3dxeffect--commitchanges.md) aktualisiert Änderungen an beliebigen Set-aufrufen im Durchlauf. Dies sollte vor einem Draw-Aufruf aufgerufen werden.
-   [**ID3DXEffect:: endpass**](id3dxeffect--endpass.md) beendet einen Durchlauf.
-   [**ID3DXEffect:: End**](id3dxeffect--end.md) beendet die aktive Technik.

Der Effekt-Rendering-Code ist auch einfacher als der entsprechende Rendering-Code. Hier ist der Rendering-Code mit einem Effekt:


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



Die Renderschleife besteht darin, den Effekt abzufragen, um zu sehen, wie viele Pass Sie enthält, und dann alle Durchgänge für eine Technik abzurufen. Die Renderschleife kann erweitert werden, um mehrere Techniken aufzurufen, die jeweils mehrere Durchgänge haben.

## <a name="use-semantics-to-find-effect-parameters"></a>Verwenden der Semantik zum Suchen von Effekt Parametern

Eine Semantik ist ein Bezeichner, der an einen Effektparameter angefügt wird, um einer Anwendung das Suchen nach dem Parameter zu ermöglichen. Ein Parameter kann höchstens über eine Semantik verfügen. Die Semantik befindet sich nach einem Doppelpunkt (:) nach dem Parameternamen. Beispiel:


```
float4x4 matWorldViewProj : WORLDVIEWPROJ;
```



Wenn Sie die globale Variable Auswirkung ohne Verwendung einer Semantik deklariert haben, sieht Sie stattdessen wie folgt aus:


```
float4x4 matWorldViewProj;
```



Die Effect-Schnittstelle kann eine Semantik verwenden, um ein Handle für einen bestimmten Effektparameter zu erhalten. Im folgenden Beispiel wird das Handle der Matrix zurückgegeben:


```
D3DHANDLE handle = 
    m_pEffect->GetParameterBySemantic(NULL, "WORLDVIEWPROJ");
```



Zusätzlich zum Durchsuchen des semantischen namens verfügt die Effect-Schnittstelle über viele andere Methoden, um nach Parametern zu suchen.

## <a name="use-handles-to-get-and-set-parameters-efficiently"></a>Verwenden von Handles zum effizienten erhalten und Festlegen von Parametern

Handles bieten eine effiziente Möglichkeit zum Verweisen auf wirkungsparameter, Techniken, Pass-und Anmerkungen mit einem Effekt. Handles (die vom Typ D3DXHANDLE sind) sind Zeichen folgen Zeiger. Die Handles, die an Funktionen wie getparameterxxx oder getannotationxxx übermittelt werden, können in einer von drei Formen vorliegen:

-   Ein Handle, das von einer Funktion wie getparameterxxx zurückgegeben wurde.
-   Eine Zeichenfolge, die den Namen des Parameters, der Technik, der Übergabe oder der Anmerkung enthält.
-   Ein Handle, das auf **null** festgelegt ist.

In diesem Beispiel wird ein Handle für den Parameter zurückgegeben, dem die "worldviewproj"-Semantik angefügt ist:


```
D3DHANDLE handle = 
    m_pEffect->GetParameterBySemantic(NULL, "WORLDVIEWPROJ");
```



## <a name="add-parameter-information-with-annotations"></a>Hinzufügen von Parameter Informationen mit Anmerkungen

Anmerkungen sind benutzerspezifische Daten, die an beliebige Techniken, Pass oder Parameter angefügt werden können. Eine Anmerkung ist eine flexible Möglichkeit zum Hinzufügen von Informationen zu einzelnen Parametern. Die Informationen können gelesen und auf jede Weise verwendet werden, die die Anwendung auswählt. Eine Anmerkung kann einen beliebigen Datentyp aufweisen und kann dynamisch hinzugefügt werden. Annotation-Deklarationen werden durch spitzen Klammern getrennt. Eine Anmerkung enthält Folgendes:

-   Ein-Datentyp.
-   Ein Variablenname.
-   Ein Gleichheitszeichen (=).
-   Der Datenwert.
-   Ein Semikolon mit Endpunkten (;).

Beispielsweise enthalten beide vorherigen Beispiele in diesem Dokument diese Anmerkung:


```
texture Tex0 < string name = "tiger.bmp"; >;
```



Die-Anmerkung wird an das Textur Objekt angefügt und gibt die Textur Datei an, die zum Initialisieren des Textur Objekts verwendet werden soll. Die-Anmerkung initialisiert nicht das Textur Objekt, sondern lediglich ein Teil der Benutzerinformationen, die an die Variable angefügt sind. Eine Anwendung kann die-Anmerkung entweder mit [**ID3DXBaseEffect:: GetAnnotation**](id3dxbaseeffect--getannotation.md) oder [**ID3DXBaseEffect:: getannotationbyname**](id3dxbaseeffect--getannotationbyname.md) lesen, um die Zeichenfolge zurückzugeben. Anmerkungen können auch von der Anwendung hinzugefügt werden.

Jede Anmerkung:

-   Muss entweder numerisch oder Zeichen folgen sein.
-   Muss immer mit einem Standardwert initialisiert werden.
-   Kann [Techniken und übergebenen (Direct3D 9)](techniques-and-passes.md) und [Effektparameter](/previous-versions/windows/desktop/ee417539(v=vs.85))der obersten Ebene zugeordnet werden.
-   Kann mit [**ID3DXEffect**](id3dxeffect.md) oder [**ID3DXEffectCompiler**](id3dxeffectcompiler.md)geschrieben und daraus gelesen werden.
-   Kann mit [**ID3DXEffect**](id3dxeffect.md)hinzugefügt werden.
-   Innerhalb des Effekts kann nicht auf Sie verwiesen werden.
-   Unter Semantik oder untergeordnete Anmerkungen sind nicht möglich.

## <a name="share-effect-parameters"></a>Parameter für Freigabe Effekte

Effektparameter sind alle nicht statischen Variablen, die in einem Effekt deklariert werden. Dies kann globale Variablen und Anmerkungen enthalten. Effektparameter können von verschiedenen Effekten gemeinsam genutzt werden, indem Parameter mit dem "Shared"-Schlüsselwort deklariert und dann der Effekt mit einem Effekt Pool erstellt wird.

Ein Effekt Pool enthält Parameter für gemeinsame Effekte. Der Pool wird durch Aufrufen von [**D3DXCreateEffectPool**](d3dxcreateeffectpool.md)erstellt, wodurch eine [**ID3DXEffectPool**](id3dxeffectpool.md) -Schnittstelle zurückgegeben wird. Die-Schnittstelle kann bei der Erstellung eines Effekts als Eingabe für jede der D3DXCreateEffectxxx-Funktionen bereitgestellt werden. Damit ein Parameter von mehreren Effekten gemeinsam genutzt werden kann, muss der Parameter in den einzelnen gemeinsamen Effekten denselben Namen, denselben Typ und dieselbe Semantik aufweisen.


```
ID3DXEffectPool* g_pEffectPool = NULL;   // Effect pool for sharing parameters

    D3DXCreateEffectPool( &g_pEffectPool );
```



Die Auswirkungen von Freigabe Parametern müssen das gleiche Gerät verwenden. Dies wird erzwungen, um zu verhindern, dass Geräte abhängige Parameter (z. b. Shader oder Texturen) auf verschiedenen Geräten gemeinsam genutzt werden. Parameter werden aus dem Pool gelöscht, wenn die Auswirkungen, die die freigegebenen Parameter enthalten, freigegeben werden. Wenn Freigabe Parameter nicht erforderlich sind, geben Sie bei der Erstellung eines Effekts **null** für den Effekt Pool an.

Geklonte Effekte verwenden denselben Effekt Pool wie der Effekt, von dem Sie geklont werden. Das Klonen eines Effekts führt zu einer exakten Kopie eines Effekts, einschließlich globaler Variablen, Techniken, Durchläufen und Anmerkungen.

## <a name="compile-an-effect-offline"></a>Einen Effekt Offline kompilieren

Sie können einen Effekt zur Laufzeit mit [**D3DXCreateEffect**](d3dxcreateeffect.md)kompilieren, oder Sie können einen Effekt Offline kompilieren, indem Sie das Befehlszeilen-Compilertool fxc.exe verwenden. Der Effekt im [compiledebug-Beispiel](https://msdn.microsoft.com/library/Ee416326(v=VS.85).aspx) enthält einen Vertex-Shader, einen Pixel-Shader und eine Technik:


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



Wenn Sie den Shader für vs 1 1 mit dem [Effekt-Compilertool](../direct3dtools/fxc.md) kompilieren, werden \_ die folgenden assemblyshaderanweisungen \_ generiert:


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



## <a name="improve-performance-with-preshaders"></a>Verbessern der Leistung durch preshaders

Ein preshader ist eine Technik zum Erhöhen der shadereffizienz, indem Konstante shaderausdrücke vorab berechnet werden. Der Effekt Compiler ruft die Shader-Berechnungen automatisch aus dem Text eines Shaders ab und führt Sie auf der CPU aus, bevor der Shader ausgeführt wird. Folglich arbeiten präshader nur mit Effekten. Diese beiden Ausdrücke können beispielsweise außerhalb des Shaders ausgewertet werden, bevor Sie ausgeführt werden.


```
mul(World,mul(View, Projection));
sin(time)
```



Shader-Berechnungen, die verschoben werden können, sind die, die einheitlichen Parametern zugeordnet sind. Das heißt, dass die Berechnungen für jeden Scheitelpunkt oder Pixel nicht geändert werden. Wenn Sie Effekte verwenden, generiert und führt der Effekt Compiler automatisch einen preshader für Sie aus. Es sind keine Flags zum Aktivieren vorhanden. Preshaders können die Anzahl der Anweisungen pro Shader verringern und auch die Anzahl der Konstanten Registrierungen verringern, die ein Shader beansprucht.

Stellen Sie sich den Effekt Compiler als eine Art von multiprozessorcompiler vor, da er Shader-Code für zwei Arten von Prozessoren kompiliert: eine CPU und eine GPU. Außerdem ist der Effekt Compiler so konzipiert, dass Code von der GPU in die CPU verschoben und somit die shaderleistung verbessert wird. Dies ist sehr ähnlich, wenn ein statischer Ausdruck aus einer Schleife abgerufen wird. Ein Shader, der die Position aus dem Raum in den Projektions Bereich umwandelt und Texturkoordinaten in HLSL wie folgt aussehen würde:


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



Wenn Sie den Shader für vs 1 1 mit dem [Effekt-Compilertool](../direct3dtools/fxc.md) kompilieren, werden \_ die folgenden Assemblyanweisungen \_ generiert:


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



Dies verbraucht ungefähr 14 Slots und beansprucht 9 Konstante Register. Bei einem preshader verschiebt der Compiler die statischen Ausdrücke aus dem Shader und in den preshader. Derselbe Shader würde wie folgt mit einem preshader aussehen:


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



Ein Effekt führt einen preshader direkt vor dem Ausführen eines Shaders aus. Das Ergebnis ist die gleiche Funktionalität mit erhöhter shaderleistung, da die Anzahl der Anweisungen, die ausgeführt werden müssen (für jeden Scheitelpunkt oder jedes Pixel, abhängig vom Typ des Shader), reduziert wurde. Außerdem werden weniger Konstante Register vom Shader beansprucht, weil die statischen Ausdrücke in den preshader verschoben werden. Dies bedeutet, dass Shader, die zuvor durch die Anzahl der benötigten Konstanten registriert wurden, jetzt kompiliert werden können, da Sie weniger Konstante Register benötigen. Es empfiehlt sich, eine Leistungsverbesserung von 5 Prozent und 20 Prozent zu erwarten.

Beachten Sie, dass sich die Eingabe Konstanten von den Ausgabe Konstanten in einem preshader unterscheiden. Die Ausgabe C1 ist nicht mit der Eingabe C1-Register identisch. Das Schreiben in ein konstantes Register in einem preshader schreibt tatsächlich in den eingabeslot (konstant) des Shader.


```
// BaseDelta c0 1
// Refinements c1 1
preshader
mul c1.x, c0.x, (-2)
add c0.x, c0.x, c0.x
cmp c5.x, c1.x, (1), (0)
```



Die obige CMP-Anweisung liest den preshader C1-Wert, während die mul-Anweisung in die Hardware-Shader-Register schreibt, die vom Vertexshader verwendet werden sollen.

## <a name="use-parameter-blocks-to-manage-effect-parameters"></a>Verwenden von Parameter Blöcken zum Verwalten von Effekt Parametern

Parameter Blöcke sind Blöcke der Auswirkung des Zustands. Ein Parameter Block kann Zustandsänderungen aufzeichnen, sodass Sie später mit einem einzigen-Befehl angewendet werden können. Erstellen Sie einen Parameter Block durch Aufrufen von [**ID3DXEffect:: beginparameterblock**](id3dxeffect--beginparameterblock.md):


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



Der Parameter Block speichert vier von den API-aufrufen angewendete Änderungen. Durch Aufrufen von [**ID3DXEffect:: beginparameterblock**](id3dxeffect--beginparameterblock.md) wird die Aufzeichnung der Zustandsänderungen gestartet. [**ID3DXEffect:: endparameterblock**](id3dxeffect--endparameterblock.md) beendet das Hinzufügen der Änderungen zum Parameter Block und gibt ein Handle zurück. Das Handle wird beim Aufrufen von [**ID3DXEffect:: applyparameterblock**](id3dxeffect--applyparameterblock.md)verwendet.

Im [effectparam-Beispiel](https://msdn.microsoft.com/library/Ee417535(v=VS.85).aspx)wird der Parameter Block in der Rendering-Sequenz angewendet:


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



Der Parameter Block legt den Wert aller vier Zustandsänderungen fest, kurz bevor [**ID3DXEffect:: begin**](id3dxeffect--begin.md) aufgerufen wird. Parameter Blöcke sind eine praktische Möglichkeit, mehrere Zustandsänderungen mit einem einzigen API-Befehl festzulegen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Effekte](effects.md)
</dt> </dl>

 

 
