---
description: Benachrichtigungs Sounds für Legacy-Audioanwendungen
ms.assetid: c5ad67d9-56fb-4bf0-aea4-5b49b0e5bf95
title: Benachrichtigungs Sounds für Legacy-Audioanwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e9ee2ef1155694e32a21779c55d290da6b3799c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523803"
---
# <a name="notification-sounds-for-legacy-audio-applications"></a>Benachrichtigungs Sounds für Legacy-Audioanwendungen

In Windows Vista weist das Betriebssystem alle System Benachrichtigungs Sounds einer prozessübergreifenden Audiositzung zu, die über das renderingendpunktgerät abgespielt wird, das zurzeit der econsole- [Geräte Rolle](device-roles.md)zugewiesen ist. Das System Volume-Control-Programm sndvol zeigt einen volumeschiebe Regler an, der für System Benachrichtigungs Sounds dediziert ist.

Einige Anwendungen spielen Benachrichtigungs Sounds. Anstatt den Benutzer zu zwingen, die Benachrichtigungs Geräusche einer Anwendung über einen separaten volumeschiebe Regler in sndvol zu verwalten, kann die Anwendung die Benachrichtigungs Geräusche der gleichen Sitzung zuweisen, in der die System Benachrichtigung ertönt. Mit dem Schieberegler sndvol-Volume, der die Systembenachrichtigungs-Sounds steuert, werden die Benachrichtigungs Geräusche der Anwendung gesteuert.

Um dieses Verhalten zu aktivieren, definiert Windows Vista ein snd- \_ Systemflag für die Legacy-Funktion [**PlaySound**](/previous-versions//dd743680(v=vs.85)) . (Dieses Flag wird in früheren Versionen von Windows, einschließlich Windows Server 2003, Windows XP und Windows 2000, nicht unterstützt.) Wenn der Aufrufer dieses Flag festlegt, weist die **PlaySound** -Funktion den Sound, den er wieder gibt, der prozessübergreifenden Sitzung zu, die das Betriebssystem für seine Benachrichtigungs Geräusche verwendet. Wenn der Aufrufer das Flag nicht festgelegt hat, weist **PlaySound** den von ihm wiederverwendeten Sound der Standard Sitzung zu – die prozessspezifische Sitzung, die durch den Sitzungs-GUID-Wert GUID NULL identifiziert wird \_ . Snd \_ System ist in der Header Datei "MMSYSTEM. h" definiert. Weitere Informationen zu **PlaySound** finden Sie in der Windows SDK-Dokumentation.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Interoperabilität mit Legacy-audioapis](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 
