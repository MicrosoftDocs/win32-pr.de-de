---
description: Sperrt eine verbundene Smartcard für die exklusive Verwendung.
ms.assetid: c39a7cfe-04b6-4298-927a-4280664cf769
title: 'Iscardmanage:: scardlock-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.SCardLock
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2198f512fde90d1c79173f5151fc4f759944500a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215467"
---
# <a name="iscardmanagescardlock-method"></a><span data-ttu-id="32b88-103">Iscardmanage:: scardlock-Methode</span><span class="sxs-lookup"><span data-stu-id="32b88-103">ISCardManage::SCardLock method</span></span>

<span data-ttu-id="32b88-104">\[Die **scardlock** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="32b88-104">\[The **SCardLock** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="32b88-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="32b88-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="32b88-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="32b88-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="32b88-107">Die **scardlock** -Methode sperrt eine verbundene [*Smartcard*](../secgloss/s-gly.md) für die exklusive Verwendung.</span><span class="sxs-lookup"><span data-stu-id="32b88-107">The **SCardLock** method locks a connected [*smart card*](../secgloss/s-gly.md) for exclusive use.</span></span>

## <a name="syntax"></a><span data-ttu-id="32b88-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="32b88-108">Syntax</span></span>


```C++
HRESULT SCardLock();
```



## <a name="parameters"></a><span data-ttu-id="32b88-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="32b88-109">Parameters</span></span>

<span data-ttu-id="32b88-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="32b88-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="32b88-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="32b88-111">Return value</span></span>

<span data-ttu-id="32b88-112">Die-Methode gibt einen der folgenden möglichen Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="32b88-112">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="32b88-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="32b88-113">Return code</span></span>                                                                            | <span data-ttu-id="32b88-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="32b88-114">Description</span></span>                                  |
|----------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="32b88-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="32b88-115"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="32b88-116">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="32b88-116">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="32b88-117"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="32b88-117"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="32b88-118">Der Vorgang konnte nicht beendet werden.</span><span class="sxs-lookup"><span data-stu-id="32b88-118">Operation failed to complete.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="32b88-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="32b88-119">Remarks</span></span>

<span data-ttu-id="32b88-120">Um die exklusive Verwendung der verbundenen Smartcard freizusetzen, nennen Sie [**scardunlock**](iscardmanage-scardunlock.md).</span><span class="sxs-lookup"><span data-stu-id="32b88-120">To releases exclusive use of the connected smart card, call [**SCardUnlock**](iscardmanage-scardunlock.md).</span></span>

<span data-ttu-id="32b88-121">Eine Liste aller Methoden, die durch diese Schnittstelle definiert werden, finden Sie unter [**iscardmanage**](iscardmanage.md).</span><span class="sxs-lookup"><span data-stu-id="32b88-121">For a list of all the methods defined by this interface, see [**ISCardManage**](iscardmanage.md).</span></span>

<span data-ttu-id="32b88-122">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="32b88-122">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="32b88-123">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="32b88-123">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="32b88-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="32b88-124">Requirements</span></span>



| <span data-ttu-id="32b88-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="32b88-125">Requirement</span></span> | <span data-ttu-id="32b88-126">Wert</span><span class="sxs-lookup"><span data-stu-id="32b88-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="32b88-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="32b88-127">Minimum supported client</span></span><br/> | <span data-ttu-id="32b88-128">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="32b88-128">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="32b88-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="32b88-129">Minimum supported server</span></span><br/> | <span data-ttu-id="32b88-130">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="32b88-130">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="32b88-131">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="32b88-131">End of client support</span></span><br/>    | <span data-ttu-id="32b88-132">Windows XP</span><span class="sxs-lookup"><span data-stu-id="32b88-132">Windows XP</span></span><br/>                                |
| <span data-ttu-id="32b88-133">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="32b88-133">End of server support</span></span><br/>    | <span data-ttu-id="32b88-134">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="32b88-134">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="32b88-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="32b88-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32b88-136">**Iscardmanage**</span><span class="sxs-lookup"><span data-stu-id="32b88-136">**ISCardManage**</span></span>](iscardmanage.md)
</dt> <dt>

[<span data-ttu-id="32b88-137">**Scardunlock**</span><span class="sxs-lookup"><span data-stu-id="32b88-137">**SCardUnlock**</span></span>](iscardmanage-scardunlock.md)
</dt> </dl>

 

 
