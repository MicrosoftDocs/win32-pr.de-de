---
title: /W-Schalter
description: Der Schalter /W gibt die Warnstufe des MIDL-Compilers an. Die Warnstufe gibt den Schweregrad der Warnung an.
ms.assetid: ee894d73-cbd1-455f-9836-a6d80cfc95f9
keywords:
- /W switch MIDL
topic_type:
- apiref
api_name:
- /W
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e03b2d4a762a7fbb1bba00f8804e8e43a77ad8183a744add63fcf0d37c86d54
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913670"
---
# <a name="w-switch"></a>/W-Schalter

Der Schalter **/W** gibt die Warnstufe des MIDL-Compilers an. Die Warnstufe gibt den Schweregrad der Warnung an.

``` syntax
midl /W level
```

## <a name="switch-options"></a>Optionen wechseln

<dl> <dt>

*level* 
</dt> <dd>

Gibt die Warnstufe an, eine ganze Zahl im Bereich von 0 bis 4. Zwischen dem Schalter **/W** und der Ziffer, die den Wert der Warnstufe angibt, ist kein Leerzeichen vorhanden.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die Warnstufen liegen zwischen 1 und 4, wobei der Wert 0 (null) bedeutet, dass keine Warnungsinformationen angezeigt werden. Die Warnung mit dem höchsten Schweregrad ist Stufe 1. In der folgenden Tabelle werden die Warnungen für jede Warnstufe beschrieben.



| Warnstufe | BESCHREIBUNG                                             | Beispiel                                                                   |
|---------------|---------------------------------------------------------|---------------------------------------------------------------------------|
| W0            | Keine Warnungen.                                            |                                                                           |
| W1            | Schwerwiegende Warnungen, die Anwendungsfehler verursachen können.      | Kein Bindungshandle angegeben, nicht attributierte Zeiger, in Konfliktstehende Switches. |
| W2            | Kann zu Problemen in der Betriebssystemumgebung des Benutzers führen. | Die Bezeichnerlänge überschreitet 31 Zeichen. Es wurde kein Standard-Union-Arm angegeben.  |
| W3            | Reserviert.                                               |                                                                           |
| W4            | Niedrigste Warnstufe.                                   | Nicht-ANSI-C-Konstrukte.                                                    |



 

Warnungen unterscheiden sich von Fehlern. Fehler führen dazu, dass der MIDL-Compiler die Verarbeitung der IDL-Datei anzuhalten. Warnungen bewirken, dass der MIDL-Compiler eine Informationsmeldung ausgibt und die Verarbeitung der IDL-Datei fortsetzt.

Die vom Schalter **/W** festgelegte Warnstufe kann mit dem Schalter [**/WX**](-wx.md) verwendet werden, damit der MIDL-Compiler die Verarbeitung der IDL-Datei anzuhalten.

Der **Schalter /W** verhält sich genauso wie der Schalter [**/warn.**](-warn.md)

## <a name="examples"></a>Beispiele

**midl /W2 filename.idl**

**midl /W4 bar.idl**

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Allgemeine MIDL-Befehlszeilensyntax](general-midl-command-line-syntax.md)
</dt> <dt>

[**/warn**](-warn.md)
</dt> </dl>

 

 




