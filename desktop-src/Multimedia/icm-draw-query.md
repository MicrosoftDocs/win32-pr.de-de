---
title: ICM_DRAW_QUERY Meldung (VFW. h)
description: Die ICM \_ - \_ Abfrage Nachricht fragt einen renderingtreiber ab, um zu bestimmen, ob Daten in einem bestimmten Format gerendert werden können. Sie können diese Nachricht explizit oder mithilfe des icdrawquery-Makros senden.
ms.assetid: b829a04b-c1be-47c6-96e9-a6dc6f802811
keywords:
- ICM_DRAW_QUERY-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_DRAW_QUERY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27266484cffa503583df32b60c6e8a0c04f344f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477256"
---
# <a name="icm_draw_query-message"></a><span data-ttu-id="2fe41-105">ICM \_ - \_ Abfrage Nachricht zeichnen</span><span class="sxs-lookup"><span data-stu-id="2fe41-105">ICM\_DRAW\_QUERY message</span></span>

<span data-ttu-id="2fe41-106">Die **ICM \_ - \_ Abfrage** Nachricht fragt einen renderingtreiber ab, um zu bestimmen, ob Daten in einem bestimmten Format gerendert werden können.</span><span class="sxs-lookup"><span data-stu-id="2fe41-106">The **ICM\_DRAW\_QUERY** message queries a rendering driver to determine if it can render data in a specific format.</span></span> <span data-ttu-id="2fe41-107">Sie können diese Nachricht explizit oder mithilfe des [**icdrawquery**](/windows/desktop/api/Vfw/nf-vfw-icdrawquery) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="2fe41-107">You can send this message explicitly or by using the [**ICDrawQuery**](/windows/desktop/api/Vfw/nf-vfw-icdrawquery) macro.</span></span>


```C++
ICM_DRAW_QUERY 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="2fe41-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2fe41-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2fe41-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiinput*</span><span class="sxs-lookup"><span data-stu-id="2fe41-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span></span>
</dt> <dd>

<span data-ttu-id="2fe41-110">Zeiger auf eine [**BitmapInfo**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) -Struktur, die das Eingabeformat enthält.</span><span class="sxs-lookup"><span data-stu-id="2fe41-110">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the input format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2fe41-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2fe41-111">Return Value</span></span>

<span data-ttu-id="2fe41-112">Gibt ICERR \_ OK zurück, wenn der Treiber die Daten im angegebenen Format oder im angegebenen Format von ICERR badformat Renderen kann \_ .</span><span class="sxs-lookup"><span data-stu-id="2fe41-112">Returns ICERR\_OK if the driver can render data in the specified format or ICERR\_BADFORMAT otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="2fe41-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2fe41-113">Remarks</span></span>

<span data-ttu-id="2fe41-114">Diese Meldung unterscheidet sich von der [**ICM \_ Draw \_ Begin**](icm-draw-begin.md) -Meldung darin, dass der Treiber allgemein abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="2fe41-114">This message differs from the [**ICM\_DRAW\_BEGIN**](icm-draw-begin.md) message in that it queries the driver in a general sense.</span></span> <span data-ttu-id="2fe41-115">**ICM \_ Zeichnen \_ Begin** bestimmt, ob der Treiber die Daten unter bestimmten Bedingungen unter Verwendung des angegebenen Formats zeichnen kann, z. b. durch Streckung des Bilds.</span><span class="sxs-lookup"><span data-stu-id="2fe41-115">**ICM\_DRAW\_BEGIN** determines if the driver can draw the data using the specified format under specific conditions, such as stretching the image.</span></span>

## <a name="requirements"></a><span data-ttu-id="2fe41-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2fe41-116">Requirements</span></span>



| <span data-ttu-id="2fe41-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2fe41-117">Requirement</span></span> | <span data-ttu-id="2fe41-118">Wert</span><span class="sxs-lookup"><span data-stu-id="2fe41-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="2fe41-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2fe41-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2fe41-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2fe41-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="2fe41-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2fe41-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2fe41-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2fe41-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2fe41-123">Header</span><span class="sxs-lookup"><span data-stu-id="2fe41-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2fe41-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="2fe41-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2fe41-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2fe41-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fe41-126">Videokomprimierungs-Manager</span><span class="sxs-lookup"><span data-stu-id="2fe41-126">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="2fe41-127">Video Komprimierungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="2fe41-127">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

