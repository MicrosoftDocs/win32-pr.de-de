---
description: Veraltet. Der "tzinputpanel" wurde durch den Text Eingabe Panel (Tip) ersetzt. Tritt auf, wenn das Objekt "pinputpanel" verschoben wird.
ms.assetid: 0c51d875-cef9-4087-b17d-5c5af04f81a5
title: "\"Pinputpanel. PanelMoving\"-Ereignis (\"msink AUT. h\")"
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7be69e227188739cb656e6a1eb471716e1aa4feb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352372"
---
# <a name="peninputpanelpanelmoving-event"></a><span data-ttu-id="b3df3-104">"Pinputpanel. PanelMoving"-Ereignis</span><span class="sxs-lookup"><span data-stu-id="b3df3-104">PenInputPanel.PanelMoving event</span></span>

<span data-ttu-id="b3df3-105">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="b3df3-105">Deprecated.</span></span> <span data-ttu-id="b3df3-106">Der " [**tzinputpanel**](peninputpanel-class.md) " wurde durch den [Text Eingabe Panel (Tip)](text-input-panel-reference.md)ersetzt.</span><span class="sxs-lookup"><span data-stu-id="b3df3-106">The [**PenInputPanel**](peninputpanel-class.md) has been replaced by the [Text Input Panel (TIP)](text-input-panel-reference.md).</span></span>

<span data-ttu-id="b3df3-107">Tritt auf, wenn das Objekt " [**pinputpanel**](peninputpanel-class.md) " verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="b3df3-107">Occurs when the [**PenInputPanel**](peninputpanel-class.md) object is moving.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3df3-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b3df3-108">Syntax</span></span>


```C++
HRESULT PanelMoving(
  [in, out] long *Left,
  [in, out] long *Top
);
```



## <a name="parameters"></a><span data-ttu-id="b3df3-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="b3df3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3df3-110">*Links* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="b3df3-110">*Left* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b3df3-111">Die neue horizontale bzw. x-Achse, Position des linken Rands des " [**tabinputpanel**](peninputpanel-class.md) "-Objekts in Bildschirm Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="b3df3-111">The new horizontal, or x-axis, position of the left edge of the [**PenInputPanel**](peninputpanel-class.md) object, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="b3df3-112">Nach *oben* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="b3df3-112">*Top* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b3df3-113">Die neue vertikale Achse bzw. y-Achse, Position des linken Randes des ""- [**raninputpanel**](peninputpanel-class.md) -Objekts in Bildschirm Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="b3df3-113">The new vertical, or y-axis, position of the left edge of the [**PenInputPanel**](peninputpanel-class.md) object, in screen coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3df3-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b3df3-114">Return value</span></span>

<span data-ttu-id="b3df3-115">Wenn dieses Ereignis erfolgreich ist, gibt es " **S \_ OK**" zurück.</span><span class="sxs-lookup"><span data-stu-id="b3df3-115">If this event succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b3df3-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b3df3-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3df3-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b3df3-117">Remarks</span></span>

<span data-ttu-id="b3df3-118">Das **PanelMoving** -Ereignis ist so konzipiert, dass es verwendet wird, um die Position des Stift Eingabe Panels durch Ändern des *linken* und des *oberen* Parameters zu ändern.</span><span class="sxs-lookup"><span data-stu-id="b3df3-118">The **PanelMoving** event is designed to be used to change the position of the pen input panel by changing the *Left* and *Top* parameters.</span></span>

<span data-ttu-id="b3df3-119">Die Methoden " [**pveto**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-moveto) " und " [**Refresh**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-refresh) " bewirken, dass das Objekt " [**pinputpanel**](peninputpanel-class.md) " seinen automatischen Positions Code aufruft, der ein **PanelMoving** -Ereignis auslöst.</span><span class="sxs-lookup"><span data-stu-id="b3df3-119">The [**MoveTo**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-moveto) and [**Refresh**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-refresh) methods cause the [**PenInputPanel**](peninputpanel-class.md) object to call its auto-positioning code which triggers a **PanelMoving** event.</span></span> <span data-ttu-id="b3df3-120">Folglich kann das Aufrufen dieser Methoden in einem **PanelMoving** -Handler zu einer rekursiven Endlosschleife führen.</span><span class="sxs-lookup"><span data-stu-id="b3df3-120">Consequently, calling these methods inside a **PanelMoving** handler can result in a recursive endless loop.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3df3-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b3df3-121">Requirements</span></span>



| <span data-ttu-id="b3df3-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b3df3-122">Requirement</span></span> | <span data-ttu-id="b3df3-123">Wert</span><span class="sxs-lookup"><span data-stu-id="b3df3-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3df3-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b3df3-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b3df3-125">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b3df3-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="b3df3-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b3df3-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b3df3-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b3df3-127">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="b3df3-128">Header</span><span class="sxs-lookup"><span data-stu-id="b3df3-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3df3-129"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="b3df3-129"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b3df3-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b3df3-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="b3df3-131"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3df3-131"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="b3df3-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b3df3-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3df3-133">**"Pendel Panel"**</span><span class="sxs-lookup"><span data-stu-id="b3df3-133">**PenInputPanel**</span></span>](peninputpanel-class.md)
</dt> </dl>

 

 




