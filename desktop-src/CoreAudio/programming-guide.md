---
description: Programmierhandbuch
ms.assetid: 825c7cd7-dc66-47b6-a1b6-d10101daebb3
title: Leitfaden zur Kern Audioprogrammierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cb99369058983ebac7205053efdf967bbb8c36d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214264"
---
# <a name="core-audio-programming-guide"></a><span data-ttu-id="c5600-103">Leitfaden zur Kern Audioprogrammierung</span><span class="sxs-lookup"><span data-stu-id="c5600-103">Core Audio Programming Guide</span></span>

<span data-ttu-id="c5600-104">In diesem Leitfaden werden die Konzepte und Features der Kerncode-APIs von Windows Vista erläutert und beschrieben, wie Sie in der Anwendungsprogrammierung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c5600-104">This guide section explains the concepts and features of the core audio APIs of Windows Vista, and describes how to use them in application programming.</span></span>

<span data-ttu-id="c5600-105">In diesem Abschnitt werden die folgenden Themen behandelt:</span><span class="sxs-lookup"><span data-stu-id="c5600-105">This section contains the following topics.</span></span>



| <span data-ttu-id="c5600-106">Thema</span><span class="sxs-lookup"><span data-stu-id="c5600-106">Topic</span></span>                                                                                                                      | <span data-ttu-id="c5600-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c5600-107">Description</span></span>                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c5600-108">Benutzermodusaudiokomponenten</span><span class="sxs-lookup"><span data-stu-id="c5600-108">User-Mode Audio Components</span></span>](user-mode-audio-components.md)                                                               | <span data-ttu-id="c5600-109">Über die Low-Level-Schnittstellen in den kernaudioapis kann ein Client auf die Systemkomponenten zugreifen, die Audiostreams verwalten und mischen.</span><span class="sxs-lookup"><span data-stu-id="c5600-109">Through the low-level interfaces in the core audio APIs, a client can access the system components that manage and mix audio streams.</span></span>                                                                        |
| [<span data-ttu-id="c5600-110">Geschützter benutzermodusaudiodatei (Puma)</span><span class="sxs-lookup"><span data-stu-id="c5600-110">Protected User Mode Audio (PUMA)</span></span>](protected-user-mode-audio--puma-.md)                                                   | <span data-ttu-id="c5600-111">In diesem Thema werden die Aktualisierungen für die Audioverarbeitung (Protected User Mode, Puma) des benutzermodusaudiomoduls in der geschützten Umgebung (PE) beschrieben, das eine sicherere Umgebung für die Audioverarbeitung und das Rendering bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="c5600-111">Describes the updates to Protected User Mode Audio (PUMA), the user-mode audio engine in the Protected Environment (PE), which provides a safer environment for audio processing and rendering.</span></span>              |
| [<span data-ttu-id="c5600-112">Audioendpunktgeräte</span><span class="sxs-lookup"><span data-stu-id="c5600-112">Audio Endpoint Devices</span></span>](audio-endpoint-devices.md)                                                                       | <span data-ttu-id="c5600-113">Bei einem audioendpunktgerät handelt es sich um eine Software Abstraktion, die benutzerfreundliche Interaktionen mit Audiogeräten wie z. b. Mikrofon und Referenten ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="c5600-113">An audio endpoint device is a software abstraction that enables user-friendly interactions with audio devices such as microphones and speakers.</span></span>                                                              |
| [<span data-ttu-id="c5600-114">Audiositzungen</span><span class="sxs-lookup"><span data-stu-id="c5600-114">Audio Sessions</span></span>](audio-sessions.md)                                                                                       | <span data-ttu-id="c5600-115">Eine Audiositzung ist eine Software Abstraktion, die es einem Client ermöglicht, eine Sammlung verwandter Audiostreams als einzelne Einheit zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="c5600-115">An audio session is a software abstraction that enables a client to manage a collection of related audio streams as a single unit.</span></span>                                                                           |
| [<span data-ttu-id="c5600-116">Lautstärkeregler</span><span class="sxs-lookup"><span data-stu-id="c5600-116">Volume Controls</span></span>](volume-controls.md)                                                                                     | <span data-ttu-id="c5600-117">Das System integriert seine Richtlinien basierten Volumeeinstellungen auf logische und konsistente Weise mit den Volumeeinstellungen des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="c5600-117">The system integrates its policy-based volume settings with the user's volume settings in a logical and consistent way.</span></span>                                                                                      |
| [<span data-ttu-id="c5600-118">Datenstrom Verwaltung</span><span class="sxs-lookup"><span data-stu-id="c5600-118">Stream Management</span></span>](stream-management.md)                                                                                 | <span data-ttu-id="c5600-119">Die Windows-audiositzungs-API (WASAPI) stellt einen Client mit einem kompletten Satz von Methoden zum Erstellen und Verwalten von Audiodatenströmen bereit.</span><span class="sxs-lookup"><span data-stu-id="c5600-119">The Windows Audio Session API (WASAPI) provides a client with a complete set of methods for creating and managing audio streams.</span></span>                                                                             |
| [<span data-ttu-id="c5600-120">Gerätetopologien</span><span class="sxs-lookup"><span data-stu-id="c5600-120">Device Topologies</span></span>](device-topologies.md)                                                                                 | <span data-ttu-id="c5600-121">Mit der-API für die Geräte-API kann ein Client die Audiosteuerelemente ermitteln, die sich entlang der verschiedenen Daten Pfade in der Audiohardware befinden.</span><span class="sxs-lookup"><span data-stu-id="c5600-121">The DeviceTopology API enables a client to discover the audio controls that lie along the various data paths in the audio hardware.</span></span>                                                                          |
| [<span data-ttu-id="c5600-122">Verwenden der ikscontrol-Schnittstelle für den Zugriff auf Audioeigenschaften</span><span class="sxs-lookup"><span data-stu-id="c5600-122">Using the IKsControl Interface to Access Audio Properties</span></span>](using-the-ikscontrol-interface-to-access-audio-properties.md) | <span data-ttu-id="c5600-123">Eine spezialisierte Audioanwendung muss möglicherweise die "ikscontrol"-Schnittstelle verwenden, um auf die Eigenschaften eines audioadapters zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="c5600-123">A specialized audio application might need to use the IKsControl interface to access the properties of an audio adapter.</span></span>                                                                                     |
| [<span data-ttu-id="c5600-124">Interoperabilität mit Legacy-audioapis</span><span class="sxs-lookup"><span data-stu-id="c5600-124">Interoperability with Legacy Audio APIs</span></span>](interoperability-with-legacy-audio-apis.md)                                     | <span data-ttu-id="c5600-125">Die wichtigsten Features der kernaudio-APIs in Windows Vista können in vorhandene Anwendungen integriert werden, die DirectSound, DirectShow und die Windows- **multimediawaveoutxxx** -und **waveinxxx** -Funktionen verwenden.</span><span class="sxs-lookup"><span data-stu-id="c5600-125">Key features of the core audio APIs in Windows Vista can be incorporated into existing applications that use DirectSound, DirectShow, and the Windows multimedia **waveOutXxx** and **waveInXxx** functions.</span></span> |
| [<span data-ttu-id="c5600-126">Raumklang</span><span class="sxs-lookup"><span data-stu-id="c5600-126">Spatial Sound</span></span>](spatial-sound.md)                                                                                         | <span data-ttu-id="c5600-127">Bietet Anleitungen für die Verwendung von Windows Sonic, der Plattform auf Platt Form Ebene von Microsoft für räumliche Audiounterstützung auf Xbox und Windows und ermöglicht sowohl das umschließen als auch das erhöhen (oberhalb oder unterhalb der Listener) Audiohinweise.</span><span class="sxs-lookup"><span data-stu-id="c5600-127">Provides guidance for using Windows Sonic, Microsoft’s platform-level solution for spatial sound support on Xbox and Windows, enabling both surround and elevation (above or below the listener) audio cues.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="c5600-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c5600-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5600-129">Kernaudioapis</span><span class="sxs-lookup"><span data-stu-id="c5600-129">Core Audio APIs</span></span>](core-audio-apis-in-windows-vista.md)
</dt> </dl>

 

 



