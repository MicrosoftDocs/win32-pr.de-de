---
description: Tritt ein, wenn der Mauszeiger über das InkPicture-Steuerelement bewegt wird.
ms.assetid: b4c703da-0e4a-4d4c-9a6c-0e002344fb2f
title: InkPicture. mousermove-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c5540831594674dd279fc14e822d6b3240b014c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216590"
---
# <a name="inkpicturemousemove-event"></a><span data-ttu-id="fe6f0-103">InkPicture. mousermove-Ereignis</span><span class="sxs-lookup"><span data-stu-id="fe6f0-103">InkPicture.MouseMove event</span></span>

<span data-ttu-id="fe6f0-104">Tritt ein, wenn der Mauszeiger über das [InkPicture](inkpicture-control-reference.md) -Steuerelement bewegt wird.</span><span class="sxs-lookup"><span data-stu-id="fe6f0-104">Occurs when the mouse pointer is moved over the [InkPicture](inkpicture-control-reference.md) control.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe6f0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fe6f0-105">Syntax</span></span>


```C++
void MouseMove(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="fe6f0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fe6f0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe6f0-107">*Schaltfläche* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fe6f0-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe6f0-108">Die Schaltfläche, die gedrückt wurde.</span><span class="sxs-lookup"><span data-stu-id="fe6f0-108">The button that was pressed.</span></span>

</dd> <dt>

<span data-ttu-id="fe6f0-109">*UMSCHALT* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fe6f0-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe6f0-110">Der Zustand der UMSCHALTTASTE.</span><span class="sxs-lookup"><span data-stu-id="fe6f0-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="fe6f0-111">*px* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fe6f0-111">*pX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe6f0-112">Die x-Koordinate des [**iinkcursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) -Objekts in Pixel.</span><span class="sxs-lookup"><span data-stu-id="fe6f0-112">The x-coordinate, in pixels, of the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object.</span></span>

</dd> <dt>

<span data-ttu-id="fe6f0-113">*pY* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fe6f0-113">*pY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe6f0-114">Die y-Koordinate des [**iinkcursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) -Objekts in Pixel.</span><span class="sxs-lookup"><span data-stu-id="fe6f0-114">The y-coordinate, in pixels, of the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object.</span></span>

</dd> <dt>

<span data-ttu-id="fe6f0-115">*Abbrechen* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="fe6f0-115">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe6f0-116">**Variant \_ TRUE** , um dieses Ereignis für das übergeordnete Steuerelement abzubrechen. Andernfalls ist der Wert **\_ false**.</span><span class="sxs-lookup"><span data-stu-id="fe6f0-116">**VARIANT\_TRUE** to cancel this event for the parent control; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe6f0-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fe6f0-117">Return value</span></span>

<span data-ttu-id="fe6f0-118">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="fe6f0-118">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe6f0-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fe6f0-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="fe6f0-120">Die Parameter *px* und *pY* liegen in Pixel und nicht in den HIMETRIC-Einheiten, die dem Freihand Raumkoordinaten System zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="fe6f0-120">The parameters *pX* and *pY* are in pixels, and not the HIMETRIC units that are associated with the ink space coordinate system.</span></span> <span data-ttu-id="fe6f0-121">Dies liegt daran, dass dieses Ereignis das verknüpfte Maus Ereignis einer Anwendung ersetzt, die nicht mit Pen kompatibel ist, und dieser Anwendungstyp nur auf Pixel verweist.</span><span class="sxs-lookup"><span data-stu-id="fe6f0-121">This is because this event replaces the related mouse event of an application that is not pen-aware, and that type of application refers only to pixels.</span></span>

 

> [!Caution]  
> <span data-ttu-id="fe6f0-122">Einige Steuerelemente basieren auf einer bestimmten Beziehung zwischen [**mouledown**](inkpicture-mousedown.md)-, **mousermove**-und [**mouberup**](inkpicture-mouseup.md) -Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="fe6f0-122">Some controls rely on a specific relationship between [**MouseDown**](inkpicture-mousedown.md), **MouseMove**, and [**MouseUp**](inkpicture-mouseup.md) events.</span></span> <span data-ttu-id="fe6f0-123">Das Abbrechen einiger dieser Ereignisse kann zu unerwarteten Ergebnissen führen.</span><span class="sxs-lookup"><span data-stu-id="fe6f0-123">Canceling some of these events may have unanticipated results.</span></span>

 

<span data-ttu-id="fe6f0-124">Diese Ereignismethode wird in der **\_ iinkpictureevents** -Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="fe6f0-124">This event method is defined in the **\_IInkPictureEvents** interface.</span></span> <span data-ttu-id="fe6f0-125">Die **\_ iinkpictureevents** -Schnittstelle implementiert die [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle mit dem Bezeichner "DISPID \_ ipemouabdown".</span><span class="sxs-lookup"><span data-stu-id="fe6f0-125">The **\_IInkPictureEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IPEMouseDown.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe6f0-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fe6f0-126">Requirements</span></span>



| <span data-ttu-id="fe6f0-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fe6f0-127">Requirement</span></span> | <span data-ttu-id="fe6f0-128">Wert</span><span class="sxs-lookup"><span data-stu-id="fe6f0-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe6f0-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fe6f0-129">Minimum supported client</span></span><br/> | <span data-ttu-id="fe6f0-130">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fe6f0-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="fe6f0-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fe6f0-131">Minimum supported server</span></span><br/> | <span data-ttu-id="fe6f0-132">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="fe6f0-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="fe6f0-133">Header</span><span class="sxs-lookup"><span data-stu-id="fe6f0-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe6f0-134"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="fe6f0-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="fe6f0-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fe6f0-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="fe6f0-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fe6f0-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="fe6f0-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fe6f0-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe6f0-138">InkPicture</span><span class="sxs-lookup"><span data-stu-id="fe6f0-138">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

