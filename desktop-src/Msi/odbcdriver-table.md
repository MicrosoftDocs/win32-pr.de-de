---
description: In der odbcdriver-Tabelle werden die ODBC-Treiber aufgelistet, die zur Installation gehören.
ms.assetid: 3518b370-0652-4b54-8057-9871365d5e8c
title: Odbcdriver-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3257f3eec5b60191df727d156572293489aa1956
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525781"
---
# <a name="odbcdriver-table"></a>Odbcdriver-Tabelle

In der odbcdriver-Tabelle werden die ODBC-Treiber aufgelistet, die zur Installation gehören.

Die odbcdriver-Tabelle weist die folgenden Spalten auf.



| Spalte      | Typ                         | Schlüssel | Nullwerte zulässig |
|-------------|------------------------------|-----|----------|
| Treiber      | [Bezeichner](identifier.md) | J   | N        |
| Komponente\_ | [Bezeichner](identifier.md) | N   | N        |
| BESCHREIBUNG | [Text](text.md)             | N   | N        |
| Datei\_      | [Bezeichner](identifier.md) | N   | N        |
| Datei \_ Einrichtung | [Bezeichner](identifier.md) | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Driver"></span><span id="driver"></span><span id="DRIVER"></span>Trei
</dt> <dd>

Interner Tokenname für den Treiber. Ein Primärschlüssel für die Tabelle

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Zulieferern\_
</dt> <dd>

Externer Schlüssel in der Komponenten Tabelle.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Beschreibung
</dt> <dd>

Die Beschreibung, die für diesen ODBC-Treiber registriert ist. Dieser Wert kann nicht lokalisiert werden.

</dd> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Datei\_
</dt> <dd>

Die DLL-Datei für Treiber, die in der Spalte Treiber aufgeführt sind. Die Datei \_ Spalte ist ein externer Schlüssel in der [Dateitabelle](file-table.md). Der Dateiname, der in der Dateiname-Spalte dieses Datei Tabellendaten Satzes eingegeben wird, muss das Kurznamen Format aufweisen. Die SFN- \| LFN-Syntax kann nicht verwendet werden.

</dd> <dt>

<span id="File_Setup"></span><span id="file_setup"></span><span id="FILE_SETUP"></span>Datei \_ Einrichtung
</dt> <dd>

Die Setup-DLL-Datei für den Treiber, wenn dieser sich von dem Treiber unterscheidet. Die Datei \_ Spalte ist ein externer Schlüssel in der [Dateitabelle](file-table.md). Der Dateiname, der in der Dateiname-Spalte dieses Datei Tabellendaten Satzes eingegeben wird, muss das Kurznamen Format aufweisen. Die SFN- \| LFN-Syntax kann nicht verwendet werden.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Informationen in dieser Tabelle werden durch die [installlodbc](installodbc-action.md) -und [removeodbc](removeodbc-action.md) -Aktionen in [*Sequenz Tabellen*](s-gly.md) verarbeitet. Weitere Informationen zum Verwenden von *Sequenz Tabellen* finden Sie unter [Verwenden einer Sequenz Tabelle](using-a-sequence-table.md).

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 



