---
description: Ruft den aktuellen Status der Smartcard oder des Readers ab.
ms.assetid: ae285e2e-6591-43ab-b92f-1ec755872379
title: 'Iscardmanage:: Status-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.Status
api_type:
- COM
api_location: ''
ms.openlocfilehash: 26683823b5b709d86b36f4345b47f306f2000ef2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345278"
---
# <a name="iscardmanagestatus-method"></a><span data-ttu-id="669ac-103">Iscardmanage:: Status-Methode</span><span class="sxs-lookup"><span data-stu-id="669ac-103">ISCardManage::Status method</span></span>

<span data-ttu-id="669ac-104">\[Die **Status** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="669ac-104">\[The **Status** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="669ac-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="669ac-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="669ac-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="669ac-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="669ac-107">Mit der **Status** -Methode wird der aktuelle Status der [*Smartcard*](../secgloss/s-gly.md) oder des [*Readers*](../secgloss/r-gly.md)abgerufen.</span><span class="sxs-lookup"><span data-stu-id="669ac-107">The **Status** method gets the current status of the [*smart card*](../secgloss/s-gly.md) or [*reader*](../secgloss/r-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="669ac-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="669ac-108">Syntax</span></span>


```C++
HRESULT Status(
  [out] SCARD_STATES    *pStatus,
  [out] SCARD_PROTOCOLS *pProtocols
);
```



## <a name="parameters"></a><span data-ttu-id="669ac-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="669ac-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="669ac-110">*pstatus* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="669ac-110">*pStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="669ac-111">Zeiger auf einen SCard \_ States-Enumerationswert.</span><span class="sxs-lookup"><span data-stu-id="669ac-111">Pointer to an SCARD\_STATES enumeration value.</span></span> <span data-ttu-id="669ac-112">Enthält bei der Rückgabe den aktuellen Status/Zustand.</span><span class="sxs-lookup"><span data-stu-id="669ac-112">On return, contains the current status/state.</span></span>

</dd> <dt>

<span data-ttu-id="669ac-113">*pprotokolle* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="669ac-113">*pProtocols* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="669ac-114">Zeiger auf den \_ Enumerationswert eines SCard-Protokolls.</span><span class="sxs-lookup"><span data-stu-id="669ac-114">Pointer to an SCARD\_PROTOCOLS enumeration value.</span></span> <span data-ttu-id="669ac-115">Enthält bei der Rückgabe das aktuelle Protokoll.</span><span class="sxs-lookup"><span data-stu-id="669ac-115">On return, contains the current protocol.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="669ac-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="669ac-116">Return value</span></span>

<span data-ttu-id="669ac-117">Die-Methode gibt einen der folgenden möglichen Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="669ac-117">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="669ac-118">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="669ac-118">Return code</span></span>                                                                                   | <span data-ttu-id="669ac-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="669ac-119">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="669ac-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="669ac-120"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="669ac-121">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="669ac-121">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="669ac-122"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="669ac-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="669ac-123">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="669ac-123">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="669ac-124"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="669ac-124"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="669ac-125">Es wurde ein fehlerhafter Zeiger übermittelt.</span><span class="sxs-lookup"><span data-stu-id="669ac-125">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="669ac-126"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="669ac-126"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="669ac-127">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="669ac-127">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="669ac-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="669ac-128">Remarks</span></span>

<span data-ttu-id="669ac-129">Eine Liste aller Methoden, die durch diese Schnittstelle definiert werden, finden Sie unter [**iscardmanage**](iscardmanage.md).</span><span class="sxs-lookup"><span data-stu-id="669ac-129">For a list of all the methods defined by this interface, see [**ISCardManage**](iscardmanage.md).</span></span>

<span data-ttu-id="669ac-130">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="669ac-130">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="669ac-131">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="669ac-131">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="669ac-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="669ac-132">Requirements</span></span>



| <span data-ttu-id="669ac-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="669ac-133">Requirement</span></span> | <span data-ttu-id="669ac-134">Wert</span><span class="sxs-lookup"><span data-stu-id="669ac-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="669ac-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="669ac-135">Minimum supported client</span></span><br/> | <span data-ttu-id="669ac-136">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="669ac-136">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="669ac-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="669ac-137">Minimum supported server</span></span><br/> | <span data-ttu-id="669ac-138">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="669ac-138">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="669ac-139">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="669ac-139">End of client support</span></span><br/>    | <span data-ttu-id="669ac-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="669ac-140">Windows XP</span></span><br/>                                |
| <span data-ttu-id="669ac-141">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="669ac-141">End of server support</span></span><br/>    | <span data-ttu-id="669ac-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="669ac-142">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="669ac-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="669ac-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="669ac-144">**Iscardmanage**</span><span class="sxs-lookup"><span data-stu-id="669ac-144">**ISCardManage**</span></span>](iscardmanage.md)
</dt> </dl>

 

 
