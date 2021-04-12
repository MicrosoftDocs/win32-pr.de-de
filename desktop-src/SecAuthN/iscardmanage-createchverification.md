---
description: Erstellt eine iscardverify-Schnittstelle.
ms.assetid: 6338e672-83cd-46fe-8f94-f4ba6e2581ea
title: 'Iscardmanage:: kreatechverification-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.CreateCHVerification
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3a5909a8782571f9bd01a1c31e5ccd04c3d029df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217761"
---
# <a name="iscardmanagecreatechverification-method"></a><span data-ttu-id="8045d-103">Iscardmanage:: kreatechverification-Methode</span><span class="sxs-lookup"><span data-stu-id="8045d-103">ISCardManage::CreateCHVerification method</span></span>

<span data-ttu-id="8045d-104">\[Die **Methode "** Methode" ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="8045d-104">\[The **CreateCHVerification** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="8045d-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8045d-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8045d-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="8045d-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="8045d-107">Die **Methode** "Methode" erstellt eine [**iscardverify**](iscardverify.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="8045d-107">The **CreateCHVerification** method creates an [**ISCardVerify**](iscardverify.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="8045d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="8045d-108">Syntax</span></span>


```C++
HRESULT CreateCHVerification(
  [out] ISCardVerify **ppISCardVerify
);
```



## <a name="parameters"></a><span data-ttu-id="8045d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="8045d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8045d-110">*ppiscardverify* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8045d-110">*ppISCardVerify* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8045d-111">Der Zeiger auf die erstellte [**iscardverify**](iscardverify.md) -Schnittstelle wurde zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8045d-111">Returned pointer to the created [**ISCardVerify**](iscardverify.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8045d-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8045d-112">Return value</span></span>

<span data-ttu-id="8045d-113">Die-Methode gibt einen der folgenden möglichen Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="8045d-113">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="8045d-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="8045d-114">Return code</span></span>                                                                                   | <span data-ttu-id="8045d-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8045d-115">Description</span></span>                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="8045d-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8045d-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="8045d-117">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="8045d-117">Operation completed successfully.</span></span><br/>             |
| <dl> <span data-ttu-id="8045d-118"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="8045d-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="8045d-119">Der *ppiscardverify* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="8045d-119">The *ppISCardVerify* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="8045d-120"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="8045d-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="8045d-121">Ein fehlerhafter Zeiger wurde in *ppiscardverify über* mittelt.</span><span class="sxs-lookup"><span data-stu-id="8045d-121">A bad pointer was passed in *ppISCardVerify*.</span></span><br/> |
| <dl> <span data-ttu-id="8045d-122"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="8045d-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="8045d-123">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="8045d-123">Out of memory.</span></span><br/>                                |



 

## <a name="remarks"></a><span data-ttu-id="8045d-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8045d-124">Remarks</span></span>

<span data-ttu-id="8045d-125">Eine Liste aller Methoden, die durch diese Schnittstelle definiert werden, finden Sie unter [**iscardmanage**](iscardmanage.md).</span><span class="sxs-lookup"><span data-stu-id="8045d-125">For a list of all the methods defined by this interface, see [**ISCardManage**](iscardmanage.md).</span></span>

<span data-ttu-id="8045d-126">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die [*Smartcard*](../secgloss/s-gly.md) zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="8045d-126">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="8045d-127">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="8045d-127">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8045d-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8045d-128">Requirements</span></span>



| <span data-ttu-id="8045d-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8045d-129">Requirement</span></span> | <span data-ttu-id="8045d-130">Wert</span><span class="sxs-lookup"><span data-stu-id="8045d-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8045d-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8045d-131">Minimum supported client</span></span><br/> | <span data-ttu-id="8045d-132">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8045d-132">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="8045d-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8045d-133">Minimum supported server</span></span><br/> | <span data-ttu-id="8045d-134">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8045d-134">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="8045d-135">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="8045d-135">End of client support</span></span><br/>    | <span data-ttu-id="8045d-136">Windows XP</span><span class="sxs-lookup"><span data-stu-id="8045d-136">Windows XP</span></span><br/>                                |
| <span data-ttu-id="8045d-137">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="8045d-137">End of server support</span></span><br/>    | <span data-ttu-id="8045d-138">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8045d-138">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="8045d-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8045d-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8045d-140">**Iscardmanage**</span><span class="sxs-lookup"><span data-stu-id="8045d-140">**ISCardManage**</span></span>](iscardmanage.md)
</dt> <dt>

[<span data-ttu-id="8045d-141">**Iscardverify**</span><span class="sxs-lookup"><span data-stu-id="8045d-141">**ISCardVerify**</span></span>](iscardverify.md)
</dt> </dl>

 

 
