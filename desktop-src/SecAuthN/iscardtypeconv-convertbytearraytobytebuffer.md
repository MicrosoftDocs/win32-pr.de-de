---
description: Konvertiert ein typisches C/C++-Bytearray in einen universellen Puffer von Bytes (IStream-Objekt).
ms.assetid: 512c561a-63f1-463e-9bae-9bec1ebdbe9b
title: 'Iscardtypekonv:: convertbytearraydebytebuffer-Methode (scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.ConvertByteArrayToByteBuffer
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 406e7aecb7e86802ad67c07669ca199b158ad954
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867839"
---
# <a name="iscardtypeconvconvertbytearraytobytebuffer-method"></a><span data-ttu-id="dd2c2-103">Iscardtypekonv:: convertbytearraydebytebuffer-Methode</span><span class="sxs-lookup"><span data-stu-id="dd2c2-103">ISCardTypeConv::ConvertByteArrayToByteBuffer method</span></span>

<span data-ttu-id="dd2c2-104">\[Die **convertbytearraytobytebuffer** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="dd2c2-104">\[The **ConvertByteArrayToByteBuffer** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="dd2c2-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="dd2c2-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="dd2c2-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="dd2c2-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="dd2c2-107">Die **convertbytearrayesbytebuffer** -Methode konvertiert ein typisches C/C++-Bytearray in einen universellen Puffer von Bytes (**IStream** -Objekt).</span><span class="sxs-lookup"><span data-stu-id="dd2c2-107">The **ConvertByteArrayToByteBuffer** method converts a typical C/C++ byte array into a universal buffer of bytes (**IStream** object).</span></span>

<span data-ttu-id="dd2c2-108">Der erstellte Byte Puffer ist ein Datenstrom, der über einem Speicherblock zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="dd2c2-108">The byte buffer created is a stream mapped over a memory block.</span></span> <span data-ttu-id="dd2c2-109">Verwenden Sie die von der **IStream** -Schnittstelle bereitgestellten Methoden, um auf den Puffer zuzugreifen oder ihn zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="dd2c2-109">To access or manage the buffer, use the methods provided by the **IStream** interface.</span></span> <span data-ttu-id="dd2c2-110">Ein eindeutiges Feature zu dieser Array Implementierung besteht darin, dass beim aufruft der **IStream:: Release** -Methode der zugrunde liegende Arbeitsspeicher für Sie freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="dd2c2-110">A unique feature about this array implementation is that when you call the **IStream::Release** method, the underlying memory will be released for you.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd2c2-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="dd2c2-111">Syntax</span></span>


```C++
HRESULT ConvertByteArrayToByteBuffer(
  [in]  LPBYTE       pbyArray,
  [in]  DWORD        dwArraySize,
  [out] LPBYTEBUFFER *ppbyBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="dd2c2-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="dd2c2-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd2c2-113">*pbyarray* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dd2c2-113">*pbyArray* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd2c2-114">Zeiger auf das Bytearray, das konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="dd2c2-114">Pointer to the array of bytes to be converted.</span></span>

</dd> <dt>

<span data-ttu-id="dd2c2-115">*dwarraysize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dd2c2-115">*dwArraySize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd2c2-116">Größe des Byte Arrays, das konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="dd2c2-116">Size of the byte array to be converted.</span></span>

</dd> <dt>

<span data-ttu-id="dd2c2-117">*ppbybuffer* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="dd2c2-117">*ppbyBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dd2c2-118">Zeiger auf das **IStream** -Objekt, das zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="dd2c2-118">Pointer to the **IStream** object to be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd2c2-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dd2c2-119">Return value</span></span>

<span data-ttu-id="dd2c2-120">Die-Methode gibt einen der folgenden möglichen Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="dd2c2-120">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="dd2c2-121">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="dd2c2-121">Return code</span></span>                                                                                   | <span data-ttu-id="dd2c2-122">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dd2c2-122">Description</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="dd2c2-123"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="dd2c2-123"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="dd2c2-124">Der Arbeitsspeicher wurde erfolgreich zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="dd2c2-124">Memory allocated successfully.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="dd2c2-125"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="dd2c2-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="dd2c2-126">Bei einem oder mehreren Parametern, die an die Funktion weitergegeben wurden, ist ein Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="dd2c2-126">There is something wrong with one or more of the parameters passed into the function.</span></span><br/> |
| <dl> <span data-ttu-id="dd2c2-127"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="dd2c2-127"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="dd2c2-128">Ein Parameter vom Zeigertyp war falsch.</span><span class="sxs-lookup"><span data-stu-id="dd2c2-128">A parameter of pointer type was incorrect.</span></span><br/>                                            |
| <dl> <span data-ttu-id="dd2c2-129"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="dd2c2-129"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="dd2c2-130">Nicht genügend freier Arbeitsspeicher, um die Anforderung zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="dd2c2-130">Not enough free memory to satisfy request.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="dd2c2-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dd2c2-131">Remarks</span></span>

<span data-ttu-id="dd2c2-132">Der zugewiesene Arbeitsspeicher ist beweglicher.</span><span class="sxs-lookup"><span data-stu-id="dd2c2-132">Memory allocated is movable.</span></span> <span data-ttu-id="dd2c2-133">Verwenden Sie die **IStream:: Release** -Methode, um den Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="dd2c2-133">Use the **IStream::Release** method to free the memory.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd2c2-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dd2c2-134">Requirements</span></span>



| <span data-ttu-id="dd2c2-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dd2c2-135">Requirement</span></span> | <span data-ttu-id="dd2c2-136">Wert</span><span class="sxs-lookup"><span data-stu-id="dd2c2-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dd2c2-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dd2c2-137">Minimum supported client</span></span><br/> | <span data-ttu-id="dd2c2-138">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dd2c2-138">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="dd2c2-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dd2c2-139">Minimum supported server</span></span><br/> | <span data-ttu-id="dd2c2-140">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dd2c2-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="dd2c2-141">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="dd2c2-141">End of client support</span></span><br/>    | <span data-ttu-id="dd2c2-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="dd2c2-142">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="dd2c2-143">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="dd2c2-143">End of server support</span></span><br/>    | <span data-ttu-id="dd2c2-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="dd2c2-144">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="dd2c2-145">Header</span><span class="sxs-lookup"><span data-stu-id="dd2c2-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd2c2-146"><dt>"Scarddat. h"</dt></span><span class="sxs-lookup"><span data-stu-id="dd2c2-146"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="dd2c2-147">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="dd2c2-147">Type library</span></span><br/>             | <dl> <span data-ttu-id="dd2c2-148"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="dd2c2-148"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="dd2c2-149">DLL</span><span class="sxs-lookup"><span data-stu-id="dd2c2-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd2c2-150"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd2c2-150"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="dd2c2-151">IID</span><span class="sxs-lookup"><span data-stu-id="dd2c2-151">IID</span></span><br/>                      | <span data-ttu-id="dd2c2-152">IID \_ iscardtypec ist als 53b6aa63-3F 56-11D0-916b-00aa00c18068 definiert.</span><span class="sxs-lookup"><span data-stu-id="dd2c2-152">IID\_ISCardTypeConv is defined as 53B6AA63-3F56-11D0-916B-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="dd2c2-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dd2c2-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd2c2-154">**Iscardtypeconfiguration**</span><span class="sxs-lookup"><span data-stu-id="dd2c2-154">**ISCardTypeConv**</span></span>](iscardtypeconv.md)
</dt> <dt>

[<span data-ttu-id="dd2c2-155">Smartcard-Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="dd2c2-155">Smart Card Return Values</span></span>](authentication-return-values.md)
</dt> </dl>

 

 
