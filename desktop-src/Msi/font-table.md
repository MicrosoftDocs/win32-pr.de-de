---
description: Die Schriftart Tabelle enthält die Informationen zum Registrieren von Schriftart Dateien beim System.
ms.assetid: 5ddff430-a6f8-473b-8006-ac0124469a99
title: Schriftart Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c10208c7b9a14ca7f311aff71653a53a3da9ed0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960055"
---
# <a name="font-table"></a>Schriftart Tabelle

Die Schriftart Tabelle enthält die Informationen zum Registrieren von Schriftart Dateien beim System.

Die Schriftart Tabelle enthält die folgenden Spalten.



| Spalte    | Typ                         | Schlüssel | Nullwerte zulässig |
|-----------|------------------------------|-----|----------|
| Datei\_    | [Bezeichner](identifier.md) | J   | N        |
| FontTitle | [Text](text.md)             | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Datei\_
</dt> <dd>

Externer Schlüssel in den [Datei Tabellen](file-table.md) Eintrag für die Schriftart Datei. Es wird empfohlen, dass für die Komponente mit der Schriftart Datei der Ordner "fontsfolder" in der Verzeichnis \_ Spalte der [Komponenten Tabelle](component-table.md)angegeben ist.

</dd> <dt>

<span id="FontTitle"></span><span id="fonttitle"></span><span id="FONTTITLE"></span>FontTitle
</dt> <dd>

Der Schriftart Name. Es wird empfohlen, dass Sie diese Spalte für TrueType-Schriftarten und TrueType-Auflistungen Null belassen, da das Installationsprogramm die Schriftart nach dem Lesen des richtigen Schriftart Titels aus der Schriftart Datei registrieren kann. Wenn der Schriftart Name eingegeben wird, muss er mit dem Schriftart Titel aus der Schriftart Datei identisch sein. Sie müssen einen Titel für Schriftarten angeben, die keine eingebetteten Namen haben, z. b.. FON-Dateien.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Tabelle wird beim Ausführen der [RegisterFonts-Aktion](registerfonts-action.md) oder der [unregisterfonts-Aktion](unregisterfonts-action.md) bezeichnet.

Wenn das FontTitle-Feld den Wert NULL hat, wird der Schriftart Name direkt aus der angegebenen Schriftart Datei gelesen. Wenn sich der in das FontTitle-Feld aufgezeichnete Schriftart Name von dem internen Schriftart Namen unterscheidet, der in der Schriftart Datei aufgezeichnet wurde, wird die Schriftart zweimal von der [RegisterFonts-Aktion](registerfonts-action.md)registriert.

Schriftart Dateien sollten nicht mit einer Sprach-ID erstellt werden, da die Schriftarten nicht über eine eingebettete Sprachen-ID-Ressource verfügen. Daher sollte die sprach Spalte der [Dateitabelle](file-table.md) für Schriftart Dateien Null belassen.

Da das Installationsprogramm Schriftart Dateien nicht standardmäßig neu anzählt, können bereits vorhandene Schriftart Dateien beim Deinstallieren einer Anwendung mit Ihrer Komponente entfernt werden. Um sicherzustellen, dass eine Schriftart Datei nicht entfernt wird, können Autoren die **msidbcomponentattributesshareddllrefcount** -oder **msidbcomponentattributestribute** -Bitflags \_ \_ \_ für die Komponente, die die Schriftart Datei enthält, in der Spalte Attribute der MSI-Komponenten Tabelle festlegen.

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE07](ice07.md)  
[ICE32](ice32.md)  
[ICE51](ice51.md)  
[ICE60](ice60.md)  
</dl>

 

 



