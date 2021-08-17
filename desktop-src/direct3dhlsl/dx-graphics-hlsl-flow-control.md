---
title: Flusssteuerung
description: Die meisten Hardwarekomponenten sind so konzipiert, dass Shadercode Zeile für Zeile ausgeführt wird, und jede HLSL-Anweisung wird einmal ausgeführt.
ms.assetid: 94f22e39-8e71-424b-8ca1-bafc843f843f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4aebaf63613aeb3a1d14607971db16602745883ab6b7b9db4723dfa2367f9bd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120284"
---
# <a name="flow-control"></a>Flusssteuerung

Die meisten Hardwarekomponenten sind so konzipiert, dass Shadercode Zeile für Zeile ausgeführt wird, und jede HLSL-Anweisung wird einmal ausgeführt. Eine Flow-Control-Anweisung bestimmt zur Laufzeit, welcher Block von HLSL-Anweisungen als Nächstes ausgeführt werden soll. Mithilfe einer Flow-Control-Anweisung kann ein Shader eine Schleife durch eine Reihe von Anweisungen oder zu einer anderen Anweisung als der anweisung in der nächsten Zeile springen (Verzweigung). Einige Flow-Control-Anweisungen unterstützen statische Steuerungen, die zur Kompilierzeit angegeben werden. Andere bieten eine prädikatierte Steuerung, die eine Komponentenentscheidung zur Laufzeit ist, und wieder andere unterstützen dynamische Steuerung, die zur Laufzeit basierend auf dem Inhalt einer Variablen getroffen wird.

HLSL unterstützt die folgenden Flusssteuerungs-Anweisungen.

-   [break](dx-graphics-hlsl-break.md)
-   [continue](dx-graphics-hlsl-continue.md)
-   [Verwerfen](dx-graphics-hlsl-discard.md)
-   [do](dx-graphics-hlsl-do.md)
-   [for](dx-graphics-hlsl-for.md)
-   [if](dx-graphics-hlsl-if.md)
-   [switch](dx-graphics-hlsl-switch.md)
-   [while](dx-graphics-hlsl-while.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Sprachsyntax (DirectX HLSL)](dx-graphics-hlsl-language-syntax.md)
</dt> </dl>

 

 




