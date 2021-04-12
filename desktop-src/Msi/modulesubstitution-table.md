---
description: Die ModuleSubstitution-Tabelle gibt die konfigurierbaren Felder einer Modul Datenbank an und stellt eine Vorlage für die Konfiguration der einzelnen Felder bereit.
ms.assetid: 8e94c31f-b3a7-4f3a-aec4-32b0e1dd5400
title: ModuleSubstitution-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e27789f723af87e228bada91b79a16d7dc4d2d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218537"
---
# <a name="modulesubstitution-table"></a>ModuleSubstitution-Tabelle

Die ModuleSubstitution-Tabelle gibt die konfigurierbaren Felder einer Modul Datenbank an und stellt eine Vorlage für die Konfiguration der einzelnen Felder bereit. Das Benutzer-oder Zusammenarbeits Tool kann diese Tabelle Abfragen, um zu bestimmen, welche Konfigurations Vorgänge durchgeführt werden sollen. Diese Tabelle wird nicht in der Zieldatenbank zusammengeführt.

Die folgenden Tabellen können keine konfigurierbaren Felder enthalten und dürfen in dieser Tabelle nicht aufgeführt werden:

ModuleSubstitution-Tabelle

[ModuleConfiguration-Tabelle](moduleconfiguration-table.md)

[Moduleausschluss-Tabelle](moduleexclusion-table.md)

[ModuleSignature-Tabelle](modulesignature-table.md)

Die ModuleSubstitution-Tabelle weist die folgenden Spalten auf.



| Spalte | Typ                         | Schlüssel | Nullwerte zulässig |
|--------|------------------------------|-----|----------|
| Tabelle  | [Bezeichner](identifier.md) | J   | N        |
| Zeile    | [Text](text.md)             | J   | N        |
| Column | [Bezeichner](identifier.md) | J   | N        |
| Wert  | [Text](text.md)             | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>Glaub
</dt> <dd>

Diese Spalte gibt den Namen der Tabelle an, die in der Modul Datenbank geändert wird.

</dd> <dt>

<span id="Row"></span><span id="row"></span><span id="ROW"></span>Zeile
</dt> <dd>

Dieses Feld gibt die Primärschlüssel der Zielzeile in der Tabelle an, die in der Tabellenspalte benannt ist. Mehrere Primärschlüssel werden durch Semikolons getrennt. Ziel Zeilen werden zur Änderung ausgewählt, bevor Änderungen an der Ziel Tabelle vorgenommen werden. Wenn ein Datensatz in der Tabelle ModuleSubstitution das Primärschlüssel Feld einer Zielzeile ändert, werden andere Datensätze in der Tabelle ModuleSubstitution auf der Grundlage der ursprünglichen Primärschlüssel Daten, nicht auf der Grundlage der Primärschlüssel Ersetzung, angewendet. Die Reihenfolge der Zeilen Ersetzung ist nicht definiert.

Werte in dieser Spalte weisen immer das [spezielle cmsm-Format](cmsm-special-format.md)auf. Ein literales Semikolon (";") oder Gleichheitszeichen ("=") kann hinzugefügt werden, indem dem Zeichen ein umgekehrter Schrägstrich vorangestellt wird. '\\'. Ein NULL-Wert für einen Schlüssel wird durch einen NULL-Wert, ein vorangestelltes Semikolon, zwei aufeinander folgende Semikolons oder ein nachfolgendes Semikolon gekennzeichnet, je nachdem, ob der NULL-Wert ein einziger, ein erster, ein mittlerer oder ein abschließender Schlüssel Spaltenwert ist.

</dd> <dt>

<span id="Column"></span><span id="column"></span><span id="COLUMN"></span>Kolumne
</dt> <dd>

Dieses Feld gibt die Ziel Spalte in der Zeile mit dem Namen in der Spalte Zeile an. Wenn mehrere Zeilen in der ModuleSubstitution-Tabelle verschiedene Spalten derselben Zielzeile ändern, werden alle Spalten Ersetzungen ausgeführt, bevor die geänderte Zeile in die Datenbank eingefügt wird. Die Reihenfolge der Spalten Ersetzung ist nicht definiert.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Wert
</dt> <dd>

