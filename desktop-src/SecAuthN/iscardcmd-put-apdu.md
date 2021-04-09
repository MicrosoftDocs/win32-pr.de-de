---
description: Kopiert die Application Protocol Data Unit (APDU) aus dem ibytebuffer (IStream)-Objekt in das APDU, das in diesem Schnittstellen Objekt umgeschrieben ist.
ms.assetid: 28dac222-ee7a-40aa-903b-e9c0b7757c9c
title: Iscardcmd::p ut_Apdu-Methode (scarddat. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_Apdu
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: ee615e7f2e8d7555cfed276658e8de1a97ddf73a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958947"
---
# <a name="iscardcmdput_apdu-method"></a><span data-ttu-id="ebc02-103">Iscardcmd::p UT- \_ APDU-Methode</span><span class="sxs-lookup"><span data-stu-id="ebc02-103">ISCardCmd::put\_Apdu method</span></span>

<span data-ttu-id="ebc02-104">\[Die **Put \_ APDU** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="ebc02-104">\[The **put\_Apdu** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="ebc02-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ebc02-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="ebc02-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="ebc02-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="ebc02-107">Die **Put \_ APDU** -Methode kopiert die APDU ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ) aus dem [**ibytebuffer**](ibytebuffer.md) (**IStream**)-Objekt in das APDU, das in diesem Schnittstellen Objekt enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="ebc02-107">The **put\_Apdu** method copies the [*application protocol data unit*](../secgloss/a-gly.md) (APDU) from the [**IByteBuffer**](ibytebuffer.md) (**IStream**) object into the APDU wrapped in this interface object.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebc02-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ebc02-108">Syntax</span></span>


```C++
HRESULT put_Apdu(
  [in] LPBYTEBUFFER pApdu
);
```



## <a name="parameters"></a><span data-ttu-id="ebc02-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ebc02-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebc02-110">*papdu* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ebc02-110">*pApdu* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebc02-111">Zeiger auf das ISO 7816-4-APDU, das in kopiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ebc02-111">Pointer to the ISO 7816-4 APDU to be copied in.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebc02-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ebc02-112">Return value</span></span>

<span data-ttu-id="ebc02-113">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="ebc02-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="ebc02-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="ebc02-114">Return code</span></span>                                                                                   | <span data-ttu-id="ebc02-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ebc02-115">Description</span></span>                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="ebc02-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ebc02-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="ebc02-117">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="ebc02-117">Operation completed successfully.</span></span><br/>    |
| <dl> <span data-ttu-id="ebc02-118"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="ebc02-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="ebc02-119">Der *papdu* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="ebc02-119">The *pApdu* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="ebc02-120"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="ebc02-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="ebc02-121">Ein fehlerhafter Zeiger wurde in *papdu* übermittelt.</span><span class="sxs-lookup"><span data-stu-id="ebc02-121">A bad pointer was passed in *pApdu*.</span></span><br/> |
| <dl> <span data-ttu-id="ebc02-122"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="ebc02-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="ebc02-123">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="ebc02-123">Out of memory.</span></span><br/>                       |



 

## <a name="remarks"></a><span data-ttu-id="ebc02-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ebc02-124">Remarks</span></span>

<span data-ttu-id="ebc02-125">Rufen [**Sie get \_ APDU**](iscardcmd-get-apdu.md)auf, um das unformatierte APDU aus dem Byte Puffer abzurufen, der über einen **IStream** zugeordnet ist, der die APDU-Nachricht enthält.</span><span class="sxs-lookup"><span data-stu-id="ebc02-125">To retrieve the raw APDU from the byte buffer mapped through an **IStream** that contains the APDU message, call [**get\_Apdu**](iscardcmd-get-apdu.md).</span></span>

<span data-ttu-id="ebc02-126">Eine Liste aller Methoden, die von dieser Schnittstelle bereitgestellt werden, finden Sie unter [**iscardcmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="ebc02-126">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="ebc02-127">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die [*Smartcard*](../secgloss/s-gly.md) zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="ebc02-127">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="ebc02-128">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="ebc02-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="ebc02-129">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ebc02-129">Examples</span></span>

<span data-ttu-id="ebc02-130">Im folgenden Beispiel wird gezeigt, wie Sie ein APDU aus einem [**ibytebuffer**](ibytebuffer.md) -Objekt (**IStream**) in das in ein Schnittstellen Objekt umschließende APDU kopieren.</span><span class="sxs-lookup"><span data-stu-id="ebc02-130">The following example shows how to copy an APDU from an [**IByteBuffer**](ibytebuffer.md) (**IStream**) object into the APDU wrapped in an interface object.</span></span> <span data-ttu-id="ebc02-131">Im Beispiel wird davon ausgegangen, dass pibyteapdu ein gültiger Zeiger auf eine Instanz von **ibytebuffer** ist und dass piscardcmd ein gültiger Zeiger auf eine Instanz der [**iscardcmd**](iscardcmd.md) -Schnittstelle ist.</span><span class="sxs-lookup"><span data-stu-id="ebc02-131">The example assumes that pIByteApdu is a valid pointer to an instance of **IByteBuffer** and that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
HRESULT    hr;


// Set the APDU.
hr = pISCardCmd->put_Apdu(pIByteApdu);
if (FAILED(hr)) 
{
    printf("Failed put_Apdu.\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="ebc02-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ebc02-132">Requirements</span></span>



| <span data-ttu-id="ebc02-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ebc02-133">Requirement</span></span> | <span data-ttu-id="ebc02-134">Wert</span><span class="sxs-lookup"><span data-stu-id="ebc02-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ebc02-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ebc02-135">Minimum supported client</span></span><br/> | <span data-ttu-id="ebc02-136">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ebc02-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ebc02-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ebc02-137">Minimum supported server</span></span><br/> | <span data-ttu-id="ebc02-138">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ebc02-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ebc02-139">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="ebc02-139">End of client support</span></span><br/>    | <span data-ttu-id="ebc02-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ebc02-140">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="ebc02-141">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="ebc02-141">End of server support</span></span><br/>    | <span data-ttu-id="ebc02-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ebc02-142">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="ebc02-143">Header</span><span class="sxs-lookup"><span data-stu-id="ebc02-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="ebc02-144"><dt>"Scarddat. h"</dt></span><span class="sxs-lookup"><span data-stu-id="ebc02-144"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="ebc02-145">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="ebc02-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="ebc02-146"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ebc02-146"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ebc02-147">DLL</span><span class="sxs-lookup"><span data-stu-id="ebc02-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ebc02-148"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ebc02-148"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="ebc02-149">IID</span><span class="sxs-lookup"><span data-stu-id="ebc02-149">IID</span></span><br/>                      | <span data-ttu-id="ebc02-150">IID \_ iscardcmd ist als D5778AE3-43DE-11D0-9171-00AA00C18068 definiert.</span><span class="sxs-lookup"><span data-stu-id="ebc02-150">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="ebc02-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ebc02-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebc02-152">**\_APDU erhalten**</span><span class="sxs-lookup"><span data-stu-id="ebc02-152">**get\_Apdu**</span></span>](iscardcmd-get-apdu.md)
</dt> <dt>

[<span data-ttu-id="ebc02-153">**Iscardcmd**</span><span class="sxs-lookup"><span data-stu-id="ebc02-153">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
