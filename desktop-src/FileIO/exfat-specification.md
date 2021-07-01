---
description: Spezifikation des ExFat-Dateisystems.
title: exFAT-Dateisystemspezifikation
ms.topic: article
ms.date: 08/27/2019
ms.openlocfilehash: 94b5bcdc69201573bc92290c148a7d3ce8304868
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119015"
---
# <a name="exfat-file-system-specification"></a>exFAT-Dateisystemspezifikation

## <a name="1-introduction"></a>1 Einführung

Das ExFAT-Dateisystem ist der Nachfolger von FAT32 in der FAT-Familie der Dateisysteme. Diese Spezifikation beschreibt das ExFAT-Dateisystem und stellt alle Informationen zur Verfügung, die für die Implementierung des exFAT-Dateisystems erforderlich sind.

### <a name="11-design-goals"></a>1.1 Entwurfsziele

Das exFAT-Dateisystem hat drei zentrale Entwurfsziele (siehe Liste unten).

1. *Behalten Sie die Einfachheit von FAT-basierten Dateisystemen bei.*

   > Zwei der Stärken von FAT-basierten Dateisystemen sind ihre relative Einfachheit und einfache Implementierung. In der Geschichte seiner Vorgänger sollten Implementierer exFAT relativ einfach und einfach zu implementieren finden.

2. *Aktivieren Sie sehr große Dateien und Speichergeräte.*

   > Das exFAT-Dateisystem verwendet 64 Bits, um die Dateigröße zu beschreiben, wodurch Anwendungen ermöglicht werden, die von sehr großen Dateien abhängig sind. Das ExFAT-Dateisystem ermöglicht auch Cluster mit einer Datengröße von bis zu 32 MB, wodurch sehr große Speichergeräte effektiv ermöglicht werden.

3. *Integrieren sie Erweiterbarkeit für zukünftige Innovationen.*

   > Das ExFAT-Dateisystem integriert Erweiterbarkeit in seinen Entwurf, sodass das Dateisystem mit Innovationen im Speicher und Änderungen in der Nutzung Schritt halten kann.

### <a name="12-specific-terminology"></a>1.2 Spezifische Terminologie

