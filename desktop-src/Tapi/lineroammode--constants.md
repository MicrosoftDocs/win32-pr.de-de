---
description: Die \_ Bit-Flag-Konstanten von lineroammode beschreiben den roamingstatus eines Linien Geräts.
ms.assetid: af0eb263-8deb-44ab-8acb-00e4ff7930ab
title: LINEROAMMODE_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3e40c40291567e7800b53070f882bf1e0bdac93
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357632"
---
# <a name="lineroammode_-constants"></a><span data-ttu-id="4dc2a-103">Lineroammode- \_ Konstanten</span><span class="sxs-lookup"><span data-stu-id="4dc2a-103">LINEROAMMODE\_ Constants</span></span>

<span data-ttu-id="4dc2a-104">Die Bit-Flag-Konstanten von **lineroammode \_** beschreiben den roamingstatus eines Linien Geräts.</span><span class="sxs-lookup"><span data-stu-id="4dc2a-104">The **LINEROAMMODE\_** bit-flag constants describe the roaming status of a line device.</span></span>

<dl> <dt>

<span data-ttu-id="4dc2a-105"><span id="LINEROAMMODE_HOME"></span><span id="lineroammode_home"></span>**lineroammode- \_ Startseite**</span><span class="sxs-lookup"><span data-stu-id="4dc2a-105"><span id="LINEROAMMODE_HOME"></span><span id="lineroammode_home"></span>**LINEROAMMODE\_HOME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4dc2a-106">Die Linie ist mit dem Heimnetzwerk Knoten verbunden.</span><span class="sxs-lookup"><span data-stu-id="4dc2a-106">The line is connected to the home network node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4dc2a-107"><span id="LINEROAMMODE_ROAMA"></span><span id="lineroammode_roama"></span>**lineroammode \_ roama**</span><span class="sxs-lookup"><span data-stu-id="4dc2a-107"><span id="LINEROAMMODE_ROAMA"></span><span id="lineroammode_roama"></span>**LINEROAMMODE\_ROAMA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4dc2a-108">Die Zeile ist mit dem Roaming verbunden-ein Netzbetreiber und Anrufe werden entsprechend abgerechnet.</span><span class="sxs-lookup"><span data-stu-id="4dc2a-108">The line is connected to the Roam-A carrier and calls are charged accordingly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4dc2a-109"><span id="LINEROAMMODE_ROAMB"></span><span id="lineroammode_roamb"></span>**lineroammode \_ roamb**</span><span class="sxs-lookup"><span data-stu-id="4dc2a-109"><span id="LINEROAMMODE_ROAMB"></span><span id="lineroammode_roamb"></span>**LINEROAMMODE\_ROAMB**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4dc2a-110">Die Zeile ist mit dem Roaming-B-Netzbetreiber verbunden, und Anrufe werden entsprechend abgerechnet.</span><span class="sxs-lookup"><span data-stu-id="4dc2a-110">The line is connected to the Roam-B carrier and calls are charged accordingly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4dc2a-111"><span id="LINEROAMMODE_UNAVAIL"></span><span id="lineroammode_unavail"></span>**lineroammode-Debugmodus \_**</span><span class="sxs-lookup"><span data-stu-id="4dc2a-111"><span id="LINEROAMMODE_UNAVAIL"></span><span id="lineroammode_unavail"></span>**LINEROAMMODE\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4dc2a-112">Der Modus "Roaming" ist nicht verfügbar und wird nicht bekannt sein.</span><span class="sxs-lookup"><span data-stu-id="4dc2a-112">The roam mode is unavailable and will not be known.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4dc2a-113"><span id="LINEROAMMODE_UNKNOWN"></span><span id="lineroammode_unknown"></span>**lineroammode \_ unbekannt**</span><span class="sxs-lookup"><span data-stu-id="4dc2a-113"><span id="LINEROAMMODE_UNKNOWN"></span><span id="lineroammode_unknown"></span>**LINEROAMMODE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4dc2a-114">Der Modus "Roaming" ist zurzeit unbekannt, kann aber später bekannt werden.</span><span class="sxs-lookup"><span data-stu-id="4dc2a-114">The roam mode is currently unknown but may become known later.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4dc2a-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4dc2a-115">Remarks</span></span>

<span data-ttu-id="4dc2a-116">Keine Erweiterbarkeit.</span><span class="sxs-lookup"><span data-stu-id="4dc2a-116">No extensibility.</span></span> <span data-ttu-id="4dc2a-117">Alle 32 Bits sind reserviert.</span><span class="sxs-lookup"><span data-stu-id="4dc2a-117">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="4dc2a-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4dc2a-118">Requirements</span></span>



| <span data-ttu-id="4dc2a-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4dc2a-119">Requirement</span></span> | <span data-ttu-id="4dc2a-120">Wert</span><span class="sxs-lookup"><span data-stu-id="4dc2a-120">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="4dc2a-121">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="4dc2a-121">TAPI version</span></span><br/> | <span data-ttu-id="4dc2a-122">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="4dc2a-122">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="4dc2a-123">Header</span><span class="sxs-lookup"><span data-stu-id="4dc2a-123">Header</span></span><br/>       | <dl> <span data-ttu-id="4dc2a-124"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="4dc2a-124"><dt>Tapi.h</dt></span></span> </dl> |



 

 




