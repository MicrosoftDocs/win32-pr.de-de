---
description: Im Diagramm werden Daten gepuffert, oder die Pufferung der Daten wurde beendet.
ms.assetid: 39e8b151-0323-42b3-99f0-3dcd230925c8
title: EC_BUFFERING_DATA (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1395a10458abd7a29fdb65e7ab55fba62328d6d5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356493"
---
# <a name="ec_buffering_data"></a><span data-ttu-id="98ae9-103">EC- \_ Puffer \_ Daten</span><span class="sxs-lookup"><span data-stu-id="98ae9-103">EC\_BUFFERING\_DATA</span></span>

<span data-ttu-id="98ae9-104">Im Diagramm werden Daten gepuffert, oder die Pufferung der Daten wurde beendet.</span><span class="sxs-lookup"><span data-stu-id="98ae9-104">The graph is buffering data, or has stopped buffering data.</span></span>

## <a name="parameters"></a><span data-ttu-id="98ae9-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="98ae9-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98ae9-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="98ae9-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="98ae9-107">(**Bool**) **True** , wenn das Diagramm mit dem Puffer beginnt, oder **false** , wenn das Diagramm die Pufferung beendet hat.</span><span class="sxs-lookup"><span data-stu-id="98ae9-107">(**BOOL**) **TRUE** if the graph is starting to buffer, or **FALSE** if the graph has stopped buffering.</span></span>

</dd> <dt>

<span data-ttu-id="98ae9-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="98ae9-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="98ae9-109">Keinen.</span><span class="sxs-lookup"><span data-stu-id="98ae9-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="98ae9-110">Standardaktion</span><span class="sxs-lookup"><span data-stu-id="98ae9-110">Default Action</span></span>

<span data-ttu-id="98ae9-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="98ae9-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="98ae9-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="98ae9-112">Remarks</span></span>

<span data-ttu-id="98ae9-113">Ein Filter kann dieses Ereignis senden, wenn Daten aus einer externen Quelle gepuffert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="98ae9-113">A filter can send this event if it needs to buffer data from an external source.</span></span> <span data-ttu-id="98ae9-114">(Beispielsweise kann es sein, dass Daten aus einem Netzwerk geladen werden.) Die Anwendung kann dieses Ereignis verwenden, um die Benutzeroberfläche anzupassen.</span><span class="sxs-lookup"><span data-stu-id="98ae9-114">(For example, it might be loading data from a network.) The application can use this event to adjust its user interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="98ae9-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="98ae9-115">Requirements</span></span>



| <span data-ttu-id="98ae9-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="98ae9-116">Requirement</span></span> | <span data-ttu-id="98ae9-117">Wert</span><span class="sxs-lookup"><span data-stu-id="98ae9-117">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="98ae9-118">Header</span><span class="sxs-lookup"><span data-stu-id="98ae9-118">Header</span></span><br/> | <dl> <span data-ttu-id="98ae9-119"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="98ae9-119"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98ae9-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="98ae9-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98ae9-121">Ereignis Benachrichtigungs Codes</span><span class="sxs-lookup"><span data-stu-id="98ae9-121">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="98ae9-122">Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="98ae9-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




