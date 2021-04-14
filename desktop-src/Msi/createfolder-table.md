---
description: Die Tabelle "| atefolder" enthält Verweise auf Ordner, die für eine bestimmte Komponente explizit erstellt werden müssen.
ms.assetid: b17b470b-6971-4124-8ec3-73914fdea95f
title: Tabelle "Buildordner"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc286b32b48e0db9e5b991ab10af663c51538bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217177"
---
# <a name="createfolder-table"></a>Tabelle "Buildordner"

Die Tabelle "| atefolder" enthält Verweise auf Ordner, die für eine bestimmte Komponente explizit erstellt werden müssen.

Die Tabelle "| atefolder" weist die folgenden Spalten auf.



| Spalte      | Typ                         | Schlüssel | Nullwerte zulässig |
|-------------|------------------------------|-----|----------|
| Verzeichnis\_ | [Bezeichner](identifier.md) | J   | N        |
| Komponente\_ | [Bezeichner](identifier.md) | J   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Befinden\_
</dt> <dd>

Externer Schlüssel in der ersten Spalte der [Verzeichnis Tabelle](directory-table.md).

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Zulieferern\_
</dt> <dd>

Externer Schlüssel in die erste Spalte der [Komponenten Tabelle](component-table.md).

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Ordner in dieser Tabelle werden bei der Installation der Komponente erstellt. Es wurde versucht, diese Ordner nur zu entfernen, wenn die Komponente deinstalliert oder in "Run-From-Source" verschoben wurde. Wenn die Ordner leer werden, wird keine automatische Entfernung ausgelöst. Im Gegensatz dazu werden Ordner, die vom Installer erstellt, aber nicht in dieser Tabelle aufgelistet werden, entfernt, wenn Sie leer sind.

Da Ordner, die vom Installationsprogramm erstellt werden, gelöscht werden, wenn Sie leer sind, müssen Sie einen Eintrag in der Tabelle "| atefolder" erstellen, um eine Komponente zu installieren, die aus einem leeren Ordner besteht.

Auf diese Tabelle wird verwiesen, wenn [die Aktion "die Aktion"](createfolders-action.md) oder " [RemoveFolders](removefolders-action.md) " aufgerufen wird.

Informationen zum Sichern eines Ordners finden Sie in der Tabelle " [msilockpermissionsex](msilockpermissionsex-table.md) " und der [Tabelle "lockberechtigungs](lockpermissions-table.md)Tabelle".

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE18](ice18.md)  
[ICE32](ice32.md)  
[ICE55](ice55.md)  
</dl>

 

 



