---
title: Schalter "/warn"
description: Der Schalter /warn gibt die Warnstufe des MIDL-Compilers an.
ms.assetid: b1e26e67-8c47-40a2-8f34-22273ddfaa1d
keywords:
- /warn switch MIDL
topic_type:
- apiref
api_name:
- /warn
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a51f57be780edeac4a91ea4f127d34d1c004ff700429f405eee4522dcb63ef4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067455"
---
# <a name="warn-switch"></a>Schalter "/warn"

Der **Schalter /warn** gibt die Warnstufe des MIDL-Compilers an.

``` syntax
midl /warn level
```

## <a name="switch-options"></a>Switch-Optionen

<dl> <dt>

*level* 
</dt> <dd>

Gibt die Warnstufe an, eine ganze Zahl im Bereich von 0 bis 4. Zwischen dem Schalter **/warn und** der Ziffer, die den Wert der Warnstufe angibt, ist kein Leerzeichen.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die Warnstufe gibt den Schweregrad der Warnung an. Die Warnstufen liegen zwischen 1 und 4, und der Wert 0 bedeutet, dass keine Warnungsinformationen angezeigt werden. Die Warnung mit dem höchsten Schweregrad ist Stufe 1. In der folgenden Tabelle werden die Warnungen für jede Warnstufe beschrieben.



| Warnstufe | Beschreibung                                             | Beispiel                                                                   |
|---------------|---------------------------------------------------------|---------------------------------------------------------------------------|
| 0             | Keine Warnungen.                                            |                                                                           |
| 1             | Schwerwiegende Warnungen, die Anwendungsfehler verursachen können.      | Kein Bindungshandler angegeben, keine attributierten Zeiger, in Konflikt stehende Schalter. |
| 2             | Kann Zu Problemen in der Betriebsumgebung des Benutzers führen. | Die Länge des Bezeichners überschreitet 31 Zeichen. Es wurde kein Standard-Union-Arm angegeben.  |
| 3             | Reserviert.                                               |                                                                           |
| 4             | Niedrigste Warnstufe.                                   | Nicht-ANSI C-Konstrukte.                                                    |



 

Warnungen unterscheiden sich von Fehlern. Fehler bewirken, dass der MIDL-Compiler die Verarbeitung der IDL-Datei anzuhalten. Warnungen führen dazu, dass der MIDL-Compiler eine Informationsmeldung aus gibt und die Verarbeitung der IDL-Datei fortbestrebt.

Die vom Schalter **/warn** festgelegte Warnstufe kann mit dem [**WX-Switch**](-wx.md) verwendet werden, um zu bewirken, dass der MIDL-Compiler die Verarbeitung der IDL-Datei anzuhalten.

Der **Schalter /warn** verhält sich genauso wie der [**Schalter /W.**](-w.md)

## <a name="examples"></a>Beispiele

**midl /warn2 filename.idl**

**midl /warn4 bar.idl**

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Allgemeine MIDL-Befehlszeilensyntax](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




