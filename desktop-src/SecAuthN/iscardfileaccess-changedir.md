---
description: Mit der changedir-Methode wird das aktuelle Smartcardverzeichnis in das neue angegebene Verzeichnis geändert.
ms.assetid: 1eb53236-c88f-4b43-ac91-de67d4029433
title: 'Iscardfileaccess:: changedir-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.ChangeDir
api_type:
- COM
api_location: ''
ms.openlocfilehash: 147456bd705eea3073f2e65cb375494187ca2473
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862628"
---
# <a name="iscardfileaccesschangedir-method"></a><span data-ttu-id="f1c97-103">Iscardfileaccess:: changedir-Methode</span><span class="sxs-lookup"><span data-stu-id="f1c97-103">ISCardFileAccess::ChangeDir method</span></span>

<span data-ttu-id="f1c97-104">\[Die **changedir** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="f1c97-104">\[The **ChangeDir** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f1c97-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f1c97-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f1c97-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="f1c97-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="f1c97-107">Mit der **changedir** -Methode wird das aktuelle [*Smartcardverzeichnis*](../secgloss/s-gly.md) in das neue angegebene Verzeichnis geändert.</span><span class="sxs-lookup"><span data-stu-id="f1c97-107">The **ChangeDir** method changes the current [*smart card*](../secgloss/s-gly.md) directory to the new specified directory.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1c97-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f1c97-108">Syntax</span></span>


```C++
HRESULT ChangeDir(
  [in] REFTYPE refType,
  [in] BSTR    bstrNewDir
);
```



## <a name="parameters"></a><span data-ttu-id="f1c97-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="f1c97-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1c97-110">*RefType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f1c97-110">*refType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1c97-111">Der Referenztyp, der in *bstrinnewdir* verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f1c97-111">Type of reference used in *bstrNewDir*.</span></span>

<dl><span id="SC_TYPE_BY_NAME"></span><span id="sc_type_by_name"></span><dt>

<span data-ttu-id="f1c97-112">**SC- \_ Typ \_ nach \_ Name**</span><span class="sxs-lookup"><span data-stu-id="f1c97-112">**SC\_TYPE\_BY\_NAME**</span></span>
</dt><span id="SC_TYPE_BY_ID"></span><span id="sc_type_by_id"></span><dt>

<span data-ttu-id="f1c97-113">**SC- \_ Typ \_ nach \_ ID**</span><span class="sxs-lookup"><span data-stu-id="f1c97-113">**SC\_TYPE\_BY\_ID**</span></span>
</dt><span id="SC_TYPE_BY_SHORT"></span><span id="sc_type_by_short"></span><dt>

<span data-ttu-id="f1c97-114">**SC \_ - \_ Typ \_ kurz**</span><span class="sxs-lookup"><span data-stu-id="f1c97-114">**SC\_TYPE\_BY\_SHORT**</span></span>
</dt><span id="SC_TYPE_BY_ANY"></span><span id="sc_type_by_any"></span><dt>

<span data-ttu-id="f1c97-115">**SC- \_ Typ \_ nach \_ beliebigen**</span><span class="sxs-lookup"><span data-stu-id="f1c97-115">**SC\_TYPE\_BY\_ANY**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="f1c97-116">*bstrinnewdir* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f1c97-116">*bstrNewDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1c97-117">Der Datei-/Verzeichnisname (von *RefType*), der ausgewählt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f1c97-117">File/directory name (by *refType*) to select.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1c97-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f1c97-118">Return value</span></span>

<span data-ttu-id="f1c97-119">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="f1c97-119">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="f1c97-120">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="f1c97-120">Return code</span></span>                                                                                   | <span data-ttu-id="f1c97-121">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f1c97-121">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="f1c97-122"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f1c97-122"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="f1c97-123">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="f1c97-123">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="f1c97-124"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="f1c97-124"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="f1c97-125">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="f1c97-125">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="f1c97-126"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="f1c97-126"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="f1c97-127">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="f1c97-127">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="f1c97-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f1c97-128">Remarks</span></span>

<span data-ttu-id="f1c97-129">Um einen absoluten Pfad zum aktuell ausgewählten Verzeichnis abzurufen, nennen Sie [**getcurrentdir**](iscardfileaccess-getcurrentdir.md).</span><span class="sxs-lookup"><span data-stu-id="f1c97-129">To get an absolute path to the currently selected directory, call [**GetCurrentDir**](iscardfileaccess-getcurrentdir.md).</span></span>

<span data-ttu-id="f1c97-130">Eine Liste aller Methoden, die durch diese Schnittstelle definiert werden, finden Sie unter [**iscardfileaccess**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="f1c97-130">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="f1c97-131">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="f1c97-131">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="f1c97-132">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="f1c97-132">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f1c97-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f1c97-133">Requirements</span></span>



| <span data-ttu-id="f1c97-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f1c97-134">Requirement</span></span> | <span data-ttu-id="f1c97-135">Wert</span><span class="sxs-lookup"><span data-stu-id="f1c97-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f1c97-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f1c97-136">Minimum supported client</span></span><br/> | <span data-ttu-id="f1c97-137">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f1c97-137">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="f1c97-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f1c97-138">Minimum supported server</span></span><br/> | <span data-ttu-id="f1c97-139">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f1c97-139">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="f1c97-140">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="f1c97-140">End of client support</span></span><br/>    | <span data-ttu-id="f1c97-141">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f1c97-141">Windows XP</span></span><br/>                                |
| <span data-ttu-id="f1c97-142">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="f1c97-142">End of server support</span></span><br/>    | <span data-ttu-id="f1c97-143">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f1c97-143">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="f1c97-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f1c97-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1c97-145">**Getcurrentdir**</span><span class="sxs-lookup"><span data-stu-id="f1c97-145">**GetCurrentDir**</span></span>](iscardfileaccess-getcurrentdir.md)
</dt> <dt>

[<span data-ttu-id="f1c97-146">**Iscardfileaccess**</span><span class="sxs-lookup"><span data-stu-id="f1c97-146">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> </dl>

 

 
