---
title: LB_INSERTSTRING Meldung (Winuser. h)
description: Fügt eine Zeichenfolge oder Elementdaten in ein Listenfeld ein. Anders als bei der LB \_ AddString-Nachricht bewirkt die LB- \_ InsertString-Nachricht nicht, dass eine Liste mit dem lbs- \_ Sortier Stil sortiert wird.
ms.assetid: dfaa742d-2f42-4485-aed5-cda8ca9ba66c
keywords:
- Windows-Steuerelemente für LB_INSERTSTRING Meldung
topic_type:
- apiref
api_name:
- LB_INSERTSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5858af0e0229f90a5ed9928e7478d0ac9a71c8f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105543"
---
# <a name="lb_insertstring-message"></a><span data-ttu-id="74dad-105">LB- \_ InsertString-Nachricht</span><span class="sxs-lookup"><span data-stu-id="74dad-105">LB\_INSERTSTRING message</span></span>

<span data-ttu-id="74dad-106">Fügt eine Zeichenfolge oder Elementdaten in ein Listenfeld ein.</span><span class="sxs-lookup"><span data-stu-id="74dad-106">Inserts a string or item data into a list box.</span></span> <span data-ttu-id="74dad-107">Anders als bei der [**lb \_ AddString**](lb-addstring.md) -Nachricht bewirkt die **lb- \_ InsertString** -Nachricht nicht, dass eine Liste mit dem [**lbs- \_ Sortier**](list-box-styles.md) Stil sortiert wird.</span><span class="sxs-lookup"><span data-stu-id="74dad-107">Unlike the [**LB\_ADDSTRING**](lb-addstring.md) message, the **LB\_INSERTSTRING** message does not cause a list with the [**LBS\_SORT**](list-box-styles.md) style to be sorted.</span></span>

## <a name="parameters"></a><span data-ttu-id="74dad-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="74dad-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74dad-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="74dad-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="74dad-110">Der null basierte Index der Position, an der die Zeichenfolge eingefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="74dad-110">The zero-based index of the position at which to insert the string.</span></span> <span data-ttu-id="74dad-111">Wenn dieser Parameter-1 ist, wird die Zeichenfolge am Ende der Liste hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="74dad-111">If this parameter is -1, the string is added to the end of the list.</span></span>

</dd> <dt>

<span data-ttu-id="74dad-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="74dad-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="74dad-113">Ein Zeiger auf die mit NULL endende Zeichenfolge, die eingefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="74dad-113">A pointer to the null-terminated string to be inserted.</span></span> <span data-ttu-id="74dad-114">Wenn im Listenfeld ein vom Besitzer gezeichneter Stil, aber nicht der [**lbs \_ hasstrings**](list-box-styles.md) -Stil enthalten ist, wird dieser Parameter nicht als Zeichenfolge, sondern als Elementdaten gespeichert.</span><span class="sxs-lookup"><span data-stu-id="74dad-114">If the list box has an owner-drawn style but not the [**LBS\_HASSTRINGS**](list-box-styles.md) style, this parameter is stored as item data instead of a string.</span></span> <span data-ttu-id="74dad-115">Sie können die [**lb- \_ GetItemData**](lb-getitemdata.md) -und [**lb- \_ ltitemdata**](lb-setitemdata.md) -Nachrichten senden, um die Elementdaten abzurufen oder zu ändern.</span><span class="sxs-lookup"><span data-stu-id="74dad-115">You can send the [**LB\_GETITEMDATA**](lb-getitemdata.md) and [**LB\_SETITEMDATA**](lb-setitemdata.md) messages to retrieve or modify the item data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74dad-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="74dad-116">Return value</span></span>

<span data-ttu-id="74dad-117">Der Rückgabewert ist der Index der Position, an der die Zeichenfolge eingefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="74dad-117">The return value is the index of the position at which the string was inserted.</span></span> <span data-ttu-id="74dad-118">Wenn ein Fehler auftritt, ist der Rückgabewert lb \_ Err.</span><span class="sxs-lookup"><span data-stu-id="74dad-118">If an error occurs, the return value is LB\_ERR.</span></span> <span data-ttu-id="74dad-119">Wenn nicht genügend Speicherplatz vorhanden ist, um die neue Zeichenfolge zu speichern, ist der Rückgabewert "lb \_ errspace".</span><span class="sxs-lookup"><span data-stu-id="74dad-119">If there is insufficient space to store the new string, the return value is LB\_ERRSPACE.</span></span>

## <a name="remarks"></a><span data-ttu-id="74dad-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="74dad-120">Remarks</span></span>

