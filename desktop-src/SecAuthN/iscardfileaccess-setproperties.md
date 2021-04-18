---
description: Die SetProperties-Methode legt den primitiven fest, auf den TLVS (Tag, Länge, Wert) für das angegebene Objekt verweist.
ms.assetid: f8f75c8e-14f4-4bc4-b49d-b232ede374b0
title: 'Iscardfileaccess:: SetProperties-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.SetProperties
api_type:
- COM
api_location: ''
ms.openlocfilehash: b54c2193ec17bca9f9b3ba00b2c2bc133707dbb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106351635"
---
# <a name="iscardfileaccesssetproperties-method"></a><span data-ttu-id="3c980-103">Iscardfileaccess:: SetProperties-Methode</span><span class="sxs-lookup"><span data-stu-id="3c980-103">ISCardFileAccess::SetProperties method</span></span>

<span data-ttu-id="3c980-104">\[Die **SetProperties** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="3c980-104">\[The **SetProperties** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="3c980-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3c980-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="3c980-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="3c980-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="3c980-107">Die **SetProperties** -Methode legt den primitiven fest, auf den TLVS (Tag, Länge, Wert) für das angegebene Objekt verweist.</span><span class="sxs-lookup"><span data-stu-id="3c980-107">The **SetProperties** method sets the primitive referred by TLVs (tag, length, value) for the specified object.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c980-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="3c980-108">Syntax</span></span>


```C++
HRESULT SetProperties(
  [in] REFTYPE     refType,
  [in] BSTR        bstrPathSpec,
  [in] SCARD_FLAGS flags,
  [in] LPTLV_TABLE pTable
);
```



## <a name="parameters"></a><span data-ttu-id="3c980-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="3c980-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c980-110">*RefType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3c980-110">*refType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c980-111">Der Referenztyp, der in *bstrinpathspec* verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3c980-111">Type of reference used in *bstrPathSpec*.</span></span>

<dl><span id="SC_TYPE_BY_NAME"></span><span id="sc_type_by_name"></span><dt>

<span data-ttu-id="3c980-112">**SC- \_ Typ \_ nach \_ Name**</span><span class="sxs-lookup"><span data-stu-id="3c980-112">**SC\_TYPE\_BY\_NAME**</span></span>
</dt><span id="SC_TYPE_BY_ID"></span><span id="sc_type_by_id"></span><dt>

<span data-ttu-id="3c980-113">**SC- \_ Typ \_ nach \_ ID**</span><span class="sxs-lookup"><span data-stu-id="3c980-113">**SC\_TYPE\_BY\_ID**</span></span>
</dt><span id="SC_TYPE_BY_SHORT"></span><span id="sc_type_by_short"></span><dt>

<span data-ttu-id="3c980-114">**SC \_ - \_ Typ \_ kurz**</span><span class="sxs-lookup"><span data-stu-id="3c980-114">**SC\_TYPE\_BY\_SHORT**</span></span>
</dt><span id="SC_TYPE_BY_ANY"></span><span id="sc_type_by_any"></span><dt>

<span data-ttu-id="3c980-115">**SC- \_ Typ \_ nach \_ beliebigen**</span><span class="sxs-lookup"><span data-stu-id="3c980-115">**SC\_TYPE\_BY\_ANY**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="3c980-116">*bstrinpathspec* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3c980-116">*bstrPathSpec* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c980-117">Datei.</span><span class="sxs-lookup"><span data-stu-id="3c980-117">File.</span></span>

</dd> <dt>

<span data-ttu-id="3c980-118">*Flags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3c980-118">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c980-119">Gibt an, ob sicheres Messaging verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3c980-119">Specifies whether secure messaging should be used.</span></span>

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

<span data-ttu-id="3c980-120">**SC \_ FL \_ Secure \_ Messaging**</span><span class="sxs-lookup"><span data-stu-id="3c980-120">**SC\_FL\_SECURE\_MESSAGING**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="3c980-121">*ptable* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3c980-121">*pTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c980-122">Zeiger auf TLV-Strukturen, deren Wert festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3c980-122">Pointer to TLV structures whose value should be set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c980-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3c980-123">Return value</span></span>

<span data-ttu-id="3c980-124">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="3c980-124">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="3c980-125">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="3c980-125">Return code</span></span>                                                                                   | <span data-ttu-id="3c980-126">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3c980-126">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="3c980-127"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3c980-127"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="3c980-128">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="3c980-128">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="3c980-129"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="3c980-129"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="3c980-130">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="3c980-130">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="3c980-131"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="3c980-131"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="3c980-132">Es wurde ein fehlerhafter Zeiger übermittelt.</span><span class="sxs-lookup"><span data-stu-id="3c980-132">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="3c980-133"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="3c980-133"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="3c980-134">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="3c980-134">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="3c980-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3c980-135">Remarks</span></span>

<span data-ttu-id="3c980-136">Eine Liste aller Methoden, die durch diese Schnittstelle definiert werden, finden Sie unter [**iscardfileaccess**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="3c980-136">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="3c980-137">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die [*Smartcard*](../secgloss/s-gly.md) zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="3c980-137">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="3c980-138">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="3c980-138">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3c980-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3c980-139">Requirements</span></span>



| <span data-ttu-id="3c980-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3c980-140">Requirement</span></span> | <span data-ttu-id="3c980-141">Wert</span><span class="sxs-lookup"><span data-stu-id="3c980-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3c980-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3c980-142">Minimum supported client</span></span><br/> | <span data-ttu-id="3c980-143">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3c980-143">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="3c980-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3c980-144">Minimum supported server</span></span><br/> | <span data-ttu-id="3c980-145">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3c980-145">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="3c980-146">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="3c980-146">End of client support</span></span><br/>    | <span data-ttu-id="3c980-147">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3c980-147">Windows XP</span></span><br/>                                |
| <span data-ttu-id="3c980-148">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="3c980-148">End of server support</span></span><br/>    | <span data-ttu-id="3c980-149">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3c980-149">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="3c980-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3c980-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c980-151">**Iscardfileaccess**</span><span class="sxs-lookup"><span data-stu-id="3c980-151">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> </dl>

 

 
