---
description: Die linecallhubtracking- \_ Bitflag-Konstanten beschreiben den Typ der bereitgestellten callhub-Nachverfolgung.
ms.assetid: ad3c8d2e-f074-4db0-bb72-fb2181cbf687
title: LINECALLHUBTRACKING_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bfae61e36551a7d186408c2c87e0727503540a5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357670"
---
# <a name="linecallhubtracking_-constants"></a><span data-ttu-id="ca36b-103">Linecallhubtracking- \_ Konstanten</span><span class="sxs-lookup"><span data-stu-id="ca36b-103">LINECALLHUBTRACKING\_ Constants</span></span>

<span data-ttu-id="ca36b-104">Die **linecallhubtracking \_** -Bitflag-Konstanten beschreiben den Typ der bereitgestellten callhub-Nachverfolgung.</span><span class="sxs-lookup"><span data-stu-id="ca36b-104">The **LINECALLHUBTRACKING\_** bit-flag constants describe the type of call hub tracking provided.</span></span>

<dl> <dt>

<span data-ttu-id="ca36b-105"><span id="LINECALLHUBTRACKING_ALLCALLS"></span><span id="linecallhubtracking_allcalls"></span>**linecallhubtracking \_ allcalls**</span><span class="sxs-lookup"><span data-stu-id="ca36b-105"><span id="LINECALLHUBTRACKING_ALLCALLS"></span><span id="linecallhubtracking_allcalls"></span>**LINECALLHUBTRACKING\_ALLCALLS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ca36b-106">Die callhub-Nachverfolgung wird auf der Rufebene bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="ca36b-106">Call hub tracking is provided at the call level.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ca36b-107"><span id="LINECALLHUBTRACKING_NONE"></span><span id="linecallhubtracking_none"></span>**linecallhubtracking \_ None**</span><span class="sxs-lookup"><span data-stu-id="ca36b-107"><span id="LINECALLHUBTRACKING_NONE"></span><span id="linecallhubtracking_none"></span>**LINECALLHUBTRACKING\_NONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ca36b-108">Es wird keine callhub-Nachverfolgung bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="ca36b-108">No call hub tracking is provided.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ca36b-109"><span id="LINECALLHUBTRACKING_PROVIDERLEVEL"></span><span id="linecallhubtracking_providerlevel"></span>**linecallhubtracking- \_ providerlevel**</span><span class="sxs-lookup"><span data-stu-id="ca36b-109"><span id="LINECALLHUBTRACKING_PROVIDERLEVEL"></span><span id="linecallhubtracking_providerlevel"></span>**LINECALLHUBTRACKING\_PROVIDERLEVEL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ca36b-110">Callhubs werden auf Dienstanbieter Ebene nachverfolgt.</span><span class="sxs-lookup"><span data-stu-id="ca36b-110">Call hubs are tracked at the service provider level.</span></span> <span data-ttu-id="ca36b-111">Aufrufe durch aufrufänderungen werden nicht gemeldet.</span><span class="sxs-lookup"><span data-stu-id="ca36b-111">Call by call changes are not reported.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ca36b-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ca36b-112">Remarks</span></span>

<span data-ttu-id="ca36b-113">Keine Erweiterbarkeit.</span><span class="sxs-lookup"><span data-stu-id="ca36b-113">No extensibility.</span></span> <span data-ttu-id="ca36b-114">Alle 32 Bits sind reserviert.</span><span class="sxs-lookup"><span data-stu-id="ca36b-114">All 32 bits are reserved.</span></span>

<span data-ttu-id="ca36b-115">Wenn in dieser Datenstruktur Änderungen auftreten, wird eine [**Zeile \_ CallInfo**](line-callinfo.md) -Meldung an die Anwendung gesendet.</span><span class="sxs-lookup"><span data-stu-id="ca36b-115">When changes occur in this data structure, a [**LINE\_CALLINFO**](line-callinfo.md) message is sent to the application.</span></span> <span data-ttu-id="ca36b-116">Die Parameter für diese Nachricht sind ein Handle für den-Befehl und ein Hinweis auf das geänderte Informationselement.</span><span class="sxs-lookup"><span data-stu-id="ca36b-116">The parameters to this message are a handle to the call and an indication of the information item that has changed.</span></span> <span data-ttu-id="ca36b-117">Die [**linecallhubtrackinginfo**](/windows/desktop/api/Tapi/ns-tapi-linecallhubtrackinginfo) -Datenstruktur gibt an, welcher Nachverfolgungstyp bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="ca36b-117">The [**LINECALLHUBTRACKINGINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallhubtrackinginfo) data structure indicates which tracking type is provided.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca36b-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ca36b-118">Requirements</span></span>



| <span data-ttu-id="ca36b-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ca36b-119">Requirement</span></span> | <span data-ttu-id="ca36b-120">Wert</span><span class="sxs-lookup"><span data-stu-id="ca36b-120">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="ca36b-121">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="ca36b-121">TAPI version</span></span><br/> | <span data-ttu-id="ca36b-122">Erfordert TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="ca36b-122">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="ca36b-123">Header</span><span class="sxs-lookup"><span data-stu-id="ca36b-123">Header</span></span><br/>       | <dl> <span data-ttu-id="ca36b-124"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca36b-124"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca36b-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ca36b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca36b-126">**\_liniencallinfo**</span><span class="sxs-lookup"><span data-stu-id="ca36b-126">**LINE\_CALLINFO**</span></span>](line-callinfo.md)
</dt> <dt>

[<span data-ttu-id="ca36b-127">**Linecallhubtrackinginfo**</span><span class="sxs-lookup"><span data-stu-id="ca36b-127">**LINECALLHUBTRACKINGINFO**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linecallhubtrackinginfo)
</dt> <dt>

[<span data-ttu-id="ca36b-128">**LINECALLINFO**</span><span class="sxs-lookup"><span data-stu-id="ca36b-128">**LINECALLINFO**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linecallinfo)
</dt> </dl>

 

 




