---
title: IMsRdpClientAdvancedSettings7 superpanaccelerationfactor-Eigenschaft
description: Gibt einen Wert an, der den superpan-Beschleunigungs Faktor angibt, oder ruft ihn ab. Der superpan-Beschleunigungs Faktor bestimmt, wie schnell der Bildschirm im superpan-Modus ist.
ms.assetid: ce04f109-8a48-48ee-a553-728f12c09dde
ms.tgt_platform: multiple
keywords:
- Superpanaccelerationfactor-Eigenschaft Remotedesktopdienste
- Superpanaccelerationfactor-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, superpanaccelerationfactor-Eigenschaft
- Superpanaccelerationfactor-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, superpanaccelerationfactor-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.SuperPanAccelerationFactor
- IMsRdpClientAdvancedSettings7.get_SuperPanAccelerationFactor
- IMsRdpClientAdvancedSettings7.put_SuperPanAccelerationFactor
- IMsRdpClientAdvancedSettings8.SuperPanAccelerationFactor
- IMsRdpClientAdvancedSettings8.get_SuperPanAccelerationFactor
- IMsRdpClientAdvancedSettings8.put_SuperPanAccelerationFactor
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0919f3b1920980790203dc265e840e24a9315ae0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957227"
---
# <a name="imsrdpclientadvancedsettings7superpanaccelerationfactor-property"></a><span data-ttu-id="96526-109">IMsRdpClientAdvancedSettings7:: superpanaccelerationfactor-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="96526-109">IMsRdpClientAdvancedSettings7::SuperPanAccelerationFactor property</span></span>

<span data-ttu-id="96526-110">Gibt einen Wert an, der den superpan-Beschleunigungs Faktor angibt, oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="96526-110">Specifies or retrieves a value that indicates the SuperPan acceleration factor.</span></span> <span data-ttu-id="96526-111">Der superpan-Beschleunigungs Faktor bestimmt, wie schnell der Bildschirm im superpan-Modus ist.</span><span class="sxs-lookup"><span data-stu-id="96526-111">The SuperPan acceleration factor determines how quickly the screen pans when in SuperPan mode.</span></span> <span data-ttu-id="96526-112">Der Beschleunigungs Faktor ist die Anzahl der Pixel, die die Bildschirmansicht für jedes Pixel der Mausbewegung durch den Client in eine bestimmte Richtung verschiebt.</span><span class="sxs-lookup"><span data-stu-id="96526-112">The acceleration factor is the number of pixels that the screen view scrolls in a given direction for every pixel of mouse movement by the client.</span></span>

<span data-ttu-id="96526-113">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="96526-113">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="96526-114">Syntax</span><span class="sxs-lookup"><span data-stu-id="96526-114">Syntax</span></span>


```C++
HRESULT put_SuperPanAccelerationFactor(
  [in]          ULONG uAccelFactor
);

HRESULT get_SuperPanAccelerationFactor(
  [out, retval] ULONG *puAccelFactor
);
```



## <a name="property-value"></a><span data-ttu-id="96526-115">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="96526-115">Property value</span></span>

<span data-ttu-id="96526-116">Der festzulegende Wert für die übergeordnete Beschleunigung.</span><span class="sxs-lookup"><span data-stu-id="96526-116">The SuperPan acceleration factor to set.</span></span> <span data-ttu-id="96526-117">Der übergeordnete Beschleunigungs Faktor ist die Anzahl der Pixel, die die Bildschirmansicht für jedes Pixel der Mausbewegung in eine bestimmte Richtung verschiebt.</span><span class="sxs-lookup"><span data-stu-id="96526-117">The SuperPan acceleration factor is the number of pixels that the screen view scrolls in a given direction for every pixel of mouse movement.</span></span>

## <a name="remarks"></a><span data-ttu-id="96526-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="96526-118">Remarks</span></span>

<span data-ttu-id="96526-119">Weitere Informationen zu superpan finden Sie unter [**enablesuperpan**](imsrdpclientadvancedsettings7-enablesuperpan.md).</span><span class="sxs-lookup"><span data-stu-id="96526-119">For more information about SuperPan, see [**EnableSuperPan**](imsrdpclientadvancedsettings7-enablesuperpan.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="96526-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="96526-120">Requirements</span></span>



| <span data-ttu-id="96526-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="96526-121">Requirement</span></span> | <span data-ttu-id="96526-122">Wert</span><span class="sxs-lookup"><span data-stu-id="96526-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96526-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="96526-123">Minimum supported client</span></span><br/> | <span data-ttu-id="96526-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="96526-124">Windows 7</span></span><br/>                                                                             |
| <span data-ttu-id="96526-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="96526-125">Minimum supported server</span></span><br/> | <span data-ttu-id="96526-126">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="96526-126">Windows Server 2008 R2</span></span><br/>                                                                |
| <span data-ttu-id="96526-127">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="96526-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="96526-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="96526-128"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="96526-129">DLL</span><span class="sxs-lookup"><span data-stu-id="96526-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="96526-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="96526-130"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="96526-131">IID</span><span class="sxs-lookup"><span data-stu-id="96526-131">IID</span></span><br/>                      | <span data-ttu-id="96526-132">IID \_ IMsRdpClientAdvancedSettings7 wird als 26036036-4010-4578-8091-0db9a1edf-C3 definiert.</span><span class="sxs-lookup"><span data-stu-id="96526-132">IID\_IMsRdpClientAdvancedSettings7 is defined as 26036036-4010-4578-8091-0db9a1edf9c3</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="96526-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="96526-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96526-134">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="96526-134">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="96526-135">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="96526-135">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="96526-136">**Enablesuperpan**</span><span class="sxs-lookup"><span data-stu-id="96526-136">**EnableSuperPan**</span></span>](imsrdpclientadvancedsettings7-enablesuperpan.md)
</dt> </dl>

 

 





