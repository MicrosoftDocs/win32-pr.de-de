---
title: Implementieren der Lizenz Sperrung
description: Implementieren der Lizenz Sperrung
ms.assetid: 50ecfeaa-89cd-4788-a25a-ee0ae8973bf0
keywords:
- Windows Media-Format-SDK, Implementieren der Lizenz Sperrung
- Windows Media-Format-SDK, Lizenz Sperrung
- Windows Media-Format-SDK, Sperren von Lizenzen
- Advanced Systems Format (ASF), Implementieren der Lizenz Sperrung
- ASF (Advanced Systems Format), Implementieren der Lizenz Sperrung
- Advanced Systems Format (ASF), Lizenz Sperrung
- ASF (Advanced Systems Format), Lizenz Sperrung
- Advanced Systems Format (ASF), Widerruf von Lizenzen
- ASF (Advanced Systems Format), Sperrung von Lizenzen
- Digital Rights Management (DRM), Implementieren der Lizenz Sperrung
- DRM (Digital Rights Management), Implementieren der Lizenz Sperrung
- Digital Rights Management (DRM), Lizenz Sperrung
- DRM (Digital Rights Management), Lizenz Sperrung
- Digital Rights Management (DRM), Sperren von Lizenzen
- DRM (Digital Rights Management), Sperren von Lizenzen
- Lizenz Sperrung, implementieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e83bfb1a512b031f5b7c297ecede4ed33fba8f2b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723568"
---
# <a name="implementing-license-revocation"></a>Implementieren der Lizenz Sperrung

Das Windows Media Rights Manager 10 SDK enthält eine Funktion mit dem Namen "Lizenz Sperrung". Mit dieser Funktion können Lizenzserver anfordern, dass Lizenzen vom Client Computer entfernt werden. Das Windows Media-Format-SDK stellt Methoden bereit, mit denen Sperr Nachrichten verarbeitet und die Lizenzen aus dem lokalen Lizenz Speicher entfernt werden.

Der Lizenz Sperrprozess wird von einem Dienst initiiert, der vom Lizenz Aussteller bereitgestellt wird. Die Anwendung kann diesen Dienst hosten, oder Sie kann eine Webanwendung sein. In beiden Fällen muss Ihre Anwendung in der Lage sein, eine vom Dienst erstellte Lizenz Herausforderung zu erhalten.

Um Lizenzen aus dem Lizenz Speicher zu entfernen, führen Sie die folgenden Schritte aus:

1.  Wenn Sie eine Lizenzanfrage vom Lizenz Aussteller erhalten haben, rufen Sie die [**wmfeatelicenserevocationagent**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatelicenserevocationagent) -Funktion auf, um ein Lizenz Sperr-Agent-Objekt zu erstellen und einen Zeiger auf die [**iwmlicenserevocationagent**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserevocationagent) -Schnittstelle zu erhalten.
2.  Rufen Sie die [**iwmlicenserevocationagent:: getlrbchallenge**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicenserevocationagent-getlrbchallenge) -Methode auf, um die Abfrage Antwort zu generieren.
3.  Senden Sie die Abfrage Antwort zurück an die Lizenz Dienst Komponente, von der Sie die Herausforderung erhalten haben.
4.  Die Lizenz Dienst Komponente sendet ein signiertes Lizenz Sperr-BLOB (LRB) an die Anwendung. Wenn Sie Sie empfangen, nennen Sie die [**iwmlicenserevocationagent::P rocess LRB**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicenserevocationagent-processlrb) -Methode. **Processlrb** erstellt eine Bestätigungsnachricht, die Sie zurück an den Lizenz Dienst senden müssen, um zu überprüfen, ob die Lizenzen entfernt wurden.

> [!Note]  
> DRM wird von der x64-basierten Version dieses SDK nicht unterstützt.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Aktivieren DRM-Unterstützung**](enabling-drm-support.md)
</dt> <dt>

[**Iwmlicenserevocationagent-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserevocationagent)
</dt> </dl>

 

 




