---
description: Die Clear-Methode löscht die APDU (Application Protocol Data Unit)-und Antwort-APDU-Nachrichten Puffer.
ms.assetid: 5fd3ebb9-b492-4668-9dd8-3ffbcfceb12c
title: 'Iscardcmd:: Clear-Methode (scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.Clear
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 0701906c38764ed1b4817f40430dde9b48bfb12e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129353"
---
# <a name="iscardcmdclear-method"></a><span data-ttu-id="9ee3d-103">Iscardcmd:: Clear-Methode</span><span class="sxs-lookup"><span data-stu-id="9ee3d-103">ISCardCmd::Clear method</span></span>

<span data-ttu-id="9ee3d-104">\[Die **Clear** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="9ee3d-104">\[The **Clear** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="9ee3d-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9ee3d-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="9ee3d-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="9ee3d-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="9ee3d-107">Die **Clear** -Methode löscht die APDU ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) )-und [*Antwort-APDU*](../secgloss/r-gly.md) -Nachrichten Puffer.</span><span class="sxs-lookup"><span data-stu-id="9ee3d-107">The **Clear** method clears the [*application protocol data unit*](../secgloss/a-gly.md) (APDU) and [*reply APDU*](../secgloss/r-gly.md) message buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ee3d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ee3d-108">Syntax</span></span>


```C++
HRESULT Clear();
```



## <a name="parameters"></a><span data-ttu-id="9ee3d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="9ee3d-109">Parameters</span></span>

<span data-ttu-id="9ee3d-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="9ee3d-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9ee3d-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9ee3d-111">Return value</span></span>

<span data-ttu-id="9ee3d-112">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="9ee3d-112">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="9ee3d-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="9ee3d-113">Return code</span></span>                                                                             | <span data-ttu-id="9ee3d-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9ee3d-114">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="9ee3d-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9ee3d-115"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="9ee3d-116">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="9ee3d-116">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="9ee3d-117"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="9ee3d-117"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="9ee3d-118">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="9ee3d-118">Unknown error.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="9ee3d-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9ee3d-119">Remarks</span></span>

<span data-ttu-id="9ee3d-120">Zum Erstellen eines Befehls-APDU rufe Sie [**buildcmd**](iscardcmd-buildcmd.md)auf.</span><span class="sxs-lookup"><span data-stu-id="9ee3d-120">To build a command APDU, call [**BuildCmd**](iscardcmd-buildcmd.md).</span></span>

<span data-ttu-id="9ee3d-121">Eine Liste aller Methoden, die von dieser Schnittstelle bereitgestellt werden, finden Sie unter [**iscardcmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="9ee3d-121">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="9ee3d-122">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="9ee3d-122">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="9ee3d-123">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="9ee3d-123">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="9ee3d-124">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9ee3d-124">Examples</span></span>

<span data-ttu-id="9ee3d-125">Im folgenden Beispiel wird gezeigt, wie die APDU-Nachrichten Puffer für APDU und Reply gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="9ee3d-125">The following example shows how to clear the APDU and reply APDU message buffers.</span></span>


```C++
HRESULT  hr;

hr = pISCardCmd->Clear();
if (FAILED(hr))
{
    printf("Failed ISCardCmd::Clear\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="9ee3d-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9ee3d-126">Requirements</span></span>



| <span data-ttu-id="9ee3d-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9ee3d-127">Requirement</span></span> | <span data-ttu-id="9ee3d-128">Wert</span><span class="sxs-lookup"><span data-stu-id="9ee3d-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ee3d-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9ee3d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="9ee3d-130">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9ee3d-130">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="9ee3d-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9ee3d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="9ee3d-132">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9ee3d-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9ee3d-133">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="9ee3d-133">End of client support</span></span><br/>    | <span data-ttu-id="9ee3d-134">Windows XP</span><span class="sxs-lookup"><span data-stu-id="9ee3d-134">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="9ee3d-135">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="9ee3d-135">End of server support</span></span><br/>    | <span data-ttu-id="9ee3d-136">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9ee3d-136">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="9ee3d-137">Header</span><span class="sxs-lookup"><span data-stu-id="9ee3d-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ee3d-138"><dt>"Scarddat. h"</dt></span><span class="sxs-lookup"><span data-stu-id="9ee3d-138"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="9ee3d-139">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="9ee3d-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="9ee3d-140"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9ee3d-140"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9ee3d-141">DLL</span><span class="sxs-lookup"><span data-stu-id="9ee3d-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ee3d-142"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ee3d-142"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="9ee3d-143">IID</span><span class="sxs-lookup"><span data-stu-id="9ee3d-143">IID</span></span><br/>                      | <span data-ttu-id="9ee3d-144">IID \_ iscardcmd ist als D5778AE3-43DE-11D0-9171-00AA00C18068 definiert.</span><span class="sxs-lookup"><span data-stu-id="9ee3d-144">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="9ee3d-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9ee3d-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ee3d-146">**Iscardcmd:: buildcmd**</span><span class="sxs-lookup"><span data-stu-id="9ee3d-146">**ISCardCmd::BuildCmd**</span></span>](iscardcmd-buildcmd.md)
</dt> <dt>

[<span data-ttu-id="9ee3d-147">**Iscardcmd**</span><span class="sxs-lookup"><span data-stu-id="9ee3d-147">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
