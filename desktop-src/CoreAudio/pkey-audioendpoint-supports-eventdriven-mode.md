---
description: "\"Pkey \\_ audioendpoint\" \\_ unterstützt die \\_ Eigenschaft \"Eventgesteuerte \\_ Modus\". gibt an, ob der Endpunkt den ereignisgesteuerten Modus unterstützt."
ms.assetid: 9cffd9ae-710b-4d41-aa02-3ab1a065e544
title: PKEY_AudioEndpoint_Supports_EventDriven_Mode (mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2707de83721d546040ac878b337faea12f533bb6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958536"
---
# <a name="pkey_audioendpoint_supports_eventdriven_mode"></a><span data-ttu-id="fd8c8-103">Pkey \_ audioendpoint \_ unterstützt den \_ ereignisbasierten \_ Modus</span><span class="sxs-lookup"><span data-stu-id="fd8c8-103">PKEY\_AudioEndpoint\_Supports\_EventDriven\_Mode</span></span>

<span data-ttu-id="fd8c8-104">" **Pkey \_ audioendpoint" unterstützt die Eigenschaft " \_ \_ Eventgesteuerte \_ Modus** ". gibt an, ob der Endpunkt den ereignisgesteuerten Modus unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fd8c8-104">The **PKEY\_AudioEndpoint\_Supports\_EventDriven\_Mode** property indicates whether the endpoint supports the event-driven mode.</span></span>

<span data-ttu-id="fd8c8-105">Der **VT** -Member der **PROPVARIANT** -Struktur ist auf VT \_ UI4 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fd8c8-105">The **vt** member of the **PROPVARIANT** structure is set to VT\_UI4.</span></span>

<span data-ttu-id="fd8c8-106">Der **uintval** -Member der **PROPVARIANT** -Struktur ist ein **DWORD** , das angibt, ob der Endpunkt den ereignisgesteuerten Modus unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fd8c8-106">The **uintVal** member of the **PROPVARIANT** structure is a **DWORD** that indicates if the endpoint supports the event-driven mode.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd8c8-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fd8c8-107">Remarks</span></span>

<span data-ttu-id="fd8c8-108">Dieser Eigenschafts Wert wird von einem audiooem in einer INF-Datei aufgefüllt, um anzugeben, dass die Hdaudio-Hardware den ereignisbasierten Modus gemäß der WHQL-Anforderung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fd8c8-108">This property value is populated by an audio OEM in an .inf file to indicate that the HDAudio hardware supports event driven mode as per the WHQL requirement.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd8c8-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fd8c8-109">Requirements</span></span>



| <span data-ttu-id="fd8c8-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fd8c8-110">Requirement</span></span> | <span data-ttu-id="fd8c8-111">Wert</span><span class="sxs-lookup"><span data-stu-id="fd8c8-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd8c8-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fd8c8-112">Minimum supported client</span></span><br/> | <span data-ttu-id="fd8c8-113">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fd8c8-113">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="fd8c8-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fd8c8-114">Minimum supported server</span></span><br/> | <span data-ttu-id="fd8c8-115">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fd8c8-115">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fd8c8-116">Header</span><span class="sxs-lookup"><span data-stu-id="fd8c8-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd8c8-117"><dt>Mmdeviceapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd8c8-117"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd8c8-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fd8c8-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd8c8-119">**Eigenschaften des audioendpunkts**</span><span class="sxs-lookup"><span data-stu-id="fd8c8-119">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="fd8c8-120">Kernaudioeigenschaften</span><span class="sxs-lookup"><span data-stu-id="fd8c8-120">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> </dl>

 

 




