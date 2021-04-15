---
title: CB_INSERTSTRING Meldung (Winuser. h)
description: Fügt eine Zeichenfolge oder Elementdaten in die Liste eines Kombinations Felds ein. Im Gegensatz zur CB \_ AddString-Nachricht bewirkt die CB \_ InsertString-Nachricht nicht, dass eine Liste mit dem CBS- \_ Sortier Stil sortiert wird.
ms.assetid: b9067b4e-afca-4c78-9ca2-c717b99c7459
keywords:
- Windows-Steuerelemente für CB_INSERTSTRING Meldung
topic_type:
- apiref
api_name:
- CB_INSERTSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14d050980137bc34652cb2fce39b9f188f4d5cd6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476650"
---
# <a name="cb_insertstring-message"></a><span data-ttu-id="99408-105">CB \_ InsertString-Nachricht</span><span class="sxs-lookup"><span data-stu-id="99408-105">CB\_INSERTSTRING message</span></span>

<span data-ttu-id="99408-106">Fügt eine Zeichenfolge oder Elementdaten in die Liste eines Kombinations Felds ein.</span><span class="sxs-lookup"><span data-stu-id="99408-106">Inserts a string or item data into the list of a combo box.</span></span> <span data-ttu-id="99408-107">Im Gegensatz zur [**CB \_ AddString**](cb-addstring.md) -Nachricht bewirkt die **CB \_ InsertString** -Nachricht nicht, dass eine Liste mit dem [**CBS- \_ Sortier**](combo-box-styles.md) Stil sortiert wird.</span><span class="sxs-lookup"><span data-stu-id="99408-107">Unlike the [**CB\_ADDSTRING**](cb-addstring.md) message, the **CB\_INSERTSTRING** message does not cause a list with the [**CBS\_SORT**](combo-box-styles.md) style to be sorted.</span></span>

## <a name="parameters"></a><span data-ttu-id="99408-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="99408-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99408-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="99408-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="99408-110">Der null basierte Index der Position, an der die Zeichenfolge eingefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="99408-110">The zero-based index of the position at which to insert the string.</span></span> <span data-ttu-id="99408-111">Wenn dieser Parameter-1 ist, wird die Zeichenfolge am Ende der Liste hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="99408-111">If this parameter is -1, the string is added to the end of the list.</span></span>

</dd> <dt>

<span data-ttu-id="99408-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="99408-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="99408-113">Ein Zeiger auf die mit NULL endende Zeichenfolge, die eingefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="99408-113">A pointer to the null-terminated string to be inserted.</span></span> <span data-ttu-id="99408-114">Wenn Sie das Kombinations Feld mit einem vom Besitzer gezeichneten Stil, aber ohne den [**CBS \_ hasstrings**](combo-box-styles.md) -Stil erstellen, wird der Wert des *LPARAM* -Parameters anstelle der Zeichenfolge gespeichert, auf die er andernfalls verweisen würde.</span><span class="sxs-lookup"><span data-stu-id="99408-114">If you create the combo box with an owner-drawn style but without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, the value of the *lParam* parameter is stored rather than the string to which it would otherwise point.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99408-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="99408-115">Return value</span></span>

<span data-ttu-id="99408-116">Der Rückgabewert ist der Index der Position, an der die Zeichenfolge eingefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="99408-116">The return value is the index of the position at which the string was inserted.</span></span> <span data-ttu-id="99408-117">Wenn ein Fehler auftritt, ist der Rückgabewert CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="99408-117">If an error occurs, the return value is CB\_ERR.</span></span> <span data-ttu-id="99408-118">Wenn nicht genügend Speicherplatz vorhanden ist, um die neue Zeichenfolge zu speichern, ist dies CB \_ errspace.</span><span class="sxs-lookup"><span data-stu-id="99408-118">If there is insufficient space available to store the new string, it is CB\_ERRSPACE.</span></span>

<span data-ttu-id="99408-119">Wenn das Kombinations Feld den [**WS- \_ HScroll**](/windows/desktop/winmsg/window-styles) -Stil aufweist und Sie eine Zeichenfolge einfügen, die breiter als das Kombinations Feld ist, sollten Sie eine [**lb- \_ sethorizontalblock**](lb-sethorizontalextent.md) -Nachricht senden, um sicherzustellen, dass die horizontale Bild Lauf Leiste</span><span class="sxs-lookup"><span data-stu-id="99408-119">If the combo box has [**WS\_HSCROLL**](/windows/desktop/winmsg/window-styles) style and you insert a string wider than the combo box, you should send a [**LB\_SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) message to ensure the horizontal scroll bar appears.</span></span>

## <a name="requirements"></a><span data-ttu-id="99408-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="99408-120">Requirements</span></span>



| <span data-ttu-id="99408-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="99408-121">Requirement</span></span> | <span data-ttu-id="99408-122">Wert</span><span class="sxs-lookup"><span data-stu-id="99408-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99408-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="99408-123">Minimum supported client</span></span><br/> | <span data-ttu-id="99408-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="99408-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="99408-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="99408-125">Minimum supported server</span></span><br/> | <span data-ttu-id="99408-126">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="99408-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="99408-127">Header</span><span class="sxs-lookup"><span data-stu-id="99408-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="99408-128"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="99408-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99408-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="99408-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="99408-130">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="99408-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="99408-131">**CB \_ AddString**</span><span class="sxs-lookup"><span data-stu-id="99408-131">**CB\_ADDSTRING**</span></span>](cb-addstring.md)
</dt> <dt>

[<span data-ttu-id="99408-132">**LB-Abbild \_ Umfang**</span><span class="sxs-lookup"><span data-stu-id="99408-132">**LB\_SETHORIZONTALEXTENT**</span></span>](lb-sethorizontalextent.md)
</dt> <dt>

[<span data-ttu-id="99408-133">**CB- \_ dir**</span><span class="sxs-lookup"><span data-stu-id="99408-133">**CB\_DIR**</span></span>](cb-dir.md)
</dt> </dl>

 

