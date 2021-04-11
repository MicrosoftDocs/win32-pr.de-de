---
description: Ruft die Rohdaten-app (Application Protocol Data Unit, APDU) ab.
ms.assetid: d8b326db-de54-4ef8-becb-fd905414c45c
title: 'Iscardcmd:: get_Apdu-Methode (scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_Apdu
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: fb943d7ade48f6684cdc10cb4b1ad7e48f87e65c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041750"
---
# <a name="iscardcmdget_apdu-method"></a><span data-ttu-id="25fe1-103">Iscardcmd:: get \_ APDU-Methode</span><span class="sxs-lookup"><span data-stu-id="25fe1-103">ISCardCmd::get\_Apdu method</span></span>

<span data-ttu-id="25fe1-104">\[Die **get \_ APDU** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="25fe1-104">\[The **get\_Apdu** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="25fe1-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="25fe1-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="25fe1-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="25fe1-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="25fe1-107">Die **get \_ APDU** -Methode ruft die RAW-APDU ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ) ab.</span><span class="sxs-lookup"><span data-stu-id="25fe1-107">The **get\_Apdu** method retrieves the raw [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="25fe1-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="25fe1-108">Syntax</span></span>


```C++
HRESULT get_Apdu(
  [out] LPBYTEBUFFER *ppApdu
);
```



## <a name="parameters"></a><span data-ttu-id="25fe1-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="25fe1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25fe1-110">*ppapdu* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="25fe1-110">*ppApdu* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="25fe1-111">Zeiger auf den Byte Puffer, der über ein **IStream** -Objekt zugeordnet ist, das die APDU-Nachricht bei der Rückgabe enthält.</span><span class="sxs-lookup"><span data-stu-id="25fe1-111">Pointer to the byte buffer mapped through an **IStream** object that contains the APDU message on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25fe1-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="25fe1-112">Return value</span></span>

<span data-ttu-id="25fe1-113">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="25fe1-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="25fe1-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="25fe1-114">Return code</span></span>                                                                                   | <span data-ttu-id="25fe1-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="25fe1-115">Description</span></span>                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="25fe1-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="25fe1-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="25fe1-117">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="25fe1-117">Operation completed successfully.</span></span><br/>     |
| <dl> <span data-ttu-id="25fe1-118"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="25fe1-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="25fe1-119">Der *ppapdu* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="25fe1-119">The *ppApdu* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="25fe1-120"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="25fe1-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="25fe1-121">Ein fehlerhafter Zeiger wurde in *ppapdu* übermittelt.</span><span class="sxs-lookup"><span data-stu-id="25fe1-121">A bad pointer was passed in *ppApdu*.</span></span><br/> |
| <dl> <span data-ttu-id="25fe1-122"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="25fe1-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="25fe1-123">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="25fe1-123">Out of memory.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="25fe1-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="25fe1-124">Remarks</span></span>

<span data-ttu-id="25fe1-125">Um das APDU aus einem [**ibytebuffer**](ibytebuffer.md) (**IStream**)-Objekt in das APDU zu kopieren, das in diesem Schnittstellen Objekt enthalten ist, wenden Sie [**Put \_ APDU**](iscardcmd-put-apdu.md)an.</span><span class="sxs-lookup"><span data-stu-id="25fe1-125">To copy the APDU from an [**IByteBuffer**](ibytebuffer.md) (**IStream**) object into the APDU wrapped in this interface object, call [**put\_Apdu**](iscardcmd-put-apdu.md).</span></span>

<span data-ttu-id="25fe1-126">Um die Länge des APDU zu ermitteln, wenden [**Sie get \_ apdulength**](iscardcmd-get-apdulength.md)an.</span><span class="sxs-lookup"><span data-stu-id="25fe1-126">To determine the length of the APDU, call [**get\_ApduLength**](iscardcmd-get-apdulength.md).</span></span>

<span data-ttu-id="25fe1-127">Eine Liste aller Methoden, die von der [**iscardcmd**](iscardcmd.md) -Schnittstelle bereitgestellt werden, finden Sie unter [**iscardcmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="25fe1-127">For a list of all the methods provided by the [**ISCardCmd**](iscardcmd.md) interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="25fe1-128">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die [*Smartcard*](../secgloss/s-gly.md) zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="25fe1-128">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="25fe1-129">Informationen zu smartcardfehlercodes finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="25fe1-129">For information about smart card error codes, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="25fe1-130">Beispiele</span><span class="sxs-lookup"><span data-stu-id="25fe1-130">Examples</span></span>

<span data-ttu-id="25fe1-131">Im folgenden Beispiel wird gezeigt, wie die RAW [*Application Protocol Data Unit*](../secgloss/a-gly.md) (APDU) abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="25fe1-131">The following example shows how to retrieve the raw [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="25fe1-132">Im Beispiel wird davon ausgegangen, dass "piscardcmd" ein gültiger Zeiger auf die [**iscardcmd**](iscardcmd.md) -Schnittstelle ist, und dass "pibyteapdu" ein gültiger Zeiger auf eine Instanz der [**ibytebuffer**](ibytebuffer.md) -Schnittstelle ist.</span><span class="sxs-lookup"><span data-stu-id="25fe1-132">The example assumes that pISCardCmd is a valid pointer to the [**ISCardCmd**](iscardcmd.md) interface, and that pIByteApdu is a valid pointer to an instance of the [**IByteBuffer**](ibytebuffer.md) interface.</span></span>


```C++
HRESULT    hr;

hr = pISCardCmd->get_Apdu(&pIByteApdu);
if (FAILED(hr)) 
{
    printf("Failed get_Apdu.\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="25fe1-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="25fe1-133">Requirements</span></span>



| <span data-ttu-id="25fe1-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="25fe1-134">Requirement</span></span> | <span data-ttu-id="25fe1-135">Wert</span><span class="sxs-lookup"><span data-stu-id="25fe1-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="25fe1-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="25fe1-136">Minimum supported client</span></span><br/> | <span data-ttu-id="25fe1-137">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="25fe1-137">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="25fe1-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="25fe1-138">Minimum supported server</span></span><br/> | <span data-ttu-id="25fe1-139">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="25fe1-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="25fe1-140">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="25fe1-140">End of client support</span></span><br/>    | <span data-ttu-id="25fe1-141">Windows XP</span><span class="sxs-lookup"><span data-stu-id="25fe1-141">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="25fe1-142">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="25fe1-142">End of server support</span></span><br/>    | <span data-ttu-id="25fe1-143">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="25fe1-143">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="25fe1-144">Header</span><span class="sxs-lookup"><span data-stu-id="25fe1-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="25fe1-145"><dt>"Scarddat. h"</dt></span><span class="sxs-lookup"><span data-stu-id="25fe1-145"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="25fe1-146">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="25fe1-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="25fe1-147"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="25fe1-147"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="25fe1-148">DLL</span><span class="sxs-lookup"><span data-stu-id="25fe1-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="25fe1-149"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25fe1-149"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="25fe1-150">IID</span><span class="sxs-lookup"><span data-stu-id="25fe1-150">IID</span></span><br/>                      | <span data-ttu-id="25fe1-151">IID \_ iscardcmd ist als D5778AE3-43DE-11D0-9171-00AA00C18068 definiert.</span><span class="sxs-lookup"><span data-stu-id="25fe1-151">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="25fe1-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="25fe1-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25fe1-153">**\_apdulength erhalten**</span><span class="sxs-lookup"><span data-stu-id="25fe1-153">**get\_ApduLength**</span></span>](iscardcmd-get-apdulength.md)
</dt> <dt>

[<span data-ttu-id="25fe1-154">**Iscardcmd**</span><span class="sxs-lookup"><span data-stu-id="25fe1-154">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="25fe1-155">**\_APDU platzieren**</span><span class="sxs-lookup"><span data-stu-id="25fe1-155">**put\_Apdu**</span></span>](iscardcmd-put-apdu.md)
</dt> </dl>

 

 
