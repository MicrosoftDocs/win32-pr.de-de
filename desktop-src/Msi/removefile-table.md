---
description: Die Tabelle RemoveFile enthält eine Liste der Dateien, die von der RemoveFiles-Aktion entfernt werden sollen. Wenn die FileName-Spalte dieser Tabelle auf NULL festgelegt wird, wird die Entfernung leerer Ordner unterstützt.
ms.assetid: 8b3cb0e3-ccc0-4030-8f57-aa124c3b5588
title: RemoveFile-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 723e42582821d79842686678c5b310e95cd1e944
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866715"
---
# <a name="removefile-table"></a>RemoveFile-Tabelle

Die Tabelle RemoveFile enthält eine Liste der Dateien, die von der [RemoveFiles-Aktion](removefiles-action.md)entfernt werden sollen. Wenn die FileName-Spalte dieser Tabelle auf NULL festgelegt wird, wird die Entfernung leerer Ordner unterstützt.

Die RemoveFile-Tabelle weist die folgenden Spalten auf.



| Spalte      | Typ                                     | Schlüssel | Nullwerte zulässig |
|-------------|------------------------------------------|-----|----------|
| Filekey     | [Bezeichner](identifier.md)             | J   | N        |
| Komponente\_ | [Bezeichner](identifier.md)             | N   | N        |
| FileName    | [Platzhalter Dateiname](wildcardfilename.md) | N   | J        |
| Dirproperty | [Bezeichner](identifier.md)             | N   | N        |
| InstallMode | [Integer](integer.md)                   | N   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="FileKey"></span><span id="filekey"></span><span id="FILEKEY"></span>Filekey
</dt> <dd>

Der Primärschlüssel, der zum Identifizieren dieses bestimmten Tabellen Eintrags verwendet wird.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Zulieferern\_
</dt> <dd>

Externer Schlüssel die erste Spalte der [Komponenten Tabelle](component-table.md). Dieses Feld verweist auf die Komponente, mit der die zu entfernende Datei gesteuert wird.

</dd> <dt>

<span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Einfügen
</dt> <dd>

Diese Spalte enthält den lokalisierbaren Namen der zu entfernenden Datei. Wenn diese Spalte NULL ist, wird der angegebene Ordner entfernt, wenn er leer ist. Alle Dateien, die dem Platzhalter entsprechen, werden aus dem angegebenen Verzeichnis entfernt.

</dd> <dt>

<span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>Dirproperty
</dt> <dd>

Der Name einer Eigenschaft, deren Wert in den vollständigen Pfad zum Ordner der zu entfernenden Datei aufgelöst werden soll. Die-Eigenschaft kann der Name eines Verzeichnisses in der [Verzeichnis Tabelle](directory-table.md), eine Eigenschaft, die von der [AppSearch-Tabelle](appsearch-table.md)festgelegt wurde, oder eine beliebige andere Eigenschaft sein, die einen vollständigen Pfad darstellt.

</dd> <dt>

<span id="InstallMode"></span><span id="installmode"></span><span id="INSTALLMODE"></span>' Installmode '
</dt> <dd>

Muss einen der folgenden Werte aufweisen.



| Konstante                                | Hexadezimal | Decimal | BESCHREIBUNG                                                                                                   |
|-----------------------------------------|-------------|---------|---------------------------------------------------------------------------------------------------------------|
| **msidbremuvefileinstallmodeoninstall** | 0x001       | 1       | Entfernen Sie nur, wenn die zugehörige Komponente installiert wird (msiinstallstatelocal oder msiinstallstaatource). |
| **msidbremuvefileinstallmodeonremove**  | 0x002       | 2       | Nur entfernen, wenn die zugeordnete Komponente entfernt wird (msiinstallstatemissing).                           |
| **msidbremuvefileinstallmodeonboth**    | 0x003       | 3       | Entfernen Sie in einem der obigen Fälle.                                                                          |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Datei Verweise in dieser Tabelle werden von der [RemoveFiles-Aktion](removefiles-action.md)verarbeitet.

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE18](ice18.md)  
[ICE32](ice32.md)  
[ICE45](ice45.md)  
[ICE64](ice64.md)  
</dl>

 

 



