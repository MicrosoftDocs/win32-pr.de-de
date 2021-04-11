---
description: Die IniFile-Tabelle enthält die ini-Informationen, die von der Anwendung in einer INI-Datei festgelegt werden müssen.
ms.assetid: fdb1a627-da6b-4da1-87a7-7f1c94d3836e
title: INIFILE-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d63ae37f7c8ed5c50b9b425b0462b445f7acb5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042144"
---
# <a name="inifile-table"></a>INIFILE-Tabelle

Die IniFile-Tabelle enthält die ini-Informationen, die von der Anwendung in einer INI-Datei festgelegt werden müssen.

Die IniFile-Tabelle weist die folgenden Spalten auf.



| Spalte      | Typ                         | Schlüssel | Nullwerte zulässig |
|-------------|------------------------------|-----|----------|
| INIFILE     | [Bezeichner](identifier.md) | J   | N        |
| FileName    | [FileName](text.md)         | N   | N        |
| Dirproperty | [Bezeichner](identifier.md) | N   | J        |
| `Section`     | [Großformatige](formatted.md)   | N   | N        |
| Schlüssel         | [Großformatige](formatted.md)   | N   | N        |
| Wert       | [Großformatige](formatted.md)   | N   | N        |
| Aktion      | [Integer](integer.md)       | N   | N        |
| Komponente\_ | [Bezeichner](identifier.md) | N   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="IniFile"></span><span id="inifile"></span><span id="INIFILE"></span>INIFILE
</dt> <dd>

Der Schlüssel für diese Tabelle.

</dd> <dt>

<span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Einfügen
</dt> <dd>

Der lokalisierbare Name der INI-Datei, in die die Informationen geschrieben werden sollen.

</dd> <dt>

<span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>Dirproperty
</dt> <dd>

Der Name einer Eigenschaft mit einem Wert, der in den vollständigen Pfad des Ordners aufgelöst wird, der die INI-Datei enthält. Die-Eigenschaft kann der Name eines Verzeichnisses in der [Verzeichnis Tabelle](directory-table.md), eine Eigenschaft, die von der [AppSearch-Tabelle](appsearch-table.md)festgelegt wurde, oder eine beliebige andere Eigenschaft sein, die einen vollständigen Pfad darstellt. Wenn dieses Feld leer bleibt, wird die INI-Datei im Ordner mit dem vollständigen Pfad erstellt, der von der [**windowsfolder**](windowsfolder.md) -Eigenschaft angegeben wird.

</dd> <dt>

<span id="Section"></span><span id="section"></span><span id="SECTION"></span>Sektions
</dt> <dd>

Der lokalisierbare Abschnitt der INI-Datei.

</dd> <dt>

<span id="Key"></span><span id="key"></span><span id="KEY"></span>Wichtigen
</dt> <dd>

Der lokalisierbare ini-Datei Schlüssel innerhalb des Abschnitts.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Wert
</dt> <dd>

Der lokalisierbare Wert, der geschrieben werden soll.

</dd> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Hinspiel
</dt> <dd>

Der Typ der Änderung, die vorgenommen werden soll.



| Konstante                         | Hexadezimal | Decimal | Modifikation (Modification)                                                                     |
|----------------------------------|-------------|---------|----------------------------------------------------------------------------------|
| **msidbinifileaktionaddline**    | 0x000       | 0       | Erstellt oder aktualisiert einen INI-Eintrag.                                                 |
| **msidbinifileaktionkreateline** | 0x001       | 1       | Erstellt einen INI-Eintrag nur, wenn der Eintrag nicht bereits vorhanden ist.                   |
| **msidbinifileaktionaddtag**     | 0x003       | 3       | Erstellt einen neuen Eintrag oder fügt einen neuen durch Trennzeichen getrennten Wert an einen vorhandenen Eintrag an. |



 

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Zulieferern\_
</dt> <dd>

Externer Schlüssel in die erste Spalte der [Komponenten Tabelle](component-table.md) , die auf die Komponente verweist, mit der die Installation des ini-Werts gesteuert wird.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Informationen der INI-Datei werden geschrieben, wenn die entsprechende Komponente als lokal oder von der Quelle ausgeführt installiert wurde.

Auf diese Tabelle wird verwiesen, wenn die Aktion " [Write](writeinivalues-action.md) " oder die [RemoveIniValues](removeinivalues-action.md) -Aktion ausgeführt wird.

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
[ICE69](ice69.md)  
[ICE88](ice88.md)  
[ICE91](ice91.md)  
</dl>

 

 



