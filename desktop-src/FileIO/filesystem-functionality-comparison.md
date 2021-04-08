---
description: Tabellen, die Funktionen und Featureunterstützung für die vier Haupt-Windows-Dateisysteme, NTFS, exFAT, UDF und FAT32 auflisten.
ms.assetid: 28cf2805-f1ce-46b4-bf08-a329f67f4d99
title: Vergleich der Datei System Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7547e48ff68a8fdab195087904a47a535aa3464
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753568"
---
# <a name="file-system-functionality-comparison"></a>Vergleich der Datei System Funktionen

In den folgenden Tabellen sind die Funktions-und Featureunterstützung für die vier Windows-Hauptdatei Systeme NTFS, exFAT, UDF und FAT32 aufgeführt:

-   [Funktion](#file-system-functionality-comparison)
-   [Einschränkungen](#limits)
-   [Journal-und Änderungsprotokoll](#journaling-and-change-log)
-   [Block Zuordnungs Funktionen](#block-allocation-features)
-   [Security](#security)
-   [Komprimierung](#compression)
-   [Kontingente](#quotas)
-   [Einzelinstanzspeicher](#single-instance-store)
-   [Zugehörige Themen](#related-topics)

## <a name="functionality"></a>Funktionalität



| Funktion                             | NTFS                           | exFAT          | UDF                           | FAT32                      |
|-------------------------------------|--------------------------------|----------------|-------------------------------|----------------------------|
| Erstellungszeit Stempel<br/>     | Ja<br/>                 | Ja<br/> | Ja<br/>                | Ja<br/>             |
| Zeitstempel des letzten Zugriffs<br/>  | Nein (siehe nachstehenden Hinweis)<br/> | Ja<br/> | Ja<br/>                | Ja (nur Datum)<br/> |
| Zeitstempel der letzten Änderung<br/>  | Ja<br/>                 | Ja<br/> | Ja<br/>                | Ja<br/>             |
| Zeitstempel der letzten Archivierung<br/> | Nein<br/>                  | Nein<br/>  | Nein<br/>                 | Nein<br/>              |
| Beachtet Groß-/Kleinschreibung<br/>           | Ja (Option)<br/>        | Nein<br/>  | Ja<br/>                | Nein<br/>              |
| Groß-und Kleinschreibung<br/>          | Ja<br/>                 | Ja<br/> | Ja<br/>                | Ja<br/>             |
| Feste Links<br/>               | Ja<br/>                 | Nein<br/>  | Ja<br/>                | Nein<br/>              |
| Weiche Links<br/>               | Ja<br/>                 | Nein<br/>  | Nein<br/>                 | Nein<br/>              |
| Sparsedateien<br/>             | Ja<br/>                 | Nein<br/>  | Ja<br/>                | Nein<br/>              |
| Benannte Datenströme<br/>            | Ja<br/>                 | Nein<br/>  | Ja<br/>                | Nein<br/>              |
| Oplocks<br/>                  | Ja<br/>                 | Ja<br/> | Ja<br/>                | Ja<br/>             |
| Erweiterte Attribute<br/>      | Ja<br/>                 | Nein<br/>  | Ja (nur auf der Festplatte)<br/> | Nein<br/>              |
| Alternative Datenströme<br/>   | Ja<br/>                 | Nein<br/>  | Ja<br/>                | Nein<br/>              |
| Bereitstellungspunkte<br/>             | Ja<br/>                 | Nein<br/>  | Nein<br/>                 | Nein<br/>              |



 

**Windows Server 2003 und Windows XP:** Das Feld für den letzten NTFS-Zugriffszeit Stempel wird aktualisiert.

## <a name="limits"></a>Grenzwerte



| Funktion                             | NTFS                                                                                      | exFAT                                                                                     | UDF                                                                                       | FAT32                                                                                     |
|-------------------------------------|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| Maximale Dateinamenslänge<br/> | 255 Unicode-Zeichen<br/>                                                         | 255 Unicode-Zeichen<br/>                                                         | 127 Unicode-oder 254-ASCII-Zeichen<br/>                                            | 255 Unicode-Zeichen<br/>                                                         |
| Maximale Pfadnamenslänge<br/> | 32.760 Unicode-Zeichen, wobei jede Pfadkomponente höchstens 255 Zeichen lang ist<br/> | 32.760 Unicode-Zeichen, wobei jede Pfadkomponente höchstens 255 Zeichen lang ist<br/> | 32.760 Unicode-Zeichen, wobei jede Pfadkomponente höchstens 255 Zeichen lang ist<br/> | 32.760 Unicode-Zeichen, wobei jede Pfadkomponente höchstens 255 Zeichen lang ist<br/> |
| Maximale Dateigröße<br/>        | 2 ^ 64 1 Bytes<br/>                                                                   | 2 ^ 64 1 Bytes<br/>                                                                   | 2 ^ 64 1 Bytes<br/>                                                                   | 4 GiB<br/>                                                                          |
| Maximale Volumegröße<br/>      | 16 TB (Clustergröße 4 KB) oder 256 TB (Clustergröße 64 KB)<br/>                        | 2 ^ 32 1 Cluster (maximale Clustergröße = 2 ^ 25 1)<br/>                               | 2 ^ 32 Blöcke<br/>                                                                    | 2 ^ 32 Blöcke<br/>                                                                    |



 

## <a name="journaling-and-change-log"></a>Journal-und Änderungsprotokoll



| Funktion                             | NTFS           | exFAT         | UDF           | FAT32         |
|-------------------------------------|----------------|---------------|---------------|---------------|
| Nur-Metadaten-Journale<br/> | Ja<br/> | Nein<br/> | Nein<br/> | Nein<br/> |
| Datei Änderungsprotokoll<br/>          | Ja<br/> | Nein<br/> | Nein<br/> | Nein<br/> |



 

## <a name="block-allocation-features"></a>Block Zuordnungs Funktionen



| Funktion                        | NTFS                                                                        | exFAT         | UDF            | FAT32         |
|--------------------------------|-----------------------------------------------------------------------------|---------------|----------------|---------------|
| Ende der Verpackung<br/>        | Ja (kleine Dateien werden im MFT-Datenstrom Deskriptor gespeichert)<br/> | Nein<br/> | Nein<br/>  | Nein<br/> |
| Extents<br/>             | Ja<br/>                                                              | Nein<br/> | Ja<br/> | Nein<br/> |
| Variable Blockgröße<br/> | Nein (durch das Volume festgelegt)<br/>                                           | Nein<br/> | Nein<br/>  | Nein<br/> |



 

## <a name="security"></a>Sicherheit



| Funktion                                  | NTFS                                                 | exFAT               | UDF                 | FAT32         |
|------------------------------------------|------------------------------------------------------|---------------------|---------------------|---------------|
| Dateibesitzer nachverfolgen<br/>              | Ja<br/>                                       | Nein<br/>       | Nein<br/>       | Nein<br/> |
| POSIX-Dateiberechtigungen<br/>        | Nein (verfügbar im POSIX-Subsystem-Feature)<br/> | Nein<br/>       | Ja<br/>      | Nein<br/> |
| Zugriffssteuerungslisten<br/>          | Ja<br/>                                       | Nein<br/>       | Nein<br/>       | Nein<br/> |
| Verschlüsselung auf Dateisystem Ebene<br/> | Ja<br/>                                       | Nein<br/>       | Nein<br/>       | Nein<br/> |
| Prüfsumme/ECC<br/>                  | Nein<br/>                                        | Metadaten<br/> | Metadaten<br/> | Nein<br/> |



 

## <a name="compression"></a>Komprimierung



| Funktion                         | NTFS           | exFAT         | UDF           | FAT32         |
|---------------------------------|----------------|---------------|---------------|---------------|
| Integrierte Komprimierung<br/> | Ja<br/> | Nein<br/> | Nein<br/> | Nein<br/> |



 

## <a name="quotas"></a>Kontingente



| Funktion                               | NTFS                           | exFAT         | UDF           | FAT32         |
|---------------------------------------|--------------------------------|---------------|---------------|---------------|
| Speicherplatz auf Benutzerebene<br/>      | Ja<br/>                 | Nein<br/> | Nein<br/> | Nein<br/> |
| Speicherplatz auf Verzeichnisebene<br/> | Nein (siehe nachstehenden Hinweis)<br/> | Nein<br/> | Nein<br/> | Nein<br/> |



 

**Hinweis**  Die Funktion "Speicherplatz Kontingente auf Verzeichnisebene" auf NTFS ist über den Datei Server Ressourcen-Manager verfügbar.

## <a name="single-instance-store"></a>Single-Instance Speicher



| Funktion               | NTFS                           | exFAT         | UDF           | FAT32         |
|-----------------------|--------------------------------|---------------|---------------|---------------|
| Dateiebene<br/> | Nein (siehe nachstehenden Hinweis)<br/> | Nein<br/> | Nein<br/> | Nein<br/> |



 

**Hinweis**  Der Einzelinstanzspeicher für NTFS ist als Teil des Single Instance Storage-Features in Windows Server verfügbar.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zur Dateiverwaltung](about-file-management.md)
</dt> <dt>

[Einzelinstanzspeicher und SIS-Sicherung](/windows/desktop/Backup/single-instance-store-and-sis-backup)
</dt> </dl>

 

