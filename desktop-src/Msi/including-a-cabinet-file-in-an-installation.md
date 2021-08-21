---
description: In diesem Abschnitt wird das Einschließen von Cab-Dateien in Installationen beschrieben. Weitere Informationen finden Sie unter Verwenden von Schränken und komprimierten Quellen.
ms.assetid: 17ea7f76-90b2-48fb-8187-64dc6d294443
title: Einschließen einer Cab-Datei in eine Installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c0970d87b8b219e1558c6b3f1daf78a6a01100a7bc41f9ae1dad51a25048b46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787340"
---
# <a name="including-a-cabinet-file-in-an-installation"></a>Einschließen einer Cab-Datei in eine Installation

In diesem Abschnitt wird das Einschließen von Cab-Dateien in Installationen beschrieben. Weitere Informationen finden Sie unter [Verwenden von Schränken und komprimierten Quellen.](using-cabinets-and-compressed-sources.md)

**So schließen Sie eine Cab-Datei in ein Installationspaket ein**

1.  Verwenden Sie ein Tool zum Erstellen von Schränken, um die Quelldateien in eine Cab-Datei zu komprimieren. Weitere Informationen finden Sie unter [Cabinet Files](cabinet-files.md).
2.  Die Cab-Datei muss sich entweder in einem Datenstrom innerhalb der .msi datei oder in einer separaten Cab-Datei befinden, die sich im Stammverzeichnis der Quellstruktur befindet, die von der [Verzeichnistabelle](directory-table.md)angegeben wird.
3.  Bestimmen Sie, ob die Quelle ein komprimierter Typ oder ein gemischter Typ sein soll, der sowohl unkomprimierte als auch komprimierte Dateien enthält. Weitere Informationen finden Sie unter [Komprimierte und nicht komprimierte Quellen.](compressed-and-uncompressed-sources.md) Legen Sie je nach Typ des Quellimages die komprimierten oder nicht komprimierten Flagbits der [**Word Count Summary-Eigenschaft**](word-count-summary.md) fest.
4.  Fügen Sie der [Dateitabelle](file-table.md) einen Datensatz für jede der Dateien im Schränk hinzu. Geben Sie in der Spalte Datei einen Dateischlüssel ein, der genau mit dem Dateischlüssel der Datei im Schränk übereinstimmt. Bei den Dateischlüsseln wird die Groß-/Kleinschreibung beachtet. Die Dateiinstallationssequenz in der Dateitabelle und im Schränk muss ebenfalls identisch sein. Die Dateisequenz wird durch die Sequenznummer in der Spalte Sequenz angegeben. Um die Sequenznummer für die erste Datei im Schränk zu erreichen, gehen Sie wie folgt vor. Suchen Sie den vorhandenen Datensatz in der [Media-Tabelle](media-table.md) mit dem größten Wert in der DiskID-Spalte. Das Feld LastSequence dieses Datensatzes gibt die letzte Dateisequenznummer an, die auf dem Medium verwendet wird. Weisen Sie der ersten Datei des neuen Schränks in der Tabelle Datei eine Sequenznummer zu, die größer als diese ist. Weisen Sie allen verbleibenden Dateien Sequenznummern in der gleichen Reihenfolge wie in der Cab-Datei zu. Eine Beschreibung der verbleibenden Datensatzfelder finden Sie unter [Dateitabelle](file-table.md).
5.  Fügen Sie der [Medientabelle](media-table.md) einen Datensatz für den Schränk hinzu. Geben Sie im Feld DiskID dieses neuen Datensatzes einen Wert an, der größer als der größte bereits in der Tabelle vorhandene DiskID-Wert ist. Geben Sie den Namen des Schränks in das Feld "Cabinet" ein. Dieser Name muss in Form [](cabinet.md) eines Cabinet-Datentyps sein. Stellen Sie dem Namen das Nummernzeichen "" voran, wenn es sich bei dem Schränk um \# einen Datenstrom handelt, der in der datei .msi gespeichert ist. Beachten Sie Folgendes: Wenn es sich bei dem Gehäuse um einen Datenstrom handelt, wird beim Namen des Schränks die Groß-/Kleinschreibung beachtet. Wenn es sich bei dem Schränk um eine separate Datei handelt, wird beim Namen der Datei die Groß-/Kleinschreibung nicht beachtet.
6.  Ermitteln Sie die größte Dateisequenznummer im neuen Schränk, indem Sie die Spalte Sequenz der aktualisierten Dateitabelle überprüfen. Geben Sie im Feld LastSequence des neuen Datensatzes der Tabelle Media einen Wert ein, der größer als dieser ist. Eine Beschreibung der verbleibenden Datensatzfelder finden Sie unter [Medientabelle](media-table.md).
7.  Sie können die Cab-Datei entweder mit einem Tool wie Msidb.exe oder mithilfe der Datenbankfunktionen des Installationsprogramms im [Installationspaket](database-functions.md)speichern. In den folgenden vier Schritten wird erläutert, wie Sie den Schränk aus einem Programm mithilfe der Datenbankfunktionen hinzufügen.
8.  Öffnen Sie mithilfe von [**MsiDatabaseOpenView**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa)eine Ansicht in der [ \_ Streams Tabelle](-streams-table.md) der Datenbank, um dem Installationspaket aus einem Programm den Schränk hinzuzufügen.
9.  Verwenden Sie [**MsiRecordSetString,**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstringa) um die Spalte Name der Streams Tabelle auf den Namen festzulegen, \_ der in der Spalte Cabinet der [Medientabelle](media-table.md)angezeigt wird. Das Nummernzeichen auslassen: \# .
10. Verwenden Sie [**MsiRecordSetStream,**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) um die Spalte Data der \_ Streams Tabelle auf die Daten des Cabs festzulegen.
11. Verwenden Sie [**MsiViewModify,**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) um den Datensatz in der Streams Tabelle zu \_ aktualisieren.
12. Um Msidb.exe zum Hinzufügen der Mycab.cab-Cab-Datei zum Installationspaket mit dem Namen Mydatabase.msi zu verwenden, verwenden Sie die folgende Befehlszeile: Msidb.exe -d mydatabase.msi -a mycab.cab. In diesem Fall sollte die Spalte Cabinet der Tabelle Media die Zeichenfolge \# enthalten:mycab.cab.

 

 



