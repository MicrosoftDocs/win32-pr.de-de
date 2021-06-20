---
description: Erfahren Sie mehr über die Konzepte und Features der Kernaudio-APIs von Windows Vista und deren Verwendung in der Anwendungsprogrammierung.
ms.assetid: 825c7cd7-dc66-47b6-a1b6-d10101daebb3
title: Core Audio Programming Guide
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02f02e27206c70cca69abf263cfa49dfd439c480
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405873"
---
# <a name="core-audio-programming-guide"></a><span data-ttu-id="6dd78-103">Core Audio Programming Guide</span><span class="sxs-lookup"><span data-stu-id="6dd78-103">Core Audio Programming Guide</span></span>

<span data-ttu-id="6dd78-104">In diesem Leitfadenabschnitt werden die Konzepte und Features der Kernaudio-APIs von Windows Vista sowie deren Verwendung in der Anwendungsprogrammierung erläutert.</span><span class="sxs-lookup"><span data-stu-id="6dd78-104">This guide section explains the concepts and features of the core audio APIs of Windows Vista, and describes how to use them in application programming.</span></span>

<span data-ttu-id="6dd78-105">In diesem Abschnitt werden die folgenden Themen behandelt:</span><span class="sxs-lookup"><span data-stu-id="6dd78-105">This section contains the following topics.</span></span>



