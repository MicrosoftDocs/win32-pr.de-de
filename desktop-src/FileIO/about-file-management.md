---
description: Informationen zur Dateiverwaltung.
ms.assetid: cf4e69b9-86dd-43a4-9011-6209fc65f550
title: Informationen zur Dateiverwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2544d31ecb95029053987a3d64e80f4cdf8c0f3170b3a679b542e145ca262947
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119766370"
---
# <a name="about-file-management"></a>Informationen zur Dateiverwaltung

Die folgenden Themen enthalten weitere Informationen zur Dateiverwaltung.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                 | Beschreibung                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Vergleich der Dateisystemfunktionalität](filesystem-functionality-comparison.md)<br/>            | Tabellen, die Funktionen und Features auflisten, unterstützen Vergleiche für die vier Windows Dateisysteme NTFS, exFAT, UDF und FAT32.<br/>                                                                           |
| [Dateien und Cluster](files-and-clusters.md)<br/>                                               | Eine *Datei* ist eine Dateneinheit im Dateisystem, auf die ein Benutzer zugreifen und diese verwalten kann.<br/>                                                                                                                              |
| [Erstellen, Löschen und Verwalten von Dateien](creating--deleting--and-maintaining-files.md)<br/> | Funktionen zum Erstellen, Löschen und Verwalten von Dateien.<br/>                                                                                                                                                       |
| [Abrufen und Festlegen von Dateiinformationen](obtaining-and-setting-file-information.md)<br/>       | Funktionen, die zum Erhalten und Festlegen von Dateiinformationen verwendet werden.<br/>                                                                                                                                                             |
| [Lesen aus und Schreiben in Dateien](reading-from-and-writing-to-files.md)<br/>                 | Eine Anwendung liest mithilfe der Funktionen [**ReadFile,**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) [**ReadFileEx,**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile)und [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) aus einer Datei und schreibt sie in diese.<br/> |
| [Datei- und Verzeichnisverknüpfung](file-and-directory-linking.md)<br/>                               | Im NTFS-Dateisystem werden zwei Arten von Links unterstützt: [feste Links und Verknüpfungen.](hard-links-and-junctions.md)<br/>                                                                                     |
| [Klonen blockieren](block-cloning.md)<br/>                                                         | Ein *Blockklonvorgang* weist das Dateisystem an, einen Bereich von Dateibytes im Auftrag einer Anwendung zu kopieren.<br/>                                                                                                |
| [Dateikomprimierung und Dekomprimierung](file-compression-and-decompression.md)<br/>               | Das NTFS-Dateisystem verwendet Lempel-Ziv Komprimierung, bei der es sich um einen verlustlosen Komprimierungsalgorithmus handelt.<br/>                                                                                                                  |
| [Dateiverschlüsselung](file-encryption.md)<br/>                                                     | Das verschlüsselte Dateisystem (Encrypted File System, EFS) bietet kryptografischen Schutz einzelner Dateien auf NTFS-Dateisystemvolumes mithilfe eines Systems mit öffentlichem Schlüssel.<br/>                                                               |
| [Dateisicherheit und Zugriffsrechte](file-security-and-access-rights.md)<br/>                     | Da Dateien [sicherungsfähige Objekte sind,](/windows/desktop/SecAuthZ/securable-objects)wird der Zugriff darauf durch das Zugriffssteuerungsmodell reguliert, das den Zugriff auf alle anderen sicherungsfähige Objekte in Windows.<br/>                     |
| [Eingabe und Ausgabe (E/A)](input-and-output--i-o-.md)<br/>                                       | Windows bietet die Möglichkeit, Eingabe- und Ausgabevorgänge (E/A) für Speicherkomponenten auf lokalen und Remotecomputern durchzuführen.<br/>                                                                        |
| [Dateien von geringer Dichte](sparse-files.md)<br/>                                                           | Die Dateikomprimierung von Dateien, die größtenteils Nullen enthalten, nutzt den Speicherplatz effizient.<br/>                                                                                                                        |
| [Symbolische Verknüpfungen](symbolic-links.md)<br/>                                                       | Eine symbolische Verknüpfung ist ein Dateisystemobjekt, das auf ein anderes Dateisystemobjekt zeigt. Das Objekt, auf das verwiesen wird, wird als Ziel bezeichnet.<br/>                                                                          |



 

 

