---
description: Gibt die Anlage auf einer bestimmten Smartcard oder einem Leser frei, der von attachbyhandle bzw. attachbyifd zugeordnet wird.
ms.assetid: 601b35a6-9094-4786-b94c-5cd1283feef5
title: Iscardmanage::D Etach-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.Detach
api_type:
- COM
api_location: ''
ms.openlocfilehash: bc5a48f76a643447b3e3d836d61ad7a769c56ff6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130653"
---
# <a name="iscardmanagedetach-method"></a><span data-ttu-id="470f5-103">Iscardmanage::D Etach-Methode</span><span class="sxs-lookup"><span data-stu-id="470f5-103">ISCardManage::Detach method</span></span>

<span data-ttu-id="470f5-104">\[Die **Detach** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="470f5-104">\[The **Detach** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="470f5-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="470f5-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="470f5-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="470f5-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="470f5-107">Die **Detach** -Methode gibt die Anlage auf eine bestimmte [*Smartcard*](../secgloss/s-gly.md) oder einen [*Leser*](../secgloss/r-gly.md) frei, der von [**attachbyhandle**](iscardmanage-attachbyhandle.md) bzw. [**attachbyifd**](iscardmanage-attachbyifd.md) zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="470f5-107">The **Detach** method releases the attachment to a particular [*smart card*](../secgloss/s-gly.md) or [*reader*](../secgloss/r-gly.md) allocated by [**AttachByHandle**](iscardmanage-attachbyhandle.md) and [**AttachByIFD**](iscardmanage-attachbyifd.md) respectively.</span></span>

## <a name="syntax"></a><span data-ttu-id="470f5-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="470f5-108">Syntax</span></span>


```C++
HRESULT Detach();
```



## <a name="parameters"></a><span data-ttu-id="470f5-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="470f5-109">Parameters</span></span>

<span data-ttu-id="470f5-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="470f5-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="470f5-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="470f5-111">Return value</span></span>

<span data-ttu-id="470f5-112">Die-Methode gibt einen der folgenden möglichen Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="470f5-112">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="470f5-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="470f5-113">Return code</span></span>                                                                                   | <span data-ttu-id="470f5-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="470f5-114">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="470f5-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="470f5-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="470f5-116">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="470f5-116">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="470f5-117"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="470f5-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="470f5-118">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="470f5-118">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="470f5-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="470f5-119">Remarks</span></span>

<span data-ttu-id="470f5-120">So fügen Sie einen smartcardanrufe an [](iscardmanage-attachbyhandle.md) [](iscardmanage-attachbyifd.md)</span><span class="sxs-lookup"><span data-stu-id="470f5-120">To attach a smart card call [**AttachByHandle**](iscardmanage-attachbyhandle.md) or [**AttachByIFD**](iscardmanage-attachbyifd.md).</span></span>

<span data-ttu-id="470f5-121">Um erneut eine Verbindung mit der Smartcard herzustellen, ohne **Detach** und [**attachbyhandle**](iscardmanage-attachbyhandle.md)aufzurufen, rufen Sie [**Verbindung**](iscardmanage-reconnect.md)auf.</span><span class="sxs-lookup"><span data-stu-id="470f5-121">To reconnect with the smart card without calling **Detach** and [**AttachByHandle**](iscardmanage-attachbyhandle.md), call [**Reconnect**](iscardmanage-reconnect.md).</span></span>

<span data-ttu-id="470f5-122">Eine Liste aller Methoden, die durch diese Schnittstelle definiert werden, finden Sie unter [**iscardmanage**](iscardmanage.md).</span><span class="sxs-lookup"><span data-stu-id="470f5-122">For a list of all the methods defined by this interface, see [**ISCardManage**](iscardmanage.md).</span></span>

<span data-ttu-id="470f5-123">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="470f5-123">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="470f5-124">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="470f5-124">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="470f5-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="470f5-125">Requirements</span></span>



| <span data-ttu-id="470f5-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="470f5-126">Requirement</span></span> | <span data-ttu-id="470f5-127">Wert</span><span class="sxs-lookup"><span data-stu-id="470f5-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="470f5-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="470f5-128">Minimum supported client</span></span><br/> | <span data-ttu-id="470f5-129">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="470f5-129">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="470f5-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="470f5-130">Minimum supported server</span></span><br/> | <span data-ttu-id="470f5-131">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="470f5-131">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="470f5-132">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="470f5-132">End of client support</span></span><br/>    | <span data-ttu-id="470f5-133">Windows XP</span><span class="sxs-lookup"><span data-stu-id="470f5-133">Windows XP</span></span><br/>                                |
| <span data-ttu-id="470f5-134">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="470f5-134">End of server support</span></span><br/>    | <span data-ttu-id="470f5-135">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="470f5-135">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="470f5-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="470f5-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="470f5-137">**Attachbyhandle**</span><span class="sxs-lookup"><span data-stu-id="470f5-137">**AttachByHandle**</span></span>](iscardmanage-attachbyhandle.md)
</dt> <dt>

[<span data-ttu-id="470f5-138">**Attachbyifd**</span><span class="sxs-lookup"><span data-stu-id="470f5-138">**AttachByIFD**</span></span>](iscardmanage-attachbyifd.md)
</dt> <dt>

[<span data-ttu-id="470f5-139">**Iscardmanage**</span><span class="sxs-lookup"><span data-stu-id="470f5-139">**ISCardManage**</span></span>](iscardmanage.md)
</dt> <dt>

[<span data-ttu-id="470f5-140">**Verbindung wiederherstellen**</span><span class="sxs-lookup"><span data-stu-id="470f5-140">**Reconnect**</span></span>](iscardmanage-reconnect.md)
</dt> </dl>

 

 
