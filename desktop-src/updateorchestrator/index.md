---
title: Update Orchestrator-API
description: UpdateOrchestrator planen Ihre automatischen Softwareupdates mit Blick auf die Auswirkungen auf den Benutzer.
ms.date: 01/14/2021
ms.topic: overview
ms.openlocfilehash: 6460446397af168a4098a7203179d5587d4dcd9a3cea813991648a5083d07334
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966104"
---
# <a name="updateorchestrator-api"></a>UpdateOrchestrator-API

**UpdateOrchestrator planen** Ihre automatischen Softwareupdates mit Blick auf die Auswirkungen auf den Benutzer. Mit dieser API können Sie automatische Downloads und Installationen sowie deren Anforderungen planen, um Updates zu einem optimalen Zeitpunkt ausführen zu können, der die Auswirkungen der Benutzer minimiert. Diese Features profitieren insbesondere von Leistungssystemen mit eingeschränkten oder langsameren Computingressourcen.

Windows 19H1 enthält eine Lösung der ersten Generation für Anwendungsfälle für automatische Softwareupdates, die von Betriebssystemupdates und Store-App-Updates übernommen wurden, und macht eine anfängliche Version mit eingeschränktem Zugriff dieser API für eine ausgewählte Gruppe von Updatern von Apps im Benutzermodus verfügbar, wie unten beschrieben.

## <a name="features"></a>Features

- Dynamisches Registrieren von Softwareupdatern
 
- Ruft registrierte Softwareupdateer zu optimalen Zeiten auf, z. B. während der Abwesenheit von Benutzer, um "Benutzermodus-Apps" zu aktualisieren.
    - Umfasst die Fähigkeit, die Stromversorgung des Wechselstroms zu "bewachen", um die Auswirkungen auf die Entfernung von Benutzer weiter zu verringern.

- Arbeitet mit einem Vertrauensstellungsmodell, das nur vertrauenswürdige von Drittanbietern registrierte Softwareupdater aufruft.
    - Es gibt erhebliche Risiken, wenn UpdateOrchestrator für alle Aufrufer verfügbar ist, z. B. das Aktualisieren der BIOS-Firmware oder Treiber, wenn ein Benutzer nicht vorhanden ist.  UpdateOrchestrator enthält ein Vertrauensmodell, um diese Risiken zu minimieren.

## <a name="developer-audience"></a>Entwicklerzielgruppe

> [!IMPORTANT]
> Die UpdateOrchestrator-API ist derzeit ein Feature [mit eingeschränktem Zugriff.](/uwp/api/windows.applicationmodel.limitedaccessfeatures) Diese API wird in einer zukünftigen Version öffentlich verfügbar sein.

Verwenden Sie die UpdateOrchestrator-API, wenn Sie bereits über Softwareupdateprogramme im Hintergrund für Win32-Anwendungen im Benutzermodus verfügen, z. B. adobe es updater for Acrobat Reader oder Valve es Valve. Diese Schnittstelle ist für UWP/Store-Anwendungen nicht erforderlich, da die Microsoft Store diese Funktionalität bereits für Softwareupdates nutzt.

Um eine optimale Kundenerfahrung zu bieten, ist dieses erste API-Release auf einen ausgewählten Satz registrierter Updater festgelegt, die die folgenden Kriterien erfüllen:

- Updates nur für Benutzermodusanwendungen
- Keine BIOS-/Firmware-/Geräte- oder Softwaretreiber einbeziehen
    - Das Aktualisieren von BIOS-, Firmware- oder Geräte-/Softwaretreibern, die kein gemeinsames Qualitätskriterien erfüllt haben, stellt ein erhebliches Risiko dar, insbesondere wenn ein Benutzer nicht vorhanden ist. 
- Die Teilnahme an der Nutzung dieser API beinhaltet die Möglichkeit, für alle Inhalte zu spricht, die von Ihren Softwareupdatern im Hintergrund über Überwachungen auf Benutzersystemen heruntergeladen und installiert werden. 

Diese API kann vor der Veröffentlichung erheblich geändert werden.   Während sich die UpdateOrchestrator-API in der Entwicklung befindet, gilt dieses erste Release als Feature mit eingeschränktem Zugriff nur für Updater, die die oben genannten Kriterien zu diesem Zeitpunkt erfüllen.

Unser Ziel ist es, die Funktionalität dieser API zu verbessern und die Auswirkungen mehrerer automatischer Softwareupdates auf die Windows. Wir würden uns über Ihre Beiträge in dieser [**kurzen**](https://aka.ms/UOAPISurvey) Umfrage freuen, um zu verstehen, wie die UpdateOrchestrator-API Ihre Entwickleranforderungen besser erfüllen kann.

