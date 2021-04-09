---
title: Ienumbackgroundcopyfiles Reset-Methode (deliveryoptimization. h)
description: Setzt die Enumerationsfolge auf den Anfang zurück.
ms.assetid: 6A303069-105C-4053-A8C5-2ECF60E789DE
keywords:
- Reset-Methode
- Reset-Methode, ienumbackgroundcopyfiles-Schnittstelle
- Ienumbackgroundcopyfiles-Schnittstelle, Reset-Methode
topic_type:
- apiref
api_name:
- IEnumBackgroundCopyFiles.Reset
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 314c7cae44ae48402642c202a624b9a60590e55b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858800"
---
# <a name="ienumbackgroundcopyfilesreset-method"></a><span data-ttu-id="ef19b-106">Ienumbackgroundcopyfiles:: Reset-Methode</span><span class="sxs-lookup"><span data-stu-id="ef19b-106">IEnumBackgroundCopyFiles::Reset method</span></span>

<span data-ttu-id="ef19b-107">Setzt die Enumerationsfolge auf den Anfang zurück.</span><span class="sxs-lookup"><span data-stu-id="ef19b-107">Resets the enumeration sequence to the beginning.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef19b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ef19b-108">Syntax</span></span>


```C++
HRESULT Reset();
```



## <a name="parameters"></a><span data-ttu-id="ef19b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ef19b-109">Parameters</span></span>

<span data-ttu-id="ef19b-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="ef19b-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ef19b-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ef19b-111">Return value</span></span>

<span data-ttu-id="ef19b-112">Diese Methode gibt **S_OK** bei Erfolg oder einen der standardmäßigen com **HRESULT** -Werte bei einem Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="ef19b-112">This method returns **S_OK** on success or one of the standard COM **HRESULT** values on error.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef19b-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ef19b-113">Requirements</span></span>



| <span data-ttu-id="ef19b-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ef19b-114">Requirement</span></span> | <span data-ttu-id="ef19b-115">Wert</span><span class="sxs-lookup"><span data-stu-id="ef19b-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef19b-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ef19b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ef19b-117">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ef19b-117">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="ef19b-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ef19b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ef19b-119">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ef19b-119">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="ef19b-120">Header</span><span class="sxs-lookup"><span data-stu-id="ef19b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef19b-121"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef19b-121"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="ef19b-122">IDL</span><span class="sxs-lookup"><span data-stu-id="ef19b-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ef19b-123"><dt>Deliveryoptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ef19b-123"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="ef19b-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ef19b-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="ef19b-125"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ef19b-125"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="ef19b-126">DLL</span><span class="sxs-lookup"><span data-stu-id="ef19b-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef19b-127"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef19b-127"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="ef19b-128">IID</span><span class="sxs-lookup"><span data-stu-id="ef19b-128">IID</span></span><br/>                      | <span data-ttu-id="ef19b-129">IID_IEnumBackgroundCopyFiles ist als CA51E165-C365-424C-8D41-24AAA4FF3C40 definiert.</span><span class="sxs-lookup"><span data-stu-id="ef19b-129">IID_IEnumBackgroundCopyFiles is defined as CA51E165-C365-424C-8D41-24AAA4FF3C40</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="ef19b-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ef19b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef19b-131">**Ienumbackgroundcopyfiles**</span><span class="sxs-lookup"><span data-stu-id="ef19b-131">**IEnumBackgroundCopyFiles**</span></span>](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

 





