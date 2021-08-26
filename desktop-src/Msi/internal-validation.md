---
description: Beim Erstellen eines Installationspakets können Sie die MsiViewModify-Funktion oder die View.Modify-Methode verwenden, um sicherzustellen, dass die von Ihnen eingeben Daten syntaktisch korrekt sind.
ms.assetid: c960e9df-dcd6-44d2-8662-40a1dea81f45
title: Interne Überprüfung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44184a87f7d8bd28b3603d81bb83ae28ec68471e6c9c849bf9322dc5e968c886
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043300"
---
# <a name="internal-validation"></a>Interne Überprüfung

Beim Erstellen eines Installationspakets können Sie die [**MsiViewModify-Funktion**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) oder die View.Modify-Methode verwenden, um sicherzustellen, dass die von Ihnen eingeben Daten syntaktisch korrekt sind. Weitere Informationen finden Sie unter [**Modify-Methode.**](view-modify.md) Auf der niedrigsten Ebene kann die Spalte einer Datenbanktabelle ganze Zahlen (kurz oder lang), Zeichenfolgen oder Binärdaten speichern. Ein Installationspaket erfordert jedoch bestimmte ganze Zahlen oder Zeichenfolgen in bestimmten Tabellen. Diese Spezifikationen werden in der [ \_ Validierungstabelle beibehalten.](-validation-table.md) Die FileName-Spalte der Tabelle [File](file-table.md) ist beispielsweise eine Zeichenfolgenspalte, speichert jedoch speziell einen Dateinamen. Daher sollte ihr Eintrag nicht nur eine Zeichenfolge sein, sondern auch die Anforderungen für die Benennung von Dateien erfüllen.

Die verschiedenen Validierungsenumerwerte, die mit der [**MsiViewModify-Funktion**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) verwendet werden, ermöglichen eine sofortige Validierung auf verschiedenen Ebenen. Die MSIMODIFY \_ VALIDATE FIELD-Enum kann verwendet werden, um einzelne \_ Felder eines Datensatzes zu überprüfen. Fremdschlüssel werden nicht überprüft. Die MSIMODIFY \_ VALIDATE-Enum überprüft eine gesamte Zeile und enthält die Fremdschlüsselüberprüfung. Wenn Sie eine neue Zeile in eine Tabelle einfügen, verwenden Sie die MSIMODIFY \_ VALIDATE NEW-Enum, um sicherzustellen, dass Sie gültige Daten hinzufügen und eindeutige \_ Primärschlüssel verwenden. Ein Einfüge schlägt fehl, wenn die Primärschlüssel nicht eindeutig sind. Wenn ein Aufruf von **MsiViewModify** mit einer der Validierungsenumerate einen Fehler zurückgibt, können Sie wiederholte Aufrufe von [**MsiViewGetError**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgeterrora) durchführen, um das Problem zu diagnostizieren. **MsiViewGetError gibt** die Spalte an, in der der Fehler aufgetreten ist, sowie den enum-Wert, um das Problem zu beheben. Weitere Informationen finden Sie unter [**GetError-Methode.**](view-geterror.md)

Sie können auch die interne Überprüfung verwenden, um sicherzustellen, dass andere Autoren Daten ordnungsgemäß in Ihre benutzerdefinierte Tabelle eingeben. Fügen Sie die einzelnen Spalten der benutzerdefinierten Tabelle der Validierungstabelle hinzu, indem Sie den Namen der benutzerdefinierten Tabelle und den Spaltennamen \_ als Primärschlüssel verwenden. Geben Sie eine Beschreibung oder einen Zweck jeder Spalte in der Spalte Beschreibung der \_ Tabelle Validation an. Geben Sie die anwendbaren Anforderungen für jede Spalte mithilfe der Spalten Nullable, MinValue, MaxValue, KeyTable, KeyColumn, Category und Set ein:

-   Wenn die Spalte NULLable ist, geben Sie "Y" ein. Falls nicht, geben Sie "N" ein.
-   Wenn die Spalte eine ganzzahlige Spalte ist und einen Bereich von ganzen Zahlen enthalten kann, geben Sie diesen Bereich mithilfe der Spalten MinValue und MaxValue ein.
-   Fremdschlüsselspalten werden mithilfe der Spalten KeyTable und KeyColumn identifiziert.
-   Geben Sie für Zeichenfolgenspalten eine Kategorie an, z. B. Dateiname, GUID oder Bezeichner. Weitere Informationen finden Sie unter [Spaltendatentypen.](column-data-types.md)
-   Wenn sich die Daten nur auf eine bestimmte Anzahl von Werten (Zeichenfolge oder ganze Zahl) beziehen können, verwenden Sie die Spalte Festlegen, um die zulässigen Werte auflisten.

Im Folgenden finden Sie eine Liste der Spalten (zusätzlich zu Tabelle, Spalte und Beschreibung) in der Validierungstabelle, die ausgefüllt werden können, wenn die Spalte den angegebenen \_ Typ auf hat. (Beachten Sie, dass Sie nicht alle Spalten ausfüllen müssen.)



| type    | Spalten                                                          |
|---------|------------------------------------------------------------------|
| Integer | Nullable, MinValue, MaxValue, KeyTable, KeyColumn, Set           |
| String  | Nullable, KeyTable, KeyColumn, Category, Set, MinValue, MaxValue |
| Binary  | Nullable, Category (Category must be "Binary")                   |



 

In Erstellungsumgebungen kann MSIMODIFY \_ VALIDATE \_ DELETE verwendet werden. Bei dieser Aufzählsumme wird davon ausgegangen, dass Sie die Zeile löschen möchten. Es wird keine Feld- oder Fremdschlüsselüberprüfung ausgeführt. Diese Enum führt tatsächlich eine umgekehrte Fremdschlüsselüberprüfung durch. Die Validierungstabelle wird auf Verweise in den Spalten KeyTable und KeyColumn für die Tabelle überprüft, zu der die \_ Zeile "deleted" gehört. Wenn Es Spalten gibt, die die Tabelle mit der Zeile "deleted" als potenziellen Fremdschlüssel auflisten, durchfing er diese Spalte, um zu sehen, ob einer der Werte auf Werte in der Zeile "deleted" verweist. Eine Fehler-Rückgabe bedeutet, dass Sie die relationale Integrität der Datenbank durch Löschen der Zeile gefährden.

 

 



