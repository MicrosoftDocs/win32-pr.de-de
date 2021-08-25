---
description: Die MIME-Tabelle ordnet einen MIME-Inhaltstyp einer Dateinamenerweiterung oder einer CLSID zu, um die Erweiterungs- oder COM-Serverinformationen zu generieren, die für die Ankündigung des MIME-Inhalts (Multipurpose Internet Mail Extensions) erforderlich sind.
ms.assetid: 5d452b24-ae04-4c45-8b3b-48e81f13a21e
title: MIME-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9e8a8f83499e286b63bf24dffa8858329231e74eec1f641588230da51578007
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913370"
---
# <a name="mime-table"></a>MIME-Tabelle

Die MIME-Tabelle ordnet einen MIME-Inhaltstyp einer Dateinamenerweiterung oder einer CLSID zu, um die Erweiterungs- oder COM-Serverinformationen zu generieren, die für die Ankündigung des MIME-Inhalts (Multipurpose Internet Mail Extensions) erforderlich sind.

Die MIME-Tabelle enthält die folgenden Spalten.



| Spalte      | Typ             | Key | Nullwerte zulässig |
|-------------|------------------|-----|----------|
| ContentType | [Text](text.md) | J   | N        |
| Durchwahl\_ | [Text](text.md) | N   | N        |
| CLSID       | [GUID](guid.md) | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="ContentType"></span><span id="contenttype"></span><span id="CONTENTTYPE"></span>Contenttype
</dt> <dd>

Diese Spalte ist ein Bezeichner für den MIME-Inhalt. Sie wird häufig in Form von Typ/Format geschrieben.

</dd> <dt>

<span id="Extension_"></span><span id="extension_"></span><span id="EXTENSION_"></span>Erweiterung\_
</dt> <dd>

Diese Spalte enthält die Servererweiterung, die dem MIME-Inhalt ohne den Punkt zugeordnet werden soll. Diese Spalte ist ein Fremdschlüssel in der [Erweiterungstabelle](extension-table.md). Die Tabelle Erweiterung enthält Informationen zum Dateinamenerweiterungsserver, die als Teil der Ankündigung verwendet werden.

</dd> <dt>

<span id="CLSID"></span><span id="clsid"></span>Clsid
</dt> <dd>

Diese Spalte enthält die COM-Server-CLSID, die dem MIME-Inhalt zugeordnet werden soll. Die CLSID in dieser Spalte kann ein Fremdschlüssel in der [Class-Tabelle](class-table.md) oder eine CLSID sein, die bereits auf dem Computer des Benutzers vorhanden ist. Die Tabelle Class enthält serverbezogene COM-Informationen, die als Teil der Ankündigung verwendet werden.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Auf diese Tabelle wird verwiesen, wenn die [RegisterMIMEInfo-Aktion](registermimeinfo-action.md) oder die [UnregisterMIMEInfo-Aktion](unregistermimeinfo-action.md) ausgeführt wird. Im Ankündigungsmodus registriert die Aktion RegisterMIMEInfo alle MIME-Informationen für Server aus der MIME-Tabelle, für die das entsprechende Feature aktiviert ist. Andernfalls registriert die Aktion MIME-Informationen für Server aus der MIME-Tabelle, für die das entsprechende Feature derzeit für die Installation ausgewählt ist. Mit [der Aktion UnregisterMIMEInfo](unregistermimeinfo-action.md) wird die Registrierung mimebezogener Registrierungsinformationen vom System aufgehoben. Durch die Aktion wird die Registrierung von MIME-Informationen für Server in der MIME-Tabelle aufgehoben, für die das entsprechende Feature derzeit für die Deinstallation ausgewählt ist.

## <a name="validation"></a>Überprüfung

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE15](ice15.md)  
[ICE32](ice32.md)  
</dl>

 

 



