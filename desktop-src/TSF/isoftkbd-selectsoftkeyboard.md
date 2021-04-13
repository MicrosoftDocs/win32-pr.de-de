---
title: Iweichkbd selectsoft Keyboard-Methode (Software-DC. h)
description: Die isoftkbd selectsoftkeyboard-Methode wählt die angegebene weiche Tastatur aus.
ms.assetid: 7e85d346-3741-457d-aadd-11d3a6710e85
keywords:
- Selectsoft Keyboard-Methode, Text Dienste-Framework
- Selectsoft Keyboard-Methode, Text Dienste-Framework, iSOFT kbd-Schnittstelle
- ISOFT kbd Interface Text Services Framework, selectsoft Keyboard-Methode
topic_type:
- apiref
api_name:
- ISoftKbd.SelectSoftKeyboard
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbda9399297e9776e7fbd7cecb364fd7f6cd4604
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518515"
---
# <a name="isoftkbdselectsoftkeyboard-method"></a><span data-ttu-id="f5fb0-106">ISOFT kbd:: selectsoft Keyboard-Methode</span><span class="sxs-lookup"><span data-stu-id="f5fb0-106">ISoftKbd::SelectSoftKeyboard method</span></span>

<span data-ttu-id="f5fb0-107">Die **isoftkbd:: selectsoftkeyboard** -Methode wählt die angegebene weiche Tastatur aus.</span><span class="sxs-lookup"><span data-stu-id="f5fb0-107">The **ISoftKbd::SelectSoftKeyboard** method selects the specified soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5fb0-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f5fb0-108">Syntax</span></span>


```C++
HRESULT SelectSoftKeyboard(
  [in] DWORD dwKeyboardId
);
```



## <a name="parameters"></a><span data-ttu-id="f5fb0-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="f5fb0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5fb0-110">*dwkeyboardid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f5fb0-110">*dwKeyboardId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5fb0-111">Der Bezeichner der ausgewählten Bildschirmtastatur.</span><span class="sxs-lookup"><span data-stu-id="f5fb0-111">Identifier of the soft keyboard to select.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5fb0-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f5fb0-112">Return value</span></span>

<span data-ttu-id="f5fb0-113">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="f5fb0-113">This method can return one of these values.</span></span>



| <span data-ttu-id="f5fb0-114">Wert</span><span class="sxs-lookup"><span data-stu-id="f5fb0-114">Value</span></span>                                                                                        | <span data-ttu-id="f5fb0-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f5fb0-115">Description</span></span>                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="f5fb0-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f5fb0-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="f5fb0-117">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="f5fb0-117">The method was successful.</span></span><br/>               |
| <dl> <span data-ttu-id="f5fb0-118"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="f5fb0-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="f5fb0-119">Der *dwkeyboardid* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="f5fb0-119">The *dwKeyboardId* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f5fb0-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f5fb0-120">Requirements</span></span>



| <span data-ttu-id="f5fb0-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f5fb0-121">Requirement</span></span> | <span data-ttu-id="f5fb0-122">Wert</span><span class="sxs-lookup"><span data-stu-id="f5fb0-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5fb0-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f5fb0-123">Minimum supported client</span></span><br/> | <span data-ttu-id="f5fb0-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f5fb0-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f5fb0-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f5fb0-125">Minimum supported server</span></span><br/> | <span data-ttu-id="f5fb0-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f5fb0-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f5fb0-127">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="f5fb0-127">Redistributable</span></span><br/>          | <span data-ttu-id="f5fb0-128">TSF 1,0 unter Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f5fb0-128">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="f5fb0-129">Header</span><span class="sxs-lookup"><span data-stu-id="f5fb0-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5fb0-130"><dt>Software-Domänen Controller. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5fb0-130"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="f5fb0-131">IDL</span><span class="sxs-lookup"><span data-stu-id="f5fb0-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f5fb0-132"><dt>Software. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f5fb0-132"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="f5fb0-133">DLL</span><span class="sxs-lookup"><span data-stu-id="f5fb0-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5fb0-134"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5fb0-134"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5fb0-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f5fb0-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5fb0-136">**Iweichkbd**</span><span class="sxs-lookup"><span data-stu-id="f5fb0-136">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> </dl>

 

 





