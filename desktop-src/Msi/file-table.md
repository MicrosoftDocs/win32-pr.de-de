---
description: Die Dateitabelle enthält eine komplette Liste der Quelldateien mit ihren verschiedenen Attributen, geordnet nach einem eindeutigen, nicht lokalisierten Bezeichner.
ms.assetid: 31d0e727-a9eb-4cd2-a211-ea7b138d0173
title: Dateitabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59838001101bbc65af50bff3f2b00b540976e4b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867043"
---
# <a name="file-table"></a>Dateitabelle

Die Dateitabelle enthält eine komplette Liste der Quelldateien mit ihren verschiedenen Attributen, geordnet nach einem eindeutigen, nicht lokalisierten Bezeichner. Dateien können auf den Quell Medien als einzelne Dateien gespeichert oder in einer CAB- [*Datei*](c-gly.md)komprimiert werden. Weitere Informationen finden Sie unter [Verwenden von Schränken und komprimierten Quellen](using-cabinets-and-compressed-sources.md).

Die Dateitabelle enthält die folgenden Spalten.



| Spalte      | Typ                               | Schlüssel | Nullwerte zulässig |
|-------------|------------------------------------|-----|----------|
| File        | [Bezeichner](identifier.md)       | J   | N        |
| Komponente\_ | [Bezeichner](identifier.md)       | N   | N        |
| FileName    | [Filename](filename.md)           | N   | N        |
| FileSize    | [Doubleiteger](doubleinteger.md) | N   | N        |
| Version     | [Version](version.md)             | N   | J        |
| Sprache    | [Sprache](language.md)           | N   | J        |
| Attribute  | [Integer](integer.md)             | N   | J        |
| Sequenz    | [Integer](integer.md)             | N   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="File"></span><span id="file"></span><span id="FILE"></span>Datei
</dt> <dd>

Ein nicht lokalisiertes Token, das die Datei eindeutig identifiziert. Dieses Feld ist für Groß-und Kleinschreibung nicht beachtet. Weisen Sie anderen Dateien keine Bezeichner zu, die sich nur in ihrer Groß-/Kleinschreibung unterscheiden.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Zulieferern\_
</dt> <dd>

Der externe Schlüssel in die erste Spalte der [Komponenten Tabelle](component-table.md). Dieses Feld identifiziert die Komponente, die die Datei steuert.

</dd> <dt>

<span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Einfügen
</dt> <dd>

Der Dateiname, der für die Installation verwendet wird. Der Name kann lokalisiert werden.

Da bei manchen Webservern die Groß-/Kleinschreibung beachtet werden kann, sollte der Dateiname genau mit der Groß-/Kleinschreibung der Quelldateien übereinstimmen, um

</dd> <dt>

<span id="FileSize"></span><span id="filesize"></span><span id="FILESIZE"></span>Filesize
</dt> <dd>

Dies ist die Größe der Datei in Byte. Dabei muss es sich um eine nicht negative Zahl handeln.

</dd> <dt>

<span id="Version"></span><span id="version"></span><span id="VERSION"></span>Version
</dt> <dd>

Dieses Feld ist die Versions Zeichenfolge für eine Datei mit Versions Angabe. Dieses Feld ist für Dateien ohne Versions Angabe leer. Die in dieses Feld eingegebene Dateiversion muss mit der Version der Datei identisch sein, die im Installationspaket enthalten ist.

Das Versions Feld kann auch so festgelegt werden, dass der Primärschlüssel eines anderen Datensatzes in der Dateitabelle enthalten ist. Die Datei, auf die verwiesen wird, bestimmt dann die Versionslogik für diese Datei. Weitere Informationen finden Sie unter [Begleit Dateien](companion-files.md). Beachten Sie, dass diese Datei nicht als Begleit Datei angegeben werden darf, wenn diese Datei der Schlüssel Pfad für Ihre Komponente ist.

</dd> <dt>

<span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Kurse
</dt> <dd>

Eine durch Kommas getrennte Liste von dezimalen Sprachen-IDs.

Schriftart Dateien sollten nicht mit einer Sprach-ID erstellt werden, da die Schriftarten nicht über eine eingebettete Sprachen-ID-Ressource verfügen. Daher sollte für Schriftart Dateien diese Spalte NULL belassen werden.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Legt
</dt> <dd>

Die ganze Zahl, die Bitflags enthält, die Dateiattribute darstellen.

In der folgenden Tabelle wird die Definition des Bitfelds angezeigt.



