---
description: Ruft einen Byte Zeiger auf den hglobal-Speicherblock ab, der von der IStream-com-Schnittstelle verwaltet wird.
ms.assetid: ea25eb98-b841-4f5e-b428-3d9cb8176142
title: 'Iscardtypekonv:: getatistreammemory-Methode (scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.GetAtIStreamMemory
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: bdd828921f18c3d06edd2d41da189260a4ed4394
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750033"
---
# <a name="iscardtypeconvgetatistreammemory-method"></a><span data-ttu-id="1e55b-103">Iscardtypekonv:: getatistreammemory-Methode</span><span class="sxs-lookup"><span data-stu-id="1e55b-103">ISCardTypeConv::GetAtIStreamMemory method</span></span>

<span data-ttu-id="1e55b-104">\[Die **getatistreammemory** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="1e55b-104">\[The **GetAtIStreamMemory** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="1e55b-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1e55b-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="1e55b-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="1e55b-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="1e55b-107">Die **getatistreammemory** -Methode erhält einen Byte Zeiger auf den hglobal-Speicherblock, der von der **IStream** -com-Schnittstelle verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="1e55b-107">The **GetAtIStreamMemory** method acquires a byte pointer to the HGLOBAL memory block that is managed by the **IStream** COM interface.</span></span>

<span data-ttu-id="1e55b-108">Dies ist eine Möglichkeit, um den Arbeitsspeicher unter dem **IStream** zu erhalten, ohne den sizeof-Wert für den Speicherblock in Bytes zu erhalten und die Bytes mithilfe der **IStream** -Schnittstelle in ein temporäres Bytearray zu lesen.</span><span class="sxs-lookup"><span data-stu-id="1e55b-108">This is a way to get at the memory under the **IStream** without having to get the sizeof value for the memory block in bytes and read the bytes into a temporary byte array using the **IStream** interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e55b-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="1e55b-109">Syntax</span></span>


```C++
HRESULT GetAtIStreamMemory(
  [in]  LPSTREAM    pStrm,
  [out] LPBYTEARRAY *ppMem
);
```



## <a name="parameters"></a><span data-ttu-id="1e55b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1e55b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e55b-111">*pstraum* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1e55b-111">*pStrm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e55b-112">Ein Zeiger auf die **IStream** -com-Schnittstelle, die den hglobal-Speicherblock verwaltet.</span><span class="sxs-lookup"><span data-stu-id="1e55b-112">A pointer to the **IStream** COM interface that manages the HGLOBAL memory block.</span></span>

</dd> <dt>

<span data-ttu-id="1e55b-113">*ppMem* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1e55b-113">*ppMem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1e55b-114">Ein Zeiger auf das erste Byte des HGLOBAL-Speicherblocks, wenn der Vorgang erfolgreich war. andernfalls **null** , wenn der Vorgang fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="1e55b-114">A pointer to the first byte of the HGLOBAL memory block if successful; else, **NULL** if operation fails.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e55b-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1e55b-115">Return value</span></span>

<span data-ttu-id="1e55b-116">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="1e55b-116">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="1e55b-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="1e55b-117">Return code</span></span>                                                                                   | <span data-ttu-id="1e55b-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1e55b-118">Description</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1e55b-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1e55b-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="1e55b-120">Der Arbeitsspeicher wurde erfolgreich zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="1e55b-120">Memory allocated successfully.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="1e55b-121"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="1e55b-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="1e55b-122">Bei einem oder mehreren Parametern, die an die Funktion weitergegeben wurden, ist ein Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="1e55b-122">There is something wrong with one or more of the parameters passed into the function.</span></span><br/> |
| <dl> <span data-ttu-id="1e55b-123"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="1e55b-123"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="1e55b-124">Ein Parameter vom Zeigertyp war falsch.</span><span class="sxs-lookup"><span data-stu-id="1e55b-124">A parameter of pointer type was incorrect.</span></span><br/>                                            |
| <dl> <span data-ttu-id="1e55b-125"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="1e55b-125"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="1e55b-126">Nicht genügend freier Arbeitsspeicher, um die Anforderung zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="1e55b-126">Not enough free memory to satisfy request.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="1e55b-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1e55b-127">Remarks</span></span>

<span data-ttu-id="1e55b-128">Der **IStream** -Verweis Zähler wird für jeden abgerufenen *ppMem* -Zeiger inkrementiert.</span><span class="sxs-lookup"><span data-stu-id="1e55b-128">The **IStream** reference count will be incremented for each *ppMem* pointer acquired.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e55b-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1e55b-129">Requirements</span></span>



| <span data-ttu-id="1e55b-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1e55b-130">Requirement</span></span> | <span data-ttu-id="1e55b-131">Wert</span><span class="sxs-lookup"><span data-stu-id="1e55b-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e55b-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1e55b-132">Minimum supported client</span></span><br/> | <span data-ttu-id="1e55b-133">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1e55b-133">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="1e55b-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1e55b-134">Minimum supported server</span></span><br/> | <span data-ttu-id="1e55b-135">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1e55b-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1e55b-136">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="1e55b-136">End of client support</span></span><br/>    | <span data-ttu-id="1e55b-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1e55b-137">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="1e55b-138">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="1e55b-138">End of server support</span></span><br/>    | <span data-ttu-id="1e55b-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1e55b-139">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="1e55b-140">Header</span><span class="sxs-lookup"><span data-stu-id="1e55b-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e55b-141"><dt>"Scarddat. h"</dt></span><span class="sxs-lookup"><span data-stu-id="1e55b-141"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="1e55b-142">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="1e55b-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="1e55b-143"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="1e55b-143"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="1e55b-144">DLL</span><span class="sxs-lookup"><span data-stu-id="1e55b-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e55b-145"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e55b-145"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="1e55b-146">IID</span><span class="sxs-lookup"><span data-stu-id="1e55b-146">IID</span></span><br/>                      | <span data-ttu-id="1e55b-147">IID \_ iscardtypec ist als 53b6aa63-3F 56-11D0-916b-00aa00c18068 definiert.</span><span class="sxs-lookup"><span data-stu-id="1e55b-147">IID\_ISCardTypeConv is defined as 53B6AA63-3F56-11D0-916B-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="1e55b-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1e55b-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e55b-149">**Iscardtypeconfiguration**</span><span class="sxs-lookup"><span data-stu-id="1e55b-149">**ISCardTypeConv**</span></span>](iscardtypeconv.md)
</dt> <dt>

[<span data-ttu-id="1e55b-150">Smartcard-Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="1e55b-150">Smart Card Return Values</span></span>](authentication-return-values.md)
</dt> </dl>

 

 
