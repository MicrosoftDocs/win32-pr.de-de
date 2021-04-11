---
title: MCM_SETCOLOR Meldung (kommstrg. h)
description: Legt die Farbe für einen angegebenen Teil eines Monatskalender-Steuer Elements fest. Sie können diese Nachricht explizit oder mit dem monthcal- \_ SetColor-Makro senden.
ms.assetid: 4ceb7b0e-82be-474a-a163-7e71356818c0
keywords:
- Windows-Steuerelemente für MCM_SETCOLOR Meldung
topic_type:
- apiref
api_name:
- MCM_SETCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 476aafd8356359cf6b4313f4b945253af6b493c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105987"
---
# <a name="mcm_setcolor-message"></a><span data-ttu-id="1e066-105">MCM- \_ SetColor-Meldung</span><span class="sxs-lookup"><span data-stu-id="1e066-105">MCM\_SETCOLOR message</span></span>

<span data-ttu-id="1e066-106">Legt die Farbe für einen angegebenen Teil eines Monatskalender-Steuer Elements fest.</span><span class="sxs-lookup"><span data-stu-id="1e066-106">Sets the color for a given portion of a month calendar control.</span></span> <span data-ttu-id="1e066-107">Sie können diese Nachricht explizit oder mit dem [**monthcal- \_ SetColor**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcolor) -Makro senden.</span><span class="sxs-lookup"><span data-stu-id="1e066-107">You can send this message explicitly or by using the [**MonthCal\_SetColor**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="1e066-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1e066-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e066-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1e066-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1e066-110">Ein Wert vom Typ **int** , der angibt, welche Monatskalender Farbe festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1e066-110">Value of type **int** specifying which month calendar color to set.</span></span> <span data-ttu-id="1e066-111">Die folgenden Werte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="1e066-111">This value can be one of the following:</span></span>



| <span data-ttu-id="1e066-112">Wert</span><span class="sxs-lookup"><span data-stu-id="1e066-112">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="1e066-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="1e066-113">Meaning</span></span>                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCSC_BACKGROUND"></span><span id="mcsc_background"></span><dl> <span data-ttu-id="1e066-114"><dt>**MCSC- \_ Hintergrund**</dt></span><span class="sxs-lookup"><span data-stu-id="1e066-114"><dt>**MCSC\_BACKGROUND**</dt></span></span> </dl>       | <span data-ttu-id="1e066-115">Legen Sie die zwischen den Monaten angezeigte Hintergrundfarbe fest.</span><span class="sxs-lookup"><span data-stu-id="1e066-115">Set the background color displayed between months.</span></span><br/>                                                                                                                                      |
| <span id="MCSC_MONTHBK"></span><span id="mcsc_monthbk"></span><dl> <span data-ttu-id="1e066-116"><dt>**MCSC \_ monthbk**</dt></span><span class="sxs-lookup"><span data-stu-id="1e066-116"><dt>**MCSC\_MONTHBK**</dt></span></span> </dl>                | <span data-ttu-id="1e066-117">Legen Sie die im Monat angezeigte Hintergrundfarbe fest.</span><span class="sxs-lookup"><span data-stu-id="1e066-117">Set the background color displayed within the month.</span></span><br/>                                                                                                                                    |
| <span id="MCSC_TEXT"></span><span id="mcsc_text"></span><dl> <span data-ttu-id="1e066-118"><dt>**MCSC- \_ Text**</dt></span><span class="sxs-lookup"><span data-stu-id="1e066-118"><dt>**MCSC\_TEXT**</dt></span></span> </dl>                         | <span data-ttu-id="1e066-119">Legen Sie die Farbe fest, mit der Text innerhalb eines Monats angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="1e066-119">Set the color used to display text within a month.</span></span><br/>                                                                                                                                      |
| <span id="MCSC_TITLEBK"></span><span id="mcsc_titlebk"></span><dl> <span data-ttu-id="1e066-120"><dt>**MCSC \_ titlebk**</dt></span><span class="sxs-lookup"><span data-stu-id="1e066-120"><dt>**MCSC\_TITLEBK**</dt></span></span> </dl>                | <span data-ttu-id="1e066-121">Legen Sie die im Titel des Kalenders angezeigte Hintergrundfarbe fest.</span><span class="sxs-lookup"><span data-stu-id="1e066-121">Set the background color displayed in the calendar's title.</span></span><br/>                                                                                                                             |
| <span id="MCSC_TITLETEXT"></span><span id="mcsc_titletext"></span><dl> <span data-ttu-id="1e066-122"><dt>**MCSC \_ TitleText**</dt></span><span class="sxs-lookup"><span data-stu-id="1e066-122"><dt>**MCSC\_TITLETEXT**</dt></span></span> </dl>          | <span data-ttu-id="1e066-123">Legen Sie die Farbe fest, die verwendet wird, um Text innerhalb des Kalender Titels anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="1e066-123">Set the color used to display text within the calendar's title.</span></span><br/>                                                                                                                         |
| <span id="MCSC_TRAILINGTEXT"></span><span id="mcsc_trailingtext"></span><dl> <span data-ttu-id="1e066-124"><dt>**MCSC- \_ trailingtext**</dt></span><span class="sxs-lookup"><span data-stu-id="1e066-124"><dt>**MCSC\_TRAILINGTEXT**</dt></span></span> </dl> | <span data-ttu-id="1e066-125">Legen Sie die Farbe fest, die verwendet wird, um den Header Tag und den nachfolgenden Tag</span><span class="sxs-lookup"><span data-stu-id="1e066-125">Set the color used to display header day and trailing day text.</span></span> <span data-ttu-id="1e066-126">Header und nachfolgende Tage sind die Tage aus den vorherigen und den nächsten Monaten, die im Kalender des aktuellen Monats angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="1e066-126">Header and trailing days are the days from the previous and following months that appear on the current month calendar.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1e066-127">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1e066-127">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1e066-128">[**COLORREF**](/windows/desktop/gdi/colorref) -Wert, der die Farbe darstellt, die für den angegebenen Bereich des Monats Kalenders festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="1e066-128">[**COLORREF**](/windows/desktop/gdi/colorref) value that represents the color that will be set for the specified area of the month calendar.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e066-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1e066-129">Return value</span></span>

<span data-ttu-id="1e066-130">Gibt einen [**COLORREF**](/windows/desktop/gdi/colorref) -Wert zurück, der die vorherige Farbeinstellung für den angegebenen Teil des Monatskalender-Steuer Elements darstellt, wenn erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="1e066-130">Returns a [**COLORREF**](/windows/desktop/gdi/colorref) value that represents the previous color setting for the specified portion of the month calendar control if successful.</span></span> <span data-ttu-id="1e066-131">Andernfalls ist die Rückgabe-1.</span><span class="sxs-lookup"><span data-stu-id="1e066-131">Otherwise, the return is -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e066-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1e066-132">Remarks</span></span>

<span data-ttu-id="1e066-133">Wenn visuelle Stile aktiviert sind, hat diese Nachricht keine Auswirkung, es sei denn, *wParam* ist ein MCSC- \_ Hintergrund.</span><span class="sxs-lookup"><span data-stu-id="1e066-133">If visual styles are active, this message has no effect except when *wParam* is MCSC\_BACKGROUND.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e066-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1e066-134">Requirements</span></span>



| <span data-ttu-id="1e066-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1e066-135">Requirement</span></span> | <span data-ttu-id="1e066-136">Wert</span><span class="sxs-lookup"><span data-stu-id="1e066-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1e066-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1e066-137">Minimum supported client</span></span><br/> | <span data-ttu-id="1e066-138">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1e066-138">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1e066-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1e066-139">Minimum supported server</span></span><br/> | <span data-ttu-id="1e066-140">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1e066-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1e066-141">Header</span><span class="sxs-lookup"><span data-stu-id="1e066-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e066-142"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e066-142"><dt>Commctrl.h</dt></span></span> </dl> |



 

