---
description: ICE03 überprüft die Datentypen und Fremdschlüssel basierend auf der \_ Validierungs Tabelle und den Datenbanktabellen in der MSI-Datei.
ms.assetid: e9be1c09-8468-4956-9aa0-12383ade4718
title: ICE03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 017c13ee568a0efe4d88c28594fb568a7b4a0736
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216747"
---
# <a name="ice03"></a>ICE03

ICE03 überprüft die Datentypen und Fremdschlüssel basierend auf der [ \_ Validierungs Tabelle](-validation-table.md) und den Datenbanktabellen in der MSI-Datei.

## <a name="result"></a>Ergebnis

ICE03 gibt die folgenden Meldungen für die Validierungs Fehler aus.



| ICE03-Fehlermeldung                                                       | BESCHREIBUNG                                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Doppelter Primärschlüssel                                                     | Die Primärschlüssel einer neuen Zeile dupliziert die Primärschlüssel einer vorhandenen Zeile. Die Nullable-Spalte der [ \_ Validierungs Tabelle](-validation-table.md) zeigt die Primärschlüssel in der Datenbank an.                                                                                              |
| Keine Spalten, die NULL-Werte zulassen                                                     | Eine Tabellenspalte, die in der Werte zulässt-Spalte der Überprüfungs [ \_ Tabelle](-validation-table.md) nicht als Werte zulässt angegeben ist, enthält einen Eintrag, der NULL ist.                                                                                                                                |
| Kein gültiger Fremdschlüssel                                                   | Eine Spalte, bei der es sich um einen Fremdschlüssel in einer zweiten Tabelle handelt, enthält einen Eintrag, der im Primärschlüssel der zweiten Tabelle nicht vorhanden ist.                                                                                                                                                          |
| Der Wert überschreitet MaxValue.                                                    | Der numerische Wert eines Eintrags in einer Datenbanktabelle überschreitet die für dieses Feld in der Spalte MaxValue der Überprüfungs [ \_ Tabelle](-validation-table.md)angegebene Obergrenze.                                                                                                           |
| Wert unterhalb von MinValue                                                      | Der numerische Wert eines Eintrags in einer Datenbanktabelle ist kleiner als der für dieses Feld in der MinValue-Spalte der [ \_ Validierungs Tabelle](-validation-table.md)angegebene Mindestgrenzwert.                                                                                                      |
| Der Wert ist kein Member der Gruppe.                                             | Der Wert eines Eintrags in einer Datenbanktabelle ist kein Member der zulässigen Werte, die für dieses Feld in der Set-Spalte der [ \_ Validierungs Tabelle](-validation-table.md)angegeben sind.                                                                                                  |
| Ungültige Version.                                                    | Weitere Informationen finden Sie unter dem Datentyp [Version](version.md) .                                                                                                                                                                                                                                                 |
| Großbuchstaben erforderlich                                                   | Siehe den [Großbuchstaben](uppercase.md) -Datentyp.                                                                                                                                                                                                                                             |
| Ungültige GUID-Zeichenfolge                                                       | Siehe den [GUID](guid.md) -Datentyp.                                                                                                                                                                                                                                                       |
| Ungültiger Dateiname/Verwendung von Platzhaltern                                      | Die Datenbank enthält einen ungültigen Dateinamen oder einen falschen Platzhalter. Weitere Informationen finden Sie unter der Platzhalter [Datentyp](wildcardfilename.md) .                                                                                                                                                          |
| Ungültiger Bezeichner                                                        | Siehe den [BezeichnerDatentyp](identifier.md) .                                                                                                                                                                                                                                           |
| Ungültige Sprach-ID                                                       | Die Datenbank enthält einen ungültigen numerischen sprach Bezeichner (langid). Weitere Informationen finden Sie unter [Language](language.md) Data Type. Siehe [sprach Bezeichner-Konstanten und-](../intl/language-identifier-constants-and-strings.md)Zeichen folgen. Beispiel: 1033 für die US-amerikanische und 0 für sprachneutral.<br/> |
| Ungültiger Datei Name                                                          | Weitere Informationen finden Sie unter [Datentyp Datentyp](filename.md) .                                                                                                                                                                                                                                               |
| Ungültiger vollständiger Pfad                                                         | Weitere Informationen finden Sie in den Datentypen [Pfad](path.md), [anypath](anypath.md)und [Pfade](paths.md) .                                                                                                                                                                                                      |
| Ungültige bedingte Zeichenfolge                                                    | Die Datenbank enthält eine ungültige bedingte Zeichenfolge. Dies ist eine Text Zeichenfolge, die entsprechend der [Syntax der bedingten Anweisung](conditional-statement-syntax.md)zu true oder false ausgewertet werden muss. Siehe Bedingungs [Datentyp](condition.md) .                                           |
| Ungültige Zeichenfolge.                                                     | Siehe den [formatierten](formatted.md) Datentyp.                                                                                                                                                                                                                                             |
| Ungültige Vorlage für Vorlage                                                   | Siehe den [Vorlagen](template.md) Datentyp.                                                                                                                                                                                                                                               |
| Ungültige DefaultDir-Zeichenfolge                                                 | Siehe den [DefaultDir](defaultdir.md) -Datentyp.                                                                                                                                                                                                                                           |
| Ungültiger Registrierungspfad                                                     | Weitere Informationen finden Sie unter [RegPath](regpath.md) -Datentyp.                                                                                                                                                                                                                                                 |
| Ungültige CustomSource-Daten                                                     | Weitere Informationen finden Sie unter [CustomSource](customsource.md) -Datentyp.                                                                                                                                                                                                                                       |
| Ungültige Zeichen folgen Eigenschaft                                                   | Siehe den [Eigenschafts](property.md) Datentyp.                                                                                                                                                                                                                                               |
| Fehlende Daten in der \_ Validierungs Tabelle oder alten Datenbank                        | In der Datenbank sind Spalten vorhanden, die nicht in der Spalte Spalte der Überprüfungs [ \_ Tabelle](-validation-table.md)aufgeführt sind. Die Datenbank-und die \_ Validierungs Tabelle stimmen nicht ab.                                                                                                           |
| Ungültige CAB-Syntax/Name                                                   | Siehe den [CAB](cabinet.md) -Datentyp.                                                                                                                                                                                                                                                 |
| \_Validierungs Tabelle: Ungültige Kategorie-Zeichenfolge                               | Dies ist ein Fehler beim Erstellen der \_ Validierungs Tabelle. Bei der Validierung wird die für diese Spalte in der Validierungs Tabelle verwendete Kategoriezeichenfolge nicht erkannt \_ . Weitere Informationen finden Sie unter [Spaltendatentypen](column-data-types.md) und Angeben einer gültigen Kategorie.                                           |
| \_Validierungs Tabelle: die Daten in der keytable-Spalte sind falsch.                  | Die keytable-Spalte in der \_ Validierungs Tabelle verweist auf eine Tabelle, die in der Datenbank nicht vorhanden ist.                                                                                                                                                                                     |
| \_Validierungs Tabelle: Wert in der MaxValue-Spalte < in der MinValue-Spalte | Dies ist ein Fehler beim Erstellen der [ \_ Validierungs Tabelle](-validation-table.md). Der minimale Wert muss immer kleiner oder gleich dem maximalen Wert sein.                                                                                                                                                              |
| Ungültiges Verknüpfungs Ziel                                                       | Siehe den Datentyp für die [Verknüpfung](shortcut.md) .                                                                                                                                                                                                                                               |
| Zeichen folgen Überlauf (größer als Länge in Spalte zulässig)                 | Die Länge der Zeichenfolge ist größer als die Spaltenbreite, die durch die Spaltendefinition angegeben wird. Beachten Sie, dass das Installationsprogramm die Spaltenbreite nicht intern auf den angegebenen Wert beschränkt. Siehe [Spalten Definitions Format](column-definition-format.md).                                         |
| Undefinierter Fehler.                                                           | Unbekannter Fehler.                                                                                                                                                                                                                                                                            |
| Die Spalte kann nicht lokalisiert werden.                                                | Primärschlüssel Spalten können nicht lokalisiert werden.                                                                                                                                                                                                                                                  |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 
