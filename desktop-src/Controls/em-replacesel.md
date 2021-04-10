---
title: EM_REPLACESEL Meldung (Winuser. h)
description: Ersetzt den markierten Text in einem Bearbeitungs Steuerelement oder in einem Rich-Edit-Steuerelement durch den angegebenen Text.
ms.assetid: 525e6f5a-f52f-4bab-bc76-caa484729897
keywords:
- Windows-Steuerelemente für EM_REPLACESEL Meldung
topic_type:
- apiref
api_name:
- EM_REPLACESEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d9745b870a310626a6cbbbddbef118a63c64479
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106269"
---
# <a name="em_replacesel-message"></a><span data-ttu-id="b75ba-104">EM \_ replacesel-Nachricht</span><span class="sxs-lookup"><span data-stu-id="b75ba-104">EM\_REPLACESEL message</span></span>

<span data-ttu-id="b75ba-105">Ersetzt den markierten Text in einem Bearbeitungs Steuerelement oder in einem Rich-Edit-Steuerelement durch den angegebenen Text.</span><span class="sxs-lookup"><span data-stu-id="b75ba-105">Replaces the selected text in an edit control or a rich edit control with the specified text.</span></span>

## <a name="parameters"></a><span data-ttu-id="b75ba-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b75ba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b75ba-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b75ba-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b75ba-108">Gibt an, ob der Ersetzungs Vorgang rückgängig gemacht werden kann.</span><span class="sxs-lookup"><span data-stu-id="b75ba-108">Specifies whether the replacement operation can be undone.</span></span> <span data-ttu-id="b75ba-109">Wenn dies **zutrifft**, kann der Vorgang rückgängig gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="b75ba-109">If this is **TRUE**, the operation can be undone.</span></span> <span data-ttu-id="b75ba-110">Wenn dies **false** ist, kann der Vorgang nicht rückgängig gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="b75ba-110">If this is **FALSE** , the operation cannot be undone.</span></span>

</dd> <dt>

<span data-ttu-id="b75ba-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b75ba-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b75ba-112">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Ersetzungstext enthält.</span><span class="sxs-lookup"><span data-stu-id="b75ba-112">A pointer to a null-terminated string containing the replacement text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b75ba-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b75ba-113">Return value</span></span>

<span data-ttu-id="b75ba-114">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b75ba-114">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b75ba-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b75ba-115">Remarks</span></span>

<span data-ttu-id="b75ba-116">Verwenden Sie die **EM \_ replacesel** -Nachricht, um nur einen Teil des Texts in einem Bearbeitungs Steuerelement zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="b75ba-116">Use the **EM\_REPLACESEL** message to replace only a portion of the text in an edit control.</span></span> <span data-ttu-id="b75ba-117">Um den gesamten Text zu ersetzen, verwenden Sie die [**WM- \_ SetText**](/windows/desktop/winmsg/wm-settext) -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="b75ba-117">To replace all of the text, use the [**WM\_SETTEXT**](/windows/desktop/winmsg/wm-settext) message.</span></span>

<span data-ttu-id="b75ba-118">Wenn keine Auswahl vorhanden ist, wird der Ersetzungstext an der Einfügemarke eingefügt.</span><span class="sxs-lookup"><span data-stu-id="b75ba-118">If there is no selection, the replacement text is inserted at the caret.</span></span>

<span data-ttu-id="b75ba-119">Umfassende **Bearbeitung:** Wird in Microsoft Rich Edit 1,0 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b75ba-119">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="b75ba-120">Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="b75ba-120">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

<span data-ttu-id="b75ba-121">In einem Rich-Edit-Steuerelement übernimmt der Ersetzungstext die Formatierung des Zeichens bei der Einfügemarke oder, wenn eine Auswahl vorliegt, das erste Zeichen in der Auswahl.</span><span class="sxs-lookup"><span data-stu-id="b75ba-121">In a rich edit control, the replacement text takes the formatting of the character at the caret or, if there is a selection, of the first character in the selection.</span></span>

## <a name="requirements"></a><span data-ttu-id="b75ba-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b75ba-122">Requirements</span></span>



| <span data-ttu-id="b75ba-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b75ba-123">Requirement</span></span> | <span data-ttu-id="b75ba-124">Wert</span><span class="sxs-lookup"><span data-stu-id="b75ba-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b75ba-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b75ba-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b75ba-126">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b75ba-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b75ba-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b75ba-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b75ba-128">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b75ba-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b75ba-129">Header</span><span class="sxs-lookup"><span data-stu-id="b75ba-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="b75ba-130"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="b75ba-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b75ba-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b75ba-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b75ba-132">**WM- \_ SetText**</span><span class="sxs-lookup"><span data-stu-id="b75ba-132">**WM\_SETTEXT**</span></span>](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 

