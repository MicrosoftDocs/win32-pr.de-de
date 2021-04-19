---
title: Iweichkbd destroysoft keyboardwindow-Methode (Software-DC. h)
description: Die isoftkbd destroysoftkeyboardwindow-Methode zerstört ein weiches Tastatur Fenster.
ms.assetid: 44030934-7b4a-46c1-95ea-709fc9004e43
keywords:
- Destroysoft keyboardwindow-Methode, Text Dienste-Framework
- Destroysoft keyboardwindow-Methode, Text Dienste-Framework, iSOFT kbd-Schnittstelle
- ISOFT kbd Interface Text Services-Framework, destroysoft keyboardwindow-Methode
topic_type:
- apiref
api_name:
- ISoftKbd.DestroySoftKeyboardWindow
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb0c460912e8b891503771425fc72484fcc471ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338761"
---
# <a name="isoftkbddestroysoftkeyboardwindow-method"></a><span data-ttu-id="f817f-106">ISOFT kbd::D estroysoft keyboardwindow-Methode</span><span class="sxs-lookup"><span data-stu-id="f817f-106">ISoftKbd::DestroySoftKeyboardWindow method</span></span>

<span data-ttu-id="f817f-107">Die **isoftkbd::D estroysoftkeyboardwindow** -Methode zerstört ein weiches Tastatur Fenster.</span><span class="sxs-lookup"><span data-stu-id="f817f-107">The **ISoftKbd::DestroySoftKeyboardWindow** method destroys a soft keyboard window.</span></span>

## <a name="syntax"></a><span data-ttu-id="f817f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f817f-108">Syntax</span></span>


```C++
HRESULT DestroySoftKeyboardWindow();
```



## <a name="parameters"></a><span data-ttu-id="f817f-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="f817f-109">Parameters</span></span>

<span data-ttu-id="f817f-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="f817f-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f817f-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f817f-111">Return value</span></span>

<span data-ttu-id="f817f-112">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="f817f-112">This method can return one of these values.</span></span>



| <span data-ttu-id="f817f-113">Wert</span><span class="sxs-lookup"><span data-stu-id="f817f-113">Value</span></span>                                                                                | <span data-ttu-id="f817f-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f817f-114">Description</span></span>                           |
|--------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="f817f-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f817f-115"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="f817f-116">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="f817f-116">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f817f-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f817f-117">Remarks</span></span>

<span data-ttu-id="f817f-118">Diese Methode entfernt ein vorläufiges Tastatur Fenster, das zuvor mit einem Aufrufen von [**isoftkbd:: kreatesoftkeyboardwindow**](isoftkbd-createsoftkeyboardwindow.md)erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="f817f-118">This method removes a soft keyboard window previously created with a call to [**ISoftKbd::CreateSoftKeyboardWindow**](isoftkbd-createsoftkeyboardwindow.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f817f-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f817f-119">Requirements</span></span>



| <span data-ttu-id="f817f-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f817f-120">Requirement</span></span> | <span data-ttu-id="f817f-121">Wert</span><span class="sxs-lookup"><span data-stu-id="f817f-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f817f-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f817f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f817f-123">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f817f-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f817f-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f817f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f817f-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f817f-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f817f-126">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="f817f-126">Redistributable</span></span><br/>          | <span data-ttu-id="f817f-127">TSF 1,0 unter Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f817f-127">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="f817f-128">Header</span><span class="sxs-lookup"><span data-stu-id="f817f-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="f817f-129"><dt>Software-Domänen Controller. h</dt></span><span class="sxs-lookup"><span data-stu-id="f817f-129"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="f817f-130">IDL</span><span class="sxs-lookup"><span data-stu-id="f817f-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f817f-131"><dt>Software. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f817f-131"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="f817f-132">DLL</span><span class="sxs-lookup"><span data-stu-id="f817f-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f817f-133"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f817f-133"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f817f-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f817f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f817f-135">**Iweichkbd**</span><span class="sxs-lookup"><span data-stu-id="f817f-135">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="f817f-136">**Iweichkbd:: kreatesoftkeyboardwindow**</span><span class="sxs-lookup"><span data-stu-id="f817f-136">**ISoftKbd::CreateSoftKeyboardWindow**</span></span>](isoftkbd-createsoftkeyboardwindow.md)
</dt> </dl>

 

 





