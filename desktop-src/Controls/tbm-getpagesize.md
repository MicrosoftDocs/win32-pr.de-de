---
title: TBM_GETPAGESIZE Meldung (kommstrg. h)
description: Ruft die Anzahl logischer Positionen ab, die der Schieberegler der TrackBar als Reaktion auf Tastatureingaben bewegt, z. b. die-Taste oder die-Taste, oder Maus Eingaben, z. b. Klicks im Kanal der Trackleiste.
ms.assetid: f0c5feac-2723-440e-96c0-dac37b0531ed
keywords:
- Windows-Steuerelemente für TBM_GETPAGESIZE Meldung
topic_type:
- apiref
api_name:
- TBM_GETPAGESIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac58c0b935b468cf8af565fba2db67c88418ee4f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103755"
---
# <a name="tbm_getpagesize-message"></a><span data-ttu-id="dbc85-104">TBM- \_ getpagesize-Meldung</span><span class="sxs-lookup"><span data-stu-id="dbc85-104">TBM\_GETPAGESIZE message</span></span>

<span data-ttu-id="dbc85-105">Ruft die Anzahl logischer Positionen ab, die der Schieberegler der TrackBar als Reaktion auf Tastatureingaben bewegt, z. b. die-Taste oder die-Taste, oder Maus Eingaben, z. b. Klicks im Kanal der Trackleiste.</span><span class="sxs-lookup"><span data-stu-id="dbc85-105">Retrieves the number of logical positions the trackbar's slider moves in response to keyboard input, such as the or keys, or mouse input, such as clicks in the trackbar's channel.</span></span> <span data-ttu-id="dbc85-106">Bei den logischen Positionen handelt es sich um die ganzzahligen Inkremente in der TrackBar im Bereich der minimalen bis zum maximalen Schieberegler.</span><span class="sxs-lookup"><span data-stu-id="dbc85-106">The logical positions are the integer increments in the trackbar's range of minimum to maximum slider positions.</span></span>

## <a name="parameters"></a><span data-ttu-id="dbc85-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="dbc85-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbc85-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dbc85-108">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="dbc85-109">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="dbc85-109">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="dbc85-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dbc85-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="dbc85-111">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="dbc85-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbc85-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dbc85-112">Return value</span></span>

<span data-ttu-id="dbc85-113">Gibt einen 32-Bit-Wert zurück, der die Seitengröße für die TrackBar angibt.</span><span class="sxs-lookup"><span data-stu-id="dbc85-113">Returns a 32-bit value that specifies the page size for the trackbar.</span></span>

## <a name="remarks"></a><span data-ttu-id="dbc85-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dbc85-114">Remarks</span></span>

<span data-ttu-id="dbc85-115">Die TrackBar sendet außerdem eine [**WM- \_ HScroll**](wm-hscroll.md) -oder [**WM- \_ VScroll**](wm-vscroll.md) -Nachricht mit den e \_ -v-Nachrichten-und TB- \_ PageDown-Benachrichtigungs Codes an das übergeordnete Fenster, wenn Sie Tastatur-oder Maus Eingaben empfängt, die die Seite</span><span class="sxs-lookup"><span data-stu-id="dbc85-115">The trackbar also sends a [**WM\_HSCROLL**](wm-hscroll.md) or [**WM\_VSCROLL**](wm-vscroll.md) message with the TB\_PAGEUP and TB\_PAGEDOWN notification codes to its parent window when it receives keyboard or mouse input that scrolls the page.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbc85-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dbc85-116">Requirements</span></span>



| <span data-ttu-id="dbc85-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dbc85-117">Requirement</span></span> | <span data-ttu-id="dbc85-118">Wert</span><span class="sxs-lookup"><span data-stu-id="dbc85-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dbc85-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dbc85-119">Minimum supported client</span></span><br/> | <span data-ttu-id="dbc85-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dbc85-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dbc85-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dbc85-121">Minimum supported server</span></span><br/> | <span data-ttu-id="dbc85-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dbc85-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dbc85-123">Header</span><span class="sxs-lookup"><span data-stu-id="dbc85-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="dbc85-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="dbc85-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbc85-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dbc85-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbc85-126">**TBM \_ setPageSize**</span><span class="sxs-lookup"><span data-stu-id="dbc85-126">**TBM\_SETPAGESIZE**</span></span>](tbm-setpagesize.md)
</dt> </dl>

 

 





