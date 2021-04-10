---
description: Erstellt ein typisches C/C++-Bytearray.
ms.assetid: 915e8cca-2a0f-409e-a6df-54fa73bdc305
title: 'Iscardtypekonv:: deatebytearray-Methode (scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.CreateByteArray
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: ae253af1b24433987baf66364519a3761f7e0365
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131728"
---
# <a name="iscardtypeconvcreatebytearray-method"></a><span data-ttu-id="99918-103">Iscardtypekonv:: up-Bytearray-Methode</span><span class="sxs-lookup"><span data-stu-id="99918-103">ISCardTypeConv::CreateByteArray method</span></span>

<span data-ttu-id="99918-104">\[Die Methode " **kreatebytearray** " ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="99918-104">\[The **CreateByteArray** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="99918-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="99918-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="99918-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="99918-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="99918-107">Die Methode " **kreatebytearray** " erstellt ein typisches C/C++-Bytearray.</span><span class="sxs-lookup"><span data-stu-id="99918-107">The **CreateByteArray** method creates a typical C/C++ byte array.</span></span>

## <a name="syntax"></a><span data-ttu-id="99918-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="99918-108">Syntax</span></span>


```C++
HRESULT CreateByteArray(
  [in]  DWORD  dwAllocSize,
  [out] LPBYTE *ppbyArray
);
```



## <a name="parameters"></a><span data-ttu-id="99918-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="99918-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99918-110">*dwallocsize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="99918-110">*dwAllocSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99918-111">Größe (in Bytes) des Arbeitsspeichers, der für das Array zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="99918-111">Size (in bytes) of the memory to be allocated for the array.</span></span>

</dd> <dt>

<span data-ttu-id="99918-112">*ppbyarray* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="99918-112">*ppbyArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="99918-113">Zeiger auf das Bytearray, das zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="99918-113">Pointer to the byte array to be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99918-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="99918-114">Return value</span></span>

<span data-ttu-id="99918-115">Die-Methode gibt einen der folgenden möglichen Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="99918-115">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="99918-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="99918-116">Return code</span></span>                                                                                   | <span data-ttu-id="99918-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="99918-117">Description</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="99918-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="99918-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="99918-119">Der Arbeitsspeicher wurde erfolgreich zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="99918-119">Memory allocated successfully.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="99918-120"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="99918-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="99918-121">Bei einem oder mehreren Parametern, die an die Funktion weitergegeben wurden, ist ein Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="99918-121">There is something wrong with one or more of the parameters passed into the function.</span></span><br/> |
| <dl> <span data-ttu-id="99918-122"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="99918-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="99918-123">Nicht genügend freier Arbeitsspeicher, um die Anforderung zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="99918-123">Not enough free memory to satisfy request.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="99918-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="99918-124">Remarks</span></span>

<span data-ttu-id="99918-125">Um einen universellen Puffer von Bytes zu erstellen, die einem **IStream** -Objekt ([**ibytebuffer**](ibytebuffer.md)) zugeordnet sind, rufen Sie " [**kreatebytebuffer**](iscardtypeconv-createbytebuffer.md)" auf.</span><span class="sxs-lookup"><span data-stu-id="99918-125">To create a universal buffer of bytes mapped into an **IStream** ([**IByteBuffer**](ibytebuffer.md)) object, call [**CreateByteBuffer**](iscardtypeconv-createbytebuffer.md).</span></span>

<span data-ttu-id="99918-126">Zum Erstellen eines Automation SafeArray mit nicht signierten Zeichen (Bytes) rufen Sie " [**kreatesafearray**](iscardtypeconv-createsafearray.md)" auf.</span><span class="sxs-lookup"><span data-stu-id="99918-126">To create an Automation SAFEARRAY of unsigned characters (bytes), call [**CreateSafeArray**](iscardtypeconv-createsafearray.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="99918-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="99918-127">Requirements</span></span>



| <span data-ttu-id="99918-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="99918-128">Requirement</span></span> | <span data-ttu-id="99918-129">Wert</span><span class="sxs-lookup"><span data-stu-id="99918-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="99918-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="99918-130">Minimum supported client</span></span><br/> | <span data-ttu-id="99918-131">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="99918-131">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="99918-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="99918-132">Minimum supported server</span></span><br/> | <span data-ttu-id="99918-133">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="99918-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="99918-134">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="99918-134">End of client support</span></span><br/>    | <span data-ttu-id="99918-135">Windows XP</span><span class="sxs-lookup"><span data-stu-id="99918-135">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="99918-136">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="99918-136">End of server support</span></span><br/>    | <span data-ttu-id="99918-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="99918-137">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="99918-138">Header</span><span class="sxs-lookup"><span data-stu-id="99918-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="99918-139"><dt>"Scarddat. h"</dt></span><span class="sxs-lookup"><span data-stu-id="99918-139"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="99918-140">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="99918-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="99918-141"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="99918-141"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="99918-142">DLL</span><span class="sxs-lookup"><span data-stu-id="99918-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="99918-143"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99918-143"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="99918-144">IID</span><span class="sxs-lookup"><span data-stu-id="99918-144">IID</span></span><br/>                      | <span data-ttu-id="99918-145">IID \_ iscardtypec ist als 53b6aa63-3F 56-11D0-916b-00aa00c18068 definiert.</span><span class="sxs-lookup"><span data-stu-id="99918-145">IID\_ISCardTypeConv is defined as 53B6AA63-3F56-11D0-916B-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="99918-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="99918-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99918-147">**Iscardtypeconfiguration**</span><span class="sxs-lookup"><span data-stu-id="99918-147">**ISCardTypeConv**</span></span>](iscardtypeconv.md)
</dt> <dt>

[<span data-ttu-id="99918-148">Smartcard-Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="99918-148">Smart Card Return Values</span></span>](authentication-return-values.md)
</dt> <dt>

[<span data-ttu-id="99918-149">**"Kreatebytebuffer"**</span><span class="sxs-lookup"><span data-stu-id="99918-149">**CreateByteBuffer**</span></span>](iscardtypeconv-createbytebuffer.md)
</dt> <dt>

[<span data-ttu-id="99918-150">**"Anatesafearray"**</span><span class="sxs-lookup"><span data-stu-id="99918-150">**CreateSafeArray**</span></span>](iscardtypeconv-createsafearray.md)
</dt> </dl>

 

 
