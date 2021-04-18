---
description: Tritt ein, wenn der Benutzer eine Taste drückt und freigibt, während das InkEdit-Steuerelement den Fokus besitzt.
ms.assetid: 8284ab41-dfac-4da2-b101-6968a43b15d7
title: InkEdit. KeyPress-Ereignis (Inked. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e49264f82b2cfe3c6998666339f08340a540791
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358549"
---
# <a name="inkeditkeypress-event"></a><span data-ttu-id="50a82-103">InkEdit. KeyPress-Ereignis</span><span class="sxs-lookup"><span data-stu-id="50a82-103">InkEdit.KeyPress event</span></span>

<span data-ttu-id="50a82-104">Tritt ein, wenn der Benutzer eine Taste drückt und freigibt, während das [InkEdit](inkedit-control-reference.md) -Steuerelement den Fokus besitzt.</span><span class="sxs-lookup"><span data-stu-id="50a82-104">Occurs when the user presses and releases a key while the [InkEdit](inkedit-control-reference.md) control has focus.</span></span>

## <a name="syntax"></a><span data-ttu-id="50a82-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="50a82-105">Syntax</span></span>


```C++
HRESULT KeyPress(
   Long *Char
);
```



## <a name="parameters"></a><span data-ttu-id="50a82-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="50a82-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50a82-107">*Char*</span><span class="sxs-lookup"><span data-stu-id="50a82-107">*Char*</span></span> 
</dt> <dd>

<span data-ttu-id="50a82-108">Eine ganze Zahl, die einen numerischen Standard-ANSI-Keycode zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="50a82-108">An integer that returns a standard numeric ANSI keycode.</span></span> <span data-ttu-id="50a82-109">Der *char* -Parameter wird als Verweis übergeben. durch das ändern wird ein anderes Zeichen an das Steuerelement gesendet.</span><span class="sxs-lookup"><span data-stu-id="50a82-109">The *Char* parameter is passed by reference; changing it sends a different character to the control.</span></span> <span data-ttu-id="50a82-110">Wenn der *char* -Parameter in 0 geändert wird, wird das Ereignis abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="50a82-110">Changing the *Char* parameter to 0 cancels the event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50a82-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="50a82-111">Return value</span></span>

<span data-ttu-id="50a82-112">Wenn dieses Ereignis erfolgreich ist, gibt es " **S \_ OK**" zurück.</span><span class="sxs-lookup"><span data-stu-id="50a82-112">If this event succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="50a82-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="50a82-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="50a82-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="50a82-114">Remarks</span></span>

<span data-ttu-id="50a82-115">Diese Ereignismethode wird in der **\_ iinkeditevents** -Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="50a82-115">This event method is defined in the **\_IInkEditEvents** interface.</span></span> <span data-ttu-id="50a82-116">Die **\_ iinkeditevents** -Schnittstelle implementiert die [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle mit dem Bezeichner DISPID \_ ieekeypress.</span><span class="sxs-lookup"><span data-stu-id="50a82-116">The **\_IInkEditEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IeeKeyPress.</span></span>

## <a name="requirements"></a><span data-ttu-id="50a82-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="50a82-117">Requirements</span></span>



| <span data-ttu-id="50a82-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="50a82-118">Requirement</span></span> | <span data-ttu-id="50a82-119">Wert</span><span class="sxs-lookup"><span data-stu-id="50a82-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50a82-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="50a82-120">Minimum supported client</span></span><br/> | <span data-ttu-id="50a82-121">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="50a82-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="50a82-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="50a82-122">Minimum supported server</span></span><br/> | <span data-ttu-id="50a82-123">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="50a82-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="50a82-124">Header</span><span class="sxs-lookup"><span data-stu-id="50a82-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="50a82-125"><dt>In "-. h" (auch als "gezeichneten \_ i. c" erforderlich)</dt></span><span class="sxs-lookup"><span data-stu-id="50a82-125"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="50a82-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="50a82-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="50a82-127"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50a82-127"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="50a82-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="50a82-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50a82-129">InkEdit</span><span class="sxs-lookup"><span data-stu-id="50a82-129">InkEdit</span></span>](inkedit-control-reference.md)
</dt> <dt>

<span data-ttu-id="50a82-130">[**KeyDown-Ereignis, \[ InkEdit-Steuerelement\]**](inkedit-keydown.md)</span><span class="sxs-lookup"><span data-stu-id="50a82-130">[**KeyDown Event \[InkEdit Control\]**](inkedit-keydown.md)</span></span>
</dt> <dt>

<span data-ttu-id="50a82-131">[**KeyUp-Ereignis \[ InkEdit-Steuerelement\]**](inkedit-keyup.md)</span><span class="sxs-lookup"><span data-stu-id="50a82-131">[**KeyUp Event \[InkEdit Control\]**](inkedit-keyup.md)</span></span>
</dt> </dl>

 

