---
description: Erstellt eine Kommunikations Verknüpfung mit einem Reader unter Verwendung eines angegebenen anzeigen Amens für den Reader.
ms.assetid: 7916896b-c460-47b2-a1db-17d8fc9bdd2e
title: 'Iscardmanage:: attachbyifd-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.AttachByIFD
api_type:
- COM
api_location: ''
ms.openlocfilehash: ae0aaae2157331d5d1bae2814c563c89dc73c757
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349479"
---
# <a name="iscardmanageattachbyifd-method"></a><span data-ttu-id="c734d-103">Iscardmanage:: attachbyifd-Methode</span><span class="sxs-lookup"><span data-stu-id="c734d-103">ISCardManage::AttachByIFD method</span></span>

<span data-ttu-id="c734d-104">\[Die **attachbyifd-** Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="c734d-104">\[The **AttachByIFD** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="c734d-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c734d-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="c734d-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="c734d-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="c734d-107">Die **attachbyifd-** Methode erstellt eine Kommunikations Verknüpfung mit einem [*Reader*](../secgloss/r-gly.md)unter Verwendung eines angegebenen anzeigen Amens für den Reader.</span><span class="sxs-lookup"><span data-stu-id="c734d-107">The **AttachByIFD** method creates a communication link to a [*reader*](../secgloss/r-gly.md), using a supplied display name for the reader.</span></span>

## <a name="syntax"></a><span data-ttu-id="c734d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c734d-108">Syntax</span></span>


```C++
HRESULT AttachByIFD(
  [in] BSTR bstrIFDName
);
```



## <a name="parameters"></a><span data-ttu-id="c734d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c734d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c734d-110">*bstrif-Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c734d-110">*bstrIFDName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c734d-111">Der Anzeige Name des Readers.</span><span class="sxs-lookup"><span data-stu-id="c734d-111">The display name of the reader.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c734d-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c734d-112">Return value</span></span>

<span data-ttu-id="c734d-113">Die-Methode gibt einen der folgenden möglichen Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="c734d-113">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="c734d-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="c734d-114">Return code</span></span>                                                                                   | <span data-ttu-id="c734d-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c734d-115">Description</span></span>                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="c734d-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c734d-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="c734d-117">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="c734d-117">Operation completed successfully.</span></span><br/>         |
| <dl> <span data-ttu-id="c734d-118"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="c734d-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="c734d-119">Der Parameter " *bstrifdname* " ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="c734d-119">The *bstrIFDName* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="c734d-120"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="c734d-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="c734d-121">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="c734d-121">Out of memory.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="c734d-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c734d-122">Remarks</span></span>

<span data-ttu-id="c734d-123">Zum Anfügen [](../secgloss/s-gly.md) eines smartcardanrufes [**attachbyhandle**](iscardmanage-attachbyhandle.md).</span><span class="sxs-lookup"><span data-stu-id="c734d-123">To attach a [*smart card*](../secgloss/s-gly.md) call [**AttachByHandle**](iscardmanage-attachbyhandle.md).</span></span>

<span data-ttu-id="c734d-124">Zum Freigeben eines Anlage Aufrufs [**trennen**](iscardmanage-detach.md).</span><span class="sxs-lookup"><span data-stu-id="c734d-124">To release an attachment call [**Detach**](iscardmanage-detach.md).</span></span>

<span data-ttu-id="c734d-125">Um erneut eine Verbindung mit der Smartcard herzustellen, ohne [**Detach**](iscardmanage-detach.md) und **attachbyifd** aufzurufen, rufen Sie [**Verbindung**](iscardmanage-reconnect.md)auf.</span><span class="sxs-lookup"><span data-stu-id="c734d-125">To reconnect with the smart card without calling [**Detach**](iscardmanage-detach.md) and **AttachByIFD**, call [**Reconnect**](iscardmanage-reconnect.md).</span></span>

<span data-ttu-id="c734d-126">Eine Liste aller Methoden, die durch diese Schnittstelle definiert werden, finden Sie unter [**iscardmanage**](iscardmanage.md).</span><span class="sxs-lookup"><span data-stu-id="c734d-126">For a list of all the methods defined by this interface, see [**ISCardManage**](iscardmanage.md).</span></span>

<span data-ttu-id="c734d-127">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="c734d-127">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="c734d-128">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="c734d-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c734d-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c734d-129">Requirements</span></span>



| <span data-ttu-id="c734d-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c734d-130">Requirement</span></span> | <span data-ttu-id="c734d-131">Wert</span><span class="sxs-lookup"><span data-stu-id="c734d-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c734d-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c734d-132">Minimum supported client</span></span><br/> | <span data-ttu-id="c734d-133">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c734d-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="c734d-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c734d-134">Minimum supported server</span></span><br/> | <span data-ttu-id="c734d-135">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c734d-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c734d-136">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="c734d-136">End of client support</span></span><br/>    | <span data-ttu-id="c734d-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c734d-137">Windows XP</span></span><br/>                                |
| <span data-ttu-id="c734d-138">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="c734d-138">End of server support</span></span><br/>    | <span data-ttu-id="c734d-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c734d-139">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="c734d-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c734d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c734d-141">**Attachbyhandle**</span><span class="sxs-lookup"><span data-stu-id="c734d-141">**AttachByHandle**</span></span>](iscardmanage-attachbyhandle.md)
</dt> <dt>

[<span data-ttu-id="c734d-142">**Trennen**</span><span class="sxs-lookup"><span data-stu-id="c734d-142">**Detach**</span></span>](iscardmanage-detach.md)
</dt> <dt>

[<span data-ttu-id="c734d-143">**Iscardmanage**</span><span class="sxs-lookup"><span data-stu-id="c734d-143">**ISCardManage**</span></span>](iscardmanage.md)
</dt> <dt>

[<span data-ttu-id="c734d-144">**Verbindung wiederherstellen**</span><span class="sxs-lookup"><span data-stu-id="c734d-144">**Reconnect**</span></span>](iscardmanage-reconnect.md)
</dt> </dl>

 

 
