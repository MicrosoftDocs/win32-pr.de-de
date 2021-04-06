---
title: Icdkbd setkeyboardlabeltext-Methode (Software BDC. h)
description: Die isoftkbd setkeyboardlabeltext-Methode legt den Beschriftungs Text aus dem Layout für eine weiche Tastatur fest.
ms.assetid: 86c45c37-fe50-4596-b4c9-960de760a2e0
keywords:
- Setkeyboardlabeltext-Methode, Text Dienste-Framework
- Setkeyboardlabeltext-Methode, Text Dienste-Framework, iSOFT kbd-Schnittstelle
- ISOFT kbd Interface Text Services-Framework, setkeyboardlabeltext-Methode
topic_type:
- apiref
api_name:
- ISoftKbd.SetKeyboardLabelText
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 862341182b9c97a751ba4a130566d5cf18437c2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742792"
---
# <a name="isoftkbdsetkeyboardlabeltext-method"></a><span data-ttu-id="64888-106">ISOFT kbd:: setkeyboardlabeltext-Methode</span><span class="sxs-lookup"><span data-stu-id="64888-106">ISoftKbd::SetKeyboardLabelText method</span></span>

<span data-ttu-id="64888-107">Die **isoftkbd:: setkeyboardlabeltext** -Methode legt den Beschriftungs Text aus dem Layout für eine weiche Tastatur fest.</span><span class="sxs-lookup"><span data-stu-id="64888-107">The **ISoftKbd::SetKeyboardLabelText** method sets the label text from the layout for a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="64888-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="64888-108">Syntax</span></span>


```C++
HRESULT SetKeyboardLabelText(
  [in] HKL hKl
);
```



## <a name="parameters"></a><span data-ttu-id="64888-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="64888-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64888-110">*HKL* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64888-110">*hKl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64888-111">Handle, das zum Abrufen des installierten Layouts für die weiche Tastatur verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="64888-111">Handle that is used to retrieve the installed layout for the soft keyboard.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64888-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="64888-112">Return value</span></span>

<span data-ttu-id="64888-113">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="64888-113">This method can return one of these values.</span></span>



| <span data-ttu-id="64888-114">Wert</span><span class="sxs-lookup"><span data-stu-id="64888-114">Value</span></span>                                                                                        | <span data-ttu-id="64888-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="64888-115">Description</span></span>                                |
|----------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <span data-ttu-id="64888-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="64888-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="64888-117">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="64888-117">The method was successful.</span></span><br/>      |
| <dl> <span data-ttu-id="64888-118"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="64888-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="64888-119">Der *HKL* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="64888-119">The *hKl* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="64888-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="64888-120">Requirements</span></span>



| <span data-ttu-id="64888-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="64888-121">Requirement</span></span> | <span data-ttu-id="64888-122">Wert</span><span class="sxs-lookup"><span data-stu-id="64888-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="64888-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="64888-123">Minimum supported client</span></span><br/> | <span data-ttu-id="64888-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="64888-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="64888-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="64888-125">Minimum supported server</span></span><br/> | <span data-ttu-id="64888-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="64888-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="64888-127">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="64888-127">Redistributable</span></span><br/>          | <span data-ttu-id="64888-128">TSF 1,0 unter Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="64888-128">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="64888-129">Header</span><span class="sxs-lookup"><span data-stu-id="64888-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="64888-130"><dt>Software-Domänen Controller. h</dt></span><span class="sxs-lookup"><span data-stu-id="64888-130"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="64888-131">IDL</span><span class="sxs-lookup"><span data-stu-id="64888-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="64888-132"><dt>Software. idl</dt></span><span class="sxs-lookup"><span data-stu-id="64888-132"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="64888-133">DLL</span><span class="sxs-lookup"><span data-stu-id="64888-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="64888-134"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="64888-134"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64888-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="64888-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64888-136">**Iweichkbd**</span><span class="sxs-lookup"><span data-stu-id="64888-136">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="64888-137">**Icdkbd:: setkeyboardlabeltextkombination**</span><span class="sxs-lookup"><span data-stu-id="64888-137">**ISoftKbd::SetKeyboardLabelTextCombination**</span></span>](isoftkbd-setkeyboardlabeltextcombination.md)
</dt> </dl>

 

 





