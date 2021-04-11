---
description: Die MIME-Tabelle ordnet einen MIME-Inhaltstyp einer Dateinamenerweiterung oder einer CLSID zu, um die Erweiterung oder die com-Server Informationen zu generieren, die für die Ankündigung des MIME-Inhalts (Multipurpose Internet Mail Extensions) erforderlich sind.
ms.assetid: 5d452b24-ae04-4c45-8b3b-48e81f13a21e
title: MIME-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca11c8596e8f3735872c88668211953fc2b18b52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217346"
---
# <a name="mime-table"></a>MIME-Tabelle

Die MIME-Tabelle ordnet einen MIME-Inhaltstyp einer Dateinamenerweiterung oder einer CLSID zu, um die Erweiterung oder die com-Server Informationen zu generieren, die für die Ankündigung des MIME-Inhalts (Multipurpose Internet Mail Extensions) erforderlich sind.

Die MIME-Tabelle weist die folgenden Spalten auf.



| Spalte      | Typ             | Schlüssel | Nullwerte zulässig |
|-------------|------------------|-----|----------|
| ContentType | [Text](text.md) | J   | N        |
| Durchwahl\_ | [Text](text.md) | N   | N        |
| CLSID       | [GUID](guid.md) | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="ContentType"></span><span id="contenttype"></span><span id="CONTENTTYPE"></span>ContentType
</dt> <dd>

Diese Spalte ist ein Bezeichner für den MIME-Inhalt. Sie wird in der Regel in Form des Typs/Formats geschrieben.

</dd> <dt>

<span id="Extension_"></span><span id="extension_"></span><span id="EXTENSION_"></span>Weiterung\_
</dt> <dd>

Diese Spalte enthält die Server Erweiterung, die dem MIME-Inhalt ohne den Punkt zugeordnet werden soll. Diese Spalte ist ein Fremdschlüssel in der [Erweiterungs Tabelle](extension-table.md). Die Erweiterungs Tabelle enthält Informationen zum Dateinamen Erweiterungs Server, die als Teil der Ankündigung verwendet werden.

</dd> <dt>

<span id="CLSID"></span><span id="clsid"></span>CLSID
</dt> <dd>

Diese Spalte enthält die com-Server-CLSID, die dem MIME-Inhalt zugeordnet werden soll. Die CLSID in dieser Spalte kann ein Fremdschlüssel in die [Klassen Tabelle](class-table.md) oder eine CLSID sein, die bereits auf dem Computer des Benutzers vorhanden ist. Die Klassen Tabelle enthält com-Server bezogene Informationen, die als Teil der Ankündigung verwendet werden.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Tabelle wird beim Ausführen der [registermimeinfo-Aktion](registermimeinfo-action.md) oder der [unregistermimeinfo-Aktion](unregistermimeinfo-action.md) bezeichnet. Im Ankündigungs Modus werden von der registermimeinfo-Aktion alle MIME-Informationen für Server aus der MIME-Tabelle, für die das entsprechende Feature aktiviert ist, registriert. Andernfalls registriert die Aktion MIME-Informationen für Server aus der MIME-Tabelle, für die die entsprechende Funktion zurzeit für die Installation ausgewählt ist. Die [unregistermimeinfo-Aktion](unregistermimeinfo-action.md) hebt die Registrierung von MIME-bezogenen Registrierungsinformationen im System auf. Die-Aktion hebt die Registrierung von MIME-Informationen für Server aus der MIME-Tabelle auf, für die die entsprechende Funktion zurzeit zur Deinstallation ausgewählt ist.

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE15](ice15.md)  
[ICE32](ice32.md)  
</dl>

 

 



