---
description: Die removeinifile-Tabelle enthält die Informationen, die eine Anwendung aus einer INI-Datei löschen muss.
ms.assetid: 702cf86e-02f4-4ea7-8573-b500ac550aae
title: Removeinifile-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b57b4ba6f2c42ee636f1b9e21e798e27665f102a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369062"
---
# <a name="removeinifile-table"></a>Removeinifile-Tabelle

Die removeinifile-Tabelle enthält die Informationen, die eine Anwendung aus einer INI-Datei löschen muss.

Die removeinifile-Tabelle weist die folgenden Spalten auf.



| Spalte        | Typ                         | Schlüssel | Nullwerte zulässig |
|---------------|------------------------------|-----|----------|
| Removeinifile | [Bezeichner](identifier.md) | J   | N        |
| FileName      | [FileName](text.md)         | N   | N        |
| Dirproperty   | [Bezeichner](identifier.md) | N   | J        |
| `Section`       | [Großformatige](formatted.md)   | N   | N        |
| Schlüssel           | [Großformatige](formatted.md)   | N   | N        |
| Wert         | [Großformatige](formatted.md)   | N   | J        |
| Aktion        | [Integer](integer.md)       | N   | N        |
| Komponente\_   | [Bezeichner](identifier.md) | N   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="RemoveIniFile"></span><span id="removeinifile"></span><span id="REMOVEINIFILE"></span>Removeinifile
</dt> <dd>

Der Schlüssel für diese Tabelle.

</dd> <dt>

<span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Einfügen
</dt> <dd>

Der Name der INI-Datei, in der die Informationen gelöscht werden sollen.

</dd> <dt>

<span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>Dirproperty
</dt> <dd>

Der Name einer Eigenschaft, deren Wert in den vollständigen Pfad zum Ordner der zu entfernenden ini-Datei aufgelöst werden soll. Die-Eigenschaft kann der Name eines Verzeichnisses in der [Verzeichnis Tabelle](directory-table.md), eine Eigenschaft, die von der [AppSearch-Tabelle](appsearch-table.md)festgelegt wurde, oder eine beliebige andere Eigenschaft sein, die einen vollständigen Pfad darstellt.

</dd> <dt>

<span id="Section"></span><span id="section"></span><span id="SECTION"></span>Sektions
</dt> <dd>

Der lokalisierbare Abschnitt der INI-Datei.

</dd> <dt>

<span id="Key"></span><span id="key"></span><span id="KEY"></span>Wichtigen
</dt> <dd>

Der lokalisierbare ini-Datei Schlüssel unterhalb des Abschnitts.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Wert
</dt> <dd>

Der lokalisierbare Wert, der gelöscht werden soll. Der Wert ist erforderlich, wenn action den Wert 4 hat.

</dd> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Hinspiel
</dt> <dd>

Der Typ der Änderung, die vorgenommen werden soll.



| Konstante                         | Hexadezimal | Decimal | Bedeutung                          |
|----------------------------------|-------------|---------|----------------------------------|
| **msidbinifileaktionremoveline** | 0x002       | 2       | Löscht den Eintrag ". ini".              |
| **msidbinifileaktionremovetag**  | 0x004       | 4       | Löscht ein Tag aus einem INI-Eintrag. |



 

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Zulieferern\_
</dt> <dd>

Externer Schlüssel in erste Spalte der [Komponenten Tabelle](component-table.md) , die auf die Komponente verweist, die das Löschen des ini-Werts steuert.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Informationen der INI-Datei werden gelöscht, wenn die entsprechende Komponente zur Installation ausgewählt wurde, entweder lokal oder über die Quelle ausgeführt.

Diese Tabelle wird beim Ausführen der [RemoveIniValues-Aktion](removeinivalues-action.md) bezeichnet.

Wenn die Verzeichnis \_ Spalte als NULL angegeben wird, ist der Speicherort der INI-Datei der standardmäßige Windows-ini-Speicherort, der standardmäßig das Windows-Verzeichnis ist.

Wenn Sie den letzten Wert aus einem Abschnitt entfernen, wird dieser Abschnitt gelöscht. Es gibt keine andere Möglichkeit, einen vollständigen Abschnitt zu löschen, außer alle seine Werte zu entfernen.

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE40](ice40.md)  
[ICE46](ice46.md)  
[ICE69](ice69.md)  
</dl>

 

 



