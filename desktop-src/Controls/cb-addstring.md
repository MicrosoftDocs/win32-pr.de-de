---
title: CB_ADDSTRING Meldung (Winuser. h)
description: Fügt eine Zeichenfolge in das Listenfeld eines Kombinations Felds ein. Wenn das Kombinations Feld nicht den CBS- \_ Sortier Stil hat, wird die Zeichenfolge am Ende der Liste hinzugefügt. Andernfalls wird die Zeichenfolge in die Liste eingefügt, und die Liste wird sortiert.
ms.assetid: 201bcb7b-e7d1-41e6-8eb7-a5864b659a52
keywords:
- Windows-Steuerelemente für CB_ADDSTRING Meldung
topic_type:
- apiref
api_name:
- CB_ADDSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dda16367ec24e869f6cb664e89751d7a13efec3c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957009"
---
# <a name="cb_addstring-message"></a><span data-ttu-id="f18f3-106">CB- \_ AddString-Nachricht</span><span class="sxs-lookup"><span data-stu-id="f18f3-106">CB\_ADDSTRING message</span></span>

<span data-ttu-id="f18f3-107">Fügt eine Zeichenfolge in das Listenfeld eines Kombinations Felds ein.</span><span class="sxs-lookup"><span data-stu-id="f18f3-107">Adds a string to the list box of a combo box.</span></span> <span data-ttu-id="f18f3-108">Wenn das Kombinations Feld nicht den CBS- [**\_ Sortier**](combo-box-styles.md) Stil hat, wird die Zeichenfolge am Ende der Liste hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="f18f3-108">If the combo box does not have the [**CBS\_SORT**](combo-box-styles.md) style, the string is added to the end of the list.</span></span> <span data-ttu-id="f18f3-109">Andernfalls wird die Zeichenfolge in die Liste eingefügt, und die Liste wird sortiert.</span><span class="sxs-lookup"><span data-stu-id="f18f3-109">Otherwise, the string is inserted into the list, and the list is sorted.</span></span>

## <a name="parameters"></a><span data-ttu-id="f18f3-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f18f3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f18f3-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f18f3-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f18f3-112">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="f18f3-112">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f18f3-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f18f3-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f18f3-114">Ein **LPCTSTR** -Zeiger auf die NULL-terminierte Zeichenfolge, die hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f18f3-114">An **LPCTSTR** pointer to the null-terminated string to be added.</span></span> <span data-ttu-id="f18f3-115">Wenn Sie das Kombinations Feld mit einem vom Besitzer gezeichneten Stil, aber ohne den [**CBS \_ hasstrings**](combo-box-styles.md) -Stil erstellen, wird der Wert des *LPARAM* -Parameters als Elementdaten gespeichert und nicht als die Zeichenfolge, auf die er andernfalls verweisen würde.</span><span class="sxs-lookup"><span data-stu-id="f18f3-115">If you create the combo box with an owner-drawn style but without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, the value of the *lParam* parameter is stored as item data rather than the string it would otherwise point to.</span></span> <span data-ttu-id="f18f3-116">Die Elementdaten können abgerufen oder geändert werden, indem die [**CB \_ GetItemData**](cb-getitemdata.md) - [**oder \_ CB**](cb-setitemdata.md) .</span><span class="sxs-lookup"><span data-stu-id="f18f3-116">The item data can be retrieved or modified by sending the [**CB\_GETITEMDATA**](cb-getitemdata.md) or [**CB\_SETITEMDATA**](cb-setitemdata.md) message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f18f3-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f18f3-117">Return value</span></span>

<span data-ttu-id="f18f3-118">Der Rückgabewert ist der null basierte Index der Zeichenfolge im Listenfeld des Kombinations Felds.</span><span class="sxs-lookup"><span data-stu-id="f18f3-118">The return value is the zero-based index to the string in the list box of the combo box.</span></span> <span data-ttu-id="f18f3-119">Wenn ein Fehler auftritt, ist der Rückgabewert CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="f18f3-119">If an error occurs, the return value is CB\_ERR.</span></span> <span data-ttu-id="f18f3-120">Wenn nicht genügend Speicherplatz zum Speichern der neuen Zeichenfolge verfügbar ist, ist dies CB \_ errspace.</span><span class="sxs-lookup"><span data-stu-id="f18f3-120">If insufficient space is available to store the new string, it is CB\_ERRSPACE.</span></span>

## <a name="remarks"></a><span data-ttu-id="f18f3-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f18f3-121">Remarks</span></span>

