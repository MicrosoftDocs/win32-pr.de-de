---
description: Erstellt eine gültige APDU (Command Application Protocol Data Unit) für die Übertragung an eine Smartcard.
ms.assetid: d1003cc3-c235-4635-ad5a-8cea7363bf30
title: 'Iscardcmd:: buildcmd-Methode (scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.BuildCmd
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: f44597ea087f7ccec191abc9dd03787780e88b2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217168"
---
# <a name="iscardcmdbuildcmd-method"></a><span data-ttu-id="02c9a-103">Iscardcmd:: buildcmd-Methode</span><span class="sxs-lookup"><span data-stu-id="02c9a-103">ISCardCmd::BuildCmd method</span></span>

<span data-ttu-id="02c9a-104">\[Die **buildcmd** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="02c9a-104">\[The **BuildCmd** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="02c9a-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="02c9a-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="02c9a-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="02c9a-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="02c9a-107">Die **buildcmd** -Methode erstellt eine gültige [*Application Protocol Data Unit*](../secgloss/a-gly.md) (APDU) für die Übertragung an eine [*Smartcard*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="02c9a-107">The **BuildCmd** method constructs a valid command [*application protocol data unit*](../secgloss/a-gly.md) (APDU) for transmission to a [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="02c9a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="02c9a-108">Syntax</span></span>


```C++
HRESULT BuildCmd(
  [in] BYTE         byClassId,
  [in] BYTE         byInsId,
  [in] BYTE         byP1,
  [in] BYTE         byP2,
  [in] LPBYTEBUFFER pbyData,
  [in] LONG         *p1Le
);
```



## <a name="parameters"></a><span data-ttu-id="02c9a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="02c9a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02c9a-110">*byclassid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="02c9a-110">*byClassId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02c9a-111">Befehls Klassen Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="02c9a-111">Command class identifier.</span></span>

</dd> <dt>

<span data-ttu-id="02c9a-112">*byinsid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="02c9a-112">*byInsId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02c9a-113">Bezeichner der Befehls Anweisung.</span><span class="sxs-lookup"><span data-stu-id="02c9a-113">Command instruction identifier.</span></span>

</dd> <dt>

<span data-ttu-id="02c9a-114">*byP1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="02c9a-114">*byP1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02c9a-115">Der erste Parameter des Befehls.</span><span class="sxs-lookup"><span data-stu-id="02c9a-115">Command's first parameter.</span></span>

</dd> <dt>

<span data-ttu-id="02c9a-116">*byP2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="02c9a-116">*byP2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02c9a-117">Der zweite Parameter des Befehls.</span><span class="sxs-lookup"><span data-stu-id="02c9a-117">Command's second parameter.</span></span>

</dd> <dt>

<span data-ttu-id="02c9a-118">*pbydata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="02c9a-118">*pbyData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02c9a-119">Zeiger auf den Daten Teil des Befehls.</span><span class="sxs-lookup"><span data-stu-id="02c9a-119">Pointer to the data portion of the command.</span></span>

</dd> <dt>

<span data-ttu-id="02c9a-120">*p1Le* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="02c9a-120">*p1Le* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02c9a-121">Ein Zeiger auf einen Long Integer-Wert, der die erwartete Länge der zurückgegebenen Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="02c9a-121">Pointer to a LONG integer containing the expected length of the returned data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02c9a-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="02c9a-122">Return value</span></span>

<span data-ttu-id="02c9a-123">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="02c9a-123">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="02c9a-124">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="02c9a-124">Return code</span></span>                                                                                   | <span data-ttu-id="02c9a-125">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="02c9a-125">Description</span></span>                                    |
|-----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="02c9a-126"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="02c9a-126"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="02c9a-127">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="02c9a-127">Operation completed successfully.</span></span><br/>   |
| <dl> <span data-ttu-id="02c9a-128"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="02c9a-128"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="02c9a-129">Einer der Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="02c9a-129">One of the parameters is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="02c9a-130"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="02c9a-130"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="02c9a-131">Es wurde ein fehlerhafter Zeiger übermittelt.</span><span class="sxs-lookup"><span data-stu-id="02c9a-131">A bad pointer was passed in.</span></span><br/>        |
| <dl> <span data-ttu-id="02c9a-132"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="02c9a-132"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="02c9a-133">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="02c9a-133">Out of memory.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="02c9a-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="02c9a-134">Remarks</span></span>

<span data-ttu-id="02c9a-135">Wenn Sie den Befehl in einem anderen Befehl Kapseln möchten, können Sie [**Kapseln**](iscardcmd-encapsulate.md)einschließen.</span><span class="sxs-lookup"><span data-stu-id="02c9a-135">To encapsulate the command into another command, call [**Encapsulate**](iscardcmd-encapsulate.md).</span></span>

<span data-ttu-id="02c9a-136">Eine Liste aller Methoden, die von dieser Schnittstelle bereitgestellt werden, finden Sie unter [**iscardcmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="02c9a-136">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="02c9a-137">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="02c9a-137">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="02c9a-138">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="02c9a-138">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="02c9a-139">Beispiele</span><span class="sxs-lookup"><span data-stu-id="02c9a-139">Examples</span></span>

<span data-ttu-id="02c9a-140">Im folgenden Beispiel wird gezeigt, wie ein Befehls-APDU erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="02c9a-140">The following example shows how to construct a command APDU.</span></span> <span data-ttu-id="02c9a-141">Im Beispiel wird davon ausgegangen, dass "piscardcmd" ein gültiger Zeiger auf eine Instanz der [**iscardcmd**](iscardcmd.md) -Schnittstelle ist und dass "pibyterequest" ein gültiger Zeiger auf eine Instanz der [**ibytebuffer**](ibytebuffer.md) -Schnittstelle ist, die mit einem vorherigen Aufrufen der [**ibytebuffer:: Initialize**](ibytebuffer-initialize.md) -Methode initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="02c9a-141">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface and that pIByteRequest is a valid pointer to an instance of the [**IByteBuffer**](ibytebuffer.md) interface initialized with a previous call to the [**IByteBuffer::Initialize**](ibytebuffer-initialize.md) method.</span></span>


```C++
LONG       lLe = 0;
HRESULT    hr;

hr = pISCardCmd->BuildCmd(0x00,   // Some cards prefer 0xC0
                          0xa4,   // 'Select File'
                          0x00,
                          0x00,
                          pIByteRequest,
                          &lLe);
if (FAILED(hr))
{
    printf("Failed ISCardCmd::BuildCmd\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="02c9a-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="02c9a-142">Requirements</span></span>



| <span data-ttu-id="02c9a-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="02c9a-143">Requirement</span></span> | <span data-ttu-id="02c9a-144">Wert</span><span class="sxs-lookup"><span data-stu-id="02c9a-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="02c9a-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="02c9a-145">Minimum supported client</span></span><br/> | <span data-ttu-id="02c9a-146">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="02c9a-146">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="02c9a-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="02c9a-147">Minimum supported server</span></span><br/> | <span data-ttu-id="02c9a-148">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="02c9a-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="02c9a-149">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="02c9a-149">End of client support</span></span><br/>    | <span data-ttu-id="02c9a-150">Windows XP</span><span class="sxs-lookup"><span data-stu-id="02c9a-150">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="02c9a-151">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="02c9a-151">End of server support</span></span><br/>    | <span data-ttu-id="02c9a-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="02c9a-152">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="02c9a-153">Header</span><span class="sxs-lookup"><span data-stu-id="02c9a-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="02c9a-154"><dt>"Scarddat. h"</dt></span><span class="sxs-lookup"><span data-stu-id="02c9a-154"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="02c9a-155">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="02c9a-155">Type library</span></span><br/>             | <dl> <span data-ttu-id="02c9a-156"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="02c9a-156"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="02c9a-157">DLL</span><span class="sxs-lookup"><span data-stu-id="02c9a-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02c9a-158"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02c9a-158"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="02c9a-159">IID</span><span class="sxs-lookup"><span data-stu-id="02c9a-159">IID</span></span><br/>                      | <span data-ttu-id="02c9a-160">IID \_ iscardcmd ist als D5778AE3-43DE-11D0-9171-00AA00C18068 definiert.</span><span class="sxs-lookup"><span data-stu-id="02c9a-160">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="02c9a-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="02c9a-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02c9a-162">**Kapseln**</span><span class="sxs-lookup"><span data-stu-id="02c9a-162">**Encapsulate**</span></span>](iscardcmd-encapsulate.md)
</dt> <dt>

[<span data-ttu-id="02c9a-163">**Iscardcmd**</span><span class="sxs-lookup"><span data-stu-id="02c9a-163">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
