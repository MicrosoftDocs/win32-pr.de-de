---
description: Die \_ Bit-Flag-Konstanten von phonehuokswitchmode beschreiben die Mikrofon-und Redner Komponenten eines "huokswitch"-Geräts.
ms.assetid: 532bf089-d5ca-4a04-847d-69e48990ff5c
title: PHONEHOOKSWITCHMODE_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8028cb531d5b38185edf75ae58e4c3c855398f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352178"
---
# <a name="phonehookswitchmode_-constants"></a><span data-ttu-id="a69e0-103">Phonehuokswitchmode- \_ Konstanten</span><span class="sxs-lookup"><span data-stu-id="a69e0-103">PHONEHOOKSWITCHMODE\_ Constants</span></span>

<span data-ttu-id="a69e0-104">Die Bit-Flag-Konstanten von **phonehuokswitchmode \_** beschreiben die Mikrofon-und Redner Komponenten eines "huokswitch"-Geräts.</span><span class="sxs-lookup"><span data-stu-id="a69e0-104">The **PHONEHOOKSWITCHMODE\_** bit-flag constants describe the microphone and speaker components of a hookswitch device.</span></span>

<dl> <dt>

<span data-ttu-id="a69e0-105"><span id="PHONEHOOKSWITCHMODE_MIC"></span><span id="phonehookswitchmode_mic"></span>**phonehuokswitchmode \_ MIC**</span><span class="sxs-lookup"><span data-stu-id="a69e0-105"><span id="PHONEHOOKSWITCHMODE_MIC"></span><span id="phonehookswitchmode_mic"></span>**PHONEHOOKSWITCHMODE\_MIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a69e0-106">Das Mikrofon des Geräts ist aktiv, der Redner ist stumm.</span><span class="sxs-lookup"><span data-stu-id="a69e0-106">The device's microphone is active, the speaker is mute.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a69e0-107"><span id="PHONEHOOKSWITCHMODE_MICSPEAKER"></span><span id="phonehookswitchmode_micspeaker"></span>**phonehuokswitchmode \_ micspeaker**</span><span class="sxs-lookup"><span data-stu-id="a69e0-107"><span id="PHONEHOOKSWITCHMODE_MICSPEAKER"></span><span id="phonehookswitchmode_micspeaker"></span>**PHONEHOOKSWITCHMODE\_MICSPEAKER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a69e0-108">Das Mikrofon und der Referent des Geräts sind aktiv.</span><span class="sxs-lookup"><span data-stu-id="a69e0-108">The device's microphone and speaker are both active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a69e0-109"><span id="PHONEHOOKSWITCHMODE_ONHOOK"></span><span id="phonehookswitchmode_onhook"></span>**phonehuokswitchmode- \_ OnHook**</span><span class="sxs-lookup"><span data-stu-id="a69e0-109"><span id="PHONEHOOKSWITCHMODE_ONHOOK"></span><span id="phonehookswitchmode_onhook"></span>**PHONEHOOKSWITCHMODE\_ONHOOK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a69e0-110">Das Mikrofon und der Referent des Geräts sind beide OnHook.</span><span class="sxs-lookup"><span data-stu-id="a69e0-110">The device's microphone and speaker are both onhook.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a69e0-111"><span id="PHONEHOOKSWITCHMODE_SPEAKER"></span><span id="phonehookswitchmode_speaker"></span>**phonehuokswitchmode- \_ Sprecher**</span><span class="sxs-lookup"><span data-stu-id="a69e0-111"><span id="PHONEHOOKSWITCHMODE_SPEAKER"></span><span id="phonehookswitchmode_speaker"></span>**PHONEHOOKSWITCHMODE\_SPEAKER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a69e0-112">Der Redner des Geräts ist aktiv, das Mikrofon ist stumm.</span><span class="sxs-lookup"><span data-stu-id="a69e0-112">The device's speaker is active, the microphone is mute.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a69e0-113"><span id="PHONEHOOKSWITCHMODE_UNKNOWN"></span><span id="phonehookswitchmode_unknown"></span>**phonehuokswitchmode \_ unbekannt**</span><span class="sxs-lookup"><span data-stu-id="a69e0-113"><span id="PHONEHOOKSWITCHMODE_UNKNOWN"></span><span id="phonehookswitchmode_unknown"></span>**PHONEHOOKSWITCHMODE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a69e0-114">Der Geräte Modus für den Gerätewechsel ist zurzeit unbekannt.</span><span class="sxs-lookup"><span data-stu-id="a69e0-114">The device's hookswitch mode is currently unknown.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a69e0-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a69e0-115">Remarks</span></span>

<span data-ttu-id="a69e0-116">Keine Erweiterbarkeit.</span><span class="sxs-lookup"><span data-stu-id="a69e0-116">No extensibility.</span></span> <span data-ttu-id="a69e0-117">Alle 32 Bits sind reserviert.</span><span class="sxs-lookup"><span data-stu-id="a69e0-117">All 32 bits are reserved.</span></span>

<span data-ttu-id="a69e0-118">Diese Konstanten werden verwendet, um eine individuelle Steuerungsebene für die Mikrofon-und Redner Komponenten eines Telefon Geräts bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="a69e0-118">These constants are used to provide an individual level of control over the microphone and speaker components of a phone device.</span></span>

## <a name="requirements"></a><span data-ttu-id="a69e0-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a69e0-119">Requirements</span></span>



| <span data-ttu-id="a69e0-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a69e0-120">Requirement</span></span> | <span data-ttu-id="a69e0-121">Wert</span><span class="sxs-lookup"><span data-stu-id="a69e0-121">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="a69e0-122">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="a69e0-122">TAPI version</span></span><br/> | <span data-ttu-id="a69e0-123">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="a69e0-123">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="a69e0-124">Header</span><span class="sxs-lookup"><span data-stu-id="a69e0-124">Header</span></span><br/>       | <dl> <span data-ttu-id="a69e0-125"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="a69e0-125"><dt>Tapi.h</dt></span></span> </dl> |



 

 




