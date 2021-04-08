---
description: Die attachbyreader-Methode öffnet die Smartcard im benannten Reader.
ms.assetid: a92f3281-5018-4e90-bfa0-f03eb9373bb1
title: 'Iscard:: attachbyreader-Methode (scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.AttachByReader
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 2607ea2e13be2dcccc3c1b6beebd40c86822d0a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960540"
---
# <a name="iscardattachbyreader-method"></a><span data-ttu-id="74355-103">Iscard:: attachbyreader-Methode</span><span class="sxs-lookup"><span data-stu-id="74355-103">ISCard::AttachByReader method</span></span>

<span data-ttu-id="74355-104">\[Die **attachbyreader** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="74355-104">\[The **AttachByReader** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="74355-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="74355-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="74355-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="74355-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="74355-107">Die **attachbyreader** -Methode öffnet die [*Smartcard*](../secgloss/s-gly.md) im benannten [*Reader*](../secgloss/r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="74355-107">The **AttachByReader** method opens the [*smart card*](../secgloss/s-gly.md) in the named [*reader*](../secgloss/r-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="74355-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="74355-108">Syntax</span></span>


```C++
HRESULT AttachByReader(
  [in] BSTR              bstrReaderName,
  [in] SCARD_SHARE_MODES ShareMode,
  [in] SCARD_PROTOCOLS   PrefProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="74355-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="74355-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74355-110">*bstrinreadername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="74355-110">*bstrReaderName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74355-111">Ein **BSTR** -Wert, der den Namen des smartcardreaders enthält.</span><span class="sxs-lookup"><span data-stu-id="74355-111">A **BSTR** that contains the name of the smart card reader.</span></span>

</dd> <dt>

<span data-ttu-id="74355-112">*Share Mode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="74355-112">*ShareMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74355-113">Der Modus, in dem der Zugriff auf die Smartcard beansprucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="74355-113">Mode in which to claim access to the smart card.</span></span>



| <span data-ttu-id="74355-114">Wert</span><span class="sxs-lookup"><span data-stu-id="74355-114">Value</span></span>                                                                                                                                            | <span data-ttu-id="74355-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="74355-115">Meaning</span></span>                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EXCLUSIVE"></span><span id="exclusive"></span><dl> <span data-ttu-id="74355-116"><dt>**Ausschließliche**</dt></span><span class="sxs-lookup"><span data-stu-id="74355-116"><dt>**EXCLUSIVE**</dt></span></span> </dl> | <span data-ttu-id="74355-117">Diese Verbindung wird von keiner anderen Person mit der Smartcard verwendet.</span><span class="sxs-lookup"><span data-stu-id="74355-117">No one else use this connection to the smart card.</span></span><br/> |
| <span id="SHARED"></span><span id="shared"></span><dl> <span data-ttu-id="74355-118"><dt>**Genu**</dt></span><span class="sxs-lookup"><span data-stu-id="74355-118"><dt>**SHARED**</dt></span></span> </dl>          | <span data-ttu-id="74355-119">Diese Verbindung kann von anderen Anwendungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="74355-119">Other applications can use this connection.</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="74355-120">*Präfetokoll* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="74355-120">*PrefProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74355-121">Bevorzugter Protokoll Wert.</span><span class="sxs-lookup"><span data-stu-id="74355-121">Preferred protocol value.</span></span>

<dl><span id="T0"></span><span id="t0"></span><dt>

<span data-ttu-id="74355-122">**T0**</span><span class="sxs-lookup"><span data-stu-id="74355-122">**T0**</span></span>
</dt><span id="T1"></span><span id="t1"></span><dt>

<span data-ttu-id="74355-123">**T1**</span><span class="sxs-lookup"><span data-stu-id="74355-123">**T1**</span></span>
</dt><span id="RAW"></span><span id="raw"></span><dt>

<span data-ttu-id="74355-124">**RAW**</span><span class="sxs-lookup"><span data-stu-id="74355-124">**RAW**</span></span>
</dt><span id="T0_T1"></span><span id="t0_t1"></span><dt>

<span data-ttu-id="74355-125">**T0 \| T1**</span><span class="sxs-lookup"><span data-stu-id="74355-125">**T0\|T1**</span></span>
</dt> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74355-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="74355-126">Return value</span></span>

<span data-ttu-id="74355-127">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="74355-127">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="74355-128">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="74355-128">Return code</span></span>                                                                                  | <span data-ttu-id="74355-129">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="74355-129">Description</span></span>                                                                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="74355-130"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="74355-130"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="74355-131">Das Öffnen auf der Smartcard im benannten Reader wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="74355-131">Open on the smart card in the named reader has been completed successfully.</span></span><br/>           |
| <dl> <span data-ttu-id="74355-132"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="74355-132"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="74355-133">Bei einem oder mehreren Parametern, die an die Funktion weitergegeben wurden, ist ein Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="74355-133">There is something wrong with one or more of the parameters passed into the function.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="74355-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="74355-134">Remarks</span></span>

<span data-ttu-id="74355-135">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die [*Smartcard*](../secgloss/s-gly.md) zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="74355-135">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="74355-136">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="74355-136">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

<span data-ttu-id="74355-137">Wenn Sie die Verwendung des Readers abgeschlossen haben, geben Sie die Anlage frei, indem Sie die [**iscard::D Etach**](iscard-detach.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="74355-137">When you have finished using the reader, release the attachment by calling the [**ISCard::Detach**](iscard-detach.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="74355-138">Beispiele</span><span class="sxs-lookup"><span data-stu-id="74355-138">Examples</span></span>

<span data-ttu-id="74355-139">Das folgende Beispiel zeigt das Anfügen an eine Smartcard in einem angegebenen Smartcardlesegerät.</span><span class="sxs-lookup"><span data-stu-id="74355-139">The following example shows attaching to a smart card in a specified smart card reader.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <Scardmgr.h>

// The reader name is vendor specific; change as needed.
#define READER_NAME L"Vendor Reader 0"

void main()
{
    BSTR     bstrReader = NULL;
    HRESULT  hr;

    bstrReader = SysAllocString(READER_NAME);
    if (NULL == bstrReader)
    {
        // Error encountered.
        exit(1);
    }

    // Connect to the reader.
    hr = pISCard->AttachByReader(bstrReader, SHARED, T0);
    if (FAILED(hr))
    {
        printf("Failed AttachByReader\n");
        // Take other error handling action.
        // ...
    }

    // Detach reader by calling ISCard::Detach (not shown).
    // ...

    // When done, free BSTR.
    if (NULL != bstrReader)
        SysFreeString(bstrReader);
}
```



## <a name="requirements"></a><span data-ttu-id="74355-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="74355-140">Requirements</span></span>



| <span data-ttu-id="74355-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="74355-141">Requirement</span></span> | <span data-ttu-id="74355-142">Wert</span><span class="sxs-lookup"><span data-stu-id="74355-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="74355-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="74355-143">Minimum supported client</span></span><br/> | <span data-ttu-id="74355-144">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="74355-144">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="74355-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="74355-145">Minimum supported server</span></span><br/> | <span data-ttu-id="74355-146">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="74355-146">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="74355-147">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="74355-147">End of client support</span></span><br/>    | <span data-ttu-id="74355-148">Windows XP</span><span class="sxs-lookup"><span data-stu-id="74355-148">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="74355-149">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="74355-149">End of server support</span></span><br/>    | <span data-ttu-id="74355-150">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="74355-150">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="74355-151">Header</span><span class="sxs-lookup"><span data-stu-id="74355-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="74355-152"><dt>"Scardmgr. h"</dt></span><span class="sxs-lookup"><span data-stu-id="74355-152"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="74355-153">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="74355-153">Type library</span></span><br/>             | <dl> <span data-ttu-id="74355-154"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="74355-154"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="74355-155">DLL</span><span class="sxs-lookup"><span data-stu-id="74355-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74355-156"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="74355-156"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="74355-157">IID</span><span class="sxs-lookup"><span data-stu-id="74355-157">IID</span></span><br/>                      | <span data-ttu-id="74355-158">IID \_ iscard ist definiert als 1461aac3-6810-11D0-918f -00aa00c18068</span><span class="sxs-lookup"><span data-stu-id="74355-158">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="74355-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="74355-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74355-160">**Attachbyhandle**</span><span class="sxs-lookup"><span data-stu-id="74355-160">**AttachByHandle**</span></span>](iscard-attachbyhandle.md)
</dt> <dt>

[<span data-ttu-id="74355-161">**Trennen**</span><span class="sxs-lookup"><span data-stu-id="74355-161">**Detach**</span></span>](iscard-detach.md)
</dt> <dt>

[<span data-ttu-id="74355-162">**Iscard**</span><span class="sxs-lookup"><span data-stu-id="74355-162">**ISCard**</span></span>](iscard.md)
</dt> <dt>

[<span data-ttu-id="74355-163">**Erneut**</span><span class="sxs-lookup"><span data-stu-id="74355-163">**ReAttach**</span></span>](iscard-reattach.md)
</dt> </dl>

 

 
