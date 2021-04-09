---
description: Die duplicatefile-Tabelle enthält eine Liste von Dateien, die dupliziert werden sollen, entweder in ein anderes Verzeichnis als die ursprüngliche Datei oder in dasselbe Verzeichnis, aber mit einem anderen Namen. Die ursprüngliche Datei muss eine Datei sein, die von der InstallFiles-Aktion installiert wird.
ms.assetid: 7fe1b52d-4b06-48cd-afe5-2bd5495bb55e
title: Duplicatefile-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 766f28b7984aedfc682a2bf23378d46ee0519c65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042393"
---
# <a name="duplicatefile-table"></a>Duplicatefile-Tabelle

Die duplicatefile-Tabelle enthält eine Liste von Dateien, die dupliziert werden sollen, entweder in ein anderes Verzeichnis als die ursprüngliche Datei oder in dasselbe Verzeichnis, aber mit einem anderen Namen. Die ursprüngliche Datei muss eine Datei sein, die von der [InstallFiles-Aktion](installfiles-action.md)installiert wird.

Die duplicatefile-Tabelle weist die folgenden Spalten auf.



| Spalte      | Typ                         | Schlüssel | Nullwerte zulässig |
|-------------|------------------------------|-----|----------|
| Filekey     | [Bezeichner](identifier.md) | J   | N        |
| Komponente\_ | [Bezeichner](identifier.md) | N   | N        |
| Datei\_      | [Bezeichner](identifier.md) | N   | N        |
| Destname    | [Filename](filename.md)     | N   | J        |
| DestFolder  | [Bezeichner](identifier.md) | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="FileKey"></span><span id="filekey"></span><span id="FILEKEY"></span>Filekey
</dt> <dd>

Ein primärer Schlüssel, ein nicht lokalisiertes Token, das einen eindeutigen duplicatefile-Datensatz identifiziert.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Zulieferern\_
</dt> <dd>

Ein externer Schlüssel für die erste Spalte der [Komponenten Tabelle](component-table.md). Wenn die durch den Schlüssel identifizierte Komponente nicht für die Installation oder Entfernung ausgewählt ist, wird für diesen duplicatefile-Datensatz keine Aktion ausgeführt.

</dd> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Datei\_
</dt> <dd>

Der Fremdschlüssel in die Dateitabelle, die die ursprüngliche zu [duplizierende](file-table.md) Datei darstellt.

</dd> <dt>

<span id="DestName"></span><span id="destname"></span><span id="DESTNAME"></span>Destname
</dt> <dd>

Lokalisier barer Name, der an die doppelte Datei übergeben werden soll. Wenn dieses Feld leer ist, erhält die Zieldatei den gleichen Namen wie die ursprüngliche Datei.

</dd> <dt>

<span id="DestFolder"></span><span id="destfolder"></span><span id="DESTFOLDER"></span>DestFolder
</dt> <dd>

Der Name einer Eigenschaft, bei der es sich um den vollständigen Pfad handelt, in den die doppelte Datei kopiert werden soll. Wenn dieses Verzeichnis mit dem Verzeichnis identisch ist, das die ursprüngliche Datei enthält, und der Name für die vorgeschlagene doppelte Datei mit der ursprünglichen Datei identisch ist, findet keine Aktion statt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Tabelle wird von der [duplicatefiles-Aktion](duplicatefiles-action.md) und der [RemoveDuplicateFiles-Aktion](removeduplicatefiles-action.md)verarbeitet.

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE18](ice18.md)  
[ICE32](ice32.md)  
</dl>

 

 



