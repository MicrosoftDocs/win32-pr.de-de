---
title: CB_FINDSTRINGEXACT Meldung (Winuser. h)
description: Sucht die erste Listenfeld Zeichenfolge in einem Kombinations Feld, das mit der im lParam-Parameter angegebenen Zeichenfolge übereinstimmt.
ms.assetid: 9065af9f-b18e-4fd5-a8cc-f780f8d0fb05
keywords:
- Windows-Steuerelemente für CB_FINDSTRINGEXACT Meldung
topic_type:
- apiref
api_name:
- CB_FINDSTRINGEXACT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f70c56a5f13fffa8dfedebd13f9830c62ef941cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519343"
---
# <a name="cb_findstringexact-message"></a><span data-ttu-id="0cebb-104">CB- \_ FindStringExact-Nachricht</span><span class="sxs-lookup"><span data-stu-id="0cebb-104">CB\_FINDSTRINGEXACT message</span></span>

<span data-ttu-id="0cebb-105">Sucht die erste Listenfeld Zeichenfolge in einem Kombinations Feld, das mit der im *LPARAM* -Parameter angegebenen Zeichenfolge übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="0cebb-105">Finds the first list box string in a combo box that matches the string specified in the *lParam* parameter.</span></span>

## <a name="parameters"></a><span data-ttu-id="0cebb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0cebb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0cebb-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0cebb-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0cebb-108">Der null basierte Index des Elements vor dem ersten zu durchsuchenden Element.</span><span class="sxs-lookup"><span data-stu-id="0cebb-108">The zero-based index of the item preceding the first item to be searched.</span></span> <span data-ttu-id="0cebb-109">Wenn die Suche das Ende des Listen Felds erreicht, wird Sie von der obersten Position des Listen Felds zurück zu dem durch den *wParam* -Parameter angegebenen Element weiter angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0cebb-109">When the search reaches the bottom of the list box, it continues from the top of the list box back to the item specified by the *wParam* parameter.</span></span> <span data-ttu-id="0cebb-110">Wenn *wParam* den Wert 1 hat, wird das gesamte Listenfeld von Anfang an durchsucht.</span><span class="sxs-lookup"><span data-stu-id="0cebb-110">If *wParam* is  1, the entire list box is searched from the beginning.</span></span>

</dd> <dt>

<span data-ttu-id="0cebb-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0cebb-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0cebb-112">Ein Zeiger auf die NULL-terminierte Zeichenfolge, nach der gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="0cebb-112">A pointer to the null-terminated string for which to search.</span></span> <span data-ttu-id="0cebb-113">Bei der Suche wird die Groß-/Kleinschreibung nicht beachtet, sodass diese Zeichenfolge eine beliebige Kombination von Groß-und Kleinbuchstaben enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="0cebb-113">The search is not case sensitive, so this string can contain any combination of uppercase and lowercase letters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0cebb-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0cebb-114">Return value</span></span>

<span data-ttu-id="0cebb-115">Der Rückgabewert ist der null basierte Index des übereinstimmenden Elements.</span><span class="sxs-lookup"><span data-stu-id="0cebb-115">The return value is the zero-based index of the matching item.</span></span> <span data-ttu-id="0cebb-116">Wenn die Suche nicht erfolgreich ist, ist Sie CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="0cebb-116">If the search is unsuccessful, it is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="0cebb-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0cebb-117">Remarks</span></span>

<span data-ttu-id="0cebb-118">Diese Funktion ist nur erfolgreich, wenn die angegebene Zeichenfolge und ein Kombinations Feld Element dieselbe Länge (außer dem abschließenden NULL-Zeichen) und denselben Zeichen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="0cebb-118">This function is successful only if the specified string and a combo box item have the same length (except for the terminating null character) and the same characters.</span></span>

<span data-ttu-id="0cebb-119">Wenn Sie das Kombinations Feld mit einem vom Besitzer gezeichneten Stil, aber ohne den [**CBS \_ hasstrings**](combo-box-styles.md) -Stil erstellen, hängt die Funktion der **CB- \_ FindStringExact** -Nachricht davon ab, ob die Anwendung den [**CBS- \_ Sortier**](combo-box-styles.md) Stil verwendet.</span><span class="sxs-lookup"><span data-stu-id="0cebb-119">If you create the combo box with an owner-drawn style but without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, the functionality of **CB\_FINDSTRINGEXACT** message depends on whether your application uses the [**CBS\_SORT**](combo-box-styles.md) style.</span></span> <span data-ttu-id="0cebb-120">Bei Verwendung des **CBS- \_ Sortier** Stils werden [**WM \_ compareitem**](wm-compareitem.md) -Nachrichten an den Besitzer des Kombinations Felds gesendet, um zu bestimmen, welches Element mit der angegebenen Zeichenfolge übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="0cebb-120">If you use the **CBS\_SORT** style, [**WM\_COMPAREITEM**](wm-compareitem.md) messages are sent to the owner of the combo box to determine which item matches the specified string.</span></span> <span data-ttu-id="0cebb-121">Wenn Sie den **Sortierungstyp \_ CBS** nicht verwenden, sucht die **CB \_ FindStringExact** -Nachricht nach einem Listenelement, das mit dem Wert des *LPARAM* -Parameters übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="0cebb-121">If you do not use the **CBS\_SORT** style, the **CB\_FINDSTRINGEXACT** message searches for a list item that matches the value of the *lParam* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="0cebb-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0cebb-122">Requirements</span></span>



| <span data-ttu-id="0cebb-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0cebb-123">Requirement</span></span> | <span data-ttu-id="0cebb-124">Wert</span><span class="sxs-lookup"><span data-stu-id="0cebb-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0cebb-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0cebb-125">Minimum supported client</span></span><br/> | <span data-ttu-id="0cebb-126">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0cebb-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0cebb-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0cebb-127">Minimum supported server</span></span><br/> | <span data-ttu-id="0cebb-128">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0cebb-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0cebb-129">Header</span><span class="sxs-lookup"><span data-stu-id="0cebb-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="0cebb-130"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="0cebb-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0cebb-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0cebb-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="0cebb-132">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="0cebb-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0cebb-133">**CB- \_ FindString**</span><span class="sxs-lookup"><span data-stu-id="0cebb-133">**CB\_FINDSTRING**</span></span>](cb-findstring.md)
</dt> <dt>

[<span data-ttu-id="0cebb-134">**CB- \_ SelectString**</span><span class="sxs-lookup"><span data-stu-id="0cebb-134">**CB\_SELECTSTRING**</span></span>](cb-selectstring.md)
</dt> <dt>

[<span data-ttu-id="0cebb-135">**WM- \_ compareitem**</span><span class="sxs-lookup"><span data-stu-id="0cebb-135">**WM\_COMPAREITEM**</span></span>](wm-compareitem.md)
</dt> </dl>

 

 





