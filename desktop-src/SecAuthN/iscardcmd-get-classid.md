---
description: Ruft den Klassen Bezeichner aus der Application Protocol Data Unit (APDU) ab.
ms.assetid: 03ea997d-7698-43c7-aa9a-dfc1bac6fcdd
title: 'Iscardcmd:: get_ClassId-Methode (scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ClassId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 6b78dfc9f3adf200a614b129ff1e86a16c88438f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129345"
---
# <a name="iscardcmdget_classid-method"></a><span data-ttu-id="61662-103">Iscardcmd:: get \_ ClassID-Methode</span><span class="sxs-lookup"><span data-stu-id="61662-103">ISCardCmd::get\_ClassId method</span></span>

<span data-ttu-id="61662-104">\[Die **get \_ ClassID-** Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="61662-104">\[The **get\_ClassId** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="61662-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="61662-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="61662-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="61662-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="61662-107">Die **get \_ ClassID-** Methode ruft den Klassen Bezeichner aus der [*Application Protocol Data Unit*](../secgloss/a-gly.md) (APDU) ab.</span><span class="sxs-lookup"><span data-stu-id="61662-107">The **get\_ClassId** method retrieves the class identifier from the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="61662-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="61662-108">Syntax</span></span>


```C++
HRESULT get_ClassId(
  [out] BYTE *pbyClass
);
```



## <a name="parameters"></a><span data-ttu-id="61662-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="61662-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61662-110">*pbyclass* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="61662-110">*pbyClass* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="61662-111">Zeiger auf das Byte, das den Klassen Bezeichner darstellt.</span><span class="sxs-lookup"><span data-stu-id="61662-111">Pointer to the byte that represents the class identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61662-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="61662-112">Return value</span></span>

<span data-ttu-id="61662-113">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="61662-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="61662-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="61662-114">Return code</span></span>                                                                                   | <span data-ttu-id="61662-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="61662-115">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="61662-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="61662-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="61662-117">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="61662-117">Operation completed successfully.</span></span><br/>       |
| <dl> <span data-ttu-id="61662-118"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="61662-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="61662-119">Der *pbyclass* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="61662-119">The *pbyClass* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="61662-120"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="61662-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="61662-121">Ein fehlerhafter Zeiger wurde in " *pbyclass*" übergeben.</span><span class="sxs-lookup"><span data-stu-id="61662-121">A bad pointer was passed in *pbyClass*.</span></span><br/> |
| <dl> <span data-ttu-id="61662-122"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="61662-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="61662-123">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="61662-123">Out of memory.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="61662-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="61662-124">Remarks</span></span>

<span data-ttu-id="61662-125">Um den Klassen Bezeichner auf einen neuen Wert festzulegen, nennen Sie [**Put \_ ClassID**](iscardcmd-put-classid.md).</span><span class="sxs-lookup"><span data-stu-id="61662-125">To set the class identifier to a new value, call [**put\_ClassId**](iscardcmd-put-classid.md).</span></span>

<span data-ttu-id="61662-126">Eine Liste aller Methoden, die von dieser Schnittstelle bereitgestellt werden, finden Sie unter [**iscardcmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="61662-126">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="61662-127">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="61662-127">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="61662-128">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="61662-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="61662-129">Beispiele</span><span class="sxs-lookup"><span data-stu-id="61662-129">Examples</span></span>

<span data-ttu-id="61662-130">Im folgenden Beispiel wird gezeigt, wie die Klassen-ID abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="61662-130">The following example shows how to retrieve the class ID.</span></span> <span data-ttu-id="61662-131">Im Beispiel wird davon ausgegangen, dass "piscardcmd" ein gültiger Zeiger auf eine Instanz der [**iscardcmd**](iscardcmd.md) -Schnittstelle ist.</span><span class="sxs-lookup"><span data-stu-id="61662-131">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
BYTE     byClassID;
HRESULT  hr;

// Retrieve the class ID.
hr = pISCardCmd->get_ClassId(&byClassID);
if (FAILED(hr))
{
  printf("Failed get_ClassId\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="61662-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="61662-132">Requirements</span></span>



| <span data-ttu-id="61662-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="61662-133">Requirement</span></span> | <span data-ttu-id="61662-134">Wert</span><span class="sxs-lookup"><span data-stu-id="61662-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="61662-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="61662-135">Minimum supported client</span></span><br/> | <span data-ttu-id="61662-136">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="61662-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="61662-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="61662-137">Minimum supported server</span></span><br/> | <span data-ttu-id="61662-138">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="61662-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="61662-139">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="61662-139">End of client support</span></span><br/>    | <span data-ttu-id="61662-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="61662-140">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="61662-141">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="61662-141">End of server support</span></span><br/>    | <span data-ttu-id="61662-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="61662-142">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="61662-143">Header</span><span class="sxs-lookup"><span data-stu-id="61662-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="61662-144"><dt>"Scarddat. h"</dt></span><span class="sxs-lookup"><span data-stu-id="61662-144"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="61662-145">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="61662-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="61662-146"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="61662-146"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="61662-147">DLL</span><span class="sxs-lookup"><span data-stu-id="61662-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61662-148"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="61662-148"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="61662-149">IID</span><span class="sxs-lookup"><span data-stu-id="61662-149">IID</span></span><br/>                      | <span data-ttu-id="61662-150">IID \_ iscardcmd ist als D5778AE3-43DE-11D0-9171-00AA00C18068 definiert.</span><span class="sxs-lookup"><span data-stu-id="61662-150">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="61662-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="61662-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61662-152">**Iscardcmd**</span><span class="sxs-lookup"><span data-stu-id="61662-152">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="61662-153">**Put \_ ClassID**</span><span class="sxs-lookup"><span data-stu-id="61662-153">**put\_ClassId**</span></span>](iscardcmd-put-classid.md)
</dt> </dl>

 

 
