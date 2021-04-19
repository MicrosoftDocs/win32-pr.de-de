---
description: Die linebusymode \_ -Bitflag-Konstanten beschreiben verschiedene ausgelastete Signale, die der Switch oder das Netzwerk generieren kann. Diese ausgelasteten Signale geben in der Regel an, dass eine andere Ressource, die für einen-Rückruf erforderlich ist, zurzeit verwendet wird.
ms.assetid: 4a3fa79f-7a7a-4f9b-9353-e6c5ca4fcb4e
title: LINEBUSYMODE_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c996ad4e6142cc8312983945ae4c716ee0b35ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372482"
---
# <a name="linebusymode_-constants"></a><span data-ttu-id="1b061-104">Linebusymode- \_ Konstanten</span><span class="sxs-lookup"><span data-stu-id="1b061-104">LINEBUSYMODE\_ Constants</span></span>

<span data-ttu-id="1b061-105">Die **linebusymode \_** -Bitflag-Konstanten beschreiben verschiedene ausgelastete Signale, die der Switch oder das Netzwerk generieren kann.</span><span class="sxs-lookup"><span data-stu-id="1b061-105">The **LINEBUSYMODE\_** bit-flag constants describe different busy signals that the switch or network can generate.</span></span> <span data-ttu-id="1b061-106">Diese ausgelasteten Signale geben in der Regel an, dass eine andere Ressource, die für einen-Rückruf erforderlich ist, zurzeit verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1b061-106">These busy signals typically indicate that a different resource that is required to make a call is currently in use.</span></span>

<dl> <dt>

<span data-ttu-id="1b061-107"><span id="LINEBUSYMODE_STATION"></span><span id="linebusymode_station"></span>**linebusymode- \_ Station**</span><span class="sxs-lookup"><span data-stu-id="1b061-107"><span id="LINEBUSYMODE_STATION"></span><span id="linebusymode_station"></span>**LINEBUSYMODE\_STATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="1b061-108">Das ausgelastete Signal gibt an, dass die Station der aufgerufenen Partei ausgelastet ist.</span><span class="sxs-lookup"><span data-stu-id="1b061-108">The busy signal indicates that the called party's station is busy.</span></span> <span data-ttu-id="1b061-109">Dies wird in der Regel mit einem *normalen* ausgelasteten Ton signalisiert.</span><span class="sxs-lookup"><span data-stu-id="1b061-109">This is usually signaled with a *normal* busy tone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b061-110"><span id="LINEBUSYMODE_TRUNK"></span><span id="linebusymode_trunk"></span>**linebusymode- \_ trunk**</span><span class="sxs-lookup"><span data-stu-id="1b061-110"><span id="LINEBUSYMODE_TRUNK"></span><span id="linebusymode_trunk"></span>**LINEBUSYMODE\_TRUNK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="1b061-111">Das ausgelastete Signal gibt an, dass ein trunk oder eine Verbindung ausgelastet ist.</span><span class="sxs-lookup"><span data-stu-id="1b061-111">The busy signal indicates that a trunk or circuit is busy.</span></span> <span data-ttu-id="1b061-112">Dies wird in der Regel mit einem *fast* ausgelasteten Ton signalisiert.</span><span class="sxs-lookup"><span data-stu-id="1b061-112">This is usually signaled with a *fast* busy tone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b061-113"><span id="LINEBUSYMODE_UNKNOWN"></span><span id="linebusymode_unknown"></span>**linebusymode \_ unbekannt**</span><span class="sxs-lookup"><span data-stu-id="1b061-113"><span id="LINEBUSYMODE_UNKNOWN"></span><span id="linebusymode_unknown"></span>**LINEBUSYMODE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="1b061-114">Der bestimmte Modus des ausgelasteten Signals ist zurzeit unbekannt, kann aber später bekannt werden.</span><span class="sxs-lookup"><span data-stu-id="1b061-114">The busy signal's specific mode is currently unknown but may become known later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b061-115"><span id="LINEBUSYMODE_UNAVAIL"></span><span id="linebusymode_unavail"></span>**der Offline Modus ist \_ nicht erreichbar.**</span><span class="sxs-lookup"><span data-stu-id="1b061-115"><span id="LINEBUSYMODE_UNAVAIL"></span><span id="linebusymode_unavail"></span>**LINEBUSYMODE\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="1b061-116">Der bestimmte Modus des ausgelasteten Signals ist nicht verfügbar und wird nicht bekannt werden.</span><span class="sxs-lookup"><span data-stu-id="1b061-116">The busy signal's specific mode is unavailable and will not become known.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1b061-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1b061-117">Remarks</span></span>

<span data-ttu-id="1b061-118">Die höherwertigen 16 Bits können für gerätespezifische Erweiterungen zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="1b061-118">The high-order 16 bits can be assigned for device-specific extensions.</span></span> <span data-ttu-id="1b061-119">Die nieder wertigen 16 Bits sind reserviert.</span><span class="sxs-lookup"><span data-stu-id="1b061-119">The low-order 16 bits are reserved.</span></span>

> [!Note]  
> <span data-ttu-id="1b061-120">Ausgelastete Signale können als Inband-Töne oder out-of-Band-Nachrichten gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="1b061-120">Busy signals can be sent as inband tones or out-of-band messages.</span></span> <span data-ttu-id="1b061-121">TAPI nimmt keine Annahmen über den spezifischen Signalisierungs Mechanismus vor.</span><span class="sxs-lookup"><span data-stu-id="1b061-121">TAPI makes no assumption about the specific signaling mechanism.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1b061-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1b061-122">Requirements</span></span>



| <span data-ttu-id="1b061-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1b061-123">Requirement</span></span> | <span data-ttu-id="1b061-124">Wert</span><span class="sxs-lookup"><span data-stu-id="1b061-124">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="1b061-125">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="1b061-125">TAPI version</span></span><br/> | <span data-ttu-id="1b061-126">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="1b061-126">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="1b061-127">Header</span><span class="sxs-lookup"><span data-stu-id="1b061-127">Header</span></span><br/>       | <dl> <span data-ttu-id="1b061-128"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b061-128"><dt>Tapi.h</dt></span></span> </dl> |



 

 




