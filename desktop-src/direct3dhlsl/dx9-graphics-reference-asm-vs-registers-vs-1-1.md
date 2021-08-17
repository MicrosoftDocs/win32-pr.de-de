---
title: Register – vs_1_1
description: Dieser Abschnitt enthält Referenzinformationen zu den Eingabe- und Ausgaberegistern, die von Vertex-Shader Version 1 1 \_ implementiert werden.
ms.assetid: 8b19a0da-1561-450f-a36a-35ac7ea6e17a
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4bcfadae2b1dca70298ffed188de2e6075892563b27bf6f624f2139e441600cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117908004"
---
# <a name="registers---vs_1_1"></a>Register im Vergleich zu \_ 1 \_ 1

Dieser Abschnitt enthält Referenzinformationen zu den Eingabe- und Ausgaberegistern, die von Vertex-Shader Version 1 1 \_ implementiert werden.

## <a name="input-registers"></a>Eingaberegister



| Registrieren | Name                                                                                  | Anzahl      | R/W | \# Lesen von Ports | \# Reads/inst | Dimension  | RelAddr | Standardeinstellungen     | Erfordert DCL |
|----------|---------------------------------------------------------------------------------------|------------|-----|---------------|-----------------|------------|---------|--------------|--------------|
| a0       | [Adressregister](dx9-graphics-reference-asm-vs-registers-address.md)               | 1          | R/W | 1             | Unbegrenzt       | Siehe Hinweis 3 | Nein      | Keine         | Nein           |
| c\#      | [Constant Float Register](dx9-graphics-reference-asm-vs-registers-constant-float.md) | Siehe Hinweis 2 | R   | 1             | Unbegrenzt       | 4          | a0.x    | (0, 0, 0, 0) | Nein           |
| V\#      | [Eingaberegister](dx9-graphics-reference-asm-vs-registers-input.md)                   | 16         | R   | 1             | Unbegrenzt       | 4          | Nein      | Siehe Hinweis 1   | Ja          |
| R\#      | [Temporäres Register](dx9-graphics-reference-asm-vs-registers-temporary.md)           | 12         | R/W | 3             | Unbegrenzt       | 4          | Nein      | Keine         | Nein           |



 

Hinweise:

1.  Partiell (0, 0, 0, 1): Wenn nur eine Teilmenge der Kanäle aktualisiert wird, werden die verbleibenden Kanäle standardmäßig auf (0, 0, 0, 1) festgelegt.
2.  Entspricht D3DCAPS9. MaxVertexShaderConst (mindestens 96 für im Vergleich \_ zu 1 \_ 1).
3.  Nur der X-Kanal ist verfügbar.

## <a name="output-registers"></a>Ausgaberegister



| Registrieren | Name                        | Anzahl | R/W | Dimension | RelAddr | Standardeinstellungen | Erfordert DCL |
|----------|-----------------------------|-------|-----|-----------|---------|----------|--------------|
| Opos     | Positionsregister           | 1     | W   | 4         | Nein      | Keine     | Nein           |
| oFog     | Fog Register                | 1     | W   | 1         | Nein      | Keine     | Nein           |
| Setzt     | Punktgrößenregister         | 1     | W   | 1         | Nein      | Keine     | Nein           |
| Od\#     | Farbregister; Siehe Hinweis 1  | 2     | W   | 4         | Nein      | Keine     | Nein           |
| Ot\#     | Texturkoordinatenregister | 8     | W   | 4         | Nein      | Keine     | Nein           |



 

Hinweise:

-   oD0 ist die Ausgabe der diffusen Farbe. oD1 ist die Ausgabe der Glanzfarbe.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shaderregister](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




