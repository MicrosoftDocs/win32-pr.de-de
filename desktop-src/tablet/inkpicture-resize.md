---
description: Tritt auf, wenn die Größe des InkPicture-Steuer Elements geändert wird (wenn sich die Eigenschaftswerte für Breite und/oder Höhe ändern).
ms.assetid: 436db420-f9ea-46f1-b922-c8663371edd5
title: InkPicture. Resize-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c4c5df298658f6ac98ddbf8fc00873f6f22dcb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042720"
---
# <a name="inkpictureresize-event"></a><span data-ttu-id="2b6b7-103">InkPicture. Resize-Ereignis</span><span class="sxs-lookup"><span data-stu-id="2b6b7-103">InkPicture.Resize event</span></span>

<span data-ttu-id="2b6b7-104">Tritt auf, wenn die Größe des [InkPicture](inkpicture-control-reference.md) -Steuer Elements geändert wird (wenn sich die Eigenschaftswerte für Breite und/oder Höhe ändern).</span><span class="sxs-lookup"><span data-stu-id="2b6b7-104">Occurs when the [InkPicture](inkpicture-control-reference.md) control is resized (when the Width and/or Height property values change).</span></span>

## <a name="syntax"></a><span data-ttu-id="2b6b7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2b6b7-105">Syntax</span></span>


```C++
void Resize(
   long Left,
   long Top,
   long Right,
   long Bottom
);
```



## <a name="parameters"></a><span data-ttu-id="2b6b7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2b6b7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b6b7-107">*Left*</span><span class="sxs-lookup"><span data-stu-id="2b6b7-107">*Left*</span></span> 
</dt> <dd>

<span data-ttu-id="2b6b7-108">Die Anzahl der Pixel von der linken Seite des Fensters, das das Steuerelement auf der linken Seite des-Steuer Elements enthält.</span><span class="sxs-lookup"><span data-stu-id="2b6b7-108">The number of pixels from the left side of the window that contains the control to the left side of the control.</span></span>

</dd> <dt>

<span data-ttu-id="2b6b7-109">*Top*</span><span class="sxs-lookup"><span data-stu-id="2b6b7-109">*Top*</span></span> 
</dt> <dd>

<span data-ttu-id="2b6b7-110">Die Anzahl der Pixel vom oberen Rand des Fensters, das das Steuerelement am oberen Rand des-Steuer Elements enthält.</span><span class="sxs-lookup"><span data-stu-id="2b6b7-110">The number of pixels from the top of the window that contains the control to the top of the control.</span></span>

</dd> <dt>

<span data-ttu-id="2b6b7-111">*Right*</span><span class="sxs-lookup"><span data-stu-id="2b6b7-111">*Right*</span></span> 
</dt> <dd>

<span data-ttu-id="2b6b7-112">Die Anzahl der Pixel von der linken Seite des Fensters, das das Steuerelement auf der rechten Seite des-Steuer Elements enthält.</span><span class="sxs-lookup"><span data-stu-id="2b6b7-112">The number of pixels from the left side of the window that contains the control to the right side of the control.</span></span>

</dd> <dt>

<span data-ttu-id="2b6b7-113">*bottom*</span><span class="sxs-lookup"><span data-stu-id="2b6b7-113">*Bottom*</span></span> 
</dt> <dd>

<span data-ttu-id="2b6b7-114">Die Anzahl der Pixel vom oberen Rand des Fensters, das das Steuerelement am unteren Rand des Steuer Elements enthält.</span><span class="sxs-lookup"><span data-stu-id="2b6b7-114">The number of pixels from the top of the window that contains the control to the bottom of the control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b6b7-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2b6b7-115">Return value</span></span>

<span data-ttu-id="2b6b7-116">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="2b6b7-116">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b6b7-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2b6b7-117">Remarks</span></span>

<span data-ttu-id="2b6b7-118">Die neue Breite des Steuer Elements in Pixel entspricht der Differenz zwischen dem *rechten* und dem *linken* Parameter.</span><span class="sxs-lookup"><span data-stu-id="2b6b7-118">The new width of the control in pixels will be equal to the difference between the *Right* and *Left* parameters.</span></span> <span data-ttu-id="2b6b7-119">Ebenso ist die neue Höhe gleich der Differenz zwischen *unten* und *oben*.</span><span class="sxs-lookup"><span data-stu-id="2b6b7-119">Likewise, the new height will be equal to the difference between *Bottom* and *Top*.</span></span>

<span data-ttu-id="2b6b7-120">Diese Ereignismethode wird in der **\_ iinkpictureevents** -Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="2b6b7-120">This event method is defined in the **\_IInkPictureEvents** interface.</span></span> <span data-ttu-id="2b6b7-121">Die **\_ iinkpictureevents** -Schnittstelle implementiert die IDispatch-Schnittstelle mit dem Bezeichner " **DISPID \_ iperesize**".</span><span class="sxs-lookup"><span data-stu-id="2b6b7-121">The **\_IInkPictureEvents** interface implements the IDispatch interface with an identifier of **DISPID\_IPEResize**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b6b7-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2b6b7-122">Requirements</span></span>



| <span data-ttu-id="2b6b7-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2b6b7-123">Requirement</span></span> | <span data-ttu-id="2b6b7-124">Wert</span><span class="sxs-lookup"><span data-stu-id="2b6b7-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b6b7-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2b6b7-125">Minimum supported client</span></span><br/> | <span data-ttu-id="2b6b7-126">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2b6b7-126">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="2b6b7-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2b6b7-127">Minimum supported server</span></span><br/> | <span data-ttu-id="2b6b7-128">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="2b6b7-128">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="2b6b7-129">Header</span><span class="sxs-lookup"><span data-stu-id="2b6b7-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b6b7-130"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="2b6b7-130"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="2b6b7-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2b6b7-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="2b6b7-132"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b6b7-132"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="2b6b7-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2b6b7-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b6b7-134">InkPicture</span><span class="sxs-lookup"><span data-stu-id="2b6b7-134">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

 




