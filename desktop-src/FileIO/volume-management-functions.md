---
description: Funktionen, die in der Volumeverwaltung verwendet werden.
ms.assetid: dc985126-970c-49f2-877f-3759125e43b6
title: VolumeVerwaltungsfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3673e73007c977992d0209bcd79ded2afd4ed555ec3a22821e5f74d90e3cb61
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130690"
---
# <a name="volume-management-functions"></a>VolumeVerwaltungsfunktionen

Funktionen, die in der Volumeverwaltung verwendet werden.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                   | Beschreibung                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DefineDosDevice**](/windows/desktop/api/FileAPI/nf-fileapi-definedosdevicew)<br/>                                   | Definiert, definiert oder löscht MS-DOS-Gerätenamen.<br/>                                                                                                                |
| [**DeleteVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-deletevolumemountpointw)<br/>                     | Löscht einen Laufwerkbuchstaben oder bereitgestellten Ordner.<br/>                                                                                                                          |
| [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew)<br/>                                   | Ruft den Namen eines Volumes auf einem Computer ab. <br/>                                                                                                                     |
| [**FindFirstVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa)<br/>               | Ruft den Namen eines bereitgestellten Ordners auf dem angegebenen Volume ab. <br/>                                                                                                   |
| [**FindNextVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew)<br/>                                     | Setzt eine Volumesuche fort, die durch einen Aufruf der [**FindFirstVolume-Funktion**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew) gestartet wurde. <br/>                                                           |
| [**FindNextVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findnextvolumemountpointa)<br/>                 | Setzt eine eingebundene Ordnersuche fort, die durch einen Aufruf der [**FindFirstVolumeMountPoint-Funktion**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa) gestartet wurde. <br/>                               |
| [**FindVolumeClose**](/windows/desktop/api/FileAPI/nf-fileapi-findvolumeclose)<br/>                                   | Schließt das angegebene Volumesuchhandle.<br/>                                                                                                                         |
| [**FindVolumeMountPointClose**](/windows/desktop/api/WinBase/nf-winbase-findvolumemountpointclose)<br/>               | Schließt das angegebene Suchhandle für bereitgestellte Ordner.<br/>                                                                                                                 |
| [**GetDriveType**](/windows/desktop/api/FileAPI/nf-fileapi-getdrivetypea)<br/>                                         | Bestimmt, ob es sich bei einem Laufwerk um ein Wechsel-, Fest-, CD-ROM-, RAM- oder Netzwerklaufwerk handelt.<br/>                                                                         |
| [**GetLogicalDrives**](/windows/desktop/api/FileAPI/nf-fileapi-getlogicaldrives)<br/>                                 | Ruft eine Bitmaske ab, die die derzeit verfügbaren Laufwerke darstellt.<br/>                                                                                              |
| [**GetLogicalDriveStrings**](/windows/desktop/api/FileAPI/nf-fileapi-getlogicaldrivestringsw)<br/>                     | Füllt einen Puffer mit Zeichenfolgen, die gültige Laufwerke im System angeben.<br/>                                                                                               |
| [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa)<br/>                         | Ruft Informationen über das Dateisystem und das Volume ab, das dem angegebenen Stammverzeichnis zugeordnet ist.<br/>                                                               |
| [**GetVolumeInformationByHandleW**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationbyhandlew)<br/>       | Ruft Informationen zum Dateisystem und Volume ab, das der angegebenen Datei zugeordnet ist.<br/>                                                                         |
| [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw)<br/> | Ruft einen **Volume-GUID-Pfad** für das Volume ab, das dem angegebenen Volume-Bereitstellungspunkt zugeordnet ist (Laufwerkbuchstabe, **Volume-GUID-Pfad** oder bereitgestellter Ordner).<br/> |
| [**GetVolumePathName**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumepathnamew)<br/>                               | Ruft den Volume-Bereitstellungspunkt ab, an dem der angegebene Pfad bereitgestellt wird.<br/>                                                                                              |
| [**GetVolumePathNamesForVolumeName**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumepathnamesforvolumenamew)<br/>   | Ruft eine Liste von Laufwerkbuchstaben und bereitgestellten Ordnerpfaden für das angegebene Volume ab.<br/>                                                                               |
| [**QueryDosDevice**](/windows/desktop/api/FileAPI/nf-fileapi-querydosdevicew)<br/>                                     | Ruft Informationen zu MS-DOS-Gerätenamen ab.<br/>                                                                                                                   |
| [**SetVolumeLabel**](/windows/desktop/api/WinBase/nf-winbase-setvolumelabela)<br/>                                     | Legt die Bezeichnung eines Dateisystemvolumes fest.<br/>                                                                                                                            |
| [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa)<br/>                           | Ordnet ein Volume einem Laufwerkbuchstaben oder einem Verzeichnis auf einem anderen Volume zu.<br/>                                                                                          |



 

Die folgenden Funktionen werden mit Volume-Bereitstellungspunkten (Laufwerkbuchstaben, VOLUME-GUID-Pfade und bereitgestellte Ordner) verwendet.

-   [**DeleteVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-deletevolumemountpointw)
-   [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew)
-   [**FindFirstVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa)
-   [**FindNextVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew)
-   [**FindNextVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findnextvolumemountpointa)
-   [**FindVolumeClose**](/windows/desktop/api/FileAPI/nf-fileapi-findvolumeclose)
-   [**FindVolumeMountPointClose**](/windows/desktop/api/WinBase/nf-winbase-findvolumemountpointclose)
-   [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw)
-   [**GetVolumePathName**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumepathnamew)
-   [**GetVolumePathNamesForVolumeName**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumepathnamesforvolumenamew)
-   [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa)

 

 




