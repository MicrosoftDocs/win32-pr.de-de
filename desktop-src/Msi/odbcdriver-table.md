---
description: In der Tabelle ODBCDriver sind die ODBC-Treiber aufgeführt, die zur Installation gehören.
ms.assetid: 3518b370-0652-4b54-8057-9871365d5e8c
title: ODBCDriver-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a1eb0da3217d7466fc0beef90933c8a6af32e3d0551ecc6975a31ac55ed2730
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118943121"
---
# <a name="odbcdriver-table"></a>ODBCDriver-Tabelle

In der Tabelle ODBCDriver sind die ODBC-Treiber aufgeführt, die zur Installation gehören.

Die ODBCDriver-Tabelle enthält die folgenden Spalten.



| Spalte      | Typ                         | Key | Nullwerte zulässig |
|-------------|------------------------------|-----|----------|
| Treiber      | [Identifier](identifier.md) | J   | N        |
| Komponente\_ | [Identifier](identifier.md) | N   | N        |
| BESCHREIBUNG | [Text](text.md)             | N   | N        |
| Datei\_      | [Identifier](identifier.md) | N   | N        |
| \_Dateieinrichtung | [Identifier](identifier.md) | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Driver"></span><span id="driver"></span><span id="DRIVER"></span>Treiber
</dt> <dd>

Interner Tokenname für treiber. Ein Primärschlüssel für die Tabelle

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Komponente\_
</dt> <dd>

Externer Schlüssel in die Tabelle Komponente.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Beschreibung
</dt> <dd>

Die Beschreibung, die für diesen ODBC-Treiber registriert ist. Dieser Wert kann nicht lokalisiert werden.

</dd> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Datei\_
</dt> <dd>

Die DLL-Datei für Treiber, die in der Spalte Treiber aufgeführt sind. Die Spalte Datei \_ ist ein externer Schlüssel in der [Dateitabelle](file-table.md). Der in der Spalte Dateiname dieses Dateitabellendatensatzes eingegebene Dateiname muss das kurze Dateiformat aufweisen. Die \| SFN-LFN-Syntax kann nicht verwendet werden.

</dd> <dt>

<span id="File_Setup"></span><span id="file_setup"></span><span id="FILE_SETUP"></span>\_Dateieinrichtung
</dt> <dd>

Die Setup-DLL-Datei für den Treiber, wenn sie sich von Driver unterscheidet. Die Spalte Datei \_ ist ein externer Schlüssel in der [Dateitabelle](file-table.md). Der in der Spalte Dateiname dieses Dateitabellendatensatzes eingegebene Dateiname muss das kurze Dateiformat aufweisen. Die \| SFN-LFN-Syntax kann nicht verwendet werden.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die [Aktionen InstallODBC](installodbc-action.md) und [RemoveODBC](removeodbc-action.md) in [*Sequenztabellen*](s-gly.md) verarbeiten die Informationen in dieser Tabelle. Informationen zur Verwendung von *Sequenztabellen* finden Sie unter [Verwenden einer Sequenztabelle.](using-a-sequence-table.md)

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 



