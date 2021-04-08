---
description: In der Volumeverwaltung verwendete Funktionen.
ms.assetid: dc985126-970c-49f2-877f-3759125e43b6
title: Volumen Verwaltungsfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd2be955b892bfcd31a70694bc79a7272676aae0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758287"
---
# <a name="volume-management-functions"></a>Volumen Verwaltungsfunktionen

In der Volumeverwaltung verwendete Funktionen.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                   | BESCHREIBUNG                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Definedosdevice**](/windows/desktop/api/FileAPI/nf-fileapi-definedosdevicew)<br/>                                   | Definiert, definiert oder löscht MS-DOS-Gerätenamen.<br/>                                                                                                                |
| [**DeleteVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-deletevolumemountpointw)<br/>                     | Löscht einen Laufwerk Buchstaben oder einen bereitgestellten Ordner.<br/>                                                                                                                          |
| [**Findfirstvolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew)<br/>                                   | Ruft den Namen eines Volumes auf einem Computer ab. <br/>                                                                                                                     |
| [**Findfirstvolumemountpoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa)<br/>               | Ruft den Namen eines eingebundenen Ordners auf dem angegebenen Volume ab. <br/>                                                                                                   |
| [**Findnextvolume**](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew)<br/>                                     | Setzt eine volumesuche fort, die durch einen Aufrufder [**findfirstvolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew) -Funktion gestartet wurde. <br/>                                                           |
| [**Findnextvolumemountpoint**](/windows/desktop/api/WinBase/nf-winbase-findnextvolumemountpointa)<br/>                 | Setzt eine bereitgestellte Ordner Suche fort, die durch einen aufrufsvorgang der [**findfirstvolumemountpoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa) -Funktion gestartet wurde. <br/>                               |
| [**Findvolumeclose**](/windows/desktop/api/FileAPI/nf-fileapi-findvolumeclose)<br/>                                   | Schließt das angegebene volumesuchhandle.<br/>                                                                                                                         |
| [**Findvolumemountpointclose**](/windows/desktop/api/WinBase/nf-winbase-findvolumemountpointclose)<br/>               | Schließt das angegebene Such Handle für den bereitgestellten Ordner.<br/>                                                                                                                 |
| [**GetDriveType**](/windows/desktop/api/FileAPI/nf-fileapi-getdrivetypea)<br/>                                         | Bestimmt, ob ein Festplattenlaufwerk eine Wechsel Datenträger, eine CD-ROM, ein RAM-Laufwerk oder ein Netzwerklaufwerk ist.<br/>                                                                         |
| [**GetLogicalDrives**](/windows/desktop/api/FileAPI/nf-fileapi-getlogicaldrives)<br/>                                 | Ruft eine Bitmaske ab, die die aktuell verfügbaren Laufwerke darstellt.<br/>                                                                                              |
| [**Getlogicaldrivestrings**](/windows/desktop/api/FileAPI/nf-fileapi-getlogicaldrivestringsw)<br/>                     | Füllt einen Puffer mit Zeichen folgen, die gültige Laufwerke im System angeben.<br/>                                                                                               |
| [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa)<br/>                         | Ruft Informationen zum Dateisystem und zum Volume ab, das dem angegebenen Stammverzeichnis zugeordnet ist.<br/>                                                               |
| [**Getvolumeingeformationbylenker**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationbyhandlew)<br/>       | Ruft Informationen über das Dateisystem und das Volume ab, die der angegebenen Datei zugeordnet sind.<br/>                                                                         |
| [**Getvolumenameforvolumemountpoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw)<br/> | Ruft einen **VolumeGuid** -Pfad für das Volume ab, das dem angegebenen volumeeinstellungspunkt (Laufwerksbuchstaben, **VolumeGuid** -Pfad oder eingebundener Ordner) zugeordnet ist.<br/> |
| [**Getvolumepathname**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumepathnamew)<br/>                               | Ruft den Volume-Einfügepunkt ab, an dem der angegebene Pfad bereitgestellt wird.<br/>                                                                                              |
| [**Getvolumepathnamesforvolumename**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumepathnamesforvolumenamew)<br/>   | Ruft eine Liste der Laufwerksbuchstaben und der bereitgestellten Ordner Pfade für das angegebene Volume ab.<br/>                                                                               |
| [**Querydosdevice**](/windows/desktop/api/FileAPI/nf-fileapi-querydosdevicew)<br/>                                     | Ruft Informationen zu MS-DOS-Gerätenamen ab.<br/>                                                                                                                   |
| [**Setvolumelabel**](/windows/desktop/api/WinBase/nf-winbase-setvolumelabela)<br/>                                     | Legt die Bezeichnung eines Dateisystem Volumes fest.<br/>                                                                                                                            |
| [**Setvolumemountpoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa)<br/>                           | Ordnet ein Volume einem Laufwerk Buchstaben oder einem Verzeichnis auf einem anderen Volume zu.<br/>                                                                                          |



 

Die folgenden Funktionen werden bei volumeeinstellungspunkten verwendet (Laufwerksbuchstaben, VolumeGuid-Pfade und eingebundene Ordner).

-   [**DeleteVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-deletevolumemountpointw)
-   [**Findfirstvolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew)
-   [**Findfirstvolumemountpoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa)
-   [**Findnextvolume**](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew)
-   [**Findnextvolumemountpoint**](/windows/desktop/api/WinBase/nf-winbase-findnextvolumemountpointa)
-   [**Findvolumeclose**](/windows/desktop/api/FileAPI/nf-fileapi-findvolumeclose)
-   [**Findvolumemountpointclose**](/windows/desktop/api/WinBase/nf-winbase-findvolumemountpointclose)
-   [**Getvolumenameforvolumemountpoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw)
-   [**Getvolumepathname**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumepathnamew)
-   [**Getvolumepathnamesforvolumename**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumepathnamesforvolumenamew)
-   [**Setvolumemountpoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa)

 

 




