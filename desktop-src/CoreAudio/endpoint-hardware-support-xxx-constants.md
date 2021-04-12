---
description: Die Endpunkt \_ Hardware \_ Unterstützung \_ xxx-Konstanten sind Hardwareunterstützungs-Flags für ein audioendpunktgerät.
ms.assetid: 54032f75-2287-4589-bda5-e005ee077c41
title: ENDPOINT_HARDWARE_SUPPORT_XXX Konstanten (mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ffb5b2255330b205519ce3065ccb5f7eebb6b65
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127665"
---
# <a name="endpoint_hardware_support_xxx-constants"></a><span data-ttu-id="e1b9c-103">Endpunkt \_ Hardware \_ Unterstützung \_ xxx-Konstanten</span><span class="sxs-lookup"><span data-stu-id="e1b9c-103">ENDPOINT\_HARDWARE\_SUPPORT\_XXX Constants</span></span>

<span data-ttu-id="e1b9c-104">Die Endpunkt \_ Hardware \_ Unterstützung \_ xxx-Konstanten sind Hardwareunterstützungs-Flags für ein audioendpunktgerät.</span><span class="sxs-lookup"><span data-stu-id="e1b9c-104">The ENDPOINT\_HARDWARE\_SUPPORT\_XXX constants are hardware support flags for an audio endpoint device.</span></span>



| <span data-ttu-id="e1b9c-105">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="e1b9c-105">Constant/value</span></span>                                                                                                                                                                                                                                                                           | <span data-ttu-id="e1b9c-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e1b9c-106">Description</span></span>                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------|
| <span id="ENDPOINT_HARDWARE_SUPPORT_VOLUME"></span><span id="endpoint_hardware_support_volume"></span><dl> <span data-ttu-id="e1b9c-107"><dt>**Endpunkt \_ Hardware \_ Support \_ Volume**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="e1b9c-107"><dt>**ENDPOINT\_HARDWARE\_SUPPORT\_VOLUME**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="e1b9c-108">Das audioendpunktgerät unterstützt ein Hardware Volume-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="e1b9c-108">The audio endpoint device supports a hardware volume control.</span></span><br/> |
| <span id="ENDPOINT_HARDWARE_SUPPORT_MUTE"></span><span id="endpoint_hardware_support_mute"></span><dl> <span data-ttu-id="e1b9c-109"><dt>**Endpunkt \_ Hardware \_ Unterstützung \_ stumm schalten**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="e1b9c-109"><dt>**ENDPOINT\_HARDWARE\_SUPPORT\_MUTE**</dt> <dt>0x00000002</dt></span></span> </dl>       | <span data-ttu-id="e1b9c-110">Das audioendpunktgerät unterstützt ein Hardware stumm Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="e1b9c-110">The audio endpoint device supports a hardware mute control.</span></span><br/>   |
| <span id="ENDPOINT_HARDWARE_SUPPORT_METER"></span><span id="endpoint_hardware_support_meter"></span><dl> <span data-ttu-id="e1b9c-111"><dt>**Endpunkt \_ Hardware \_ Support \_ Meter**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="e1b9c-111"><dt>**ENDPOINT\_HARDWARE\_SUPPORT\_METER**</dt> <dt>0x00000004</dt></span></span> </dl>    | <span data-ttu-id="e1b9c-112">Das audioendpunktgerät unterstützt einen Hardware Spitzen Zähler.</span><span class="sxs-lookup"><span data-stu-id="e1b9c-112">The audio endpoint device supports a hardware peak meter.</span></span><br/>     |



## <a name="remarks"></a><span data-ttu-id="e1b9c-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e1b9c-113">Remarks</span></span>

<span data-ttu-id="e1b9c-114">Die [**iaudioendpointvolume:: queryhardwaresupport**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-queryhardwaresupport) -Methode und die [**iaudiometerinformation:: queryhardwaresupport**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudiometerinformation-queryhardwaresupport) -Methode verwenden die Endpoint \_ Hardware- \_ Unterstützung \_ xxx-Konstanten.</span><span class="sxs-lookup"><span data-stu-id="e1b9c-114">The [**IAudioEndpointVolume::QueryHardwareSupport**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-queryhardwaresupport) and [**IAudioMeterInformation::QueryHardwareSupport**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudiometerinformation-queryhardwaresupport) methods use the ENDPOINT\_HARDWARE\_SUPPORT\_XXX constants.</span></span>

<span data-ttu-id="e1b9c-115">Eine Hardware Unterstützungs Maske gibt an, welche Funktionen ein audioendpunktgerät in der Hardware implementiert.</span><span class="sxs-lookup"><span data-stu-id="e1b9c-115">A hardware support mask indicates which functions an audio endpoint device implements in hardware.</span></span> <span data-ttu-id="e1b9c-116">Die Maske kann entweder 0 oder eine bitweise OR-Kombination von mindestens einem Endpunkt Hardware- \_ \_ Unterstützung \_ xxx-Konstanten sein.</span><span class="sxs-lookup"><span data-stu-id="e1b9c-116">The mask can be either 0 or the bitwise-OR combination of one or more ENDPOINT\_HARDWARE\_SUPPORT\_XXX constants.</span></span> <span data-ttu-id="e1b9c-117">Wenn ein Bit, das einer bestimmten Endpunkt \_ Hardware \_ Unterstützung xxx-Konstante entspricht \_ , in der Maske festgelegt ist, ist die Bedeutung, dass die durch diese Konstante dargestellte Funktion vom Gerät in der Hardware implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="e1b9c-117">If a bit that corresponds to a particular ENDPOINT\_HARDWARE\_SUPPORT\_XXX constant is set in the mask, then the meaning is that the function represented by that constant is implemented in hardware by the device.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1b9c-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e1b9c-118">Requirements</span></span>



| <span data-ttu-id="e1b9c-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e1b9c-119">Requirement</span></span> | <span data-ttu-id="e1b9c-120">Wert</span><span class="sxs-lookup"><span data-stu-id="e1b9c-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1b9c-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e1b9c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e1b9c-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e1b9c-122">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e1b9c-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e1b9c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e1b9c-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e1b9c-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e1b9c-125">Header</span><span class="sxs-lookup"><span data-stu-id="e1b9c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1b9c-126"><dt>Mmdeviceapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1b9c-126"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1b9c-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e1b9c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1b9c-128">Kernaudiokonstanten</span><span class="sxs-lookup"><span data-stu-id="e1b9c-128">Core Audio Constants</span></span>](core-audio-constants.md)
</dt> <dt>

[<span data-ttu-id="e1b9c-129">**Iaudioendpointvolume:: queryhardwaresupport**</span><span class="sxs-lookup"><span data-stu-id="e1b9c-129">**IAudioEndpointVolume::QueryHardwareSupport**</span></span>](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-queryhardwaresupport)
</dt> <dt>

[<span data-ttu-id="e1b9c-130">**Iaudiometerinformation:: queryhardwaresupport**</span><span class="sxs-lookup"><span data-stu-id="e1b9c-130">**IAudioMeterInformation::QueryHardwareSupport**</span></span>](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudiometerinformation-queryhardwaresupport)
</dt> </dl>

 

 




