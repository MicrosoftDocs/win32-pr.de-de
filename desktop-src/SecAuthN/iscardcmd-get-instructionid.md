---
description: Ruft das Anweisungs bezeichnerbyte aus der Anwendungsprotokoll Daten-Einheit (APDU) ab.
ms.assetid: 294f51cd-0a13-4dfb-bf02-9edd11a7085e
title: 'Iscardcmd:: get_InstructionId-Methode (scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_InstructionId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 4b0125237ef94a5d6173f517483b9ae8781d5607
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960821"
---
# <a name="iscardcmdget_instructionid-method"></a><span data-ttu-id="0025a-103">Iscardcmd:: get- \_ instructionid-Methode</span><span class="sxs-lookup"><span data-stu-id="0025a-103">ISCardCmd::get\_InstructionId method</span></span>

<span data-ttu-id="0025a-104">\[Die **get \_ instructionid** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="0025a-104">\[The **get\_InstructionId** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="0025a-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0025a-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="0025a-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="0025a-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="0025a-107">Die **get \_ instructionid** -Methode ruft das Anweisungs bezeichnerbyte aus der [*Application Protocol Data Unit*](../secgloss/a-gly.md) (APDU) ab.</span><span class="sxs-lookup"><span data-stu-id="0025a-107">The **get\_InstructionId** method retrieves the instruction identifier byte from the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="0025a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0025a-108">Syntax</span></span>


```C++
HRESULT get_InstructionId(
  [out] BYTE *pbyIns
);
```



## <a name="parameters"></a><span data-ttu-id="0025a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="0025a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0025a-110">*pbyins* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="0025a-110">*pbyIns* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0025a-111">Zeiger auf das Byte, das die Anweisungs-ID aus dem APDU bei der Rückgabe ist.</span><span class="sxs-lookup"><span data-stu-id="0025a-111">Pointer to the byte that is the instruction ID from the APDU on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0025a-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0025a-112">Return value</span></span>

<span data-ttu-id="0025a-113">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="0025a-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="0025a-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="0025a-114">Return code</span></span>                                                                                   | <span data-ttu-id="0025a-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0025a-115">Description</span></span>                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="0025a-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0025a-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="0025a-117">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="0025a-117">Operation completed successfully.</span></span><br/>     |
| <dl> <span data-ttu-id="0025a-118"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="0025a-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="0025a-119">Der *pbyins* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="0025a-119">The *pbyIns* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="0025a-120"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="0025a-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="0025a-121">Ein fehlerhafter Zeiger wurde in *pbyins* übergeben.</span><span class="sxs-lookup"><span data-stu-id="0025a-121">A bad pointer was passed in *pbyIns*.</span></span><br/> |
| <dl> <span data-ttu-id="0025a-122"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="0025a-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="0025a-123">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="0025a-123">Out of memory.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="0025a-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0025a-124">Remarks</span></span>

<span data-ttu-id="0025a-125">Um den Anweisungs Bezeichner auf einen neuen Wert festzulegen, wenden Sie [**Put \_ instructionid**](iscardcmd-put-instructionid.md)an.</span><span class="sxs-lookup"><span data-stu-id="0025a-125">To set the instructional identifier to a new value, call [**put\_InstructionId**](iscardcmd-put-instructionid.md).</span></span>

<span data-ttu-id="0025a-126">Eine Liste aller Methoden, die von dieser Schnittstelle bereitgestellt werden, finden Sie unter [**iscardcmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="0025a-126">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="0025a-127">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die [*Smartcard*](../secgloss/s-gly.md) zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="0025a-127">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="0025a-128">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="0025a-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="0025a-129">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0025a-129">Examples</span></span>

<span data-ttu-id="0025a-130">Im folgenden Beispiel wird gezeigt, wie das Anweisungs bezeichnerbyte aus der [*Anwendungsprotokoll Dateneinheit (Application Protocol Data Unit*](../secgloss/a-gly.md) , APDU) abgerufen wird</span><span class="sxs-lookup"><span data-stu-id="0025a-130">The following example shows how to retrieve the instruction identifier byte from the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="0025a-131">Im Beispiel wird davon ausgegangen, dass "piscardcmd" ein gültiger Zeiger auf eine Instanz der [**iscardcmd**](iscardcmd.md) -Schnittstelle ist.</span><span class="sxs-lookup"><span data-stu-id="0025a-131">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
BYTE  byInstructID;
HRESULT hr;

// Retrieve the instruction ID.
hr = pISCardCmd->get_InstructionId(&byInstructID);
if (FAILED(hr))
{
  printf("Failed get_InstructionId\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="0025a-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0025a-132">Requirements</span></span>



| <span data-ttu-id="0025a-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0025a-133">Requirement</span></span> | <span data-ttu-id="0025a-134">Wert</span><span class="sxs-lookup"><span data-stu-id="0025a-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0025a-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0025a-135">Minimum supported client</span></span><br/> | <span data-ttu-id="0025a-136">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0025a-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="0025a-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0025a-137">Minimum supported server</span></span><br/> | <span data-ttu-id="0025a-138">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0025a-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0025a-139">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="0025a-139">End of client support</span></span><br/>    | <span data-ttu-id="0025a-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="0025a-140">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="0025a-141">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="0025a-141">End of server support</span></span><br/>    | <span data-ttu-id="0025a-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0025a-142">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="0025a-143">Header</span><span class="sxs-lookup"><span data-stu-id="0025a-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="0025a-144"><dt>"Scarddat. h"</dt></span><span class="sxs-lookup"><span data-stu-id="0025a-144"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="0025a-145">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="0025a-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="0025a-146"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0025a-146"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0025a-147">DLL</span><span class="sxs-lookup"><span data-stu-id="0025a-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0025a-148"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0025a-148"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="0025a-149">IID</span><span class="sxs-lookup"><span data-stu-id="0025a-149">IID</span></span><br/>                      | <span data-ttu-id="0025a-150">IID \_ iscardcmd ist als D5778AE3-43DE-11D0-9171-00AA00C18068 definiert.</span><span class="sxs-lookup"><span data-stu-id="0025a-150">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="0025a-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0025a-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0025a-152">**Iscardcmd**</span><span class="sxs-lookup"><span data-stu-id="0025a-152">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="0025a-153">**\_instructionid platzieren**</span><span class="sxs-lookup"><span data-stu-id="0025a-153">**put\_InstructionId**</span></span>](iscardcmd-put-instructionid.md)
</dt> </dl>

 

 
