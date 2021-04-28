---
title: ImageMastering-API
description: ImageMastering-API
ms.assetid: 4902d3fb-3195-4909-ab64-28f8a77ba14c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 641d9357496eb82a7e30f25a711928b16eeee2bb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117578"
---
# <a name="image-mastering-api"></a>ImageMastering-API

## <a name="purpose"></a>Zweck

Mit der Microsoft Windows-Imagemastering-API können Anwendungen Bilder auf optischen CD-, DVD- und Blu-Ray-Speichermedien bereitstellen und auf diese speichern. Andere datenträgerähnliche Medien, die Bilder auf die gleiche Weise ablegen, können diese API ebenfalls verwenden.

## <a name="developer-audience"></a>Entwicklergruppe

IMAPI ist für C/C++- und Visual Basic-Entwickler sowie für Entwickler konzipiert, die Skripts mit VBScript schreiben.

Kenntnisse über CD-, DVD- und Blu-ray-Technologien und Dateisysteme werden empfohlen. Entwickler können von einer Vertrautheit mit der neuesten Revision von Multimedia command (MMC) unter [ftp://ftp.t10.org/t10/drafts/mmc6](https://www.microsoft.com/?ref=go)profitieren.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

IMAPI 2.0 wird ab Windows Vista und Windows Server 2008 nativ unterstützt. Zum Aktivieren der IMAPI 2.0-Funktionalität für Windows XP und Windows Server 2003 muss das Updatepaket [KB932716](https://support.microsoft.com/kb/932716) installiert werden. Wenn dieses Paket nicht installiert ist, unterstützt Windows XP [IMAPI 1.0](imapiv1.md)weiterhin nativ.

> [!Note]  
> Das Windows Feature Pack für Storage ist für die Öffentlichkeit über das [Microsoft Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=63ab51ea-99c9-45c0-980a-c556746fcf05)verfügbar. Weitere Informationen zu bestimmten API-Änderungen finden Sie im Abschnitt [Neuerungen.](what-s-new.md)

 

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                             | BESCHREIBUNG                                                                           |
|---------------------------------------------------|---------------------------------------------------------------------------------------|
| [Neuerungen](what-s-new.md)<br/>           | Informationen zu den einzelnen wichtigen Freigaben der ImageMastering-API.<br/> |
| [Informationen zu IMAPI](about-imapi.md)<br/>         | Allgemeine Informationen zur Imagemastering-API.<br/>                         |
| [Verwenden von IMAPI](using-imapi.md)<br/>         | Aufgabenbezogene Themen, die die Verwendung der Imagemastering-API veranschaulichen.<br/>   |
| [IMAPI-Referenz](imapi-reference.md)<br/> | Ausführliche Beschreibungen von IMAPI-Schnittstellen und anderen Programmierelementen.<br/>  |



 

## <a name="additional-resources"></a>Zusätzliche Ressourcen

Weitere Informationen zu IMAPI und anderen verwandten Themen finden Sie an den folgenden Stellen:



|                                                                                                  |                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Microsoft Optical Storage Blog](/archive/blogs/opticalstorage/)                | Hebt Themen hervor, die sich auf die Implementierung der Bildmaster-API in realen Entwicklungsszenarien konzentrieren.                                                                                                                                                                                                                                                 |
| [Diskussionsforum zur optischen Plattform](https://social.msdn.microsoft.com/forums/windowsopticalplatform/threads/)              | Erläutern CDROM.SYS, IMAPIv2- und Live File System-Problemen. Dieses Forum konzentriert sich auf Themen auf Systemebene und ist für Anwendungsentwickler und nicht für Endbenutzer vorgesehen.                                                                                                                                                                                                 |
| [T10 Technical Committee](https://www.t10.org/)                       | Ein technischer Ausschuss des InterNational-Ausschuss für Informationstechnologiestandards (INCITS, ausgesprochen als "Erkenntnisse"). INCITS wird von der Ansi (American National Standards Institute) zugelassen und arbeitet gemäß diesen Regeln. Diese Regeln sollen sicherstellen, dass freiwillige Standards durch den Konsens von Branchengruppen entwickelt werden. |
| [Optical Storage Technology Association (LAGERUNG)](http://www.osta.org/) | Arbeitet an der Gestaltung der Zukunft der Branche durch regelmäßige Besprechungen von kommerziellen optischen Speicheranwendungen (Commercial Optical Storage Applications, COSA), DVD-Kompatibilität, Marketing, MPV (MusicPhotoVideo), UDF-Sprechungen und einem neuen Ad-hoc-BlueScan-Ausschuss. Interessierten Unternehmen auf der ganzen Welt werden eingeladen, der Organisation beizunehmen und an deren Programmen und Programmen teilzunehmen.               |



 

 

