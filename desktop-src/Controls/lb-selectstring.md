---
title: LB_SELECTSTRING Meldung (Winuser. h)
description: Durchsucht ein Listenfeld nach einem Element, das mit den Zeichen in einer angegebenen Zeichenfolge beginnt. Wenn ein übereinstimmendes Element gefunden wird, wird das Element ausgewählt.
ms.assetid: fd443ade-665d-439a-8951-3d9fed50695b
keywords:
- Windows-Steuerelemente für LB_SELECTSTRING Meldung
topic_type:
- apiref
api_name:
- LB_SELECTSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5963ea6530038e17bc7f23d9ab66eba14ca0b05d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478549"
---
# <a name="lb_selectstring-message"></a><span data-ttu-id="459e2-105">LB- \_ SelectString-Nachricht</span><span class="sxs-lookup"><span data-stu-id="459e2-105">LB\_SELECTSTRING message</span></span>

<span data-ttu-id="459e2-106">Durchsucht ein Listenfeld nach einem Element, das mit den Zeichen in einer angegebenen Zeichenfolge beginnt.</span><span class="sxs-lookup"><span data-stu-id="459e2-106">Searches a list box for an item that begins with the characters in a specified string.</span></span> <span data-ttu-id="459e2-107">Wenn ein übereinstimmendes Element gefunden wird, wird das Element ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="459e2-107">If a matching item is found, the item is selected.</span></span>

## <a name="parameters"></a><span data-ttu-id="459e2-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="459e2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="459e2-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="459e2-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="459e2-110">Der nullbasierte Index des Elements vor dem ersten zu durchsuchenden Element.</span><span class="sxs-lookup"><span data-stu-id="459e2-110">The zero-based index of the item before the first item to be searched.</span></span> <span data-ttu-id="459e2-111">Wenn die Suche das Ende des Listen Felds erreicht, wird Sie von der obersten Position des Listen Felds zurück zu dem durch den *wParam* -Parameter angegebenen Element weiter angezeigt.</span><span class="sxs-lookup"><span data-stu-id="459e2-111">When the search reaches the bottom of the list box, it continues from the top of the list box back to the item specified by the *wParam* parameter.</span></span> <span data-ttu-id="459e2-112">Wenn *wParam* den Wert-1 hat, wird das gesamte Listenfeld von Anfang an durchsucht.</span><span class="sxs-lookup"><span data-stu-id="459e2-112">If *wParam* is -1, the entire list box is searched from the beginning.</span></span>

<span data-ttu-id="459e2-113">Windows 95/Windows 98/Windows Millennium Edition (Windows Me): der *wParam* -Parameter ist auf 16-Bit-Werte beschränkt.</span><span class="sxs-lookup"><span data-stu-id="459e2-113">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="459e2-114">Dies bedeutet, dass Listenfelder nicht mehr als 32.767 Elemente enthalten dürfen.</span><span class="sxs-lookup"><span data-stu-id="459e2-114">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="459e2-115">Obwohl die Anzahl der Elemente eingeschränkt ist, wird die Gesamtgröße der Elemente in einem Listenfeld in Bytes nur durch den verfügbaren Arbeitsspeicher beschränkt.</span><span class="sxs-lookup"><span data-stu-id="459e2-115">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="459e2-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="459e2-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="459e2-117">Ein Zeiger auf die NULL-terminierte Zeichenfolge, die das Präfix enthält, nach dem gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="459e2-117">A pointer to the null-terminated string that contains the prefix for which to search.</span></span> <span data-ttu-id="459e2-118">Die Suche erfolgt unabhängig von der Groß-/Kleinschreibung, sodass diese Zeichenfolge eine beliebige Kombination von Groß-und Kleinbuchstaben enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="459e2-118">The search is case independent, so this string can contain any combination of uppercase and lowercase letters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="459e2-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="459e2-119">Return value</span></span>

<span data-ttu-id="459e2-120">Wenn die Suche erfolgreich ist, ist der Rückgabewert der Index des ausgewählten Elements.</span><span class="sxs-lookup"><span data-stu-id="459e2-120">If the search is successful, the return value is the index of the selected item.</span></span> <span data-ttu-id="459e2-121">Wenn die Suche nicht erfolgreich ist, lautet der Rückgabewert "lb err", \_ und die aktuelle Auswahl wird nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="459e2-121">If the search is unsuccessful, the return value is LB\_ERR and the current selection is not changed.</span></span>

## <a name="remarks"></a><span data-ttu-id="459e2-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="459e2-122">Remarks</span></span>

