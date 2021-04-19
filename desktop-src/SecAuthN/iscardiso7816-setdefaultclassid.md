---
description: Die setdefaultclassid-Methode weist ein Standard-klassenbezeichnerbyte zu, das bei der Erstellung einer ISO 7816-4-Befehls Anwendungsprotokoll-Dateneinheit (APDU) in allen Vorgängen verwendet wird. Standardmäßig ist das Standard-klassenbezeichnerbyte 0x00.
ms.assetid: 5a53d5f1-7986-4c4c-9512-f592cd398d1c
title: 'ISCardISO7816:: setdefaultclassid-Methode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.SetDefaultClassId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 29e8868f491f0b9a61554da008c4100622815dd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349919"
---
# <a name="iscardiso7816setdefaultclassid-method"></a><span data-ttu-id="27f75-104">ISCardISO7816:: setdefaultclassid-Methode</span><span class="sxs-lookup"><span data-stu-id="27f75-104">ISCardISO7816::SetDefaultClassId method</span></span>

<span data-ttu-id="27f75-105">\[Die **setdefaultclassid-** Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="27f75-105">\[The **SetDefaultClassId** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="27f75-106">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="27f75-106">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="27f75-107">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="27f75-107">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="27f75-108">Die **setdefaultclassid-** Methode weist ein Standard-klassenbezeichnerbyte zu, das bei der Erstellung einer ISO 7816-4-Befehls [*Anwendungsprotokoll-Dateneinheit*](../secgloss/a-gly.md) (APDU) in allen Vorgängen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="27f75-108">The **SetDefaultClassId** method assigns a standard class identifier byte that will be used in all operations when constructing an ISO 7816-4 command [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="27f75-109">Standardmäßig ist das Standard-klassenbezeichnerbyte 0x00.</span><span class="sxs-lookup"><span data-stu-id="27f75-109">By default, the standard class identifier byte is 0x00.</span></span>

## <a name="syntax"></a><span data-ttu-id="27f75-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="27f75-110">Syntax</span></span>


```C++
HRESULT SetDefaultClassId(
  [in] BYTE byClass
);
```



## <a name="parameters"></a><span data-ttu-id="27f75-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="27f75-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27f75-112">*byclass* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="27f75-112">*byClass* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27f75-113">Klassen-ID-Byte.</span><span class="sxs-lookup"><span data-stu-id="27f75-113">Class ID byte.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27f75-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="27f75-114">Return value</span></span>

<span data-ttu-id="27f75-115">Folgende Rückgabewerte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="27f75-115">The possible return values are the following:</span></span>



| <span data-ttu-id="27f75-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="27f75-116">Return code</span></span>                                                                          | <span data-ttu-id="27f75-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="27f75-117">Description</span></span>                                  |
|--------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="27f75-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="27f75-118"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="27f75-119">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="27f75-119">Operation completed successfully.</span></span><br/> |



 

<span data-ttu-id="27f75-120">Eine Liste aller Methoden, die von der [**ISCardISO7816**](iscardiso7816.md) -Schnittstelle bereitgestellt werden, finden Sie unter **ISCardISO7816**.</span><span class="sxs-lookup"><span data-stu-id="27f75-120">For a list of all the methods provided by the [**ISCardISO7816**](iscardiso7816.md) interface, see **ISCardISO7816**.</span></span>

<span data-ttu-id="27f75-121">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die [*Smartcard*](../secgloss/s-gly.md) zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="27f75-121">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="27f75-122">Informationen zu smartcardfehlercodes finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="27f75-122">For information about smart card error codes, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="27f75-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="27f75-123">Requirements</span></span>



| <span data-ttu-id="27f75-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="27f75-124">Requirement</span></span> | <span data-ttu-id="27f75-125">Wert</span><span class="sxs-lookup"><span data-stu-id="27f75-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="27f75-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="27f75-126">Minimum supported client</span></span><br/> | <span data-ttu-id="27f75-127">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="27f75-127">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="27f75-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="27f75-128">Minimum supported server</span></span><br/> | <span data-ttu-id="27f75-129">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="27f75-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="27f75-130">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="27f75-130">End of client support</span></span><br/>    | <span data-ttu-id="27f75-131">Windows XP</span><span class="sxs-lookup"><span data-stu-id="27f75-131">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="27f75-132">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="27f75-132">End of server support</span></span><br/>    | <span data-ttu-id="27f75-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="27f75-133">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="27f75-134">Header</span><span class="sxs-lookup"><span data-stu-id="27f75-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="27f75-135"><dt>"Scardssp. h"</dt></span><span class="sxs-lookup"><span data-stu-id="27f75-135"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="27f75-136">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="27f75-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="27f75-137"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="27f75-137"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="27f75-138">DLL</span><span class="sxs-lookup"><span data-stu-id="27f75-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="27f75-139"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="27f75-139"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="27f75-140">IID</span><span class="sxs-lookup"><span data-stu-id="27f75-140">IID</span></span><br/>                      | <span data-ttu-id="27f75-141">IID \_ ISCardISO7816 ist als 53b6aa68-3F 56-11D0-916b-00aa00c18068 definiert</span><span class="sxs-lookup"><span data-stu-id="27f75-141">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="27f75-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="27f75-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27f75-143">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="27f75-143">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> </dl>

 

 