| Konstante                             | Hexadezimal | Decimal | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------------|-------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **msidbfileattributeslesonly**      | 0x000001    | 1       | Schreibgeschützt                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **msidbfileattributeshidden**        | 0x000002    | 2       | Ausgeblendet                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **msidbfileattributessystem**        | 0x000004    | 4       | System                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **msidbfileattributesvital**         | 0x000200    | 512     | Die Datei ist wichtig für die genaue Ausführung der Komponente, zu der Sie gehört. Wenn die Installation einer Datei mit dem Attribut msidbfileattributesvital fehlschlägt, wird die Installation angehalten, und es wird ein Rollback ausgeführt. In diesem Fall zeigt das Installationsprogramm ein Dialogfeld ohne die Schaltfläche ignorieren an. Wenn dieses Attribut nicht festgelegt ist und bei der Installation der Datei ein Fehler auftritt, zeigt das Installationsprogramm ein Dialogfeld mit der Schaltfläche ignorieren an. In diesem Fall kann der Benutzer die fehlerhafte Installation der Datei ignorieren und den Vorgang fortsetzen. <br/> |
| **msidbFileAttributesChecksum**      | 0x000400    | 1024    | Die Datei enthält eine gültige [*Prüfsumme*](c-gly.md). Eine Prüfsumme ist erforderlich, um eine Datei zu reparieren, die beschädigt wurde.                                                                                                                                                                                                                                                                                                                                                                                           |
| **msidbfileattributespatchadded**    | 0x001000    | 4096    | Dieses Bit darf nur von einem Patch hinzugefügt werden, und wenn die Datei durch den Patch hinzugefügt wird.                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **msidbfileattributesnoncompressed** | 0x002000    | 8192    | Der Quelltyp der Datei ist unkomprimiert. Wenn diese Einstellung festgelegt ist, ignorieren Sie die Eigenschaft [**Wort Anzahl Zusammenfassung**](word-count-summary.md) Wenn weder ' **msidbfileattributesnoncompressed** ' noch ' **msidbfileattributescompressed** ' festgelegt sind, wird der Komprimierungs Status der Datei von der ' **Word Count Summary** '-Eigenschaft angegeben. Legen Sie nicht sowohl **msidbfileattributesnoncompressed** als auch **msidbfileattributescompressed** fest.                                                                                                                            |
| **msidbfileattributescompressed**    | 0x004000    | 16384   | Der Quelltyp der Datei ist komprimiert. Wenn diese Einstellung festgelegt ist, ignorieren Sie die Eigenschaft [**Wort Anzahl Zusammenfassung**](word-count-summary.md) Wenn weder ' **msidbfileattributesnoncompressed** ' noch ' **msidbfileattributescompressed** ' festgelegt sind, wird der Komprimierungs Status der Datei von der ' **Word Count Summary** '-Eigenschaft angegeben. Legen Sie nicht sowohl **msidbfileattributesnoncompressed** als auch **msidbfileattributescompressed** fest.                                                                                                                              |



 

Wenn das **msidbfileattributestbit** in der Spalte Attribute festgelegt ist und die Komponente, zu der die Datei gehört, für die Installation ausgewählt ist, muss das Installationsprogramm diese Datei installieren können, damit die Installation erfolgreich abgeschlossen werden kann. Wenn das Installationsprogramm die Datei aus irgendeinem Grund nicht installieren kann (z. b. wenn die Quelldatei nicht innerhalb des Quell Abbilds gefunden werden kann), wird ein Fehler Dialogfeld mit den Optionen "Wiederholen" oder "Abbrechen" angezeigt. Bei einer Datei, für die **msidbfileattributesvital** nicht festgelegt ist, sind die Optionen im Falle eines Installations Fehlers "Abbrechen", "Wiederholen" und "ignorieren" (d. h., der Benutzer hat die Möglichkeit, die Installation erfolgreich abzuschließen, ohne diese Datei zu installieren).

Das **msidbFileAttributesChecksum** -Bit in der Spalte Attribute sollte für jede ausführbare Datei in der Installation festgelegt werden, die über eine gültige [*Prüfsumme*](c-gly.md) im Header der portablen ausführbaren Datei (PE) verfügt. Nur die Dateien, für die dieses Bit festgelegt ist, werden bei einer erneuten Installation immer auf eine gültige Prüfsumme überprüft. Weitere Informationen finden Sie unter [**REINSTALLMODE**](reinstallmode.md).

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequenz
</dt> <dd>

Sequenz Position dieser Datei auf den Medienbildern. Diese Reihenfolge muss der Reihenfolge der Dateien in der CAB-Datei entsprechen, wenn die Dateien komprimiert werden. Die ganzen Zahlen in diesem Feld müssen gleich oder größer als 1 sein.

