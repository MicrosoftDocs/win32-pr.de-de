---
title: Flusssteuerung
description: Die meisten Hardwarekomponenten sind dafür ausgelegt, den Shader-Codezeilen Weise auszuführen und jede HLSL-Anweisung einmal auszuführen.
ms.assetid: 94f22e39-8e71-424b-8ca1-bafc843f843f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 70bb7706e520818c86286947acfba6cae0759b4d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309668"
---
# <a name="flow-control"></a>Flusssteuerung

Die meisten Hardwarekomponenten sind dafür ausgelegt, den Shader-Codezeilen Weise auszuführen und jede HLSL-Anweisung einmal auszuführen. Eine Fluss Steuerungs Anweisung bestimmt zur Laufzeit den Block der HLSL-Anweisungen, der als nächstes ausgeführt werden soll. Mithilfe einer Flow-Control-Anweisung kann ein Shader eine Reihe von Anweisungen durchlaufen oder eine Schleife (Verzweigung) in eine andere Anweisung als die in der nächsten Zeile springen. Einige Fluss Steuerungs Anweisungen unterstützen ein statisches Steuerelement, das zum Zeitpunkt der Kompilierung angegeben wird. andere bieten eine Prädikat Kontrolle, bei der es sich um eine pro-Komponente-Entscheidung zur Laufzeit handelt, und andere unterstützen die dynamische Steuerung, die zur Laufzeit basierend auf dem Inhalt einer Variablen getroffen wird.

HLSL unterstützt die folgenden Anweisungen für die Fluss Steuerung.

-   [break](dx-graphics-hlsl-break.md)
-   [continue](dx-graphics-hlsl-continue.md)
-   [Würfen](dx-graphics-hlsl-discard.md)
-   [do](dx-graphics-hlsl-do.md)
-   [for](dx-graphics-hlsl-for.md)
-   [if](dx-graphics-hlsl-if.md)
-   [switch](dx-graphics-hlsl-switch.md)
-   [while](dx-graphics-hlsl-while.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Sprach Syntax (DirectX HLSL)](dx-graphics-hlsl-language-syntax.md)
</dt> </dl>

 

 




