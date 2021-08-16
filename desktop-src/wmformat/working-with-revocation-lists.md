---
title: Arbeiten mit Sperrlisten
description: Arbeiten mit Sperrlisten
ms.assetid: 4463abb5-f48f-484f-b837-512313572c0a
keywords:
- Windows Medienformat-SDK, Sperrlisten
- Advanced Systems Format (ASF), Sperrlisten
- ASF (Advanced Systems Format), Sperrlisten
- Sperrlisten
- Digital Rights Management (DRM), Sperrlisten
- DRM (Verwaltung digitaler Rechte),Sperrlisten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d022b9b55a1a14b147d76d289efeac956bae8f1858d155f138efa579d533fa9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118194880"
---
# <a name="working-with-revocation-lists"></a>Arbeiten mit Sperrlisten

Um auf Sicherheitsverletzungen zu reagieren und sicherzustellen, dass Playeranwendungen, die bekanntermaßen fehlerhaft oder kompromittiert sind, keine geschützten Dateien wiedergeben oder verwenden können, enthält jede ausgestellte Lizenz eine Sperrliste. Eine Sperrliste enthält die Anwendungszertifikate aller Playeranwendungen, die bekanntermaßen fehlerhaft oder beschädigt sind. Wenn eine neue Lizenz empfangen wird, prüft die DRM-Komponente der Playeranwendung auf eine Sperrliste. Wenn eine gefunden wird, die neuer ist als die, die sich derzeit auf dem Computer befindet, wird die neuere Liste gespeichert. Wenn der Consumer das nächste Mal eine geschützte ASF-Datei abspielt, vergleicht die DRM-Komponente die Playeranwendung mit der Sperrliste. Wenn die Playeranwendung widerrufen wird, sendet die DRM-Komponente eine Fehlermeldung an die Anwendung.

Playeranwendungen können in den folgenden Szenarien eine Sperrfehlermeldung erhalten:

-   Die Fehlermeldung wird empfangen, nachdem die Anwendung die [**IWMDRMReader::AcquireLicense-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense) für eine geschützte Datei aufruft. Der Aufruf schlägt mit dem **HRESULT-Code** NS \_ E \_ DRM \_ APPCERT \_ REVOKED fehl, der für die **OnStatus-Rückruffunktion** mit dem WMT \_ ACQUIRE \_ LICENSE-Status bereitgestellt wird. Wenn dieser **HRESULT-Code** ignoriert wird, treten weiterhin Fehler auf.
-   Die Fehlermeldung wird empfangen, wenn die Anwendung den DRM-fähigen Reader erstellt und die [**IWMReader::Open-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) für eine geschützte Datei aufruft. Der Aufruf schlägt mit dem **HRESULT-Code** NS \_ E \_ DRM \_ APPCERT \_ REVOKED fehl, der für die [**IWMStatusCallback::OnStatus-Rückrufmethode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) mit dem WMT \_ OPENED-Status bereitgestellt wird. Wenn eine Playeranwendung diese Fehlermeldung empfängt, sollte die Anwendung Endbenutzer benachrichtigen und ihnen eine Möglichkeit bieten, die Funktionalität für ihren Player wiederherzustellen. Beispielsweise kann die Anwendung eine URL öffnen, unter der Endbenutzer ein Upgrade für die kompromittierte Anwendung herunterladen können.

**Hinweis** DRM wird von der x64-basierten Version dieses SDK nicht unterstützt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Digital Rights Management Features**](digital-rights-management-features.md)
</dt> <dt>

[**Behandeln von Lizenzerwerbsereignissen**](handling-license-acquisition-events.md)
</dt> </dl>

 

 




