---
description: Kernaudiostrukturen
ms.assetid: 92585cd4-baa9-4f75-816e-b83f5badad37
title: Kernaudiostrukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 078f49ac7abce8fc2773549df26431b780550c1b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344341"
---
# <a name="core-audio-structures"></a><span data-ttu-id="4d685-103">Kernaudiostrukturen</span><span class="sxs-lookup"><span data-stu-id="4d685-103">Core Audio Structures</span></span>

<span data-ttu-id="4d685-104">In diesem Abschnitt werden die Strukturen beschrieben, die von den Kerncode-APIs in Windows Vista und höher verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4d685-104">This section describes the structures that are used by the Core Audio APIs in Windows Vista and later.</span></span>



| <span data-ttu-id="4d685-105">Struktur</span><span class="sxs-lookup"><span data-stu-id="4d685-105">Structure</span></span>                                                                     | <span data-ttu-id="4d685-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4d685-106">Description</span></span>                                                                                                                                                         |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4d685-107">**\_ \_ Benachrichtigungs Daten für audiovolume \_**</span><span class="sxs-lookup"><span data-stu-id="4d685-107">**AUDIO\_VOLUME\_NOTIFICATION\_DATA**</span></span>](/windows/desktop/api/Endpointvolume/ns-endpointvolume-audio_volume_notification_data)   | <span data-ttu-id="4d685-108">Beschreibt eine Änderung der Volumeebene oder des stumm Schaltung-Zustands eines audioendpunkt-Geräts.</span><span class="sxs-lookup"><span data-stu-id="4d685-108">Describes a change in the volume level or muting state of an audio endpoint device.</span></span>                                                                                 |
| [<span data-ttu-id="4d685-109">**DirectX \_ - \_ audioaktivierungs Parameter \_**</span><span class="sxs-lookup"><span data-stu-id="4d685-109">**DIRECTX\_AUDIO\_ACTIVATION\_PARAMS**</span></span>](/windows/win32/api/mmdeviceapi/ns-mmdeviceapi-directx_audio_activation_params) | <span data-ttu-id="4d685-110">Gibt die Initialisierungs Parameter für einen DirectSound-Stream an.</span><span class="sxs-lookup"><span data-stu-id="4d685-110">Specifies the initialization parameters for a DirectSound stream.</span></span>                                                                                                   |
| [<span data-ttu-id="4d685-111">**ksjack- \_ Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4d685-111">**KSJACK\_DESCRIPTION**</span></span>](/windows/win32/api/devicetopology/ns-devicetopology-ksjack_description)                             | <span data-ttu-id="4d685-112">Abgerufen durch " [**iksjackdescription:: getjackdescription**](/windows/desktop/api/Devicetopology/nf-devicetopology-iksjackdescription-getjackdescription);" Beschreibt einen audiowagen.</span><span class="sxs-lookup"><span data-stu-id="4d685-112">Retrieved through [**IKsJackDescription::GetJackDescription**](/windows/desktop/api/Devicetopology/nf-devicetopology-iksjackdescription-getjackdescription); describes an audio jack.</span></span>                                 |
| [<span data-ttu-id="4d685-113">**Ksjack \_ DESCRIPTION2**</span><span class="sxs-lookup"><span data-stu-id="4d685-113">**KSJACK\_DESCRIPTION2**</span></span>](/windows/desktop/api/Devicetopology/ns-devicetopology-ksjack_description2)<br/>                | <span data-ttu-id="4d685-114">Abgerufen über [**IKsJackDescription2:: GetJackDescription2**](/windows/desktop/api/Devicetopology/nf-devicetopology-iksjackdescription2-getjackdescription2); Beschreibt einen audiowagen.</span><span class="sxs-lookup"><span data-stu-id="4d685-114">Retrieved through [**IKsJackDescription2::GetJackDescription2**](/windows/desktop/api/Devicetopology/nf-devicetopology-iksjackdescription2-getjackdescription2); describes an audio jack.</span></span> <br/>                 |
| [<span data-ttu-id="4d685-115">**Informationen zu ksjack- \_ Senke \_**</span><span class="sxs-lookup"><span data-stu-id="4d685-115">**KSJACK\_SINK\_INFORMATION**</span></span>](/windows/desktop/api/Devicetopology/ns-devicetopology-ksjack_sink_information)<br/>       | <span data-ttu-id="4d685-116">Abgerufen durch " [**iksjacksink Information:: getjacksink Information**](/windows/desktop/api/Devicetopology/nf-devicetopology-iksjacksinkinformation-getjacksinkinformation);" Beschreibt eine AudioJack-Senke.</span><span class="sxs-lookup"><span data-stu-id="4d685-116">Retrieved through [**IKsJackSinkInformation::GetJackSinkInformation**](/windows/desktop/api/Devicetopology/nf-devicetopology-iksjacksinkinformation-getjacksinkinformation); describes an audio jack sink.</span></span><br/> |
| [<span data-ttu-id="4d685-117">**LUID**</span><span class="sxs-lookup"><span data-stu-id="4d685-117">**LUID**</span></span>](/windows/desktop/api/Devicetopology/ns-devicetopology-luid)<br/>                                               | <span data-ttu-id="4d685-118">Speichert den Videoport Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="4d685-118">Stores the video port identifier.</span></span><br/>                                                                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="4d685-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4d685-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d685-120">Programmierverzeichnis</span><span class="sxs-lookup"><span data-stu-id="4d685-120">Programming Reference</span></span>](programming-reference.md)
</dt> </dl>

 

 




