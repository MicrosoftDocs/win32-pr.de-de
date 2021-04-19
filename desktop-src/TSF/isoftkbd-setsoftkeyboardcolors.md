---
title: Icdkbd setsoft keyboardcolors-Methode (Software-DC. h)
description: Die isoftkbd setsoftkeyboardcolors-Methode legt die weiche Tastatur Farbe für den angegebenen Farbtyp fest.
ms.assetid: 1abbff35-a5ef-4119-9367-60b6e0961c59
keywords:
- Setsoft keyboardcolors-Methode, Text Dienste-Framework
- Setsoft keyboardcolors-Methode, Text Dienste-Framework, iSOFT kbd-Schnittstelle
- ISOFT kbd Interface Text Services-Framework, setsoft keyboardcolors-Methode
topic_type:
- apiref
api_name:
- ISoftKbd.SetSoftKeyboardColors
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38357331db2440c35ca7557d08c97729fde9c9f0
ms.sourcegitcommit: d6bf2018c588c9782e1eed21b3cdea3523ec6955
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2021
ms.locfileid: "106355698"
---
# <a name="isoftkbdsetsoftkeyboardcolors-method"></a><span data-ttu-id="ccd39-106">ISOFT kbd:: setsoft keyboardcolors-Methode</span><span class="sxs-lookup"><span data-stu-id="ccd39-106">ISoftKbd::SetSoftKeyboardColors method</span></span>

<span data-ttu-id="ccd39-107">Die **isoftkbd:: setsoftkeyboardcolors** -Methode legt die weiche Tastatur Farbe für den angegebenen Farbtyp fest.</span><span class="sxs-lookup"><span data-stu-id="ccd39-107">The **ISoftKbd::SetSoftKeyboardColors** method sets the soft keyboard color for the specified color type.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccd39-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ccd39-108">Syntax</span></span>


```C++
HRESULT SetSoftKeyboardColors(
  [in] COLORTYPE colorType,
  [in] COLORREF  Color
);
```



## <a name="parameters"></a><span data-ttu-id="ccd39-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ccd39-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ccd39-110">*ColorType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ccd39-110">*colorType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccd39-111">Ein-Wert, der den Farbtyp für die weiche Tastatur angibt.</span><span class="sxs-lookup"><span data-stu-id="ccd39-111">A value specifying the color type for the soft keyboard.</span></span> <span data-ttu-id="ccd39-112">Mögliche Werte sind für die [**ColorType**](/windows/win32/api/icm/ne-icm-colortype) -Enumeration definiert.</span><span class="sxs-lookup"><span data-stu-id="ccd39-112">Possible values are defined for the [**COLORTYPE**](/windows/win32/api/icm/ne-icm-colortype) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="ccd39-113">*Farbe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ccd39-113">*Color* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccd39-114">Ein 32-Bit- [**COLORREF**](/windows/desktop/gdi/colorref) -Wert, der eine RGB-Farbe angibt.</span><span class="sxs-lookup"><span data-stu-id="ccd39-114">A 32-bit [**COLORREF**](/windows/desktop/gdi/colorref) value specifying an RGB color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ccd39-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ccd39-115">Return value</span></span>

<span data-ttu-id="ccd39-116">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="ccd39-116">This method can return one of these values.</span></span>



| <span data-ttu-id="ccd39-117">Wert</span><span class="sxs-lookup"><span data-stu-id="ccd39-117">Value</span></span>                                                                                        | <span data-ttu-id="ccd39-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ccd39-118">Description</span></span>                                  |
|----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="ccd39-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ccd39-119"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="ccd39-120">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="ccd39-120">The method was successful.</span></span><br/>        |
| <dl> <span data-ttu-id="ccd39-121"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="ccd39-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="ccd39-122">Einer der Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="ccd39-122">One of the parameters is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ccd39-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ccd39-123">Requirements</span></span>



| <span data-ttu-id="ccd39-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ccd39-124">Requirement</span></span> | <span data-ttu-id="ccd39-125">Wert</span><span class="sxs-lookup"><span data-stu-id="ccd39-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ccd39-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ccd39-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ccd39-127">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ccd39-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ccd39-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ccd39-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ccd39-129">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ccd39-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ccd39-130">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="ccd39-130">Redistributable</span></span><br/>          | <span data-ttu-id="ccd39-131">TSF 1,0 unter Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ccd39-131">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="ccd39-132">Header</span><span class="sxs-lookup"><span data-stu-id="ccd39-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="ccd39-133"><dt>Software-Domänen Controller. h</dt></span><span class="sxs-lookup"><span data-stu-id="ccd39-133"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="ccd39-134">IDL</span><span class="sxs-lookup"><span data-stu-id="ccd39-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ccd39-135"><dt>Software. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ccd39-135"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="ccd39-136">DLL</span><span class="sxs-lookup"><span data-stu-id="ccd39-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ccd39-137"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ccd39-137"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ccd39-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ccd39-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccd39-139">**Iweichkbd**</span><span class="sxs-lookup"><span data-stu-id="ccd39-139">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="ccd39-140">**Iweichkbd:: getsoft keyboardcolors**</span><span class="sxs-lookup"><span data-stu-id="ccd39-140">**ISoftKbd::GetSoftKeyboardColors**</span></span>](isoftkbd-getsoftkeyboardcolors.md)
</dt> <dt>

[<span data-ttu-id="ccd39-141">**ColorType**</span><span class="sxs-lookup"><span data-stu-id="ccd39-141">**COLORTYPE**</span></span>](/windows/win32/api/icm/ne-icm-colortype)
</dt> <dt>

[<span data-ttu-id="ccd39-142">**COLORREF**</span><span class="sxs-lookup"><span data-stu-id="ccd39-142">**COLORREF**</span></span>](/windows/desktop/gdi/colorref)
</dt> </dl>

 

