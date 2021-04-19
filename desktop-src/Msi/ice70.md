---
description: ICE70 überprüft, ob ganzzahlige Werte für Registrierungseinträge ordnungsgemäß angegeben werden.
ms.assetid: f8493622-867b-42e1-9fda-a7c3229bbb4e
title: ICE70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 616592a772dec6f95d81b92f03f0bffea6ce7bf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353623"
---
# <a name="ice70"></a>ICE70

ICE70 überprüft, ob ganzzahlige Werte für Registrierungseinträge ordnungsgemäß angegeben werden. Werte der Form \# \# Str, \# % unexpanded Str, werden nicht überprüft. Werte der Form \# xhex, \# xhex, \# Integer und \# \[ Property \] werden überprüft. In der folgenden Tabelle finden Sie eine kurze Übersicht.



| Wert                 | Überprüfen                                                                    |
|-----------------------|-------------------------------------------------------------------------------|
| \#\#SRT               | gültigen                                                                         |
| \#% nicht erweitert Str     | gültigen                                                                         |
| \#xhex, \# xhex         | Überprüfen Sie auf gültige hexadezimale Zeichen (0-9, a-f, a-f). Eigenschaften sind hier zulässig. |
| \#+ int, \# -int, \# int | Validieren Sie auf gültige numerische Zeichen (0-9). Eigenschaften sind hier zulässig.     |



 

Die Syntax für einen ganzzahligen Wert, der in die Registrierung eingegeben werden soll, ist \# Integer, wobei Integer numerisch ist.

## <a name="result"></a>Ergebnis

ICE70 meldet einen Fehler, wenn ganzzahlige Werte für Registrierungseinträge nicht ordnungsgemäß angegeben sind.

## <a name="example"></a>Beispiel

ICE70 meldet die folgenden Fehler für das angegebene Beispiel.

``` syntax
The value #12xz34 is an invalid numeric value for registry entry Reg1. If you meant to use a string, then the string value entry must be preceded by ## not #.
```

So beheben Sie diesen Fehler: Wenn der Wert numerisch sein soll, ändern Sie den Wert so, dass alle numerischen Zeichen verwendet werden. Wenn Sie möchten, dass der Wert eine Zeichenfolge ist, muss der Wert zwei ' \# ' ( \# \# ) anstelle von nur einem vorangestellt werden.

``` syntax
The value #xz34 is an invalid hexadecimal value for registry entry Reg2.
```

So beheben Sie diesen Fehler: gültige hexadezimale Zeichen sind 0-9, a-f und a-f. Nur diese Zeichen können auf das \# x (oder \# x) folgen.

[Registrierungs Tabelle](registry-table.md) (partiell)



| Registrierung | Wert    |
|----------|----------|
| Reg1     | \#12xz34 |
| Reg2     | \#xz34   |



 

## <a name="remarks"></a>Bemerkungen

-   \#\[MyProperty \] ist gültig.
-   \#\[MyProperty ist ungültig (fehlende schließende Klammer).
-   \#\[myProp1 \] \[ myProp2 ist gültig. (Obwohl der letzte Klammer die schließende Klammer fehlt, kann myProp1 zu Str ausgewertet werden \# \# \# , sodass Str \[ myProp2 gültig ist.
-   \#\]MyProperty \[ ist ungültig.
-   Alle eingebetteten Eigenschaften in einer Wert Zeichenfolge dürfen nicht in \[ $compkey- \] , \[ \# filekey- \] oder \[ ! filekey-Form vorliegen, \] da diese nicht numerisch sind. Es gibt jedoch eine Ausnahme: \# \[ MyProperty \] \[ $compkey \] (oder \[ \# filekey \] oder \[ ! filekey) ist gültig, da " \] MyProperty" wie bei der vorhergehenden \[ in "str" ausgewertet werden \] kann \# .

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 



