---
title: /Warn-Schalter
description: Der/Warn-Schalter gibt die Warnstufe des Mittell-Compilers an.
ms.assetid: b1e26e67-8c47-40a2-8f34-22273ddfaa1d
keywords:
- /Warn-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /warn
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebb2effd65175bf7bf54cb74cb63a56af0278784
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718198"
---
# <a name="warn-switch"></a>/Warn-Schalter

Der **/Warn** -Schalter gibt die Warnstufe des Mittell-Compilers an.

``` syntax
midl /warn level
```

## <a name="switch-options"></a>Optionen wechseln

<dl> <dt>

*level* 
</dt> <dd>

Gibt die Warnstufe an, eine ganze Zahl im Bereich von 0 bis 4. Zwischen dem Schalter **/Warn** und der Ziffer, die den Wert für die Warnstufe angibt, besteht kein Leerzeichen.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Warnstufe zeigt den Schweregrad der Warnung an. Die Warnungs Stufen liegen zwischen 1 und 4. der Wert 0 bedeutet, dass keine Warn Informationen angezeigt werden. Die Warnung mit dem höchsten Schweregrad ist Ebene 1. In der folgenden Tabelle werden die Warnungen für die einzelnen Warn Stufen beschrieben.



| Warnstufe | BESCHREIBUNG                                             | Beispiel                                                                   |
|---------------|---------------------------------------------------------|---------------------------------------------------------------------------|
| 0             | Keine Warnungen.                                            |                                                                           |
| 1             | Schwerwiegende Warnungen, die zu Anwendungsfehlern führen können.      | Es wurde kein Bindungs handle angegeben, nicht attributierte Zeiger, widersprüchliche Switches. |
| 2             | Kann zu Problemen in der Betriebsumgebung des Benutzers führen. | Die Bezeichnerlänge überschreitet 31 Zeichen. Es wurde kein Standard-Union-Arm angegeben.  |
| 3             | Reserviert.                                               |                                                                           |
| 4             | Niedrigste Warnstufe.                                   | Nicht-ANSI-C-Konstrukte.                                                    |



 

Warnungen unterscheiden sich von Fehlern. Fehler bewirken, dass der Mittell-Compiler die Verarbeitung der IDL-Datei stoppt. Warnungen bewirken, dass der Mittell-Compiler eine Informations Meldung ausgibt und die Verarbeitung der IDL-Datei fortsetzt.

Die Warnstufe, die durch den Schalter " **/Warn** " festgelegt wird, kann mit dem [**WX**](-wx.md) -Schalter verwendet werden, damit der Mittell-Compiler die Verarbeitung der IDL-Datei stoppt.

Der **/Warn** -Schalter verhält sich wie der [**/W**](-w.md) -Schalter.

## <a name="examples"></a>Beispiele

**Mittel l/warn2 Dateiname. idl**

**Mittel l/warn4 Leiste. idl**

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Allgemeine Syntax der Mittell-Befehlszeile](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




