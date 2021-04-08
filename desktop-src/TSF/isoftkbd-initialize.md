---
title: ISOFT kbd Initialize-Methode (Software-BDC. h)
description: Die isoftkbd Initialize-Methode initialisiert alle erforderlichen Felder für eine weiche Tastatur und generiert standardmäßige weiche Tastaturlayouts.
ms.assetid: c997864c-2596-4086-8062-cd30f371c38f
keywords:
- Initialisieren der Methode Text Dienste-Framework
- Initialize Method Text Services Framework, iSOFT kbd Interface
- ISOFT kbd Interface Text Services-Framework, Initialize-Methode
topic_type:
- apiref
api_name:
- ISoftKbd.Initialize
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6e820becb05d7c474004b4889735f9637e0135a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740208"
---
# <a name="isoftkbdinitialize-method"></a><span data-ttu-id="3107d-106">ISOFT kbd:: Initialize-Methode</span><span class="sxs-lookup"><span data-stu-id="3107d-106">ISoftKbd::Initialize method</span></span>

<span data-ttu-id="3107d-107">Die **isoftkbd:: Initialize** -Methode initialisiert alle notwendigen Felder für eine weiche Tastatur und generiert standardmäßige weiche Tastaturlayouts.</span><span class="sxs-lookup"><span data-stu-id="3107d-107">The **ISoftKbd::Initialize** method initializes all necessary fields for a soft keyboard and generates standard soft keyboard layouts.</span></span>

## <a name="syntax"></a><span data-ttu-id="3107d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="3107d-108">Syntax</span></span>


```C++
HRESULT Initialize();
```



## <a name="parameters"></a><span data-ttu-id="3107d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="3107d-109">Parameters</span></span>

<span data-ttu-id="3107d-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="3107d-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3107d-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3107d-111">Return value</span></span>

<span data-ttu-id="3107d-112">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="3107d-112">This method can return one of these values.</span></span>



| <span data-ttu-id="3107d-113">Wert</span><span class="sxs-lookup"><span data-stu-id="3107d-113">Value</span></span>                                                                                | <span data-ttu-id="3107d-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3107d-114">Description</span></span>                           |
|--------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="3107d-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3107d-115"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="3107d-116">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="3107d-116">The method was successful.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3107d-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3107d-117">Requirements</span></span>



| <span data-ttu-id="3107d-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3107d-118">Requirement</span></span> | <span data-ttu-id="3107d-119">Wert</span><span class="sxs-lookup"><span data-stu-id="3107d-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3107d-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3107d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3107d-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3107d-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="3107d-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3107d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3107d-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3107d-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="3107d-124">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="3107d-124">Redistributable</span></span><br/>          | <span data-ttu-id="3107d-125">TSF 1,0 unter Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="3107d-125">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="3107d-126">Header</span><span class="sxs-lookup"><span data-stu-id="3107d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="3107d-127"><dt>Software-Domänen Controller. h</dt></span><span class="sxs-lookup"><span data-stu-id="3107d-127"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="3107d-128">IDL</span><span class="sxs-lookup"><span data-stu-id="3107d-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3107d-129"><dt>Software. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3107d-129"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="3107d-130">DLL</span><span class="sxs-lookup"><span data-stu-id="3107d-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3107d-131"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3107d-131"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3107d-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3107d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3107d-133">**Iweichkbd**</span><span class="sxs-lookup"><span data-stu-id="3107d-133">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> </dl>

 

 





