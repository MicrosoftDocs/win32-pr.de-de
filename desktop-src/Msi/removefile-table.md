---
description: Die RemoveFile-Tabelle enthält eine Liste der Dateien, die von der RemoveFiles-Aktion entfernt werden sollen. Das Festlegen der FileName -Spalte dieser Tabelle auf NULL unterstützt das Entfernen leerer Ordner.
ms.assetid: 8b3cb0e3-ccc0-4030-8f57-aa124c3b5588
title: RemoveFile-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12cf63e9b7616eb033a696da2ad29cb4310e6dc0dc56279ef465c3c549cb5437
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082600"
---
# <a name="removefile-table"></a>RemoveFile-Tabelle

Die RemoveFile-Tabelle enthält eine Liste der Dateien, die von der [RemoveFiles-Aktion entfernt werden sollen.](removefiles-action.md) Das Festlegen der FileName -Spalte dieser Tabelle auf NULL unterstützt das Entfernen leerer Ordner.

Die RemoveFile-Tabelle enthält die folgenden Spalten.



| Spalte      | Typ                                     | Key | Nullwerte zulässig |
|-------------|------------------------------------------|-----|----------|
| FileKey     | [Identifier](identifier.md)             | J   | N        |
| Komponente\_ | [Identifier](identifier.md)             | N   | N        |
| FileName    | [WildCardFilename](wildcardfilename.md) | N   | J        |
| DirProperty | [Identifier](identifier.md)             | N   | N        |
| InstallMode | [Integer](integer.md)                   | N   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="FileKey"></span><span id="filekey"></span><span id="FILEKEY"></span>FileKey
</dt> <dd>

Primärschlüssel, der zum Identifizieren dieses bestimmten Tabelleneintrags verwendet wird.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Komponente\_
</dt> <dd>

Externer Schlüssel die erste Spalte der [Komponententabelle](component-table.md). Dieses Feld verweist auf die Komponente, die die zu entfernende Datei steuert.

</dd> <dt>

<span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Dateiname
</dt> <dd>

Diese Spalte enthält den lokalisierbaren Namen der zu entfernenden Datei. Wenn diese Spalte NULL ist, wird der angegebene Ordner entfernt, wenn er leer ist. Alle Dateien, die mit dem Platzhalter übereinstimmen, werden aus dem angegebenen Verzeichnis entfernt.

</dd> <dt>

<span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>DirProperty
</dt> <dd>

Der Name einer Eigenschaft, deren Wert in den vollständigen Pfad zum Ordner der zu entfernenden Datei aufzulösen ist. Die -Eigenschaft kann der Name [](directory-table.md)eines Verzeichnisses in der Directory-Tabelle, eine von der [AppSearch-Tabelle](appsearch-table.md)festgelegte Eigenschaft oder eine beliebige andere Eigenschaft sein, die einen vollständigen Pfad darstellt.

</dd> <dt>

<span id="InstallMode"></span><span id="installmode"></span><span id="INSTALLMODE"></span>InstallMode
</dt> <dd>

Dabei muss es sich um einen der folgenden Werte handeln.



| Konstante                                | Hexadezimal | Decimal | Beschreibung                                                                                                   |
|-----------------------------------------|-------------|---------|---------------------------------------------------------------------------------------------------------------|
| **msidbRemoveFileInstallModeOnInstall** | 0x001       | 1       | Entfernen Sie nur, wenn die zugeordnete Komponente installiert wird (msiInstallStateLocal oder msiInstallStateSource). |
| **msidbRemoveFileInstallModeOnRemove**  | 0x002       | 2       | Entfernen Sie nur, wenn die zugeordnete Komponente entfernt wird (msiInstallStateAbsent).                           |
| **msidbRemoveFileInstallModeOnBoth**    | 0x003       | 3       | Entfernen Sie in einem der oben genannten Fälle.                                                                          |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die Dateiverweise in dieser Tabelle werden von der [RemoveFiles-Aktion verarbeitet.](removefiles-action.md)

## <a name="validation"></a>Überprüfung

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE18](ice18.md)  
[ICE32](ice32.md)  
[ICE45](ice45.md)  
[ICE64](ice64.md)  
</dl>

 

 



