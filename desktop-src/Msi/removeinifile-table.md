---
description: Die RemoveIniFile-Tabelle enthält die Informationen, die eine Anwendung aus einer .ini löschen muss.
ms.assetid: 702cf86e-02f4-4ea7-8573-b500ac550aae
title: RemoveIniFile-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6aca38f320a8cb548faf00d284cff4c934e127a44cbaf7ca5b96013fac80d63
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074580"
---
# <a name="removeinifile-table"></a>RemoveIniFile-Tabelle

Die RemoveIniFile-Tabelle enthält die Informationen, die eine Anwendung aus einer .ini löschen muss.

Die RemoveIniFile-Tabelle enthält die folgenden Spalten.



| Spalte        | Typ                         | Key | Nullwerte zulässig |
|---------------|------------------------------|-----|----------|
| RemoveIniFile | [Identifier](identifier.md) | J   | N        |
| FileName      | [FileName](text.md)         | N   | N        |
| DirProperty   | [Identifier](identifier.md) | N   | J        |
| `Section`       | [Formatiert](formatted.md)   | N   | N        |
| Key           | [Formatiert](formatted.md)   | N   | N        |
| Wert         | [Formatiert](formatted.md)   | N   | J        |
| Aktion        | [Integer](integer.md)       | N   | N        |
| Komponente\_   | [Identifier](identifier.md) | N   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="RemoveIniFile"></span><span id="removeinifile"></span><span id="REMOVEINIFILE"></span>RemoveIniFile
</dt> <dd>

Der Schlüssel für diese Tabelle.

</dd> <dt>

<span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Dateiname
</dt> <dd>

Der .ini, in dem die Informationen gelöscht werden.

</dd> <dt>

<span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>DirProperty
</dt> <dd>

Der Name einer Eigenschaft, deren Wert in den vollständigen Pfad zum Ordner der zu entfernenden .ini wird. Die -Eigenschaft kann der Name [](directory-table.md)eines Verzeichnisses in der Directory-Tabelle, eine von der [AppSearch-Tabelle](appsearch-table.md)festgelegte Eigenschaft oder eine beliebige andere Eigenschaft sein, die einen vollständigen Pfad darstellt.

</dd> <dt>

<span id="Section"></span><span id="section"></span><span id="SECTION"></span>Abschnitt
</dt> <dd>

Der lokalisierbare .ini Dateiabschnitt.

</dd> <dt>

<span id="Key"></span><span id="key"></span><span id="KEY"></span>Schlüssel
</dt> <dd>

Der lokalisierbare .ini dateischlüssel unterhalb des Abschnitts.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Wert
</dt> <dd>

Der lokalisierbare Wert, der gelöscht werden soll. Der Wert ist erforderlich, wenn Aktion 4 ist.

</dd> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Aktion
</dt> <dd>

Der Typ der zu ändernden Änderung.



| Konstante                         | Hexadezimal | Decimal | Bedeutung                          |
|----------------------------------|-------------|---------|----------------------------------|
| **msidbIniFileActionRemoveLine** | 0x002       | 2       | Löscht .ini Eintrag.              |
| **msidbIniFileActionRemoveTag**  | 0x004       | 4       | Löscht ein Tag aus einem .ini Eintrag. |



 

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Komponente\_
</dt> <dd>

Externer Schlüssel in der ersten Spalte der [Component-Tabelle,](component-table.md) die auf die Komponente verweisen, die das Löschen des .ini steuert.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die .ini Dateiinformationen werden gelöscht, wenn die entsprechende Komponente für die Installation ausgewählt wurde, entweder lokal oder aus der Quelle ausgeführt.

Auf diese Tabelle wird verwiesen, wenn die [RemoveIniValues-Aktion](removeinivalues-action.md) ausgeführt wird.

Wenn die Spalte Verzeichnis als NULL angegeben wird, ist der Speicherort der ini-Datei der standarde Windows ini-Speicherort, Windows standardmäßig das Verzeichnis \_ ist.

Wenn Sie den letzten Wert aus einem Abschnitt entfernen, wird dieser Abschnitt gelöscht. Es gibt keine andere Möglichkeit, einen gesamten Abschnitt zu löschen, als alle Werte zu entfernen.

## <a name="validation"></a>Überprüfung

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE40](ice40.md)  
[ICE46](ice46.md)  
[ICE69](ice69.md)  
</dl>

 

 



