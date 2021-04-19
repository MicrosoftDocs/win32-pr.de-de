---
title: ISoftware. getsoft keyboardcolors-Methode (Software BDC. h)
description: Die isoftkbd getsoftkeyboardcolors-Methode ruft die weiche Tastatur Farbe ab, die dem angegebenen Farbtyp entspricht.
ms.assetid: d59d249c-a1c4-4d6a-add6-632be55a7549
keywords:
- Getsoft keyboardcolors-Methode, Text Dienste-Framework
- Getsoft keyboardcolors-Methode, Text Dienste-Framework, iSOFT kbd-Schnittstelle
- ISOFT kbd Interface Text Services Framework, getsoft keyboardcolors-Methode
topic_type:
- apiref
api_name:
- ISoftKbd.GetSoftKeyboardColors
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f8f184dc04ddcbef18a9279000b1a68acd35bd3
ms.sourcegitcommit: d6bf2018c588c9782e1eed21b3cdea3523ec6955
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2021
ms.locfileid: "106366349"
---
# <a name="isoftkbdgetsoftkeyboardcolors-method"></a><span data-ttu-id="e8580-106">ISOFT kbd:: getsoft keyboardcolors-Methode</span><span class="sxs-lookup"><span data-stu-id="e8580-106">ISoftKbd::GetSoftKeyboardColors method</span></span>

<span data-ttu-id="e8580-107">Die **isoftkbd:: getsoftkeyboardcolors** -Methode ruft die weiche Tastatur Farbe ab, die dem angegebenen Farbtyp entspricht.</span><span class="sxs-lookup"><span data-stu-id="e8580-107">The **ISoftKbd::GetSoftKeyboardColors** method retrieves the soft keyboard color corresponding to the supplied color type.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8580-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e8580-108">Syntax</span></span>


```C++
HRESULT GetSoftKeyboardColors(
  [in]  COLORTYPE colorType,
  [out] COLORREF  *lpColor
);
```



## <a name="parameters"></a><span data-ttu-id="e8580-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="e8580-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8580-110">*ColorType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e8580-110">*colorType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8580-111">Ein-Wert, der den für die weiche Tastatur abzurufenden Farbtyp angibt.</span><span class="sxs-lookup"><span data-stu-id="e8580-111">A value specifying the color type to retrieve for the soft keyboard.</span></span> <span data-ttu-id="e8580-112">Mögliche Werte sind für die [**ColorType**](/windows/win32/api/icm/ne-icm-colortype) -Enumeration definiert.</span><span class="sxs-lookup"><span data-stu-id="e8580-112">Possible values are defined for the [**COLORTYPE**](/windows/win32/api/icm/ne-icm-colortype) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="e8580-113">*lpcolor* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e8580-113">*lpColor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e8580-114">Ein Zeiger auf einen Puffer, in dem diese Methode einen 32-Bit- [**COLORREF**](/windows/desktop/gdi/colorref) -Wert abruft, der eine RGB-Farbe angibt.</span><span class="sxs-lookup"><span data-stu-id="e8580-114">Pointer to a buffer in which this method retrieves a 32-bit [**COLORREF**](/windows/desktop/gdi/colorref) value specifying an RGB color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8580-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e8580-115">Return value</span></span>

<span data-ttu-id="e8580-116">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="e8580-116">This method can return one of these values.</span></span>



| <span data-ttu-id="e8580-117">Wert</span><span class="sxs-lookup"><span data-stu-id="e8580-117">Value</span></span>                                                                                        | <span data-ttu-id="e8580-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e8580-118">Description</span></span>                                  |
|----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="e8580-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e8580-119"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="e8580-120">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="e8580-120">The method was successful.</span></span><br/>        |
| <dl> <span data-ttu-id="e8580-121"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="e8580-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="e8580-122">Einer der Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="e8580-122">One of the parameters is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e8580-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e8580-123">Requirements</span></span>



| <span data-ttu-id="e8580-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e8580-124">Requirement</span></span> | <span data-ttu-id="e8580-125">Wert</span><span class="sxs-lookup"><span data-stu-id="e8580-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e8580-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e8580-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e8580-127">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e8580-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e8580-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e8580-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e8580-129">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e8580-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e8580-130">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="e8580-130">Redistributable</span></span><br/>          | <span data-ttu-id="e8580-131">TSF 1,0 unter Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e8580-131">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="e8580-132">Header</span><span class="sxs-lookup"><span data-stu-id="e8580-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8580-133"><dt>Software-Domänen Controller. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8580-133"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="e8580-134">IDL</span><span class="sxs-lookup"><span data-stu-id="e8580-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e8580-135"><dt>Software. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e8580-135"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="e8580-136">DLL</span><span class="sxs-lookup"><span data-stu-id="e8580-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e8580-137"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8580-137"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8580-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e8580-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8580-139">**Iweichkbd**</span><span class="sxs-lookup"><span data-stu-id="e8580-139">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="e8580-140">**Iweichkbd:: setsoft keyboardcolors**</span><span class="sxs-lookup"><span data-stu-id="e8580-140">**ISoftKbd::SetSoftKeyboardColors**</span></span>](/windows/desktop/TSF/isoftkbd-setsoftkeyboardcolors)
</dt> <dt>

[<span data-ttu-id="e8580-141">**ColorType**</span><span class="sxs-lookup"><span data-stu-id="e8580-141">**COLORTYPE**</span></span>](/windows/win32/api/icm/ne-icm-colortype)
</dt> <dt>

[<span data-ttu-id="e8580-142">**COLORREF**</span><span class="sxs-lookup"><span data-stu-id="e8580-142">**COLORREF**</span></span>](/windows/desktop/gdi/colorref)
</dt> </dl>

 

