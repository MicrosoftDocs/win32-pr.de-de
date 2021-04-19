---
description: Erstellt eine iscardauth-Schnittstelle.
ms.assetid: a091e361-416e-45c9-8077-617b16db654c
title: 'Iscardmanage:: featecardauth-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.CreateCardAuth
api_type:
- COM
api_location: ''
ms.openlocfilehash: d0b81fd8211491527f39999c6873f7b047bcb32f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373112"
---
# <a name="iscardmanagecreatecardauth-method"></a><span data-ttu-id="84909-103">Iscardmanage:: featecardauth-Methode</span><span class="sxs-lookup"><span data-stu-id="84909-103">ISCardManage::CreateCardAuth method</span></span>

<span data-ttu-id="84909-104">\[Die Methode " **kreatecardauth** " ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="84909-104">\[The **CreateCardAuth** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="84909-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="84909-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="84909-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="84909-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="84909-107">Die Methode " **kreatecardauth** " erstellt eine [**iscardauth**](iscardauth.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="84909-107">The **CreateCardAuth** method creates an [**ISCardAuth**](iscardauth.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="84909-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="84909-108">Syntax</span></span>


```C++
HRESULT CreateCardAuth(
  [out] ISCardAuth **ppISCardAuth
);
```



## <a name="parameters"></a><span data-ttu-id="84909-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="84909-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84909-110">*ppiscardauth* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="84909-110">*ppISCardAuth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="84909-111">Der Zeiger auf die erstellte Schnittstelle wurde zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="84909-111">Returned pointer to the created interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84909-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="84909-112">Return value</span></span>

<span data-ttu-id="84909-113">Die-Methode gibt einen der folgenden möglichen Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="84909-113">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="84909-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="84909-114">Return code</span></span>                                                                                   | <span data-ttu-id="84909-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="84909-115">Description</span></span>                                            |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <span data-ttu-id="84909-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="84909-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="84909-117">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="84909-117">Operation completed successfully.</span></span><br/>           |
| <dl> <span data-ttu-id="84909-118"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="84909-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="84909-119">Der *ppiscardauth* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="84909-119">The *ppISCardAuth* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="84909-120"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="84909-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="84909-121">Ein fehlerhafter Zeiger wurde in *ppiscardauth* übergeben.</span><span class="sxs-lookup"><span data-stu-id="84909-121">A bad pointer was passed in *ppISCardAuth*.</span></span><br/> |
| <dl> <span data-ttu-id="84909-122"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="84909-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="84909-123">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="84909-123">Out of memory.</span></span><br/>                              |



 

## <a name="remarks"></a><span data-ttu-id="84909-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="84909-124">Remarks</span></span>

<span data-ttu-id="84909-125">Eine Liste aller Methoden, die durch diese Schnittstelle definiert werden, finden Sie unter [**iscardmanage**](iscardmanage.md).</span><span class="sxs-lookup"><span data-stu-id="84909-125">For a list of all the methods defined by this interface, see [**ISCardManage**](iscardmanage.md).</span></span>

<span data-ttu-id="84909-126">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die [*Smartcard*](../secgloss/s-gly.md) zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="84909-126">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="84909-127">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="84909-127">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="84909-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="84909-128">Requirements</span></span>



| <span data-ttu-id="84909-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="84909-129">Requirement</span></span> | <span data-ttu-id="84909-130">Wert</span><span class="sxs-lookup"><span data-stu-id="84909-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="84909-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="84909-131">Minimum supported client</span></span><br/> | <span data-ttu-id="84909-132">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="84909-132">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="84909-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="84909-133">Minimum supported server</span></span><br/> | <span data-ttu-id="84909-134">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="84909-134">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="84909-135">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="84909-135">End of client support</span></span><br/>    | <span data-ttu-id="84909-136">Windows XP</span><span class="sxs-lookup"><span data-stu-id="84909-136">Windows XP</span></span><br/>                                |
| <span data-ttu-id="84909-137">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="84909-137">End of server support</span></span><br/>    | <span data-ttu-id="84909-138">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="84909-138">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="84909-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="84909-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84909-140">**Iscardmanage**</span><span class="sxs-lookup"><span data-stu-id="84909-140">**ISCardManage**</span></span>](iscardmanage.md)
</dt> </dl>

 

 
