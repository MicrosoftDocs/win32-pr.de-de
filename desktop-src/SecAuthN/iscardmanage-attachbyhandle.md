---
description: Erstellt mithilfe eines Handles, das von der Smartcard-Ressourcen-Manager zurückgegeben wird, einen Kommunikationslink zu einer Smartcard (ICC).
ms.assetid: dfd05dce-4416-4881-92ca-c85baccf3b86
title: 'Iscardmanage:: attachbyhandle-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.AttachByHandle
api_type:
- COM
api_location: ''
ms.openlocfilehash: 266b6a0d2a4027fe85f1f5539b970a44fc21bbee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866012"
---
# <a name="iscardmanageattachbyhandle-method"></a><span data-ttu-id="10119-103">Iscardmanage:: attachbyhandle-Methode</span><span class="sxs-lookup"><span data-stu-id="10119-103">ISCardManage::AttachByHandle method</span></span>

<span data-ttu-id="10119-104">\[Die **attachbyhandle** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="10119-104">\[The **AttachByHandle** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="10119-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="10119-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="10119-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="10119-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="10119-107">Die **attachbyhandle** -Methode erstellt mithilfe eines Handles, das von der Smartcard- [*Ressourcen-Manager*](../secgloss/r-gly.md)zurückgegeben wird, einen Kommunikationslink zu einer [*Smartcard*](../secgloss/s-gly.md) (ICC).</span><span class="sxs-lookup"><span data-stu-id="10119-107">The **AttachByHandle** method creates a communication link to a [*smart card*](../secgloss/s-gly.md) (ICC) using a handle returned by the smart card [*resource manager*](../secgloss/r-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="10119-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="10119-108">Syntax</span></span>


```C++
HRESULT AttachByHandle(
  [in] HSCARD hICC
);
```



## <a name="parameters"></a><span data-ttu-id="10119-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="10119-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10119-110">*hicc* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="10119-110">*hICC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10119-111">Ein Handle für eine Smartcard.</span><span class="sxs-lookup"><span data-stu-id="10119-111">A handle to a smart card.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10119-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="10119-112">Return value</span></span>

<span data-ttu-id="10119-113">Die-Methode gibt einen der folgenden möglichen Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="10119-113">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="10119-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="10119-114">Return code</span></span>                                                                                   | <span data-ttu-id="10119-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="10119-115">Description</span></span>                                   |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="10119-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="10119-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="10119-117">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="10119-117">Operation completed successfully.</span></span><br/>  |
| <dl> <span data-ttu-id="10119-118"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="10119-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="10119-119">Der *hicc* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="10119-119">The *hICC* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="10119-120"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="10119-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="10119-121">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="10119-121">Out of memory.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="10119-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="10119-122">Remarks</span></span>

<span data-ttu-id="10119-123">Zum Anfügen eines [*Reader*](../secgloss/r-gly.md) -Anfügens [**attachbyifd**](iscardmanage-attachbyifd.md).</span><span class="sxs-lookup"><span data-stu-id="10119-123">To attach a [*reader*](../secgloss/r-gly.md) call [**AttachByIFD**](iscardmanage-attachbyifd.md).</span></span>

<span data-ttu-id="10119-124">Zum Freigeben eines Anlage Aufrufs [**trennen**](iscardmanage-detach.md).</span><span class="sxs-lookup"><span data-stu-id="10119-124">To release an attachment call [**Detach**](iscardmanage-detach.md).</span></span>

<span data-ttu-id="10119-125">Um erneut eine Verbindung mit der Smartcard herzustellen, ohne [**Detach**](iscardmanage-detach.md) und **attachbyhandle** aufzurufen, rufen Sie [**Verbindung**](iscardmanage-reconnect.md)auf.</span><span class="sxs-lookup"><span data-stu-id="10119-125">To reconnect with the smart card without calling [**Detach**](iscardmanage-detach.md) and **AttachByHandle**, call [**Reconnect**](iscardmanage-reconnect.md).</span></span>

<span data-ttu-id="10119-126">Eine Liste aller Methoden, die von der [**iscardmanage**](iscardmanage.md) -Schnittstelle definiert werden, finden Sie unter [**iscardmanage**](iscardmanage.md).</span><span class="sxs-lookup"><span data-stu-id="10119-126">For a list of all the methods defined by the [**ISCardManage**](iscardmanage.md) interface, see [**ISCardManage**](iscardmanage.md).</span></span>

<span data-ttu-id="10119-127">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="10119-127">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="10119-128">Informationen zu smartcardfehlercodes finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="10119-128">For information about smart card error codes, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="10119-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="10119-129">Requirements</span></span>



| <span data-ttu-id="10119-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="10119-130">Requirement</span></span> | <span data-ttu-id="10119-131">Wert</span><span class="sxs-lookup"><span data-stu-id="10119-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="10119-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="10119-132">Minimum supported client</span></span><br/> | <span data-ttu-id="10119-133">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="10119-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="10119-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="10119-134">Minimum supported server</span></span><br/> | <span data-ttu-id="10119-135">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="10119-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="10119-136">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="10119-136">End of client support</span></span><br/>    | <span data-ttu-id="10119-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="10119-137">Windows XP</span></span><br/>                                |
| <span data-ttu-id="10119-138">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="10119-138">End of server support</span></span><br/>    | <span data-ttu-id="10119-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="10119-139">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="10119-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="10119-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10119-141">**Attachbyifd**</span><span class="sxs-lookup"><span data-stu-id="10119-141">**AttachByIFD**</span></span>](iscardmanage-attachbyifd.md)
</dt> <dt>

[<span data-ttu-id="10119-142">**Trennen**</span><span class="sxs-lookup"><span data-stu-id="10119-142">**Detach**</span></span>](iscardmanage-detach.md)
</dt> <dt>

[<span data-ttu-id="10119-143">**Iscardmanage**</span><span class="sxs-lookup"><span data-stu-id="10119-143">**ISCardManage**</span></span>](iscardmanage.md)
</dt> <dt>

[<span data-ttu-id="10119-144">**Verbindung wiederherstellen**</span><span class="sxs-lookup"><span data-stu-id="10119-144">**Reconnect**</span></span>](iscardmanage-reconnect.md)
</dt> </dl>

 

 
