---
description: Die "phonehuokswitchdev" \_ -Bitflag-Konstanten beschreiben verschiedene e/a-Audiogeräte, die jeweils über einen eigenen, von einem computergesteuerten Port verfügen.
ms.assetid: b3272a75-87b0-4afc-b2e2-2d65e4b49300
title: PHONEHOOKSWITCHDEV_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14a6727bf8103c35402bebc048de4ed9286650be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106374041"
---
# <a name="phonehookswitchdev_-constants"></a><span data-ttu-id="79ec4-103">Phonehuokswitchdev- \_ Konstanten</span><span class="sxs-lookup"><span data-stu-id="79ec4-103">PHONEHOOKSWITCHDEV\_ Constants</span></span>

<span data-ttu-id="79ec4-104">Die " **phonehuokswitchdev \_** "-Bitflag-Konstanten beschreiben verschiedene e/a-Audiogeräte, die jeweils über einen eigenen, von einem computergesteuerten Port verfügen.</span><span class="sxs-lookup"><span data-stu-id="79ec4-104">The **PHONEHOOKSWITCHDEV\_** bit-flag constants describe various audio I/O devices each with its own hookswitch controllable from the computer.</span></span>

<dl> <dt>

<span data-ttu-id="79ec4-105"><span id="PHONEHOOKSWITCHDEV_HANDSET"></span><span id="phonehookswitchdev_handset"></span>**phonehuokswitchdev- \_ Mobiltelefon**</span><span class="sxs-lookup"><span data-stu-id="79ec4-105"><span id="PHONEHOOKSWITCHDEV_HANDSET"></span><span id="phonehookswitchdev_handset"></span>**PHONEHOOKSWITCHDEV\_HANDSET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="79ec4-106">Dabei handelt es sich um ein Standardmäßiges Ohr-und-Telefon Telefon.</span><span class="sxs-lookup"><span data-stu-id="79ec4-106">This is a standard ear- and mouthpiece phone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="79ec4-107"><span id="PHONEHOOKSWITCHDEV_HEADSET"></span><span id="phonehookswitchdev_headset"></span>**phonehuokswitchdev- \_ Headset**</span><span class="sxs-lookup"><span data-stu-id="79ec4-107"><span id="PHONEHOOKSWITCHDEV_HEADSET"></span><span id="phonehookswitchdev_headset"></span>**PHONEHOOKSWITCHDEV\_HEADSET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="79ec4-108">Dabei handelt es sich um ein mit dem Telefon Satz verbundenes Headset.</span><span class="sxs-lookup"><span data-stu-id="79ec4-108">This is a headset connected to the phone set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="79ec4-109"><span id="PHONEHOOKSWITCHDEV_SPEAKER"></span><span id="phonehookswitchdev_speaker"></span>**phonehuokswitchdev- \_ Sprecher**</span><span class="sxs-lookup"><span data-stu-id="79ec4-109"><span id="PHONEHOOKSWITCHDEV_SPEAKER"></span><span id="phonehookswitchdev_speaker"></span>**PHONEHOOKSWITCHDEV\_SPEAKER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="79ec4-110">Dabei handelt es sich um einen integrierten Lautsprecher und ein Mikrofon.</span><span class="sxs-lookup"><span data-stu-id="79ec4-110">This is a built-in loudspeaker and microphone.</span></span> <span data-ttu-id="79ec4-111">Dabei kann es sich auch um einen extern verbundenen Ergänzung-Sprecher mit dem Telefon Satz handeln.</span><span class="sxs-lookup"><span data-stu-id="79ec4-111">This could also be an externally connected adjunct speaker to the telephone set.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="79ec4-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="79ec4-112">Remarks</span></span>

<span data-ttu-id="79ec4-113">Keine Erweiterbarkeit.</span><span class="sxs-lookup"><span data-stu-id="79ec4-113">No extensibility.</span></span> <span data-ttu-id="79ec4-114">Alle 32 Bits sind reserviert.</span><span class="sxs-lookup"><span data-stu-id="79ec4-114">All 32 bits are reserved.</span></span>

<span data-ttu-id="79ec4-115">Diese Konstanten werden in der [**phonecaps**](/windows/desktop/api/Tapi/ns-tapi-phonecaps) -Datenstruktur verwendet, um die Gerätefunktionen von "hostingswitch" auf einem Telefongerät anzugeben.</span><span class="sxs-lookup"><span data-stu-id="79ec4-115">These constants are used in the [**PHONECAPS**](/windows/desktop/api/Tapi/ns-tapi-phonecaps) data structure to indicate the hookswitch device capabilities of a phone device.</span></span> <span data-ttu-id="79ec4-116">In der [**phonestatus**](/windows/desktop/api/Tapi/ns-tapi-phonestatus) -Struktur wird der Status der Geräte des Telefons für den Gerätewechsel gemeldet.</span><span class="sxs-lookup"><span data-stu-id="79ec4-116">The [**PHONESTATUS**](/windows/desktop/api/Tapi/ns-tapi-phonestatus) structure reports the state of the phone's hookswitch devices.</span></span> <span data-ttu-id="79ec4-117">Die Funktion " [**phonesethookswitch**](/windows/desktop/api/Tapi/nf-tapi-phonesethookswitch) " und " [**phonegethookswitch**](/windows/desktop/api/Tapi/nf-tapi-phonegethookswitch) " verwenden Sie als Parameter, um das e/a-Gerät des Telefons auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="79ec4-117">The function [**phoneSetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonesethookswitch) and [**phoneGetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonegethookswitch) use it as a parameter to select the phone's I/O device.</span></span>

## <a name="requirements"></a><span data-ttu-id="79ec4-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="79ec4-118">Requirements</span></span>



| <span data-ttu-id="79ec4-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="79ec4-119">Requirement</span></span> | <span data-ttu-id="79ec4-120">Wert</span><span class="sxs-lookup"><span data-stu-id="79ec4-120">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="79ec4-121">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="79ec4-121">TAPI version</span></span><br/> | <span data-ttu-id="79ec4-122">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="79ec4-122">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="79ec4-123">Header</span><span class="sxs-lookup"><span data-stu-id="79ec4-123">Header</span></span><br/>       | <dl> <span data-ttu-id="79ec4-124"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="79ec4-124"><dt>Tapi.h</dt></span></span> </dl> |



 

 




