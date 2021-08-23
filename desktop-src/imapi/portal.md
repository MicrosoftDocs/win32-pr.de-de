---
title: ImageMastering-API
description: ImageMastering-API
ms.assetid: 4902d3fb-3195-4909-ab64-28f8a77ba14c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e28f98422a1845234ec9eda7054978797c876a41a905484a95a505bdf4e133c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119611790"
---
# <a name="image-mastering-api"></a>ImageMastering-API

## <a name="purpose"></a>Zweck

Mit der Microsoft Windows-Bildmastering-API können Anwendungen Bilder auf optischen CD-, DVD- und Blu-Ray-Speichermedien bereitstellen und dort speichern. Andere datenträgerähnliche Medien, die Bilder auf die gleiche Weise ablegen, können diese API ebenfalls verwenden.

## <a name="developer-audience"></a>Entwicklergruppe

IMAPI ist für C/C++- und Visual Basic-Entwickler sowie für Entwickler konzipiert, die Skripts mit VBScript schreiben.

Kenntnisse über CD-, DVD- und Blu-ray-Technologien und Dateisysteme werden empfohlen. Entwickler können von einer Vertrautheit mit der neuesten Revision von Multimedia command (MMC) unter [ftp://ftp.t10.org/t10/drafts/mmc6](https://www.microsoft.com/?ref=go)profitieren.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

IMAPI 2.0 wird ab Windows Vista und Windows Server 2008 nativ unterstützt. Das Aktivieren der IMAPI 2.0-Funktionalität für Windows XP und Windows Server 2003 erfordert die Installation des [Updatepakets KB932716.](https://support.microsoft.com/kb/932716) Wenn dieses Paket nicht installiert ist, unterstützt Windows XP [IMAPI 1.0](imapiv1.md)weiterhin nativ.

> [!Note]  
> Das Windows Feature Pack für Storage ist für die Öffentlichkeit über das [Microsoft Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=63ab51ea-99c9-45c0-980a-c556746fcf05)verfügbar. Weitere Informationen zu bestimmten API-Änderungen finden Sie im Abschnitt [Neuerungen.](what-s-new.md)

 

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                             | Beschreibung                                                                           |
|---------------------------------------------------|---------------------------------------------------------------------------------------|
| [Neuigkeiten](what-s-new.md)<br/>           | Informationen zu den einzelnen wichtigen Freigaben der Imagemastering-API.<br/> |
| [Informationen zu IMAPI](about-imapi.md)<br/>         | Allgemeine Informationen zur ImageMastering-API.<br/>                         |
| [Verwenden von IMAPI](using-imapi.md)<br/>         | Aufgabenbezogene Themen, die die Verwendung der Imagemastering-API veranschaulichen.<br/>   |
| [IMAPI-Referenz](imapi-reference.md)<br/> | Ausführliche Beschreibungen von IMAPI-Schnittstellen und anderen Programmierelementen.<br/>  |



 

## <a name="additional-resources"></a>Zusätzliche Ressourcen

Weitere Informationen zu IMAPI und anderen verwandten Themen finden Sie an den folgenden Speicherorten:



| Thema                                                                                                 | Beschreibung                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Microsoft Optical Storage Blog](/archive/blogs/opticalstorage/)                | Hebt Themen hervor, die sich auf die Implementierung der Image Mastering-API in realen Entwicklungsszenarien konzentrieren.                                                                                                                                                                                                                                                 |
| [Diskussionsforum zur optischen Plattform](https://social.msdn.microsoft.com/forums/windowsopticalplatform/threads/)              | Behandeln sie probleme mit CDROM.SYS, IMAPIv2 und Live File System. Dieses Forum konzentriert sich auf Themen auf Systemebene und richtet sich an Anwendungsentwickler und nicht an Endbenutzer.                                                                                                                                                                                                 |
| [T10 Technical Committee](https://www.t10.org/)                       | Ein Technischer Ausschuss des Inter National Committee on Information Technology Standards (INCITS, ausgesprochen "Erkenntnisse"). INCITS wird von der American National Standards Institute (ANSI) zugelassen und unterliegt regeln, die von diesen genehmigt werden. Diese Regeln sollen sicherstellen, dass freiwillige Standards im Konsens der Branchengruppen entwickelt werden. |
| [Optical Storage Technology Association (ASSO)](http://www.osta.org/) | Arbeitet daran, die Zukunft der Branche durch regelmäßige Besprechungen von commercial Optical Storage Applications (COSA), DVD Compatibility, Marketing, MPV (MusicPhotoVideo), UDF-Vertriebspartnern und einem neuen adhoc Blue Photo Committee zu gestalten. Interessierten Unternehmen auf der ganzen Welt werden eingeladen, der Organisation beizutreten und an ihren Programmen und Programmen teilzunehmen.               |



 

 

