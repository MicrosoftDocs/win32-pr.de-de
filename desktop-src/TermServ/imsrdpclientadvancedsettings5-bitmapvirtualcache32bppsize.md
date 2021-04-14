---
title: IMsRdpClientAdvancedSettings5 BitmapVirtualCache32BppSize-Eigenschaft
description: Legt die Größe der virtuellen Cachedatei für 32 Bits pro Pixel (BPP)-Bitmaps fest oder ruft Sie ab.
ms.assetid: 7084293a-ae75-4711-a8d8-f813117333e7
ms.tgt_platform: multiple
keywords:
- BitmapVirtualCache32BppSize-Eigenschaft Remotedesktopdienste
- BitmapVirtualCache32BppSize-Eigenschaften Remotedesktopdienste, IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5-Schnittstelle Remotedesktopdienste, BitmapVirtualCache32BppSize-Eigenschaft
- BitmapVirtualCache32BppSize-Eigenschaften Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6-Schnittstelle Remotedesktopdienste, BitmapVirtualCache32BppSize-Eigenschaft
- BitmapVirtualCache32BppSize-Eigenschaften Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7-Schnittstelle Remotedesktopdienste, BitmapVirtualCache32BppSize-Eigenschaft
- BitmapVirtualCache32BppSize-Eigenschaften Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8-Schnittstelle Remotedesktopdienste, BitmapVirtualCache32BppSize-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5.BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings5.get_BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings5.put_BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings6.BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings6.get_BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings6.put_BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings7.BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings7.get_BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings7.put_BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings8.BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings8.get_BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings8.put_BitmapVirtualCache32BppSize
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d43de82b97e16fa36f83a5edde43712b2a9cbbb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391732"
---
# <a name="imsrdpclientadvancedsettings5bitmapvirtualcache32bppsize-property"></a><span data-ttu-id="cd1b2-112">IMsRdpClientAdvancedSettings5:: BitmapVirtualCache32BppSize-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="cd1b2-112">IMsRdpClientAdvancedSettings5::BitmapVirtualCache32BppSize property</span></span>

<span data-ttu-id="cd1b2-113">Legt die Größe der virtuellen Cachedatei für 32 Bits pro Pixel (BPP)-Bitmaps fest oder ruft Sie ab.</span><span class="sxs-lookup"><span data-stu-id="cd1b2-113">Sets or retrieves the virtual cache file size for 32 bits per pixel (bpp) bitmaps.</span></span>

<span data-ttu-id="cd1b2-114">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="cd1b2-114">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd1b2-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="cd1b2-115">Syntax</span></span>


```C++
HRESULT put_BitmapVirtualCache32BppSize(
  [in]  LONG bitmapVirtualCache32BppSize
);

HRESULT get_BitmapVirtualCache32BppSize(
  [out] LONG *pbitmapVirtualCache32BppSize
);
```



## <a name="property-value"></a><span data-ttu-id="cd1b2-116">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="cd1b2-116">Property value</span></span>

<span data-ttu-id="cd1b2-117">Legt die Größe der virtuellen Cachedatei für 32 bpp-Bitmaps in Megabyte (MB) fest.</span><span class="sxs-lookup"><span data-stu-id="cd1b2-117">Sets the size of the virtual cache file for 32 bpp bitmaps, in megabytes (MB).</span></span> <span data-ttu-id="cd1b2-118">Der Maximalwert ist 48 MB.</span><span class="sxs-lookup"><span data-stu-id="cd1b2-118">The maximum value is 48 MB.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd1b2-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cd1b2-119">Requirements</span></span>



| <span data-ttu-id="cd1b2-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cd1b2-120">Requirement</span></span> | <span data-ttu-id="cd1b2-121">Wert</span><span class="sxs-lookup"><span data-stu-id="cd1b2-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd1b2-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cd1b2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="cd1b2-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cd1b2-123">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="cd1b2-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cd1b2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="cd1b2-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cd1b2-125">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="cd1b2-126">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="cd1b2-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="cd1b2-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd1b2-127"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="cd1b2-128">DLL</span><span class="sxs-lookup"><span data-stu-id="cd1b2-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd1b2-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd1b2-129"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="cd1b2-130">IID</span><span class="sxs-lookup"><span data-stu-id="cd1b2-130">IID</span></span><br/>                      | <span data-ttu-id="cd1b2-131">IID \_ IMsRdpClientAdvancedSettings5 ist als FBA7F64E-6783-4405-DA45-FA4A763DABD0 definiert.</span><span class="sxs-lookup"><span data-stu-id="cd1b2-131">IID\_IMsRdpClientAdvancedSettings5 is defined as FBA7F64E-6783-4405-DA45-FA4A763DABD0</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cd1b2-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cd1b2-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd1b2-133">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="cd1b2-133">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="cd1b2-134">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="cd1b2-134">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="cd1b2-135">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="cd1b2-135">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="cd1b2-136">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="cd1b2-136">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> </dl>

 

 





