---
description: Benachrichtigungsgeräusche für Ältere Audioanwendungen
ms.assetid: c5ad67d9-56fb-4bf0-aea4-5b49b0e5bf95
title: Benachrichtigungsgeräusche für Ältere Audioanwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4ce813fb2d38a9995f929c62936879f502392415d040e88ddb50f3b4699734a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077524"
---
# <a name="notification-sounds-for-legacy-audio-applications"></a>Benachrichtigungsgeräusche für Ältere Audioanwendungen

In Windows Vista weist das Betriebssystem alle Systembenachrichtigungs-Sounds einer prozessübergreifenden Audiositzung zu, die über das Renderingendpunktgerät abspielt, das derzeit der eConsole-Geräterolle zugewiesen [ist.](device-roles.md) Das Systemvolumesteuerungsprogramm Sndvol zeigt einen Volumeschieberegler an, der für Systembenachrichtigungs-Sounds de dedicated ist.

Einige Anwendungen geben Benachrichtigungsgeräusche wieder. Anstatt den Benutzer zur Verwaltung der Benachrichtigungsgeräusche einer Anwendung über einen separaten Volumeschieberegler in Sndvol zu schieben, kann die Anwendung seine Benachrichtigungsgeräusche derselben Sitzung zuweisen, in der die Systembenachrichtigung klingt. Der Sndvol-Volumeschieberegler, der die Systembenachrichtigung steuert, steuert dann die Benachrichtigungsgeräusche der Anwendung.

Um dieses Verhalten zu aktivieren, Windows Vista ein SND \_ SYSTEM-Flag für die legacy [**PlaySound-Funktion**](/previous-versions//dd743680(v=vs.85)) definiert. (Dieses Flag wird in früheren Versionen von Windows nicht unterstützt, einschließlich Windows Server 2003, Windows XP und Windows 2000.) Wenn der Aufrufer dieses Flag fest legt, weist die **PlaySound-Funktion** den Sound, den er abspielt, der prozessübergreifenden Sitzung zu, die das Betriebssystem für seine Benachrichtigungssounds verwendet. Wenn der Aufrufer das Flag nicht festgelegt hat, weist **PlaySound** den Sound, den er wiedergibt, der Standardsitzung zu– der prozessspezifischen Sitzung, die durch den SITZUNGs-GUID-Wert GUID NULL identifiziert \_ wird. SND \_ SYSTEM wird in der Headerdatei Mmsystem.h definiert. Weitere Informationen zu **PlaySound** finden Sie in der dokumentation Windows SDK.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Interoperabilität mit Legacyaudio-APIs](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 
