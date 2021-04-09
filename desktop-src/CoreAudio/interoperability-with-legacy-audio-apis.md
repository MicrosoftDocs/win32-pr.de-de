---
description: Interoperabilität mit Legacy-audioapis
ms.assetid: 34939f6d-a6e4-4f7a-afa3-b1fed52b471f
title: Interoperabilität mit Legacy-audioapis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a6b9a80b55695ffcfd3ac54e871f00ea27744d8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958505"
---
# <a name="interoperability-with-legacy-audio-apis"></a>Interoperabilität mit Legacy-audioapis

Viele vorhandene Anwendungen verwenden ältere Audio-APIs, wie z. b. DirectSound, DirectShow und die Multimedia-Funktionen von Windows. Mit nur geringfügigen Änderungen können diese Anwendungen erweitert werden, um [Geräte Rollen](device-roles.md), [Sitzungs-volumesteuerelemente](session-volume-controls.md)und andere Features der Kerncode-APIs in Windows Vista zu verwenden.

Wie im [benutzermodusaudiokomponenten](user-mode-audio-components.md)erläutert, dienen die kernaudioapis als Grundlage für die Erstellung von audioapis auf höherer Ebene. In Windows Vista sind audioendpunktgeräte, die von den kernaudio-APIs implementiert werden, auf audioendpunktgeräten, auf die über Legacy-Audio-APIs wie DirectSound [](audio-endpoint-devices.md) und Windows Media **waveoutxxx** -und **waveinixxx** -Funktionen zugegriffen wird. Aufgrund der inhärenten Einschränkungen in den Schnittstellen von Legacy-audioapis kann eine Anwendung über diese Schnittstellen auf einige Funktionen von audioendpunktgeräten zugreifen. In den folgenden Abschnitten werden Techniken zum Erweitern vorhandener Anwendungen beschrieben, indem direkt über die Kerncode-APIs auf zusätzliche Funktionen von audioendpunktgeräten zugegriffen wird. Diese Verbesserungen erfordern in der Regel nur geringfügige Änderungen am vorhandenen Anwendungscode.

In den folgenden Abschnitten wird beschrieben, wie Features der kernaudioapis in vorhandene Anwendungen integriert werden, die Legacy-audioapis verwenden:

-   [Geräte Rollen für DirectSound-Anwendungen](device-roles-for-directsound-applications.md)
-   [Geräte Rollen für DirectShow-Anwendungen](device-roles-for-directshow-applications.md)
-   [Geräte Rollen für ältere Windows-Multimediaanwendungen](device-roles-for-legacy-windows-multimedia-applications.md)
-   [Audioereignisse für Legacy-Audioanwendungen](audio-events-for-legacy-audio-applications.md)
-   [Benachrichtigungs Sounds für Legacy-Audioanwendungen](notification-sounds-for-legacy-audio-applications.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Geräte Rollen](device-roles.md)
</dt> </dl>

 

 



