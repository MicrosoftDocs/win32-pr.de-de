---
title: CB_SELECTSTRING Meldung (Winuser. h)
description: Durchsucht die Liste eines Kombinations Felds nach einem Element, das mit den Zeichen in einer angegebenen Zeichenfolge beginnt. Wenn ein übereinstimmendes Element gefunden wird, wird es ausgewählt und in das Bearbeitungs Steuerelement kopiert.
ms.assetid: c08dff72-7e44-40ed-8b64-513359292829
keywords:
- Windows-Steuerelemente für CB_SELECTSTRING Meldung
topic_type:
- apiref
api_name:
- CB_SELECTSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2913b95c02cdfd3c7a9c96a8652038a04d8fde8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040593"
---
# <a name="cb_selectstring-message"></a><span data-ttu-id="859c9-105">CB- \_ SelectString-Nachricht</span><span class="sxs-lookup"><span data-stu-id="859c9-105">CB\_SELECTSTRING message</span></span>

<span data-ttu-id="859c9-106">Durchsucht die Liste eines Kombinations Felds nach einem Element, das mit den Zeichen in einer angegebenen Zeichenfolge beginnt.</span><span class="sxs-lookup"><span data-stu-id="859c9-106">Searches the list of a combo box for an item that begins with the characters in a specified string.</span></span> <span data-ttu-id="859c9-107">Wenn ein übereinstimmendes Element gefunden wird, wird es ausgewählt und in das Bearbeitungs Steuerelement kopiert.</span><span class="sxs-lookup"><span data-stu-id="859c9-107">If a matching item is found, it is selected and copied to the edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="859c9-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="859c9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="859c9-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="859c9-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="859c9-110">Der null basierte Index des Elements vor dem ersten zu durchsuchenden Element.</span><span class="sxs-lookup"><span data-stu-id="859c9-110">The zero-based index of the item preceding the first item to be searched.</span></span> <span data-ttu-id="859c9-111">Wenn die Suche das Ende der Liste erreicht, wird Sie von der Spitze der Liste zurück zu dem durch den *wParam* -Parameter angegebenen Element weiter angezeigt.</span><span class="sxs-lookup"><span data-stu-id="859c9-111">When the search reaches the bottom of the list, it continues from the top of the list back to the item specified by the *wParam* parameter.</span></span> <span data-ttu-id="859c9-112">Wenn *wParam* den Wert-1 hat, wird die gesamte Liste von Anfang an durchsucht.</span><span class="sxs-lookup"><span data-stu-id="859c9-112">If *wParam* is -1, the entire list is searched from the beginning.</span></span>

</dd> <dt>

<span data-ttu-id="859c9-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="859c9-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="859c9-114">Ein Zeiger auf die NULL-terminierte Zeichenfolge, die die zu durchsuchenden Zeichen enthält.</span><span class="sxs-lookup"><span data-stu-id="859c9-114">A pointer to the null-terminated string that contains the characters for which to search.</span></span> <span data-ttu-id="859c9-115">Bei der Suche wird die Groß-/Kleinschreibung nicht beachtet, sodass diese Zeichenfolge eine beliebige Kombination von Groß-und Kleinbuchstaben enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="859c9-115">The search is not case sensitive, so this string can contain any combination of uppercase and lowercase letters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="859c9-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="859c9-116">Return value</span></span>

<span data-ttu-id="859c9-117">Wenn die Zeichenfolge gefunden wird, ist der Rückgabewert der Index des ausgewählten Elements.</span><span class="sxs-lookup"><span data-stu-id="859c9-117">If the string is found, the return value is the index of the selected item.</span></span> <span data-ttu-id="859c9-118">Wenn die Suche nicht erfolgreich ist, ist der Rückgabewert CB \_ Err, und die aktuelle Auswahl wird nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="859c9-118">If the search is unsuccessful, the return value is CB\_ERR and the current selection is not changed.</span></span>

## <a name="remarks"></a><span data-ttu-id="859c9-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="859c9-119">Remarks</span></span>

<span data-ttu-id="859c9-120">Eine Zeichenfolge wird nur ausgewählt, wenn die Zeichen vom Startpunkt den Zeichen in der Präfix Zeichenfolge entsprechen.</span><span class="sxs-lookup"><span data-stu-id="859c9-120">A string is selected only if the characters from the starting point match the characters in the prefix string.</span></span>

<span data-ttu-id="859c9-121">Wenn Sie das Kombinations Feld mit einem vom Besitzer gezeichneten Stil, aber ohne den [**CBS \_ hasstrings**](combo-box-styles.md) -Stil erstellen, hängt die **CB- \_ SelectString** -Nachricht davon ab, ob Sie das CBS- [**\_ Sortier**](combo-box-styles.md) Format verwenden.</span><span class="sxs-lookup"><span data-stu-id="859c9-121">If you create the combo box with an owner-drawn style but without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, what the **CB\_SELECTSTRING** message does depends on whether you use the [**CBS\_SORT**](combo-box-styles.md) style.</span></span> <span data-ttu-id="859c9-122">Wenn der **CBS- \_ Sortier** Stil verwendet wird, sendet das System [**WM \_ compareitem**](wm-compareitem.md) -Nachrichten an den Besitzer des Kombinations Felds, um zu bestimmen, welches Element mit der angegebenen Zeichenfolge übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="859c9-122">If the **CBS\_SORT** style is used, the system sends [**WM\_COMPAREITEM**](wm-compareitem.md) messages to the owner of the combo box to determine which item matches the specified string.</span></span> <span data-ttu-id="859c9-123">Wenn Sie den **sortierungstil \_ CBS** nicht verwenden, versucht **CB \_ SelectString** , den **DWORD** -Wert mit dem Wert des *LPARAM* -Parameters abzugleichen.</span><span class="sxs-lookup"><span data-stu-id="859c9-123">If you do not use the **CBS\_SORT** style, **CB\_SELECTSTRING** attempts to match the **DWORD** value against the value of the *lParam* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="859c9-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="859c9-124">Requirements</span></span>



| <span data-ttu-id="859c9-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="859c9-125">Requirement</span></span> | <span data-ttu-id="859c9-126">Wert</span><span class="sxs-lookup"><span data-stu-id="859c9-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="859c9-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="859c9-127">Minimum supported client</span></span><br/> | <span data-ttu-id="859c9-128">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="859c9-128">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="859c9-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="859c9-129">Minimum supported server</span></span><br/> | <span data-ttu-id="859c9-130">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="859c9-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="859c9-131">Header</span><span class="sxs-lookup"><span data-stu-id="859c9-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="859c9-132"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="859c9-132"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="859c9-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="859c9-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="859c9-134">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="859c9-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="859c9-135">**CB- \_ FindString**</span><span class="sxs-lookup"><span data-stu-id="859c9-135">**CB\_FINDSTRING**</span></span>](cb-findstring.md)
</dt> <dt>

[<span data-ttu-id="859c9-136">**CB- \_ FindStringExact**</span><span class="sxs-lookup"><span data-stu-id="859c9-136">**CB\_FINDSTRINGEXACT**</span></span>](cb-findstringexact.md)
</dt> <dt>

[<span data-ttu-id="859c9-137">**CB \_ setcurrsel**</span><span class="sxs-lookup"><span data-stu-id="859c9-137">**CB\_SETCURSEL**</span></span>](cb-setcursel.md)
</dt> <dt>

[<span data-ttu-id="859c9-138">**WM- \_ compareitem**</span><span class="sxs-lookup"><span data-stu-id="859c9-138">**WM\_COMPAREITEM**</span></span>](wm-compareitem.md)
</dt> </dl>

 

 





