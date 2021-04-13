---
description: Veraltet. Der "tzinputpanel" wurde durch den Text Eingabe Panel (Tip) ersetzt. Tritt auf, wenn sich das Objekt "pinputpanel" zwischen Layouts ändert.
ms.assetid: 21d38406-7ed9-4741-a092-ed3a369dc0dc
title: "\"Pinputpanel. PanelChanged\"-Ereignis (msink AUT. h)"
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d6ff0f415e12131221a8dad1c0775a347ef96cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347869"
---
# <a name="peninputpanelpanelchanged-event"></a><span data-ttu-id="a08b4-104">"Pinputpanel. PanelChanged"-Ereignis</span><span class="sxs-lookup"><span data-stu-id="a08b4-104">PenInputPanel.PanelChanged event</span></span>

<span data-ttu-id="a08b4-105">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="a08b4-105">Deprecated.</span></span> <span data-ttu-id="a08b4-106">Der " [**tzinputpanel**](peninputpanel-class.md) " wurde durch den [Text Eingabe Panel (Tip)](text-input-panel-reference.md)ersetzt.</span><span class="sxs-lookup"><span data-stu-id="a08b4-106">The [**PenInputPanel**](peninputpanel-class.md) has been replaced by the [Text Input Panel (TIP)](text-input-panel-reference.md).</span></span>

<span data-ttu-id="a08b4-107">Tritt auf, wenn sich das Objekt " [**pinputpanel**](peninputpanel-class.md) " zwischen Layouts ändert.</span><span class="sxs-lookup"><span data-stu-id="a08b4-107">Occurs when the [**PenInputPanel**](peninputpanel-class.md) object changes between layouts.</span></span>

## <a name="syntax"></a><span data-ttu-id="a08b4-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a08b4-108">Syntax</span></span>


```C++
HRESULT PanelChanged(
  [in] PanelType NewPanelType
);
```



## <a name="parameters"></a><span data-ttu-id="a08b4-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a08b4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a08b4-110">*Newpaneltype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a08b4-110">*NewPanelType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a08b4-111">Der neue Panel-Typ, der nach dem Auslösen des **PanelChanged** -Ereignisses für die Eingabe innerhalb des " [**kinputpanel**](peninputpanel-class.md) "-Objekts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a08b4-111">The new panel type used for input within the [**PenInputPanel**](peninputpanel-class.md) object, after the **PanelChanged** event fires.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a08b4-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a08b4-112">Return value</span></span>

<span data-ttu-id="a08b4-113">Wenn dieses Ereignis erfolgreich ist, gibt es " **S \_ OK**" zurück.</span><span class="sxs-lookup"><span data-stu-id="a08b4-113">If this event succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a08b4-114">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a08b4-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a08b4-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a08b4-115">Remarks</span></span>

<span data-ttu-id="a08b4-116">Beim Erstellen eines " [**pinputpanel**](peninputpanel-class.md) "-Objekts ist [**Handschrift**](/windows/win32/api/peninputpanel/ne-peninputpanel-paneltype) der standardmäßige **PanelType**.</span><span class="sxs-lookup"><span data-stu-id="a08b4-116">When creating a [**PenInputPanel**](peninputpanel-class.md) object, [**Handwriting**](/windows/win32/api/peninputpanel/ne-peninputpanel-paneltype) is the default **PanelType**.</span></span> <span data-ttu-id="a08b4-117">Wenn Sie den Bereich ändern, indem Sie die [**CurrentPanel**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_currentpanel) -Eigenschaft festlegen, bevor der Stift Eingabebereich zum ersten Mal aktiviert wird, tritt ein **PanelChanged** -Ereignis auf.</span><span class="sxs-lookup"><span data-stu-id="a08b4-117">If you change the panel by setting the [**CurrentPanel**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_currentpanel) property before the pen input panel becomes active for the first time, a **PanelChanged** event occurs.</span></span>

<span data-ttu-id="a08b4-118">Das **PanelChanged** -Ereignis wird nicht ausgelöst, wenn sich der Benutzer zwischen den gepackten und geschachtelten Schreibvorgängen ändert.</span><span class="sxs-lookup"><span data-stu-id="a08b4-118">The **PanelChanged** event is not raised when the user changes between Lined and Boxed writing pads.</span></span>

## <a name="requirements"></a><span data-ttu-id="a08b4-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a08b4-119">Requirements</span></span>



| <span data-ttu-id="a08b4-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a08b4-120">Requirement</span></span> | <span data-ttu-id="a08b4-121">Wert</span><span class="sxs-lookup"><span data-stu-id="a08b4-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a08b4-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a08b4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a08b4-123">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a08b4-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="a08b4-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a08b4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a08b4-125">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a08b4-125">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="a08b4-126">Header</span><span class="sxs-lookup"><span data-stu-id="a08b4-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a08b4-127"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="a08b4-127"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a08b4-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a08b4-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="a08b4-129"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a08b4-129"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="a08b4-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a08b4-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a08b4-131">**"Pendel Panel"**</span><span class="sxs-lookup"><span data-stu-id="a08b4-131">**PenInputPanel**</span></span>](peninputpanel-class.md)
</dt> </dl>

 

 
