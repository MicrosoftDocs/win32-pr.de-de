---
title: Bild-Mastering-API
description: .
ms.assetid: 4902d3fb-3195-4909-ab64-28f8a77ba14c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc23c972cf111dee5edf3cb014a52351eda3605e
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "103949194"
---
# <a name="image-mastering-api"></a>Bild-Mastering-API

## <a name="purpose"></a>Zweck

Die Microsoft Windows-Abbild-Mastering-API ermöglicht Anwendungen das Staging und Brennen von Bildern auf optischen CD-, DVD-und Blu-Ray-Speichermedien. Andere auf dem Bild Platten ähnliche Medien, die Bilder auf die gleiche Weise aufstellen, können diese API ebenfalls verwenden.

## <a name="developer-audience"></a>Entwicklergruppe

IMAPI ist für C/C++-und Visual Basic-Entwickler und solche konzipiert, die Skripts mithilfe von VBScript schreiben.

Es wird empfohlen, auf CD-, DVD-und Blu-Ray-Technologien und Dateisysteme zu wissen. Entwickler können von einer Vertrautheit mit der neuesten Revision von Multimedia Command (MMC) unter [FTP://FTP.T10.org/T10/Drafts/mmc6](https://www.microsoft.com/?ref=go)profitieren.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

IMAPI 2,0 wird nativ unterstützt, beginnend mit Windows Vista und Windows Server 2008. Um die IMAPI 2,0-Funktionalität für Windows XP und Windows Server 2003 zu aktivieren, muss das [KB932716](https://support.microsoft.com/kb/932716) -Update Paket installiert werden. Wenn dieses Paket nicht installiert ist, unterstützt Windows XP weiterhin nativ [IMAPI 1,0](imapiv1.md).

> [!Note]  
> Das Windows Feature Pack für Storage steht dem öffentlichen über das [Microsoft Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=63ab51ea-99c9-45c0-980a-c556746fcf05)zur Verfügung. Weitere Informationen zu bestimmten API-Änderungen finden Sie im Abschnitt [Neuerungen](what-s-new.md) .

 

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                             | BESCHREIBUNG                                                                           |
|---------------------------------------------------|---------------------------------------------------------------------------------------|
| [Neuerungen](what-s-new.md)<br/>           | Informationen, die jede bedeutende Version der Image-Mastering-API beschreiben.<br/> |
| [Informationen zu IMAPI](about-imapi.md)<br/>         | Allgemeine Informationen zur Image-Mastering-API.<br/>                         |
| [Verwenden von IMAPI](using-imapi.md)<br/>         | Aufgabenbezogene Themen, die veranschaulichen, wie die Image-Mastering-API verwendet wird.<br/>   |
| [IMAPI-Referenz](imapi-reference.md)<br/> | Ausführliche Beschreibungen von IMAPI-Schnittstellen und anderen Programmier Elementen.<br/>  |



 

## <a name="additional-resources"></a>Zusätzliche Ressourcen

Weitere Informationen zu IMAPI und anderen verwandten Themen finden Sie unter den folgenden Speicherorten:



|                                                                                                  |                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Blog zu optischen Microsoft-Speicher](/archive/blogs/opticalstorage/)                | Hebt Themen hervor, die sich auf die Implementierung der Image-Mastering-API in realen Entwicklungsszenarien konzentrieren.                                                                                                                                                                                                                                                 |
| [Forum zur optischen Platt Form Diskussion](https://social.msdn.microsoft.com/forums/windowsopticalplatform/threads/)              | Erörtern Sie Probleme mit CDROM.SYS, IMAPIv2 und Live File System. Dieses Forum konzentriert sich auf Themen auf Systemebene und ist eher für Anwendungsentwickler als auch für ender vorgesehen.                                                                                                                                                                                                 |
| [T10 Technical Committee](https://www.t10.org/)                       | Ein technisches Committee des internationalen Komitees zu Informationstechnologie Standards ("Einblicke"). Die aufhetzen werden von der-American National Standards Institute (ANSI) genehmigt und unter Regeln angewendet, die von genehmigt werden. Diese Regeln stellen sicher, dass die freiwillig geltenden Standards durch den Konsens von Branchengruppen entwickelt werden. |
| [Optical Storage Technology Association (OSTA)](http://www.osta.org/) | Funktioniert, um die Zukunft der Branche durch reguläre Besprechungen von kommerziellen optischen Speicheranwendungen (Cosa), DVD-Kompatibilität, Marketing, MPV (musicphotovideo), UDF-Komitees und ein neues Adhoc Blue Laser Committee zu gestalten. Interessierte Unternehmen in der ganzen Welt sind eingeladen, der Organisation beizutreten und an Ihren Ausschüssen und Programmen teilzunehmen.               |



 

 

