---
description: Setzt den aktuellen Sicherheitskontext der Smartcard zurück.
ms.assetid: fcd55b65-a741-4244-8597-ec61cea3f4b7
title: 'Iscardverify:: resetsecuritystate-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardVerify.ResetSecurityState
api_type:
- COM
api_location: ''
ms.openlocfilehash: ba96d400258fb58957c8c263438160d6710806db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861979"
---
# <a name="iscardverifyresetsecuritystate-method"></a><span data-ttu-id="c8b43-103">Iscardverify:: resetsecuritystate-Methode</span><span class="sxs-lookup"><span data-stu-id="c8b43-103">ISCardVerify::ResetSecurityState method</span></span>

<span data-ttu-id="c8b43-104">\[Die **resetsecuritystate** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="c8b43-104">\[The **ResetSecurityState** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="c8b43-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c8b43-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="c8b43-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="c8b43-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="c8b43-107">Die **resetsecuritystate** -Methode setzt den aktuellen [*Sicherheitskontext*](../secgloss/s-gly.md) der [*Smartcard*](../secgloss/s-gly.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="c8b43-107">The **ResetSecurityState** method resets the current [*security context*](../secgloss/s-gly.md) of the [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c8b43-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c8b43-108">Syntax</span></span>


```C++
HRESULT ResetSecurityState();
```



## <a name="parameters"></a><span data-ttu-id="c8b43-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c8b43-109">Parameters</span></span>

<span data-ttu-id="c8b43-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="c8b43-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c8b43-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c8b43-111">Return value</span></span>

<span data-ttu-id="c8b43-112">Die-Methode gibt einen der folgenden möglichen Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="c8b43-112">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="c8b43-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="c8b43-113">Return code</span></span>                                                                                   | <span data-ttu-id="c8b43-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c8b43-114">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="c8b43-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c8b43-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="c8b43-116">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="c8b43-116">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="c8b43-117"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="c8b43-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="c8b43-118">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="c8b43-118">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="c8b43-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c8b43-119">Remarks</span></span>

<span data-ttu-id="c8b43-120">Um den [*Sicherheitskontext*](../secgloss/s-gly.md) wieder zu aktivieren, ohne die Einstellung zurückzusetzen, nennen Sie [**Unblock**](/previous-versions/windows/desktop/legacy/aa377269(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c8b43-120">To re-enable the [*security context*](../secgloss/s-gly.md) without resetting, call [**Unblock**](/previous-versions/windows/desktop/legacy/aa377269(v=vs.85)).</span></span>

<span data-ttu-id="c8b43-121">Eine Liste aller Methoden, die durch diese Schnittstelle definiert werden, finden Sie unter [**iscardverify**](iscardverify.md).</span><span class="sxs-lookup"><span data-stu-id="c8b43-121">For a list of all the methods defined by this interface, see [**ISCardVerify**](iscardverify.md).</span></span>

<span data-ttu-id="c8b43-122">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="c8b43-122">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="c8b43-123">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="c8b43-123">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c8b43-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c8b43-124">Requirements</span></span>



| <span data-ttu-id="c8b43-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c8b43-125">Requirement</span></span> | <span data-ttu-id="c8b43-126">Wert</span><span class="sxs-lookup"><span data-stu-id="c8b43-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c8b43-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c8b43-127">Minimum supported client</span></span><br/> | <span data-ttu-id="c8b43-128">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c8b43-128">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="c8b43-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c8b43-129">Minimum supported server</span></span><br/> | <span data-ttu-id="c8b43-130">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c8b43-130">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c8b43-131">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="c8b43-131">End of client support</span></span><br/>    | <span data-ttu-id="c8b43-132">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c8b43-132">Windows XP</span></span><br/>                                |
| <span data-ttu-id="c8b43-133">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="c8b43-133">End of server support</span></span><br/>    | <span data-ttu-id="c8b43-134">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c8b43-134">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="c8b43-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c8b43-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8b43-136">**Iscardverify**</span><span class="sxs-lookup"><span data-stu-id="c8b43-136">**ISCardVerify**</span></span>](iscardverify.md)
</dt> <dt>

<span data-ttu-id="c8b43-137">[**Blockierung**](/previous-versions/windows/desktop/legacy/aa377269(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c8b43-137">[**Unblock**](/previous-versions/windows/desktop/legacy/aa377269(v=vs.85))</span></span>
</dt> </dl>

 

 