Die Sequenznummern in der Sequenz Spalte werden verwendet, um sowohl die Reihenfolge der Installation für Dateien als auch das Quell Medium anzugeben, auf dem sich die Datei befindet (in Verbindung mit der [Medien Tabelle](media-table.md)). Nehmen wir beispielsweise an, eine Datei hat die Sequenznummer 92. Zum Ermitteln des Quell Datenträgers, auf dem sich diese Datei befindet, suchen Sie in der Medien Tabelle nach dem Eintrag mit dem kleinsten letzten Sequenzwert, der größer als 92 ist.

Obwohl komprimierte Dateien interne Sequenznummern innerhalb von schränken zugewiesen werden, müssen die absoluten Zahlen nicht mit den Sequenznummern innerhalb der Dateitabelle verglichen werden. Es ist jedoch wichtig, dass die Reihenfolge der Dateien in der Dateitabelle mit der Sequenz der Dateien in den Schränken identisch ist.

Bei Dateien, die nicht komprimiert sind, müssen die Sequenznummern nicht eindeutig sein. Wenn beispielsweise alle Dateien dekomprimiert sind und alle auf einem Datenträger gespeichert sind, können Sie allen Dateien die gleiche Sequenznummer zuordnen.

Der maximale Grenzwert beträgt 32767 Dateien. Informationen zum Erstellen eines Windows Installer Pakets mit weiteren Dateien finden Sie unter Erstellen [eines großen Pakets](authoring-a-large-package.md).

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Mit den Aktionen " [InstallFiles](installfiles-action.md) " und " [RemoveFiles](removefiles-action.md) " in den [*Sequenz Tabellen*](s-gly.md) werden die Informationen in dieser Tabelle verarbeitet. Weitere Informationen zum Verwenden von *Sequenz Tabellen* finden Sie unter [Verwenden einer Sequenz Tabelle](using-a-sequence-table.md).

Die Tabelle wird anfänglich aus der Datei Liste generiert, aber wenn die CAB-Komprimierung verwendet wird, wird die Tabelle aus der Ausgabe der Komprimierungs-Engine neu generiert. Weitere Informationen finden Sie unter CAB- [Dateien](cabinet-files.md).

Zum Verschieben einer vorhandenen Datei auf dem Computer des Benutzers während der Installation verwenden Sie die [movefiles-Aktion](movefiles-action.md) und die [MoveFile-Tabelle](movefile-table.md). Verwenden Sie die [duplicatefiles-Aktion](duplicatefiles-action.md) und die [duplicatefile-Tabelle](duplicatefile-table.md), um eine Datei an mehreren Speicherorten zu installieren.

In der folgenden Tabelle werden die möglichen Kombinationen von Werten in der Spalte Version und in der Spalte Sprache zusammengefasst. Weitere Informationen finden Sie unter [Regeln für die Datei Versions](file-versioning-rules.md)Verwaltung.



| Version | Sprache | BESCHREIBUNG                                                                     |
|---------|----------|---------------------------------------------------------------------------------|
| 1.2.3.4 | 1033     | Die Version und die Sprache.                                                       |
| 1.2.3.4 | Normal   | Die Version, aber keine Sprache.                                                    |
| 1.2.3.4 | 0        | Die-Version und die-Sprache sind neutral.                                           |
| TestDB  | Normal   | Die Begleit Datei ohne zugeordnete Sprache.                         |
| TestDB  | 1033     | Die Begleit Datei und-Sprache.                                                |
| Normal  | 1033     | Es ist keine Version, sondern eine Sprache zugeordnet (d. h. typelib, HelpFile). |



 

Weitere Informationen finden Sie in der Tabelle " [msilockpermissionsex](msilockpermissionsex-table.md) " und der [Tabelle "lockberechtigungs](lockpermissions-table.md)Tabelle".

## <a name="validation"></a>Überprüfen

<dl>

[ICE02](ice02.md)  
[ICE03](ice03.md)  
[ICE04](ice04.md)  
[ICE06](ice06.md)  
[ICE18](ice18.md)  
[ICE30](ice30.md)  
[ICE32](ice32.md)  
[ICE35](ice35.md)  
[ICE39](ice39.md)  
[ICE42](ice42.md)  
[ICE45](ice45.md)  
[ICE50](ice50.md)  
[ICE51](ice51.md)  
[ICE54](ice54.md)  
[ICE55](ice55.md)  
[ICE57](ice57.md)  
[ICE59](ice59.md)  
[ICE60](ice60.md)  
[ICE67](ice67.md)  
[ICE69](ice69.md)  
[ICE76](ice76.md)  
[ICE91](ice91.md)  
</dl>

 

 




