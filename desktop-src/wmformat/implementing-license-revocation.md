---
title: Implementieren der Lizenzsperrung
description: Implementieren der Lizenzsperrung
ms.assetid: 50ecfeaa-89cd-4788-a25a-ee0ae8973bf0
keywords:
- Windows Medienformat-SDK, Implementieren der Lizenzsperrung
- Windows Medienformat-SDK,Lizenzsperrung
- Windows Media Format SDK,Sperrung von Lizenzen
- Advanced Systems Format (ASF), Implementieren der Lizenzsperrung
- ASF (Advanced Systems Format),Implementieren der Lizenzsperrung
- Advanced Systems Format (ASF), Lizenzsperrung
- ASF (Advanced Systems Format), Lizenzsperrung
- Advanced Systems Format (ASF), Widerruf von Lizenzen
- ASF (Advanced Systems Format), Widerruf von Lizenzen
- Digital Rights Management (DRM), Implementieren der Lizenzsperrung
- DRM (Digital Rights Management),Implementieren der Lizenzsperrung
- Digital Rights Management (DRM), Lizenzsperrung
- DRM (Digital Rights Management), Lizenzsperrung
- Digital Rights Management (DRM), Widerruf von Lizenzen
- DRM (Digital Rights Management), Widerruf von Lizenzen
- Lizenzsperrung,Implementieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c73d0204e83c941600eefb53579b19ef72217055080c6ef4603d8eac28e08caa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809130"
---
# <a name="implementing-license-revocation"></a>Implementieren der Lizenzsperrung

Das Windows Media Rights Manager 10 SDK enthält ein Feature namens Lizenzsperrung. Mit diesem Feature können Lizenzserver anfordern, dass Lizenzen vom Clientcomputer entfernt werden. Das Windows Media Format SDK stellt Methoden bereit, die Sperrmeldungen verarbeiten und die Lizenzen aus dem lokalen Lizenzspeicher entfernen.

Der Lizenzsperrprozess wird von einem Vom Lizenzaussteller bereitgestellten Dienst initiiert. Ihre Anwendung kann diesen Dienst hosten, oder es kann sich um eine Webanwendung handelt. In beiden Fällen muss Ihre Anwendung in der Lage sein, eine vom Dienst erstellte Lizenzaufforderung zu erhalten.

Führen Sie die folgenden Schritte aus, um Lizenzen aus dem Lizenzspeicher zu entfernen:

1.  Rufen Sie beim Empfang einer Lizenzaufforderung vom Lizenzaussteller die [**WMCreateLicenseRevocationAgent-Funktion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatelicenserevocationagent) auf, um ein Lizenzsperr-Agent-Objekt zu erstellen und einen Zeiger auf die [**IWMLicenseRevocationAgent-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserevocationagent) abzurufen.
2.  Rufen Sie die [**IWMLicenseRevocationAgent::GetLRBChallenge-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicenserevocationagent-getlrbchallenge) auf, um die Abfrageantwort zu generieren.
3.  Senden Sie die Antwort zurück an die Lizenzdienstkomponente, von der Sie die Abfrage erhalten haben.
4.  Die Lizenzdienstkomponente sendet ein signiertes Lizenzsperrblob (LRB) an Ihre Anwendung. Wenn Sie sie erhalten, rufen Sie die [**IWMLicenseRevocationAgent::P rocessLRB-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicenserevocationagent-processlrb) auf. **ProcessLRB** erstellt eine Bestätigungsmeldung, die Sie an den Lizenzdienst zurücksenden müssen, um zu überprüfen, ob die Lizenzen entfernt wurden.

> [!Note]  
> DRM wird von der x64-basierten Version dieses SDK nicht unterstützt.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Aktivieren der DRM-Unterstützung**](enabling-drm-support.md)
</dt> <dt>

[**IWMLicenseRevocationAgent-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserevocationagent)
</dt> </dl>

 

 




