---
title: TBM_SETPAGESIZE Meldung (kommstrg. h)
description: Legt die Anzahl der logischen Positionen fest, die der Schieberegler der TrackBar als Reaktion auf Tastatureingaben bewegt, wie z. b. die-Taste oder die-Taste oder Maus Eingaben, z. b. Klicks im Kanal der Trackleiste.
ms.assetid: 34edb868-4b6b-4b3f-b315-3ce39346b134
keywords:
- Windows-Steuerelemente für TBM_SETPAGESIZE Meldung
topic_type:
- apiref
api_name:
- TBM_SETPAGESIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec5d8a396bb605b4276346e84e7b46bfbefe0657
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040838"
---
# <a name="tbm_setpagesize-message"></a><span data-ttu-id="54953-104">TBM- \_ setPageSize-Meldung</span><span class="sxs-lookup"><span data-stu-id="54953-104">TBM\_SETPAGESIZE message</span></span>

<span data-ttu-id="54953-105">Legt die Anzahl der logischen Positionen fest, die der Schieberegler der TrackBar als Reaktion auf Tastatureingaben bewegt, wie z. b. die-Taste oder die-Taste oder Maus Eingaben, z. b. Klicks im Kanal der Trackleiste.</span><span class="sxs-lookup"><span data-stu-id="54953-105">Sets the number of logical positions the trackbar's slider moves in response to keyboard input, such as the or keys, or mouse input, such as clicks in the trackbar's channel.</span></span> <span data-ttu-id="54953-106">Bei den logischen Positionen handelt es sich um die ganzzahligen Inkremente in der TrackBar im Bereich der minimalen bis zum maximalen Schieberegler.</span><span class="sxs-lookup"><span data-stu-id="54953-106">The logical positions are the integer increments in the trackbar's range of minimum to maximum slider positions.</span></span>

## <a name="parameters"></a><span data-ttu-id="54953-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="54953-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54953-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="54953-108">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="54953-109">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="54953-109">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="54953-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="54953-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="54953-111">Neue Seitengröße.</span><span class="sxs-lookup"><span data-stu-id="54953-111">New page size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54953-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="54953-112">Return value</span></span>

<span data-ttu-id="54953-113">Gibt einen 32-Bit-Wert zurück, der die vorherige Seitengröße angibt.</span><span class="sxs-lookup"><span data-stu-id="54953-113">Returns a 32-bit value that specifies the previous page size.</span></span>

## <a name="remarks"></a><span data-ttu-id="54953-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="54953-114">Remarks</span></span>

<span data-ttu-id="54953-115">Die TrackBar sendet außerdem eine [**WM- \_ HScroll**](wm-hscroll.md) -oder [**WM- \_ VScroll**](wm-vscroll.md) -Nachricht mit den e \_ -v-Nachrichten-und TB- \_ PageDown-Benachrichtigungs Codes an das übergeordnete Fenster, wenn Sie Tastatur-oder Maus Eingaben empfängt, die die Seite</span><span class="sxs-lookup"><span data-stu-id="54953-115">The trackbar also sends a [**WM\_HSCROLL**](wm-hscroll.md) or [**WM\_VSCROLL**](wm-vscroll.md) message with the TB\_PAGEUP and TB\_PAGEDOWN notification codes to its parent window when it receives keyboard or mouse input that scrolls the page.</span></span>

## <a name="requirements"></a><span data-ttu-id="54953-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="54953-116">Requirements</span></span>



| <span data-ttu-id="54953-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="54953-117">Requirement</span></span> | <span data-ttu-id="54953-118">Wert</span><span class="sxs-lookup"><span data-stu-id="54953-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="54953-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="54953-119">Minimum supported client</span></span><br/> | <span data-ttu-id="54953-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="54953-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="54953-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="54953-121">Minimum supported server</span></span><br/> | <span data-ttu-id="54953-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="54953-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="54953-123">Header</span><span class="sxs-lookup"><span data-stu-id="54953-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="54953-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="54953-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54953-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="54953-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54953-126">**TBM \_ getpagesize**</span><span class="sxs-lookup"><span data-stu-id="54953-126">**TBM\_GETPAGESIZE**</span></span>](tbm-getpagesize.md)
</dt> </dl>

 

 





