---
title: Arbeiten mit Sperr Listen
description: Arbeiten mit Sperr Listen
ms.assetid: 4463abb5-f48f-484f-b837-512313572c0a
keywords:
- Windows Media-Format-SDK, Sperr Listen
- Advanced Systems Format (ASF), Sperr Listen
- ASF (Advanced Systems Format), Sperr Listen
- Sperr Listen
- Digital Rights Management (DRM), Sperr Listen
- DRM (Digital Rights Management), Sperr Listen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75f4eca82dd82c9225406a85034ff2a6df227fce
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104516580"
---
# <a name="working-with-revocation-lists"></a>Arbeiten mit Sperr Listen

Um auf Sicherheitsverletzungen zu reagieren und sicherzustellen, dass Player-Anwendungen, die bekanntermaßen beschädigt oder kompromittiert sind, keine geschützten Dateien wiedergeben oder verwenden können, enthält jede ausgegebene Lizenz eine Sperr Liste. Eine Sperr Liste enthält die Anwendungs Zertifikate aller Player-Anwendungen, die bekanntermaßen beschädigt oder beschädigt sind. Beim Empfang einer neuen Lizenz wird von der DRM-Komponente der Player Anwendung eine Sperr Liste geprüft. Wenn eine neue gefunden wird, die aktueller als die derzeit auf dem Computer ist, wird die neuere Liste gespeichert. Wenn der Consumer das nächste Mal eine geschützte ASF-Datei abspielt, vergleicht die DRM-Komponente die Player Anwendung mit der Sperr Liste. Wenn die Player Anwendung widerrufen wird, sendet die DRM-Komponente eine Fehlermeldung an die Anwendung.

Spieler Anwendungen können in den folgenden Szenarien eine Sperr Fehlermeldung erhalten:

-   Die Fehlermeldung wird empfangen, nachdem die Anwendung die [**iwmdrmreader:: AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense) -Methode für eine geschützte Datei aufgerufen hat. Der-Befehl schlägt fehl, wenn der **HRESULT** -Code NS \_ E \_ DRM \_ appcert \_ widerrufen wurde, der für die **OnStatus** -Rückruffunktion mit dem WMT-Abruf \_ Lizenzstatus bereitgestellt wird \_ . Wenn dieser **HRESULT** -Code ignoriert wird, treten Fehler weiterhin auf.
-   Die Fehlermeldung wird empfangen, wenn die Anwendung den DRM-fähigen Reader erstellt und die [**iwmreader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) -Methode für eine geschützte Datei aufruft. Der-Befehl schlägt fehl, wenn der **HRESULT** -Code NS \_ E \_ DRM \_ appcert \_ widerrufen wurde, der für die [**iwmstatuscallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) -Rückruf Methode mit dem geöffneten WMT-Status bereitgestellt wird \_ . Wenn eine Player Anwendung diese Fehlermeldung empfängt, sollte Sie von der Anwendung benachrichtigt und eine Möglichkeit zum Wiederherstellen der Funktionalität für Ihren Player bereitgestellt werden. Die Anwendung kann z. b. eine URL öffnen, in der Endbenutzer ein Upgrade für die kompromittierte Anwendung herunterladen können.

**Hinweis** DRM wird von der x64-basierten Version dieses SDK nicht unterstützt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Features digitaler Rights Management**](digital-rights-management-features.md)
</dt> <dt>

[**Behandeln von Lizenz Erwerbs Ereignissen**](handling-license-acquisition-events.md)
</dt> </dl>

 

 




