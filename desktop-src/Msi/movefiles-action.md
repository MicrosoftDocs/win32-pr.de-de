---
description: Die Aktion MoveFiles sucht vorhandene Dateien auf dem Computer des Benutzers und verschiebt oder kopiert diese Dateien an einen neuen Speicherort.
ms.assetid: f08f751d-877b-4b17-8015-7108d5fd8195
title: MoveFiles-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b8581cd19569109c0f7697b5dfebf33e91b33da9ba84d15caf424242e4e21ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118945035"
---
# <a name="movefiles-action"></a>MoveFiles-Aktion

Die Aktion MoveFiles sucht vorhandene Dateien auf dem Computer des Benutzers und verschiebt oder kopiert diese Dateien an einen neuen Speicherort. Die MoveFiles-Aktion fragt die [MoveFile-Tabelle](movefile-table.md) ab und verschiebt dort angegebene Dateien, wenn die mit den Einträgen verknüpfte Komponente für die lokale Installation angegeben oder von der Quelle ausgeführt wird.

## <a name="sequence-restrictions"></a>Sequenzeinschränkungen

Die MoveFiles-Aktion muss nach der [InstallValidate-Aktion](installvalidate-action.md) und vor der [InstallFiles-Aktion](installfiles-action.md) erfolgen.

## <a name="actiondata-messages"></a>ActionData-Nachrichten



| Feld | Beschreibung der Aktionsdaten                  |
|-------|---------------------------------------------|
| \[1\] | Bezeichner der verschobenen Datei.                   |
| \[6\] | Größe der installierten Datei in Bytes.            |
| \[9\] | Bezeichner des Verzeichnisses, das die verschobene Datei enthält. |



 

## <a name="remarks"></a>Hinweise

Die Tabelle MoveFiles enthält eine Spalte mit dem Namen "options", die die zu verschiebenden oder zu kopierenden Quelldateien angibt. Eine verschobene Quelldatei wird gelöscht, nachdem sie an einen neuen Speicherort kopiert wurde. Die genaue Syntax finden Sie in der [Tabelle MoveFile.](movefile-table.md)

Die Spalten SourceFolder und DestFolder der MoveFile-Tabelle sind Eigenschaftennamen, deren Werte in vollqualifizierte Pfade aufgelöst werden sollen. Bei diesen Eigenschaften kann es sich um einen beliebigen Verzeichniseintrag in der [Directory-Tabelle,](directory-table.md) um eine vordefinierte Ordnereigenschaft (z.[**B. FavoritenOrdner)**](favoritesfolder.md)oder um eine Eigenschaft handeln, die von einem beliebigen Eintrag in der [AppSearch-Tabelle](appsearch-table.md) festgelegt wird. Diese Eigenschaften können einen vollständigen Pfad enthalten, der den Dateinamen zu einer bestimmten Datei enthält. Beispielsweise kann die AppSearch-Tabelle erstellt werden, um nach einer bestimmten Datei zu suchen und eine Eigenschaft auf den vollständigen Pfad zu dieser Datei festzulegen. In diesem Beispiel kann die SourceName-Spalte in der MoveFile-Tabelle leer gelassen werden, um anzugeben, dass der Wert in der SourceFolder-Eigenschaft einen vollständigen Dateipfad enthält. Das Semikolon ist das Listentrennzeichen für Transformationen, Quellen und Patches und sollte nicht in Dateinamen oder Pfaden verwendet werden.

Die MoveFiles-Aktion reagiert nicht auf Einträge in der MoveFile-Tabelle, in der die SourceFolder- oder DestFolder-Eigenschaft nicht zu einem vollständigen Pfad ausgewertet wird.

Die MoveFiles-Aktion versucht, alle Dateien im Quellverzeichnis zu verschieben oder zu kopieren, die mit dem in der Spalte SourceName der Tabelle MoveFiles angegebenen Namen übereinstimmen. Der Name in der SourceName -Spalte kann entweder oder \* enthalten. Platzhalter, mit denen eine Gruppe von Dateien verschoben oder kopiert werden kann. Beispielsweise kann die SourceName -Spalte den Eintrag ".xls" enthalten, \* und die MoveFiles-Aktion verschiebt oder kopiert jede Microsoft Excel Arbeitsmappe aus dem Quellverzeichnis in das Ziel.

Der Name, der der Zieldatei gegeben werden soll, kann in der Spalte DestName der MoveFile-Tabelle angegeben werden. Der Name der Zieldatei behält den Namen der Quelldatei bei, wenn diese Spalte leer gelassen wird.

Wenn \* in die SourceName-Spalte der [MoveFile-Tabelle](movefile-table.md) ein Platzhalterzeichen eingegeben und in der Spalte DestName ein Zieldateiname angegeben wird, behalten alle verschobenen oder kopierten Dateien die Namen in den Quellen bei.

Dateien, die von der MoveFiles-Aktion verschoben oder kopiert werden, werden nicht gelöscht, wenn das Produkt deinstalliert wird.

 

 



