---
description: Erstellt eine Datei (EF oder DF), die zuvor mit der Invalidate-Methode, auf die die Anwendung zugreifen kann, nicht gültig war.
ms.assetid: 1906fcc5-ae76-4950-b2eb-e5ce1882637f
title: 'Iscardfileaccess:: rehabiliingmethode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Rehabilitate
api_type:
- COM
api_location: ''
ms.openlocfilehash: 7ed02131de08104dab8aff23ee9054659fd4cd63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360578"
---
# <a name="iscardfileaccessrehabilitate-method"></a><span data-ttu-id="fe7f1-103">Iscardfileaccess:: rehabiliingmethode</span><span class="sxs-lookup"><span data-stu-id="fe7f1-103">ISCardFileAccess::Rehabilitate method</span></span>

<span data-ttu-id="fe7f1-104">\[Die Methode " **Rehabilitation** " ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="fe7f1-104">\[The **Rehabilitate** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="fe7f1-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="fe7f1-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="fe7f1-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="fe7f1-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="fe7f1-107">Mit der Methode " **Rehabilitierung** " wird eine Datei (EF oder DF) erstellt, die zuvor mit der [**Invalidate**](iscardfileaccess-invalidate.md) -Methode, auf die die Anwendung zugreifen kann, nicht gültig war.</span><span class="sxs-lookup"><span data-stu-id="fe7f1-107">The **Rehabilitate** method makes a file (EF or DF) that was previously made not valid by using the [**Invalidate**](iscardfileaccess-invalidate.md) method, accessible by the application.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe7f1-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="fe7f1-108">Syntax</span></span>


```C++
HRESULT Rehabilitate(
  [in] BSTR        bstrPathSpec,
  [in] SCARD_FLAGS flags
);
```



## <a name="parameters"></a><span data-ttu-id="fe7f1-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="fe7f1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe7f1-110">*bstrinpathspec* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fe7f1-110">*bstrPathSpec* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe7f1-111">Die zu rehabilitierte Datei.</span><span class="sxs-lookup"><span data-stu-id="fe7f1-111">File to rehabilitate.</span></span>

</dd> <dt>

<span data-ttu-id="fe7f1-112">*Flags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fe7f1-112">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe7f1-113">Gibt an, ob sicheres Messaging verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="fe7f1-113">Specifies whether secure messaging should be used.</span></span>

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

<span data-ttu-id="fe7f1-114">**SC \_ FL \_ Secure \_ Messaging**</span><span class="sxs-lookup"><span data-stu-id="fe7f1-114">**SC\_FL\_SECURE\_MESSAGING**</span></span>
</dt> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe7f1-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fe7f1-115">Return value</span></span>

<span data-ttu-id="fe7f1-116">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="fe7f1-116">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="fe7f1-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="fe7f1-117">Return code</span></span>                                                                                   | <span data-ttu-id="fe7f1-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fe7f1-118">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="fe7f1-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="fe7f1-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="fe7f1-120">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="fe7f1-120">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="fe7f1-121"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="fe7f1-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="fe7f1-122">Ein Parameter ist nicht gültig.</span><span class="sxs-lookup"><span data-stu-id="fe7f1-122">A parameter is not valid.</span></span><br/>         |
| <dl> <span data-ttu-id="fe7f1-123"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="fe7f1-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="fe7f1-124">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="fe7f1-124">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="fe7f1-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fe7f1-125">Remarks</span></span>

<span data-ttu-id="fe7f1-126">Eine Liste aller Methoden, die durch diese Schnittstelle definiert werden, finden Sie unter [**iscardfileaccess**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="fe7f1-126">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="fe7f1-127">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die [*Smartcard*](../secgloss/s-gly.md) zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="fe7f1-127">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="fe7f1-128">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="fe7f1-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fe7f1-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fe7f1-129">Requirements</span></span>



| <span data-ttu-id="fe7f1-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fe7f1-130">Requirement</span></span> | <span data-ttu-id="fe7f1-131">Wert</span><span class="sxs-lookup"><span data-stu-id="fe7f1-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fe7f1-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fe7f1-132">Minimum supported client</span></span><br/> | <span data-ttu-id="fe7f1-133">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fe7f1-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="fe7f1-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fe7f1-134">Minimum supported server</span></span><br/> | <span data-ttu-id="fe7f1-135">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fe7f1-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="fe7f1-136">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="fe7f1-136">End of client support</span></span><br/>    | <span data-ttu-id="fe7f1-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="fe7f1-137">Windows XP</span></span><br/>                                |
| <span data-ttu-id="fe7f1-138">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="fe7f1-138">End of server support</span></span><br/>    | <span data-ttu-id="fe7f1-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fe7f1-139">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="fe7f1-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fe7f1-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe7f1-141">**Ungültig**</span><span class="sxs-lookup"><span data-stu-id="fe7f1-141">**Invalidate**</span></span>](iscardfileaccess-invalidate.md)
</dt> <dt>

[<span data-ttu-id="fe7f1-142">**Iscardfileaccess**</span><span class="sxs-lookup"><span data-stu-id="fe7f1-142">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> </dl>

 

 
