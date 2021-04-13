---
description: Kernaudioenumerationen
ms.assetid: 7d25be71-ffbe-4e8c-9a45-cdeb35d10292
title: Kernaudioenumerationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35c786e1e18f25374a942a4140b67f0992ca7281
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483918"
---
# <a name="core-audio-enumerations"></a><span data-ttu-id="51685-103">Kernaudioenumerationen</span><span class="sxs-lookup"><span data-stu-id="51685-103">Core Audio Enumerations</span></span>

<span data-ttu-id="51685-104">In diesem Abschnitt werden die-Enumerationen beschrieben, die von den Kerncode-APIs in Windows Vista und höher verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="51685-104">This section describes the enumerations that are used by the Core Audio APIs in Windows Vista and later.</span></span>



| <span data-ttu-id="51685-105">Enumeration</span><span class="sxs-lookup"><span data-stu-id="51685-105">Enumeration</span></span>                                                                   | <span data-ttu-id="51685-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="51685-106">Description</span></span>                                                                                        |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="51685-107">**\_audclnt- \_ bufferflags**</span><span class="sxs-lookup"><span data-stu-id="51685-107">**\_AUDCLNT\_BUFFERFLAGS**</span></span>](/windows/win32/api/audioclient/ne-audioclient-_audclnt_bufferflags)                        | <span data-ttu-id="51685-108">Statusflags für einen audioendpunktpuffer.</span><span class="sxs-lookup"><span data-stu-id="51685-108">Status flags for an audio endpoint buffer.</span></span>                                                         |
| [<span data-ttu-id="51685-109">**"audclnt \_ sharemode"**</span><span class="sxs-lookup"><span data-stu-id="51685-109">**AUDCLNT\_SHAREMODE**</span></span>](/windows/desktop/api/Audiosessiontypes/ne-audiosessiontypes-audclnt_sharemode)                               | <span data-ttu-id="51685-110">Der Freigabe Modus für einen Stream.</span><span class="sxs-lookup"><span data-stu-id="51685-110">The sharing mode for a stream.</span></span>                                                                     |
| [<span data-ttu-id="51685-111">**"audclnt \_ streamoptions"**</span><span class="sxs-lookup"><span data-stu-id="51685-111">**AUDCLNT\_STREAMOPTIONS**</span></span>](/windows/desktop/api/audioclient/ne-audioclient-audclnt_streamoptions)                       | <span data-ttu-id="51685-112">Definiert Werte, die die Merkmale eines Audiostreams beschreiben.</span><span class="sxs-lookup"><span data-stu-id="51685-112">Defines values that describe the characteristics of an audio stream.</span></span>                               |
| [<span data-ttu-id="51685-113">**\_ \_ audiostreamkategorie**</span><span class="sxs-lookup"><span data-stu-id="51685-113">**AUDIO\_STREAM\_CATEGORY**</span></span>](/windows/desktop/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category)                      | <span data-ttu-id="51685-114">Gibt die Kategorie eines Audiostreams an.</span><span class="sxs-lookup"><span data-stu-id="51685-114">Specifies the category of an audio stream.</span></span>                                                         |
| [<span data-ttu-id="51685-115">**Audiosessionstate**</span><span class="sxs-lookup"><span data-stu-id="51685-115">**AudioSessionState**</span></span>](/windows/desktop/api/Audiosessiontypes/ne-audiosessiontypes-audiosessionstate)                                | <span data-ttu-id="51685-116">Der Status einer Audiositzung.</span><span class="sxs-lookup"><span data-stu-id="51685-116">The state of an audio session.</span></span>                                                                     |
| [<span data-ttu-id="51685-117">**Connector Type**</span><span class="sxs-lookup"><span data-stu-id="51685-117">**ConnectorType**</span></span>](/windows/win32/api/devicetopology/ne-devicetopology-connectortype)                                        | <span data-ttu-id="51685-118">Der Verbindungstyp in einer Geräte Topologie.</span><span class="sxs-lookup"><span data-stu-id="51685-118">The type of connector in a device topology.</span></span>                                                        |
| [<span data-ttu-id="51685-119">**Datenfluss**</span><span class="sxs-lookup"><span data-stu-id="51685-119">**DataFlow**</span></span>](/windows/win32/api/devicetopology/ne-devicetopology-dataflow)                                                  | <span data-ttu-id="51685-120">Die Datenfluss Richtung eines Audiostreams.</span><span class="sxs-lookup"><span data-stu-id="51685-120">The data-flow direction of an audio stream.</span></span>                                                        |
| [<span data-ttu-id="51685-121">**Edataflow**</span><span class="sxs-lookup"><span data-stu-id="51685-121">**EDataFlow**</span></span>](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-edataflow)                                                | <span data-ttu-id="51685-122">Die Richtung, in der Audiodaten zwischen einem audioendpunktgerät und einer Client Anwendung fließen.</span><span class="sxs-lookup"><span data-stu-id="51685-122">The direction in which audio data flows between an audio endpoint device and a client application.</span></span> |
| [<span data-ttu-id="51685-123">**Endpointformfactor**</span><span class="sxs-lookup"><span data-stu-id="51685-123">**EndpointFormFactor**</span></span>](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-endpointformfactor)                              | <span data-ttu-id="51685-124">Die allgemeinen physischen Attribute eines audioendpunktgeräts.</span><span class="sxs-lookup"><span data-stu-id="51685-124">The general physical attributes of an audio endpoint device.</span></span>                                       |
| [<span data-ttu-id="51685-125">**Erole**</span><span class="sxs-lookup"><span data-stu-id="51685-125">**ERole**</span></span>](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole)                                                        | <span data-ttu-id="51685-126">Die Systemrolle eines audioendpunktgeräts.</span><span class="sxs-lookup"><span data-stu-id="51685-126">The system role of an audio endpoint device.</span></span>                                                       |
| [<span data-ttu-id="51685-127">**ksjack- \_ Senke \_ connectionType**</span><span class="sxs-lookup"><span data-stu-id="51685-127">**KSJACK\_SINK\_CONNECTIONTYPE**</span></span>](/windows/win32/api/devicetopology/ne-devicetopology-ksjack_sink_connectiontype)<br/> | <span data-ttu-id="51685-128">Der Verbindungstyp.</span><span class="sxs-lookup"><span data-stu-id="51685-128">The type of connection.</span></span><br/>                                                                 |
| [<span data-ttu-id="51685-129">**Paramettype**</span><span class="sxs-lookup"><span data-stu-id="51685-129">**PartType**</span></span>](/windows/win32/api/devicetopology/ne-devicetopology-parttype)                                                  | <span data-ttu-id="51685-130">Der Teiltyp eines Teils (Connector oder Untereinheit) in einer Geräte Topologie.</span><span class="sxs-lookup"><span data-stu-id="51685-130">The part type of a part (connector or subunit) in a device topology.</span></span>                               |



 

## <a name="related-topics"></a><span data-ttu-id="51685-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="51685-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="51685-132">Programmierverzeichnis</span><span class="sxs-lookup"><span data-stu-id="51685-132">Programming Reference</span></span>](programming-reference.md)
</dt> </dl>

 

 




