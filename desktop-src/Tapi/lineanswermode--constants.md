---
description: Die Bit-Flag-Konstanten für den linebeantwortermodus \_ beschreiben, wie sich ein vorhandener aktiver-Befehl auf einem Zeilen Gerät durch das beantworten eines anderen Angebots Aufrufes in derselben Zeile auswirkt.
ms.assetid: 35f63d92-970f-4fb8-aba9-179fc7de70f4
title: LINEANSWERMODE_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 658d5b1265d28f8cb719719e4303fde97d3fff3e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358771"
---
# <a name="lineanswermode_-constants"></a><span data-ttu-id="7be6b-103">Linebeantwortungsmoduskonstanten \_</span><span class="sxs-lookup"><span data-stu-id="7be6b-103">LINEANSWERMODE\_ Constants</span></span>

<span data-ttu-id="7be6b-104">Die Bit-Flag-Konstanten für den **linebeantwortermodus \_** beschreiben, wie sich ein vorhandener aktiver-Befehl auf einem Zeilen Gerät durch das beantworten eines anderen *Angebots* Aufrufes in derselben Zeile auswirkt.</span><span class="sxs-lookup"><span data-stu-id="7be6b-104">The **LINEANSWERMODE\_** bit-flag constants describe how an existing active call on a line device is affected by answering another *offering* call on the same line.</span></span>

<dl> <dt>

<span data-ttu-id="7be6b-105"><span id="LINEANSWERMODE_DROP"></span><span id="lineanswermode_drop"></span>**Zeilen beantwortungsmodus- \_ Drop**</span><span class="sxs-lookup"><span data-stu-id="7be6b-105"><span id="LINEANSWERMODE_DROP"></span><span id="lineanswermode_drop"></span>**LINEANSWERMODE\_DROP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7be6b-106">Der derzeit aktive-Rückruf wird automatisch gelöscht.</span><span class="sxs-lookup"><span data-stu-id="7be6b-106">The currently active call will automatically be dropped.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7be6b-107"><span id="LINEANSWERMODE_HOLD"></span><span id="lineanswermode_hold"></span>**lineantwortmodus \_ halten**</span><span class="sxs-lookup"><span data-stu-id="7be6b-107"><span id="LINEANSWERMODE_HOLD"></span><span id="lineanswermode_hold"></span>**LINEANSWERMODE\_HOLD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7be6b-108">Der derzeit aktive Anruf wird automatisch angehalten.</span><span class="sxs-lookup"><span data-stu-id="7be6b-108">The currently active call will automatically be placed on hold.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7be6b-109"><span id="LINEANSWERMODE_NONE"></span><span id="lineanswermode_none"></span>**lineantwortmodus " \_ None"**</span><span class="sxs-lookup"><span data-stu-id="7be6b-109"><span id="LINEANSWERMODE_NONE"></span><span id="lineanswermode_none"></span>**LINEANSWERMODE\_NONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7be6b-110">Das beantworten eines weiteren Aufrufes in derselben Zeile hat keine Auswirkung auf den vorhandenen aktiven-Befehl in der Zeile.</span><span class="sxs-lookup"><span data-stu-id="7be6b-110">Answering another call on the same line has no effect on the existing active call on the line.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7be6b-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7be6b-111">Remarks</span></span>

<span data-ttu-id="7be6b-112">Keine Erweiterbarkeit.</span><span class="sxs-lookup"><span data-stu-id="7be6b-112">No extensibility.</span></span> <span data-ttu-id="7be6b-113">Alle 32 Bits sind reserviert.</span><span class="sxs-lookup"><span data-stu-id="7be6b-113">All 32 bits are reserved.</span></span>

<span data-ttu-id="7be6b-114">Wenn ein Aufruf erfolgt (wird angeboten), wenn ein anderer Aufruf bereits aktiv ist, wird der neue Aufruf durch Aufrufen von [**lineanswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer)mit verbunden.</span><span class="sxs-lookup"><span data-stu-id="7be6b-114">If a call comes in (is offered) at the time another call is already active, the new call is connected to by invoking [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer).</span></span> <span data-ttu-id="7be6b-115">Welche Auswirkung dies auf den vorhandenen aktiven-Rückruf hat, hängt von den Gerätefunktionen der Zeile ab.</span><span class="sxs-lookup"><span data-stu-id="7be6b-115">The effect this has on the existing active call depends on the line's device capabilities.</span></span> <span data-ttu-id="7be6b-116">Der erste Anruf ist möglicherweise nicht betroffen, er wird möglicherweise automatisch gelöscht, oder er wird automatisch angehalten.</span><span class="sxs-lookup"><span data-stu-id="7be6b-116">The first call may be unaffected, it may automatically be dropped, or it may automatically be placed on hold.</span></span>

## <a name="requirements"></a><span data-ttu-id="7be6b-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7be6b-117">Requirements</span></span>



| <span data-ttu-id="7be6b-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7be6b-118">Requirement</span></span> | <span data-ttu-id="7be6b-119">Wert</span><span class="sxs-lookup"><span data-stu-id="7be6b-119">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="7be6b-120">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="7be6b-120">TAPI version</span></span><br/> | <span data-ttu-id="7be6b-121">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="7be6b-121">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="7be6b-122">Header</span><span class="sxs-lookup"><span data-stu-id="7be6b-122">Header</span></span><br/>       | <dl> <span data-ttu-id="7be6b-123"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="7be6b-123"><dt>Tapi.h</dt></span></span> </dl> |



 

 




