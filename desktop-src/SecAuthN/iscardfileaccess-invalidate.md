---
description: Legt fest, dass die angegebene Datei (EF oder DF) ungültig ist. Auf eine ungültige Datei kann nicht durch andere Methoden zugegriffen werden, bevor die Verwendung von "Rehabilitation" erfolgt.
ms.assetid: 5600fcf0-091c-437e-a45c-4de5b0a47d68
title: 'Iscardfileaccess:: Invalidate-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Invalidate
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3e1d74885f97eca64f403155f1dba52e398b9426
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369732"
---
# <a name="iscardfileaccessinvalidate-method"></a><span data-ttu-id="b0b21-104">Iscardfileaccess:: Invalidate-Methode</span><span class="sxs-lookup"><span data-stu-id="b0b21-104">ISCardFileAccess::Invalidate method</span></span>

<span data-ttu-id="b0b21-105">\[Die **Invalidate** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="b0b21-105">\[The **Invalidate** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b0b21-106">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b0b21-106">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="b0b21-107">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="b0b21-107">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="b0b21-108">Die **Invalidate** -Methode macht die angegebene Datei (EF oder DF) ungültig.</span><span class="sxs-lookup"><span data-stu-id="b0b21-108">The **Invalidate** method makes the specified file (EF or DF) not valid.</span></span> <span data-ttu-id="b0b21-109">Auf eine ungültige Datei kann nicht durch andere Methoden zugegriffen werden, bevor die Verwendung von " [**Rehabilitation**](iscardfileaccess-rehabilitate.md)" erfolgt.</span><span class="sxs-lookup"><span data-stu-id="b0b21-109">A file that is not valid cannot be accessed by other methods prior to using [**Rehabilitate**](iscardfileaccess-rehabilitate.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b0b21-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="b0b21-110">Syntax</span></span>


```C++
HRESULT Invalidate(
  [in] BSTR        bstrPathSpec,
  [in] SCARD_FLAGS flags
);
```



## <a name="parameters"></a><span data-ttu-id="b0b21-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="b0b21-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0b21-112">*bstrinpathspec* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b0b21-112">*bstrPathSpec* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0b21-113">Datei.</span><span class="sxs-lookup"><span data-stu-id="b0b21-113">File.</span></span>

</dd> <dt>

<span data-ttu-id="b0b21-114">*Flags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b0b21-114">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0b21-115">Gibt an, ob sicheres Messaging verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b0b21-115">Specifies whether secure messaging should be used.</span></span>

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

<span data-ttu-id="b0b21-116">**SC \_ FL \_ Secure \_ Messaging**</span><span class="sxs-lookup"><span data-stu-id="b0b21-116">**SC\_FL\_SECURE\_MESSAGING**</span></span>
</dt> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0b21-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b0b21-117">Return value</span></span>

<span data-ttu-id="b0b21-118">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="b0b21-118">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="b0b21-119">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="b0b21-119">Return code</span></span>                                                                                   | <span data-ttu-id="b0b21-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b0b21-120">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="b0b21-121"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b0b21-121"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="b0b21-122">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="b0b21-122">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="b0b21-123"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="b0b21-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="b0b21-124">Ein Parameter ist nicht gültig.</span><span class="sxs-lookup"><span data-stu-id="b0b21-124">A parameter is not valid.</span></span><br/>         |
| <dl> <span data-ttu-id="b0b21-125"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="b0b21-125"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="b0b21-126">Es wurde ein fehlerhafter Zeiger übermittelt.</span><span class="sxs-lookup"><span data-stu-id="b0b21-126">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="b0b21-127"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="b0b21-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="b0b21-128">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="b0b21-128">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="b0b21-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b0b21-129">Remarks</span></span>

<span data-ttu-id="b0b21-130">Eine Liste aller Methoden, die durch diese Schnittstelle definiert werden, finden Sie unter [**iscardfileaccess**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="b0b21-130">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="b0b21-131">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die [*Smartcard*](../secgloss/s-gly.md) zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="b0b21-131">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="b0b21-132">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="b0b21-132">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b0b21-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b0b21-133">Requirements</span></span>



| <span data-ttu-id="b0b21-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b0b21-134">Requirement</span></span> | <span data-ttu-id="b0b21-135">Wert</span><span class="sxs-lookup"><span data-stu-id="b0b21-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b0b21-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b0b21-136">Minimum supported client</span></span><br/> | <span data-ttu-id="b0b21-137">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b0b21-137">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="b0b21-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b0b21-138">Minimum supported server</span></span><br/> | <span data-ttu-id="b0b21-139">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b0b21-139">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b0b21-140">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="b0b21-140">End of client support</span></span><br/>    | <span data-ttu-id="b0b21-141">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b0b21-141">Windows XP</span></span><br/>                                |
| <span data-ttu-id="b0b21-142">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="b0b21-142">End of server support</span></span><br/>    | <span data-ttu-id="b0b21-143">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b0b21-143">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="b0b21-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b0b21-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0b21-145">**Iscardfileaccess**</span><span class="sxs-lookup"><span data-stu-id="b0b21-145">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> <dt>

[<span data-ttu-id="b0b21-146">**Rehabilitations**</span><span class="sxs-lookup"><span data-stu-id="b0b21-146">**Rehabilitate**</span></span>](iscardfileaccess-rehabilitate.md)
</dt> </dl>

 

 
