---
description: Erstellt einen universellen Puffer von Bytes, der einem IStream-Objekt (ibytebuffer) zugeordnet ist.
ms.assetid: 8015c7e8-2cbb-4ba8-9bd0-2f84751840f1
title: 'Iscardtypekonv:: up-ByteBuffer-Methode (scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.CreateByteBuffer
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: ab69c8061d2e2740e652e29b2fe6407574fe7076
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042323"
---
# <a name="iscardtypeconvcreatebytebuffer-method"></a><span data-ttu-id="d05bd-103">Iscardtypekonv:: deatebytebuffer-Methode</span><span class="sxs-lookup"><span data-stu-id="d05bd-103">ISCardTypeConv::CreateByteBuffer method</span></span>

<span data-ttu-id="d05bd-104">\[Die Methode " **kreatebytebuffer** " ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="d05bd-104">\[The **CreateByteBuffer** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d05bd-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d05bd-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="d05bd-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="d05bd-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="d05bd-107">Die **Methode** "-Methode" erstellt einen universellen Puffer von Bytes, die einem **IStream** -Objekt ([**ibytebuffer**](ibytebuffer.md)) zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="d05bd-107">The **CreateByteBuffer** method creates a universal buffer of bytes mapped into an **IStream** ([**IByteBuffer**](ibytebuffer.md)) object.</span></span>

<span data-ttu-id="d05bd-108">Der erstellte Byte Puffer ist ein Datenstrom, der über einem Speicherblock zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d05bd-108">The byte buffer created is a stream mapped over a memory block.</span></span> <span data-ttu-id="d05bd-109">Verwenden Sie die von der **IStream** -Schnittstelle bereitgestellten Methoden, um auf den Puffer zuzugreifen oder ihn zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="d05bd-109">To access or manage the buffer, use the methods provided by the **IStream** interface.</span></span> <span data-ttu-id="d05bd-110">Ein eindeutiges Feature zu dieser Array Implementierung besteht darin, dass beim aufruft der **IStream:: Release** -Methode der zugrunde liegende Arbeitsspeicher für Sie freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d05bd-110">A unique feature about this array implementation is that when you call the **IStream::Release** method, the underlying memory will be released for you.</span></span>

## <a name="syntax"></a><span data-ttu-id="d05bd-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="d05bd-111">Syntax</span></span>


```C++
HRESULT CreateByteBuffer(
  [in]  DWORD        dwAllocSize,
  [out] LPBYTEBUFFER *ppbyBuff
);
```



## <a name="parameters"></a><span data-ttu-id="d05bd-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="d05bd-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d05bd-113">*dwallocsize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d05bd-113">*dwAllocSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d05bd-114">Größe des Arbeitsspeichers in Bytes, der für das Array zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d05bd-114">Size in bytes of the memory to be allocated for the array.</span></span>

</dd> <dt>

<span data-ttu-id="d05bd-115">*ppbybuff* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d05bd-115">*ppbyBuff* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d05bd-116">Zeiger auf das IStream-Objekt, das zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="d05bd-116">Pointer to the IStream object to be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d05bd-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d05bd-117">Return value</span></span>

<span data-ttu-id="d05bd-118">Folgende Rückgabewerte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="d05bd-118">The possible return values are the following:</span></span>



| <span data-ttu-id="d05bd-119">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="d05bd-119">Return code</span></span>                                                                                   | <span data-ttu-id="d05bd-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d05bd-120">Description</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d05bd-121"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d05bd-121"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="d05bd-122">Der Arbeitsspeicher wurde erfolgreich zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="d05bd-122">Memory allocated successfully.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="d05bd-123"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="d05bd-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="d05bd-124">Bei einem oder mehreren Parametern, die an die Funktion weitergegeben wurden, ist ein Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="d05bd-124">There is something wrong with one or more of the parameters passed into the function.</span></span><br/> |
| <dl> <span data-ttu-id="d05bd-125"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="d05bd-125"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="d05bd-126">Nicht genügend freier Arbeitsspeicher, um die Anforderung zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="d05bd-126">Not enough free memory to satisfy request.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="d05bd-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d05bd-127">Remarks</span></span>

<span data-ttu-id="d05bd-128">Der zugewiesene Arbeitsspeicher ist beweglicher.</span><span class="sxs-lookup"><span data-stu-id="d05bd-128">Memory allocated is movable.</span></span> <span data-ttu-id="d05bd-129">Verwenden Sie die **IStream:: Release** -Methode, um den Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="d05bd-129">Use the **IStream::Release** method to free the memory.</span></span>

<span data-ttu-id="d05bd-130">Um ein typisches C/C++-Bytearray zu erstellen, rufen Sie " [**kreatebytearray**](iscardtypeconv-createbytearray.md)" auf.</span><span class="sxs-lookup"><span data-stu-id="d05bd-130">To create a typical C/C++ byte array, call [**CreateByteArray**](iscardtypeconv-createbytearray.md).</span></span>

<span data-ttu-id="d05bd-131">Zum Erstellen eines Automation SafeArray mit nicht signierten Zeichen (Bytes) rufen Sie " [**kreatesafearray**](iscardtypeconv-createsafearray.md)" auf.</span><span class="sxs-lookup"><span data-stu-id="d05bd-131">To create an Automation SAFEARRAY of unsigned characters (bytes), call [**CreateSafeArray**](iscardtypeconv-createsafearray.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d05bd-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d05bd-132">Requirements</span></span>



| <span data-ttu-id="d05bd-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d05bd-133">Requirement</span></span> | <span data-ttu-id="d05bd-134">Wert</span><span class="sxs-lookup"><span data-stu-id="d05bd-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d05bd-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d05bd-135">Minimum supported client</span></span><br/> | <span data-ttu-id="d05bd-136">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d05bd-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d05bd-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d05bd-137">Minimum supported server</span></span><br/> | <span data-ttu-id="d05bd-138">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d05bd-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d05bd-139">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="d05bd-139">End of client support</span></span><br/>    | <span data-ttu-id="d05bd-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="d05bd-140">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="d05bd-141">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="d05bd-141">End of server support</span></span><br/>    | <span data-ttu-id="d05bd-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d05bd-142">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="d05bd-143">Header</span><span class="sxs-lookup"><span data-stu-id="d05bd-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="d05bd-144"><dt>"Scarddat. h"</dt></span><span class="sxs-lookup"><span data-stu-id="d05bd-144"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="d05bd-145">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="d05bd-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="d05bd-146"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d05bd-146"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d05bd-147">DLL</span><span class="sxs-lookup"><span data-stu-id="d05bd-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d05bd-148"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d05bd-148"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d05bd-149">IID</span><span class="sxs-lookup"><span data-stu-id="d05bd-149">IID</span></span><br/>                      | <span data-ttu-id="d05bd-150">IID \_ iscardtypec ist als 53b6aa63-3F 56-11D0-916b-00aa00c18068 definiert.</span><span class="sxs-lookup"><span data-stu-id="d05bd-150">IID\_ISCardTypeConv is defined as 53B6AA63-3F56-11D0-916B-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="d05bd-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d05bd-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d05bd-152">**Iscardtypeconfiguration**</span><span class="sxs-lookup"><span data-stu-id="d05bd-152">**ISCardTypeConv**</span></span>](iscardtypeconv.md)
</dt> <dt>

[<span data-ttu-id="d05bd-153">Smartcard-Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="d05bd-153">Smart Card Return Values</span></span>](authentication-return-values.md)
</dt> <dt>

[<span data-ttu-id="d05bd-154">**"Kreatebytearray"**</span><span class="sxs-lookup"><span data-stu-id="d05bd-154">**CreateByteArray**</span></span>](iscardtypeconv-createbytearray.md)
</dt> <dt>

[<span data-ttu-id="d05bd-155">**"Anatesafearray"**</span><span class="sxs-lookup"><span data-stu-id="d05bd-155">**CreateSafeArray**</span></span>](iscardtypeconv-createsafearray.md)
</dt> </dl>

 

 
