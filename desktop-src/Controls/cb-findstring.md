---
title: CB_FINDSTRING Meldung (Winuser. h)
description: Durchsucht das Listenfeld eines Kombinations Felds nach einem Element, beginnend mit den Zeichen in einer angegebenen Zeichenfolge.
ms.assetid: 872a72d5-4d8e-41c7-ac6b-eeb571403623
keywords:
- Windows-Steuerelemente für CB_FINDSTRING Meldung
topic_type:
- apiref
api_name:
- CB_FINDSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 295300790a27a956bce953e4e293c07c22ec0d81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103631"
---
# <a name="cb_findstring-message"></a><span data-ttu-id="306e7-104">CB- \_ FindString-Nachricht</span><span class="sxs-lookup"><span data-stu-id="306e7-104">CB\_FINDSTRING message</span></span>

<span data-ttu-id="306e7-105">Durchsucht das Listenfeld eines Kombinations Felds nach einem Element, beginnend mit den Zeichen in einer angegebenen Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="306e7-105">Searches the list box of a combo box for an item beginning with the characters in a specified string.</span></span>

## <a name="parameters"></a><span data-ttu-id="306e7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="306e7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="306e7-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="306e7-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="306e7-108">Der null basierte Index des Elements vor dem ersten zu durchsuchenden Element.</span><span class="sxs-lookup"><span data-stu-id="306e7-108">The zero-based index of the item preceding the first item to be searched.</span></span> <span data-ttu-id="306e7-109">Wenn die Suche das Ende des Listen Felds erreicht, wird Sie von der obersten Position des Listen Felds zurück zu dem durch den *wParam* -Parameter angegebenen Element weiter angezeigt.</span><span class="sxs-lookup"><span data-stu-id="306e7-109">When the search reaches the bottom of the list box, it continues from the top of the list box back to the item specified by the *wParam* parameter.</span></span> <span data-ttu-id="306e7-110">Wenn *wParam* den Wert-1 hat, wird das gesamte Listenfeld von Anfang an durchsucht.</span><span class="sxs-lookup"><span data-stu-id="306e7-110">If *wParam* is  -1, the entire list box is searched from the beginning.</span></span>

</dd> <dt>

<span data-ttu-id="306e7-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="306e7-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="306e7-112">Ein Zeiger auf die NULL-terminierte Zeichenfolge, die die zu durchsuchenden Zeichen enthält.</span><span class="sxs-lookup"><span data-stu-id="306e7-112">A pointer to the null-terminated string that contains the characters for which to search.</span></span> <span data-ttu-id="306e7-113">Bei der Suche wird die Groß-/Kleinschreibung nicht beachtet, sodass diese Zeichenfolge eine beliebige Kombination von Groß-und Kleinbuchstaben enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="306e7-113">The search is not case sensitive, so this string can contain any combination of uppercase and lowercase letters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="306e7-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="306e7-114">Return value</span></span>

<span data-ttu-id="306e7-115">Der Rückgabewert ist der null basierte Index des übereinstimmenden Elements.</span><span class="sxs-lookup"><span data-stu-id="306e7-115">The return value is the zero-based index of the matching item.</span></span> <span data-ttu-id="306e7-116">Wenn die Suche nicht erfolgreich ist, ist Sie CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="306e7-116">If the search is unsuccessful, it is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="306e7-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="306e7-117">Remarks</span></span>

<span data-ttu-id="306e7-118">Wenn Sie das Kombinations Feld mit einem vom Besitzer gezeichneten Stil, aber ohne den [**CBS \_ hasstrings**](combo-box-styles.md) -Stil erstellen, hängt die **CB- \_ FindString** -Nachricht davon ab, ob die Anwendung den CBS- [**\_ Sortier**](combo-box-styles.md) Stil verwendet.</span><span class="sxs-lookup"><span data-stu-id="306e7-118">If you create the combo box with an owner-drawn style but without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, what the **CB\_FINDSTRING** message does depends on whether your application uses the [**CBS\_SORT**](combo-box-styles.md) style.</span></span> <span data-ttu-id="306e7-119">Bei Verwendung des **CBS- \_ Sortier** Stils werden [**WM \_ compareitem**](wm-compareitem.md) -Nachrichten an den Besitzer des Kombinations Felds gesendet, um zu bestimmen, welches Element mit der angegebenen Zeichenfolge übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="306e7-119">If you use the **CBS\_SORT** style, [**WM\_COMPAREITEM**](wm-compareitem.md) messages are sent to the owner of the combo box to determine which item matches the specified string.</span></span> <span data-ttu-id="306e7-120">Wenn Sie den **Sortierungstyp \_ CBS** nicht verwenden, sucht die **CB- \_ FindString** -Nachricht nach einem Listenelement, das mit dem Wert des *LPARAM* -Parameters übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="306e7-120">If you do not use the **CBS\_SORT** style, the **CB\_FINDSTRING** message searches for a list item that matches the value of the *lParam* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="306e7-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="306e7-121">Requirements</span></span>



| <span data-ttu-id="306e7-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="306e7-122">Requirement</span></span> | <span data-ttu-id="306e7-123">Wert</span><span class="sxs-lookup"><span data-stu-id="306e7-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="306e7-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="306e7-124">Minimum supported client</span></span><br/> | <span data-ttu-id="306e7-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="306e7-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="306e7-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="306e7-126">Minimum supported server</span></span><br/> | <span data-ttu-id="306e7-127">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="306e7-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="306e7-128">Header</span><span class="sxs-lookup"><span data-stu-id="306e7-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="306e7-129"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="306e7-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="306e7-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="306e7-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="306e7-131">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="306e7-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="306e7-132">**CB- \_ FindStringExact**</span><span class="sxs-lookup"><span data-stu-id="306e7-132">**CB\_FINDSTRINGEXACT**</span></span>](cb-findstringexact.md)
</dt> <dt>

[<span data-ttu-id="306e7-133">**CB- \_ SelectString**</span><span class="sxs-lookup"><span data-stu-id="306e7-133">**CB\_SELECTSTRING**</span></span>](cb-selectstring.md)
</dt> <dt>

[<span data-ttu-id="306e7-134">**CB \_ setcurrsel**</span><span class="sxs-lookup"><span data-stu-id="306e7-134">**CB\_SETCURSEL**</span></span>](cb-setcursel.md)
</dt> <dt>

[<span data-ttu-id="306e7-135">**WM- \_ compareitem**</span><span class="sxs-lookup"><span data-stu-id="306e7-135">**WM\_COMPAREITEM**</span></span>](wm-compareitem.md)
</dt> </dl>

 

 





