---
description: In der filesfpcatalog-Tabelle werden angegebene Dateien den Katalogdateien zugeordnet, die vom Systemdatei Schutz verwendet werden.
ms.assetid: 70c8b64a-cf15-411c-8388-4a7e3051f45c
title: Filesfpcatalog-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2300b73cc1639d8a54e206ea609043cf657c91f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362371"
---
# <a name="filesfpcatalog-table"></a>Filesfpcatalog-Tabelle

In der filesfpcatalog-Tabelle werden angegebene Dateien den Katalogdateien zugeordnet, die vom Systemdatei Schutz verwendet werden.

**Windows Vista, Windows Server 2003 und Windows XP:** Nicht unterstützt.

Die filesfpcatalog-Tabelle weist die folgenden Spalten auf.



| Spalte       | Typ                         | Schlüssel | Nullwerte zulässig |
|--------------|------------------------------|-----|----------|
| Datei\_       | [Bezeichner](identifier.md) | J   | N        |
| Sfpcatalog\_ | [Filename](filename.md)     | J   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Datei\_
</dt> <dd>

Fremdschlüssel für die [Dateitabelle](file-table.md).

</dd> <dt>

<span id="SFPCatalog_"></span><span id="sfpcatalog_"></span><span id="SFPCATALOG_"></span>Sfpcatalog\_
</dt> <dd>

Fremdschlüssel für die [sfpcatalog-Tabelle](sfpcatalog-table.md).

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Mit der [Aktion installsfpcatalogfile](installsfpcatalogfile-action.md) werden die [Komponenten Tabelle](component-table.md), die [Dateitabelle](file-table.md), die filesfpcatalog-Tabelle und die [sfpcatalog-Tabelle](sfpcatalog-table.md)abgefragt.

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE66](ice66.md)  
[ICE76](ice76.md)  
</dl>

 

 



