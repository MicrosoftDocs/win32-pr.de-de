---
description: Beim Erstellen eines Installationspakets können Sie die msiviewmodify-Funktion oder die View. Modify-Methode verwenden, um sicherzustellen, dass die eingegebenen Daten syntaktisch korrekt sind.
ms.assetid: c960e9df-dcd6-44d2-8662-40a1dea81f45
title: Interne Validierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca3c1a9e6f7b7e35b4d7d91287af64eff7812de6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128376"
---
# <a name="internal-validation"></a>Interne Validierung

Beim Erstellen eines Installationspakets können Sie die [**msiviewmodify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) -Funktion oder die View. Modify-Methode verwenden, um sicherzustellen, dass die eingegebenen Daten syntaktisch korrekt sind. Weitere Informationen finden Sie unter [**Modify-Methode**](view-modify.md). Auf der niedrigsten Ebene kann die Spalte einer Datenbanktabelle ganze Zahlen (Short oder Long), Zeichen folgen oder Binärdaten speichern. Ein Installationspaket erfordert jedoch bestimmte ganze Zahlen oder Zeichen folgen in bestimmten Tabellen. Diese Spezifikationen werden in der [ \_ Validierungs Tabelle](-validation-table.md)beibehalten. Beispielsweise ist die FileName-Spalte der [File-Tabelle](file-table.md) eine Zeichen folgen Spalte, aber Sie speichert speziell einen Dateinamen. Daher sollte Ihr Eintrag nicht nur eine Zeichenfolge sein, sondern auch die Anforderungen für das Benennen von Dateien erfüllen.

Die verschiedenen Validierungs Enumerationswerte, die mit der [**msiviewmodify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) -Funktion verwendet werden, ermöglichen eine sofortige Validierung auf unterschiedlichen Ebenen. Die msimodify-Feld-Überprüfung \_ \_ kann verwendet werden, um einzelne Felder eines Datensatzes zu überprüfen. Fremdschlüssel werden nicht überprüft. Die msimodify \_ -Enumeration-Überprüfung überprüft eine ganze Zeile und schließt die Fremdschlüssel Überprüfung ein. Wenn Sie eine neue Zeile in eine Tabelle einfügen, überprüfen Sie mithilfe der msimodify \_ \_ New-Enumeration, ob Sie gültige Daten hinzufügen, und verwenden Sie eindeutige Primärschlüssel. Eine Einfügung schlägt fehl, wenn die Primärschlüssel nicht eindeutig sind. Wenn bei einem Aufruf von **msiviewmodify** mit einer der Überprüfungs Aufstellungen ein Fehler zurückgegeben wird, können Sie [**msiviewgeterror**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgeterrora) wiederholt aufrufen, um das Problem zu diagnostizieren. **Msiviewgeterror** gibt die Spalte an, in der der Fehler aufgetreten ist, sowie den Enumerationswert, um das Problem zu beheben. Weitere Informationen finden Sie unter [**GetError-Methode**](view-geterror.md).

Sie können auch die interne Validierung verwenden, um sicherzustellen, dass andere Autoren Daten ordnungsgemäß in die benutzerdefinierte Tabelle eingeben. Fügen Sie jede der Spalten Ihrer benutzerdefinierten Tabelle \_ mithilfe des benutzerdefinierten Tabellennamens und des Spaltennamens als Primärschlüssel zur Validierungs Tabelle hinzu. Geben Sie eine Beschreibung oder einen Zweck für jede Spalte in der Beschreibungs Spalte der Überprüfungs \_ Tabelle an. Geben Sie die anwendbaren Anforderungen für jede Spalte mithilfe der Spalten Nullable, MinValue, MaxValue, keytable, KeyColumn, Category und Set ein:

-   Wenn die Spalte NULL-Werte zulässt, geben Sie "Y" ein. Wenn dies nicht der gibt, geben Sie "N" ein.
-   Wenn es sich bei der Spalte um eine ganzzahlige Spalte handelt, die einen Bereich von ganzen Zahlen enthalten kann, geben Sie diesen Bereich mithilfe der Spalten MinValue und MaxValue ein.
-   Fremdschlüssel Spalten werden mithilfe der keytable-Spalte und der KeyColumn-Spalte identifiziert.
-   Geben Sie für Zeichen folgen Spalten eine Kategorie an, z. b. Dateiname, GUID oder Bezeichner. Weitere Informationen finden Sie unter [Spaltendatentypen](column-data-types.md).
-   Wenn sich die Daten nur auf eine bestimmte Anzahl von Werten (Zeichenfolge oder ganze Zahl) beziehen können, verwenden Sie die Set-Spalte, um die zulässigen Werte aufzulisten.

Im folgenden finden Sie eine Liste der Spalten (zusätzlich zu Tabelle, Spalte und Beschreibung) in der \_ Validierungs Tabelle, die ausgefüllt werden kann, wenn die Spalte den angegebenen Typ hat. (Beachten Sie, dass Sie nicht alle Spalten ausfüllen müssen.)



| type    | Spalten                                                          |
|---------|------------------------------------------------------------------|
| Integer | Nullable, MinValue, MaxValue, keytable, KeyColumn, Set           |
| String  | Nullable, keytable, KeyColumn, Category, Set, MinValue, MaxValue |
| Binary  | Nullable, Category (Kategorie muss "Binary" lauten)                   |



 

Erstellungs Umgebungen verwenden möglicherweise die msimodify- \_ \_ Delete-Löschung. Diese Aufzählung geht davon aus, dass Sie die Zeile löschen möchten. Es wird keine Feld-oder Fremdschlüssel Validierung ausgeführt. Diese Enumeration führt tatsächlich eine rückgängig-Fremdschlüssel Überprüfung durch. Er überprüft die \_ Validierungs Tabelle auf Verweise in den keytable-und KeyColumn-Spalten für die Tabelle, zu der die gelöschte Zeile gehört. Wenn Spalten vorhanden sind, in denen die Tabelle, die die Zeile "gelöscht" enthält, als potenzieller Fremdschlüssel aufgeführt ist, wird diese Spalte durchlaufen, um festzustellen, ob einer der Werte auf Werte in der Zeile "gelöscht" verweist. Eine Fehlerrückgabe bedeutet, dass Sie die relationale Integrität der Datenbank durch Löschen der Zeile unterbrechen.

 

 



