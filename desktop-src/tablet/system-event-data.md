---
description: Enthält Informationen zu einem Tablet-System Ereignis.
ms.assetid: 725f4b43-0bcb-4452-a87f-b24a85de0049
title: SYSTEM_EVENT_DATA Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SYSTEM_EVENT_DATA
api_type:
- NA
api_location: ''
ms.openlocfilehash: 5d77c78a78a6cecae0368e8d9192a0dc0efc10e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218573"
---
# <a name="system_event_data-structure"></a><span data-ttu-id="c7ba4-103">System \_ Ereignis- \_ Datenstruktur</span><span class="sxs-lookup"><span data-stu-id="c7ba4-103">SYSTEM\_EVENT\_DATA structure</span></span>

<span data-ttu-id="c7ba4-104">Enthält Informationen zu einem Tablet-System Ereignis.</span><span class="sxs-lookup"><span data-stu-id="c7ba4-104">Contains information about a tablet system event.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7ba4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c7ba4-105">Syntax</span></span>


```C++
typedef struct tagSYSTEM_EVENT_DATA {
  BYTE  bModifier;
  WCHAR wKey;
  LONG  xPos;
  LONG  yPos;
  BYTE  bCursorMode;
  DWORD dwButtonState;
} SYSTEM_EVENT_DATA;
```



## <a name="members"></a><span data-ttu-id="c7ba4-106">Member</span><span class="sxs-lookup"><span data-stu-id="c7ba4-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c7ba4-107">**bmodifizierer**</span><span class="sxs-lookup"><span data-stu-id="c7ba4-107">**bModifier**</span></span>
</dt> <dd>

<span data-ttu-id="c7ba4-108">Bitwerte für die Modifizierer.</span><span class="sxs-lookup"><span data-stu-id="c7ba4-108">Bit values for the modifiers.</span></span> <span data-ttu-id="c7ba4-109">Weitere Informationen finden Sie im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="c7ba4-109">See the remarks section for more information.</span></span>

</dd> <dt>

<span data-ttu-id="c7ba4-110">**wkey**</span><span class="sxs-lookup"><span data-stu-id="c7ba4-110">**wKey**</span></span>
</dt> <dd>

<span data-ttu-id="c7ba4-111">Scannen Sie den Code nach dem Tastatur Zeichen.</span><span class="sxs-lookup"><span data-stu-id="c7ba4-111">Scan code for the keyboard character.</span></span>

</dd> <dt>

<span data-ttu-id="c7ba4-112">**XPos**</span><span class="sxs-lookup"><span data-stu-id="c7ba4-112">**xPos**</span></span>
</dt> <dd>

<span data-ttu-id="c7ba4-113">X-Position des Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="c7ba4-113">X position of the event.</span></span>

</dd> <dt>

<span data-ttu-id="c7ba4-114">**YPos**</span><span class="sxs-lookup"><span data-stu-id="c7ba4-114">**yPos**</span></span>
</dt> <dd>

<span data-ttu-id="c7ba4-115">Y-Position des Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="c7ba4-115">Y position of the event.</span></span>

</dd> <dt>

<span data-ttu-id="c7ba4-116">**bcurrsormode**</span><span class="sxs-lookup"><span data-stu-id="c7ba4-116">**bCursorMode**</span></span>
</dt> <dd>

<span data-ttu-id="c7ba4-117">Der Cursortyp, der das Ereignis verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="c7ba4-117">The type of cursor that caused the event.</span></span> <span data-ttu-id="c7ba4-118">Weitere Informationen finden Sie im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="c7ba4-118">See the remarks section for more information.</span></span>

</dd> <dt>

<span data-ttu-id="c7ba4-119">**dwbuttonstate**</span><span class="sxs-lookup"><span data-stu-id="c7ba4-119">**dwButtonState**</span></span>
</dt> <dd>

<span data-ttu-id="c7ba4-120">Der Zustand der Schaltflächen zum Zeitpunkt des System Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="c7ba4-120">State of the buttons at the time of the system event.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c7ba4-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c7ba4-121">Remarks</span></span>

<span data-ttu-id="c7ba4-122">Die folgenden Systemereignisse werden für die Verwendung im **bmodifier** -Member definiert.</span><span class="sxs-lookup"><span data-stu-id="c7ba4-122">The following system events are defined for use in the **bModifier** member.</span></span>



