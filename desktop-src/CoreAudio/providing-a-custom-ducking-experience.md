---
description: Eine Anwendung kann die standardmäßige Ducking-Benutzerfreundlichkeit, die vom System verarbeitet wird, ablehnen und durch eine benutzerdefinierte Implementierung ersetzen.
ms.assetid: 18290d05-b114-476b-8365-6bbb5fe6cffc
title: Bereitstellen eines benutzerdefinierten Ducking-Verhaltens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b4051dc7b79f698f10d007beaafa97e90d79f3b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127425"
---
# <a name="providing-a-custom-ducking-behavior"></a><span data-ttu-id="4eec2-103">Bereitstellen eines benutzerdefinierten Ducking-Verhaltens</span><span class="sxs-lookup"><span data-stu-id="4eec2-103">Providing a Custom Ducking Behavior</span></span>

<span data-ttu-id="4eec2-104">Eine Anwendung kann die [standardmäßige Ducking](stream-attenuation.md) -Benutzerfreundlichkeit, die vom System verarbeitet wird, ablehnen und durch eine benutzerdefinierte Implementierung ersetzen.</span><span class="sxs-lookup"><span data-stu-id="4eec2-104">An application can opt out of the [Default Ducking Experience](stream-attenuation.md) handled by the system and replace it with a custom implementation.</span></span>

<span data-ttu-id="4eec2-105">Eine Anwendung kann eine benutzerdefinierte Ducking-Benutzerfreundlichkeit bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="4eec2-105">An application can provide a custom ducking experience.</span></span> <span data-ttu-id="4eec2-106">Beispielsweise bietet Windows Media Player eine eigene Ducking-Umgebung, indem der aktuelle Mediendaten Strom während einer Kommunikationssitzung angehalten und die Wiedergabe fortgesetzt wird, wenn die Sitzung geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="4eec2-106">For example, Windows Media Player provides its own ducking experience by pausing the current media stream during a communication session and resuming playback when the session is closed.</span></span> <span data-ttu-id="4eec2-107">Ein Beispiel für eine Medien Anwendung, die das Ducking implementiert, ist in Windows SDK Beispielen enthalten. Weitere Informationen finden Sie unter [duckingmediaplayer](duckingmediaplayer.md).</span><span class="sxs-lookup"><span data-stu-id="4eec2-107">A sample media application that implements ducking is included with Windows SDK samples; for more information, see [DuckingMediaPlayer](duckingmediaplayer.md).</span></span> <span data-ttu-id="4eec2-108">Informationen zum Simulieren des Öffnens und Schließens von Kommunikationsstreams und zum Erstellen von Ducking-Ereignissen finden Sie unter " [duckingcapturesample](duckingcapturesample.md)", das auch in Windows SDK Beispielen enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="4eec2-108">To simulate the experience of opening and closing communication streams, and generating ducking events, see [DuckingCaptureSample](duckingcapturesample.md), which is also included with Windows SDK samples.</span></span>

<span data-ttu-id="4eec2-109">Eine Medien Anwendung, die zu dämpfende Sounds wieder gibt, muss die Kommunikationsstreams beachten, wenn Sie im System geöffnet und geschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="4eec2-109">A media application that plays sounds to be attenuated must be aware of the communication streams, when they are opened and closed in the system.</span></span> <span data-ttu-id="4eec2-110">Die benutzerdefinierte Implementierung kann mithilfe von mediafoundations, DirectShow oder DirectSound bereitgestellt werden, die die kernaudio-APIs verwenden.</span><span class="sxs-lookup"><span data-stu-id="4eec2-110">The custom implementation can be provided by using MediaFoundation, DirectShow, or DirectSound, which use the Core Audio APIs.</span></span> <span data-ttu-id="4eec2-111">Ein direkter WASAPI-Client kann die Standardbehandlung auch überschreiben, wenn er weiß, wann die Kommunikationssitzung gestartet und beendet wird.</span><span class="sxs-lookup"><span data-stu-id="4eec2-111">A direct WASAPI client can also override the default handling if it knows when the communication session starts and ends.</span></span>

