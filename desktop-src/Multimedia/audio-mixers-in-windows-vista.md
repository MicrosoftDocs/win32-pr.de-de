---
title: Audiomixer in Windows Vista
description: Audiomixer in Windows Vista
ms.assetid: 541cb5f3-b5ca-436f-88dd-6ef8459c6157
keywords:
- Multimedia-Audiodaten, Windows Vista-Audiomixer
- Audiodaten, Windows Vista-Audiomixer
- Audiomixer, Windows Vista
- Mixer, Windows Vista
- Windows Vista-Audiomixer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0610e9f16e13c19a253fbd9f6fac5ef452fa68ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104561274"
---
# <a name="audio-mixers-in-windows-vista"></a><span data-ttu-id="c5a5b-108">Audiomixer in Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c5a5b-108">Audio Mixers in Windows Vista</span></span>

<span data-ttu-id="c5a5b-109">Ab Windows Vista werden einige Mixer-Steuerelemente in Software anstelle von Hardware implementiert.</span><span class="sxs-lookup"><span data-stu-id="c5a5b-109">Starting in Windows Vista, some mixer controls are implemented in software rather than hardware.</span></span> <span data-ttu-id="c5a5b-110">Beispielsweise werden die volumesteuerelemente mithilfe der Windows-audiositzungs-API (WASAPI) implementiert.</span><span class="sxs-lookup"><span data-stu-id="c5a5b-110">For example, the volume controls are implemented using the Windows audio session API (WASAPI).</span></span> <span data-ttu-id="c5a5b-111">Diese Steuerelemente wirken sich nicht direkt auf die Hardware Einstellungen aus.</span><span class="sxs-lookup"><span data-stu-id="c5a5b-111">These controls do not directly affect hardware settings.</span></span> <span data-ttu-id="c5a5b-112">Außerdem sind Sie einer prozessspezifischen Audiositzung zugeordnet, sodass sich die Änderungen auf die aufrufenden Anwendungen auswirken, sich aber nicht auf andere Anwendungen auswirken.</span><span class="sxs-lookup"><span data-stu-id="c5a5b-112">In addition, they are associated with a process-specific audio session, so changes affect the calling application but do not affect other applications.</span></span>

<span data-ttu-id="c5a5b-113">Jedes audioendpunktgerät verfügt über ein Standard-Mischungs Layout, das in Software implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="c5a5b-113">Each audio endpoint device has a standard mixer layout, implemented in software.</span></span>

-   <span data-ttu-id="c5a5b-114">Jeder audiorenderingendpunkt enthält eine Zielzeile, die Folgendes enthält:</span><span class="sxs-lookup"><span data-stu-id="c5a5b-114">Each audio rendering endpoint contains one destination line that contains the following:</span></span>
    -   <span data-ttu-id="c5a5b-115">Volumesteuerung</span><span class="sxs-lookup"><span data-stu-id="c5a5b-115">Volume control</span></span>
    -   <span data-ttu-id="c5a5b-116">Steuerelement stumm schalten</span><span class="sxs-lookup"><span data-stu-id="c5a5b-116">Mute control</span></span>
    -   <span data-ttu-id="c5a5b-117">Quellzeile: Waveform-Audioausgabe.</span><span class="sxs-lookup"><span data-stu-id="c5a5b-117">Source line: Waveform-audio output.</span></span>
    -   <span data-ttu-id="c5a5b-118">Quellzeile: AudioCD.</span><span class="sxs-lookup"><span data-stu-id="c5a5b-118">Source line: Audio CD.</span></span>
-   <span data-ttu-id="c5a5b-119">Jeder audioerfassungs-Endpunkt enthält eine Zielzeile, die Folgendes enthält:</span><span class="sxs-lookup"><span data-stu-id="c5a5b-119">Each audio capture endpoint contains one destination line that contains the following:</span></span>
    -   <span data-ttu-id="c5a5b-120">Volumesteuerung</span><span class="sxs-lookup"><span data-stu-id="c5a5b-120">Volume control</span></span>
    -   <span data-ttu-id="c5a5b-121">Steuerelement stumm schalten</span><span class="sxs-lookup"><span data-stu-id="c5a5b-121">Mute control</span></span>
    -   <span data-ttu-id="c5a5b-122">Quellzeile: Waveform-Audioeingabe.</span><span class="sxs-lookup"><span data-stu-id="c5a5b-122">Source line: Waveform-audio input.</span></span> <span data-ttu-id="c5a5b-123">Der Komponententyp ist abhängig vom Eingabegerät – z. b. einem Mikrofon.</span><span class="sxs-lookup"><span data-stu-id="c5a5b-123">The component type depends on the input device— for example, a microphone.</span></span>

<span data-ttu-id="c5a5b-124">Jede Quellzeile enthält ein volumensteuerelement und ein stumm Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="c5a5b-124">Each source line contains a volume control and a mute control.</span></span> <span data-ttu-id="c5a5b-125">Das folgende Diagramm zeigt die Komponenten der Rendering-Endpunkte und Aufzeichnungs Endpunkte.</span><span class="sxs-lookup"><span data-stu-id="c5a5b-125">The following diagram shows the components of render endpoints and capture endpoints.</span></span>

![standardmischlayouts](images/mixer1.gif)

<span data-ttu-id="c5a5b-127">Alle-Steuerelemente für einen Endpunkt manipulieren das gleiche zugrunde liegende Software Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="c5a5b-127">All of the controls for an endpoint manipulate the same underlying software control.</span></span> <span data-ttu-id="c5a5b-128">Wenn Sie die Einstellungen für ein Steuerelement ändern, erhalten Sie daher eine Benachrichtigung zum Ändern des Steuer Elements für die anderen Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="c5a5b-128">Therefore, if you change the settings on one control, you will receive a control change notification on the other controls.</span></span> <span data-ttu-id="c5a5b-129">(Siehe [**mm- \_ mixm- \_ Steuerelement \_ Änderung**](mm-mixm-control-change.md).)</span><span class="sxs-lookup"><span data-stu-id="c5a5b-129">(See [**MM\_MIXM\_CONTROL\_CHANGE**](mm-mixm-control-change.md).)</span></span>

<span data-ttu-id="c5a5b-130">Dieses Standardlayout wird für die Kompatibilität mit vorhandenen Anwendungen bereitgestellt, die die Audiomixer-Funktionen verwenden.</span><span class="sxs-lookup"><span data-stu-id="c5a5b-130">This standard layout is provided for compatibility with existing applications that use the audio mixer functions.</span></span> <span data-ttu-id="c5a5b-131">Neue Anwendungen sollten diese Funktionen nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="c5a5b-131">New applications should avoid using these functions.</span></span>

 

 




