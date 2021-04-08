---
description: Konvertiert einen universellen Puffer von Bytes (IStream-Objekt) in ein SAFEARRAY vom Typ Ganzzahl ohne Vorzeichen char (Byte).
ms.assetid: b8d052e8-2f36-42cf-b88c-ace215a2fc68
title: 'Iscardtypekonv:: convertbytebufferdesafearray-Methode (scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.ConvertByteBufferToSafeArray
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: eb6f646df60ab505c41c45bea34fd2d59aa3bb4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757284"
---
# <a name="iscardtypeconvconvertbytebuffertosafearray-method"></a><span data-ttu-id="ebd77-103">Iscardtypekonv:: convertbytebufferdesafearray-Methode</span><span class="sxs-lookup"><span data-stu-id="ebd77-103">ISCardTypeConv::ConvertByteBufferToSafeArray method</span></span>

<span data-ttu-id="ebd77-104">\[Die **convertbytebuffertosafearray** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="ebd77-104">\[The **ConvertByteBufferToSafeArray** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="ebd77-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ebd77-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="ebd77-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="ebd77-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="ebd77-107">Die **convertbytebufferessafearray** -Methode konvertiert einen universellen Puffer von Bytes (**IStream** -Objekt) in ein SAFEARRAY vom Typ Ganzzahl ohne Vorzeichen char (Byte).</span><span class="sxs-lookup"><span data-stu-id="ebd77-107">The **ConvertByteBufferToSafeArray** method converts a universal buffer of bytes (**IStream** object) into a SAFEARRAY of unsigned char (byte).</span></span>

## <a name="syntax"></a><span data-ttu-id="ebd77-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ebd77-108">Syntax</span></span>


```C++
HRESULT ConvertByteBufferToSafeArray(
  [in]  LPBYTEBUFFER pbyBuffer,
  [out] LPSAFEARRAY  *ppbyArray
);
```



## <a name="parameters"></a><span data-ttu-id="ebd77-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ebd77-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebd77-110">*pbybuffer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ebd77-110">*pbyBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebd77-111">Zeiger auf das **IStream** -Objekt, das konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ebd77-111">Pointer to the **IStream** object to be converted.</span></span>

</dd> <dt>

<span data-ttu-id="ebd77-112">*ppbyarray* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ebd77-112">*ppbyArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ebd77-113">Zeiger auf das SafeArray, das zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="ebd77-113">Pointer to the SAFEARRAY to be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebd77-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ebd77-114">Return value</span></span>

<span data-ttu-id="ebd77-115">Die-Methode gibt einen der folgenden möglichen Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="ebd77-115">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="ebd77-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="ebd77-116">Return code</span></span>                                                                                   | <span data-ttu-id="ebd77-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ebd77-117">Description</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ebd77-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ebd77-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="ebd77-119">Der Arbeitsspeicher wurde erfolgreich zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="ebd77-119">Memory allocated successfully.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="ebd77-120"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="ebd77-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="ebd77-121">Bei einem oder mehreren Parametern, die an die Funktion weitergegeben wurden, ist ein Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="ebd77-121">There is something wrong with one or more of the parameters passed into the function.</span></span><br/> |
| <dl> <span data-ttu-id="ebd77-122"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="ebd77-122"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="ebd77-123">Ein Parameter vom Zeigertyp war falsch.</span><span class="sxs-lookup"><span data-stu-id="ebd77-123">A parameter of pointer type was incorrect.</span></span><br/>                                            |
| <dl> <span data-ttu-id="ebd77-124"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="ebd77-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="ebd77-125">Nicht genügend freier Arbeitsspeicher, um die Anforderung zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="ebd77-125">Not enough free memory to satisfy request.</span></span><br/>                                            |



 

## <a name="requirements"></a><span data-ttu-id="ebd77-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ebd77-126">Requirements</span></span>



| <span data-ttu-id="ebd77-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ebd77-127">Requirement</span></span> | <span data-ttu-id="ebd77-128">Wert</span><span class="sxs-lookup"><span data-stu-id="ebd77-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ebd77-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ebd77-129">Minimum supported client</span></span><br/> | <span data-ttu-id="ebd77-130">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ebd77-130">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ebd77-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ebd77-131">Minimum supported server</span></span><br/> | <span data-ttu-id="ebd77-132">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ebd77-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ebd77-133">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="ebd77-133">End of client support</span></span><br/>    | <span data-ttu-id="ebd77-134">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ebd77-134">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="ebd77-135">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="ebd77-135">End of server support</span></span><br/>    | <span data-ttu-id="ebd77-136">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ebd77-136">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="ebd77-137">Header</span><span class="sxs-lookup"><span data-stu-id="ebd77-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="ebd77-138"><dt>"Scarddat. h"</dt></span><span class="sxs-lookup"><span data-stu-id="ebd77-138"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="ebd77-139">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="ebd77-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="ebd77-140"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ebd77-140"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ebd77-141">DLL</span><span class="sxs-lookup"><span data-stu-id="ebd77-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ebd77-142"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ebd77-142"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="ebd77-143">IID</span><span class="sxs-lookup"><span data-stu-id="ebd77-143">IID</span></span><br/>                      | <span data-ttu-id="ebd77-144">IID \_ iscardtypec ist als 53b6aa63-3F 56-11D0-916b-00aa00c18068 definiert.</span><span class="sxs-lookup"><span data-stu-id="ebd77-144">IID\_ISCardTypeConv is defined as 53B6AA63-3F56-11D0-916B-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="ebd77-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ebd77-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebd77-146">**Iscardtypeconfiguration**</span><span class="sxs-lookup"><span data-stu-id="ebd77-146">**ISCardTypeConv**</span></span>](iscardtypeconv.md)
</dt> <dt>

[<span data-ttu-id="ebd77-147">Smartcard-Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="ebd77-147">Smart Card Return Values</span></span>](authentication-return-values.md)
</dt> </dl>

 

 
