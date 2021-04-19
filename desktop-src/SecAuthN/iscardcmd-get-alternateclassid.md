---
description: Ruft den Wert der alternativen Klassen-ID ab.
ms.assetid: 80c7cbba-e28d-4973-9f3f-7636ff331b64
title: 'Iscardcmd:: get_AlternateClassId-Methode (scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_AlternateClassId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 8cfc47011881ae3e3f6df5ef51c910899a054f84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363335"
---
# <a name="iscardcmdget_alternateclassid-method"></a><span data-ttu-id="4c8a0-103">Iscardcmd:: get- \_ Methode "alternative Methode"</span><span class="sxs-lookup"><span data-stu-id="4c8a0-103">ISCardCmd::get\_AlternateClassId method</span></span>

<span data-ttu-id="4c8a0-104">\[Die Methode " **get \_ Alternativen Klassifizierungs d** " ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="4c8a0-104">\[The **get\_AlternateClassId** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="4c8a0-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4c8a0-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="4c8a0-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="4c8a0-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="4c8a0-107">Die Methode **Get Alternate \_ -lassid** Ruft den Wert der alternativen Klassen-ID ab.</span><span class="sxs-lookup"><span data-stu-id="4c8a0-107">The **get\_AlternateClassId** method retrieves the value of the alternate class ID.</span></span> <span data-ttu-id="4c8a0-108">Bei dieser Methode tritt ein Fehler auf, es sei [**denn, die \_**](iscardcmd-put-alternateclassid.md)Alternative ID wurde durch einen vorherigen-Befehl von Set Alternate</span><span class="sxs-lookup"><span data-stu-id="4c8a0-108">This method will fail unless the alternate ID has been set by a previous call to [**put\_AlternateClassId**](iscardcmd-put-alternateclassid.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4c8a0-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="4c8a0-109">Syntax</span></span>


```C++
HRESULT get_AlternateClassId(
  [out] BYTE *pbyClass
);
```



## <a name="parameters"></a><span data-ttu-id="4c8a0-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4c8a0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c8a0-111">*pbyclass* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="4c8a0-111">*pbyClass* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4c8a0-112">Zeiger auf das Byte, das bei Rückgabe den Wert der alternativen Klassen-ID enthält.</span><span class="sxs-lookup"><span data-stu-id="4c8a0-112">Pointer to the byte that contains the alternate class ID value on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c8a0-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4c8a0-113">Return value</span></span>

<span data-ttu-id="4c8a0-114">Die-Methode gibt die folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="4c8a0-114">The method returns the following possible values.</span></span>



| <span data-ttu-id="4c8a0-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="4c8a0-115">Return code</span></span>                                                                                    | <span data-ttu-id="4c8a0-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4c8a0-116">Description</span></span>                                                                                                                                 |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4c8a0-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4c8a0-117"><dt>**S\_OK**</dt></span></span> </dl>           | <span data-ttu-id="4c8a0-118">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="4c8a0-118">Operation was completed successfully.</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="4c8a0-119"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="4c8a0-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>   | <span data-ttu-id="4c8a0-120">Der *pbyclass* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="4c8a0-120">The *pbyClass* parameter is not valid.</span></span><br/>                                                                                           |
| <dl> <span data-ttu-id="4c8a0-121"><dt>**E \_ AccessDenied**</dt></span><span class="sxs-lookup"><span data-stu-id="4c8a0-121"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl> | <span data-ttu-id="4c8a0-122">Die Alternative Klassen-ID wurde zuvor nicht durch einen-Befehl zum Einfügen von ' Alternate [**\_ -lassid**](iscardcmd-put-alternateclassid.md)' festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4c8a0-122">The alternate class ID has not been previously set by a call to [**put\_AlternateClassId**](iscardcmd-put-alternateclassid.md).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4c8a0-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4c8a0-123">Remarks</span></span>

<span data-ttu-id="4c8a0-124">Diese Methode gilt für die Kommunikation mit dem [*Protokoll T = 0*](../secgloss/t-gly.md).</span><span class="sxs-lookup"><span data-stu-id="4c8a0-124">This method applies to communications using the [*T=0 protocol*](../secgloss/t-gly.md).</span></span> <span data-ttu-id="4c8a0-125">Weitere Informationen finden Sie unter [**Put \_ -Alternativen**](iscardcmd-put-alternateclassid.md).</span><span class="sxs-lookup"><span data-stu-id="4c8a0-125">For more information, see [**put\_AlternateClassId**](iscardcmd-put-alternateclassid.md).</span></span>

## <a name="examples"></a><span data-ttu-id="4c8a0-126">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4c8a0-126">Examples</span></span>

<span data-ttu-id="4c8a0-127">Im folgenden Beispiel wird gezeigt, wie die Alternative Klassen-ID abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="4c8a0-127">The following example shows how to retrieve the alternate class ID.</span></span> <span data-ttu-id="4c8a0-128">Im Beispiel wird davon ausgegangen, dass "piscardcmd" ein gültiger Zeiger auf eine Instanz der [**iscardcmd**](iscardcmd.md) -Schnittstelle ist.</span><span class="sxs-lookup"><span data-stu-id="4c8a0-128">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
BYTE     byAltClassID;
HRESULT  hr;

// Retrieve the alternate class ID.
hr = pISCardCmd->get_AlternateClassId(&byAltClassID);
if (FAILED(hr))
{
  printf("Failed get_AltClassId\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="4c8a0-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4c8a0-129">Requirements</span></span>



| <span data-ttu-id="4c8a0-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4c8a0-130">Requirement</span></span> | <span data-ttu-id="4c8a0-131">Wert</span><span class="sxs-lookup"><span data-stu-id="4c8a0-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4c8a0-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4c8a0-132">Minimum supported client</span></span><br/> | <span data-ttu-id="4c8a0-133">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4c8a0-133">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="4c8a0-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4c8a0-134">Minimum supported server</span></span><br/> | <span data-ttu-id="4c8a0-135">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4c8a0-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4c8a0-136">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="4c8a0-136">End of client support</span></span><br/>    | <span data-ttu-id="4c8a0-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="4c8a0-137">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="4c8a0-138">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="4c8a0-138">End of server support</span></span><br/>    | <span data-ttu-id="4c8a0-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4c8a0-139">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="4c8a0-140">Header</span><span class="sxs-lookup"><span data-stu-id="4c8a0-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c8a0-141"><dt>"Scarddat. h"</dt></span><span class="sxs-lookup"><span data-stu-id="4c8a0-141"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="4c8a0-142">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="4c8a0-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="4c8a0-143"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4c8a0-143"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4c8a0-144">DLL</span><span class="sxs-lookup"><span data-stu-id="4c8a0-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4c8a0-145"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c8a0-145"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="4c8a0-146">IID</span><span class="sxs-lookup"><span data-stu-id="4c8a0-146">IID</span></span><br/>                      | <span data-ttu-id="4c8a0-147">IID \_ iscardcmd ist als D5778AE3-43DE-11D0-9171-00AA00C18068 definiert.</span><span class="sxs-lookup"><span data-stu-id="4c8a0-147">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="4c8a0-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4c8a0-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c8a0-149">**Iscardcmd**</span><span class="sxs-lookup"><span data-stu-id="4c8a0-149">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="4c8a0-150">**" \_ Alternative" platzieren**</span><span class="sxs-lookup"><span data-stu-id="4c8a0-150">**put\_AlternateClassId**</span></span>](iscardcmd-put-alternateclassid.md)
</dt> </dl>

 

 
