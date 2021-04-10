---
description: Die Open-Methode öffnet die angegebene Datei zur weiteren Verwendung.
ms.assetid: a970daba-ed04-45f0-9b2d-3883807050df
title: 'Iscardfileaccess:: Open-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Open
api_type:
- COM
api_location: ''
ms.openlocfilehash: d1b68c004d4de308b641a1c4cb187312150f4d2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131456"
---
# <a name="iscardfileaccessopen-method"></a><span data-ttu-id="c9270-103">Iscardfileaccess:: Open-Methode</span><span class="sxs-lookup"><span data-stu-id="c9270-103">ISCardFileAccess::Open method</span></span>

<span data-ttu-id="c9270-104">\[Die **Open** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="c9270-104">\[The **Open** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="c9270-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c9270-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="c9270-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="c9270-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="c9270-107">Die **Open** -Methode öffnet die angegebene Datei zur weiteren Verwendung.</span><span class="sxs-lookup"><span data-stu-id="c9270-107">The **Open** method opens the specified file for further use.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9270-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c9270-108">Syntax</span></span>


```C++
HRESULT Open(
  [in]  REFTYPE     refType,
  [in]  BSTR        bstrPathSpec,
  [out] HSCARD_FILE *phFile
);
```



## <a name="parameters"></a><span data-ttu-id="c9270-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c9270-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9270-110">*RefType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c9270-110">*refType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9270-111">Der Referenztyp, der in *bstrinpathspec* verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c9270-111">Type of reference used in *bstrPathSpec*.</span></span>

<dl><span id="SC_TYPE_BY_NAME"></span><span id="sc_type_by_name"></span><dt>

<span data-ttu-id="c9270-112">**SC- \_ Typ \_ nach \_ Name**</span><span class="sxs-lookup"><span data-stu-id="c9270-112">**SC\_TYPE\_BY\_NAME**</span></span>
</dt><span id="SC_TYPE_BY_ID"></span><span id="sc_type_by_id"></span><dt>

<span data-ttu-id="c9270-113">**SC- \_ Typ \_ nach \_ ID**</span><span class="sxs-lookup"><span data-stu-id="c9270-113">**SC\_TYPE\_BY\_ID**</span></span>
</dt><span id="SC_TYPE_BY_SHORT"></span><span id="sc_type_by_short"></span><dt>

<span data-ttu-id="c9270-114">**SC \_ - \_ Typ \_ kurz**</span><span class="sxs-lookup"><span data-stu-id="c9270-114">**SC\_TYPE\_BY\_SHORT**</span></span>
</dt><span id="SC_TYPE_BY_ANY"></span><span id="sc_type_by_any"></span><dt>

<span data-ttu-id="c9270-115">**SC- \_ Typ \_ nach \_ beliebigen**</span><span class="sxs-lookup"><span data-stu-id="c9270-115">**SC\_TYPE\_BY\_ANY**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="c9270-116">*bstrinpathspec* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c9270-116">*bstrPathSpec* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9270-117">Die zu öffnende Datei.</span><span class="sxs-lookup"><span data-stu-id="c9270-117">File to open.</span></span>

</dd> <dt>

<span data-ttu-id="c9270-118">*phfile* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c9270-118">*phFile* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c9270-119">Zeiger auf eine hscard- \_ Datei, die das Datei Handle enthalten wird.</span><span class="sxs-lookup"><span data-stu-id="c9270-119">Pointer to an HSCARD\_FILE that will hold the file handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9270-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c9270-120">Return value</span></span>

<span data-ttu-id="c9270-121">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="c9270-121">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="c9270-122">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="c9270-122">Return code</span></span>                                                                                   | <span data-ttu-id="c9270-123">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c9270-123">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="c9270-124"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c9270-124"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="c9270-125">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="c9270-125">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="c9270-126"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="c9270-126"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="c9270-127">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="c9270-127">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="c9270-128"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="c9270-128"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="c9270-129">Es wurde ein fehlerhafter Zeiger übermittelt.</span><span class="sxs-lookup"><span data-stu-id="c9270-129">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="c9270-130"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="c9270-130"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="c9270-131">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="c9270-131">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="c9270-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c9270-132">Remarks</span></span>

<span data-ttu-id="c9270-133">Um eine Datei zu schließen, müssen Sie [**Close**](iscardfileaccess-close.md)aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="c9270-133">To close a file, call [**Close**](iscardfileaccess-close.md).</span></span>

<span data-ttu-id="c9270-134">Eine Liste aller Methoden, die durch diese Schnittstelle definiert werden, finden Sie unter [**iscardfileaccess**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="c9270-134">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="c9270-135">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die [*Smartcard*](../secgloss/s-gly.md) zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="c9270-135">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="c9270-136">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="c9270-136">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c9270-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c9270-137">Requirements</span></span>



| <span data-ttu-id="c9270-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c9270-138">Requirement</span></span> | <span data-ttu-id="c9270-139">Wert</span><span class="sxs-lookup"><span data-stu-id="c9270-139">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c9270-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c9270-140">Minimum supported client</span></span><br/> | <span data-ttu-id="c9270-141">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c9270-141">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="c9270-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c9270-142">Minimum supported server</span></span><br/> | <span data-ttu-id="c9270-143">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c9270-143">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c9270-144">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="c9270-144">End of client support</span></span><br/>    | <span data-ttu-id="c9270-145">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c9270-145">Windows XP</span></span><br/>                                |
| <span data-ttu-id="c9270-146">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="c9270-146">End of server support</span></span><br/>    | <span data-ttu-id="c9270-147">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c9270-147">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="c9270-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c9270-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9270-149">**Schließen**</span><span class="sxs-lookup"><span data-stu-id="c9270-149">**Close**</span></span>](iscardfileaccess-close.md)
</dt> <dt>

[<span data-ttu-id="c9270-150">**Iscardfileaccess**</span><span class="sxs-lookup"><span data-stu-id="c9270-150">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> </dl>

 

 
