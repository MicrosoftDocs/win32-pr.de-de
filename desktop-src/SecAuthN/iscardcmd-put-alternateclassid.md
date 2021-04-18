---
description: Gibt einen neuen alternativen Klassen Bezeichner in APDU (Application Protocol Data Unit) an.
ms.assetid: 45a49699-41ce-439c-b896-e663a290b188
title: Iscardcmd::p ut_AlternateClassId-Methode (scarddat. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_AlternateClassId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: ee1ee5da5875ec2fa1f4f7f6e474f551befdaf8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343306"
---
# <a name="iscardcmdput_alternateclassid-method"></a><span data-ttu-id="7004c-103">Iscardcmd::p UT \_ -Methode "alternative Methode"</span><span class="sxs-lookup"><span data-stu-id="7004c-103">ISCardCmd::put\_AlternateClassId method</span></span>

<span data-ttu-id="7004c-104">\[Die **Put \_ -** Methode "Alternativen" ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="7004c-104">\[The **put\_AlternateClassId** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="7004c-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7004c-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="7004c-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="7004c-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="7004c-107">Die **Put Alternate \_ eclassid-** Methode gibt einen neuen alternativen Klassen Bezeichner in der [*Anwendungsprotokoll Daten-Einheit*](../secgloss/a-gly.md) (APDU) an.</span><span class="sxs-lookup"><span data-stu-id="7004c-107">The **put\_AlternateClassId** method specifies a new alternate class identifier in the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="7004c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="7004c-108">Syntax</span></span>


```C++
HRESULT put_AlternateClassId(
  [in] BYTE byClass
);
```



## <a name="parameters"></a><span data-ttu-id="7004c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="7004c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7004c-110">*byclass* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7004c-110">*byClass* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7004c-111">Alternativer Klassen Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="7004c-111">Alternate class identifier.</span></span> <span data-ttu-id="7004c-112">Der Standardwert ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="7004c-112">The default value is zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7004c-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7004c-113">Return value</span></span>

<span data-ttu-id="7004c-114">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="7004c-114">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="7004c-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="7004c-115">Return code</span></span>                                                                                  | <span data-ttu-id="7004c-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7004c-116">Description</span></span>                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="7004c-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7004c-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="7004c-118">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="7004c-118">Operation completed successfully.</span></span><br/>     |
| <dl> <span data-ttu-id="7004c-119"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="7004c-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="7004c-120">Der *byclass* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="7004c-120">The *byClass* parameter is not valid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7004c-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7004c-121">Remarks</span></span>

<span data-ttu-id="7004c-122">Bei der Kommunikation mit dem [*T = 0-Protokoll*](../secgloss/t-gly.md)können zusätzliche Karten Befehle automatisch von APDU generiert und an die Übertragungsprotokoll-Dateneinheit gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="7004c-122">With communications using the [*T=0 protocol*](../secgloss/t-gly.md), additional card commands can be automatically generated by the APDU and sent to the transmission protocol data unit (TPDU).</span></span> <span data-ttu-id="7004c-123">Die zusätzlichen Befehle verwenden normalerweise dieselbe Klassen-ID wie der ursprüngliche Befehl. durch die Angabe einer neuen Klassen-ID mithilfe dieser Methode können automatisch generierte Befehle die neue Klassen-ID verwenden.</span><span class="sxs-lookup"><span data-stu-id="7004c-123">The additional commands typically use the same class ID as the original command; specifying a new class ID by means of this method allows automatically generated commands to use the new class ID.</span></span>

## <a name="examples"></a><span data-ttu-id="7004c-124">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7004c-124">Examples</span></span>

<span data-ttu-id="7004c-125">Im folgenden Beispiel wird gezeigt, wie Sie einen neuen alternativen Klassen Bezeichner in der [*Anwendungsprotokoll Daten-Einheit (Application Protocol Data Unit*](../secgloss/a-gly.md) , APDU) festlegen.</span><span class="sxs-lookup"><span data-stu-id="7004c-125">The following example shows how to set a new alternate class identifier in the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="7004c-126">Im Beispiel wird davon ausgegangen, dass "piscardcmd" ein gültiger Zeiger auf eine Instanz der [**iscardcmd**](iscardcmd.md) -Schnittstelle ist.</span><span class="sxs-lookup"><span data-stu-id="7004c-126">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
HRESULT  hr;

// Set the class ID.
hr = pISCardCmd->put_AlternateClassId(0xC0);
if (FAILED(hr))
{
  printf("Failed put_AlternateClassId\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="7004c-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7004c-127">Requirements</span></span>



| <span data-ttu-id="7004c-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7004c-128">Requirement</span></span> | <span data-ttu-id="7004c-129">Wert</span><span class="sxs-lookup"><span data-stu-id="7004c-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7004c-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7004c-130">Minimum supported client</span></span><br/> | <span data-ttu-id="7004c-131">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7004c-131">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="7004c-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7004c-132">Minimum supported server</span></span><br/> | <span data-ttu-id="7004c-133">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7004c-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7004c-134">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="7004c-134">End of client support</span></span><br/>    | <span data-ttu-id="7004c-135">Windows XP</span><span class="sxs-lookup"><span data-stu-id="7004c-135">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="7004c-136">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="7004c-136">End of server support</span></span><br/>    | <span data-ttu-id="7004c-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7004c-137">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="7004c-138">Header</span><span class="sxs-lookup"><span data-stu-id="7004c-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="7004c-139"><dt>"Scarddat. h"</dt></span><span class="sxs-lookup"><span data-stu-id="7004c-139"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="7004c-140">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="7004c-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="7004c-141"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7004c-141"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7004c-142">DLL</span><span class="sxs-lookup"><span data-stu-id="7004c-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7004c-143"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7004c-143"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="7004c-144">IID</span><span class="sxs-lookup"><span data-stu-id="7004c-144">IID</span></span><br/>                      | <span data-ttu-id="7004c-145">IID \_ iscardcmd ist als D5778AE3-43DE-11D0-9171-00AA00C18068 definiert.</span><span class="sxs-lookup"><span data-stu-id="7004c-145">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="7004c-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7004c-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7004c-147">**Iscardcmd**</span><span class="sxs-lookup"><span data-stu-id="7004c-147">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="7004c-148">**\_Alternative zum abwechseln**</span><span class="sxs-lookup"><span data-stu-id="7004c-148">**get\_AlternateClassId**</span></span>](iscardcmd-get-alternateclassid.md)
</dt> </dl>

 

 
