---
description: Durch die Methode zum erneuten Anfügen wird die Smartcard zurückgesetzt oder erneut initialisiert.
ms.assetid: c9cd9cd7-5ee6-48dc-8460-deb9c827fcc4
title: 'Iscard:: reattach-Methode (scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.ReAttach
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 3f5ff4cd46b2b523b0031e1389b96d9c2c3973a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215111"
---
# <a name="iscardreattach-method"></a><span data-ttu-id="dc21a-103">Iscard:: reattach-Methode</span><span class="sxs-lookup"><span data-stu-id="dc21a-103">ISCard::ReAttach method</span></span>

<span data-ttu-id="dc21a-104">\[Die Methode zum **erneuten Anfügen** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="dc21a-104">\[The **ReAttach** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="dc21a-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="dc21a-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="dc21a-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="dc21a-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="dc21a-107">Durch die Methode zum **erneuten Anfügen** wird die [*Smartcard*](../secgloss/s-gly.md)zurückgesetzt oder erneut initialisiert.</span><span class="sxs-lookup"><span data-stu-id="dc21a-107">The **ReAttach** method resets, or reinitializes, the [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="dc21a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="dc21a-108">Syntax</span></span>


```C++
HRESULT ReAttach(
  [in] SCARD_SHARE_MODES  ShareMode,
  [in] SCARD_DISPOSITIONS InitState
);
```



## <a name="parameters"></a><span data-ttu-id="dc21a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="dc21a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc21a-110">*Share Mode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dc21a-110">*ShareMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc21a-111">Der Modus, in dem die Verbindung mit der Smartcard gemeinsam genutzt oder exklusiv ist.</span><span class="sxs-lookup"><span data-stu-id="dc21a-111">Mode in which to share or exclusively own the connection to the smart card.</span></span>



| <span data-ttu-id="dc21a-112">Wert</span><span class="sxs-lookup"><span data-stu-id="dc21a-112">Value</span></span>                                                                                                                                            | <span data-ttu-id="dc21a-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="dc21a-113">Meaning</span></span>                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EXCLUSIVE"></span><span id="exclusive"></span><dl> <span data-ttu-id="dc21a-114"><dt>**Ausschließliche**</dt></span><span class="sxs-lookup"><span data-stu-id="dc21a-114"><dt>**EXCLUSIVE**</dt></span></span> </dl> | <span data-ttu-id="dc21a-115">Diese Verbindung wird von keiner anderen Person mit der Smartcard verwendet.</span><span class="sxs-lookup"><span data-stu-id="dc21a-115">No one else use this connection to the smart card.</span></span><br/> |
| <span id="SHARED"></span><span id="shared"></span><dl> <span data-ttu-id="dc21a-116"><dt>**Genu**</dt></span><span class="sxs-lookup"><span data-stu-id="dc21a-116"><dt>**SHARED**</dt></span></span> </dl>          | <span data-ttu-id="dc21a-117">Diese Verbindung kann von anderen Anwendungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dc21a-117">Other applications can use this connection.</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="dc21a-118">*Initstate* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dc21a-118">*InitState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc21a-119">Gibt an, was mit der Karte zu tun ist.</span><span class="sxs-lookup"><span data-stu-id="dc21a-119">Indicates what to do with the card.</span></span>



| <span data-ttu-id="dc21a-120">Wert</span><span class="sxs-lookup"><span data-stu-id="dc21a-120">Value</span></span>                                                                                                                                      | <span data-ttu-id="dc21a-121">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="dc21a-121">Meaning</span></span>                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="LEAVE"></span><span id="leave"></span><dl> <span data-ttu-id="dc21a-122"><dt>**Lassen Sie**</dt></span><span class="sxs-lookup"><span data-stu-id="dc21a-122"><dt>**LEAVE**</dt></span></span> </dl>       | <span data-ttu-id="dc21a-123">Verlässt die Smartcard im aktuellen [*Zustand*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="dc21a-123">Leaves the smart card in the current [*state*](../secgloss/s-gly.md).</span></span><br/> |
| <span id="RESET"></span><span id="reset"></span><dl> <span data-ttu-id="dc21a-124"><dt>**Festlegen**</dt></span><span class="sxs-lookup"><span data-stu-id="dc21a-124"><dt>**RESET**</dt></span></span> </dl>       | <span data-ttu-id="dc21a-125">Setzt die Smartcard auf einen bekannten Zustand zurück.</span><span class="sxs-lookup"><span data-stu-id="dc21a-125">Resets the smart card to some known state.</span></span><br/>                                                              |
| <span id="UNPOWER"></span><span id="unpower"></span><dl> <span data-ttu-id="dc21a-126"><dt>**Nicht mehr**</dt></span><span class="sxs-lookup"><span data-stu-id="dc21a-126"><dt>**UNPOWER**</dt></span></span> </dl> | <span data-ttu-id="dc21a-127">Entfernt die Stromversorgung von der Smartcard.</span><span class="sxs-lookup"><span data-stu-id="dc21a-127">Removes power from the smart card.</span></span><br/>                                                                      |
| <span id="EJECT"></span><span id="eject"></span><dl> <span data-ttu-id="dc21a-128"><dt>**Auswerfen**</dt></span><span class="sxs-lookup"><span data-stu-id="dc21a-128"><dt>**EJECT**</dt></span></span> </dl>       | <span data-ttu-id="dc21a-129">Fügt die Smartcard ein, wenn der Reader über Auswerfen-Funktionen verfügt.</span><span class="sxs-lookup"><span data-stu-id="dc21a-129">Ejects the smart card if the reader has eject capabilities.</span></span><br/>                                             |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc21a-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dc21a-130">Return value</span></span>

<span data-ttu-id="dc21a-131">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="dc21a-131">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="dc21a-132">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="dc21a-132">Return code</span></span>                                                                                  | <span data-ttu-id="dc21a-133">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dc21a-133">Description</span></span>                                                                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="dc21a-134"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="dc21a-134"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="dc21a-135">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="dc21a-135">Operation completed successfully.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="dc21a-136"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="dc21a-136"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="dc21a-137">Bei einem oder mehreren Parametern, die an die Funktion weitergegeben wurden, ist ein Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="dc21a-137">There is something wrong with one or more of the parameters passed into the function.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="dc21a-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dc21a-138">Remarks</span></span>

<span data-ttu-id="dc21a-139">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="dc21a-139">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="dc21a-140">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="dc21a-140">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="dc21a-141">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dc21a-141">Examples</span></span>

<span data-ttu-id="dc21a-142">Das folgende Beispiel zeigt, wie die Smartcard erneut initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="dc21a-142">The following example shows reinitializing the smart card.</span></span>


```C++
HRESULT    hr;

// Reattach the smart card.
hr = pISCard->ReAttach(SHARED, LEAVE);
if (FAILED(hr))
{
   printf("Failed ReAttach\n");
   // Take error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="dc21a-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dc21a-143">Requirements</span></span>



| <span data-ttu-id="dc21a-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dc21a-144">Requirement</span></span> | <span data-ttu-id="dc21a-145">Wert</span><span class="sxs-lookup"><span data-stu-id="dc21a-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc21a-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dc21a-146">Minimum supported client</span></span><br/> | <span data-ttu-id="dc21a-147">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dc21a-147">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="dc21a-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dc21a-148">Minimum supported server</span></span><br/> | <span data-ttu-id="dc21a-149">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dc21a-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="dc21a-150">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="dc21a-150">End of client support</span></span><br/>    | <span data-ttu-id="dc21a-151">Windows XP</span><span class="sxs-lookup"><span data-stu-id="dc21a-151">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="dc21a-152">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="dc21a-152">End of server support</span></span><br/>    | <span data-ttu-id="dc21a-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="dc21a-153">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="dc21a-154">Header</span><span class="sxs-lookup"><span data-stu-id="dc21a-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc21a-155"><dt>"Scardmgr. h"</dt></span><span class="sxs-lookup"><span data-stu-id="dc21a-155"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="dc21a-156">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="dc21a-156">Type library</span></span><br/>             | <dl> <span data-ttu-id="dc21a-157"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="dc21a-157"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="dc21a-158">DLL</span><span class="sxs-lookup"><span data-stu-id="dc21a-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc21a-159"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc21a-159"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="dc21a-160">IID</span><span class="sxs-lookup"><span data-stu-id="dc21a-160">IID</span></span><br/>                      | <span data-ttu-id="dc21a-161">IID \_ iscard ist definiert als 1461aac3-6810-11D0-918f -00aa00c18068</span><span class="sxs-lookup"><span data-stu-id="dc21a-161">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="dc21a-162">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dc21a-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc21a-163">**Attachbyhandle**</span><span class="sxs-lookup"><span data-stu-id="dc21a-163">**AttachByHandle**</span></span>](iscard-attachbyhandle.md)
</dt> <dt>

[<span data-ttu-id="dc21a-164">**Attachbyreader**</span><span class="sxs-lookup"><span data-stu-id="dc21a-164">**AttachByReader**</span></span>](iscard-attachbyreader.md)
</dt> <dt>

[<span data-ttu-id="dc21a-165">**Trennen**</span><span class="sxs-lookup"><span data-stu-id="dc21a-165">**Detach**</span></span>](iscard-detach.md)
</dt> <dt>

[<span data-ttu-id="dc21a-166">**Iscard**</span><span class="sxs-lookup"><span data-stu-id="dc21a-166">**ISCard**</span></span>](iscard.md)
</dt> </dl>

 

 
