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
# <a name="notification-sounds-for-legacy-audio-applications"></a><span data-ttu-id="4eecb-103">Benachrichtigungs Sounds für Legacy-Audioanwendungen</span><span class="sxs-lookup"><span data-stu-id="4eecb-103">Notification Sounds for Legacy Audio Applications</span></span>

<span data-ttu-id="4eecb-104">In Windows Vista weist das Betriebssystem alle System Benachrichtigungs Sounds einer prozessübergreifenden Audiositzung zu, die über das renderingendpunktgerät abgespielt wird, das zurzeit der econsole- [Geräte Rolle](device-roles.md)zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="4eecb-104">In Windows Vista, the operating system assigns all of its system notification sounds to a cross-process audio session that plays through the rendering endpoint device that is currently assigned to the eConsole [device role](device-roles.md).</span></span> <span data-ttu-id="4eecb-105">Das System Volume-Control-Programm sndvol zeigt einen volumeschiebe Regler an, der für System Benachrichtigungs Sounds dediziert ist.</span><span class="sxs-lookup"><span data-stu-id="4eecb-105">The system volume-control program, Sndvol, displays a volume slider that is dedicated to system notification sounds.</span></span>

<span data-ttu-id="4eecb-106">Einige Anwendungen spielen Benachrichtigungs Sounds.</span><span class="sxs-lookup"><span data-stu-id="4eecb-106">Some applications play notification sounds.</span></span> <span data-ttu-id="4eecb-107">Anstatt den Benutzer zu zwingen, die Benachrichtigungs Geräusche einer Anwendung über einen separaten volumeschiebe Regler in sndvol zu verwalten, kann die Anwendung die Benachrichtigungs Geräusche der gleichen Sitzung zuweisen, in der die System Benachrichtigung ertönt.</span><span class="sxs-lookup"><span data-stu-id="4eecb-107">Instead of requiring the user to manage an application's notification sounds through a separate volume slider in Sndvol, the application can assign its notification sounds to the same session as the system notification sounds.</span></span> <span data-ttu-id="4eecb-108">Mit dem Schieberegler sndvol-Volume, der die Systembenachrichtigungs-Sounds steuert, werden die Benachrichtigungs Geräusche der Anwendung gesteuert.</span><span class="sxs-lookup"><span data-stu-id="4eecb-108">The Sndvol volume slider that controls the system notification sounds then controls the notification sounds from the application.</span></span>

<span data-ttu-id="4eecb-109">Um dieses Verhalten zu aktivieren, definiert Windows Vista ein snd- \_ Systemflag für die Legacy-Funktion [**PlaySound**](/previous-versions//dd743680(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="4eecb-109">To enable this behavior, Windows Vista defines a SND\_SYSTEM flag for the legacy [**PlaySound**](/previous-versions//dd743680(v=vs.85)) function.</span></span> <span data-ttu-id="4eecb-110">(Dieses Flag wird in früheren Versionen von Windows, einschließlich Windows Server 2003, Windows XP und Windows 2000, nicht unterstützt.) Wenn der Aufrufer dieses Flag festlegt, weist die **PlaySound** -Funktion den Sound, den er wieder gibt, der prozessübergreifenden Sitzung zu, die das Betriebssystem für seine Benachrichtigungs Geräusche verwendet.</span><span class="sxs-lookup"><span data-stu-id="4eecb-110">(This flag is not supported in earlier versions of Windows, including Windows Server 2003, Windows XP, and Windows 2000.) If the caller sets this flag, then the **PlaySound** function assigns the sound that it plays to the cross-process session that the operating system uses for its notification sounds.</span></span> <span data-ttu-id="4eecb-111">Wenn der Aufrufer das Flag nicht festgelegt hat, weist **PlaySound** den von ihm wiederverwendeten Sound der Standard Sitzung zu – die prozessspezifische Sitzung, die durch den Sitzungs-GUID-Wert GUID NULL identifiziert wird \_ .</span><span class="sxs-lookup"><span data-stu-id="4eecb-111">If the caller does not set the flag, then **PlaySound** assigns the sound that it plays to the default session—the process-specific session that is identified by the session GUID value GUID\_NULL.</span></span> <span data-ttu-id="4eecb-112">Snd \_ System ist in der Header Datei "MMSYSTEM. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="4eecb-112">SND\_SYSTEM is defined in the header file Mmsystem.h.</span></span> <span data-ttu-id="4eecb-113">Weitere Informationen zu **PlaySound** finden Sie in der Windows SDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="4eecb-113">For more information about **PlaySound**, see the Windows SDK documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4eecb-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4eecb-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4eecb-115">Interoperabilität mit Legacy-audioapis</span><span class="sxs-lookup"><span data-stu-id="4eecb-115">Interoperability with Legacy Audio APIs</span></span>](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 
