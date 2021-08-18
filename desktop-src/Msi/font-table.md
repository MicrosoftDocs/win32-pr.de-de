---
description: Die Tabelle Schriftart enthält die Informationen zum Registrieren von Schriftartdateien beim System.
ms.assetid: 5ddff430-a6f8-473b-8006-ac0124469a99
title: Schriftarttabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65efb786d4379bbe14fec0239cd8f3edee50f1b79a6413904b6e00331bc49a25
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118946981"
---
# <a name="font-table"></a>Schriftarttabelle

Die Tabelle Schriftart enthält die Informationen zum Registrieren von Schriftartdateien beim System.

Die Tabelle Font enthält die folgenden Spalten.



| Spalte    | Typ                         | Key | Nullwerte zulässig |
|-----------|------------------------------|-----|----------|
| Datei\_    | [Identifier](identifier.md) | J   | N        |
| FontTitle | [Text](text.md)             | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Datei\_
</dt> <dd>

Externer Schlüssel in den [Dateitabelleneintrag](file-table.md) für die Schriftartdatei. Es wird empfohlen, dass für die Komponente, die die Schriftartdatei enthält, der in der Directory -Spalte der \_ [Component-Tabelle angegebene FontsFolder angegeben ist.](component-table.md)

</dd> <dt>

<span id="FontTitle"></span><span id="fonttitle"></span><span id="FONTTITLE"></span>FontTitle
</dt> <dd>

Schriftartname. Es wird empfohlen, diese Spalte für TrueType-Schriftarten und TrueType-Auflistungen null zu lassen, da das Installationsprogramm die Schriftart registrieren kann, nachdem der richtige Schriftarttitel aus der Schriftartdatei gelesen wurde. Wenn der Schriftartname eingegeben wird, muss er mit dem Titel der Schriftart aus der Schriftartdatei identisch sein. Sie müssen einen Titel für Schriftarten angeben, die keine eingebetteten Namen haben, z. B. FON-Dateien.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Auf diese Tabelle wird verwiesen, wenn die [RegisterFonts-Aktion](registerfonts-action.md) oder die [UnregisterFonts-Aktion](unregisterfonts-action.md) ausgeführt wird.

Wenn das FontTitle-Feld null gelassen wird, wird der Schriftartname direkt aus der angegebenen Schriftartdatei gelesen. Wenn sich der im Feld FontTitle aufgezeichnete Schriftartname vom internen Schriftartnamen unterscheidet, der in der Schriftartdatei aufgezeichnet wurde, wird die Schriftart zweimal von der [RegisterFonts-Aktion registriert.](registerfonts-action.md)

Schriftartdateien sollten nicht mit einer Sprach-ID verfasst werden, da Schriftarten keine eingebettete Sprach-ID-Ressource haben. Daher sollte die Spalte Language der [Tabelle File](file-table.md) für Schriftartdateien NULL bleiben.

Da das Installationsprogramm schriftartendateien standardmäßig nicht aufzählt, können bereits vorhandene Schriftartdateien mit ihrer Komponente entfernt werden, wenn eine Anwendung deinstalliert wird. Um sicherzustellen, dass eine Schriftartdatei nicht entfernt wird, können Autoren die **Bitflags msidbComponentAttributesSharedDllRefCount** oder **msidbComponentAttributesPermanent** in der Spalte Attribute der Msi-Komponententabelle der Komponententabelle für die Komponente festlegen, die die \_ \_ \_ Schriftartdatei enthält.

## <a name="validation"></a>Überprüfung

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE07](ice07.md)  
[ICE32](ice32.md)  
[ICE51](ice51.md)  
[ICE60](ice60.md)  
</dl>

 

 



