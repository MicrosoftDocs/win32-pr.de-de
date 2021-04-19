---
description: Die TAPI-zeilige \_ callhubclose-Nachricht wird gesendet, wenn ein callhub geschlossen wurde.
ms.assetid: 738dcb20-99b5-44fe-8ad9-b14b8d977f53
title: LINE_CALLHUBCLOSE Meldung (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b538d6f154f3dacb2d779b6233722df16cc635d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352987"
---
# <a name="line_callhubclose-message"></a><span data-ttu-id="6d639-103">Zeile \_ callhubclose-Meldung</span><span class="sxs-lookup"><span data-stu-id="6d639-103">LINE\_CALLHUBCLOSE message</span></span>

<span data-ttu-id="6d639-104">Die TAPI- **zeilige \_ callhubclose** -Nachricht wird gesendet, wenn ein callhub geschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="6d639-104">The TAPI **LINE\_CALLHUBCLOSE** message is sent when a call hub has been closed.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="6d639-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="6d639-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d639-106">*hdevice*</span><span class="sxs-lookup"><span data-stu-id="6d639-106">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="6d639-107">Ein Handle für den-Befehl.</span><span class="sxs-lookup"><span data-stu-id="6d639-107">A handle to the call.</span></span>

</dd> <dt>

<span data-ttu-id="6d639-108">*dwcallbackinstance*</span><span class="sxs-lookup"><span data-stu-id="6d639-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="6d639-109">Die beim Öffnen der Zeile des Aufrufs angegebene Rückruf Instanz.</span><span class="sxs-lookup"><span data-stu-id="6d639-109">The callback instance supplied when opening the call's line.</span></span>

</dd> <dt>

<span data-ttu-id="6d639-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="6d639-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="6d639-111">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="6d639-111">Reserved.</span></span> <span data-ttu-id="6d639-112">Auf 0 festlegen.</span><span class="sxs-lookup"><span data-stu-id="6d639-112">Set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="6d639-113">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="6d639-113">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="6d639-114">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="6d639-114">Reserved.</span></span> <span data-ttu-id="6d639-115">Auf 0 festlegen.</span><span class="sxs-lookup"><span data-stu-id="6d639-115">Set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="6d639-116">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="6d639-116">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="6d639-117">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="6d639-117">Reserved.</span></span> <span data-ttu-id="6d639-118">Auf 0 festlegen.</span><span class="sxs-lookup"><span data-stu-id="6d639-118">Set to 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d639-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6d639-119">Return value</span></span>

<span data-ttu-id="6d639-120">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="6d639-120">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d639-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6d639-121">Remarks</span></span>

<span data-ttu-id="6d639-122">Diese Nachricht stammt von TAPI anstelle eines Dienstanbieters, sodass keine entsprechende TSPI-Nachricht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="6d639-122">This message originates with TAPI rather than with a service provider, so there is no corresponding TSPI message.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d639-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6d639-123">Requirements</span></span>



| <span data-ttu-id="6d639-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6d639-124">Requirement</span></span> | <span data-ttu-id="6d639-125">Wert</span><span class="sxs-lookup"><span data-stu-id="6d639-125">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="6d639-126">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="6d639-126">TAPI version</span></span><br/> | <span data-ttu-id="6d639-127">Erfordert TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="6d639-127">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="6d639-128">Header</span><span class="sxs-lookup"><span data-stu-id="6d639-128">Header</span></span><br/>       | <dl> <span data-ttu-id="6d639-129"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d639-129"><dt>Tapi.h</dt></span></span> </dl> |



 

 




