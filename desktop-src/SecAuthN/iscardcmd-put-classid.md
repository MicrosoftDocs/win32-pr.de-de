---
description: Legt einen neuen Klassen Bezeichner in der Application Protocol Data Unit (APDU) fest.
ms.assetid: 7e7d42f2-2858-4b37-a7d5-a919e3e005da
title: Iscardcmd::p ut_ClassId-Methode (scarddat. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_ClassId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: ed4b1f273ebe9ea0a5e105ec3d88fc8446f7a831
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959172"
---
# <a name="iscardcmdput_classid-method"></a><span data-ttu-id="9ead2-103">Iscardcmd::p UT \_ ClassID-Methode</span><span class="sxs-lookup"><span data-stu-id="9ead2-103">ISCardCmd::put\_ClassId method</span></span>

<span data-ttu-id="9ead2-104">\[Die **Put \_ ClassID-** Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="9ead2-104">\[The **put\_ClassId** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="9ead2-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9ead2-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="9ead2-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="9ead2-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="9ead2-107">Die **Put \_ ClassID-** Methode legt einen neuen Klassen Bezeichner in der [*Application Protocol Data Unit*](../secgloss/a-gly.md) (APDU) fest.</span><span class="sxs-lookup"><span data-stu-id="9ead2-107">The **put\_ClassId** method sets a new class identifier in the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="9ead2-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ead2-108">Syntax</span></span>


```C++
HRESULT put_ClassId(
  [in] BYTE byClass
);
```



## <a name="parameters"></a><span data-ttu-id="9ead2-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="9ead2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ead2-110">*byclass* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9ead2-110">*byClass* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ead2-111">Das Byte, das den Klassen Bezeichner darstellt.</span><span class="sxs-lookup"><span data-stu-id="9ead2-111">The byte that represents the class identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ead2-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9ead2-112">Return value</span></span>

<span data-ttu-id="9ead2-113">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="9ead2-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="9ead2-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="9ead2-114">Return code</span></span>                                                                                   | <span data-ttu-id="9ead2-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9ead2-115">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="9ead2-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9ead2-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="9ead2-117">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="9ead2-117">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="9ead2-118"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="9ead2-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="9ead2-119">Die *byclass* ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="9ead2-119">The *byClass* is not valid.</span></span><br/>       |
| <dl> <span data-ttu-id="9ead2-120"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="9ead2-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="9ead2-121">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="9ead2-121">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="9ead2-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9ead2-122">Remarks</span></span>

<span data-ttu-id="9ead2-123">Rufen Sie zum Abrufen des aktuellen Klassen Bezeichners [**get \_ ClassID**](iscardcmd-get-classid.md)auf.</span><span class="sxs-lookup"><span data-stu-id="9ead2-123">To retrieve the current class identifier, call [**get\_ClassId**](iscardcmd-get-classid.md).</span></span>

<span data-ttu-id="9ead2-124">Eine Liste aller Methoden, die von dieser Schnittstelle bereitgestellt werden, finden Sie unter [**iscardcmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="9ead2-124">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="9ead2-125">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die [*Smartcard*](../secgloss/s-gly.md) zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="9ead2-125">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="9ead2-126">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="9ead2-126">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="9ead2-127">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9ead2-127">Examples</span></span>

<span data-ttu-id="9ead2-128">Das folgende Beispiel zeigt, wie Sie einen neuen Klassen Bezeichner in der [*Anwendungsprotokoll Daten-Einheit (Application Protocol Data Unit*](../secgloss/a-gly.md) , APDU) festlegen.</span><span class="sxs-lookup"><span data-stu-id="9ead2-128">The following example shows how to set a new class identifier in the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="9ead2-129">Im Beispiel wird davon ausgegangen, dass "piscardcmd" ein gültiger Zeiger auf eine Instanz der [**iscardcmd**](iscardcmd.md) -Schnittstelle ist.</span><span class="sxs-lookup"><span data-stu-id="9ead2-129">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
HRESULT  hr;

// Set the class ID.
hr = pISCardCmd->put_ClassId(0xC0);
if (FAILED(hr))
{
  printf("Failed put_ClassId\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="9ead2-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9ead2-130">Requirements</span></span>



| <span data-ttu-id="9ead2-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9ead2-131">Requirement</span></span> | <span data-ttu-id="9ead2-132">Wert</span><span class="sxs-lookup"><span data-stu-id="9ead2-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ead2-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9ead2-133">Minimum supported client</span></span><br/> | <span data-ttu-id="9ead2-134">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9ead2-134">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="9ead2-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9ead2-135">Minimum supported server</span></span><br/> | <span data-ttu-id="9ead2-136">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9ead2-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9ead2-137">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="9ead2-137">End of client support</span></span><br/>    | <span data-ttu-id="9ead2-138">Windows XP</span><span class="sxs-lookup"><span data-stu-id="9ead2-138">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="9ead2-139">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="9ead2-139">End of server support</span></span><br/>    | <span data-ttu-id="9ead2-140">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9ead2-140">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="9ead2-141">Header</span><span class="sxs-lookup"><span data-stu-id="9ead2-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ead2-142"><dt>"Scarddat. h"</dt></span><span class="sxs-lookup"><span data-stu-id="9ead2-142"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="9ead2-143">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="9ead2-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="9ead2-144"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9ead2-144"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9ead2-145">DLL</span><span class="sxs-lookup"><span data-stu-id="9ead2-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ead2-146"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ead2-146"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="9ead2-147">IID</span><span class="sxs-lookup"><span data-stu-id="9ead2-147">IID</span></span><br/>                      | <span data-ttu-id="9ead2-148">IID \_ iscardcmd ist als D5778AE3-43DE-11D0-9171-00AA00C18068 definiert.</span><span class="sxs-lookup"><span data-stu-id="9ead2-148">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="9ead2-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9ead2-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ead2-150">**\_ClassID Get**</span><span class="sxs-lookup"><span data-stu-id="9ead2-150">**get\_ClassId**</span></span>](iscardcmd-get-classid.md)
</dt> <dt>

[<span data-ttu-id="9ead2-151">**Iscardcmd**</span><span class="sxs-lookup"><span data-stu-id="9ead2-151">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
