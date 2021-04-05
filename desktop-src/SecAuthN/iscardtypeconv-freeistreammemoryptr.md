---
description: Gibt den Byte Zeiger frei, der auf den von einer IStream-com-Schnittstelle verwalteten HGLOBAL-Speicherblock zeigt.
ms.assetid: a76c97a9-d0e9-4eb0-9f97-15f22111187d
title: 'Iscardtypekonv:: freeistreammemoryptr-Methode (scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.FreeIStreamMemoryPtr
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 12912b8130ed6e1ccaa995f88069b59e96f57c09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103756876"
---
# <a name="iscardtypeconvfreeistreammemoryptr-method"></a><span data-ttu-id="48b9e-103">Iscardtypekonv:: freeistreammemoryptr-Methode</span><span class="sxs-lookup"><span data-stu-id="48b9e-103">ISCardTypeConv::FreeIStreamMemoryPtr method</span></span>

<span data-ttu-id="48b9e-104">\[Die **freeistreammemoryptr** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="48b9e-104">\[The **FreeIStreamMemoryPtr** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="48b9e-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="48b9e-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="48b9e-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="48b9e-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="48b9e-107">Die **freeistreammemoryptr** -Methode gibt den Byte Zeiger frei, der auf den von einer **IStream** -com-Schnittstelle verwalteten HGLOBAL-Speicherblock zeigt.</span><span class="sxs-lookup"><span data-stu-id="48b9e-107">The **FreeIStreamMemoryPtr** method frees the byte pointer pointing to the HGLOBAL memory block managed by an **IStream** COM interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="48b9e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="48b9e-108">Syntax</span></span>


```C++
HRESULT FreeIStreamMemoryPtr(
  [in] LPSTREAM pStrm,
  [in] LPBYTE   pMem
);
```



## <a name="parameters"></a><span data-ttu-id="48b9e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="48b9e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48b9e-110">*pstraum* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="48b9e-110">*pStrm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48b9e-111">Ein Zeiger auf die **IStream** -Schnittstelle, die den Speicherblock verwaltet, auf den *pMem* zeigt.</span><span class="sxs-lookup"><span data-stu-id="48b9e-111">Pointer to the **IStream** interface that manages the memory block pointed to by *pMem*.</span></span>

</dd> <dt>

<span data-ttu-id="48b9e-112">*pMem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="48b9e-112">*pMem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48b9e-113">Zeiger auf den von der **IStream** -Schnittstelle verwalteten Speicherblock.</span><span class="sxs-lookup"><span data-stu-id="48b9e-113">Pointer to the memory block managed by the **IStream** interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48b9e-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="48b9e-114">Return value</span></span>

<span data-ttu-id="48b9e-115">Die-Methode gibt einen der folgenden möglichen Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="48b9e-115">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="48b9e-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="48b9e-116">Return code</span></span>                                                                                   | <span data-ttu-id="48b9e-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="48b9e-117">Description</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="48b9e-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="48b9e-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="48b9e-119">Der Arbeitsspeicher wurde erfolgreich zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="48b9e-119">Memory allocated successfully.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="48b9e-120"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="48b9e-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="48b9e-121">Bei einem oder mehreren Parametern, die an die Funktion weitergegeben wurden, ist ein Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="48b9e-121">There is something wrong with one or more of the parameters passed into the function.</span></span><br/> |
| <dl> <span data-ttu-id="48b9e-122"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="48b9e-122"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="48b9e-123">Ein Parameter vom Zeigertyp war falsch.</span><span class="sxs-lookup"><span data-stu-id="48b9e-123">A parameter of pointer type was incorrect.</span></span><br/>                                            |
| <dl> <span data-ttu-id="48b9e-124"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="48b9e-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="48b9e-125">Nicht genügend freier Arbeitsspeicher, um die Anforderung zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="48b9e-125">Not enough free memory to satisfy request.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="48b9e-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="48b9e-126">Remarks</span></span>

<span data-ttu-id="48b9e-127">Diese Funktion gibt vollständig und sauber den Byte Zeiger frei, der auf den von der **IStream** -Schnittstelle verwalteten HGLOBAL-Speicherblock zeigt.</span><span class="sxs-lookup"><span data-stu-id="48b9e-127">This function completely and cleanly releases the byte pointer pointing to the HGLOBAL memory block managed by the **IStream** interface.</span></span> <span data-ttu-id="48b9e-128">Der Byte Zeiger wird durch einen get-Befehl von [**getatistreammemory**](iscardtypeconv-getatistreammemory.md)abgerufen.</span><span class="sxs-lookup"><span data-stu-id="48b9e-128">The byte pointer is acquired by a call to [**GetAtIStreamMemory**](iscardtypeconv-getatistreammemory.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="48b9e-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="48b9e-129">Requirements</span></span>



| <span data-ttu-id="48b9e-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="48b9e-130">Requirement</span></span> | <span data-ttu-id="48b9e-131">Wert</span><span class="sxs-lookup"><span data-stu-id="48b9e-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="48b9e-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="48b9e-132">Minimum supported client</span></span><br/> | <span data-ttu-id="48b9e-133">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="48b9e-133">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="48b9e-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="48b9e-134">Minimum supported server</span></span><br/> | <span data-ttu-id="48b9e-135">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="48b9e-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="48b9e-136">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="48b9e-136">End of client support</span></span><br/>    | <span data-ttu-id="48b9e-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="48b9e-137">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="48b9e-138">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="48b9e-138">End of server support</span></span><br/>    | <span data-ttu-id="48b9e-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="48b9e-139">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="48b9e-140">Header</span><span class="sxs-lookup"><span data-stu-id="48b9e-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="48b9e-141"><dt>"Scarddat. h"</dt></span><span class="sxs-lookup"><span data-stu-id="48b9e-141"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="48b9e-142">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="48b9e-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="48b9e-143"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="48b9e-143"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="48b9e-144">DLL</span><span class="sxs-lookup"><span data-stu-id="48b9e-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48b9e-145"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="48b9e-145"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="48b9e-146">IID</span><span class="sxs-lookup"><span data-stu-id="48b9e-146">IID</span></span><br/>                      | <span data-ttu-id="48b9e-147">IID \_ iscardtypec ist als 53b6aa63-3F 56-11D0-916b-00aa00c18068 definiert.</span><span class="sxs-lookup"><span data-stu-id="48b9e-147">IID\_ISCardTypeConv is defined as 53B6AA63-3F56-11D0-916B-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="48b9e-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="48b9e-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48b9e-149">**Iscardtypeconfiguration**</span><span class="sxs-lookup"><span data-stu-id="48b9e-149">**ISCardTypeConv**</span></span>](iscardtypeconv.md)
</dt> <dt>

[<span data-ttu-id="48b9e-150">Smartcard-Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="48b9e-150">Smart Card Return Values</span></span>](authentication-return-values.md)
</dt> <dt>

[<span data-ttu-id="48b9e-151">**Getatistreammemory**</span><span class="sxs-lookup"><span data-stu-id="48b9e-151">**GetAtIStreamMemory**</span></span>](iscardtypeconv-getatistreammemory.md)
</dt> </dl>

 

 
