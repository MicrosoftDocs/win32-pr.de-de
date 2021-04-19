---
title: /W-Schalter
description: Der/W-Schalter gibt die Warnstufe des Mittell-Compilers an. Die Warnstufe zeigt den Schweregrad der Warnung an.
ms.assetid: ee894d73-cbd1-455f-9836-a6d80cfc95f9
keywords:
- /W-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /W
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00b1f15ae0c28722adaca8c4b0651606681ce3af
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106338420"
---
# <a name="w-switch"></a>/W-Schalter

Der **/W** -Schalter gibt die Warnstufe des Mittell-Compilers an. Die Warnstufe zeigt den Schweregrad der Warnung an.

``` syntax
midl /W level
```

## <a name="switch-options"></a>Optionen wechseln

<dl> <dt>

*level* 
</dt> <dd>

Gibt die Warnstufe an, eine ganze Zahl im Bereich von 0 bis 4. Zwischen dem Schalter **/W** und der Ziffer, die den Wert für die Warnstufe angibt, besteht kein Leerzeichen.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Warnungs Stufen liegen zwischen 1 und 4. der Wert 0 bedeutet, dass keine Warn Informationen angezeigt werden. Die Warnung mit dem höchsten Schweregrad ist Ebene 1. In der folgenden Tabelle werden die Warnungen für die einzelnen Warn Stufen beschrieben.



| Warnstufe | BESCHREIBUNG                                             | Beispiel                                                                   |
|---------------|---------------------------------------------------------|---------------------------------------------------------------------------|
| W0            | Keine Warnungen.                                            |                                                                           |
| W1            | Schwerwiegende Warnungen, die zu Anwendungsfehlern führen können.      | Es wurde kein Bindungs handle angegeben, nicht attributierte Zeiger, widersprüchliche Switches. |
| W2            | Kann zu Problemen in der Betriebsumgebung des Benutzers führen. | Die Bezeichnerlänge überschreitet 31 Zeichen. Es wurde kein Standard-Union-Arm angegeben.  |
| W3            | Reserviert.                                               |                                                                           |
| W4            | Niedrigste Warnstufe.                                   | Nicht-ANSI-C-Konstrukte.                                                    |



 

Warnungen unterscheiden sich von Fehlern. Fehler bewirken, dass der Mittell-Compiler die Verarbeitung der IDL-Datei stoppt. Warnungen bewirken, dass der Mittell-Compiler eine Informations Meldung ausgibt und die Verarbeitung der IDL-Datei fortsetzt.

Die vom **/W** -Schalter festgelegte Warnstufe kann mit dem [**/WX**](-wx.md) -Schalter verwendet werden, damit der Mittell-Compiler die Verarbeitung der IDL-Datei stoppt.

Der **/W** -Schalter verhält sich wie der [**/Warn**](-warn.md) -Schalter.

## <a name="examples"></a>Beispiele

**Mittel l/W2 Dateiname. idl**

**Mittel l/W4 Leiste. idl**

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Allgemeine Syntax der Mittell-Befehlszeile](general-midl-command-line-syntax.md)
</dt> <dt>

[**/Warn**](-warn.md)
</dt> </dl>

 

 




