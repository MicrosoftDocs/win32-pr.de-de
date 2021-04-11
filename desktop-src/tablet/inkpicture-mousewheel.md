---
description: Tritt auf, wenn das Mausrad bewegt wird, während das inkbilsteuerelement den Fokus besitzt.
ms.assetid: f56a8af9-7618-4fa3-8dd5-aa81a7f817e4
title: InkPicture. mouswheel-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cab870f3a00b2aa0cea3c003993e2b35cd2abbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346109"
---
# <a name="inkpicturemousewheel-event"></a><span data-ttu-id="999c9-103">InkPicture. mouswheel-Ereignis</span><span class="sxs-lookup"><span data-stu-id="999c9-103">InkPicture.MouseWheel event</span></span>

<span data-ttu-id="999c9-104">Tritt auf, wenn das Mausrad bewegt wird, während das [inkbilsteuerelement](inkpicture-control-reference.md) den Fokus besitzt.</span><span class="sxs-lookup"><span data-stu-id="999c9-104">Occurs when the mouse wheel moves while the [InkPicture](inkpicture-control-reference.md) control has focus.</span></span>

## <a name="syntax"></a><span data-ttu-id="999c9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="999c9-105">Syntax</span></span>


```C++
void MouseWheel(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     Delta,
  [in]      long                     x,
  [in]      long                     y,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="999c9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="999c9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="999c9-107">*Schaltfläche* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="999c9-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="999c9-108">Die Schaltfläche, die gedrückt wurde.</span><span class="sxs-lookup"><span data-stu-id="999c9-108">The button that was pressed.</span></span>

</dd> <dt>

<span data-ttu-id="999c9-109">*UMSCHALT* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="999c9-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="999c9-110">Der Zustand der UMSCHALTTASTE.</span><span class="sxs-lookup"><span data-stu-id="999c9-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="999c9-111">*Delta* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="999c9-111">*Delta* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="999c9-112">Die Entfernung des Mausrades.</span><span class="sxs-lookup"><span data-stu-id="999c9-112">The distance that the mouse wheel turned.</span></span>

</dd> <dt>

<span data-ttu-id="999c9-113">*x* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="999c9-113">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="999c9-114">Die x-Koordinate des [**iinkcursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) -Objekts in Pixel.</span><span class="sxs-lookup"><span data-stu-id="999c9-114">The x-coordinate, in pixels, of the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object.</span></span>

</dd> <dt>

<span data-ttu-id="999c9-115">*j* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="999c9-115">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="999c9-116">Die y-Koordinate des [**iinkcursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) -Objekts in Pixel.</span><span class="sxs-lookup"><span data-stu-id="999c9-116">The y-coordinate, in pixels, of the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object.</span></span>

</dd> <dt>

<span data-ttu-id="999c9-117">*Abbrechen* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="999c9-117">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="999c9-118">Variant \_ true, um das **mouswheel** -Ereignis für das übergeordnete Steuerelement abzubrechen, andernfalls Variant \_ false.</span><span class="sxs-lookup"><span data-stu-id="999c9-118">VARIANT\_TRUE to cancel the **MouseWheel** event for the parent control; otherwise, VARIANT\_FALSE.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="999c9-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="999c9-119">Return value</span></span>

<span data-ttu-id="999c9-120">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="999c9-120">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="999c9-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="999c9-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="999c9-122">Die Parameter *x* und *y* befinden sich in Pixel, nicht jedoch die HIMETRIC-Einheiten, die dem Koordinatensystem des frei Hand Raum-Koordinatensystems zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="999c9-122">The parameters *x* and *y* are in pixels, and not the HIMETRIC units that are associated with the ink space coordinate system.</span></span> <span data-ttu-id="999c9-123">Dies liegt daran, dass dieses Ereignis das verknüpfte Maus Ereignis einer Anwendung ersetzt, die nicht mit Pen kompatibel ist, und dieser Anwendungstyp nur auf Pixel verweist.</span><span class="sxs-lookup"><span data-stu-id="999c9-123">This is because this event replaces the related mouse event of an application that is not pen-aware, and that type of application refers only to pixels.</span></span>

 

<span data-ttu-id="999c9-124">Diese Ereignismethode wird in der **\_ iinkpictureevents** -Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="999c9-124">This event method is defined in the **\_IInkPictureEvents** interface.</span></span> <span data-ttu-id="999c9-125">Die **\_ iinkpictureevents** -Schnittstelle implementiert die [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle mit dem Bezeichner "DISPID \_ ipemouserwheel".</span><span class="sxs-lookup"><span data-stu-id="999c9-125">The **\_IInkPictureEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IPEMouseWheel.</span></span>

## <a name="requirements"></a><span data-ttu-id="999c9-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="999c9-126">Requirements</span></span>



| <span data-ttu-id="999c9-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="999c9-127">Requirement</span></span> | <span data-ttu-id="999c9-128">Wert</span><span class="sxs-lookup"><span data-stu-id="999c9-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="999c9-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="999c9-129">Minimum supported client</span></span><br/> | <span data-ttu-id="999c9-130">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="999c9-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="999c9-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="999c9-131">Minimum supported server</span></span><br/> | <span data-ttu-id="999c9-132">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="999c9-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="999c9-133">Header</span><span class="sxs-lookup"><span data-stu-id="999c9-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="999c9-134"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="999c9-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="999c9-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="999c9-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="999c9-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="999c9-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="999c9-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="999c9-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="999c9-138">InkPicture</span><span class="sxs-lookup"><span data-stu-id="999c9-138">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

