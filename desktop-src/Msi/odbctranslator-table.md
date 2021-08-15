---
description: In der ODBCTranslator-Tabelle sind die ODBC-Translators aufgeführt, die zur Installation gehören.
ms.assetid: fecb7454-29bb-4ddf-b4d5-2e56c20ff2dc
title: ODBCTranslator-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd59c535963b3c42e94c8c904d448540072913b56bedb58c3e0bddc72dd6c6c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118942891"
---
# <a name="odbctranslator-table"></a>ODBCTranslator-Tabelle

In der ODBCTranslator-Tabelle sind die ODBC-Translators aufgeführt, die zur Installation gehören.

Die ODBCTranslator-Tabelle enthält die folgenden Spalten.



| Spalte      | Typ                         | Key | Nullwerte zulässig |
|-------------|------------------------------|-----|----------|
| Übersetzer  | [Identifier](identifier.md) | J   | N        |
| Komponente\_ | [Identifier](identifier.md) | N   | N        |
| BESCHREIBUNG | [Text](text.md)             | N   | N        |
| Datei\_      | [Identifier](identifier.md) | N   | N        |
| \_Dateieinrichtung | [Identifier](identifier.md) | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Translator"></span><span id="translator"></span><span id="TRANSLATOR"></span>Translator
</dt> <dd>

Interner Tokenname für Translator. Ein Primärschlüssel für die Tabelle.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Komponente\_
</dt> <dd>

Externer Schlüssel in die Tabelle Komponente.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Beschreibung
</dt> <dd>

Die Für diesen ODBC-Treiberübersetzungs-Translator registrierte Beschreibung. Dieser Wert kann nicht lokalisiert werden.

</dd> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Datei\_
</dt> <dd>

Die DLL-Datei für die Übertragung, die in der spalte Translator aufgeführt ist. Die Spalte Datei \_ ist ein externer Schlüssel in der [Dateitabelle](file-table.md). Der in der Spalte Dateiname dieses Dateitabellendatensatzes eingegebene Dateiname muss das kurze Dateiformat aufweisen. Die \| SFN-LFN-Syntax kann nicht verwendet werden.

</dd> <dt>

<span id="File_Setup"></span><span id="file_setup"></span><span id="FILE_SETUP"></span>\_Dateieinrichtung
</dt> <dd>

Die Setup-DLL-Datei für den Translator, wenn sie sich von der spalte Translator unterscheidet. Die Spalte Datei \_ ist ein externer Schlüssel in der [Dateitabelle](file-table.md). Der in der Spalte Dateiname dieses Dateitabellendatensatzes eingegebene Dateiname muss das kurze Dateiformat aufweisen. Die \| SFN-LFN-Syntax kann nicht verwendet werden.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die [Aktionen InstallODBC](installodbc-action.md) und [RemoveODBC](removeodbc-action.md) in [*Sequenztabellen*](s-gly.md) verarbeiten die Informationen in dieser Tabelle. Informationen zur Verwendung von *Sequenztabellen* finden Sie unter [Verwenden einer Sequenztabelle.](using-a-sequence-table.md)

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 



