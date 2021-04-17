---
title: Kompilieren von Shadern
description: Sehen wir uns nun verschiedene Möglichkeiten zum Kompilieren Ihres shadercodes und Konventionen für Dateierweiterungen für Shader-Code an.
ms.assetid: a4e6b7cd-c5cc-4165-ba73-205155e449c9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3ea71da99dd68769324b07d3fc76a0c5ca00009d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315525"
---
# <a name="compiling-shaders"></a>Kompilieren von Shadern

> [!NOTE]
> In diesem Thema wird der Compiler behandelt, der `FXC.EXE` für Shader-Modelle 2 bis 5,1 verwendet wird. Für Shader Model 6 verwenden Sie `DXC.EXE` stattdessen, das unter [Verwenden von dxc.exe und dxcompiler.dll](https://github.com/microsoft/DirectXShaderCompiler/wiki/Using-dxc.exe-and-dxcompiler.dll)dokumentiert ist.

Microsoft Visual Studio 2012 kann nun Shader-Code aus \* . HLSL-Dateien kompilieren, die Sie in das C++-Projekt einschließen.

Im Rahmen des Buildprozesses verwendet Visual Studio 2012 den [fxc.exe](/windows/desktop/direct3dtools/fxc) HLSL-Code Compiler zum Kompilieren der HLSL-Dateien in binäre shaderobjektdateien oder in Byte Arrays, die in Header Dateien definiert sind. Wie der HLSL-Code Compiler jede HLSL-Datei in Ihrem Projekt kompiliert, hängt davon ab, wie Sie die **Ouput files** -Eigenschaft für diese Datei angeben. Weitere Informationen zu Eigenschaften Seiten von HLSL finden Sie unter [HLSL-Eigenschaften Seiten](/previous-versions/visualstudio/visual-studio-2012/jj620902(v=vs.110)).

Die Kompilierungs Methode, die Sie verwenden, hängt in der Regel von der Größe Ihrer \* HLSL-Datei ab. Wenn Sie eine große Menge an Bytecode in einen Header einschließen, erhöhen Sie die Größe und die anfängliche Ladezeit Ihrer APP. Außerdem erzwingen Sie, dass sämtlicher Bytecode auch nach der Erstellung des Shaders im Speicher gespeichert wird, wodurch Ressourcen verschwendet werden. Wenn Sie jedoch Bytecode in einen Header einschließen, können Sie die Codekomplexität verringern und die Shader-Erstellung vereinfachen.

Sehen wir uns nun verschiedene Möglichkeiten zum Kompilieren Ihres shadercodes und Konventionen für Dateierweiterungen für Shader-Code an.

-   [Verwenden von Shader-Code Dateierweiterungen](#using-shader-code-file-extensions)
-   [Kompilieren bei Buildzeit in Objektdateien](#compiling-at-build-time-to-object-files)
-   [Kompilieren bei Buildzeit in Header Dateien](#compiling-at-build-time-to-header-files)
-   [Kompilieren mit D3DCompileFromFile](#compiling-with-d3dcompilefromfile)
-   [Verwandte Themen](#related-topics)
-   [Zugehörige Themen](#related-topics)

## <a name="using-shader-code-file-extensions"></a>Verwenden von Shader-Code Dateierweiterungen

Um die Microsoft-Konvention einzuhalten, verwenden Sie diese Dateierweiterungen für den Shader-Code:

-   Eine Datei mit der Erweiterung. HLSL enthält einen[HLSL](dx-graphics-hlsl-reference.md)-Quellcode (High Level Shading Language).
-   Eine Datei mit der Erweiterung. CSO enthält ein kompiliertes Shader-Objekt.
-   Eine Datei mit der Erweiterung ". h" ist eine Header Datei, aber in einem Shader-Code Kontext definiert diese Header Datei ein Bytearray, das Shader-Daten enthält.

## <a name="compiling-at-build-time-to-object-files"></a>Kompilieren bei Buildzeit in Objektdateien

Wenn Sie die HLSL-Dateien in binäre shaderobjektdateien kompilieren, muss Ihre APP die Daten aus diesen Objektdateien lesen (. CSO ist die Standard Erweiterung für diese Objektdateien), die Daten Byte Arrays zuweisen und aus diesen Byte Arrays Shader-Objekte erstellen. Um z. b. einen Vertex-Shader ([**ID3D11VertexShader**](/windows/desktop/api/d3d11/nn-d3d11-id3d11vertexshader)) zu erstellen \* \* , rufen Sie die [**ID3D11Device:: kreatevertexshader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createvertexshader) -Methode mit einem Bytearray auf, das kompilierten Vertex-Shader-Bytecode enthält. Das [Direct3D Tutorial-Beispiel](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample) veranschaulicht, wie shaderobjekte aus Byte Arrays erstellt werden, die von CSO-Binär-shaderobjektdateien abgerufen wurden. In diesem Beispielcode aus dem [Direct3D-tutorialbeispiel](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)gibt die **Ouput files** -Eigenschaft für die simplevertexshader. HLSL-Datei an, dass in die simplevertexshader. CSO-Objektdatei kompiliert werden soll.

```cpp
        auto vertexShaderBytecode = reader->ReadData("SimpleVertexShader.cso");
        ComPtr<ID3D11VertexShader> vertexShader;
        DX::ThrowIfFailed(
            m_d3dDevice->CreateVertexShader(
                vertexShaderBytecode->Data,
                vertexShaderBytecode->Length,
                nullptr,
                &vertexShader
                )
```

## <a name="compiling-at-build-time-to-header-files"></a>Kompilieren bei Buildzeit in Header Dateien

Wenn Sie die HLSL-Dateien in Byte Arrays kompilieren, die in Header Dateien definiert sind, müssen Sie diese Header Dateien in Ihren Code einschließen. Das [Beispiel für Medien Erweiterungen](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Media%20extensions%20sample) veranschaulicht das Erstellen von shaderobjekten aus Byte Arrays, die in Header Dateien definiert sind und die Sie zum Zeitpunkt der Kompilierung in das Projekt einschließen. In diesem Beispielcode aus dem Beispiel für [Medien Erweiterungen](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Media%20extensions%20sample)gibt die **Ouput files** -Eigenschaft für die PixelShader. HLSL-Datei an, dass die Kompilierung in das *g \_ psshader* -Bytearray erfolgt, das in der Header Datei "Pixelshader. h" definiert ist.


```C++
#       include "PixelShader.h"
        ComPtr<ID3D11PixelShader> m_pPixelShader;
        hr = pDevice->CreatePixelShader(g_psshader, sizeof(g_psshader), nullptr, &m_pPixelShader);
```



## <a name="compiling-with-d3dcompilefromfile"></a>Kompilieren mit D3DCompileFromFile

Sie können auch die [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile) -Funktion zur Laufzeit verwenden, um Shader-Code zu kompilieren. Weitere Informationen hierzu finden Sie unter Gewusst [wie: Kompilieren eines Shaders](/windows/desktop/direct3d11/how-to--compile-a-shader).

> [!Note]  
> Windows Store-Apps unterstützen [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile) für die Entwicklung, aber nicht für die Bereitstellung.

 

## <a name="related-topics"></a>Verwandte Themen

[Programmieranleitung für HLSL](dx-graphics-hlsl-pguide.md)


## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmieranleitung für HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 