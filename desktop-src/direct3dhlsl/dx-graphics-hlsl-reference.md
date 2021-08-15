---
title: Referenz zu HLSL
description: In der HLSL-Referenzdokumentation werden die Sprachmerkmale angegeben. Sie ist in mehrere Abschnitte unterteilt.
ms.assetid: 1d0e12ff-8559-4e5c-9914-6ed313ea5464
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 425dc1d56801bbbd6b73429d8d17024a78dffe47a045ec6b34d5cd45b752bcca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118513849"
---
# <a name="reference-for-hlsl"></a>Referenz zu HLSL

In der HLSL-Referenzdokumentation werden die Sprachmerkmale angegeben. Sie ist in mehrere Abschnitte unterteilt.

-   [Sprachsyntax (DirectX HLSL):](dx-graphics-hlsl-language-syntax.md) Zum Programmieren von Shadern in HLSL müssen Sie die Sprachsyntax verstehen, d. h. wie Sie HLSL-Code schreiben. Dies umfasst Code zum Deklarieren und Initialisieren von Variablen, zum Schreiben benutzerdefinierter Shaderfunktionen und zum Hinzufügen von Flusssteuerungs-Anweisungen, um Ihre Funktionen leistungsfähiger zu machen.
-   [Shadermodelle im Vergleich zu Shaderprofilen:](dx-graphics-hlsl-models.md) Der HLSL-Compiler implementiert Regeln und Einschränkungen, die auf Shadermodellen basieren. Der Code in jedem Vertex-Shader, Geometrie-Shader (bei Verwendung von Direct3D 10) und Pixel-Shader wird anhand eines Shadermodells überprüft, das Sie zur Kompilierzeit zur Hand haben.
-   [**Systeminterne Funktionen (DirectX HLSL):**](dx-graphics-hlsl-intrinsic-functions.md) HLSL verfügt über viele systeminterne Funktionen. Diese werden implementiert und getestet, damit Sie sie in dem Wissen verwenden können, dass sie bereits gedebuggt sind und eine gute Leistung haben. Wenn Sie ihre eigenen Funktionen schreiben möchten, lesen Sie den Abschnitt zur Sprachsyntax zum Schreiben benutzerdefinierter Funktionen.
-   [Asm-Shaderreferenz:](dx9-graphics-reference-asm.md) Assemblyanweisungen, die Sie zum Programmieren und Debuggen von Shadern verwenden können.
-   [D3DCompiler-Referenz:](dx-graphics-d3dcompiler-reference.md) Kompiliert eine unformatierte HLSL-Quelle.
-   [Inlineformatkonvertierungsreferenz:](inline-format-conversion-reference.md) Die Datei D3DX DXGIFormatConvert.inl enthält Inlineformatkonvertierungsfunktionen, die Sie im Compute-Shader oder Pixel-Shader auf \_ Direct3D 11-Hardware verwenden können. Sie können diese Funktionen in Ihrer Anwendung verwenden, um gleichzeitig aus einer Textur zu lesen und in diese zu schreiben. Das heißt, Sie können die Bildbearbeitung vor Ort durchführen. Um diese Inlineformatkonvertierungsfunktionen zu verwenden, schließen Sie die Datei D3DX \_ DXGIFormatConvert.inl in Ihre Anwendung ein.
-   [Anhang (DirectX HLSL):](dx-graphics-hlsl-appendix.md) Der Anhang ist der Vollständigkeit halber enthalten. Sie enthält eine Liste der Schlüsselwörter und reservierten Wörter. diese Wörter können nicht als Bezeichner in Ihren Programmen verwendet werden. Sie enthält auch eine Liste der Sprachgrammatik als Referenz.
-   [**HLSL errors and warnings (HLSL-Fehler und -Warnungen)**](hlsl-errors-and-warnings.md) – Stellt Fehler- und Warnungscodes fest, die ein Shader zurückgeben kann.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Hlsl](dx-graphics-hlsl.md)
</dt> <dt>

[Programmieranleitung für HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 




