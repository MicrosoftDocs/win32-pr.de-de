---
title: Signierte Skalierung des Quellregisters
description: Subtrahiert 0,5 von jedem Kanal und skaliert das Ergebnis um 2,0. Der Name bx2 stammt aus bias und scale-times-two. Dies ist der Vorgang, der durchgeführt wird.
ms.assetid: ad94145a-2687-4c20-b3ed-70270a0c53bf
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 161cacbf9f10a36e65f37816970aea5d5d804096151a4ae1ce3f814be918ae08
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854600"
---
# <a name="source-register-signed-scaling"></a>Signierte Skalierung des Quellregisters

Subtrahiert 0,5 von jedem Kanal und skaliert das Ergebnis um 2,0. Der Name bx2 stammt aus bias und scale-times-two. Dies ist der Vorgang, der durchgeführt wird.

## <a name="syntax"></a>Syntax


```
source register_bx2
```



## <a name="register"></a>Registrieren

Quellregister. Weitere Informationen zu Registertypen finden Sie unter [ps \_ 1 \_ 1 \_ \_ ps \_ 1 \_ 2 ps \_ \_ \_ 1 \_ 3 ps \_ \_ \_ 1 \_ 4 Register.](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)

## <a name="remarks"></a>Hinweise

Dieser Vorgang wird häufig verwendet, um Daten von \[ 0.0 auf 1.0 auf \] \[ -1.0 auf 1.0 zu \] erweitern. Dieser Modifizierer ist für die Verwendung mit arithmetischen Anweisungen konzipiert. Dieser Modifizierer wird häufig für Eingaben in die dot product-Anweisung ([dp3 - ps ) verwendet.](dp3---ps.md) Die \_ Verwendung von bx2 für Daten außerhalb des Bereichs von 0 bis 1 kann zu undefinierten Ergebnissen führen.

Der signierte Skalierungsvorgang wird auf die aus dem Register gelesenen Daten angewendet, bevor die nächste Anweisung ausgeführt wird. Der Vorgang wird wie folgt auf alle vier Farbkanäle (RGBA) angewendet:


```
y = 2(x - 0.5)
```



Der Inhalt des Registers wird nicht geändert. Der -Modifizierer wird nur auf die aus dem Register gelesenen Daten angewendet.

Dieser Modifizierer schließen sich mit [Source Register Invert](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md) gegenseitig aus, sodass er nicht auf dasselbe Register angewendet werden kann.

Versionsinformationen:

-   Für ps 1 0 und ps 1 1 können Sie bx2 in jedem Quellregister für Texturanweisungen der Form \_ \_ \_ \_ \_ texm3x2 und \* texm3x3 \* verwenden. \_bx2 kann nicht für eine der anderen Texturanweisungen wie [texreg2ar – ps](texreg2ar---ps.md) oder [texreg2gb – ps – verwendet werden.](texreg2gb---ps.md)
-   Für ps 1 2 und ps 1 3 können Sie bx2 in jedem Quellregister für jede tex-Anweisung verwenden, \_ \_ \_ \_ \_ \* außer: [texreg2ar - ps](texreg2ar---ps.md), [texreg2gb - ps](texreg2gb---ps.md), [texbem - ps](texbem---ps.md) oder [texbeml - ps](texbeml---ps.md).

## <a name="example"></a>Beispiel

In diesem Beispiel wird eine Textur entnommen, Daten in den Bereich von -1 bis +1 konvertiert und ein Punktprodukt berechnet.


```
tex t0                        ; Read a texture color.
dp3_sat r0, t0_bx2, v0_bx2    ; Calculate a dot product.
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Modifizierer für Das Pixel-Shader-Quellregister](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




