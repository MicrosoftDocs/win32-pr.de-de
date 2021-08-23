---
description: Die Patchtabelle gibt die Datei an, die einen bestimmten Patch empfangen soll, und den physischen Speicherort der Patchdateien auf den Medienbildern.
ms.assetid: 1b624702-de25-4b1a-9dac-21f359ee97f7
title: Patchtabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9e5f41f206557589bf0b90d9ffb125a80d05d39ce809dc01a8e687a21045475
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119558460"
---
# <a name="patch-table"></a>Patchtabelle

Die Patchtabelle gibt die Datei an, die einen bestimmten Patch empfangen soll, und den physischen Speicherort der Patchdateien auf den Medienbildern.

Die Patch-Tabelle enthält die folgenden Spalten.



| Spalte      | Typ                               | Key | Nullwerte zulässig |
|-------------|------------------------------------|-----|----------|
| Datei\_      | [Identifier](identifier.md)       | J   | N        |
| Sequenz    | [Integer](integer.md)             | J   | N        |
| Patchgr÷▀e   | [DoubleInteger](doubleinteger.md) | N   | N        |
| Attribute  | [Integer](integer.md)             | N   | N        |
| Header      | [Binär (Binary)](binary.md)               | N   | J        |
| StreamRef\_ | [Identifier](identifier.md)       | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Datei\_
</dt> <dd>

Der Patch wird auf die Datei angewendet, die durch den Bezeichner in dieser Spalte angegeben wird. Dies ist ein Primärschlüssel für die Tabelle und ein Fremdschlüssel für die [Dateitabelle](file-table.md).

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequenz
</dt> <dd>

Dies ist die Position der Patchdatei in der Sequenzreihenfolge der Dateien auf den Medienbildern. Die Sequenzreihenfolge muss der Reihenfolge der Dateien in der Patchpaket-Cabinet-Datei entsprechen. Dies ist ein Primärschlüssel für diese Tabelle. Der maximale Grenzwert beträgt 3.2767 Dateien. Informationen zum Erstellen eines Windows Installer-Pakets mit mehr Dateien finden Sie unter [Erstellen eines großen Pakets.](authoring-a-large-package.md)

</dd> <dt>

<span id="PatchSize"></span><span id="patchsize"></span><span id="PATCHSIZE"></span>Patchgr÷▀e
</dt> <dd>

Diese Spalte gibt die Größe des Patches in Bytes an, die als lange ganze Zahl geschrieben wurden.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attribute
</dt> <dd>

Ganze Zahl, die Bitflags enthält, die Patchattribute darstellen. Fügen Sie den Wert 1 in diese Spalte ein, um anzugeben, dass der Fehler beim Anwenden dieses Patches kein schwerwiegender Fehler ist.



| Konstante                         | Hexadezimal | Decimal | Beschreibung                                                          |
|----------------------------------|-------------|---------|----------------------------------------------------------------------|
| (none)                           | 0x000       | 0       | Wenn dieser Patch nicht angewendet wird, ist dies ein schwerwiegender Fehler.                        |
| **msidbPatchAttributesNonVital** | 0x001       | 1       | Gibt an, dass der Fehler beim Anwenden dieses Patches kein schwerwiegender Fehler ist. |



 

</dd> <dt>

<span id="Header"></span><span id="header"></span><span id="HEADER"></span>Header
</dt> <dd>

Diese Spalte ist der binäre Streampatchheader, der für die Patchvalidierung verwendet wird. Diese Spalte sollte NULL sein, wenn die \_ StreamRef-Spalte nicht NULL ist. In diesem Fall wird der Patchheaderstream in der [Tabelle MsiPatchHeaders](msipatchheaders-table.md) gespeichert, um die Einschränkung des Streamnamens zu umgehen, die unter [OLE-Einschränkungen](ole-limitations-on-streams.md)für Streams.

</dd> <dt>

<span id="StreamRef_"></span><span id="streamref_"></span><span id="STREAMREF_"></span>StreamRef\_
</dt> <dd>

Externer Schlüssel in der MsiPatchHeaders-Tabelle, der die Zeile an gibt, die den Patchheaderstream enthält.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Tabelle wird von der [PatchFiles-Aktion verarbeitet.](patchfiles-action.md) Sie wird dem Installationspaket in der Regel durch eine Transformation aus einem Patchpaket hinzugefügt. Sie wird in der Regel nicht direkt in einem Installationspaket erstellt.

## <a name="validation"></a>Überprüfung

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE29](ice29.md)  
[ICE45](ice45.md)  
</dl>

 

 