<span data-ttu-id="459e2-123">Das Listenfeld wird ggf. mit einem Bildlauf ausgeführt, um das ausgewählte Element in der Ansicht anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="459e2-123">The list box is scrolled, if necessary, to bring the selected item into view.</span></span>

<span data-ttu-id="459e2-124">Verwenden Sie diese Meldung nicht mit einem Listenfeld, das die " [**lbs \_ multiplesel**](list-box-styles.md) "-oder " [**lbs \_ extendedsel**](list-box-styles.md) "-Stile aufweist.</span><span class="sxs-lookup"><span data-stu-id="459e2-124">Do not use this message with a list box that has the [**LBS\_MULTIPLESEL**](list-box-styles.md) or the [**LBS\_EXTENDEDSEL**](list-box-styles.md) styles.</span></span>

<span data-ttu-id="459e2-125">Ein Element wird nur ausgewählt, wenn die ursprünglichen Zeichen vom Startpunkt den Zeichen in der durch den *LPARAM* -Parameter angegebenen Zeichenfolge entsprechen.</span><span class="sxs-lookup"><span data-stu-id="459e2-125">An item is selected only if its initial characters from the starting point match the characters in the string specified by the *lParam* parameter.</span></span>

<span data-ttu-id="459e2-126">Wenn im Listenfeld der vom Besitzer gezeichnete Stil, jedoch nicht der [**lbs \_ hasstrings**](list-box-styles.md) -Stil enthalten ist, hängt die von **lb \_ SelectString** ausgeführte Aktion davon ab, ob der [**lbs- \_ Sortier**](list-box-styles.md) Stil verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="459e2-126">If the list box has the owner-drawn style but not the [**LBS\_HASSTRINGS**](list-box-styles.md) style, the action taken by **LB\_SELECTSTRING** depends on whether the [**LBS\_SORT**](list-box-styles.md) style is used.</span></span> <span data-ttu-id="459e2-127">Wenn **lbs \_ Sort** verwendet wird, sendet das System [**WM \_ compareitem**](wm-compareitem.md) -Nachrichten an den Listenfeld Besitzer, um zu bestimmen, welches Element mit der angegebenen Zeichenfolge übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="459e2-127">If **LBS\_SORT** is used, the system sends [**WM\_COMPAREITEM**](wm-compareitem.md) messages to the list box owner to determine which item matches the specified string.</span></span> <span data-ttu-id="459e2-128">Andernfalls versucht **lb \_ SelectString** , ein Element zu finden, das über einen Long-Wert verfügt (angegeben als *LPARAM* -Parameter der [**lb \_ AddString**](lb-addstring.md) -oder [**lb \_ InsertString**](lb-insertstring.md) -Nachricht), der mit dem *LPARAM* -Parameter übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="459e2-128">Otherwise, **LB\_SELECTSTRING** attempts to find an item that has a long value (supplied as the *lParam* parameter of the [**LB\_ADDSTRING**](lb-addstring.md) or [**LB\_INSERTSTRING**](lb-insertstring.md) message) that matches the *lParam* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="459e2-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="459e2-129">Requirements</span></span>



| <span data-ttu-id="459e2-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="459e2-130">Requirement</span></span> | <span data-ttu-id="459e2-131">Wert</span><span class="sxs-lookup"><span data-stu-id="459e2-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="459e2-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="459e2-132">Minimum supported client</span></span><br/> | <span data-ttu-id="459e2-133">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="459e2-133">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="459e2-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="459e2-134">Minimum supported server</span></span><br/> | <span data-ttu-id="459e2-135">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="459e2-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="459e2-136">Header</span><span class="sxs-lookup"><span data-stu-id="459e2-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="459e2-137"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="459e2-137"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="459e2-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="459e2-138">See also</span></span>

<dl> <dt>

<span data-ttu-id="459e2-139">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="459e2-139">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="459e2-140">**LB- \_ AddString**</span><span class="sxs-lookup"><span data-stu-id="459e2-140">**LB\_ADDSTRING**</span></span>](lb-addstring.md)
</dt> <dt>

[<span data-ttu-id="459e2-141">**LB- \_ FindString**</span><span class="sxs-lookup"><span data-stu-id="459e2-141">**LB\_FINDSTRING**</span></span>](lb-findstring.md)
</dt> <dt>

[<span data-ttu-id="459e2-142">**LB- \_ InsertString**</span><span class="sxs-lookup"><span data-stu-id="459e2-142">**LB\_INSERTSTRING**</span></span>](lb-insertstring.md)
</dt> </dl>

 

 





