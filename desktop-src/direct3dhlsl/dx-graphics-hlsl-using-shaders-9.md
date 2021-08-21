---
title: Verwenden von Shadern in Direct3D 9
description: Verwenden von Shadern in Direct3D 9
ms.assetid: 8d8f5124-fbf3-4af5-8399-43ba28aa6eb9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a1ef04c14682aa6e763222fd0c8db0e2eedf33abf747da97a16b2b1621e1c42a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119744"
---
# <a name="using-shaders-in-direct3d-9"></a>Verwenden von Shadern in Direct3D 9

-   [Kompilieren eines Shaders für bestimmte Hardware](#compiling-a-shader-for-specific-hardware)
-   [Initialisieren von Shaderkonstanten](#initializing-shader-constants)
-   [Binden eines Shaderparameters an ein bestimmtes Register](#binding-a-shader-parameter-to-a-particular-register)
-   [Rendern eines programmierbaren Shaders](#rendering-a-programmable-shader)
-   [Debuggen von Shadern](#debugging-shaders)
-   [Zugehörige Themen](#related-topics)

## <a name="compiling-a-shader-for-specific-hardware"></a>Kompilieren eines Shaders für bestimmte Hardware

Shader wurden zunächst in DirectX 8.0 zu Microsoft DirectX hinzugefügt. Zu diesem Zeitpunkt wurden mehrere virtuelle Shadercomputer definiert, die jeweils ungefähr einem bestimmten Grafikprozessor entsprechen, der von den führenden 3D-Grafikanbietern erzeugt wurde. Für jeden dieser virtuellen Shadercomputer wurde eine Assemblysprache entworfen. Programme, die in die Shadermodelle geschrieben wurden (Namen im Vergleich zu \_ \_ 1 1 und PS \_ \_ 1 1 – ps \_ \_ 1 4), waren relativ kurz und wurden in der Regel direkt von Entwicklern in der entsprechenden Assemblysprache geschrieben. Die Anwendung würde diesen lesbaren Assemblysprachcode mithilfe von [**D3DXAssembleShader**](/windows/desktop/direct3d9/d3dxassembleshader) an die D3DX-Bibliothek übergeben und eine binäre Darstellung des Shaders abrufen, die wiederum mit [**CreateVertexShader**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createvertexshader) oder [**CreatePixelShader**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createpixelshader)übergeben würde. Weitere Informationen finden Sie im Software Development Kit (SDK).

Die Situation in Direct3D 9 ist ähnlich. Eine Anwendung übergibt einen HLSL-Shader mit [**D3DXCompileShader an D3DX**](/windows/desktop/direct3d9/d3dxcompileshader) und erhält eine binäre Darstellung des kompilierten Shaders zurück, die wiederum mit [**createPixelShader**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createpixelshader) oder [**CreateVertexShader**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createvertexshader)an Microsoft Direct3D übergeben wird. Die Runtime weiß nichts über HLSL, sondern nur über die Binärassembly-Shadermodelle. Dies ist gut, da dies bedeutet, dass der HLSL-Compiler unabhängig von der Direct3D-Runtime aktualisiert werden kann. Sie können Shader auch offline mit [fxc](/windows/desktop/direct3dtools/fxc)kompilieren.

Zusätzlich zur Entwicklung des HLSL-Compilers wurden mit Direct3D 9 auch die Shadermodelle auf Assemblyebene eingeführt, um die Funktionalität der neuesten Generation von Grafikhardware verfügbar zu machen. Anwendungsentwickler können in der Assembly für diese neuen Modelle arbeiten \_ (vs. \_ 2 0, \_ \_ vs. 3 0, ps \_ 2 \_ 0, ps \_ 3 \_ 0), aber wir erwarten, dass die meisten Entwickler für die Shaderentwicklung zu HLSL wechseln.

Natürlich ermöglicht die Möglichkeit, ein HLSL-Programm zum Ausdrücken eines bestimmten Schattierungsalgorithmus zu schreiben, nicht automatisch die Ausführung auf einer bestimmten Hardware. Eine Anwendung ruft D3DX auf, um einen Shader mit [**D3DXCompileShader**](/windows/desktop/direct3d9/d3dxcompileshader)in binären Assemblycode zu kompilieren. Eine der Einschränkungen bei diesem Einstiegspunkt ist ein Parameter, der definiert, welche der Modelle auf Assemblyebene (oder Kompilierungsziele) der HLSL-Compiler verwenden soll, um den endgültigen Shadercode auszudrücken. Wenn eine Anwendung die HLSL-Shaderkompilierung zur Laufzeit (im Gegensatz zur Kompilierzeit oder offline) durchläuft, kann die Anwendung die Funktionen des Direct3D-Geräts untersuchen und das kompilierungsziel auswählen, das übereinstimmen soll. Wenn der im HLSL-Shader ausgedrückte Algorithmus zu komplex für die Ausführung auf dem ausgewählten Kompilierungsziel ist, tritt bei der Kompilierung ein Fehler auf. Dies bedeutet, dass HLSL zwar ein großer Vorteil für die Shaderentwicklung ist, entwickler jedoch nicht von der Realität des Versands von Spielen an eine Zielgruppe mit Grafikgeräten mit unterschiedlichen Funktionen frei wird. Als Spieleentwickler müssen Sie weiterhin einen mehrstufigen Ansatz für Ihre Visuals verwalten. Dies bedeutet, dass bessere Shader für leistungsfähigere Grafikkarten und einfachere Versionen für ältere Karten geschrieben werden. Bei gut geschriebenen HLSL kann diese Last jedoch erheblich reduziert werden.

Anstatt HLSL-Shader mithilfe von D3DX auf dem Computer des Kunden zur Ladezeit der Anwendung oder bei der ersten Verwendung zu kompilieren, entscheiden sich viele Entwickler dafür, ihren Shader von HLSL in binären Assemblycode zu kompilieren, bevor sie überhaupt geliefert werden. Dadurch wird der HLSL-Quellcode nicht mit blickenden Augen verfolgt, und es wird sichergestellt, dass alle Shader, die ihre Anwendung jemals ausführen wird, ihren internen Qualitätssicherungsprozess durchlaufen haben. Ein praktisches Hilfsprogramm zum Offline-Kompilieren von Shadern ist [fxc](/windows/desktop/direct3dtools/fxc). Dieses Tool verfügt über eine Reihe von Optionen, mit denen Sie Code für das angegebene Kompilierungsziel kompilieren können. Die Untersuchung der disassemblierten Ausgabe kann während der Entwicklung sehr lernfähig sein, wenn Sie Ihre Shader optimieren oder einfach nur die Funktionen des virtuellen Shadercomputers auf einer detaillierteren Ebene kennenlernen möchten. Diese Optionen sind unten zusammengefasst:

## <a name="initializing-shader-constants"></a>Initialisieren von Shaderkonstanten

Shaderkonstanten sind in der Konstantentabelle enthalten. Der Zugriff darauf ist über die [**ID3DXConstantTable-Schnittstelle**](/windows/desktop/direct3d9/id3dxconstanttable) möglich. Globale Shadervariablen können im Shadercode initialisiert werden. Diese werden zur Laufzeit durch Aufrufen von [**SetDefaults**](/windows/desktop/direct3d9/id3dxconstanttable--setdefaults)initialisiert.

## <a name="binding-a-shader-parameter-to-a-particular-register"></a>Binden eines Shaderparameters an ein bestimmtes Register

Der Compiler weist globalen Variablen automatisch Register zu. Der Compiler weist Umgebung dem Samplerregister s0, SparkleNoise dem Samplerregister s1 und k \_ s dem Konstantenregister c0 (vorausgesetzt, es wurden keine anderen Sampler- oder Konstantenregister zugewiesen) für die folgenden drei globalen Variablen zu:


```
sampler Environment;
sampler SparkleNoise;
float4 k_s;
```



Es ist auch möglich, Variablen an ein bestimmtes Register zu binden. Verwenden Sie die folgende Syntax, um zu erzwingen, dass der Compiler einem bestimmten Register zugewiesen wird:


```
register(RegisterName)
```



Dabei ist RegisterName der Name des jeweiligen Registers. Die folgenden Beispiele veranschaulichen die spezielle Registerzuweisungssyntax, bei der die Samplerumgebung an das Samplerregister s1 gebunden wird, SparkleNoise an das Samplerregister s0 und k s an das \_ konstante Register c12 gebunden wird:


```
sampler Environment : register(s1);
sampler SparkleNoise : register(s0);
float4 k_s : register(c12);
```



## <a name="rendering-a-programmable-shader"></a>Rendern eines programmierbaren Shaders

Ein Shader wird gerendert, indem der aktuelle Shader auf dem Gerät festgelegt, die Shaderkonstanten initialisiert, dem Gerät mitgeteilt wird, woher die unterschiedlichen Eingabedaten stammen, und schließlich die Primitiven gerendert werden. Jede dieser Methoden kann durch Aufrufen der folgenden Methoden erreicht werden:

-   [**SetVertexShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader)
-   [**SetVertexShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf)
-   [**SetStreamSource**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource)
-   [**DrawPrimitive**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-drawprimitive)

## <a name="debugging-shaders"></a>Debuggen von Shadern

Die DirectX-Erweiterung für Microsoft Visual Studio .NET bietet einen vollständig integrierten HLSL-Debugger innerhalb der Visual Studio .NET Integrated Development Environment (IDE). Um sich auf das Debuggen von Shadern vorzubereiten, müssen Sie die richtigen Tools auf Ihrem Computer installieren (siehe [Debuggen von Shadern in Visual Studio (Direct3D 9)](dx-graphics-hlsl-debug-visual-studio.md)).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmieranleitung für HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 