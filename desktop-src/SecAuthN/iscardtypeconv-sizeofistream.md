---
description: Bestimmt die Größe (in Bytes) der IStream-com-Schnittstelle.
ms.assetid: 8c2f081d-cc41-409e-a868-bcf834e1f128
title: 'Iscardtypekonv:: sizeofstream-Methode (scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.SizeOfIStream
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 603a01dc6cb4727d59a7fb82c3270c08a495f021
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359109"
---
# <a name="iscardtypeconvsizeofistream-method"></a><span data-ttu-id="6917d-103">Iscardtypekonv:: sizeofstream-Methode</span><span class="sxs-lookup"><span data-stu-id="6917d-103">ISCardTypeConv::SizeOfIStream method</span></span>

<span data-ttu-id="6917d-104">\[Die **sizeofstream** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="6917d-104">\[The **SizeOfIStream** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6917d-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6917d-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="6917d-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="6917d-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="6917d-107">Die **sizeofstream** -Methode bestimmt die Größe der **IStream** -com-Schnittstelle in Byte.</span><span class="sxs-lookup"><span data-stu-id="6917d-107">The **SizeOfIStream** method determines the size, in bytes, of the **IStream** COM interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="6917d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="6917d-108">Syntax</span></span>


```C++
HRESULT SizeOfIStream(
  [in]  LPSTREAM       pStrm,
  [out] ULARGE_INTEGER *puliSize
);
```



## <a name="parameters"></a><span data-ttu-id="6917d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="6917d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6917d-110">*pstraum* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6917d-110">*pStrm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6917d-111">Ein Zeiger auf die **IStream** -com-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="6917d-111">A pointer to the **IStream** COM interface.</span></span>

</dd> <dt>

<span data-ttu-id="6917d-112">*pulisize* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6917d-112">*puliSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6917d-113">Ein Zeiger auf die große ganze Zahl ohne Vorzeichen, die den gesamten 64-Bit-sizeof-Wert der **IStream** -com-Schnittstelle enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="6917d-113">A pointer to the unsigned large integer that can hold the entire 64-bit sizeof value of the **IStream** COM interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6917d-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6917d-114">Return value</span></span>

<span data-ttu-id="6917d-115">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="6917d-115">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="6917d-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="6917d-116">Return code</span></span>                                                                                  | <span data-ttu-id="6917d-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6917d-117">Description</span></span>                                                                                             |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6917d-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6917d-118"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="6917d-119">Die Funktion war erfolgreich, und " *\* pulisize* " ist die Größe (in Bytes) der IStream-com-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="6917d-119">The function succeeded and *\*puliSize* is the size, in bytes, of the IStream COM interface.</span></span><br/> |
| <dl> <span data-ttu-id="6917d-120"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="6917d-120"><dt>**E\_FAIL**</dt></span></span> </dl>       | <span data-ttu-id="6917d-121">Ein nicht spezifizierter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="6917d-121">Unspecified failure occurred.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="6917d-122"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="6917d-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="6917d-123">Der " *pulisize* "-Parameter ist falsch.</span><span class="sxs-lookup"><span data-stu-id="6917d-123">The *puliSize* parameter is incorrect.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="6917d-124"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="6917d-124"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="6917d-125">Der *pstrinm* -Parameter ist falsch.</span><span class="sxs-lookup"><span data-stu-id="6917d-125">The *pStrm* parameter is incorrect.</span></span><br/>                                                          |
| <dl> <span data-ttu-id="6917d-126"><dt>**E \_ unerwartet**</dt></span><span class="sxs-lookup"><span data-stu-id="6917d-126"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="6917d-127">Unerwarteter Fehler.</span><span class="sxs-lookup"><span data-stu-id="6917d-127">Unexpected error occurred.</span></span><br/>                                                                   |



 

## <a name="requirements"></a><span data-ttu-id="6917d-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6917d-128">Requirements</span></span>



| <span data-ttu-id="6917d-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6917d-129">Requirement</span></span> | <span data-ttu-id="6917d-130">Wert</span><span class="sxs-lookup"><span data-stu-id="6917d-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6917d-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6917d-131">Minimum supported client</span></span><br/> | <span data-ttu-id="6917d-132">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6917d-132">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="6917d-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6917d-133">Minimum supported server</span></span><br/> | <span data-ttu-id="6917d-134">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6917d-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6917d-135">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="6917d-135">End of client support</span></span><br/>    | <span data-ttu-id="6917d-136">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6917d-136">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="6917d-137">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="6917d-137">End of server support</span></span><br/>    | <span data-ttu-id="6917d-138">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6917d-138">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="6917d-139">Header</span><span class="sxs-lookup"><span data-stu-id="6917d-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="6917d-140"><dt>"Scarddat. h"</dt></span><span class="sxs-lookup"><span data-stu-id="6917d-140"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="6917d-141">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="6917d-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="6917d-142"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6917d-142"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6917d-143">DLL</span><span class="sxs-lookup"><span data-stu-id="6917d-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6917d-144"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6917d-144"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="6917d-145">IID</span><span class="sxs-lookup"><span data-stu-id="6917d-145">IID</span></span><br/>                      | <span data-ttu-id="6917d-146">IID \_ iscardtypec ist als 53b6aa63-3F 56-11D0-916b-00aa00c18068 definiert.</span><span class="sxs-lookup"><span data-stu-id="6917d-146">IID\_ISCardTypeConv is defined as 53B6AA63-3F56-11D0-916B-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="6917d-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6917d-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6917d-148">**Iscardtypeconfiguration**</span><span class="sxs-lookup"><span data-stu-id="6917d-148">**ISCardTypeConv**</span></span>](iscardtypeconv.md)
</dt> <dt>

[<span data-ttu-id="6917d-149">Smartcard-Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="6917d-149">Smart Card Return Values</span></span>](authentication-return-values.md)
</dt> </dl>

 

 
