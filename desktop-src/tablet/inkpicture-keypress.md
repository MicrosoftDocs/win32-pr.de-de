---
description: Tritt auf, wenn eine Taste gedrückt wird, während das InkPicture-Steuerelement den Fokus besitzt.
ms.assetid: adb61eff-a92c-40b0-940c-02e14cd34e5f
title: InkPicture. KeyPress-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35f9ef48a0e117d6a3d4c29a9ca69aba3bf6e054
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959044"
---
# <a name="inkpicturekeypress-event"></a><span data-ttu-id="09100-103">InkPicture. KeyPress-Ereignis</span><span class="sxs-lookup"><span data-stu-id="09100-103">InkPicture.KeyPress event</span></span>

<span data-ttu-id="09100-104">Tritt auf, wenn eine Taste gedrückt wird, während das [InkPicture](inkpicture-control-reference.md) -Steuerelement den Fokus besitzt.</span><span class="sxs-lookup"><span data-stu-id="09100-104">Occurs when a key is pressed while the [InkPicture](inkpicture-control-reference.md) control has focus.</span></span>

## <a name="syntax"></a><span data-ttu-id="09100-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="09100-105">Syntax</span></span>


```C++
void KeyPress(
  [in, out] short *KeyAscii
);
```



## <a name="parameters"></a><span data-ttu-id="09100-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="09100-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09100-107">*KeyAscii* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="09100-107">*KeyAscii* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="09100-108">Der ASCII-Wert des Schlüssels, der gedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="09100-108">The ASCII value of the key that is being pressed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09100-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="09100-109">Return value</span></span>

<span data-ttu-id="09100-110">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="09100-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="09100-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="09100-111">Remarks</span></span>

<span data-ttu-id="09100-112">Diese Ereignismethode wird in der **\_ iinkpictureevents** -Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="09100-112">This event method is defined in the **\_IInkPictureEvents** interface.</span></span> <span data-ttu-id="09100-113">Die **\_ iinkpictureevents** -Schnittstelle implementiert die [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle mit dem Bezeichner DISPID \_ iPeer KeyPress.</span><span class="sxs-lookup"><span data-stu-id="09100-113">The **\_IInkPictureEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IPEKeyPress.</span></span>

## <a name="requirements"></a><span data-ttu-id="09100-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="09100-114">Requirements</span></span>



| <span data-ttu-id="09100-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="09100-115">Requirement</span></span> | <span data-ttu-id="09100-116">Wert</span><span class="sxs-lookup"><span data-stu-id="09100-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09100-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="09100-117">Minimum supported client</span></span><br/> | <span data-ttu-id="09100-118">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="09100-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="09100-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="09100-119">Minimum supported server</span></span><br/> | <span data-ttu-id="09100-120">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="09100-120">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="09100-121">Header</span><span class="sxs-lookup"><span data-stu-id="09100-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="09100-122"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="09100-122"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="09100-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="09100-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="09100-124"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="09100-124"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="09100-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="09100-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09100-126">InkPicture</span><span class="sxs-lookup"><span data-stu-id="09100-126">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

