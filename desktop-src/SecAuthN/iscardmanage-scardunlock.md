---
description: Gibt die exklusive Verwendung der verbundenen Smartcard frei.
ms.assetid: a236743a-1d12-44db-853d-f757f43a7e8f
title: 'Iscardmanage:: scardunlock-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.SCardUnlock
api_type:
- COM
api_location: ''
ms.openlocfilehash: 90c6b10d407992ae8147998d2d420989cc91e970
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215465"
---
# <a name="iscardmanagescardunlock-method"></a><span data-ttu-id="86b3b-103">Iscardmanage:: scardunlock-Methode</span><span class="sxs-lookup"><span data-stu-id="86b3b-103">ISCardManage::SCardUnlock method</span></span>

<span data-ttu-id="86b3b-104">\[Die Methode " **scardunlock** " ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="86b3b-104">\[The **SCardUnlock** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="86b3b-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="86b3b-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="86b3b-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="86b3b-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="86b3b-107">Die **scardunlock** -Methode gibt die exklusive Verwendung der verbundenen [*Smartcard*](../secgloss/s-gly.md)frei.</span><span class="sxs-lookup"><span data-stu-id="86b3b-107">The **SCardUnlock** method releases exclusive use of the connected [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="86b3b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="86b3b-108">Syntax</span></span>


```C++
HRESULT SCardUnlock(
  [in] SCARD_DISPOSITIONS Disposition
);
```



## <a name="parameters"></a><span data-ttu-id="86b3b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="86b3b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86b3b-110">*Disposition* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="86b3b-110">*Disposition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86b3b-111">Der Zustand, in dem die Smartcard bei der Freigabe der Sperre belassen werden soll.</span><span class="sxs-lookup"><span data-stu-id="86b3b-111">The state to leave the smart card in when the lock is released.</span></span>

<dl><span id="LEAVE"></span><span id="leave"></span><dt>

<span data-ttu-id="86b3b-112">**Lassen Sie**</span><span class="sxs-lookup"><span data-stu-id="86b3b-112">**LEAVE**</span></span>
</dt><span id="RESET"></span><span id="reset"></span><dt>

<span data-ttu-id="86b3b-113">**RESET**</span><span class="sxs-lookup"><span data-stu-id="86b3b-113">**RESET**</span></span>
</dt><span id="UNPOWER"></span><span id="unpower"></span><dt>

<span data-ttu-id="86b3b-114">**Nicht mehr**</span><span class="sxs-lookup"><span data-stu-id="86b3b-114">**UNPOWER**</span></span>
</dt><span id="EJECT"></span><span id="eject"></span><dt>

<span data-ttu-id="86b3b-115">**Auswerfen**</span><span class="sxs-lookup"><span data-stu-id="86b3b-115">**EJECT**</span></span>
</dt> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86b3b-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="86b3b-116">Return value</span></span>

<span data-ttu-id="86b3b-117">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="86b3b-117">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="86b3b-118">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="86b3b-118">Return code</span></span>                                                                                  | <span data-ttu-id="86b3b-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="86b3b-119">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="86b3b-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="86b3b-120"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="86b3b-121">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="86b3b-121">Operation completed successfully.</span></span><br/>         |
| <dl> <span data-ttu-id="86b3b-122"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="86b3b-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="86b3b-123">Der *Disposition* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="86b3b-123">The *Disposition* parameter is not valid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="86b3b-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="86b3b-124">Remarks</span></span>

<span data-ttu-id="86b3b-125">Um die verbundene Smartcard zu sperren, nennen Sie [**scardlock**](iscardmanage-scardlock.md).</span><span class="sxs-lookup"><span data-stu-id="86b3b-125">To lock the connected smart card, call [**SCardLock**](iscardmanage-scardlock.md).</span></span>

<span data-ttu-id="86b3b-126">Eine Liste aller Methoden, die durch diese Schnittstelle definiert werden, finden Sie unter [**iscardmanage**](iscardmanage.md).</span><span class="sxs-lookup"><span data-stu-id="86b3b-126">For a list of all the methods defined by this interface, see [**ISCardManage**](iscardmanage.md).</span></span>

<span data-ttu-id="86b3b-127">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="86b3b-127">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="86b3b-128">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="86b3b-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="86b3b-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="86b3b-129">Requirements</span></span>



| <span data-ttu-id="86b3b-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="86b3b-130">Requirement</span></span> | <span data-ttu-id="86b3b-131">Wert</span><span class="sxs-lookup"><span data-stu-id="86b3b-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="86b3b-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="86b3b-132">Minimum supported client</span></span><br/> | <span data-ttu-id="86b3b-133">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="86b3b-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="86b3b-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="86b3b-134">Minimum supported server</span></span><br/> | <span data-ttu-id="86b3b-135">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="86b3b-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="86b3b-136">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="86b3b-136">End of client support</span></span><br/>    | <span data-ttu-id="86b3b-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="86b3b-137">Windows XP</span></span><br/>                                |
| <span data-ttu-id="86b3b-138">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="86b3b-138">End of server support</span></span><br/>    | <span data-ttu-id="86b3b-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="86b3b-139">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="86b3b-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="86b3b-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86b3b-141">**Iscardmanage**</span><span class="sxs-lookup"><span data-stu-id="86b3b-141">**ISCardManage**</span></span>](iscardmanage.md)
</dt> <dt>

[<span data-ttu-id="86b3b-142">**Scardlock**</span><span class="sxs-lookup"><span data-stu-id="86b3b-142">**SCardLock**</span></span>](iscardmanage-scardlock.md)
</dt> </dl>

 

 
