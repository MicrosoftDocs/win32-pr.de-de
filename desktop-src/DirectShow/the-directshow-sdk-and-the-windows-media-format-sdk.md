---
description: Das DirectShow SDK und das Windows Media-Format-SDK
ms.assetid: d9ac89cc-0d55-4c51-ae0a-592422d97383
title: Das DirectShow SDK und das Windows Media-Format-SDK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f85c5553c9a1cdd3f62380c9fc90d836a47a650
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351659"
---
# <a name="the-directshow-sdk-and-the-windows-media-format-sdk"></a>Das DirectShow SDK und das Windows Media-Format-SDK

DirectShow und das Windows Media-Format SDK bieten ergänzende Lösungen zum Schreiben von Anwendungen, mit denen Windows Media-Format Datenströme erstellt und wiedergegeben werden. Weitere Informationen finden Sie im Abschnitt "[Audiodateien und Video](../audio-and-video.md)" der MSDN Library.

Der ASF Writer-Filter akzeptiert eine beliebige Anzahl von Eingabedaten strömen und erstellt eine ASF-Datei. Der Filter verwendet das SDK für den Windows Media-Format, um unkomprimierte Audiodateien oder Videodateien in Windows Media-basierte Inhalte zu konvertieren. Der komprimierte Inhalt wird dann im ASF-Container-Format gespeichert. Wenn es sich bei dem Inhalt nur um Audiodaten handelt, erhält die Datei die Erweiterung. WMA und wird als Windows Media Audio Datei bezeichnet. Wenn der Inhalt nur Video-oder Video-und Audioinhalte ist, erhält die Datei die Erweiterung. WMV und wird als Windows Media Video Datei bezeichnet. Jeder Dateityp kann auch Metadaten enthalten.

Sie können den WM-ASF-Writer in verschiedenen Szenarien verwenden, einschließlich Digital Video (DV) Capture, audiorekomprimierung und Konvertierung von Audio-Video Interleaved (AVI) oder MPEG Multimedia-Dateien für das Netzwerk Streaming. Dieser Filter bietet die einzige Möglichkeit zum Erstellen von Microsoft® Windows Media™-Audiodateien (WMA) und Windows Media Video-Dateien (WMV) in DirectShow-®. Mit dem Filter können auch Dateien erstellt werden, die durch den Digital Rights Management (DRM) gesichert sind. Außerdem können Sie mit dem Microsoft MPEG-4-Encoder MPEG-4-Inhalte erstellen. Dieser Inhalt wird im ASF-Container-Format gespeichert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen von ASF-Dateien in DirectShow](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 
