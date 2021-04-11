---
description: Konvertiert einen universellen Puffer von Bytes (IStream-Objekt) in ein typisches C/C++-Bytearray.
ms.assetid: f5b14096-d848-4de9-a5c3-bb60af9044a2
title: 'Iscardtypekonv:: convertbytebufferdebytearray-Methode (scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.ConvertByteBufferToByteArray
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 7eed6758373aebf08863669b5b81909fca1c0840
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217460"
---
# <a name="iscardtypeconvconvertbytebuffertobytearray-method"></a><span data-ttu-id="f08c8-103">Iscardtypekonv:: convertbytebufferdebytearray-Methode</span><span class="sxs-lookup"><span data-stu-id="f08c8-103">ISCardTypeConv::ConvertByteBufferToByteArray method</span></span>

<span data-ttu-id="f08c8-104">\[Die **convertbytebuffertobytearray** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="f08c8-104">\[The **ConvertByteBufferToByteArray** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f08c8-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f08c8-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f08c8-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="f08c8-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="f08c8-107">Die **convertbytebufferesbytearray** -Methode konvertiert einen universellen Puffer von Bytes (**IStream** -Objekt) in ein typisches C/C++-Bytearray.</span><span class="sxs-lookup"><span data-stu-id="f08c8-107">The **ConvertByteBufferToByteArray** method converts a universal buffer of bytes (**IStream** object) into a typical C/C++ byte array.</span></span>

## <a name="syntax"></a><span data-ttu-id="f08c8-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f08c8-108">Syntax</span></span>


```C++
HRESULT ConvertByteBufferToByteArray(
  [in]  LPBYTEBUFFER pbyBuffer,
  [out] LPBYTEARRAY  *ppArray
);
```



## <a name="parameters"></a><span data-ttu-id="f08c8-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="f08c8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f08c8-110">*pbybuffer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f08c8-110">*pbyBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f08c8-111">Zeiger auf das **IStream** -Objekt, das konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f08c8-111">Pointer to the **IStream** object to be converted.</span></span>

</dd> <dt>

<span data-ttu-id="f08c8-112">*p-Ray* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f08c8-112">*ppArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f08c8-113">Zeiger auf das Bytearray, das zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="f08c8-113">Pointer to the array of bytes to be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f08c8-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f08c8-114">Return value</span></span>

<span data-ttu-id="f08c8-115">Die-Methode gibt einen der folgenden möglichen Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="f08c8-115">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="f08c8-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="f08c8-116">Return code</span></span>                                                                                   | <span data-ttu-id="f08c8-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f08c8-117">Description</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f08c8-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f08c8-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="f08c8-119">Der Arbeitsspeicher wurde erfolgreich zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="f08c8-119">Memory allocated successfully.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="f08c8-120"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="f08c8-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="f08c8-121">Bei einem oder mehreren Parametern, die an die Funktion weitergegeben wurden, ist ein Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="f08c8-121">There is something wrong with one or more of the parameters passed into the function.</span></span><br/> |
| <dl> <span data-ttu-id="f08c8-122"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="f08c8-122"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="f08c8-123">Ein Parameter vom Zeigertyp war falsch.</span><span class="sxs-lookup"><span data-stu-id="f08c8-123">A parameter of pointer type was incorrect.</span></span><br/>                                            |
| <dl> <span data-ttu-id="f08c8-124"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="f08c8-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="f08c8-125">Nicht genügend freier Arbeitsspeicher, um die Anforderung zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="f08c8-125">Not enough free memory to satisfy request.</span></span><br/>                                            |



 

## <a name="requirements"></a><span data-ttu-id="f08c8-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f08c8-126">Requirements</span></span>



| <span data-ttu-id="f08c8-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f08c8-127">Requirement</span></span> | <span data-ttu-id="f08c8-128">Wert</span><span class="sxs-lookup"><span data-stu-id="f08c8-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f08c8-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f08c8-129">Minimum supported client</span></span><br/> | <span data-ttu-id="f08c8-130">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f08c8-130">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f08c8-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f08c8-131">Minimum supported server</span></span><br/> | <span data-ttu-id="f08c8-132">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f08c8-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f08c8-133">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="f08c8-133">End of client support</span></span><br/>    | <span data-ttu-id="f08c8-134">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f08c8-134">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="f08c8-135">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="f08c8-135">End of server support</span></span><br/>    | <span data-ttu-id="f08c8-136">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f08c8-136">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="f08c8-137">Header</span><span class="sxs-lookup"><span data-stu-id="f08c8-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="f08c8-138"><dt>"Scarddat. h"</dt></span><span class="sxs-lookup"><span data-stu-id="f08c8-138"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="f08c8-139">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="f08c8-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="f08c8-140"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f08c8-140"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f08c8-141">DLL</span><span class="sxs-lookup"><span data-stu-id="f08c8-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f08c8-142"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f08c8-142"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="f08c8-143">IID</span><span class="sxs-lookup"><span data-stu-id="f08c8-143">IID</span></span><br/>                      | <span data-ttu-id="f08c8-144">IID \_ iscardtypec ist als 53b6aa63-3F 56-11D0-916b-00aa00c18068 definiert.</span><span class="sxs-lookup"><span data-stu-id="f08c8-144">IID\_ISCardTypeConv is defined as 53B6AA63-3F56-11D0-916B-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="f08c8-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f08c8-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f08c8-146">**Iscardtypeconfiguration**</span><span class="sxs-lookup"><span data-stu-id="f08c8-146">**ISCardTypeConv**</span></span>](iscardtypeconv.md)
</dt> <dt>

[<span data-ttu-id="f08c8-147">Smartcard-Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="f08c8-147">Smart Card Return Values</span></span>](authentication-return-values.md)
</dt> </dl>

 

 
