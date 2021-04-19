---
description: Die linecallselect \_ -Bitflag-Konstanten beschreiben, welche Aufrufe ausgewählt werden sollen.
ms.assetid: f19a41bc-403a-4d4b-ab85-240a73514ebb
title: LINECALLSELECT_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8330b4c4e4e14ac399595d10d4a208a3c67f5b2a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370336"
---
# <a name="linecallselect_-constants"></a><span data-ttu-id="c315c-103">Linecallselect- \_ Konstanten</span><span class="sxs-lookup"><span data-stu-id="c315c-103">LINECALLSELECT\_ Constants</span></span>

<span data-ttu-id="c315c-104">Die **linecallselect \_** -Bitflag-Konstanten beschreiben, welche Aufrufe ausgewählt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c315c-104">The **LINECALLSELECT\_** bit-flag constants describe which calls are to be selected.</span></span>

<dl> <dt>

<span data-ttu-id="c315c-105"><span id="LINECALLSELECT_ADDRESS"></span><span id="linecallselect_address"></span>**linecallselect- \_ Adresse**</span><span class="sxs-lookup"><span data-stu-id="c315c-105"><span id="LINECALLSELECT_ADDRESS"></span><span id="linecallselect_address"></span>**LINECALLSELECT\_ADDRESS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c315c-106">Wählt den-Befehl für die angegebene Adresse aus.</span><span class="sxs-lookup"><span data-stu-id="c315c-106">Selects call on the specified address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c315c-107"><span id="LINECALLSELECT_CALL"></span><span id="linecallselect_call"></span>**linecallselect \_ -Befehl**</span><span class="sxs-lookup"><span data-stu-id="c315c-107"><span id="LINECALLSELECT_CALL"></span><span id="linecallselect_call"></span>**LINECALLSELECT\_CALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c315c-108">Wählt Verwandte Aufrufe des angegebenen Aufrufs aus.</span><span class="sxs-lookup"><span data-stu-id="c315c-108">Selects related calls to the specified call.</span></span> <span data-ttu-id="c315c-109">Beispielsweise werden die Parteien in einer Konferenz aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="c315c-109">For example, the parties in a conference call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c315c-110"><span id="LINECALLSELECT_CALLID"></span><span id="linecallselect_callid"></span>**linecallselect- \_ kallid**</span><span class="sxs-lookup"><span data-stu-id="c315c-110"><span id="LINECALLSELECT_CALLID"></span><span id="linecallselect_callid"></span>**LINECALLSELECT\_CALLID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c315c-111">Wählt Verwandte Aufrufe der angegebenen Aufruf Kennung aus.</span><span class="sxs-lookup"><span data-stu-id="c315c-111">Selects related calls to the specified call identifier.</span></span> <span data-ttu-id="c315c-112">Dieses Flag ist nur für Anwendungen verfügbar, die eine TAPI-Version von 3,0 oder höher aushandeln.</span><span class="sxs-lookup"><span data-stu-id="c315c-112">This flag is exposed only to applications that negotiate a TAPI version of 3.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c315c-113"><span id="LINECALLSELECT_DEVICEID"></span><span id="linecallselect_deviceid"></span>**linecallselect-Geräte-ID \_**</span><span class="sxs-lookup"><span data-stu-id="c315c-113"><span id="LINECALLSELECT_DEVICEID"></span><span id="linecallselect_deviceid"></span>**LINECALLSELECT\_DEVICEID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c315c-114">Wählt Aufrufe für den angegebenen Geräte Bezeichner aus.</span><span class="sxs-lookup"><span data-stu-id="c315c-114">Selects calls on the specified device identifier.</span></span> <span data-ttu-id="c315c-115">Dieses Flag ist nur für Anwendungen verfügbar, die eine TAPI-Version von 2,1 oder höher aushandeln.</span><span class="sxs-lookup"><span data-stu-id="c315c-115">This flag is exposed only to applications that negotiate a TAPI version of 2.1 or higher.</span></span> <span data-ttu-id="c315c-116">Anwendungen sollten in Erwägung gezogen werden, die linecallselect- \_ Zeilen Konstante anstelle dieser zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="c315c-116">Applications should consider using the LINECALLSELECT\_LINE constant instead of this one.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c315c-117"><span id="LINECALLSELECT_LINE"></span><span id="linecallselect_line"></span>**linecallselect- \_ Zeile**</span><span class="sxs-lookup"><span data-stu-id="c315c-117"><span id="LINECALLSELECT_LINE"></span><span id="linecallselect_line"></span>**LINECALLSELECT\_LINE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c315c-118">Wählt Aufrufe auf dem angegebenen Zeilen Gerät aus.</span><span class="sxs-lookup"><span data-stu-id="c315c-118">Selects calls on the specified line device.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c315c-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c315c-119">Remarks</span></span>

<span data-ttu-id="c315c-120">Keine Erweiterbarkeit.</span><span class="sxs-lookup"><span data-stu-id="c315c-120">No extensibility.</span></span> <span data-ttu-id="c315c-121">Alle 32 Bits sind reserviert.</span><span class="sxs-lookup"><span data-stu-id="c315c-121">All 32 bits are reserved.</span></span>

<span data-ttu-id="c315c-122">Diese Konstante wird in [**linegetnewcalls**](/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls) verwendet, um eine Auswahl (Bereich) der angeforderten Aufrufe anzugeben.</span><span class="sxs-lookup"><span data-stu-id="c315c-122">This constant is used in [**lineGetNewCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls) and to specify a selection (scope) of the calls that are requested.</span></span>

## <a name="requirements"></a><span data-ttu-id="c315c-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c315c-123">Requirements</span></span>



| <span data-ttu-id="c315c-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c315c-124">Requirement</span></span> | <span data-ttu-id="c315c-125">Wert</span><span class="sxs-lookup"><span data-stu-id="c315c-125">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="c315c-126">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="c315c-126">TAPI version</span></span><br/> | <span data-ttu-id="c315c-127">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="c315c-127">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="c315c-128">Header</span><span class="sxs-lookup"><span data-stu-id="c315c-128">Header</span></span><br/>       | <dl> <span data-ttu-id="c315c-129"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="c315c-129"><dt>Tapi.h</dt></span></span> </dl> |



 

 




