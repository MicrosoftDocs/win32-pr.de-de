---
description: Die Tabelle ModuleSubs extensions gibt die konfigurierbaren Felder einer Moduldatenbank an und stellt eine Vorlage für die Konfiguration der einzelnen Felder bereit.
ms.assetid: 8e94c31f-b3a7-4f3a-aec4-32b0e1dd5400
title: Tabelle "ModuleSubsbor"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a66fbbb0898a254b181d02eca78f33709f8c0e037de140a37893ea3887af6390
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118628587"
---
# <a name="modulesubstitution-table"></a>Tabelle "ModuleSubsbor"

Die Tabelle ModuleSubs extensions gibt die konfigurierbaren Felder einer Moduldatenbank an und stellt eine Vorlage für die Konfiguration der einzelnen Felder bereit. Der Benutzer oder das Mergetool kann diese Tabelle abfragen, um zu bestimmen, welche Konfigurationsvorgänge durchgeführt werden sollen. Diese Tabelle wird nicht mit der Zieldatenbank zusammengeführt.

Die folgenden Tabellen dürfen keine konfigurierbaren Felder enthalten und nicht in dieser Tabelle aufgeführt werden:

Tabelle "ModuleSubsbor"

[Tabelle "ModuleConfiguration"](moduleconfiguration-table.md)

[Tabelle "ModuleExclusion"](moduleexclusion-table.md)

[Tabelle "ModuleSignature"](modulesignature-table.md)

Die Tabelle ModuleSubsfassung enthält die folgenden Spalten.



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

Dieses Feld gibt die Primärschlüssel der Zielzeile in der Tabelle an, die in der Spalte Tabelle benannt ist. Mehrere Primärschlüssel werden durch Semikolons getrennt. Zielzeilen werden zur Änderung ausgewählt, bevor Änderungen an der Zieltabelle vorgenommen werden. Wenn ein Datensatz in der Tabelle ModuleSubsakus das Primärschlüsselfeld einer Zielzeile ändert, werden andere Datensätze in der Tabelle ModuleSubsdatenbank basierend auf den ursprünglichen Primärschlüsseldaten und nicht auf dem Ergebnis der Primärschlüsselersetzungen angewendet. Die Reihenfolge der Zeilenersetzung ist nicht definiert.

Werte in dieser Spalte liegen immer im [CMSM-Sonderformat vor.](cmsm-special-format.md) Ein literales Semikolon (';') oder Gleichheitszeichen ('=') kann hinzugefügt werden, indem dem Zeichen ein umgekehrter Schrägstrich vorangestellt wird. '\\'. Ein NULL-Wert für einen Schlüssel wird durch ein NULL-, ein führendes Semikolon, zwei aufeinander folgende Semikolons oder ein nachfolgendes Semikolon gekennzeichnet, je nachdem, ob der NULL-Wert ein alleiniger, erster, mittlerer oder endgültiger Schlüsselspaltenwert ist.

</dd> <dt>

<span id="Column"></span><span id="column"></span><span id="COLUMN"></span>Spalte
</dt> <dd>

Dieses Feld gibt die Zielspalte in der Zeile mit dem Namen in der Spalte Row an. Wenn mehrere Zeilen in der Tabelle ModuleSubskonvention verschiedene Spalten derselben Zielzeile ändern, werden alle Spaltenersetzungen ausgeführt, bevor die geänderte Zeile in die Datenbank eingefügt wird. Die Reihenfolge der Spaltenersetzung ist nicht definiert.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Wert
</dt> <dd>

Diese Spalte enthält eine Zeichenfolge, die eine Formatierungsvorlage für die Daten bereitstellt, die in das durch Tabelle, Zeile und Spalte angegebene Zielfeld ersetzt werden. Wenn eine Ersetzungszeichenfolge im Format \[ =ItemA \] gefunden wird, wird die Zeichenfolge, einschließlich der eckigen Zeichen, durch den Wert für das konfigurierbare "ItemA" ersetzt. Das konfigurierbare Element "ItemA" wird in der Spalte Name der [Tabelle ModuleConfiguration](moduleconfiguration-table.md) angegeben, und sein Wert wird vom Mergetool bereitgestellt. Wenn das Mergetool die Angabe eines Elements in einer Ersatzzeichenfolge ablehnt, wird der in der Spalte DefaultValue der ModuleConfiguration-Tabelle angegebene Standardwert ersetzt. Wenn eine Zeichenfolge auf ein Element verweist, das nicht in der Tabelle ModuleConfiguration enthalten ist, tritt bei der Zusammenführung ein Fehler auf.

