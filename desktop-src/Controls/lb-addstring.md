---
title: LB_ADDSTRING Meldung (Winuser. h)
description: Fügt einem Listenfeld eine Zeichenfolge hinzu. Wenn das Listenfeld nicht den lbs- \_ Sortier Stil hat, wird die Zeichenfolge am Ende der Liste hinzugefügt. Andernfalls wird die Zeichenfolge in die Liste eingefügt und die Liste sortiert.
ms.assetid: 924d9232-6e38-49c3-aa3e-19efd46b01ba
keywords:
- Windows-Steuerelemente für LB_ADDSTRING Meldung
topic_type:
- apiref
api_name:
- LB_ADDSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87e1c820b7a4c122012076c82ce20adc0d01e2e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040541"
---
# <a name="lb_addstring-message"></a><span data-ttu-id="7dcd8-106">LB- \_ AddString-Nachricht</span><span class="sxs-lookup"><span data-stu-id="7dcd8-106">LB\_ADDSTRING message</span></span>

<span data-ttu-id="7dcd8-107">Fügt einem Listenfeld eine Zeichenfolge hinzu.</span><span class="sxs-lookup"><span data-stu-id="7dcd8-107">Adds a string to a list box.</span></span> <span data-ttu-id="7dcd8-108">Wenn das Listenfeld nicht den lbs- [**\_ Sortier**](list-box-styles.md) Stil hat, wird die Zeichenfolge am Ende der Liste hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7dcd8-108">If the list box does not have the [**LBS\_SORT**](list-box-styles.md) style, the string is added to the end of the list.</span></span> <span data-ttu-id="7dcd8-109">Andernfalls wird die Zeichenfolge in die Liste eingefügt und die Liste sortiert.</span><span class="sxs-lookup"><span data-stu-id="7dcd8-109">Otherwise, the string is inserted into the list and the list is sorted.</span></span>

## <a name="parameters"></a><span data-ttu-id="7dcd8-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7dcd8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7dcd8-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7dcd8-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7dcd8-112">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="7dcd8-112">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7dcd8-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7dcd8-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7dcd8-114">Ein Zeiger auf die NULL-terminierte Zeichenfolge, die hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7dcd8-114">A pointer to the null-terminated string that is to be added.</span></span>

<span data-ttu-id="7dcd8-115">Wenn im Listenfeld ein vom Besitzer gezeichneter Stil, aber nicht der [**lbs \_ hasstrings**](list-box-styles.md) -Stil enthalten ist, wird dieser Parameter nicht als Zeichenfolge, sondern als Elementdaten gespeichert.</span><span class="sxs-lookup"><span data-stu-id="7dcd8-115">If the list box has an owner-drawn style but not the [**LBS\_HASSTRINGS**](list-box-styles.md) style, this parameter is stored as item data instead of a string.</span></span> <span data-ttu-id="7dcd8-116">Sie können die **lb- \_ GetItemData** -und **lb- \_ ltitemdata** -Nachrichten senden, um die Elementdaten abzurufen oder zu ändern.</span><span class="sxs-lookup"><span data-stu-id="7dcd8-116">You can send the **LB\_GETITEMDATA** and **LB\_SETITEMDATA** messages to retrieve or modify the item data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7dcd8-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7dcd8-117">Return value</span></span>

<span data-ttu-id="7dcd8-118">Der Rückgabewert ist der null basierte Index der Zeichenfolge im Listenfeld.</span><span class="sxs-lookup"><span data-stu-id="7dcd8-118">The return value is the zero-based index of the string in the list box.</span></span> <span data-ttu-id="7dcd8-119">Wenn ein Fehler auftritt, ist der Rückgabewert lb \_ Err.</span><span class="sxs-lookup"><span data-stu-id="7dcd8-119">If an error occurs, the return value is LB\_ERR.</span></span> <span data-ttu-id="7dcd8-120">Wenn nicht genügend Speicherplatz vorhanden ist, um die neue Zeichenfolge zu speichern, ist der Rückgabewert "lb \_ errspace".</span><span class="sxs-lookup"><span data-stu-id="7dcd8-120">If there is insufficient space to store the new string, the return value is LB\_ERRSPACE.</span></span>

## <a name="remarks"></a><span data-ttu-id="7dcd8-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7dcd8-121">Remarks</span></span>

<span data-ttu-id="7dcd8-122">Wenn im Listenfeld ein vom Besitzer gezeichneter Stil und der [**lbs- \_ Sortier**](list-box-styles.md) Stil, jedoch nicht der [**lbs \_ hasstrings**](list-box-styles.md) -Stil vorhanden ist, sendet das System die [**WM- \_ compareitem**](wm-compareitem.md) -Nachricht einmal oder mehrmals an den Besitzer des Listen Felds, um das neue Element ordnungsgemäß im Listenfeld zu platzieren.</span><span class="sxs-lookup"><span data-stu-id="7dcd8-122">If the list box has an owner-drawn style and the [**LBS\_SORT**](list-box-styles.md) style, but not the [**LBS\_HASSTRINGS**](list-box-styles.md) style, the system sends the [**WM\_COMPAREITEM**](wm-compareitem.md) message one or more times to the owner of the list box to place the new item properly in the list box.</span></span>

