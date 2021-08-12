---
description: Das DirectShow SDK und das Windows Media Format SDK
ms.assetid: d9ac89cc-0d55-4c51-ae0a-592422d97383
title: Das DirectShow SDK und das Windows Media Format SDK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 993f7ea0c9ac47861547cc08662fcb7916c3587c566445960505fe05a5c3d37a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118651757"
---
# <a name="the-directshow-sdk-and-the-windows-media-format-sdk"></a>Das DirectShow SDK und das Windows Media Format SDK

DirectShow und das Windows Media Format SDK bieten ergänzende Lösungen zum Schreiben von Anwendungen, die Windows Medienformatstreams erstellen und wiedergeben. Weitere Informationen finden Sie im Abschnitt["Audio und Video"](../audio-and-video.md)der MSDN Library.

Der ASF Writer-Filter akzeptiert eine beliebige Anzahl von Eingabestreams und erstellt eine ASF-Datei. Der Filter verwendet das Windows Media Format SDK, um nicht komprimierte Audio- oder Videodateien in Windows medienbasierten Inhalt zu konvertieren. Der komprimierte Inhalt wird dann im ASF-Containerformat gespeichert. Wenn der Inhalt nur audio ist, erhält die Datei die Erweiterung WMA und wird als Windows Medienaudiodatei bezeichnet. Wenn es sich bei dem Inhalt nur um Video oder Video und Audio handelt, erhält die Datei die Erweiterung WMV und wird als Windows Medienvideodatei bezeichnet. Beide Dateitypen können auch Metadaten enthalten.

Sie können den WM ASF Writer in verschiedenen Szenarien verwenden, z. B. digitale Videoaufzeichnung (DV), Audiorekomprimierung und Konvertierung von Audio-Video Interleaved -Dateien (AVI) oder MPEG-Multimediadateien für das Netzwerkstreaming. Dieser Filter bietet die einzige Möglichkeit, Microsoft® Windows Media™ Audio -Dateien (WMA) und Windows Media Video-Dateien (WMV) in DirectShow® zu erstellen. Der Filter kann auch Dateien erstellen, die durch Digital Rights Management (DRM) geschützt sind, und mpeg-4-Inhalte mit dem Microsoft MPEG-4-Encoder erstellen. Dieser Inhalt wird im ASF-Containerformat gespeichert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen von ASF-Dateien in DirectShow](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 