<span data-ttu-id="f18f3-122">Wenn Sie ein vom Besitzer gezeichnetes Kombinations Feld mit dem [**CBS- \_ Sortier**](combo-box-styles.md) Stil, aber ohne den [**CBS \_ hasstrings**](combo-box-styles.md) -Stil erstellen, wird die [**WM \_ compareitem**](wm-compareitem.md) -Nachricht einmal oder mehrmals an den Besitzer des Kombinations Felds gesendet, damit das neue Element ordnungsgemäß in die Liste eingefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="f18f3-122">If you create an owner-drawn combo box with the [**CBS\_SORT**](combo-box-styles.md) style but without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, the [**WM\_COMPAREITEM**](wm-compareitem.md) message is sent one or more times to the owner of the combo box so the new item can be properly placed in the list.</span></span>

<span data-ttu-id="f18f3-123">Um eine Zeichenfolge an einer bestimmten Position in der Liste einzufügen, verwenden Sie die [**CB \_ InsertString**](cb-insertstring.md) -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="f18f3-123">To insert a string at a specific location within the list, use the [**CB\_INSERTSTRING**](cb-insertstring.md) message.</span></span>

<span data-ttu-id="f18f3-124">Wenn das Kombinations Feld über den [**WS- \_ HScroll**](/windows/desktop/winmsg/window-styles) -Stil verfügt und Sie eine Zeichenfolge hinzufügen, die größer als das Kombinations Feld ist, senden Sie eine [**lb- \_ sethorizontalblock**](lb-sethorizontalextent.md) -Nachricht, um sicherzustellen, dass die horizontale</span><span class="sxs-lookup"><span data-stu-id="f18f3-124">If the combo box has [**WS\_HSCROLL**](/windows/desktop/winmsg/window-styles) style and you add a string wider than the combo box, send a [**LB\_SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) message to ensure the horizontal scroll bar appears.</span></span>

<span data-ttu-id="f18f3-125">**Comclt32.dll Version 5,0 oder höher:** Wenn " [**CBS \_ lowercase**](combo-box-styles.md) " oder " [**CBS \_ UpperCase**](combo-box-styles.md) " festgelegt ist, ändert die Unicode-Version von **CB \_ AddString** die Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="f18f3-125">**Comclt32.dll version 5.0 or later:** If [**CBS\_LOWERCASE**](combo-box-styles.md) or [**CBS\_UPPERCASE**](combo-box-styles.md) is set, the Unicode version of **CB\_ADDSTRING** alters the string.</span></span> <span data-ttu-id="f18f3-126">Bei Verwendung des schreibgeschützten globalen Speichers bewirkt dies, dass die Anwendung fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="f18f3-126">If using read-only global memory, this causes the application to fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="f18f3-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f18f3-127">Requirements</span></span>



| <span data-ttu-id="f18f3-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f18f3-128">Requirement</span></span> | <span data-ttu-id="f18f3-129">Wert</span><span class="sxs-lookup"><span data-stu-id="f18f3-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f18f3-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f18f3-130">Minimum supported client</span></span><br/> | <span data-ttu-id="f18f3-131">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f18f3-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f18f3-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f18f3-132">Minimum supported server</span></span><br/> | <span data-ttu-id="f18f3-133">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f18f3-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f18f3-134">Header</span><span class="sxs-lookup"><span data-stu-id="f18f3-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="f18f3-135"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="f18f3-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f18f3-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f18f3-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="f18f3-137">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="f18f3-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f18f3-138">**CB- \_ dir**</span><span class="sxs-lookup"><span data-stu-id="f18f3-138">**CB\_DIR**</span></span>](cb-dir.md)
</dt> <dt>

[<span data-ttu-id="f18f3-139">**CB \_ InsertString**</span><span class="sxs-lookup"><span data-stu-id="f18f3-139">**CB\_INSERTSTRING**</span></span>](cb-insertstring.md)
</dt> <dt>

[<span data-ttu-id="f18f3-140">**LB-Abbild \_ Umfang**</span><span class="sxs-lookup"><span data-stu-id="f18f3-140">**LB\_SETHORIZONTALEXTENT**</span></span>](lb-sethorizontalextent.md)
</dt> <dt>

[<span data-ttu-id="f18f3-141">**WM- \_ compareitem**</span><span class="sxs-lookup"><span data-stu-id="f18f3-141">**WM\_COMPAREITEM**</span></span>](wm-compareitem.md)
</dt> </dl>

 