-   In dieser Spalte wird das [CMSM-Sonderformat verwendet.](cmsm-special-format.md) Ein literales Semikolon (';') oder Gleichheitszeichen ('=') kann der Tabelle hinzugefügt werden, indem dem Zeichen ein umgekehrter Schrägstrich vorangestellt wird. '\\'.
-   Das Feld Wert kann mehrere Ersetzungszeichenfolgen enthalten. Beispiel: Die Konfiguration der Elemente "Food1" und "Food2" in der Zeichenfolge : \[ "=Food1 \] is good, but \[ =Food2 \] is better because \[ =Food2 \] is moreious."
-   Ersetzungszeichenfolgen dürfen nicht geschachtelt sein. Die Vorlage " \[ =AB \[ =CDE \] \] " ist ungültig.
-   Wenn das Feld Wert als NULL ausgewertet wird und das Zielfeld nicht NULL-Werte zulässt, schlägt die Zusammenführung fehl, und ein Fehlerobjekt vom Typ msmErrorBadNullSubsune wird erstellt und der Fehlerliste hinzugefügt. Weitere Informationen finden Sie in den unter Get Type Function (Abrufen der [**\_ Typfunktion)**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_type)beschriebenen Fehlertypen.
-   Wenn das Feld Wert die NULL-GUID ergibt: {00000000-0000-0000-0000-000000000000} , wird die NULL-GUID durch den Namen des Features ersetzt, bevor die Zeile mit dem Modul zusammengeführt wird. Weitere Informationen finden Sie unter [Verweisen auf Funktionen in Mergemodulen.](referencing-features-in-merge-modules.md)
-   Die Vorlage im Feld Wert wird ausgewertet, bevor sie in das Zielfeld eingefügt wird. Die Ersetzung in eine Zeile erfolgt vor dem Ersetzen von Features.
-   Wenn die Spalte Wert zu einer Zeichenfolge mit nur ganzzahligen Zeichen ausgewertet wird (mit einem optionalen + oder -), wird die Zeichenfolge in eine ganze Zahl konvertiert, bevor sie in ein Zielfeld des [Ganzzahlformattyps](integer-format-types.md)ersetzt wird. Wenn die Vorlage zu einer Zeichenfolge ausgewertet wird, die nicht nur aus ganzzahligen Zeichen (und einem optionalen + oder -) besteht, kann das Ergebnis nicht in ein ganzzahliges Zielfeld ersetzt werden. Der Versuch, eine Nicht-Ganzzahl in ein ganzzahliges Feld einzufügen, führt dazu, dass die Zusammenführung fehlschlägt, und fügt der Fehlerliste ein msmErrorBadSubsakutype-Fehlerobjekt hinzu.
-   Wenn die in den Feldern Tabelle und Spalte angegebene Zielspalte ein [Textformattyp](text-format-types.md)ist und die Auswertung des Felds Wert zu einem [ganzzahligen Formattyp](integer-format-types.md)führt, wird eine Dezimaldarstellung der Zahl in das Zieltextfeld eingefügt.
-   Wenn das Zielfeld ein [Ganzzahlformattyp](integer-format-types.md)ist und das Feld Wert aus einer nicht durch Trennzeichen getrennten Liste von Elementen im [Bitfield-Format](bitfield-format-types.md)besteht, wird der Wert im Zielfeld mithilfe des bitweisen **AND-Operators** mit der Umkehrung des bitweisen **OR** aller Maskierungswerte aus den Elementen kombiniert und dann mit dem bitweisen **OR-Operator** mit jedem der ganzzahligen elemente oder Bitfeldelemente kombiniert, wenn sie durch die entsprechenden Maskierungswerte maskiert werden. Im Wesentlichen legt dies die Bits aus den Eigenschaften explizit auf die bereitgestellten Werte fest, lässt jedoch alle anderen Bits in der Zelle allein.
-   Wenn das Feld Wert zu einem [Schlüsselformattyp](key-format-types.md)ausgewertet wird und ein Schlüssel in einer Tabelle ist, die mehrere Primärschlüssel verwendet, kann auf den Elementnamen ein Semikolon und ein ganzzahliger Wert folgen, der den 1-basierten Index in den Satz von Werten angibt, die zusammen einen Primärschlüssel bilden. Wenn keine ganze Zahl angegeben wird, wird der Wert 1 verwendet. Die [Control-Tabelle](control-table.md) verfügt beispielsweise über zwei Primärschlüsselspalten: Dialog \_ und Control. Der Wert eines Elements "Item1", das ein Schlüssel in der Control-Tabelle ist, hat das Format "DialogName; ControlName", wobei DialogName der Wert in der \_ Dialogtabelle und ControlName der Wert in der Control -Spalte ist. Um nur ControlName zu ersetzen, sollte die Ersetzungszeichenfolge \[ =Item1;2 \] verwendet werden.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die Tabelle ModuleSubstition wird von [konfigurierbaren Mergemodulen](configurable-merge-modules.md)verwendet. Mergemod.dll Version 2.0 oder höher ist erforderlich, um ein konfigurierbares Mergemodul zu erstellen.

Um die Kompatibilität mit Versionen von Mergemod.dll vor Version 2.0 sicherzustellen, sollten die Tabellen [ModuleConfiguration](moduleconfiguration-table.md) und ModuleSubsverzeichnisse in der [Tabelle ModuleIgnoreTable](moduleignoretable-table.md) jedes Moduls enthalten sein.

 

 