| <span data-ttu-id="6dd78-106">Thema</span><span class="sxs-lookup"><span data-stu-id="6dd78-106">Topic</span></span>                                                                                                                      | <span data-ttu-id="6dd78-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6dd78-107">Description</span></span>                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6dd78-108">Benutzermodus-Audiokomponenten</span><span class="sxs-lookup"><span data-stu-id="6dd78-108">User-Mode Audio Components</span></span>](user-mode-audio-components.md)                                                               | <span data-ttu-id="6dd78-109">Über die Low-Level-Schnittstellen in den Kernaudio-APIs kann ein Client auf die Systemkomponenten zugreifen, die Audiostreams verwalten und mischen.</span><span class="sxs-lookup"><span data-stu-id="6dd78-109">Through the low-level interfaces in the core audio APIs, a client can access the system components that manage and mix audio streams.</span></span>                                                                        |
| [<span data-ttu-id="6dd78-110">Audio im geschützten Benutzermodus (PROTECTED)</span><span class="sxs-lookup"><span data-stu-id="6dd78-110">Protected User Mode Audio (PUMA)</span></span>](protected-user-mode-audio--puma-.md)                                                   | <span data-ttu-id="6dd78-111">Beschreibt die Updates für Protected User Mode Audio (CSV), die Benutzermodus-Audio-Engine in der geschützten Umgebung (PE), die eine sicherere Umgebung für die Audioverarbeitung und das Rendering bietet.</span><span class="sxs-lookup"><span data-stu-id="6dd78-111">Describes the updates to Protected User Mode Audio (PUMA), the user-mode audio engine in the Protected Environment (PE), which provides a safer environment for audio processing and rendering.</span></span>              |
| [<span data-ttu-id="6dd78-112">Audioendpunktgeräte</span><span class="sxs-lookup"><span data-stu-id="6dd78-112">Audio Endpoint Devices</span></span>](audio-endpoint-devices.md)                                                                       | <span data-ttu-id="6dd78-113">Ein Audioendpunktgerät ist eine Softwareabstraktion, die benutzerfreundliche Interaktionen mit Audiogeräten wie Mikrofonen und Lautsprechern ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="6dd78-113">An audio endpoint device is a software abstraction that enables user-friendly interactions with audio devices such as microphones and speakers.</span></span>                                                              |
| [<span data-ttu-id="6dd78-114">Audiositzungen</span><span class="sxs-lookup"><span data-stu-id="6dd78-114">Audio Sessions</span></span>](audio-sessions.md)                                                                                       | <span data-ttu-id="6dd78-115">Eine Audiositzung ist eine Softwareabstraktion, die es einem Client ermöglicht, eine Sammlung verwandter Audiostreams als einzelne Einheit zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="6dd78-115">An audio session is a software abstraction that enables a client to manage a collection of related audio streams as a single unit.</span></span>                                                                           |
| [<span data-ttu-id="6dd78-116">Lautstärkeregler</span><span class="sxs-lookup"><span data-stu-id="6dd78-116">Volume Controls</span></span>](volume-controls.md)                                                                                     | <span data-ttu-id="6dd78-117">Das System integriert seine richtlinienbasierten Volumeeinstellungen logisch und konsistent in die Volumeeinstellungen des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="6dd78-117">The system integrates its policy-based volume settings with the user's volume settings in a logical and consistent way.</span></span>                                                                                      |
| [<span data-ttu-id="6dd78-118">Streamverwaltung</span><span class="sxs-lookup"><span data-stu-id="6dd78-118">Stream Management</span></span>](stream-management.md)                                                                                 | <span data-ttu-id="6dd78-119">Die Windows-Audiositzungs-API (WASAPI) bietet einem Client einen vollständigen Satz von Methoden zum Erstellen und Verwalten von Audiostreams.</span><span class="sxs-lookup"><span data-stu-id="6dd78-119">The Windows Audio Session API (WASAPI) provides a client with a complete set of methods for creating and managing audio streams.</span></span>                                                                             |
| [<span data-ttu-id="6dd78-120">Gerätetopologien</span><span class="sxs-lookup"><span data-stu-id="6dd78-120">Device Topologies</span></span>](device-topologies.md)                                                                                 | <span data-ttu-id="6dd78-121">Mit der DeviceTopology-API kann ein Client die Audiosteuerelemente ermitteln, die sich entlang der verschiedenen Datenpfade in der Audiohardware befinden.</span><span class="sxs-lookup"><span data-stu-id="6dd78-121">The DeviceTopology API enables a client to discover the audio controls that lie along the various data paths in the audio hardware.</span></span>                                                                          |
| [<span data-ttu-id="6dd78-122">Verwenden der IKsControl-Schnittstelle für den Zugriff auf Audioeigenschaften</span><span class="sxs-lookup"><span data-stu-id="6dd78-122">Using the IKsControl Interface to Access Audio Properties</span></span>](using-the-ikscontrol-interface-to-access-audio-properties.md) | <span data-ttu-id="6dd78-123">Eine spezielle Audioanwendung muss möglicherweise die IKsControl-Schnittstelle verwenden, um auf die Eigenschaften eines Audioadapters zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="6dd78-123">A specialized audio application might need to use the IKsControl interface to access the properties of an audio adapter.</span></span>                                                                                     |
| [<span data-ttu-id="6dd78-124">Interoperabilität mit Legacy-Audio-APIs</span><span class="sxs-lookup"><span data-stu-id="6dd78-124">Interoperability with Legacy Audio APIs</span></span>](interoperability-with-legacy-audio-apis.md)                                     | <span data-ttu-id="6dd78-125">Wichtige Features der Kernaudio-APIs in Windows Vista können in vorhandene Anwendungen integriert werden, die DirectSound, DirectShow und die Windows-Multimediafunktionen **waveOutXxx** und **waveInXxx** verwenden.</span><span class="sxs-lookup"><span data-stu-id="6dd78-125">Key features of the core audio APIs in Windows Vista can be incorporated into existing applications that use DirectSound, DirectShow, and the Windows multimedia **waveOutXxx** and **waveInXxx** functions.</span></span> |
| [<span data-ttu-id="6dd78-126">Raumklang</span><span class="sxs-lookup"><span data-stu-id="6dd78-126">Spatial Sound</span></span>](spatial-sound.md)                                                                                         | <span data-ttu-id="6dd78-127">Enthält Anleitungen für die Verwendung von Windows Sonic, der Plattformlösung von Microsoft für die Unterstützung räumlicher Sound auf Xbox und Windows, die Audiohinweise sowohl umschließen als auch die Höhe (über oder unterhalb des Listeners) ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="6dd78-127">Provides guidance for using Windows Sonic, Microsoft’s platform-level solution for spatial sound support on Xbox and Windows, enabling both surround and elevation (above or below the listener) audio cues.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="6dd78-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6dd78-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6dd78-129">Kernaudio-APIs</span><span class="sxs-lookup"><span data-stu-id="6dd78-129">Core Audio APIs</span></span>](core-audio-apis-in-windows-vista.md)
</dt> </dl>

 

 



