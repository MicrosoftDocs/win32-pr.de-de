---
description: In diesem Abschnitt wird beschrieben, wie Sie die transcodieren-API zum erneuten Codieren von Mediendateien verwenden. Die transcodieren-API wurde in Windows 7 eingeführt.
ms.assetid: 24bf68a8-39bf-4302-b28c-71bb23b63469
title: Transcode-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9783c6f99a25ba6835171dcc7f7555a1f747c72b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863943"
---
# <a name="transcode-api"></a>Transcode-API

In diesem Abschnitt wird beschrieben, wie Sie die transcodieren-API zum erneuten Codieren von Mediendateien verwenden. Die transcodieren-API wurde in Windows 7 eingeführt.

*Transcoding* ist die Konvertierung einer digitalen Mediendatei von einem Format in ein anderes. Die transcodieren-API ist für die Verwendung mit der [Medien Sitzung](media-session.md)konzipiert. Es vereinfacht die Verwendung der Medien Sitzung für bestimmte Arten von Transcodierungs Anwendungen:

-   CBR-Codierung (Constant Bitrate), bei der die Zielbitrate im Voraus bekannt ist.
-   Höchstens einen Audiostream und einen Videostream.
-   Codierung von und in eine Datei.

Die transcode-API unterstützt Folgendes nicht:

-   Variablenbitrate (VBR) oder Multipass-Codierung.
-   Mehrere Audiostreams oder mehrere Videostreams.
-   DRM-geschützter Inhalt, der nicht mit WMDRM geschützten ASF-Dateien ist.
-   Live Streaming, z. b. Live-zu-Datei-Streaming oder Live-zu-Live-Streaming.

Wenn Ihre Codierungs Anwendung in diese Einschränkungen passt, ist die transcodieren-API ein einfacheres Programmiermodell, als die Medien Sitzung allein zu verwenden.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                          | BESCHREIBUNG                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informationen zur transcode-API](about-the-transcode-api.md)<br/>                              | Bietet eine allgemeine Übersicht über die transcodieren-API.<br/>                                                                                                                                                                |
| [Verwenden der transcode-API](fast-transcode-objects.md)<br/>                               | Beschreibt, wie eine Anwendung die transcodieren-API verwendet.<br/>                                                                                                                                                             |
| [Tutorial: Codieren einer MP4-Datei](tutorial--encoding-an-mp4-file-.md)<br/>               | Ein schrittweises Tutorial, das zeigt, wie Sie die transcodieren-API verwenden, um eine MP4-Datei zu codieren.<br/>                                                                                                                           |
| [Tutorial: Codieren einer WMA-Datei](tutorial--converting-an-mp3-file-to-a-wma-file.md)<br/> | Zeigt, wie Sie die transcodieren-API verwenden, um eine WMA-Datei zu codieren. In diesem Tutorial wird der in [Tutorial: Codieren einer MP4-Datei](tutorial--encoding-an-mp4-file-.md)gezeigte Code geändert. Sie sollten daher zuerst das Lernprogramm Lesen.<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Codierung und Dateierstellung](encoding-and-file-authoring.md)
</dt> <dt>

[Media Foundation: Grundlegende Konzepte](media-foundation-programming--essential-concepts.md)
</dt> <dt>

[Übersicht über die Codierung in Media Foundation](overview-of-encoding-in-media-foundation.md)
</dt> </dl>

 

 




