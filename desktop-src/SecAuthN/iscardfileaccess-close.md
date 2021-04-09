---
description: Die Close-Methode schließt die angegebene Datei. Es ist kein weiterer Zugriff auf die Datei zulässig.
ms.assetid: fecce23e-8604-4a87-9efb-a26e2498c2f3
title: 'Iscardfileaccess:: Close-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Close
api_type:
- COM
api_location: ''
ms.openlocfilehash: ac08d62e71045df49503eb4c05fcb5ea273b4cf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129321"
---
# <a name="iscardfileaccessclose-method"></a><span data-ttu-id="ec4fc-104">Iscardfileaccess:: Close-Methode</span><span class="sxs-lookup"><span data-stu-id="ec4fc-104">ISCardFileAccess::Close method</span></span>

<span data-ttu-id="ec4fc-105">\[Die **Close** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="ec4fc-105">\[The **Close** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="ec4fc-106">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ec4fc-106">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="ec4fc-107">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="ec4fc-107">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="ec4fc-108">Die **Close** -Methode schließt die angegebene Datei.</span><span class="sxs-lookup"><span data-stu-id="ec4fc-108">The **Close** method closes the specified file.</span></span> <span data-ttu-id="ec4fc-109">Es ist kein weiterer Zugriff auf die Datei zulässig.</span><span class="sxs-lookup"><span data-stu-id="ec4fc-109">No further access to file is allowed.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec4fc-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="ec4fc-110">Syntax</span></span>


```C++
HRESULT Close(
  [in] HSCARD_FILE hFile
);
```



## <a name="parameters"></a><span data-ttu-id="ec4fc-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="ec4fc-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec4fc-112">*hFile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ec4fc-112">*hFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec4fc-113">Ein Handle für die Datei, die geschlossen werden soll.</span><span class="sxs-lookup"><span data-stu-id="ec4fc-113">A handle to the file to be closed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec4fc-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ec4fc-114">Return value</span></span>

<span data-ttu-id="ec4fc-115">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="ec4fc-115">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="ec4fc-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="ec4fc-116">Return code</span></span>                                                                                   | <span data-ttu-id="ec4fc-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ec4fc-117">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="ec4fc-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ec4fc-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="ec4fc-119">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="ec4fc-119">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="ec4fc-120"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="ec4fc-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="ec4fc-121">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="ec4fc-121">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="ec4fc-122"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="ec4fc-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="ec4fc-123">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="ec4fc-123">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="ec4fc-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ec4fc-124">Remarks</span></span>

<span data-ttu-id="ec4fc-125">Um eine Datei zu öffnen, [**Öffnen**](iscardfileaccess-open.md)Sie "Öffnen".</span><span class="sxs-lookup"><span data-stu-id="ec4fc-125">To open a file, call [**Open**](iscardfileaccess-open.md).</span></span>

<span data-ttu-id="ec4fc-126">Eine Liste aller Methoden, die durch diese Schnittstelle definiert werden, finden Sie unter [**iscardfileaccess**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="ec4fc-126">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="ec4fc-127">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die [*Smartcard*](../secgloss/s-gly.md) zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="ec4fc-127">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="ec4fc-128">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="ec4fc-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ec4fc-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ec4fc-129">Requirements</span></span>



| <span data-ttu-id="ec4fc-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ec4fc-130">Requirement</span></span> | <span data-ttu-id="ec4fc-131">Wert</span><span class="sxs-lookup"><span data-stu-id="ec4fc-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ec4fc-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ec4fc-132">Minimum supported client</span></span><br/> | <span data-ttu-id="ec4fc-133">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ec4fc-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="ec4fc-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ec4fc-134">Minimum supported server</span></span><br/> | <span data-ttu-id="ec4fc-135">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ec4fc-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="ec4fc-136">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="ec4fc-136">End of client support</span></span><br/>    | <span data-ttu-id="ec4fc-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ec4fc-137">Windows XP</span></span><br/>                                |
| <span data-ttu-id="ec4fc-138">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="ec4fc-138">End of server support</span></span><br/>    | <span data-ttu-id="ec4fc-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ec4fc-139">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="ec4fc-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ec4fc-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec4fc-141">**Iscardfileaccess**</span><span class="sxs-lookup"><span data-stu-id="ec4fc-141">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> <dt>

[<span data-ttu-id="ec4fc-142">**Eren**</span><span class="sxs-lookup"><span data-stu-id="ec4fc-142">**Open**</span></span>](iscardfileaccess-open.md)
</dt> </dl>

 

 
