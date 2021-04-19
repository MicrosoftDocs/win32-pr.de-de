---
description: Die Statusmeldung der TAPI-Zeile \_ wird gesendet, wenn sich der Status einer Adresse in einer Zeile ändert, die zurzeit von der Anwendung geöffnet ist. Die Anwendung kann linegetaddressstatus aufrufen, um den aktuellen Status der Adresse zu bestimmen.
ms.assetid: af211fa1-79f8-49ac-a1d8-b62981f50519
title: LINE_ADDRESSSTATE Meldung (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d85b42f6957487ff24706485bd09d1d47880fe9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359312"
---
# <a name="line_addressstate-message"></a><span data-ttu-id="5def3-104">Zeile \_ addressstate-Meldung</span><span class="sxs-lookup"><span data-stu-id="5def3-104">LINE\_ADDRESSSTATE message</span></span>

<span data-ttu-id="5def3-105">Die Statusmeldung der TAPI- **Zeile \_** wird gesendet, wenn sich der Status einer Adresse in einer Zeile ändert, die zurzeit von der Anwendung geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="5def3-105">The TAPI **LINE\_ADDRESSSTATE** message is sent when the status of an address changes on a line that is currently open by the application.</span></span> <span data-ttu-id="5def3-106">Die Anwendung kann [**linegetaddressstatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus) aufrufen, um den aktuellen Status der Adresse zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="5def3-106">The application can invoke [**lineGetAddressStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus) to determine the current status of the address.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="5def3-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="5def3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5def3-108">*hdevice*</span><span class="sxs-lookup"><span data-stu-id="5def3-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="5def3-109">Ein Handle für das liniengerät.</span><span class="sxs-lookup"><span data-stu-id="5def3-109">A handle to the line device.</span></span>

</dd> <dt>

<span data-ttu-id="5def3-110">*dwcallbackinstance*</span><span class="sxs-lookup"><span data-stu-id="5def3-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="5def3-111">Die beim Öffnen der Zeile angegebene Rückruf Instanz.</span><span class="sxs-lookup"><span data-stu-id="5def3-111">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="5def3-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="5def3-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="5def3-113">Der Adress Bezeichner der Adresse, die den Status geändert hat.</span><span class="sxs-lookup"><span data-stu-id="5def3-113">The address identifier of the address that changed status.</span></span>

</dd> <dt>

<span data-ttu-id="5def3-114">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="5def3-114">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="5def3-115">Der Adress Zustand, der geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="5def3-115">The address state that changed.</span></span> <span data-ttu-id="5def3-116">Kann eine oder mehrere der [**lineaddressstate- \_ Konstanten**](lineaddressstate--constants.md)sein.</span><span class="sxs-lookup"><span data-stu-id="5def3-116">Can be one or more of the [**LINEADDRESSSTATE\_ constants**](lineaddressstate--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="5def3-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="5def3-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="5def3-118">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="5def3-118">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5def3-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5def3-119">Return value</span></span>

<span data-ttu-id="5def3-120">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="5def3-120">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5def3-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5def3-121">Remarks</span></span>

<span data-ttu-id="5def3-122">Die **Zeile \_ addressstate** wird an jede Anwendung gesendet, die das Zeilen Gerät geöffnet hat und die diese Meldung aktiviert hat.</span><span class="sxs-lookup"><span data-stu-id="5def3-122">The **LINE\_ADDRESSSTATE** message is sent to any application that has opened the line device and that has enabled this message.</span></span> <span data-ttu-id="5def3-123">Das Senden dieser Nachricht für die verschiedenen Status Elemente kann mithilfe von [**linegetstatusmessages**](/windows/desktop/api/Tapi/nf-tapi-linegetstatusmessages) und [**linesetstatusmessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages)gesteuert und abgefragt werden.</span><span class="sxs-lookup"><span data-stu-id="5def3-123">The sending of this message for the various status items can be controlled and queried using [**lineGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linegetstatusmessages) and [**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages).</span></span> <span data-ttu-id="5def3-124">Standardmäßig ist die Adress Status Berichterstattung deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="5def3-124">By default, address status reporting is disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="5def3-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5def3-125">Requirements</span></span>



| <span data-ttu-id="5def3-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5def3-126">Requirement</span></span> | <span data-ttu-id="5def3-127">Wert</span><span class="sxs-lookup"><span data-stu-id="5def3-127">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="5def3-128">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="5def3-128">TAPI version</span></span><br/> | <span data-ttu-id="5def3-129">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="5def3-129">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="5def3-130">Header</span><span class="sxs-lookup"><span data-stu-id="5def3-130">Header</span></span><br/>       | <dl> <span data-ttu-id="5def3-131"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="5def3-131"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5def3-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5def3-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5def3-133">**Lineaddresscaps**</span><span class="sxs-lookup"><span data-stu-id="5def3-133">**LINEADDRESSCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[<span data-ttu-id="5def3-134">**linegetaddresscaps**</span><span class="sxs-lookup"><span data-stu-id="5def3-134">**lineGetAddressCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)
</dt> <dt>

[<span data-ttu-id="5def3-135">**linegetaddressstatus**</span><span class="sxs-lookup"><span data-stu-id="5def3-135">**lineGetAddressStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus)
</dt> <dt>

[<span data-ttu-id="5def3-136">**linegetstatus Messages**</span><span class="sxs-lookup"><span data-stu-id="5def3-136">**lineGetStatusMessages**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetstatusmessages)
</dt> <dt>

[<span data-ttu-id="5def3-137">**linesetstatus-Meldungen**</span><span class="sxs-lookup"><span data-stu-id="5def3-137">**lineSetStatusMessages**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages)
</dt> </dl>

 

 




