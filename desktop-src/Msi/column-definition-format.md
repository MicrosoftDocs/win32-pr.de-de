---
description: Msiviewgetcolumninfo und die ColumnInfo-Eigenschaft des View-Objekts verwenden das folgende Format, um Daten Bank Spaltendefinitionen zu beschreiben.
ms.assetid: 77379664-26f2-4c1d-8c44-d9be2376efa9
title: Spalten Definitions Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e43e7f70c942fda32bf5003571fa687250e971d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216381"
---
# <a name="column-definition-format"></a>Spalten Definitions Format

[**Msiviewgetcolumninfo**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo) und die [**ColumnInfo-Eigenschaft**](view-columninfo.md) des [**View**](view-object.md) -Objekts verwenden das folgende Format, um Daten Bank Spaltendefinitionen zu beschreiben. Jede Spalte wird durch eine Zeichenfolge im entsprechenden Daten Satz Feld beschrieben, das von der Funktion oder der Eigenschaft zurückgegeben wird. Die Definitions Zeichenfolge besteht aus einem einzelnen Buchstaben, der den Datentyp gefolgt von der Breite der Spalte darstellt (falls zutreffend, bytes, andernfalls). Eine Breite von 0 (null) kennzeichnet eine unbegrenzte Breite (z. b. lange Textfelder und Streams). Ein Großbuchstabe gibt an, dass NULL-Werte in der Spalte zulässig sind.



| Spalten Deskriptor | Definitions Zeichenfolge                 |
|-------------------|-----------------------------------|
| Hymnen?                | String, Variable Length (? = 1-255) |
| S0                | Zeichenfolge, Variable Länge           |
| i2                | Kurze Ganzzahl                     |
| i4                | Lange ganze Zahl                      |
| v0                | Binärer Stream                     |
| selbst?                | Temporäre Zeichenfolge (? = 0-255)        |
| IStGH?                | Temporäre Ganzzahl (? = 0, 1, 2, 4)     |
| O0                | Temporäres Objekt                  |



 

Die zum Beschreiben von Spalten verwendeten Zeichen folgen haben die folgende Beziehung zu den SQL-Abfrage Zeichenfolgen, die von CREATE und Alter verwendet werden. Weitere Informationen finden Sie unter [SQL-Syntax](sql-syntax.md).



| Rückgabewert | SQL-Syntax                |
|----------------|---------------------------|
| S0             | LONGCHAR                  |
| L0             | LONGCHAR lokalisierbar      |
| Hymnen \#           | CHAR ( \# )                  |
| Hymnen \#           | Zeichen ( \# )             |
| int \#           | CHAR ( \# ) lokalisierbar      |
| int \#           | \#Lokalisier bares Zeichen () |
| i2             | SHORT                     |
| i2             | INT                       |
| i2             | INTEGER                   |
| i4             | LONG                      |
| v0             | OBJECT                    |



 

Wenn der Buchstabe nicht groß geschrieben ist, muss die SQL-Anweisung mit Not Null angehängt werden.



| Rückgabewert | SQL-Syntax        |
|----------------|-------------------|
| S0             | LONGCHAR not NULL |



 

Das Installationsprogramm schränkt die Spaltenlänge nicht intern auf den Wert ein, der im Spalten Definitions Format angegeben ist. Wenn die in ein Feld eingegebenen Daten die angegebene Spaltenlänge überschreiten, kann das Paket die [Paket](package-validation.md)Überprüfung nicht durchlaufen. Um die Validierung in diesem Fall zu übergeben, müssen entweder die Daten oder das Datenbankschema geändert werden. Die einzige Möglichkeit zum Ändern der Spaltenlänge einer Standardtabelle besteht darin, die Tabelle mithilfe von " [**msidatabaseexport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta)" zu exportieren, die exportierte IDT-Datei zu bearbeiten und dann die Tabelle mithilfe von " [**msidatabaseimport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)" zu importieren. Autoren können die Spaltendatentypen, die NULL-Zulässigkeit oder die Lokalisierungs Attribute von Spalten in Standard Tabellen nicht ändern. Autoren können benutzerdefinierte Tabellen mit Spalten Attributen erstellen, die Spalten Attribute aufweisen.

Wenn Sie [**msidatabasemerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) verwenden, um eine Verweis Datenbank in eine Zieldatenbank zusammenzuführen, müssen die Spaltennamen, die Anzahl der Primärschlüssel und die Spaltendatentypen identisch sein. **Msidatabasemerge** ignoriert die Attribute für Lokalisierung und Spaltenlänge. Wenn eine Spalte in der Verweis Datenbank eine Länge von 0 (null) oder größer als die Länge der Spalte in der Zieldatenbank aufweist, erhöht **msidatabasemerge** die Spaltenlänge in der Zieldatenbank auf die Länge in der Verweis Datenbank.

Wenn Sie Mergmod.dll Version 2,0 verwenden, ändert die Anwendung eines Mergemoduls zu einer MSI-Datei nie die Spaltenlänge oder die Spaltentypen einer vorhandenen Datenbanktabelle. Die Anwendung eines Mergemoduls kann jedoch das Schema einer vorhandenen Datenbanktabelle ändern, wenn das Modul einer Tabelle neue Spalten hinzufügt, für die es gültig ist, Spalten hinzuzufügen. Bei Verwendung einer Mergemod.dll Version, die kleiner als Version 2,0 ist, ändert die Anwendung eines Mergemoduls nie die Spaltenlänge und ändert niemals das Schema der Zieldatenbank.

 

 