<span data-ttu-id="4eec2-112">**Zum Bereitstellen einer benutzerdefinierten Ducking-Funktion muss ein WASAPI-Client die folgenden Aufgaben ausführen:**</span><span class="sxs-lookup"><span data-stu-id="4eec2-112">**To provide a custom ducking experience, a WASAPI client must perform the following tasks:**</span></span>

1.  <span data-ttu-id="4eec2-113">Registrieren Sie sich für den Empfang von abzurufenden Ereignissen vom *Ducking-Manager*– eine Komponente des Audiosystems, die Benachrichtigungen im Zusammenhang mit Änderungen des Kommunikationsdaten Stroms verarbeitet</span><span class="sxs-lookup"><span data-stu-id="4eec2-113">Register to receive ducking events from the *ducking manager*—a component of the audio system that handles notifications related to communication stream changes.</span></span> <span data-ttu-id="4eec2-114">Weitere Informationen finden Sie unter [erhalten von Ducking-Ereignissen](handling-audio-ducking-events-from-communication-devices.md).</span><span class="sxs-lookup"><span data-stu-id="4eec2-114">For more information, [Getting Ducking Events](handling-audio-ducking-events-from-communication-devices.md).</span></span>
    > [!Note]  
    > <span data-ttu-id="4eec2-115">Wenn der Client für den Empfang von Benachrichtigungen registriert wird, wird das vom System bereitgestellte Standardverhalten deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="4eec2-115">If the client is gets registered to receive ducking notifications, the ducking manager disables the default behavior provided by the system.</span></span> <span data-ttu-id="4eec2-116">Wenn das Standardverhalten explizit deaktiviert ist (siehe [Deaktivieren der standardmäßigen Ducking](disabling-the-ducking-experience.md)-Darstellung) und der Client kein Ersatz Verhalten bereitstellt, tritt bei der Anwendung kein Ducking-Verhalten auf.</span><span class="sxs-lookup"><span data-stu-id="4eec2-116">If the default behavior is disabled explictly (see [Disabling the Default Ducking Experience](disabling-the-ducking-experience.md)) and the client does not provide a substitute behavior, the application does not experience any ducking behavior.</span></span>

     

2.  <span data-ttu-id="4eec2-117">Lauschen Sie auf die vom Ducking-Manager gesendeten Enten Ereignis Benachrichtigungen, und führen Sie das gewünschte Ducking-Verhalten aus.</span><span class="sxs-lookup"><span data-stu-id="4eec2-117">Listen for the duck event notifications sent by the ducking manager and perform the desired ducking behavior.</span></span> <span data-ttu-id="4eec2-118">Weitere Informationen zum Implementieren eines Ducking-Verhaltens finden Sie unter [Implementierungs Überlegungen für Ducking-Benachrichtigungen](handling-audio-ducking-events-from-communication-devices.md).</span><span class="sxs-lookup"><span data-stu-id="4eec2-118">For more information about implementing a ducking behavior, see [Implementation Considerations for Ducking Notifications](handling-audio-ducking-events-from-communication-devices.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4eec2-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4eec2-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4eec2-120">Verwenden eines kommunikationsgeräts</span><span class="sxs-lookup"><span data-stu-id="4eec2-120">Using a Communication Device</span></span>](using-the-communication-device.md)
</dt> <dt>

[<span data-ttu-id="4eec2-121">Standardmäßiges ducken</span><span class="sxs-lookup"><span data-stu-id="4eec2-121">Default Ducking Experience</span></span>](stream-attenuation.md)
</dt> <dt>

[<span data-ttu-id="4eec2-122">Deaktivieren der Standardeinstellung für das ducken</span><span class="sxs-lookup"><span data-stu-id="4eec2-122">Disabling the Default Ducking Experience</span></span>](disabling-the-ducking-experience.md)
</dt> <dt>

[<span data-ttu-id="4eec2-123">Implementierungs Überlegungen für Ducking-Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="4eec2-123">Implementation Considerations for Ducking Notifications</span></span>](handling-audio-ducking-events-from-communication-devices.md)
</dt> <dt>

[<span data-ttu-id="4eec2-124">Erhalten von Ducking-Ereignissen</span><span class="sxs-lookup"><span data-stu-id="4eec2-124">Getting Ducking Events</span></span>](getting-ducking-events-from-a-communication-device.md)
</dt> </dl>

 

 



