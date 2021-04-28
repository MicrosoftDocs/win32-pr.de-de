---
title: IEnumBackgroundCopyFiles Reset-Methode (Deliveryoptimization.h)
description: 'IEnumBackgroundCopyFiles::Reset-Methode: Setzt die Enumerationssequenz auf den Anfang zurück.'
ms.assetid: 6A303069-105C-4053-A8C5-2ECF60E789DE
keywords:
- Reset-Methode
- Reset-Methode, IEnumBackgroundCopyFiles-Schnittstelle
- IEnumBackgroundCopyFiles-Schnittstelle, Reset-Methode
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
ms.openlocfilehash: d6800095d0a6f20ef8b632830a224d4da27356bf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105488"
---
# <a name="ienumbackgroundcopyfilesreset-method"></a><span data-ttu-id="71b8f-106">IEnumBackgroundCopyFiles::Reset-Methode</span><span class="sxs-lookup"><span data-stu-id="71b8f-106">IEnumBackgroundCopyFiles::Reset method</span></span>

<span data-ttu-id="71b8f-107">Setzt die Enumerationsfolge auf den Anfang zurück.</span><span class="sxs-lookup"><span data-stu-id="71b8f-107">Resets the enumeration sequence to the beginning.</span></span>

## <a name="syntax"></a><span data-ttu-id="71b8f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="71b8f-108">Syntax</span></span>


```C++
HRESULT Reset();
```



## <a name="parameters"></a><span data-ttu-id="71b8f-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="71b8f-109">Parameters</span></span>

<span data-ttu-id="71b8f-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="71b8f-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="71b8f-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="71b8f-111">Return value</span></span>

<span data-ttu-id="71b8f-112">Diese Methode gibt **S_OK** bei Erfolg oder einen der STANDARDMÄßIGEN COM **HRESULT-Werte** bei Einem Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="71b8f-112">This method returns **S_OK** on success or one of the standard COM **HRESULT** values on error.</span></span>

## <a name="requirements"></a><span data-ttu-id="71b8f-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="71b8f-113">Requirements</span></span>



| <span data-ttu-id="71b8f-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="71b8f-114">Requirement</span></span> | <span data-ttu-id="71b8f-115">Wert</span><span class="sxs-lookup"><span data-stu-id="71b8f-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71b8f-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="71b8f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="71b8f-117">Windows 10 Desktop-Apps, Version 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="71b8f-117">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="71b8f-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="71b8f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="71b8f-119">Nur Windows Server, Version 1709 \[ von Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="71b8f-119">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="71b8f-120">Header</span><span class="sxs-lookup"><span data-stu-id="71b8f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="71b8f-121"><dt>Deliveryoptimization.h</dt></span><span class="sxs-lookup"><span data-stu-id="71b8f-121"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="71b8f-122">Idl</span><span class="sxs-lookup"><span data-stu-id="71b8f-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="71b8f-123"><dt>DeliveryOptimization.idl</dt></span><span class="sxs-lookup"><span data-stu-id="71b8f-123"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="71b8f-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="71b8f-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="71b8f-125"><dt>Dosvc.lib</dt></span><span class="sxs-lookup"><span data-stu-id="71b8f-125"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="71b8f-126">DLL</span><span class="sxs-lookup"><span data-stu-id="71b8f-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71b8f-127"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71b8f-127"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="71b8f-128">IID</span><span class="sxs-lookup"><span data-stu-id="71b8f-128">IID</span></span><br/>                      | <span data-ttu-id="71b8f-129">IID_IEnumBackgroundCopyFiles ist als CA51E165-C365-424C-8D41-24AAA4FF3C40 definiert.</span><span class="sxs-lookup"><span data-stu-id="71b8f-129">IID_IEnumBackgroundCopyFiles is defined as CA51E165-C365-424C-8D41-24AAA4FF3C40</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="71b8f-130">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="71b8f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71b8f-131">**IEnumBackgroundCopyFiles**</span><span class="sxs-lookup"><span data-stu-id="71b8f-131">**IEnumBackgroundCopyFiles**</span></span>](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

 





