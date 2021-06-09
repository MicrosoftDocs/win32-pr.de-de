---
description: Einführung in DirectShow
ms.assetid: 39a701b3-2633-426f-9733-2172ad3ea372
title: Einführung in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5706ff0dec34c5db3762f5782f96804e5c85e889
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2021
ms.locfileid: "111827224"
---
# <a name="introduction-to-directshow"></a>Einführung in DirectShow

Microsoft® DirectShow® ist eine Architektur für Streamingmedien auf der Microsoft Windows®Plattform. DirectShow bietet eine qualitativ hochwertige Erfassung und Wiedergabe von Multimediastreams. Es unterstützt eine Vielzahl von Formaten, einschließlich Advanced Systems Format (ASF), Motion Picture Experts Group (MPEG), Audio-Video Interleaved (AVI), MPEG Audio Layer-3 (MP3) und WAV-Sounddateien. Es unterstützt die Erfassung von digitalen und analogen Geräten basierend auf Windows-Treibermodell (WDM) oder Video für Windows. Er erkennt und verwendet automatisch Hardware für die Video- und Audiobeschleunigung, wenn verfügbar, unterstützt aber auch Systeme ohne Beschleunigungshardware.

DirectShow basiert auf dem Component Object Model (COM). Um eine DirectShow-Anwendung oder -Komponente zu schreiben, müssen Sie die COM-Clientprogrammierung verstehen. Für die meisten Anwendungen müssen Sie keine eigenen COM-Objekte implementieren. DirectShow stellt die benötigten Komponenten zurVerfingung. Wenn Sie DirectShow erweitern möchten, indem Sie Ihre eigenen Komponenten schreiben, müssen Sie diese jedoch als COM-Objekte implementieren.

DirectShow ist für C++ konzipiert. Microsoft stellt keine verwaltete API für DirectShow bereit.

DirectShow vereinfacht die Medienwiedergabe, Formatkonvertierung und Erfassungsaufgaben. Gleichzeitig ermöglicht sie den Zugriff auf die zugrunde liegende Streamsteuerungsarchitektur für Anwendungen, die benutzerdefinierte Lösungen erfordern. Sie können auch eigene DirectShow-Komponenten erstellen, um neue Formate oder benutzerdefinierte Effekte zu unterstützen.

Beispiele für die Anwendungstypen, die Sie mit DirectShow schreiben können, sind Dateiplayer, TV- und DVD-Player, Videobearbeitungsanwendungen, Dateiformatkonverter, Audiovideoerfassungsanwendungen, Encoder und Decoder, Digitale Signalprozessoren und mehr.

Dieser Abschnitt enthält die folgenden Themen:

-   [Neues in DirectShow](whats-new-in-directshow.md)
-   [Unterstützte Formate in DirectShow](supported-formats-in-directshow.md)
-   [DirectShow – Häufig gestellte Fragen](directshow-faq.yml)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erste Schritte](getting-started.md)
</dt> <dt>

[Verwenden von DirectShow](using-directshow.md)
</dt> </dl>

 

 



