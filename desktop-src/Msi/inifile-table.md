---
description: Die IniFile-Tabelle enthält die .ini, die die Anwendung in einer Datei .ini muss.
ms.assetid: fdb1a627-da6b-4da1-87a7-7f1c94d3836e
title: IniFile-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4cd12c02fa0123ac9e1a763b4e725681e6c6b1d51a331a1efea9916b5ac4cbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118946567"
---
# <a name="inifile-table"></a>IniFile-Tabelle

Die IniFile-Tabelle enthält die .ini, die die Anwendung in einer Datei .ini muss.

Die IniFile-Tabelle enthält die folgenden Spalten.



| Spalte      | Typ                         | Key | Nullwerte zulässig |
|-------------|------------------------------|-----|----------|
| IniFile     | [Identifier](identifier.md) | J   | N        |
| FileName    | [FileName](text.md)         | N   | N        |
| DirProperty | [Identifier](identifier.md) | N   | J        |
| `Section`     | [Formatiert](formatted.md)   | N   | N        |
| Key         | [Formatiert](formatted.md)   | N   | N        |
| Wert       | [Formatiert](formatted.md)   | N   | N        |
| Aktion      | [Integer](integer.md)       | N   | N        |
| Komponente\_ | [Identifier](identifier.md) | N   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="IniFile"></span><span id="inifile"></span><span id="INIFILE"></span>IniFile
</dt> <dd>

Der Schlüssel für diese Tabelle.

</dd> <dt>

<span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Dateiname
</dt> <dd>

Der lokalisierbare Name der .ini, in die die Informationen geschrieben werden.

</dd> <dt>

<span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>DirProperty
</dt> <dd>

Name einer Eigenschaft mit einem Wert, der in den vollständigen Pfad des Ordners mit der .ini wird. Die -Eigenschaft kann der Name [](directory-table.md)eines Verzeichnisses in der Directory-Tabelle, eine von der [AppSearch-Tabelle](appsearch-table.md)festgelegte Eigenschaft oder eine beliebige andere Eigenschaft sein, die einen vollständigen Pfad darstellt. Wenn dieses Feld leer gelassen wird, wird die .ini-Datei in dem Ordner mit dem vollständigen Pfad erstellt, der von der [**WindowsFolder-Eigenschaft angegeben**](windowsfolder.md) wird.

</dd> <dt>

<span id="Section"></span><span id="section"></span><span id="SECTION"></span>Abschnitt
</dt> <dd>

Der abschnitt lokalisierbare .ini Datei.

</dd> <dt>

<span id="Key"></span><span id="key"></span><span id="KEY"></span>Schlüssel
</dt> <dd>

Der lokalisierbare .ini dateischlüssel innerhalb des Abschnitts.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Wert
</dt> <dd>

Der lokalisierbare Wert, der geschrieben werden soll.

</dd> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Aktion
</dt> <dd>

Der Typ der zu ändernden Änderung.



| Konstante                         | Hexadezimal | Decimal | Modifikation (Modification)                                                                     |
|----------------------------------|-------------|---------|----------------------------------------------------------------------------------|
| **msidbIniFileActionAddLine**    | 0x000       | 0       | Erstellt oder aktualisiert einen .ini Eintrag.                                                 |
| **msidbIniFileActionCreateLine** | 0x001       | 1       | Erstellt einen .ini Eintrag nur, wenn der Eintrag noch nicht vorhanden ist.                   |
| **msidbIniFileActionAddTag**     | 0x003       | 3       | Erstellt einen neuen Eintrag oder fügt einen neuen durch Komma getrennten Wert an einen vorhandenen Eintrag an. |



 

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Komponente\_
</dt> <dd>

Externer Schlüssel in der ersten Spalte der [Tabelle Komponente,](component-table.md) die auf die Komponente verweisen, die die Installation des .ini steuert.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die .ini Dateiinformationen werden geschrieben, wenn die entsprechende Komponente ausgewählt wurde, um als lokal installiert oder aus der Quelle ausgeführt zu werden.

Auf diese Tabelle wird verwiesen, wenn die [WriteIniValues-Aktion](writeinivalues-action.md) oder die [RemoveIniValues-Aktion](removeinivalues-action.md) ausgeführt wird.

## <a name="validation"></a>Überprüfung

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
[ICE69](ice69.md)  
[ICE88](ice88.md)  
[ICE91](ice91.md)  
</dl>

 

 



