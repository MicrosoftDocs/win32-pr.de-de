---
description: ICE03 überprüft die Datentypen und Fremdschlüssel basierend auf der Validation-Tabelle und den Datenbanktabellen \_ in der .msi Datei.
ms.assetid: e9be1c09-8468-4956-9aa0-12383ade4718
title: ICE03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4814bb8023b32c85e752201909f77bd851ec3545c907c03e1c2349a34117d4e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118946644"
---
# <a name="ice03"></a>ICE03

ICE03 überprüft die Datentypen und Fremdschlüssel basierend auf der [ \_ Validation-Tabelle](-validation-table.md) und den Datenbanktabellen in .msi Datei.

## <a name="result"></a>Ergebnis

ICE03 veröffentlicht die folgenden Meldungen zu den Validierungsfehlern.



| ICE03-Fehlermeldung                                                       | BESCHREIBUNG                                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Doppelter Primärschlüssel                                                     | Die Primärschlüssel einer neuen Zeile duplizieren die Primärschlüssel einer vorhandenen Zeile. In der Spalte Nullable der [ \_ Tabelle Validation werden](-validation-table.md) die Primärschlüssel in der Datenbank angezeigt.                                                                                              |
| Keine Spalte, die NULL-Werte zuwertet                                                     | Eine Tabellenspalte, die in der Spalte Nullable der [ \_ Tabelle Validation](-validation-table.md) nicht als NULL-Werte zu verwenden angegeben ist, enthält einen Eintrag, der NULL ist.                                                                                                                                |
| Kein gültiger Fremdschlüssel                                                   | Eine Spalte, die ein Fremdschlüssel in einer zweiten Tabelle ist, enthält einen Eintrag, der im Primärschlüssel der zweiten Tabelle nicht vorhanden ist.                                                                                                                                                          |
| Wert überschreitet MaxValue                                                    | Der numerische Wert eines Eintrags in einer Datenbanktabelle überschreitet den für dieses Feld in der Spalte MaxValue der [ \_ Validierungstabelle angegebenen Höchstwert.](-validation-table.md)                                                                                                           |
| Wert unter MinValue                                                      | Der numerische Wert eines Eintrags in einer Datenbanktabelle ist kleiner als der für dieses Feld in der Spalte MinValue der [ \_ Validation-Tabelle angegebene Mindestgrenzwert.](-validation-table.md)                                                                                                      |
| Der Wert ist kein Member der Menge.                                             | Der Wert eines Eintrags in einer Datenbanktabelle ist kein Member des zulässigen Wertesatzes, der für dieses Feld in der Spalte Set der [ \_ Validierungstabelle angegeben ist.](-validation-table.md)                                                                                                  |
| Ungültige Versionszeichenfolge                                                    | Weitere Informationen finden [Sie unter Versionsdatentyp.](version.md)                                                                                                                                                                                                                                                 |
| Groß-/Groß-/Groß-/Groß-/Groß-                                                   | Weitere Informationen finden [Sie unter UpperCase-Datentyp.](uppercase.md)                                                                                                                                                                                                                                             |
| Ungültige GUID-Zeichenfolge                                                       | Weitere Informationen finden Sie [unter GUID-Datentyp.](guid.md)                                                                                                                                                                                                                                                       |
| Ungültiger Dateiname/Ungültige Verwendung von Platzhaltern                                      | Die Datenbank enthält einen ungültigen Dateinamen oder einen falschen Platzhalter. Weitere Informationen finden [Sie unter dem Datentyp WildCardFilename.](wildcardfilename.md)                                                                                                                                                          |
| Ungültiger Bezeichner                                                        | Weitere Informationen finden Sie [unter Bezeichnerdatentyp.](identifier.md)                                                                                                                                                                                                                                           |
| Ungültige Sprach-ID                                                       | Die Datenbank enthält einen ungültigen numerischen Sprachbezeichner (LANGID). Weitere Informationen finden [Sie unter Sprachdatentyp.](language.md) Weitere Informationen [finden Sie unter Sprachbezeichnerkonst konstanten und Zeichenfolgen](../intl/language-identifier-constants-and-strings.md). Beispiel: 1033 für die USA und 0 für sprachneutral.<br/> |
| Ungültiger Dateiname                                                          | Weitere Informationen finden [Sie unter Filename-Datentyp.](filename.md)                                                                                                                                                                                                                                               |
| Ungültiger vollständiger Pfad                                                         | Weitere Informationen finden [Sie unter den Datentypen Path,](path.md) [AnyPath](anypath.md) [und Paths.](paths.md)                                                                                                                                                                                                      |
| Fehlerhafte bedingte Zeichenfolge                                                    | Die Datenbank enthält eine ungültige bedingte Zeichenfolge. Dies ist eine Textzeichenfolge, die gemäß der Syntax der bedingten Anweisung zu TRUE oder FALSE [ausgewertet werden muss.](conditional-statement-syntax.md) Weitere Informationen finden [Sie unter Condition-Datentyp.](condition.md)                                           |
| Ungültige Formatzeichenfolge                                                     | Weitere Informationen finden [Sie unter Formatierte](formatted.md) Datentypen.                                                                                                                                                                                                                                             |
| Ungültige Vorlagenzeichenfolge                                                   | Weitere Informationen finden [Sie unter Template](template.md) data type (Vorlagendatentyp).                                                                                                                                                                                                                                               |
| Ungültige DefaultDir-Zeichenfolge                                                 | Weitere Informationen finden [Sie unter DefaultDir-Datentyp.](defaultdir.md)                                                                                                                                                                                                                                           |
| Ungültiger Registrierungspfad                                                     | Weitere Informationen finden [Sie unter RegPath-Datentyp.](regpath.md)                                                                                                                                                                                                                                                 |
| Fehlerhafte CustomSource-Daten                                                     | Weitere Informationen finden [Sie unter Dem CustomSource-Datentyp.](customsource.md)                                                                                                                                                                                                                                       |
| Ungültige Eigenschaftenzeichenfolge                                                   | Weitere Informationen finden [Sie unter Property-Datentyp.](property.md)                                                                                                                                                                                                                                               |
| Fehlende Daten in der \_ Validierungstabelle oder alten Datenbank                        | Es gibt Spalten in der Datenbank, die nicht in der Spalte Spalte der [ \_ Validierungstabelle aufgeführt sind.](-validation-table.md) Die Datenbank und \_ die Validierungstabelle sind nicht übereinstimmend.                                                                                                           |
| Bad cabinet syntax/name (Fehlerhafte Syntax/Name des Schränken)                                                   | Weitere Informationen finden [Sie unter dem Datentyp "Cabinet".](cabinet.md)                                                                                                                                                                                                                                                 |
| \_Validierungstabelle: Ungültige Kategoriezeichenfolge                               | Dies ist ein Fehler beim Erstellen der \_ Validierungstabelle. Bei der Validierung wird die Kategoriezeichenfolge, die für diese bestimmte Spalte in der Validierungstabelle verwendet \_ wird, nicht erkannt. Weitere Informationen [finden Sie unter Spaltendatentypen,](column-data-types.md) und geben Sie eine gültige Kategorie an.                                           |
| \_Validierungstabelle: Daten in der KeyTable-Spalte sind falsch                  | Die KeyTable-Spalte in der Validierungstabelle verweist auf \_ eine Tabelle, die in der Datenbank nicht vorhanden ist.                                                                                                                                                                                     |
| \_Validierungstabelle: Der Wert in der Spalte MaxValue < wert in der MinValue-Spalte. | Dies ist ein Fehler beim Erstellen der [ \_ Validierungstabelle](-validation-table.md). Min muss immer kleiner oder gleich Max sein.                                                                                                                                                              |
| Fehlerhaftes Verknüpfungsziel                                                       | Weitere Informationen finden [Sie unter Dem Shortcut-Datentyp.](shortcut.md)                                                                                                                                                                                                                                               |
| Zeichenfolgenüberlauf (größer als die in spalte zulässige Länge)                 | Die Länge der Zeichenfolge ist größer als die Spaltenbreite, die von der Spaltendefinition angegeben wird. Beachten Sie, dass das Installationsprogramm die Spaltenbreite nicht intern auf den angegebenen Wert einschränkt. Siehe [Spaltendefinitionsformat](column-definition-format.md).                                         |
| Undefinierter Fehler.                                                           | Unbekannter Fehler.                                                                                                                                                                                                                                                                            |
| Spalte kann nicht lokalisiert werden                                                | Primärschlüsselspalten können nicht lokalisiert werden.                                                                                                                                                                                                                                                  |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz](ice-reference.md)
</dt> </dl>

 

 
