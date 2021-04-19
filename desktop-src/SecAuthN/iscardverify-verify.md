---
description: Fordert eine Überprüfung des Benutzers an.
ms.assetid: e8b7155c-3444-4aa8-8a15-3b3624a44a77
title: 'Iscardverify:: Verify-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardVerify.Verify
api_type:
- COM
api_location: ''
ms.openlocfilehash: 68f3a97df672d97e635180f41405a75c4cb84661
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368730"
---
# <a name="iscardverifyverify-method"></a><span data-ttu-id="9e5e1-103">Iscardverify:: Verify-Methode</span><span class="sxs-lookup"><span data-stu-id="9e5e1-103">ISCardVerify::Verify method</span></span>

<span data-ttu-id="9e5e1-104">\[Die **Verifizierungs** Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="9e5e1-104">\[The **Verify** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="9e5e1-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9e5e1-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="9e5e1-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="9e5e1-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="9e5e1-107">Die **Verify** -Methode fordert eine Überprüfung des Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="9e5e1-107">The **Verify** method requests a verification of the user.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e5e1-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="9e5e1-108">Syntax</span></span>


```C++
HRESULT Verify(
  [in] LPBYTEBUFFER pCode,
  [in] SCARD_FLAGS  Flags,
  [in] LONG         lRef
);
```



## <a name="parameters"></a><span data-ttu-id="9e5e1-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="9e5e1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e5e1-110">*pcode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9e5e1-110">*pCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e5e1-111">Enthält den Code, der für die [*Smartcard*](../secgloss/s-gly.md) im CHV-Prozess (Karteninhaber Überprüfung) angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9e5e1-111">Contains the code to be presented to the [*smart card*](../secgloss/s-gly.md) in the CHV (card holder verification) process.</span></span>

</dd> <dt>

<span data-ttu-id="9e5e1-112">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="9e5e1-112">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e5e1-113">Gibt an, ob der Code Global oder lokal ist.</span><span class="sxs-lookup"><span data-stu-id="9e5e1-113">Indicates whether the code is global or local.</span></span>

<dl><span id="SC_FL_IHV_GLOBAL"></span><span id="sc_fl_ihv_global"></span><dt>

<span data-ttu-id="9e5e1-114">**SC \_ FL \_ IHV \_ Global**</span><span class="sxs-lookup"><span data-stu-id="9e5e1-114">**SC\_FL\_IHV\_GLOBAL**</span></span>
</dt><span id="SC_FL_IHV_LOCAL"></span><span id="sc_fl_ihv_local"></span><dt>

<span data-ttu-id="9e5e1-115">**SC \_ FL \_ IHV \_ local**</span><span class="sxs-lookup"><span data-stu-id="9e5e1-115">**SC\_FL\_IHV\_LOCAL**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="9e5e1-116">*lref* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9e5e1-116">*lRef* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e5e1-117">Smartcardspezifischer Verweis.</span><span class="sxs-lookup"><span data-stu-id="9e5e1-117">Smart card specific reference.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e5e1-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9e5e1-118">Return value</span></span>

<span data-ttu-id="9e5e1-119">Die **Verify** -Methode gibt einen der folgenden Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="9e5e1-119">The **Verify** method returns one of the following values:</span></span>



| <span data-ttu-id="9e5e1-120">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="9e5e1-120">Return code</span></span>                                                                                   | <span data-ttu-id="9e5e1-121">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9e5e1-121">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="9e5e1-122"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9e5e1-122"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="9e5e1-123">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="9e5e1-123">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="9e5e1-124"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="9e5e1-124"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="9e5e1-125">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="9e5e1-125">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="9e5e1-126"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="9e5e1-126"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="9e5e1-127">Es wurde ein fehlerhafter Zeiger übermittelt.</span><span class="sxs-lookup"><span data-stu-id="9e5e1-127">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="9e5e1-128"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="9e5e1-128"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="9e5e1-129">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="9e5e1-129">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="9e5e1-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9e5e1-130">Remarks</span></span>

<span data-ttu-id="9e5e1-131">Eine Liste aller Methoden, die durch diese Schnittstelle definiert werden, finden Sie unter [**iscardverify**](iscardverify.md).</span><span class="sxs-lookup"><span data-stu-id="9e5e1-131">For a list of all the methods defined by this interface, see [**ISCardVerify**](iscardverify.md).</span></span>

<span data-ttu-id="9e5e1-132">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="9e5e1-132">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="9e5e1-133">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="9e5e1-133">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9e5e1-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9e5e1-134">Requirements</span></span>



| <span data-ttu-id="9e5e1-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9e5e1-135">Requirement</span></span> | <span data-ttu-id="9e5e1-136">Wert</span><span class="sxs-lookup"><span data-stu-id="9e5e1-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9e5e1-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9e5e1-137">Minimum supported client</span></span><br/> | <span data-ttu-id="9e5e1-138">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9e5e1-138">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="9e5e1-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9e5e1-139">Minimum supported server</span></span><br/> | <span data-ttu-id="9e5e1-140">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9e5e1-140">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="9e5e1-141">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="9e5e1-141">End of client support</span></span><br/>    | <span data-ttu-id="9e5e1-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="9e5e1-142">Windows XP</span></span><br/>                                |
| <span data-ttu-id="9e5e1-143">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="9e5e1-143">End of server support</span></span><br/>    | <span data-ttu-id="9e5e1-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9e5e1-144">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="9e5e1-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9e5e1-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e5e1-146">**Iscardverify**</span><span class="sxs-lookup"><span data-stu-id="9e5e1-146">**ISCardVerify**</span></span>](iscardverify.md)
</dt> </dl>

 

 
