---
description: Spezifikation des exFAT-Dateisystems.
title: exFAT-Dateisystem Spezifikation
ms.topic: article
ms.date: 08/27/2019
ms.openlocfilehash: c23a1f0c7aa9f0ad4752ce83cb734e753094c2cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350897"
---
# <a name="exfat-file-system-specification"></a>exFAT-Dateisystem Spezifikation

## <a name="1-introduction"></a>1 Einführung

Das exFAT-Dateisystem ist der Nachfolger von FAT32 in der FAT-Familie von Dateisystemen. Diese Spezifikation beschreibt das exFAT-Dateisystem und stellt alle Informationen bereit, die für die Implementierung des exFAT-Dateisystems benötigt werden.

### <a name="11-design-goals"></a>1,1 Entwurfs Ziele

Das exFAT-Dateisystem umfasst drei zentrale Entwurfs Ziele (siehe Liste unten).

1. *Behalten Sie die Einfachheit der FAT-basierten Dateisysteme bei.*

   > Zwei der Stärken von FAT-basierten Dateisystemen sind ihre relative Einfachheit und einfache Implementierung. Im Sinne seiner Vorgänger sollten Implementierer das exFAT relativ einfach und einfach zu implementieren finden.

2. *Aktivieren Sie sehr große Dateien und Speichergeräte.*

   > Das exFAT-Dateisystem verwendet 64 Bits, um die Dateigröße zu beschreiben. Dadurch werden Anwendungen aktiviert, die von sehr großen Dateien abhängen. Das Dateisystem exFAT ermöglicht auch Cluster mit einer Größe von 32 MB und ermöglicht dadurch eine effektive Aktivierung sehr großer Speichergeräte.

3. *Integrieren Sie die Erweiterbarkeit für zukünftige Innovationen.*

   > Das exFAT-Dateisystem integriert die Erweiterbarkeit in den Entwurf, sodass das Dateisystem mit Innovationen im Speicher und den Nutzungsänderungen Schritt halten kann.

### <a name="12-specific-terminology"></a>1,2 spezifische Terminologie

