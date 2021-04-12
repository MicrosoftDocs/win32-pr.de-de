---
description: Die msipatcholdassemblyname-Tabelle gibt den alten Namen für eine Assembly an.
ms.assetid: e9f22ba1-6be4-4382-abe5-5cfdc68c0855
title: Msipatcholdassemblyname-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee301801efc1618f84794c48172aff47734b38d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347348"
---
# <a name="msipatcholdassemblyname-table"></a>Msipatcholdassemblyname-Tabelle

Die msipatcholdassemblyname-Tabelle gibt den alten Namen für eine Assembly an.

Die msipatcholdassemblyname-Tabelle weist die folgenden Spalten auf.



| Spalte   | Typ                         | Schlüssel | Nullwerte zulässig |
|----------|------------------------------|-----|----------|
| Assembly | [Bezeichner](identifier.md) | J   | N        |
| Name     | [Text](text.md)             | J   | N        |
| Wert    | [Text](text.md)             | N   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Assembly"></span><span id="assembly"></span><span id="ASSEMBLY"></span>Stadtverordneten
</dt> <dd>

Eindeutiger Bezeichner für den alten Assemblynamen. Dieser Schlüssel wird als Zuordnung zwischen dieser und der Tabelle " [msipatcholdassemblyfile](msipatcholdassemblyfile-table.md)" verwendet.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Benennen
</dt> <dd>

Der Name des Attributs, das dem in der Spalte Wert angegebenen Wert zugeordnet ist.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Wert
</dt> <dd>

Der Wert, der dem in der Spalte Name angegebenen Namen zugeordnet ist.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Beim Patchen von Assemblys, die im globalen Assemblycache (GAC) installiert sind, verwendet Windows Installer die Tabelle [msipatcholdassemblyfile](msipatcholdassemblyfile-table.md) und die Tabelle msipatcholdassemblyname. Wenn eine neuere Version einer Assembly freigegeben wird, wird der starke Name der Assembly geändert. Die beiden Tabellen identifizieren den alten Assemblynamen für eine aktualisierte Assembly. Dadurch kann der Installer den alten Assemblynamen verwenden, um die ursprüngliche Datei im GAC zu suchen und einen binären Patch anzuwenden. Ohne diese Informationen muss das Installationsprogramm möglicherweise auf die ursprüngliche Installationsquelle zugreifen, um eine im GAC installierte Assembly zu patchen.

Die [msipatcholdassemblyfile-Tabelle](msipatcholdassemblyfile-table.md) und die msipatcholdassemblyname-Tabelle werden nicht automatisch von [patchwiz](patchwiz-dll.md)generiert. Das Update Paket, das in der [Tabelle "UpgradedImages](upgradedimages-table-patchwiz-dll-.md) " angegeben ist, muss diese Tabellen enthalten, damit der Patch diese Informationen enthält.

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 



