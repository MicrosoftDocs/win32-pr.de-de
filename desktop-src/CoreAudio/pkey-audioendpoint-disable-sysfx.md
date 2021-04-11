---
description: Die pkey \_ audioendpoint \_ - \_ Eigenschaft "sysfx deaktivieren" gibt an, ob System Effekte im freigegebenen modusstream aktiviert sind, der zum oder vom audioendpunktgerät fließt.
ms.assetid: 9e73e9b6-1864-49cb-adf8-233cc1f9bfe5
title: PKEY_AudioEndpoint_Disable_SysFx (mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61a5486222c1c22158c70864b2b9bb0c4c31b5e1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127309"
---
# <a name="pkey_audioendpoint_disable_sysfx"></a><span data-ttu-id="b22be-103">Pkey \_ audioendpoint \_ Deaktivieren von \_ sysfx</span><span class="sxs-lookup"><span data-stu-id="b22be-103">PKEY\_AudioEndpoint\_Disable\_SysFx</span></span>

<span data-ttu-id="b22be-104">Die **pkey \_ audioendpoint-Eigenschaft " \_ \_ sysfx deaktivieren** " gibt an, ob System Effekte im freigegebenen modusstream aktiviert sind, der zum oder vom audioendpunktgerät fließt.</span><span class="sxs-lookup"><span data-stu-id="b22be-104">The **PKEY\_AudioEndpoint\_Disable\_SysFx** property specifies whether system effects are enabled in the shared-mode stream that flows to or from the audio endpoint device.</span></span>

<span data-ttu-id="b22be-105">System Effekte werden als audioverarbeitungsobjekte (apos) implementiert, die in einen Audiostream eingefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="b22be-105">System effects are implemented as audio processing objects (APOs) that can be inserted into an audio stream.</span></span> <span data-ttu-id="b22be-106">APOS sind Softwaremodule, die audioverarbeitungsfunktionen wie z. b. volumesteuerung und Formatkonvertierung ausführen.</span><span class="sxs-lookup"><span data-stu-id="b22be-106">APOs are software modules that perform audio processing functions such as volume control and format conversion.</span></span> <span data-ttu-id="b22be-107">Durch das Deaktivieren der System Effekte für ein Endpunkt Gerät kann der zugehörige Stream die apos unverändert durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="b22be-107">Disabling the system effects for an endpoint device enables the associated stream to pass through the APOs unmodified.</span></span>

<span data-ttu-id="b22be-108">Weitere Informationen zu System Effekten in Windows Vista finden Sie in den Whitepapers mit dem Titel "benutzerdefinierte Audioeffekte in Windows Vista" und "wieder verwenden von Windows Vista-audiosystemeffekten" auf der Website " [audiogerätetechnologien für Windows](https://www.microsoft.com/whdc/device/audio/default.mspx) ".</span><span class="sxs-lookup"><span data-stu-id="b22be-108">For more information about system effects in Windows Vista, see the white papers titled "Custom Audio Effects in Windows Vista" and "Reusing Windows Vista Audio System Effects" at the [Audio Device Technologies for Windows](https://www.microsoft.com/whdc/device/audio/default.mspx) website.</span></span>

<span data-ttu-id="b22be-109">Diese Eigenschaft gilt nur für die lokalen Effekte und globalen Effekte, die von der INF-Datei installiert wurden, die den Audioadapter installiert hat, mit dem das Endpunkt Gerät verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="b22be-109">This property applies only to the local-effects and global-effects APOs that were installed by the .inf file that installed the audio adapter to which the endpoint device is connected.</span></span> <span data-ttu-id="b22be-110">Außerdem wirkt sich diese Eigenschaft nur auf das Ziel Endpunkt Gerät aus – Sie wirkt sich nicht auf die Auswirkungen auf die System Auswirkungen anderer Endpunkt Geräte aus, auch wenn Sie eine Verbindung mit dem gleichen Adapter herstellen.</span><span class="sxs-lookup"><span data-stu-id="b22be-110">In addition, this property affects only the target endpoint device—it has no effect on the system effects for any other endpoint devices, even if they connect to the same adapter.</span></span>

<span data-ttu-id="b22be-111">Der **VT** -Member der **PROPVARIANT** -Struktur ist auf **VT \_ UI4** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b22be-111">The **vt** member of the **PROPVARIANT** structure is set to **VT\_UI4**.</span></span>

<span data-ttu-id="b22be-112">Der **ulVal** -Member der **PROPVARIANT** -Struktur ist auf **EndPoint \_ sysfx \_ aktiviert** festgelegt, wenn System Effekte aktiviert sind, oder wenn der **Endpunkt \_ sysfx \_ deaktiviert** ist, wenn Sie deaktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="b22be-112">The **ulVal** member of the **PROPVARIANT** structure is set to **ENDPOINT\_SYSFX\_ENABLED** if system effects are enabled or to **ENDPOINT\_SYSFX\_DISABLED** if they are disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="b22be-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b22be-113">Requirements</span></span>



| <span data-ttu-id="b22be-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b22be-114">Requirement</span></span> | <span data-ttu-id="b22be-115">Wert</span><span class="sxs-lookup"><span data-stu-id="b22be-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b22be-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b22be-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b22be-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b22be-117">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b22be-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b22be-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b22be-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b22be-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b22be-120">Header</span><span class="sxs-lookup"><span data-stu-id="b22be-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b22be-121"><dt>Mmdeviceapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b22be-121"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b22be-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b22be-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b22be-123">**Eigenschaften des audioendpunkts**</span><span class="sxs-lookup"><span data-stu-id="b22be-123">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="b22be-124">Kernaudioeigenschaften</span><span class="sxs-lookup"><span data-stu-id="b22be-124">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> </dl>

 

 