Diese Spalte enthält eine Zeichenfolge, die eine Formatierungs Vorlage für die Daten bereitstellt, die in das durch Tabelle, Zeile und Spalte angegebene Zielfeld ersetzt werden. Wenn eine Ersetzungs Zeichenfolge der Form \[ = itema gefunden \] wird, wird die Zeichenfolge, einschließlich der Klammer Zeichen, durch den Wert für das konfigurierbare "itema" ersetzt. Das konfigurierbare Element "itema" wird in der Spalte "Name" der [Tabelle "ModuleConfiguration](moduleconfiguration-table.md) " angegeben, und der Wert wird durch das Mergetool bereitgestellt. Wenn das Mergetool die Angabe eines Werts für ein Element in einer Ersetzungs Zeichenfolge ablehnt, wird der in der Spalte DefaultValue der Tabelle ModuleConfiguration angegebene Standardwert ersetzt. Wenn eine Zeichenfolge auf ein Element verweist, das nicht in der Tabelle ModuleConfiguration enthalten ist, schlägt die Zusammenführung fehl

-   In dieser Spalte wird das [spezielle cmsm-Format](cmsm-special-format.md)verwendet. Der Tabelle kann ein literales Semikolon (";") oder Gleichheitszeichen ("=") hinzugefügt werden, indem dem Zeichen ein umgekehrter Schrägstrich vorangestellt wird. '\\'.
-   Das Wertfeld kann mehrere Ersetzungs Zeichenfolgen enthalten. Beispielsweise ist die Konfiguration der Elemente "Food1" und "Food2" in der Zeichenfolge: " \[ = Food1 \] gut, aber \[ = Food2 \] ist besser, da \[ = Food2 \] etwas nahrhafter ist."
-   Ersetzungs Zeichenfolgen dürfen nicht eingefügt werden. Die Vorlage " \[ = ab \[ = CDE \] \] " ist ungültig.
-   Wenn das Wertefeld NULL ergibt und das Zielfeld keine NULL-Werte zulässt, schlägt die Zusammenführung fehl, und es wird ein Fehler Objekt vom Typ msmerrorbadnullsubstitution erstellt und der Fehlerliste hinzugefügt. Weitere Informationen finden Sie in den Fehlertypen, die unter [**get \_ Type Function**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_type)beschrieben werden.
-   Wenn das Wertfeld die NULL-GUID ergibt {00000000-0000-0000-0000-000000000000} , wird die NULL-GUID durch den Namen der Funktion ersetzt, bevor die Zeile mit dem Modul zusammengeführt wird. Weitere Informationen finden Sie unter [verweisen auf Features in Mergemodulen](referencing-features-in-merge-modules.md).
-   Die Vorlage im Feld Wert wird ausgewertet, bevor Sie in das Zielfeld eingefügt wird. Die Ersetzung in eine Zeile erfolgt, bevor Funktionen ersetzt werden.
-   Wenn die Value-Spalte als Zeichenfolge nur aus ganzzahligen Zeichen ausgewertet wird (mit optionalem + oder-), wird die Zeichenfolge in eine ganze Zahl konvertiert, bevor Sie in ein Zielfeld des [ganzzahligen Formattyps](integer-format-types.md)ersetzt wird. Wenn die Vorlage zu einer Zeichenfolge ausgewertet wird, die nicht nur aus ganzzahligen Zeichen besteht (und optional + oder-), kann das Ergebnis nicht in ein ganzzahliges Zielfeld ersetzt werden. Wenn Sie versuchen, eine nicht ganzzahlige in ein ganzzahliges Feld einzufügen, schlägt die Zusammenführung fehl, und es wird ein msmerrorbadsubstitutiontype-Fehler Objekt zur Fehlerliste hinzugefügt.
-   Wenn die in den Tabellen-und Spalten Feldern angegebene Ziel Spalte ein [Text Formattyp](text-format-types.md)ist und die Auswertung des Wertfelds einen [ganzzahligen Formattyp](integer-format-types.md)ergibt, wird eine Dezimal Darstellung der Zahl in das Zieltextfeld eingefügt.
-   Wenn das Zielfeld ein [ganzzahliger Formattyp](integer-format-types.md)ist und das Wertfeld aus einer nicht durch Trennzeichen getrennten Liste von Elementen im [Bitfeld-Format](bitfield-format-types.md)besteht, der Wert im Feld Ziel wird mit dem bitweisen **and-** Operator mit der Umkehrung des bitweisen **or** aller Masken Werte aus den Elementen kombiniert und dann mithilfe des bitweisen **or** -Operators mit den einzelnen ganzzahligen oder Bitfeld-Elementen kombiniert, wenn diese durch die entsprechenden Masken Werte maskiert werden. Dadurch werden die Bits aus den Eigenschaften explizit auf die bereitgestellten Werte festgelegt, aber alle anderen Bits in der Zelle bleiben unverändert.
-   Wenn das Wertfeld einen [Schlüssel Formattyp](key-format-types.md)ergibt und es sich um einen Schlüssel in einer Tabelle mit mehreren primär Schlüsseln handelt, kann auf den Elementnamen ein Semikolon und ein ganzzahliger Wert folgen, der den 1-basierten Index in der Menge der Werte angibt, die einen Primärschlüssel bilden. Wenn keine Ganzzahl angegeben wird, wird der Wert 1 verwendet. Beispielsweise verfügt die [Steuerelement Tabelle](control-table.md) über zwei Primärschlüssel Spalten: Dialog \_ und Steuerelement. Der Wert eines Elements "item1", bei dem es sich um einen Schlüssel in der Steuerelement Tabelle handelt, weist die Form "Dialogname;" auf. ControlName ", wobei Dialogname der Wert in der Dialog Feld \_ Tabelle und ControlName der Wert in der Steuerelement Spalte ist. Um nur ControlName zu ersetzen, sollte die \[ Ersetzungs Zeichenfolge = item1; 2 \] verwendet werden.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die modulesubstition-Tabelle wird von [konfigurierbaren Mergemodulen](configurable-merge-modules.md)verwendet. Mergemod.dll Version 2,0 oder höher ist erforderlich, um ein konfigurierbares Mergemodul zu erstellen.

Um die Kompatibilität mit Versionen von Mergemod.dll vor Version 2,0 zu gewährleisten, sollten die Tabellen [ModuleConfiguration](moduleconfiguration-table.md) und ModuleSubstitution in der [Tabelle moduleignoretable](moduleignoretable-table.md) jedes Moduls enthalten sein.

 

 
