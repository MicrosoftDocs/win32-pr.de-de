---
description: Einführung in DirectShow
ms.assetid: 39a701b3-2633-426f-9733-2172ad3ea372
title: Einführung in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01733db5f8168a67871ec1797f79cd10a90c6c22
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124352"
---
# <a name="introduction-to-directshow"></a>Einführung in DirectShow

Microsoft® DirectShow® ist eine Architektur für das Streaming von Medien auf der Microsoft Windows®-Plattform. DirectShow bietet eine qualitativ hochwertige Erfassung und Wiedergabe von Multimedia-Streams. Es unterstützt eine Vielzahl von Formaten, einschließlich Advanced Systems Format (ASF), Motion Picture Experts Group (MPEG), Audio-Video Interleaved (AVI), MPEG Audio Layer-3 (MP3) und wav Soundfiles. Sie unterstützt die Erfassung von digitalen und analogen Geräten basierend auf dem Windows-Treibermodell (WDM) oder Video für Windows. Sie erkennt und verwendet automatisch Video-und audioacceleration-Hardware, wenn Sie verfügbar ist, aber auch Systeme ohne Beschleunigung der Hardware unterstützt.

DirectShow basiert auf dem Component Object Model (com). Um eine DirectShow-Anwendung oder-Komponente zu schreiben, müssen Sie mit der com-Client Programmierung vertraut sein. Bei den meisten Anwendungen müssen Sie keine eigenen com-Objekte implementieren. DirectShow stellt die Komponenten bereit, die Sie benötigen. Wenn Sie DirectShow durch Schreiben Ihrer eigenen Komponenten erweitern möchten, müssen Sie Sie jedoch als COM-Objekte implementieren.

DirectShow ist für C++ konzipiert. Microsoft stellt keine verwaltete API für DirectShow bereit.

DirectShow vereinfacht die Medienwiedergabe, die Formatkonvertierung und Erfassungs Tasks. Gleichzeitig ermöglicht Sie den Zugriff auf die zugrunde liegende Stream-Steuerungsarchitektur für Anwendungen, die benutzerdefinierte Lösungen erfordern. Sie können auch eigene DirectShow-Komponenten erstellen, um neue Formate oder benutzerdefinierte Effekte zu unterstützen.

Beispiele für die Anwendungs Typen, die Sie mit DirectShow schreiben können, sind u. a. Datei Player, TV-und DVD-Player, Videobearbeitungsanwendungen, Dateiformatkonverter, Audiovideo-Erfassungs Anwendungen, Encoder und Decoders, digitale Signalprozessoren und mehr.

Dieser Abschnitt enthält die folgenden Themen:

-   [Neues in DirectShow](whats-new-in-directshow.md)
-   [Unterstützte Formate in DirectShow](supported-formats-in-directshow.md)
-   [FAQ zu DirectShow](directshow-faq.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erste Schritte](getting-started.md)
</dt> <dt>

[Verwenden von DirectShow](using-directshow.md)
</dt> </dl>

 

 



