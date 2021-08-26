---
description: Die CreateFolder-Tabelle enthält Verweise auf Ordner, die explizit für eine bestimmte Komponente erstellt werden müssen.
ms.assetid: b17b470b-6971-4124-8ec3-73914fdea95f
title: CreateFolder-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c4cb926f6df388241a9c779328346a6e1bfb9fba4b365afce778c6e0b7a2548
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045090"
---
# <a name="createfolder-table"></a>CreateFolder-Tabelle

Die CreateFolder-Tabelle enthält Verweise auf Ordner, die explizit für eine bestimmte Komponente erstellt werden müssen.

Die CreateFolder-Tabelle enthält die folgenden Spalten.



| Spalte      | Typ                         | Key | Nullwerte zulässig |
|-------------|------------------------------|-----|----------|
| Verzeichnis\_ | [Identifier](identifier.md) | J   | N        |
| Komponente\_ | [Identifier](identifier.md) | J   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Verzeichnis\_
</dt> <dd>

Externer Schlüssel in der ersten Spalte der [Verzeichnistabelle](directory-table.md).

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Komponente\_
</dt> <dd>

Externer Schlüssel in der ersten Spalte der [Component-Tabelle.](component-table.md)

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die Ordner in dieser Tabelle werden erstellt, wenn die Komponente installiert wird. Es wird nur versucht, diese Ordner zu entfernen, wenn die Komponente deinstalliert oder in die Quelle "Run-from-Source" verschoben wird. Wenn die Ordner leer werden, wird kein automatisches Entfernen ausgelöst. Im Gegensatz dazu werden ordner, die vom Installationsprogramm erstellt, aber nicht in dieser Tabelle aufgeführt sind, entfernt, wenn sie leer werden.

Da vom Installationsprogramm erstellte Ordner gelöscht werden, wenn sie leer werden, müssen Sie einen Eintrag in der CreateFolder-Tabelle erstellen, um eine Komponente zu installieren, die aus einem leeren Ordner besteht.

Auf diese Tabelle wird verwiesen, wenn die [CreateFolders-Aktion](createfolders-action.md) oder die [RemoveFolders-Aktion](removefolders-action.md) aufgerufen wird.

Informationen zum Schützen eines Ordners finden Sie in der [MsiLockPermissionsEx-Tabelle](msilockpermissionsex-table.md) und [der LockPermissions-Tabelle.](lockpermissions-table.md)

## <a name="validation"></a>Überprüfung

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE18](ice18.md)  
[ICE32](ice32.md)  
[ICE55](ice55.md)  
</dl>

 

 



