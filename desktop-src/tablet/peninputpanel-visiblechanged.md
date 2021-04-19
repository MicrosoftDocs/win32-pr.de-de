---
description: Veraltet. Der "tzinputpanel" wurde durch den Text Eingabe Panel (Tip) ersetzt. Tritt auf, wenn das ""-Objekt des ""-Objekts angezeigt oder ausgeblendet wird.
ms.assetid: bf4651f4-2cf4-4952-a93e-3c6ba4846722
title: "\"Pinputpanel. VisibleChanged\"-Ereignis (msink AUT. h)"
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c739f3517ad9739f1d1ba95af9e5001dfbe659a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362992"
---
# <a name="peninputpanelvisiblechanged-event"></a><span data-ttu-id="9d08f-104">"Pinputpanel. VisibleChanged"-Ereignis</span><span class="sxs-lookup"><span data-stu-id="9d08f-104">PenInputPanel.VisibleChanged event</span></span>

<span data-ttu-id="9d08f-105">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="9d08f-105">Deprecated.</span></span> <span data-ttu-id="9d08f-106">Der " [**tzinputpanel**](peninputpanel-class.md) " wurde durch den [Text Eingabe Panel (Tip)](text-input-panel-reference.md)ersetzt.</span><span class="sxs-lookup"><span data-stu-id="9d08f-106">The [**PenInputPanel**](peninputpanel-class.md) has been replaced by the [Text Input Panel (TIP)](text-input-panel-reference.md).</span></span>

<span data-ttu-id="9d08f-107">Tritt auf, [**Wenn das "**](peninputpanel-class.md) "-Objekt des ""-Objekts angezeigt oder ausgeblendet wird.</span><span class="sxs-lookup"><span data-stu-id="9d08f-107">Occurs when the [**PenInputPanel**](peninputpanel-class.md) object has shown or hidden itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d08f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="9d08f-108">Syntax</span></span>


```C++
HRESULT VisibleChanged(
  [in] VARIANT_BOOL NewVisibility
);
```



## <a name="parameters"></a><span data-ttu-id="9d08f-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="9d08f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d08f-110">*Neusicht barkeit* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9d08f-110">*NewVisibility* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d08f-111">**Variant \_ TRUE** , wenn das Objekt " [**pinputpanel**](peninputpanel-class.md) " sichtbar wird. Andernfalls ist der Wert **\_ false**.</span><span class="sxs-lookup"><span data-stu-id="9d08f-111">**VARIANT\_TRUE** to cause the [**PenInputPanel**](peninputpanel-class.md) object to become visible; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d08f-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9d08f-112">Return value</span></span>

<span data-ttu-id="9d08f-113">Wenn dieses Ereignis erfolgreich ist, gibt es " **S \_ OK**" zurück.</span><span class="sxs-lookup"><span data-stu-id="9d08f-113">If this event succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9d08f-114">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9d08f-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d08f-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9d08f-115">Remarks</span></span>

<span data-ttu-id="9d08f-116">Das **VisibleChanged** -Ereignis gilt für den Tablet PC-Eingabe Panel-Hover-Ziel.</span><span class="sxs-lookup"><span data-stu-id="9d08f-116">The **VisibleChanged** event applies to the Tablet PC Input Panel hover target.</span></span> <span data-ttu-id="9d08f-117">Sie wird jedoch nicht ausgelöst, wenn das Hover-Ziel erweitert wird, um den vollständigen Tablet PC-Eingabebereich anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="9d08f-117">However, it is not raised when the hover target expands to show the full Tablet PC Input Panel.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d08f-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9d08f-118">Requirements</span></span>



| <span data-ttu-id="9d08f-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9d08f-119">Requirement</span></span> | <span data-ttu-id="9d08f-120">Wert</span><span class="sxs-lookup"><span data-stu-id="9d08f-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d08f-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9d08f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9d08f-122">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9d08f-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="9d08f-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9d08f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9d08f-124">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="9d08f-124">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="9d08f-125">Header</span><span class="sxs-lookup"><span data-stu-id="9d08f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d08f-126"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="9d08f-126"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="9d08f-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9d08f-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="9d08f-128"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d08f-128"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="9d08f-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9d08f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d08f-130">**"Pendel Panel"**</span><span class="sxs-lookup"><span data-stu-id="9d08f-130">**PenInputPanel**</span></span>](peninputpanel-class.md)
</dt> </dl>

 

 




