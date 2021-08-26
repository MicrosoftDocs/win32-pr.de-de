---
description: MsiViewGetColumnInfo und die ColumnInfo-Eigenschaft des View-Objekts verwenden das folgende Format, um Datenbankspaltendefinitionen zu beschreiben.
ms.assetid: 77379664-26f2-4c1d-8c44-d9be2376efa9
title: Spaltendefinitionsformat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2f0fcad09d0c87b766022602b152c09f466b4d6cddc87467b89ff02793240b8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077918"
---
# <a name="column-definition-format"></a>Spaltendefinitionsformat

[**MsiViewGetColumnInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo) und [**die ColumnInfo-Eigenschaft**](view-columninfo.md) des [**View-Objekts**](view-object.md) verwenden das folgende Format, um Datenbankspaltendefinitionen zu beschreiben. Jede Spalte wird durch eine Zeichenfolge im entsprechenden Datensatzfeld beschrieben, das von der Funktion oder Eigenschaft zurückgegeben wird. Die Definitionszeichenfolge besteht aus einem einzelnen Buchstaben, der den Datentyp darstellt, gefolgt von der Breite der Spalte (in Zeichen, falls zutreffend, bytes andernfalls ). Eine Breite von 0 (null) gibt eine ungebundene Breite an (z. B. lange Textfelder und Streams). Ein Großbuchstabe gibt an, dass NULL-Werte in der Spalte zulässig sind.



| Spaltendeskriptor | Definitionszeichenfolge                 |
|-------------------|-----------------------------------|
| s?                | Zeichenfolge, variable Länge (?=1-255) |
| s0                | Zeichenfolge, variable Länge           |
| i2                | Kurze ganze Zahl                     |
| i4                | Lange ganze Zahl                      |
| v0                | Binärdatenstrom                     |
| G?                | Temporäre Zeichenfolge (?=0-255)        |
| J?                | Temporäre ganze Zahl (?=0,1,2,4)     |
| O0                | Temporäres Objekt                  |



 

Die Zeichenfolgen, die zum Beschreiben von Spalten verwendet werden, haben die folgende Beziehung zu den SQL abfragezeichenfolgen, die von CREATE und ALTER verwendet werden. Weitere Informationen finden Sie unter [SQL Syntax](sql-syntax.md).



| Rückgabewert | SQL-Syntax                |
|----------------|---------------------------|
| s0             | LONGCHAR                  |
| l0             | LONGCHAR LOCALIZABLE      |
| s \#           | CHAR( \# )                  |
| s \#           | CHARACTER( \# )             |
| L \#           | CHAR( \# ) LOCALIZABLE      |
| L \#           | CHARACTER( \# ) LOCALIZABLE |
| i2             | SHORT                     |
| i2             | INT                       |
| i2             | INTEGER                   |
| i4             | LONG                      |
| v0             | OBJECT                    |



 

Wenn der Buchstabe nicht groß geschrieben wird, sollte die SQL-Anweisung mit NOT NULL angefügt werden.



| Rückgabewert | SQL-Syntax        |
|----------------|-------------------|
| s0             | LONGCHAR NOT NULL |



 

Das Installationsprogramm schränkt die Länge von Spalten nicht intern auf den Wert ein, der durch das Spaltendefinitionsformat angegeben wird. Wenn die in ein Feld eingegebenen Daten die angegebene Spaltenlänge überschreiten, kann das Paket die [Paketvalidierung nicht bestehen.](package-validation.md) Um die Überprüfung in diesem Fall zu bestehen, müssen entweder die Daten oder das Datenbankschema geändert werden. Die einzige Möglichkeit, die Spaltenlänge einer Standardtabelle zu ändern, ist das Exportieren der Tabelle mit [**msiDatabaseExport,**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta)das Bearbeiten der exportierten IDT-Datei und das anschließende Importieren der Tabelle mit [**msiDatabaseImport.**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) Autoren können die Spaltendatentypen, NULL-Werte oder Lokalisierungsattribute von Spalten in Standardtabellen nicht ändern. Autoren können benutzerdefinierte Tabellen mit Spalten mit spaltenspezifischen Attributen erstellen.

Bei Verwendung [**von MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) zum Zusammenführen einer Verweisdatenbank in einer Zieldatenbank müssen die Spaltennamen, die Anzahl der Primärschlüssel und die Spaltendatentypen übereinstimmen. **MsiDatabaseMerge ignoriert** die Lokalisierungs- und Spaltenlängenattribute. Wenn eine Spalte in der Verweisdatenbank eine Länge von 0 oder größer als die Länge der Spalte in der Zieldatenbank hat, erhöht **MsiDatabaseMerge** die Spaltenlänge in der Zieldatenbank auf die Länge in der Verweisdatenbank.

Bei verwendung Mergmod.dll Version 2.0 ändert die Anwendung eines Mergemoduls auf eine .msi-Datei nie die Länge von Spalten oder die Spaltentypen einer vorhandenen Datenbanktabelle. Die Anwendung eines Mergemoduls kann jedoch das Schema einer vorhandenen Datenbanktabelle ändern, wenn das Modul einer Tabelle, für die es gültig ist, Spalten hinzuzufügen, neue Spalten hinzufügt. Wenn Sie Mergemod.dll Version 2.0 verwenden, ändert die Anwendung eines Mergemoduls nie die Länge der Spalten und nie das Schema der Zieldatenbank.

 

 



