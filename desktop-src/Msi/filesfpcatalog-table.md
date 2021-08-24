---
description: Die FileSFPCatalog-Tabelle ordnet die angegebenen Dateien den Katalogdateien zu, die vom Systemdateischutz verwendet werden.
ms.assetid: 70c8b64a-cf15-411c-8388-4a7e3051f45c
title: FileSFPCatalog-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41bec6e31cba93730cc65b04ffdfb4a509f0cd817ba709cc029edfb47c4c4e60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119581590"
---
# <a name="filesfpcatalog-table"></a>FileSFPCatalog-Tabelle

Die FileSFPCatalog-Tabelle ordnet die angegebenen Dateien den Katalogdateien zu, die vom Systemdateischutz verwendet werden.

**Windows Vista, Windows Server 2003 und Windows XP:** Wird nicht unterstützt.

Die FileSFPCatalog-Tabelle enthält die folgenden Spalten.



| Spalte       | Typ                         | Key | Nullwerte zulässig |
|--------------|------------------------------|-----|----------|
| Datei\_       | [Identifier](identifier.md) | J   | N        |
| SFPCatalog\_ | [Filename](filename.md)     | J   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Datei\_
</dt> <dd>

Fremdschlüssel für die [Dateitabelle](file-table.md).

</dd> <dt>

<span id="SFPCatalog_"></span><span id="sfpcatalog_"></span><span id="SFPCATALOG_"></span>SFPCatalog\_
</dt> <dd>

Fremdschlüssel für die [SFPCatalog-Tabelle](sfpcatalog-table.md).

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die [InstallSFPCatalogFile-Aktion](installsfpcatalogfile-action.md) fragt die [Komponententabelle,](component-table.md) [die Dateitabelle,](file-table.md)die FileSFPCatalog-Tabelle und die [SFPCatalog-Tabelle ab.](sfpcatalog-table.md)

## <a name="validation"></a>Überprüfung

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE66](ice66.md)  
[ICE76](ice76.md)  
</dl>

 

 



