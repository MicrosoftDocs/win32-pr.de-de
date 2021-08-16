---
description: Tabellen, in denen Funktionen und Features aufgeführt sind, unterstützen Vergleiche für die vier haupt- Windows Dateisysteme NTFS, exFAT, UDF und FAT32.
ms.assetid: 28cf2805-f1ce-46b4-bf08-a329f67f4d99
title: Vergleich der Dateisystemfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5af85dbacfd04920d8eb0a9558e0d57cc6e4020da35ffac57f7bdc703e6ef15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119790690"
---
# <a name="file-system-functionality-comparison"></a>Vergleich der Dateisystemfunktionen

In den folgenden Tabellen sind die Funktionen und Features aufgeführt, die Vergleiche für die vier haupt- Windows Dateisysteme NTFS, exFAT, UDF und FAT32 unterstützen:

-   [Funktion](#file-system-functionality-comparison)
-   [Einschränkungen](#limits)
-   [Journaling und Änderungsprotokoll](#journaling-and-change-log)
-   [Blockzuordnungsfeatures](#block-allocation-features)
-   [Sicherheit](#security)
-   [Komprimierung](#compression)
-   [Kontingente](#quotas)
-   [Einzelinstanz-Store](#single-instance-store)
-   [Zugehörige Themen](#related-topics)

## <a name="functionality"></a>Funktionalität



| Komponente                             | NTFS                           | exFAT          | UDF                           | FAT32                      |
|-------------------------------------|--------------------------------|----------------|-------------------------------|----------------------------|
| Erstellungszeitstempel<br/>     | Ja<br/>                 | Ja<br/> | Ja<br/>                | Ja<br/>             |
| Zeitstempel des letzten Zugriffs<br/>  | Nein (siehe nachstehenden Hinweis)<br/> | Ja<br/> | Ja<br/>                | Ja (nur Datum)<br/> |
| Zeitstempel der letzten Änderung<br/>  | Ja<br/>                 | Ja<br/> | Ja<br/>                | Ja<br/>             |
| Zeitstempel des letzten Archivs<br/> | Nein<br/>                  | Nein<br/>  | Nein<br/>                 | Nein<br/>              |
| Beachtet Groß-/Kleinschreibung<br/>           | Ja (Option)<br/>        | Nein<br/>  | Ja<br/>                | Nein<br/>              |
| Beibehalten der Case-Aufrechterhaltung<br/>          | Ja<br/>                 | Ja<br/> | Ja<br/>                | Ja<br/>             |
| Feste Links<br/>               | Ja<br/>                 | Nein<br/>  | Ja<br/>                | Nein<br/>              |
| Weiche Links<br/>               | Ja<br/>                 | Nein<br/>  | Nein<br/>                 | Nein<br/>              |
| Sparsedateien<br/>             | Ja<br/>                 | Nein<br/>  | Ja<br/>                | Nein<br/>              |
| Benannte Datenströme<br/>            | Ja<br/>                 | Nein<br/>  | Ja<br/>                | Nein<br/>              |
| Oplocks<br/>                  | Ja<br/>                 | Ja<br/> | Ja<br/>                | Ja<br/>             |
| Erweiterte Attribute<br/>      | Ja<br/>                 | Nein<br/>  | Ja (nur auf dem Datenträger)<br/> | Nein<br/>              |
| Alternative Datenströme<br/>   | Ja<br/>                 | Nein<br/>  | Ja<br/>                | Nein<br/>              |
| Bereitstellungspunkte<br/>             | Ja<br/>                 | Nein<br/>  | Nein<br/>                 | Nein<br/>              |



 

**Windows Server 2003 und Windows XP:** Das Ntfs-Zeitstempelfeld für den letzten Zugriff wird aktualisiert.

## <a name="limits"></a>Grenzwerte



| Funktion                             | NTFS                                                                                      | exFAT                                                                                     | UDF                                                                                       | FAT32                                                                                     |
|-------------------------------------|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| Maximale Dateinamenslänge<br/> | 255 Unicode-Zeichen<br/>                                                         | 255 Unicode-Zeichen<br/>                                                         | 127 Unicode- oder 254 ASCII-Zeichen<br/>                                            | 255 Unicode-Zeichen<br/>                                                         |
| Maximale Pfadnamenslänge<br/> | 32.760 Unicode-Zeichen mit jeder Pfadkomponente nicht mehr als 255 Zeichen<br/> | 32.760 Unicode-Zeichen mit jeder Pfadkomponente nicht mehr als 255 Zeichen<br/> | 32.760 Unicode-Zeichen mit jeder Pfadkomponente nicht mehr als 255 Zeichen<br/> | 32.760 Unicode-Zeichen mit jeder Pfadkomponente nicht mehr als 255 Zeichen<br/> |
| Maximale Dateigröße<br/>        | 2^64 1 Bytes<br/>                                                                   | 2^64 1 Bytes<br/>                                                                   | 2^64 1 Bytes<br/>                                                                   | 4 GiB<br/>                                                                          |
| Maximale Volumegröße<br/>      | 16 TB (4 KB Clustergröße) oder 256 TB (64 KB Clustergröße)<br/>                        | 2^32 1 Cluster (Maximale Clustergröße = 2^25 1)<br/>                               | 2^32 Blöcke<br/>                                                                    | 2^32 Blöcke<br/>                                                                    |



 

## <a name="journaling-and-change-log"></a>Journaling und Änderungsprotokoll



| Komponente                             | NTFS           | exFAT         | UDF           | FAT32         |
|-------------------------------------|----------------|---------------|---------------|---------------|
| Nur Metadaten-Journaling<br/> | Ja<br/> | Nein<br/> | Nein<br/> | Nein<br/> |
| Dateiänderungsprotokoll<br/>          | Ja<br/> | Nein<br/> | Nein<br/> | Nein<br/> |



 

## <a name="block-allocation-features"></a>Blockzuordnungsfeatures



| Komponente                        | NTFS                                                                        | exFAT         | UDF            | FAT32         |
|--------------------------------|-----------------------------------------------------------------------------|---------------|----------------|---------------|
| Packen des Endes<br/>        | Ja (kleine Dateien werden im MFT-Streamdeskriptor gespeichert)<br/> | Nein<br/> | Nein<br/>  | Nein<br/> |
| Extents<br/>             | Ja<br/>                                                              | Nein<br/> | Ja<br/> | Nein<br/> |
| Variable Blockgröße<br/> | Nein (durch das Volume festgelegt)<br/>                                           | Nein<br/> | Nein<br/>  | Nein<br/> |



 

## <a name="security"></a>Sicherheit



| Funktion                                  | NTFS                                                 | exFAT               | UDF                 | FAT32         |
|------------------------------------------|------------------------------------------------------|---------------------|---------------------|---------------|
| Nachverfolgen des Dateibesitzers<br/>              | Ja<br/>                                       | Nein<br/>       | Nein<br/>       | Nein<br/> |
| POSIX-Dateiberechtigungen<br/>        | Nein (verfügbar im POSIX-Subsystemfeature)<br/> | Nein<br/>       | Ja<br/>      | Nein<br/> |
| Zugriffssteuerungslisten<br/>          | Ja<br/>                                       | Nein<br/>       | Nein<br/>       | Nein<br/> |
| Verschlüsselung auf Dateisystemebene<br/> | Ja<br/>                                       | Nein<br/>       | Nein<br/>       | Nein<br/> |
| Prüfsumme/ECC<br/>                  | Nein<br/>                                        | Metadaten<br/> | Metadaten<br/> | Nein<br/> |



 

## <a name="compression"></a>Komprimierung



| Komponente                         | NTFS           | exFAT         | UDF           | FAT32         |
|---------------------------------|----------------|---------------|---------------|---------------|
| Integrierte Komprimierung<br/> | Ja<br/> | Nein<br/> | Nein<br/> | Nein<br/> |



 

## <a name="quotas"></a>Kontingente



| Komponente                               | NTFS                           | exFAT         | UDF           | FAT32         |
|---------------------------------------|--------------------------------|---------------|---------------|---------------|
| Speicherplatz auf Benutzerebene<br/>      | Ja<br/>                 | Nein<br/> | Nein<br/> | Nein<br/> |
| Speicherplatz auf Verzeichnisebene<br/> | Nein (siehe nachstehenden Hinweis)<br/> | Nein<br/> | Nein<br/> | Nein<br/> |



 

**Hinweis:**  Das Feature speicherplatzkontingente auf Verzeichnisebene auf NTFS ist über die Dateiserver-Resource Manager.

## <a name="single-instance-store"></a>Single-Instance Store



| Komponente               | NTFS                           | exFAT         | UDF           | FAT32         |
|-----------------------|--------------------------------|---------------|---------------|---------------|
| Dateiebene<br/> | Nein (siehe nachstehenden Hinweis)<br/> | Nein<br/> | Nein<br/> | Nein<br/> |



 

**Hinweis:**  Der Einzelinstanzspeicher für NTFS ist als Teil des Features Single Instance Storage in Windows Server verfügbar.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zur Dateiverwaltung](about-file-management.md)
</dt> <dt>

[Einzelinstanz-Store und SIS-Sicherung](/windows/desktop/Backup/single-instance-store-and-sis-backup)
</dt> </dl>

 

