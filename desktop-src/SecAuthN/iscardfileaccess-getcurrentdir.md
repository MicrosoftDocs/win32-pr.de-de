---
description: Die getcurrentdir-Methode gibt einen absoluten Pfad zum aktuell ausgewählten Verzeichnis zurück.
ms.assetid: 12196143-a98a-4772-a803-d0c9b95a66e4
title: 'Iscardfileaccess:: getcurrentdir-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.GetCurrentDir
api_type:
- COM
api_location: ''
ms.openlocfilehash: a779dca10a94250bf4b500585b8b50238b0267dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218507"
---
# <a name="iscardfileaccessgetcurrentdir-method"></a><span data-ttu-id="57a23-103">Iscardfileaccess:: getcurrentdir-Methode</span><span class="sxs-lookup"><span data-stu-id="57a23-103">ISCardFileAccess::GetCurrentDir method</span></span>

<span data-ttu-id="57a23-104">\[Die **getcurrentdir** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="57a23-104">\[The **GetCurrentDir** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="57a23-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="57a23-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="57a23-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="57a23-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="57a23-107">Die **getcurrentdir** -Methode gibt einen absoluten Pfad zum aktuell ausgewählten Verzeichnis zurück.</span><span class="sxs-lookup"><span data-stu-id="57a23-107">The **GetCurrentDir** method returns an absolute path to the currently selected directory.</span></span>

## <a name="syntax"></a><span data-ttu-id="57a23-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="57a23-108">Syntax</span></span>


```C++
HRESULT GetCurrentDir(
  [out] BSTR *pbstrPathSpec
);
```



## <a name="parameters"></a><span data-ttu-id="57a23-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="57a23-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57a23-110">*pbstrinpathspec* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="57a23-110">*pbstrPathSpec* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="57a23-111">Zeiger auf einen BSTR-Wert, der den Pfad enthält.</span><span class="sxs-lookup"><span data-stu-id="57a23-111">Pointer to a BSTR that will contain the path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57a23-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="57a23-112">Return value</span></span>

<span data-ttu-id="57a23-113">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="57a23-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="57a23-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="57a23-114">Return code</span></span>                                                                                   | <span data-ttu-id="57a23-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="57a23-115">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="57a23-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="57a23-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="57a23-117">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="57a23-117">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="57a23-118"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="57a23-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="57a23-119">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="57a23-119">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="57a23-120"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="57a23-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="57a23-121">Es wurde ein fehlerhafter Zeiger übermittelt.</span><span class="sxs-lookup"><span data-stu-id="57a23-121">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="57a23-122"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="57a23-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="57a23-123">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="57a23-123">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="57a23-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="57a23-124">Remarks</span></span>

<span data-ttu-id="57a23-125">Um das aktuelle Verzeichnis zu ändern, nennen Sie [**changedir**](iscardfileaccess-changedir.md).</span><span class="sxs-lookup"><span data-stu-id="57a23-125">To change the current directory, call [**ChangeDir**](iscardfileaccess-changedir.md).</span></span>

<span data-ttu-id="57a23-126">Eine Liste aller Methoden, die durch diese Schnittstelle definiert werden, finden Sie unter [**iscardfileaccess**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="57a23-126">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="57a23-127">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die [*Smartcard*](../secgloss/s-gly.md) zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="57a23-127">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="57a23-128">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="57a23-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="57a23-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="57a23-129">Requirements</span></span>



| <span data-ttu-id="57a23-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="57a23-130">Requirement</span></span> | <span data-ttu-id="57a23-131">Wert</span><span class="sxs-lookup"><span data-stu-id="57a23-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="57a23-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="57a23-132">Minimum supported client</span></span><br/> | <span data-ttu-id="57a23-133">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="57a23-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="57a23-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="57a23-134">Minimum supported server</span></span><br/> | <span data-ttu-id="57a23-135">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="57a23-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="57a23-136">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="57a23-136">End of client support</span></span><br/>    | <span data-ttu-id="57a23-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="57a23-137">Windows XP</span></span><br/>                                |
| <span data-ttu-id="57a23-138">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="57a23-138">End of server support</span></span><br/>    | <span data-ttu-id="57a23-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="57a23-139">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="57a23-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="57a23-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57a23-141">**Changedir**</span><span class="sxs-lookup"><span data-stu-id="57a23-141">**ChangeDir**</span></span>](iscardfileaccess-changedir.md)
</dt> <dt>

[<span data-ttu-id="57a23-142">**Iscardfileaccess**</span><span class="sxs-lookup"><span data-stu-id="57a23-142">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> </dl>

 

 
