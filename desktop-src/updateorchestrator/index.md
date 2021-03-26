---
title: Update Orchestrator-API
description: Updateorchestrator plant Ihre automatischen Software Updates mit Benutzer Beeinträchtigung.
ms.date: 01/14/2021
ms.topic: overview
ms.openlocfilehash: a172cccdc56d2c645bb4e7d048066ca34aea07ba
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/21/2021
ms.locfileid: "103869295"
---
# <a name="updateorchestrator-api"></a>Updateorchestrator-API

**Updateorchestrator** plant Ihre automatischen Software Updates mit Benutzer Beeinträchtigung. Diese API ermöglicht es Ihnen, den automatischen Download und die Installation zusammen mit Ihren Anforderungen zu planen, um Updates zu einem optimalen Zeitpunkt auszuführen, der die Auswirkungen des Benutzers minimiert. Diese Features profitieren insbesondere von niedrigeren Leistungssystemen mit eingeschränkten oder langsameren computingressourcen.

Windows 19h1 umfasst eine erste Generation für automatische Software Update-Anwendungsfälle, die von Betriebssystemupdates übernommen und APP-Updates gespeichert werden, und stellt eine anfängliche "eingeschränkte Zugriffs Version" dieser API für eine ausgewählte Gruppe von Aktualisierer von "User-Mode"-Apps bereit, wie unten beschrieben.

## <a name="features"></a>Features

- Registriert Software-updaterer dynamisch.
 
- Ruft registrierte Softwareupdates während der optimalen Zeiten auf, z. b. während des Benutzer Mangels, um "Benutzermodusanwendungen" zu aktualisieren.
    - Bietet die Möglichkeit, auf der Stromversorgung "aktiv" zu bleiben, um die Auswirkungen auf die Benutzer zu verringern.

- Arbeitet mit einem Vertrauensstellungs Modell, das nur von einem Drittanbieter registrierte Software-Aktualisierungen aufruft.
    - Beim verfügbar machen von updateorchestrator bei allen Aufrufern, wie z. b. Aktualisieren der BIOS-Firmware oder Treiber, wenn ein Benutzer nicht vorhanden ist, besteht ein erhebliches Risiko.  Updateorchestrator enthält ein Vertrauens Modell, um diese Risiken zu mindern.

## <a name="developer-audience"></a>Entwicklerzielgruppe

> [!IMPORTANT]
> Die updateorchestrator-API ist zurzeit ein [eingeschränktes Zugriffs Feature](/uwp/api/windows.applicationmodel.limitedaccessfeatures). Diese API wird in einer zukünftigen Version öffentlich verfügbar.

Verwenden Sie die updateorchestrator-API, wenn Sie bereits über hintergrundsoftwareupdateupdaterer für Win32-Benutzermodusanwendungen verfügen, z. b. den Updater von Adobe für Acrobat Reader oder den Diese Schnittstelle ist für UWP-/Store-Anwendungen nicht erforderlich, da die Microsoft Store diese Funktionalität bereits für Software Updates nutzt.

Um die bestmögliche Benutzerfreundlichkeit zu gewährleisten, ist diese erste API-Version auf einen ausgewählten Satz registrierter updaterer beschränkt, die die folgenden Kriterien erfüllen:

- Nur Updates für Anwendungen im Benutzermodus
- BIOS/Firmware/Gerät oder Software Treiber nicht einbeziehen
    - Das Aktualisieren von BIOS-, Firmware-oder Geräte-/Softwaretreibern, die keine allgemeinen Qualitätskriterien erfüllen, stellt ein erhebliches Risiko dar, insbesondere dann, wenn ein Benutzer nicht vorhanden ist. 
- Die Teilnahme an der Verwendung dieser API erfordert, dass Sie für alle Inhalte, die von ihren background-softwareupdatern auf den Benutzer Systemen per Überwachungen heruntergeladen und installiert werden, bürgen können. 

Diese API kann vor der öffentlichen Freigabe erheblich geändert werden.   Während sich die updateorchestrator-API in der Entwicklungsphase befindet, ist diese erste Version als beschränkte Zugriffs Funktion nur für Update Entwickler vorgesehen, die zu diesem Zeitpunkt die oben aufgeführten Kriterien erfüllen.

Unser Ziel ist es, die Funktionalität dieser API zu verbessern und die Auswirkungen mehrerer automatischer softwareupdateupdaterer unter Windows zu verringern. Wir freuen uns über Ihre Eingaben in dieser [**kurzen Umfrage**](https://aka.ms/UOAPISurvey) , um uns zu helfen, zu verstehen, wie die updateorchestrator-API Ihre Entwickler Anforderungen besser bedienen kann.

