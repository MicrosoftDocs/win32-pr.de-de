---
description: Tritt auf, wenn eine Taste losgelassen wird, während das InkPicture-Steuerelement den Fokus besitzt.
ms.assetid: e22633b5-40fe-4b94-a660-684c4f5c96f3
title: InkPicture. KeyUp-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c2390b6cbb7b91ab8e447df912e591ea37248e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347487"
---
# <a name="inkpicturekeyup-event"></a><span data-ttu-id="557cf-103">InkPicture. KeyUp-Ereignis</span><span class="sxs-lookup"><span data-stu-id="557cf-103">InkPicture.KeyUp event</span></span>

<span data-ttu-id="557cf-104">Tritt auf, wenn eine Taste losgelassen wird, während das [InkPicture](inkpicture-control-reference.md) -Steuerelement den Fokus besitzt.</span><span class="sxs-lookup"><span data-stu-id="557cf-104">Occurs when a key is released while the [InkPicture](inkpicture-control-reference.md) control has focus.</span></span>

## <a name="syntax"></a><span data-ttu-id="557cf-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="557cf-105">Syntax</span></span>


```C++
void KeyUp(
  [in, out] short *KeyCode,
  [in, out] short *Shift
);
```



## <a name="parameters"></a><span data-ttu-id="557cf-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="557cf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="557cf-107">*Keycode* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="557cf-107">*KeyCode* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="557cf-108">Der ASCII-Wert des Schlüssels, der gedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="557cf-108">The ASCII value of the key that is being pressed.</span></span>

</dd> <dt>

<span data-ttu-id="557cf-109">*UMSCHALT* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="557cf-109">*Shift* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="557cf-110">Der Zustand der UMSCHALTTASTE.</span><span class="sxs-lookup"><span data-stu-id="557cf-110">The state of the SHIFT key.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="557cf-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="557cf-111">Return value</span></span>

<span data-ttu-id="557cf-112">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="557cf-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="557cf-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="557cf-113">Remarks</span></span>

<span data-ttu-id="557cf-114">Diese Ereignismethode wird in der **\_ iinkpictureevents** -Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="557cf-114">This event method is defined in the **\_IInkPictureEvents** interface.</span></span> <span data-ttu-id="557cf-115">Die **\_ iinkpictureevents** -Schnittstelle implementiert die [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle mit dem Bezeichner DISPID \_ iPeer KeyUp.</span><span class="sxs-lookup"><span data-stu-id="557cf-115">The **\_IInkPictureEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IPEKeyUp.</span></span>

## <a name="requirements"></a><span data-ttu-id="557cf-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="557cf-116">Requirements</span></span>



| <span data-ttu-id="557cf-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="557cf-117">Requirement</span></span> | <span data-ttu-id="557cf-118">Wert</span><span class="sxs-lookup"><span data-stu-id="557cf-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="557cf-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="557cf-119">Minimum supported client</span></span><br/> | <span data-ttu-id="557cf-120">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="557cf-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="557cf-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="557cf-121">Minimum supported server</span></span><br/> | <span data-ttu-id="557cf-122">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="557cf-122">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="557cf-123">Header</span><span class="sxs-lookup"><span data-stu-id="557cf-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="557cf-124"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="557cf-124"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="557cf-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="557cf-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="557cf-126"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="557cf-126"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="557cf-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="557cf-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="557cf-128">InkPicture</span><span class="sxs-lookup"><span data-stu-id="557cf-128">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

