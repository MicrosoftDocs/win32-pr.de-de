---
description: Die pkey \_ audioendpoint \_ controlpanelpageprovider-Eigenschaft gibt die CLSID des registrierten Anbieters der Geräteeigenschaften Erweiterung für das audioendpunktgerät an.
ms.assetid: 429a7572-b609-46fd-946e-ee34ddd6cc5e
title: PKEY_AudioEndpoint_ControlPanelPageProvider (mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 205ccdfba799652d9b09af21eefbedd3c3049533
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861152"
---
# <a name="pkey_audioendpoint_controlpanelpageprovider"></a><span data-ttu-id="751e3-103">Pkey \_ audioendpoint \_ controlpanelpageprovider</span><span class="sxs-lookup"><span data-stu-id="751e3-103">PKEY\_AudioEndpoint\_ControlPanelPageProvider</span></span>

<span data-ttu-id="751e3-104">Die **pkey \_ audioendpoint \_ controlpanelpageprovider** -Eigenschaft gibt die CLSID des registrierten Anbieters der Geräteeigenschaften Erweiterung für das audioendpunktgerät an.</span><span class="sxs-lookup"><span data-stu-id="751e3-104">The **PKEY\_AudioEndpoint\_ControlPanelPageProvider** property specifies the CLSID of the registered provider of the device-properties extension for the audio endpoint device.</span></span> <span data-ttu-id="751e3-105">Die Erweiterung stellt die Eigenschaften für den audioendpunkt bereit, die auf der Seite Geräteeigenschaften der Windows-Multimedia-Systemsteuerung angezeigt werden, Mmsys.cpl.</span><span class="sxs-lookup"><span data-stu-id="751e3-105">The extension supplies the audio endpoint properties that are displayed in the device-properties page of the Windows multimedia control panel, Mmsys.cpl.</span></span> <span data-ttu-id="751e3-106">Weitere Informationen zu Mmsys.cpl finden Sie in der Windows-DDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="751e3-106">For more information about Mmsys.cpl, see the Windows DDK documentation.</span></span>

<span data-ttu-id="751e3-107">Der **VT** -Member der **PROPVARIANT** -Struktur ist auf VT \_ LPWSTR festgelegt.</span><span class="sxs-lookup"><span data-stu-id="751e3-107">The **vt** member of the **PROPVARIANT** structure is set to VT\_LPWSTR.</span></span>

<span data-ttu-id="751e3-108">Der **pwszval** -Member der **PROPVARIANT** -Struktur verweist auf eine mit NULL endenden Zeichenfolge mit breit Zeichen, die eine GUID enthält, die den Anbieter der Steuerelement Bereichs Erweiterung identifiziert.</span><span class="sxs-lookup"><span data-stu-id="751e3-108">The **pwszVal** member of the **PROPVARIANT** structure points to a null-terminated, wide-character string that contains a GUID that identifies the provider of the control-panel extension.</span></span>

## <a name="requirements"></a><span data-ttu-id="751e3-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="751e3-109">Requirements</span></span>



| <span data-ttu-id="751e3-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="751e3-110">Requirement</span></span> | <span data-ttu-id="751e3-111">Wert</span><span class="sxs-lookup"><span data-stu-id="751e3-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="751e3-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="751e3-112">Minimum supported client</span></span><br/> | <span data-ttu-id="751e3-113">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="751e3-113">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="751e3-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="751e3-114">Minimum supported server</span></span><br/> | <span data-ttu-id="751e3-115">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="751e3-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="751e3-116">Header</span><span class="sxs-lookup"><span data-stu-id="751e3-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="751e3-117"><dt>Mmdeviceapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="751e3-117"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="751e3-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="751e3-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="751e3-119">**Eigenschaften des audioendpunkts**</span><span class="sxs-lookup"><span data-stu-id="751e3-119">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="751e3-120">Kernaudioeigenschaften</span><span class="sxs-lookup"><span data-stu-id="751e3-120">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> </dl>

 

 




