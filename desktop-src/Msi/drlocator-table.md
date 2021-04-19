---
description: Die drlocator-Tabelle enthält die Informationen, die erforderlich sind, um eine Datei oder ein Verzeichnis durchsuchen der Verzeichnisstruktur zu finden.
ms.assetid: 2b779ff7-f410-4af0-899d-4432b015d526
title: Drlocator-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78df5a5af83a18a14027b88033e977b2c63d2027
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346998"
---
# <a name="drlocator-table"></a>Drlocator-Tabelle

Die drlocator-Tabelle enthält die Informationen, die erforderlich sind, um eine Datei oder ein Verzeichnis durchsuchen der Verzeichnisstruktur zu finden.

Die drlocator-Tabelle weist die folgenden Spalten auf.



| Spalte      | Typ                         | Schlüssel | Nullwerte zulässig |
|-------------|------------------------------|-----|----------|
| Signatur\_ | [Bezeichner](identifier.md) | J   | N        |
| Parent      | [Bezeichner](identifier.md) | J   | J        |
| Pfad        | [Anypath](anypath.md)       | J   | J        |
| Tiefe       | [Integer](integer.md)       | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Unter\_
</dt> <dd>

Die Signatur \_ Spalte ist ein externer Schlüssel für die erste Spalte der [Signatur Tabelle](signature-table.md). Dieses Feld kann eine eindeutige Datei Signatur darstellen, die in der Signatur Tabelle aufgeführt ist. Wenn der Wert in dieser Spalte in der Signatur Tabelle nicht vorhanden ist, wird angenommen, dass es sich bei der Suche um ein Verzeichnis handelt, auf das von der drlocator-Tabelle verwiesen wird.

</dd> <dt>

<span id="Parent"></span><span id="parent"></span><span id="PARENT"></span>Übergeordneten
</dt> <dd>

Diese Spalte ist die Signatur des übergeordneten Verzeichnisses der Datei oder des Verzeichnisses in der \_ Spalte Signatur. Wenn dieses Feld NULL ist und die Path-Spalte nicht zu einem vollständigen Pfad erweitert wird, werden alle Festplattenlaufwerke des Benutzer Systems unter Verwendung des Pfads durchsucht.

Dieses Feld ist ein Schlüssel in einer der folgenden Tabellen: die Tabellen [reglocator](reglocator-table.md), [inilocator](inilocator-table.md), [complocator](complocator-table.md)oder drlocator.

</dd> <dt>

<span id="Path"></span><span id="path"></span><span id="PATH"></span>ADS
</dt> <dd>

Die Path-Spalte enthält den Pfad auf dem System des Benutzers. Dies ist entweder ein vollständiger Pfad oder ein relativer unter Pfad unterhalb des Verzeichnisses, das in der übergeordneten Spalte angegeben ist. Weitere Informationen finden Sie unter Einschränkungen für den [anypath](anypath.md) -Datentyp.

</dd> <dt>

<span id="Depth"></span><span id="depth"></span><span id="DEPTH"></span>Eingeh
</dt> <dd>

Die Tiefe unterhalb des Pfads, den das Installationsprogramm nach der in der Spalte Signatur angegebenen Datei oder dem Verzeichnis durchsucht \_ . Der im Feld Tiefe verwendete Wert basiert auf 0 (null). Wenn das Feld Pfad z. b. c:/Program Files/bin ist, muss die Spalte Tiefe auf 0 oder höher festgelegt werden, um eine Datei im Ordner bin zu erkennen. Wenn das tiefen Feld leer ist, wird davon ausgegangen, dass die Tiefe 0 (null) ist.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Tabelle wird mit der [AppSearch-Tabelle](appsearch-table.md)verwendet.

Die Spalten dieser Tabelle sind im Allgemeinen nicht lokalisiert. Wenn ein Autor eine Suche nach Produkten in mehreren Sprachen beschließt, muss für jede Sprache ein separater Eintrag in der Tabelle enthalten sein.

Weitere Informationen finden Sie [untersuchen nach vorhandenen Anwendungen, Dateien, Registrierungs Einträgen oder INI-Datei Einträgen](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE46](ice46.md)  
</dl>

 

 



