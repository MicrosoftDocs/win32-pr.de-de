---
description: Ruft das Datenfeld aus der Application Protocol Data Unit (APDU) ab und platziert es in einem Byte Puffer Objekt.
ms.assetid: fbffeeeb-56e5-4484-b294-8b6f59c919eb
title: 'Iscardcmd:: get_data-Methode (scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_Data
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: feb6a8c28316bd4fd08160063606d3e15054fd87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530221"
---
# <a name="iscardcmdget_data-method"></a><span data-ttu-id="a9c39-103">Iscardcmd:: get- \_ Daten Methode</span><span class="sxs-lookup"><span data-stu-id="a9c39-103">ISCardCmd::get\_Data method</span></span>

<span data-ttu-id="a9c39-104">\[Die Methode " **get \_ Data** " ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="a9c39-104">\[The **get\_Data** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a9c39-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a9c39-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a9c39-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="a9c39-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="a9c39-107">Die Methode **get \_ Data** Ruft das Datenfeld aus der [*Anwendungsprotokoll Daten-Einheit*](../secgloss/a-gly.md) (APDU) ab und platziert es in einem Byte Puffer Objekt.</span><span class="sxs-lookup"><span data-stu-id="a9c39-107">The **get\_Data** method retrieves the data field from the [*application protocol data unit*](../secgloss/a-gly.md) (APDU), placing it in a byte buffer object.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9c39-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9c39-108">Syntax</span></span>


```C++
HRESULT get_Data(
  [out] LPBYTEBUFFER *ppData
);
```



## <a name="parameters"></a><span data-ttu-id="a9c39-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a9c39-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9c39-110">*ppData* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a9c39-110">*ppData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a9c39-111">Zeiger auf das Byte Puffer Objekt (**IStream**), das das APDU-Datenfeld enthält, wenn zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a9c39-111">Pointer to the byte buffer object (**IStream**) that holds the APDU data field on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9c39-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a9c39-112">Return value</span></span>

<span data-ttu-id="a9c39-113">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="a9c39-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="a9c39-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="a9c39-114">Return code</span></span>                                                                                   | <span data-ttu-id="a9c39-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a9c39-115">Description</span></span>                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="a9c39-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a9c39-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="a9c39-117">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="a9c39-117">Operation completed successfully.</span></span><br/>     |
| <dl> <span data-ttu-id="a9c39-118"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="a9c39-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="a9c39-119">Der *ppData* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="a9c39-119">The *ppData* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="a9c39-120"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="a9c39-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="a9c39-121">Ein fehlerhafter Zeiger wurde in *ppData* übermittelt.</span><span class="sxs-lookup"><span data-stu-id="a9c39-121">A bad pointer was passed in *ppData*.</span></span><br/> |
| <dl> <span data-ttu-id="a9c39-122"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="a9c39-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="a9c39-123">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="a9c39-123">Out of memory.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="a9c39-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a9c39-124">Remarks</span></span>

<span data-ttu-id="a9c39-125">Um das Datenfeld des APDU festzulegen, nennen Sie [**Put \_ Data**](iscardcmd-put-data.md).</span><span class="sxs-lookup"><span data-stu-id="a9c39-125">To set the data field of the APDU, call [**put\_Data**](iscardcmd-put-data.md).</span></span>

<span data-ttu-id="a9c39-126">Eine Liste aller Methoden, die von dieser Schnittstelle bereitgestellt werden, finden Sie unter [**iscardcmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="a9c39-126">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="a9c39-127">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die [*Smartcard*](../secgloss/s-gly.md) zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="a9c39-127">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="a9c39-128">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="a9c39-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="a9c39-129">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a9c39-129">Examples</span></span>

<span data-ttu-id="a9c39-130">Im folgenden Beispiel wird gezeigt, wie das Datenfeld der [*Anwendungsprotokoll Daten-Einheit (Application Protocol Data Unit*](../secgloss/a-gly.md) , APDU) abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="a9c39-130">The following example shows how to retrieve the data field of the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="a9c39-131">In diesem Beispiel wird davon ausgegangen, dass pibytedata ein gültiger Zeiger auf eine Instanz der [**ibytebuffer**](ibytebuffer.md) -Schnittstelle ist und dass "piscardcmd" ein gültiger Zeiger auf eine Instanz der [**iscardcmd**](iscardcmd.md) -Schnittstelle ist.</span><span class="sxs-lookup"><span data-stu-id="a9c39-131">The example assumes that pIByteData is a valid pointer to an instance of the [**IByteBuffer**](ibytebuffer.md) interface, and that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
HRESULT    hr;

// pIByteData is a pointer to an instance of IByteBuffer.
// Retrieve the data.
hr = pISCardCmd->get_Data(&pIByteData);
if (FAILED(hr)) 
{
    printf("Failed get_Data.\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="a9c39-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a9c39-132">Requirements</span></span>



| <span data-ttu-id="a9c39-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a9c39-133">Requirement</span></span> | <span data-ttu-id="a9c39-134">Wert</span><span class="sxs-lookup"><span data-stu-id="a9c39-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a9c39-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a9c39-135">Minimum supported client</span></span><br/> | <span data-ttu-id="a9c39-136">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a9c39-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a9c39-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a9c39-137">Minimum supported server</span></span><br/> | <span data-ttu-id="a9c39-138">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a9c39-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a9c39-139">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="a9c39-139">End of client support</span></span><br/>    | <span data-ttu-id="a9c39-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a9c39-140">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="a9c39-141">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="a9c39-141">End of server support</span></span><br/>    | <span data-ttu-id="a9c39-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a9c39-142">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="a9c39-143">Header</span><span class="sxs-lookup"><span data-stu-id="a9c39-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9c39-144"><dt>"Scarddat. h"</dt></span><span class="sxs-lookup"><span data-stu-id="a9c39-144"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="a9c39-145">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="a9c39-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="a9c39-146"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a9c39-146"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a9c39-147">DLL</span><span class="sxs-lookup"><span data-stu-id="a9c39-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a9c39-148"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a9c39-148"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a9c39-149">IID</span><span class="sxs-lookup"><span data-stu-id="a9c39-149">IID</span></span><br/>                      | <span data-ttu-id="a9c39-150">IID \_ iscardcmd ist als D5778AE3-43DE-11D0-9171-00AA00C18068 definiert.</span><span class="sxs-lookup"><span data-stu-id="a9c39-150">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="a9c39-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a9c39-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9c39-152">**Iscardcmd**</span><span class="sxs-lookup"><span data-stu-id="a9c39-152">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="a9c39-153">**\_Daten einfügen**</span><span class="sxs-lookup"><span data-stu-id="a9c39-153">**put\_Data**</span></span>](iscardcmd-put-data.md)
</dt> </dl>

 

 
