---
description: Ruft eine ATR-Zeichenfolge der Smartcard ab.
ms.assetid: 2021bd0c-6ef8-4679-be6c-9a9fd33d9fd6
title: 'Iscard:: get_Atr-Methode (scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.get_Atr
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 4f2a5688ee85318003ea366bbce614e8250a131a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373271"
---
# <a name="iscardget_atr-method"></a><span data-ttu-id="eaa68-103">Iscard:: get- \_ ATR-Methode</span><span class="sxs-lookup"><span data-stu-id="eaa68-103">ISCard::get\_Atr method</span></span>

<span data-ttu-id="eaa68-104">\[Die **get \_ ATR** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="eaa68-104">\[The **get\_Atr** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="eaa68-105">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="eaa68-105">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="eaa68-106">Die **get \_ ATR** -Methode ruft eine [*ATR-Zeichenfolge*](../secgloss/a-gly.md) der [*Smartcard*](../secgloss/s-gly.md)ab.</span><span class="sxs-lookup"><span data-stu-id="eaa68-106">The **get\_Atr** method retrieves an [*ATR string*](../secgloss/a-gly.md) of the [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="eaa68-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="eaa68-107">Syntax</span></span>


```C++
HRESULT get_Atr(
  [out] LPBYTEBUFFER *ppAtr
);
```



## <a name="parameters"></a><span data-ttu-id="eaa68-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="eaa68-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eaa68-109">*ppatr* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="eaa68-109">*ppAtr* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eaa68-110">Zeiger auf einen Byte Puffer in der Form eines [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) , der die ATR-Zeichenfolge bei der Rückgabe enthält.</span><span class="sxs-lookup"><span data-stu-id="eaa68-110">Pointer to a byte buffer in the form of an [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) that will contain the ATR string on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eaa68-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="eaa68-111">Return value</span></span>

<span data-ttu-id="eaa68-112">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="eaa68-112">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="eaa68-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="eaa68-113">Return code</span></span>                                                                                   | <span data-ttu-id="eaa68-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eaa68-114">Description</span></span>                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="eaa68-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="eaa68-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="eaa68-116">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="eaa68-116">Operation completed successfully.</span></span><br/>             |
| <dl> <span data-ttu-id="eaa68-117"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="eaa68-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="eaa68-118">Der *ppatr* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="eaa68-118">The *ppAtr* parameter is not valid.</span></span><br/>           |
| <dl> <span data-ttu-id="eaa68-119"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="eaa68-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="eaa68-120">Ein fehlerhafter Zeiger wurde in *ppatr* übermittelt.</span><span class="sxs-lookup"><span data-stu-id="eaa68-120">A bad pointer was passed in *ppAtr*.</span></span><br/>          |
| <dl> <span data-ttu-id="eaa68-121"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="eaa68-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="eaa68-122">Der Arbeitsspeicher zum erfüllen der Anforderung ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="eaa68-122">Memory to satisfy the request is unavailable.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="eaa68-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eaa68-123">Remarks</span></span>

<span data-ttu-id="eaa68-124">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="eaa68-124">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="eaa68-125">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="eaa68-125">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="eaa68-126">Beispiele</span><span class="sxs-lookup"><span data-stu-id="eaa68-126">Examples</span></span>

<span data-ttu-id="eaa68-127">Das folgende Beispiel zeigt, wie Sie die ATR-Zeichenfolge von der Smartcard abrufen.</span><span class="sxs-lookup"><span data-stu-id="eaa68-127">The following example shows retrieving the ATR string from the smart card.</span></span>


```C++
// Retrieve the ATR.
// pISCard is a pointer to a previously instantiated ISCard.
// pAtr is a pointer to a previously instantiated IByteBuffer.
hr = pISCard->get_Atr(&pAtr);
if (FAILED(hr))
{
    printf("Failed get_Atr\n");
    // Take other error handling action.
}
// Success, you can now use IByteBuffer::Read to access ATR bytes.
BYTE  byAtr[32];
   long  lBytesRead, i;
   // Read the ATR string into a byte array.
   hr = pAtr->Read(byAtr, 32, &lBytesRead);
   // Use the ATR value. (This example merely displays the bytes.)
   for ( i = 0; i < lBytesRead; i++)
       printf("%c", *(byAtr + i));
   printf("\n");
```



## <a name="requirements"></a><span data-ttu-id="eaa68-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eaa68-128">Requirements</span></span>



| <span data-ttu-id="eaa68-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eaa68-129">Requirement</span></span> | <span data-ttu-id="eaa68-130">Wert</span><span class="sxs-lookup"><span data-stu-id="eaa68-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eaa68-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="eaa68-131">Minimum supported client</span></span><br/> | <span data-ttu-id="eaa68-132">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eaa68-132">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="eaa68-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="eaa68-133">Minimum supported server</span></span><br/> | <span data-ttu-id="eaa68-134">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eaa68-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="eaa68-135">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="eaa68-135">End of client support</span></span><br/>    | <span data-ttu-id="eaa68-136">Windows XP</span><span class="sxs-lookup"><span data-stu-id="eaa68-136">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="eaa68-137">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="eaa68-137">End of server support</span></span><br/>    | <span data-ttu-id="eaa68-138">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="eaa68-138">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="eaa68-139">Header</span><span class="sxs-lookup"><span data-stu-id="eaa68-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="eaa68-140"><dt>"Scardmgr. h"</dt></span><span class="sxs-lookup"><span data-stu-id="eaa68-140"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="eaa68-141">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="eaa68-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="eaa68-142"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="eaa68-142"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="eaa68-143">DLL</span><span class="sxs-lookup"><span data-stu-id="eaa68-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eaa68-144"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eaa68-144"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="eaa68-145">IID</span><span class="sxs-lookup"><span data-stu-id="eaa68-145">IID</span></span><br/>                      | <span data-ttu-id="eaa68-146">IID \_ iscard ist definiert als 1461aac3-6810-11D0-918f -00aa00c18068</span><span class="sxs-lookup"><span data-stu-id="eaa68-146">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="eaa68-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eaa68-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eaa68-148">**\_cardhandle erhalten**</span><span class="sxs-lookup"><span data-stu-id="eaa68-148">**get\_CardHandle**</span></span>](iscard-get-cardhandle.md)
</dt> <dt>

[<span data-ttu-id="eaa68-149">**\_Kontext erhalten**</span><span class="sxs-lookup"><span data-stu-id="eaa68-149">**get\_Context**</span></span>](iscard-get-context.md)
</dt> <dt>

[<span data-ttu-id="eaa68-150">**get- \_ Protokoll**</span><span class="sxs-lookup"><span data-stu-id="eaa68-150">**get\_Protocol**</span></span>](iscard-get-protocol.md)
</dt> <dt>

[<span data-ttu-id="eaa68-151">**\_Status erhalten**</span><span class="sxs-lookup"><span data-stu-id="eaa68-151">**get\_Status**</span></span>](iscard-get-status.md)
</dt> <dt>

[<span data-ttu-id="eaa68-152">**Iscard**</span><span class="sxs-lookup"><span data-stu-id="eaa68-152">**ISCard**</span></span>](iscard.md)
</dt> <dt>

[<span data-ttu-id="eaa68-153">**Ibytebuffer:: Read**</span><span class="sxs-lookup"><span data-stu-id="eaa68-153">**IByteBuffer::Read**</span></span>](ibytebuffer-read.md)
</dt> </dl>

 

 
