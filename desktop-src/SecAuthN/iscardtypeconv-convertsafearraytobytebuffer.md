---
description: Konvertiert ein als SAFEARRAY definiertes Bytearray in einen universellen Puffer von Bytes (IStream-Objekt).
ms.assetid: faa07bb5-cfdb-4181-b86a-f82a9c6b251a
title: 'Iscardtypekonv:: convertafearraydebytebuffer-Methode (scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.ConvertSafeArrayToByteBuffer
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: aa6503f474d96e3c25da3f2780ac43976b6507a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958875"
---
# <a name="iscardtypeconvconvertsafearraytobytebuffer-method"></a><span data-ttu-id="616bd-103">Iscardtypekonv:: converzafearraydebytebuffer-Methode</span><span class="sxs-lookup"><span data-stu-id="616bd-103">ISCardTypeConv::ConvertSafeArrayToByteBuffer method</span></span>

<span data-ttu-id="616bd-104">\[Die **convertafearraytobytebuffer** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="616bd-104">\[The **ConvertSafeArrayToByteBuffer** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="616bd-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="616bd-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="616bd-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="616bd-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="616bd-107">Die **convertsafearraydebytebuffer** -Methode konvertiert ein als SAFEARRAY definiertes Bytearray in einen universellen Puffer von Bytes (**IStream** -Objekt).</span><span class="sxs-lookup"><span data-stu-id="616bd-107">The **ConvertSafeArrayToByteBuffer** method converts a byte array defined as a SAFEARRAY into a universal buffer of bytes (**IStream** object).</span></span>

<span data-ttu-id="616bd-108">Der erstellte Byte Puffer ist ein Datenstrom, der über einem Speicherblock zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="616bd-108">The byte buffer created is a stream mapped over a memory block.</span></span> <span data-ttu-id="616bd-109">Verwenden Sie die von der **IStream** -Schnittstelle bereitgestellten Methoden, um auf den Puffer zuzugreifen oder ihn zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="616bd-109">To access or manage the buffer, use the methods provided by the **IStream** interface.</span></span> <span data-ttu-id="616bd-110">Ein eindeutiges Feature zu dieser Array Implementierung besteht darin, dass beim aufruft der **IStream:: Release** -Methode der zugrunde liegende Arbeitsspeicher für Sie freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="616bd-110">A unique feature about this array implementation is that when you call the **IStream::Release** method, the underlying memory will be released for you.</span></span>

## <a name="syntax"></a><span data-ttu-id="616bd-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="616bd-111">Syntax</span></span>


```C++
HRESULT ConvertSafeArrayToByteBuffer(
  [in]  LPSAFEARRAY  pbyArray,
  [out] LPBYTEBUFFER *ppbyBuff
);
```



## <a name="parameters"></a><span data-ttu-id="616bd-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="616bd-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="616bd-113">*pbyarray* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="616bd-113">*pbyArray* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="616bd-114">Zeiger auf das SafeArray, das konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="616bd-114">Pointer to the SAFEARRAY to be converted.</span></span>

</dd> <dt>

<span data-ttu-id="616bd-115">*ppbybuff* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="616bd-115">*ppbyBuff* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="616bd-116">Zeiger auf das **IStream** -Objekt, das zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="616bd-116">Pointer to the **IStream** object to be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="616bd-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="616bd-117">Return value</span></span>

<span data-ttu-id="616bd-118">Die-Methode gibt einen der folgenden möglichen Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="616bd-118">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="616bd-119">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="616bd-119">Return code</span></span>                                                                                   | <span data-ttu-id="616bd-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="616bd-120">Description</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="616bd-121"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="616bd-121"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="616bd-122">Der Arbeitsspeicher wurde erfolgreich zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="616bd-122">Memory allocated successfully.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="616bd-123"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="616bd-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="616bd-124">Bei einem oder mehreren Parametern, die an die Funktion weitergegeben wurden, ist ein Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="616bd-124">There is something wrong with one or more of the parameters passed into the function.</span></span><br/> |
| <dl> <span data-ttu-id="616bd-125"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="616bd-125"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="616bd-126">Ein Parameter vom Zeigertyp war falsch.</span><span class="sxs-lookup"><span data-stu-id="616bd-126">A parameter of pointer type was incorrect.</span></span><br/>                                            |
| <dl> <span data-ttu-id="616bd-127"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="616bd-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="616bd-128">Nicht genügend freier Arbeitsspeicher, um die Anforderung zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="616bd-128">Not enough free memory to satisfy request.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="616bd-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="616bd-129">Remarks</span></span>

<span data-ttu-id="616bd-130">Der zugeordnete Arbeitsspeicher kann verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="616bd-130">Memory allocated is moveable.</span></span> <span data-ttu-id="616bd-131">Verwenden Sie die **IStream:: Release** -Methode, um den Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="616bd-131">Use the **IStream::Release** method to free the memory.</span></span>

## <a name="requirements"></a><span data-ttu-id="616bd-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="616bd-132">Requirements</span></span>



| <span data-ttu-id="616bd-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="616bd-133">Requirement</span></span> | <span data-ttu-id="616bd-134">Wert</span><span class="sxs-lookup"><span data-stu-id="616bd-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="616bd-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="616bd-135">Minimum supported client</span></span><br/> | <span data-ttu-id="616bd-136">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="616bd-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="616bd-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="616bd-137">Minimum supported server</span></span><br/> | <span data-ttu-id="616bd-138">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="616bd-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="616bd-139">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="616bd-139">End of client support</span></span><br/>    | <span data-ttu-id="616bd-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="616bd-140">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="616bd-141">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="616bd-141">End of server support</span></span><br/>    | <span data-ttu-id="616bd-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="616bd-142">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="616bd-143">Header</span><span class="sxs-lookup"><span data-stu-id="616bd-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="616bd-144"><dt>"Scarddat. h"</dt></span><span class="sxs-lookup"><span data-stu-id="616bd-144"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="616bd-145">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="616bd-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="616bd-146"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="616bd-146"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="616bd-147">DLL</span><span class="sxs-lookup"><span data-stu-id="616bd-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="616bd-148"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="616bd-148"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="616bd-149">IID</span><span class="sxs-lookup"><span data-stu-id="616bd-149">IID</span></span><br/>                      | <span data-ttu-id="616bd-150">IID \_ iscardtypec ist als 53b6aa63-3F 56-11D0-916b-00aa00c18068 definiert.</span><span class="sxs-lookup"><span data-stu-id="616bd-150">IID\_ISCardTypeConv is defined as 53B6AA63-3F56-11D0-916B-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="616bd-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="616bd-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="616bd-152">**Iscardtypeconfiguration**</span><span class="sxs-lookup"><span data-stu-id="616bd-152">**ISCardTypeConv**</span></span>](iscardtypeconv.md)
</dt> <dt>

[<span data-ttu-id="616bd-153">Smartcard-Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="616bd-153">Smart Card Return Values</span></span>](authentication-return-values.md)
</dt> </dl>

 

 
