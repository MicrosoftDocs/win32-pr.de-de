---
description: Ermöglicht es einer Anwendung, erneut eine Verbindung mit einer Smartcard oder einem Reader herzustellen, ohne einen Trenn Befehl, gefolgt von einem attachbyhandle-oder attachbyifd-Rückruf, ausgeben zu müssen.
ms.assetid: 450e817d-2cb2-4752-a86e-50cc8e434723
title: 'Iscardmanage:: Reconnect-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.Reconnect
api_type:
- COM
api_location: ''
ms.openlocfilehash: b8b05e6292a92267569eb1f53e10f6143554aba1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864047"
---
# <a name="iscardmanagereconnect-method"></a><span data-ttu-id="27c54-103">Iscardmanage:: Reconnect-Methode</span><span class="sxs-lookup"><span data-stu-id="27c54-103">ISCardManage::Reconnect method</span></span>

<span data-ttu-id="27c54-104">\[Die Methode zum **erneuten Verbinden** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="27c54-104">\[The **Reconnect** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="27c54-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="27c54-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="27c54-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="27c54-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="27c54-107">Mit der Methode " **Verbindung Connect** " kann eine Anwendung erneut eine Verbindung mit einer [*Smartcard*](../secgloss/s-gly.md) oder einem [*Reader*](../secgloss/r-gly.md) herstellen, ohne einen [**Trenn**](iscardmanage-detach.md) Befehl, gefolgt von einem [**attachbyhandle**](iscardmanage-attachbyhandle.md) -oder [**attachbyifd-**](iscardmanage-attachbyifd.md) Rückruf, ausgeben zu müssen.</span><span class="sxs-lookup"><span data-stu-id="27c54-107">The **Reconnect** method allows an application to reconnect to a [*smart card*](../secgloss/s-gly.md) or [*reader*](../secgloss/r-gly.md) without having to issue a [**Detach**](iscardmanage-detach.md) call followed by an [**AttachByHandle**](iscardmanage-attachbyhandle.md) or [**AttachByIFD**](iscardmanage-attachbyifd.md) call respectively.</span></span>

## <a name="syntax"></a><span data-ttu-id="27c54-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="27c54-108">Syntax</span></span>


```C++
HRESULT Reconnect();
```



## <a name="parameters"></a><span data-ttu-id="27c54-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="27c54-109">Parameters</span></span>

<span data-ttu-id="27c54-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="27c54-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="27c54-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="27c54-111">Return value</span></span>

<span data-ttu-id="27c54-112">Die-Methode gibt einen der folgenden möglichen Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="27c54-112">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="27c54-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="27c54-113">Return code</span></span>                                                                                   | <span data-ttu-id="27c54-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="27c54-114">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="27c54-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="27c54-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="27c54-116">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="27c54-116">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="27c54-117"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="27c54-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="27c54-118">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="27c54-118">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="27c54-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="27c54-119">Remarks</span></span>

<span data-ttu-id="27c54-120">So fügen Sie einen smartcardanrufe an [](iscardmanage-attachbyhandle.md) [](iscardmanage-attachbyifd.md)</span><span class="sxs-lookup"><span data-stu-id="27c54-120">To attach a smart card call [**AttachByHandle**](iscardmanage-attachbyhandle.md) or [**AttachByIFD**](iscardmanage-attachbyifd.md).</span></span>

<span data-ttu-id="27c54-121">Um eine Smartcard zu trennen, wenden Sie [**trennen**](iscardmanage-detach.md)an.</span><span class="sxs-lookup"><span data-stu-id="27c54-121">To detach a smart card, call [**Detach**](iscardmanage-detach.md).</span></span>

<span data-ttu-id="27c54-122">Eine Liste aller Methoden, die durch diese Schnittstelle definiert werden, finden Sie unter [**iscardmanage**](iscardmanage.md).</span><span class="sxs-lookup"><span data-stu-id="27c54-122">For a list of all the methods defined by this interface, see [**ISCardManage**](iscardmanage.md).</span></span>

<span data-ttu-id="27c54-123">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="27c54-123">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="27c54-124">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="27c54-124">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="27c54-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="27c54-125">Requirements</span></span>



| <span data-ttu-id="27c54-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="27c54-126">Requirement</span></span> | <span data-ttu-id="27c54-127">Wert</span><span class="sxs-lookup"><span data-stu-id="27c54-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="27c54-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="27c54-128">Minimum supported client</span></span><br/> | <span data-ttu-id="27c54-129">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="27c54-129">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="27c54-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="27c54-130">Minimum supported server</span></span><br/> | <span data-ttu-id="27c54-131">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="27c54-131">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="27c54-132">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="27c54-132">End of client support</span></span><br/>    | <span data-ttu-id="27c54-133">Windows XP</span><span class="sxs-lookup"><span data-stu-id="27c54-133">Windows XP</span></span><br/>                                |
| <span data-ttu-id="27c54-134">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="27c54-134">End of server support</span></span><br/>    | <span data-ttu-id="27c54-135">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="27c54-135">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="27c54-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="27c54-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27c54-137">**Attachbyhandle**</span><span class="sxs-lookup"><span data-stu-id="27c54-137">**AttachByHandle**</span></span>](iscardmanage-attachbyhandle.md)
</dt> <dt>

[<span data-ttu-id="27c54-138">**Attachbyifd**</span><span class="sxs-lookup"><span data-stu-id="27c54-138">**AttachByIFD**</span></span>](iscardmanage-attachbyifd.md)
</dt> <dt>

[<span data-ttu-id="27c54-139">**Trennen**</span><span class="sxs-lookup"><span data-stu-id="27c54-139">**Detach**</span></span>](iscardmanage-detach.md)
</dt> <dt>

[<span data-ttu-id="27c54-140">**Iscardmanage**</span><span class="sxs-lookup"><span data-stu-id="27c54-140">**ISCardManage**</span></span>](iscardmanage.md)
</dt> </dl>

 

 
