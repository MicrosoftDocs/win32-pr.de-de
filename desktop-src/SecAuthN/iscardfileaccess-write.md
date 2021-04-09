---
description: Die Write-Methode schreibt Daten in eine aktuelle geöffnete Datei.
ms.assetid: 0c92af34-a9db-4242-8b6e-d1010a0d7afa
title: 'Iscardfileaccess:: Write-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Write
api_type:
- COM
api_location: ''
ms.openlocfilehash: 48091d39fff49e54d57f5a26fb7d033bfd8e5952
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131453"
---
# <a name="iscardfileaccesswrite-method"></a><span data-ttu-id="6b683-103">Iscardfileaccess:: Write-Methode</span><span class="sxs-lookup"><span data-stu-id="6b683-103">ISCardFileAccess::Write method</span></span>

<span data-ttu-id="6b683-104">\[Die **Write** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="6b683-104">\[The **Write** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6b683-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6b683-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="6b683-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="6b683-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="6b683-107">Die **Write** -Methode schreibt Daten in eine aktuelle geöffnete Datei.</span><span class="sxs-lookup"><span data-stu-id="6b683-107">The **Write** method writes data to a current opened file.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b683-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b683-108">Syntax</span></span>


```C++
HRESULT Write(
  [in] HSCARD_FILE  hFile,
  [in] LPBYTEBUFFER pData,
  [in] SCARD_FLAGS  flags
);
```



## <a name="parameters"></a><span data-ttu-id="6b683-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="6b683-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b683-110">*hFile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6b683-110">*hFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b683-111">Ein Handle für eine geöffnete Datei.</span><span class="sxs-lookup"><span data-stu-id="6b683-111">A handle to an open file.</span></span>

</dd> <dt>

<span data-ttu-id="6b683-112">*pData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6b683-112">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b683-113">Objekt/Daten, die geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6b683-113">Object/data to be written.</span></span>

</dd> <dt>

<span data-ttu-id="6b683-114">*Flags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6b683-114">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b683-115">Gibt an, ob sicheres Messaging verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6b683-115">Specifies whether secure messaging should be used.</span></span>

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

<span data-ttu-id="6b683-116">**SC \_ FL \_ Secure \_ Messaging**</span><span class="sxs-lookup"><span data-stu-id="6b683-116">**SC\_FL\_SECURE\_MESSAGING**</span></span>
</dt> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b683-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6b683-117">Return value</span></span>

<span data-ttu-id="6b683-118">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="6b683-118">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="6b683-119">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="6b683-119">Return code</span></span>                                                                                   | <span data-ttu-id="6b683-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6b683-120">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="6b683-121"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6b683-121"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="6b683-122">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="6b683-122">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="6b683-123"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="6b683-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="6b683-124">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="6b683-124">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="6b683-125"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="6b683-125"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="6b683-126">Es wurde ein fehlerhafter Zeiger übermittelt.</span><span class="sxs-lookup"><span data-stu-id="6b683-126">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="6b683-127"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="6b683-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="6b683-128">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="6b683-128">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="6b683-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6b683-129">Remarks</span></span>

<span data-ttu-id="6b683-130">Um eine Datei zu öffnen oder zu schließen, öffnen Sie " [**Öffnen**](iscardfileaccess-open.md) " oder " [**Schließen**](iscardfileaccess-close.md)".</span><span class="sxs-lookup"><span data-stu-id="6b683-130">To open or close a file, call [**Open**](iscardfileaccess-open.md) or [**Close**](iscardfileaccess-close.md), respectively.</span></span>

<span data-ttu-id="6b683-131">Eine Liste aller Methoden, die durch diese Schnittstelle definiert werden, finden Sie unter [**iscardfileaccess**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="6b683-131">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="6b683-132">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die [*Smartcard*](../secgloss/s-gly.md) zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="6b683-132">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="6b683-133">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="6b683-133">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6b683-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6b683-134">Requirements</span></span>



| <span data-ttu-id="6b683-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6b683-135">Requirement</span></span> | <span data-ttu-id="6b683-136">Wert</span><span class="sxs-lookup"><span data-stu-id="6b683-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6b683-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6b683-137">Minimum supported client</span></span><br/> | <span data-ttu-id="6b683-138">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6b683-138">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="6b683-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6b683-139">Minimum supported server</span></span><br/> | <span data-ttu-id="6b683-140">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6b683-140">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="6b683-141">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="6b683-141">End of client support</span></span><br/>    | <span data-ttu-id="6b683-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6b683-142">Windows XP</span></span><br/>                                |
| <span data-ttu-id="6b683-143">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="6b683-143">End of server support</span></span><br/>    | <span data-ttu-id="6b683-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6b683-144">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="6b683-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6b683-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b683-146">**Schließen**</span><span class="sxs-lookup"><span data-stu-id="6b683-146">**Close**</span></span>](iscardfileaccess-close.md)
</dt> <dt>

[<span data-ttu-id="6b683-147">**Iscardfileaccess**</span><span class="sxs-lookup"><span data-stu-id="6b683-147">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> <dt>

[<span data-ttu-id="6b683-148">**Eren**</span><span class="sxs-lookup"><span data-stu-id="6b683-148">**Open**</span></span>](iscardfileaccess-open.md)
</dt> </dl>

 

 
