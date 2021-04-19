---
description: ICE68 prüft, ob alle für eine Installation benötigten benutzerdefinierten Aktions Typen gültig sind.
ms.assetid: a37d6d6c-3005-425b-883a-6fe074b9d708
title: ICE68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1392db6ec05085c672ed70c8f035ea8eed3015e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373343"
---
# <a name="ice68"></a>ICE68

ICE68 prüft, ob alle für eine Installation benötigten benutzerdefinierten Aktions Typen gültig sind. Wenn Sie den von ICE68 gemeldeten Fehler nicht beheben, bewirkt dies, dass eine Installation fehlschlägt, die versucht, die Aktion auszuführen. ICE68 gibt eine Warnung aus, wenn das **msidbcustomaktiontypoidentitäts Ate** -Attribut festgelegt wird, ohne dass auch das **msidbcustomaktiontypeinscript** -Attribut festgelegt wird.

## <a name="result"></a>Ergebnis

ICE68 gibt einen Fehler zurück, wenn ein für eine Installation benötigter Aktionstyp ungültig ist.

## <a name="example"></a>Beispiel

ICE68 gibt die folgende Warnung aus, wenn für eine benutzerdefinierte Aktion das **msidbcustomaction typoidentitäts Ate** -Bit im type-Feld der CustomAction-Tabelle festgelegt ist, ohne dass **msidbcustomaction typeinscript** ebenfalls festgelegt ist.

``` syntax
Even though custom action '[2]' is marked to be elevated (with 
attribute msidbCustomActionTypeNoImpersonate), it will not be run with elevated 
privileges because it's not deferred (with attribute msidbCustomActionTypeInScript).
```

Um diese Warnung zu beheben, schließen Sie **msidbcustomaction typeinscript** (0x400) ein, wenn die benutzerdefinierte Aktion **msidbcustomaction typoidentitäts Ate** (0x800) einschließt. Andernfalls ignoriert das Installationsprogramm das **msidbcustomaktiontypoidentitäts Ate** -Attribut. Weitere Informationen finden Sie unter [benutzerdefinierte Aktion In-Script Ausführungs Optionen](custom-action-in-script-execution-options.md).

ICE68 meldet den folgenden Fehler für das gezeigte Beispiel:

``` syntax
Invalid custom action type for action 'Action1'.
```

1027 ist kein gültiger Aktionstyp.

Wählen Sie einen gültigen benutzerdefinierten Aktionstyp aus, um diesen Fehler zu beheben.

[CustomAction-Tabelle](customaction-table.md) (partiell)



| Aktion  | type | `Source`   | Ziel     |
|---------|------|----------|------------|
| Action1 | 1027 | Argument | Component1 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 



