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
ms.openlocfilehash: 6455b47d24c1c83683ce8b85c48990bb32e221ae
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993359"
---
# <a name="using-shaders-in-direct3d-9"></a>Verwenden von Shadern in Direct3D 9

-   [Kompilieren eines Shaders für bestimmte Hardware](#compiling-a-shader-for-specific-hardware)
-   [Initialisieren von shaderkonstanten](#initializing-shader-constants)
-   [Binden eines shaderparameters an ein bestimmtes Register](#binding-a-shader-parameter-to-a-particular-register)
-   [Rendern eines programmierbaren Shaders](#rendering-a-programmable-shader)
-   [Shader Debuggen](#debugging-shaders)
-   [Zugehörige Themen](#related-topics)

## <a name="compiling-a-shader-for-specific-hardware"></a>Kompilieren eines Shaders für bestimmte Hardware

Shader wurden zuerst zu Microsoft DirectX in DirectX 8,0 hinzugefügt. Zu diesem Zeitpunkt wurden mehrere virtuelle shadercomputer definiert, von denen jede ungefähr einem bestimmten Grafikprozessor entspricht, der von den ersten 3D-Grafik Anbietern erzeugt wurde. Für jeden dieser virtuellen Shader-Computer wurde eine Assemblysprache entworfen. In Shader-Modellen geschriebene Programme (Namen im Vergleich zu \_ 1 \_ 1 und PS \_ 1 \_ 1-PS \_ 1 \_ 4) waren relativ kurz und wurden in der Regel von Entwicklern direkt in die entsprechende Assemblysprache geschrieben. Die Anwendung würde diesen lesbaren assemblysprachencode mithilfe von [**D3DXAssembleShader**](/windows/desktop/direct3d9/d3dxassembleshader) an die D3DX-Bibliothek übergeben und eine binäre Darstellung des Shaders zurückerhalten, der wiederum mithilfe von " [**kreatevertexshader**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createvertexshader) " oder " [**kreatepixelshader**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createpixelshader)" übergeben würde. Weitere Informationen finden Sie unter Software Development Kit (SDK).

Die Situation in Direct3D 9 ist ähnlich. Eine Anwendung übergibt mithilfe von [**D3DXCompileShader**](/windows/desktop/direct3d9/d3dxcompileshader) einen HLSL-Shader an D3DX und ruft eine binäre Darstellung des kompilierten Shaders ab, der [**wiederum mithilfe von**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createpixelshader) "" von "" von "", "", "", "", "", " [**" und "**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createvertexshader)" von "" in Die Laufzeit weiß nichts über HLSL, sondern nur über die binären assemblyshader-Modelle. Dies ist nützlich, da es bedeutet, dass der HLSL-Compiler unabhängig von der Direct3D-Laufzeit aktualisiert werden kann. Sie können Shader auch offline mithilfe von [FXC](/windows/desktop/direct3dtools/fxc)kompilieren.

Zusätzlich zur Entwicklung des HLSL-Compilers wurden in Direct3D 9 auch die Shader-Modelle auf Assemblyebene eingeführt, um die Funktionalität der neuesten Generation von Grafikhardware verfügbar zu machen. Anwendungsentwickler können für diese neuen Modelle in der Assembly arbeiten (vs \_ 2 \_ 0, vs \_ 3 \_ 0, PS \_ 2 \_ 0, PS \_ 3 \_ 0), aber wir erwarten, dass die meisten Entwickler zu HLSL for Shader Development wechseln.

Natürlich kann die Möglichkeit, ein HLSL-Programm zu schreiben, um einen bestimmten Schattierungs Algorithmus auszudrücken, nicht automatisch auf einer bestimmten Hardware ausgeführt werden. Eine Anwendung ruft D3DX auf, um einen Shader in binären Assemblycode mit [**D3DXCompileShader**](/windows/desktop/direct3d9/d3dxcompileshader)zu kompilieren. Eine der Einschränkungen bei diesem Einstiegspunkt ist ein Parameter, der definiert, welche der Modelle auf Assemblyebene (oder Kompilierungs Ziele) der HLSL-Compiler zum Ausdrücken des abschließenden shadercodes verwenden soll. Wenn eine Anwendung die HLSL-Shader-Kompilierung zur Laufzeit (im Gegensatz zur Kompilierzeit oder offline) durchführt, kann die Anwendung die Funktionen des Direct3D-Geräts untersuchen und das zu suchende Kompilierungs Ziel auswählen. Wenn der im HLSL-Shader ausgedrückte Algorithmus zu komplex ist, um auf dem ausgewählten Kompilierungs Ziel ausgeführt zu werden, schlägt die Kompilierung fehl. Dies bedeutet, dass es sich bei HLSL um einen großen Vorteil bei der Shader-Entwicklung handelt, aber nicht für Entwickler, die mit Grafik Geräten unterschiedlicher Funktionen an eine Zielgruppe ausgeliefert werden. Als Spielentwickler müssen Sie immer noch einen mehrstufigen Ansatz für Ihre visuellen Elemente verwalten. Dies bedeutet, dass Sie bessere Shader für leistungsfähigere Grafikkarten schreiben und weitere grundlegende Versionen für ältere Karten schreiben können. Wenn Sie HLSL gut geschrieben haben, kann diese Belastung jedoch erheblich gelockert werden.

Anstatt HLSL-Shader mithilfe von D3DX auf dem Computer des Kunden zur Ladezeit der Anwendung oder bei der ersten Verwendung zu kompilieren, haben viele Entwickler die Möglichkeit, ihren Shader aus HLSL in binären Assemblycode zu kompilieren, bevor Sie überhaupt ausgeliefert werden. Dadurch bleibt der HLSL-Quellcode nicht mehr auf dem Weg, sondern es wird auch sichergestellt, dass alle Shader, die Ihre Anwendung ausführen wird, den internen Qualitätssicherungsprozess durchlaufen haben. Ein nützliches Hilfsprogramm für die Offline Kompilierung von Shadern ist [FXC](/windows/desktop/direct3dtools/fxc). Dieses Tool verfügt über eine Reihe von Optionen, die Sie verwenden können, um Code für das angegebene Kompilierungs Ziel zu kompilieren. Das Untersuchen der disassemblierten Ausgabe kann während der Entwicklung sehr lehrbar sein, wenn Sie Ihre Shader optimieren möchten, oder die Funktionen des virtuellen shadercomputers in der Regel ausführlicher kennenlernen. Diese Optionen werden im folgenden zusammengefasst:

## <a name="initializing-shader-constants"></a>Initialisieren von shaderkonstanten

Shaderkonstanten sind in der Konstanten Tabelle enthalten. Auf diesen kann mit der [**ID3DXConstantTable**](/windows/desktop/direct3d9/id3dxconstanttable) -Schnittstelle zugegriffen werden. Globale shadervariablen können im Shader-Code initialisiert werden. Diese werden zur Laufzeit initialisiert, indem [**SetDefaults**](/windows/desktop/direct3d9/id3dxconstanttable--setdefaults)aufgerufen wird.

## <a name="binding-a-shader-parameter-to-a-particular-register"></a>Binden eines shaderparameters an ein bestimmtes Register

Der Compiler weist automatisch Registern globalen Variablen zu. Der Compiler würde die Umgebung dem samplingregister S0, sparklenoise, dem samplingregister S1 und k \_ s in konstanter Register C0 zuweisen (vorausgesetzt, dass keine anderen Sampler oder Konstanten Register bereits zugewiesen wurden) für die folgenden drei globalen Variablen:


```
sampler Environment;
sampler SparkleNoise;
float4 k_s;
```



Es ist auch möglich, Variablen an ein bestimmtes Register zu binden. Verwenden Sie die folgende Syntax, um zu erzwingen, dass der Compiler einem bestimmten Register zugewiesen wird:


```
register(RegisterName)
```



Where Register Name ist der Name des jeweiligen Registers. Die folgenden Beispiele veranschaulichen die spezifische Register Zuweisungs Syntax, bei der die samplingumgebung an das samplingregister S1 gebunden wird, sparklenoise an das samplenregister S0 gebunden wird und k \_ s an den konstanten Registrierungs-C12 gebunden ist:


```
sampler Environment : register(s1);
sampler SparkleNoise : register(s0);
float4 k_s : register(c12);
```



## <a name="rendering-a-programmable-shader"></a>Rendern eines programmierbaren Shaders

Ein Shader wird gerendert, indem der aktuelle Shader auf dem Gerät festgelegt wird, die shaderkonstanten initialisiert werden und das Gerät, von dem die unterschiedlichen Eingabedaten stammen, und schließlich die primitiven gerendert werden. Diese können durch Aufrufen der folgenden Methoden erreicht werden:

-   [**Setvertexshader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader)
-   [**Setvertexshaderconstantf**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf)
-   [**SetStreamSource**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource)
-   [**Drawprimitiv**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-drawprimitive)

## <a name="debugging-shaders"></a>Shader Debuggen

Die DirectX-Erweiterung für Microsoft Visual Studio .net ist ein vollständig integrierter HLSL-Debugger in der integrierten Entwicklungsumgebung (Integrated Development Environment, IDE) von Visual Studio. Um das Debuggen von Shader vorzubereiten, müssen Sie die richtigen Tools auf Ihrem Computer installieren (siehe [Debuggen von Shadern in Visual Studio (Direct3D 9)](dx-graphics-hlsl-debug-visual-studio.md)).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmieranleitung für HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 