<span data-ttu-id="74dad-121">Die " [**lb- \_ InitStorage**](lb-initstorage.md) "-Nachricht beschleunigt die Initialisierung von Listenfeldern, die über eine große Anzahl von Elementen (mehr als 100) verfügen.</span><span class="sxs-lookup"><span data-stu-id="74dad-121">The [**LB\_INITSTORAGE**](lb-initstorage.md) message helps speed up the initialization of list boxes that have a large number of items (more than 100).</span></span> <span data-ttu-id="74dad-122">Sie reserviert die angegebene Menge an Arbeitsspeicher, sodass nachfolgende **lb- \_ InsertString** -Nachrichten die kürzeste Zeit in Anspruch nehmen.</span><span class="sxs-lookup"><span data-stu-id="74dad-122">It reserves the specified amount of memory so that subsequent **LB\_INSERTSTRING** messages take the shortest possible time.</span></span> <span data-ttu-id="74dad-123">Sie können Schätzwerte für den *wParam* -Parameter und den *LPARAM* -Parameter verwenden.</span><span class="sxs-lookup"><span data-stu-id="74dad-123">You can use estimates for the *wParam* and *lParam* parameters.</span></span> <span data-ttu-id="74dad-124">Wenn Sie den Wert überschätzen, wird der zusätzliche Arbeitsspeicher zugeordnet. Wenn Sie unterschätzen, wird die normale Zuordnung für Elemente verwendet, die den angeforderten Betrag überschreiten.</span><span class="sxs-lookup"><span data-stu-id="74dad-124">If you overestimate, the extra memory is allocated; if you underestimate, the normal allocation is used for items that exceed the requested amount.</span></span>

<span data-ttu-id="74dad-125">Wenn das Listenfeld den [**WS- \_ HScroll**](/windows/desktop/winmsg/window-styles) -Stil aufweist und Sie eine Zeichenfolge als das Listenfeld einfügen, senden Sie eine [**lb- \_ lthorizontalblock**](lb-sethorizontalextent.md) -Nachricht, um sicherzustellen, dass die horizontale Bild Lauf Leiste angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="74dad-125">If the list box has [**WS\_HSCROLL**](/windows/desktop/winmsg/window-styles) style and you insert a string wider than the list box, send an [**LB\_SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) message to ensure the horizontal scroll bar appears.</span></span>

<span data-ttu-id="74dad-126">Für eine ANSI-Anwendung konvertiert das System den Text in einem Listenfeld mithilfe von CP ACP in Unicode \_ .</span><span class="sxs-lookup"><span data-stu-id="74dad-126">For an ANSI application, the system converts the text in a list box to Unicode using CP\_ACP.</span></span> <span data-ttu-id="74dad-127">Dies kann zu Problemen führen.</span><span class="sxs-lookup"><span data-stu-id="74dad-127">This can cause problems.</span></span> <span data-ttu-id="74dad-128">Beispielsweise werden Zeichen mit untergeordneten Zeichen in einem nicht-Unicode-Listenfeld in einem japanischen Fenster gegartet.</span><span class="sxs-lookup"><span data-stu-id="74dad-128">For example, accented Roman characters in a non-Unicode list box in Japanese Windows will come out garbled.</span></span> <span data-ttu-id="74dad-129">Um dieses Problem zu beheben, kompilieren Sie die Anwendung entweder als Unicode, oder verwenden Sie ein vom Besitzer gezeichnetes Listenfeld.</span><span class="sxs-lookup"><span data-stu-id="74dad-129">To fix this, either compile the application as Unicode or use an owner-drawn list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="74dad-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="74dad-130">Requirements</span></span>



| <span data-ttu-id="74dad-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="74dad-131">Requirement</span></span> | <span data-ttu-id="74dad-132">Wert</span><span class="sxs-lookup"><span data-stu-id="74dad-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74dad-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="74dad-133">Minimum supported client</span></span><br/> | <span data-ttu-id="74dad-134">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="74dad-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="74dad-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="74dad-135">Minimum supported server</span></span><br/> | <span data-ttu-id="74dad-136">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="74dad-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="74dad-137">Header</span><span class="sxs-lookup"><span data-stu-id="74dad-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="74dad-138"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="74dad-138"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74dad-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="74dad-139">See also</span></span>

<dl> <dt>

<span data-ttu-id="74dad-140">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="74dad-140">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="74dad-141">**LB- \_ AddString**</span><span class="sxs-lookup"><span data-stu-id="74dad-141">**LB\_ADDSTRING**</span></span>](lb-addstring.md)
</dt> <dt>

[<span data-ttu-id="74dad-142">**LB- \_ SelectString**</span><span class="sxs-lookup"><span data-stu-id="74dad-142">**LB\_SELECTSTRING**</span></span>](lb-selectstring.md)
</dt> <dt>

[<span data-ttu-id="74dad-143">**LB-Abbild \_ Umfang**</span><span class="sxs-lookup"><span data-stu-id="74dad-143">**LB\_SETHORIZONTALEXTENT**</span></span>](lb-sethorizontalextent.md)
</dt> </dl>

 

