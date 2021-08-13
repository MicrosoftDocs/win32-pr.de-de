---
description: Die Tabelle ModuleSubsators gibt die konfigurierbaren Felder einer Moduldatenbank an und stellt eine Vorlage für die Konfiguration der einzelnen Felder zur Verfügung.
ms.assetid: 8e94c31f-b3a7-4f3a-aec4-32b0e1dd5400
title: ModuleSubsmodultabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a66fbbb0898a254b181d02eca78f33709f8c0e037de140a37893ea3887af6390
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118628587"
---
# <a name="modulesubstitution-table"></a>ModuleSubsmodultabelle

Die Tabelle ModuleSubsators gibt die konfigurierbaren Felder einer Moduldatenbank an und stellt eine Vorlage für die Konfiguration der einzelnen Felder zur Verfügung. Der Benutzer oder das Mergetool kann diese Tabelle abfragen, um zu bestimmen, welche Konfigurationsvorgänge ausgeführt werden sollen. Diese Tabelle wird nicht mit der Zieldatenbank zusammengeführt.

Die folgenden Tabellen dürfen keine konfigurierbaren Felder enthalten und dürfen nicht in dieser Tabelle aufgeführt werden:

ModuleSubsmodultabelle

[ModuleConfiguration-Tabelle](moduleconfiguration-table.md)

[ModuleExclusion-Tabelle](moduleexclusion-table.md)

[ModuleSignature-Tabelle](modulesignature-table.md)

Die ModuleSubstitution-Tabelle enthält die folgenden Spalten.



| Spalte | Typ                         | Key | Nullwerte zulässig |
|--------|------------------------------|-----|----------|
| Tabelle  | [Identifier](identifier.md) | J   | N        |
| Zeile    | [Text](text.md)             | J   | N        |
| Column | [Identifier](identifier.md) | J   | N        |
| Wert  | [Text](text.md)             | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>Tabelle
</dt> <dd>

Diese Spalte gibt den Namen der Tabelle an, die in der Moduldatenbank geändert wird.

</dd> <dt>

<span id="Row"></span><span id="row"></span><span id="ROW"></span>Zeile
</dt> <dd>

Dieses Feld gibt die Primärschlüssel der Zielzeile in der Tabelle mit dem Namen in der Spalte Tabelle an. Mehrere Primärschlüssel werden durch Semikolons getrennt. Zielzeilen werden zur Änderung ausgewählt, bevor Änderungen an der Zieltabelle vorgenommen werden. Wenn ein Datensatz in der Tabelle ModuleSubsregister das Primärschlüsselfeld einer Zielzeile ändert, werden andere Datensätze in der ModuleSubsubs -Tabelle basierend auf den ursprünglichen Primärschlüsseldaten angewendet, nicht auf dem Ergebnis von Primärschlüsselersetzungen. Die Reihenfolge der Zeilenersetzung ist nicht definiert.

Werte in dieser Spalte liegen immer im [CMSM-Sonderformat vor.](cmsm-special-format.md) Ein literales Semikolon (';') oder Gleichheitszeichen ('=') kann hinzugefügt werden, indem dem Zeichen ein schräger Schrägstrich vorangestellt wird. '\\'. Ein NULL-Wert für einen Schlüssel wird durch einen NULL-Wert, ein führendes Semikolon, zwei aufeinander folgende Semikolons oder ein nacheinanderfolgendes Semikolon angegeben, je nachdem, ob es sich bei dem NULL-Wert um einen alleinigen, ersten, mittleren oder endgültigen Schlüsselspaltenwert handelt.

</dd> <dt>

<span id="Column"></span><span id="column"></span><span id="COLUMN"></span>Spalte
</dt> <dd>

Dieses Feld gibt die Zielspalte in der Zeile mit dem Namen in der Spalte Zeile an. Wenn mehrere Zeilen in der Tabelle ModuleSubs substitution unterschiedliche Spalten derselben Zielzeile ändern, werden alle Spaltenersetzungen ausgeführt, bevor die geänderte Zeile in die Datenbank eingefügt wird. Die Reihenfolge der Spaltenersetzung ist nicht definiert.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Wert
</dt> <dd>

Diese Spalte enthält eine Zeichenfolge, die eine Formatierungsvorlage für die Daten enthält, die in das durch Tabelle, Zeile und Spalte angegebene Zielfeld ersetzt werden. Wenn eine Ersetzungszeichenfolge der Form =ItemA gefunden wird, wird die Zeichenfolge, einschließlich der Klammerzeichen, durch den Wert für das konfigurierbare \[ \] "ItemA" ersetzt. Das konfigurierbare Element "ItemA" wird in der Spalte Name der [Tabelle ModuleConfiguration](moduleconfiguration-table.md) angegeben, und sein Wert wird vom Mergetool bereitgestellt. Wenn das Mergetool die Bereitstellung eines Werts für ein Element in einer Ersetzungszeichenfolge abgelehnt hat, wird der standardwert ersetzt, der in der DefaultValue -Spalte der ModuleConfiguration-Tabelle angegeben ist. Wenn eine Zeichenfolge auf ein Element verweist, das nicht in der ModuleConfiguration-Tabelle enthalten ist, schlägt die Zusammenführung fehl.