| <span data-ttu-id="c7ba4-123">Wert</span><span class="sxs-lookup"><span data-stu-id="c7ba4-123">Value</span></span>               | <span data-ttu-id="c7ba4-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c7ba4-124">Description</span></span>                  |
|---------------------|------------------------------|
| <span data-ttu-id="c7ba4-125">SE- \_ Modifizierer \_ STRG</span><span class="sxs-lookup"><span data-stu-id="c7ba4-125">SE\_MODIFIER\_CTRL</span></span>  | <span data-ttu-id="c7ba4-126">Die Steuerelement Taste wurde gedrückt.</span><span class="sxs-lookup"><span data-stu-id="c7ba4-126">The Control key was pressed.</span></span> |
| <span data-ttu-id="c7ba4-127">SE- \_ Modifizierer \_ alt</span><span class="sxs-lookup"><span data-stu-id="c7ba4-127">SE\_MODIFIER\_ALT</span></span>   | <span data-ttu-id="c7ba4-128">Die Alt-Taste wurde gedrückt.</span><span class="sxs-lookup"><span data-stu-id="c7ba4-128">The Alt key was pressed.</span></span>     |
| <span data-ttu-id="c7ba4-129">SE- \_ \_ modifiziererschicht</span><span class="sxs-lookup"><span data-stu-id="c7ba4-129">SE\_MODIFIER\_SHIFT</span></span> | <span data-ttu-id="c7ba4-130">Die UMSCHALTTASTE wurde gedrückt.</span><span class="sxs-lookup"><span data-stu-id="c7ba4-130">The Shift key was pressed.</span></span>   |



 

<span data-ttu-id="c7ba4-131">Die folgenden Systemereignisse sind für die Verwendung im **bcurrsormode** -Member definiert.</span><span class="sxs-lookup"><span data-stu-id="c7ba4-131">The following system events are defined for use in the **bCursorMode** member.</span></span>



| <span data-ttu-id="c7ba4-132">Wert</span><span class="sxs-lookup"><span data-stu-id="c7ba4-132">Value</span></span>              | <span data-ttu-id="c7ba4-133">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c7ba4-133">Description</span></span>               |
|--------------------|---------------------------|
| <span data-ttu-id="c7ba4-134">\_normaler \_ Cursor SE</span><span class="sxs-lookup"><span data-stu-id="c7ba4-134">SE\_NORMAL\_CURSOR</span></span> | <span data-ttu-id="c7ba4-135">Gibt den Stift Tipp an.</span><span class="sxs-lookup"><span data-stu-id="c7ba4-135">Indicates the pen tip.</span></span>    |
| <span data-ttu-id="c7ba4-136">SE- \_ \_ radierercursor</span><span class="sxs-lookup"><span data-stu-id="c7ba4-136">SE\_ERASER\_CURSOR</span></span> | <span data-ttu-id="c7ba4-137">Gibt den Stift Radierer an.</span><span class="sxs-lookup"><span data-stu-id="c7ba4-137">Indicates the pen eraser.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="c7ba4-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c7ba4-138">Requirements</span></span>



| <span data-ttu-id="c7ba4-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c7ba4-139">Requirement</span></span> | <span data-ttu-id="c7ba4-140">Wert</span><span class="sxs-lookup"><span data-stu-id="c7ba4-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="c7ba4-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c7ba4-141">Minimum supported client</span></span><br/> | <span data-ttu-id="c7ba4-142">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c7ba4-142">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c7ba4-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c7ba4-143">Minimum supported server</span></span><br/> | <span data-ttu-id="c7ba4-144">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c7ba4-144">None supported</span></span><br/>                                     |



## <a name="see-also"></a><span data-ttu-id="c7ba4-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c7ba4-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7ba4-146">**Istylusplugin:: systemevent-Methode**</span><span class="sxs-lookup"><span data-stu-id="c7ba4-146">**IStylusPlugin::SystemEvent Method**</span></span>](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-systemevent)
</dt> <dt>

[<span data-ttu-id="c7ba4-147">**Itableteventsink:: systemevent-Methode**</span><span class="sxs-lookup"><span data-stu-id="c7ba4-147">**ITabletEventSink::SystemEvent Method**</span></span>](itableteventsink-systemevent.md)
</dt> </dl>

 

 




