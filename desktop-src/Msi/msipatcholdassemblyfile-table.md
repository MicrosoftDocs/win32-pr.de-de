---
description: Die msipatcholdassemblyfile-Tabelle verknüpft eine Datei in der Dateitabelle mit einem Assemblynamen in der msipatcholdassemblyname-Tabelle. Mehrere alte Assemblynamen können einer einzelnen Datei zugeordnet werden.
ms.assetid: a3c1e7fb-5f97-41db-bdc8-bd3ddb695c42
title: Msipatcholdassemblyfile-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c995e4f6d6622dd3d7d1c96c9ef1297a787b66d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357074"
---
# <a name="msipatcholdassemblyfile-table"></a>Msipatcholdassemblyfile-Tabelle

Die msipatcholdassemblyfile-Tabelle verknüpft eine Datei in der [Dateitabelle](file-table.md) mit einem [Assemblynamen in der msipatcholdassemblyname-Tabelle](msipatcholdassemblyname-table.md). Mehrere alte Assemblynamen können einer einzelnen Datei zugeordnet werden.

Die msipatcholdassemblyfile-Tabelle weist die folgenden Spalten auf.



| Spalte     | Typ                         | Schlüssel | Nullwerte zulässig |
|------------|------------------------------|-----|----------|
| Datei\_     | [Bezeichner](identifier.md) | J   | N        |
| Assembly\_ | [Bezeichner](identifier.md) | J   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Datei\_
</dt> <dd>

Fremdschlüssel für die [Dateitabelle](file-table.md) , der die zu patchen Assembly angibt. Diese Spalte ist Teil des Primärschlüssels.

</dd> <dt>

<span id="Assembly_"></span><span id="assembly_"></span><span id="ASSEMBLY_"></span>Stadtverordneten\_
</dt> <dd>

Der Fremdschlüssel für die [msipatcholdassemblyname-Tabelle](msipatcholdassemblyname-table.md) , der einen der alten Assemblynamen für die Assembly identifiziert. Diese Spalte ist Teil des Primärschlüssels.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Beim Patchen von Assemblys, die im globalen Assemblycache (GAC) installiert sind, verwendet Windows Installer die Tabelle msipatcholdassemblyfile und die [Tabelle msipatcholdassemblyname](msipatcholdassemblyname-table.md) . Wenn eine neuere Version einer Assembly freigegeben wird, wird der starke Name der Assembly geändert. Die beiden Tabellen identifizieren den alten Assemblynamen für eine aktualisierte Assembly. Dadurch kann der Installer den alten Assemblynamen verwenden, um die ursprüngliche Datei im GAC zu suchen und einen binären Patch anzuwenden. Ohne diese Informationen muss das Installationsprogramm möglicherweise auf die ursprüngliche Installationsquelle zugreifen, um eine im GAC installierte Assembly zu patchen.

Die msipatcholdassemblyfile-Tabelle und die [msipatcholdassemblyname-Tabelle](msipatcholdassemblyname-table.md) werden nicht automatisch von [patchwiz](patchwiz-dll.md)generiert. Das Update Paket, das in der [Tabelle "UpgradedImages](upgradedimages-table-patchwiz-dll-.md) " angegeben ist, muss diese Tabellen enthalten, damit der Patch diese Informationen enthält.

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 



