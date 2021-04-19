---
description: Die \_ Bitflag-Konstanten von linecallprivilege beschreiben die Arten von Zugriffsrechten oder Berechtigungen, die eine Anwendung mit einem callhandle möglicherweise auf den entsprechenden-Befehl hat.
ms.assetid: a58b7e9e-696e-4421-9b31-1ba8afe6e03b
title: LINECALLPRIVILEGE_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac2569ec255d2da3ad384292eb87afaa285f54b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371767"
---
# <a name="linecallprivilege_-constants"></a><span data-ttu-id="8c814-103">Linecallprivilege- \_ Konstanten</span><span class="sxs-lookup"><span data-stu-id="8c814-103">LINECALLPRIVILEGE\_ Constants</span></span>

<span data-ttu-id="8c814-104">Die Bitflag-Konstanten von **linecallprivilege \_** beschreiben die Arten von Zugriffsrechten oder Berechtigungen, die eine Anwendung mit einem callhandle möglicherweise auf den entsprechenden-Befehl hat.</span><span class="sxs-lookup"><span data-stu-id="8c814-104">The **LINECALLPRIVILEGE\_** bit-flag constants describe the kinds of access rights or privileges an application with a call handle may have to the corresponding call.</span></span>

<dl> <dt>

<span data-ttu-id="8c814-105"><span id="LINECALLPRIVILEGE_MONITOR"></span><span id="linecallprivilege_monitor"></span>**linecallprivilege- \_ Monitor**</span><span class="sxs-lookup"><span data-stu-id="8c814-105"><span id="LINECALLPRIVILEGE_MONITOR"></span><span id="linecallprivilege_monitor"></span>**LINECALLPRIVILEGE\_MONITOR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8c814-106">Die Anwendung verfügt über Monitor Berechtigungen für den-Befehl.</span><span class="sxs-lookup"><span data-stu-id="8c814-106">The application has monitor privileges to the call.</span></span> <span data-ttu-id="8c814-107">Diese Berechtigungen ermöglichen es der Anwendung, Zustandsänderungen sowie Abfrage Informationen und den Status des Aufrufes zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="8c814-107">These privileges allow the application to monitor state changes and query information and status about the call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8c814-108"><span id="LINECALLPRIVILEGE_NONE"></span><span id="linecallprivilege_none"></span>**linecallprivilege \_ None**</span><span class="sxs-lookup"><span data-stu-id="8c814-108"><span id="LINECALLPRIVILEGE_NONE"></span><span id="linecallprivilege_none"></span>**LINECALLPRIVILEGE\_NONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8c814-109">Die Anwendung besitzt keine Berechtigungen für den-Befehl.</span><span class="sxs-lookup"><span data-stu-id="8c814-109">The application has no privileges to the call.</span></span> <span data-ttu-id="8c814-110">Das Handle der Anwendung ist void und sollte nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8c814-110">The application's handle is void and should not be used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8c814-111"><span id="LINECALLPRIVILEGE_OWNER"></span><span id="linecallprivilege_owner"></span>**linecallprivilege- \_ Besitzer**</span><span class="sxs-lookup"><span data-stu-id="8c814-111"><span id="LINECALLPRIVILEGE_OWNER"></span><span id="linecallprivilege_owner"></span>**LINECALLPRIVILEGE\_OWNER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8c814-112">Die Anwendung verfügt über Besitzer Berechtigungen für den-Befehl.</span><span class="sxs-lookup"><span data-stu-id="8c814-112">The application has owner privileges to the call.</span></span> <span data-ttu-id="8c814-113">Mit diesen Berechtigungen kann die Anwendung den-Befehl so bearbeiten, dass Sie den Status des Aufrufes beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="8c814-113">These privileges allow the application to manipulate the call in ways that affect the state of the call.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8c814-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8c814-114">Remarks</span></span>

<span data-ttu-id="8c814-115">Keine Erweiterbarkeit.</span><span class="sxs-lookup"><span data-stu-id="8c814-115">No extensibility.</span></span> <span data-ttu-id="8c814-116">Alle 32 Bits sind reserviert.</span><span class="sxs-lookup"><span data-stu-id="8c814-116">All 32 bits are reserved.</span></span>

<span data-ttu-id="8c814-117">Wenn ein Aufruf handle zuerst für eine Anwendung bereitgestellt wird oder wenn die Aufruf Berechtigungen dieser Anwendung geändert werden, wird die [**Zeile \_ CallState**](line-callstate.md) -Nachricht an die Anwendung gesendet.</span><span class="sxs-lookup"><span data-stu-id="8c814-117">When a call handle is first provided to an application or whenever call privileges of that application are modified, the [**LINE\_CALLSTATE**](line-callstate.md) message is sent to the application.</span></span> <span data-ttu-id="8c814-118">Wenn eine Anwendung einen-Rückruf übergibt und die empfangende Anwendung nicht bereits über ein Handle mit Besitzer Berechtigungen verfügt, informiert diese Nachricht die Anwendung über die neuen Berechtigungen des Aufrufes.</span><span class="sxs-lookup"><span data-stu-id="8c814-118">When an application hands off a call, and if the receiving application does not already have a handle with owner privileges, then this message informs the application about its new privileges to the call.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c814-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8c814-119">Requirements</span></span>



| <span data-ttu-id="8c814-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8c814-120">Requirement</span></span> | <span data-ttu-id="8c814-121">Wert</span><span class="sxs-lookup"><span data-stu-id="8c814-121">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="8c814-122">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="8c814-122">TAPI version</span></span><br/> | <span data-ttu-id="8c814-123">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="8c814-123">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="8c814-124">Header</span><span class="sxs-lookup"><span data-stu-id="8c814-124">Header</span></span><br/>       | <dl> <span data-ttu-id="8c814-125"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c814-125"><dt>Tapi.h</dt></span></span> </dl> |



 

 