Im Kontext dieser Spezifikation haben bestimmte Begriffe (siehe [Tabelle 1](#table-1-definition-of-terms-which-carry-very-specific-meaning)) eine bestimmte Bedeutung für den Entwurf und die Implementierung des exFAT-Dateisystems.

<div id="table-1-definition-of-terms-which-carry-very-specific-meaning" />

**Tabelle 1 Definition von Begriffen, die eine sehr spezifische Bedeutung haben**

<table>
<thead>
<tr class="header">
<th><strong>Begriff</strong></th>
<th><strong>Definition</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Soll</td>
<td>Diese Spezifikation verwendet den Begriff "soll", um ein Verhalten zu beschreiben, das obligatorisch ist.</td>
</tr>
<tr class="even">
<td>Optional</td>
<td>In dieser Spezifikation wird der Begriff "sollte" verwendet, um ein Verhalten zu beschreiben, das dringend empfohlen wird, aber nicht zwingend erforderlich ist.</td>
</tr>
<tr class="odd">
<td>May</td>
<td>Diese Spezifikation verwendet den Begriff "may", um ein Verhalten zu beschreiben, das optional ist.</td>
</tr>
<tr class="even">
<td>Obligatorisch.</td>
<td>Dieser Begriff beschreibt ein Feld oder eine Struktur, das von einer Implementierung geändert und wie in dieser Spezifikation beschrieben interpretiert werden soll.</td>
</tr>
<tr class="odd">
<td>Optional</td>
<td>Dieser Begriff beschreibt ein Feld oder eine Struktur, das von einer Implementierung unterstützt werden kann oder nicht. Wenn eine Implementierung ein bestimmtes optionales Feld oder eine bestimmte Optionalstruktur unterstützt, muss sie das Feld oder die Struktur ändern und interpretieren, wie in dieser Spezifikation beschrieben.</td>
</tr>
<tr class="even">
<td>Nicht definiert</td>
<td>Dieser Begriff beschreibt Feld- oder Strukturinhalte, die von einer Implementierung nach Bedarf geändert werden können (d. h. beim Festlegen von umgebenden Feldern oder Strukturen auf 0 (null) gesetzt werden) und dürfen nicht interpretiert werden, um eine bestimmte Bedeutung zu haben.</td>
</tr>
<tr class="odd">
<td>Reserviert</td>
<td><p>Dieser Begriff beschreibt Feld- oder Strukturinhalte, die implementierungen:</p>
<ol type="1">
<li><p>Soll auf 0 (null) initialisieren und sollte für keinen Zweck verwenden.</p></li>
<li><p>Sollte nicht interpretiert werden, außer beim Berechnen von Prüfsummen</p></li>
<li><p>Beibehalten über Vorgänge hinweg, die umgebende Felder oder Strukturen ändern</p></li>
</ol></td>
</tr>
</tbody>
</table>

### <a name="13-full-text-of-common-acronyms"></a>1.3 Vollständiger Text gängiger Akronyme

Diese Spezifikation verwendet Akronyme, die in der Personalcomputerbranche häufig verwendet werden (siehe [Tabelle 2](#table-2-full-text-of-common-acronyms)).

<div id="table-2-full-text-of-common-acronyms" />

**Tabelle 2: Vollständiger Text gängiger Akronyme**

| **Akronym** | **Volltext**                                      |
|-------------|----------------------------------------------------|
| ASCII       | American Standard Code for Information Interchange |
| BIOS        | Grundlegendes Eingabeausgabesystem                          |
| CPU         | Zentrale Verarbeitungseinheit                            |
| exFAT       | Erweiterbare Dateizuordnungstabelle                   |
| FAT         | Dateizuordnungstabelle                              |
| FAT12       | Dateizuordnungstabelle, 12-Bit-Clusterindizes      |
| FAT16       | Dateizuordnungstabelle, 16-Bit-Clusterindizes      |
| FAT32       | Dateizuordnungstabelle, 32-Bit-Clusterindizes      |
| GPT         | GUID-Partitionstabelle                               |
| GUID        | Globally Unique Identifier (global eindeutiger [Bezeichner) (siehe Abschnitt 10.1](#101-globally-unique-identifiers-guids))      |
| INT         | Interrupt                                          |
| MBR         | Master Boot Record                                 |
| texFAT      | Transaktionssicherer ExFAT-Vorgang                             |
| UTC         | Koordinierte Weltzeit (UTC)                         |

### <a name="14-default-field-and-structure-qualifiers"></a>1.4 Standardqualifizierer für Feld und Struktur

Felder und Strukturen in dieser Spezifikation verfügen über die folgenden Qualifizierer (siehe Liste unten), sofern in den Spezifikationshinweisen nichts anderes angegeben ist.

1. Sind nicht signiert

2. Verwenden Sie dezimale Notation, um Werte zu beschreiben, sofern nicht anders angegeben. Diese Spezifikation verwendet den Nachkorrekturbuchstaben "h", um Hexadezimalzahlen zu bezeichnen, und schließt GUIDs in geschweifte Klammern ein.

3. Im Little-Endian-Format

4. Kein Nullabschlusszeichen für Zeichenfolgen erforderlich

### <a name="15-windows-ce-and-texfat"></a>1.5 Windows CE und TexFAT

TexFAT ist eine Erweiterung von exFAT, die zusätzlich zum Basisdateisystem transaktionssichere Betriebssemantik hinzufügt. TexFAT wird von Windows CE.
TexFAT erfordert die Verwendung der beiden FATs und Zuordnungsbitmaps für die Verwendung in Transaktionen. Außerdem werden mehrere zusätzliche Strukturen definiert, einschließlich Auf padding-Deskriptoren und Sicherheitsdeskriptoren.

## <a name="2-volume-structure"></a>2 Volumestruktur

Ein Volume ist der Satz aller Dateisystemstrukturen und des Datenspeicherplatzes, die zum Speichern und Abrufen von Benutzerdaten erforderlich sind. Alle exFAT-Volumes enthalten vier Regionen (siehe [Tabelle 3](#table-3-volume-structure)).

<div id="table-3-volume-structure" />

**Volumestruktur in Tabelle 3**

<table>
<thead>
<tr class="header">
<th><strong>Name der Unterregion</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(Sektor)</strong></p></th>
<th><p><strong>Größe</strong></p>
<p><strong>(Sektoren)</strong></p></th>
<th><strong>Kommentare</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Hauptstartregion</strong></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td>Hauptstartbranche</td>
<td>0</td>
<td>1</td>
<td>Diese Unterregion ist obligatorisch, und <a href="#31-main-and-backup-boot-sector-sub-regions">in Abschnitt 3.1 wird</a> ihr Inhalt definiert.</td>
</tr>
<tr class="odd">
<td>Wichtigste erweiterte Startsektoren</td>
<td>1</td>
<td>8</td>
<td>Diese Unterregion ist obligatorisch, und <a href="#32-main-and-backup-extended-boot-sectors-sub-regions">Abschnitt 3.2</a>) definiert ihren Inhalt.</td>
</tr>
<tr class="even">
<td>OEM-Hauptparameter</td>
<td>9</td>
<td>1</td>
<td>Diese Unterregion ist obligatorisch, und <a href="#33-main-and-backup-oem-parameters-sub-regions">Abschnitt 3.3</a> definiert ihren Inhalt.</td>
</tr>
<tr class="odd">
<td>Reservierter Hauptteil</td>
<td>10</td>
<td>1</td>
<td>Diese Unterregion ist obligatorisch, und ihr Inhalt ist reserviert.</td>
</tr>
<tr class="even">
<td>Hauptstartprüfsumme</td>
<td>11</td>
<td>1</td>
<td>Diese Unterregion ist obligatorisch, und <a href="#34-main-and-backup-boot-checksum-sub-regions">Abschnitt 3.4</a> definiert ihren Inhalt.</td>
</tr>
<tr class="odd">
<td><strong>Region für den Sicherungsstart</strong></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td>Backup Boot-Sektor</td>
<td>12</td>
<td>1</td>
<td>Diese Unterregion ist obligatorisch, und <a href="#31-main-and-backup-boot-sector-sub-regions">Abschnitt 3.1</a> definiert ihren Inhalt.</td>
</tr>
<tr class="odd">
<td>Sichern erweiterter Startbranches</td>
<td>13</td>
<td>8</td>
<td>Diese Unterregion ist obligatorisch, und <a href="#32-main-and-backup-extended-boot-sectors-sub-regions">Abschnitt 3.2</a> definiert ihren Inhalt.</td>
</tr>
<tr class="even">
<td>OEM-Parameter sichern</td>
<td>21</td>
<td>1</td>
<td>Diese Unterregion ist obligatorisch, und <a href="#33-main-and-backup-oem-parameters-sub-regions">Abschnitt 3.3</a> definiert ihren Inhalt.</td>
</tr>
<tr class="odd">
<td>Reservierte Sicherung</td>
<td>22</td>
<td>1</td>
<td>Diese Unterregion ist obligatorisch, und ihr Inhalt ist reserviert.</td>
</tr>
<tr class="even">
<td>Sicherungsstartprüfsumme</td>
<td>23</td>
<td>1</td>
<td>Diese Unterregion ist obligatorisch, und <a href="#34-main-and-backup-boot-checksum-sub-regions">Abschnitt 3.4</a> definiert ihren Inhalt.</td>
</tr>
<tr class="odd">
<td><strong>FAT-Region</strong></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td>FAT-Ausrichtung</td>
<td>24</td>
<td>FatOffset – 24</td>
<td><p>Diese Unterregion ist obligatorisch, und ihre Inhalte sind ggf. nicht definiert.</p>
<p>Hinweis: Der Haupt- und der Sicherungsstartsektor enthalten beide das Feld FatOffset.</p></td>
</tr>
<tr class="odd">
<td>Erstes FAT</td>
<td>FatOffset</td>
<td>FatLength</td>
<td><p>Diese Unterregion ist obligatorisch, und <a href="#41-first-and-second-fat-sub-regions">Abschnitt 4.1</a> definiert ihren Inhalt.</p>
<p>Hinweis: Der Haupt- und der Sicherungsstartsektor enthalten beide die Felder FatOffset und FatLength.</p></td>
</tr>
<tr class="even">
<td>Zweites FAT</td>
<td>FatOffset + FatLength</td>
<td>FatLength * (NumberOfFats – 1)</td>
<td><p>Diese Unterregion ist obligatorisch, und <a href="#41-first-and-second-fat-sub-regions">Abschnitt 4.1</a> definiert ggf. ihren Inhalt.</p>
<p>Hinweis: Die Felder Haupt- und Sicherungsstartsektor enthalten die Felder FatOffset, FatLength und NumberOfFats. Das Feld NumberOfFats darf nur die Werte 1 und 2 enthalten.</p></td>
</tr>
<tr class="odd">
<td><strong>Datenbereich</strong></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td>Clusterheapausrichtung</td>
<td>FatOffset + FatLength * NumberOfFats</td>
<td>ClusterHeapOffset – (FatOffset + FatLength * NumberOfFats)</td>
<td><p>Diese Unterregion ist obligatorisch, und ihre Inhalte sind ggf. nicht definiert.</p>
<p>Hinweis: Der Haupt- und der Sicherungsstartsektor enthalten beide die Felder FatOffset, FatLength, NumberOfFats und ClusterHeapOffset. Die gültigen Werte des Felds NumberOfFats sind 1 und 2.</p></td>
</tr>
<tr class="odd">
<td>Clusterheap</td>
<td>ClusterHeapOffset</td>
<td>ClusterCount * 2<sup>SectorsPerClusterShift</sup></td>
<td><p>Diese Unterregion ist obligatorisch, und <a href="#51-cluster-heap-sub-region">Abschnitt 5.1</a> definiert ihren Inhalt.</p>
<p>Hinweis: Die Felder Haupt- und Sicherungsstartsektoren enthalten die Felder ClusterHeapOffset, ClusterCount und SectorsPerClusterShift.</p></td>
</tr>
<tr class="even">
<td>Übermäßiger Speicherplatz</td>
<td>ClusterHeapOffset + ClusterCount * 2<sup>SectorsPerClusterShift</sup></td>
<td>VolumeLength – (ClusterHeapOffset + ClusterCount * 2<sup>SectorsPerClusterShift</sup>)</td>
<td><p>Diese Unterregion ist obligatorisch, und ihre Inhalte sind ggf. nicht definiert.</p>
<p>Hinweis: Die Haupt- und Sicherungsstartsektoren enthalten die Felder ClusterHeapOffset, ClusterCount, SectorsPerClusterShift und VolumeLength.</p></td>
</tr>
</tbody>
</table>

## <a name="3-main-and-backup-boot-regions"></a>3 Haupt- und Sicherungsstartregionen

Die Hauptstartregion enthält alle erforderlichen Startanweisungen, Informationen zur Identifizierung und Dateisystemparameter, damit eine Implementierung Folgendes ausführen kann:

1. Starten sie ein Computersystem von einem exFAT-Volume.

2. Identifizieren Sie das Dateisystem auf dem Volume als exFAT.

3. Ermitteln Sie den Speicherort der ExFAT-Dateisystemstrukturen.

Die Region "Sicherungsstart" ist eine Sicherung der Hauptstartregion. Sie unterstützt die Wiederherstellung des exFAT-Volumes, wenn sich die Hauptstartregion in einem inkonsistenten Zustand befindet. Außer unter seltenen Umständen, z. B. beim Aktualisieren von Startanweisungen, sollten Implementierungen den Inhalt der Sicherungsstartregion nicht ändern.

### <a name="31-main-and-backup-boot-sector-sub-regions"></a>3.1 Unterregionen des Haupt- und Sicherungsstartbranches

Der Hauptstartsektor enthält Code zum Starten von einem exFAT-Volume und grundlegende exFAT-Parameter, die die Volumestruktur beschreiben (siehe [Tabelle 4).](#table-4-main-and-backup-boot-sector-structure) BIOS, MBR oder andere Bootumreifungs-Agents können diesen Sektor untersuchen und alle darin enthaltenen Startanweisungen laden und ausführen.

Der Sicherungsstart-Sektor ist eine Sicherung des Hauptstartbranches und weist die gleiche Struktur auf (siehe [Tabelle 4).](#table-4-main-and-backup-boot-sector-structure) Der Sicherungsstart-Sektor kann Wiederherstellungsvorgänge unterstützen. Implementierungen müssen jedoch den Inhalt der Felder VolumeFlags und PercentInUse als veraltet behandeln.

Vor der Verwendung des Inhalts des Haupt- oder Sicherungsstartbranches müssen Implementierungen ihren Inhalt überprüfen, indem sie ihre jeweilige Startprüfsumme überprüfen und sicherstellen, dass sich alle ihre Felder innerhalb ihres gültigen Wertbereichs befinden.

Während der anfängliche Formatvorgang den Inhalt des Haupt- und des Sicherungsstartsektors initialisiert, können Implementierungen diese Sektoren nach Bedarf aktualisieren (und auch ihre jeweilige Startprüfsumme aktualisieren). Implementierungen können jedoch entweder die Felder VolumeFlags oder PercentInUse aktualisieren, ohne die jeweilige Startprüfsumme zu aktualisieren (die Prüfsumme schließt diese beiden Felder ausdrücklich aus).

<div id="table-4-main-and-backup-boot-sector-structure" />

**Tabelle 4: Struktur des Haupt- und Sicherungsstarts**

<table>
<thead>
<tr class="header">
<th><strong>Feldname</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(Byte)</strong></p></th>
<th><p><strong>Größe</strong></p>
<p><strong>(Bytes)</strong></p></th>
<th><strong>Kommentare</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>JumpBoot</td>
<td>0</td>
<td>3</td>
<td>Dieses Feld ist obligatorisch, und <a href="#311-jumpboot-field">Abschnitt 3.1.1</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>FileSystemName</td>
<td>3</td>
<td>8</td>
<td>Dieses Feld ist obligatorisch, und <a href="#312-filesystemname-field">Abschnitt 3.1.2</a> definiert seinen Inhalt.</td>
</tr>
<tr class="odd">
<td>MustBeZero</td>
<td>11</td>
<td>53</td>
<td>Dieses Feld ist obligatorisch, und <a href="#313-mustbezero-field">in Abschnitt 3.1.3 wird</a> der Inhalt definiert.</td>
</tr>
<tr class="even">
<td>PartitionOffset</td>
<td>64</td>
<td>8</td>
<td>Dieses Feld ist obligatorisch, und <a href="#314-partitionoffset-field">in Abschnitt 3.1.4 wird</a> der Inhalt definiert.</td>
</tr>
<tr class="odd">
<td>VolumeLength</td>
<td>72</td>
<td>8</td>
<td>Dieses Feld ist obligatorisch, und <a href="#315-volumelength-field">in Abschnitt 3.1.5 wird</a> der Inhalt definiert.</td>
</tr>
<tr class="even">
<td>FatOffset</td>
<td>80</td>
<td>4</td>
<td>Dieses Feld ist obligatorisch, und <a href="#316-fatoffset-field">in Abschnitt 3.1.6 wird</a> der Inhalt definiert.</td>
</tr>
<tr class="odd">
<td>FatLength</td>
<td>84</td>
<td>4</td>
<td>Dieses Feld ist obligatorisch, und <a href="#317-fatlength-field">in Abschnitt 3.1.7 wird</a> der Inhalt definiert.</td>
</tr>
<tr class="even">
<td>ClusterHeapOffset</td>
<td>88</td>
<td>4</td>
<td>Dieses Feld ist obligatorisch, und <a href="#318-clusterheapoffset-field">in Abschnitt 3.1.8</a> wird der Inhalt definiert.</td>
</tr>
<tr class="odd">
<td>ClusterCount</td>
<td>92</td>
<td>4</td>
<td>Dieses Feld ist obligatorisch, und <a href="#319-clustercount-field">in Abschnitt 3.1.9 wird</a> der Inhalt definiert.</td>
</tr>
<tr class="even">
<td>FirstClusterOfRootDirectory</td>
<td>96</td>
<td>4</td>
<td>Dieses Feld ist obligatorisch, und <a href="#3110-firstclusterofrootdirectory-field">in Abschnitt 3.1.10 wird</a> der Inhalt definiert.</td>
</tr>
<tr class="odd">
<td>VolumeSerialNumber</td>
<td>100</td>
<td>4</td>
<td>Dieses Feld ist obligatorisch, und <a href="#3111-volumeserialnumber-field">in Abschnitt 3.1.11 wird</a> der Inhalt definiert.</td>
</tr>
<tr class="even">
<td>FileSystemRevision</td>
<td>104</td>
<td>2</td>
<td>Dieses Feld ist obligatorisch, und <a href="#3112-filesystemrevision-field">in Abschnitt 3.1.12 wird</a> der Inhalt definiert.</td>
</tr>
<tr class="odd">
<td>VolumeFlags</td>
<td>106</td>
<td>2</td>
<td>Dieses Feld ist obligatorisch, und <a href="#3113-volumeflags-field">in Abschnitt 3.1.13 wird</a> der Inhalt definiert.</td>
</tr>
<tr class="even">
<td>BytesPerSectorShift</td>
<td>108</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#3114-bytespersectorshift-field">in Abschnitt 3.1.14 wird</a> der Inhalt definiert.</td>
</tr>
<tr class="odd">
<td>SectorsPerClusterShift</td>
<td>109</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#3115-sectorsperclustershift-field">in Abschnitt 3.1.15 wird</a> der Inhalt definiert.</td>
</tr>
<tr class="even">
<td>NumberOfFats</td>
<td>110</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#3116-numberoffats-field">in Abschnitt 3.1.16 wird</a> der Inhalt definiert.</td>
</tr>
<tr class="odd">
<td>DriveSelect</td>
<td>111</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#3117-driveselect-field">in Abschnitt 3.1.17 wird</a> der Inhalt definiert.</td>
</tr>
<tr class="even">
<td>PercentInUse</td>
<td>112</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#3118-percentinuse-field">in Abschnitt 3.1.18</a> wird der Inhalt definiert.</td>
</tr>
<tr class="odd">
<td>Reserviert</td>
<td>113</td>
<td>7</td>
<td>Dieses Feld ist obligatorisch, und sein Inhalt ist reserviert.</td>
</tr>
<tr class="even">
<td>BootCode</td>
<td>120</td>
<td>390</td>
<td>Dieses Feld ist obligatorisch, und <a href="#3119-bootcode-field">in Abschnitt 3.1.19 wird</a> der Inhalt definiert.</td>
</tr>
<tr class="odd">
<td>BootSignature</td>
<td>510</td>
<td>2</td>
<td>Dieses Feld ist obligatorisch, und <a href="#3120-bootsignature-field">in Abschnitt 3.1.20</a> wird der Inhalt definiert.</td>
</tr>
<tr class="even">
<td>ExcessSpace</td>
<td>512</td>
<td>2<sup>BytesPerSectorShift</sup> – 512</td>
<td><p>Dieses Feld ist obligatorisch, und sein Inhalt ist ( falls erforderlich) nicht definiert.</p>
<p>Hinweis: Die Haupt- und Sicherungsstartsektoren enthalten beide das Feld BytesPerSectorShift.</p></td>
</tr>
</tbody>
</table>

#### <a name="311-jumpboot-field"></a>3.1.1 JumpBoot-Feld

Das Feld JumpBoot muss die Sprunganweisung für CPUs enthalten, die auf PCs üblich sind, die bei der Ausführung die CPU "springen", um die Anweisungen zum Abschnappen des Startvorgangs im Feld BootCode auszuführen.

Der gültige Wert für dieses Feld ist (in der Reihenfolge von low-order byte bis high-order byte) EBh 76h 90h.

#### <a name="312-filesystemname-field"></a>3.1.2 FileSystemName-Feld

Das Feld FileSystemName muss den Namen des Dateisystems auf dem Volume enthalten.

Der gültige Wert für dieses Feld ist in ASCII-Zeichen "EXFAT", der drei nachstellende Leerzeichen enthält.

#### <a name="313-mustbezero-field"></a>3.1.3 MustBeZero-Feld

Das MustBeZero-Feld muss direkt dem Bytebereich entsprechen, den der gepackte BIOS-Parameterblock auf FAT12/16/32-Volumes verbraucht.

Der gültige Wert für dieses Feld ist 0, wodurch verhindert wird, dass FAT12/16/32-Implementierungen fälschlicherweise ein exFAT-Volume einbinden.

#### <a name="314-partitionoffset-field"></a>3.1.4 PartitionOffset-Feld

Das Feld PartitionOffset muss den medien relativen Sektoroffset der Partition beschreiben, die das gegebene exFAT-Volume hostet. Dieses Feld unterstützt das Starten des Volumes mit erweiterten INT-13-Stunden auf Personalcomputern.

Alle möglichen Werte für dieses Feld sind gültig. Der Wert 0 gibt jedoch an, dass Implementierungen dieses Feld ignorieren sollen.

#### <a name="315-volumelength-field"></a>3.1.5 VolumeLength-Feld

Das VolumeLength-Feld muss die Größe des angegebenen exFAT-Volumes in Sektoren beschreiben.

Der gültige Wertebereich für dieses Feld ist:

- Mindestens 2<sup>20/2</sup><sup>BytesPerSectorShift,</sup>wodurch sichergestellt wird, dass das kleinste Volume nicht kleiner als 1 MB ist

- Mindestens 2<sup>64</sup>bis 1, der größte Wert, den dieses Feld beschreiben kann

Wenn die Größe des Unterbereichs "Excess Space" jedoch 0 ist, ist der Wert dieses Felds ClusterHeapOffset + (2<sup>32</sup>- 11) \* 2<sup>SectorsPerClusterShift</sup>.

#### <a name="316-fatoffset-field"></a>3.1.6 FatOffset-Feld

Das Feld FatOffset muss den volumebezogenen Sektoroffset des ersten FAT beschreiben. Mit diesem Feld können Implementierungen das erste FAT an den Merkmalen des zugrunde liegenden Speichermediums ausrichten.

Der gültige Wertebereich für dieses Feld muss:

- Mindestens 24, was die Sektoren der Hauptstart- und Sicherungsstartregionen einnimmt

- Höchstens ClusterHeapOffset (FatLength \* NumberOfFats), der die vom Clusterheap verbrauchten Sektoren darstellt

#### <a name="317-fatlength-field"></a>3.1.7 FatLength-Feld

Das Feld FatLength muss die Länge jeder FAT-Tabelle in Sektoren beschreiben (das Volume kann bis zu zwei FATs enthalten).

Der gültige Wertebereich für dieses Feld muss:

- Mindestens (ClusterCount + 2) \* 2<sup>2/2</sup><sup>BytesPerSectorShift</sup>auf die nächste ganze Zahl aufgerundet, wodurch sichergestellt wird, dass jedes FAT über ausreichend Platz zum Beschreiben aller Cluster im Clusterheap verfügt.

- Höchstens (ClusterHeapOffset – FatOffset) /NumberOfFats auf die nächste ganze Zahl gerundet, wodurch sichergestellt wird, dass die FATs vor dem Clusterheap vorhanden sind.

Dieses Feld kann einen Wert enthalten, der über der unteren Grenze liegt (wie oben beschrieben), damit das zweite FAT(sofern vorhanden) auch an den Merkmalen des zugrunde liegenden Speichermediums ausgerichtet werden kann. Der Inhalt des Speicherplatzes, der das von FAT selbst geforderte Maß überschreitet, ist ggf. nicht definiert.

#### <a name="318-clusterheapoffset-field"></a>3.1.8 ClusterHeapOffset-Feld

Das Feld ClusterHeapOffset muss den volumebezogenen Sektoroffset des Clusterheaps beschreiben. Mit diesem Feld können Implementierungen den Clusterheap an den Merkmalen des zugrunde liegenden Speichermediums ausrichten.

Der gültige Wertebereich für dieses Feld muss:

- Mindestens FatOffset + FatLength \* NumberOfFats, um die Sektoren zu berücksichtigen, die alle vorherigen Regionen verbrauchen

- Höchstens 2<sup>32</sup>– 1 oder VolumeLength – (ClusterCount \* 2<sup>SectorsPerClusterShift),</sup>je nachdem, welche Berechnung kleiner ist

#### <a name="319-clustercount-field"></a>3.1.9 Feld "ClusterCount"

Das Feld ClusterCount muss die Anzahl der Cluster beschreiben, die der Clusterheap enthält.

Der gültige Wert für dieses Feld muss kleiner als der folgende sein:

- (VolumeLength – ClusterHeapOffset) / 2<sup>SectorsPerClusterShift</sup>wird auf die nächste ganze Zahl aufgerundet. Dies ist genau die Anzahl von Clustern, die zwischen dem Anfang des Clusterheaps und dem Ende des Volumes passen können.

- 2<sup>32</sup>bis 11, die maximale Anzahl von Clustern, die ein FAT beschreiben kann

Der Wert des Felds ClusterCount bestimmt die Mindestgröße eines FAT. Um extrem große FATs zu vermeiden, können Implementierungen die Anzahl von Clustern im Clusterheap steuern, indem sie die Clustergröße erhöhen (über das Feld SectorsPerClusterShift). Diese Spezifikation empfiehlt nicht mehr als 2<sup>24</sup>bis 2 Cluster im Clusterheap. Implementierungen müssen jedoch Volumes mit bis zu 2<sup>32</sup>bis 11 Clustern im Clusterheap verarbeiten können.

#### <a name="3110-firstclusterofrootdirectory-field"></a>3.1.10 FirstClusterOfRootDirectory-Feld

Das Feld FirstClusterOfRootDirectory muss den Clusterindex des ersten Clusters des Stammverzeichnisses enthalten. Implementierungen sollten alle Anstrengungen unternehmen, um den ersten Cluster des Stammverzeichnisses im ersten nicht fehlerhaften Cluster zu platzieren, nachdem die Cluster die Zuordnungsbitmap und die Up-Case-Tabelle nutzen.

Der gültige Wertebereich für dieses Feld muss:

- Mindestens 2, der Index des ersten Clusters im Clusterheap

- Höchstens ClusterCount + 1, der Index des letzten Clusters im Clusterheap

#### <a name="3111-volumeserialnumber-field"></a>3.1.11 VolumeSerialNumber-Feld

Das VolumeSerialNumber-Feld muss eine eindeutige Seriennummer enthalten. Dies unterstützt Implementierungen bei der Unterscheidung zwischen verschiedenen exFAT-Volumes.
Implementierungen sollten die Seriennummer generieren, indem das Datum und die Uhrzeit der Formatierung des exFAT-Volumes kombiniert werden. Der Mechanismus zum Kombinieren von Datum und Uhrzeit, um eine Seriennummer zu bilden, ist implementierungsspezifisch.

Alle möglichen Werte für dieses Feld sind gültig.

#### <a name="3112-filesystemrevision-field"></a>3.1.12 FileSystemRevision-Feld

Das Feld FileSystemRevision muss die Haupt- und Nebenrevisionsnummern der exFAT-Strukturen auf dem angegebenen Volume beschreiben.

Das High-Order-Byte ist die Hauptrevisionsnummer, und das Low-Order-Byte ist die Nebenrevisionsnummer. Wenn das hochwertige Byte beispielsweise den Wert 01h und das Low-Order-Byte den Wert 05h enthält, beschreibt das Feld FileSystemRevision die Revisionsnummer 1.05.
Wenn das Hochreihenfolge-Byte den Wert 0Ah und das Low-Order-Byte den Wert 0Fh enthält, beschreibt das Feld FileSystemRevision die Revisionsnummer 10.15.

Der gültige Wertebereich für dieses Feld muss:

- Mindestens 0 für das Low-Order-Byte und 1 für das High-Order-Byte

- Höchstens 99 für das Low-Order-Byte und 99 für das höherwertige Byte

Die Revisionsnummer von exFAT, die in dieser Spezifikation beschrieben wird, ist 1,00.
Implementierungen dieser Spezifikation sollten alle exFAT-Volumes mit der Hauptrevisionsnummer 1 einbinden und dürfen kein exFAT-Volume mit einer anderen Hauptrevisionsnummer einbinden. Implementierungen müssen die Kleinere Revisionsnummer einhalten und dürfen keine Vorgänge ausführen oder Dateisystemstrukturen erstellen, die in der entsprechenden Spezifikation der angegebenen Nebenrevisionsnummer nicht beschrieben sind.

#### <a name="3113-volumeflags-field"></a>3.1.13 VolumeFlags-Feld

Das Feld VolumeFlags muss Flags enthalten, die den Status verschiedener Dateisystemstrukturen auf dem exFAT-Volume angeben (siehe [Tabelle 5).](#table-5-volumeflags-field-structure)

Implementierungen dürfen dieses Feld nicht enthalten, wenn sie die jeweilige Prüfsumme für den Hauptstart oder die Sicherungsstartregion berechnen. Beim Verweisen auf den Sicherungsstart-Sektor müssen Implementierungen dieses Feld als veraltet behandeln.

<div id="table-5-volumeflags-field-structure" />

**VolumeFlags-Feldstruktur in Tabelle 5**

<table>
<thead>
<tr class="header">
<th><strong>Feldname</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(Bit)</strong></p></th>
<th><p><strong>Größe</strong></p>
<p><strong>(Bits)</strong></p></th>
<th><strong>Kommentare</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ActiveFat</td>
<td>0</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#31131-activefat-field">Abschnitt 3.1.13.1</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>VolumeDirty</td>
<td>1</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#31132-volumedirty-field">Abschnitt 3.1.13.2</a> definiert seinen Inhalt.</td>
</tr>
<tr class="odd">
<td>MediaFailure</td>
<td>2</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#31133-mediafailure-field">Abschnitt 3.1.13.3</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>ClearToZero</td>
<td>3</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#31134-cleartozero-field">Abschnitt 3.1.13.4</a> definiert seinen Inhalt.</td>
</tr>
<tr class="odd">
<td>Reserviert</td>
<td>4</td>
<td>12</td>
<td>Dieses Feld ist obligatorisch, und sein Inhalt ist reserviert.</td>
</tr>
</tbody>
</table>

##### <a name="31131-activefat-field"></a>3.1.13.1 ActiveFat-Feld

Das Feld ActiveFat muss wie folgt beschreiben, welche FAT- und Zuordnungsbitmap aktiv sind (und implementierungen müssen verwenden):

- 0, was bedeutet, dass die erste FAT- und die erste Zuordnungsbitmap aktiv sind.

- 1 bedeutet, dass die zweite FAT- und zweite Zuordnungsbitmap aktiv sind und nur möglich ist, wenn das Feld NumberOfFats den Wert 2 enthält.

Implementierungen sollten das inaktive FAT und die Zuordnungsbitmap als veraltet betrachten. Nur TexFAT-fähige Implementierungen dürfen die aktiven FAT- und Zuordnungsbitmaps wechseln (siehe [Abschnitt 7.1).](#71-allocation-bitmap-directory-entry)

##### <a name="31132-volumedirty-field"></a>3.1.13.2 VolumeDirty-Feld

Das Feld VolumeDirty muss wie folgt beschreiben, ob das Volume geändert wurde oder nicht:

- 0, was bedeutet, dass sich das Volume wahrscheinlich in einem konsistenten Zustand befindet.

- 1, was bedeutet, dass sich das Volume wahrscheinlich in einem inkonsistenten Zustand befindet.

Implementierungen sollten den Wert dieses Felds auf 1 festlegen, wenn Dateisystemmetadateninkonsistenzen auftreten, die sie nicht auflösen. Wenn beim Einbinden eines Volumes der Wert dieses Felds 1 ist, können nur Implementierungen, die Dateisystemmetadateninkonsistenzen auflösen, den Wert dieses Felds auf 0 (0) setzen. Solche Implementierungen müssen den Wert dieses Felds erst auf 0 (0) setzen, nachdem sichergestellt wurde, dass sich das Dateisystem in einem konsistenten Zustand befindet.

Wenn beim Einbinden eines Volumes der Wert dieses Felds 0 ist, sollten Implementierungen dieses Feld vor dem Aktualisieren der Dateisystemmetadaten auf 1 festlegen und dieses Feld anschließend auf 0 löschen, ähnlich wie in [Abschnitt 8.1](#81-recommended-write-ordering)beschrieben.

##### <a name="31133-mediafailure-field"></a>3.1.13.3 MediaFailure-Feld

Das Feld MediaFailure muss wie folgt beschreiben, ob eine Implementierung Medienfehler ermittelt hat:

- 0 bedeutet, dass das Hostingmedium keine Fehler gemeldet hat oder bekannte Fehler bereits im FAT als "ungültige" Cluster aufgezeichnet wurden.

- 1, was bedeutet, dass das Hostingmedium Fehler gemeldet hat (d. h. lese- oder schreibvorgänge fehlgeschlagen sind)

Eine Implementierung sollte dieses Feld auf 1 festlegen, wenn:

1. Das Hostingmedium schlägt bei Zugriffsversuchen auf eine beliebige Region auf dem Volume fehl.

2. Die Implementierung hat die Wiederholungsalgorithmen für den Zugriff erschöpft, falls vorhanden.

Wenn beim Einbinden eines Volumes der Wert dieses Felds 1 ist, können Implementierungen, die das gesamte Volume auf Medienfehler überprüfen und alle Fehler als "ungültige" Cluster im FAT aufzeichnen (oder anderweitig Medienfehler beheben), den Wert dieses Felds auf 0 setzen.

##### <a name="31134-cleartozero-field"></a>3.1.13.4 ClearToZero-Feld

Das Feld ClearToZero hat in dieser Spezifikation keine signifikante Bedeutung.

Die gültigen Werte für dieses Feld sind:

- 0, das keine besondere Bedeutung hat

- 1 bedeutet, dass Implementierungen dieses Feld vor dem Ändern von Dateisystemstrukturen, Verzeichnissen oder Dateien auf 0 löschen müssen.

#### <a name="3114-bytespersectorshift-field"></a>3.1.14 BytesPerSectorShift-Feld

Das Feld BytesPerSectorShift muss die Bytes pro Sektor beschreiben, ausgedrückt als Protokoll<sub>2</sub>(N), wobei N die Anzahl der Bytes pro Sektor ist. Für 512 Bytes pro Sektor ist der Wert dieses Felds beispielsweise 9.

Der gültige Wertebereich für dieses Feld muss:

- Mindestens 9 (Sektorgröße 512 Byte), dies ist der kleinstmögliche Sektor für ein exFAT-Volume.

- Höchstens 12 (Sektorgröße von 4.096 Byte), was der Arbeitsspeicherseitengröße von CPUs entspricht, die auf PCs üblich sind.

#### <a name="3115-sectorsperclustershift-field"></a>3.1.15 SectorsPerClusterShift Field

Das Feld SectorsPerClusterShift muss die Sektoren pro Cluster beschreiben, ausgedrückt als Protokoll<sub>2</sub>(N), wobei N für die Anzahl der Sektoren pro Cluster steht. Für 8 Sektoren pro Cluster ist der Wert dieses Felds beispielsweise 3.

Der gültige Wertebereich für dieses Feld muss:

- Mindestens 0 (1 Sektor pro Cluster), der kleinstmögliche Cluster

- Höchstens 25 : BytesPerSectorShift, das zu einer Clustergröße von 32 MB ausgewertet wird

#### <a name="3116-numberoffats-field"></a>3.1.16 NumberOfFats-Feld

Das Feld NumberOfFats muss die Anzahl der FATs und Zuordnungsbitmaps beschreiben, die das Volume enthält.

Der gültige Wertebereich für dieses Feld muss:

- 1, das angibt, dass das Volume nur die erste FAT- und erste Zuordnungsbitmap enthält.

- 2, das angibt, dass das Volume die erste FAT-, zweite FAT-, Erste Zuordnungsbitmap und zweite Zuordnungsbitmap enthält. Dieser Wert ist nur für TexFAT-Volumes gültig.

#### <a name="3117-driveselect-field"></a>3.1.17 LaufwerkFeld auswählen

Das Feld DriveSelect muss die erweiterte INT 13h-Laufwerksnummer enthalten, die das Starten dieses Volumes mithilfe von erweitertem INT 13h auf PCs unterstützt.

Alle möglichen Werte für dieses Feld sind gültig. Ähnliche Felder in früheren FAT-basierten Dateisystemen enthielten häufig den Wert 80h.

#### <a name="3118-percentinuse-field"></a>3.1.18 PercentInUse-Feld

Das Feld PercentInUse muss den Prozentsatz der Cluster im Clusterheap beschreiben, die zugeordnet sind.

Der gültige Wertebereich für dieses Feld muss:

- Zwischen 0 und einschließlich 100, d. h. dem Prozentsatz der zugeordneten Cluster im Clusterheap, gerundet auf die nächste ganze Zahl

- Genau FFh, was angibt, dass der Prozentsatz der zugeordneten Cluster im Clusterheap nicht verfügbar ist

Implementierungen müssen den Wert dieses Felds ändern, um Änderungen bei der Zuordnung von Clustern im Clusterheap widerzuspiegeln, oder sie müssen ihn in FFh ändern.

Implementierungen dürfen dieses Feld nicht enthalten, wenn sie die jeweilige Prüfsumme für den Hauptstart oder die Sicherungsstartregion berechnen. Beim Verweisen auf den Sicherungsstart-Sektor müssen Implementierungen dieses Feld als veraltet behandeln.

#### <a name="3119-bootcode-field"></a>3.1.19 BootCode-Feld

Das Feld BootCode muss Anweisungen zum Starten enthalten.
Implementierungen füllen dieses Feld möglicherweise mit den CPU-Anweisungen auf, die zum Starten eines Computersystems erforderlich sind. Implementierungen, die keine Startanleitungen bereitstellen, müssen jedes Byte in diesem Feld im Rahmen des Formatvorgangs mit F4h initialisieren (die Stoppanweisung für CPUs, die auf PCs üblich sind).

#### <a name="3120-bootsignature-field"></a>3.1.20 BootSignature-Feld

Das Feld BootSignature muss beschreiben, ob die Absicht eines bestimmten Sektor darin besteht, ein Boot-Sektor zu sein oder nicht.

Der gültige Wert für dieses Feld ist AA55h. Jeder andere Wert in diesem Feld macht den jeweiligen Startsektor ungültig. Implementierungen sollten den Inhalt dieses Felds vor je nach einem anderen Feld im jeweiligen Startsektor überprüfen.

### <a name="32-main-and-backup-extended-boot-sectors-sub-regions"></a>3.2 Haupt- und Sicherungsregionen für erweiterte Startsektoren

Jeder Sektor der Hauptbranches für erweiterte Starte weist die gleiche Struktur auf. Jeder Sektor kann jedoch unterschiedliche Startanweisungen enthalten (siehe Tabelle 6). Bootumschnall-Agents, z. B. die Startanleitungen im Hauptstartsektor, alternative BIOS-Implementierungen oder die Firmware eines eingebetteten Systems, können diese Sektoren laden und die darin enthaltenen Anweisungen ausführen.

Der Erweiterte Startsektoren sichern ist eine Sicherung der Hauptbranches für erweiterte Starte und weist die gleiche Struktur auf (siehe [Tabelle 6).](#table-6-extended-boot-sector-structure)

Vor der Ausführung der Anweisungen des Haupt- oder Sicherungsbranches für erweiterte Starte sollten Implementierungen ihren Inhalt überprüfen, indem sie sicherstellen, dass das Feld ExtendedBootSignature jedes Sektor seinen vorgeschriebenen Wert enthält.

Während der anfängliche Formatvorgang den Inhalt sowohl des Haupt- als auch des erweiterten Startsektors für Sicherungen initialisiert, können Implementierungen diese Sektoren nach Bedarf aktualisieren (und auch ihre jeweilige Startprüfsumme aktualisieren).

<div id="table-6-extended-boot-sector-structure" />

**Tabelle 6: Struktur des erweiterten Startbranches**

<table>
<thead>
<tr class="header">
<th><strong>Feldname</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(Byte)</strong></p></th>
<th><p><strong>Größe</strong></p>
<p><strong>(Bytes)</strong></p></th>
<th><strong>Kommentare</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ExtendedBootCode</td>
<td>0</td>
<td>2<sup>BytesPerSectorShift</sup> – 4</td>
<td><p>Dieses Feld ist obligatorisch, und <a href="#321-extendedbootcode-field">Abschnitt 3.2.1</a> definiert seinen Inhalt.</p>
<p>Hinweis: Sowohl der Haupt- als auch der Sicherungsstartsektor enthalten das Feld BytesPerSectorShift.</p></td>
</tr>
<tr class="even">
<td>ExtendedBootSignature</td>
<td>2<sup>BytesPerSectorShift</sup> – 4</td>
<td>4</td>
<td><p>Dieses Feld ist obligatorisch, und <a href="#322-extendedbootsignature-field">Abschnitt 3.2.2</a> definiert seinen Inhalt.</p>
<p>Hinweis: Sowohl der Haupt- als auch der Sicherungsstartsektor enthalten das Feld BytesPerSectorShift.</p></td>
</tr>
</tbody>
</table>

#### <a name="321-extendedbootcode-field"></a>3.2.1 Feld "ExtendedBootCode"

Das Feld ExtendedBootCode muss Anweisungen zum Starten enthalten.
Implementierungen füllen dieses Feld möglicherweise mit den CPU-Anweisungen auf, die zum Starten eines Computersystems erforderlich sind. Implementierungen, die keine Startanweisungen bereitstellen, müssen jedes Byte in diesem Feld im Rahmen des Formatvorgangs mit 00h initialisieren.

#### <a name="322-extendedbootsignature-field"></a>3.2.2 Feld "ExtendedBootSignature"

Das Feld ExtendedBootSignature muss beschreiben, ob die Absicht eines bestimmten Sektor darin besteht, ein erweiterter Startsektor zu sein oder nicht.

Der gültige Wert für dieses Feld ist AA550000h. Jeder andere Wert in diesem Feld macht den jeweiligen Main- oder Backup Extended Boot Sector ungültig.
Implementierungen sollten den Inhalt dieses Felds vor je nach einem anderen Feld im jeweiligen erweiterten Startbereich überprüfen.

### <a name="33-main-and-backup-oem-parameters-sub-regions"></a>3.3 Oem-Parameter-Unterregionen für Haupt- und Sicherungsdaten

Die Unterregion OEM-Hauptparameter enthält zehn Parameterstrukturen, die herstellerspezifische Informationen enthalten können (siehe [Tabelle 7).](#table-7-oem-parameters-structure) Jede der zehn Parameterstrukturen wird von der Vorlage für generische Parameter abgeleitet (siehe [Abschnitt 3.3.2).](#332-generic-parameters-template) Hersteller können ihre eigenen benutzerdefinierten Parameterstrukturen aus der Vorlage generische Parameter ableiten. Diese Spezifikation selbst definiert zwei Parameterstrukturen: NULL-Parameter (siehe [Abschnitt 3.3.3)](#333-null-parameters)und Flashparameter (siehe [Abschnitt 3.3.4](#334-flash-parameters)).

Die OEM-Sicherungsparameter sind eine Sicherung der OEM-Hauptparameter und haben die gleiche Struktur (siehe [Tabelle 7).](#table-7-oem-parameters-structure)

Vor der Verwendung der Inhalte der OEM-Parameter Main oder Backup müssen Implementierungen ihren Inhalt überprüfen, indem sie ihre jeweilige Startprüfsumme überprüfen.

Hersteller sollten die OEM-Haupt- und Sicherungsparameter mit ihren eigenen benutzerdefinierten Parameterstrukturen (falls vorhanden) und beliebigen anderen Parameterstrukturen auffüllen. Bei nachfolgenden Formatvorgängen muss der Inhalt der OEM-Parameter Main und Backup beibehalten werden.

Implementierungen können die OEM-Parameter Main und Backup nach Bedarf aktualisieren (und müssen auch ihre jeweilige Startprüfsumme aktualisieren).

<div id="table-7-oem-parameters-structure" />

**Struktur der OEM-Parameter in Tabelle 7**

<table>
<thead>
<tr class="header">
<th><strong>Feldname</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(Byte)</strong></p></th>
<th><p><strong>Größe</strong></p>
<p><strong>(Bytes)</strong></p></th>
<th><strong>Kommentare</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Parameter[0]</td>
<td>0</td>
<td>48</td>
<td>Dieses Feld ist obligatorisch, und <a href="#331-parameters0--parameters9">Abschnitt 3.3.1</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
</tr>
<tr class="odd">
<td>Parameter[9]</td>
<td>432</td>
<td>48</td>
<td>Dieses Feld ist obligatorisch, und <a href="#331-parameters0--parameters9">Abschnitt 3.3.1</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>Reserviert</td>
<td>480</td>
<td>2<sup>BytesPerSectorShift</sup> – 480</td>
<td><p>Dieses Feld ist obligatorisch, und sein Inhalt ist reserviert.</p>
<p>Hinweis: Sowohl der Haupt- als auch der Sicherungsstartsektor enthalten das Feld BytesPerSectorShift.</p></td>
</tr>
</tbody>
</table>

#### <a name="331-parameters0--parameters9"></a>3.3.1 Parameter \[ 0 \] ... Parameter \[ 9\]

Jedes Parameterfeld in diesem Array enthält eine Parameterstruktur, die von der Vorlage für generische Parameter abgeleitet wird (siehe [Abschnitt 3.3.2](#332-generic-parameters-template)).
Alle nicht verwendeten Parameterfelder müssen so beschrieben werden, dass sie eine Nullparameterstruktur enthalten (siehe [Abschnitt 3.3.3](#333-null-parameters)).

#### <a name="332-generic-parameters-template"></a>3.3.2 Vorlage für generische Parameter

Die Vorlage Generische Parameter stellt die Basisdefinition einer Parameterstruktur bereit (siehe [Tabelle 8).](#table-8-generic-parameters-template) Alle Parameterstrukturen werden von dieser Vorlage abgeleitet. Die Unterstützung für diese Vorlage für generische Parameter ist obligatorisch.

<div id="table-8-generic-parameters-template" />

**Tabelle 8: Vorlage für generische Parameter**

<table>
<thead>
<tr class="header">
<th><strong>Feldname</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(Byte)</strong></p></th>
<th><p><strong>Größe</strong></p>
<p><strong>(Bytes)</strong></p></th>
<th><strong>Kommentare</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ParametersGuid</td>
<td>0</td>
<td>16</td>
<td>Dieses Feld ist obligatorisch, und <a href="#3321-parametersguid-field">Abschnitt 3.3.2.1</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>CustomDefined</td>
<td>16</td>
<td>32</td>
<td>Dieses Feld ist obligatorisch, und die von dieser Vorlage abgeleiteten Strukturen definieren ihren Inhalt.</td>
</tr>
</tbody>
</table>

##### <a name="3321-parametersguid-field"></a>3.3.2.1 ParametersGuid-Feld

Das Feld ParametersGuid muss eine GUID beschreiben, die das Layout des Rests der angegebenen Parameterstruktur bestimmt.

Alle möglichen Werte für dieses Feld sind gültig. Hersteller sollten jedoch ein GUID-generierungstool wie GuidGen.exe verwenden, um eine GUID auszuwählen, wenn sie benutzerdefinierte Parameterstrukturen aus dieser Vorlage ableiten.

#### <a name="333-null-parameters"></a>3.3.3 NULL-Parameter

Die Nullparameterstruktur wird von der Vorlage für generische Parameter abgeleitet (siehe [Abschnitt 3.3.2)](#332-generic-parameters-template)und muss ein nicht verwendetes Parameterfeld beschreiben (siehe [Tabelle 9).](#table-9-null-parameters-structure) Beim Erstellen oder Aktualisieren der OEM-Parameterstruktur müssen Implementierungen nicht verwendeten Parameterfelder mit der Struktur NULL-Parameter auffüllen. Außerdem sollten Implementierungen beim Erstellen oder Aktualisieren der OEM-Parameterstruktur NULL-Parameterstrukturen am Ende des Arrays konsolidieren, sodass alle anderen Parameterstrukturen am Anfang der OEM-Parameterstruktur bleiben.

Die Unterstützung für die Nullparameterstruktur ist obligatorisch.

<div id="table-9-null-parameters-structure" />

**Struktur von NULL-Parametern in Tabelle 9**

<table>
<thead>
<tr class="header">
<th><strong>Feldname</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(Byte)</strong></p></th>
<th><p><strong>Größe</strong></p>
<p><strong>(Bytes)</strong></p></th>
<th><strong>Kommentare</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ParametersGuid</td>
<td>0</td>
<td>16</td>
<td>Dieses Feld ist obligatorisch, und <a href="#3331-parametersguid-field">Abschnitt 3.3.3.1</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>Reserviert</td>
<td>16</td>
<td>32</td>
<td>Dieses Feld ist obligatorisch, und sein Inhalt ist reserviert.</td>
</tr>
</tbody>
</table>

##### <a name="3331-parametersguid-field"></a>3.3.3.1 ParametersGuid-Feld

Das Feld ParametersGuid muss der Definition entsprechen, die von der Vorlage für generische Parameter bereitgestellt wird (siehe [Abschnitt 3.3.2.1).](#3321-parametersguid-field)

Der gültige Wert für dieses Feld in GUID-Notation ist {00000000-0000-0000-0000-000000000000} .

#### <a name="334-flash-parameters"></a>3.3.4 Flashparameter

Die Flash-Parameterstruktur wird von der Vorlage für generische Parameter abgeleitet (siehe [Abschnitt 3.3.2)](#332-generic-parameters-template)und enthält Parameter für Flashmedien (siehe [Tabelle 10).](#table-10-flash-parameters-structure) Hersteller flashbasierter Speichergeräte können ein Parameterfeld (vorzugsweise das Feld Parameter \[ \] 0) mit dieser Parameterstruktur auffüllen. Implementierungen können die Informationen in der Struktur "Flashparameter" verwenden, um Zugriffsvorgänge während Lese-/Schreibvorgängen zu optimieren und die Formatierung der Medien durch Dateisystemstrukturen zu optimieren.

Die Unterstützung für die Flashparameterstruktur ist optional.

<div id="table-10-flash-parameters-structure" />

**Struktur von Flashparametern in Tabelle 10**

<table>
<thead>
<tr class="header">
<th><strong>Feldname</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(Byte)</strong></p></th>
<th><p><strong>Größe</strong></p>
<p><strong>(Bytes)</strong></p></th>
<th><strong>Kommentare</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ParametersGuid</td>
<td>0</td>
<td>16</td>
<td>Dieses Feld ist obligatorisch, und <a href="#3341-parametersguid-field">Abschnitt 3.3.4.1</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>EraseBlockSize</td>
<td>16</td>
<td>4</td>
<td>Dieses Feld ist obligatorisch, und <a href="#3342-eraseblocksize-field">Abschnitt 3.3.4.2</a> definiert seinen Inhalt.</td>
</tr>
<tr class="odd">
<td>PageSize</td>
<td>20</td>
<td>4</td>
<td>Dieses Feld ist obligatorisch, und <a href="#3343-pagesize-field">Abschnitt 3.3.4.3</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>SpareSectors</td>
<td>24</td>
<td>4</td>
<td>Dieses Feld ist obligatorisch, und <a href="#3344-sparesectors-field">Abschnitt 3.3.4.4</a> definiert seinen Inhalt.</td>
</tr>
<tr class="odd">
<td>RandomAccessTime</td>
<td>28</td>
<td>4</td>
<td>Dieses Feld ist obligatorisch, und <a href="#3345-randomaccesstime-field">Abschnitt 3.3.4.5</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>ProgrammingTime</td>
<td>32</td>
<td>4</td>
<td>Dieses Feld ist obligatorisch, und <a href="#3346-programmingtime-field">Abschnitt 3.3.4.6</a> definiert seinen Inhalt.</td>
</tr>
<tr class="odd">
<td>ReadCycle</td>
<td>36</td>
<td>4</td>
<td>Dieses Feld ist obligatorisch, und <a href="#3347-readcycle-field">Abschnitt 3.3.4.7</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>WriteCycle</td>
<td>40</td>
<td>4</td>
<td>Dieses Feld ist obligatorisch, und <a href="#3348-writecycle-field">in Abschnitt 3.3.4.8</a> wird der Inhalt definiert.</td>
</tr>
<tr class="odd">
<td>Reserviert</td>
<td>44</td>
<td>4</td>
<td>Dieses Feld ist obligatorisch, und sein Inhalt ist reserviert.</td>
</tr>
</tbody>
</table>

Alle möglichen Werte für alle Flashparameterfelder, mit Ausnahme des ParametersGuid-Felds, sind gültig. Der Wert 0 gibt jedoch an, dass das Feld tatsächlich bedeutungslos ist (Implementierungen sollten das gegebene Feld ignorieren).

##### <a name="3341-parametersguid-field"></a>3.3.4.1 ParameterGuid-Feld

Das Feld ParametersGuid muss der Definition entsprechen, die in der Vorlage Generische Parameter angegeben ist (siehe [Abschnitt 3.3.2.1](#3321-parametersguid-field)).

Der gültige Wert für dieses Feld in GUID-Notation ist {0A0C7E46-3399-4021-90C8-FA6D389C4BA2}.

##### <a name="3342-eraseblocksize-field"></a>3.3.4.2 EraseBlockSize-Feld

Das Feld EraseBlockSize muss die Größe des Löschblocks des Flashmediums in Bytes beschreiben.

##### <a name="3343-pagesize-field"></a>3.3.4.3 PageSize-Feld

Das Feld PageSize soll die Größe der Seite des Flashmediums in Bytes beschreiben.

##### <a name="3344-sparesectors-field"></a>3.3.4.4 Feld "SpareSectors"

Das Feld "SpareSectors" muss die Anzahl der Sektoren beschreiben, die das Flashmedium für seine internen Sparingvorgänge zur Verfügung hat.

##### <a name="3345-randomaccesstime-field"></a>3.3.4.5 RandomAccessTime-Feld

Das Feld RandomAccessTime muss die durchschnittliche zufällige Zugriffszeit des Flashmediums in Nanosekunden beschreiben.

##### <a name="3346-programmingtime-field"></a>3.3.4.6 ProgrammingTime-Feld

Das Feld ProgrammingTime muss die durchschnittliche Programmierzeit des Flashmediums in Nanosekunden beschreiben.

##### <a name="3347-readcycle-field"></a>3.3.4.7 ReadCycle-Feld

Das Feld ReadCycle muss die durchschnittliche Lesezykluszeit des Flashmediums in Nanosekunden beschreiben.

##### <a name="3348-writecycle-field"></a>3.3.4.8 WriteCycle-Feld

Das Feld WriteCycle muss die durchschnittliche Schreibzykluszeit in Nanosekunden beschreiben.

### <a name="34-main-and-backup-boot-checksum-sub-regions"></a>3.4 Haupt- und Sicherungsstart-Prüfsummenunterregionen

Die Haupt- und Sicherungsstart-Prüfsummen enthalten jeweils ein sich wiederholende Muster der Vier-Byte-Prüfsumme der Inhalte aller anderen Unterregionen in ihren jeweiligen Startregionen. Die Prüfsummenberechnung darf die Felder VolumeFlags und PercentInUse nicht in ihrem jeweiligen Startbereich enthalten (siehe [Abbildung 1](#figure-1-boot-checksum-computation)). Das sich wiederholende Muster der Vier-Byte-Prüfsumme füllt den entsprechenden Unterbereich der Startüberprüfungssumme vom Anfang bis zum Ende des Unterbereichs.

Vor der Verwendung des Inhalts einer der anderen Unterregionen in den Haupt- oder Sicherungsstartregionen müssen Implementierungen ihren Inhalt überprüfen, indem sie ihre jeweilige Startprüfsumme überprüfen.

Während der anfängliche Formatvorgang sowohl die Haupt- als auch die Sicherungsstart-Prüfsumme mit dem sich wiederholenden Prüfsummenmuster auffüllt, müssen Implementierungen diese Sektoren aktualisieren, wenn sich die Inhalte der anderen Sektoren in ihren jeweiligen Startregionen ändern.

<div id="figure-1-boot-checksum-computation" />

**Abbildung 1 Berechnung der Start-Prüfsumme**

```c
UInt32 BootChecksum
(
    UCHAR  * Sectors,        // points to an in-memory copy of the 11 sectors
    USHORT   BytesPerSector
)
{
    UInt32 NumberOfBytes = (UInt32)BytesPerSector * 11;
    UInt32 Checksum = 0;
    UInt32 Index;

    for (Index = 0; Index < NumberOfBytes; Index++)
    {
        if ((Index == 106) || (Index == 107) || (Index == 112))
        {
            continue;
        }
        Checksum = ((Checksum&1) ? 0x80000000 : 0) + (Checksum>>1) + (UInt32)Sectors[Index];
    }

    return Checksum;
}
```

## <a name="4-file-allocation-table-region"></a>4 Dateizuordnungstabellenbereich

Die Fat-Region (File Allocation Table) kann bis zu zwei FATs enthalten, eine in der ersten FAT-Unterregion und eine in der zweiten FAT-Unterregion.
Im Feld NumberOfFats wird beschrieben, wie viele FATs in dieser Region enthalten sind. Die gültigen Werte für das NumberOfFats-Feld sind 1 und 2. Daher enthält die erste FAT-Unterregion immer eine FAT-Datei. Wenn das NumberOfFats-Feld zwei ist, enthält die zweite FAT-Unterregion ebenfalls eine FAT-Datei.

Das Feld ActiveFat des Felds VolumeFlags beschreibt, welche FAT aktiv ist. Nur das VolumeFlags-Feld im Main Boot Sector ist aktuell.
Implementierungen müssen fat, das nicht aktiv ist, als veraltet behandeln. Die Verwendung des inaktiven FAT und der Wechsel zwischen FATs ist implementierungsspezifisch.

### <a name="41-first-and-second-fat-sub-regions"></a>4.1 Erste und zweite FAT-Unterregionen

Ein FAT muss Clusterketten im Cluster heap beschreiben (siehe [Tabelle 11](#table-11-file-allocation-table-structure)).
Eine Clusterkette ist eine Reihe von Clustern, die Speicherplatz zum Aufzeichnen der Inhalte von Dateien, Verzeichnissen und anderen Dateisystemstrukturen bieten. Ein FAT stellt eine Clusterkette als eine singly-verknüpfte Liste von Clusterindizes dar. Mit Ausnahme der ersten beiden Einträge stellt jeder Eintrag in einem FAT genau einen Cluster dar.

<div id="table-11-file-allocation-table-structure" />

**Tabellenstruktur für Dateizuordnungstabellen in Tabelle 11**

<table>
<thead>
<tr class="header">
<th><strong>Feldname</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(Byte)</strong></p></th>
<th><p><strong>Größe</strong></p>
<p><strong>(Bytes)</strong></p></th>
<th><strong>Kommentare</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>FatEntry[0]</td>
<td>0</td>
<td>4</td>
<td>Dieses Feld ist obligatorisch, und <a href="#412-fatentry1-field">in Abschnitt 4.1.2 wird</a> der Inhalt definiert.</td>
</tr>
<tr class="even">
<td>FatEntry[1]</td>
<td>4</td>
<td>4</td>
<td>Dieses Feld ist obligatorisch, und <a href="#412-fatentry1-field">in Abschnitt 4.1.2 wird</a> der Inhalt definiert.</td>
</tr>
<tr class="odd">
<td>FatEntry[2]</td>
<td>8</td>
<td>4</td>
<td>Dieses Feld ist obligatorisch, und <a href="#413-fatentry2--fatentryclustercount1-fields">in Abschnitt 4.1.3 wird</a> der Inhalt definiert.</td>
</tr>
<tr class="even">
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
</tr>
<tr class="odd">
<td>FatEntry[ClusterCount+1]</td>
<td>(ClusterCount + 1) * 4</td>
<td>4</td>
<td><p>Dieses Feld ist obligatorisch, und <a href="#413-fatentry2--fatentryclustercount1-fields">in Abschnitt 4.1.3 wird</a> der Inhalt definiert.</p>
<p>ClusterCount + 1 darf FFFFFFF6h nicht überschreiten.</p>
<p>Hinweis: Die Haupt- und Sicherungsstartsektoren enthalten beide das Feld ClusterCount.</p></td>
</tr>
<tr class="even">
<td>ExcessSpace</td>
<td>(ClusterCount + 2) * 4</td>
<td>(FatLength * 2<sup>BytesPerSectorShift</sup>) – ((ClusterCount + 2) * 4)</td>
<td><p>Dieses Feld ist obligatorisch, und sein Inhalt ist ( falls erforderlich) nicht definiert.</p>
<p>Hinweis: Die Haupt- und Sicherungsstartsektoren enthalten beide die Felder ClusterCount, FatLength und BytesPerSectorShift.</p></td>
</tr>
</tbody>
</table>

#### <a name="411-fatentry0-field"></a>4.1.1 FatEntry \[ \] 0-Feld

Das Feld FatEntry 0 muss den Medientyp im ersten Byte (dem niedrigsten Byte) beschreiben und FFh in den verbleibenden \[ \] drei Bytes enthalten.

Der Medientyp (das erste Byte) sollte F8h sein.

#### <a name="412-fatentry1-field"></a>4.1.2 FatEntry \[ \] 1-Feld

Das Feld FatEntry 1 ist nur aufgrund der vorherigen Rangfolge vorhanden und beschreibt \[ \] nichts von Interesse.

Der gültige Wert für dieses Feld ist FFFFFFFFh. Implementierungen müssen dieses Feld mit dem vorgeschriebenen Wert initialisieren und sollten dieses Feld nicht für beliebige Zwecke verwenden. Implementierungen sollten dieses Feld nicht interpretieren und seinen Inhalt über Vorgänge hinweg beibehalten, die umgebende Felder ändern.

#### <a name="413-fatentry2--fatentryclustercount1-fields"></a>4.1.3 FatEntry \[ 2 \] ... FatEntry \[ ClusterCount+1 \] Fields

Jedes FatEntry-Feld in diesem Array muss einen Cluster im Cluster heap darstellen. FatEntry 2 stellt den ersten Cluster \[ im Cluster \] heap und FatEntry \[ ClusterCount+1 den letzten Cluster \] im Cluster heap dar.

Der gültige Wertebereich für diese Felder muss sein:

- Zwischen 2 und ClusterCount + 1, einschließlich, was auf die nächste FatEntry in der angegebenen Clusterkette verweist; Die gegebene FatEntry darf nicht auf fatEntry verweisen, die ihr in der angegebenen Clusterkette vorangegangen ist.

- Genau FFFFFFF7h, wodurch der entsprechende Cluster von FatEntry als "schlecht" markiert wird

- Genau FFFFFFFFh, das den entsprechenden Cluster des angegebenen FatEntry-Clusters als letzten Cluster einer Clusterkette markiert. dies ist der einzige gültige Wert für die letzte FatEntry einer bestimmten Clusterkette.

## <a name="5-data-region"></a>5 Datenbereich

Der Datenbereich enthält den Cluster heap, der verwalteten Speicherplatz für Dateisystemstrukturen, Verzeichnisse und Dateien bietet.

### <a name="51-cluster-heap-sub-region"></a>5.1 Cluster heap sub-region

Die Struktur des Cluster heap ist sehr einfach (siehe [Tabelle 12](#table-12-cluster-heap-structure)); Jede aufeinander folgende Reihe von Sektoren beschreibt einen Cluster, wie im Feld "SectorsPerClusterShift" definiert. Wichtig ist, dass der erste Cluster des Cluster heap über Index 2 verfügt, der direkt dem Index von FatEntry \[ 2 \] entspricht.

In einem exFAT-Volume verwaltet eine Zuordnungsbitmap (siehe Abschnitt [7.1.5](#715-allocation-bitmap)) den Datensatz des Zuordnungsstatus aller Cluster. Dies ist ein signifikanter Unterschied zu den Vorgängern von exFAT (FAT12, FAT16 und FAT32), bei denen ein FAT einen Datensatz des Zuordnungsstatus aller Cluster im Cluster heap verwaltet hat.

<div id="table-12-cluster-heap-structure" />

**Tabelle 12: Cluster heap structure**

<table>
<thead>
<tr class="header">
<th><strong>Feldname</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(Sektor)</strong></p></th>
<th><p><strong>Größe</strong></p>
<p><strong>(Sektoren)</strong></p></th>
<th><strong>Kommentare</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Cluster[2]</td>
<td>ClusterHeapOffset</td>
<td>2<sup>SectorsPerClusterShift</sup></td>
<td><p>Dieses Feld ist obligatorisch, und <a href="#511-cluster2--clusterclustercount1-fields">Abschnitt 5.1.1</a> definiert seinen Inhalt.</p>
<p>Hinweis: Die Felder Haupt- und Sicherungsstartsektoren enthalten die Felder ClusterHeapOffset und SectorsPerClusterShift.</p></td>
</tr>
<tr class="even">
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
</tr>
<tr class="odd">
<td>Cluster[ClusterCount+1]</td>
<td>ClusterHeapOffset + (ClusterCount – 1) * 2<sup>SectorsPerClusterShift</sup></td>
<td>2<sup>SectorsPerClusterShift</sup></td>
<td><p>Dieses Feld ist obligatorisch, und <a href="#511-cluster2--clusterclustercount1-fields">Abschnitt 5.1.1</a> definiert seinen Inhalt.</p>
<p>Hinweis: Die Felder Haupt- und Sicherungsstartsektoren enthalten die Felder ClusterCount, ClusterHeapOffset und SectorsPerClusterShift.</p></td>
</tr>
</tbody>
</table>

#### <a name="511-cluster2--clusterclustercount1-fields"></a>5.1.1 Cluster \[ 2 \] ... \[ClusterclusterAnzahl+1 \] Felder

Jedes Clusterfeld in diesem Array ist eine Reihe zusammenhängender Sektoren, deren Größe durch das Feld SectorsPerClusterShift definiert wird.

## <a name="6-directory-structure"></a>6 Verzeichnisstruktur

Das exFAT-Dateisystem verwendet einen Verzeichnisstrukturansatz, um die Dateisystemstrukturen und -dateien zu verwalten, die im Clusterheap vorhanden sind. Verzeichnisse weisen eine 1:n-Beziehung zwischen übergeordnetem und untergeordnetem Element in der Verzeichnisstruktur auf.

Das Verzeichnis, auf das das Feld FirstClusterOfRootDirectory verweist, ist der Stamm der Verzeichnisstruktur. Alle anderen Verzeichnisse werden auf singly-verknüpfte Weise aus dem Stammverzeichnis abgeleitet.

Jedes Verzeichnis besteht aus einer Reihe von Verzeichniseinträgen (siehe [Tabelle 13).](#table-13-directory-structure)

Ein oder mehrere Verzeichniseinträge werden zu einem Verzeichniseintragssatz kombiniert, der etwas Interessantes beschreibt, z. B. eine Dateisystemstruktur, ein Unterverzeichnis oder eine Datei.

<div id="table-13-directory-structure" />

**Tabellen-13-Verzeichnisstruktur**

<table>
<thead>
<tr class="header">
<th><strong>Feldname</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(Byte)</strong></p></th>
<th><p><strong>Größe</strong></p>
<p><strong>(Byte)</strong></p></th>
<th><strong>Kommentare</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>DirectoryEntry[0]</td>
<td>0</td>
<td>32</td>
<td>Dieses Feld ist obligatorisch, und <a href="#61-directoryentry0--directoryentryn--1">Abschnitt 6.1</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
</tr>
<tr class="odd">
<td>DirectoryEntry[N-1]</td>
<td>(N – 1) * 32</td>
<td>32</td>
<td><p>Dieses Feld ist obligatorisch, und <a href="#61-directoryentry0--directoryentryn--1">Abschnitt 6.1</a> definiert seinen Inhalt.</p>
<p>N, die Anzahl der DirectoryEntry-Felder, ist die Größe der Clusterkette in Byte, die das angegebene Verzeichnis enthält, dividiert durch die Größe eines DirectoryEntry-Felds, 32 Bytes.</p></td>
</tr>
</tbody>
</table>

### <a name="61-directoryentry0--directoryentryn--1"></a>6.1 DirectoryEntry \[ 0 \] ... DirectoryEntry \[ N--1\]

Jedes DirectoryEntry-Feld in diesem Array wird von der generischen DirectoryEntry-Vorlage abgeleitet (siehe [Abschnitt 6.2](#62-generic-directoryentry-template)).

### <a name="62-generic-directoryentry-template"></a>6.2 Generisches VerzeichnisVersuchsvorlage

Die Vorlage Generic DirectoryEntry stellt die Basisdefinition für Verzeichniseinträge bereit (siehe [Tabelle 14](#table-14-generic-directoryentry-template)). Alle Verzeichniseintragsstrukturen leiten sich von dieser Vorlage ab, und nur von Microsoft definierte Verzeichniseintragsstrukturen sind gültig (exFAT verfügt nicht über Bestimmungen für vom Hersteller definierte Verzeichniseintragsstrukturen, außer wie in [Abschnitt 7.8](#78-vendor-extension-directory-entry) und [Abschnitt 7.9](#79-vendor-allocation-directory-entry)definiert). Die Möglichkeit, die Vorlage Generic DirectoryEntry zu interpretieren, ist obligatorisch.

<div id="table-14-generic-directoryentry-template" />

**Tabelle 14: Generisches VerzeichnisEntry-Vorlage**

<table>
<thead>
<tr class="header">
<th><strong>Feldname</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(Byte)</strong></p></th>
<th><p><strong>Größe</strong></p>
<p><strong>(Byte)</strong></p></th>
<th><strong>Kommentare</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EntryType</td>
<td>0</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#621-entrytype-field">Abschnitt 6.2.1</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>CustomDefined</td>
<td>1</td>
<td>19</td>
<td>Dieses Feld ist obligatorisch, und Strukturen, die von dieser Vorlage abgeleitet werden, können ihren Inhalt definieren.</td>
</tr>
<tr class="odd">
<td>FirstCluster</td>
<td>20</td>
<td>4</td>
<td>Dieses Feld ist obligatorisch, und <a href="#622-firstcluster-field">Abschnitt 6.2.2</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>DataLength</td>
<td>24</td>
<td>8</td>
<td>Dieses Feld ist obligatorisch, und <a href="#623-datalength-field">Abschnitt 6.2.3</a> definiert seinen Inhalt.</td>
</tr>
</tbody>
</table>

#### <a name="621-entrytype-field"></a>6.2.1 EntryType-Feld

Das Feld EntryType verfügt über drei Verwendungsmodi, die der Wert des Felds definiert (siehe Liste unten).

- 00h ist ein Marker für das Ende des Verzeichnisses, und es gelten die folgenden Bedingungen:

  - Alle anderen Felder in der angegebenen DirectoryEntry sind tatsächlich reserviert.

  - Alle nachfolgenden Verzeichniseinträge im angegebenen Verzeichnis sind ebenfalls End-of-Directory-Marker.

  - End-of-Directory-Marker sind nur außerhalb von Verzeichniseintragssätzen gültig.

  - Implementierungen können Bei Bedarf End-of-Directory-Marker überschreiben.

- Zwischen 01h und einschließlich 7Fh, was ein nicht verwendeter Verzeichniseintragsmarker ist und die folgenden Bedingungen gelten:

  - Alle anderen Felder in der angegebenen DirectoryEntry sind tatsächlich nicht definiert.

  - Nicht verwendete Verzeichniseinträge sind nur außerhalb von Verzeichniseintragssätzen gültig.

  - Implementierungen können nicht verwendeten Verzeichniseinträge nach Bedarf überschreiben.

  - Dieser Wertebereich entspricht dem Feld InUse (siehe [Abschnitt 6.2.1.4),](#6214-inuse-field)das den Wert 0 enthält.

- Zwischen 81h und einschließlich FFh, was ein regulärer Verzeichniseintrag ist und die folgenden Bedingungen gelten:

  - Der Inhalt des EntryType-Felds (siehe [Tabelle 15)](#table-15-generic-entrytype-field-structure)bestimmt das Layout des Rests der DirectoryEntry-Struktur.

  - Dieser Wertebereich und nur dieser Wertebereich sind innerhalb eines Verzeichniseintragssatzes gültig.

  - Dieser Wertebereich entspricht direkt dem Feld InUse (siehe [Abschnitt 6.2.1.4),](#6214-inuse-field)das den Wert 1 enthält.

Um Änderungen am Feld InUse (siehe [Abschnitt 6.2.1.4)](#6214-inuse-field)zu verhindern, die fälschlicherweise zu einem Verzeichnisendemarker führen, ist der Wert 80h ungültig.

<div id="table-15-generic-entrytype-field-structure" />

**Table 15 Generic EntryType Field Structure**

<table>
<thead>
<tr class="header">
<th><strong>Feldname</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(Bit)</strong></p></th>
<th><p><strong>Größe</strong></p>
<p><strong>(Bits)</strong></p></th>
<th><strong>Kommentare</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>TypeCode</td>
<td>0</td>
<td>5</td>
<td>Dieses Feld ist obligatorisch, und <a href="#6211-typecode-field">Abschnitt 6.2.1.1</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>TypeImportance</td>
<td>5</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#6212-typeimportance-field">Abschnitt 6.2.1.2</a> definiert seinen Inhalt.</td>
</tr>
<tr class="odd">
<td>TypeCategory</td>
<td>6</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#6213-typecategory-field">Abschnitt 6.2.1.3</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>InUse</td>
<td>7</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#6214-inuse-field">Abschnitt 6.2.1.4</a> definiert seinen Inhalt.</td>
</tr>
</tbody>
</table>

##### <a name="6211-typecode-field"></a>6.2.1.1 TypCodefeld

Das Feld TypeCode beschreibt teilweise den spezifischen Typ des angegebenen Verzeichniseintrags. Dieses Feld sowie die Felder TypeImportance und TypeCategory (siehe [Abschnitt 6.2.1.2](#6212-typeimportance-field) bzw. [Abschnitt 6.2.1.3)](#6213-typecategory-field)identifizieren eindeutig den Typ des angegebenen Verzeichniseintrags.

Alle möglichen Werte dieses Felds sind gültig, es sei denn, die Felder TypeImportance und TypeCategory enthalten jeweils den Wert 0. In diesem Fall ist der Wert 0 für dieses Feld ungültig.

##### <a name="6212-typeimportance-field"></a>6.2.1.2 TypeImportance-Feld

Das Feld TypeImportance muss die Wichtigkeit des angegebenen Verzeichniseintrags beschreiben.

Die gültigen Werte für dieses Feld müssen:

- 0, was bedeutet, dass der angegebene Verzeichniseintrag kritisch ist (siehe [Abschnitt 6.3.1.2.1](#63121-critical-primary-directory-entries) und [Abschnitt 6.4.1.2.1](#64121-critical-secondary-directory-entries) für kritische primäre bzw. kritische sekundäre Verzeichniseinträge)

- 1, was bedeutet, dass der angegebene Verzeichniseintrag unbedenklich ist (siehe [Abschnitt 6.3.1.2.2](#63122-benign-primary-directory-entries) und [Abschnitt 6.4.1.2.2](#64122-benign-secondary-directory-entries) für unbedenkliche primäre bzw. unbedenkliche sekundäre Verzeichniseinträge)

##### <a name="6213-typecategory-field"></a>6.2.1.3 TypeCategory-Feld

Das Feld TypeCategory muss die Kategorie des angegebenen Verzeichniseintrags beschreiben.

Die gültigen Werte für dieses Feld müssen:

- 0 bedeutet, dass der angegebene Verzeichniseintrag primär ist (siehe [Abschnitt 6.3](#63-generic-primary-directoryentry-template)).

- 1 bedeutet, dass der angegebene Verzeichniseintrag sekundär ist (siehe [Abschnitt 6.4](#64-generic-secondary-directoryentry-template)).

##### <a name="6214-inuse-field"></a>6.2.1.4 Feld "InUse"

Das Feld InUse muss beschreiben, ob der angegebene Verzeichniseintrag verwendet wird oder nicht.

Die gültigen Werte für dieses Feld müssen:

- 0 bedeutet, dass der angegebene Verzeichniseintrag nicht verwendet wird. Dies bedeutet, dass die angegebene Struktur tatsächlich ein nicht verwendeter Verzeichniseintrag ist.

- 1, d. h. der angegebene Verzeichniseintrag wird verwendet. Dies bedeutet, dass die angegebene Struktur ein regulärer Verzeichniseintrag ist.

#### <a name="622-firstcluster-field"></a>6.2.2 FirstCluster-Feld

Das Feld FirstCluster muss den Index des ersten Clusters einer Zuordnung im Clusterheap enthalten, der dem angegebenen Verzeichniseintrag zugeordnet ist.

Der gültige Wertebereich für dieses Feld muss:

- Genau 0, was bedeutet, dass keine Clusterzuordnung vorhanden ist

- Zwischen 2 und ClusterCount + 1, der Bereich gültiger Clusterindizes

Strukturen, die von dieser Vorlage abgeleitet werden, können sowohl die Felder FirstCluster als auch DataLength neu definieren, wenn eine Clusterzuordnung nicht mit der abgeleiteten Struktur kompatibel ist.

#### <a name="623-datalength-field"></a>6.2.3 DataLength-Feld

Im Feld DataLength wird die Größe der Daten, die die zugeordnete Clusterzuordnung enthält, in Bytes beschrieben.

Der gültige Wertbereich für dieses Feld lautet:

- Mindestens 0; Wenn das FirstCluster-Feld den Wert 0 enthält, ist der einzige gültige Wert dieses Felds 0.

- Höchstens ClusterCount \* <sup>2-SektorenPerClusterShift</sup> \* 2<sup>BytesPerSectorShift</sup>

Strukturen, die von dieser Vorlage abgeleitet werden, können die Felder FirstCluster und DataLength neu definieren, wenn eine Clusterzuordnung für die abgeleitete Struktur nicht möglich ist.

### <a name="63-generic-primary-directoryentry-template"></a>6.3 Generisches primäres VerzeichnisEntry-Vorlage

Der erste Verzeichniseintrag in einem Verzeichniseintragssatz muss ein primärer Verzeichniseintrag sein. Alle nachfolgenden Verzeichniseinträge im Verzeichniseintragssatz müssen ggf. sekundäre Verzeichniseinträge sein (siehe [Abschnitt 6.4](#64-generic-secondary-directoryentry-template)).

Die Fähigkeit zum Interpretieren der Generischen primären DirectoryEntry-Vorlage ist obligatorisch.

Alle Primären Verzeichniseintragsstrukturen werden von der Generischen primären DirectoryEntry-Vorlage abgeleitet (siehe [Tabelle 16](#table-16-generic-primary-directoryentry-template)), die von der Generischen DirectoryEntry-Vorlage abgeleitet ist (siehe [Abschnitt 6.2](#62-generic-directoryentry-template)).

<div id="table-16-generic-primary-directoryentry-template" />

**Tabelle 16 Generisches primäres VerzeichnisEntry-Vorlage**

<table>
<thead>
<tr class="header">
<th><strong>Feldname</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(Byte)</strong></p></th>
<th><p><strong>Größe</strong></p>
<p><strong>(Byte)</strong></p></th>
<th><strong>Kommentare</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EntryType</td>
<td>0</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#631-entrytype-field">Abschnitt 6.3.1</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>SecondaryCount</td>
<td>1</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#632-secondarycount-field">Abschnitt 6.3.2</a> definiert seinen Inhalt.</td>
</tr>
<tr class="odd">
<td>SetChecksum</td>
<td>2</td>
<td>2</td>
<td>Dieses Feld ist obligatorisch, und <a href="#633-setchecksum-field">Abschnitt 6.3.3</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>GeneralPrimaryFlags</td>
<td>4</td>
<td>2</td>
<td>Dieses Feld ist obligatorisch, und <a href="#634-generalprimaryflags-field">Abschnitt 6.3.4</a> definiert seinen Inhalt.</td>
</tr>
<tr class="odd">
<td>CustomDefined</td>
<td>6</td>
<td>14</td>
<td>Dieses Feld ist obligatorisch, und Strukturen, die von dieser Vorlage abgeleitet werden, definieren ihren Inhalt.</td>
</tr>
<tr class="even">
<td>FirstCluster</td>
<td>20</td>
<td>4</td>
<td>Dieses Feld ist obligatorisch, und <a href="#635-firstcluster-field">Abschnitt 6.3.5</a> definiert seinen Inhalt.</td>
</tr>
<tr class="odd">
<td>DataLength</td>
<td>24</td>
<td>8</td>
<td>Dieses Feld ist obligatorisch, und <a href="#636-datalength-field">Abschnitt 6.3.6</a> definiert seinen Inhalt.</td>
</tr>
</tbody>
</table>

#### <a name="631-entrytype-field"></a>6.3.1 EntryType-Feld

Das EntryType-Feld muss der Definition entsprechen, die in der Generischen DirectoryEntry-Vorlage angegeben ist (siehe [Abschnitt 6.2.1](#621-entrytype-field)).

##### <a name="6311-typecode-field"></a>6.3.1.1 TypCodefeld

Das TypeCode-Feld muss der Definition in der Vorlage Generic DirectoryEntry entsprechen (siehe [Abschnitt 6.2.1.1](#6211-typecode-field)).

##### <a name="6312-typeimportance-field"></a>6.3.1.2 TypeImportance Field

Das Feld TypeImportance muss der Definition in der Vorlage Generic DirectoryEntry entsprechen (siehe [Abschnitt 6.2.1.2](#6212-typeimportance-field)).

###### <a name="63121-critical-primary-directory-entries"></a>6.3.1.2.1 Kritische primäre Verzeichniseinträge

Kritische primäre Verzeichniseinträge enthalten Informationen, die für die ordnungsgemäße Verwaltung eines exFAT-Volumes von entscheidender Bedeutung sind. Nur das Stammverzeichnis enthält wichtige primäre Verzeichniseinträge (Dateiverzeichniseinträge stellen eine Ausnahme dar, siehe [Abschnitt 7.4](#74-file-directory-entry)).

Die Definition kritischer primärer Verzeichniseinträge korreliert mit der Hauptrevisionsnummer exFAT. Implementierungen müssen alle kritischen primären Verzeichniseinträge unterstützen und nur die kritischen primären Verzeichniseintragsstrukturen aufzeichnen, die diese Spezifikation definiert.

###### <a name="63122-benign-primary-directory-entries"></a>6.3.1.2.2 Unbedenkliche Einträge im primären Verzeichnis

Unbedenkliche primäre Verzeichniseinträge enthalten zusätzliche Informationen, die für die Verwaltung eines exFAT-Volumes nützlich sein können. Jedes Verzeichnis kann unbedenkliche primäre Verzeichniseinträge enthalten.

Die Definition von unbedenklichen primären Verzeichniseinträgen korreliert mit der kleineren ExFAT-Revisionsnummer. Die Unterstützung für jeden unbedenklichen primären Verzeichniseintrag, den diese Spezifikation oder eine nachfolgende Spezifikation definiert, ist optional. Ein nicht erkannter unbedenklicher primärer Verzeichniseintrag rendert den gesamten Verzeichniseintragssatz als nicht erkannt (über die Definition der entsprechenden Verzeichniseintragsvorlagen hinaus).

##### <a name="6313-typecategory-field"></a>6.3.1.3 TypeCategory-Feld

Das Feld TypeCategory muss der Definition in der Vorlage Generic DirectoryEntry entsprechen (siehe [Abschnitt 6.2.1.3).](#6213-typecategory-field)

Für diese Vorlage muss der gültige Wert für dieses Feld 0 sein.

##### <a name="6314-inuse-field"></a>6.3.1.4 Feld "InUse"

Das Feld InUse muss der Definition entsprechen, die in der Generischen DirectoryEntry-Vorlage angegeben ist (siehe [Abschnitt 6.2.1.4](#6214-inuse-field)).

#### <a name="632-secondarycount-field"></a>6.3.2 SecondaryCount-Feld

Das Feld SecondaryCount muss die Anzahl der sekundären Verzeichniseinträge beschreiben, die unmittelbar auf den angegebenen eintrag des primären Verzeichnisses folgen. Diese sekundären Verzeichniseinträge bestehen zusammen mit dem angegebenen primären Verzeichniseintrag aus dem Verzeichniseintragssatz.

Der gültige Wertebereich für dieses Feld muss:

- Mindestens 0. Dies bedeutet, dass dieser eintrag des primären Verzeichnisses der einzige Eintrag im Verzeichniseintragssatz ist.

- Höchstens 255, was bedeutet, dass die nächsten 255 Verzeichniseinträge und dieser primäre Verzeichniseintrag den Verzeichniseintragssatz umfassen.

Kritische primäre Verzeichniseintragsstrukturen, die von dieser Vorlage abgeleitet werden, können die Felder SecondaryCount und SetChecksum neu definieren.

#### <a name="633-setchecksum-field"></a>6.3.3 SetChecksum-Feld

Das Feld SetChecksum muss die Prüfsumme aller Verzeichniseinträge im angegebenen Verzeichniseintragssatz enthalten. Die Prüfsumme schließt dieses Feld jedoch aus (siehe [Abbildung 2).](#figure-2-entrysetchecksum-computation) Implementierungen müssen überprüfen, ob der Inhalt dieses Felds gültig ist, bevor ein anderer Verzeichniseintrag im angegebenen Verzeichniseintragssatz verwendet wird.

Kritische primäre Verzeichniseintragsstrukturen, die von dieser Vorlage abgeleitet werden, können die Felder SecondaryCount und SetChecksum neu definieren.

<div id="figure-2-entrysetchecksum-computation" />

**Abbildung 2 EntrySetChecksum-Berechnung**

```C
UInt16 EntrySetChecksum
(
    UCHAR * Entries,       // points to an in-memory copy of the directory entry set
    UCHAR   SecondaryCount
)
{
    UInt16 NumberOfBytes = ((UInt16)SecondaryCount + 1) * 32;
    UInt16 Checksum = 0;
    UInt16 Index;

    for (Index = 0; Index < NumberOfBytes; Index++)
    {
        if ((Index == 2) || (Index == 3))
        {
            continue;
        }
        Checksum = ((Checksum&1) ? 0x8000 : 0) + (Checksum>>1) +  (UInt16)Entries[Index];
    }
    return Checksum;
}
```

#### <a name="634-generalprimaryflags-field"></a>6.3.4 GeneralPrimaryFlags-Feld

Das Feld GeneralPrimaryFlags enthält Flags (siehe [Tabelle 17](#table-17-generic-generalprimaryflags-field-structure)).

Kritische primäre Verzeichniseintragsstrukturen, die von dieser Vorlage abgeleitet werden, können dieses Feld neu definieren.

<div id="table-17-generic-generalprimaryflags-field-structure" />

**Tabelle 17 Generische GeneralPrimaryFlags-Feldstruktur**

<table>
<thead>
<tr class="header">
<th><strong>Feldname</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(Bit)</strong></p></th>
<th><p><strong>Größe</strong></p>
<p><strong>(Bits)</strong></p></th>
<th><strong>Kommentare</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>AllocationPossible</td>
<td>0</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#6341-allocationpossible-field">Abschnitt 6.3.4.1</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>NoFatChain</td>
<td>1</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#6342-nofatchain-field">Abschnitt 6.3.4.2</a> definiert seinen Inhalt.</td>
</tr>
<tr class="odd">
<td>CustomDefined</td>
<td>2</td>
<td>14</td>
<td>Dieses Feld ist obligatorisch, und Strukturen, die von dieser Vorlage abgeleitet werden, können dieses Feld definieren.</td>
</tr>
</tbody>
</table>

##### <a name="6341-allocationpossible-field"></a>6.3.4.1 AllocationPossible Field

Das Feld AllocationPossible muss beschreiben, ob eine Zuordnung im Clusterheap für den angegebenen Verzeichniseintrag möglich ist.

Die gültigen Werte für dieses Feld müssen:

- 0 bedeutet, dass eine zugeordnete Zuordnung von Clustern nicht möglich ist und die Felder FirstCluster und DataLength tatsächlich nicht definiert sind (Strukturen, die von dieser Vorlage abgeleitet werden, können diese Felder neu definieren).

- 1. Dies bedeutet, dass eine zugeordnete Zuordnung von Clustern möglich ist und die Felder FirstCluster und DataLength wie definiert sind.

##### <a name="6342-nofatchain-field"></a>6.3.4.2 NoFatChain-Feld

Das Feld NoFatChain muss angeben, ob das aktive FAT die Clusterkette der angegebenen Zuordnung beschreibt oder nicht.

Die gültigen Werte für dieses Feld müssen:

- 0, d. h. die entsprechenden FAT-Einträge für die Clusterkette der Zuordnung sind gültig, und Implementierungen müssen sie interpretieren. Wenn das Feld AllocationPossible den Wert 0 enthält oder das Feld AllocationPossible den Wert 1 und das Feld FirstCluster den Wert 0 enthält, ist der einzige gültige Wert dieses Felds 0.

- 1, was bedeutet, dass die zugeordnete Zuordnung eine zusammenhängende Reihe von Clustern ist. die entsprechenden FAT-Einträge für die Cluster sind ungültig, und Implementierungen dürfen sie nicht interpretieren. -Implementierungen können die folgende Gleichung verwenden, um die Größe der zugeordneten Zuordnung zu berechnen: DataLength / (2<sup>SectorsPerClusterShift</sup> \* 2<sup>BytesPerSectorShift</sup>), aufgerundet auf die nächste ganze Zahl

Wenn kritische primäre Verzeichniseintragsstrukturen, die von dieser Vorlage abgeleitet werden, das Feld GeneralPrimaryFlags neu definieren, sind die entsprechenden FAT-Einträge für die Clusterkette einer zugeordneten Zuordnung gültig.

#### <a name="635-firstcluster-field"></a>6.3.5 FirstCluster-Feld

Das Feld FirstCluster muss der Definition in der Vorlage Generic DirectoryEntry entsprechen (siehe [Abschnitt 6.2.2](#622-firstcluster-field)).

Wenn das NoFatChain-Bit 1 ist, muss FirstCluster auf einen gültigen Cluster im Clusterheap verweisen.

Kritische primäre Verzeichniseintragsstrukturen, die von dieser Vorlage abgeleitet werden, können die Felder FirstCluster und DataLength neu definieren. Andere Strukturen, die von dieser Vorlage abgeleitet werden, können die Felder FirstCluster und DataLength nur neu definieren, wenn das Feld AllocationPossible den Wert 0 enthält.

#### <a name="636-datalength-field"></a>6.3.6 DataLength-Feld

Das DataLength-Feld muss der Definition in der Generischen DirectoryEntry-Vorlage entsprechen (siehe [Abschnitt 6.2.3](#623-datalength-field)).

Wenn das NoFatChain-Bit 1 ist, darf DataLength nicht 0 (null) sein. Wenn das FirstCluster-Feld 0 (null) ist, muss DataLength ebenfalls 0 (null) sein.

Kritische primäre Verzeichniseintragsstrukturen, die von dieser Vorlage abgeleitet werden, können die Felder FirstCluster und DataLength neu definieren. Andere Strukturen, die von dieser Vorlage abgeleitet werden, können die Felder FirstCluster und DataLength nur neu definieren, wenn das Feld AllocationPossible den Wert 0 enthält.

### <a name="64-generic-secondary-directoryentry-template"></a>6.4 Generisches sekundäres VerzeichnisVersuchsvorlage

Der zentrale Zweck sekundärer Verzeichniseinträge besteht darin, zusätzliche Informationen zu einem Verzeichniseintragssatz bereitzustellen. Die Fähigkeit zum Interpretieren der generischen sekundären DirectoryEntry-Vorlage ist obligatorisch.

Die Definition von kritischen und unbedenklichen sekundären Verzeichniseinträgen korreliert mit der kleineren ExFAT-Revisionsnummer. Die Unterstützung für alle kritischen oder unbedenklichen sekundären Verzeichniseinträge, die diese Spezifikation oder nachfolgende Spezifikationen definiert, ist optional.

Alle sekundären Verzeichniseintragsstrukturen werden von der generischen sekundären DirectoryEntry-Vorlage abgeleitet (siehe [Tabelle 18](#table-18-generic-secondary-directoryentry-template)), die von der Generischen DirectoryEntry-Vorlage abgeleitet ist (siehe [Abschnitt 6.2](#62-generic-directoryentry-template)).

<div id="table-18-generic-secondary-directoryentry-template" />

**Tabelle 18 Generisches sekundäres VerzeichnisEntry-Vorlage**

<table>
<thead>
<tr class="header">
<th><strong>Feldname</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(Byte)</strong></p></th>
<th><p><strong>Größe</strong></p>
<p><strong>(Byte)</strong></p></th>
<th><strong>Kommentare</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EntryType</td>
<td>0</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#641-entrytype-field">Abschnitt 6.4.1</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>GeneralSecondaryFlags</td>
<td>1</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#642-generalsecondaryflags-field">Abschnitt 6.4.2</a> definiert seinen Inhalt.</td>
</tr>
<tr class="odd">
<td>CustomDefined</td>
<td>2</td>
<td>18</td>
<td>Dieses Feld ist obligatorisch, und Strukturen, die von dieser Vorlage abgeleitet werden, definieren ihren Inhalt.</td>
</tr>
<tr class="even">
<td>FirstCluster</td>
<td>20</td>
<td>4</td>
<td>Dieses Feld ist obligatorisch, und <a href="#643-firstcluster-field">Abschnitt 6.4.3</a> definiert seinen Inhalt.</td>
</tr>
<tr class="odd">
<td>DataLength</td>
<td>24</td>
<td>8</td>
<td>Dieses Feld ist obligatorisch, und <a href="#644-datalength-field">Abschnitt 6.4.4</a> definiert seinen Inhalt.</td>
</tr>
</tbody>
</table>

#### <a name="641-entrytype-field"></a>6.4.1 EntryType-Feld

Das EntryType-Feld muss der Definition in der Generischen DirectoryEntry-Vorlage entsprechen (siehe [Abschnitt 6.2.1](#621-entrytype-field)).

##### <a name="6411-typecode-field"></a>6.4.1.1 TypCodefeld

Das TypeCode-Feld muss der Definition entsprechen, die in der Generischen DirectoryEntry-Vorlage angegeben ist (siehe [Abschnitt 6.2.1.1](#6211-typecode-field)).

##### <a name="6412-typeimportance-field"></a>6.4.1.2 TypeImportance-Feld

Das Feld TypeImportance muss der Definition in der Vorlage Generic DirectoryEntry entsprechen (siehe [Abschnitt 6.2.1.2](#6212-typeimportance-field)).

###### <a name="64121-critical-secondary-directory-entries"></a>6.4.1.2.1 Kritische sekundäre Verzeichniseinträge

Kritische sekundäre Verzeichniseinträge enthalten Informationen, die für die ordnungsgemäße Verwaltung des enthaltenden Verzeichniseintragssatzes von entscheidender Bedeutung sind.
Obwohl die Unterstützung für einen bestimmten kritischen sekundären Verzeichniseintrag optional ist, rendert ein unbekannter kritischer Verzeichniseintrag den gesamten Verzeichniseintragssatz als nicht unbekannt (über die Definition der entsprechenden Verzeichniseintragsvorlagen hinaus).

Wenn ein Verzeichniseintragssatz jedoch mindestens einen kritischen sekundären Verzeichniseintrag enthält, den eine Implementierung nicht erkennt, dann sollte die Implementierung die Vorlagen der Verzeichniseinträge im Verzeichniseintragssatz und nicht die Daten interpretieren, die jede Zuordnung zu einem Verzeichniseintrag im Verzeichniseintragssatz enthält (Dateiverzeichniseinträge sind eine Ausnahme, siehe [Abschnitt 7.4](#74-file-directory-entry)).

###### <a name="64122-benign-secondary-directory-entries"></a>6.4.1.2.2 Unbedenkliche sekundäre Verzeichniseinträge

Unbedenkliche sekundäre Verzeichniseinträge enthalten zusätzliche Informationen, die für die Verwaltung des enthaltenden Verzeichniseintragssets nützlich sein können. Die Unterstützung für jeden spezifischen unschädlichen sekundären Verzeichniseintrag ist optional.
Unbekannte unschädliche sekundäre Verzeichniseinträge rendern nicht den gesamten Verzeichniseintragssatz als nicht unbekannt.

Implementierungen ignorieren möglicherweise alle unbedenklichen sekundären Eintrags, die nicht erkannt werden.

##### <a name="6413-typecategory-field"></a>6.4.1.3 TypeCategory-Feld

Das Feld TypeCategory muss der Definition entsprechen, die in der Vorlage Generic DirectoryEntry bereitgestellt wird (siehe [Abschnitt 6.2.1.3](#6213-typecategory-field)).

Für diese Vorlage ist der gültige Wert für dieses Feld 1.

##### <a name="6414-inuse-field"></a>6.4.1.4 InUse-Feld

Das Feld InUse muss der Definition entsprechen, die in der Vorlage "Generic DirectoryEntry" angegeben ist (siehe [Abschnitt 6.2.1.4](#6214-inuse-field)).

#### <a name="642-generalsecondaryflags-field"></a>6.4.2 GeneralSecondaryFlags-Feld

Das Feld GeneralSecondaryFlags enthält Flags (siehe [Tabelle 19](#table-19-generic-generalsecondaryflags-field-structure)).

<div id="table-19-generic-generalsecondaryflags-field-structure" />

**Tabelle 19: Generische GeneralSecondaryFlags-Feldstruktur**

<table>
<thead>
<tr class="header">
<th><strong>Feldname</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(bit)</strong></p></th>
<th><p><strong>Größe</strong></p>
<p><strong>(Bits)</strong></p></th>
<th><strong>Kommentare</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>AllocationPossible</td>
<td>0</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#6421-allocationpossible-field">in Abschnitt 6.4.2.1 wird</a> der Inhalt definiert.</td>
</tr>
<tr class="even">
<td>NoFatChain</td>
<td>1</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#6422-nofatchain-field">in Abschnitt 6.4.2.2 wird</a> der Inhalt definiert.</td>
</tr>
<tr class="odd">
<td>CustomDefined</td>
<td>2</td>
<td>6</td>
<td>Dieses Feld ist obligatorisch, und Strukturen, die von dieser Vorlage ableiten, können dieses Feld definieren.</td>
</tr>
</tbody>
</table>

##### <a name="6421-allocationpossible-field"></a>6.4.2.1 ZuordnungPossible-Feld

Das Feld AllocationPossible muss die gleiche Definition wie das feld mit dem gleichen Namen in der Vorlage Generic Primary DirectoryEntry haben (siehe [Abschnitt 6.3.4.1](#6341-allocationpossible-field)).

##### <a name="6422-nofatchain-field"></a>6.4.2.2 NoFatChain-Feld

Das Feld NoFatChain muss die gleiche Definition wie das feld mit dem gleichen Namen in der Vorlage Generic Primary DirectoryEntry haben (siehe [Abschnitt 6.3.4.2](#6342-nofatchain-field)).

#### <a name="643-firstcluster-field"></a>6.4.3 FirstCluster-Feld

Das FirstCluster-Feld muss der Definition entsprechen, die in der Vorlage "Generic DirectoryEntry" angegeben ist (siehe [Abschnitt 6.2.2](#622-firstcluster-field)).

Wenn das NoFatChain-Bit 1 ist, muss FirstCluster auf einen gültigen Cluster im Clusterhap verweisen.

#### <a name="644-datalength-field"></a>6.4.4 DataLength-Feld

Das DataLength-Feld muss der Definition entsprechen, die in der Vorlage "Generic DirectoryEntry" angegeben ist (siehe [Abschnitt 6.2.3](#623-datalength-field)).

Wenn das NoFatChain-Bit 1 ist, darf DataLength nicht 0 (null) sein. Wenn das FirstCluster-Feld 0 (null) ist, muss DataLength ebenfalls 0 (null) sein.

## <a name="7-directory-entry-definitions"></a>7 Verzeichniseintragsdefinitionen

Revision 1.00 des exFAT-Dateisystems definiert die folgenden Verzeichniseinträge:

- Kritisches primäres

  - Zuordnungsbitmap ([Abschnitt 7.1](#71-allocation-bitmap-directory-entry))

  - Up-Case-Tabelle ([Abschnitt 7.2](#72-up-case-table-directory-entry))

  - Volumebezeichnung ([Abschnitt 7.3](#73-volume-label-directory-entry))

  - Datei ([Abschnitt 7.4](#74-file-directory-entry))

- Unbedenkliches primäres

  - Volume-GUID ([Abschnitt 7.5](#75-volume-guid-directory-entry))

  - TexFAT Padding ([Abschnitt 7.10](#710-texfat-padding-directory-entry))

<!-- -->

- Kritische sekundäre Replikate

  - Streamerweiterung ([Abschnitt 7.6](#76-stream-extension-directory-entry))

  - Dateiname ([Abschnitt 7.7](#77-file-name-directory-entry))

- Unbedenkliche sekundäre Replikate

  - Anbietererweiterung ([Abschnitt 7.8](#78-vendor-extension-directory-entry))

  - Anbieterzuordnung ([Abschnitt 7.9](#79-vendor-allocation-directory-entry))

### <a name="71-allocation-bitmap-directory-entry"></a>7.1 Zuordnungsbitmap-Verzeichniseintrag

Im exFAT-Dateisystem beschreibt eine FAT-Datei nicht den Zuordnungsstatus von Clustern. stattdessen funktioniert eine Zuordnungsbitmap. Zuordnungsbitmaps sind im Cluster heap vorhanden (siehe Abschnitt [7.1.5](#715-allocation-bitmap)) und verfügen über entsprechende kritische primäre Verzeichniseinträge im Stammverzeichnis (siehe [Tabelle 20](#table-20-allocation-bitmap-directoryentry-structure)).

Das NumberOfFats-Feld bestimmt die Anzahl gültiger Zuordnungsbitmap-Verzeichniseinträge im Stammverzeichnis. Wenn das NumberOfFats-Feld den Wert 1 enthält, ist die einzige gültige Anzahl von Zuordnungsbitmap-Verzeichniseinträgen 1. Darüber hinaus ist der einzige Zuordnungsbitmap-Verzeichniseintrag nur gültig, wenn er die erste Zuordnungsbitmap beschreibt (siehe [Abschnitt 7.1.2.1](#7121-bitmapidentifier-field)). Wenn das Feld NumberOfFats den Wert 2 enthält, ist die einzige gültige Anzahl von Zuordnungsbitmap-Verzeichniseinträgen 2.
Darüber hinaus sind die beiden Zuordnungsbitmap-Verzeichniseinträge nur gültig, wenn eine die erste Zuordnungsbitmap und die andere die zweite Zuordnungsbitmap beschreibt.

<div id="table-20-allocation-bitmap-directoryentry-structure" />

**Table 20 Allocation Bitmap DirectoryEntry Structure**

<table>
<thead>
<tr class="header">
<th><strong>Feldname</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(Byte)</strong></p></th>
<th><p><strong>Größe</strong></p>
<p><strong>(Byte)</strong></p></th>
<th><strong>Kommentare</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EntryType</td>
<td>0</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#711-entrytype-field">in Abschnitt 7.1.1 wird</a> der Inhalt definiert.</td>
</tr>
<tr class="even">
<td>BitmapFlags</td>
<td>1</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#712-bitmapflags-field">in Abschnitt 7.1.2 wird</a> der Inhalt definiert.</td>
</tr>
<tr class="odd">
<td>Reserviert</td>
<td>2</td>
<td>18</td>
<td>Dieses Feld ist obligatorisch, und sein Inhalt ist reserviert.</td>
</tr>
<tr class="even">
<td>FirstCluster</td>
<td>20</td>
<td>4</td>
<td>Dieses Feld ist obligatorisch, und <a href="#713-firstcluster-field">in Abschnitt 7.1.3 wird</a> der Inhalt definiert.</td>
</tr>
<tr class="odd">
<td>DataLength</td>
<td>24</td>
<td>8</td>
<td>Dieses Feld ist obligatorisch, und <a href="#714-datalength-field">in Abschnitt 7.1.4 wird</a> der Inhalt definiert.</td>
</tr>
</tbody>
</table>

#### <a name="711-entrytype-field"></a>7.1.1 EntryType-Feld

Das Feld EntryType muss der Definition entsprechen, die in der Vorlage Generic Primary DirectoryEntry (Generisches primäres Verzeichnis) angegeben ist (siehe [Abschnitt 6.3.1](#631-entrytype-field)).

##### <a name="7111-typecode-field"></a>7.1.1.1 TypeCode-Feld

Das Feld TypeCode muss der Definition entsprechen, die in der Vorlage Generic Primary DirectoryEntry (Generisches primäres Verzeichnis) angegeben ist (siehe [Abschnitt 6.3.1.1](#6311-typecode-field)).

Für einen Zuordnungsbitmap-Verzeichniseintrag ist der gültige Wert für dieses Feld 1.

##### <a name="7112-typeimportance-field"></a>7.1.1.2 TypeImportance Field

Das Feld TypeImportance muss der Definition entsprechen, die in der Vorlage Generic Primary DirectoryEntry (generisches primäres Verzeichnis) angegeben ist (siehe [Abschnitt 6.3.1.2).](#6312-typeimportance-field)

Für einen Zuordnungsbitmap-Verzeichniseintrag ist der gültige Wert für dieses Feld 0.

##### <a name="7113-typecategory-field"></a>7.1.1.3 TypeCategory Field

Das Feld TypeCategory muss der Definition entsprechen, die in der Vorlage Generic Primary DirectoryEntry (siehe [Abschnitt 6.3.1.3)](#6313-typecategory-field)angegeben ist.

##### <a name="7114-inuse-field"></a>7.1.1.4 Feld "InUse"

Das Feld InUse muss der Definition entsprechen, die in der Vorlage Generic Primary DirectoryEntry (siehe [Abschnitt 6.3.1.4)](#6314-inuse-field)angegeben ist.

#### <a name="712-bitmapflags-field"></a>7.1.2 BitmapFlags-Feld

Das Feld BitmapFlags enthält Flags (siehe [Tabelle 21).](#table-21-bitmapflags-field-structure)

<div id="table-21-bitmapflags-field-structure" />

**BitmapFlags-Feldstruktur in Tabelle 21**

<table>
<thead>
<tr class="header">
<th><strong>Feldname</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(Bit)</strong></p></th>
<th><p><strong>Größe</strong></p>
<p><strong>(Bits)</strong></p></th>
<th><strong>Kommentare</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>BitmapIdentifier</td>
<td>0</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#7121-bitmapidentifier-field">Abschnitt 7.1.2.1</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>Reserviert</td>
<td>1</td>
<td>7</td>
<td>Dieses Feld ist obligatorisch, und sein Inhalt ist reserviert.</td>
</tr>
</tbody>
</table>

##### <a name="7121-bitmapidentifier-field"></a>7.1.2.1 BitmapIdentifier-Feld

Das Feld BitmapIdentifier muss angeben, welche Zuordnungsbitmap vom angegebenen Verzeichniseintrag beschrieben wird. Implementierungen müssen die erste Zuordnungsbitmap in Verbindung mit dem ersten FAT und die zweite Zuordnungsbitmap in Verbindung mit dem zweiten FAT verwenden. Das Feld ActiveFat beschreibt, welche FAT- und Allocation Bitmap-Dateien aktiv sind.

Die gültigen Werte für dieses Feld müssen:

- 0, was bedeutet, dass der angegebene Verzeichniseintrag die erste Zuordnungsbitmap beschreibt.

- 1, d. h. der angegebene Verzeichniseintrag beschreibt die zweite Zuordnungsbitmap und ist nur möglich, wenn NumberOfFats den Wert 2 enthält.

#### <a name="713-firstcluster-field"></a>7.1.3 FirstCluster-Feld

Das Feld FirstCluster muss der Definition entsprechen, die in der Vorlage Generic Primary DirectoryEntry (generisches primäres Verzeichnis) angegeben ist (siehe [Abschnitt 6.3.5).](#635-firstcluster-field)

Dieses Feld enthält den Index des ersten Clusters der Clusterkette, wie im FAT beschrieben, der die Zuordnungsbitmap hostet.

#### <a name="714-datalength-field"></a>7.1.4 DataLength-Feld

Das DataCluster-Feld muss der Definition entsprechen, die in der Vorlage Generic Primary DirectoryEntry (siehe [Abschnitt 6.3.6)](#636-datalength-field)angegeben ist.

#### <a name="715-allocation-bitmap"></a>7.1.5 Zuordnungsbitmap

Eine Zuordnungsbitmap zeichnet den Zuordnungsstatus der Cluster im Clusterheap auf. Jedes Bit in einer Zuordnungsbitmap gibt an, ob der entsprechende Cluster für die Zuordnung verfügbar ist.

Eine Zuordnungsbitmap stellt Cluster vom niedrigsten zum höchsten Index dar (siehe [Tabelle 22).](#table-22-allocation-bitmap-structure) Aus historischen Gründen weist der erste Cluster den Index 2 auf.
Hinweis: Das erste Bit in der Bitmap ist das Bit der niedrigsten Reihenfolge des ersten Byte.

<div id="table-22-allocation-bitmap-structure" />

**Table 22 Allocation Bitmap Structure**

<table>
<thead>
<tr class="header">
<th><strong>Feldname</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(Bit)</strong></p></th>
<th><p><strong>Größe</strong></p>
<p><strong>(Bits)</strong></p></th>
<th><strong>Kommentare</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>BitmapEntry[2]</td>
<td>0</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#7151-bitmapentry2--bitmapentryclustercount1-fields">Abschnitt 7.1.5.1</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
</tr>
<tr class="odd">
<td>BitmapEntry[ClusterCount+1]</td>
<td>ClusterCount – 1</td>
<td>1</td>
<td><p>Dieses Feld ist obligatorisch, und <a href="#7151-bitmapentry2--bitmapentryclustercount1-fields">Abschnitt 7.1.5.1</a> definiert seinen Inhalt.</p>
<p>Hinweis: Die Haupt- und Sicherungsstartsektoren enthalten beide das Feld ClusterCount.</p></td>
</tr>
<tr class="even">
<td>Reserviert</td>
<td>ClusterCount</td>
<td>(DataLength * 8) – ClusterCount</td>
<td><p>Dieses Feld ist obligatorisch, und sein Inhalt, falls vorhanden, ist reserviert.</p>
<p>Hinweis: Die Haupt- und Sicherungsstartsektoren enthalten beide das Feld ClusterCount.</p></td>
</tr>
</tbody>
</table>

##### <a name="7151-bitmapentry2--bitmapentryclustercount1-fields"></a>7.1.5.1 BitmapEntry \[ 2 \] ... BitmapEntry \[ ClusterCount+1 \] Fields

Jedes BitmapEntry-Feld in diesem Array stellt einen Cluster im Clusterheap dar. BitmapEntry \[ 2 \] stellt den ersten Cluster im Clusterheap und BitmapEntry \[ ClusterCount+1 \] den letzten Cluster im Clusterheap dar.

Die gültigen Werte für diese Felder müssen:

- 0, der den entsprechenden Cluster als verfügbar für die Zuordnung beschreibt

- 1: Beschreibt den entsprechenden Cluster als nicht für die Zuordnung verfügbar (eine Clusterzuordnung belegt möglicherweise bereits den entsprechenden Cluster, oder das aktive FAT kann den entsprechenden Cluster als fehlerhaft beschreiben).

### <a name="72-up-case-table-directory-entry"></a>7.2 Up-case Table Directory Entry

Die Up-Case-Tabelle definiert die Konvertierung von Kleinbuchstaben in Großbuchstaben. Dies ist wichtig, da der Verzeichniseintrag Dateiname (siehe Abschnitt 7.7) Unicode-Zeichen verwendet und das exFAT-Dateisystem die Groß-/Kleinschreibung nicht beachtet und die Groß-/Kleinschreibung beibehalten wird. Die Up-Case-Tabelle ist im Clusterheap vorhanden (siehe [Abschnitt 7.2.5](#725-up-case-table)) und verfügt über einen entsprechenden kritischen primären Verzeichniseintrag im Stammverzeichnis (siehe [Tabelle 23).](#table-23-up-case-table-directoryentry-structure) Die gültige Anzahl von Einträgen im Up-Case-Tabellenverzeichnis ist 1.

Aufgrund der Beziehung zwischen der Up-Case-Tabelle und dateinamen sollten Implementierungen die Up-Case-Tabelle nur aufgrund von Formatvorgängen ändern.

<div id="table-23-up-case-table-directoryentry-structure" />

**Table 23 Up-case Table DirectoryEntry Structure**

<table>
<thead>
<tr class="header">
<th><strong>Feldname</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(Byte)</strong></p></th>
<th><p><strong>Größe</strong></p>
<p><strong>(Byte)</strong></p></th>
<th><strong>Kommentare</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EntryType</td>
<td>0</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#721-entrytype-field">Abschnitt 7.2.1</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>Reserved1</td>
<td>1</td>
<td>3</td>
<td>Dieses Feld ist obligatorisch, und sein Inhalt ist reserviert.</td>
</tr>
<tr class="odd">
<td>TableChecksum</td>
<td>4</td>
<td>4</td>
<td>Dieses Feld ist obligatorisch, und <a href="#722-tablechecksum-field">Abschnitt 7.2.2</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>Reserved2</td>
<td>8</td>
<td>12</td>
<td>Dieses Feld ist obligatorisch, und sein Inhalt ist reserviert.</td>
</tr>
<tr class="odd">
<td>FirstCluster</td>
<td>20</td>
<td>4</td>
<td>Dieses Feld ist obligatorisch, und <a href="#723-firstcluster-field">in Abschnitt 7.2.3 wird</a> der Inhalt definiert.</td>
</tr>
<tr class="even">
<td>DataLength</td>
<td>24</td>
<td>8</td>
<td>Dieses Feld ist obligatorisch, und <a href="#724-datalength-field">in Abschnitt 7.2.4 wird</a> der Inhalt definiert.</td>
</tr>
</tbody>
</table>

#### <a name="721-entrytype-field"></a>7.2.1 EntryType-Feld

Das Feld EntryType muss der Definition entsprechen, die in der Vorlage Generic Primary DirectoryEntry (Generisches primäres Verzeichnis) angegeben ist (siehe [Abschnitt 6.3.1](#631-entrytype-field)).

##### <a name="7211-typecode-field"></a>7.2.1.1 TypeCode-Feld

Das Feld TypeCode muss der Definition entsprechen, die in der Vorlage Generic Primary DirectoryEntry (Generisches primäres Verzeichnis) angegeben ist (siehe [Abschnitt 6.3.1.1](#6311-typecode-field)).

Für den Verzeichniseintrag Up-case Table ist der gültige Wert für dieses Feld.
2.

##### <a name="7212-typeimportance-field"></a>7.2.1.2 TypeImportance-Feld

Das Feld TypeImportance muss der Definition entsprechen, die in der Vorlage Generic Primary DirectoryEntry (Generisches primäres Verzeichnis) angegeben ist (siehe [Abschnitt 6.3.1.2](#6312-typeimportance-field)).

Für den Verzeichniseintrag Up-case Table ist der gültige Wert für dieses Feld.
0.

##### <a name="7213-typecategory-field"></a>7.2.1.3 TypeCategory-Feld

Das Feld TypeCategory muss der Definition entsprechen, die in der Vorlage Generic Primary DirectoryEntry (Generisches primäres Verzeichnis) angegeben ist (siehe [Abschnitt 6.3.1.3](#6313-typecategory-field)).

##### <a name="7214-inuse-field"></a>7.2.1.4 InUse-Feld

Das Feld InUse muss der Definition entsprechen, die in der Vorlage Generic Primary DirectoryEntry (Generisches primäres Verzeichnis) angegeben ist (siehe [Abschnitt 6.3.1.4](#6314-inuse-field)).

#### <a name="722-tablechecksum-field"></a>7.2.2 TableChecksum-Feld

Das Feld TableChecksum enthält die Prüfsumme der Up-case-Tabelle (die in den Feldern FirstCluster und DataLength beschrieben wird). Implementierungen müssen überprüfen, ob der Inhalt dieses Felds gültig ist, bevor die Up-case-Tabelle verwendet wird.

<div id="figure-3-tablechecksum-computation" />

**Abbildung 3 TableChecksum-Berechnung**

```C
UInt32 TableChecksum
(
    UCHAR  * Table,    // points to an in-memory copy of the up-case table
    UInt64   DataLength
)
{
    UInt32 Checksum = 0;
    UInt64 Index;

    for (Index = 0; Index < DataLength; Index++)
    {
        Checksum = ((Checksum&1) ? 0x80000000 : 0) + (Checksum>>1) + (UInt32)Table[Index];
    }

    return Checksum;
}
```

#### <a name="723-firstcluster-field"></a>7.2.3 FirstCluster-Feld

Das FirstCluster-Feld muss der Definition entsprechen, die in der Vorlage Generic Primary DirectoryEntry (Generisches primäres Verzeichnis) angegeben ist (siehe [Abschnitt 6.3.5](#635-firstcluster-field)).

Dieses Feld enthält den Index des ersten Clusters der Clusterkette, wie von FAT beschrieben, der die Up-case-Tabelle hostet.

#### <a name="724-datalength-field"></a>7.2.4 DataLength-Feld

Das DataCluster-Feld muss der Definition entsprechen, die in der Vorlage Generic Primary DirectoryEntry (Generisches primäres Verzeichnis) angegeben ist (siehe [Abschnitt 6.3.6](#636-datalength-field)).

#### <a name="725-up-case-table"></a>7.2.5 Up-Case-Tabelle

Eine Up-Case-Tabelle ist eine Reihe von Unicode-Zeichenzuordnungen. Eine Zeichenzuordnung besteht aus einem 2-Byte-Feld, bei dem der Index des Felds in der Up-Case-Tabelle das Unicode-Zeichen darstellt, für das die 2-Byte-Case-Zeichenfolge verwendet werden soll, und das 2-Byte-Feld, das das Unicode-Zeichen mit voraufgekannten Zeichen darstellt.

Die ersten 128 Unicode-Zeichen verfügen über obligatorische Zuordnungen (siehe [Tabelle 24](#table-24-mandatory-first-128-up-case-table-entries)).
Eine Up-Case-Tabelle mit einer anderen Zeichenzuordnung für eines der ersten 128 Unicode-Zeichen ist ungültig.

Implementierungen, die nur Zeichen aus dem obligatorischen Zuordnungsbereich unterstützen, ignorieren möglicherweise die Zuordnungen der restlichen Up-Case-Tabelle. Solche Implementierungen dürfen beim Erstellen oder Umbenennen von Dateien nur Zeichen aus dem obligatorischen Zuordnungsbereich verwenden (siehe Abschnitt [7.7](#77-file-name-directory-entry)). Wenn sie vorhandene Dateinamen in eine neue Schreib schreibe, dürfen solche Implementierungen keine Zeichen aus dem nicht obligatorischen Zuordnungsbereich verwenden, sondern sie im resultierenden Dateinamen mit vorgeänderten Schreibfehlern intakt lassen (dies ist eine partielle Auf-Schreib-/Schreibmaschierung). Beim Vergleichen von Dateinamen müssen solche Implementierungen Dateinamen, die sich vom verglichenen Namen unterscheiden, nur durch Unicode-Zeichen aus dem nicht obligatorischen Zuordnungsbereich als gleichwertig behandeln. Obwohl solche Dateinamen nur potenziell äquivalent sind, können solche Implementierungen nicht sicherstellen, dass der Dateiname mit der vollständigen Hochsentsprechung nicht mit dem zu vergleichenden Namen in Zusammenhang steht.

<div id="table-24-mandatory-first-128-up-case-table-entries" />

**Tabelle 24: Obligatorische erste 128 Einträge in Einer-Fall-Tabelle**

| Tabellenindex | + 0 | + 1 | + 2 | + 3 | + 4 | + 5 | + 6 | + 7 |
|-----------------|-------------------|-----------|-----------|-----------|-----------|-----------|-----------|-----------|
| **0000h**       | 0000h             | 0001h     | 0002h     | 0003h     | 0004h     | 0005h     | 0006h     | 0007h     |
| **0008h**       | 0008h             | 0009h     | 000Ah     | 000Bh     | 000Ch     | 000Dh     | 000Eh     | 000Fh     |
| **0010h**       | 0010h             | 0011h     | 0012h     | 0013h     | 0014h     | 0015h     | 0016h     | 0017h     |
| **0018h**       | 0018h             | 0019h     | 001Ah     | 001Bh     | 001Ch     | 001Dh     | 001Eh     | 001Fh     |
| **0020h**       | 0020h             | 0021h     | 0022h     | 0023h     | 0024h     | 0025h     | 0026h     | 0027h     |
| **0028h**       | 0028h             | 0029h     | 002Ah     | 002Bh     | 002Ch     | 002Dh     | 002Eh     | 002Fh     |
| **0030h**       | 0030h             | 0031h     | 0032h     | 0033h     | 0034h     | 0035h     | 0036h     | 0037h     |
| **0038h**       | 0038h             | 0039h     | 003Ah     | 003Bh     | 003Ch     | 003Dh     | 003Eh     | 003Fh     |
| **0040h**       | 0040h             | 0041h     | 0042h     | 0043h     | 0044h     | 0045h     | 0046h     | 0047h     |
| **0048h**       | 0048h             | 0049h     | 004Ah     | 004Bh     | 004Ch     | 004Dh     | 004Eh     | 004Fh     |
| **0050h**       | 0050h             | 0051h     | 0052h     | 0053h     | 0054h     | 0055h     | 0056h     | 0057h     |
| **0058h**       | 0058h             | 0059h     | 005Ah     | 005Bh     | 005Ch     | 005Dh     | 005Eh     | 005Fh     |
| **0060h**       | 0060h             | **0041h** | **0042h** | **0043h** | **0044h** | **0045h** | **0046h** | **0047h** |
| **0068h**       | **0048h**         | **0049h** | **004Ah** | **004Bh** | **004Ch** | **004Dh** | **004Eh** | **004Fh** |
| **0070h**       | **0050h**         | **0051h** | **0052h** | **0053h** | **0054h** | **0055h** | **0056h** | **0057h** |
| **0078h**       | **0058h**         | **0059h** | **005Ah** | 007Bh     | 007Ch     | 007Dh     | 007Eh     | 007Fh     |

**(Hinweis: Einträge mit Up-Case-Zuordnungen ohne Identität sind fett formatiert.)**

Beim Formatieren eines Volumes können Implementierungen eine Up-Case-Tabelle in einem komprimierten Format mithilfe der Komprimierung der Identitätszuordnung generieren, da ein großer Teil des Unicode-Zeichenraums kein Konzept der Groß-/Klein-Groß-/Klein formatiert hat (was bedeutet, dass die Zeichen "klein" und "groß" gleichwertig sind).
Implementierungen komprimieren eine Up-Case-Tabelle, indem sie eine Reihe von Identitätszuordnungen mit dem Wert FFFFh gefolgt von der Anzahl der Identitätszuordnungen darstellen.

Beispielsweise kann eine Implementierung die ersten 100 (64h) Zeichenzuordnungen mit den folgenden acht Einträgen einer komprimierten Up-Case-Tabelle darstellen:

> FFFFh, 0061h, 0041h, 0042h, 0043h

Die ersten beiden Einträge geben an, dass die ersten 97 (61h) Zeichen (von 0000h bis 0060h) identitätszuordnungen haben. Die nachfolgenden Zeichen 0061h bis 0063h sind den Zeichen 0041h bis 0043h bzw.

Die Möglichkeit, beim Formatieren eines Volumes eine komprimierte Up-Case-Tabelle zur Verfügung zu stellen, ist optional. Die Möglichkeit, sowohl eine unkomprimierte als auch eine komprimierte Up-Case-Tabelle zu interpretieren, ist jedoch obligatorisch. Der Wert des TableChecksum-Felds entspricht immer der Art und Weise, wie die Up-Case-Tabelle auf dem Volume vorhanden ist, die entweder im komprimierten oder unkomprimierten Format vorliegen kann.

##### <a name="7251-recommended-up-case-table"></a>7.2.5.1 Empfohlene Up-Case-Tabelle

Beim Formatieren eines Volumes sollten Implementierungen die empfohlene Up-Case-Tabelle im komprimierten Format aufzeichnen (siehe Tabelle [25](#table-25-recommended-up-case-table-in-compressed-format)), für die der Wert des TableChecksum-Felds E619D30Dh ist.

Wenn eine Implementierung eine eigene Up-Case-Tabelle definiert , entweder komprimiert oder unkomprimiert, dann muss diese Tabelle den gesamten Unicode-Zeichenbereich abdecken (von Zeichencodes 0000h bis einschließlich FFFFh).

<div id="table-25-recommended-up-case-table-in-compressed-format" />

**Tabelle 25 Empfohlene Up-Case-Tabelle im komprimierten Format**

| Rohoffset | + 0 |  + 1       |  + 2       |  + 3       |  + 4       | + 5        |  + 6       | + 7        |
|----------------|------------------------------|---------|---------|---------|---------|---------|---------|---------|
| **0000h**      | 0000h                        | 0001h   | 0002h   | 0003h   | 0004h   | 0005h   | 0006h   | 0007h   |
| **0008h**      | 0008h                        | 0009h   | 000Ah   | 000Bh   | 000Ch   | 000Dh   | 000Eh   | 000Fh   |
| **0010h**      | 0010h                        | 0011h   | 0012h   | 0013h   | 0014h   | 0015h   | 0016h   | 0017h   |
| **0018h**      | 0018h                        | 0019h   | 001Ah   | 001Bh   | 001Ch   | 001Dh   | 001Eh   | 001Fh   |
| **0020h**      | 0020h                        | 0021h   | 0022h   | 0023h   | 0024h   | 0025h   | 0026h   | 0027h   |
| **0028h**      | 0028h                        | 0029h   | 002Ah   | 002Bh   | 002Ch   | 002Dh   | 002Eh   | 002Fh   |
| **0030h**      | 0030h                        | 0031h   | 0032h   | 0033h   | 0034h   | 0035h   | 0036h   | 0037h   |
| **0038h**      | 0038h                        | 0039h   | 003Ah   | 003Bh   | 003Ch   | 003Dh   | 003Eh   | 003Fh   |
| **0040h**      | 0040h                        | 0041h   | 0042h   | 0043h   | 0044h   | 0045h   | 0046h   | 0047h   |
| **0048h**      | 0048h                        | 0049h   | 004Ah   | 004Bh   | 004Ch   | 004Dh   | 004Eh   | 004Fh   |
| **0050h**      | 0050h                        | 0051h   | 0052h   | 0053h   | 0054h   | 0055h   | 0056h   | 0057h   |
| **0058h**      | 0058h                        | 0059h   | 005Ah   | 005Bh   | 005Ch   | 005Dh   | 005Eh   | 005Fh   |
| **0060h**      | 0060h                        | 0041h   | 0042h   | 0043h   | 0044h   | 0045h   | 0046h   | 0047h   |
| **0068h**      | 0048h                        | 0049h   | 004Ah   | 004Bh   | 004Ch   | 004Dh   | 004Eh   | 004Fh   |
| **0070h**      | 0050h                        | 0051h   | 0052h   | 0053h   | 0054h   | 0055h   | 0056h   | 0057h   |
| **0078h**      | 0058h                        | 0059h   | 005Ah   | 007Bh   | 007Ch   | 007Dh   | 007Eh   | 007Fh   |
| **0080h**      | 0080h                        | 0081h   | 0082h   | 0083h   | 0084h   | 0085h   | 0086h   | 0087h   |
| **0088h**      | 0088h                        | 0089h   | 008Ah   | 008Bh   | 008Ch   | 008Dh   | 008Eh   | 008Fh   |
| **0090h**      | 0090h                        | 0091h   | 0092h   | 0093h   | 0094h   | 0095h   | 0096h   | 0097h   |
| **0098h**      | 0098h                        | 0099h   | 009Ah   | 009Bh   | 009Ch   | 009Dh   | 009Eh   | 009Fh   |
| **00A0h**      | 00A0h                        | 00A1h   | 00A2h   | 00A3h   | 00A4h   | 00A5h   | 00A6h   | 00A7h   |
| **00A8h**      | 00A8h                        | 00A9h   | 00AAh   | 00ABh   | 00ACh   | 00ADh   | 00AEh   | 00AFh   |
| **00B0h**      | 00B0h                        | 00B1h   | 00B2h   | 00B3h   | 00B4h   | 00B5h   | 00B6h   | 00B7h   |
| **00B8h**      | 00B8h                        | 00B9h   | 00BAh   | 00BBh   | 00BCh   | 00BDh   | 00BEh   | 00BFh   |
| **00C0h**      | 00C0h                        | 00C1h   | 00C2h   | 00C3h   | 00C4h   | 00C5h   | 00C6h   | 00C7h   |
| **00C8h**      | 00C8h                        | 00C9h   | 00CAh   | 00CBh   | 00CCh   | 00CDh   | 00CEh   | 00CFh   |
| **00D0h**      | 00D0h                        | 00D1h   | 00D2h   | 00D3h   | 00D4h   | 00D5h   | 00D6h   | 00D7h   |
| **00D8h**      | 00D8h                        | 00D9h   | 00DAh   | 00DBh   | 00DCh   | 00DDh   | 00DEh   | 00DFh   |
| **00E0h**      | 00C0h                        | 00C1h   | 00C2h   | 00C3h   | 00C4h   | 00C5h   | 00C6h   | 00C7h   |
| **00E8h**      | 00C8h                        | 00C9h   | 00CAh   | 00CBh   | 00CCh   | 00CDh   | 00CEh   | 00CFh   |
| **00F0h**      | 00D0h                        | 00D1h   | 00D2h   | 00D3h   | 00D4h   | 00D5h   | 00D6h   | 00F7h   |
| **00F8h**      | 00D8h                        | 00D9h   | 00DAh   | 00DBh   | 00DCh   | 00DDh   | 00DEh   | 0178h   |
| **0100h**      | 0100h                        | 0100h   | 0102h   | 0102h   | 0104h   | 0104h   | 0106h   | 0106h   |
| **0108h**      | 0108h                        | 0108h   | 010Ah   | 010Ah   | 010Ch   | 010Ch   | 010Eh   | 010Eh   |
| **0110h**      | 0110h                        | 0110h   | 0112h   | 0112h   | 0114h   | 0114h   | 0116h   | 0116h   |
| **0118h**      | 0118h                        | 0118h   | 011Ah   | 011Ah   | 011Ch   | 011Ch   | 011Eh   | 011Eh   |
| **0120h**      | 0120h                        | 0120h   | 0122h   | 0122h   | 0124h   | 0124h   | 0126h   | 0126h   |
| **0128h**      | 0128h                        | 0128h   | 012Ah   | 012Ah   | 012Ch   | 012Ch   | 012Eh   | 012Eh   |
| **0130h**      | 0130h                        | 0131h   | 0132h   | 0132h   | 0134h   | 0134h   | 0136h   | 0136h   |
| **0138h**      | 0138h                        | 0139h   | 0139h   | 013Bh   | 013Bh   | 013Dh   | 013Dh   | 013Fh   |
| **0140h**      | 013Fh                        | 0141h   | 0141h   | 0143h   | 0143h   | 0145h   | 0145h   | 0147h   |
| **0148h**      | 0147h                        | 0149h   | 014Ah   | 014Ah   | 014Ch   | 014Ch   | 014Eh   | 014Eh   |
| **0150h**      | 0150h                        | 0150h   | 0152h   | 0152h   | 0154h   | 0154h   | 0156h   | 0156h   |
| **0158h**      | 0158h                        | 0158h   | 015Ah   | 015Ah   | 015Ch   | 015Ch   | 015Eh   | 015Eh   |
| **0160h**      | 0160h                        | 0160h   | 0162h   | 0162h   | 0164h   | 0164h   | 0166h   | 0166h   |
| **0168h**      | 0168h                        | 0168h   | 016Ah   | 016Ah   | 016Ch   | 016Ch   | 016Eh   | 016Eh   |
| **0170h**      | 0170h                        | 0170h   | 0172h   | 0172h   | 0174h   | 0174h   | 0176h   | 0176h   |
| **0178h**      | 0178h                        | 0179h   | 0179h   | 017Bh   | 017Bh   | 017Dh   | 017Dh   | 017Fh   |
| **0180h**      | 0243h                        | 0181h   | 0182h   | 0182h   | 0184h   | 0184h   | 0186h   | 0187h   |
| **0188h**      | 0187h                        | 0189h   | 018Ah   | 018Bh   | 018Bh   | 018Dh   | 018Eh   | 018Fh   |
| **0190h**      | 0190h                        | 0191h   | 0191h   | 0193h   | 0194h   | 01F6h   | 0196h   | 0197h   |
| **0198h**      | 0198h                        | 0198h   | 023Dh   | 019Bh   | 019Ch   | 019Dh   | 0220h   | 019Fh   |
| **01A0h**      | 01A0h                        | 01A0h   | 01A2h   | 01A2h   | 01A4h   | 01A4h   | 01A6h   | 01A7h   |
| **01A8h**      | 01A7h                        | 01A9h   | 01AAh   | 01ABh   | 01ACh   | 01ACh   | 01AEh   | 01AFh   |
| **01B0h**      | 01AFh                        | 01B1h   | 01B2h   | 01B3h   | 01B3h   | 01B5h   | 01B5h   | 01B7h   |
| **01B8h**      | 01B8h                        | 01B8h   | 01BAh   | 01BBh   | 01BCh   | 01BCh   | 01BEh   | 01F7h   |
| **01C0h**      | 01C0h                        | 01C1h   | 01C2h   | 01C3h   | 01C4h   | 01C5h   | 01C4h   | 01C7h   |
| **01C8h**      | 01C8h                        | 01C7h   | 01CAh   | 01CBh   | 01CAh   | 01CDh   | 01CDh   | 01CFh   |
| **01D0h**      | 01CFh                        | 01D1h   | 01D1h   | 01D3h   | 01D3h   | 01D5h   | 01D5h   | 01D7h   |
| **01D8h**      | 01D7h                        | 01D9h   | 01D9h   | 01DBh   | 01DBh   | 018Eh   | 01DEh   | 01DEh   |
| **01E0h**      | 01E0h                        | 01E0h   | 01E2h   | 01E2h   | 01E4h   | 01E4h   | 01E6h   | 01E6h   |
| **01E8h**      | 01E8h                        | 01E8h   | 01EAh   | 01EAh   | 01ECh   | 01ECh   | 01EEh   | 01EEh   |
| **01F0h**      | 01F0h                        | 01F1h   | 01F2h   | 01F1h   | 01F4h   | 01F4h   | 01F6h   | 01F7h   |
| **01F8h**      | 01F8h                        | 01F8h   | 01FAh   | 01FAh   | 01FCh   | 01FCh   | 01FEh   | 01FEh   |
| **0200h**      | 0200h                        | 0200h   | 0202h   | 0202h   | 0204h   | 0204h   | 0206h   | 0206h   |
| **0208h**      | 0208h                        | 0208h   | 020Ah   | 020Ah   | 020Ch   | 020Ch   | 020Eh   | 020Eh   |
| **0210h**      | 0210h                        | 0210h   | 0212h   | 0212h   | 0214h   | 0214h   | 0216h   | 0216h   |
| **0218h**      | 0218h                        | 0218h   | 021Ah   | 021Ah   | 021Ch   | 021Ch   | 021Eh   | 021Eh   |
| **0220h**      | 0220h                        | 0221h   | 0222h   | 0222h   | 0224h   | 0224h   | 0226h   | 0226h   |
| **0228h**      | 0228h                        | 0228h   | 022Ah   | 022Ah   | 022Ch   | 022Ch   | 022Eh   | 022Eh   |
| **0230h**      | 0230h                        | 0230h   | 0232h   | 0232h   | 0234h   | 0235h   | 0236h   | 0237h   |
| **0238h**      | 0238h                        | 0239h   | 2C65h   | 023Bh   | 023Bh   | 023Dh   | 2C66h   | 023Fh   |
| **0240h**      | 0240h                        | 0241h   | 0241h   | 0243h   | 0244h   | 0245h   | 0246h   | 0246h   |
| **0248h**      | 0248h                        | 0248h   | 024Ah   | 024Ah   | 024Ch   | 024Ch   | 024Eh   | 024Eh   |
| **0250h**      | 0250h                        | 0251h   | 0252h   | 0181h   | 0186h   | 0255h   | 0189h   | 018Ah   |
| **0258h**      | 0258h                        | 018Fh   | 025Ah   | 0190h   | 025Ch   | 025Dh   | 025Eh   | 025Fh   |
| **0260h**      | 0193h                        | 0261h   | 0262h   | 0194h   | 0264h   | 0265h   | 0266h   | 0267h   |
| **0268h**      | 0197h                        | 0196h   | 026Ah   | 2C62h   | 026Ch   | 026Dh   | 026Eh   | 019Ch   |
| **0270h**      | 0270h                        | 0271h   | 019Dh   | 0273h   | 0274h   | 019Fh   | 0276h   | 0277h   |
| **0278h**      | 0278h                        | 0279h   | 027Ah   | 027Bh   | 027Ch   | 2C64h   | 027Eh   | 027Fh   |
| **0280h**      | 01A6h                        | 0281h   | 0282h   | 01A9h   | 0284h   | 0285h   | 0286h   | 0287h   |
| **0288h**      | 01AEh                        | 0244h   | 01B1h   | 01B2h   | 0245h   | 028Dh   | 028Eh   | 028Fh   |
| **0290h**      | 0290h                        | 0291h   | 01B7h   | 0293h   | 0294h   | 0295h   | 0296h   | 0297h   |
| **0298h**      | 0298h                        | 0299h   | 029Ah   | 029Bh   | 029Ch   | 029Dh   | 029Eh   | 029Fh   |
| **02A0h**      | 02A0h                        | 02A1h   | 02A2h   | 02A3h   | 02A4h   | 02A5h   | 02A6h   | 02A7h   |
| **02A8h**      | 02A8h                        | 02A9h   | 02AAh   | 02ABh   | 02ACh   | 02ADh   | 02AEh   | 02AFh   |
| **02B0h**      | 02B0h                        | 02B1h   | 02B2h   | 02B3h   | 02B4h   | 02B5h   | 02B6h   | 02B7h   |
| **02B8h**      | 02B8h                        | 02B9h   | 02BAh   | 02BBh   | 02BCh   | 02BDh   | 02BEh   | 02BFh   |
| **02C0h**      | 02C0h                        | 02C1h   | 02C2h   | 02C3h   | 02C4h   | 02C5h   | 02C6h   | 02C7h   |
| **02C8h**      | 02C8h                        | 02C9h   | 02CAh   | 02CBh   | 02CCh   | 02CDh   | 02CEh   | 02CFh   |
| **02D0h**      | 02D0h                        | 02D1h   | 02D2h   | 02D3h   | 02D4h   | 02D5h   | 02D6h   | 02D7h   |
| **02D8h**      | 02D8h                        | 02D9h   | 02DAh   | 02DBh   | 02DCh   | 02DDh   | 02DEh   | 02DFh   |
| **02E0h**      | 02E0h                        | 02E1h   | 02E2h   | 02E3h   | 02E4h   | 02E5h   | 02E6h   | 02E7h   |
| **02E8h**      | 02E8h                        | 02E9h   | 02EAh   | 02EBh   | 02ECh   | 02EDh   | 02EEh   | 02EFh   |
| **02F0h**      | 02F0h                        | 02F1h   | 02F2h   | 02F3h   | 02F4h   | 02F5h   | 02F6h   | 02F7h   |
| **02F8h**      | 02F8h                        | 02F9h   | 02FAh   | 02FBh   | 02FCh   | 02FDh   | 02FEh   | 02FFh   |
| **0300h**      | 0300h                        | 0301h   | 0302h   | 0303h   | 0304h   | 0305h   | 0306h   | 0307h   |
| **0308h**      | 0308h                        | 0309h   | 030Ah   | 030Bh   | 030Ch   | 030Dh   | 030Eh   | 030Fh   |
| **0310h**      | 0310h                        | 0311h   | 0312h   | 0313h   | 0314h   | 0315h   | 0316h   | 0317h   |
| **0318h**      | 0318h                        | 0319h   | 031Ah   | 031Bh   | 031Ch   | 031Dh   | 031Eh   | 031Fh   |
| **0320h**      | 0320h                        | 0321h   | 0322h   | 0323h   | 0324h   | 0325h   | 0326h   | 0327h   |
| **0328h**      | 0328h                        | 0329h   | 032Ah   | 032Bh   | 032Ch   | 032Dh   | 032Eh   | 032Fh   |
| **0330h**      | 0330h                        | 0331h   | 0332h   | 0333h   | 0334h   | 0335h   | 0336h   | 0337h   |
| **0338h**      | 0338h                        | 0339h   | 033Ah   | 033Bh   | 033Ch   | 033Dh   | 033Eh   | 033Fh   |
| **0340h**      | 0340h                        | 0341h   | 0342h   | 0343h   | 0344h   | 0345h   | 0346h   | 0347h   |
| **0348h**      | 0348h                        | 0349h   | 034Ah   | 034Bh   | 034Ch   | 034Dh   | 034Eh   | 034Fh   |
| **0350h**      | 0350h                        | 0351h   | 0352h   | 0353h   | 0354h   | 0355h   | 0356h   | 0357h   |
| **0358h**      | 0358h                        | 0359h   | 035Ah   | 035Bh   | 035Ch   | 035Dh   | 035Eh   | 035Fh   |
| **0360h**      | 0360h                        | 0361h   | 0362h   | 0363h   | 0364h   | 0365h   | 0366h   | 0367h   |
| **0368h**      | 0368h                        | 0369h   | 036Ah   | 036Bh   | 036Ch   | 036Dh   | 036Eh   | 036Fh   |
| **0370h**      | 0370h                        | 0371h   | 0372h   | 0373h   | 0374h   | 0375h   | 0376h   | 0377h   |
| **0378h**      | 0378h                        | 0379h   | 037Ah   | 03FDh   | 03FEh   | 03FFh   | 037Eh   | 037Fh   |
| **0380h**      | 0380h                        | 0381h   | 0382h   | 0383h   | 0384h   | 0385h   | 0386h   | 0387h   |
| **0388h**      | 0388h                        | 0389h   | 038Ah   | 038Bh   | 038Ch   | 038Dh   | 038Eh   | 038Fh   |
| **0390h**      | 0390h                        | 0391h   | 0392h   | 0393h   | 0394h   | 0395h   | 0396h   | 0397h   |
| **0398h**      | 0398h                        | 0399h   | 039Ah   | 039Bh   | 039Ch   | 039Dh   | 039Eh   | 039Fh   |
| **03A0h**      | 03A0h                        | 03A1h   | 03A2h   | 03A3h   | 03A4h   | 03A5h   | 03A6h   | 03A7h   |
| **03A8h**      | 03A8h                        | 03A9h   | 03AAh   | 03ABh   | 0386h   | 0388h   | 0389h   | 038Ah   |
| **03B0h**      | 03B0h                        | 0391h   | 0392h   | 0393h   | 0394h   | 0395h   | 0396h   | 0397h   |
| **03B8h**      | 0398h                        | 0399h   | 039Ah   | 039Bh   | 039Ch   | 039Dh   | 039Eh   | 039Fh   |
| **03C0h**      | 03A0h                        | 03A1h   | 03A3h   | 03A3h   | 03A4h   | 03A5h   | 03A6h   | 03A7h   |
| **03C8h**      | 03A8h                        | 03A9h   | 03AAh   | 03ABh   | 038Ch   | 038Eh   | 038Fh   | 03CFh   |
| **03D0h**      | 03D0h                        | 03D1h   | 03D2h   | 03D3h   | 03D4h   | 03D5h   | 03D6h   | 03D7h   |
| **03D8h**      | 03D8h                        | 03D8h   | 03DAh   | 03DAh   | 03DCh   | 03DCh   | 03DEh   | 03DEh   |
| **03E0h**      | 03E0h                        | 03E0h   | 03E2h   | 03E2h   | 03E4h   | 03E4h   | 03E6h   | 03E6h   |
| **03E8h**      | 03E8h                        | 03E8h   | 03EAh   | 03EAh   | 03ECh   | 03ECh   | 03EEh   | 03EEh   |
| **03F0h**      | 03F0h                        | 03F1h   | 03F9h   | 03F3h   | 03F4h   | 03F5h   | 03F6h   | 03F7h   |
| **03F8h**      | 03F7h                        | 03F9h   | 03FAh   | 03FAh   | 03FCh   | 03FDh   | 03FEh   | 03FFh   |
| **0400h**      | 0400h                        | 0401h   | 0402h   | 0403h   | 0404h   | 0405h   | 0406h   | 0407h   |
| **0408h**      | 0408h                        | 0409h   | 040Ah   | 040Bh   | 040Ch   | 040Dh   | 040Eh   | 040Fh   |
| **0410h**      | 0410h                        | 0411h   | 0412h   | 0413h   | 0414h   | 0415h   | 0416h   | 0417h   |
| **0418h**      | 0418h                        | 0419h   | 041Ah   | 041Bh   | 041Ch   | 041Dh   | 041Eh   | 041Fh   |
| **0420h**      | 0420h                        | 0421h   | 0422h   | 0423h   | 0424h   | 0425h   | 0426h   | 0427h   |
| **0428h**      | 0428h                        | 0429h   | 042Ah   | 042Bh   | 042Ch   | 042Dh   | 042Eh   | 042Fh   |
| **0430h**      | 0410h                        | 0411h   | 0412h   | 0413h   | 0414h   | 0415h   | 0416h   | 0417h   |
| **0438h**      | 0418h                        | 0419h   | 041Ah   | 041Bh   | 041Ch   | 041Dh   | 041Eh   | 041Fh   |
| **0440h**      | 0420h                        | 0421h   | 0422h   | 0423h   | 0424h   | 0425h   | 0426h   | 0427h   |
| **0448h**      | 0428h                        | 0429h   | 042Ah   | 042Bh   | 042Ch   | 042Dh   | 042Eh   | 042Fh   |
| **0450h**      | 0400h                        | 0401h   | 0402h   | 0403h   | 0404h   | 0405h   | 0406h   | 0407h   |
| **0458h**      | 0408h                        | 0409h   | 040Ah   | 040Bh   | 040Ch   | 040Dh   | 040Eh   | 040Fh   |
| **0460h**      | 0460h                        | 0460h   | 0462h   | 0462h   | 0464h   | 0464h   | 0466h   | 0466h   |
| **0468h**      | 0468h                        | 0468h   | 046Ah   | 046Ah   | 046Ch   | 046Ch   | 046Eh   | 046Eh   |
| **0470h**      | 0470h                        | 0470h   | 0472h   | 0472h   | 0474h   | 0474h   | 0476h   | 0476h   |
| **0478h**      | 0478h                        | 0478h   | 047Ah   | 047Ah   | 047Ch   | 047Ch   | 047Eh   | 047Eh   |
| **0480h**      | 0480h                        | 0480h   | 0482h   | 0483h   | 0484h   | 0485h   | 0486h   | 0487h   |
| **0488h**      | 0488h                        | 0489h   | 048Ah   | 048Ah   | 048Ch   | 048Ch   | 048Eh   | 048Eh   |
| **0490h**      | 0490h                        | 0490h   | 0492h   | 0492h   | 0494h   | 0494h   | 0496h   | 0496h   |
| **0498h**      | 0498h                        | 0498h   | 049Ah   | 049Ah   | 049Ch   | 049Ch   | 049Eh   | 049Eh   |
| **04A0h**      | 04A0h                        | 04A0h   | 04A2h   | 04A2h   | 04A4h   | 04A4h   | 04A6h   | 04A6h   |
| **04A8h**      | 04A8h                        | 04A8h   | 04AAh   | 04AAh   | 04ACh   | 04ACh   | 04AEh   | 04AEh   |
| **04B0h**      | 04B0h                        | 04B0h   | 04B2h   | 04B2h   | 04B4h   | 04B4h   | 04B6h   | 04B6h   |
| **04B8h**      | 04B8h                        | 04B8h   | 04BAh   | 04BAh   | 04BCh   | 04BCh   | 04BEh   | 04BEh   |
| **04C0h**      | 04C0h                        | 04C1h   | 04C1h   | 04C3h   | 04C3h   | 04C5h   | 04C5h   | 04C7h   |
| **04C8h**      | 04C7h                        | 04C9h   | 04C9h   | 04CBh   | 04CBh   | 04CDh   | 04CDh   | 04C0h   |
| **04D0h**      | 04D0h                        | 04D0h   | 04D2h   | 04D2h   | 04D4h   | 04D4h   | 04D6h   | 04D6h   |
| **04D8h**      | 04D8h                        | 04D8h   | 04DAh   | 04DAh   | 04DCh   | 04DCh   | 04DEh   | 04DEh   |
| **04E0h**      | 04E0h                        | 04E0h   | 04E2h   | 04E2h   | 04E4h   | 04E4h   | 04E6h   | 04E6h   |
| **04E8h**      | 04E8h                        | 04E8h   | 04EAh   | 04EAh   | 04ECh   | 04ECh   | 04EEh   | 04EEh   |
| **04F0h**      | 04F0h                        | 04F0h   | 04F2h   | 04F2h   | 04F4h   | 04F4h   | 04F6h   | 04F6h   |
| **04F8h**      | 04F8h                        | 04F8h   | 04FAh   | 04FAh   | 04FCh   | 04FCh   | 04FEh   | 04FEh   |
| **0500h**      | 0500h                        | 0500h   | 0502h   | 0502h   | 0504h   | 0504h   | 0506h   | 0506h   |
| **0508h**      | 0508h                        | 0508h   | 050Ah   | 050Ah   | 050Ch   | 050Ch   | 050Eh   | 050Eh   |
| **0510h**      | 0510h                        | 0510h   | 0512h   | 0512h   | 0514h   | 0515h   | 0516h   | 0517h   |
| **0518h**      | 0518h                        | 0519h   | 051Ah   | 051Bh   | 051Ch   | 051Dh   | 051Eh   | 051Fh   |
| **0520h**      | 0520h                        | 0521h   | 0522h   | 0523h   | 0524h   | 0525h   | 0526h   | 0527h   |
| **0528h**      | 0528h                        | 0529h   | 052Ah   | 052Bh   | 052Ch   | 052Dh   | 052Eh   | 052Fh   |
| **0530h**      | 0530h                        | 0531h   | 0532h   | 0533h   | 0534h   | 0535h   | 0536h   | 0537h   |
| **0538h**      | 0538h                        | 0539h   | 053Ah   | 053Bh   | 053Ch   | 053Dh   | 053Eh   | 053Fh   |
| **0540h**      | 0540h                        | 0541h   | 0542h   | 0543h   | 0544h   | 0545h   | 0546h   | 0547h   |
| **0548h**      | 0548h                        | 0549h   | 054Ah   | 054Bh   | 054Ch   | 054Dh   | 054Eh   | 054Fh   |
| **0550h**      | 0550h                        | 0551h   | 0552h   | 0553h   | 0554h   | 0555h   | 0556h   | 0557h   |
| **0558h**      | 0558h                        | 0559h   | 055Ah   | 055Bh   | 055Ch   | 055Dh   | 055Eh   | 055Fh   |
| **0560h**      | 0560h                        | 0531h   | 0532h   | 0533h   | 0534h   | 0535h   | 0536h   | 0537h   |
| **0568h**      | 0538h                        | 0539h   | 053Ah   | 053Bh   | 053Ch   | 053Dh   | 053Eh   | 053Fh   |
| **0570h**      | 0540h                        | 0541h   | 0542h   | 0543h   | 0544h   | 0545h   | 0546h   | 0547h   |
| **0578h**      | 0548h                        | 0549h   | 054Ah   | 054Bh   | 054Ch   | 054Dh   | 054Eh   | 054Fh   |
| **0580h**      | 0550h                        | 0551h   | 0552h   | 0553h   | 0554h   | 0555h   | 0556h   | FFFFh   |
| **0588h**      | 17F6h                        | 2C63h   | 1D7Eh   | 1D7Fh   | 1D80h   | 1D81h   | 1D82h   | 1D83h   |
| **0590h**      | 1D84h                        | 1D85h   | 1D86h   | 1D87h   | 1D88h   | 1D89h   | 1D8Ah   | 1D8Bh   |
| **0598h**      | 1D8Ch                        | 1D8Dh   | 1D8Eh   | 1D8Fh   | 1D90h   | 1D91h   | 1D92h   | 1D93h   |
| **05A0h**      | 1D94h                        | 1D95h   | 1D96h   | 1D97h   | 1D98h   | 1D99h   | 1D9Ah   | 1D9Bh   |
| **05A8h**      | 1D9Ch                        | 1D9Dh   | 1D9Eh   | 1D9Fh   | 1DA0h   | 1DA1h   | 1DA2h   | 1DA3h   |
| **05B0h**      | 1DA4h                        | 1DA5h   | 1DA6h   | 1DA7h   | 1DA8h   | 1DA9h   | 1DAAh   | 1DABh   |
| **05B8h**      | 1DACh                        | 1DADh   | 1DAEh   | 1DAFh   | 1DB0h   | 1DB1h   | 1DB2h   | 1DB3h   |
| **05C0h**      | 1DB4h                        | 1DB5h   | 1DB6h   | 1DB7h   | 1DB8h   | 1DB9h   | 1DBAh   | 1DBBh   |
| **05C8h**      | 1DBCh                        | 1DBDh   | 1DBEh   | 1DBFh   | 1DC0h   | 1DC1h   | 1DC2h   | 1DC3h   |
| **05D0h**      | 1DC4h                        | 1DC5h   | 1DC6h   | 1DC7h   | 1DC8h   | 1DC9h   | 1DCAh   | 1DCBh   |
| **05D8h**      | 1DCCh                        | 1DCDh   | 1DCEh   | 1DCFh   | 1DD0h   | 1DD1h   | 1DD2h   | 1DD3h   |
| **05E0h**      | 1DD4h                        | 1DD5h   | 1DD6h   | 1DD7h   | 1DD8h   | 1DD9h   | 1DDAh   | 1DDBh   |
| **05E8h**      | 1DDCh                        | 1DDDh   | 1DDEh   | 1DDFh   | 1DE0h   | 1DE1h   | 1DE2h   | 1DE3h   |
| **05F0h**      | 1DE4h                        | 1DE5h   | 1DE6h   | 1DE7h   | 1DE8h   | 1DE9h   | 1DEAh   | 1DEBh   |
| **05F8h**      | 1DECh                        | 1DEDh   | 1DEEh   | 1DEFh   | 1DF0h   | 1DF1h   | 1DF2h   | 1DF3h   |
| **0600h**      | 1DF4h                        | 1DF5h   | 1DF6h   | 1DF7h   | 1DF8h   | 1DF9h   | 1DFAh   | 1DFBh   |
| **0608h**      | 1DFCh                        | 1DFDh   | 1DFEh   | 1DFFH   | 1E00h   | 1E00h   | 1E02h   | 1E02h   |
| **0610h**      | 1E04h                        | 1E04h   | 1E06h   | 1E06h   | 1E08h   | 1E08h   | 1E0Ah   | 1E0Ah   |
| **0618h**      | 1E0Ch                        | 1E0Ch   | 1E0Eh   | 1E0Eh   | 1E10h   | 1E10h   | 1E12h   | 1E12h   |
| **0620h**      | 1E14h                        | 1E14h   | 1E16h   | 1E16h   | 1E18h   | 1E18h   | 1E1Ah   | 1E1Ah   |
| **0628h**      | 1E1Ch                        | 1E1Ch   | 1E1Eh   | 1E1Eh   | 1E20h   | 1E20h   | 1E22h   | 1E22h   |
| **0630h**      | 1E24h                        | 1E24h   | 1E26h   | 1E26h   | 1E28h   | 1E28h   | 1E2Ah   | 1E2Ah   |
| **0638h**      | 1E2Ch                        | 1E2Ch   | 1E2Eh   | 1E2Eh   | 1E30h   | 1E30h   | 1E32h   | 1E32h   |
| **0640h**      | 1E34h                        | 1E34h   | 1E36h   | 1E36h   | 1E38h   | 1E38h   | 1E3Ah   | 1E3Ah   |
| **0648h**      | 1E3Ch                        | 1E3Ch   | 1E3Eh   | 1E3Eh   | 1E40h   | 1E40h   | 1E42h   | 1E42h   |
| **0650h**      | 1E44h                        | 1E44h   | 1E46h   | 1E46h   | 1E48h   | 1E48h   | 1E4Ah   | 1E4Ah   |
| **0658h**      | 1E4Ch                        | 1E4Ch   | 1E4Eh   | 1E4Eh   | 1E50h   | 1E50h   | 1E52h   | 1E52h   |
| **0660h**      | 1E54h                        | 1E54h   | 1E56h   | 1E56h   | 1E58h   | 1E58h   | 1E5Ah   | 1E5Ah   |
| **0668h**      | 1E5Ch                        | 1E5Ch   | 1E5Eh   | 1E5Eh   | 1E60h   | 1E60h   | 1E62h   | 1E62h   |
| **0670h**      | 1E64h                        | 1E64h   | 1E66h   | 1E66h   | 1E68h   | 1E68h   | 1E6Ah   | 1E6Ah   |
| **0678h**      | 1E6Ch                        | 1E6Ch   | 1E6Eh   | 1E6Eh   | 1E70h   | 1E70h   | 1E72h   | 1E72h   |
| **0680h**      | 1E74h                        | 1E74h   | 1E76h   | 1E76h   | 1E78h   | 1E78h   | 1E7Ah   | 1E7Ah   |
| **0688h**      | 1E7Ch                        | 1E7Ch   | 1E7Eh   | 1E7Eh   | 1E80h   | 1E80h   | 1E82h   | 1E82h   |
| **0690h**      | 1E84h                        | 1E84h   | 1E86h   | 1E86h   | 1E88h   | 1E88h   | 1E8Ah   | 1E8Ah   |
| **0698h**      | 1E8Ch                        | 1E8Ch   | 1E8Eh   | 1E8Eh   | 1E90h   | 1E90h   | 1E92h   | 1E92h   |
| **06A0h**      | 1E94h                        | 1E94h   | 1E96h   | 1E97h   | 1E98h   | 1E99h   | 1E9Ah   | 1E9Bh   |
| **06A8h**      | 1E9Ch                        | 1E9Dh   | 1E9Eh   | 1E9Fh   | 1EA0h   | 1EA0h   | 1EA2h   | 1EA2h   |
| **06B0h**      | 1EA4h                        | 1EA4h   | 1EA6h   | 1EA6h   | 1EA8h   | 1EA8h   | 1EAAh   | 1EAAh   |
| **06B8h**      | 1EACh                        | 1EACh   | 1EAEh   | 1EAEh   | 1EB0h   | 1EB0h   | 1EB2h   | 1EB2h   |
| **06C0h**      | 1EB4h                        | 1EB4h   | 1EB6h   | 1EB6h   | 1EB8h   | 1EB8h   | 1EBAh   | 1EBAh   |
| **06C8h**      | 1EBCh                        | 1EBCh   | 1EBEh   | 1EBEh   | 1EC0h   | 1EC0h   | 1EC2h   | 1EC2h   |
| **06D0h**      | 1EC4h                        | 1EC4h   | 1EC6h   | 1EC6h   | 1EC8h   | 1EC8h   | 1ECAh   | 1ECAh   |
| **06D8h**      | 1ECCh                        | 1ECCh   | 1ECEh   | 1ECEh   | 1ED0h   | 1ED0h   | 1ED2h   | 1ED2h   |
| **06E0h**      | 1ED4h                        | 1ED4h   | 1ED6h   | 1ED6h   | 1ED8h   | 1ED8h   | 1EDAh   | 1EDAh   |
| **06E8h**      | 1EDCh                        | 1EDCh   | 1EDEh   | 1EDEh   | 1EE0h   | 1EE0h   | 1EE2h   | 1EE2h   |
| **06F0h**      | 1EE4h                        | 1EE4h   | 1EE6h   | 1EE6h   | 1EE8h   | 1EE8h   | 1EEAh   | 1EEAh   |
| **06F8h**      | 1EECh                        | 1EECh   | 1EEEh   | 1EEEh   | 1EF0h   | 1EF0h   | 1EF2h   | 1EF2h   |
| **0700h**      | 1EF4h                        | 1EF4h   | 1EF6h   | 1EF6h   | 1EF8h   | 1EF8h   | 1EFAh   | 1EFBh   |
| **0708h**      | 1EFCh                        | 1EFDh   | 1EFEh   | 1EFFh   | 1F08h   | 1F09h   | 1F0Ah   | 1F0Bh   |
| **0710h**      | 1F0Ch                        | 1F0Dh   | 1F0Eh   | 1F0Fh   | 1F08h   | 1F09h   | 1F0Ah   | 1F0Bh   |
| **0718h**      | 1F0Ch                        | 1F0Dh   | 1F0Eh   | 1F0Fh   | 1F18h   | 1F19h   | 1F1Ah   | 1F1Bh   |
| **0720h**      | 1F1Ch                        | 1F1Dh   | 1F16h   | 1F17h   | 1F18h   | 1F19h   | 1F1Ah   | 1F1Bh   |
| **0728h**      | 1F1Ch                        | 1F1Dh   | 1F1Eh   | 1F1Fh   | 1F28h   | 1F29h   | 1F2Ah   | 1F2Bh   |
| **0730h**      | 1F2Ch                        | 1F2Dh   | 1F2Eh   | 1F2Fh   | 1F28h   | 1F29h   | 1F2Ah   | 1F2Bh   |
| **0738h**      | 1F2Ch                        | 1F2Dh   | 1F2Eh   | 1F2Fh   | 1F38h   | 1F39h   | 1F3Ah   | 1F3Bh   |
| **0740h**      | 1F3Ch                        | 1F3Dh   | 1F3Eh   | 1F3Fh   | 1F38h   | 1F39h   | 1F3Ah   | 1F3Bh   |
| **0748h**      | 1F3Ch                        | 1F3Dh   | 1F3Eh   | 1F3Fh   | 1F48h   | 1F49h   | 1F4Ah   | 1F4Bh   |
| **0750h**      | 1F4Ch                        | 1F4Dh   | 1F46h   | 1F47h   | 1F48h   | 1F49h   | 1F4Ah   | 1F4Bh   |
| **0758h**      | 1F4Ch                        | 1F4Dh   | 1F4Eh   | 1F4Fh   | 1F50h   | 1F59h   | 1F52h   | 1F5Bh   |
| **0760h**      | 1F54h                        | 1F5Dh   | 1F56h   | 1F5Fh   | 1F58h   | 1F59h   | 1F5Ah   | 1F5Bh   |
| **0768h**      | 1F5Ch                        | 1F5Dh   | 1F5Eh   | 1F5Fh   | 1F68h   | 1F69h   | 1F6Ah   | 1F6Bh   |
| **0770h**      | 1F6Ch                        | 1F6Dh   | 1F6Eh   | 1F6Fh   | 1F68h   | 1F69h   | 1F6Ah   | 1F6Bh   |
| **0778h**      | 1F6Ch                        | 1F6Dh   | 1F6Eh   | 1F6Fh   | 1FBAh   | 1FBBh   | 1FC8h   | 1FC9h   |
| **0780h**      | 1FCAh                        | 1FCBh   | 1FDAh   | 1FDBh   | 1FF8h   | 1FF9h   | 1FEAh   | 1FEBh   |
| **0788h**      | 1FFAh                        | 1FFBh   | 1F7Eh   | 1F7Fh   | 1F88h   | 1F89h   | 1F8Ah   | 1F8Bh   |
| **0790h**      | 1F8Ch                        | 1F8Dh   | 1F8Eh   | 1F8Fh   | 1F88h   | 1F89h   | 1F8Ah   | 1F8Bh   |
| **0798h**      | 1F8Ch                        | 1F8Dh   | 1F8Eh   | 1F8Fh   | 1F98h   | 1F99h   | 1F9Ah   | 1F9Bh   |
| **07A0h**      | 1F9Ch                        | 1F9Dh   | 1F9Eh   | 1F9Fh   | 1F98h   | 1F99h   | 1F9Ah   | 1F9Bh   |
| **07A8h**      | 1F9Ch                        | 1F9Dh   | 1F9Eh   | 1F9Fh   | 1FA8h   | 1FA9h   | 1FAAh   | 1FABh   |
| **07B0h**      | 1FACh                        | 1FADh   | 1FAEh   | 1FAFh   | 1FA8h   | 1FA9h   | 1FAAh   | 1FABh   |
| **07B8h**      | 1FACh                        | 1FADh   | 1FAEh   | 1FAFh   | 1FB8h   | 1FB9h   | 1FB2h   | 1FBCh   |
| **07C0h**      | 1FB4h                        | 1FB5h   | 1FB6h   | 1FB7h   | 1FB8h   | 1FB9h   | 1FBAh   | 1FBBh   |
| **07C8h**      | 1FBCh                        | 1FBDh   | 1FBEh   | 1FBFh   | 1FC0h   | 1FC1h   | 1FC2h   | 1FC3h   |
| **07D0h**      | 1FC4h                        | 1FC5h   | 1FC6h   | 1FC7h   | 1FC8h   | 1FC9h   | 1FCAh   | 1FCBh   |
| **07D8h**      | 1FC3h                        | 1FCDh   | 1FCEh   | 1FCFh   | 1FD8h   | 1FD9h   | 1FD2h   | 1FD3h   |
| **07E0h**      | 1FD4h                        | 1FD5h   | 1FD6h   | 1FD7h   | 1FD8h   | 1FD9h   | 1FDAh   | 1FDBh   |
| **07E8h**      | 1FDCh                        | 1FDDh   | 1FDEh   | 1FDFh   | 1FE8h   | 1FE9h   | 1FE2h   | 1FE3h   |
| **07F0h**      | 1FE4h                        | 1FECh   | 1FE6h   | 1FE7h   | 1FE8h   | 1FE9h   | 1FEAh   | 1FEBh   |
| **07F8h**      | 1FECh                        | 1FEDh   | 1FEEh   | 1FEFh   | 1FF0h   | 1FF1h   | 1FF2h   | 1FF3h   |
| **0800h**      | 1FF4h                        | 1FF5h   | 1FF6h   | 1FF7h   | 1FF8h   | 1FF9h   | 1FFAh   | 1FFBh   |
| **0808h**      | 1FF3h                        | 1FFDh   | 1FFEh   | 1FFFh   | 2000h   | 2001h   | 2002h   | 2003h   |
| **0810h**      | 2004h                        | 2005h   | 2006h   | 2007h   | 2008h   | 2009h   | 200Ah   | 200Bh   |
| **0818h**      | 200Ch                        | 200Dh   | 200Eh   | 200Fh   | 2010h   | 2011h   | 2012h   | 2013h   |
| **0820h**      | 2014h                        | 2015h   | 2016h   | 2017h   | 2018h   | 2019h   | 201Ah   | 201Bh   |
| **0828h**      | 201Ch                        | 201Dh   | 201Eh   | 201Fh   | 2020h   | 2021h   | 2022h   | 2023h   |
| **0830h**      | 2024h                        | 2025h   | 2026h   | 2027h   | 2028h   | 2029h   | 202Ah   | 202Bh   |
| **0838h**      | 202Ch                        | 202Dh   | 202Eh   | 202Fh   | 2030h   | 2031h   | 2032h   | 2033h   |
| **0840h**      | 2034h                        | 2035h   | 2036h   | 2037h   | 2038h   | 2039h   | 203Ah   | 203Bh   |
| **0848h**      | 203Ch                        | 203Dh   | 203Eh   | 203Fh   | 2040h   | 2041h   | 2042h   | 2043h   |
| **0850h**      | 2044h                        | 2045h   | 2046h   | 2047h   | 2048h   | 2049h   | 204Ah   | 204Bh   |
| **0858h**      | 204Ch                        | 204Dh   | 204Eh   | 204Fh   | 2050h   | 2051h   | 2052h   | 2053h   |
| **0860h**      | 2054h                        | 2055h   | 2056h   | 2057h   | 2058h   | 2059h   | 205Ah   | 205Bh   |
| **0868h**      | 205Ch                        | 205Dh   | 205Eh   | 205Fh   | 2060h   | 2061h   | 2062h   | 2063h   |
| **0870h**      | 2064h                        | 2065h   | 2066h   | 2067h   | 2068h   | 2069h   | 206Ah   | 206Bh   |
| **0878h**      | 206Ch                        | 206Dh   | 206Eh   | 206Fh   | 2070h   | 2071h   | 2072h   | 2073h   |
| **0880h**      | 2074h                        | 2075h   | 2076h   | 2077h   | 2078h   | 2079h   | 207Ah   | 207Bh   |
| **0888h**      | 207Ch                        | 207Dh   | 207Eh   | 207Fh   | 2080h   | 2081h   | 2082h   | 2083h   |
| **0890h**      | 2084h                        | 2085h   | 2086h   | 2087h   | 2088h   | 2089h   | 208Ah   | 208Bh   |
| **0898h**      | 208Ch                        | 208Dh   | 208Eh   | 208Fh   | 2090h   | 2091h   | 2092h   | 2093h   |
| **08A0h**      | 2094h                        | 2095h   | 2096h   | 2097h   | 2098h   | 2099h   | 209Ah   | 209Bh   |
| **08A8h**      | 209Ch                        | 209Dh   | 209Eh   | 209Fh   | 20A0h   | 20A1h   | 20A2h   | 20A3h   |
| **08B0h**      | 20A4h                        | 20A5h   | 20A6h   | 20A7h   | 20A8h   | 20A9h   | 20AAh   | 20ABh   |
| **08B8h**      | 20ACh                        | 20ADh   | 20AEh   | 20AFh   | 20B0h   | 20B1h   | 20B2h   | 20B3h   |
| **08C0h**      | 20B4h                        | 20B5h   | 20B6h   | 20B7h   | 20B8h   | 20B9h   | 20BAh   | 20BBh   |
| **08C8h**      | 20BCh                        | 20BDh   | 20BEh   | 20BFh   | 20C0h   | 20C1h   | 20C2h   | 20C3h   |
| **08D0h**      | 20C4h                        | 20C5h   | 20C6h   | 20C7h   | 20C8h   | 20C9h   | 20CAh   | 20CBh   |
| **08D8h**      | 20CCh                        | 20CDh   | 20CEh   | 20CFh   | 20D0h   | 20D1h   | 20D2h   | 20D3h   |
| **08E0h**      | 20D4h                        | 20D5h   | 20D6h   | 20D7h   | 20D8h   | 20D9h   | 20DAh   | 20DBh   |
| **08E8h**      | 20DCh                        | 20DDh   | 20DEh   | 20DFh   | 20E0h   | 20E1h   | 20E2h   | 20E3h   |
| **08F0h**      | 20E4h                        | 20E5h   | 20E6h   | 20E7h   | 20E8h   | 20E9h   | 20EAh   | 20EBh   |
| **08F8h**      | 20ECh                        | 20EDh   | 20EEh   | 20EFh   | 20F0h   | 20F1h   | 20F2h   | 20F3h   |
| **0900h**      | 20F4h                        | 20F5h   | 20F6h   | 20F7h   | 20F8h   | 20F9h   | 20FAh   | 20FBh   |
| **0908h**      | 20FCh                        | 20FDh   | 20FEh   | 20FFh   | 2100h   | 2101h   | 2102h   | 2103h   |
| **0910h**      | 2104 Stunden                        | 2105h   | 2106h   | 2107h   | 2108h   | 2109h   | 210Ah   | 210Bh   |
| **0918h**      | 210Ch                        | 210Dh   | 210Eh   | 210Fh   | 2110h   | 2111h   | 2112h   | 2113h   |
| **0920h**      | 2114h                        | 2115h   | 2116h   | 2117h   | 2118h   | 2119h   | 211Ah   | 211Bh   |
| **0928h**      | 211Ch                        | 211Dh   | 211Eh   | 211Fh   | 2120h   | 2121h   | 2122h   | 2123h   |
| **0930h**      | 2124h                        | 2125h   | 2126h   | 2127h   | 2128h   | 2129h   | 212Ah   | 212Bh   |
| **0938h**      | 212Ch                        | 212Dh   | 212Eh   | 212Fh   | 2130h   | 2131h   | 2132h   | 2133h   |
| **0940h**      | 2134h                        | 2135h   | 2136h   | 2137h   | 2138h   | 2139h   | 213Ah   | 213Bh   |
| **0948h**      | 213Ch                        | 213Dh   | 213Eh   | 213Fh   | 2140h   | 2141h   | 2142h   | 2143h   |
| **0950h**      | 2144h                        | 2145h   | 2146h   | 2147h   | 2148h   | 2149h   | 214Ah   | 214Bh   |
| **0958h**      | 214Ch                        | 214Dh   | 2132h   | 214Fh   | 2150h   | 2151h   | 2152h   | 2153h   |
| **0960h**      | 2154h                        | 2155h   | 2156h   | 2157h   | 2158h   | 2159h   | 215Ah   | 215Bh   |
| **0968h**      | 215Ch                        | 215Dh   | 215Eh   | 215Fh   | 2160h   | 2161h   | 2162h   | 2163h   |
| **0970h**      | 2164h                        | 2165h   | 2166h   | 2167h   | 2168h   | 2169h   | 216Ah   | 216Bh   |
| **0978h**      | 216Ch                        | 216Dh   | 216Eh   | 216Fh   | 2160h   | 2161h   | 2162h   | 2163h   |
| **0980h**      | 2164h                        | 2165h   | 2166h   | 2167h   | 2168h   | 2169h   | 216Ah   | 216Bh   |
| **0988h**      | 216Ch                        | 216Dh   | 216Eh   | 216Fh   | 2180h   | 2181h   | 2182h   | 2183h   |
| **0990h**      | 2183h                        | FFFFh   | 034Bh   | 24B6h   | 24B7h   | 24B8h   | 24B9h   | 24BAh   |
| **0998h**      | 24BBh                        | 24BCh   | 24BDh   | 24BEh   | 24BFh   | 24C0h   | 24C1h   | 24C2h   |
| **09A0h**      | 24C3h                        | 24C4h   | 24C5h   | 24C6h   | 24C7h   | 24C8h   | 24C9h   | 24CAh   |
| **09A8h**      | 24CBh                        | 24CCh   | 24CDh   | 24CEh   | 24CFh   | FFFFh   | 0746h   | 2C00h   |
| **09B0h**      | 2C01h                        | 2C02h   | 2C03h   | 2C04h   | 2C05h   | 2C06h   | 2C07h   | 2C08h   |
| **09B8h**      | 2C09h                        | 2C0Ah   | 2C0Bh   | 2C0Ch   | 2C0Dh   | 2C0Eh   | 2C0Fh   | 2C10h   |
| **09C0h**      | 2C11h                        | 2C12h   | 2C13h   | 2C14h   | 2C15h   | 2C16h   | 2C17h   | 2C18h   |
| **09C8h**      | 2C19h                        | 2C1Ah   | 2C1Bh   | 2C1Ch   | 2C1Dh   | 2C1Eh   | 2C1Fh   | 2C20h   |
| **09D0h**      | 2C21h                        | 2C22h   | 2C23h   | 2C24h   | 2C25h   | 2C26h   | 2C27h   | 2C28h   |
| **09D8h**      | 2C29h                        | 2C2Ah   | 2C2Bh   | 2C2Ch   | 2C2Dh   | 2C2Eh   | 2C5Fh   | 2C60h   |
| **09E0h**      | 2C60h                        | 2C62h   | 2C63h   | 2C64h   | 2C65h   | 2C66h   | 2C67h   | 2C67h   |
| **09E8h**      | 2C69h                        | 2C69h   | 2C6Bh   | 2C6Bh   | 2C6Dh   | 2C6Eh   | 2C6Fh   | 2C70h   |
| **09F0h**      | 2C71h                        | 2C72h   | 2C73h   | 2C74h   | 2C75h   | 2C75h   | 2C77h   | 2C78h   |
| **09F8h**      | 2C79h                        | 2C7Ah   | 2C7Bh   | 2C7Ch   | 2C7Dh   | 2C7Eh   | 2C7Fh   | 2C80h   |
| **0A00h**      | 2C80h                        | 2C82h   | 2C82h   | 2C84h   | 2C84h   | 2C86h   | 2C86h   | 2C88h   |
| **0A08h**      | 2C88h                        | 2C8Ah   | 2C8Ah   | 2C8Ch   | 2C8Ch   | 2C8Eh   | 2C8Eh   | 2C90h   |
| **0A10h**      | 2C90h                        | 2C92h   | 2C92h   | 2C94h   | 2C94h   | 2C96h   | 2C96h   | 2C98h   |
| **0A18h**      | 2C98h                        | 2C9Ah   | 2C9Ah   | 2C9Ch   | 2C9Ch   | 2C9Eh   | 2C9Eh   | 2CA0h   |
| **0A20h**      | 2CA0h                        | 2CA2h   | 2CA2h   | 2CA4h   | 2CA4h   | 2CA6h   | 2CA6h   | 2CA8h   |
| **0A28h**      | 2CA8h                        | 2CAAh   | 2CAAh   | 2CACh   | 2CACh   | 2CAEh   | 2CAEh   | 2CB0h   |
| **0A30h**      | 2CB0h                        | 2CB2h   | 2CB2h   | 2CB4h   | 2CB4h   | 2CB6h   | 2CB6h   | 2CB8h   |
| **0A38h**      | 2CB8h                        | 2CBAh   | 2CBAh   | 2CBCh   | 2CBCh   | 2CBEh   | 2CBEh   | 2CC0h   |
| **0A40h**      | 2CC0h                        | 2CC2h   | 2CC2h   | 2CC4h   | 2CC4h   | 2CC6h   | 2CC6h   | 2CC8h   |
| **0A48h**      | 2CC8h                        | 2CCAh   | 2CCAh   | 2CCCh   | 2CCCh   | 2CCEh   | 2CCEh   | 2CD0h   |
| **0A50h**      | 2CD0h                        | 2CD2h   | 2CD2h   | 2CD4h   | 2CD4h   | 2CD6h   | 2CD6h   | 2CD8h   |
| **0A58h**      | 2CD8h                        | 2CDAh   | 2CDAh   | 2CDCh   | 2CDCh   | 2CDEh   | 2CDEh   | 2CE0h   |
| **0A60h**      | 2CE0h                        | 2CE2h   | 2CE2h   | 2CE4h   | 2CE5h   | 2CE6h   | 2CE7h   | 2CE8h   |
| **0A68h**      | 2CE9h                        | 2CEAh   | 2CEBh   | 2CECh   | 2CEDh   | 2CEEh   | 2CEFh   | 2CF0h   |
| **0A70h**      | 2CF1h                        | 2CF2h   | 2CF3h   | 2CF4h   | 2CF5h   | 2CF6h   | 2CF7h   | 2CF8h   |
| **0A78h**      | 2CF9h                        | 2CFAh   | 2CFBh   | 2CFCh   | 2CFDh   | 2CFEh   | 2CFFh   | 10A0h   |
| **0A80h**      | 10A1h                        | 10A2h   | 10A3h   | 10A4h   | 10A5h   | 10A6h   | 10A7h   | 10A8h   |
| **0A88h**      | 10A9h                        | 10AAh   | 10ABh   | 10ACh   | 10ADh   | 10AEh   | 10AFh   | 10B0h   |
| **0A90h**      | 10B1h                        | 10B2h   | 10B3h   | 10B4h   | 10B5h   | 10B6h   | 10B7h   | 10B8h   |
| **0A98h**      | 10B9h                        | 10BAh   | 10BBh   | 10BCh   | 10BDh   | 10BEh   | 10BFh   | 10C0h   |
| **0AA0h**      | 10C1h                        | 10C2h   | 10C3h   | 10C4h   | 10C5h   | FFFFh   | D21Bh   | FF21h   |
| **0AA8h**      | FF22h                        | FF23h   | FF24h   | FF25h   | FF26h   | FF27h   | FF28h   | FF29h   |
| **0AB0h**      | FF2Ah                        | FF2Bh   | FF2Ch   | FF2Dh   | FF2Eh   | FF2Fh   | FF30h   | FF31h   |
| **0AB8h**      | FF32h                        | FF33h   | FF34h   | FF35h   | FF36h   | FF37h   | FF38h   | FF39h   |
| **0AC0h**      | FF3Ah                        | FF5Bh   | FF5Ch   | FF5Dh   | FF5Eh   | FF5Fh   | FF60h   | FF61h   |
| **0AC8h**      | FF62h                        | FF63h   | FF64h   | FF65h   | FF66h   | FF67h   | FF68h   | FF69h   |
| **0AD0h**      | FF6Ah                        | FF6Bh   | FF6Ch   | FF6Dh   | FF6Eh   | FF6Fh   | FF70h   | FF71h   |
| **0AD8h**      | FF72h                        | FF73h   | FF74h   | FF75h   | FF76h   | FF77h   | FF78h   | FF79h   |
| **0AE0h**      | FF7Ah                        | FF7Bh   | FF7Ch   | FF7Dh   | FF7Eh   | FF7Fh   | FF80h   | FF81h   |
| **0AE8h**      | FF82h                        | FF83h   | FF84h   | FF85h   | FF86h   | FF87h   | FF88h   | FF89h   |
| **0AF0h**      | FF8Ah                        | FF8Bh   | FF8Ch   | FF8Dh   | FF8Eh   | FF8Fh   | FF90h   | FF91h   |
| **0AF8h**      | FF92h                        | FF93h   | FF94h   | FF95h   | FF96h   | FF97h   | FF98h   | FF99h   |
| **0B00h**      | FF9Ah                        | FF9Bh   | FF9Ch   | FF9Dh   | FF9Eh   | FF9Fh   | FFA0h   | FFA1h   |
| **0B08h**      | FFA2h                        | FFA3h   | FFA4h   | FFA5h   | FFA6h   | FFA7h   | FFA8h   | FFA9h   |
| **0B10h**      | FFAAh                        | FFABh   | FFACh   | FFADh   | FFAEh   | FFAFh   | FFB0h   | FFB1h   |
| **0B18h**      | FFB2h                        | FFB3h   | FFB4h   | FFB5h   | FFB6h   | FFB7h   | FFB8h   | FFB9h   |
| **0B20h**      | FFBAh                        | FFBBh   | FFBCh   | FFBDh   | FFBEh   | FFBFh   | FFC0h   | FFC1h   |
| **0B28h**      | FFC2h                        | FFC3h   | FFC4h   | FFC5h   | FFC6h   | FFC7h   | FFC8h   | FFC9h   |
| **0B30h**      | FFCAh                        | FFCBh   | FFCCh   | FFCDh   | FFCEh   | FFCFh   | FFD0h   | FFD1h   |
| **0B38h**      | FFD2h                        | FFD3h   | FFD4h   | FFD5h   | FFD6h   | FFD7h   | FFD8h   | FFD9h   |
| **0B40h**      | FFDAh                        | FFDBh   | FFDCh   | FFDDh   | FFDEh   | FFDFh   | FFE0h   | FFE1h   |
| **0B48h**      | FFE2h                        | FFE3h   | FFE4h   | FFE5h   | FFE6h   | FFE7h   | FFE8h   | FFE9h   |
| **0B50h**      | FFEAh                        | FFEBh   | FFECh   | FFEDh   | FFEEh   | FFEFh   | FFF0h   | FFF1h   |
| **0B58h**      | FFF2h                        | FFF3h   | FFF4h   | FFF5h   | FFF6h   | FFF7h   | FFF8h   | FFF9h   |
| **0B60h**      | FFFAh                        | FFFBh   | FFFCh   | FFFDh   | FFFEh   | FFFFh   |         |         |

### <a name="73-volume-label-directory-entry"></a>7.3 VolumeBezeichnungsverzeichniseintrag

Die Volumebezeichnung ist eine Unicode-Zeichenfolge, mit der Endbenutzer ihre Speichervolumes unterscheiden können. Im exFAT-Dateisystem ist die Volumebezeichnung als kritischer primärer Verzeichniseintrag im Stammverzeichnis vorhanden (siehe [Tabelle 26).](#table-26-volume-label-directoryentry-structure) Die gültige Anzahl von Volume Label-Verzeichniseinträgen liegt zwischen 0 und 1.

<div id="table-26-volume-label-directoryentry-structure" />

**Tabelle 26 Volume label DirectoryEntry Structure**

<table>
<thead>
<tr class="header">
<th><strong>Feldname</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(Byte)</strong></p></th>
<th><p><strong>Größe</strong></p>
<p><strong>(Byte)</strong></p></th>
<th><strong>Kommentare</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EntryType</td>
<td>0</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#731-entrytype-field">Abschnitt 7.3.1</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>CharacterCount</td>
<td>1</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#732-charactercount-field">Abschnitt 7.3.2</a> definiert seinen Inhalt.</td>
</tr>
<tr class="odd">
<td>VolumeLabel</td>
<td>2</td>
<td>22</td>
<td>Dieses Feld ist obligatorisch, und <a href="#733-volumelabel-field">Abschnitt 7.3.3</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>Reserviert</td>
<td>24</td>
<td>8</td>
<td>Dieses Feld ist obligatorisch, und sein Inhalt ist reserviert.</td>
</tr>
</tbody>
</table>

#### <a name="731-entrytype-field"></a>7.3.1 EntryType-Feld

Das Feld EntryType muss der Definition entsprechen, die in der Vorlage Generic Primary DirectoryEntry (siehe [Abschnitt 6.3.1)](#631-entrytype-field)angegeben ist.

##### <a name="7311-typecode-field"></a>7.3.1.1 TypCodefeld

Das TypeCode-Feld muss der Definition entsprechen, die in der Generischen primären DirectoryEntry-Vorlage angegeben ist (siehe [Abschnitt 6.3.1.1](#6311-typecode-field)).

Für den Verzeichniseintrag Volume Label ist der gültige Wert für dieses Feld.
3.

##### <a name="7312-typeimportance-field"></a>7.3.1.2 TypeImportance Field

Das Feld TypeImportance muss der Definition entsprechen, die in der Vorlage Generic Primary DirectoryEntry (generisches primäres Verzeichnis) angegeben ist (siehe [Abschnitt 6.3.1.2).](#6312-typeimportance-field)

Für den Verzeichniseintrag Volume Label ist der gültige Wert für dieses Feld.
0.

##### <a name="7313-typecategory-field"></a>7.3.1.3 TypeCategory-Feld

Das Feld TypeCategory muss der Definition entsprechen, die in der Vorlage Generic Primary DirectoryEntry (siehe [Abschnitt 6.3.1.3)](#6313-typecategory-field)angegeben ist.

##### <a name="7314-inuse-field"></a>7.3.1.4 Feld "InUse"

Das Feld InUse muss der Definition entsprechen, die in der Vorlage Generic Primary DirectoryEntry (siehe [Abschnitt 6.3.1.4)](#6314-inuse-field)angegeben ist.

#### <a name="732-charactercount-field"></a>7.3.2 CharacterCount-Feld

Das Feld CharacterCount muss die Länge der Unicode-Zeichenfolge enthalten, die das VolumeLabel-Feld enthält.

Der gültige Wertebereich für dieses Feld muss:

- Mindestens 0, d.h. die Unicode-Zeichenfolge ist 0 Zeichen lang (entspricht keiner Volumebezeichnung).

- Höchstens 11, was bedeutet, dass die Unicode-Zeichenfolge 11 Zeichen lang ist

#### <a name="733-volumelabel-field"></a>7.3.3 VolumeLabel-Feld

Das Feld VolumeLabel muss eine Unicode-Zeichenfolge enthalten, bei der es sich um den benutzerfreundlichen Namen des Volumes handelt. Das VolumeLabel-Feld weist den gleichen Satz ungültiger Zeichen auf wie das FileName-Feld des Dateinamen-Verzeichniseintrags (siehe [Abschnitt 7.7.3).](#773-filename-field)

### <a name="74-file-directory-entry"></a>7.4 Dateiverzeichniseintrag

Dateiverzeichniseinträge beschreiben Dateien und Verzeichnisse. Dabei handelt es sich um wichtige primäre Verzeichniseinträge, und jedes Verzeichnis kann null oder mehr Dateiverzeichniseinträge enthalten (siehe [Tabelle 27).](#table-27-file-directoryentry) Damit ein Dateiverzeichniseintrag gültig ist, muss genau ein Eintrag für das Stream Extension-Verzeichnis und mindestens ein Dateinamen-Verzeichniseintrag unmittelbar auf den Eintrag Dateiverzeichnis folgen (siehe [Abschnitt 7.6](#76-stream-extension-directory-entry) bzw. [Abschnitt 7.7).](#77-file-name-directory-entry)

<div id="table-27-file-directoryentry" />

**Tabelle 27: DateiverzeichnisEntry**

<table>
<thead>
<tr class="header">
<th><strong>Feldname</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(Byte)</strong></p></th>
<th><p><strong>Größe</strong></p>
<p><strong>(Byte)</strong></p></th>
<th><strong>Kommentare</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EntryType</td>
<td>0</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#741-entrytype-field">Abschnitt 7.4.1</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>SecondaryCount</td>
<td>1</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#742-secondarycount-field">Abschnitt 7.4.2</a> definiert seinen Inhalt.</td>
</tr>
<tr class="odd">
<td>SetChecksum</td>
<td>2</td>
<td>2</td>
<td>Dieses Feld ist obligatorisch, und <a href="#743-setchecksum-field">Abschnitt 7.4.3</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>FileAttributes</td>
<td>4</td>
<td>2</td>
<td>Dieses Feld ist obligatorisch, und <a href="#744-fileattributes-field">Abschnitt 7.4.4</a> definiert seinen Inhalt.</td>
</tr>
<tr class="odd">
<td>Reserved1</td>
<td>6</td>
<td>2</td>
<td>Dieses Feld ist obligatorisch, und sein Inhalt ist reserviert.</td>
</tr>
<tr class="even">
<td>CreateTimestamp</td>
<td>8</td>
<td>4</td>
<td>Dieses Feld ist obligatorisch, und <a href="#745-createtimestamp-create10msincrement-and-createutcoffset-fields"> Abschnitt 7.4.5 </
a> definiert seinen Inhalt.</td>
</tr>
<tr class="odd">
<td>LastModifiedTimestamp</td>
<td>12</td>
<td>4</td>
<td>Dieses Feld ist obligatorisch, und <a href="#746-lastmodifiedtimestamp-lastmodified10msincrement-and-lastmodifiedutcoffset-fields">Abschnitt 7.4.6</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>LastAccessedTimestamp</td>
<td>16</td>
<td>4</td>
<td>Dieses Feld ist obligatorisch, und <a href="#747-lastaccessedtimestamp-and-lastaccessedutcoffset-fields">Abschnitt 7.4.7</a> definiert seinen Inhalt.</td>
</tr>
<tr class="odd">
<td>Create10msIncrement</td>
<td>20</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#745-createtimestamp-create10msincrement-and-createutcoffset-fields"> Abschnitt 7.4.5 </
a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>LastModified10msIncrement</td>
<td>21</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#746-lastmodifiedtimestamp-lastmodified10msincrement-and-lastmodifiedutcoffset-fields">Abschnitt 7.4.6</a> definiert seinen Inhalt.</td>
</tr>
<tr class="odd">
<td>CreateUtcOffset</td>
<td>22</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#745-createtimestamp-create10msincrement-and-createutcoffset-fields"> Abschnitt 7.4.5 </
a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>LastModifiedUtcOffset</td>
<td>23</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#746-lastmodifiedtimestamp-lastmodified10msincrement-and-lastmodifiedutcoffset-fields">in Abschnitt 7.4.6 wird</a> der Inhalt definiert.</td>
</tr>
<tr class="odd">
<td>LastAccessedUtcOffset</td>
<td>24</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#747-lastaccessedtimestamp-and-lastaccessedutcoffset-fields">in Abschnitt 7.4.7 wird</a> der Inhalt definiert.</td>
</tr>
<tr class="even">
<td>Reserved2</td>
<td>25</td>
<td>7</td>
<td>Dieses Feld ist obligatorisch, und sein Inhalt ist reserviert.</td>
</tr>
</tbody>
</table>

#### <a name="741-entrytype-field"></a>7.4.1 EntryType-Feld

Das Feld EntryType muss der Definition entsprechen, die in der Vorlage Generic Primary DirectoryEntry (Generisches primäres Verzeichnis) angegeben ist (siehe [Abschnitt 6.3.1](#631-entrytype-field)).

##### <a name="7411-typecode-field"></a>7.4.1.1 TypeCode-Feld

Das Feld TypeCode muss der Definition entsprechen, die in der Vorlage Generic Primary DirectoryEntry (Generisches primäres Verzeichnis) angegeben ist (siehe [Abschnitt 6.3.1.1](#6311-typecode-field)).

Für einen Dateiverzeichniseintrag ist der gültige Wert für dieses Feld 5.

##### <a name="7412-typeimportance-field"></a>7.4.1.2 TypeImportance-Feld

Das Feld TypeImportance muss der Definition entsprechen, die in der Vorlage Generic Primary DirectoryEntry (Generisches primäres Verzeichnis) angegeben ist (siehe [Abschnitt 6.3.1.2](#6312-typeimportance-field)).

Für einen Dateiverzeichniseintrag ist der gültige Wert für dieses Feld 0.

##### <a name="7413-typecategory-field"></a>7.4.1.3 TypeCategory-Feld

Das Feld TypeCategory muss der Definition entsprechen, die in der Vorlage Generic Primary DirectoryEntry (Generisches primäres Verzeichnis) angegeben ist (siehe [Abschnitt 6.3.1.3](#6313-typecategory-field)).

##### <a name="7414-inuse-field"></a>7.4.1.4 InUse-Feld

Das Feld InUse muss der Definition entsprechen, die in der Vorlage Generic Primary DirectoryEntry (Generisches primäres Verzeichnis) angegeben ist (siehe [Abschnitt 6.3.1.4](#6314-inuse-field)).

#### <a name="742-secondarycount-field"></a>7.4.2 SecondaryCount-Feld

Das Feld SecondaryCount muss der Definition entsprechen, die in der Vorlage Generic Primary DirectoryEntry (Generisches primäres Verzeichnis) angegeben ist (siehe [Abschnitt 6.3.2](#632-secondarycount-field)).

#### <a name="743-setchecksum-field"></a>7.4.3 SetChecksum-Feld

Das Feld SetChecksum muss der Definition entsprechen, die in der Vorlage Generic Primary DirectoryEntry (Generisches primäres Verzeichnis) angegeben ist (siehe [Abschnitt 6.3.3](#633-setchecksum-field)).

#### <a name="744-fileattributes-field"></a>7.4.4 FileAttributes-Feld

Das Feld FileAttributes enthält Flags (siehe [Tabelle 28](#table-28-fileattributes-field-structure)).

<div id="table-28-fileattributes-field-structure" />

**FileAttributes-Feldstruktur in Tabelle 28**

<table>
<thead>
<tr class="header">
<th><strong>Feldname</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(bit)</strong></p></th>
<th><p><strong>Größe</strong></p>
<p><strong>(Bits)</strong></p></th>
<th><strong>Kommentare</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ReadOnly</td>
<td>0</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch und entspricht der MS-DOS-Definition.</td>
</tr>
<tr class="even">
<td>Ausgeblendet</td>
<td>1</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch und entspricht der MS-DOS-Definition.</td>
</tr>
<tr class="odd">
<td>System</td>
<td>2</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch und entspricht der MS-DOS-Definition.</td>
</tr>
<tr class="even">
<td>Reserved1</td>
<td>3</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und sein Inhalt ist reserviert.</td>
</tr>
<tr class="odd">
<td>Verzeichnis</td>
<td>4</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch und entspricht der MS-DOS-Definition.</td>
</tr>
<tr class="even">
<td>Archive (Archiv)</td>
<td>5</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch und entspricht der MS-DOS-Definition.</td>
</tr>
<tr class="odd">
<td>Reserved2</td>
<td>6</td>
<td>10</td>
<td>Dieses Feld ist obligatorisch, und sein Inhalt ist reserviert.</td>
</tr>
</tbody>
</table>

#### <a name="745-createtimestamp-create10msincrement-and-createutcoffset-fields"></a>7.4.5 CreateTimestamp, Create10msIncrement und CreateUtcOffset Fields

In Kombination müssen die Felder CreateTimestamp und CreateTime10msIncrement das lokale Datum und die Uhrzeit der Erstellung der angegebenen Datei bzw. des angegebenen Verzeichnisses beschreiben. Das Feld CreateUtcOffset beschreibt den Offset des lokalen Datums und der Uhrzeit von UTC. Implementierungen müssen diese Felder bei der Erstellung des angegebenen Verzeichniseintragssets festlegen.

Diese Felder müssen den Definitionen der Felder Timestamp, 10msIncrement und UtcOffset entsprechen (siehe [Abschnitt 7.4.8,](#748-timestamp-fields) [Abschnitt 7.4.9](#749-10msincrement-fields)und [Abschnitt 7.4.10).](#7410-utcoffset-fields)

#### <a name="746-lastmodifiedtimestamp-lastmodified10msincrement-and-lastmodifiedutcoffset-fields"></a>7.4.6 LastModifiedTimestamp, LastModified10msIncrement und LastModifiedUtcOffset Fields

In Kombination müssen die Felder LastModifiedTimestamp und LastModifiedTime10msIncrement das lokale Datum und die Uhrzeit beschreiben, zu der der Inhalt eines der Cluster, die dem angegebenen Verzeichniseintrag der Stream-Erweiterung zugeordnet sind, zuletzt geändert wurde. Das Feld LastModifiedUtcOffset beschreibt den Offset des lokalen Datums und der Uhrzeit von UTC. Implementierungen müssen diese Felder aktualisieren:

1. Nach dem Ändern des Inhalts eines der Cluster, die dem angegebenen Verzeichniseintrag der Stream-Erweiterung zugeordnet sind (mit Ausnahme von Inhalten, die über den Punkt hinausgehen, den das Feld ValidDataLength beschreibt)

2. Beim Ändern der Werte der Felder ValidDataLength oder DataLength

Diese Felder müssen den Definitionen der Felder Timestamp, 10msIncrement und UtcOffset entsprechen (siehe [Abschnitt 7.4.8,](#748-timestamp-fields) [Abschnitt 7.4.9](#749-10msincrement-fields)und [Abschnitt 7.4.10).](#7410-utcoffset-fields)

#### <a name="747-lastaccessedtimestamp-and-lastaccessedutcoffset-fields"></a>7.4.7 LastAccessedTimestamp- und LastAccessedUtcOffset-Felder

Das Feld LastAccessedTimestamp muss das lokale Datum und die Uhrzeit des letzten Zugriffes auf den Inhalt eines der Cluster beschreiben, die dem angegebenen Verzeichniseintrag für die Streamerweiterung zugeordnet sind. Das Feld LastAccessedUtcOffset beschreibt den Offset des lokalen Datums und der Uhrzeit von UTC.
Implementierungen müssen diese Felder aktualisieren:

1. Nach dem Ändern des Inhalts eines der Cluster, die dem angegebenen Verzeichniseintrag der Stream-Erweiterung zugeordnet sind (mit Ausnahme von Inhalten, die außerhalb von ValidDataLength vorhanden sind)

2. Beim Ändern der Werte der Felder ValidDataLength oder DataLength

Implementierungen sollten diese Felder aktualisieren, nachdem sie den Inhalt eines der Cluster gelesen haben, die dem angegebenen Verzeichniseintrag für die Stream-Erweiterung zugeordnet sind.

Diese Felder müssen den Definitionen der Felder Timestamp und UtcOffset entsprechen (siehe [Abschnitt 7.4.8](#748-timestamp-fields) [bzw. Abschnitt 7.4.10).](#7410-utcoffset-fields)

#### <a name="748-timestamp-fields"></a>7.4.8 Zeitstempelfelder

Zeitstempelfelder beschreiben sowohl lokale Datums- als auch Uhrzeit bis zu einer Auflösung von zwei Sekunden (siehe [Tabelle 29](#table-29-timestamp-field-structure)).

<div id="table-29-timestamp-field-structure" />

**Tabelle 29: Zeitstempelfeldstruktur**

<table>
<thead>
<tr class="header">
<th><strong>Feldname</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(bit)</strong></p></th>
<th><p><strong>Größe</strong></p>
<p><strong>(Bits)</strong></p></th>
<th><strong>Kommentare</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>DoubleSeconds</td>
<td>0</td>
<td>5</td>
<td>Dieses Feld ist obligatorisch, und <a href="#7481-doubleseconds-field">in Abschnitt 7.4.8.1 wird</a> der Inhalt definiert.</td>
</tr>
<tr class="even">
<td>Minute</td>
<td>5</td>
<td>6</td>
<td>Dieses Feld ist obligatorisch, und <a href="#7482-minute-field">Abschnitt 7.4.8.2</a> definiert seinen Inhalt.</td>
</tr>
<tr class="odd">
<td>Stunde</td>
<td>11</td>
<td>5</td>
<td>Dieses Feld ist obligatorisch, und <a href="#7483-hour-field">Abschnitt 7.4.8.3</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>Tag</td>
<td>16</td>
<td>5</td>
<td>Dieses Feld ist obligatorisch, und <a href="#7484-day-field">Abschnitt 7.4.8.4</a> definiert seinen Inhalt.</td>
</tr>
<tr class="odd">
<td>Month</td>
<td>21</td>
<td>4</td>
<td>Dieses Feld ist obligatorisch, und <a href="#7485-month-field">Abschnitt 7.4.8.5</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>Year</td>
<td>25</td>
<td>7</td>
<td>Dieses Feld ist obligatorisch, und <a href="#7486-year-field">Abschnitt 7.4.8.6</a> definiert seinen Inhalt.</td>
</tr>
</tbody>
</table>

##### <a name="7481-doubleseconds-field"></a>7.4.8.1 DoubleSeconds-Feld

Das Feld DoubleSeconds muss den Sekundenteil des Timestamp-Felds in Zwei-Sekunden-Vielfachen beschreiben.

Der gültige Wertebereich für dieses Feld muss:

- 0, was 0 Sekunden darstellt

- 29, was 58 Sekunden darstellt

##### <a name="7482-minute-field"></a>7,4,8,2-Minuten-Feld

Das Feld Minute muss den Minutenbereich des Felds Zeitstempel beschreiben.

Der gültige Wertebereich für dieses Feld muss:

- 0, was 0 Minuten darstellt

- 59, was 59 Minuten entspricht

##### <a name="7483-hour-field"></a>7.4.8.3 Stundenfeld

Das Feld Stunde muss den Stundenteil des Felds Zeitstempel beschreiben.

Der gültige Wertebereich für dieses Feld muss:

- 0, was 00:00 Stunden darstellt

- 23, was 23:00 Stunden darstellt

##### <a name="7484-day-field"></a>7.4.8.4 Tagfeld

Das Feld Tag muss den Tagesteil des Felds Zeitstempel beschreiben.

Der gültige Wertebereich für dieses Feld muss:

- 1, der erste Tag des angegebenen Monats

- Der letzte Tag des angegebenen Monats (der angegebene Monat definiert die Anzahl gültiger Tage)

##### <a name="7485-month-field"></a>Feld "7.4.8.5 Monat"

Das Feld Monat muss den Monatsteil des Felds Zeitstempel beschreiben.

Der gültige Wertebereich für dieses Feld muss:

- Mindestens 1, das Den Januar darstellt

- Höchstens 12, was Dezember darstellt

##### <a name="7486-year-field"></a>Feld "7.4.8.6 Jahr"

Das Feld Jahr muss den Jahresteil des Felds Zeitstempel relativ zum Jahr 1980 beschreiben. Dieses Feld stellt das Jahr 1980 mit dem Wert 0 und das Jahr 2107 mit dem Wert 127 dar.

Alle möglichen Werte für dieses Feld sind gültig.

#### <a name="749-10msincrement-fields"></a>7.4.9 10msIncrement Fields

10msIncrement-Felder müssen eine zusätzliche Zeitauflösung für die entsprechenden Zeitstempelfelder in 10-Millisekunden-Vielfachen bereitstellen.

Der gültige Wertebereich für diese Felder muss folgendermaßen sein:

- Mindestens 0, was 0 Millisekunden darstellt

- Höchstens 199, was 1990 Millisekunden entspricht

#### <a name="7410-utcoffset-fields"></a>7.4.10 UtcOffset-Felder

UtcOffset-Felder (siehe [Tabelle 30)](#table-30-utcoffset-field-structure)müssen den Offset von UTC zum lokalen Datum und zur lokalen Uhrzeit beschreiben, die in den entsprechenden Zeitstempel- und 10 msIncrement-Feldern beschrieben werden. Der Offset von UTC zum lokalen Datum und zur lokalen Uhrzeit umfasst die Auswirkungen von Zeitzonen und anderen Datums-/Uhrzeitanpassungen, z. B. Sommerzeit und regionale Sommerzeitänderungen.

<div id="table-30-utcoffset-field-structure" />

**Tabellen-30 UtcOffset-Feldstruktur**

<table>
<thead>
<tr class="header">
<th><strong>Feldname</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(Bit)</strong></p></th>
<th><p><strong>Größe</strong></p>
<p><strong>(Bits)</strong></p></th>
<th><strong>Kommentare</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>OffsetFromUtc</td>
<td>0</td>
<td>7</td>
<td>Dieses Feld ist obligatorisch, und <a href="#74101-offsetfromutc-field">Abschnitt 7.4.10.1</a>definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>OffsetValid</td>
<td>7</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#74102-offsetvalid-field">Abschnitt 7.4.10.2</a> definiert seinen Inhalt.</td>
</tr>
</tbody>
</table>

##### <a name="74101-offsetfromutc-field"></a>7.4.10.1 OffsetFromUtc-Feld

Das Feld OffsetFromUtc muss den Offset von UTC des lokalen Datums und der Uhrzeit beschreiben, die die zugehörigen Felder Timestamp und 10msIncrement enthalten.
In diesem Feld wird der Offset von UTC in Intervallen von 15 Minuten beschrieben (siehe Tabelle 31).

<div id="table-31-meaning-of-the-values-of-the-offsetfromutc-field" />

**Tabelle 31 Bedeutung der Werte des OffsetFromUtc-Felds**

<table>
<thead>
<tr class="header">
<th><strong>Wert</strong></th>
<th><strong>Dezimale Entsprechung mit Vorzeichen</strong></th>
<th><strong>Beschreibung</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>3Fh</td>
<td>63</td>
<td>Ortsdatum und -uhrzeit ist UTC + 15:45</td>
</tr>
<tr class="even">
<td>3Eh</td>
<td>62</td>
<td>Ortsdatum und -uhrzeit ist UTC + 15:30</td>
</tr>
<tr class="odd">
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
</tr>
<tr class="even">
<td>01h</td>
<td>1</td>
<td>Lokales Datum und Lokale Uhrzeit ist UTC + 00:15</td>
</tr>
<tr class="odd">
<td>00h</td>
<td>0</td>
<td>Lokales Datum und Lokale Uhrzeit ist UTC</td>
</tr>
<tr class="even">
<td>7Fh</td>
<td>-1</td>
<td>Ortsdatum und -uhrzeit ist UTC – 00:15</td>
</tr>
<tr class="odd">
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
</tr>
<tr class="even">
<td>41h</td>
<td>-63</td>
<td>Ortsdatum und -uhrzeit ist UTC – 15:45</td>
</tr>
<tr class="odd">
<td>40h</td>
<td>-64</td>
<td>Ortsdatum und -uhrzeit ist UTC – 16:00 Uhr</td>
</tr>
</tbody>
</table>

Wie in der obigen Tabelle angegeben, sind alle möglichen Werte für dieses Feld gültig. Implementierungen sollten jedoch nur dann den Wert 00h für dieses Feld aufzeichnen, wenn:

1. Das lokale Datum und die lokale Uhrzeit sind tatsächlich identisch mit UTC. In diesem Fall muss der Wert des Felds OffsetValid 1 sein.

2. Lokale Datums- und Uhrzeitwerte sind nicht bekannt. In diesem Fall muss der Wert des Felds OffsetValid 1 sein, und implementierungen sollten UTC als lokales Datum und lokale Uhrzeit betrachten.

3. UTC ist nicht bekannt. In diesem Fall muss der Wert des Felds OffsetValid 0 sein.

Wenn der lokale Datums- und Uhrzeitoffset von UTC kein Vielfaches von 15-Minuten-Intervallen ist, müssen Implementierungen 00 Stunden im Feld OffsetFromUtc aufzeichnen und UTC als lokales Datum und lokale Uhrzeit betrachten.

##### <a name="74102-offsetvalid-field"></a>7.4.10.2 OffsetValid-Feld

Das Feld OffsetValid muss wie folgt beschreiben, ob der Inhalt des Felds OffsetFromUtc gültig ist:

- 0, was bedeutet, dass der Inhalt des Felds OffsetFromUtc ungültig ist.
    > und müssen 00h sein.

- 1, was bedeutet, dass der Inhalt des Felds OffsetFromUtc gültig ist.

Implementierungen sollten dieses Feld nur auf den Wert 0 festlegen, wenn UTC nicht für die Berechnung des Werts des Felds OffsetFromUtc verfügbar ist. Wenn dieses Feld den Wert 0 enthält, behandeln Implementierungen die Felder Timestamp und 10msIncrement so, als hätten sie den gleichen UTC-Offset wie das aktuelle lokale Datum und die aktuelle lokale Uhrzeit.

### <a name="75-volume-guid-directory-entry"></a>7.5 Volume-GUID-Verzeichniseintrag

Der Verzeichniseintrag Volume-GUID enthält eine GUID, mit der Implementierungen Volumes eindeutig und programmgesteuert unterscheiden können.
Die Volume-GUID ist als unbedenklicher primärer Verzeichniseintrag im Stammverzeichnis vorhanden (siehe [Tabelle 32](#table-32-volume-guid-directoryentry)). Die gültige Anzahl von Volume-GUID-Verzeichniseinträgen liegt zwischen 0 und 1.

<div id="table-32-volume-guid-directoryentry" />

**Table 32 Volume GUID DirectoryEntry**

<table>
<thead>
<tr class="header">
<th><strong>Feldname</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(Byte)</strong></p></th>
<th><p><strong>Größe</strong></p>
<p><strong>(Byte)</strong></p></th>
<th><strong>Kommentare</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EntryType</td>
<td>0</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#751-entrytype-field">in Abschnitt 7.5.1 wird</a> der Inhalt definiert.</td>
</tr>
<tr class="even">
<td>SecondaryCount</td>
<td>1</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, <a href="#752-secondarycount-field">und in Abschnitt 7.5.2 wird</a> der Inhalt definiert.</td>
</tr>
<tr class="odd">
<td>SetChecksum</td>
<td>2</td>
<td>2</td>
<td>Dieses Feld ist obligatorisch, und <a href="#753-setchecksum-field">in Abschnitt 7.5.3 wird</a> der Inhalt definiert.</td>
</tr>
<tr class="even">
<td>GeneralPrimaryFlags</td>
<td>4</td>
<td>2</td>
<td>Dieses Feld ist obligatorisch, und <a href="#754-generalprimaryflags-field">in Abschnitt 7.5.4 wird</a> der Inhalt definiert.</td>
</tr>
<tr class="odd">
<td>VolumeGuid</td>
<td>6</td>
<td>16</td>
<td>Dieses Feld ist obligatorisch, und <a href="#755-volumeguid-field">in Abschnitt 7.5.5 wird</a> der Inhalt definiert.</td>
</tr>
<tr class="even">
<td>Reserviert</td>
<td>22</td>
<td>10</td>
<td>Dieses Feld ist obligatorisch, und sein Inhalt ist reserviert.</td>
</tr>
</tbody>
</table>

#### <a name="751-entrytype-field"></a>7.5.1 EntryType-Feld

Das Feld EntryType muss der Definition entsprechen, die in der Vorlage Generic Primary DirectoryEntry (Generisches primäres Verzeichnis) angegeben ist (siehe [Abschnitt 6.3.1](#631-entrytype-field)).

##### <a name="7511-typecode-field"></a>7.5.1.1 TypeCode-Feld

Das Feld TypeCode muss der Definition entsprechen, die in der Vorlage Generic Primary DirectoryEntry (Generisches primäres Verzeichnis) angegeben ist (siehe [Abschnitt 6.3.1.1](#6311-typecode-field)).

Für den Verzeichniseintrag Volume-GUID ist der gültige Wert für dieses Feld.
0.

##### <a name="7512-typeimportance-field"></a>7.5.1.2 TypeImportance-Feld

Das Feld TypeImportance muss der Definition entsprechen, die in der Vorlage Generic Primary DirectoryEntry (Generisches primäres Verzeichnis) angegeben ist (siehe [Abschnitt 6.3.1.2](#6312-typeimportance-field)).

Für den Verzeichniseintrag Volume-GUID ist der gültige Wert für dieses Feld.
1.

##### <a name="7513-typecategory-field"></a>7.5.1.3 TypeCategory-Feld

Das Feld TypeCategory muss der Definition entsprechen, die in der Vorlage Generic Primary DirectoryEntry (Generisches primäres Verzeichnis) angegeben ist (siehe [Abschnitt 6.3.1.3](#6313-typecategory-field)).

##### <a name="7514-inuse-field"></a>7.5.1.4 InUse-Feld

Das Feld InUse muss der Definition entsprechen, die in der Vorlage Generic Primary DirectoryEntry (Generisches primäres Verzeichnis) angegeben ist (siehe [Abschnitt 6.3.1.4](#6314-inuse-field)).

#### <a name="752-secondarycount-field"></a>7.5.2 SecondaryCount-Feld

Das Feld SecondaryCount muss der Definition entsprechen, die in der Vorlage Generic Primary DirectoryEntry (Generisches primäres Verzeichnis) angegeben ist (siehe [Abschnitt 6.3.2](#632-secondarycount-field)).

Für den Verzeichniseintrag Volume-GUID ist der gültige Wert für dieses Feld.
0.

#### <a name="753-setchecksum-field"></a>7.5.3 SetChecksum-Feld

Das Feld SetChecksum muss der Definition entsprechen, die in der Vorlage Generic Primary DirectoryEntry (Generisches primäres Verzeichnis) angegeben ist (siehe [Abschnitt 6.3.3](#633-setchecksum-field)).

#### <a name="754-generalprimaryflags-field"></a>7.5.4 GeneralPrimaryFlags-Feld

Das Feld GeneralPrimaryFlags muss der Definition entsprechen, die in der Vorlage Generic Primary DirectoryEntry (siehe Abschnitt [6.3.4)](#634-generalprimaryflags-field)angegeben ist, und definiert den Inhalt des zu reservierten CustomDefined-Felds.

##### <a name="7541-allocationpossible-field"></a>7.5.4.1 ZuordnungPossible-Feld

Das Feld AllocationPossible muss der Definition entsprechen, die in der Vorlage Generic Primary DirectoryEntry (Generisches primäres Verzeichnis) angegeben ist (siehe [Abschnitt 6.3.4.1](#6341-allocationpossible-field)).

Für den Verzeichniseintrag Volume-GUID ist der gültige Wert für dieses Feld.
0.

##### <a name="7542-nofatchain-field"></a>7.5.4.2 NoFatChain-Feld

Das Feld NoFatChain muss der Definition entsprechen, die in der Vorlage Generic Primary DirectoryEntry (Generisches primäres Verzeichnis) angegeben ist (siehe [Abschnitt 6.3.4.2](#6342-nofatchain-field)).

#### <a name="755-volumeguid-field"></a>7.5.5 VolumeGuid-Feld

Das VolumeGuid-Feld muss eine GUID enthalten, die das gegebene Volume eindeutig identifiziert.

Alle möglichen Werte für dieses Feld sind gültig, mit Ausnahme der NULL-GUID, die {00000000-0000-0000-0000-000000000000} ist.

### <a name="76-stream-extension-directory-entry"></a>7.6 Verzeichniseintrag der Streamerweiterung

Der Verzeichniseintrag Streamerweiterung ist ein wichtiger sekundärer Verzeichniseintrag in Dateiverzeichniseintragssätzen (siehe [Tabelle 33](#table-33-stream-extension-directoryentry)). Die gültige Anzahl von Verzeichniseinträgen für die Streamerweiterung in einem Dateiverzeichniseintragssatz ist 1.
Darüber hinaus ist dieser Verzeichniseintrag nur gültig, wenn er unmittelbar auf den Dateiverzeichniseintrag folgt.

<div id="table-33-stream-extension-directoryentry" />

**Tabelle 33: Verzeichnis der StreamerweiterungEntry**

<table>
<thead>
<tr class="header">
<th><strong>Feldname</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(Byte)</strong></p></th>
<th><p><strong>Größe</strong></p>
<p><strong>(Byte)</strong></p></th>
<th><strong>Kommentare</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EntryType</td>
<td>0</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#761-entrytype-field">in Abschnitt 7.6.1 wird</a> der Inhalt definiert.</td>
</tr>
<tr class="even">
<td>GeneralSecondaryFlags</td>
<td>1</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#762-generalsecondaryflags-field">in Abschnitt 7.6.2 wird</a> der Inhalt definiert.</td>
</tr>
<tr class="odd">
<td>Reserved1</td>
<td>2</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und sein Inhalt ist reserviert.</td>
</tr>
<tr class="even">
<td>NameLength</td>
<td>3</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#763-namelength-field">in Abschnitt 7.6.3 wird</a> der Inhalt definiert.</td>
</tr>
<tr class="odd">
<td>NameHash</td>
<td>4</td>
<td>2</td>
<td>Dieses Feld ist obligatorisch, und <a href="#764-namehash-field">Abschnitt 7.6.4</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>Reserved2</td>
<td>6</td>
<td>2</td>
<td>Dieses Feld ist obligatorisch, und sein Inhalt ist reserviert.</td>
</tr>
<tr class="odd">
<td>ValidDataLength</td>
<td>8</td>
<td>8</td>
<td>Dieses Feld ist obligatorisch, und <a href="#765-validdatalength-field">Abschnitt 7.6.5</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>Reserviert3</td>
<td>16</td>
<td>4</td>
<td>Dieses Feld ist obligatorisch, und sein Inhalt ist reserviert.</td>
</tr>
<tr class="odd">
<td>FirstCluster</td>
<td>20</td>
<td>4</td>
<td>Dieses Feld ist obligatorisch, und <a href="#766-firstcluster-field">Abschnitt 7.6.6</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>DataLength</td>
<td>24</td>
<td>8</td>
<td>Dieses Feld ist obligatorisch, und <a href="#767-datalength-field">Abschnitt 7.6.7</a> definiert seinen Inhalt.</td>
</tr>
</tbody>
</table>

#### <a name="761-entrytype-field"></a>7.6.1 EntryType-Feld

Das Feld EntryType muss der Definition entsprechen, die in der Vorlage Generic Secondary DirectoryEntry (siehe [Abschnitt 6.4.1)](#641-entrytype-field)angegeben ist.

##### <a name="7611-typecode-field"></a>7.6.1.1 TypCodefeld

Das Feld TypeCode muss der Definition entsprechen, die in der Vorlage Generic Secondary DirectoryEntry (siehe [Abschnitt 6.4.1.1)](#6411-typecode-field)angegeben ist.

Für den Eintrag stream extension directory ist der gültige Wert für dieses Feld 0.

##### <a name="7612-typeimportance-field"></a>7.6.1.2 TypeImportance Field

Das Feld TypeImportance muss der Definition entsprechen, die in der Vorlage Generic Secondary DirectoryEntry (siehe [Abschnitt 6.4.1.2)](#6412-typeimportance-field)angegeben ist.

Für den Eintrag stream extension directory ist der gültige Wert für dieses Feld 0.

##### <a name="7613-typecategory-field"></a>7.6.1.3 TypeCategory-Feld

Das Feld TypeCategory muss der Definition in der Vorlage Generic Secondary DirectoryEntry entsprechen (siehe [Abschnitt 6.4.1.3).](#6413-typecategory-field)

##### <a name="7614-inuse-field"></a>7.6.1.4 Feld "InUse"

Das Feld InUse muss der Definition entsprechen, die in der Vorlage Generic Secondary DirectoryEntry (siehe [Abschnitt 6.4.1.4)](#6414-inuse-field)angegeben ist.

#### <a name="762-generalsecondaryflags-field"></a>7.6.2 GeneralSecondaryFlags-Feld

Das Feld GeneralSecondaryFlags muss der Definition in der Vorlage Generic Secondary DirectoryEntry (siehe [Abschnitt 6.4.2)](#642-generalsecondaryflags-field)entsprechen und den Inhalt des zu reservierenden CustomDefined-Felds definieren.

##### <a name="7621-allocationpossible-field"></a>7.6.2.1 AllocationPossible Field

Das Feld AllocationPossible muss der Definition entsprechen, die in der Vorlage Generic Secondary DirectoryEntry (siehe [Abschnitt 6.4.2.1)](#6421-allocationpossible-field)angegeben ist.

Für den Eintrag Stream Extension directory (Streamerweiterungsverzeichnis) ist der gültige Wert für dieses Feld 1.

##### <a name="7622-nofatchain-field"></a>7.6.2.2 NoFatChain-Feld

Das Feld NoFatChain muss der Definition in der Vorlage Generic Secondary DirectoryEntry entsprechen (siehe [Abschnitt 6.4.2.2](#6422-nofatchain-field)).

#### <a name="763-namelength-field"></a>7.6.3 NameLength-Feld

Das Feld NameLength muss die Länge der Unicode-Zeichenfolge enthalten, die die nachfolgenden Dateinamen-Verzeichniseinträge (siehe [Abschnitt 7.7)](#77-file-name-directory-entry)zusammen enthalten.

Der gültige Wertebereich für dieses Feld muss:

- Mindestens 1. Dies ist der kürzeste mögliche Dateiname.

- Höchstens 255. Dies ist der längste mögliche Dateiname.

Der Wert des Felds NameLength wirkt sich auch auf die Anzahl der Dateinamenverzeichniseinträge aus (siehe [Abschnitt 7.7](#77-file-name-directory-entry)).

#### <a name="764-namehash-field"></a>7.6.4 NameHashfeld

Das Feld NameHash muss einen 2-Byte-Hash (siehe [Abbildung 4)](#figure-4-namehash-computation)des Dateinamens enthalten, für den die Hochschreibung gilt. Dadurch können Implementierungen einen schnellen Vergleich durchführen, wenn nach einer Datei anhand des Namens gesucht wird. Wichtig: NameHash stellt eine sichere Überprüfung eines Konflikts bereit. Implementierungen müssen überprüfen, ob alle NameHash-Übereinstimmungen mit einem Vergleich des Dateinamens in der Hochschreibung vorliegen.

<div id="figure-4-namehash-computation" />

**Abbildung 4: NameHash-Berechnung**

```C
UInt16 NameHash
(
    WCHAR * FileName,    // points to an in-memory copy of the up-cased file name
    UCHAR   NameLength
)
{
    UCHAR  * Buffer = (UCHAR *)FileName;
    UInt16   NumberOfBytes = (UInt16)NameLength * 2;
    UInt16   Hash = 0;
    UInt16   Index;

    for (Index = 0; Index < NumberOfBytes; Index++)
    {
        Hash = ((Hash&1) ? 0x8000 : 0) + (Hash>>1) + (UInt16)Buffer[Index];
    }
    return Hash;
}
```

#### <a name="765-validdatalength-field"></a>7.6.5 ValidDataLength-Feld

Das Feld ValidDataLength soll beschreiben, wie weit benutzerdaten in den Datenstrom geschrieben wurden. Implementierungen müssen dieses Feld aktualisieren, wenn sie Daten weiter in den Datenstrom schreiben. Auf den Speichermedien sind die Daten zwischen der gültigen Datenlänge und der Datenlänge des Datenstroms nicht definiert. Implementierungen müssen Nullen für Lesevorgänge zurückgeben, die über die gültige Datenlänge hinausgehen.

Wenn der entsprechende Dateiverzeichniseintrag ein Verzeichnis beschreibt, ist der einzige gültige Wert für dieses Feld gleich dem Wert des DataLength-Felds. Andernfalls muss der Bereich der gültigen Werte für dieses Feld wie hier angegeben sein:

- Mindestens 0, was bedeutet, dass keine Benutzerdaten in den Datenstrom geschrieben wurden.

- Höchstens DataLength, was bedeutet, dass Benutzerdaten in die gesamte Länge des Datenstroms geschrieben wurden.

#### <a name="766-firstcluster-field"></a>7.6.6 FirstCluster-Feld

Das Feld FirstCluster muss der Definition entsprechen, die in der Vorlage Generic Secondary DirectoryEntry (siehe [Abschnitt 6.4.3)](#643-firstcluster-field)angegeben ist.

Dieses Feld muss den Index des ersten Clusters des Datenstroms enthalten, der die Benutzerdaten hostet.

#### <a name="767-datalength-field"></a>7.6.7 DataLength-Feld

Das DataLength-Feld muss der Definition in der Vorlage Generic Secondary DirectoryEntry (siehe [Abschnitt 6.4.4)](#644-datalength-field)entsprechen.

Wenn der entsprechende Dateiverzeichniseintrag ein Verzeichnis beschreibt, ist der gültige Wert für dieses Feld die gesamte Größe der zugeordneten Zuordnung in Bytes, die 0 sein kann. Darüber hinaus beträgt der Höchstwert für dieses Feld für Verzeichnisse 256 MB.

### <a name="77-file-name-directory-entry"></a>7.7 Dateiname Verzeichniseintrag

Dateinamen-Verzeichniseinträge sind wichtige sekundäre Verzeichniseinträge in Dateiverzeichniseintragssätzen (siehe [Tabelle 34).](#table-34-file-name-directoryentry) Die gültige Anzahl von Dateinamen-Verzeichniseinträgen in einem Dateiverzeichniseintragssatz ist NameLength/15, aufgerundet auf die nächste ganze Zahl. Darüber hinaus sind Dateinamen-Verzeichniseinträge nur gültig, wenn sie unmittelbar auf den Eintrag des Verzeichnisses der Streamerweiterung als aufeinanderfolgende Reihe folgen. Dateinamen-Verzeichniseinträge werden kombiniert, um den Dateinamen für den Dateiverzeichniseintragssatz zu bilden.

Alle untergeordneten Elemente eines bestimmten Verzeichniseintrags müssen eindeutige Dateinamen-Verzeichniseintragssätze aufweisen. Das heißt, dass nach der Groß-/Kleinschreibung innerhalb eines Verzeichnisses keine doppelten Datei- oder Verzeichnisnamen vorhanden sein dürfen.

<div id="table-34-file-name-directoryentry" />

**Tabelle 34: Dateiname DirectoryEntry**

<table>
<thead>
<tr class="header">
<th><strong>Feldname</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(Byte)</strong></p></th>
<th><p><strong>Größe</strong></p>
<p><strong>(Byte)</strong></p></th>
<th><strong>Kommentare</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EntryType</td>
<td>0</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#771-entrytype-field">Abschnitt 7.7.1</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>GeneralSecondaryFlags</td>
<td>1</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#772-generalsecondaryflags-field">Abschnitt 7.7.2</a> definiert seinen Inhalt.</td>
</tr>
<tr class="odd">
<td>FileName</td>
<td>2</td>
<td>30</td>
<td>Dieses Feld ist obligatorisch, und <a href="#773-filename-field">Abschnitt 7.7.3</a> definiert seinen Inhalt.</td>
</tr>
</tbody>
</table>

#### <a name="771-entrytype-field"></a>7.7.1 EntryType-Feld

Das Feld EntryType muss der Definition entsprechen, die in der Vorlage Generic Secondary DirectoryEntry (siehe [Abschnitt 6.4.1)](#641-entrytype-field)angegeben ist.

##### <a name="7711-typecode-field"></a>7.7.1.1 TypCodefeld

Das Feld TypeCode muss der Definition entsprechen, die in der Vorlage Generic Secondary DirectoryEntry (siehe [Abschnitt 6.4.1.1)](#6411-typecode-field)angegeben ist.

Für den Verzeichniseintrag Streamerweiterung ist der gültige Wert für dieses Feld 1.

##### <a name="7712-typeimportance-field"></a>7.7.1.2 TypeImportance-Feld

Das TypeImportance-Feld muss der Definition entsprechen, die in der Vorlage Generic Secondary DirectoryEntry (generisches sekundäres Verzeichnis) angegeben ist (siehe [Abschnitt 6.4.1.2](#6412-typeimportance-field)).

Für den Verzeichniseintrag Streamerweiterung ist der gültige Wert für dieses Feld 0.

##### <a name="7713-typecategory-field"></a>7.7.1.3 TypeCategory-Feld

Das Feld TypeCategory muss der Definition entsprechen, die in der Vorlage Generic Secondary DirectoryEntry bereitgestellt wird (siehe [Abschnitt 6.4.1.3](#6413-typecategory-field)).

##### <a name="7714-inuse-field"></a>7.7.1.4 InUse-Feld

Das Feld InUse muss der Definition entsprechen, die in der Vorlage Generic Secondary DirectoryEntry (Generisches sekundäres Verzeichnis)(siehe [Abschnitt 6.4.1.4) angegeben ist.](#6414-inuse-field)

#### <a name="772-generalsecondaryflags-field"></a>7.7.2 GeneralSecondaryFlags-Feld

Das Feld GeneralSecondaryFlags muss der Definition entsprechen, die in der Vorlage Generic Secondary DirectoryEntry (siehe Abschnitt [6.4.2)](#642-generalsecondaryflags-field)angegeben ist, und definiert den Inhalt des zu reservierten CustomDefined-Felds.

##### <a name="7721-allocationpossible-field"></a>7.7.2.1 ZuordnungPossible Field

Das Feld AllocationPossible muss der Definition entsprechen, die in der Vorlage Generic Secondary DirectoryEntry (Generisches sekundäres Verzeichnis) angegeben ist (siehe [Abschnitt 6.4.2.1](#6421-allocationpossible-field)).

Für den Verzeichniseintrag Streamerweiterung ist der gültige Wert für dieses Feld 0.

##### <a name="7722-nofatchain-field"></a>7.7.2.2 NoFatChain-Feld

Das NoFatChain-Feld muss der Definition entsprechen, die in der Vorlage Generic Secondary DirectoryEntry (Generisches sekundäres DirectoryEntry) angegeben ist (siehe [Abschnitt 6.4.2.2](#6422-nofatchain-field)).

#### <a name="773-filename-field"></a>7.7.3 FileName-Feld

Das Feld FileName muss eine Unicode-Zeichenfolge enthalten, die ein Teil des Dateinamens ist. In der Reihenfolge, in der Dateinamen-Verzeichniseinträge in einem Dateiverzeichniseintragssatz vorhanden sind, werden die FileName-Felder verkettet, um den Dateinamen für den Dateiverzeichniseintragssatz zu bilden. Angesichts der Länge des Felds "FileName", 15 Zeichen und der maximalen Anzahl von Dateinamen-Verzeichniseinträgen (17) beträgt die maximale Länge des endgültigen, verketteten Dateinamens.
255.

Der verkettete Dateiname hat denselben Satz unzulässiger Zeichen wie andere FAT-basierte Dateisysteme (siehe [Tabelle 35](#table-35-invalid-filename-characters)). Implementierungen sollten die nicht verwendeten Zeichen von FileName-Feldern auf den Wert 0000h festlegen.

<div id="table-35-invalid-filename-characters" />

**Tabelle 35 Ungültige FileName-Zeichen**

| **Zeichencode** | **Beschreibung** | **Zeichencode** | **Beschreibung**   | **Zeichencode** | **Beschreibung** |
|--------------------|-----------------|--------------------|-------------------|--------------------|-----------------|
| 0000h              | Steuerungscode    | 0001h              | Steuerungscode      | 0002h              | Steuerungscode    |
| 0003h              | Steuerungscode    | 0004h              | Steuerungscode      | 0005h              | Steuerungscode    |
| 0006h              | Steuerungscode    | 0007h              | Steuerungscode      | 0008h              | Steuerungscode    |
| 0009h              | Steuerungscode    | 000Ah              | Steuerungscode      | 000Bh              | Steuerungscode    |
| 000Ch              | Steuerungscode    | 000Dh              | Steuerungscode      | 000Eh              | Steuerungscode    |
| 000Fh              | Steuerungscode    | 0010h              | Steuerungscode      | 0011h              | Steuerungscode    |
| 0012h              | Steuerungscode    | 0013h              | Steuerungscode      | 0014h              | Steuerungscode    |
| 0015h              | Steuerungscode    | 0016h              | Steuerungscode      | 0017h              | Steuerungscode    |
| 0018h              | Steuerungscode    | 0019h              | Steuerungscode      | 001Ah              | Steuerungscode    |
| 001Bh              | Steuerungscode    | 001Ch              | Steuerungscode      | 001Dh              | Steuerungscode    |
| 001Eh              | Steuerungscode    | 001Fh              | Steuerungscode      | 0022h              | Anführungszeichen  |
| 002Ah              | Asterisk        | 002Fh              | Schrägstrich     | 003Ah              | Doppelpunkt           |
| 003Ch              | Kleiner-als-Zeichen  | 003Eh              | Größer-als-Zeichen | 003Fh              | Fragezeichen   |
| 005Ch              | Schrägstrich zurück      | 007Ch              | Vertikaler Balken      |                    |                 |

Die Dateinamen "." und ".." haben die besondere Bedeutung "dieses Verzeichnis" bzw. "enthaltende Verzeichnis". Implementierungen dürfen keinen dieser reservierten Dateinamen im Feld FileName aufzeichnen.
Implementierungen können diese beiden Dateinamen jedoch in Verzeichnisauflistungen generieren, um auf das aufgelistete Verzeichnis und das enthaltende Verzeichnis zu verweisen.

Implementierungen können Datei- und Verzeichnisnamen auf den ASCII-Zeichensatz beschränken. Falls ja, sollten sie ihre Zeichennutzung auf den Bereich gültiger Zeichen in den ersten 128 Unicode-Einträgen beschränken. Sie müssen datei- und verzeichnisnamen weiterhin in Unicode auf dem Volume speichern und bei der Interfacing mit dem Benutzer in/aus ASCII/Unicode übersetzen.

### <a name="78-vendor-extension-directory-entry"></a>7.8 Verzeichniseintrag der Anbietererweiterung

Der Verzeichniseintrag Vendor Extension ist ein unbedenklicher sekundärer Verzeichniseintrag in Dateiverzeichniseintragssätzen (siehe [Tabelle 36](#table-36-vendor-extension-directoryentry)). Ein Dateiverzeichniseintragssatz kann eine beliebige Anzahl von Verzeichniseinträgen der Anbietererweiterung bis zum Grenzwert sekundärer Verzeichniseinträge enthalten, weniger als die Anzahl der anderen sekundären Verzeichniseinträge. Darüber hinaus sind Verzeichniseinträge der Anbietererweiterung nur gültig, wenn sie nicht den erforderlichen Verzeichniseinträgen stream extension und file name voran liegen.

Verzeichniseinträge der Anbietererweiterung ermöglichen es Anbietern, über das Feld VendorGuid eindeutige, herstellerspezifische Verzeichniseinträge in einzelnen Dateiverzeichniseintragssätzen zu haben (siehe [Tabelle 36](#table-36-vendor-extension-directoryentry)). Eindeutige Verzeichniseinträge ermöglichen es Anbietern effektiv, das ExFAT-Dateisystem zu erweitern. Hersteller können den Inhalt des Felds VendorDefined definieren (siehe [Tabelle 36](#table-36-vendor-extension-directoryentry)). Anbieterimplementierungen behalten möglicherweise den Inhalt des Felds VendorDefined bei und stellen anbieterspezifische Funktionen zur Verfügung.

Implementierungen, die die GUID eines Verzeichniseintrags der Anbietererweiterung nicht erkennen, müssen den Verzeichniseintrag genauso behandeln wie alle anderen nicht erkannten unbedenklichen sekundären Verzeichniseintrage (siehe [Abschnitt 8.2](#82-implications-of-unrecognized-directory-entries)).

<div id="table-36-vendor-extension-directoryentry" />

**Tabelle 36 Vendor Extension DirectoryEntry**

<table>
<thead>
<tr class="header">
<th><strong>Feldname</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(Byte)</strong></p></th>
<th><p><strong>Größe</strong></p>
<p><strong>(Byte)</strong></p></th>
<th><strong>Kommentare</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EntryType</td>
<td>0</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#781-entrytype-field">in Abschnitt 7.8.1 wird</a> der Inhalt definiert.</td>
</tr>
<tr class="even">
<td>GeneralSecondaryFlags</td>
<td>1</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#782-generalsecondaryflags-field">in Abschnitt 7.8.2 wird</a> der Inhalt definiert.</td>
</tr>
<tr class="odd">
<td>VendorGuid</td>
<td>2</td>
<td>16</td>
<td>Dieses Feld ist obligatorisch, und <a href="#783-vendorguid-field">in Abschnitt 7.8.3 wird</a> der Inhalt definiert.</td>
</tr>
<tr class="even">
<td>VendorDefined</td>
<td>18</td>
<td>14</td>
<td>Dieses Feld ist obligatorisch, und Anbieter können seinen Inhalt definieren.</td>
</tr>
</tbody>
</table>

#### <a name="781-entrytype-field"></a>7.8.1 EntryType-Feld

Das EntryType-Feld muss der Definition entsprechen, die in der Vorlage Generic Secondary DirectoryEntry (Generisches sekundäres DirectoryEntry) angegeben ist (siehe [Abschnitt 6.4.1](#641-entrytype-field)).

##### <a name="7811-typecode-field"></a>7.8.1.1 TypeCode-Feld

Das TypeCode-Feld muss der Definition entsprechen, die in der Vorlage Generic Secondary DirectoryEntry (Generisches sekundäres Verzeichnis) angegeben ist (siehe [Abschnitt 6.4.1.1](#6411-typecode-field)).

Für den Verzeichniseintrag Anbietererweiterung ist der gültige Wert für dieses Feld 0.

##### <a name="7812-typeimportance-field"></a>7.8.1.2 TypeImportance-Feld

Das TypeImportance-Feld muss der Definition entsprechen, die in der Vorlage Generic Secondary DirectoryEntry (generisches sekundäres Verzeichnis) angegeben ist (siehe [Abschnitt 6.4.1.2](#6412-typeimportance-field)).

Für den Verzeichniseintrag Anbietererweiterung ist der gültige Wert für dieses Feld 1.

##### <a name="7813-typecategory-field"></a>7.8.1.3 TypeCategory-Feld

Das Feld TypeCategory muss der Definition entsprechen, die in der Vorlage Generic Secondary DirectoryEntry bereitgestellt wird (siehe [Abschnitt 6.4.1.3](#6413-typecategory-field)).

##### <a name="7814-inuse-field"></a>7.8.1.4 InUse-Feld

Das Feld InUse muss der Definition entsprechen, die in der Vorlage Generic Secondary DirectoryEntry (Generisches sekundäres Verzeichnis)(siehe [Abschnitt 6.4.1.4) angegeben ist.](#6414-inuse-field)

#### <a name="782-generalsecondaryflags-field"></a>7.8.2 GeneralSecondaryFlags-Feld

Das Feld GeneralSecondaryFlags muss der Definition entsprechen, die in der Vorlage Generic Secondary DirectoryEntry (siehe Abschnitt [6.4.2)](#642-generalsecondaryflags-field)angegeben ist, und definiert den Inhalt des zu reservierten CustomDefined-Felds.

##### <a name="7821-allocationpossible-field"></a>7.8.2.1 ZuordnungPossible-Feld

Das Feld AllocationPossible muss der Definition entsprechen, die in der Vorlage Generic Secondary DirectoryEntry (Generisches sekundäres Verzeichnis) angegeben ist (siehe [Abschnitt 6.4.2.1](#6421-allocationpossible-field)).

Für den Verzeichniseintrag Anbietererweiterung ist der gültige Wert für dieses Feld 0.

##### <a name="7822-nofatchain-field"></a>7.8.2.2 NoFatChain-Feld

Das NoFatChain-Feld muss der Definition entsprechen, die in der Vorlage Generic Secondary DirectoryEntry (Generisches sekundäres DirectoryEntry) angegeben ist (siehe [Abschnitt 6.4.2.2](#6422-nofatchain-field)).

#### <a name="783-vendorguid-field"></a>7.8.3 VendorGuid-Feld

Das Feld VendorGuid muss eine GUID enthalten, die die bestimmte Anbietererweiterung eindeutig identifiziert.

Alle möglichen Werte für dieses Feld sind gültig, mit Ausnahme der NULL-GUID, die {00000000-0000-0000-0000-000000000000} ist. Anbieter sollten jedoch ein GUID-generierendes Tool verwenden, z. B. GuidGen.exe, um eine GUID auszuwählen, wenn sie ihre Erweiterungen definieren.

Der Wert dieses Felds bestimmt die herstellerspezifische Struktur des VendorDefined-Felds.

### <a name="79-vendor-allocation-directory-entry"></a>7.9 Eintrag des Anbieterzuordnungsverzeichnisses

Der Verzeichniseintrag Vendor Allocation ist ein unbedenklicher sekundärer Verzeichniseintrag in Dateiverzeichniseintragssätzen (siehe [Tabelle 37](#table-37-vendor-allocation-directoryentry)). Ein Dateiverzeichniseintragssatz kann eine beliebige Anzahl von Verzeichniseinträgen für die Anbieterzuordnung bis zum Grenzwert sekundärer Verzeichniseinträge enthalten, weniger als die Anzahl der anderen sekundären Verzeichniseinträge. Darüber hinaus sind Verzeichniseinträge für die Anbieterzuordnung nur gültig, wenn sie nicht den erforderlichen Verzeichniseinträgen stream extension und file name voran stehen.

Anbieterzuordnungsverzeichniseinträge ermöglichen Es Anbietern, über das Feld VendorGuid eindeutige, herstellerspezifische Verzeichniseinträge in einzelnen Dateiverzeichniseintragssätzen zu erhalten (siehe [Tabelle 37](#table-37-vendor-allocation-directoryentry)). Eindeutige Verzeichniseinträge ermöglichen es Anbietern effektiv, das ExFAT-Dateisystem zu erweitern. Anbieter können den Inhalt der zugeordneten Cluster definieren, sofern vorhanden. Anbieterimplementierungen können den Inhalt der zugeordneten Cluster (sofern erforderlich) verwalten und anbieterspezifische Funktionen bereitstellen.

Implementierungen, die die GUID eines Verzeichniseintrags "Vendor Allocation" nicht erkennen, müssen den Verzeichniseintrag genauso behandeln wie alle anderen nicht erkannten unschädlichen sekundären Verzeichniseintrage (siehe [Abschnitt 8.2](#82-implications-of-unrecognized-directory-entries)).

<div id="table-37-vendor-allocation-directoryentry" />

**Tabelle 37: Vendor Allocation DirectoryEntry**

<table>
<thead>
<tr class="header">
<th><strong>Feldname</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(Byte)</strong></p></th>
<th><p><strong>Größe</strong></p>
<p><strong>(Byte)</strong></p></th>
<th><strong>Kommentare</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EntryType</td>
<td>0</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#791-entrytype-field">in Abschnitt 7.9.1 wird</a> der Inhalt definiert.</td>
</tr>
<tr class="even">
<td>GeneralSecondaryFlags</td>
<td>1</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#792-generalsecondaryflags-field">in Abschnitt 7.9.2 wird</a> der Inhalt definiert.</td>
</tr>
<tr class="odd">
<td>VendorGuid</td>
<td>2</td>
<td>16</td>
<td>Dieses Feld ist obligatorisch, und <a href="#793-vendorguid-field">in Abschnitt 7.9.3 wird</a> der Inhalt definiert.</td>
</tr>
<tr class="even">
<td>VendorDefined</td>
<td>18</td>
<td>2</td>
<td>Dieses Feld ist obligatorisch, und Anbieter können seinen Inhalt definieren.</td>
</tr>
<tr class="odd">
<td>FirstCluster</td>
<td>20</td>
<td>4</td>
<td>Dieses Feld ist obligatorisch, und <a href="#794-firstcluster-field">in Abschnitt 7.9.4 wird</a> der Inhalt definiert.</td>
</tr>
<tr class="even">
<td>DataLength</td>
<td>24</td>
<td>8</td>
<td>Dieses Feld ist obligatorisch, und <a href="#795-datalength-field">in Abschnitt 7.9.5 wird</a> der Inhalt definiert.</td>
</tr>
</tbody>
</table>

#### <a name="791-entrytype-field"></a>7.9.1 EntryType-Feld

Das EntryType-Feld muss der Definition entsprechen, die in der Vorlage Generic Secondary DirectoryEntry (Generisches sekundäres DirectoryEntry) angegeben ist (siehe [Abschnitt 6.4.1](#641-entrytype-field)).

##### <a name="7911-typecode-field"></a>7.9.1.1 TypeCode-Feld

Das TypeCode-Feld muss der Definition entsprechen, die in der Vorlage Generic Secondary DirectoryEntry (Generisches sekundäres Verzeichnis) angegeben ist (siehe [Abschnitt 6.4.1.1](#6411-typecode-field)).

Für den Verzeichniseintrag Vendor Allocation ist der gültige Wert für dieses Feld 1.

##### <a name="7912-typeimportance-field"></a>7.9.1.2 TypeImportance-Feld

Das TypeImportance-Feld muss der Definition entsprechen, die in der Vorlage Generic Secondary DirectoryEntry (generisches sekundäres Verzeichnis) angegeben ist (siehe [Abschnitt 6.4.1.2](#6412-typeimportance-field)).

Für den Verzeichniseintrag Vendor Allocation ist der gültige Wert für dieses Feld 1.

##### <a name="7913-typecategory-field"></a>7.9.1.3 TypeCategory-Feld

Das Feld TypeCategory muss der Definition entsprechen, die in der Vorlage Generic Secondary DirectoryEntry bereitgestellt wird (siehe [Abschnitt 6.4.1.3](#6413-typecategory-field)).

##### <a name="7914-inuse-field"></a>7.9.1.4 InUse-Feld

Das Feld InUse muss der Definition entsprechen, die in der Vorlage Generic Secondary DirectoryEntry (Generisches sekundäres Verzeichnis)(siehe [Abschnitt 6.4.1.4) angegeben ist.](#6414-inuse-field)

#### <a name="792-generalsecondaryflags-field"></a>7.9.2 GeneralSecondaryFlags-Feld

Das Feld GeneralSecondaryFlags muss der Definition entsprechen, die in der Vorlage Generic Secondary DirectoryEntry (siehe Abschnitt [6.4.2)](#642-generalsecondaryflags-field)angegeben ist, und definiert den Inhalt des zu reservierten CustomDefined-Felds.

##### <a name="7921-allocationpossible-field"></a>7.9.2.1 ZuordnungPossible Field

Das Feld AllocationPossible muss der Definition entsprechen, die in der Vorlage Generic Secondary DirectoryEntry (Generisches sekundäres Verzeichnis) angegeben ist (siehe [Abschnitt 6.4.2.1](#6421-allocationpossible-field)).

Für den Verzeichniseintrag Vendor Allocation ist der gültige Wert für dieses Feld 1.

##### <a name="7922-nofatchain-field"></a>7.9.2.2 NoFatChain-Feld

Das NoFatChain-Feld muss der Definition entsprechen, die in der Vorlage Generic Secondary DirectoryEntry (Generisches sekundäres DirectoryEntry) angegeben ist (siehe [Abschnitt 6.4.2.2](#6422-nofatchain-field)).

#### <a name="793-vendorguid-field"></a>7.9.3 VendorGuid-Feld

Das Feld VendorGuid muss eine GUID enthalten, die die bestimmte Anbieterzuordnung eindeutig identifiziert.

Alle möglichen Werte für dieses Feld sind gültig, mit Ausnahme der NULL-GUID, die {00000000-0000-0000-0000-000000000000} ist. Anbieter sollten jedoch ein GUID-generierendes Tool verwenden, z. B. GuidGen.exe, um eine GUID auszuwählen, wenn sie ihre Erweiterungen definieren.

Der Wert dieses Felds bestimmt die herstellerspezifische Struktur des Inhalts der zugeordneten Cluster, sofern vorhanden.

#### <a name="794-firstcluster-field"></a>7.9.4 FirstCluster-Feld

Das FirstCluster-Feld muss der Definition entsprechen, die in der Vorlage Generic Secondary DirectoryEntry (Generisches sekundäres DirectoryEntry) angegeben ist (siehe [Abschnitt 6.4.3](#643-firstcluster-field)).

#### <a name="795-datalength-field"></a>7.9.5 DataLength-Feld

Das DataLength-Feld muss der Definition entsprechen, die in der Vorlage Generic Secondary DirectoryEntry (Generisches sekundäres Verzeichnis) angegeben ist (siehe [Abschnitt 6.4.4](#644-datalength-field)).

### <a name="710-texfat-padding-directory-entry"></a>7.10 TexFAT Padding Directory Entry

Diese Spezifikation, exFAT Revision 1.00 File System Basic Specification, definiert den TexFAT Padding-Verzeichniseintrag nicht. Der Typcode ist jedoch 1 und die Typ wichtigkeit 1. Implementierungen dieser Spezifikation müssen TexFAT Padding-Verzeichniseinträge genauso behandeln wie alle anderen nicht unbekannten, unbedenklichen primären Verzeichniseinträge. Implementierungen dürfen keine TexFAT Padding-Verzeichniseinträge verschieben.

## <a name="8-implementation-notes"></a>8 Hinweise zur Implementierung

### <a name="81-recommended-write-ordering"></a>8.1 Empfohlene Schreib reihenfolge

Implementierungen sollten sicherstellen, dass das Volume so resilient wie möglich gegen Stromausfälle und andere unvermeidbare Fehler ist. Wenn Sie neue Verzeichniseinträge erstellen oder Clusterzuordnungen ändern, sollten Implementierungen in der Regel die folgende Schreib reihenfolge befolgen:

1. Legen Sie den Wert des Felds VolumeDirty auf 1 fest.

2. Aktualisieren Sie bei Bedarf das aktive FAT.

3. Aktualisieren der aktiven Zuordnungsbitmap

4. Erstellen oder aktualisieren Sie bei Bedarf den Verzeichniseintrag.

5. Löschen Sie den Wert des Felds VolumeDirty auf 0, wenn der Wert vor dem ersten Schritt 0 war.

Beim Löschen von Verzeichniseinträgen oder dem Freischreiben von Clusterzuordnungen sollten Implementierungen die folgende Schreib reihenfolge befolgen:

1. Legen Sie den Wert des Felds VolumeDirty auf 1 fest.

2. Löschen oder aktualisieren Sie bei Bedarf den Verzeichniseintrag.

3. Aktualisieren Sie bei Bedarf das aktive FAT.

4. Aktualisieren der aktiven Zuordnungsbitmap

5. Löschen Sie den Wert des Felds VolumeDirty auf 0, wenn der Wert vor dem ersten Schritt 0 war.

### <a name="82-implications-of-unrecognized-directory-entries"></a>8.2 Auswirkungen unbekannter Verzeichniseinträge

Zukünftige exFAT-Spezifikationen mit der gleichen Hauptrevisionsnummer 1 und einer kleineren Revisionsnummer, die höher als 0 sind, können neue unbedenkliche primäre, kritische sekundäre und unbedenkliche sekundäre Verzeichniseinträge definieren. Nur exFAT-Spezifikationen einer höheren Hauptrevisionsnummer können neue kritische primäre Verzeichniseinträge definieren. Implementierungen dieser Spezifikation, exFAT Revision 1.00 File System Basic Specification, sollten in der Lage sein, ein beliebiges ExFAT-Volume der Hauptrevisionsnummer 1 und eine kleinere Revisionsnummer ein- und darauf zu zugreifen. Dies stellt Szenarien vor, in denen eine Implementierung auf Verzeichniseinträge stoßen kann, die sie nicht erkennt. Im Folgenden werden die Auswirkungen dieser Szenarien beschrieben:

1. Wenn im Stammverzeichnis nicht unbekannte kritische primäre Verzeichniseinträge vorhanden sind, wird das Volume ungültig. Wenn ein kritischer primärer Verzeichniseintrag vorhanden ist, mit Ausnahme von Dateiverzeichniseinträgen, wird das Hostverzeichnis ungültig.

2. Implementierungen dürfen nicht unbekannte, unbedenkliche primäre Verzeichniseinträge oder ihre zugeordneten Clusterzuordnungen nicht ändern. Beim Löschen eines Verzeichnisses und nur beim Löschen eines Verzeichnisses sollten Implementierungen jedoch nicht unbekannte, unbedenkliche primäre Verzeichniseinträge löschen und alle zugeordneten Clusterzuordnungen (sofern vorhanden) frei geben.

3. Implementierungen dürfen nicht unbekannte kritische sekundäre Verzeichniseinträge oder ihre zugeordneten Clusterzuordnungen nicht ändern. Wenn mindestens ein nicht unbekannter kritischer sekundärer Verzeichniseintrag in einem Verzeichniseintragssatz vorhanden ist, wird der gesamte Verzeichniseintragssatz nicht mehr angezeigt. Beim Löschen eines Verzeichniseintragssets, der mindestens einen nicht unbekannten kritischen sekundären Verzeichniseintrag enthält, müssen Implementierungen alle Clusterzuordnungen, sofern vorhanden, frei geben, die unbekannten kritischen sekundären Verzeichniseinträgen zugeordnet sind.
   Wenn der Verzeichniseintragssatz ein Verzeichnis beschreibt, können Implementierungen außerdem Folgendes:

   - Durchlaufen des Verzeichnisses

   - Aufzählen der verzeichniseinträge, die sie enthält

   - Löschen enthaltener Verzeichniseinträge

   - Verschieben von enthaltenen Verzeichniseinträgen in ein anderes Verzeichnis

   Implementierungen dürfen jedoch nicht:

   - Ändern sie enthaltene Verzeichniseinträge mit Ausnahme von "delete", wie bereits erwähnt.

   - Erstellen neuer eigenständiger Verzeichniseinträge

   - Öffnen Sie enthaltene Verzeichniseinträge, mit Ausnahme von traverse und enumerate, wie bereits erwähnt.

4. Implementierungen dürfen nicht unbekannte, unbedenkliche sekundäre Verzeichniseinträge oder ihre zugeordneten Clusterzuordnungen nicht ändern.
   Implementierungen sollten unbekannte, unbedenkliche sekundäre Verzeichniseinträge ignorieren. Beim Löschen eines Verzeichniseintragssets müssen Implementierungen alle Clusterzuordnungen(sofern vorhanden) freistellen, die nicht unbekannten, unbedenklichen sekundären Verzeichniseinträgen zugeordnet sind.

## <a name="9-file-system-limits"></a>9 Dateisystemgrenzwerte

### <a name="91-sector-size-limits"></a>9.1 Sektorgrößenbeschränkungen

Das Feld BytesPerSectorShift definiert die Größenbeschränkungen für den unteren und oberen Sektor (die als unterer Grenzwert **ausgewertet werden: 512 Bytes; Obergrenze: 4.096 Byte).**

### <a name="92-cluster-size-limits"></a>9.2 Grenzwerte für die Clustergröße

Das Feld SectorPerClusterShift definiert die unteren und oberen Clustergrößenlimits ( untere **Grenze: 1 Sektor; Obergrenze: 25 -- BytesPerSectorShift-Sektoren,** die zu 32 MB ausgewertet werden).

### <a name="93-cluster-heap-size-limits"></a>9.3 Größenbeschränkungen für Clusterhaps

Der Cluster heap muss mindestens genügend Speicherplatz zum Hosten der folgenden grundlegenden Dateisystemstrukturen enthalten: das Stammverzeichnis, alle Zuordnungsbitmaps und die Up-Case-Tabelle.

Der untere Grenzwert für die Cluster heap-Größe ist eine Funktion der unteren Größenbeschränkung für jede der grundlegenden Dateisystemstrukturen, die sich im Cluster heap befinden. Selbst bei einem klein möglichen Cluster (512 Bytes) benötigt jede der grundlegenden Dateisystemstrukturen nicht mehr als einen Cluster. Daher ist die untere **Grenze: 2 + NumberOfFats-Cluster,** die je nach Wert des NumberOfFats-Felds entweder zu 3 oder 4 Clustern ausgewertet werden.

Die Obergröße des Cluster heaps ist eine einfache Funktion der maximal möglichen Anzahl von Clustern, die im ClusterCount-Feld definiert wird **(Obergrenze: 2 <sup>32</sup>bis 11 Cluster).** Unabhängig von der Clustergröße verfügt ein solcher Clusterhap über genügend Speicherplatz, um mindestens die grundlegenden Dateisystemstrukturen zu hosten.

### <a name="94-volume-size-limits"></a>9.4 Volumegrößenlimits

Das VolumeLength-Feld definiert die unteren und oberen Volumegrößenlimits (Untergrenze: **<sup>2 20</sup>/2 <sup>BytesPerSectorShift-Sektoren,</sup>** die zu 1 MB ausgewertet werden; **Obergrenze: 2 <sup>64</sup>bis 1** Sektoren, die bei einer möglichst großen Sektorgröße ungefähr 64 GRAD beträgt. Diese Spezifikation empfiehlt jedoch nicht mehr als 2<sup>24</sup>bis 2 Cluster im Cluster heap (siehe [Abschnitt 3.1.9](#319-clustercount-field)). Daher ist die empfohlene Obergrenze für ein Volume: ClusterHeapOffset + (2<sup>24</sup>- 2) \* 2<sup>SectorsPerClusterShift</sup>. Bei der größten möglichen Clustergröße von 32 MB und der Annahme, dass ClusterHeapOffset 96 MB beträgt (ausreichend Speicherplatz für die Haupt- und Sicherungsstartregionen und nur die erste FAT-Datei), wird die empfohlene Obergrenze eines Volumes auf ungefähr 512 TB ausgewertet.

### <a name="95-directory-size-limits"></a>9.5 Grenzwerte für die Verzeichnisgröße

Das Feld DataLength des Verzeichniseintrags Stream-Erweiterung definiert die Größenbeschränkungen für untere und obere Verzeichnisse ( untere **Grenze: 0 Bytes; Obergrenze: 256 MB**). Dies bedeutet, dass ein Verzeichnis bis zu 8.388.608 Verzeichniseinträge hosten kann (jeder Verzeichniseintrag verbraucht 32 Bytes). Bei dem kleinsten möglichen Dateiverzeichniseintragssatz, drei Verzeichniseinträgen, kann ein Verzeichnis bis zu 2.796.202 Dateien hosten.

## <a name="10-appendix"></a>10 Anhang

### <a name="101-globally-unique-identifiers-guids"></a>10.1 Globally Unique Identifiers (GUIDs)

Eine GUID ist die Microsoft-Implementierung eines universell eindeutigen Bezeichners. Eine GUID ist ein 128-Bit-Wert, der aus einer Gruppe von acht Hexadezimalziffern gefolgt von drei Gruppen von jeweils vier Hexadezimalziffern gefolgt von einer Gruppe von 12 Hexadezimalziffern besteht, z. B. {6B29FC40-CA47-1067-B31D-00DD010662DA}, (siehe [Tabelle 38](#table-38-guid-structure)).

<div id="table-38-guid-structure" />

**GUID-Struktur in Tabelle 38**

<table>
<thead>
<tr class="header">
<th><strong>Feldname</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(Byte)</strong></p></th>
<th><p><strong>Größe</strong></p>
<p><strong>(Bytes)</strong></p></th>
<th><strong>Kommentare</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Data1</td>
<td>0</td>
<td>4</td>
<td>Dieses Feld ist obligatorisch und enthält die vier Bytes aus der ersten Gruppe der GUID (6B29FC40h aus dem Beispiel).</td>
</tr>
<tr class="even">
<td>Data2</td>
<td>4</td>
<td>2</td>
<td>Dieses Feld ist obligatorisch und enthält die zwei Bytes aus der zweiten Gruppe der GUID (CA47h aus dem Beispiel).</td>
</tr>
<tr class="odd">
<td>Data3</td>
<td>6</td>
<td>2</td>
<td>Dieses Feld ist obligatorisch und enthält die beiden Bytes aus der dritten Gruppe der GUID (1067h aus dem Beispiel).</td>
</tr>
<tr class="even">
<td>Data4[0]</td>
<td>8</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch und enthält das wichtigste Byte aus der vierten Gruppe der GUID (B3h aus dem Beispiel).</td>
</tr>
<tr class="odd">
<td>Data4[1]</td>
<td>9</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch und enthält das am wenigsten signifikante Byte aus der vierten Gruppe der GUID (1Dh aus dem Beispiel).</td>
</tr>
<tr class="even">
<td>Data4[2]</td>
<td>10</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch und enthält das erste Byte aus der fünften Gruppe der GUID (00h aus dem Beispiel).</td>
</tr>
<tr class="odd">
<td>Data4[3]</td>
<td>11</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch und enthält das zweite Byte aus der fünften Gruppe der GUID (DDh aus dem Beispiel).</td>
</tr>
<tr class="even">
<td>Data4[4]</td>
<td>12</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch und enthält das dritte Byte aus der fünften Gruppe der GUID (01h aus dem Beispiel).</td>
</tr>
<tr class="odd">
<td>Data4[5]</td>
<td>13</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch und enthält das vierte Byte aus der fünften Gruppe der GUID (06h aus dem Beispiel).</td>
</tr>
<tr class="even">
<td>Data4[6]</td>
<td>14</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch und enthält das fünfte Byte aus der fünften Gruppe der GUID (62 Stunden aus dem Beispiel).</td>
</tr>
<tr class="odd">
<td>Data4[7]</td>
<td>15</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch und enthält das sechste Byte aus der fünften Gruppe der GUID (DAh aus dem Beispiel).</td>
</tr>
</tbody>
</table>

### <a name="102-partition-tables"></a>10.2 Partitionstabellen

Um die Interoperabilität von exFAT-Volumes in einer Vielzahl von Verwendungsszenarien sicherzustellen, sollten Implementierungen den Partitionstyp 07h für den partitionierten MBR-Speicher und die Partitions-GUID {EBD0A0A2-B9E5-4433-87C0-68B6B72699C7} für partitionierten GPT-Speicher verwenden.

## <a name="11-documentation-change-history"></a>11 Dokumentation Änderungsverlauf

In Tabelle 39 wird der Verlauf von Releases, Korrekturen, Ergänzungen, Entfernungen aus und Erläuterungen dieses Dokuments beschrieben.

<div id="table-39-documentation-change-history" />

**Tabelle 39: Änderungsverlauf der Dokumentation**

<table>
<thead>
<tr class="header">
<th><strong>Datum</strong></th>
<th><strong>Beschreibung der Änderung</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>08-Jan-2008</td>
<td><p>Erste Version der Basic-Spezifikation, die Folgendes umfasst:</p>
<blockquote>
<p>Abschnitt 1: Einführung</p>
<p>Abschnitt 2:<br />
Volumestruktur</p>
<p>Abschnitt 3: Haupt- und Sicherungsstartregionen</p>
<p>Abschnitt 4: Dateizuordnungstabellenbereich</p>
<p>Abschnitt 5, Datenbereich</p>
<p>Abschnitt 6, Verzeichnisstruktur</p>
<p>Abschnitt 7, Verzeichniseintragsdefinitionen</p>
<p>Abschnitt 8, Implementierungshinweise</p>
<p>Abschnitt 9, Dateisystemgrenzwerte</p>
<p>Abschnitt 10, Anhang</p>
</blockquote></td>
</tr>
<tr class="even">
<td>08-Jun-2008</td>
<td><p>Zweite Version der Basisspezifikation, die die folgenden Änderungen enthält:</p>
<blockquote>
<p>Addition von Abschnitt 11,<br />
Änderungsverlauf der Dokumentation</p>
<p>Hinzufügen der Verzeichniseinträge "Vendor Extension" und "Vendor Allocation" in den Abschnitten 7.8 und 7.9</p>
<p>Addition der empfohlenen Up-Case-Tabelle in den Abschnitten 7.2.5 und 7.2.5.1</p>
<p>Addition der UtcOffset-Felder in Abschnitt 7.4 und Addition des UTC-Akronyms in Abschnitt 1.3</p>
<p>Korrektur der Größe des CustomDefined-Felds in Tabelle 19</p>
<p>Korrektur des gültigen Bereichs von NameLength-Werten in Abschnitt 7.6.3</p>
<p>Korrektur und Erläuterung der Felder "Timestamp" und "10msIncrement" in Abschnitt 7.4</p>
<p>Erläuterung der Nullparameterstruktur in Abschnitt 3.3</p>
<p>Erläuterung der Bedeutung der Werte des Felds NoFatChain in Abschnitt 6.3.4.2</p>
<p>Erläuterung der Bedeutung der Werte des DataLength-Felds in Abschnitt 6.2.3</p>
<p>Erläuterung des Felds VolumeDirty in Abschnitt 3.1.13.2 und der empfohlenen Schreib reihenfolge in Abschnitt 8.1</p>
<p>Erläuterung des Felds "MediaFailure" in Abschnitt 3.1.13.3</p>
</blockquote></td>
</tr>
<tr class="odd">
<td>01.10.2008</td>
<td><p>Dritte Version der Basisspezifikation, die die folgenden Änderungen enthält:</p>
<blockquote>
<p>Addition von SHOULD, SHOULD und MAY zu Felderklärungen</p>
<p>Addition der UTC-Definition in Tabelle 2 Abschnitt 1.3</p>
<p>Die Abschnitte 1.5 wurden geändert, um die Übereinstimmung mit dem Dokument zur TexFAT-Spezifikation sicherzustellen.</p>
<p>Es wurde die Einschränkung verdeutlicht, dass nur Microsoft das Layout von Verzeichniseinträgen in Abschnitt 6.2 definieren darf.</p>
<p>Es wurde erläutert, dass FirstCluster Field null sein soll, wenn DataLength 0 (null) und NoFatChain auf Abschnitt 6.3.5 und Abschnitt 6.4.3 festgelegt ist.</p>
<p>In Abschnitt 7.4 wurden die Anforderungen für gültige Dateiverzeichniseinträge erläutert.</p>
<p>Anforderung für eindeutige Datei- und Verzeichnisnamen zu Abschnitt 7.7 hinzugefügt</p>
<p>Implementierungshinweis für ASCII am Ende von Abschnitt 7.7.3 hinzugefügt</p>
</blockquote></td>
</tr>
<tr class="even">
<td>01-Jan-2009</td>
<td><p>Vierte Version der Basisspezifikation, die die folgenden Änderungen umfasst:</p>
<blockquote>
<p>Verweise auf Windows CE Access Control wurden entfernt.</p>
<p>Erläuterung zu Abschnitt 7.2.5.1 hinzugefügt, um explizit eine vollständige Up-Case-Tabelle zu erfordern</p>
</blockquote></td>
</tr>
<tr class="odd">
<td>02.09.2009</td>
<td><p>Fünfte Version der Basisspezifikation, die die folgenden Änderungen umfasst:</p>
<blockquote>
<p>Dokumentformatierungsänderungen, um eine bessere PDF-Konvertierung zu ermöglichen</p>
</blockquote></td>
</tr>
<tr class="even">
<td>24-Feb-2010</td>
<td><p>Sechste Version der Basisspezifikation, die die folgenden Änderungen umfasst:</p>
<blockquote>
<p>Falsche Anweisung geändert: "FirstCluster Field must be zero if the DataLength is 0 and NoFatChain is set" in Section 6.3.5 and Section 6.4.3 to "If the NoFatChain bit is 1 the FirstCluster must point to a valid cluster in the cluster heap" (FirstCluster-Feld muss null sein, wenn das DataLength-Bit 0 (null) und NoFatChain festgelegt ist) in Abschnitt 6.3.5 und Section 6.4.3 auf "If the NoFatChain bit is 1 the FirstCluster must point to a valid cluster in the cluster heap" (Wenn das NoFatChain-Bit 1 ist, muss FirstCluster auf einen gültigen Cluster im Clusterheap verweisen), um zu verdeutlichen, dass eine gültige Zuordnung möglich sein muss, wenn das NoFatChain-Bit festgelegt ist.</p>
<p>Hinzugefügt: "Wenn das NoFatChain-Bit 1 ist, darf DataLength nicht 0 (null) sein. Wenn das FirstCluster-Feld 0 (null) ist, muss DataLength auch 0 (null) für Abschnitt 6.3.6 und Abschnitt 6.4.4 sein, um zu verdeutlichen, dass es eine gültige Zuordnung geben muss, wenn das NoFatChain-Bit festgelegt ist.</p>
<p>Copyrighthinweis auf 2010 aktualisiert</p>
</blockquote></td>
</tr>
<tr class="odd">
<td>26-Aug-2019</td>
<td><p>Das siebten Release der Basisspezifikation, das die folgenden Änderungen umfasst:</p>
<blockquote>
<p>Aktualisierte rechtliche Bestimmungen in Bezug auf die Spezifikation, einschließlich:</p>
<p>Entfernen des vertraulichen Microsoft-Hinweises</p>
<p>Entfernen des Microsoft Corporation Abschnitts "Lizenzvereinbarung für die technische Dokumentation"</p>
<p>Copyrighthinweis auf 2019 aktualisiert</p>
</blockquote></td>
</tr>
</tbody>
</table>
