---
title: Quell Registrierung mit signierter Skalierung
description: Subtrahiert 0,5 von jedem Kanal und skaliert das Ergebnis um 2,0. Der Name bx2 stammt von "Bias" und "Scale-Time-Two", bei dem es sich um den ausgeführten Vorgang handelt.
ms.assetid: ad94145a-2687-4c20-b3ed-70270a0c53bf
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 214f4fcb6ad4f382a97b8c8d75a733124c31d68a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207448"
---
# <a name="source-register-signed-scaling"></a>Quell Registrierung mit signierter Skalierung

Subtrahiert 0,5 von jedem Kanal und skaliert das Ergebnis um 2,0. Der Name bx2 stammt von "Bias" und "Scale-Time-Two", bei dem es sich um den ausgeführten Vorgang handelt.

## <a name="syntax"></a>Syntax


```
source register_bx2
```



## <a name="register"></a>Register

Quell Register. Weitere Informationen zu Register Typen finden Sie unter [PS \_ 1 1 PS 1 \_ \_ \_ \_ \_ 2 \_ \_ PS \_ 1 \_ 3 \_ \_ PS \_ 1 \_ 4 Registern](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).

## <a name="remarks"></a>Bemerkungen

Dieser Vorgang wird häufig zum Erweitern von Daten zwischen \[ 0,0 und 1,0 \] auf \[ -1,0 bis 1,0 verwendet \] . Dieser Modifizierer ist für die Verwendung mit arithmetischen Anweisungen konzipiert. Dieser Modifizierer wird häufig bei Eingaben für die dot-Produkt Anweisung ([DP3-PS](dp3---ps.md)) verwendet. \_Die Verwendung von bx2 für Daten außerhalb des Bereichs 0 bis 1 kann zu undefinierten Ergebnissen führen.

Der Vorgang für die signierte Skalierung wird auf die aus dem Register gelesenen Daten angewendet, bevor die nächste Anweisung ausgeführt wird. Der Vorgang wird wie folgt auf alle vier Farbkanäle (RGBA) angewendet:


```
y = 2(x - 0.5)
```



Der Inhalt des Registers wird nicht geändert. Der-Modifizierer wird nur auf die aus dem Register gelesenen Daten angewendet.

Dieser Modifizierer schließt sich mit dem [Quell Register Invert](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md) gegenseitig aus, sodass er nicht auf dasselbe Register angewendet werden kann.

Versionsinformationen:

-   Für PS \_ 1 \_ 0 und PS \_ 1 \_ 1 können Sie \_ bx2 für ein beliebiges Quell Register für Textur Anweisungen im Format texm3x2 \* und texm3x3 verwenden \* . \_bx2 kann nicht für eine der anderen Textur Anweisungen wie [texreg2ar-PS](texreg2ar---ps.md) oder [texreg2gb-PS](texreg2gb---ps.md)verwendet werden.
-   Für PS \_ 1 \_ 2 und PS \_ 1 \_ 3 können Sie \_ bx2 für beliebige Quell Register für jede beliebige tex- \* Anweisung mit Ausnahme von: [texreg2ar-PS](texreg2ar---ps.md), [texreg2gb-PS](texreg2gb---ps.md), [texbem-PS](texbem---ps.md) oder [texbeml-PS](texbeml---ps.md)verwenden.

## <a name="example"></a>Beispiel

Dieses Beispiel veranschaulicht eine Textur, konvertiert Daten in den Bereich von-1 bis + 1 und berechnet ein Punktprodukt.


```
tex t0                        ; Read a texture color.
dp3_sat r0, t0_bx2, v0_bx2    ; Calculate a dot product.
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixel-Shader-quellregistrierungs Modifizierern](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




