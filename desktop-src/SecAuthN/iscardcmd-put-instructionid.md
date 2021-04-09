---
description: Legt den angegebenen Anweisungs Bezeichner in der Application Protocol Data Unit (APDU) fest.
ms.assetid: ea527ffd-b053-467d-883d-b93d5bbfb071
title: Iscardcmd::p ut_InstructionId-Methode (scarddat. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_InstructionId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 6194accfb834152cf07a58fbb8036b13d3fdcd5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959171"
---
# <a name="iscardcmdput_instructionid-method"></a><span data-ttu-id="ef3f9-103">Iscardcmd::p UT- \_ instructionid-Methode</span><span class="sxs-lookup"><span data-stu-id="ef3f9-103">ISCardCmd::put\_InstructionId method</span></span>

<span data-ttu-id="ef3f9-104">\[Die **Put \_ instructionid** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="ef3f9-104">\[The **put\_InstructionId** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="ef3f9-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ef3f9-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="ef3f9-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="ef3f9-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="ef3f9-107">Mit der **Put \_ instructionid** -Methode wird der angegebene Anweisungs Bezeichner in der [*Anwendungsprotokoll Daten-Einheit*](../secgloss/a-gly.md) (APDU) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ef3f9-107">The **put\_InstructionId** method sets the given instruction identifier in the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="ef3f9-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ef3f9-108">Syntax</span></span>


```C++
HRESULT put_InstructionId(
  [in] BYTE byIns
);
```



## <a name="parameters"></a><span data-ttu-id="ef3f9-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ef3f9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef3f9-110">*byins* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ef3f9-110">*byIns* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef3f9-111">Das Byte, das der Anweisungs Bezeichner ist.</span><span class="sxs-lookup"><span data-stu-id="ef3f9-111">The byte that is the instruction identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef3f9-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ef3f9-112">Return value</span></span>

<span data-ttu-id="ef3f9-113">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="ef3f9-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="ef3f9-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="ef3f9-114">Return code</span></span>                                                                                   | <span data-ttu-id="ef3f9-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ef3f9-115">Description</span></span>                                    |
|-----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="ef3f9-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ef3f9-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="ef3f9-117">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="ef3f9-117">Operation completed successfully.</span></span><br/>   |
| <dl> <span data-ttu-id="ef3f9-118"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="ef3f9-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="ef3f9-119">Der *byins* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="ef3f9-119">The *byIns* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="ef3f9-120"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="ef3f9-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="ef3f9-121">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="ef3f9-121">Out of memory.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="ef3f9-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ef3f9-122">Remarks</span></span>

<span data-ttu-id="ef3f9-123">Um den vorhandenen Anweisungs Bezeichner abzurufen, wenden [**Sie get \_ instructionid**](iscardcmd-get-instructionid.md)an.</span><span class="sxs-lookup"><span data-stu-id="ef3f9-123">To get the existing instructional identifier, call [**get\_InstructionId**](iscardcmd-get-instructionid.md).</span></span>

<span data-ttu-id="ef3f9-124">Eine Liste aller Methoden, die von dieser Schnittstelle bereitgestellt werden, finden Sie unter [**iscardcmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="ef3f9-124">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="ef3f9-125">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die [*Smartcard*](../secgloss/s-gly.md) zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="ef3f9-125">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="ef3f9-126">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="ef3f9-126">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="ef3f9-127">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ef3f9-127">Examples</span></span>

<span data-ttu-id="ef3f9-128">Im folgenden Beispiel wird gezeigt, wie Sie einen Anweisungs Bezeichner in der [*Anwendungsprotokoll Daten-Einheit (Application Protocol Data Unit*](../secgloss/a-gly.md) , APDU)</span><span class="sxs-lookup"><span data-stu-id="ef3f9-128">The following example shows how to set an instruction identifier in the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="ef3f9-129">Im Beispiel wird davon ausgegangen, dass "piscardcmd" ein gültiger Zeiger auf eine Instanz der [**iscardcmd**](iscardcmd.md) -Schnittstelle ist.</span><span class="sxs-lookup"><span data-stu-id="ef3f9-129">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
HRESULT hr;

// Set the instruction ID.
hr = pISCardCmd->put_InstructionId(0xb2);
if (FAILED(hr))
{
  printf("Failed put_InstructionId\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="ef3f9-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ef3f9-130">Requirements</span></span>



| <span data-ttu-id="ef3f9-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ef3f9-131">Requirement</span></span> | <span data-ttu-id="ef3f9-132">Wert</span><span class="sxs-lookup"><span data-stu-id="ef3f9-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ef3f9-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ef3f9-133">Minimum supported client</span></span><br/> | <span data-ttu-id="ef3f9-134">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ef3f9-134">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ef3f9-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ef3f9-135">Minimum supported server</span></span><br/> | <span data-ttu-id="ef3f9-136">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ef3f9-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ef3f9-137">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="ef3f9-137">End of client support</span></span><br/>    | <span data-ttu-id="ef3f9-138">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ef3f9-138">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="ef3f9-139">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="ef3f9-139">End of server support</span></span><br/>    | <span data-ttu-id="ef3f9-140">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ef3f9-140">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="ef3f9-141">Header</span><span class="sxs-lookup"><span data-stu-id="ef3f9-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef3f9-142"><dt>"Scarddat. h"</dt></span><span class="sxs-lookup"><span data-stu-id="ef3f9-142"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="ef3f9-143">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="ef3f9-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="ef3f9-144"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ef3f9-144"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ef3f9-145">DLL</span><span class="sxs-lookup"><span data-stu-id="ef3f9-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef3f9-146"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef3f9-146"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="ef3f9-147">IID</span><span class="sxs-lookup"><span data-stu-id="ef3f9-147">IID</span></span><br/>                      | <span data-ttu-id="ef3f9-148">IID \_ iscardcmd ist als D5778AE3-43DE-11D0-9171-00AA00C18068 definiert.</span><span class="sxs-lookup"><span data-stu-id="ef3f9-148">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="ef3f9-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ef3f9-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef3f9-150">**\_instructionid erhalten**</span><span class="sxs-lookup"><span data-stu-id="ef3f9-150">**get\_InstructionId**</span></span>](iscardcmd-get-instructionid.md)
</dt> <dt>

[<span data-ttu-id="ef3f9-151">**Iscardcmd**</span><span class="sxs-lookup"><span data-stu-id="ef3f9-151">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
