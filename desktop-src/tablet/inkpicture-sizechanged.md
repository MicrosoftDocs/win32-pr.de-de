---
description: Tritt auf, nachdem die Größe des InkPicture-Steuer Elements geändert wurde, genauer gesagt, nachdem sich der Wert der Breite oder Höhe geändert hat.
ms.assetid: a5fc6c82-f9c8-4104-8abe-082c47c56be9
title: InkPicture. SizeChanged-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5675d2a581d9e8973b88fa9fb6e213f54c0e283
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960668"
---
# <a name="inkpicturesizechanged-event"></a><span data-ttu-id="513aa-103">InkPicture. SizeChanged-Ereignis</span><span class="sxs-lookup"><span data-stu-id="513aa-103">InkPicture.SizeChanged event</span></span>

<span data-ttu-id="513aa-104">Tritt auf, nachdem die Größe des [InkPicture](inkpicture-control-reference.md) -Steuer Elements geändert wurde, genauer gesagt, nachdem sich der Wert der [**Breite**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_width) oder [**Höhe**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_height) geändert hat.</span><span class="sxs-lookup"><span data-stu-id="513aa-104">Occurs after the [InkPicture](inkpicture-control-reference.md) control has been resized, specifically, after the [**Width**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_width) or [**Height**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_height) property value changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="513aa-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="513aa-105">Syntax</span></span>


```C++
void SizeChanged(
  [in] long Left,
  [in] long Top,
  [in] long Right,
  [in] long Bottom
);
```



## <a name="parameters"></a><span data-ttu-id="513aa-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="513aa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="513aa-107">*Links* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="513aa-107">*Left* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="513aa-108">Die x-Koordinate der linken Seite des [InkPicture](inkpicture-control-reference.md) -Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="513aa-108">The x-coordinate of the left side of the [InkPicture](inkpicture-control-reference.md) control.</span></span>

</dd> <dt>

<span data-ttu-id="513aa-109">Nach *oben* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="513aa-109">*Top* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="513aa-110">Die y-Koordinate des oberen Rands des [InkPicture](inkpicture-control-reference.md) -Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="513aa-110">The y-coordinate of the top of the [InkPicture](inkpicture-control-reference.md) control.</span></span>

</dd> <dt>

<span data-ttu-id="513aa-111">*Rechts* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="513aa-111">*Right* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="513aa-112">Die x-Koordinate der rechten Seite des [InkPicture](inkpicture-control-reference.md) -Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="513aa-112">The x-coordinate of the right side of the [InkPicture](inkpicture-control-reference.md) control.</span></span>

</dd> <dt>

<span data-ttu-id="513aa-113">*Unten* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="513aa-113">*Bottom* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="513aa-114">Die y-Koordinate für den unteren Rand des [InkPicture](inkpicture-control-reference.md) -Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="513aa-114">The y-coordinate of the bottom of the [InkPicture](inkpicture-control-reference.md) control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="513aa-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="513aa-115">Return value</span></span>

<span data-ttu-id="513aa-116">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="513aa-116">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="513aa-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="513aa-117">Remarks</span></span>

<span data-ttu-id="513aa-118">Diese Ereignismethode wird in der **\_ iinkpictureevents** -Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="513aa-118">This event method is defined in the **\_IInkPictureEvents** interface.</span></span> <span data-ttu-id="513aa-119">Die **\_ iinkpictureevents** -Schnittstelle implementiert die [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle mit dem Bezeichner "DISPID \_ iPeer SizeChanged".</span><span class="sxs-lookup"><span data-stu-id="513aa-119">The **\_IInkPictureEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IPESizeChanged.</span></span>

## <a name="requirements"></a><span data-ttu-id="513aa-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="513aa-120">Requirements</span></span>



| <span data-ttu-id="513aa-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="513aa-121">Requirement</span></span> | <span data-ttu-id="513aa-122">Wert</span><span class="sxs-lookup"><span data-stu-id="513aa-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="513aa-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="513aa-123">Minimum supported client</span></span><br/> | <span data-ttu-id="513aa-124">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="513aa-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="513aa-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="513aa-125">Minimum supported server</span></span><br/> | <span data-ttu-id="513aa-126">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="513aa-126">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="513aa-127">Header</span><span class="sxs-lookup"><span data-stu-id="513aa-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="513aa-128"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="513aa-128"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="513aa-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="513aa-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="513aa-130"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="513aa-130"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="513aa-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="513aa-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="513aa-132">InkPicture</span><span class="sxs-lookup"><span data-stu-id="513aa-132">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

