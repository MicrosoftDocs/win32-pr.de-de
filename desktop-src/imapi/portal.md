---
title: Bildmaster-API
description: Bildmaster-API
ms.assetid: 4902d3fb-3195-4909-ab64-28f8a77ba14c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7fabf41d1c82420709b39bb5db03c2ac3e851d2
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119676"
---
# <a name="image-mastering-api"></a>Bildmaster-API

## <a name="purpose"></a>Zweck

Mit der Microsoft Windows-Imagemastering-API können Anwendungen Bilder auf cd-, DVD- und Blu-ray-Optische Speichermedien stagen und darauf speichern. Andere datenträgerbasierte Medien, die Bilder auf die gleiche Weise erstellen, können diese API ebenfalls verwenden.

## <a name="developer-audience"></a>Entwicklergruppe

IMAPI ist für C/C++- und Visual Basic entwickler sowie für Entwickler konzipiert, die Skripts mit VBScript schreiben.

Kenntnisse über CD-, DVD- und Blu-ray-Technologien und Dateisysteme werden empfohlen. Entwickler können von einer vertrauten Version des Multimedia-Befehls (MMC) bei [ftp://ftp.t10.org/t10/drafts/mmc6.](https://www.microsoft.com/?ref=go)

## <a name="run-time-requirements"></a>Laufzeitanforderungen

IMAPI 2.0 wird ab Windows Vista und Windows Server 2008 nativ unterstützt. Zum Aktivieren der IMAPI 2.0-Funktionalität für Windows XP und Windows Server 2003 muss das [Updatepaket KB932716](https://support.microsoft.com/kb/932716) installiert werden. Wenn dieses Paket nicht installiert ist, unterstützt Windows XP weiterhin [nativ IMAPI 1.0.](imapiv1.md)

> [!Note]  
> Das Windows Feature Pack für Storage ist für die Öffentlichkeit über das [Microsoft Download Center verfügbar.](https://www.microsoft.com/downloads/details.aspx?FamilyID=63ab51ea-99c9-45c0-980a-c556746fcf05) Weitere Informationen zu bestimmten API-Änderungen finden Sie im Abschnitt [Neuerungen.](what-s-new.md)

 

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                             | Beschreibung                                                                           |
|---------------------------------------------------|---------------------------------------------------------------------------------------|
| [Neuerungen](what-s-new.md)<br/>           | Informationen zu jedem wichtigen Release der Imagemaster-API.<br/> |
| [Informationen zu IMAPI](about-imapi.md)<br/>         | Allgemeine Informationen zur Imagemastering-API.<br/>                         |
| [Verwenden von IMAPI](using-imapi.md)<br/>         | Aufgabenbezogene Themen, die die Verwendung der Bildmaster-API veranschaulichen.<br/>   |
| [IMAPI-Referenz](imapi-reference.md)<br/> | Ausführliche Beschreibungen von IMAPI-Schnittstellen und anderen Programmierelementen.<br/>  |



 

## <a name="additional-resources"></a>Zusätzliche Ressourcen

Weitere Informationen zu IMAPI und anderen verwandten Themen finden Sie an den folgenden Stellen:



| Thema                                                                                                 | Beschreibung                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Microsoft Optical Storage Blog](/archive/blogs/opticalstorage/)                | Hebt Themen hervor, die sich auf die Implementierung der Bildmaster-API in realen Entwicklungsszenarien konzentrieren.                                                                                                                                                                                                                                                 |
| [Diskussionsforum zur optischen Plattform](https://social.msdn.microsoft.com/forums/windowsopticalplatform/threads/)              | Erläutern CDROM.SYS, IMAPIv2- und Live File System-Problemen. Dieses Forum konzentriert sich auf Themen auf Systemebene und ist für Anwendungsentwickler und nicht für Endbenutzer vorgesehen.                                                                                                                                                                                                 |
| [T10 Technical Committee](https://www.t10.org/)                       | Ein technischer Ausschuss des InterNational-Ausschuss für Informationstechnologiestandards (INCITS, ausgesprochen als "Erkenntnisse"). INCITS wird von der Ansi (American National Standards Institute) zugelassen und arbeitet gemäß diesen Regeln. Diese Regeln sollen sicherstellen, dass freiwillige Standards durch den Konsens von Branchengruppen entwickelt werden. |
| [Optical Storage Technology Association (LAGERUNG)](http://www.osta.org/) | Arbeitet an der Gestaltung der Zukunft der Branche durch regelmäßige Besprechungen von kommerziellen optischen Speicheranwendungen (Commercial Optical Storage Applications, COSA), DVD-Kompatibilität, Marketing, MPV (MusicPhotoVideo), UDF-Sprechungen und einem neuen Ad-hoc-BlueScan-Ausschuss. Interessierten Unternehmen auf der ganzen Welt werden eingeladen, der Organisation beizunehmen und an deren Programmen und Programmen teilzunehmen.               |



 

 

