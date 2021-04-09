---
title: /WX-Schalter
description: Der/WX-Schalter weist den Mittelwert Compiler an, alle Fehler auf der angegebenen Warnstufe als Fehler zu behandeln.
ms.assetid: 1dd9791c-0488-4ca3-8a29-082ae03c3cd4
keywords:
- /WX-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /WX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04b502cea5f686de2951f6f21ab92fdbffef779b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857503"
---
# <a name="wx-switch"></a>/WX-Schalter

Der **/WX** -Schalter weist den Mittelwert Compiler an, alle Fehler auf der angegebenen Warnstufe als Fehler zu behandeln.

``` syntax
midl /WX
```

## <a name="switch-options"></a>Optionen wechseln

Dieser Switch hat keine Parameter.

## <a name="remarks"></a>Bemerkungen

Wenn der Schalter **/WX** angegeben wird und der Schalter [**/W**](-w.md)*n* nicht angegeben ist, werden alle Warnungen auf der Standard Ebene Ebene 1 als Fehler behandelt.

Der Schalter [**/W**](-w.md)*n* weist den Compiler an, alle Warnungen auf der Ebene *n* anzuzeigen, und **/WX** weist den Compiler an, alle Warnungen als Fehler zu behandeln. Die Kombination dieser beiden Switches bewirkt, dass der Compiler alle Warnungen auf Ebene *n* als Fehler behandelt.

Fehler unterscheiden sich von Warnungen. Fehler bewirken, dass der Mittell-Compiler die Verarbeitung der IDL-Datei stoppt. Warnungen bewirken, dass der Mittell-Compiler eine Informations Meldung ausgibt und die Verarbeitung der IDL-Datei fortsetzt.

Warning-Level NULL (0) weist den Mittelwert Compiler an, Warn Informationen zu unterdrücken. Wenn die Schalter **/W0** und **/WX** kombiniert werden, unterdrückt der kompil-Compiler alle Warn Informationen. In diesem Fall hat der Schalter **/WX** keine Auswirkung.

## <a name="examples"></a>Beispiele

**Mittel l/WX Dateiname. idl**

**Mittel l/w3/WX filename. idl**

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Allgemeine Syntax der Mittell-Befehlszeile](general-midl-command-line-syntax.md)
</dt> <dt>

[**/W**](-w.md)
</dt> </dl>

 

 




