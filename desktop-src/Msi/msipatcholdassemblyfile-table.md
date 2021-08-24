---
description: Die Tabelle MsiPatchOldAssemblyFile bezieht eine Datei in der Tabelle File auf einen Assemblynamen in der Tabelle MsiPatchOldAssemblyName. Mehrere alte Assemblynamen können einer einzelnen Datei zugeordnet werden.
ms.assetid: a3c1e7fb-5f97-41db-bdc8-bd3ddb695c42
title: MsiPatchOldAssemblyFile-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4570b862773d2dc1d5b9c7458dbc1ccd8825ce77bf504d5e0fb2bf116d7a095
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119559080"
---
# <a name="msipatcholdassemblyfile-table"></a>MsiPatchOldAssemblyFile-Tabelle

Die Tabelle MsiPatchOldAssemblyFile bezieht eine Datei in der [Tabelle File](file-table.md) auf einen Assemblynamen in der [Tabelle MsiPatchOldAssemblyName.](msipatcholdassemblyname-table.md) Mehrere alte Assemblynamen können einer einzelnen Datei zugeordnet werden.

Die Tabelle MsiPatchOldAssemblyFile enthält die folgenden Spalten.



| Spalte     | Typ                         | Key | Nullwerte zulässig |
|------------|------------------------------|-----|----------|
| Datei\_     | [Identifier](identifier.md) | J   | N        |
| Assembly\_ | [Identifier](identifier.md) | J   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Datei\_
</dt> <dd>

Fremdschlüssel für die [Dateitabelle,](file-table.md) der die zu patchende Assembly angibt. Diese Spalte ist Teil des Primärschlüssels.

</dd> <dt>

<span id="Assembly_"></span><span id="assembly_"></span><span id="ASSEMBLY_"></span>Versammlung\_
</dt> <dd>

Fremdschlüssel für die [MsiPatchOldAssemblyName-Tabelle,](msipatcholdassemblyname-table.md) die einen der alten Assemblynamen für die Assembly identifiziert. Diese Spalte ist Teil des Primärschlüssels.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Windows Das Installationsprogramm verwendet die Tabelle MsiPatchOldAssemblyFile und die [Tabelle MsiPatchOldAssemblyName](msipatcholdassemblyname-table.md) beim Patchen von Assemblys, die im globalen Assemblycache (GAC) installiert sind. Beim Freigeben einer neueren Version einer Assembly wird der starke Name der Assembly geändert. Die beiden Tabellen identifizieren zusammen den alten Assemblynamen für eine aktualisierte Assembly. Dadurch kann der Installer den alten Assemblynamen verwenden, um die ursprüngliche Datei im GAC zu finden und einen binären Patch anzuwenden. Ohne diese Informationen muss das Installationsprogramm möglicherweise auf die ursprüngliche Installationsquelle zugreifen, um eine im GAC installierte Assembly zu patchen.

Die Tabelle MsiPatchOldAssemblyFile und [die Tabelle MsiPatchOldAssemblyName](msipatcholdassemblyname-table.md) werden nicht automatisch von [PatchWiz generiert.](patchwiz-dll.md) Das in der [Tabelle UpgradedImages](upgradedimages-table-patchwiz-dll-.md) angegebene Updatepaket muss diese Tabellen enthalten, damit der Patch über diese Informationen verfügen kann.

## <a name="validation"></a>Überprüfung

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 



