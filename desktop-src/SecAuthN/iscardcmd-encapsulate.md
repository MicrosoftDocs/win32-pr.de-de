---
description: Die Kapselungsmethode kapselt die angegebene Application Protocol Data Unit (APDU) für die Übertragung an eine Smartcard in ein anderes Befehls-APDU.
ms.assetid: dfffad09-046b-46cb-b6fd-286a4bbf1066
title: 'Iscardcmd:: Kapseln-Methode (scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.Encapsulate
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: cd671a11edd9977695eeaf858e38f962b3dd0962
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350011"
---
# <a name="iscardcmdencapsulate-method"></a><span data-ttu-id="9f074-103">Iscardcmd:: Kapseln-Methode</span><span class="sxs-lookup"><span data-stu-id="9f074-103">ISCardCmd::Encapsulate method</span></span>

<span data-ttu-id="9f074-104">\[Die **Kapseln** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="9f074-104">\[The **Encapsulate** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="9f074-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9f074-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="9f074-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="9f074-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="9f074-107">Die **Kapselungsmethode** kapselt die angegebene [*Application Protocol Data Unit*](../secgloss/a-gly.md) (APDU) für die Übertragung an eine [*Smartcard*](../secgloss/s-gly.md)in ein anderes Befehls-APDU.</span><span class="sxs-lookup"><span data-stu-id="9f074-107">The **Encapsulate** method encapsulates the given command [*application protocol data unit*](../secgloss/a-gly.md) (APDU) into another command APDU for transmission to a [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9f074-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="9f074-108">Syntax</span></span>


```C++
HRESULT Encapsulate(
  [in] LPBYTEBUFFER  pApdu,
  [in] ISO_APDU_TYPE ApduType
);
```



## <a name="parameters"></a><span data-ttu-id="9f074-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="9f074-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f074-110">*papdu* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9f074-110">*pApdu* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f074-111">Zeiger auf das zu gekapselte APDU.</span><span class="sxs-lookup"><span data-stu-id="9f074-111">Pointer to the APDU to be encapsulated.</span></span>

</dd> <dt>

<span data-ttu-id="9f074-112">*Apdutype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9f074-112">*ApduType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f074-113">ISO 7816-4-Fall für [*T = 0*](../secgloss/t-gly.md) -Übertragungen.</span><span class="sxs-lookup"><span data-stu-id="9f074-113">ISO 7816-4 case for [*T=0*](../secgloss/t-gly.md) transmissions.</span></span>

<dl><span id="ISO_CASE_1"></span><span id="iso_case_1"></span><dt>

<span data-ttu-id="9f074-114">**ISO- \_ Fall \_ 1**</span><span class="sxs-lookup"><span data-stu-id="9f074-114">**ISO\_CASE\_1**</span></span>
</dt><span id="ISO_CASE_2"></span><span id="iso_case_2"></span><dt>

<span data-ttu-id="9f074-115">**ISO- \_ Fall \_ 2**</span><span class="sxs-lookup"><span data-stu-id="9f074-115">**ISO\_CASE\_2**</span></span>
</dt><span id="ISO_CASE_3"></span><span id="iso_case_3"></span><dt>

<span data-ttu-id="9f074-116">**ISO- \_ Fall \_ 3**</span><span class="sxs-lookup"><span data-stu-id="9f074-116">**ISO\_CASE\_3**</span></span>
</dt><span id="ISO_CASE_4"></span><span id="iso_case_4"></span><dt>

<span data-ttu-id="9f074-117">**ISO- \_ Fall \_ 4**</span><span class="sxs-lookup"><span data-stu-id="9f074-117">**ISO\_CASE\_4**</span></span>
</dt> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f074-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9f074-118">Return value</span></span>

<span data-ttu-id="9f074-119">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="9f074-119">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="9f074-120">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="9f074-120">Return code</span></span>                                                                                   | <span data-ttu-id="9f074-121">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9f074-121">Description</span></span>                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="9f074-122"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9f074-122"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="9f074-123">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="9f074-123">Operation completed successfully.</span></span><br/>    |
| <dl> <span data-ttu-id="9f074-124"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="9f074-124"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="9f074-125">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="9f074-125">Invalid parameter.</span></span><br/>                   |
| <dl> <span data-ttu-id="9f074-126"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="9f074-126"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="9f074-127">Ein fehlerhafter Zeiger wurde in *papdu* übermittelt.</span><span class="sxs-lookup"><span data-stu-id="9f074-127">A bad pointer was passed in *pApdu*.</span></span><br/> |
| <dl> <span data-ttu-id="9f074-128"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="9f074-128"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="9f074-129">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="9f074-129">Out of memory.</span></span><br/>                       |



 

## <a name="remarks"></a><span data-ttu-id="9f074-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9f074-130">Remarks</span></span>

<span data-ttu-id="9f074-131">Zum Erstellen eines Befehls-APDU rufe Sie [**buildcmd**](iscardcmd-buildcmd.md)auf.</span><span class="sxs-lookup"><span data-stu-id="9f074-131">To build a command APDU, call [**BuildCmd**](iscardcmd-buildcmd.md).</span></span>

<span data-ttu-id="9f074-132">Eine Liste aller Methoden, die von dieser Schnittstelle bereitgestellt werden, finden Sie unter [**iscardcmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="9f074-132">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="9f074-133">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="9f074-133">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="9f074-134">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="9f074-134">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="9f074-135">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9f074-135">Examples</span></span>

<span data-ttu-id="9f074-136">Im folgenden Beispiel wird gezeigt, wie Sie einen Befehls-APDU Kapseln.</span><span class="sxs-lookup"><span data-stu-id="9f074-136">The following example shows how to encapsulate a command APDU.</span></span> <span data-ttu-id="9f074-137">Im Beispiel wird davon ausgegangen, dass pibyteapdu ein gültiger Zeiger auf eine Instanz der [**ibytebuffer**](ibytebuffer.md) -Schnittstelle ist.</span><span class="sxs-lookup"><span data-stu-id="9f074-137">The example assumes that pIByteApdu is a valid pointer to an instance of the [**IByteBuffer**](ibytebuffer.md) interface.</span></span>


```C++
HRESULT    hr;

// pIByteApdu is a pointer to an instance of IByteBuffer.
// Encapsulate the APDU.
hr = pISCardCmd->Encapsulate(pIByteApdu, ISO_CASE_1);
if (FAILED(hr)) 
{
    printf("Failed Encapsulate.\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="9f074-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9f074-138">Requirements</span></span>



| <span data-ttu-id="9f074-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9f074-139">Requirement</span></span> | <span data-ttu-id="9f074-140">Wert</span><span class="sxs-lookup"><span data-stu-id="9f074-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9f074-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9f074-141">Minimum supported client</span></span><br/> | <span data-ttu-id="9f074-142">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9f074-142">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="9f074-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9f074-143">Minimum supported server</span></span><br/> | <span data-ttu-id="9f074-144">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9f074-144">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9f074-145">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="9f074-145">End of client support</span></span><br/>    | <span data-ttu-id="9f074-146">Windows XP</span><span class="sxs-lookup"><span data-stu-id="9f074-146">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="9f074-147">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="9f074-147">End of server support</span></span><br/>    | <span data-ttu-id="9f074-148">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9f074-148">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="9f074-149">Header</span><span class="sxs-lookup"><span data-stu-id="9f074-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f074-150"><dt>"Scarddat. h"</dt></span><span class="sxs-lookup"><span data-stu-id="9f074-150"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="9f074-151">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="9f074-151">Type library</span></span><br/>             | <dl> <span data-ttu-id="9f074-152"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9f074-152"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9f074-153">DLL</span><span class="sxs-lookup"><span data-stu-id="9f074-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f074-154"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f074-154"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="9f074-155">IID</span><span class="sxs-lookup"><span data-stu-id="9f074-155">IID</span></span><br/>                      | <span data-ttu-id="9f074-156">IID \_ iscardcmd ist als D5778AE3-43DE-11D0-9171-00AA00C18068 definiert.</span><span class="sxs-lookup"><span data-stu-id="9f074-156">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="9f074-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9f074-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f074-158">**Buildcmd**</span><span class="sxs-lookup"><span data-stu-id="9f074-158">**BuildCmd**</span></span>](iscardcmd-buildcmd.md)
</dt> <dt>

[<span data-ttu-id="9f074-159">**Iscardcmd**</span><span class="sxs-lookup"><span data-stu-id="9f074-159">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
