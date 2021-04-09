---
description: Durch die Aktion "Aktion" werden vorhandene Dateien auf dem Computer des Benutzers lokalisiert und an einen neuen Speicherort verschoben oder kopiert.
ms.assetid: f08f751d-877b-4b17-8015-7108d5fd8195
title: Aktion "muvefiles"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f06db0cef12753652bf94bf05875b2c2f9d4067c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868864"
---
# <a name="movefiles-action"></a>Aktion "muvefiles"

Durch die Aktion "Aktion" werden vorhandene Dateien auf dem Computer des Benutzers lokalisiert und an einen neuen Speicherort verschoben oder kopiert. Mit der Aktion "muvefiles" wird die [Tabelle "muvefile](movefile-table.md) " abgefragt und die dort angegebenen Dateien verschoben, wenn die mit den Einträgen verknüpfte Komponente für die lokale Installation angegeben ist oder von der Quelle ausgeführt wird.

## <a name="sequence-restrictions"></a>Sequenz Einschränkungen

Die Aktion "muvefiles" muss nach der [InstallValidate](installvalidate-action.md) -Aktion und vor der [InstallFiles](installfiles-action.md) -Aktion erfolgen.

## <a name="actiondata-messages"></a>Aktions Daten Meldungen



| Feld | Beschreibung der Aktions Daten                  |
|-------|---------------------------------------------|
| \[1\] | Der Bezeichner der verschoden Datei.                   |
| \[6\] | Größe der installierten Datei in Bytes.            |
| \[9\] | Bezeichner des Verzeichnisses, das die verschoderte Datei enthält. |



 

## <a name="remarks"></a>Bemerkungen

Die Tabelle "muvefiles" enthält eine Spalte mit dem Namen "Options", die die zu verschiebenden oder zu kopierenden Quelldateien angibt. Eine verschoderte Quelldatei wird gelöscht, nachdem Sie an einen neuen Speicherort kopiert wurde. Die genaue Syntax finden Sie in der [Tabelle "muvefile](movefile-table.md)".

Die Spalten sourcefolder und destfolder der Tabelle "muvefile" sind Eigenschaftsnamen, deren Werte in voll qualifizierte Pfade aufgelöst werden sollen. Diese Eigenschaften können alle Verzeichniseinträge in der [Verzeichnis](directory-table.md) Tabelle, jede vordefinierte Ordner Eigenschaft (z. b.[**FavoritesFolder**](favoritesfolder.md)) oder eine Eigenschaft sein, die von einem beliebigen Eintrag in der [AppSearch](appsearch-table.md) -Tabelle festgelegt wird. Diese Eigenschaften können einen vollständigen Pfad enthalten, der den Dateinamen für eine bestimmte Datei enthält. Beispielsweise kann die Tabelle "AppSearch" erstellt werden, um nach einer bestimmten Datei zu suchen und eine Eigenschaft auf den vollständigen Pfad zu dieser Datei festzulegen. In diesem Beispiel kann die Spalte SourceName in der Tabelle "muvefile" leer gelassen werden, um anzugeben, dass der Wert in der sourcefolder-Eigenschaft einen vollständigen Dateipfad enthält. Das Semikolon ist das Listen Trennzeichen für Transformationen, Quellen und Patches und sollte nicht in Dateinamen oder Pfaden verwendet werden.

Die Aktion "muvefiles" wirkt sich nicht auf Einträge in der "muvefile"-Tabelle aus, in der die Eigenschaft "sourcefolder" oder "destfolder" nicht zu einem vollständigen Pfad ausgewertet wird.

Die Aktion movefiles versucht, alle Dateien im Quellverzeichnis zu verschieben oder zu kopieren, die dem in der Spalte SourceName der Tabelle movefiles angegebenen Namen entsprechen. Der Name in der Spalte SourceName kann entweder oder enthalten \* ? Platzhalter, die es ermöglichen, eine Gruppe von Dateien zu verschieben oder zu kopieren. Beispielsweise kann die Spalte SourceName einen Eintrag von " \* . xls" enthalten, und mit der Aktion "muvefiles" wird jede Microsoft Excel-Arbeitsmappe aus dem Quellverzeichnis in das Ziel verschoben oder kopiert.

Der Name, der an die Zieldatei übergeben werden soll, kann in der Spalte "destname" der Tabelle "muvefile" angegeben werden. Der Name der Ziel Datei behält den Quell Dateinamen bei, wenn diese Spalte leer bleibt.

Wenn ein " \* "-Platzhalter in die Spalte "SourceName" der [Tabelle "muvefile](movefile-table.md) " eingegeben wird und in der Spalte "destname" ein Ziel Dateiname angegeben ist, behalten alle verschobener oder kopierten Dateien die Namen in den Quellen bei.

Dateien, die von der Aktion "muvefiles" verschoben oder kopiert werden, werden bei der Installation des Produkts nicht gelöscht.

 

 