<span data-ttu-id="7dcd8-123">Die " [**lb- \_ InitStorage**](lb-initstorage.md) "-Nachricht beschleunigt die Initialisierung von Listenfeldern, die über eine große Anzahl von Elementen (mehr als 100) verfügen.</span><span class="sxs-lookup"><span data-stu-id="7dcd8-123">The [**LB\_INITSTORAGE**](lb-initstorage.md) message helps speed up the initialization of list boxes that have a large number of items (more than 100).</span></span> <span data-ttu-id="7dcd8-124">Sie reserviert die angegebene Menge an Arbeitsspeicher, sodass nachfolgende **lb- \_ AddString** -Nachrichten die kürzeste Zeit in Anspruch nehmen.</span><span class="sxs-lookup"><span data-stu-id="7dcd8-124">It reserves the specified amount of memory so that subsequent **LB\_ADDSTRING** messages take the shortest possible time.</span></span> <span data-ttu-id="7dcd8-125">Sie können Schätzwerte für den *wParam* -Parameter und den *LPARAM* -Parameter verwenden.</span><span class="sxs-lookup"><span data-stu-id="7dcd8-125">You can use estimates for the *wParam* and *lParam* parameters.</span></span> <span data-ttu-id="7dcd8-126">Wenn Sie den Wert überschätzen, wird der zusätzliche Arbeitsspeicher zugeordnet. Wenn Sie unterschätzen, wird die normale Zuordnung für Elemente verwendet, die den angeforderten Betrag überschreiten.</span><span class="sxs-lookup"><span data-stu-id="7dcd8-126">If you overestimate, the extra memory is allocated; if you underestimate, the normal allocation is used for items that exceed the requested amount.</span></span>

<span data-ttu-id="7dcd8-127">Wenn das Listenfeld den [**WS- \_ HScroll**](/windows/desktop/winmsg/window-styles) -Stil aufweist und Sie eine Zeichenfolge hinzufügen, die breiter als das Listenfeld ist, senden Sie eine [**lb- \_ lthorizontalblock**](lb-sethorizontalextent.md) -Nachricht, um sicherzustellen, dass die horizontale Schiebe Leiste</span><span class="sxs-lookup"><span data-stu-id="7dcd8-127">If the list box has the [**WS\_HSCROLL**](/windows/desktop/winmsg/window-styles) style and you add a string wider than the list box, send an [**LB\_SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) message to ensure the horizontal scroll bar appears.</span></span>

<span data-ttu-id="7dcd8-128">Für eine ANSI-Anwendung konvertiert das System den Text in einem Listenfeld mithilfe von CP ACP in Unicode \_ .</span><span class="sxs-lookup"><span data-stu-id="7dcd8-128">For an ANSI application, the system converts the text in a list box to Unicode using CP\_ACP.</span></span> <span data-ttu-id="7dcd8-129">Dies kann zu Problemen führen.</span><span class="sxs-lookup"><span data-stu-id="7dcd8-129">This can cause problems.</span></span> <span data-ttu-id="7dcd8-130">Beispielsweise werden Zeichen mit untergeordneten Zeichen in einem nicht-Unicode-Listenfeld in einem japanischen Fenster gegartet.</span><span class="sxs-lookup"><span data-stu-id="7dcd8-130">For example, accented Roman characters in a non-Unicode list box in Japanese Windows will come out garbled.</span></span> <span data-ttu-id="7dcd8-131">Um dieses Problem zu beheben, kompilieren Sie die Anwendung entweder als Unicode, oder verwenden Sie ein vom Besitzer gezeichnetes Listenfeld.</span><span class="sxs-lookup"><span data-stu-id="7dcd8-131">To fix this, either compile the application as Unicode or use an owner-drawn list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="7dcd8-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7dcd8-132">Requirements</span></span>



| <span data-ttu-id="7dcd8-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7dcd8-133">Requirement</span></span> | <span data-ttu-id="7dcd8-134">Wert</span><span class="sxs-lookup"><span data-stu-id="7dcd8-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7dcd8-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7dcd8-135">Minimum supported client</span></span><br/> | <span data-ttu-id="7dcd8-136">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7dcd8-136">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7dcd8-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7dcd8-137">Minimum supported server</span></span><br/> | <span data-ttu-id="7dcd8-138">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7dcd8-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7dcd8-139">Header</span><span class="sxs-lookup"><span data-stu-id="7dcd8-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="7dcd8-140"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="7dcd8-140"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7dcd8-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7dcd8-141">See also</span></span>

<dl> <dt>

<span data-ttu-id="7dcd8-142">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="7dcd8-142">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7dcd8-143">**LB- \_ deletestring**</span><span class="sxs-lookup"><span data-stu-id="7dcd8-143">**LB\_DELETESTRING**</span></span>](lb-deletestring.md)
</dt> <dt>

[<span data-ttu-id="7dcd8-144">**LB- \_ InsertString**</span><span class="sxs-lookup"><span data-stu-id="7dcd8-144">**LB\_INSERTSTRING**</span></span>](lb-insertstring.md)
</dt> <dt>

[<span data-ttu-id="7dcd8-145">**LB- \_ SelectString**</span><span class="sxs-lookup"><span data-stu-id="7dcd8-145">**LB\_SELECTSTRING**</span></span>](lb-selectstring.md)
</dt> <dt>

[<span data-ttu-id="7dcd8-146">**LB-Abbild \_ Umfang**</span><span class="sxs-lookup"><span data-stu-id="7dcd8-146">**LB\_SETHORIZONTALEXTENT**</span></span>](lb-sethorizontalextent.md)
</dt> <dt>

[<span data-ttu-id="7dcd8-147">**WM- \_ compareitem**</span><span class="sxs-lookup"><span data-stu-id="7dcd8-147">**WM\_COMPAREITEM**</span></span>](wm-compareitem.md)
</dt> </dl>

 

