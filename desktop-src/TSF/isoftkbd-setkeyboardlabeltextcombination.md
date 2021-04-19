---
title: Icdkbd setkeyboardlabeltextcombination-Methode (Software-DC. h)
description: Mit der isoftkbd setkeyboardlabeltextcombination-Methode wird eine Kombination aus Bezeichnung und Text festgelegt, mit der eine weiche Tastatur beschrieben wird.
ms.assetid: fe054eae-1a44-41ad-9a44-bc0b46df7c7b
keywords:
- Setkeyboardlabeltextcombination-Methode, Text Dienste-Framework
- Setkeyboardlabeltextcombination-Methode, Text Dienste-Framework, iSOFT kbd-Schnittstelle
- ISOFT kbd Interface Text Services-Framework, setkeyboardlabeltextcombination-Methode
topic_type:
- apiref
api_name:
- ISoftKbd.SetKeyboardLabelTextCombination
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0f98dad124455625f0da3ada1a717c692437398
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346106"
---
# <a name="isoftkbdsetkeyboardlabeltextcombination-method"></a><span data-ttu-id="c9274-106">Icdkbd:: setkeyboardlabeltextcombination-Methode</span><span class="sxs-lookup"><span data-stu-id="c9274-106">ISoftKbd::SetKeyboardLabelTextCombination method</span></span>

<span data-ttu-id="c9274-107">Die **isoftkbd:: setkeyboardlabeltextcombination** -Methode legt eine Kombination aus Bezeichnung und Text fest, mit der eine weiche Tastatur beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="c9274-107">The **ISoftKbd::SetKeyboardLabelTextCombination** method sets a combination of label and text used to describe a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9274-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c9274-108">Syntax</span></span>


```C++
HRESULT SetKeyboardLabelTextCombination(
  [in] DWORD nModifierCombination
);
```



## <a name="parameters"></a><span data-ttu-id="c9274-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c9274-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9274-110">*nmodifierkombination* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c9274-110">*nModifierCombination* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9274-111">Eine Kombination aus Bezeichnung und Text, mit der die weiche Tastatur beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="c9274-111">Combination of label and text used to describe the soft keyboard.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9274-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c9274-112">Return value</span></span>

<span data-ttu-id="c9274-113">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="c9274-113">This method can return one of these values.</span></span>



| <span data-ttu-id="c9274-114">Wert</span><span class="sxs-lookup"><span data-stu-id="c9274-114">Value</span></span>                                                                                        | <span data-ttu-id="c9274-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c9274-115">Description</span></span>                                                 |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="c9274-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c9274-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="c9274-117">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="c9274-117">The method was successful.</span></span><br/>                       |
| <dl> <span data-ttu-id="c9274-118"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="c9274-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="c9274-119">Der *nmodifiercombination* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="c9274-119">The *nModifierCombination* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c9274-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c9274-120">Requirements</span></span>



| <span data-ttu-id="c9274-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c9274-121">Requirement</span></span> | <span data-ttu-id="c9274-122">Wert</span><span class="sxs-lookup"><span data-stu-id="c9274-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c9274-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c9274-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c9274-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c9274-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c9274-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c9274-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c9274-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c9274-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c9274-127">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="c9274-127">Redistributable</span></span><br/>          | <span data-ttu-id="c9274-128">TSF 1,0 unter Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c9274-128">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="c9274-129">Header</span><span class="sxs-lookup"><span data-stu-id="c9274-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9274-130"><dt>Software-Domänen Controller. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9274-130"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="c9274-131">IDL</span><span class="sxs-lookup"><span data-stu-id="c9274-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c9274-132"><dt>Software. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c9274-132"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="c9274-133">DLL</span><span class="sxs-lookup"><span data-stu-id="c9274-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9274-134"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9274-134"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9274-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c9274-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9274-136">**Iweichkbd**</span><span class="sxs-lookup"><span data-stu-id="c9274-136">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="c9274-137">**Icdkbd:: setkeyboardlabeltext**</span><span class="sxs-lookup"><span data-stu-id="c9274-137">**ISoftKbd::SetKeyboardLabelText**</span></span>](isoftkbd-setkeyboardlabeltext.md)
</dt> </dl>

 

 





