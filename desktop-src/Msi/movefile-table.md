---
description: Diese Tabelle enthält eine Liste der Dateien, die aus einem angegebenen Quellverzeichnis in ein angegebenes Zielverzeichnis verschoben oder kopiert werden sollen.
ms.assetid: 9ba47bdc-90c8-444a-ba8b-71c723b54556
title: MoveFile-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49d90afe8a5fb950f2e6fdb96ba0f8af4f8969226a5dc219bc9cd0598481beb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118945095"
---
# <a name="movefile-table"></a>MoveFile-Tabelle

Diese Tabelle enthält eine Liste der Dateien, die aus einem angegebenen Quellverzeichnis in ein angegebenes Zielverzeichnis verschoben oder kopiert werden sollen.

Die Tabelle MoveFile enthält die folgenden Spalten.



| Spalte       | Typ                         | Key | Nullwerte zulässig |
|--------------|------------------------------|-----|----------|
| FileKey      | [Identifier](identifier.md) | J   | N        |
| Komponente\_  | [Identifier](identifier.md) | N   | N        |
| SourceName   | [Text](text.md)             | N   | J        |
| DestName     | [Filename](filename.md)     | N   | J        |
| SourceFolder | [Identifier](identifier.md) | N   | J        |
| DestFolder   | [Identifier](identifier.md) | N   | N        |
| Optionen      | [Integer](integer.md)       | N   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="FileKey"></span><span id="filekey"></span><span id="FILEKEY"></span>FileKey
</dt> <dd>

Primärschlüssel, der einen bestimmten MoveFile-Datensatz eindeutig identifiziert.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Komponente\_
</dt> <dd>

Externer Schlüssel in der [Component-Tabelle.](component-table.md) Wenn die Komponente, auf die von diesem Schlüssel verwiesen wird, nicht für die Installation oder Entfernung ausgewählt ist, wird für diesen MoveFile-Eintrag keine Aktion ausgeführt.

</dd> <dt>

<span id="SourceName"></span><span id="sourcename"></span><span id="SOURCENAME"></span>Sourcename
</dt> <dd>

Diese Spalte enthält den lokalisierbaren Namen der Quelldateien, die verschoben oder kopiert werden sollen. Diese Spalte wird möglicherweise leer gelassen. Weitere Informationen finden Sie in der Beschreibung der SourceFolder-Spalte. Dieses Feld muss einen langen Dateinamen enthalten und kann Platzhalterzeichen ( \* und ?) enthalten.

</dd> <dt>

<span id="DestName"></span><span id="destname"></span><span id="DESTNAME"></span>DestName
</dt> <dd>

Diese Spalte enthält den lokalisierbaren Namen, der der ursprünglichen Datei nach dem Verschieben oder Kopieren gegeben werden soll. Wenn dieses Feld leer ist, erhält die Zieldatei den gleichen Namen wie die Quelldatei.

</dd> <dt>

<span id="SourceFolder"></span><span id="sourcefolder"></span><span id="SOURCEFOLDER"></span>SourceFolder
</dt> <dd>

Diese Spalte enthält den Namen einer Eigenschaft mit einem Wert, der in den vollständigen Pfad zum Quellverzeichnis aufgelöst wird. Wenn die Spalte SourceName leer gelassen wird, wird davon ausgegangen, dass die in der SourceFolder-Spalte benannte Eigenschaft den vollständigen Pfad zur Quelldatei selbst (einschließlich des Dateinamens) enthält.

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
| **msidbMoveFileOptionsMove** | 0x001       | 1       | Verschieben Sie die Quelldatei. |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Wenn \* in die SourceName-Spalte der MoveFile-Tabelle ein Platzhalterzeichen eingegeben und in der Spalte DestName ein Zieldateiname angegeben wird, behalten alle verschobenen oder kopierten Dateien die Namen in den Quellen bei.

Diese Tabelle wird von der [MoveFiles-Aktion](movefiles-action.md)verarbeitet.

## <a name="validation"></a>Überprüfung

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE18](ice18.md)  
[ICE32](ice32.md)  
[ICE45](ice45.md)  
[ICE85](ice85.md)  
</dl>

 

 



