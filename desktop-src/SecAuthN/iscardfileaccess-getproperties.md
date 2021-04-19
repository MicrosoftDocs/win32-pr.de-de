---
description: Ruft die primitiven Daten ab, auf die von TLVS (Tag, Länge, Wert) für das angegebene Objekt verwiesen wird.
ms.assetid: 135aeb9a-b851-4522-862f-02a7e020c36b
title: 'Iscardfileaccess:: GetProperties-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.GetProperties
api_type:
- COM
api_location: ''
ms.openlocfilehash: 25e6ae1ab657d92dda0ad421b650eaaa7076bd63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368846"
---
# <a name="iscardfileaccessgetproperties-method"></a><span data-ttu-id="893fc-103">Iscardfileaccess:: GetProperties-Methode</span><span class="sxs-lookup"><span data-stu-id="893fc-103">ISCardFileAccess::GetProperties method</span></span>

<span data-ttu-id="893fc-104">\[Die **GetProperties** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="893fc-104">\[The **GetProperties** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="893fc-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="893fc-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="893fc-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="893fc-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="893fc-107">Die **GetProperties** -Methode ruft die primitiven Daten ab, auf die von TLVS (Tag, Länge, Wert) für das angegebene Objekt verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="893fc-107">The **GetProperties** method retrieves the primitive data referred by TLVs (tag, length, value) for the specified object.</span></span>

## <a name="syntax"></a><span data-ttu-id="893fc-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="893fc-108">Syntax</span></span>


```C++
HRESULT GetProperties(
  [in]      REFTYPE     refType,
  [in]      BSTR        bstrPathSpec,
  [in]      SCARD_FLAGS flags,
  [in, out] LPTLV_TABLE *ppTLV
);
```



## <a name="parameters"></a><span data-ttu-id="893fc-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="893fc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="893fc-110">*RefType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="893fc-110">*refType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="893fc-111">Der Referenztyp, der in *bstrinnewdir* verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="893fc-111">Type of reference used in *bstrNewDir*.</span></span>

<dl><span id="SC_TYPE_BY_NAME"></span><span id="sc_type_by_name"></span><dt>

<span data-ttu-id="893fc-112">**SC- \_ Typ \_ nach \_ Name**</span><span class="sxs-lookup"><span data-stu-id="893fc-112">**SC\_TYPE\_BY\_NAME**</span></span>
</dt><span id="SC_TYPE_BY_ID"></span><span id="sc_type_by_id"></span><dt>

<span data-ttu-id="893fc-113">**SC- \_ Typ \_ nach \_ ID**</span><span class="sxs-lookup"><span data-stu-id="893fc-113">**SC\_TYPE\_BY\_ID**</span></span>
</dt><span id="SC_TYPE_BY_SHORT"></span><span id="sc_type_by_short"></span><dt>

<span data-ttu-id="893fc-114">**SC \_ - \_ Typ \_ kurz**</span><span class="sxs-lookup"><span data-stu-id="893fc-114">**SC\_TYPE\_BY\_SHORT**</span></span>
</dt><span id="SC_TYPE_BY_ANY"></span><span id="sc_type_by_any"></span><dt>

<span data-ttu-id="893fc-115">**SC- \_ Typ \_ nach \_ beliebigen**</span><span class="sxs-lookup"><span data-stu-id="893fc-115">**SC\_TYPE\_BY\_ANY**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="893fc-116">*bstrinpathspec* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="893fc-116">*bstrPathSpec* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="893fc-117">Datei.</span><span class="sxs-lookup"><span data-stu-id="893fc-117">File.</span></span>

</dd> <dt>

<span data-ttu-id="893fc-118">*Flags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="893fc-118">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="893fc-119">Gibt an, ob sicheres Messaging verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="893fc-119">Specifies whether secure messaging should be used.</span></span>

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

<span data-ttu-id="893fc-120">**SC \_ FL \_ Secure \_ Messaging**</span><span class="sxs-lookup"><span data-stu-id="893fc-120">**SC\_FL\_SECURE\_MESSAGING**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="893fc-121">*pptlv* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="893fc-121">*ppTLV* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="893fc-122">Zeiger auf TLV-Strukturen, deren Wert abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="893fc-122">Pointer to TLV structures whose value has been retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="893fc-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="893fc-123">Return value</span></span>

<span data-ttu-id="893fc-124">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="893fc-124">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="893fc-125">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="893fc-125">Return code</span></span>                                                                                   | <span data-ttu-id="893fc-126">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="893fc-126">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="893fc-127"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="893fc-127"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="893fc-128">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="893fc-128">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="893fc-129"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="893fc-129"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="893fc-130">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="893fc-130">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="893fc-131"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="893fc-131"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="893fc-132">Es wurde ein fehlerhafter Zeiger übermittelt.</span><span class="sxs-lookup"><span data-stu-id="893fc-132">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="893fc-133"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="893fc-133"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="893fc-134">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="893fc-134">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="893fc-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="893fc-135">Remarks</span></span>

<span data-ttu-id="893fc-136">Eine Liste aller Methoden, die durch diese Schnittstelle definiert werden, finden Sie unter [**iscardfileaccess**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="893fc-136">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="893fc-137">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die [*Smartcard*](../secgloss/s-gly.md) zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="893fc-137">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="893fc-138">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="893fc-138">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="893fc-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="893fc-139">Requirements</span></span>



| <span data-ttu-id="893fc-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="893fc-140">Requirement</span></span> | <span data-ttu-id="893fc-141">Wert</span><span class="sxs-lookup"><span data-stu-id="893fc-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="893fc-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="893fc-142">Minimum supported client</span></span><br/> | <span data-ttu-id="893fc-143">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="893fc-143">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="893fc-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="893fc-144">Minimum supported server</span></span><br/> | <span data-ttu-id="893fc-145">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="893fc-145">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="893fc-146">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="893fc-146">End of client support</span></span><br/>    | <span data-ttu-id="893fc-147">Windows XP</span><span class="sxs-lookup"><span data-stu-id="893fc-147">Windows XP</span></span><br/>                                |
| <span data-ttu-id="893fc-148">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="893fc-148">End of server support</span></span><br/>    | <span data-ttu-id="893fc-149">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="893fc-149">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="893fc-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="893fc-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="893fc-151">**Iscardfileaccess**</span><span class="sxs-lookup"><span data-stu-id="893fc-151">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> </dl>

 

 
