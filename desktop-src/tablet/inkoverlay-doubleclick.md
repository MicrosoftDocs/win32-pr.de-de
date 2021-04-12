---
description: Tritt auf, wenn auf das InkCollector-oder InkOverlay-Objekt Doppel geklickt wird.
ms.assetid: 76ea40d4-82cf-420a-a9eb-66cb0492b43b
title: InkOverlay. DoubleClick-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4baddc89e309b7d64ba2294827b58956b3e6c47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217680"
---
# <a name="inkoverlaydoubleclick-event"></a><span data-ttu-id="df133-103">InkOverlay. DoubleClick-Ereignis</span><span class="sxs-lookup"><span data-stu-id="df133-103">InkOverlay.DoubleClick event</span></span>

<span data-ttu-id="df133-104">Tritt auf, wenn auf das [**InkCollector**](inkcollector-class.md) -oder [**InkOverlay**](inkoverlay-class.md) -Objekt Doppel geklickt wird.</span><span class="sxs-lookup"><span data-stu-id="df133-104">Occurs when the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object is double-clicked.</span></span>

## <a name="syntax"></a><span data-ttu-id="df133-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="df133-105">Syntax</span></span>


```C++
void DoubleClick(
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="df133-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="df133-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df133-107">*Abbrechen* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="df133-107">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="df133-108">Ob das Ereignis für das übergeordnete Steuerelement abgebrochen werden soll.</span><span class="sxs-lookup"><span data-stu-id="df133-108">Whether the event should be canceled for the parent control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df133-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="df133-109">Return value</span></span>

<span data-ttu-id="df133-110">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="df133-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="df133-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="df133-111">Remarks</span></span>

<span data-ttu-id="df133-112">Diese Ereignismethode wird in den \_ Schnittstellen iinkcollectorevents, \_ iinkoverlayevents und \_ iinkpictureevents Dispatch-only (Dispinterfaces) mit der ID DISPID \_ ipedblclick definiert.</span><span class="sxs-lookup"><span data-stu-id="df133-112">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEDblClick.</span></span>

## <a name="requirements"></a><span data-ttu-id="df133-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="df133-113">Requirements</span></span>



| <span data-ttu-id="df133-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="df133-114">Requirement</span></span> | <span data-ttu-id="df133-115">Wert</span><span class="sxs-lookup"><span data-stu-id="df133-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df133-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="df133-116">Minimum supported client</span></span><br/> | <span data-ttu-id="df133-117">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="df133-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="df133-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="df133-118">Minimum supported server</span></span><br/> | <span data-ttu-id="df133-119">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="df133-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="df133-120">Header</span><span class="sxs-lookup"><span data-stu-id="df133-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="df133-121"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="df133-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="df133-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="df133-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="df133-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df133-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="df133-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="df133-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df133-125">**InkOverlay-Klasse**</span><span class="sxs-lookup"><span data-stu-id="df133-125">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> </dl>

 

 




