---
description: Entwickler von Windows Installer Paketen können einen benutzerdefinierten Aktionstyp 19 verwenden, wenn die Standard Aktionen nicht ausreichen, um die Installation auszuführen.
ms.assetid: c6df5462-e20e-4486-8480-8c747193c5d9
title: Benutzerdefinierter Aktionstyp 19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 695f86db0848bd65884ce5e233b4d9a249275c1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362792"
---
# <a name="custom-action-type-19"></a>Benutzerdefinierter Aktionstyp 19

Diese benutzerdefinierte Aktion zeigt eine angegebene Fehlermeldung an, gibt einen Fehler zurück und beendet dann die Installation. Die angezeigte Fehlermeldung kann als Zeichenfolge oder als Index in der [Fehler Tabelle](error-table.md)angegeben werden.

## <a name="source"></a>`Source`

Belassen Sie die Spalte "Source" der [Tabelle "CustomAction](customaction-table.md) " leer.

## <a name="type-value"></a>Typwert

Fügen Sie den folgenden Wert in die Spalte Type der Tabelle CustomAction ein, um den grundlegenden numerischen Typ anzugeben.



| Konstanten                                                               | Hexadezimal | Decimal |
|-------------------------------------------------------------------------|-------------|---------|
| **msidbcustomaktiontypetextdata**  +  **msidbcustomaktiontypesourcefile** | 0x013       | 19      |



 

## <a name="target"></a>Ziel

Die Ziel Spalte der [Tabelle CustomAction](customaction-table.md) enthält eine Text Zeichenfolge, die mit der in [**msiformatrecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) (ohne numerische feldspezifizierer) angegebenen Funktionalität formatiert ist. Die zu ersetzenden Parameter sind in eckige Klammern ( \[ ...) eingeschlossen \] und können Eigenschaften, Umgebungsvariablen (% prefix), Dateipfade ( \# Präfix) oder Komponenten Verzeichnispfade ($ prefix) sein. Wenn die Zeichenfolge nach der Formatierung in eine ganze Zahl ausgewertet wird, wird diese Ganzzahl als Index in der [Fehler Tabelle](error-table.md) verwendet, um die anzuzeigende Meldung abzurufen. Wenn die Zeichenfolge nach der Formatierung nicht numerische Zeichen enthält, wird die Zeichenfolge selbst als Nachricht angezeigt.

## <a name="return-processing-options"></a>Rückgabe Verarbeitungsoptionen

Die benutzerdefinierte Aktion verwendet keine Optionen.

## <a name="execution-scheduling-options"></a>Ausführungszeit Planungsoptionen

Die benutzerdefinierte Aktion verwendet keine Optionen.

## <a name="in-script-execution-options"></a>Ausführungs Optionen für In-Script

Die benutzerdefinierte Aktion verwendet keine Optionen.

## <a name="return-values"></a>Rückgabewerte

Siehe [Rückgabewerte für benutzerdefinierte Aktionen](custom-action-return-values.md).

## <a name="remarks"></a>Bemerkungen

Beispielsweise geben die benutzerdefinierten Aktionen CAError1, CAError2, CAError3 und CAError4 diese Nachrichten zurück.

[Tabelle "CustomAction"](customaction-table.md)



| Aktion   | type | `Source` | Ziel                              |
|----------|------|--------|-------------------------------------|
| CAError1 | 19   |        | \[Eigenschaft PROP1\]                           |
| CAError2 | 19   |        | Installationsfehler aufgrund von error2. |
| CAError3 | 19   |        | 25000                               |
| CAError4 | 19   |        | \[Prop2\]                           |



 

[Eigenschaften Tabelle](property-table.md)



| Eigenschaft | Wert                                 |
|----------|---------------------------------------|
| Eigenschaft PROP1    | "Fehler bei der Installation aufgrund von Error1". |
| Prop2    | "25100"                               |



 

[Fehler Tabelle](error-table.md)



| Code  | `Message`                             |
|-------|-------------------------------------|
| 25000 | Installationsfehler aufgrund von Error3. |
| 25100 | Installationsfehler aufgrund von Error4. |



 

Diese benutzerdefinierten Aktionen geben die folgenden Fehlermeldungen zurück:



| Benutzerdefinierte Aktion | Zurückgegebene Zeichenfolge             |
|---------------|-------------------------------------|
| CAError1      | Installationsfehler aufgrund von Error1. |
| CAError2      | Installationsfehler aufgrund von error2. |
| CAError3      | Installationsfehler aufgrund von Error3. |
| CAError4      | Installationsfehler aufgrund von Error4. |



 

Beachten Sie Folgendes: da die Reihenfolge der Auswertung von Startbedingungen durch das Erstellen der [LaunchCondition-Tabelle](launchcondition-table.md)nicht garantiert werden kann, sollten Sie benutzerdefinierte Aktionen vom Typ 19 benutzerdefinierte Aktionen in der Installation verwenden, um Bedingungen in einer bestimmten Reihenfolge auszuwerten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Benutzerdefinierte \_ Aktionen](custom-actions.md)
</dt> </dl>

 

 



