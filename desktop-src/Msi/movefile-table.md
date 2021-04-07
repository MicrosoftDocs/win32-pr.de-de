---
description: Diese Tabelle enthält eine Liste der Dateien, die aus einem angegebenen Quellverzeichnis in ein bestimmtes Zielverzeichnis verschoben oder kopiert werden sollen.
ms.assetid: 9ba47bdc-90c8-444a-ba8b-71c723b54556
title: "\"Muvefile\"-Tabelle"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2340626e745627c3c6146998c851a076d21ab81a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760165"
---
# <a name="movefile-table"></a>"Muvefile"-Tabelle

Diese Tabelle enthält eine Liste der Dateien, die aus einem angegebenen Quellverzeichnis in ein bestimmtes Zielverzeichnis verschoben oder kopiert werden sollen.

Die "muvefile"-Tabelle weist die folgenden Spalten auf.



| Spalte       | Typ                         | Schlüssel | Nullwerte zulässig |
|--------------|------------------------------|-----|----------|
| Filekey      | [Bezeichner](identifier.md) | J   | N        |
| Komponente\_  | [Bezeichner](identifier.md) | N   | N        |
| SourceName   | [Text](text.md)             | N   | J        |
| Destname     | [Filename](filename.md)     | N   | J        |
| Quellordner | [Bezeichner](identifier.md) | N   | J        |
| DestFolder   | [Bezeichner](identifier.md) | N   | N        |
| Optionen      | [Integer](integer.md)       | N   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="FileKey"></span><span id="filekey"></span><span id="FILEKEY"></span>Filekey
</dt> <dd>

Primärschlüssel, der einen bestimmten "vfile"-Datensatz eindeutig identifiziert.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Zulieferern\_
</dt> <dd>

Externer Schlüssel in der [Komponenten Tabelle](component-table.md). Wenn die Komponente, auf die von diesem Schlüssel verwiesen wird, nicht für die Installation oder Entfernung ausgewählt ist, wird für diesen Eintrag keine Aktion ausgeführt.

</dd> <dt>

<span id="SourceName"></span><span id="sourcename"></span><span id="SOURCENAME"></span>SourceName
</dt> <dd>

Diese Spalte enthält den lokalisierbaren Namen der Quelldateien, die verschoben oder kopiert werden sollen. Diese Spalte kann leer gelassen werden. Weitere Informationen finden Sie in der Beschreibung der sourcefolder-Spalte. Dieses Feld muss einen langen Dateinamen enthalten und darf Platzhalter Zeichen ( \* und?) enthalten.

</dd> <dt>

<span id="DestName"></span><span id="destname"></span><span id="DESTNAME"></span>Destname
</dt> <dd>

Diese Spalte enthält den lokalisierbaren Namen, der der ursprünglichen Datei nach dem Verschieben oder kopieren übergeben werden soll. Wenn dieses Feld leer ist, erhält die Zieldatei den gleichen Namen wie die Quelldatei.

</dd> <dt>

<span id="SourceFolder"></span><span id="sourcefolder"></span><span id="SOURCEFOLDER"></span>Quellordner
</dt> <dd>

Diese Spalte enthält den Namen einer Eigenschaft mit einem Wert, der in den vollständigen Pfad des Quell Verzeichnisses aufgelöst wird. Wenn die Spalte SourceName leer bleibt, wird angenommen, dass die in der Spalte sourcefolder benannte Eigenschaft den vollständigen Pfad zur Quelldatei selbst (einschließlich des Datei namens) enthält.

</dd> <dt>

<span id="DestFolder"></span><span id="destfolder"></span><span id="DESTFOLDER"></span>DestFolder
</dt> <dd>

Der Name einer Eigenschaft, deren Wert in den vollständigen Pfad zum Zielverzeichnis aufgelöst wird.

</dd> <dt>

<span id="Options"></span><span id="options"></span><span id="OPTIONS"></span>Optionen
</dt> <dd>

Ganzzahliger Wert, der den Betriebsmodus angibt.



| Konstante                     | Hexadezimal | Decimal | Bedeutung               |
|------------------------------|-------------|---------|-----------------------|
| (none)                       | 0x000       | 0       | Kopieren Sie die Quelldatei. |
| **msidbmuvemeflitionsmove** | 0x001       | 1       | Verschieben Sie die Quelldatei. |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn ein " \* "-Platzhalter in die Spalte "SourceName" der Tabelle "muvefile" eingegeben wird und in der Spalte "destname" ein Ziel Dateiname angegeben ist, behalten alle verschobener oder kopierten Dateien die Namen in den Quellen bei.

Diese Tabelle wird von der [Aktion "muvefiles](movefiles-action.md)" verarbeitet.

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE18](ice18.md)  
[ICE32](ice32.md)  
[ICE45](ice45.md)  
[ICE85](ice85.md)  
</dl>

 

 



