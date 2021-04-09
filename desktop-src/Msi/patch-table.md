---
description: In der patchtabelle ist die Datei angegeben, die einen bestimmten Patch und den physischen Speicherort der Patchdateien auf den Medien Images erhalten soll.
ms.assetid: 1b624702-de25-4b1a-9dac-21f359ee97f7
title: Patchtabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 061b2082f88a8c7c3967652900bb6bf6e1c29802
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760152"
---
# <a name="patch-table"></a>Patchtabelle

In der patchtabelle ist die Datei angegeben, die einen bestimmten Patch und den physischen Speicherort der Patchdateien auf den Medien Images erhalten soll.

Die patchtabelle enthält die folgenden Spalten.



| Spalte      | Typ                               | Schlüssel | Nullwerte zulässig |
|-------------|------------------------------------|-----|----------|
| Datei\_      | [Bezeichner](identifier.md)       | J   | N        |
| Sequenz    | [Integer](integer.md)             | J   | N        |
| Patchgröße   | [Doubleiteger](doubleinteger.md) | N   | N        |
| Attribute  | [Integer](integer.md)             | N   | N        |
| Header      | [Binär (Binary)](binary.md)               | N   | J        |
| Streamref\_ | [Bezeichner](identifier.md)       | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Datei\_
</dt> <dd>

Der Patch wird auf die Datei angewendet, die durch den Bezeichner in dieser Spalte angegeben wird. Dies ist ein Primärschlüssel für die Tabelle, und es handelt sich um einen Fremdschlüssel für die [Dateitabelle](file-table.md).

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequenz
</dt> <dd>

Dies ist die Position der Patchdatei in der Reihenfolge der Dateien auf den Medienbildern. Die Reihenfolge der Reihenfolge muss der Reihenfolge der Dateien in der Datei mit dem Patchpaketdatei entsprechen. Dies ist ein Primärschlüssel für diese Tabelle. Der Höchstwert beträgt 32767 Dateien. zum Erstellen eines Windows Installer Pakets mit weiteren Dateien finden Sie unter Erstellen [eines großen Pakets](authoring-a-large-package.md)Weitere Informationen.

</dd> <dt>

<span id="PatchSize"></span><span id="patchsize"></span><span id="PATCHSIZE"></span>Patchgröße
</dt> <dd>

Diese Spalte gibt die Größe des Patches in Bytes an, die als Long Integer-Wert geschrieben werden.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Legt
</dt> <dd>

Ganze Zahl mit Bitflags, die Patchattribute darstellen. Fügen Sie in dieser Spalte den Wert 1 ein, um anzugeben, dass der Fehler beim Anwenden dieses Patches kein schwerwiegender Fehler ist.



| Konstante                         | Hexadezimal | Decimal | BESCHREIBUNG                                                          |
|----------------------------------|-------------|---------|----------------------------------------------------------------------|
| (none)                           | 0x000       | 0       | Ein Fehler beim Anwenden dieses Patches ist ein schwerwiegender Fehler.                        |
| **msidbpatchattributesnonvital** | 0x001       | 1       | Gibt an, dass der Fehler beim Anwenden dieses Patches kein schwerwiegender Fehler ist. |



 

</dd> <dt>

<span id="Header"></span><span id="header"></span><span id="HEADER"></span>Header
</dt> <dd>

Diese Spalte ist der binäre Stream-patchheader, der für die patchvalidierung verwendet wird. Diese Spalte sollte NULL sein, wenn die streamref- \_ Spalte nicht NULL ist. In diesem Fall wird der patchheader-Stream in der [msipatchheaders-Tabelle](msipatchheaders-table.md) gespeichert, um die in [OLE-Einschränkungen für Streams](ole-limitations-on-streams.md)beschriebene Einschränkung für den Datenstrom Namen zu überwinden.

</dd> <dt>

<span id="StreamRef_"></span><span id="streamref_"></span><span id="STREAMREF_"></span>Streamref\_
</dt> <dd>

Externer Schlüssel in die msipatchheaders-Tabelle, die die Zeile angibt, die den patchheader-Stream enthält.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Tabelle wird von der [Aktion PATCHFILES](patchfiles-action.md)verarbeitet. Sie wird normalerweise durch eine Transformation aus einem Patchpaket zum Installationspaket hinzugefügt. Sie wird in der Regel nicht direkt in ein Installationspaket verfasst.

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE29](ice29.md)  
[ICE45](ice45.md)  
</dl>

 

 



