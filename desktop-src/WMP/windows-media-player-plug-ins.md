---
title: Windows Media Player-Plug-ins
description: Windows Media Player-Plug-ins
ms.assetid: 6265084b-e1ff-455b-aca8-dc008d94ed43
keywords:
- Windows Media Player-Plug-ins
- Windows Media Player-Plug-ins, Informationen zu
- Plug-ins, Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d7d666874590f380e6f3828031b297d483ffff7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106341539"
---
# <a name="windows-media-player-plug-ins"></a><span data-ttu-id="bf967-106">Windows Media Player-Plug-ins</span><span class="sxs-lookup"><span data-stu-id="bf967-106">Windows Media Player Plug-ins</span></span>

<span data-ttu-id="bf967-107">Microsoft Windows Media Player macht Schnittstellen verfügbar, die es Ihnen ermöglichen, die Funktionalität auf verschiedene Weise zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="bf967-107">Microsoft Windows Media Player exposes interfaces that allow you to extend functionality in several ways.</span></span> <span data-ttu-id="bf967-108">In den folgenden Abschnitten werden die unterstützten Plug-in-Architekturen und der Prozess zum Aufbau eines Plug-Ins beschrieben:</span><span class="sxs-lookup"><span data-stu-id="bf967-108">The following sections describe the supported plug-in architectures and the process of building a plug-in:</span></span>



| <span data-ttu-id="bf967-109">`Section`</span><span class="sxs-lookup"><span data-stu-id="bf967-109">Section</span></span>                                                                                                         | <span data-ttu-id="bf967-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bf967-110">Description</span></span>                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bf967-111">Aufbauen eines Plug-ins</span><span class="sxs-lookup"><span data-stu-id="bf967-111">Building a Plug-in</span></span>](building-a-plug-in.md)                                                                    | <span data-ttu-id="bf967-112">Mithilfe von Visual Studio und dem Assistenten für Windows Media Player-Plug-Ins können Sie verschiedene Plug-in-Typen erstellen.</span><span class="sxs-lookup"><span data-stu-id="bf967-112">You can build several types of plug-ins by using Visual Studio and the Windows Media Player plug-in wizard.</span></span>                                                                                                                                                                                             |
| [<span data-ttu-id="bf967-113">Benutzerdefinierte Visualisierungen in Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="bf967-113">Windows Media Player Custom Visualizations</span></span>](windows-media-player-custom-visualizations.md)                    | <span data-ttu-id="bf967-114">Windows Media Player-Visualisierungen sind Component Object Model (com)-Objekte, die zum Anzeigen von visuellen Bildern verwendet werden, die mit dem Audioteil der Medienwiedergabe des Players synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="bf967-114">Windows Media Player visualizations are Component Object Model (COM) objects used to display visual imagery that is synchronized to the audio portion of the media playback of the player.</span></span> <span data-ttu-id="bf967-115">Benutzerdefinierte Visualisierungen können mit Microsoft Visual C++ erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="bf967-115">Custom visualizations can be created using Microsoft Visual C++.</span></span>                                             |
| [<span data-ttu-id="bf967-116">Plug-Ins für Windows Media Player-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="bf967-116">Windows Media Player User Interface Plug-ins</span></span>](windows-media-player-user-interface-plug-ins.md)                | <span data-ttu-id="bf967-117">Windows Media Player-Plug-Ins für die Benutzeroberfläche fügen dem Bereich " **jetzt Wiedergabe** " des vollmodusplayers neue Funktionen hinzu.</span><span class="sxs-lookup"><span data-stu-id="bf967-117">Windows Media Player user interface plug-ins add new functionality to the **Now Playing** pane of the full mode Player.</span></span> <span data-ttu-id="bf967-118">Sie können Plug-ins erstellen, die den Visualisierungs Bereich, ein separates Fenster, den Einstellungsbereich, den Metadatenbereich oder Background-Plug-Ins verwenden, die keine sichtbare Benutzeroberfläche verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="bf967-118">You can create plug-ins that use the visualization area, a separate window, the settings area, the metadata area, or background plug-ins that expose no visible user interface.</span></span> |
| [<span data-ttu-id="bf967-119">Windows Media Player DSP-Plug-ins</span><span class="sxs-lookup"><span data-stu-id="bf967-119">Windows Media Player DSP Plug-ins</span></span>](windows-media-player-dsp-plug-ins.md)                                      | <span data-ttu-id="bf967-120">Windows Media Player DSP-Plug-ins ändern oder verarbeiten Audiodaten und Videodaten, bevor Sie vom Player gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="bf967-120">Windows Media Player DSP plug-ins modify or process audio and video data before it is rendered by the Player.</span></span> <span data-ttu-id="bf967-121">DSP-Plug-ins sind DirectX Media Objects (DMO), die über COM-Schnittstellen eine Verbindung mit dem Player herstellen.</span><span class="sxs-lookup"><span data-stu-id="bf967-121">DSP plug-ins are DirectX Media Objects (DMO) that connect to the Player through COM interfaces.</span></span>                                                                                           |
| <span data-ttu-id="bf967-122">[Windows Media Player Rendering-Plug-ins (veraltet)](/previous-versions/windows/desktop/legacy/dd564683(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="bf967-122">[Windows Media Player Rendering Plug-ins (deprecated)](/previous-versions/windows/desktop/legacy/dd564683(v=vs.85))</span></span> | <span data-ttu-id="bf967-123">Windows Media Player Rendering-Plug-ins decodieren (falls erforderlich) und Rendern benutzerdefinierter Daten, die in einem Windows Media-formatstream enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="bf967-123">Windows Media Player rendering plug-ins decode (if necessary) and render custom data contained in a Windows Media format stream.</span></span> <span data-ttu-id="bf967-124">Rendering-Plug-ins sind DirectX Media Objects (DMO), die über COM-Schnittstellen eine Verbindung mit dem Player herstellen.</span><span class="sxs-lookup"><span data-stu-id="bf967-124">Rendering plug-ins are DirectX Media Objects (DMO) that connect to the Player through COM interfaces.</span></span>                                                                  |
| [<span data-ttu-id="bf967-125">Windows Media Player-Konvertierungs-Plug-ins</span><span class="sxs-lookup"><span data-stu-id="bf967-125">Windows Media Player Conversion Plug-ins</span></span>](windows-media-player-conversion-plug-ins.md)                        | <span data-ttu-id="bf967-126">Windows Media Player-Konvertierungs-Plug-ins konvertieren digitale Mediendateien, die mithilfe von nicht von Microsoft bereitgestellten Technologien erstellt wurden, in das Advanced Systems Format (ASF).</span><span class="sxs-lookup"><span data-stu-id="bf967-126">Windows Media Player conversion plug-ins convert digital media files that are created using technologies not provided by Microsoft, into Advanced Systems Format (ASF).</span></span>                                                                                                                                 |



 

## <a name="related-topics"></a><span data-ttu-id="bf967-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bf967-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf967-128">**Windows Media Player SDK**</span><span class="sxs-lookup"><span data-stu-id="bf967-128">**Windows Media Player SDK**</span></span>](windows-media-player-sdk.md)
</dt> </dl>

 

 