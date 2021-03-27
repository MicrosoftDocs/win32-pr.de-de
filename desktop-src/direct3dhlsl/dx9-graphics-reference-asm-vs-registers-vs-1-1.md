---
title: Register-vs_1_1
description: Dieser Abschnitt enthält Referenzinformationen zu den von Vertex Shader Version 1 1 implementierten Eingabe-und Ausgabe Registern \_ .
ms.assetid: 8b19a0da-1561-450f-a36a-35ac7ea6e17a
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e6776fef206f9ced0608e86cbf596585399d4a12
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856579"
---
# <a name="registers---vs_1_1"></a>Register-vs \_ 1 \_ 1

Dieser Abschnitt enthält Referenzinformationen zu den von Vertex Shader Version 1 1 implementierten Eingabe-und Ausgabe Registern \_ .

## <a name="input-registers"></a>Eingabe Register



| Register | Name                                                                                  | Anzahl      | R/W | \# Leseports | \# Lese-/inst- | Dimension  | Reladdr | der Arbeitszeittabelle     | Erfordert DCL |
|----------|---------------------------------------------------------------------------------------|------------|-----|---------------|-----------------|------------|---------|--------------|--------------|
| a0       | [Adress Register](dx9-graphics-reference-asm-vs-registers-address.md)               | 1          | R/W | 1             | Unbegrenzt       | Siehe Hinweis 3 | Nein      | Keine         | Nein           |
| c\#      | [Konstantes float-Register](dx9-graphics-reference-asm-vs-registers-constant-float.md) | Siehe Hinweis 2 | R   | 1             | Unbegrenzt       | 4          | a0. x    | (0, 0, 0, 0) | Nein           |
| Ramelow\#      | [Eingabe Register](dx9-graphics-reference-asm-vs-registers-input.md)                   | 16         | R   | 1             | Unbegrenzt       | 4          | Nein      | Siehe Hinweis 1   | Ja          |
| r\#      | [Temporäres Register](dx9-graphics-reference-asm-vs-registers-temporary.md)           | 12         | R/W | 3             | Unbegrenzt       | 4          | Nein      | Keine         | Nein           |



 

Hinweise:

1.  Partiell (0, 0, 0, 1): Wenn nur eine Teilmenge von Kanälen aktualisiert wird, werden die restlichen Kanäle standardmäßig auf (0, 0, 0, 1) festgelegt.
2.  Gleich D3DCAPS9. Maxvertexshaderconst (mindestens 96 für vs \_ 1 \_ 1).
3.  Es ist nur ein. x-Kanal verfügbar.

## <a name="output-registers"></a>Ausgabe Register



| Register | Name                        | Anzahl | R/W | Dimension | Reladdr | der Arbeitszeittabelle | Erfordert DCL |
|----------|-----------------------------|-------|-----|-----------|---------|----------|--------------|
| OPOS     | Positions Register           | 1     | W   | 4         | Nein      | Keine     | Nein           |
| onebel     | Nebelregister                | 1     | W   | 1         | Nein      | Keine     | Nein           |
| oPts     | Punktgröße registrieren         | 1     | W   | 1         | Nein      | Keine     | Nein           |
| gen\#     | Farb Register; Siehe Hinweis 1  | 2     | W   | 4         | Nein      | Keine     | Nein           |
| TS\#     | Texturkoordinaten Register | 8     | W   | 4         | Nein      | Keine     | Nein           |



 

Hinweise:

-   oD0 ist die Ausgabe der diffusen Farbe. oD1 ist die Glanz Farben Ausgabe.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shader-Register](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




