---
description: Die DrLocator-Tabelle enthält die Informationen, die zum Suchen einer Datei oder eines Verzeichnisses durch Durchsuchen der Verzeichnisstruktur erforderlich sind.
ms.assetid: 2b779ff7-f410-4af0-899d-4432b015d526
title: DrLocator-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe1765c7b8f5c38d5701c4c401eb333c7db6a7c403689b8c3100d55b5e51e28e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118378324"
---
# <a name="drlocator-table"></a>DrLocator-Tabelle

Die DrLocator-Tabelle enthält die Informationen, die zum Suchen einer Datei oder eines Verzeichnisses durch Durchsuchen der Verzeichnisstruktur erforderlich sind.

Die DrLocator-Tabelle enthält die folgenden Spalten.



| Spalte      | Typ                         | Key | Nullwerte zulässig |
|-------------|------------------------------|-----|----------|
| Signatur\_ | [Identifier](identifier.md) | J   | N        |
| Parent      | [Identifier](identifier.md) | J   | J        |
| Pfad        | [AnyPath](anypath.md)       | J   | J        |
| Tiefe       | [Integer](integer.md)       | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signatur\_
</dt> <dd>

Die Spalte Signatur \_ ist ein externer Schlüssel für die erste Spalte der [Signaturtabelle](signature-table.md). Dieses Feld kann eine eindeutige Dateisignatur darstellen, die in der Signaturtabelle aufgeführt ist. Wenn der Wert in dieser Spalte in der Signature-Tabelle nicht vorhanden ist, wird davon ausgegangen, dass die Suche nach einem Verzeichnis erfolgt, auf das von der DrLocator-Tabelle verwiesen wird.

</dd> <dt>

<span id="Parent"></span><span id="parent"></span><span id="PARENT"></span>Elternteil
</dt> <dd>

Diese Spalte ist die Signatur des übergeordneten Verzeichnisses der Datei oder des Verzeichnisses in der \_ Spalte Signatur. Wenn dieses Feld NULL ist und die Spalte Pfad nicht auf einen vollständigen Pfad erweitert wird, werden alle Festplattenlaufwerke des Systems des Benutzers mithilfe des Pfads durchsucht.

Dieses Feld ist ein Schlüssel in einer der folgenden Tabellen: [RegLocator,](reglocator-table.md) [IniLocator,](inilocator-table.md) [CompLocator](complocator-table.md)oder DrLocator.

</dd> <dt>

<span id="Path"></span><span id="path"></span><span id="PATH"></span>Pfad
</dt> <dd>

Die Spalte Path enthält den Pfad auf dem System des Benutzers. Dies ist entweder ein vollständiger Pfad oder ein relativer Unterpfad unterhalb des Verzeichnisses, das in der Spalte Parent angegeben ist. Sehen Sie sich die Einschränkungen für den [AnyPath-Datentyp](anypath.md) an.

</dd> <dt>

<span id="Depth"></span><span id="depth"></span><span id="DEPTH"></span>Tiefe
</dt> <dd>

Die Tiefe unter dem Pfad, den das Installationsprogramm nach der Datei oder dem Verzeichnis sucht, die bzw. das in der Spalte Signatur angegeben \_ ist. Der im Feld Tiefe verwendete Wert basiert auf 0 (null). Wenn das Feld Pfad z. B. c:/Programme/bin ist, muss die Spalte Tiefe auf 0 oder höher festgelegt werden, um eine Datei zu erkennen, die sich im Ordnerbehälter befindet. Wenn das Feld Tiefe leer ist, wird davon ausgegangen, dass die Tiefe 0 (null) ist.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Tabelle wird mit der [AppSearch-Tabelle](appsearch-table.md)verwendet.

Die Spalten dieser Tabelle sind im Allgemeinen nicht lokalisiert. Wenn ein Autor entscheidet, nach Produkten in mehreren Sprachen zu suchen, muss für jede Sprache ein separater Eintrag in der Tabelle enthalten sein.

Weitere Informationen finden Sie unter [Suchen nach vorhandenen Anwendungen, Dateien, Registrierungseinträgen oder .ini Dateieinträgen.](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE46](ice46.md)  
</dl>

 

 



