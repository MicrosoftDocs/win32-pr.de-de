---
description: Gibt das Le-Feld der Application Protocol Data Unit (APDU) zurück.
ms.assetid: 249e8105-273b-42f0-9427-9b3cda5bf0a1
title: 'Iscardcmd:: get_LeField-Methode (scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_LeField
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: bc35f2686a32ce07e1ca630d3ccad3c47b36ca2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760111"
---
# <a name="iscardcmdget_lefield-method"></a><span data-ttu-id="7da61-103">Iscardcmd:: get \_ lefield-Methode</span><span class="sxs-lookup"><span data-stu-id="7da61-103">ISCardCmd::get\_LeField method</span></span>

<span data-ttu-id="7da61-104">\[Die **get \_ lefield** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="7da61-104">\[The **get\_LeField** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="7da61-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7da61-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="7da61-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="7da61-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="7da61-107">Die **get \_ lefield** -Methode gibt das Le-Feld der [*Application Protocol Data Unit*](../secgloss/a-gly.md) (APDU) zurück.</span><span class="sxs-lookup"><span data-stu-id="7da61-107">The **get\_LeField** method returns the Le field of the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="7da61-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="7da61-108">Syntax</span></span>


```C++
HRESULT get_LeField(
  [out] LONG *plSize
);
```



## <a name="parameters"></a><span data-ttu-id="7da61-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="7da61-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7da61-110">*plsize* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7da61-110">*plSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7da61-111">Zeiger auf den Wert des Le-Felds bei Rückgabe.</span><span class="sxs-lookup"><span data-stu-id="7da61-111">Pointer to the Le field value on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7da61-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7da61-112">Return value</span></span>

<span data-ttu-id="7da61-113">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="7da61-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="7da61-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="7da61-114">Return code</span></span>                                                                                  | <span data-ttu-id="7da61-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7da61-115">Description</span></span>                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="7da61-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7da61-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="7da61-117">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="7da61-117">Operation was completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="7da61-118"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="7da61-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="7da61-119">Der *plsize* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="7da61-119">The *plSize* parameter is not valid.</span></span><br/>  |



 

## <a name="examples"></a><span data-ttu-id="7da61-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7da61-120">Examples</span></span>

<span data-ttu-id="7da61-121">Im folgenden Beispiel wird gezeigt, wie der Wert des Le-Felds aus der [*Anwendungsprotokoll Daten-Einheit*](../secgloss/a-gly.md)</span><span class="sxs-lookup"><span data-stu-id="7da61-121">The following example shows how to retrieve the Le field value from the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="7da61-122">Im Beispiel wird davon ausgegangen, dass "piscardcmd" ein gültiger Zeiger auf eine Instanz der [**iscardcmd**](iscardcmd.md) -Schnittstelle ist.</span><span class="sxs-lookup"><span data-stu-id="7da61-122">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
LONG     lLe;
HRESULT  hr;

// Retrieve the Le field value.
hr = pISCardCmd->get_LeField(&lLe);
if (FAILED(hr))
{
    printf("Failed get_LeField\n");
    // Take other error handling action.
}
else
    printf("Le field value returned is %d\n", lLe);
```



## <a name="requirements"></a><span data-ttu-id="7da61-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7da61-123">Requirements</span></span>



| <span data-ttu-id="7da61-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7da61-124">Requirement</span></span> | <span data-ttu-id="7da61-125">Wert</span><span class="sxs-lookup"><span data-stu-id="7da61-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7da61-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7da61-126">Minimum supported client</span></span><br/> | <span data-ttu-id="7da61-127">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7da61-127">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="7da61-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7da61-128">Minimum supported server</span></span><br/> | <span data-ttu-id="7da61-129">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7da61-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7da61-130">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="7da61-130">End of client support</span></span><br/>    | <span data-ttu-id="7da61-131">Windows XP</span><span class="sxs-lookup"><span data-stu-id="7da61-131">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="7da61-132">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="7da61-132">End of server support</span></span><br/>    | <span data-ttu-id="7da61-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7da61-133">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="7da61-134">Header</span><span class="sxs-lookup"><span data-stu-id="7da61-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="7da61-135"><dt>"Scarddat. h"</dt></span><span class="sxs-lookup"><span data-stu-id="7da61-135"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="7da61-136">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="7da61-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="7da61-137"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7da61-137"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7da61-138">DLL</span><span class="sxs-lookup"><span data-stu-id="7da61-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7da61-139"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7da61-139"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="7da61-140">IID</span><span class="sxs-lookup"><span data-stu-id="7da61-140">IID</span></span><br/>                      | <span data-ttu-id="7da61-141">IID \_ iscardcmd ist als D5778AE3-43DE-11D0-9171-00AA00C18068 definiert.</span><span class="sxs-lookup"><span data-stu-id="7da61-141">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="7da61-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7da61-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7da61-143">**Iscardcmd**</span><span class="sxs-lookup"><span data-stu-id="7da61-143">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