Im Kontext dieser Spezifikation tragen bestimmte Begriffe (siehe [Tabelle 1](#table-1-definition-of-terms-which-carry-very-specific-meaning)) eine bestimmte Bedeutung für das Design und die Implementierung des exFAT-Dateisystems.

<div id="table-1-definition-of-terms-which-carry-very-specific-meaning" />

**Tabelle 1 Definition der Begriffe, die eine sehr spezifische Bedeutung haben**

<table>
<thead>
<tr class="header">
<th><strong>Begriff</strong></th>
<th><strong>Definition</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Gerne</td>
<td>Diese Spezifikation verwendet den Begriff "soll", um ein erforderliches Verhalten zu beschreiben.</td>
</tr>
<tr class="even">
<td>Optional</td>
<td>Diese Spezifikation verwendet den Begriff "sollte", um ein Verhalten zu beschreiben, das dringend empfohlen wird, aber nicht zwingend erforderlich ist.</td>
</tr>
<tr class="odd">
<td>May</td>
<td>Diese Spezifikation verwendet den Begriff "May", um ein optionales Verhalten zu beschreiben.</td>
</tr>
<tr class="even">
<td>Obligatorisch.</td>
<td>Dieser Begriff beschreibt ein Feld oder eine Struktur, das von einer Implementierung geändert werden muss, und die in dieser Spezifikation interpretiert werden soll.</td>
</tr>
<tr class="odd">
<td>Optional</td>
<td>Dieser Begriff beschreibt ein Feld oder eine Struktur, das von einer Implementierung unterstützt werden kann. Wenn eine Implementierung ein bestimmtes optionales Feld oder eine gegebene Struktur unterstützt, muss Sie das Feld oder die Struktur ändern und interpretieren, wie in dieser Spezifikation beschrieben wird.</td>
</tr>
<tr class="even">
<td>Nicht definiert</td>
<td>In diesem Begriff werden die Feld-oder Struktur Inhalte beschrieben, die eine Implementierung ggf. ändern kann (d. h. beim Festlegen von umgebenden Feldern oder Strukturen auf 0 (null) festgelegt wird) und nicht für eine bestimmte Bedeutung interpretiert werden</td>
</tr>
<tr class="odd">
<td>Reserviert</td>
<td><p>Dieser Begriff beschreibt Feld-oder Struktur Inhalte, welche Implementierungen:</p>
<ol type="1">
<li><p>Initialisierung mit 0 (null) und sollte nicht für einen beliebigen Zweck verwendet werden.</p></li>
<li><p>Sollte nicht interpretiert werden, außer wenn Prüfsummen berechnet werden.</p></li>
<li><p>Muss über Vorgänge hinweg beibehalten werden, die umgebende Felder oder Strukturen ändern</p></li>
</ol></td>
</tr>
</tbody>
</table>

### <a name="13-full-text-of-common-acronyms"></a>1,3 vollständiger Text von allgemeinen Akronymen

Diese Spezifikation verwendet Akronyme, die häufig in der persönlichen Computerbranche verwendet werden (siehe [Tabelle 2](#table-2-full-text-of-common-acronyms)).

<div id="table-2-full-text-of-common-acronyms" />

**Tabelle 2 Volltext von allgemeinen Akronymen**

| **Akronym** | **Volltext**                                      |
|-------------|----------------------------------------------------|
| ASCII       | American Standard Code for Information Interchange |
| BIOS        | Einfaches Eingabe Ausgabe System                          |
| CPU         | Zentrale Verarbeitungseinheit                            |
| exFAT       | erweiterbare Datei Zuordnungs Tabelle                   |
| FAT         | Datei Zuordnungs Tabelle                              |
| FAT12       | Datei Zuordnungs Tabelle, 12-Bit-Cluster Indizes      |
| FAT16       | Datei Zuordnungs Tabelle, 16-Bit-Cluster Indizes      |
| FAT32       | Datei Zuordnungs Tabelle, 32-Bit-Cluster Indizes      |
| GPT         | GUID-Partitionstabelle                               |
| GUID        | Global eindeutiger Bezeichner (siehe [Abschnitt 10,1](#101-globally-unique-identifiers-guids))      |
| INT         | Interrupt                                          |
| MBR         | Master Boot Record                                 |
| texfat      | Transaktions sicheres exFAT                             |
| UTC         | Koordinierte Weltzeit (UTC)                         |

### <a name="14-default-field-and-structure-qualifiers"></a>1,4 Standard Qualifizierer für Felder und Strukturen

Felder und Strukturen in dieser Spezifikation haben die folgenden Qualifizierer (siehe nachstehende Liste), es sei denn, die Spezifikation ist anderweitig angegeben.

1. Nicht signiert

2. Verwenden Sie die Dezimal Schreibweise, um Werte zu beschreiben, sofern nicht anderweitig angegeben. Diese Spezifikation verwendet den Postfix-Buchstaben "h", um hexadezimale Zahlen anzugeben und GUIDs in geschweiften Klammern einzuschließen.

3. Im Little-Endian-Format

4. NULL-abschließende Zeichen für Zeichen folgen nicht erforderlich

### <a name="15-windows-ce-and-texfat"></a>1,5 Windows CE und texfat

Texfat ist eine Erweiterung für exFAT, mit der eine Transaktions sichere Betriebs Semantik zusätzlich zum Basisdatei System hinzugefügt wird. Texfat wird von Windows CE verwendet.
Für texfat müssen die zwei Fetten und Zuordnungs Bitmaps für die Verwendung in Transaktionen verwendet werden. Außerdem werden mehrere zusätzliche Strukturen definiert, einschließlich Auffüll Deskriptoren und Sicherheits Deskriptoren.

## <a name="2-volume-structure"></a>2 Volumenstruktur

Ein Volume ist der Satz aller Dateisystem Strukturen und des Daten Speicherplatzes, der zum Speichern und Abrufen von Benutzerdaten erforderlich ist. Alle exFAT-Volumes enthalten vier Regionen (siehe [Tabelle 3](#table-3-volume-structure)).

<div id="table-3-volume-structure" />

**Tabelle 3, Volumestruktur**

<table>
<thead>
<tr class="header">
<th><strong>Name der Unterregion</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>Teil</strong></p></th>
<th><p><strong>Größe</strong></p>
<p><strong>Sektors</strong></p></th>
<th><strong>Kommentare</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Haupt Startbereich</strong></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td>Haupt Startsektor</td>
<td>0</td>
<td>1</td>
<td>Diese Unterregion ist obligatorisch, und in <a href="#31-main-and-backup-boot-sector-sub-regions">Abschnitt 3,1</a> wird Ihr Inhalt definiert.</td>
</tr>
<tr class="odd">
<td>Erweiterte Haupt Start Sektoren</td>
<td>1</td>
<td>8</td>
<td>Diese Unterregion ist obligatorisch, und <a href="#32-main-and-backup-extended-boot-sectors-sub-regions">Abschnitt 3,2</a>) definiert ihren Inhalt.</td>
</tr>
<tr class="even">
<td>OEM-Hauptparameter</td>
<td>9</td>
<td>1</td>
<td>Diese Unterregion ist obligatorisch, und in <a href="#33-main-and-backup-oem-parameters-sub-regions">Abschnitt 3,3</a> wird Ihr Inhalt definiert.</td>
</tr>
<tr class="odd">
<td>Main reserviert</td>
<td>10</td>
<td>1</td>
<td>Diese Unterregion ist obligatorisch, und ihre Inhalte sind reserviert.</td>
</tr>
<tr class="even">
<td>Haupt startprüfsumme</td>
<td>11</td>
<td>1</td>
<td>Diese Unterregion ist obligatorisch, und in <a href="#34-main-and-backup-boot-checksum-sub-regions">Abschnitt 3,4</a> wird Ihr Inhalt definiert.</td>
</tr>
<tr class="odd">
<td><strong>Startbereich der Sicherung</strong></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td>Sicherungs Startsektor</td>
<td>12</td>
<td>1</td>
<td>Diese Unterregion ist obligatorisch, und in <a href="#31-main-and-backup-boot-sector-sub-regions">Abschnitt 3,1</a> wird Ihr Inhalt definiert.</td>
</tr>
<tr class="odd">
<td>Erweiterte Start Sektoren sichern</td>
<td>13</td>
<td>8</td>
<td>Diese Unterregion ist obligatorisch, und in <a href="#32-main-and-backup-extended-boot-sectors-sub-regions">Abschnitt 3,2</a> wird Ihr Inhalt definiert.</td>
</tr>
<tr class="even">
<td>OEM-Parameter sichern</td>
<td>21</td>
<td>1</td>
<td>Diese Unterregion ist obligatorisch, und in <a href="#33-main-and-backup-oem-parameters-sub-regions">Abschnitt 3,3</a> wird Ihr Inhalt definiert.</td>
</tr>
<tr class="odd">
<td>Sicherung reserviert</td>
<td>22</td>
<td>1</td>
<td>Diese Unterregion ist obligatorisch, und ihre Inhalte sind reserviert.</td>
</tr>
<tr class="even">
<td>Prüfsumme für Sicherungs Start</td>
<td>23</td>
<td>1</td>
<td>Diese Unterregion ist obligatorisch, und in <a href="#34-main-and-backup-boot-checksum-sub-regions">Abschnitt 3,4</a> wird Ihr Inhalt definiert.</td>
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
<td>Fatoffset – 24</td>
<td><p>Diese Unterregion ist obligatorisch, und ihre Inhalte sind ggf. nicht definiert.</p>
<p>Hinweis: die Start Sektoren "Main" und "Backup" enthalten beide das Feld "fatoffset".</p></td>
</tr>
<tr class="odd">
<td>Erstes FAT</td>
<td>Fatoffset</td>
<td>Fatlength</td>
<td><p>Diese Unterregion ist obligatorisch, und in <a href="#41-first-and-second-fat-sub-regions">Abschnitt 4,1</a> wird Ihr Inhalt definiert.</p>
<p>Hinweis: die Haupt-und Sicherungs Start Sektoren enthalten beide die Felder "fatoffset" und "fatlength".</p></td>
</tr>
<tr class="even">
<td>Zweites FAT</td>
<td>Fatoffset + fatlength</td>
<td>Fatlength * (zahloffats – 1)</td>
<td><p>Diese Unterregion ist obligatorisch, und <a href="#41-first-and-second-fat-sub-regions">Abschnitt 4,1</a> definiert ihren Inhalt, falls vorhanden.</p>
<p>Hinweis: die Haupt-und Sicherungs Start Sektoren enthalten beide die Felder "fatoffset", "fatlength" und "numoffats". Das Feld "Anzahlen" darf nur die Werte 1 und 2 enthalten.</p></td>
</tr>
<tr class="odd">
<td><strong>Datenbereich</strong></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td>Cluster Heap Ausrichtung</td>
<td>Fatoffset + fatlength *-nummerierte</td>
<td>Clusterheapoffset – (fatoffset + fatlength *-nummerierte)</td>
<td><p>Diese Unterregion ist obligatorisch, und ihre Inhalte sind ggf. nicht definiert.</p>
<p>Hinweis: die Haupt-und Sicherungs Start Sektoren enthalten beide die Felder "fatoffset", "fatlength", "numoffats" und "clusterheapoffset". Die gültigen Werte für das Feld "zahloffats" lauten 1 und 2.</p></td>
</tr>
<tr class="odd">
<td>Cluster Heap</td>
<td>Clusterheapoffset</td>
<td>Cluster count * 2<sup>Sector sperclustershift</sup></td>
<td><p>Diese Unterregion ist obligatorisch, und in <a href="#51-cluster-heap-sub-region">Abschnitt 5,1</a> wird Ihr Inhalt definiert.</p>
<p>Hinweis: die Haupt-und Sicherungs Start Sektoren enthalten beide Felder "clusterheapoffset", "clustercount" und "sectorsperclustershift".</p></td>
</tr>
<tr class="even">
<td>Mehr Speicherplatz</td>
<td>Clusterheapoffset + Cluster count * 2<sup>Sector sperclustershift</sup></td>
<td>Volumelength – (clusterheapoffset + Cluster count * 2<sup>Sector sperclustershift</sup>)</td>
<td><p>Diese Unterregion ist obligatorisch, und ihre Inhalte sind ggf. nicht definiert.</p>
<p>Hinweis: die Haupt-und Sicherungs Start Sektoren enthalten beide Felder "clusterheapoffset", "clustercount", "sectorsperclustershift" und "volumelength".</p></td>
</tr>
</tbody>
</table>

## <a name="3-main-and-backup-boot-regions"></a>3 Haupt-und Sicherungs Start Regionen

Der Haupt Startbereich bietet alle erforderlichen Bootstrapping-Anweisungen, identifizierende Informationen und Dateisystem Parameter, damit eine Implementierung Folgendes ausführen kann:

1. Starten Sie ein Computersystem über ein exFAT-Volume.

2. Identifizieren Sie das Dateisystem auf dem Volume als exFAT.

3. Ermitteln Sie den Speicherort der exFAT-Dateisystem Strukturen.

Der Startbereich der Sicherung ist eine Sicherung des Haupt Startbereichs. Dadurch wird die Wiederherstellung des exFAT-Volumes unterstützt, wenn sich der Haupt Startbereich in einem inkonsistenten Zustand befindet. Mit Ausnahme von seltenen Fällen, z. b. beim Aktualisieren von Bootstrapping-Anweisungen, sollten Implementierungen den Inhalt des Startbereichs der Sicherung nicht ändern.

### <a name="31-main-and-backup-boot-sector-sub-regions"></a>3,1 Haupt-und Sicherungs-Start sektorunterregionen

Der Haupt Startsektor enthält Code für das Bootstrapping von einem exFAT-Volume und grundlegende exFAT-Parameter, die die Volumestruktur beschreiben (siehe [Tabelle 4](#table-4-main-and-backup-boot-sector-structure)). BIOS-, MBR-oder andere Bootstrapping-Agents können diesen Sektor untersuchen und alle darin enthaltenen Bootstrapping-Anweisungen laden und ausführen.

Der Sicherungs Startsektor ist eine Sicherung des Haupt Bootsektors und verfügt über die gleiche Struktur (siehe [Tabelle 4](#table-4-main-and-backup-boot-sector-structure)). Der Sicherungs Startsektor kann Wiederherstellungs Vorgänge unterstützen. Allerdings müssen Implementierungen den Inhalt der Felder "Volumeflags" und "prozentualuse" als veraltet behandeln.

Vor der Verwendung des Inhalts des Haupt-oder Sicherungs Start Sektors müssen Implementierungen ihren Inhalt überprüfen, indem Sie die jeweilige Start Prüfsumme überprüfen und sicherstellen, dass sich alle Felder innerhalb des gültigen Wertebereichs befinden.

Während der anfängliche Formatierungs Vorgang den Inhalt sowohl des Haupt-als auch des Sicherungs Start Sektors initialisieren, können Implementierungen diese Sektoren aktualisieren (und auch Ihre entsprechende Start Prüfsumme aktualisieren), wenn dies erforderlich ist. Allerdings können Implementierungen entweder die Felder "Volumeflags" oder "prozentualuse" aktualisieren, ohne die jeweilige Start Prüfsumme zu aktualisieren (die Prüfsumme schließt diese beiden Felder ausdrücklich aus).

<div id="table-4-main-and-backup-boot-sector-structure" />

**Tabelle 4, Haupt-und Sicherungs Start Sektorstruktur**

<table>
<thead>
<tr class="header">
<th><strong>Feldname</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>Hobby</strong></p></th>
<th><p><strong>Größe</strong></p>
<p><strong>Satz</strong></p></th>
<th><strong>Kommentare</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Jumpboot</td>
<td>0</td>
<td>3</td>
<td>Dieses Feld ist obligatorisch, und <a href="#311-jumpboot-field">Abschnitt 3.1.1</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>File Systemname</td>
<td>3</td>
<td>8</td>
<td>Dieses Feld ist obligatorisch, und <a href="#312-filesystemname-field">Abschnitt 3.1.2</a> definiert seinen Inhalt.</td>
</tr>
<tr class="odd">
<td>Mustbezero</td>
<td>11</td>
<td>53</td>
<td>Dieses Feld ist obligatorisch, und <a href="#313-mustbezero-field">Abschnitt 3.1.3</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>Partitionoffset</td>
<td>64</td>
<td>8</td>
<td>Dieses Feld ist obligatorisch, und <a href="#314-partitionoffset-field">section 3.1.4</a> definiert seinen Inhalt.</td>
</tr>
<tr class="odd">
<td>Volumelength</td>
<td>72</td>
<td>8</td>
<td>Dieses Feld ist obligatorisch, und <a href="#315-volumelength-field">section 3.1.5</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>Fatoffset</td>
<td>80</td>
<td>4</td>
<td>Dieses Feld ist obligatorisch, und <a href="#316-fatoffset-field">section 3.1.6</a> definiert seinen Inhalt.</td>
</tr>
<tr class="odd">
<td>Fatlength</td>
<td>84</td>
<td>4</td>
<td>Dieses Feld ist obligatorisch, und <a href="#317-fatlength-field">section 3.1.7</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>Clusterheapoffset</td>
<td>88</td>
<td>4</td>
<td>Dieses Feld ist obligatorisch, und <a href="#318-clusterheapoffset-field">section 3.1.8</a> definiert seinen Inhalt.</td>
</tr>
<tr class="odd">
<td>Cluster count (</td>
<td>92</td>
<td>4</td>
<td>Dieses Feld ist obligatorisch, und <a href="#319-clustercount-field">section 3.1.9</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>Firstclusterofrootdirectory</td>
<td>96</td>
<td>4</td>
<td>Dieses Feld ist obligatorisch, und <a href="#3110-firstclusterofrootdirectory-field">section 3.1.10</a> definiert seinen Inhalt.</td>
</tr>
<tr class="odd">
<td>VolumeSerialNumber</td>
<td>100</td>
<td>4</td>
<td>Dieses Feld ist obligatorisch, und <a href="#3111-volumeserialnumber-field">section 3.1.11</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>Filesystemrevision</td>
<td>104</td>
<td>2</td>
<td>Dieses Feld ist obligatorisch, und <a href="#3112-filesystemrevision-field">section 3.1.12</a> definiert seinen Inhalt.</td>
</tr>
<tr class="odd">
<td>Volumeflags</td>
<td>106</td>
<td>2</td>
<td>Dieses Feld ist obligatorisch, und <a href="#3113-volumeflags-field">section 3.1.13</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>BytesPerSector Shift</td>
<td>108</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#3114-bytespersectorshift-field">section 3.1.14</a> definiert seinen Inhalt.</td>
</tr>
<tr class="odd">
<td>Sector sperclustershift</td>
<td>109</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#3115-sectorsperclustershift-field">section 3.1.15</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>Anzahlen</td>
<td>110</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#3116-numberoffats-field">section 3.1.16</a> definiert seinen Inhalt.</td>
</tr>
<tr class="odd">
<td>Driveselect</td>
<td>111</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#3117-driveselect-field">section 3.1.17</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>Prozentualuse</td>
<td>112</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#3118-percentinuse-field">section 3.1.18</a> definiert seinen Inhalt.</td>
</tr>
<tr class="odd">
<td>Reserviert</td>
<td>113</td>
<td>7</td>
<td>Dieses Feld ist obligatorisch, und die Inhalte sind reserviert.</td>
</tr>
<tr class="even">
<td>Bootcode</td>
<td>120</td>
<td>390</td>
<td>Dieses Feld ist obligatorisch, und <a href="#3119-bootcode-field">section 3.1.19</a> definiert seinen Inhalt.</td>
</tr>
<tr class="odd">
<td>Bootsignature</td>
<td>510</td>
<td>2</td>
<td>Dieses Feld ist obligatorisch, und <a href="#3120-bootsignature-field">section 3.1.20</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>Excess Space</td>
<td>512</td>
<td>2<sup>BytesPerSector Shift</sup> – 512</td>
<td><p>Dieses Feld ist obligatorisch, und sein Inhalt ist ggf. nicht definiert.</p>
<p>Hinweis: die Haupt-und Sicherungs Start Sektoren enthalten das Feld bytespersectorshift.</p></td>
</tr>
</tbody>
</table>

#### <a name="311-jumpboot-field"></a>3.1.1 jumpboot-Feld

Das jumpboot-Feld muss die Sprung Anweisung für CPUs enthalten, die in PCs üblich sind, die bei der Ausführung "springt" die CPU, um die Bootstrapping-Anweisungen im Feld "Bootcode" auszuführen.

Der gültige Wert für dieses Feld ist (in der Reihenfolge von Byte bis zu höherwertigen Byte) EBH 76h 90h.

#### <a name="312-filesystemname-field"></a>3.1.2 filesystemname-Feld

Das Feld "filesystemname" muss den Namen des Dateisystems auf dem Volume enthalten.

Der gültige Wert für dieses Feld ist, in ASCII-Zeichen "exFAT", die drei nachfolgende Leerzeichen enthält.

#### <a name="313-mustbezero-field"></a>3.1.3 mustbezero-Feld

Das Feld mustbezero muss direkt mit dem Bereich von Bytes übereinstimmen, den der gepackte BIOS-Parameter Block auf FAT12/16/32-Volumes verbraucht.

Der gültige Wert für dieses Feld ist 0, wodurch verhindert wird, dass FAT12/16/32-Implementierungen versehentlich ein exFAT-Volume einbinden.

#### <a name="314-partitionoffset-field"></a>3.1.4 partitionoffset-Feld

Im Feld partitionoffset muss der Medien relative sektoroffset der Partition, die das angegebene exFAT-Volume hostet, beschrieben werden. Dieses Feld unterstützt das Bootstrapping vom Volume mithilfe des erweiterten int 13 h auf PCs.

Alle möglichen Werte für dieses Feld sind gültig. der Wert 0 gibt jedoch an, dass die Implementierungen dieses Feld ignorieren müssen.

#### <a name="315-volumelength-field"></a>3.1.5 volumelength-Feld

Im volumelength-Feld muss die Größe des angegebenen exFAT-Volumes in Sektoren beschrieben werden.

Der gültige Wertebereich für dieses Feld muss wie folgt lauten:

- Mindestens 2<sup>20</sup>/2<sup>BytesPerSector Shift</sup>, wodurch sichergestellt wird, dass das kleinste Volume nicht kleiner als 1 MB ist.

- Höchstens 2<sup>64</sup>-1, der größte Wert, der in diesem Feld beschrieben werden kann

Wenn die Größe des unter Bereichs für den überzähligen Raum jedoch 0 beträgt, ist der Wert dieses Felds clusterheapoffset + (2<sup>32</sup>-11) \* 2<sup>sectorsperclustershift</sup>.

#### <a name="316-fatoffset-field"></a>3.1.6 fatoffset-Feld

Im Feld "fatoffset" muss der volumerelative sektoroffset des ersten FAT beschrieben werden. Dieses Feld ermöglicht Implementierungen, das erste FAT an den Merkmalen des zugrunde liegenden Speichermediums auszurichten.

Der gültige Wertebereich für dieses Feld muss wie folgt lauten:

- Mindestens 24, welche Konten für die von den Haupt-und Sicherungs Start Regionen genutzten Sektoren

- Höchstens clusterheapoffset-(Anzahl der maximal Dauer \* ), welche die von dem Cluster Heap verbrauchten Sektoren belegen

#### <a name="317-fatlength-field"></a>3.1.7 fatlength-Feld

Im Feld "fatlength" wird die Länge der einzelnen FAT-Tabellen in Sektoren beschrieben (das Volume kann bis zu zwei Fette enthalten).

Der gültige Wertebereich für dieses Feld muss wie folgt lauten:

- Mindestens (Cluster count + 2) \* 2<sup>2</sup>/2<sup>bytespersectorshift</sup>aufgerundet auf die nächste ganze Zahl, um sicherzustellen, dass jedes Fat über ausreichend Speicherplatz verfügt, um alle Cluster im Cluster Heap zu beschreiben.

- Höchstens (clusterheapoffset-fatoffset)/-nummerierte werden auf die nächste ganze Zahl gerundet, um sicherzustellen, dass die Fette vor dem Cluster Heap vorhanden sind.

Dieses Feld kann einen Wert enthalten, der über der unteren Grenze hinausgeht (wie oben beschrieben), damit das zweite FAT, falls vorhanden, auch an den Merkmalen des zugrunde liegenden Speichermediums ausgerichtet werden kann. Der Inhalt des Speicherplatzes, der überschreitet, was das FAT selbst benötigt, ist ggf. nicht definiert.

#### <a name="318-clusterheapoffset-field"></a>3.1.8 clusterheapoffset-Feld

Im Feld clusterheapoffset muss der volumerelative sektoroffset des Cluster Heaps beschrieben werden. Dieses Feld ermöglicht Implementierungen, den Cluster Heap den Merkmalen des zugrunde liegenden Speichermediums auszurichten.

Der gültige Wertebereich für dieses Feld muss wie folgt lauten:

- Mindestens "fatoffset + fatlength"-Anzahlen \* , um die Sektoren zu berücksichtigen, die in allen vorherigen Regionen verwendet werden.

- Höchstens 2<sup>32</sup>-1 oder volumelength-(Cluster Count \* 2<sup>Sector sperclustershift</sup>), je nachdem, welche Berechnung kleiner ist

#### <a name="319-clustercount-field"></a>3.1.9 clustercount-Feld

Im Feld clustercount muss die Anzahl der Cluster, die der Cluster Heap enthält, beschrieben werden.

Der gültige Wert für dieses Feld ist der kleinere der folgenden Werte:

- (Volumelength-clusterheapoffset)/2<sup>sectorsperclustershift</sup>auf die nächste ganze Zahl gerundet. Dies ist genau die Anzahl der Cluster, die zwischen dem Anfang des Cluster Heaps und dem Ende des Volumes passen können.

- 2<sup>32</sup>-11, dies ist die maximale Anzahl von Clustern, die ein FAT beschreiben kann.

Der Wert des Felds "clustercount" bestimmt die Mindestgröße eines FAT. Um extrem große Fette zu vermeiden, können Implementierungen die Anzahl der Cluster im Cluster Heap steuern, indem Sie die Clustergröße (über das Feld sectorsperclustershift) erhöhen. Diese Spezifikation empfiehlt, dass nicht mehr als 2<sup>24</sup>-2-Cluster im Cluster Heap angezeigt werden. Allerdings müssen Implementierungen Volumes mit bis zu 2<sup>32</sup>-11-Clustern im Cluster Heap verarbeiten können.

#### <a name="3110-firstclusterofrootdirectory-field"></a>3.1.10 firstclusterofrootdirectory-Feld

Das Feld firstclusterofrootdirectory muss den Cluster Index des ersten Stammverzeichnis Clusters enthalten. Bei Implementierungen sollten Sie jeden Versuch durchführen, den ersten Cluster des Stamm Verzeichnisses im ersten nicht fehlerhaften Cluster zu platzieren, nachdem die Cluster die Zuordnungs Bitmap und die Tabellen-/Schreibtabelle genutzt haben.

Der gültige Wertebereich für dieses Feld muss wie folgt lauten:

- Mindestens 2, der Index des ersten Clusters im Cluster Heap

- Höchstens Cluster count + 1, der Index des letzten Clusters im Cluster Heap

#### <a name="3111-volumeserialnumber-field"></a>3.1.11 VolumeSerialNumber-Feld

Das VolumeSerialNumber-Feld muss eine eindeutige Seriennummer enthalten. Dies unterstützt Implementierungen bei der Unterscheidung zwischen verschiedenen exFAT-Volumes.
Implementierungen sollten die Seriennummer generieren, indem Sie das Datum und die Uhrzeit der Formatierung des exFAT-Volumes kombinieren. Der Mechanismus zum Kombinieren von Datum und Uhrzeit zum bilden einer Seriennummer ist Implementierungs spezifisch.

Alle möglichen Werte für dieses Feld sind gültig.

#### <a name="3112-filesystemrevision-field"></a>3.1.12 filesystemrevision-Feld

Im Feld filesystemrevision müssen die Haupt-und neben Versionsnummern der exFAT-Strukturen auf dem angegebenen Volume beschrieben werden.

Das höchst wertige Byte ist die Haupt Revisionsnummer, und das nieder wertige Byte ist die neben Versionsnummer. Wenn das hochwertige Byte z. b. den Wert 01h enthält und das nieder wertige Byte den Wert 05h enthält, wird im Feld filesystemrevision die Revisionsnummer 1,05 beschrieben.
Wenn das hochwertige Byte den Wert 0Ah enthält und das nieder wertige Byte den Wert 0Fh enthält, wird das Feld filesystemrevision entsprechend der Revisionsnummer 10,15 beschrieben.

Der gültige Wertebereich für dieses Feld muss wie folgt lauten:

- Mindestens 0 für das nieder wertige Byte und 1 für das höherwertige Byte

- Höchstens 99 für das nieder wertige Byte und 99 für das hochwertige Byte

Die Revisionsnummer von exFAT, die diese Spezifikation beschreibt, ist 1,00.
Implementierungen dieser Spezifikation sollten ein beliebiges exFAT-Volume mit der Haupt Revisionsnummer 1 einbinden und kein exFAT-Volume mit einer anderen Haupt Revisionsnummer einbinden. Implementierungen müssen die neben Versionsnummer berücksichtigen und keine Vorgänge ausführen oder Dateisystem Strukturen erstellen, die nicht in der entsprechenden Spezifikation der angegebenen neben Versionsnummer beschrieben werden.

#### <a name="3113-volumeflags-field"></a>3.1.13 Volumeflags-Feld

Das Feld Volumeflags muss Flags enthalten, die den Status verschiedener Dateisystem Strukturen auf dem exFAT-Volume angeben (siehe [Tabelle 5](#table-5-volumeflags-field-structure)).

Bei der Berechnung der entsprechenden Prüfsumme für den Haupt Start oder den Sicherungs Startbereich ist dieses Feld bei Implementierungen nicht enthalten. Beim Verweis auf den Sicherungs Startsektor müssen Implementierungen dieses Feld als veraltet behandeln.

<div id="table-5-volumeflags-field-structure" />

**Tabelle 5 volummeflags-Feldstruktur**

<table>
<thead>
<tr class="header">
<th><strong>Feldname</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>trate</strong></p></th>
<th><p><strong>Größe</strong></p>
<p><strong>Bohrer</strong></p></th>
<th><strong>Kommentare</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Activefat</td>
<td>0</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#31131-activefat-field">section 3.1.13.1</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>VolumeDirty</td>
<td>1</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#31132-volumedirty-field">section 3.1.13.2</a> definiert seinen Inhalt.</td>
</tr>
<tr class="odd">
<td>Mediafailure</td>
<td>2</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#31133-mediafailure-field">section 3.1.13.3</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>Clearto Zero</td>
<td>3</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#31134-cleartozero-field">section 3.1.13.4</a> definiert seinen Inhalt.</td>
</tr>
<tr class="odd">
<td>Reserviert</td>
<td>4</td>
<td>12</td>
<td>Dieses Feld ist obligatorisch, und die Inhalte sind reserviert.</td>
</tr>
</tbody>
</table>

##### <a name="31131-activefat-field"></a>3.1.13.1 activefat-Feld

Das activefat-Feld muss beschreiben, welche FAT-und Zuordnungs Bitmap aktiv ist (und Implementierungen verwenden), wie im folgenden dargestellt:

- 0 (null) bedeutet, dass die erste FAT-und erste Zuordnungs Bitmap aktiv ist.

- 1. Dies bedeutet, dass die zweite Zuordnungs Bitmap "FAT" und "Second" aktiv ist und nur möglich ist, wenn das Feld "Anzahlen" den Wert 2 enthält.

Bei Implementierungen müssen die inaktiven FAT-und Zuordnungs Bitmap als veraltet betrachtet werden. Nur texfat-kompatible Implementierungen müssen die Bitmaps für aktive FAT-und Zuordnungs Bitmaps wechseln (siehe [Abschnitt 7,1](#71-allocation-bitmap-directory-entry)).

##### <a name="31132-volumedirty-field"></a>3.1.13.2 VolumeDirty-Feld

Das Feld VolumeDirty muss wie folgt beschreiben, ob das Volume geändert wurde:

- 0, was bedeutet, dass sich das Volume wahrscheinlich in einem konsistenten Zustand befindet

- 1, was bedeutet, dass sich das Volume wahrscheinlich in einem inkonsistenten Zustand befindet

Bei Implementierungen sollte der Wert dieses Felds auf 1 festgelegt werden, wenn Inkonsistenzen von Dateisystem Metadaten auftreten, die nicht aufgelöst werden. Wenn bei der Bereitstellung eines Volumes der Wert dieses Felds 1 ist, wird der Wert dieses Felds von nur Implementierungen, die die Inkonsistenzen von Dateisystem Metadaten auflösen, möglicherweise auf 0 festgesetzt. Solche Implementierungen dürfen den Wert dieses Felds nur auf 0 löschen, nachdem sichergestellt wurde, dass sich das Dateisystem in einem konsistenten Zustand befindet.

Wenn bei der Bereitstellung eines Volumes der Wert für dieses Feld 0 ist, sollten Implementierungen dieses Feld vor dem Aktualisieren der Dateisystem Metadaten auf 1 festlegen und dieses Feld dann auf 0 (null) festlegen, ähnlich der empfohlenen Schreib Reihenfolge, die im [Abschnitt 8,1](#81-recommended-write-ordering)beschrieben wird.

##### <a name="31133-mediafailure-field"></a>3.1.13.3 mediafailure-Feld

Das Feld mediafailure muss wie folgt beschreiben, ob eine Implementierung ermittelte Medien Fehler erkannt hat:

- 0 (null) bedeutet, dass die hostingmedien keine Fehler gemeldet haben oder dass bekannte Fehler bereits in FAT als "Ungültige" Cluster aufgezeichnet wurden.

- 1. Dies bedeutet, dass die hostingmedien Fehler gemeldet haben (d. h. fehlgeschlagene Lese-oder Schreibvorgänge).

In einer Implementierung sollte dieses Feld in folgenden Bereichen auf 1 festgelegt werden:

1. Die hostingmedien haben keine Zugriffsversuche auf eine beliebige Region im Volume.

2. Die Implementierung hat ggf. die Zugriffs Algorithmen für den Zugriff ausgeschöpft.

Wenn bei der Bereitstellung eines Volumes der Wert dieses Felds 1 ist, kann der Wert dieses Felds durch Implementierungen, die das gesamte Volume nach Medien Fehlern überprüfen und alle Fehler aufzeichnen, als "Ungültige" Cluster im FAT (oder anderweitig durch das Beheben von Medien Fehlern) aufgezeichnet werden.

##### <a name="31134-cleartozero-field"></a>3.1.13.4 clearto Zero-Feld

Das clearto Zero-Feld weist in dieser Spezifikation keine signifikante Bedeutung auf.

Gültige Werte für dieses Feld sind:

- 0, das keine bestimmte Bedeutung hat

- 1. das bedeutet, dass Implementierungen dieses Feld vor der Änderung von Dateisystem Strukturen,-Verzeichnissen oder-Dateien auf 0 löschen müssen.

#### <a name="3114-bytespersectorshift-field"></a>3.1.14 bytespersectorshift-Feld

Das bytespersectorshift-Feld muss die Bytes pro Sektor beschreiben, ausgedrückt als log<sub>2</sub>(n), wobei N die Anzahl der Bytes pro Sektor ist. Beispielsweise ist der Wert dieses Felds für 512 Bytes pro Sektor 9.

Der gültige Wertebereich für dieses Feld muss wie folgt lauten:

- Mindestens 9 (Sektorgröße von 512 Bytes), dies ist der kleinste Sektor, der für ein exFAT-Volume möglich ist

- Höchstens 12 (Sektorgröße von 4096 Bytes), d. h. die Arbeitsspeicher Seitengröße von CPUs, die auf persönlichen Computern üblich sind

#### <a name="3115-sectorsperclustershift-field"></a>3.1.15 sectorsperclustershift-Feld

Im Feld sectorsperclustershift müssen die Sektoren pro Cluster als log<sub>2</sub>(n) bezeichnet werden, wobei N die Anzahl der Sektoren pro Cluster ist. Bei 8 Sektoren pro Cluster ist der Wert dieses Felds beispielsweise 3.

Der gültige Wertebereich für dieses Feld muss wie folgt lauten:

- Mindestens 0 (1 Sektor pro Cluster), bei dem es sich um den kleinsten Cluster handelt.

- Höchstens 25-BytesPerSector Shift ergibt eine Clustergröße von 32 MB.

#### <a name="3116-numberoffats-field"></a>3.1.16-Feld "Nummerier"

Im Feld "Feld" wird die Anzahl von Fetten und Zuordnungs Bitmaps beschrieben, die das Volume enthält.

Der gültige Wertebereich für dieses Feld muss wie folgt lauten:

- 1 gibt an, dass das Volume nur das erste FAT und das erste Zuordnungs Bitmap enthält.

- 2 gibt an, dass das Volume das erste FAT, das zweite FAT, das erste Zuordnungs Bitmap und das zweite Zuordnungs Bitmap enthält. Dieser Wert gilt nur für texfat-Volumes.

#### <a name="3117-driveselect-field"></a>3.1.17 driveselect-Feld

Das Feld driveselect muss die erweiterte Laufwerk Nummer "int 13h" enthalten, die das Bootstrapping von diesem Volume mithilfe des erweiterten int 13 h auf PCs unterstützt.

Alle möglichen Werte für dieses Feld sind gültig. Ähnliche Felder in früheren FAT-basierten Dateisystemen enthielten häufig den Wert 80H.

#### <a name="3118-percentinuse-field"></a>3.1.18 prozentualuse-Feld

Im Feld "prozentualuse" muss der Prozentsatz der Cluster im Cluster Heap beschrieben werden, die zugeordnet werden.

Der gültige Wertebereich für dieses Feld muss wie folgt lauten:

- Zwischen 0 und 100, einschließlich des Prozentsatzes zugewiesener Cluster im Cluster Heap, auf die nächste ganze Zahl gerundet.

- Genau FFH gibt an, dass der Prozentsatz der zugeordneten Cluster im Cluster Heap nicht verfügbar ist.

Implementierungen müssen den Wert dieses Felds ändern, damit Änderungen an der Zuordnung von Clustern im Cluster Heap widerspiegeln werden, oder Sie müssen in "FFH" geändert werden.

Bei der Berechnung der entsprechenden Prüfsumme für den Haupt Start oder den Sicherungs Startbereich ist dieses Feld bei Implementierungen nicht enthalten. Beim Verweis auf den Sicherungs Startsektor müssen Implementierungen dieses Feld als veraltet behandeln.

#### <a name="3119-bootcode-field"></a>3.1.19 bootcodefeld

Das Feld Bootcode muss Anweisungen für das Start Trap Ping enthalten.
Implementierungen können dieses Feld mit den erforderlichen CPU-Anweisungen für das Starten eines Computer Systems auffüllen. Implementierungen, die keine Bootstrapping-Anweisungen bereitstellen, müssen jedes Byte in diesem Feld mit F4h (der Stop-Anweisung für CPUs, die auf persönlichen Computern üblich sind) als Teil Ihres Formatierungs Vorgangs initialisieren.

#### <a name="3120-bootsignature-field"></a>3.1.20 bootsignature-Feld

Das bootsignature-Feld muss beschreiben, ob die Absicht eines bestimmten Sektors ein Startsektor sein soll oder nicht.

Der gültige Wert für dieses Feld ist AA55h. Alle anderen Werte in diesem Feld machen den jeweiligen Startsektor ungültig. Implementierungen sollten den Inhalt dieses Felds vor der Abhängigkeit von einem anderen Feld im jeweiligen Startsektor überprüfen.

### <a name="32-main-and-backup-extended-boot-sectors-sub-regions"></a>3,2 Haupt-und Sicherungs-Unterregionen für erweiterte Start Sektoren

Jeder Sektor der Hauptbereiche für erweiterte Starts hat dieselbe Struktur. jeder Sektor kann jedoch unterschiedliche Bootstrapping-Anweisungen enthalten (siehe Tabelle 6). Bei der Durchführung von Bootstrapping-Agents, wie z. b. die Bootstrapping-Anweisungen im Haupt Startsektor, Alternative BIOS-Implementierungen oder die Firmware eines eingebetteten Systems, können diese Sektoren geladen und die darin enthaltenen Anweisungen ausgeführt werden.

Der erweiterte Startsektor für Sicherungen ist eine Sicherung der wichtigsten erweiterten Start Sektoren und hat die gleiche Struktur (siehe [Tabelle 6](#table-6-extended-boot-sector-structure)).

Vor dem Ausführen der Anweisungen für die erweiterten Start Sektoren "Main" oder "Backup" sollten die Implementierungen ihren Inhalt überprüfen, indem Sie sicherstellen, dass das extendedbootsignature-Feld der einzelnen Sektoren den vorgeschriebenen Wert enthält.

Während der anfängliche Formatierungs Vorgang den Inhalt der erweiterten Start Sektoren "Main" und "Backup" initialisiert, können Implementierungen diese Sektoren aktualisieren (und auch Ihre entsprechende Start Prüfsumme aktualisieren), wenn dies erforderlich ist.

<div id="table-6-extended-boot-sector-structure" />

**Tabelle 6, Struktur des erweiterten Start Sektors**

<table>
<thead>
<tr class="header">
<th><strong>Feldname</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>Hobby</strong></p></th>
<th><p><strong>Größe</strong></p>
<p><strong>Satz</strong></p></th>
<th><strong>Kommentare</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Extendedbootcode</td>
<td>0</td>
<td>2<sup>BytesPerSector Shift</sup> – 4</td>
<td><p>Dieses Feld ist obligatorisch, und <a href="#321-extendedbootcode-field">Abschnitt 3.2.1</a> definiert seinen Inhalt.</p>
<p>Hinweis: die Haupt-und Sicherungs Start Sektoren enthalten das Feld bytespersectorshift.</p></td>
</tr>
<tr class="even">
<td>Extendedbootsignature</td>
<td>2<sup>BytesPerSector Shift</sup> – 4</td>
<td>4</td>
<td><p>Dieses Feld ist obligatorisch, und <a href="#322-extendedbootsignature-field">Abschnitt 3.2.2</a> definiert seinen Inhalt.</p>
<p>Hinweis: die Haupt-und Sicherungs Start Sektoren enthalten das Feld bytespersectorshift.</p></td>
</tr>
</tbody>
</table>

#### <a name="321-extendedbootcode-field"></a>3.2.1 extendedbootcode-Feld

Das Feld extendedbootcode muss eine Bootstrapping-Anweisung enthalten.
Implementierungen können dieses Feld mit den erforderlichen CPU-Anweisungen für das Starten eines Computer Systems auffüllen. Implementierungen, die keine Bootstrapping-Anweisungen bereitstellen, müssen jedes Byte in diesem Feld im Rahmen Ihres Formatierungs Vorgangs auf Werktagen initialisieren.

#### <a name="322-extendedbootsignature-field"></a>3.2.2 extendedbootsignature-Feld

Das Feld extendedbootsignature muss beschreiben, ob die Absicht eines bestimmten Sektors ein erweiterter Startsektor sein soll oder nicht.

Der gültige Wert für dieses Feld ist AA550000h. Durch einen anderen Wert in diesem Feld wird der entsprechende Haupt-oder Sicherungs Startsektor ungültig.
Implementierungen sollten den Inhalt dieses Felds vor der Abhängigkeit von einem anderen Feld im jeweiligen erweiterten Startsektor überprüfen.

### <a name="33-main-and-backup-oem-parameters-sub-regions"></a>3,3 Haupt-und Sicherungs-OEM-Parameter Unterregionen

Der Unterbereich der OEM-Hauptparameter enthält zehn Parameter Strukturen, die herstellerspezifische Informationen enthalten können (siehe [Tabelle 7](#table-7-oem-parameters-structure)). Jede der zehn Parameter Strukturen wird von der Vorlage für generische Parameter abgeleitet (siehe [Abschnitt 3.3.2](#332-generic-parameters-template)). Hersteller können Ihre eigenen benutzerdefinierten Parameter Strukturen aus der Vorlage für generische Parameter ableiten. Diese Spezifikation definiert zwei Parameter Strukturen: NULL-Parameter (siehe [Abschnitt 3.3.3](#333-null-parameters)) und Flash Parameter (siehe [Abschnitt 3.3.4](#334-flash-parameters)).

Bei den OEM-Sicherungs Parametern handelt es sich um eine Sicherung der OEM-Hauptparameter, die die gleiche Struktur aufweist (siehe [Tabelle 7](#table-7-oem-parameters-structure)).

Vor der Verwendung des Inhalts der OEM-Parameter "Main" oder "Backup" müssen Implementierungen ihren Inhalt überprüfen, indem Sie die jeweilige Start Prüfsumme überprüfen.

Hersteller sollten die Haupt-und Sicherungs-OEM-Parameter mit ihren eigenen benutzerdefinierten Parameter Strukturen (sofern vorhanden) und anderen Parameter Strukturen auffüllen. Nachfolgende Format Vorgänge müssen den Inhalt der OEM-Parameter "Main" und "Backup" beibehalten.

Implementierungen können die Haupt-und Sicherungs-OEM-Parameter nach Bedarf aktualisieren (und müssen außerdem ihre jeweilige Start Prüfsumme aktualisieren).

<div id="table-7-oem-parameters-structure" />

**Tabelle 7 OEM-Parameter Struktur**

<table>
<thead>
<tr class="header">
<th><strong>Feldname</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>Hobby</strong></p></th>
<th><p><strong>Größe</strong></p>
<p><strong>Satz</strong></p></th>
<th><strong>Kommentare</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Parameter [0]</td>
<td>0</td>
<td>48</td>
<td>Dieses Feld ist obligatorisch, und <a href="#331-parameters0--parameters9">section 3.3.1</a> definiert seinen Inhalt.</td>
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
<td>Parameter [9]</td>
<td>432</td>
<td>48</td>
<td>Dieses Feld ist obligatorisch, und <a href="#331-parameters0--parameters9">section 3.3.1</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>Reserviert</td>
<td>480</td>
<td>2<sup>BytesPerSector Shift</sup> – 480</td>
<td><p>Dieses Feld ist obligatorisch, und die Inhalte sind reserviert.</p>
<p>Hinweis: die Haupt-und Sicherungs Start Sektoren enthalten das Feld bytespersectorshift.</p></td>
</tr>
</tbody>
</table>

#### <a name="331-parameters0--parameters9"></a>3.3.1 Parameter \[ 0 \] ... Parameter \[ 9\]

Jedes Parameterfeld in diesem Array enthält eine Parameter Struktur, die von der Vorlage für generische Parameter abgeleitet wird (siehe [Abschnitt 3.3.2](#332-generic-parameters-template)).
Alle nicht verwendeten Parameter Felder müssen so beschrieben werden, dass Sie eine Struktur mit NULL-Parametern enthalten (siehe [Abschnitt 3.3.3](#333-null-parameters)).

#### <a name="332-generic-parameters-template"></a>3.3.2 Vorlage für generische Parameter

Die Vorlage für generische Parameter stellt die Basis Definition einer Parameter Struktur bereit (siehe [Tabelle 8](#table-8-generic-parameters-template)). Alle Parameter Strukturen werden von dieser Vorlage abgeleitet. Die Unterstützung für diese Vorlage für generische Parameter ist obligatorisch.

<div id="table-8-generic-parameters-template" />

**Tabelle 8, Vorlage für generische Parameter**

<table>
<thead>
<tr class="header">
<th><strong>Feldname</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>Hobby</strong></p></th>
<th><p><strong>Größe</strong></p>
<p><strong>Satz</strong></p></th>
<th><strong>Kommentare</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Parametersguid</td>
<td>0</td>
<td>16</td>
<td>Dieses Feld ist obligatorisch, und <a href="#3321-parametersguid-field">section 3.3.2.1</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>Customdefined</td>
<td>16</td>
<td>32</td>
<td>Dieses Feld ist obligatorisch, und die Strukturen, die von dieser Vorlage abgeleitet werden, definieren ihren Inhalt.</td>
</tr>
</tbody>
</table>

##### <a name="3321-parametersguid-field"></a>3.3.2.1 parametersguid-Feld

Im Feld parametersguid muss eine GUID beschrieben werden, die das Layout der restlichen Parameter Struktur bestimmt.

Alle möglichen Werte für dieses Feld sind gültig. Allerdings sollten Hersteller eine GUID verwenden, wie z. b. GuidGen.exe, um beim Ableiten von benutzerdefinierten Parameter Strukturen aus dieser Vorlage eine GUID auszuwählen.

#### <a name="333-null-parameters"></a>3.3.3 NULL-Parameter

Die Struktur der NULL-Parameter wird von der Vorlage für generische Parameter abgeleitet (siehe [Abschnitt 3.3.2](#332-generic-parameters-template)) und beschreibt ein nicht verwendetes Parameterfeld (siehe [Tabelle 9](#table-9-null-parameters-structure)). Beim Erstellen oder Aktualisieren der OEM-Parameter Struktur müssen Implementierungen nicht verwendete Parameter Felder mit der NULL-Parameter Struktur auffüllen. Beim Erstellen oder Aktualisieren der OEM-Parameter Struktur sollten Implementierungen NULL-Parameter Strukturen am Ende des Arrays konsolidieren und so alle anderen Parameter Strukturen am Anfang der OEM-Parameter Struktur belassen.

Die Unterstützung für die Struktur der NULL-Parameter ist obligatorisch.

<div id="table-9-null-parameters-structure" />

**Tabelle 9, Struktur der NULL-Parameter**

<table>
<thead>
<tr class="header">
<th><strong>Feldname</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>Hobby</strong></p></th>
<th><p><strong>Größe</strong></p>
<p><strong>Satz</strong></p></th>
<th><strong>Kommentare</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Parametersguid</td>
<td>0</td>
<td>16</td>
<td>Dieses Feld ist obligatorisch, und <a href="#3331-parametersguid-field">section 3.3.3.1</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>Reserviert</td>
<td>16</td>
<td>32</td>
<td>Dieses Feld ist obligatorisch, und die Inhalte sind reserviert.</td>
</tr>
</tbody>
</table>

##### <a name="3331-parametersguid-field"></a>3.3.3.1 parametersguid-Feld

Das Feld parametersguid muss der Definition entsprechen, die von der Vorlage für generische Parameter bereitgestellt wird (siehe [Abschnitt 3.3.2.1](#3321-parametersguid-field)).

Der gültige Wert für dieses Feld, in GUID-Notation, ist {00000000-0000-0000-0000-000000000000} .

#### <a name="334-flash-parameters"></a>3.3.4 Flash-Parameter

Die Flash-Parameter Struktur wird von der Vorlage für generische Parameter abgeleitet (siehe [Abschnitt 3.3.2](#332-generic-parameters-template)) und enthält Parameter für Flash Medien (siehe [Tabelle 10](#table-10-flash-parameters-structure)). Hersteller von Flash basierten Speichergeräten können ein Parameterfeld (vorzugsweise das \[ Feld Parameter 0 \] ) mit dieser Parameter Struktur auffüllen. Implementierungen können die Informationen in der Struktur der Flash Parameter verwenden, um die Zugriffs Vorgänge bei Lese-/Schreibvorgängen zu optimieren, sowie für die Ausrichtung von Dateisystem Strukturen, die die Formatierung der Medien festlegen.

Die Unterstützung für die Flash Parameter-Struktur ist optional.

<div id="table-10-flash-parameters-structure" />

**Tabelle 10, Struktur der Flash Parameter**

<table>
<thead>
<tr class="header">
<th><strong>Feldname</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>Hobby</strong></p></th>
<th><p><strong>Größe</strong></p>
<p><strong>Satz</strong></p></th>
<th><strong>Kommentare</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Parametersguid</td>
<td>0</td>
<td>16</td>
<td>Dieses Feld ist obligatorisch, und <a href="#3341-parametersguid-field">section 3.3.4.1</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>Eraseblocksize</td>
<td>16</td>
<td>4</td>
<td>Dieses Feld ist obligatorisch, und <a href="#3342-eraseblocksize-field">section 3.3.4.2</a> definiert seinen Inhalt.</td>
</tr>
<tr class="odd">
<td>PageSize</td>
<td>20</td>
<td>4</td>
<td>Dieses Feld ist obligatorisch, und <a href="#3343-pagesize-field">section 3.3.4.3</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>Sparesectors</td>
<td>24</td>
<td>4</td>
<td>Dieses Feld ist obligatorisch, und <a href="#3344-sparesectors-field">section 3.3.4.4</a> definiert seinen Inhalt.</td>
</tr>
<tr class="odd">
<td>Randomaccesstime</td>
<td>28</td>
<td>4</td>
<td>Dieses Feld ist obligatorisch, und <a href="#3345-randomaccesstime-field">section 3.3.4.5</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>Programmmingtime</td>
<td>32</td>
<td>4</td>
<td>Dieses Feld ist obligatorisch, und <a href="#3346-programmingtime-field">section 3.3.4.6</a> definiert seinen Inhalt.</td>
</tr>
<tr class="odd">
<td>Lektüre</td>
<td>36</td>
<td>4</td>
<td>Dieses Feld ist obligatorisch, und <a href="#3347-readcycle-field">section 3.3.4.7</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>Schreibvorgang</td>
<td>40</td>
<td>4</td>
<td>Dieses Feld ist obligatorisch, und <a href="#3348-writecycle-field">section 3.3.4.8</a> definiert seinen Inhalt.</td>
</tr>
<tr class="odd">
<td>Reserviert</td>
<td>44</td>
<td>4</td>
<td>Dieses Feld ist obligatorisch, und die Inhalte sind reserviert.</td>
</tr>
</tbody>
</table>

Alle möglichen Werte für alle Flash Parameter Felder, mit Ausnahme des Felds parametersguid, sind gültig. Der Wert 0 gibt jedoch an, dass das Feld tatsächlich bedeutungslos ist (Implementierungen müssen das angegebene Feld ignorieren).

##### <a name="3341-parametersguid-field"></a>3.3.4.1 parametersguid-Feld

Das Feld parametersguid muss der in der Vorlage für generische Parameter bereitgestellten Definition entsprechen (siehe [Abschnitt 3.3.2.1](#3321-parametersguid-field)).

Der gültige Wert für dieses Feld in der GUID-Notation ist {0a0c7e46-3399-4021-90c8-fa6d389c4ba2}.

##### <a name="3342-eraseblocksize-field"></a>3.3.4.2 eraseblocksize-Feld

Im Feld eraseblocksize muss die Größe des Lösch Blocks des Flash Mediums in Bytes beschrieben werden.

##### <a name="3343-pagesize-field"></a>3.3.4.3 PageSize-Feld

Im Feld PageSize muss die Größe der Seite des Flash Mediums in Bytes beschrieben werden.

##### <a name="3344-sparesectors-field"></a>3.3.4.4 sparesectors-Feld

Im Feld sparesectors muss die Anzahl der Sektoren beschrieben werden, die das Flash Medium für seine internen Einfügevorgänge verfügbar ist.

##### <a name="3345-randomaccesstime-field"></a>3.3.4.5 randomaccesstime-Feld

Im Feld randomaccesstime muss die durchschnittliche Zeit für den zufälligen Zugriff des Flash Mediums in Nanosekunden beschrieben werden.

##### <a name="3346-programmingtime-field"></a>3.3.4.6 Program mingtime-Feld

Im Feld programmmingtime muss die durchschnittliche Programmierzeit des Flash Mediums in Nanosekunden beschrieben werden.

##### <a name="3347-readcycle-field"></a>3.3.4.7-Feld "Read Cycle"

Im Feld "Read Cycle" muss die durchschnittliche Lese Zyklen des Flash Mediums in Nanosekunden beschrieben werden.

##### <a name="3348-writecycle-field"></a>3.3.4.8-Feld "Beschreib tecycle"

Das Feld "Write Cycle" muss die durchschnittliche Schreibzeit in Nanosekunden beschreiben.

### <a name="34-main-and-backup-boot-checksum-sub-regions"></a>3,4 Haupt-und Sicherungs Start Prüfsummen-Unterregionen

Die Haupt-und Sicherungs Start Prüfsummen enthalten jeweils ein sich wiederholendes Muster der vier-Byte-Prüfsumme für den Inhalt aller anderen Teilregionen in den jeweiligen Start Regionen. Die Berechnung der Prüfsumme darf nicht die Felder "Volumeflags" und "prozentualuse" in ihrem jeweiligen Startsektor enthalten (siehe [Abbildung 1](#figure-1-boot-checksum-computation)). Das sich wiederholende Muster der vier-Byte-Prüfsumme füllt den jeweiligen Unterbereich der Start Prüf Summe von Anfang bis zum Ende der Unterregion.

Vor der Verwendung des Inhalts der anderen Teilregionen in den Haupt-oder Sicherungs Start Regionen müssen Implementierungen ihren Inhalt überprüfen, indem Sie die jeweilige Start Prüfsumme überprüfen.

Während der anfängliche Formatierungs Vorgang die Haupt-und Sicherungs Start Prüfsummen mit dem sich wiederholenden Prüfsummen Muster auffüllen, müssen Implementierungen diese Sektoren aktualisieren, wenn sich die Inhalte der anderen Sektoren in den jeweiligen Start Regionen ändern.

<div id="figure-1-boot-checksum-computation" />

**Abbildung 1 Start Prüfsummenberechnung**

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

## <a name="4-file-allocation-table-region"></a>4 Bereich der Datei Zuordnungs Tabelle

Die FAT-Region (File Allocation Table, Datei Zuordnungs Tabelle) kann bis zu zwei Fette enthalten, eine in der ersten FAT-Unterregion und eine andere in der zweiten FAT-Unterregion.
Im Feld "Anzahlen" wird beschrieben, wie viele Fette in diesem Bereich enthalten sind. Die gültigen Werte für das Feld "numoffats" lauten 1 und 2. Daher enthält der erste FAT-Teilbereich immer ein FAT. Wenn das Feld "numoffats" zwei ist, enthält der zweite FAT-Unterbereich auch ein FAT.

Das Feld activefat im Feld Volumeflags beschreibt, welches FAT aktiv ist. Nur das Feld Volumeflags im Haupt Startsektor ist aktuell.
Implementierungen müssen das FAT behandeln, das nicht als veraltet aktiv ist. Die Verwendung des inaktiven FAT und der Wechsel zwischen den Fetten ist Implementierungs spezifisch.

### <a name="41-first-and-second-fat-sub-regions"></a>4,1 erste und zweite FAT-Unterbereiche

Ein FAT muss Cluster Ketten im Cluster Heap beschreiben (siehe [Tabelle 11](#table-11-file-allocation-table-structure)).
Eine Cluster Kette ist eine Reihe von Clustern, die Speicherplatz zum Aufzeichnen der Inhalte von Dateien, Verzeichnissen und anderen Dateisystem Strukturen bereitstellt. Ein FAT stellt eine Cluster Kette als einzeln verknüpfte Liste von Cluster Indizes dar. Mit Ausnahme der ersten beiden Einträge stellt jeder Eintrag in einem FAT genau einen Cluster dar.

<div id="table-11-file-allocation-table-structure" />

**Tabelle 11, Struktur der Datei Zuordnungs Tabelle**

<table>
<thead>
<tr class="header">
<th><strong>Feldname</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>Hobby</strong></p></th>
<th><p><strong>Größe</strong></p>
<p><strong>Satz</strong></p></th>
<th><strong>Kommentare</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Fatentry [0]</td>
<td>0</td>
<td>4</td>
<td>Dieses Feld ist obligatorisch, und <a href="#412-fatentry1-field">Abschnitt 4.1.2</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>Fatentry [1]</td>
<td>4</td>
<td>4</td>
<td>Dieses Feld ist obligatorisch, und <a href="#412-fatentry1-field">Abschnitt 4.1.2</a> definiert seinen Inhalt.</td>
</tr>
<tr class="odd">
<td>Fatentry [2]</td>
<td>8</td>
<td>4</td>
<td>Dieses Feld ist obligatorisch, und <a href="#413-fatentry2--fatentryclustercount1-fields">Abschnitt 4.1.3</a> definiert seinen Inhalt.</td>
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
<td>Fatentry [Cluster count + 1]</td>
<td>(Cluster count + 1) * 4</td>
<td>4</td>
<td><p>Dieses Feld ist obligatorisch, und <a href="#413-fatentry2--fatentryclustercount1-fields">Abschnitt 4.1.3</a> definiert seinen Inhalt.</p>
<p>"Clustercount + 1" darf FFFFFFF6h nie überschreiten.</p>
<p>Hinweis: die Haupt-und Sicherungs Start Sektoren enthalten beide das Feld "clustercount".</p></td>
</tr>
<tr class="even">
<td>Excess Space</td>
<td>(Cluster count + 2) * 4</td>
<td>(Fatlength * 2<sup>BytesPerSector Shift</sup>) – ((Cluster count + 2) * 4)</td>
<td><p>Dieses Feld ist obligatorisch, und sein Inhalt ist ggf. nicht definiert.</p>
<p>Hinweis: die Haupt-und Sicherungs Start Sektoren enthalten beide Felder "clustercount", "fatlength" und "bytespersectorshift".</p></td>
</tr>
</tbody>
</table>

#### <a name="411-fatentry0-field"></a>4.1.1 fatentry \[ 0- \] Feld

Das Feld fatentry \[ 0 muss \] den Medientyp im ersten Byte (das niedrigste Reihenfolge Byte) beschreiben und in den restlichen drei Bytes die Zeichenfolge FFH enthalten.

Der Medientyp (das erste Byte) sollte "F8h" lauten.

#### <a name="412-fatentry1-field"></a>4.1.2 fatentry \[ 1- \] Feld

Das Feld "fatentry \[ 1" \] ist nur aufgrund der Verlaufs Rangfolge vorhanden und beschreibt nichts von Interesse.

Der gültige Wert für dieses Feld ist ffffffffh. Implementierungen müssen dieses Feld mit dem vorgeschriebenen Wert initialisieren und sollten dieses Feld nicht für einen beliebigen Zweck verwenden. Bei Implementierungen sollte dieses Feld nicht interpretiert werden, und der Inhalt muss über Vorgänge hinweg beibehalten werden, die umgebende Felder ändern.

#### <a name="413-fatentry2--fatentryclustercount1-fields"></a>4.1.3 fatentry \[ 2 \] ... "Fatentry \[ clustercount + 1"- \] Felder

Jedes Feld "fatentry" in diesem Array muss einen Cluster im Cluster Heap darstellen. Fatentry \[ 2 \] steht für den ersten Cluster im Cluster Heap, und fatentry \[ clustercount + 1 \] stellt den letzten Cluster im Cluster Heap dar.

Der gültige Wertebereich für diese Felder muss wie folgt lauten:

- Zwischen 2 und clustercount + 1, einschließlich, das auf den nächsten fatentry in der angegebenen Cluster Kette zeigt. der angegebene fatentry darf nicht auf einen fatentry zeigen, der in der angegebenen Cluster Kette vorangestellt ist.

- Genau FFFFFFF7h, wodurch der angegebene Cluster von fatentry als "schlecht" markiert wird.

- Genau "ffffffffh", mit dem der angegebene Cluster "fatentry" als letzter Cluster einer Cluster Kette gekennzeichnet wird. Dies ist der einzige gültige Wert für den letzten fatentry einer angegebenen Cluster Kette.

## <a name="5-data-region"></a>5 Datenbereich

Der Datenbereich enthält den Cluster Heap, der verwalteten Speicherplatz für Dateisystem Strukturen, Verzeichnisse und Dateien bereitstellt.

### <a name="51-cluster-heap-sub-region"></a>5,1 Cluster Heap-Unterregion

Die Struktur des Cluster Heaps ist sehr einfach (siehe [Tabelle 12](#table-12-cluster-heap-structure)); jede aufeinander folgende Reihe von Sektoren beschreibt einen Cluster, wie das Feld sectorsperclustershift definiert. Wichtig ist, dass der erste Cluster des Cluster Heaps den Index Two hat, der direkt dem Index von fatentry \[ 2 entspricht \] .

In einem exFAT-Volume verwaltet eine Zuordnungs Bitmap (siehe [Abschnitt 7.1.5](#715-allocation-bitmap)) den Datensatz des Zuordnungs Zustands aller Cluster. Dies ist ein bedeutender Unterschied zu den Vorgängern von exFAT (FAT12, FAT16 und FAT32), bei denen ein FAT einen Datensatz des Zuordnungs Zustands aller Cluster im Cluster Heap verwaltet hat.

<div id="table-12-cluster-heap-structure" />

**Tabelle 12 Cluster Heap Struktur**

<table>
<thead>
<tr class="header">
<th><strong>Feldname</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>Teil</strong></p></th>
<th><p><strong>Größe</strong></p>
<p><strong>Sektors</strong></p></th>
<th><strong>Kommentare</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Cluster [2]</td>
<td>Clusterheapoffset</td>
<td>2<sup>Sector sperclustershift</sup></td>
<td><p>Dieses Feld ist obligatorisch, und <a href="#511-cluster2--clusterclustercount1-fields">section 5.1.1</a> definiert seinen Inhalt.</p>
<p>Hinweis: die Haupt-und Sicherungs Start Sektoren enthalten beide Felder "clusterheapoffset" und "sectorsperclustershift".</p></td>
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
<td>Cluster [Cluster count + 1]</td>
<td>Clusterheapoffset + (Cluster count – 1) * 2<sup>Sector sperclustershift</sup></td>
<td>2<sup>Sector sperclustershift</sup></td>
<td><p>Dieses Feld ist obligatorisch, und <a href="#511-cluster2--clusterclustercount1-fields">section 5.1.1</a> definiert seinen Inhalt.</p>
<p>Hinweis: die Haupt-und Sicherungs Start Sektoren enthalten beide die Felder "clustercount", "clusterheapoffset" und "sectorsperclustershift".</p></td>
</tr>
</tbody>
</table>

#### <a name="511-cluster2--clusterclustercount1-fields"></a>5.1.1 Cluster \[ 2 \] ... Cluster Cluster \[ count + 1 \] Felder

Jedes Cluster Feld in diesem Array ist eine Reihe von zusammenhängenden Sektoren, deren Größe durch das Feld "sectorsperclustershift" definiert wird.

## <a name="6-directory-structure"></a>6 Verzeichnisstruktur

Das exFAT-Dateisystem verwendet einen Verzeichnisstruktur Ansatz, um die Dateisystem Strukturen und-Dateien zu verwalten, die im Cluster Heap vorhanden sind. Verzeichnisse haben eine 1: n-Beziehung zwischen übergeordnetem und untergeordnetem Element in der Verzeichnisstruktur.

Das Verzeichnis, auf das das Feld firstclusterofrootdirectory verweist, ist das Stammverzeichnis der Verzeichnisstruktur. Alle anderen Verzeichnisse werden auf einzeln verknüpfte Weise aus dem Stammverzeichnis abgeleitet.

Jedes Verzeichnis besteht aus einer Reihe von Verzeichnis Einträgen (siehe [Tabelle 13](#table-13-directory-structure)).

Ein oder mehrere Verzeichniseinträge werden in einem Verzeichniseintrags Satz zusammengefasst, der relevante Informationen beschreibt, z. b. eine Dateisystem Struktur, ein Unterverzeichnis oder eine Datei.

<div id="table-13-directory-structure" />

**Tabelle 13 Verzeichnisstruktur**

<table>
<thead>
<tr class="header">
<th><strong>Feldname</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>Hobby</strong></p></th>
<th><p><strong>Größe</strong></p>
<p><strong>Hobby</strong></p></th>
<th><strong>Kommentare</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Directoriyentry [0]</td>
<td>0</td>
<td>32</td>
<td>Dieses Feld ist obligatorisch, und <a href="#61-directoryentry0--directoryentryn--1">Abschnitt 6,1</a> definiert seinen Inhalt.</td>
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
<td>Director Entry [N – 1]</td>
<td>(N – 1) * 32</td>
<td>32</td>
<td><p>Dieses Feld ist obligatorisch, und <a href="#61-directoryentry0--directoryentryn--1">Abschnitt 6,1</a> definiert seinen Inhalt.</p>
<p>N, die Anzahl von DirectoryEntry-Feldern, ist die Größe (in Bytes) der Cluster Kette, die das angegebene Verzeichnis enthält, dividiert durch die Größe eines DirectoryEntry-Felds (32 Bytes).</p></td>
</tr>
</tbody>
</table>

### <a name="61-directoryentry0--directoryentryn--1"></a>6,1 Director Entry \[ 0 \] ... Director Entry \[ N--1\]

Jedes Feld "DirectoryEntry" in diesem Array wird von der generischen DirectoryEntry-Vorlage abgeleitet (siehe [Abschnitt 6,2](#62-generic-directoryentry-template)).

### <a name="62-generic-directoryentry-template"></a>6,2 generische Director Entry-Vorlage

Die generische Director Entry-Vorlage stellt die Basis Definition für Verzeichniseinträge bereit (siehe [Tabelle 14](#table-14-generic-directoryentry-template)). Alle Verzeichniseintrags Strukturen werden von dieser Vorlage abgeleitet, und nur von Microsoft definierte Verzeichniseintrags Strukturen sind gültig (exFAT hat keine bereit Stellungen für Hersteller definierte Verzeichniseintrags Strukturen, außer wie im [Abschnitt 7,8](#78-vendor-extension-directory-entry) und [Abschnitt 7,9](#79-vendor-allocation-directory-entry)definiert). Die Möglichkeit, die generische Director Entry-Vorlage zu interpretieren, ist obligatorisch.

<div id="table-14-generic-directoryentry-template" />

**Tabelle 14 generische Director Entry-Vorlage**

<table>
<thead>
<tr class="header">
<th><strong>Feldname</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>Hobby</strong></p></th>
<th><p><strong>Größe</strong></p>
<p><strong>Hobby</strong></p></th>
<th><strong>Kommentare</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EntryType</td>
<td>0</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#621-entrytype-field">section 6.2.1</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>Customdefined</td>
<td>1</td>
<td>19</td>
<td>Dieses Feld ist obligatorisch, und Strukturen, die von dieser Vorlage abgeleitet werden, können ihren Inhalt definieren.</td>
</tr>
<tr class="odd">
<td>Firstcluster</td>
<td>20</td>
<td>4</td>
<td>Dieses Feld ist obligatorisch, und <a href="#622-firstcluster-field">section 6.2.2</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>DataLength</td>
<td>24</td>
<td>8</td>
<td>Dieses Feld ist obligatorisch, und <a href="#623-datalength-field">section 6.2.3</a> definiert seinen Inhalt.</td>
</tr>
</tbody>
</table>

#### <a name="621-entrytype-field"></a>6.2.1 EntryType-Feld

Das EntryType-Feld weist drei Verwendungs Modi auf, die der Wert des Felds definiert (siehe Liste unten).

- 00H, ein Ende der Verzeichnis Markierung, und die folgenden Bedingungen gelten:

  - Alle anderen Felder im angegebenen DirectoryEntry sind tatsächlich reserviert.

  - Alle nachfolgenden Verzeichniseinträge im angegebenen Verzeichnis sind auch Ende der Verzeichnis Marker.

  - Markerenmarkermarker sind nur außerhalb der Verzeichniseintrags Sätze gültig.

  - Implementierungen können das Ende der Verzeichnis Marker nach Bedarf überschreiben.

- Zwischen 01h und 7Fh, was ein nicht verwendeter-Verzeichniseintrags Marker ist und die folgenden Bedingungen zutreffen:

  - Alle anderen Felder im angegebenen DirectoryEntry sind tatsächlich nicht definiert.

  - Nicht verwendete Verzeichniseinträge sind nur außerhalb der Verzeichniseintrags Sätze gültig.

  - Implementierungen können nicht verwendete Verzeichniseinträge bei Bedarf überschreiben.

  - Dieser Wertebereich entspricht dem Feld "InUse" (siehe [Abschnitt 6.2.1.4](#6214-inuse-field)), der den Wert 0 (null) enthält.

- Zwischen 81h und FFH, bei dem es sich um einen regulären Verzeichniseintrag handelt und die folgenden Bedingungen zutreffen:

  - Der Inhalt des Felds EntryType (siehe [Tabelle 15](#table-15-generic-entrytype-field-structure)) bestimmt das Layout der restlichen DirectoryEntry-Struktur.

  - Dieser Wertebereich und nur dieser Wertebereich sind innerhalb eines Verzeichniseintrags Satzes gültig.

  - Dieser Wertebereich entspricht direkt dem Feld "InUse" (siehe [Abschnitt 6.2.1.4](#6214-inuse-field)), der den Wert 1 enthält.

Um zu verhindern, dass Änderungen am InUse-Feld (siehe [Abschnitt 6.2.1.4](#6214-inuse-field)) irrtümlich zu einem Ende der Verzeichnis Markierung geführt werden, ist der Wert 80H ungültig.

<div id="table-15-generic-entrytype-field-structure" />

**Tabelle 15 generische EntryType-Feldstruktur**

<table>
<thead>
<tr class="header">
<th><strong>Feldname</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>trate</strong></p></th>
<th><p><strong>Größe</strong></p>
<p><strong>Bohrer</strong></p></th>
<th><strong>Kommentare</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>TypeCode</td>
<td>0</td>
<td>5</td>
<td>Dieses Feld ist obligatorisch, und <a href="#6211-typecode-field">section 6.2.1.1</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>Typeimportance</td>
<td>5</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und Abschnitts <a href="#6212-typeimportance-field">Abschnitt 6.2.1.2</a> definiert seinen Inhalt.</td>
</tr>
<tr class="odd">
<td>Typecategory</td>
<td>6</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#6213-typecategory-field">section 6.2.1.3</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>InUse</td>
<td>7</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#6214-inuse-field">section 6.2.1.4</a> definiert seinen Inhalt.</td>
</tr>
</tbody>
</table>

##### <a name="6211-typecode-field"></a>6.2.1.1 TypeCode-Feld

Das Feld TypeCode beschreibt den spezifischen Typ des angegebenen Verzeichniseintrags teilweise. In diesem Feld sowie in den Feldern typeimportance und typecategory (siehe [Abschnitt 6.2.1.2](#6212-typeimportance-field) und [section 6.2.1.3](#6213-typecategory-field)) wird der Typ des angegebenen Verzeichniseintrags eindeutig identifiziert.

Alle möglichen Werte dieses Felds sind gültig, es sei denn, die Felder typeimportance und typecategory enthalten jeweils den Wert 0. in diesem Fall ist der Wert 0 für dieses Feld ungültig.

##### <a name="6212-typeimportance-field"></a>6.2.1.2 typeimportance-Feld

Im Feld typeimportance muss die Wichtigkeit des angegebenen Verzeichniseintrags beschrieben werden.

Die gültigen Werte für dieses Feld müssen lauten:

- 0 bedeutet, dass der angegebene Verzeichniseintrag kritisch ist (siehe [Abschnitt 6.3.1.2.1](#63121-critical-primary-directory-entries) und [Abschnitt 6.4.1.2.1](#64121-critical-secondary-directory-entries) für wichtige primäre und kritische sekundäre Verzeichniseinträge).

- 1. Dies bedeutet, dass der angegebene Verzeichniseintrag nicht gutartig ist (Weitere Informationen finden Sie im [Abschnitt 6.3.1.2.2](#63122-benign-primary-directory-entries) und [Abschnitt 6.4.1.2.2](#64122-benign-secondary-directory-entries) für nicht gutartige primäre und gutartige sekundäre Verzeichniseinträge).

##### <a name="6213-typecategory-field"></a>6.2.1.3 typecategory-Feld

Im Feld typecategory muss die Kategorie des angegebenen Verzeichniseintrags beschrieben werden.

Die gültigen Werte für dieses Feld müssen lauten:

- 0 (null) bedeutet, dass der angegebene Verzeichniseintrag primär ist (siehe [Abschnitt 6,3](#63-generic-primary-directoryentry-template)).

- 1. Dies bedeutet, dass der angegebene Verzeichniseintrag sekundär ist (siehe [Abschnitt 6,4](#64-generic-secondary-directoryentry-template)).

##### <a name="6214-inuse-field"></a>6.2.1.4 InUse-Feld

Das Feld "InUse" muss beschreiben, ob der angegebene Verzeichniseintrag verwendet wird.

Die gültigen Werte für dieses Feld müssen lauten:

- 0 (null) bedeutet, dass der angegebene Verzeichniseintrag nicht verwendet wird. Dies bedeutet, dass die angegebene Struktur tatsächlich ein nicht verwendeter Verzeichniseintrag ist.

- 1. Dies bedeutet, dass der angegebene Verzeichniseintrag verwendet wird. Dies bedeutet, dass die angegebene Struktur ein regulärer Verzeichniseintrag ist.

#### <a name="622-firstcluster-field"></a>6.2.2 firstcluster-Feld

Das Feld "firstcluster" muss den Index des ersten Clusters einer Zuordnung in dem Cluster Heap enthalten, der dem angegebenen Verzeichniseintrag zugeordnet ist.

Der gültige Wertebereich für dieses Feld muss wie folgt lauten:

- Genau 0, was bedeutet, dass keine Cluster Zuordnung vorhanden ist

- Zwischen 2 und clustercount + 1, dem Bereich gültiger Cluster Indizes.

Strukturen, die von dieser Vorlage abgeleitet werden, können die Felder firstcluster und DATALENGTH neu definieren, wenn eine Cluster Zuordnung nicht mit der abgeleiteten Struktur kompatibel ist.

#### <a name="623-datalength-field"></a>6.2.3 DATALENGTH-Feld

Im Feld DATALENGTH wird die Größe (in Bytes) der Daten beschrieben, die die zugeordnete Cluster Zuordnung enthält.

Der gültige Wertebereich für dieses Feld lautet:

- Mindestens 0; Wenn das Feld firstcluster den Wert 0 (null) enthält, ist der einzige gültige Wert für dieses Feld 0.

- Höchstens Cluster Count \* 2<sup>Sector sperclustershift</sup> \* 2<sup>BytesPerSector Shift</sup>

Strukturen, die von dieser Vorlage abgeleitet werden, können die Felder firstcluster und DATALENGTH neu definieren, wenn eine Cluster Zuordnung für die abgeleitete Struktur nicht möglich ist.

### <a name="63-generic-primary-directoryentry-template"></a>6,3 generische primäre directentry-Vorlage

Der erste Verzeichniseintrag in einem Verzeichniseintrags Satz muss ein primärer Verzeichniseintrag sein. Alle nachfolgenden Verzeichniseinträge (sofern vorhanden) im Verzeichniseintrags Satz sind sekundäre Verzeichniseinträge (siehe [Abschnitt 6,4](#64-generic-secondary-directoryentry-template)).

Die Möglichkeit zur Interpretation der generischen primären directentry-Vorlage ist obligatorisch.

Alle primären Verzeichniseintrags Strukturen werden von der generischen primären directentry-Vorlage abgeleitet (siehe [Tabelle 16](#table-16-generic-primary-directoryentry-template)), die von der generischen Directoren Entry-Vorlage abgeleitet ist (siehe [Abschnitt 6,2](#62-generic-directoryentry-template)).

<div id="table-16-generic-primary-directoryentry-template" />

**Tabelle 16 generic Primary Director Entry-Vorlage**

<table>
<thead>
<tr class="header">
<th><strong>Feldname</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>Hobby</strong></p></th>
<th><p><strong>Größe</strong></p>
<p><strong>Hobby</strong></p></th>
<th><strong>Kommentare</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EntryType</td>
<td>0</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#631-entrytype-field">section 6.3.1</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>Secondarycount</td>
<td>1</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#632-secondarycount-field">section 6.3.2</a> definiert seinen Inhalt.</td>
</tr>
<tr class="odd">
<td>SetChecksum</td>
<td>2</td>
<td>2</td>
<td>Dieses Feld ist obligatorisch, und <a href="#633-setchecksum-field">section 6.3.3</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>Generalprimaryflags</td>
<td>4</td>
<td>2</td>
<td>Dieses Feld ist obligatorisch, und <a href="#634-generalprimaryflags-field">section 6.3.4</a> definiert seinen Inhalt.</td>
</tr>
<tr class="odd">
<td>Customdefined</td>
<td>6</td>
<td>14</td>
<td>Dieses Feld ist obligatorisch, und Strukturen, die von dieser Vorlage abgeleitet werden, definieren ihren Inhalt.</td>
</tr>
<tr class="even">
<td>Firstcluster</td>
<td>20</td>
<td>4</td>
<td>Dieses Feld ist obligatorisch, und <a href="#635-firstcluster-field">section 6.3.5</a> definiert seinen Inhalt.</td>
</tr>
<tr class="odd">
<td>DataLength</td>
<td>24</td>
<td>8</td>
<td>Dieses Feld ist obligatorisch, und <a href="#636-datalength-field">section 6.3.6</a> definiert seinen Inhalt.</td>
</tr>
</tbody>
</table>

#### <a name="631-entrytype-field"></a>6.3.1 EntryType-Feld

Das EntryType-Feld muss der Definition entsprechen, die in der generischen DirectoryEntry-Vorlage bereitgestellt wird (siehe [Abschnitt 6.2.1](#621-entrytype-field)).

##### <a name="6311-typecode-field"></a>6.3.1.1 TypeCode-Feld

Das TypeCode-Feld muss der Definition entsprechen, die in der generischen DirectoryEntry-Vorlage bereitgestellt wird (siehe [Abschnitt 6.2.1.1](#6211-typecode-field)).

##### <a name="6312-typeimportance-field"></a>6.3.1.2 typeimportance-Feld

Das typeimportance-Feld muss der Definition entsprechen, die in der generischen DirectoryEntry-Vorlage bereitgestellt wird (siehe [Abschnitt 6.2.1.2](#6212-typeimportance-field)).

###### <a name="63121-critical-primary-directory-entries"></a>6.3.1.2.1 wichtige primäre Verzeichniseinträge

Wichtige primäre Verzeichniseinträge enthalten Informationen, die für die ordnungsgemäße Verwaltung eines exFAT-Volumes wichtig sind. Nur das Stammverzeichnis enthält wichtige primäre Verzeichniseinträge (Datei Verzeichniseinträge stellen eine Ausnahme dar, siehe [Abschnitt 7,4](#74-file-directory-entry)).

Die Definition kritischer primär Verzeichniseinträge korreliert mit der wichtigen exFAT-Revisionsnummer. Implementierungen müssen alle kritischen primär Verzeichniseinträge unterstützen und nur die kritischen primären Verzeichniseintrags Strukturen aufzeichnen, die von dieser Spezifikation definiert werden.

###### <a name="63122-benign-primary-directory-entries"></a>6.3.1.2.2 nicht gutartige primäre Verzeichniseinträge

Nicht gutartige primäre Verzeichniseinträge enthalten zusätzliche Informationen, die für die Verwaltung eines exFAT-Volumes nützlich sein können. Alle Verzeichnisse können nicht genügend primäre Verzeichniseinträge enthalten.

Die Definition von nicht gutartigen primär Verzeichnis Einträgen korreliert mit der kleineren exFAT-Revisionsnummer. Unterstützung für jeden nicht wohlwollenden primär Verzeichniseintrag diese Spezifikation bzw. jede nachfolgende Spezifikation definiert, ist optional. Ein nicht erkannter, nicht erkannter primär Verzeichniseintrag rendert den gesamten Verzeichniseintrags Satz als nicht erkannt (über die Definition der entsprechenden Verzeichniseintrags Vorlagen hinaus).

##### <a name="6313-typecategory-field"></a>6.3.1.3 typecategory-Feld

Das Feld typecategory muss der Definition entsprechen, die in der generischen DirectoryEntry-Vorlage bereitgestellt wird (siehe [Abschnitt 6.2.1.3](#6213-typecategory-field)).

Für diese Vorlage sollte der gültige Wert für dieses Feld "0" lauten.

##### <a name="6314-inuse-field"></a>6.3.1.4 InUse-Feld

Das Feld "InUse" muss der Definition entsprechen, die in der generischen DirectoryEntry-Vorlage angegeben ist (siehe [Abschnitt 6.2.1.4](#6214-inuse-field)).

#### <a name="632-secondarycount-field"></a>6.3.2 secondarycount-Feld

Im Feld secondarycount muss die Anzahl der Einträge des sekundären Verzeichnisses beschrieben werden, die direkt dem angegebenen primären Verzeichniseintrag folgen. Diese sekundären Verzeichniseinträge enthalten zusammen mit dem angegebenen primär Verzeichniseintrag den Verzeichniseintrags Satz.

Der gültige Wertebereich für dieses Feld muss wie folgt lauten:

- Mindestens 0. Dies bedeutet, dass dieser primäre Verzeichniseintrag der einzige Eintrag im Verzeichniseintrags Satz ist.

- Höchstens 255 bedeutet das, dass die nächsten 255 Verzeichniseinträge und dieser primäre Verzeichniseintrag den Verzeichniseintrags Satz enthalten.

Wichtige primäre Verzeichniseintrags Strukturen, die von dieser Vorlage abgeleitet werden, können die Felder secondarycount und SetCheckSum neu definieren.

#### <a name="633-setchecksum-field"></a>6.3.3 SetCheckSum-Feld

Das Feld SetCheckSum muss die Prüfsumme aller Verzeichniseinträge im angegebenen Verzeichniseintrags Satz enthalten. Die Prüfsumme schließt dieses Feld jedoch aus (siehe [Abbildung 2](#figure-2-entrysetchecksum-computation)). Durch Implementierungen muss überprüft werden, ob der Inhalt dieses Felds gültig ist, bevor ein anderer Verzeichniseintrag im angegebenen Verzeichniseintrags Satz verwendet wird.

Wichtige primäre Verzeichniseintrags Strukturen, die von dieser Vorlage abgeleitet werden, können die Felder secondarycount und SetCheckSum neu definieren.

<div id="figure-2-entrysetchecksum-computation" />

**Abbildung 2 entrysetchecksum-Berechnung**

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

#### <a name="634-generalprimaryflags-field"></a>6.3.4 generalprimaryflags-Feld

Das Feld generalprimaryflags enthält Flags (siehe [Tabelle 17](#table-17-generic-generalprimaryflags-field-structure)).

Wichtige primäre Verzeichniseintrags Strukturen, die von dieser Vorlage abgeleitet werden, können dieses Feld neu definieren.

<div id="table-17-generic-generalprimaryflags-field-structure" />

**Tabelle 17 generische generalprimaryflags-Feldstruktur**

<table>
<thead>
<tr class="header">
<th><strong>Feldname</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>trate</strong></p></th>
<th><p><strong>Größe</strong></p>
<p><strong>Bohrer</strong></p></th>
<th><strong>Kommentare</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Zuordnung möglich</td>
<td>0</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#6341-allocationpossible-field">section 6.3.4.1</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>Nofatchain</td>
<td>1</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#6342-nofatchain-field">section 6.3.4.2</a> definiert seinen Inhalt.</td>
</tr>
<tr class="odd">
<td>Customdefined</td>
<td>2</td>
<td>14</td>
<td>Dieses Feld ist obligatorisch, und Strukturen, die von dieser Vorlage abgeleitet werden, können dieses Feld definieren.</td>
</tr>
</tbody>
</table>

##### <a name="6341-allocationpossible-field"></a>6.3.4.1-Feld (Zuordnung möglich)

Im Feld allocationpossible muss beschrieben werden, ob eine Zuordnung im Cluster Heap für den angegebenen Verzeichniseintrag möglich ist.

Die gültigen Werte für dieses Feld müssen lauten:

- 0 (null) bedeutet, dass eine zugeordnete Zuordnung von Clustern nicht möglich ist, und die Felder firstcluster und DATALENGTH sind tatsächlich undefiniert (Strukturen, die von dieser Vorlage abgeleitet werden, können diese Felder neu definieren)

- 1. Dies bedeutet, dass eine zugeordnete Zuordnung von Clustern möglich ist und die Felder "firstcluster" und "DATALENGTH" wie definiert sind.

##### <a name="6342-nofatchain-field"></a>6.3.4.2 nofatchain-Feld

Im Feld nofatchain muss angegeben werden, ob das aktive FAT die Cluster Kette der angegebenen Zuordnung beschreibt.

Die gültigen Werte für dieses Feld müssen lauten:

- 0 (null) bedeutet, dass die entsprechenden FAT-Einträge für die Cluster Kette der Zuordnung gültig sind und diese von den Implementierungen interpretiert werden. Wenn das Feld "Zuweisung möglich" den Wert 0 oder das Feld "Zuweisung möglich" den Wert 1 enthält und das Feld "firstcluster" den Wert 0 (null) enthält, ist der einzige gültige Wert dieses Felds 0.

- 1. Dies bedeutet, dass die zugeordnete Zuordnung eine zusammenhängende Reihe von Clustern ist. die entsprechenden FAT-Einträge für die Cluster sind ungültig, und Implementierungen sollten Sie nicht interpretieren. Implementierungen können mithilfe der folgenden Gleichung die Größe der zugeordneten Zuordnung berechnen: DATALENGTH/(2<sup>sectorsperclustershift</sup> \* 2<sup>bytespersectorshift</sup>) aufgerundet auf die nächste ganze Zahl.

Wenn wichtige primäre Verzeichniseintrags Strukturen, die von dieser Vorlage abgeleitet sind, das Feld generalprimaryflags neu definieren, dann sind die entsprechenden FAT-Einträge für die Cluster Kette der zugeordneten Zuordnung gültig.

#### <a name="635-firstcluster-field"></a>6.3.5 firstcluster-Feld

Das Feld "firstcluster" muss der Definition entsprechen, die in der generischen DirectoryEntry-Vorlage angegeben ist (siehe [Abschnitt 6.2.2](#622-firstcluster-field)).

Wenn das nofatchain-Bit 1 ist, muss firstcluster auf einen gültigen Cluster im Cluster Heap zeigen.

Wichtige primäre Verzeichniseintrags Strukturen, die von dieser Vorlage abgeleitet werden, können die Felder firstcluster und DATALENGTH neu definieren. Andere Strukturen, die von dieser Vorlage abgeleitet werden, können die Felder firstcluster und DATALENGTH nur dann neu definieren, wenn das Feld "Zuweisung möglich" den Wert 0 (null) enthält.

#### <a name="636-datalength-field"></a>6.3.6 DATALENGTH-Feld

Das DATALENGTH-Feld muss der Definition entsprechen, die in der generischen DirectoryEntry-Vorlage bereitgestellt wird (siehe [Abschnitt 6.2.3](#623-datalength-field)).

Wenn das nofatchain-Bit 1 ist, darf DATALENGTH nicht 0 (null) sein. Wenn das Feld firstcluster NULL ist, muss DATALENGTH ebenfalls NULL sein.

Wichtige primäre Verzeichniseintrags Strukturen, die von dieser Vorlage abgeleitet werden, können die Felder firstcluster und DATALENGTH neu definieren. Andere Strukturen, die von dieser Vorlage abgeleitet werden, können die Felder firstcluster und DATALENGTH nur dann neu definieren, wenn das Feld "Zuweisung möglich" den Wert 0 (null) enthält.

### <a name="64-generic-secondary-directoryentry-template"></a>6,4 generische sekundäre directentry-Vorlage

Der zentrale Zweck sekundärer Verzeichniseinträge besteht darin, zusätzliche Informationen über einen Verzeichniseintrags Satz bereitzustellen. Die Möglichkeit, die generische sekundäre directentry-Vorlage zu interpretieren, ist obligatorisch.

Die Definition von kritischen und unbedeutenden Sekundär Verzeichnis Einträgen korreliert mit der kleineren exFAT-Revisionsnummer. Die Unterstützung für alle wichtigen oder ungutartigen sekundären Verzeichniseinträge, die diese Spezifikation oder nachfolgende Spezifikationen haben, definiert ist optional.

Alle sekundären Verzeichniseintrags Strukturen werden von der generischen Vorlage für sekundäre Directoren (siehe [Tabelle 18](#table-18-generic-secondary-directoryentry-template)) abgeleitet, die von der generischen Director Entry-Vorlage abgeleitet ist (siehe [Abschnitt 6,2](#62-generic-directoryentry-template)).

<div id="table-18-generic-secondary-directoryentry-template" />

**Tabelle 18 generische sekundäre Directoren Entry-Vorlage**

<table>
<thead>
<tr class="header">
<th><strong>Feldname</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>Hobby</strong></p></th>
<th><p><strong>Größe</strong></p>
<p><strong>Hobby</strong></p></th>
<th><strong>Kommentare</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EntryType</td>
<td>0</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und Abschnitts <a href="#641-entrytype-field">Abschnitt 6.4.1</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>Generalsecondaryflags</td>
<td>1</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#642-generalsecondaryflags-field">section 6.4.2</a> definiert seinen Inhalt.</td>
</tr>
<tr class="odd">
<td>Customdefined</td>
<td>2</td>
<td>18</td>
<td>Dieses Feld ist obligatorisch, und Strukturen, die von dieser Vorlage abgeleitet werden, definieren ihren Inhalt.</td>
</tr>
<tr class="even">
<td>Firstcluster</td>
<td>20</td>
<td>4</td>
<td>Dieses Feld ist obligatorisch, und <a href="#643-firstcluster-field">section 6.4.3</a> definiert seinen Inhalt.</td>
</tr>
<tr class="odd">
<td>DataLength</td>
<td>24</td>
<td>8</td>
<td>Dieses Feld ist obligatorisch, und <a href="#644-datalength-field">section 6.4.4</a> definiert seinen Inhalt.</td>
</tr>
</tbody>
</table>

#### <a name="641-entrytype-field"></a>6.4.1 EntryType-Feld

Das EntryType-Feld muss der Definition entsprechen, die in der generischen DirectoryEntry-Vorlage bereitgestellt wird (siehe [Abschnitt 6.2.1](#621-entrytype-field)).

##### <a name="6411-typecode-field"></a>6.4.1.1 TypeCode-Feld

Das TypeCode-Feld muss der Definition entsprechen, die in der generischen DirectoryEntry-Vorlage bereitgestellt wird (siehe [Abschnitt 6.2.1.1](#6211-typecode-field)).

##### <a name="6412-typeimportance-field"></a>6.4.1.2 typeimportance-Feld

Das typeimportance-Feld muss der Definition entsprechen, die in der generischen DirectoryEntry-Vorlage bereitgestellt wird (siehe [Abschnitt 6.2.1.2](#6212-typeimportance-field)).

###### <a name="64121-critical-secondary-directory-entries"></a>6.4.1.2.1 wichtige Einträge für das sekundäre Verzeichnis

Wichtige Einträge im sekundären Verzeichnis enthalten Informationen, die für die ordnungsgemäße Verwaltung des enthaltenen Verzeichniseintrags Satzes wichtig sind.
Obwohl die Unterstützung für einen bestimmten kritischen sekundären Verzeichniseintrag optional ist, rendert ein unbekannter kritischer Verzeichniseintrag den gesamten Verzeichniseintrags Satz als nicht erkannt (über die Definition der entsprechenden Verzeichniseintrags Vorlagen hinaus).

Wenn jedoch ein Verzeichniseintrags Satz mindestens einen wichtigen Eintrag für ein sekundäres Verzeichnis enthält, den eine Implementierung nicht erkennt, sollte die Implementierung höchstens die Vorlagen der Verzeichniseinträge im Verzeichniseintrags Satz interpretieren, und nicht die Datenzuordnung, die mit einem Verzeichniseintrag im Verzeichniseintrags Satz verknüpft ist (Weitere Informationen finden Sie im [Abschnitt 7,4](#74-file-directory-entry)).

###### <a name="64122-benign-secondary-directory-entries"></a>6.4.1.2.2 nicht gutartige sekundäre Verzeichniseinträge

Nicht gutartige sekundäre Verzeichniseinträge enthalten zusätzliche Informationen, die für die Verwaltung des enthaltenen Verzeichniseintrags Satzes nützlich sein können. Die Unterstützung für einen bestimmten, nicht bestimmten sekundären Verzeichniseintrag ist optional.
Unbekannte, nicht erkannte sekundäre Verzeichniseinträge führen nicht dazu, dass der gesamte Verzeichniseintrag als unbekannt festgelegt wird.

Implementierungen können einen nicht erkannten, nicht erkannten, nicht erkannten sekundären Eintrag ignorieren.

##### <a name="6413-typecategory-field"></a>6.4.1.3 typecategory-Feld

Das Feld typecategory muss der Definition entsprechen, die in der generischen DirectoryEntry-Vorlage bereitgestellt wird (siehe [Abschnitt 6.2.1.3](#6213-typecategory-field)).

Für diese Vorlage lautet der gültige Wert für dieses Feld 1.

##### <a name="6414-inuse-field"></a>6.4.1.4 InUse-Feld

Das Feld "InUse" muss der Definition entsprechen, die in der generischen DirectoryEntry-Vorlage angegeben ist (siehe [Abschnitt 6.2.1.4](#6214-inuse-field)).

#### <a name="642-generalsecondaryflags-field"></a>6.4.2 generalsecondaryflags-Feld

Das Feld generalsecondaryflags enthält Flags (siehe [Tabelle 19](#table-19-generic-generalsecondaryflags-field-structure)).

<div id="table-19-generic-generalsecondaryflags-field-structure" />

**Tabelle 19 generische generalsecondaryflags-Feldstruktur**

<table>
<thead>
<tr class="header">
<th><strong>Feldname</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>trate</strong></p></th>
<th><p><strong>Größe</strong></p>
<p><strong>Bohrer</strong></p></th>
<th><strong>Kommentare</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Zuordnung möglich</td>
<td>0</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#6421-allocationpossible-field">section 6.4.2.1</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>Nofatchain</td>
<td>1</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#6422-nofatchain-field">section 6.4.2.2</a> definiert seinen Inhalt.</td>
</tr>
<tr class="odd">
<td>Customdefined</td>
<td>2</td>
<td>6</td>
<td>Dieses Feld ist obligatorisch, und Strukturen, die von dieser Vorlage abgeleitet werden, können dieses Feld definieren.</td>
</tr>
</tbody>
</table>

##### <a name="6421-allocationpossible-field"></a>6.4.2.1-Feld (Zuordnung möglich)

Das Feld "zugsmöglichkeit" muss dieselbe Definition wie das benannte Feld in der generischen primären DirectoryEntry-Vorlage aufweisen (siehe [Abschnitt 6.3.4.1](#6341-allocationpossible-field)).

##### <a name="6422-nofatchain-field"></a>6.4.2.2 nofatchain-Feld

Das Feld nofatchain muss die gleiche Definition wie das benannte Feld in der generischen primären DirectoryEntry-Vorlage aufweisen (siehe [Abschnitt 6.3.4.2](#6342-nofatchain-field)).

#### <a name="643-firstcluster-field"></a>6.4.3 firstcluster-Feld

Das Feld "firstcluster" muss der Definition entsprechen, die in der generischen DirectoryEntry-Vorlage angegeben ist (siehe [Abschnitt 6.2.2](#622-firstcluster-field)).

Wenn das nofatchain-Bit 1 ist, muss firstcluster auf einen gültigen Cluster im Cluster Heap zeigen.

#### <a name="644-datalength-field"></a>6.4.4 DATALENGTH-Feld

Das DATALENGTH-Feld muss der Definition entsprechen, die in der generischen DirectoryEntry-Vorlage bereitgestellt wird (siehe [Abschnitt 6.2.3](#623-datalength-field)).

Wenn das nofatchain-Bit 1 ist, darf DATALENGTH nicht 0 (null) sein. Wenn das Feld firstcluster NULL ist, muss DATALENGTH ebenfalls NULL sein.

## <a name="7-directory-entry-definitions"></a>7 Verzeichniseintrags Definitionen

Revision 1,00 des exFAT-Dateisystems definiert die folgenden Verzeichniseinträge:

- Kritischer primär

  - Zuordnungs Bitmap ([Abschnitt 7,1](#71-allocation-bitmap-directory-entry))

  - Up-Case-Tabelle ([Abschnitt 7,2](#72-up-case-table-directory-entry))

  - Volumebezeichnung ([Abschnitt 7,3](#73-volume-label-directory-entry))

  - File ([Abschnitt 7,4](#74-file-directory-entry))

- Nicht wohlwollend

  - VolumeGuid ([Abschnitt 7,5](#75-volume-guid-directory-entry))

  - Texfat Padding ([Abschnitt 7,10](#710-texfat-padding-directory-entry))

<!-- -->

- Kritische sekundäre Datenbank

  - Streamingerweiterung ([Abschnitt 7,6](#76-stream-extension-directory-entry))

  - Dateiname ([Abschnitt 7,7](#77-file-name-directory-entry))

- Gutartige sekundäre Datenbank

  - Hersteller Erweiterung ([Abschnitt 7,8](#78-vendor-extension-directory-entry))

  - Hersteller Zuordnung ([Abschnitt 7,9](#79-vendor-allocation-directory-entry))

### <a name="71-allocation-bitmap-directory-entry"></a>7,1 Zuordnungs Bitmap-Verzeichniseintrag

Im exFAT-Dateisystem wird in einem FAT nicht der Zuordnungs Status von Clustern beschrieben. Stattdessen wird eine Zuordnungs Bitmap verwendet. Zuordnungs Bitmaps sind im Cluster Heap vorhanden (siehe [Abschnitt 7.1.5](#715-allocation-bitmap)) und verfügen über entsprechende wichtige primäre Verzeichniseinträge im Stammverzeichnis (siehe [Tabelle 20](#table-20-allocation-bitmap-directoryentry-structure)).

Das Feld "anzahlungsabate" bestimmt die Anzahl der gültigen Zuordnungs-bitmapverzeichniseinträge im Stammverzeichnis. Wenn das Feld "Werte" den Wert 1 enthält, ist die einzige gültige Anzahl von Zuordnungs Bitmap-Verzeichnis Einträgen 1. Der einzige Zuordnungs Bitmap-Verzeichniseintrag ist nur gültig, wenn die erste Zuordnungs Bitmap beschrieben wird (siehe [Abschnitt 7.1.2.1](#7121-bitmapidentifier-field)). Wenn das Feld "Werte" den Wert 2 enthält, ist die einzige gültige Anzahl von Zuordnungs Bitmap-Verzeichnis Einträgen 2.
Außerdem sind die beiden Zuordnungs Bitmap-Verzeichniseinträge nur gültig, wenn die erste Zuordnungs Bitmap und die andere die zweite Zuordnungs Bitmap beschreiben.

<div id="table-20-allocation-bitmap-directoryentry-structure" />

**Tabelle 20 Zuordnungs Bitmap directoriyentry-Struktur**

<table>
<thead>
<tr class="header">
<th><strong>Feldname</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>Hobby</strong></p></th>
<th><p><strong>Größe</strong></p>
<p><strong>Hobby</strong></p></th>
<th><strong>Kommentare</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EntryType</td>
<td>0</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#711-entrytype-field">Abschnitt 7.1.1</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>Bitmapflags</td>
<td>1</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#712-bitmapflags-field">section 7.1.2</a> definiert seinen Inhalt.</td>
</tr>
<tr class="odd">
<td>Reserviert</td>
<td>2</td>
<td>18</td>
<td>Dieses Feld ist obligatorisch, und die Inhalte sind reserviert.</td>
</tr>
<tr class="even">
<td>Firstcluster</td>
<td>20</td>
<td>4</td>
<td>Dieses Feld ist obligatorisch, und <a href="#713-firstcluster-field">section 7.1.3</a> definiert seinen Inhalt.</td>
</tr>
<tr class="odd">
<td>DataLength</td>
<td>24</td>
<td>8</td>
<td>Dieses Feld ist obligatorisch, und <a href="#714-datalength-field">section 7.1.4</a> definiert seinen Inhalt.</td>
</tr>
</tbody>
</table>

#### <a name="711-entrytype-field"></a>7.1.1 EntryType-Feld

Das EntryType-Feld muss der Definition entsprechen, die in der generischen primären DirectoryEntry-Vorlage bereitgestellt wird (siehe [Abschnitt 6.3.1](#631-entrytype-field)).

##### <a name="7111-typecode-field"></a>7.1.1.1 TypeCode-Feld

Das TypeCode-Feld muss der Definition entsprechen, die in der generischen primären DirectoryEntry-Vorlage bereitgestellt wird (siehe [Abschnitt 6.3.1.1](#6311-typecode-field)).

Für einen Zuordnungs Bitmap-Verzeichniseintrag ist der gültige Wert für dieses Feld 1.

##### <a name="7112-typeimportance-field"></a>7.1.1.2 typeimportance-Feld

Das typeimportance-Feld muss der Definition entsprechen, die in der generischen primären DirectoryEntry-Vorlage bereitgestellt wird (siehe [Abschnitt 6.3.1.2](#6312-typeimportance-field)).

Für einen Zuordnungs Bitmap-Verzeichniseintrag ist der gültige Wert für dieses Feld 0.

##### <a name="7113-typecategory-field"></a>7.1.1.3 typecategory-Feld

Das Feld typecategory muss der Definition in der generischen primären DirectoryEntry-Vorlage entsprechen (siehe [Abschnitt 6.3.1.3](#6313-typecategory-field)).

##### <a name="7114-inuse-field"></a>7.1.1.4 InUse-Feld

Das Feld "InUse" muss der Definition entsprechen, die in der generischen primären DirectoryEntry-Vorlage angegeben ist (siehe [Abschnitt 6.3.1.4](#6314-inuse-field)).

#### <a name="712-bitmapflags-field"></a>7.1.2 bitmapflags-Feld

Das Feld "bitmapflags" enthält Flags (siehe [Tabelle 21](#table-21-bitmapflags-field-structure)).

<div id="table-21-bitmapflags-field-structure" />

**Tabelle 21 bitmapflags-Feldstruktur**

<table>
<thead>
<tr class="header">
<th><strong>Feldname</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>trate</strong></p></th>
<th><p><strong>Größe</strong></p>
<p><strong>Bohrer</strong></p></th>
<th><strong>Kommentare</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Bitmapidentifier</td>
<td>0</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#7121-bitmapidentifier-field">section 7.1.2.1</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>Reserviert</td>
<td>1</td>
<td>7</td>
<td>Dieses Feld ist obligatorisch, und die Inhalte sind reserviert.</td>
</tr>
</tbody>
</table>

##### <a name="7121-bitmapidentifier-field"></a>7.1.2.1 bitmapidentifier-Feld

Das Feld bitmapidentifier gibt an, welche Zuordnungs Bitmap im angegebenen Verzeichniseintrag beschrieben wird. Implementierungen müssen das erste Zuordnungs Bitmuster in Verbindung mit dem ersten FAT verwenden und müssen die zweite Zuordnungs Bitmap in Verbindung mit dem zweiten FAT verwenden. Das activefat-Feld beschreibt, welche FAT-und Zuordnungs Bitmap aktiv ist.

Die gültigen Werte für dieses Feld müssen lauten:

- 0 (null) bedeutet, dass der angegebene Verzeichniseintrag das erste Zuordnungs Bitmap beschreibt.

- 1. Dies bedeutet, dass der angegebene Verzeichniseintrag die zweite Zuordnungs Bitmap beschreibt und nur möglich ist, wenn "numoffats" den Wert 2 enthält.

#### <a name="713-firstcluster-field"></a>7.1.3 firstcluster-Feld

Das Feld "firstcluster" muss der Definition entsprechen, die in der generischen primären DirectoryEntry-Vorlage angegeben ist (siehe [Abschnitt 6.3.5](#635-firstcluster-field)).

Dieses Feld enthält den Index des ersten Clusters der Cluster Kette, wie in FAT beschrieben, das die Zuordnungs Bitmap hostet.

#### <a name="714-datalength-field"></a>7.1.4 DATALENGTH-Feld

Das dataclunerfeld muss der Definition entsprechen, die in der generischen primären DirectoryEntry-Vorlage bereitgestellt wird (siehe [Abschnitt 6.3.6](#636-datalength-field)).

#### <a name="715-allocation-bitmap"></a>7.1.5-Zuordnungs Bitmap

Eine Zuordnungs Bitmap zeichnet den Zuordnungs Status der Cluster im Cluster Heap auf. Jedes Bit in einer Zuordnungs Bitmap gibt an, ob der zugehörige Cluster für die Zuordnung verfügbar ist.

Eine Zuordnungs Bitmap stellt Cluster vom niedrigsten zum höchsten Index dar (siehe [Tabelle 22](#table-22-allocation-bitmap-structure)). Aus historischen Gründen hat der erste Cluster den Index 2.
Hinweis: das erste Bit in der Bitmap ist das niedrigste Bit des ersten Byte.

<div id="table-22-allocation-bitmap-structure" />

**Tabelle 22 Zuordnungs Bitmap-Struktur**

<table>
<thead>
<tr class="header">
<th><strong>Feldname</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>trate</strong></p></th>
<th><p><strong>Größe</strong></p>
<p><strong>Bohrer</strong></p></th>
<th><strong>Kommentare</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Bitmapentry [2]</td>
<td>0</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und Abschnitts <a href="#7151-bitmapentry2--bitmapentryclustercount1-fields">Abschnitt 7.1.5.1</a> definiert seinen Inhalt.</td>
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
<td>Bitmapentry [Cluster count + 1]</td>
<td>Clustercount-1</td>
<td>1</td>
<td><p>Dieses Feld ist obligatorisch, und <a href="#7151-bitmapentry2--bitmapentryclustercount1-fields">section 7.1.5.1</a> definiert seinen Inhalt.</p>
<p>Hinweis: die Haupt-und Sicherungs Start Sektoren enthalten beide das Feld "clustercount".</p></td>
</tr>
<tr class="even">
<td>Reserviert</td>
<td>Cluster count (</td>
<td>(DATALENGTH * 8) – clustercount</td>
<td><p>Dieses Feld ist obligatorisch, und sein Inhalt ist ggf. reserviert.</p>
<p>Hinweis: die Haupt-und Sicherungs Start Sektoren enthalten beide das Feld "clustercount".</p></td>
</tr>
</tbody>
</table>

##### <a name="7151-bitmapentry2--bitmapentryclustercount1-fields"></a>7.1.5.1 bitmapentry \[ 2 \] ... Bitmapentry- \[ clustercount + 1 \] Felder

Jedes bitmapentry-Feld in diesem Array stellt einen Cluster im Cluster Heap dar. Bitmapentry \[ 2 \] stellt den ersten Cluster im Cluster Heap dar, und bitmapentry \[ clustercount + 1 \] stellt den letzten Cluster im Cluster Heap dar.

Die gültigen Werte für diese Felder müssen lauten:

- 0: Beschreibt den entsprechenden Cluster als verfügbar für die Zuordnung.

- 1: Beschreibt den entsprechenden Cluster als nicht verfügbar für die Zuordnung (eine Cluster Zuordnung nutzt möglicherweise bereits den entsprechenden Cluster, oder das aktive FAT beschreibt den entsprechenden Cluster möglicherweise als schlecht).

### <a name="72-up-case-table-directory-entry"></a>7,2 Eintrag für den Tabellen Verzeichniseintrag

Die nach Fall Tabelle definiert die Konvertierung von Kleinbuchstaben in Großbuchstaben. Dies ist wichtig aufgrund des Dateinamen-Verzeichniseintrags (siehe Abschnitt 7,7) mithilfe von Unicode-Zeichen und dem exFAT-Dateisystem, bei dem die Groß-/Kleinschreibung nicht beachtet wird. Die up-Case-Tabelle ist im Cluster Heap vorhanden (siehe [Abschnitt 7.2.5](#725-up-case-table)) und verfügt über einen entsprechenden wichtigen primären Verzeichniseintrag im Stammverzeichnis (siehe [Tabelle 23](#table-23-up-case-table-directoryentry-structure)). Die gültige Anzahl von Tabellen Verzeichnis Einträgen in der Groß-/Kleinschreibung ist 1.

Aufgrund der Beziehung zwischen den Tabellen-und Dateinamen für die Groß-und Kleinschreibung sollten Implementierungen die nach Fall Tabelle nicht ändern, außer als Ergebnis von Format Vorgängen.

<div id="table-23-up-case-table-directoryentry-structure" />

**Tabelle 23: directoriyentry-Struktur in der up-Case-Tabelle**

<table>
<thead>
<tr class="header">
<th><strong>Feldname</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>Hobby</strong></p></th>
<th><p><strong>Größe</strong></p>
<p><strong>Hobby</strong></p></th>
<th><strong>Kommentare</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EntryType</td>
<td>0</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#721-entrytype-field">section 7.2.1</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>Reserved1</td>
<td>1</td>
<td>3</td>
<td>Dieses Feld ist obligatorisch, und die Inhalte sind reserviert.</td>
</tr>
<tr class="odd">
<td>Tablechecksum</td>
<td>4</td>
<td>4</td>
<td>Dieses Feld ist obligatorisch, und <a href="#722-tablechecksum-field">section 7.2.2</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>Reserved2</td>
<td>8</td>
<td>12</td>
<td>Dieses Feld ist obligatorisch, und die Inhalte sind reserviert.</td>
</tr>
<tr class="odd">
<td>Firstcluster</td>
<td>20</td>
<td>4</td>
<td>Dieses Feld ist obligatorisch, und <a href="#723-firstcluster-field">section 7.2.3</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>DataLength</td>
<td>24</td>
<td>8</td>
<td>Dieses Feld ist obligatorisch, und <a href="#724-datalength-field">section 7.2.4</a> definiert seinen Inhalt.</td>
</tr>
</tbody>
</table>

#### <a name="721-entrytype-field"></a>7.2.1 EntryType-Feld

Das EntryType-Feld muss der Definition entsprechen, die in der generischen primären DirectoryEntry-Vorlage bereitgestellt wird (siehe [Abschnitt 6.3.1](#631-entrytype-field)).

##### <a name="7211-typecode-field"></a>7.2.1.1 TypeCode-Feld

Das TypeCode-Feld muss der Definition entsprechen, die in der generischen primären DirectoryEntry-Vorlage bereitgestellt wird (siehe [Abschnitt 6.3.1.1](#6311-typecode-field)).

Der gültige Wert für dieses Feld lautet wie folgt:
2.

##### <a name="7212-typeimportance-field"></a>7.2.1.2 typeimportance-Feld

Das typeimportance-Feld muss der Definition entsprechen, die in der generischen primären DirectoryEntry-Vorlage bereitgestellt wird (siehe [Abschnitt 6.3.1.2](#6312-typeimportance-field)).

Der gültige Wert für dieses Feld lautet wie folgt:
0.

##### <a name="7213-typecategory-field"></a>7.2.1.3 typecategory-Feld

Das Feld typecategory muss der Definition in der generischen primären DirectoryEntry-Vorlage entsprechen (siehe [Abschnitt 6.3.1.3](#6313-typecategory-field)).

##### <a name="7214-inuse-field"></a>7.2.1.4 InUse-Feld

Das Feld "InUse" muss der Definition entsprechen, die in der generischen primären DirectoryEntry-Vorlage angegeben ist (siehe [Abschnitt 6.3.1.4](#6314-inuse-field)).

#### <a name="722-tablechecksum-field"></a>7.2.2 tablechecksum-Feld

Das Feld tablechecksum enthält die Prüfsumme der up-Case-Tabelle (die in den Feldern firstcluster und DATALENGTH beschrieben wird). Durch Implementierungen muss überprüft werden, ob der Inhalt dieses Felds gültig ist, bevor die up-Case-Tabelle verwendet wird.

<div id="figure-3-tablechecksum-computation" />

**Abbildung 3 tablechecksum-Berechnung**

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

#### <a name="723-firstcluster-field"></a>7.2.3 firstcluster-Feld

Das Feld "firstcluster" muss der Definition entsprechen, die in der generischen primären DirectoryEntry-Vorlage angegeben ist (siehe [Abschnitt 6.3.5](#635-firstcluster-field)).

Dieses Feld enthält den Index des ersten Clusters der Cluster Kette, wie in FAT beschrieben, das die up-Case-Tabelle hostet.

#### <a name="724-datalength-field"></a>7.2.4 DATALENGTH-Feld

Das dataclunerfeld muss der Definition entsprechen, die in der generischen primären DirectoryEntry-Vorlage bereitgestellt wird (siehe [Abschnitt 6.3.6](#636-datalength-field)).

#### <a name="725-up-case-table"></a>7.2.5-Tabelle

Eine Fall Tabelle ist eine Reihe von Unicode-Zeichen Zuordnungen. Eine Zeichen Zuordnung besteht aus einem 2-Byte-Feld mit dem Index des Felds in der Tabelle "up-Case", das das zu schreibende Unicode-Zeichen darstellt, und dem 2-Byte-Feld, das das Unicode-Zeichen mit der Zeichenfolge darstellt.

Die ersten 128 Unicode-Zeichen verfügen über verbindliche Zuordnungen (siehe [Tabelle 24](#table-24-mandatory-first-128-up-case-table-entries)).
Eine Tabellen-/Schreibtabelle, die eine beliebige andere Zeichen Zuordnung für die ersten 128 Unicode-Zeichen aufweist, ist ungültig.

Bei Implementierungen, die nur Zeichen aus dem obligatorischen Zuordnungs Bereich unterstützen, werden möglicherweise die Zuordnungen der restlichen Fall Tabelle ignoriert. Bei solchen Implementierungen dürfen beim Erstellen oder Umbenennen von Dateien nur Zeichen aus dem obligatorischen Zuordnungsbereich verwendet werden (Informationen hierzu finden Sie im [Abschnitt 7,7](#77-file-name-directory-entry)). Wenn vorhandene Dateinamen in der Groß-/Kleinschreibung vorhanden sind, dürfen solche Implementierungen keine Groß-/kleinschreibungszeichen aus dem nicht obligatorischen Mapping-Bereich enthalten, Sie sollten Sie jedoch im sich ergebenden Dateinamen unverändert lassen (Hierbei handelt es sich um eine partielle Schreibweise). Beim Vergleichen von Dateinamen müssen solche Implementierungen Dateinamen, die sich von dem Namen unterscheiden, nur durch Unicode-Zeichen aus dem nicht obligatorischen Mapping-Bereich als gleichwertig behandeln. Obwohl solche Dateinamen nur potenziell äquivalent sind, können solche Implementierungen nicht sicherstellen, dass der Dateiname der vollständigen Schreibweise nicht mit dem Namen im Vergleich in Konflikt steht.

<div id="table-24-mandatory-first-128-up-case-table-entries" />

**Tabelle 24: verbindliche erste 128-Tabelleneinträge**

| **Tabellen Index** | **Tabelleneinträge** |           |           |           |           |           |           |           |
|-----------------|-------------------|-----------|-----------|-----------|-----------|-----------|-----------|-----------|
|                 | **+ 0**           | **+ 1**   | **+ 2**   | **+ 3**   | **+ 4**   | **+ 5**   | **+ 6**   | **+ 7**   |
| **0000H**       | 0000H             | 0001h     | 0002h     | 0003h     | 0004h     | 0005h     | 0006h     | 0007h     |
| **0008h**       | 0008h             | 0009h     | 000ah     | 000bh     | 000ch     | 000dh     | 000eh     | 000fh     |
| **0010h**       | 0010h             | 0011h     | 0012h     | 0013h     | 0014h     | 0015h     | 0016h     | 0017h     |
| **0018h**       | 0018h             | 0019h     | 001ah     | 001-BH     | 001ch     | 001dh     | 001eh     | 001fh     |
| **0020h**       | 0020h             | 0021h     | 0022h     | 0023h     | 0024h     | 0025h     | 0026h     | 0027h     |
| **0028h**       | 0028h             | 0029h     | 002ah     | 002-BH     | 002ch     | 002dh     | 002eh     | 002fh     |
| **0030h**       | 0030h             | 0031h     | 0032h     | 0033h     | 0034h     | 0035h     | 0036h     | 0037h     |
| **0038h**       | 0038h             | 0039h     | 003ah     | 003-BH     | 003ch     | 003dh     | 003eh     | 003fh     |
| **0040h**       | 0040h             | 0041h     | 0042h     | 0043h     | 0044h     | 0045h     | 0046h     | 0047h     |
| **0048h**       | 0048h             | 0049h     | 004ah     | 004-BH     | 004ch     | 004dh     | 004eh     | 004fh     |
| **0050h**       | 0050h             | 0051h     | 0052h     | 0053h     | 0054h     | 0055h     | 0056h     | 0057h     |
| **0058h**       | 0058h             | 0059h     | 005ah     | 005-BH     | 005ch     | 005dh     | 005eh     | 005fh     |
| **0060h**       | 0060h             | **0041h** | **0042h** | **0043h** | **0044h** | **0045h** | **0046h** | **0047h** |
| **0068h**       | **0048h**         | **0049h** | **004ah** | **004-BH** | **004ch** | **004dh** | **004eh** | **004fh** |
| **0070h**       | **0050h**         | **0051h** | **0052h** | **0053h** | **0054h** | **0055h** | **0056h** | **0057h** |
| **0078h**       | **0058h**         | **0059h** | **005ah** | 007-BH     | 007ch     | 007dh     | 007eh     | 007fh     |

**(Hinweis: Einträge mit nicht Identitäts Zuordnungen, die nicht in der Identität vorliegen, sind fett formatiert.)**

Beim Formatieren eines Volumes können Implementierungen eine Tabellen-/Schreibtabelle in komprimiertem Format mithilfe der identitätsmapping-Komprimierung generieren, da ein großer Teil des Unicode-Zeichen Raums kein Konzept von Case hat (was bedeutet, dass die Zeichen "Kleinbuchstaben" und "Großbuchstaben" äquivalent sind).
Implementierungen komprimieren eine nach Fall Tabelle, indem Sie eine Reihe von Identitäts Zuordnungen mit dem Wert FFFFh und der Anzahl der Identitäts Zuordnungen darstellen.

Eine-Implementierung kann z. b. die ersten 100 (64h)-Zeichen Zuordnungen mit den folgenden acht Einträgen einer komprimierten Tabellen Fall Tabelle darstellen:

> FFFFh, 0061h, 0041h, 0042h, 0043h

Die ersten beiden Einträge geben an, dass die ersten 97 (61h)-Zeichen (von 0000H bis 0060h) Identitäts Zuordnungen aufweisen. Die nachfolgenden Zeichen, 0061h bis 0063h, werden den Zeichen 0041h bis 0043h zugeordnet.

Die Möglichkeit, bei der Formatierung eines Volumes eine komprimierte Tabelle für den Fall eines Volumes bereitzustellen, ist optional. Allerdings ist die Möglichkeit, sowohl eine nicht komprimierte als auch eine komprimierte Tabelle mit dem Fall zu interpretieren, obligatorisch. Der Wert des tablechecksum-Felds entspricht immer der Art und Weise, wie die Tabellen-/uhrzeittabelle auf dem Volume vorhanden ist, das entweder im komprimierten oder unkomprimierten Format vorliegt.

##### <a name="7251-recommended-up-case-table"></a>7.2.5.1 Empfohlene up-Case-Tabelle

Beim Formatieren eines Volumes sollten die Implementierungen die empfohlene up-Case-Tabelle in komprimiertem Format (siehe [Tabelle 25](#table-25-recommended-up-case-table-in-compressed-format)) aufzeichnen, bei der der Wert des Felds tablechecksum E619D30Dh lautet.

Wenn eine Implementierung eine eigene, komprimierte oder unkomprimierte Komprimierungs Tabelle definiert, sollte diese Tabelle den gesamten Unicode-Zeichenbereich abdecken (von Zeichen Codes 0000H bis FFFFh inklusiv).

<div id="table-25-recommended-up-case-table-in-compressed-format" />

**Tabelle 25 Empfohlene up-Case-Tabelle in komprimiertem Format**

| **Rohoffset** | **Komprimierte Tabelleneinträge** |         |         |         |         |         |         |         |
|----------------|------------------------------|---------|---------|---------|---------|---------|---------|---------|
|                | **+ 0**                      | **+ 1** | **+ 2** | **+ 3** | **+ 4** | **+ 5** | **+ 6** | **+ 7** |
| **0000H**      | 0000H                        | 0001h   | 0002h   | 0003h   | 0004h   | 0005h   | 0006h   | 0007h   |
| **0008h**      | 0008h                        | 0009h   | 000ah   | 000bh   | 000ch   | 000dh   | 000eh   | 000fh   |
| **0010h**      | 0010h                        | 0011h   | 0012h   | 0013h   | 0014h   | 0015h   | 0016h   | 0017h   |
| **0018h**      | 0018h                        | 0019h   | 001ah   | 001-BH   | 001ch   | 001dh   | 001eh   | 001fh   |
| **0020h**      | 0020h                        | 0021h   | 0022h   | 0023h   | 0024h   | 0025h   | 0026h   | 0027h   |
| **0028h**      | 0028h                        | 0029h   | 002ah   | 002-BH   | 002ch   | 002dh   | 002eh   | 002fh   |
| **0030h**      | 0030h                        | 0031h   | 0032h   | 0033h   | 0034h   | 0035h   | 0036h   | 0037h   |
| **0038h**      | 0038h                        | 0039h   | 003ah   | 003-BH   | 003ch   | 003dh   | 003eh   | 003fh   |
| **0040h**      | 0040h                        | 0041h   | 0042h   | 0043h   | 0044h   | 0045h   | 0046h   | 0047h   |
| **0048h**      | 0048h                        | 0049h   | 004ah   | 004-BH   | 004ch   | 004dh   | 004eh   | 004fh   |
| **0050h**      | 0050h                        | 0051h   | 0052h   | 0053h   | 0054h   | 0055h   | 0056h   | 0057h   |
| **0058h**      | 0058h                        | 0059h   | 005ah   | 005-BH   | 005ch   | 005dh   | 005eh   | 005fh   |
| **0060h**      | 0060h                        | 0041h   | 0042h   | 0043h   | 0044h   | 0045h   | 0046h   | 0047h   |
| **0068h**      | 0048h                        | 0049h   | 004ah   | 004-BH   | 004ch   | 004dh   | 004eh   | 004fh   |
| **0070h**      | 0050h                        | 0051h   | 0052h   | 0053h   | 0054h   | 0055h   | 0056h   | 0057h   |
| **0078h**      | 0058h                        | 0059h   | 005ah   | 007-BH   | 007ch   | 007dh   | 007eh   | 007fh   |
| **0080h**      | 0080h                        | 0081h   | 0082h   | 0083h   | 0084h   | 0085h   | 0086h   | 0087h   |
| **0088h**      | 0088h                        | 0089h   | 008ah   | 008-BH   | 008ch   | 008dh   | 008eh   | 008fh   |
| **0090h**      | 0090h                        | 0091h   | 0092h   | 0093h   | 0094h   | 0095h   | 0096h   | 0097h   |
| **0098h**      | 0098h                        | 0099h   | 009ah   | 009-BH   | 009ch   | 009dh   | 009eh   | 009fh   |
| **00a0h**      | 00a0h                        | 00a1h   | 00a2h   | 00a3h   | 00a4h   | 00a5h   | 00a6h   | 00a7h   |
| **00a8h**      | 00a8h                        | 00a9h   | 00aah   | 00abh   | 00ach   | 00adh   | 00aeh   | 00afh   |
| **00b0h**      | 00b0h                        | 00b1h   | 00b2h   | 00b3h   | 00b4h   | 00b5h   | 00b6h   | 00b7h   |
| **00b8h**      | 00b8h                        | 00b9h   | 00ba   | 00bbh   | 00bch   | 00bdh   | 00beh   | 00bfh   |
| **00c0h**      | 00c0h                        | 00c1h   | 00c2h   | 00c3h   | 00c4h   | 00c5h   | 00c6h   | 00c7h   |
| **00c8h**      | 00c8h                        | 00c9h   | 00cah   | 00cbh   | 00cch   | 00cdh   | 00ceh   | 00cfh   |
| **00d0h**      | 00d0h                        | 00d1h   | 00d2h   | 00d3h   | 00d4h   | 00d5h   | 00d6h   | 00d7h   |
| **00d8h**      | 00d8h                        | 00d9h   | 00dah   | 00dbh   | 00dch   | 00ddh   | 00deh   | 00dfh   |
| **00e0h**      | 00c0h                        | 00c1h   | 00c2h   | 00c3h   | 00c4h   | 00c5h   | 00c6h   | 00c7h   |
| **00e8h**      | 00c8h                        | 00c9h   | 00cah   | 00cbh   | 00cch   | 00cdh   | 00ceh   | 00cfh   |
| **00F 0h**      | 00d0h                        | 00d1h   | 00d2h   | 00d3h   | 00d4h   | 00d5h   | 00d6h   | 00F   |
| **00F 8h**      | 00d8h                        | 00d9h   | 00dah   | 00dbh   | 00dch   | 00ddh   | 00deh   | 0178h   |
| **0100h**      | 0100h                        | 0100h   | 0102h   | 0102h   | 0104h   | 0104h   | 0106h   | 0106h   |
| **0108h**      | 0108h                        | 0108h   | 010ah   | 010ah   | 010ch   | 010ch   | 010eh   | 010eh   |
| **0110h**      | 0110h                        | 0110h   | 0112h   | 0112h   | 0114h   | 0114h   | 0116h   | 0116h   |
| **0118h**      | 0118h                        | 0118h   | 011ah   | 011ah   | 011ch   | 011ch   | 011eh   | 011eh   |
| **0120h**      | 0120h                        | 0120h   | 0122h   | 0122h   | 0124h   | 0124h   | 0126h   | 0126h   |
| **0128h**      | 0128h                        | 0128h   | 012ah   | 012ah   | 012ch   | 012ch   | 012eh   | 012eh   |
| **0130h**      | 0130h                        | 0131h   | 0132h   | 0132h   | 0134h   | 0134h   | 0136h   | 0136h   |
| **0138h**      | 0138h                        | 0139h   | 0139h   | 013-BH   | 013-BH   | 013dh   | 013dh   | 013fh   |
| **0140h**      | 013fh                        | 0141h   | 0141h   | 0143h   | 0143h   | 0145h   | 0145h   | 0147h   |
| **0148h**      | 0147h                        | 0149h   | 014ah   | 014ah   | 014ch   | 014ch   | 014eh   | 014eh   |
| **0150h**      | 0150h                        | 0150h   | 0152h   | 0152h   | 0154h   | 0154h   | 0156h   | 0156h   |
| **0158h**      | 0158h                        | 0158h   | 015ah   | 015ah   | 015ch   | 015ch   | 015eh   | 015eh   |
| **0160h**      | 0160h                        | 0160h   | 0162h   | 0162h   | 0164h   | 0164h   | 0166h   | 0166h   |
| **0168h**      | 0168h                        | 0168h   | 016ah   | 016ah   | 016ch   | 016ch   | 016eh   | 016eh   |
| **0170h**      | 0170h                        | 0170h   | 0172h   | 0172h   | 0174h   | 0174h   | 0176h   | 0176h   |
| **0178h**      | 0178h                        | 0179h   | 0179h   | 017-BH   | 017-BH   | 017dh   | 017dh   | 017fh   |
| **0180h**      | 0243h                        | 0181h   | 0182h   | 0182h   | 0184h   | 0184h   | 0186h   | 0187h   |
| **0188h**      | 0187h                        | 0189h   | 018ah   | 018-BH   | 018-BH   | 018dh   | 018eh   | 018fh   |
| **0190h**      | 0190h                        | 0191h   | 0191h   | 0193h   | 0194h   | 01F 6h   | 0196h   | 0197h   |
| **0198h**      | 0198h                        | 0198h   | 023dh   | 019-BH   | 019ch   | 019dh   | 0220h   | 019fh   |
| **01a0h**      | 01a0h                        | 01a0h   | 01a2h   | 01a2h   | 01a4h   | 01a4h   | 01a6h   | 01a7h   |
| **01a8h**      | 01a7h                        | 01a9h   | 01aah   | 01abh   | 01ach   | 01ach   | 01aeh   | 01afh   |
| **01b0h**      | 01afh                        | 01b1h   | 01b2h   | 01b3h   | 01b3h   | 01b5h   | 01b5h   | 01b7h   |
| **01b8h**      | 01b8h                        | 01b8h   | 01ba   | 01bbh   | 01bch   | 01bch   | 01beh   | 01F 7H   |
| **01c0h**      | 01c0h                        | 01c1h   | 01c2h   | 01c3h   | 01c4h   | 01c5h   | 01c4h   | 01c7h   |
| **01c8h**      | 01c8h                        | 01c7h   | 01cah   | 01cbh   | 01cah   | 01cdh   | 01cdh   | 01cfh   |
| **01d0h**      | 01cfh                        | 01d1h   | 01d1h   | 01d3h   | 01d3h   | 01d5h   | 01d5h   | 01d7h   |
| **01d8h**      | 01d7h                        | 01d9h   | 01d9h   | 01dbh   | 01dbh   | 018eh   | 01deh   | 01deh   |
| **01e0h**      | 01e0h                        | 01e0h   | 01e2h   | 01e2h   | 01e4h   | 01e4h   | 01e6h   | 01e6h   |
| **01e8h**      | 01e8h                        | 01e8h   | 01eah   | 01eah   | 01ech   | 01ech   | 01eeh   | 01eeh   |
| **010h**      | 010h                        | 01F 1H   | 01F 2H   | 01F 1H   | 01F 4H   | 01F 4H   | 01F 6h   | 01F 7H   |
| **01F 8h**      | 01F 8h                        | 01F 8h   | 01fah   | 01fah   | 01F   | 01F   | 01feh   | 01feh   |
| **0200h**      | 0200h                        | 0200h   | 0202h   | 0202h   | 0204h   | 0204h   | 0206h   | 0206h   |
| **0208h**      | 0208h                        | 0208h   | 020ah   | 020ah   | 020ch   | 020ch   | 020eh   | 020eh   |
| **0210h**      | 0210h                        | 0210h   | 0212h   | 0212h   | 0214h   | 0214h   | 0216h   | 0216h   |
| **0218h**      | 0218h                        | 0218h   | 021ah   | 021ah   | 021ch   | 021ch   | 021eh   | 021eh   |
| **0220h**      | 0220h                        | 0221h   | 0222h   | 0222h   | 0224h   | 0224h   | 0226h   | 0226h   |
| **0228h**      | 0228h                        | 0228h   | 022ah   | 022ah   | 022ch   | 022ch   | 022eh   | 022eh   |
| **0230h**      | 0230h                        | 0230h   | 0232h   | 0232h   | 0234h   | 0235h   | 0236h   | 0237h   |
| **0238h**      | 0238h                        | 0239h   | 2c65h   | 023-BH   | 023-BH   | 023dh   | 2c66h   | 023fh   |
| **0240h**      | 0240h                        | 0241h   | 0241h   | 0243h   | 0244h   | 0245h   | 0246h   | 0246h   |
| **0248h**      | 0248h                        | 0248h   | 024ah   | 024ah   | 024ch   | 024ch   | 024eh   | 024eh   |
| **0250h**      | 0250h                        | 0251h   | 0252h   | 0181h   | 0186h   | 0255h   | 0189h   | 018ah   |
| **0258h**      | 0258h                        | 018fh   | 025ah   | 0190h   | 025ch   | 025dh   | 025eh   | 025fh   |
| **0260h**      | 0193h                        | 0261h   | 0262h   | 0194h   | 0264h   | 0265h   | 0266h   | 0267h   |
| **0268h**      | 0197h                        | 0196h   | 026ah   | 2c62h   | 026ch   | 026dh   | 026eh   | 019ch   |
| **0270h**      | 0270h                        | 0271h   | 019dh   | 0273h   | 0274h   | 019fh   | 0276h   | 0277h   |
| **0278h**      | 0278h                        | 0279h   | 027ah   | 027-BH   | 027ch   | 2c64h   | 027eh   | 027fh   |
| **0280h**      | 01a6h                        | 0281h   | 0282h   | 01a9h   | 0284h   | 0285h   | 0286h   | 0287h   |
| **0288h**      | 01aeh                        | 0244h   | 01b1h   | 01b2h   | 0245h   | 028dh   | 028eh   | 028fh   |
| **0290h**      | 0290h                        | 0291h   | 01b7h   | 0293h   | 0294h   | 0295h   | 0296h   | 0297h   |
| **0298h**      | 0298h                        | 0299h   | 029ah   | 029-BH   | 029ch   | 029dh   | 029eh   | 029fh   |
| **02a0h**      | 02a0h                        | 02a1h   | 02a2h   | 02a3h   | 02a4h   | 02a5h   | 02a6h   | 02a7h   |
| **02a8h**      | 02a8h                        | 02a9h   | 02aah   | 02abh   | 02ach   | 02adh   | 02aeh   | 02afh   |
| **02b0h**      | 02b0h                        | 02b1h   | 02b2h   | 02b3h   | 02b4h   | 02b5h   | 02b6h   | 02b7h   |
| **02b8h**      | 02b8h                        | 02b9h   | 02ba   | 02bbh   | 02bch   | 02bdh   | 02beh   | 02bfh   |
| **02c0h**      | 02c0h                        | 02c1h   | 02c2h   | 02c3h   | 02c4h   | 02c5h   | 02c6h   | 02c7h   |
| **02c8h**      | 02c8h                        | 02c9h   | 02cah   | 02cbh   | 02cch   | 02cdh   | 02ceh   | 02cfh   |
| **02d0h**      | 02d0h                        | 02d1h   | 02d2h   | 02d3h   | 02d4h   | 02d5h   | 02d6h   | 02d7h   |
| **02d8h**      | 02d8h                        | 02d9h   | 02dah   | 02dbh   | 02dch   | 02ddh   | 02deh   | 02dfh   |
| **02e0h**      | 02e0h                        | 02e1h   | 02e2h   | 02e3h   | 02e4h   | 02e5h   | 02e6h   | 02e7h   |
| **02e8h**      | 02e8h                        | 02e9h   | 02eah   | 02ebh   | 02ech   | 02edh   | 02eeh   | 02efh   |
| **02f 0h**      | 02f 0h                        | 02f 1H   | 02f 2H   | 02f 3H   | 02f 4H   | 02f 5h   | 02f 6h   | 02f 7H   |
| **02f 8h**      | 02f 8h                        | 02f 9H   | 02fah   | 02f   | 02f   | 02f   | 02feh   | 02ffh   |
| **0300h**      | 0300h                        | 0301h   | 0302h   | 0303h   | 0304h   | 0305h   | 0306h   | 0307h   |
| **0308h**      | 0308h                        | 0309h   | 030ah   | 030-BH   | 030ch   | 030dh   | 030eh   | 030fh   |
| **0310h**      | 0310h                        | 0311h   | 0312h   | 0313h   | 0314h   | 0315h   | 0316h   | 0317h   |
| **0318h**      | 0318h                        | 0319h   | 031ah   | 031-BH   | 031ch   | 031dh   | 031eh   | 031fh   |
| **0320h**      | 0320h                        | 0321h   | 0322h   | 0323h   | 0324h   | 0325h   | 0326h   | 0327h   |
| **0328h**      | 0328h                        | 0329h   | 032ah   | 032-BH   | 032ch   | 032dh   | 032eh   | 032fh   |
| **0330h**      | 0330h                        | 0331h   | 0332h   | 0333h   | 0334h   | 0335h   | 0336h   | 0337h   |
| **0338h**      | 0338h                        | 0339h   | 033ah   | 033-BH   | 033ch   | 033dh   | 033eh   | 033fh   |
| **0340h**      | 0340h                        | 0341h   | 0342h   | 0343h   | 0344h   | 0345h   | 0346h   | 0347h   |
| **0348h**      | 0348h                        | 0349h   | 034ah   | 034-BH   | 034ch   | 034dh   | 034eh   | 034fh   |
| **0350h**      | 0350h                        | 0351h   | 0352h   | 0353h   | 0354h   | 0355h   | 0356h   | 0357h   |
| **0358h**      | 0358h                        | 0359h   | 035ah   | 035-BH   | 035ch   | 035dh   | 035eh   | 035fh   |
| **0360h**      | 0360h                        | 0361h   | 0362h   | 0363h   | 0364h   | 0365h   | 0366h   | 0367h   |
| **0368h**      | 0368h                        | 0369h   | 036ah   | 036-BH   | 036ch   | 036dh   | 036eh   | 036fh   |
| **0370h**      | 0370h                        | 0371h   | 0372h   | 0373h   | 0374h   | 0375h   | 0376h   | 0377h   |
| **0378h**      | 0378h                        | 0379h   | 037ah   | 03f dh   | 03feh   | 03ffh   | 037eh   | 037fh   |
| **0380h**      | 0380h                        | 0381h   | 0382h   | 0383h   | 0384h   | 0385h   | 0386h   | 0387h   |
| **0388h**      | 0388h                        | 0389h   | 038ah   | 038-BH   | 038ch   | 038dh   | 038eh   | 038fh   |
| **0390h**      | 0390h                        | 0391h   | 0392h   | 0393h   | 0394h   | 0395h   | 0396h   | 0397h   |
| **0398h**      | 0398h                        | 0399h   | 039ah   | 039-BH   | 039ch   | 039dh   | 039eh   | 039fh   |
| **03a0h**      | 03a0h                        | 03a1h   | 03a2h   | 03a3h   | 03a4h   | 03a5h   | 03a6h   | 03a7h   |
| **03a8h**      | 03a8h                        | 03a9h   | 03aah   | 03abh   | 0386h   | 0388h   | 0389h   | 038ah   |
| **03b0h**      | 03b0h                        | 0391h   | 0392h   | 0393h   | 0394h   | 0395h   | 0396h   | 0397h   |
| **03b8h**      | 0398h                        | 0399h   | 039ah   | 039-BH   | 039ch   | 039dh   | 039eh   | 039fh   |
| **03c0h**      | 03a0h                        | 03a1h   | 03a3h   | 03a3h   | 03a4h   | 03a5h   | 03a6h   | 03a7h   |
| **03c8h**      | 03a8h                        | 03a9h   | 03aah   | 03abh   | 038ch   | 038eh   | 038fh   | 03cfh   |
| **03d0h**      | 03d0h                        | 03d1h   | 03d2h   | 03d3h   | 03d4h   | 03d5h   | 03d6h   | 03d7h   |
| **03d8h**      | 03d8h                        | 03d8h   | 03dah   | 03dah   | 03dch   | 03dch   | 03deh   | 03deh   |
| **03e0h**      | 03e0h                        | 03e0h   | 03e2h   | 03e2h   | 03e4h   | 03e4h   | 03e6h   | 03e6h   |
| **03e8h**      | 03e8h                        | 03e8h   | 03eah   | 03eah   | 03ech   | 03ech   | 03eeh   | 03eeh   |
| **03f 0h**      | 03f 0h                        | 03f 1H   | 03f 9H   | 03f 3H   | 03f 4H   | 03x 5h   | 03f 6h   | 03f 7H   |
| **03f 8h**      | 03f 7H                        | 03f 9H   | 03fah   | 03fah   | 03f   | 03f dh   | 03feh   | 03ffh   |
| **0400h**      | 0400h                        | 0401h   | 0402h   | 0403h   | 0404h   | 0405h   | 0406h   | 0407h   |
| **0408h**      | 0408h                        | 0409h   | 040ah   | 040-BH   | 040ch   | 040dh   | 040eh   | 040fh   |
| **0410h**      | 0410h                        | 0411h   | 0412h   | 0413h   | 0414h   | 0415h   | 0416h   | 0417h   |
| **0418h**      | 0418h                        | 0419h   | 041ah   | 041-BH   | 041ch   | 041dh   | 041eh   | 041fh   |
| **0420h**      | 0420h                        | 0421h   | 0422h   | 0423h   | 0424h   | 0425h   | 0426h   | 0427h   |
| **0428h**      | 0428h                        | 0429h   | 042ah   | 042-BH   | 042ch   | 042dh   | 042eh   | 042fh   |
| **0430h**      | 0410h                        | 0411h   | 0412h   | 0413h   | 0414h   | 0415h   | 0416h   | 0417h   |
| **0438h**      | 0418h                        | 0419h   | 041ah   | 041-BH   | 041ch   | 041dh   | 041eh   | 041fh   |
| **0440h**      | 0420h                        | 0421h   | 0422h   | 0423h   | 0424h   | 0425h   | 0426h   | 0427h   |
| **0448h**      | 0428h                        | 0429h   | 042ah   | 042-BH   | 042ch   | 042dh   | 042eh   | 042fh   |
| **0450h**      | 0400h                        | 0401h   | 0402h   | 0403h   | 0404h   | 0405h   | 0406h   | 0407h   |
| **0458h**      | 0408h                        | 0409h   | 040ah   | 040-BH   | 040ch   | 040dh   | 040eh   | 040fh   |
| **0460h**      | 0460h                        | 0460h   | 0462h   | 0462h   | 0464h   | 0464h   | 0466h   | 0466h   |
| **0468h**      | 0468h                        | 0468h   | 046ah   | 046ah   | 046ch   | 046ch   | 046eh   | 046eh   |
| **0470h**      | 0470h                        | 0470h   | 0472h   | 0472h   | 0474h   | 0474h   | 0476h   | 0476h   |
| **0478h**      | 0478h                        | 0478h   | 047ah   | 047ah   | 047ch   | 047ch   | 047eh   | 047eh   |
| **0480h**      | 0480h                        | 0480h   | 0482h   | 0483h   | 0484h   | 0485h   | 0486h   | 0487h   |
| **0488h**      | 0488h                        | 0489h   | 048ah   | 048ah   | 048ch   | 048ch   | 048eh   | 048eh   |
| **0490h**      | 0490h                        | 0490h   | 0492h   | 0492h   | 0494h   | 0494h   | 0496h   | 0496h   |
| **0498h**      | 0498h                        | 0498h   | 049ah   | 049ah   | 049ch   | 049ch   | 049eh   | 049eh   |
| **04a0h**      | 04a0h                        | 04a0h   | 04a2h   | 04a2h   | 04a4h   | 04a4h   | 04a6h   | 04a6h   |
| **04a8h**      | 04a8h                        | 04a8h   | 04aah   | 04aah   | 04ach   | 04ach   | 04aeh   | 04aeh   |
| **04b0h**      | 04b0h                        | 04b0h   | 04b2h   | 04b2h   | 04b4h   | 04b4h   | 04b6h   | 04b6h   |
| **04b8h**      | 04b8h                        | 04b8h   | 04BA   | 04BA   | 04bch   | 04bch   | 04beh   | 04beh   |
| **04c0h**      | 04c0h                        | 04c1h   | 04c1h   | 04c3h   | 04c3h   | 04c5h   | 04c5h   | 04c7h   |
| **04c8h**      | 04c7h                        | 04c9h   | 04c9h   | 04cbh   | 04cbh   | 04cdh   | 04cdh   | 04c0h   |
| **04d0h**      | 04d0h                        | 04d0h   | 04d2h   | 04d2h   | 04d4h   | 04d4h   | 04d6h   | 04d6h   |
| **04d8h**      | 04d8h                        | 04d8h   | 04dah   | 04dah   | 04dch   | 04dch   | 04deh   | 04deh   |
| **04e0h**      | 04e0h                        | 04e0h   | 04e2h   | 04e2h   | 04e4h   | 04e4h   | 04e6h   | 04e6h   |
| **04e8h**      | 04e8h                        | 04e8h   | 04eah   | 04eah   | 04ech   | 04ech   | 04eeh   | 04eeh   |
| **04f**      | 04f                        | 04f   | 04f 2   | 04f 2   | 04f 4H   | 04f 4H   | 04f 6h   | 04f 6h   |
| **04f 8**      | 04f 8                        | 04f 8   | 04fah   | 04fah   | 04f   | 04f   | 04feh   | 04feh   |
| **0500h**      | 0500h                        | 0500h   | 0502h   | 0502h   | 0504h   | 0504h   | 0506h   | 0506h   |
| **0508h**      | 0508h                        | 0508h   | 050ah   | 050ah   | 050ch   | 050ch   | 050eh   | 050eh   |
| **0510h**      | 0510h                        | 0510h   | 0512h   | 0512h   | 0514h   | 0515h   | 0516h   | 0517h   |
| **0518h**      | 0518h                        | 0519h   | 051ah   | 051-BH   | 051ch   | 051dh   | 051eh   | 051fh   |
| **0520h**      | 0520h                        | 0521h   | 0522h   | 0523h   | 0524h   | 0525h   | 0526h   | 0527h   |
| **0528h**      | 0528h                        | 0529h   | 052ah   | 052-BH   | 052ch   | 052dh   | 052eh   | 052fh   |
| **0530h**      | 0530h                        | 0531h   | 0532h   | 0533h   | 0534h   | 0535h   | 0536h   | 0537h   |
| **0538h**      | 0538h                        | 0539h   | 053ah   | 053-BH   | 053ch   | 053dh   | 053eh   | 053fh   |
| **0540h**      | 0540h                        | 0541h   | 0542h   | 0543h   | 0544h   | 0545h   | 0546h   | 0547h   |
| **0548h**      | 0548h                        | 0549h   | 054ah   | 054-BH   | 054ch   | 054dh   | 054eh   | 054fh   |
| **0550h**      | 0550h                        | 0551h   | 0552h   | 0553h   | 0554h   | 0555h   | 0556h   | 0557h   |
| **0558h**      | 0558h                        | 0559h   | 055ah   | 055-BH   | 055ch   | 055dh   | 055eh   | 055fh   |
| **0560h**      | 0560h                        | 0531h   | 0532h   | 0533h   | 0534h   | 0535h   | 0536h   | 0537h   |
| **0568h**      | 0538h                        | 0539h   | 053ah   | 053-BH   | 053ch   | 053dh   | 053eh   | 053fh   |
| **0570h**      | 0540h                        | 0541h   | 0542h   | 0543h   | 0544h   | 0545h   | 0546h   | 0547h   |
| **0578h**      | 0548h                        | 0549h   | 054ah   | 054-BH   | 054ch   | 054dh   | 054eh   | 054fh   |
| **0580h**      | 0550h                        | 0551h   | 0552h   | 0553h   | 0554h   | 0555h   | 0556h   | FFFFh   |
| **0588h**      | 17f 6h                        | 2c63h   | 1d7eh   | 1d7fh   | 1d80h   | 1d81h   | 1d82h   | 1d83h   |
| **0590h**      | 1d84 h                        | 1d85h   | 1d86h   | 1d87h   | 1d88h   | 1d89h   | 1d8ah   | 1d8bh   |
| **0598h**      | 1d8ch                        | 1d8dh   | 1d8eh   | 1d8fh   | 1d90h   | 1d91h   | 1D92 h   | 1d93 h   |
| **05a0h**      | 1d94h                        | 1d95h   | 1d96h   | 1d97h   | 1d98h   | 1d99 h   | 1d9ah   | 1d9bh   |
| **05a8h**      | 1d9ch                        | 1d9dh   | 1d9eh   | 1d9fh   | 1da0h   | 1da1h   | 1da2h   | 1da3h   |
| **05b0h**      | 1da4h                        | 1da5h   | 1da6h   | 1da7h   | 1da8h   | 1da9h   | 1daah   | 1dabh   |
| **05b8h**      | 1dach                        | 1dadh   | 1daeh   | 1dafh   | 1db0h   | 1db1h   | 1db2h   | 1db3h   |
| **05c0h**      | 1db4h                        | 1db5h   | 1db6h   | 1db7h   | 1db8h   | 1db9h   | 1dBA   | 1dbbh   |
| **05c8h**      | 1dbch                        | 1dbdh   | 1dbeh   | 1dbfh   | 1dc0h   | 1dc1h   | 1dc2h   | 1dc3h   |
| **05d0h**      | 1dc4h                        | 1dc5h   | 1dc6h   | 1dc7h   | 1dc8h   | 1dc9h   | 1 dcah   | 1dcbh   |
| **05d8h**      | 1dcch                        | 1dcdh   | 1dceh   | 1dcfh   | 1dd0h   | 1dd1h   | 1dd2h   | 1dd3h   |
| **05e0h**      | 1dd4h                        | 1dd5h   | 1dd6h   | 1dd7h   | 1dd8h   | 1dd9h   | 1ddah   | 1ddbh   |
| **05e8h**      | 1ddch                        | 1dddh   | 1ddeh   | 1ddfh   | 1DE 0h   | 1DE 1H   | 1ent2h   | 1ent3h   |
| **05f**      | 1DE 4H                        | 1Der 5h   | 1ent6h   | 1Von 7H   | 1Der 8h   | 1DE 9H   | 1DE   | 1debh   |
| **05f 8h**      | 1DE                        | 1DE dh   | 1DE eh   | 1defh   | 1df0h   | 1df1h   | 1df2h   | 1df3h   |
| **0600h**      | 1df4h                        | 1df5h   | 1df6h   | 1df7h   | 1df8h   | 1df9h   | 1dfah   | 1dfbh   |
| **0608h**      | 1dfch                        | 1dfdh   | 1dfeh   | 1dffh   | 1e00h   | 1e00h   | 1e02h   | 1e02h   |
| **0610h**      | 1e04h                        | 1e04h   | 1e06h   | 1e06h   | 1e08h   | 1e08h   | 1e0ah   | 1e0ah   |
| **0618h**      | 1e0ch                        | 1e0ch   | 1e0eh   | 1e0eh   | 1e10h   | 1e10h   | 1e12h   | 1e12h   |
| **0620h**      | 1e14h                        | 1e14h   | 1e16h   | 1e16h   | 1e18h   | 1e18h   | 1e1ah   | 1e1ah   |
| **0628h**      | 1e1ch                        | 1e1ch   | 1e1eh   | 1e1eh   | 1e20h   | 1e20h   | 1e22h   | 1e22h   |
| **0630h**      | 1e24h                        | 1e24h   | 1e26h   | 1e26h   | 1e28h   | 1e28h   | 1e2ah   | 1e2ah   |
| **0638h**      | 1e2ch                        | 1e2ch   | 1e2eh   | 1e2eh   | 1e30h   | 1e30h   | 1e32h   | 1e32h   |
| **0640h**      | 1e34h                        | 1e34h   | 1e36h   | 1e36h   | 1e38h   | 1e38h   | 1e3ah   | 1e3ah   |
| **0648h**      | 1e3ch                        | 1e3ch   | 1e3eh   | 1e3eh   | 1e40h   | 1e40h   | 1e42h   | 1e42h   |
| **0650h**      | 1e44h                        | 1e44h   | 1e46h   | 1e46h   | 1e48h   | 1e48h   | 1e4ah   | 1e4ah   |
| **0658h**      | 1e4ch                        | 1e4ch   | 1e4eh   | 1e4eh   | 1e50h   | 1e50h   | 1e52h   | 1e52h   |
| **0660h**      | 1e54h                        | 1e54h   | 1e56h   | 1e56h   | 1e58h   | 1e58h   | 1e5ah   | 1e5ah   |
| **0668h**      | 1e5ch                        | 1e5ch   | 1e5eh   | 1e5eh   | 1e60h   | 1e60h   | 1e62h   | 1e62h   |
| **0670h**      | 1e64h                        | 1e64h   | 1e66h   | 1e66h   | 1e68h   | 1e68h   | 1e6ah   | 1e6ah   |
| **0678h**      | 1e6ch                        | 1e6ch   | 1e6eh   | 1e6eh   | 1e70h   | 1e70h   | 1e72h   | 1e72h   |
| **0680h**      | 1e74h                        | 1e74h   | 1e76h   | 1e76h   | 1e78h   | 1e78h   | 1e7ah   | 1e7ah   |
| **0688h**      | 1e7ch                        | 1e7ch   | 1e7eh   | 1e7eh   | 1e80h   | 1e80h   | 1e82h   | 1e82h   |
| **0690h**      | 1e84 h                        | 1e84 h   | 1e86h   | 1e86h   | 1e88h   | 1e88h   | 1e8ah   | 1e8ah   |
| **0698h**      | 1e8ch                        | 1e8ch   | 1e8eh   | 1e8eh   | 1e90h   | 1e90h   | 1e92h   | 1e92h   |
| **06a0h**      | 1e94h                        | 1e94h   | 1e96h   | 1e97h   | 1e98h   | 1e99 h   | 1e9ah   | 1e9bh   |
| **06a8h**      | 1e9ch                        | 1e9dh   | 1e9eh   | 1e9fh   | 1ea0h   | 1ea0h   | 1ea2h   | 1ea2h   |
| **06b0h**      | 1ea4h                        | 1ea4h   | 1ea6h   | 1ea6h   | 1ea8h   | 1ea8h   | 1eaah   | 1eaah   |
| **06b8h**      | 1each                        | 1each   | 1eaeh   | 1eaeh   | 1eb0h   | 1eb0h   | 1eb2h   | 1eb2h   |
| **06c0h**      | 1eb4h                        | 1eb4h   | 1eb6h   | 1eb6h   | 1eb8h   | 1eb8h   | 1ebah   | 1ebah   |
| **06c8h**      | 1ebch                        | 1ebch   | 1ebeh   | 1ebeh   | 1ec0h   | 1ec0h   | 1ec2h   | 1ec2h   |
| **06d0h**      | 1ec4h                        | 1ec4h   | 1ec6h   | 1ec6h   | 1ec8h   | 1ec8h   | 1ecah   | 1ecah   |
| **06d8h**      | 1ecch                        | 1ecch   | 1eceh   | 1eceh   | 1ed0h   | 1ed0h   | 1ed2h   | 1ed2h   |
| **06e0h**      | 1ed4h                        | 1ed4h   | 1ed6h   | 1ed6h   | 1ed8h   | 1ed8h   | 1edah   | 1edah   |
| **06e8h**      | 1edch                        | 1edch   | 1edeh   | 1edeh   | 1ee0h   | 1ee0h   | 1ee2h   | 1ee2h   |
| **06f 0h**      | 1ee4h                        | 1ee4h   | 1ee6h   | 1ee6h   | 1ee8h   | 1ee8h   | 1eeah   | 1eeah   |
| **06f 8**      | 1eech                        | 1eech   | 1eeeh   | 1eeeh   | 1ef0h   | 1ef0h   | 1ef2h   | 1ef2h   |
| **0700h**      | 1ef4h                        | 1ef4h   | 1ef6h   | 1ef6h   | 1ef8h   | 1ef8h   | 1efah   | 1efbh   |
| **0708h**      | 1 EFCH                        | 1efdh   | 1efeh   | 1effh   | 1F 08h   | 1F-h   | 1g0ah   | 1g0bh   |
| **0710h**      | 1g0ch                        | 1F-dh   | 1g0eh   | 1F-FH   | 1F 08h   | 1F-h   | 1g0ah   | 1g0bh   |
| **0718h**      | 1g0ch                        | 1F-dh   | 1g0eh   | 1F-FH   | 1-18 h   | 1Std.   | 1F   | 1F 1Bh   |
| **0720h**      | 1F                        | 1F 1 dh   | 1X 16h   | 1Std.   | 1-18 h   | 1Std.   | 1F   | 1F 1Bh   |
| **0728h**      | 1F                        | 1F 1 dh   | 1g1eh   | 1F-FH   | 1F   | 1F-Stunde   | 1g2ah   | 1F 2BH   |
| **0730h**      | 1F                        | 1F 2DH   | 1g2eh   | 1Der 2 FH   | 1F   | 1F-Stunde   | 1g2ah   | 1F 2BH   |
| **0738h**      | 1F                        | 1F 2DH   | 1g2eh   | 1Der 2 FH   | 1F 38h   | 1F 39h   | 1F   | 1F 3BH   |
| **0740h**      | 1F                        | 1g3dh   | 1g3eh   | 1g3fh   | 1F 38h   | 1F 39h   | 1F   | 1F 3BH   |
| **0748h**      | 1F                        | 1g3dh   | 1g3eh   | 1g3fh   | 1F 48 h   | 1F 49h   | 1F   | 1F 4BH   |
| **0750h**      | 1F 4CH                        | 1F 4DH   | 1X 46h   | 1F 47h   | 1F 48 h   | 1F 49h   | 1F   | 1F 4BH   |
| **0758h**      | 1F 4CH                        | 1F 4DH   | 1F 4EH   | 1F-FH   | 1X 50h   | 1F 59h   | 1X 52h   | 1g5bh   |
| **0760h**      | 1F 54h                        | 1F 5 dh   | 1F-Stunde   | 1F-FH   | 1F 58 h   | 1F 59h   | 1F   | 1g5bh   |
| **0768h**      | 1g5ch                        | 1F 5 dh   | 1Der 5EH   | 1F-FH   | 1F 68h   | 1X 69h   | 1F 6ah   | 1F 6BH   |
| **0770h**      | 1F 6ch                        | 1F 6 dh   | 1F 6EH   | 1F 6 FH   | 1F 68h   | 1X 69h   | 1F 6ah   | 1F 6BH   |
| **0778h**      | 1F 6ch                        | 1F 6 dh   | 1F 6EH   | 1F 6 FH   | 1BA   | 1fbbh   | 1fc8h   | 1fc9h   |
| **0780h**      | 1F                        | 1fcbh   | 1Der   | 1gdbh   | 1ff8h   | 1ff9h   | 1feah   | 1febh   |
| **0788h**      | 1ffah                        | 1ffbh   | 1f.   | 1F-FH   | 1F 88 h   | 1F 89h   | 1F   | 1F-BH   |
| **0790h**      | 1F                        | 1F-dh   | 1g8eh   | 1F-FH   | 1F 88 h   | 1F 89h   | 1F   | 1F-BH   |
| **0798h**      | 1F                        | 1F-dh   | 1g8eh   | 1F-FH   | 1F 98h   | 1F 99 h   | 1g9ah   | 1g9bh   |
| **07a0h**      | 1g9ch                        | 1g9dh   | 1Der 9eh   | 1F-FH   | 1F 98h   | 1F 99 h   | 1g9ah   | 1g9bh   |
| **07a8h**      | 1g9ch                        | 1g9dh   | 1Der 9eh   | 1F-FH   | 1fa8h   | 1fa9h   | 1faah   | 1 fabh   |
| **07b0h**      | 1fach                        | 1fadh   | 1faeh   | 1afh   | 1fa8h   | 1fa9h   | 1faah   | 1 fabh   |
| **07b8h**      | 1fach                        | 1fadh   | 1faeh   | 1afh   | 1gb8h   | 1b9h   | 1-B2H   | 1bch   |
| **07c0h**      | 1bb4h                        | 1b5h   | 1bb6h   | 1b7h   | 1gb8h   | 1b9h   | 1BA   | 1fbbh   |
| **07c8h**      | 1bch                        | 1bdh   | 1Bh   | 1bfh   | 1fc0h   | 1fc1h   | 1fc2h   | 1fc3h   |
| **07d0h**      | 1fc4h                        | 1fc5h   | 1fc6h   | 1fc7h   | 1fc8h   | 1fc9h   | 1F   | 1fcbh   |
| **07d8h**      | 1fc3h                        | 1fcdh   | 1fceh   | 1fcfh   | 1F-8 h   | 1F-9H   | 1gd2h   | 1gd3h   |
| **07e0h**      | 1F-4H                        | 1gd5h   | 1F-6h   | 1gd7h   | 1F-8 h   | 1F-9H   | 1Der   | 1gdbh   |
| **07e8h**      | 1F                        | 1gddh   | 1F   | 1fädfh   | 1fe8h   | 1fe9h   | 1fe2h   | 1fe3h   |
| **07f 0h**      | 1fe4h                        | 1fech   | 1fe6h   | 1fe7h   | 1fe8h   | 1fe9h   | 1feah   | 1febh   |
| **07f 8**      | 1fech                        | 1fedh   | 1feeh   | 1fefh   | 1ff0h   | 1ff1h   | 1ff2h   | 1ff3h   |
| **0800h**      | 1ff4h                        | 1ff5h   | 1ff6h   | 1ff7h   | 1ff8h   | 1ff9h   | 1ffah   | 1ffbh   |
| **0808h**      | 1ff3h                        | 1ffdh   | 1ffeh   | 1fffh   | 2000h   | 2001h   | 2002h   | 2003h   |
| **0810h**      | 2004h                        | 2005h   | 2006h   | 2007h   | 2008h   | 2009 h   | 200Ah   | 200bh   |
| **0818h**      | 200ch                        | 200dh   | 200eh   | 200fh   | 2010h   | 2011h   | 2012h   | 2013h   |
| **0820h**      | 2014h                        | 2015h   | 2016h   | 2017h   | 2018h   | 2019h   | 201ah   | 201bh   |
| **0828h**      | 201ch                        | 201dh   | 201eh   | 201fh   | 2020h   | 2021h   | 2022h   | 2023h   |
| **0830h**      | 2024h                        | 2025h   | 2026h   | 2027h   | 2028h   | 2029h   | 202ah   | 202-BH   |
| **0838h**      | 202ch                        | 202dh   | 202eh   | 202fh   | 2030uhr   | 2031h   | 2032h   | 2033h   |
| **0840h**      | 2034h                        | 2035h   | 2036h   | 2037h   | 2038h   | 2039h   | 203ah   | 203-BH   |
| **0848h**      | 203ch                        | 203dh   | 203eh   | 203fh   | 2040h   | 2041h   | 2042h   | 2043h   |
| **0850h**      | 2044h                        | 2045h   | 2046h   | 2047h   | 2048h   | 2049h   | 204ah   | 204bh   |
| **0858h**      | 204ch                        | 204dh   | 204eh   | 204fh   | 2050h   | 2051h   | 2052h   | 2053h   |
| **0860h**      | 2054h                        | 2055h   | 2056h   | 2057h   | 2058h   | 2059h   | 205ah   | 205bh   |
| **0868h**      | 205ch                        | 205dh   | 205eh   | 205fh   | 2060h   | 2061h   | 2062h   | 2063h   |
| **0870h**      | 2064h                        | 2065h   | 2066h   | 2067h   | 2068h   | 2069h   | 206ah   | 206-BH   |
| **0878h**      | 206ch                        | 206dh   | 206eh   | 206fh   | 2070h   | 2071h   | 2072h   | 2073h   |
| **0880h**      | 2074h                        | 2075h   | 2076h   | 2077h   | 2078h   | 2079h   | 207ah   | 207-BH   |
| **0888h**      | 207ch                        | 207dh   | 207eh   | 207fh   | 2080h   | 2081h   | 2082h   | 2083h   |
| **0890h**      | 2084h                        | 2085h   | 2086h   | 2087h   | 2088h   | 2089h   | 208 ah   | 208-BH   |
| **0898h**      | 208ch                        | 208dh   | 208eh   | 208fh   | 2090h   | 2091h   | 2092h   | 2093h   |
| **08a0h**      | 2094h                        | 2095h   | 2096h   | 2097h   | 2098h   | 2099h   | 209ah   | 209bh   |
| **08a8h**      | 209ch                        | 209dh   | 209eh   | 209fh   | 20a0h   | 20a1h   | 20a2h   | 20a3h   |
| **08b0h**      | 20a4h                        | 20a5h   | 20a6h   | 20a7h   | 20a8h   | 20a9h   | 20aah   | 20 abh   |
| **08b8h**      | 20 Uhr                        | 20adh   | 20aeh   | 20afh   | 20b0h   | 20b1h   | 20b2h   | 20b3h   |
| **08c0h**      | 20b4h                        | 20b5h   | 20b6h   | 20b7h   | 20b8h   | 20b9h   | 20bah   | 20bbh   |
| **08c8h**      | 20bch                        | 20bdh   | 20 Beh   | 20bfh   | 20c0h   | 20c1h   | 20c2h   | 20c3h   |
| **08d0h**      | 20c4h                        | 20c5h   | 20c6h   | 20c7h   | 20c8h   | 20c9h   | 20 CAH   | 20cbh   |
| **08d8h**      | 20cch                        | 20cdh   | 20ceh   | 20cfh   | 20d0h   | 20d1h   | 20d2h   | 20d3h   |
| **08e0h**      | 20d4h                        | 20d5h   | 20d6h   | 20d7h   | 20d8h   | 20d9h   | 20 Mio.   | 20dbh   |
| **08e8h**      | 20dch                        | 20ddh   | 20deh   | 20dfh   | 20e0h   | 20e1h   | 20e2h   | 20e3h   |
| **08F 0h**      | 20e4h                        | 20e5h   | 20e6h   | 20e7h   | 20e8h   | 20e9h   | 20eah   | 20 EBH   |
| **08F 8h**      | 20ech                        | 20edh   | 20eeh   | 20 EFH   | 20F   | 20mm   | 20 Stunden   | 20F-   |
| **0900h**      | 20X 4H                        | 20X 5h   | 20F 6h   | 20 Stunden   | 20X 8h   | 20Uhr   | 20fah   | 20F   |
| **0908h**      | 20-fache                        | 20F   | 20 feh   | 20ffh   | 2100h   | 2101h   | 2102h   | 2103h   |
| **0910h**      | 2104h                        | 2105h   | 2106h   | 2107h   | 2108h   | 2109h   | 210 Ah   | 210bh   |
| **0918h**      | 210                        | 210dh   | 210eh   | 210fh   | 2110h   | 2111h   | 2112h   | 2113h   |
| **0920h**      | 2114h                        | 2115h   | 2116h   | 2117h   | 2118h   | 2119h   | 211ah   | 211-BH   |
| **0928h**      | 211ch                        | 211dh   | 211eh   | 211fh   | 2120h   | 2121h   | 2122h   | 2123h   |
| **0930h**      | 2124h                        | 2125h   | 2126h   | 2127h   | 2128h   | 2129h   | 212ah   | 212-BH   |
| **0938h**      | 212ch                        | 212dh   | 212eh   | 212fh   | 2130h   | 2131h   | 2132h   | 2133h   |
| **0940h**      | 2134h                        | 2135h   | 2136h   | 2137h   | 2138h   | 2139h   | 213ah   | 213-BH   |
| **0948h**      | 213ch                        | 213dh   | 213eh   | 213fh   | 2140h   | 2141h   | 2142h   | 2143h   |
| **0950h**      | 2144h                        | 2145h   | 2146h   | 2147h   | 2148h   | 2149h   | 214ah   | 214-BH   |
| **0958h**      | 214ch                        | 214dh   | 2132h   | 214fh   | 2150h   | 2151h   | 2152h   | 2153h   |
| **0960h**      | 2154h                        | 2155h   | 2156h   | 2157h   | 2158h   | 2159h   | 215 ah   | 215 BH   |
| **0968h**      | 215 ch                        | 215 DH   | 215 eh   | 215 FH   | 2160h   | 2161h   | 2162h   | 2163h   |
| **0970h**      | 2164h                        | 2165h   | 2166h   | 2167h   | 2168h   | 2169h   | 216ah   | 216-BH   |
| **0978h**      | 216ch                        | 216dh   | 216eh   | 216fh   | 2160h   | 2161h   | 2162h   | 2163h   |
| **0980h**      | 2164h                        | 2165h   | 2166h   | 2167h   | 2168h   | 2169h   | 216ah   | 216-BH   |
| **0988h**      | 216ch                        | 216dh   | 216eh   | 216fh   | 2180h   | 2181h   | 2182h   | 2183h   |
| **0990h**      | 2183h                        | FFFFh   | 034-BH   | rund um die Uhr   | rund um die Uhr   | rund um die Uhr   | rund um die Uhr   | 24BA   |
| **0998h**      | rund um die Uhr                        | rund um die Uhr   | 24bdh   | rund um die Uhr   | 24bfh   | 24c0h   | rund um die Uhr   | rund um die Uhr   |
| **09a0h**      | rund um die Uhr                        | rund um die Uhr   | rund um die Uhr   | 24c6h   | rund um die Uhr   | rund um die Uhr   | rund um die Uhr   | rund um die Uhr   |
| **09a8h**      | 24cbh                        | rund um die Uhr   | 24cdh   | 24ceh   | rund um die Uhr   | FFFFh   | 0746h   | 2c00h   |
| **09b0h**      | 2c01h                        | 2c02h   | 2c03h   | 2c04h   | 2c05h   | 2c06h   | 2c07h   | 2c08h   |
| **09b8h**      | 2c09h                        | 2c0ah   | 2c0bh   | 2c0ch   | 2c0dh   | 2c0eh   | 2c0fh   | 2c10h   |
| **09c0h**      | 2c11h                        | 2c12h   | 2c13h   | 2c14h   | 2c15h   | 2c16h   | 2c17h   | 2c18h   |
| **09c8h**      | 2c19h                        | 2c1ah   | 2c1bh   | 2c1ch   | 2c1dh   | 2c1eh   | 2c1fh   | 2c20h   |
| **09d0h**      | 2c21h                        | 2c22h   | 2c23h   | 2c24h   | 2c25h   | 2c26h   | 2c27h   | 2c28h   |
| **09d8h**      | 2c29h                        | 2c2ah   | 2c2bh   | 2c2ch   | 2c2dh   | 2c2eh   | 2c5fh   | 2c60h   |
| **09e0h**      | 2c60h                        | 2c62h   | 2c63h   | 2c64h   | 2c65h   | 2c66h   | 2c67h   | 2c67h   |
| **09e8h**      | 2c69h                        | 2c69h   | 2c6bh   | 2c6bh   | 2c6dh   | 2c6eh   | 2c6fh   | 2c70h   |
| **09F 0h**      | 2c71h                        | 2c72h   | 2c73h   | 2c74h   | 2c75h   | 2c75h   | 2c77h   | 2c78h   |
| **09F 8h**      | 2c79h                        | 2c7ah   | 2c7bh   | 2c7ch   | 2c7dh   | 2c7eh   | 2c7fh   | 2c80h   |
| **0a00h**      | 2c80h                        | 2c82h   | 2c82h   | 2c84 h   | 2c84 h   | 2c86h   | 2c86h   | 2c88h   |
| **0a08h**      | 2c88h                        | 2c8ah   | 2c8ah   | 2c8ch   | 2c8ch   | 2c8eh   | 2c8eh   | 2c90h   |
| **0a10h**      | 2c90h                        | 2c92h   | 2c92h   | 2c94h   | 2c94h   | 2c96h   | 2c96h   | 2c98h   |
| **0a18h**      | 2c98h                        | 2c9ah   | 2c9ah   | 2c9ch   | 2c9ch   | 2c9eh   | 2c9eh   | 2ca0h   |
| **0a20h**      | 2ca0h                        | 2ca2h   | 2ca2h   | 2ca4h   | 2ca4h   | 2ca6h   | 2ca6h   | 2ca8h   |
| **0a28h**      | 2ca8h                        | 2caah   | 2caah   | 2cach   | 2cach   | 2caeh   | 2caeh   | 2 CB0H   |
| **0a30h**      | 2 CB0H                        | 2cb2h   | 2cb2h   | 2cb4h   | 2cb4h   | 2cb6h   | 2cb6h   | 2cb8h   |
| **0a38h**      | 2cb8h                        | 2cba   | 2cba   | 2 cbch   | 2 cbch   | 2cbeh   | 2cbeh   | 2 cc0h   |
| **0A40 h**      | 2 cc0h                        | 2cc2h   | 2cc2h   | 2cc4h   | 2cc4h   | 2cc6h   | 2cc6h   | 2cc8h   |
| **0a48h**      | 2cc8h                        | 2ccah   | 2ccah   | 2ccch   | 2ccch   | 2cceh   | 2cceh   | 2 cd0h   |
| **0a50h**      | 2 cd0h                        | 2cd2h   | 2cd2h   | 2 cd4h   | 2 cd4h   | 2cd6h   | 2cd6h   | 2cd8h   |
| **0a58h**      | 2cd8h                        | 2cdah   | 2cdah   | 2 cdch   | 2 cdch   | 2cdeh   | 2cdeh   | 2ce0h   |
| **0a60h**      | 2ce0h                        | 2ce2h   | 2ce2h   | 2ce4h   | 2ce5h   | 2ce6h   | 2ce7h   | 2ce8h   |
| **0a68h**      | 2ce9h                        | 2ceah   | 2cebh   | 2cech   | 2cedh   | 2ceeh   | 2 cefh   | 2cf0h   |
| **0a70h**      | 2cf1h                        | 2cf2h   | 2cf3h   | 2cf4h   | 2cf5h   | 2cf6h   | 2cf7h   | 2cf8h   |
| **0a78h**      | 2cf9h                        | 2cfah   | 2cfbh   | 2cfch   | 2cfdh   | 2cfeh   | 2cffh   | 10a0h   |
| **0a80h**      | 10a1h                        | 10a2h   | 10a3h   | 10a4h   | 10a5h   | 10a6h   | 10a7h   | 10a8h   |
| **0a88h**      | 10a9h                        | 10aah   | 10abh   | 10ach   | 10adh   | 10aeh   | 10afh   | 10b0h   |
| **0a90h**      | 10b1h                        | 10b2h   | 10b3h   | 10b4h   | 10b5h   | 10b6h   | 10b7h   | 10b8h   |
| **0a98h**      | 10b9h                        | 10BA   | 10bbh   | 10bch   | 10bdh   | 10beh   | 10bfh   | 10c0h   |
| **0aa0h**      | 10c1h                        | 10c2h   | 10c3h   | 10c4h   | 10c5h   | FFFFh   | D21Bh   | FF21h   |
| **0aa8h**      | FF22h                        | FF23h   | FF24h   | FF25h   | FF26h   | FF27h   | FF28h   | FF29h   |
| **0ab0h**      | FF2Ah                        | FF2Bh   | FF2Ch   | FF2Dh   | FF2Eh   | FF2Fh   | FF30h   | FF31h   |
| **0ab8h**      | FF32h                        | FF33h   | FF34h   | FF35h   | FF36h   | FF37h   | FF38h   | FF39h   |
| **0ac0h**      | FF3Ah                        | FF5Bh   | FF5Ch   | FF5Dh   | FF5Eh   | FF5Fh   | FF60h   | FF61h   |
| **0ac8h**      | FF62h                        | FF63h   | FF64h   | FF65h   | FF66h   | FF67h   | FF68h   | FF69h   |
| **0ad0h**      | FF6Ah                        | FF6Bh   | FF6Ch   | FF6Dh   | FF6Eh   | FF6Fh   | FF70h   | FF71h   |
| **0ad8h**      | FF72h                        | FF73h   | FF74h   | FF75h   | FF76h   | FF77h   | FF78h   | FF79h   |
| **0ae0h**      | FF7Ah                        | FF7Bh   | FF7Ch   | FF7Dh   | FF7Eh   | FF7Fh   | FF80h   | FF81h   |
| **0ae8h**      | FF82h                        | FF83h   | FF84h   | FF85h   | FF86h   | FF87h   | FF88h   | FF89h   |
| **0af0h**      | FF8Ah                        | FF8Bh   | FF8Ch   | FF8Dh   | FF8Eh   | FF8Fh   | FF90h   | FF91h   |
| **0af8h**      | FF92h                        | FF93h   | FF94h   | FF95h   | FF96h   | FF97h   | FF98h   | FF99h   |
| **0b00h**      | FF9Ah                        | FF9Bh   | FF9Ch   | FF9Dh   | FF9Eh   | FF9Fh   | FFA0h   | FFA1h   |
| **0b08h**      | FFA2h                        | FFA3h   | FFA4h   | FFA5h   | FFA6h   | FFA7h   | FFA8h   | FFA9h   |
| **0b10h**      | Ffaah                        | Ffabh   | FFach   | Ffadh   | Ffaeh   | Ffafh   | FFB0h   | FFB1h   |
| **0b18h**      | FFB2h                        | FFB3h   | FFB4h   | FFB5h   | FFB6h   | FFB7h   | FFB8h   | FFB9h   |
| **0b20h**      | Ffba                        | Ffbbh   | Ffbch   | Ffbdh   | Ffbeh   | Ffbfh   | FFC0h   | FFC1h   |
| **0b28h**      | FFC2h                        | FFC3h   | FFC4h   | FFC5h   | FFC6h   | FFC7h   | FFC8h   | FFC9h   |
| **0b30h**      | Ffcah                        | Ffcbh   | Ffcch   | Ffcdh   | Ffceh   | Ffcfh   | FFD0h   | FFD1h   |
| **0b38h**      | FFD2h                        | FFD3h   | FFD4h   | FFD5h   | FFD6h   | FFD7h   | FFD8h   | FFD9h   |
| **0b40 h**      | Ffdah                        | Ffdbh   | Ffdch   | Ffddh   | Ffdeh   | Ffdfh   | FFE0h   | FFE1h   |
| **0b48h**      | FFE2h                        | FFE3h   | FFE4h   | FFE5h   | FFE6h   | FFE7h   | FFE8h   | FFE9h   |
| **0b50h**      | Ffeah                        | Ffebh   | Ffech   | Ffedh   | Ffeeh   | Ffefh   | FFF0h   | FFF1h   |
| **0b58h**      | FFF2h                        | FFF3h   | FFF4h   | FFF5h   | FFF6h   | FFF7h   | FFF8h   | FFF9h   |
| **0b60h**      | Fffah                        | Fffbh   | Fffch   | Fffdh   | Fffeh   | FFFFh   |         |         |

### <a name="73-volume-label-directory-entry"></a>7,3 Verzeichniseintrag für Volumebezeichnung

Die Volumebezeichnung ist eine Unicode-Zeichenfolge, mit der Endbenutzer ihre Speichervolumes unterscheiden können. Im exFAT-Dateisystem ist die Volumebezeichnung als kritischer primär Verzeichniseintrag im Stammverzeichnis vorhanden (siehe [Tabelle 26](#table-26-volume-label-directoryentry-structure)). Die gültige Anzahl der Verzeichniseinträge für die Volumebezeichnung liegt zwischen 0 und 1.

<div id="table-26-volume-label-directoryentry-structure" />

**Tabelle 26, Volumebezeichnung directoriyentry-Struktur**

<table>
<thead>
<tr class="header">
<th><strong>Feldname</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>Hobby</strong></p></th>
<th><p><strong>Größe</strong></p>
<p><strong>Hobby</strong></p></th>
<th><strong>Kommentare</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EntryType</td>
<td>0</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#731-entrytype-field">section 7.3.1</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>Anzahl von Charakteristika</td>
<td>1</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#732-charactercount-field">section 7.3.2</a> definiert seinen Inhalt.</td>
</tr>
<tr class="odd">
<td>VolumeLabel</td>
<td>2</td>
<td>22</td>
<td>Dieses Feld ist obligatorisch, und <a href="#733-volumelabel-field">section 7.3.3</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>Reserviert</td>
<td>24</td>
<td>8</td>
<td>Dieses Feld ist obligatorisch, und die Inhalte sind reserviert.</td>
</tr>
</tbody>
</table>

#### <a name="731-entrytype-field"></a>7.3.1 EntryType-Feld

Das EntryType-Feld muss der Definition entsprechen, die in der generischen primären DirectoryEntry-Vorlage bereitgestellt wird (siehe [Abschnitt 6.3.1](#631-entrytype-field)).

##### <a name="7311-typecode-field"></a>7.3.1.1 TypeCode-Feld

Das TypeCode-Feld muss der Definition entsprechen, die in der generischen primären DirectoryEntry-Vorlage bereitgestellt wird (siehe [Abschnitt 6.3.1.1](#6311-typecode-field)).

Für den Verzeichniseintrag Volumenbezeichnung lautet der gültige Wert für dieses Feld.
3.

##### <a name="7312-typeimportance-field"></a>7.3.1.2 typeimportance-Feld

Das typeimportance-Feld muss der Definition entsprechen, die in der generischen primären DirectoryEntry-Vorlage bereitgestellt wird (siehe [Abschnitt 6.3.1.2](#6312-typeimportance-field)).

Für den Verzeichniseintrag Volumenbezeichnung lautet der gültige Wert für dieses Feld.
0.

##### <a name="7313-typecategory-field"></a>7.3.1.3 typecategory-Feld

Das Feld typecategory muss der Definition in der generischen primären DirectoryEntry-Vorlage entsprechen (siehe [Abschnitt 6.3.1.3](#6313-typecategory-field)).

##### <a name="7314-inuse-field"></a>7.3.1.4 InUse-Feld

Das Feld "InUse" muss der Definition entsprechen, die in der generischen primären DirectoryEntry-Vorlage angegeben ist (siehe [Abschnitt 6.3.1.4](#6314-inuse-field)).

#### <a name="732-charactercount-field"></a>7.3.2 Merkmal count-Feld

Das Feld "Merkmal Anzahl" muss die Länge der Unicode-Zeichenfolge enthalten, die das VolumeLabel-Feld enthält.

Der gültige Wertebereich für dieses Feld muss wie folgt lauten:

- Mindestens 0 (null) bedeutet, dass die Unicode-Zeichenfolge 0 Zeichen lang ist (entspricht keiner Volumebezeichnung)

- Höchstens 11 bedeutet das, dass die Unicode-Zeichenfolge 11 Zeichen lang ist.

#### <a name="733-volumelabel-field"></a>7.3.3 VolumeLabel-Feld

Das VolumeLabel-Feld muss eine Unicode-Zeichenfolge enthalten, bei der es sich um den benutzerfreundlichen Namen des Volumes handelt. Das VolumeLabel-Feld enthält denselben Satz ungültiger Zeichen wie das fileName-Feld des Dateinamen-Verzeichniseintrags (siehe [Abschnitt 7.7.3](#773-filename-field)).

### <a name="74-file-directory-entry"></a>7,4-Datei Verzeichniseintrag

Datei Verzeichniseinträge beschreiben Dateien und Verzeichnisse. Dabei handelt es sich um wichtige primäre Verzeichniseinträge, und alle Verzeichnisse enthalten möglicherweise NULL oder mehr Datei Verzeichniseinträge (siehe [Tabelle 27](#table-27-file-directoryentry)). Damit ein Datei Verzeichniseintrag gültig ist, müssen genau ein Stream-Erweiterungs Verzeichniseintrag und mindestens ein Dateiname-Verzeichniseintrag direkt dem Datei Verzeichniseintrag folgen (siehe [Abschnitt 7,6](#76-stream-extension-directory-entry) bzw. [7,7](#77-file-name-directory-entry)).

<div id="table-27-file-directoryentry" />

**Tabelle 27 dateiverzeichteneintrag**

<table>
<thead>
<tr class="header">
<th><strong>Feldname</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>Hobby</strong></p></th>
<th><p><strong>Größe</strong></p>
<p><strong>Hobby</strong></p></th>
<th><strong>Kommentare</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EntryType</td>
<td>0</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#741-entrytype-field">Section Version 7.4.1</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>Secondarycount</td>
<td>1</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#742-secondarycount-field">section 7.4.2</a> definiert seinen Inhalt.</td>
</tr>
<tr class="odd">
<td>SetChecksum</td>
<td>2</td>
<td>2</td>
<td>Dieses Feld ist obligatorisch, und <a href="#743-setchecksum-field">section 7.4.3</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>FileAttributes</td>
<td>4</td>
<td>2</td>
<td>Dieses Feld ist obligatorisch, und <a href="#744-fileattributes-field">section 7.4.4</a> definiert seinen Inhalt.</td>
</tr>
<tr class="odd">
<td>Reserved1</td>
<td>6</td>
<td>2</td>
<td>Dieses Feld ist obligatorisch, und die Inhalte sind reserviert.</td>
</tr>
<tr class="even">
<td>"Kreatetimestamp"</td>
<td>8</td>
<td>4</td>
<td>Dieses Feld ist obligatorisch, und <a href="#745-createtimestamp-create10msincrement-and-createutcoffset-fields"> section 7.4.5 </
a> definiert seinen Inhalt.</td>
</tr>
<tr class="odd">
<td>LastModifiedTimestamp</td>
<td>12</td>
<td>4</td>
<td>Dieses Feld ist obligatorisch, und <a href="#746-lastmodifiedtimestamp-lastmodified10msincrement-and-lastmodifiedutcoffset-fields">section 7.4.6</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>Lastaccessedtimestamp</td>
<td>16</td>
<td>4</td>
<td>Dieses Feld ist obligatorisch, und <a href="#747-lastaccessedtimestamp-and-lastaccessedutcoffset-fields">section 7.4.7</a> definiert seinen Inhalt.</td>
</tr>
<tr class="odd">
<td>Create10msIncrement</td>
<td>20</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#745-createtimestamp-create10msincrement-and-createutcoffset-fields"> section 7.4.5 </
a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>LastModified10msIncrement</td>
<td>21</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#746-lastmodifiedtimestamp-lastmodified10msincrement-and-lastmodifiedutcoffset-fields">section 7.4.6</a> definiert seinen Inhalt.</td>
</tr>
<tr class="odd">
<td>"Kreateutcoffset"</td>
<td>22</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#745-createtimestamp-create10msincrement-and-createutcoffset-fields"> section 7.4.5 </
a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>Lastmodifiedutcoffset</td>
<td>23</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#746-lastmodifiedtimestamp-lastmodified10msincrement-and-lastmodifiedutcoffset-fields">section 7.4.6</a> definiert seinen Inhalt.</td>
</tr>
<tr class="odd">
<td>Lastaccessedutcoffset</td>
<td>24</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#747-lastaccessedtimestamp-and-lastaccessedutcoffset-fields">section 7.4.7</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>Reserved2</td>
<td>25</td>
<td>7</td>
<td>Dieses Feld ist obligatorisch, und die Inhalte sind reserviert.</td>
</tr>
</tbody>
</table>

#### <a name="741-entrytype-field"></a>Version 7.4.1 EntryType-Feld

Das EntryType-Feld muss der Definition entsprechen, die in der generischen primären DirectoryEntry-Vorlage bereitgestellt wird (siehe [Abschnitt 6.3.1](#631-entrytype-field)).

##### <a name="7411-typecode-field"></a>7.4.1.1 TypeCode-Feld

Das TypeCode-Feld muss der Definition entsprechen, die in der generischen primären DirectoryEntry-Vorlage bereitgestellt wird (siehe [Abschnitt 6.3.1.1](#6311-typecode-field)).

Für einen Datei Verzeichniseintrag ist der gültige Wert für dieses Feld 5.

##### <a name="7412-typeimportance-field"></a>7.4.1.2 typeimportance-Feld

Das typeimportance-Feld muss der Definition entsprechen, die in der generischen primären DirectoryEntry-Vorlage bereitgestellt wird (siehe [Abschnitt 6.3.1.2](#6312-typeimportance-field)).

Für einen Datei Verzeichniseintrag ist der gültige Wert für dieses Feld 0.

##### <a name="7413-typecategory-field"></a>7.4.1.3 typecategory-Feld

Das Feld typecategory muss der Definition in der generischen primären DirectoryEntry-Vorlage entsprechen (siehe [Abschnitt 6.3.1.3](#6313-typecategory-field)).

##### <a name="7414-inuse-field"></a>7.4.1.4 InUse-Feld

Das Feld "InUse" muss der Definition entsprechen, die in der generischen primären DirectoryEntry-Vorlage angegeben ist (siehe [Abschnitt 6.3.1.4](#6314-inuse-field)).

#### <a name="742-secondarycount-field"></a>7.4.2 secondarycount-Feld

Das secondarycount-Feld muss der Definition entsprechen, die in der generischen primären DirectoryEntry-Vorlage angegeben ist (siehe [Abschnitt 6.3.2](#632-secondarycount-field)).

#### <a name="743-setchecksum-field"></a>7.4.3 SetCheckSum-Feld

Das Feld SetCheckSum muss der Definition entsprechen, die in der generischen primären DirectoryEntry-Vorlage bereitgestellt wird (siehe [Abschnitt 6.3.3](#633-setchecksum-field)).

#### <a name="744-fileattributes-field"></a>Feld "7.4.4 FileAttribute"

Das Feld "FileAttribute" enthält Flags (siehe [Tabelle 28](#table-28-fileattributes-field-structure)).

<div id="table-28-fileattributes-field-structure" />

**Tabelle 28, FileAttribute-Feldstruktur**

<table>
<thead>
<tr class="header">
<th><strong>Feldname</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>trate</strong></p></th>
<th><p><strong>Größe</strong></p>
<p><strong>Bohrer</strong></p></th>
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
<td>Dieses Feld ist obligatorisch, und die Inhalte sind reserviert.</td>
</tr>
<tr class="odd">
<td>Verzeichnis</td>
<td>4</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch und entspricht der MS-DOS-Definition.</td>
</tr>
<tr class="even">
<td>Archivieren</td>
<td>5</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch und entspricht der MS-DOS-Definition.</td>
</tr>
<tr class="odd">
<td>Reserved2</td>
<td>6</td>
<td>10</td>
<td>Dieses Feld ist obligatorisch, und die Inhalte sind reserviert.</td>
</tr>
</tbody>
</table>

#### <a name="745-createtimestamp-create10msincrement-and-createutcoffset-fields"></a>Felder "7.4.5", "", "", "" und ""

In Kombination müssen die Felder "CreateTime10msIncrement" und "" das lokale Datum und die Uhrzeit beschreiben, zu denen die angegebene Datei bzw. das angegebene Verzeichnis erstellt wurde. Das Feld "" im Feld "" in der UTC-Zeit beschreibt den Offset von lokalem Datum und Uhrzeit. Implementierungen müssen diese Felder bei der Erstellung des angegebenen Verzeichniseintrags Satzes festlegen.

Diese Felder müssen den Definitionen der Felder "timestamp", "10msinkrement" und "UtcOffset" entsprechen (siehe [Abschnitt 7.4.8](#748-timestamp-fields), [section 7.4.9](#749-10msincrement-fields), bzw. [section 7.4.10](#7410-utcoffset-fields)).

#### <a name="746-lastmodifiedtimestamp-lastmodified10msincrement-and-lastmodifiedutcoffset-fields"></a>Felder "7.4.6 lastmodifiedtimestamp", "LastModified10msIncrement" und "lastmodifiedutcoffset"

In der Kombination müssen die Felder lastmodifiedtimestamp und LastModifiedTime10msIncrement das lokale Datum und die Uhrzeit beschreiben, an denen der Inhalt eines Clusters, der dem angegebenen Stream-Erweiterungs Verzeichniseintrag zugeordnet ist, zuletzt geändert wurde. Das lastmodifiedutcoffset-Feld beschreibt den Offset von lokalem Datum und Uhrzeit in UTC. Implementierungen müssen diese Felder aktualisieren:

1. Nachdem der Inhalt eines Clusters geändert wurde, der mit dem angegebenen Stream-Erweiterungs Verzeichniseintrag verknüpft ist (mit Ausnahme von Inhalten, die über den Punkt hinaus liegen, der im Feld validdatalength beschrieben wird).

2. Beim Ändern der Werte der Felder "validdatalength" oder "DATALENGTH"

Diese Felder müssen den Definitionen der Felder "timestamp", "10msinkrement" und "UtcOffset" entsprechen (siehe [Abschnitt 7.4.8](#748-timestamp-fields), [section 7.4.9](#749-10msincrement-fields), bzw. [section 7.4.10](#7410-utcoffset-fields)).

#### <a name="747-lastaccessedtimestamp-and-lastaccessedutcoffset-fields"></a>7.4.7 lastaccessedtimestamp-und lastaccessedutcoffset-Felder

Das lastaccessedtimestamp-Feld muss das lokale Datum und die Uhrzeit beschreiben, an denen der Inhalt eines Clusters, der dem angegebenen Stream-Erweiterungs Verzeichniseintrag zugeordnet ist, zuletzt aufgerufen wurde. Das lastaccessedutcoffset-Feld beschreibt den Offset von lokalem Datum und Uhrzeit in UTC.
Implementierungen müssen diese Felder aktualisieren:

1. Nachdem der Inhalt eines Clusters geändert wurde, der mit dem angegebenen Stream-Erweiterungs Verzeichniseintrag verknüpft ist (mit Ausnahme von Inhalten, die über den validdatalength-Wert hinaus vorhanden sind).

2. Beim Ändern der Werte der Felder "validdatalength" oder "DATALENGTH"

Implementierungen sollten diese Felder nach dem Lesen der Inhalte eines Clusters, der dem angegebenen Stream-Erweiterungs Verzeichniseintrag zugeordnet ist, aktualisieren.

Diese Felder müssen den Definitionen der Felder "timestamp" und "UtcOffset" entsprechen (siehe [Abschnitt 7.4.8](#748-timestamp-fields) und [section 7.4.10](#7410-utcoffset-fields)bzw.).

#### <a name="748-timestamp-fields"></a>7.4.8 Timestamp-Felder

Timestamp-Felder beschreiben lokale Datums-und Uhrzeitangabe, bis zu einer Auflösung von zwei Sekunden (siehe [Tabelle 29](#table-29-timestamp-field-structure)).

<div id="table-29-timestamp-field-structure" />

**Tabelle 29 Zeitstempel-Feldstruktur**

<table>
<thead>
<tr class="header">
<th><strong>Feldname</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>trate</strong></p></th>
<th><p><strong>Größe</strong></p>
<p><strong>Bohrer</strong></p></th>
<th><strong>Kommentare</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Doubleseconds</td>
<td>0</td>
<td>5</td>
<td>Dieses Feld ist obligatorisch, und <a href="#7481-doubleseconds-field">section 7.4.8.1</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>Minute</td>
<td>5</td>
<td>6</td>
<td>Dieses Feld ist obligatorisch, und <a href="#7482-minute-field">section 7.4.8.2</a> definiert seinen Inhalt.</td>
</tr>
<tr class="odd">
<td>Stunde</td>
<td>11</td>
<td>5</td>
<td>Dieses Feld ist obligatorisch, und <a href="#7483-hour-field">section 7.4.8.3</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>Tag</td>
<td>16</td>
<td>5</td>
<td>Dieses Feld ist obligatorisch, und <a href="#7484-day-field">section 7.4.8.4</a> definiert seinen Inhalt.</td>
</tr>
<tr class="odd">
<td>Monat</td>
<td>21</td>
<td>4</td>
<td>Dieses Feld ist obligatorisch, und <a href="#7485-month-field">section 7.4.8.5</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>Year</td>
<td>25</td>
<td>7</td>
<td>Dieses Feld ist obligatorisch, und <a href="#7486-year-field">section 7.4.8.6</a> definiert seinen Inhalt.</td>
</tr>
</tbody>
</table>

##### <a name="7481-doubleseconds-field"></a>7.4.8.1 doubleseconds-Feld

Das Feld Double seconds (Double seconds) muss den Sekunden Teil des Timestamp-Felds in zweidimensionalen vielfachen beschreiben.

Der gültige Wertebereich für dieses Feld muss wie folgt lauten:

- 0, das 0 Sekunden darstellt

- 29, das 58 Sekunden darstellt

##### <a name="7482-minute-field"></a>7.4.8.2-minütiges Feld

Im Feld Minute muss der Minuten Teil des Timestamp-Felds beschrieben werden.

Der gültige Wertebereich für dieses Feld muss wie folgt lauten:

- 0, das 0 Minuten darstellt

- 59, das 59 Minuten darstellt

##### <a name="7483-hour-field"></a>7.4.8.3 Hour-Feld

Das Stunden Feld muss den Stunden Teil des Timestamp-Felds beschreiben.

Der gültige Wertebereich für dieses Feld muss wie folgt lauten:

- 0, das 00:00 Stunden darstellt

- 23, das 23:00 Stunden darstellt

##### <a name="7484-day-field"></a>7.4.8.4 Day-Feld

Im Feld "Day" muss der Tagesabschnitt des Timestamp-Felds beschrieben werden.

Der gültige Wertebereich für dieses Feld muss wie folgt lauten:

- 1, dies ist der erste Tag des angegebenen Monats.

- Der letzte Tag des angegebenen Monats (der angegebene Monat definiert die Anzahl gültiger Tage).

##### <a name="7485-month-field"></a>7.4.8.5 month-Feld

Das Feld "Month" muss den Monats Teil des Timestamp-Felds beschreiben.

Der gültige Wertebereich für dieses Feld muss wie folgt lauten:

- Mindestens 1, das den Januar darstellt.

- Höchstens 12, was den Dezember darstellt

##### <a name="7486-year-field"></a>7.4.8.6 year-Feld

Im Feld Year muss der Jahres Anteil des Timestamp-Felds relativ zum Jahr 1980 beschrieben werden. Dieses Feld stellt das Jahr 1980 mit dem Wert 0 und dem Jahr 2107 mit dem Wert 127 dar.

Alle möglichen Werte für dieses Feld sind gültig.

#### <a name="749-10msincrement-fields"></a>7.4.9 10msinkrement-Felder

10msinkrement-Felder müssen zusätzliche Zeitauflösung für ihre entsprechenden Timestamp-Felder in 10-Millisekunden-vielfachen bereitstellen.

Der gültige Wertebereich für diese Felder muss wie folgt lauten:

- Mindestens 0, das 0 Millisekunden darstellt.

- Höchstens 199, das 1990 Millisekunden darstellt

#### <a name="7410-utcoffset-fields"></a>7.4.10 UtcOffset-Felder

UtcOffset-Felder (siehe [Tabelle 30](#table-30-utcoffset-field-structure)) beschreiben den Offset von UTC zum lokalen Datum und zur Uhrzeit der entsprechenden Zeitstempel-und 10msinkrement-Felder. Der Offset von UTC zum lokalen Datum und der Ortszeit umfasst die Auswirkungen von Zeitzonen und anderen Anpassungen bei der Datums-/uhrzeitanzeit, z. b. Sommerzeit Änderungen.

<div id="table-30-utcoffset-field-structure" />

**Tabelle 30 UtcOffset-Feldstruktur**

<table>
<thead>
<tr class="header">
<th><strong>Feldname</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>trate</strong></p></th>
<th><p><strong>Größe</strong></p>
<p><strong>Bohrer</strong></p></th>
<th><strong>Kommentare</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Offsetfromutc</td>
<td>0</td>
<td>7</td>
<td>Dieses Feld ist obligatorisch, und <a href="#74101-offsetfromutc-field">section 7.4.10.1</a>definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>Offsetvalid</td>
<td>7</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#74102-offsetvalid-field">section 7.4.10.2</a> definiert seinen Inhalt.</td>
</tr>
</tbody>
</table>

##### <a name="74101-offsetfromutc-field"></a>7.4.10.1 offsetfromutc-Feld

Das Feld offsetfromutc muss den Offset von UTC des lokalen Datums und der Uhrzeit beschreiben, in der der zugehörige Zeitstempel und die 10msinkrement-Felder enthalten sind.
In diesem Feld wird der Offset von UTC in 15-Minuten-Intervallen beschrieben (siehe Tabelle 31).

<div id="table-31-meaning-of-the-values-of-the-offsetfromutc-field" />

**Tabelle 31 Bedeutung der Werte für das Feld "offsetfromutc"**

<table>
<thead>
<tr class="header">
<th><strong>Wert</strong></th>
<th><strong>Dezimaltrennzeichen mit Vorzeichen</strong></th>
<th><strong>Beschreibung</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>3fh</td>
<td>63</td>
<td>Lokaler Zeitpunkt (Datum und Uhrzeit) ist UTC + 15:45</td>
</tr>
<tr class="even">
<td>3EH</td>
<td>62</td>
<td>Lokaler Zeitpunkt (Datum und Uhrzeit) ist UTC + 15:30</td>
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
<td>Lokaler Zeitpunkt (Datum und Uhrzeit) ist UTC + 00:15</td>
</tr>
<tr class="odd">
<td>Werktagen</td>
<td>0</td>
<td>Lokale Datums-und uhrzeitanzeit ist UTC</td>
</tr>
<tr class="even">
<td>7Fh</td>
<td>-1</td>
<td>Lokaler Zeitpunkt (Datum und Uhrzeit) ist UTC – 00:15</td>
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
<td>Lokaler Zeitpunkt (Datum und Uhrzeit) ist UTC – 15:45</td>
</tr>
<tr class="odd">
<td>40 h</td>
<td>-64</td>
<td>Lokaler Zeitpunkt (Datum und Uhrzeit) ist UTC – 16:00</td>
</tr>
</tbody>
</table>

Wie in der obigen Tabelle angegeben, sind alle möglichen Werte für dieses Feld gültig. Allerdings sollten Implementierungen den Wert Werktagen für dieses Feld nur dann aufzeichnen, wenn Folgendes der Fall ist:

1. Das lokale Datum und die Uhrzeit stimmen mit der UTC überein. in diesem Fall muss der Wert des offsetvalid-Felds 1 lauten.

2. Lokale Datums-und uhrzeitanzeiten sind nicht bekannt. in diesem Fall sollte der Wert des offsetvalid-Felds 1 lauten, und Implementierungen müssen UTC als lokales Datum und Uhrzeit festlegen.

3. Die UTC ist nicht bekannt. in diesem Fall muss der Wert des offsetvalid-Felds "0" lauten.

Wenn der Offset für die lokale Datums-und Uhrzeit Abweichung von UTC nicht ein Vielfaches von 15 Minuten ist, dann müssen die Implementierungen Werktagen im Feld offsetfromutc aufzeichnen und die UTC als lokales Datum und eine Uhrzeit in Erwägung gezogen werden.

##### <a name="74102-offsetvalid-field"></a>7.4.10.2 offsetvalid-Feld

Das Feld offsetvalid soll wie folgt beschreiben, ob der Inhalt des offsetfromutc-Felds gültig ist oder nicht:

- 0 (null) bedeutet, dass der Inhalt des offsetfromutc-Felds ungültig ist.
    > und müssen Werktagen sein.

- 1. Dies bedeutet, dass der Inhalt des offsetfromutc-Felds gültig ist.

Implementierungen sollten dieses Feld nur auf den Wert 0 festlegen, wenn UTC nicht zum Berechnen des Werts des offsetfromutc-Felds verfügbar ist. Wenn dieses Feld den Wert 0 (null) enthält, müssen die Implementierungen die timestamp-und 10msinkrement-Felder als UTC-Offset mit dem aktuellen lokalen Datum und der aktuellen Uhrzeit behandeln.

### <a name="75-volume-guid-directory-entry"></a>7,5 Volume GUID-Verzeichniseintrag

Der VolumeGuid-Verzeichniseintrag enthält eine GUID, die es Implementierungen ermöglicht, Volumes eindeutig und Programm gesteuert zu unterscheiden.
Die VolumeGuid ist als nicht [verarbeitbarer](#table-32-volume-guid-directoryentry)primär Verzeichniseintrag im Stammverzeichnis vorhanden (siehe Tabelle 32). Die gültige Anzahl von VolumeGuid-Verzeichnis Einträgen liegt zwischen 0 und 1.

<div id="table-32-volume-guid-directoryentry" />

**Tabelle 32 Volume GUID Directoren Entry**

<table>
<thead>
<tr class="header">
<th><strong>Feldname</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>Hobby</strong></p></th>
<th><p><strong>Größe</strong></p>
<p><strong>Hobby</strong></p></th>
<th><strong>Kommentare</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EntryType</td>
<td>0</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#751-entrytype-field">section 7.5.1</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>Secondarycount</td>
<td>1</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#752-secondarycount-field">section 7.5.2</a> definiert seinen Inhalt.</td>
</tr>
<tr class="odd">
<td>SetChecksum</td>
<td>2</td>
<td>2</td>
<td>Dieses Feld ist obligatorisch, und <a href="#753-setchecksum-field">section 7.5.3</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>Generalprimaryflags</td>
<td>4</td>
<td>2</td>
<td>Dieses Feld ist obligatorisch, und <a href="#754-generalprimaryflags-field">section 7.5.4</a> definiert seinen Inhalt.</td>
</tr>
<tr class="odd">
<td>VolumeGuid</td>
<td>6</td>
<td>16</td>
<td>Dieses Feld ist obligatorisch, und <a href="#755-volumeguid-field">section 7.5.5</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>Reserviert</td>
<td>22</td>
<td>10</td>
<td>Dieses Feld ist obligatorisch, und die Inhalte sind reserviert.</td>
</tr>
</tbody>
</table>

#### <a name="751-entrytype-field"></a>7.5.1 EntryType-Feld

Das EntryType-Feld muss der Definition entsprechen, die in der generischen primären DirectoryEntry-Vorlage bereitgestellt wird (siehe [Abschnitt 6.3.1](#631-entrytype-field)).

##### <a name="7511-typecode-field"></a>7.5.1.1 TypeCode-Feld

Das TypeCode-Feld muss der Definition entsprechen, die in der generischen primären DirectoryEntry-Vorlage bereitgestellt wird (siehe [Abschnitt 6.3.1.1](#6311-typecode-field)).

Für den Volume GUID-Verzeichniseintrag lautet der gültige Wert für dieses Feld.
0.

##### <a name="7512-typeimportance-field"></a>7.5.1.2 typeimportance-Feld

Das typeimportance-Feld muss der Definition entsprechen, die in der generischen primären DirectoryEntry-Vorlage bereitgestellt wird (siehe [Abschnitt 6.3.1.2](#6312-typeimportance-field)).

Für den Volume GUID-Verzeichniseintrag lautet der gültige Wert für dieses Feld.
1.

##### <a name="7513-typecategory-field"></a>7.5.1.3 typecategory-Feld

Das Feld typecategory muss der Definition in der generischen primären DirectoryEntry-Vorlage entsprechen (siehe [Abschnitt 6.3.1.3](#6313-typecategory-field)).

##### <a name="7514-inuse-field"></a>7.5.1.4 InUse-Feld

Das Feld "InUse" muss der Definition entsprechen, die in der generischen primären DirectoryEntry-Vorlage angegeben ist (siehe [Abschnitt 6.3.1.4](#6314-inuse-field)).

#### <a name="752-secondarycount-field"></a>"7.5.2 secondarycount"-Feld

Das secondarycount-Feld muss der Definition entsprechen, die in der generischen primären DirectoryEntry-Vorlage angegeben ist (siehe [Abschnitt 6.3.2](#632-secondarycount-field)).

Für den Volume GUID-Verzeichniseintrag lautet der gültige Wert für dieses Feld.
0.

#### <a name="753-setchecksum-field"></a>7.5.3 SetCheckSum-Feld

Das Feld SetCheckSum muss der Definition entsprechen, die in der generischen primären DirectoryEntry-Vorlage bereitgestellt wird (siehe [Abschnitt 6.3.3](#633-setchecksum-field)).

#### <a name="754-generalprimaryflags-field"></a>7.5.4 generalprimaryflags-Feld

Das Feld "generalprimaryflags" muss der in der generischen primären DirectoryEntry-Vorlage bereitgestellten Definition entsprechen (siehe [Abschnitt 6.3.4](#634-generalprimaryflags-field)) und definiert den Inhalt des zu reservierenden customdefined-Felds.

##### <a name="7541-allocationpossible-field"></a>7.5.4.1-Feld (Zuordnung möglich)

Das Feld "zugsmöglichkeit" muss der Definition in der generischen primären DirectoryEntry-Vorlage entsprechen (siehe [Abschnitt 6.3.4.1](#6341-allocationpossible-field)).

Für den Volume GUID-Verzeichniseintrag lautet der gültige Wert für dieses Feld.
0.

##### <a name="7542-nofatchain-field"></a>7.5.4.2 nofatchain-Feld

Das Feld nofatchain muss der Definition entsprechen, die in der generischen primären DirectoryEntry-Vorlage bereitgestellt wird (siehe [Abschnitt 6.3.4.2](#6342-nofatchain-field)).

#### <a name="755-volumeguid-field"></a>7.5.5 VolumeGuid-Feld

Das Feld VolumeGuid muss eine GUID enthalten, durch die das angegebene Volume eindeutig identifiziert wird.

Alle möglichen Werte für dieses Feld sind gültig, außer der NULL-GUID, die ist {00000000-0000-0000-0000-000000000000} .

### <a name="76-stream-extension-directory-entry"></a>7,6 Stream-Erweiterungs Verzeichniseintrag

Der Stream-Erweiterungs Verzeichniseintrag ist ein wichtiger Eintrag für ein sekundäres Verzeichnis in Datei Verzeichnis-Eintrags Sätzen (siehe [Tabelle 33](#table-33-stream-extension-directoryentry)). Die gültige Anzahl von Stream-Erweiterungs Verzeichnis Einträgen in einem Datei Verzeichnis-Eintrags Satz ist 1.
Außerdem ist dieser Verzeichniseintrag nur gültig, wenn er unmittelbar auf den Eintrag im Datei Verzeichnis folgt.

<div id="table-33-stream-extension-directoryentry" />

**Tabelle 33 Datenstrom Erweiterung Director Entry**

<table>
<thead>
<tr class="header">
<th><strong>Feldname</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>Hobby</strong></p></th>
<th><p><strong>Größe</strong></p>
<p><strong>Hobby</strong></p></th>
<th><strong>Kommentare</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EntryType</td>
<td>0</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#761-entrytype-field">section 7.6.1</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>Generalsecondaryflags</td>
<td>1</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#762-generalsecondaryflags-field">section 7.6.2</a> definiert seinen Inhalt.</td>
</tr>
<tr class="odd">
<td>Reserved1</td>
<td>2</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und die Inhalte sind reserviert.</td>
</tr>
<tr class="even">
<td>NameLength</td>
<td>3</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#763-namelength-field">section 7.6.3</a> definiert seinen Inhalt.</td>
</tr>
<tr class="odd">
<td>Namehash</td>
<td>4</td>
<td>2</td>
<td>Dieses Feld ist obligatorisch, und <a href="#764-namehash-field">section 7.6.4</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>Reserved2</td>
<td>6</td>
<td>2</td>
<td>Dieses Feld ist obligatorisch, und die Inhalte sind reserviert.</td>
</tr>
<tr class="odd">
<td>Validdatalength</td>
<td>8</td>
<td>8</td>
<td>Dieses Feld ist obligatorisch, und <a href="#765-validdatalength-field">section 7.6.5</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>"Reserved3"</td>
<td>16</td>
<td>4</td>
<td>Dieses Feld ist obligatorisch, und die Inhalte sind reserviert.</td>
</tr>
<tr class="odd">
<td>Firstcluster</td>
<td>20</td>
<td>4</td>
<td>Dieses Feld ist obligatorisch, und <a href="#766-firstcluster-field">section 7.6.6</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>DataLength</td>
<td>24</td>
<td>8</td>
<td>Dieses Feld ist obligatorisch, und <a href="#767-datalength-field">section 7.6.7</a> definiert seinen Inhalt.</td>
</tr>
</tbody>
</table>

#### <a name="761-entrytype-field"></a>7.6.1 EntryType-Feld

Das EntryType-Feld muss der in der generischen sekundären DirectoryEntry-Vorlage bereitgestellten Definition entsprechen (siehe [Abschnitt 6.4.1](#641-entrytype-field)).

##### <a name="7611-typecode-field"></a>7.6.1.1 TypeCode-Feld

Das TypeCode-Feld muss der Definition in der generischen sekundären DirectoryEntry-Vorlage entsprechen (siehe [Abschnitt 6.4.1.1](#6411-typecode-field)).

Für den Verzeichniseintrag für die Datenstrom Erweiterung lautet der gültige Wert für dieses Feld 0.

##### <a name="7612-typeimportance-field"></a>7.6.1.2 typeimportance-Feld

Das typeimportance-Feld muss der Definition in der generischen sekundären DirectoryEntry-Vorlage entsprechen (siehe [Abschnitt 6.4.1.2](#6412-typeimportance-field)).

Für den Verzeichniseintrag für die Datenstrom Erweiterung lautet der gültige Wert für dieses Feld 0.

##### <a name="7613-typecategory-field"></a>7.6.1.3 typecategory-Feld

Das Feld typecategory muss der Definition in der generischen sekundären DirectoryEntry-Vorlage entsprechen (siehe [Abschnitt 6.4.1.3](#6413-typecategory-field)).

##### <a name="7614-inuse-field"></a>7.6.1.4 InUse-Feld

Das InUse-Feld muss der Definition entsprechen, die in der generischen sekundären DirectoryEntry-Vorlage bereitgestellt wird (siehe [Abschnitt 6.4.1.4](#6414-inuse-field)).

#### <a name="762-generalsecondaryflags-field"></a>7.6.2 generalsecondaryflags-Feld

Das Feld generalsecondaryflags muss der Definition in der generischen sekundären DirectoryEntry-Vorlage entsprechen (siehe [Abschnitt 6.4.2](#642-generalsecondaryflags-field)) und definiert den Inhalt des zu reservierenden customdefined-Felds.

##### <a name="7621-allocationpossible-field"></a>7.6.2.1-Feld (Zuordnung möglich)

Das Feld "zugsmöglichkeit" muss der Definition entsprechen, die in der generischen Vorlage "DirectoryEntry" bereitgestellt wird (siehe [Abschnitt 6.4.2.1](#6421-allocationpossible-field)).

Für den Verzeichniseintrag für die Datenstrom Erweiterung lautet der gültige Wert für dieses Feld 1.

##### <a name="7622-nofatchain-field"></a>7.6.2.2 nofatchain-Feld

Das Feld nofatchain muss der Definition entsprechen, die in der generischen Vorlage für sekundäre DirectoryEntry bereitgestellt wird (siehe [Abschnitt 6.4.2.2](#6422-nofatchain-field)).

#### <a name="763-namelength-field"></a>7.6.3-namelength-Feld

Das Feld "namelength" muss die Länge der Unicode-Zeichenfolge der nachfolgenden Dateinamen-Verzeichniseinträge (siehe [Abschnitt 7,7](#77-file-name-directory-entry)) enthalten, die zusammen enthalten sind.

Der gültige Wertebereich für dieses Feld muss wie folgt lauten:

- Mindestens 1, dies ist der kürzeste mögliche Dateiname.

- Höchstens 255, dies ist der am längsten mögliche Dateiname.

Der Wert des Felds "namelength" wirkt sich auch auf die Anzahl der Dateinamen-Verzeichniseinträge aus (siehe [Abschnitt 7,7](#77-file-name-directory-entry)).

#### <a name="764-namehash-field"></a>7.6.4 namehash-Feld

Das Feld "namehash" muss einen 2-Byte-Hash (siehe [Abbildung 4](#figure-4-namehash-computation)) mit dem Namen der Dateinamen enthalten. Dies ermöglicht es Implementierungen, bei der Suche nach einer Datei anhand des Namens einen schnellen Vergleich durchzuführen. Wichtig ist, dass der namehash eine sichere Überprüfung eines Konflikts bereitstellt. Implementierungen überprüfen, ob alle namehash-Übereinstimmungen mit einem Vergleich mit dem Dateinamen in der uploschreibung übereinstimmen.

<div id="figure-4-namehash-computation" />

**Abbildung 4 namehash-Berechnung**

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

#### <a name="765-validdatalength-field"></a>7.6.5 validdatalength-Feld

Im Feld validdatalength muss beschrieben werden, wie weit die Datenstrom-Benutzerdaten geschrieben wurden. Implementierungen müssen dieses Feld aktualisieren, wenn Sie Daten weiter in den Datenstream schreiben. Auf dem Speichermedium sind die Daten zwischen der gültigen Daten Länge und der Daten Länge des Datenstroms nicht definiert. Implementierungen müssen Nullen für Lesevorgänge zurückgeben, die über die gültige Daten Länge hinausgehen.

Wenn der entsprechende Datei Verzeichniseintrag ein Verzeichnis beschreibt, ist der einzige gültige Wert für dieses Feld gleich dem Wert des Felds DATALENGTH. Andernfalls sollte der Bereich gültiger Werte für dieses Feld wie folgt lauten:

- Mindestens 0 (null) bedeutet, dass keine Benutzerdaten in den Datenstrom geschrieben wurden.

- Höchstens DATALENGTH bedeutet, dass Benutzerdaten in die gesamte Länge des Datenstroms geschrieben wurden.

#### <a name="766-firstcluster-field"></a>7.6.6 firstcluster-Feld

Das Feld "firstcluster" muss der Definition entsprechen, die in der generischen Vorlage für sekundäre DirectoryEntry bereitgestellt wird (siehe [Abschnitt 6.4.3](#643-firstcluster-field)).

Dieses Feld muss den Index des ersten Clusters des Datenstroms enthalten, der die Benutzerdaten hostet.

#### <a name="767-datalength-field"></a>7.6.7 DATALENGTH-Feld

Das DATALENGTH-Feld muss der Definition entsprechen, die in der generischen sekundären DirectoryEntry-Vorlage bereitgestellt wird (siehe [Abschnitt 6.4.4](#644-datalength-field)).

Wenn im entsprechenden Datei Verzeichniseintrag ein Verzeichnis beschrieben wird, ist der gültige Wert für dieses Feld die gesamte Größe der zugeordneten Zuordnung (in Bytes), die 0 (null) sein kann. Für Verzeichnisse beträgt der Maximalwert für dieses Feld 256 MB.

### <a name="77-file-name-directory-entry"></a>7,7 Dateinamen Verzeichniseintrag

Dateiname-Verzeichniseinträge sind wichtige Einträge für sekundäre Verzeichnisse in Datei Verzeichniseintrags Sätzen (siehe [Tabelle 34](#table-34-file-name-directoryentry)). Die gültige Anzahl von Dateinamen-Verzeichnis Einträgen in einem Datei Verzeichniseintrags Satz ist "namelength/15", aufgerundet auf die nächste ganze Zahl. Außerdem sind Dateinamen-Verzeichniseinträge nur gültig, wenn Sie unmittelbar auf den Verzeichniseintrag für die Datenstrom Erweiterung als aufeinander folgende Reihe folgen. Dateinamen Verzeichniseinträge werden kombiniert, um den Dateinamen für den Eintrag für den Datei Verzeichniseintrag zu bilden.

Alle untergeordneten Elemente eines bestimmten Verzeichniseintrags verfügen über eindeutige Verzeichniseintrags Sätze für Dateinamen. Das heißt, es dürfen keine doppelten Datei-oder Verzeichnisnamen nach der Groß-/Kleinschreibung in einem Verzeichnis vorhanden sein.

<div id="table-34-file-name-directoryentry" />

**Tabelle 34, Dateiname Directoren Entry**

<table>
<thead>
<tr class="header">
<th><strong>Feldname</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>Hobby</strong></p></th>
<th><p><strong>Größe</strong></p>
<p><strong>Hobby</strong></p></th>
<th><strong>Kommentare</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EntryType</td>
<td>0</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#771-entrytype-field">section 7.7.1</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>Generalsecondaryflags</td>
<td>1</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#772-generalsecondaryflags-field">section 7.7.2</a> definiert seinen Inhalt.</td>
</tr>
<tr class="odd">
<td>FileName</td>
<td>2</td>
<td>30</td>
<td>Dieses Feld ist obligatorisch, und <a href="#773-filename-field">section 7.7.3</a> definiert seinen Inhalt.</td>
</tr>
</tbody>
</table>

#### <a name="771-entrytype-field"></a>7.7.1 EntryType-Feld

Das EntryType-Feld muss der in der generischen sekundären DirectoryEntry-Vorlage bereitgestellten Definition entsprechen (siehe [Abschnitt 6.4.1](#641-entrytype-field)).

##### <a name="7711-typecode-field"></a>7.7.1.1 TypeCode-Feld

Das TypeCode-Feld muss der Definition in der generischen sekundären DirectoryEntry-Vorlage entsprechen (siehe [Abschnitt 6.4.1.1](#6411-typecode-field)).

Für den Verzeichniseintrag für die Datenstrom Erweiterung lautet der gültige Wert für dieses Feld 1.

##### <a name="7712-typeimportance-field"></a>7.7.1.2 typeimportance-Feld

Das typeimportance-Feld muss der Definition in der generischen sekundären DirectoryEntry-Vorlage entsprechen (siehe [Abschnitt 6.4.1.2](#6412-typeimportance-field)).

Für den Verzeichniseintrag für die Datenstrom Erweiterung lautet der gültige Wert für dieses Feld 0.

##### <a name="7713-typecategory-field"></a>7.7.1.3 typecategory-Feld

Das Feld typecategory muss der Definition in der generischen sekundären DirectoryEntry-Vorlage entsprechen (siehe [Abschnitt 6.4.1.3](#6413-typecategory-field)).

##### <a name="7714-inuse-field"></a>7.7.1.4 InUse-Feld

Das InUse-Feld muss der Definition entsprechen, die in der generischen sekundären DirectoryEntry-Vorlage bereitgestellt wird (siehe [Abschnitt 6.4.1.4](#6414-inuse-field)).

#### <a name="772-generalsecondaryflags-field"></a>7.7.2 generalsecondaryflags-Feld

Das Feld generalsecondaryflags muss der Definition in der generischen sekundären DirectoryEntry-Vorlage entsprechen (siehe [Abschnitt 6.4.2](#642-generalsecondaryflags-field)) und definiert den Inhalt des zu reservierenden customdefined-Felds.

##### <a name="7721-allocationpossible-field"></a>7.7.2.1-Feld (Zuordnung möglich)

Das Feld "zugsmöglichkeit" muss der Definition entsprechen, die in der generischen Vorlage "DirectoryEntry" bereitgestellt wird (siehe [Abschnitt 6.4.2.1](#6421-allocationpossible-field)).

Für den Verzeichniseintrag für die Datenstrom Erweiterung lautet der gültige Wert für dieses Feld 0.

##### <a name="7722-nofatchain-field"></a>7.7.2.2 nofatchain-Feld

Das Feld nofatchain muss der Definition entsprechen, die in der generischen Vorlage für sekundäre DirectoryEntry bereitgestellt wird (siehe [Abschnitt 6.4.2.2](#6422-nofatchain-field)).

#### <a name="773-filename-field"></a>7.7.3 fileName-Feld

Das fileName-Feld muss eine Unicode-Zeichenfolge enthalten, bei der es sich um einen Teil des Datei namens handelt. In den Order File Name Directory-Einträge sind in einem Datei Verzeichniseintrags Satz enthalten. Dateiname Felder werden verkettet, um den Dateinamen für den Eintrags Satz des Dateiverzeichnisses zu bilden. Bei Angabe der Länge des filename-Felds, von 15 Zeichen und der maximalen Anzahl der Einträge im Dateinamen Verzeichnis 17 beträgt die maximale Länge des endgültigen, verketteten Datei namens
255.

Der verketteten Dateiname hat denselben Satz von ungültigen Zeichen wie andere FAT-basierte Dateisysteme (siehe [Tabelle 35](#table-35-invalid-filename-characters)). Implementierungen sollten die nicht verwendeten Zeichen von Dateiname-Feldern auf den Wert 0000H festlegen.

<div id="table-35-invalid-filename-characters" />

**Tabelle 35 ungültige Dateinamen Zeichen**

| **Zeichen Code** | **Beschreibung** | **Zeichen Code** | **Beschreibung**   | **Zeichen Code** | **Beschreibung** |
|--------------------|-----------------|--------------------|-------------------|--------------------|-----------------|
| 0000H              | Steuerungs Code    | 0001h              | Steuerungs Code      | 0002h              | Steuerungs Code    |
| 0003h              | Steuerungs Code    | 0004h              | Steuerungs Code      | 0005h              | Steuerungs Code    |
| 0006h              | Steuerungs Code    | 0007h              | Steuerungs Code      | 0008h              | Steuerungs Code    |
| 0009h              | Steuerungs Code    | 000ah              | Steuerungs Code      | 000bh              | Steuerungs Code    |
| 000ch              | Steuerungs Code    | 000dh              | Steuerungs Code      | 000eh              | Steuerungs Code    |
| 000fh              | Steuerungs Code    | 0010h              | Steuerungs Code      | 0011h              | Steuerungs Code    |
| 0012h              | Steuerungs Code    | 0013h              | Steuerungs Code      | 0014h              | Steuerungs Code    |
| 0015h              | Steuerungs Code    | 0016h              | Steuerungs Code      | 0017h              | Steuerungs Code    |
| 0018h              | Steuerungs Code    | 0019h              | Steuerungs Code      | 001ah              | Steuerungs Code    |
| 001-BH              | Steuerungs Code    | 001ch              | Steuerungs Code      | 001dh              | Steuerungs Code    |
| 001eh              | Steuerungs Code    | 001fh              | Steuerungs Code      | 0022h              | Anführungszeichen  |
| 002ah              | Asterisk        | 002fh              | Schrägstrich     | 003ah              | Doppelpunkt           |
| 003ch              | Kleiner-als-Zeichen  | 003eh              | Größer-als-Zeichen | 003fh              | Fragezeichen   |
| 005ch              | Umgekehrter Schrägstrich      | 007ch              | Senkrechter Strich      |                    |                 |

Die Dateinamen "." und ".." haben die besondere Bedeutung von "this Directory" bzw. "enthaltende Verzeichnis". Implementierungen dürfen keinen dieser reservierten Dateinamen im Feld Dateiname aufzeichnen.
Allerdings können Implementierungen diese beiden Dateinamen in Verzeichnislisten generieren, um auf das Verzeichnis zu verweisen, das aufgeführt wird, und das enthaltende Verzeichnis.

Implementierungen möchten Datei-und Verzeichnisnamen möglicherweise nur auf den ASCII-Zeichensatz beschränken. Wenn dies der Fall ist, sollten Sie die Zeichen Verwendung auf den Bereich gültiger Zeichen in den ersten 128 Unicode-Einträgen beschränken. Sie müssen weiterhin Datei-und Verzeichnisnamen in Unicode auf dem Volume speichern und bei der Schnittstellen mit dem Benutzer in bzw. aus ASCII/Unicode konvertieren.

### <a name="78-vendor-extension-directory-entry"></a>7,8 Anbieter-Erweiterungs Verzeichniseintrag

Der Anbieter Erweiterungs Verzeichniseintrag ist ein unfreundliches sekundäres Verzeichniseintrag in Datei Verzeichniseintrags Sätzen (siehe [Tabelle 36](#table-36-vendor-extension-directoryentry)). Ein Datei Verzeichnis-Eintrags Satz kann eine beliebige Anzahl von Anbieter-Erweiterungs Verzeichnis Einträgen enthalten, bis zum Limit sekundärer Verzeichniseinträge, abzüglich der Anzahl der anderen sekundären Verzeichniseinträge. Außerdem sind Lieferanten Erweiterungs Verzeichniseinträge nur gültig, wenn Sie nicht den erforderlichen Datenstrom Erweiterungen und Dateinamen Verzeichniseinträge vorangestellt sind.

Anbieter Erweiterungs Verzeichniseinträge ermöglichen es Anbietern, eindeutige, herstellerspezifische Verzeichniseinträge in einzelnen Datei Verzeichnis Einträgen über das VendorGUID-Feld zu haben (siehe [Tabelle 36](#table-36-vendor-extension-directoryentry)). Eindeutige Verzeichniseinträge ermöglichen es Anbietern, das exFAT-Dateisystem zu erweitern. Anbieter können den Inhalt des Felds vendordefined definieren (siehe [Tabelle 36](#table-36-vendor-extension-directoryentry)). Anbieter Implementierungen können den Inhalt des Felds vendordefined beibehalten und herstellerspezifische Funktionen bereitstellen.

Implementierungen, die nicht die GUID eines Lieferanten Erweiterungs Verzeichnisses erkennen, müssen den Verzeichniseintrag genauso wie alle anderen nicht erkannten, nicht erkannten, nicht erkannten sekundären Verzeichniseinträge behandeln (siehe [Abschnitt 8,2](#82-implications-of-unrecognized-directory-entries)).

<div id="table-36-vendor-extension-directoryentry" />

**Tabelle 36 Hersteller Erweiterung DirectoryEntry**

<table>
<thead>
<tr class="header">
<th><strong>Feldname</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>Hobby</strong></p></th>
<th><p><strong>Größe</strong></p>
<p><strong>Hobby</strong></p></th>
<th><strong>Kommentare</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EntryType</td>
<td>0</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#781-entrytype-field">section 7.8.1</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>Generalsecondaryflags</td>
<td>1</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#782-generalsecondaryflags-field">section 7.8.2</a> definiert seinen Inhalt.</td>
</tr>
<tr class="odd">
<td>VendorGUID</td>
<td>2</td>
<td>16</td>
<td>Dieses Feld ist obligatorisch, und <a href="#783-vendorguid-field">section 7.8.3</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>VendorDefined</td>
<td>18</td>
<td>14</td>
<td>Dieses Feld ist obligatorisch, und die Anbieter können ihren Inhalt definieren.</td>
</tr>
</tbody>
</table>

#### <a name="781-entrytype-field"></a>7.8.1 EntryType-Feld

Das EntryType-Feld muss der in der generischen sekundären DirectoryEntry-Vorlage bereitgestellten Definition entsprechen (siehe [Abschnitt 6.4.1](#641-entrytype-field)).

##### <a name="7811-typecode-field"></a>7.8.1.1 TypeCode-Feld

Das TypeCode-Feld muss der Definition in der generischen sekundären DirectoryEntry-Vorlage entsprechen (siehe [Abschnitt 6.4.1.1](#6411-typecode-field)).

Für den Verzeichniseintrag Lieferanten Erweiterung ist der gültige Wert für dieses Feld 0.

##### <a name="7812-typeimportance-field"></a>7.8.1.2 typeimportance-Feld

Das typeimportance-Feld muss der Definition in der generischen sekundären DirectoryEntry-Vorlage entsprechen (siehe [Abschnitt 6.4.1.2](#6412-typeimportance-field)).

Für den Verzeichniseintrag Lieferanten Erweiterung lautet der gültige Wert für dieses Feld 1.

##### <a name="7813-typecategory-field"></a>7.8.1.3 typecategory-Feld

Das Feld typecategory muss der Definition in der generischen sekundären DirectoryEntry-Vorlage entsprechen (siehe [Abschnitt 6.4.1.3](#6413-typecategory-field)).

##### <a name="7814-inuse-field"></a>7.8.1.4 InUse-Feld

Das InUse-Feld muss der Definition entsprechen, die in der generischen sekundären DirectoryEntry-Vorlage bereitgestellt wird (siehe [Abschnitt 6.4.1.4](#6414-inuse-field)).

#### <a name="782-generalsecondaryflags-field"></a>7.8.2 generalsecondaryflags-Feld

Das Feld generalsecondaryflags muss der Definition in der generischen sekundären DirectoryEntry-Vorlage entsprechen (siehe [Abschnitt 6.4.2](#642-generalsecondaryflags-field)) und definiert den Inhalt des zu reservierenden customdefined-Felds.

##### <a name="7821-allocationpossible-field"></a>7.8.2.1-Feld (Zuordnung möglich)

Das Feld "zugsmöglichkeit" muss der Definition entsprechen, die in der generischen Vorlage "DirectoryEntry" bereitgestellt wird (siehe [Abschnitt 6.4.2.1](#6421-allocationpossible-field)).

Für den Verzeichniseintrag Lieferanten Erweiterung ist der gültige Wert für dieses Feld 0.

##### <a name="7822-nofatchain-field"></a>7.8.2.2 nofatchain-Feld

Das Feld nofatchain muss der Definition entsprechen, die in der generischen Vorlage für sekundäre DirectoryEntry bereitgestellt wird (siehe [Abschnitt 6.4.2.2](#6422-nofatchain-field)).

#### <a name="783-vendorguid-field"></a>7.8.3 VendorGUID-Feld

Das Feld VendorGUID muss eine GUID enthalten, die die angegebene Lieferanten Erweiterung eindeutig identifiziert.

Alle möglichen Werte für dieses Feld sind gültig, außer der NULL-GUID, die ist {00000000-0000-0000-0000-000000000000} . Allerdings sollten die Anbieter ein Tool mit GUID-Generierungs Tool, wie z. b. GuidGen.exe, verwenden, um beim Definieren der Erweiterungen eine GUID auszuwählen.

Der Wert dieses Felds bestimmt die herstellerspezifische Struktur des vendordefined-Felds.

### <a name="79-vendor-allocation-directory-entry"></a>7,9 Hersteller Zuordnungs Verzeichniseintrag

Der Eintrag des Lieferanten Zuordnungs Verzeichnisses ist ein nicht ordnungsgemäß sekundäres Verzeichniseintrag in Datei Verzeichnis-Eintrags Sätzen (siehe [Tabelle 37](#table-37-vendor-allocation-directoryentry)). Ein Datei Verzeichnis-Eintrags Satz kann eine beliebige Anzahl von Zuordnungen für Lieferanten Zuordnungs Verzeichnisse enthalten, bis zum Grenzwert für sekundäre Verzeichniseinträge, abzüglich der Anzahl der anderen sekundären Verzeichniseinträge. Außerdem sind die Einträge des Lieferanten Zuordnungs Verzeichnisses nur gültig, wenn Sie nicht den erforderlichen Datenstrom Erweiterungen und Dateinamen Verzeichniseinträge vorangestellt sind.

Hersteller Zuordnungs Verzeichnis-Einträge ermöglichen es Anbietern, eindeutige, herstellerspezifische Verzeichniseinträge in einzelnen Datei Verzeichnis Einträgen über das VendorGUID-Feld zu haben (siehe [Tabelle 37](#table-37-vendor-allocation-directoryentry)). Eindeutige Verzeichniseinträge ermöglichen es Anbietern, das exFAT-Dateisystem zu erweitern. Anbieter können den Inhalt der zugeordneten Cluster definieren, sofern vorhanden. Anbieter Implementierungen behalten ggf. den Inhalt der zugehörigen Cluster bei und stellen möglicherweise anbieterspezifische Funktionen bereit.

Bei Implementierungen, die die GUID eines Lieferanten Zuordnungs Verzeichnisses nicht erkennen, muss der Verzeichniseintrag genauso behandelt werden wie alle anderen nicht erkannten, nicht erkannten, nicht erkannten sekundären Verzeichniseinträge (siehe [Abschnitt 8,2](#82-implications-of-unrecognized-directory-entries)).

<div id="table-37-vendor-allocation-directoryentry" />

**Tabelle 37 Hersteller Zuweisungs Verzeichnis**

<table>
<thead>
<tr class="header">
<th><strong>Feldname</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>Hobby</strong></p></th>
<th><p><strong>Größe</strong></p>
<p><strong>Hobby</strong></p></th>
<th><strong>Kommentare</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EntryType</td>
<td>0</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#791-entrytype-field">section 7.9.1</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>Generalsecondaryflags</td>
<td>1</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch, und <a href="#792-generalsecondaryflags-field">section 7.9.2</a> definiert seinen Inhalt.</td>
</tr>
<tr class="odd">
<td>VendorGUID</td>
<td>2</td>
<td>16</td>
<td>Dieses Feld ist obligatorisch, und <a href="#793-vendorguid-field">section 7.9.3</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>VendorDefined</td>
<td>18</td>
<td>2</td>
<td>Dieses Feld ist obligatorisch, und die Anbieter können ihren Inhalt definieren.</td>
</tr>
<tr class="odd">
<td>Firstcluster</td>
<td>20</td>
<td>4</td>
<td>Dieses Feld ist obligatorisch, und <a href="#794-firstcluster-field">section 7.9.4</a> definiert seinen Inhalt.</td>
</tr>
<tr class="even">
<td>DataLength</td>
<td>24</td>
<td>8</td>
<td>Dieses Feld ist obligatorisch, und <a href="#795-datalength-field">section 7.9.5</a> definiert seinen Inhalt.</td>
</tr>
</tbody>
</table>

#### <a name="791-entrytype-field"></a>7.9.1 EntryType-Feld

Das EntryType-Feld muss der in der generischen sekundären DirectoryEntry-Vorlage bereitgestellten Definition entsprechen (siehe [Abschnitt 6.4.1](#641-entrytype-field)).

##### <a name="7911-typecode-field"></a>7.9.1.1 TypeCode-Feld

Das TypeCode-Feld muss der Definition in der generischen sekundären DirectoryEntry-Vorlage entsprechen (siehe [Abschnitt 6.4.1.1](#6411-typecode-field)).

Für den Eintrag des Lieferanten Zuordnungs Verzeichnisses lautet der gültige Wert für dieses Feld 1.

##### <a name="7912-typeimportance-field"></a>7.9.1.2 typeimportance-Feld

Das typeimportance-Feld muss der Definition in der generischen sekundären DirectoryEntry-Vorlage entsprechen (siehe [Abschnitt 6.4.1.2](#6412-typeimportance-field)).

Für den Eintrag des Lieferanten Zuordnungs Verzeichnisses lautet der gültige Wert für dieses Feld 1.

##### <a name="7913-typecategory-field"></a>7.9.1.3 typecategory-Feld

Das Feld typecategory muss der Definition in der generischen sekundären DirectoryEntry-Vorlage entsprechen (siehe [Abschnitt 6.4.1.3](#6413-typecategory-field)).

##### <a name="7914-inuse-field"></a>7.9.1.4 InUse-Feld

Das InUse-Feld muss der Definition entsprechen, die in der generischen sekundären DirectoryEntry-Vorlage bereitgestellt wird (siehe [Abschnitt 6.4.1.4](#6414-inuse-field)).

#### <a name="792-generalsecondaryflags-field"></a>7.9.2 generalsecondaryflags-Feld

Das Feld generalsecondaryflags muss der Definition in der generischen sekundären DirectoryEntry-Vorlage entsprechen (siehe [Abschnitt 6.4.2](#642-generalsecondaryflags-field)) und definiert den Inhalt des zu reservierenden customdefined-Felds.

##### <a name="7921-allocationpossible-field"></a>7.9.2.1-Feld (Zuordnung möglich)

Das Feld "zugsmöglichkeit" muss der Definition entsprechen, die in der generischen Vorlage "DirectoryEntry" bereitgestellt wird (siehe [Abschnitt 6.4.2.1](#6421-allocationpossible-field)).

Für den Eintrag des Lieferanten Zuordnungs Verzeichnisses lautet der gültige Wert für dieses Feld 1.

##### <a name="7922-nofatchain-field"></a>7.9.2.2 nofatchain-Feld

Das Feld nofatchain muss der Definition entsprechen, die in der generischen Vorlage für sekundäre DirectoryEntry bereitgestellt wird (siehe [Abschnitt 6.4.2.2](#6422-nofatchain-field)).

#### <a name="793-vendorguid-field"></a>7.9.3 VendorGUID-Feld

Das Feld VendorGUID muss eine GUID enthalten, die die angegebene Lieferanten Zuordnung eindeutig identifiziert.

Alle möglichen Werte für dieses Feld sind gültig, außer der NULL-GUID, die ist {00000000-0000-0000-0000-000000000000} . Allerdings sollten die Anbieter ein Tool mit GUID-Generierungs Tool, wie z. b. GuidGen.exe, verwenden, um beim Definieren der Erweiterungen eine GUID auszuwählen.

Der Wert dieses Felds bestimmt die herstellerspezifische Struktur der Inhalte der zugeordneten Cluster, sofern vorhanden.

#### <a name="794-firstcluster-field"></a>7.9.4 firstcluster-Feld

Das Feld "firstcluster" muss der Definition entsprechen, die in der generischen Vorlage für sekundäre DirectoryEntry bereitgestellt wird (siehe [Abschnitt 6.4.3](#643-firstcluster-field)).

#### <a name="795-datalength-field"></a>7.9.5 DATALENGTH-Feld

Das DATALENGTH-Feld muss der Definition entsprechen, die in der generischen sekundären DirectoryEntry-Vorlage bereitgestellt wird (siehe [Abschnitt 6.4.4](#644-datalength-field)).

### <a name="710-texfat-padding-directory-entry"></a>7,10 texfat Padding-Verzeichniseintrag

In dieser Spezifikation, exFAT Revision 1,00 File System Basic Specification, wird der Verzeichniseintrag texfat Padding nicht definiert. Allerdings ist der Typcode 1, und seine typwichtigkeit ist 1. Bei Implementierungen dieser Spezifikation müssen Text-Auffüll Verzeichniseinträge genauso behandelt werden wie alle anderen nicht erkannten, nicht erkannten primär Verzeichniseinträge. Implementierungen dürfen keine texfat-Padding-Verzeichniseinträge verschieben.

## <a name="8-implementation-notes"></a>8 Implementierungs Hinweise

### <a name="81-recommended-write-ordering"></a>8,1 Empfohlene Schreib Reihenfolge

Implementierungen sollten sicherstellen, dass das Volume so robust wie möglich ist, um Fehler und andere unvermeidbare Fehler zu beheben. Wenn Sie neue Verzeichniseinträge erstellen oder Cluster Zuordnungen ändern, sollten Implementierungen in der Regel dieser Schreib Reihenfolge folgen:

1. Legen Sie den Wert des Felds VolumeDirty auf 1 fest.

2. Aktualisieren Sie ggf. das aktive FAT.

3. Aktualisieren der Bitmap für die aktive Zuordnung

4. Erstellen oder aktualisieren Sie ggf. den Verzeichniseintrag.

5. Löschen Sie den Wert des Felds VolumeDirty auf 0, wenn der Wert vor dem ersten Schritt 0 war.

Wenn Sie Verzeichniseinträge löschen oder Cluster Zuordnungen freigeben, sollten Implementierungen dieser Schreib Reihenfolge folgen:

1. Legen Sie den Wert des Felds VolumeDirty auf 1 fest.

2. Löschen oder aktualisieren Sie ggf. den Verzeichniseintrag.

3. Aktualisieren Sie ggf. das aktive FAT.

4. Aktualisieren der Bitmap für die aktive Zuordnung

5. Löschen Sie den Wert des Felds VolumeDirty auf 0, wenn der Wert vor dem ersten Schritt 0 war.

### <a name="82-implications-of-unrecognized-directory-entries"></a>8,2 Auswirkungen unbekannter Verzeichniseinträge

Zukünftige exFAT-Spezifikationen mit derselben Haupt Revisionsnummer, 1 und einer neben Versionsnummer oberhalb von 0, können neue, unwesentliche primäre, sekundäre und unwichtige sekundäre Verzeichniseinträge definieren. Nur mit exFAT-Spezifikationen einer höheren wichtigen Revisionsnummer können neue wichtige primäre Verzeichniseinträge definiert werden. Implementierungen dieser Spezifikation, exFAT Revision 1,00 File System Basic Specification, sollten in der Lage sein, alle exFAT-Volumes mit der Haupt Revisionsnummer 1 und jede kleinere Revisionsnummer bereitzustellen und darauf zuzugreifen. In diesem Szenario werden Szenarios dargestellt, in denen eine Implementierung möglicherweise Verzeichniseinträge erkennt, die nicht erkannt werden. Im folgenden werden die Auswirkungen dieser Szenarios beschrieben:

1. Das vorhanden sein unbekannter kritischer primär Verzeichniseinträge im Stammverzeichnis rendert das Volume als ungültig. Wenn ein kritischer primär Verzeichniseintrag mit Ausnahme von Datei Verzeichnis Einträgen in einem anderen Verzeichnis als dem Stammverzeichnis vorhanden ist, wird das Hostingverzeichnis ungültig.

2. Bei Implementierungen dürfen keine unbekannten nicht erkannten primär Verzeichniseinträge oder die zugehörigen Cluster Zuordnungen geändert werden. Wenn jedoch ein Verzeichnis gelöscht wird und nur beim Löschen eines Verzeichnisses, werden von den Implementierungen nicht erkannte, nicht erkannte primär Verzeichniseinträge gelöscht und ggf. alle zugeordneten Cluster Zuordnungen freigegeben.

3. Bei Implementierungen dürfen keine unbekannten kritischen sekundären Verzeichniseinträge oder die zugehörigen Cluster Zuordnungen geändert werden. Wenn ein oder mehrere nicht erkannte wichtige sekundäre Verzeichniseinträge in einem Verzeichniseintrags Satz vorhanden sind, wird der gesamte Verzeichniseintrags Satz nicht erkannt. Beim Löschen eines Verzeichniseintrags Satzes, der mindestens ein unbekanntes, nicht erkanntes Verzeichnis enthält, werden von den Implementierungen alle Cluster Zuordnungen freigegeben, sofern vorhanden, die nicht erkannten kritischen sekundären Verzeichnis Einträgen zugeordnet sind.
   Wenn der Verzeichniseintrags Satz ein Verzeichnis beschreibt, können Implementierungen folgende Aktionen ausführen:

   - Wechseln Sie in das Verzeichnis.

   - Auflisten der enthaltenen Verzeichniseinträge

   - Enthaltene Verzeichniseinträge löschen

   - Verschieben von enthaltenen Verzeichnis Einträgen in ein anderes Verzeichnis

   Implementierungen dürfen jedoch nicht:

   - Ändern Sie enthaltene Verzeichniseinträge mit Ausnahme von DELETE, wie bereits erwähnt.

   - Neue enthaltene Verzeichniseinträge erstellen

   - Öffnen Sie enthaltene Verzeichniseinträge, außer durchsuchen und auflisten, wie bereits erwähnt.

4. In-Implementierungen dürfen nicht erkannte, nicht erkannte sekundäre Verzeichniseinträge oder die zugehörigen Cluster Zuordnungen nicht geändert werden.
   Bei Implementierungen sollten nicht erkannte, nicht erkannte sekundäre Verzeichniseinträge ignoriert werden. Beim Löschen eines Verzeichniseintrags Satzes müssen Implementierungen alle Cluster Zuordnungen freigeben, sofern vorhanden, die nicht erkannten, nicht erkannten, nicht vorhandenen Verzeichnis Einträgen zugeordnet sind.

## <a name="9-file-system-limits"></a>9 Datei System Limits

### <a name="91-sector-size-limits"></a>9,1 Sektorgrößen Limits

Das bytespersectorshift-Feld definiert die unteren und oberen Sektorgrößen Limits (was den **unteren Grenzwert ergibt: 512 Bytes; Obergrenze: 4.096 Bytes**).

### <a name="92-cluster-size-limits"></a>9,2 Cluster Größen Limits

Das Feld sectorsperclustershift definiert die unteren und oberen Cluster Größen Limits (**untere Grenze: 1 Sektor; obere Grenze: 25--bytespersectorshift-Sektoren**, die bis zu 32 MB ausgewertet werden).

### <a name="93-cluster-heap-size-limits"></a>9,3 Größenbeschränkungen für Cluster Heaps

Der Cluster Heap muss mindestens über genügend Speicherplatz verfügen, um die folgenden grundlegenden Dateisystem Strukturen zu hosten: das Stammverzeichnis, alle Zuordnungs Bitmaps und die up-Case-Tabelle.

Die geringere Größenbeschränkung für Cluster Heaps ist eine Funktion der niedrigeren Größenbeschränkung für jede der grundlegenden Dateisystem Strukturen, die sich im Cluster Heap befinden. Trotz des kleinsten möglichen Clusters (512 Bytes) benötigt jede der grundlegenden Dateisystem Strukturen nicht mehr als einen Cluster. Daher ist der **untere Grenzwert: 2 + numoffats Clusters**, der je nach dem Wert des Felds "zahloffats" entweder 3 oder 4 Cluster ergibt.

Die maximale Größe des Cluster Heaps ist eine einfache Funktion der maximal möglichen Anzahl von Clustern, die das Feld "clustercount" definiert (**Obergrenze: 2 <sup>32</sup>-11-Cluster**). Unabhängig von der Clustergröße verfügt ein solcher Cluster Heap über genügend Speicherplatz, um die grundlegenden Dateisystem Strukturen zumindest zu hosten.

### <a name="94-volume-size-limits"></a>9,4 volumegrößenlimits

Das volumelength-Feld definiert die unteren und oberen volumegrößengrenzen (untere Grenze: **2 <sup>20</sup>/2 <sup>bytespersectorshift</sup>-Sektoren**, die auf 1 MB ausgewertet werden). **Obergrenze: 2 <sup>64</sup>-1 Sektoren**, bei denen die größtmögliche Sektorgröße bei ungefähr 64KB ergibt. Diese Spezifikation empfiehlt jedoch nicht mehr als 2<sup>24</sup>-2-Cluster im Cluster Heap (siehe [Abschnitt 3.1.9](#319-clustercount-field)). Daher ist die empfohlene Obergrenze für ein Volume: clusterheapoffset + (2<sup>24</sup>-2) \* 2<sup>Sector sperclustershift</sup>. Mit der größtmöglichen Clustergröße, 32 MB und der Annahme, dass "clusterheapoffset" eine Größe von 96 MB hat (ausreichend Speicherplatz für die Haupt-und Sicherungs Startbereiche und nur das erste FAT), wird die empfohlene Obergrenze für ein Volume auf ungefähr 512 TB ausgewertet.

### <a name="95-directory-size-limits"></a>9,5 Größenbeschränkungen für Verzeichnisse

Das DATALENGTH-Feld des Stream-Erweiterungs Verzeichniseintrags definiert die unteren und oberen Verzeichnis Größen Limits (**untere Grenze: 0 Bytes; Obergrenze: 256 MB**). Dies bedeutet, dass ein Verzeichnis bis zu 8.388.608 Verzeichniseinträge hostet (jeder Verzeichniseintrag beansprucht 32 Bytes). Im kleinsten möglichen Datei Verzeichniseintrags Satz werden drei Verzeichniseinträge, ein Verzeichnis kann bis zu 2.796.202 Dateien hosten.

## <a name="10-appendix"></a>10 Anhang

### <a name="101-globally-unique-identifiers-guids"></a>10,1 Global Unique Identifier (GUIDs)

Eine GUID ist die Microsoft-Implementierung eines universell eindeutigen Bezeichners. Eine GUID ist ein 128-Bit-Wert, der aus einer Gruppe von 8 hexadezimalen Ziffern, gefolgt von drei Gruppen mit vier hexadezimalen Ziffern, gefolgt von einer Gruppe von 12 hexadezimalen Ziffern, z. b. {6B29FC40-CA47-1067-B31D-00DD010662DA}, besteht (siehe [Tabelle 38](#table-38-guid-structure)).

<div id="table-38-guid-structure" />

**Tabelle 38 GUID-Struktur**

<table>
<thead>
<tr class="header">
<th><strong>Feldname</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>Hobby</strong></p></th>
<th><p><strong>Größe</strong></p>
<p><strong>Satz</strong></p></th>
<th><strong>Kommentare</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Data1</td>
<td>0</td>
<td>4</td>
<td>Dieses Feld ist obligatorisch und enthält die vier Bytes aus der ersten Gruppe der GUID (6B29FC40 h aus dem Beispiel).</td>
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
<td>Dieses Feld ist obligatorisch und enthält die zwei Bytes aus der dritten Gruppe der GUID (1067h aus dem Beispiel).</td>
</tr>
<tr class="even">
<td>Data4 [0]</td>
<td>8</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch und enthält das signifikanteste Byte aus der vierten Gruppe der GUID (B3h aus dem Beispiel).</td>
</tr>
<tr class="odd">
<td>Data4 [1]</td>
<td>9</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch und enthält das am wenigsten signifikante Byte aus der vierten Gruppe der GUID (1DH aus dem Beispiel).</td>
</tr>
<tr class="even">
<td>Data4 [2]</td>
<td>10</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch und enthält das erste Byte aus der fünften Gruppe der GUID (00H aus dem Beispiel).</td>
</tr>
<tr class="odd">
<td>Data4 [3]</td>
<td>11</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch und enthält das zweite Byte aus der fünften Gruppe der GUID (DDH aus dem Beispiel).</td>
</tr>
<tr class="even">
<td>Data4 [4]</td>
<td>12</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch und enthält das dritte Byte aus der fünften Gruppe der GUID (01h aus dem Beispiel).</td>
</tr>
<tr class="odd">
<td>Data4 [5]</td>
<td>13</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch und enthält das vierte Byte aus der fünften Gruppe der GUID (06h aus dem Beispiel).</td>
</tr>
<tr class="even">
<td>Data4 [6]</td>
<td>14</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch und enthält das fünfte Byte aus der fünften Gruppe der GUID (62h aus dem Beispiel).</td>
</tr>
<tr class="odd">
<td>Data4 [7]</td>
<td>15</td>
<td>1</td>
<td>Dieses Feld ist obligatorisch und enthält das sechste Byte aus der fünften Gruppe der GUID (DAh aus dem Beispiel).</td>
</tr>
</tbody>
</table>

### <a name="102-partition-tables"></a>10,2-Partitionstabellen

Um die Interoperabilität von exFAT-Volumes in einer Vielzahl von Verwendungs Szenarien sicherzustellen, sollten Implementierungen den Partitionstyp 07h für den partitionierten MBR-Speicher und die Partitions-GUID {EBD0A0A2-B9E5-4433-87C0-68B6B72699C7} für den GPT-partitionierten Speicher verwenden.

## <a name="11-documentation-change-history"></a>11 Änderungs Verlauf der Dokumentation

In Tabelle 39 wird der Verlauf von Releases, Korrekturen, Ergänzungen, Ergänzungen und Erläuterungen zu diesem Dokument beschrieben.

<div id="table-39-documentation-change-history" />

**Tabelle 39 Dokumentations Änderungs Verlauf**

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
<td><p>Erste Version der grundlegenden Spezifikation, die Folgendes umfasst:</p>
<blockquote>
<p>Abschnitt 1, Einführung</p>
<p>Abschnitt 2,<br />
Volumestruktur</p>
<p>Bereich 3, Haupt-und Sicherungs Startbereiche</p>
<p>Abschnitt 4, Bereich "Datei Zuordnungs Tabelle"</p>
<p>Abschnitt 5, Datenbereich</p>
<p>Abschnitt 6, Verzeichnisstruktur</p>
<p>Abschnitt 7, Verzeichniseintrags Definitionen</p>
<p>Abschnitt 8, Implementierungs Hinweise</p>
<p>Abschnitt 9, Datei System Limits</p>
<p>Abschnitt 10, Anhang</p>
</blockquote></td>
</tr>
<tr class="even">
<td>08-Jun-2008</td>
<td><p>Zweite Version der grundlegenden Spezifikation, die die folgenden Änderungen umfasst:</p>
<blockquote>
<p>Hinzufügung von Abschnitt 11,<br />
Verlauf der Dokumentations Änderung</p>
<p>Hinzufügen der Lieferanten Erweiterung und der Lieferanten Zuordnungs Verzeichnisse in den Abschnitten 7,8 und 7,9</p>
<p>Hinzufügen der empfohlenen up-Case-Tabelle in den Abschnitten 7.2.5 und 7.2.5.1</p>
<p>Hinzufügen der UtcOffset-Felder in Abschnitt 7,4 und Hinzufügen des UTC-Akronyms in Abschnitt 1,3</p>
<p>Korrektur der Größe des customdefined-Felds in Tabelle 19</p>
<p>Korrektur des gültigen Bereichs von namelength-Werten im Abschnitt 7.6.3</p>
<p>Korrektur und Erläuterung der Timestamp-und 10msinkrement-Felder im Abschnitt 7,4</p>
<p>Erläuterung der NULL-Parameter Struktur in Abschnitt 3,3</p>
<p>Erläuterung der Bedeutung der Werte des Felds nofatchain im Abschnitt 6.3.4.2</p>
<p>Erläuterung der Bedeutung der Werte des Felds "DATALENGTH" im Abschnitt "6.2.3"</p>
<p>Erläuterungen zum VolumeDirty-Feld im Abschnitt 3.1.13.2 und empfohlene Schreib Reihenfolge in Abschnitt 8,1</p>
<p>Erläuterung des Felds "mediafailure" im Abschnitt "3.1.13.3"</p>
</blockquote></td>
</tr>
<tr class="odd">
<td>01-Oct-2008</td>
<td><p>Dritte Version der grundlegenden Spezifikation, die die folgenden Änderungen umfasst:</p>
<blockquote>
<p>Hinzufügen der Erläuterungen zu</p>
<p>Hinzufügen von UTC-Definitionen in Tabelle 2, Abschnitt 1,3</p>
<p>Geänderte Abschnitte 1,5, um die Ausrichtung mit dem texfat-Spezifikationsdokument sicherzustellen.</p>
<p>Verdeutlichte die Einschränkung, dass nur Microsoft das Layout der Verzeichniseinträge in Abschnitt 6,2 definieren kann.</p>
<p>Es wurde klar, dass das Feld "firstcluster" 0 (null) sein muss, wenn "DATALENGTH" den Wert "0" hat und nofatchain auf "section 6.3.5</p>
<p>Erläuterte Anforderungen für gültige Datei Verzeichniseinträge im Abschnitt 7,4</p>
<p>Anforderung für eindeutige Datei-und Verzeichnisnamen zu Abschnitt 7,7 hinzugefügt</p>
<p>Implementierungs Hinweis für ASCII bis zum Ende des Abschnitts 7.7.3 hinzugefügt</p>
</blockquote></td>
</tr>
<tr class="even">
<td>01-Jan-2009</td>
<td><p>Vierte Version der grundlegenden Spezifikation, die die folgenden Änderungen umfasst:</p>
<blockquote>
<p>Verweise auf Windows CE Access Control Einträge entfernt.</p>
<p>Es wurde eine Erläuterung zum Abschnitt 7.2.5.1 hinzugefügt, um explizit eine vollständige auffüllungs Tabelle anzufordern</p>
</blockquote></td>
</tr>
<tr class="odd">
<td>02-Sep-2009</td>
<td><p>Fünfte Version der grundlegenden Spezifikation, die die folgenden Änderungen umfasst:</p>
<blockquote>
<p>Dokument Formatierungs Änderungen, um eine bessere PDF-Konvertierung zuzulassen</p>
</blockquote></td>
</tr>
<tr class="even">
<td>24-Feb-2010</td>
<td><p>Sechste Version der grundlegenden Spezifikation, die die folgenden Änderungen umfasst:</p>
<blockquote>
<p>Geänderte falsche Anweisung: "das Feld ' firstcluster ' muss NULL sein, wenn ' DATALENGTH ' den Wert ' 0 ' aufweist und nofatchain" im Abschnitt 6.3.5 und im Abschnitt 6.4.3 auf "festgelegt ist. wenn das nofatchain-Bit 1 ist, muss firstcluster auf einen gültigen Cluster im Cluster Heap zeigen.</p>
<p>"", Wenn das nofatchain-Bit 1 ist, darf "DATALENGTH" nicht gleich NULL sein. Wenn das Feld firstcluster den Wert NULL aufweist, muss DATALENGTH ebenfalls 0 (null) sein, um Abschnitt 6.3.6 und section 6.4.4, um zu verdeutlichen, dass eine gültige Zuordnung vorhanden sein muss, wenn das nofatchain-Bit festgelegt ist.</p>
<p>Aktualisierter Copyright Hinweis zu 2010</p>
</blockquote></td>
</tr>
<tr class="odd">
<td>26. Aug-2019</td>
<td><p>Die siebte Version der grundlegenden Spezifikation, die die folgenden Änderungen umfasst:</p>
<blockquote>
<p>Aktualisierte rechtliche Bedingungen bezüglich der Spezifikation, einschließlich:</p>
<p>Entfernen von vertraulichen Microsoft-hinweisen</p>
<p>Entfernen des Lizenzvertrags Abschnitts der Microsoft Corporation Technical Documentation</p>
<p>Aktualisierter Copyright Hinweis zu 2019</p>
</blockquote></td>
</tr>
</tbody>
</table>
