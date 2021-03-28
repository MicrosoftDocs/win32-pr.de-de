---
title: Verweis für HLSL
description: In der HLSL-Referenz Dokumentation werden die Sprachmerkmale angegeben. Es ist in mehrere Abschnitte unterteilt.
ms.assetid: 1d0e12ff-8559-4e5c-9914-6ed313ea5464
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ce0bb59dd26bd8bb9723bcdff23bbc79ee810253
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037349"
---
# <a name="reference-for-hlsl"></a>Verweis für HLSL

In der HLSL-Referenz Dokumentation werden die Sprachmerkmale angegeben. Es ist in mehrere Abschnitte unterteilt.

-   [Sprachsyntax (DirectX HLSL)](dx-graphics-hlsl-language-syntax.md) : das Programmieren von Shadern in HLSL erfordert, dass Sie die Sprachsyntax verstehen, d. h. wie Sie HLSL-Code schreiben. Dies umfasst Code zum Deklarieren und Initialisieren von Variablen, Schreiben benutzerdefinierter Shaderfunktionen und Hinzufügen von flowsteuerungsanweisungen, damit ihre Funktionen leistungsfähiger werden.
-   [Shader-Modelle vs shaderprofile](dx-graphics-hlsl-models.md) : der HLSL-Compiler implementiert Regeln und Einschränkungen basierend auf shadermodellen. Der Code in jedem Vertex-Shader, Geometry-Shader (bei Verwendung von Direct3D 10) und PixelShader werden anhand eines shadermodells überprüft, das Sie zum Zeitpunkt der Kompilierung angeben.
-   [**Intrinsische Funktionen (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md) : HLSL verfügt über viele intrinsische Funktionen. Diese werden implementiert und getestet, damit Sie Sie verwenden können, um Sie zu überprüfen, dass Sie bereits gedeentschlallte und gut funktionieren. Wenn Sie eigene Funktionen schreiben möchten, lesen Sie den Abschnitt Sprachsyntax zum Schreiben von benutzerdefinierten Funktionen.
-   [ASM-Shader](dx9-graphics-reference-asm.md) -verweisassemblyanweisungen, mit denen Sie Shader programmieren und Debuggen können.
-   [D3DCompiler Reference](dx-graphics-d3dcompiler-reference.md) : kompiliert eine Rohdaten-HLSL-Quelle.
-   [Referenz zur Inline-Formatkonvertierung](inline-format-conversion-reference.md) : die D3DX \_ dxgiformatconvert. INL-Datei enthält Funktionen für Inline Formatkonvertierungen, die Sie im COMPUTE-Shader oder Pixel-Shader auf Direct3D 11-Hardware verwenden können. Sie können diese Funktionen in der Anwendung verwenden, um gleichzeitig Lese-und Schreibvorgänge für eine Textur auszuführen. Das heißt, Sie können eine direkte Bildbearbeitung ausführen. Um diese Funktionen für die Inline Formatkonvertierung zu verwenden, schließen \_ Sie die Datei D3DX dxgiformatconvert. INL in Ihre Anwendung ein.
-   [Anhang (DirectX HLSL)](dx-graphics-hlsl-appendix.md) : der Anhang ist aus Gründen der Vollständigkeit enthalten. Sie enthält eine Liste der Schlüsselwörter und reservierten Wörter. Diese Wörter können nicht als Bezeichner in ihren Programmen verwendet werden. Außerdem enthält Sie eine Auflistung der Sprachgrammatik für den Verweis.
-   [**HLSL-Fehler und-Warnungen**](hlsl-errors-and-warnings.md) : gibt Fehler-und Warn Codes an, die ein Shader zurückgeben kann.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[HLSL](dx-graphics-hlsl.md)
</dt> <dt>

[Programmieranleitung für HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 




