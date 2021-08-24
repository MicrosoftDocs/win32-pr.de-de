---
description: Interoperabilität mit Legacy-Audio-APIs
ms.assetid: 34939f6d-a6e4-4f7a-afa3-b1fed52b471f
title: Interoperabilität mit Legacy-Audio-APIs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f894c20785ebd49e50765ad67ba19056f5439bd5ab8c8fc7e0bcfbdd05fe04ed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875430"
---
# <a name="interoperability-with-legacy-audio-apis"></a>Interoperabilität mit Legacy-Audio-APIs

Viele vorhandene Anwendungen verwenden Legacy-Audio-APIs wie DirectSound, DirectShow und die Windows Multimediafunktionen. Mit nur geringfügigen Änderungen können diese Anwendungen erweitert werden, um [Geräterollen,](device-roles.md) [Sitzungsvolumesteuerelemente](session-volume-controls.md)und andere Features der Kernaudio-APIs in Windows Vista zu nutzen.

Wie unter [Benutzermodus-Audiokomponenten](user-mode-audio-components.md)erläutert, bilden die Kern-Audio-APIs die Grundlage, auf der audio-APIs auf höherer Ebene erstellt werden. In Windows Vista sind die Audiogeräte, auf die Anwendungen über Legacy-Audio-APIs wie DirectSound und die Windows **Medienfunktionen waveOutXxx** und **waveInXxx** zugreifen, tatsächlich [Audioendpunktgeräte,](audio-endpoint-devices.md) die von den Kernaudio-APIs implementiert werden. Aufgrund der inhärenten Einschränkungen in den Schnittstellen von Legacy-Audio-APIs kann eine Anwendung über diese Schnittstellen auf einige, aber nicht alle Funktionen von Audioendpunktgeräten zugreifen. In den folgenden Abschnitten werden Techniken zum Verbessern vorhandener Anwendungen beschrieben, indem auf zusätzliche Funktionen von Audioendpunktgeräten direkt über die Kernaudio-APIs zugegriffen wird. Diese Erweiterungen erfordern in der Regel nur geringfügige Änderungen am vorhandenen Anwendungscode.

In den folgenden Abschnitten wird beschrieben, wie Sie Features der Kernaudio-APIs in vorhandene Anwendungen integrieren, die Legacy-Audio-APIs verwenden:

-   [Geräterollen für DirectSound-Anwendungen](device-roles-for-directsound-applications.md)
-   [Geräterollen für DirectShow-Anwendungen](device-roles-for-directshow-applications.md)
-   [Geräterollen für Legacy-Windows Multimediaanwendungen](device-roles-for-legacy-windows-multimedia-applications.md)
-   [Audioereignisse für Legacyaudioanwendungen](audio-events-for-legacy-audio-applications.md)
-   [Benachrichtigungsgeräusche für Legacyaudioanwendungen](notification-sounds-for-legacy-audio-applications.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Geräterollen](device-roles.md)
</dt> </dl>

 

 