-   Diese Spalte verwendet [das CMSM-Sonderformat](cmsm-special-format.md). Ein literales Semikolon (';') oder Gleichheitszeichen ('=') kann der Tabelle hinzugefügt werden, indem dem Zeichen ein schräger Schrägstrich vorangestellt wird. '\\'.
-   Das Feld Wert kann mehrere Ersetzungszeichenfolgen enthalten. Beispielsweise ist die Konfiguration der Elemente "Food1" und "Food2" in der Zeichenfolge : " \[ =Food1 \] is good, but \[ =Food2 \] is better because =Food2 is more \[ ious." (=Food1 ist gut, aber =Food2 ist besser, da =Food2 unerschmeidiger \] ist.)
-   Ersetzungszeichenfolgen dürfen nicht geschachtelt werden. Die Vorlage \[ "=AB \[ =CDE" \] \] ist ungültig.
-   Wenn das Feld Wert als NULL ausgewertet wird und das Zielfeld keine NULL-Werte zugibt, schlägt die Zusammenführung fehl, und ein Fehlerobjekt vom Typ msmErrorBadNullSubserror wird erstellt und der Fehlerliste hinzugefügt. Weitere Informationen finden Sie in den unter Get [**\_ Type Function beschriebenen Fehlertypen.**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_type)
-   Wenn das Feld Wert die NULL-GUID auswertet: , wird die NULL-GUID durch den Namen des Features ersetzt, bevor die Zeile mit dem {00000000-0000-0000-0000-000000000000} Modul zusammengeführt wird. Weitere Informationen finden Sie unter [Verweisen auf Funktionen in Mergemodulen.](referencing-features-in-merge-modules.md)
-   Die Vorlage im Feld Wert wird ausgewertet, bevor sie in das Zielfeld eingefügt wird. Die Ersetzung in eine Zeile erfolgt vor dem Ersetzen von Features.
-   Wenn die Value -Spalte zu einer Zeichenfolge aus nur ganzzahligen Zeichen (mit einem optionalen + oder -) ausgewertet wird, wird die Zeichenfolge in eine ganze Zahl konvertiert, bevor sie in ein Zielfeld des Ganzzahlformattyps [ersetzt wird.](integer-format-types.md) Wenn die Vorlage zu einer Zeichenfolge ausgewertet wird, die nicht nur aus ganzzahligen Zeichen (und einem optionalen + oder -) besteht, kann das Ergebnis nicht in ein ganzzahliges Zielfeld ersetzt werden. Der Versuch, eine Nicht-Ganzzahl in ein ganzzahliges Feld einfügt, führt dazu, dass die Zusammenführung fehlschlägt und der Fehlerliste ein msmErrorBadSubs integerType-Fehlerobjekt hinzufügt.
-   Wenn die in den Feldern Tabelle und Spalte angegebene Zielspalte ein [Textformattyp](text-format-types.md)ist und die Auswertung des Felds Wert zu einem Ganzzahlformattyp [führt,](integer-format-types.md)wird eine Dezimaldarstellung der Zahl in das Zieltextfeld eingefügt.
-   Wenn das Zielfeld ein ganzzahliger [Formattyp](integer-format-types.md)ist und das Feld Wert aus einer nicht durch Trennzeichen getrennten Liste von Elementen im [Bitfield-Format](bitfield-format-types.md)besteht, wird der Wert im Zielfeld mit dem  bitweisem **AND-Operator** mit der Umkehrung des bitweises **OR** aller Maskenwerte aus den Elementen kombiniert und dann mithilfe des bitweise OR-Operators mit jedem der ganzzahligen oder bitfield-Elemente kombiniert, wenn es durch die entsprechenden Maskierungswerte maskiert wird. Dadurch werden die Bits aus den Eigenschaften explizit auf die bereitgestellten Werte fest gestellt, aber alle anderen Bits bleiben in der Zelle allein.
-   Wenn das Feld Wert [](key-format-types.md)zu einem Schlüsselformattyp ausgewertet wird und ein Schlüssel in einer Tabelle ist, die mehrere Primärschlüssel verwendet, kann auf den Elementnamen ein Semikolon und ein ganzzahliger Wert folgen, der den 1-basierten Index in der Gruppe von Werten angibt, aus denen zusammen ein Primärschlüssel besteht. Wenn keine ganze Zahl angegeben wird, wird der Wert 1 verwendet. Die [Control-Tabelle verfügt beispielsweise](control-table.md) über zwei Primärschlüsselspalten: Dialog und \_ Control. Der Wert eines Elements "Item1", das ein Schlüssel in der Control-Tabelle ist, hat das Folgende: "DialogName; ControlName", wobei DialogName der Wert in der Tabelle Dialog und ControlName der Wert \_ in der Control -Spalte ist. Um nur ControlName zu ersetzen, sollte die Ersetzungszeichenfolge \[ =Item1;2 \] verwendet werden.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die Tabelle ModuleSubstition wird von [konfigurierbaren Mergemodulen verwendet.](configurable-merge-modules.md) Mergemod.dll Version 2.0 oder höher ist erforderlich, um ein konfigurierbares Mergemodul zu erstellen.

Um die Kompatibilität mit Versionen von Mergemod.dll vor Version 2.0 sicherzustellen, sollten die [ModuleConfiguration-Tabelle](moduleconfiguration-table.md) und die ModuleSubsconfig-Tabellen in der [ModuleIgnoreTable-Tabelle](moduleignoretable-table.md) jedes Moduls enthalten sein.

 

 
