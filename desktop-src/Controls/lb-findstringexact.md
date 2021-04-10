---
title: LB_FINDSTRINGEXACT Meldung (Winuser. h)
description: Sucht die erste Listenfeld Zeichenfolge, die exakt mit der angegebenen Zeichenfolge übereinstimmt
ms.assetid: 9bfe21af-626d-4416-aa20-65c425bd99af
keywords:
- Windows-Steuerelemente für LB_FINDSTRINGEXACT Meldung
topic_type:
- apiref
api_name:
- LB_FINDSTRINGEXACT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d85b4f817eabae95c6021647b0c47926b2163722
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040956"
---
# <a name="lb_findstringexact-message"></a><span data-ttu-id="649e5-104">LB- \_ FindStringExact-Nachricht</span><span class="sxs-lookup"><span data-stu-id="649e5-104">LB\_FINDSTRINGEXACT message</span></span>

<span data-ttu-id="649e5-105">Sucht die erste Listenfeld Zeichenfolge, die exakt mit der angegebenen Zeichenfolge übereinstimmt</span><span class="sxs-lookup"><span data-stu-id="649e5-105">Finds the first list box string that exactly matches the specified string, except that the search is not case sensitive.</span></span>

## <a name="parameters"></a><span data-ttu-id="649e5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="649e5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="649e5-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="649e5-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="649e5-108">Der nullbasierte Index des Elements vor dem ersten zu durchsuchenden Element.</span><span class="sxs-lookup"><span data-stu-id="649e5-108">The zero-based index of the item before the first item to be searched.</span></span> <span data-ttu-id="649e5-109">Wenn die Suche das Ende des Listen Felds erreicht, wird die Suche vom oberen Rand des Listen Felds zurück zu dem durch den *wParam* -Parameter angegebenen Element fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="649e5-109">When the search reaches the bottom of the list box, it continues searching from the top of the list box back to the item specified by the *wParam* parameter.</span></span> <span data-ttu-id="649e5-110">Wenn *wParam* den Wert-1 hat, wird das gesamte Listenfeld von Anfang an durchsucht.</span><span class="sxs-lookup"><span data-stu-id="649e5-110">If *wParam* is -1, the entire list box is searched from the beginning.</span></span>

<span data-ttu-id="649e5-111">Windows 95/Windows 98/Windows Millennium Edition (Windows Me): der *wParam* -Parameter ist auf 16-Bit-Werte beschränkt.</span><span class="sxs-lookup"><span data-stu-id="649e5-111">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="649e5-112">Dies bedeutet, dass Listenfelder nicht mehr als 32.767 Elemente enthalten dürfen.</span><span class="sxs-lookup"><span data-stu-id="649e5-112">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="649e5-113">Obwohl die Anzahl der Elemente eingeschränkt ist, wird die Gesamtgröße der Elemente in einem Listenfeld in Bytes nur durch den verfügbaren Arbeitsspeicher beschränkt.</span><span class="sxs-lookup"><span data-stu-id="649e5-113">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="649e5-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="649e5-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="649e5-115">Ein Zeiger auf die NULL-terminierte Zeichenfolge, nach der gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="649e5-115">A pointer to the null-terminated string for which to search.</span></span> <span data-ttu-id="649e5-116">Bei der Suche wird die Groß-/Kleinschreibung nicht beachtet, sodass diese Zeichenfolge eine beliebige Kombination von Groß-und Kleinbuchstaben enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="649e5-116">The search is not case sensitive, so this string can contain any combination of uppercase and lowercase letters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="649e5-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="649e5-117">Return value</span></span>

<span data-ttu-id="649e5-118">Der Rückgabewert ist der null basierte Index des übereinstimmenden Elements oder der LB- \_ Err, wenn die Suche nicht erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="649e5-118">The return value is the zero-based index of the matching item, or LB\_ERR if the search was unsuccessful.</span></span>

## <a name="remarks"></a><span data-ttu-id="649e5-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="649e5-119">Remarks</span></span>

<span data-ttu-id="649e5-120">Diese Funktion ist nur erfolgreich, wenn die angegebene Zeichenfolge und ein Listenfeld Element dieselbe Länge aufweisen (mit Ausnahme von Null am Ende der angegebenen Zeichenfolge) und genau die gleichen Zeichen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="649e5-120">This function is only successful if the specified string and a list box item have the same length (except for the null at the end of the specified string) and have exactly the same characters.</span></span>

<span data-ttu-id="649e5-121">Wenn im Listenfeld der vom Besitzer gezeichnete Stil, jedoch nicht der [**lbs \_ hasstrings**](list-box-styles.md) -Stil enthalten ist, hängt die von **lb \_ FindStringExact** ausgeführte Aktion davon ab, ob der [**lbs- \_ Sortier**](list-box-styles.md) Stil verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="649e5-121">If the list box has the owner-drawn style but not the [**LBS\_HASSTRINGS**](list-box-styles.md) style, the action taken by **LB\_FINDSTRINGEXACT** depends on whether the [**LBS\_SORT**](list-box-styles.md) style is used.</span></span> <span data-ttu-id="649e5-122">Wenn **lbs \_ Sort** verwendet wird, sendet das System [**WM \_ compareitem**](wm-compareitem.md) -Nachrichten an den Listenfeld Besitzer, um zu bestimmen, welches Element mit der angegebenen Zeichenfolge übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="649e5-122">If **LBS\_SORT** is used, the system sends [**WM\_COMPAREITEM**](wm-compareitem.md) messages to the list box owner to determine which item matches the specified string.</span></span> <span data-ttu-id="649e5-123">Andernfalls versucht **lb \_ FindStringExact** , ein Element zu finden, das über einen Long-Wert verfügt (angegeben als *LPARAM* -Parameter der [**lb \_ AddString**](lb-addstring.md) -oder [**lb \_ InsertString**](lb-insertstring.md) -Nachricht), der mit dem *LPARAM* -Parameter übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="649e5-123">Otherwise, **LB\_FINDSTRINGEXACT** attempts to find an item that has a long value (supplied as the *lParam* parameter of the [**LB\_ADDSTRING**](lb-addstring.md) or [**LB\_INSERTSTRING**](lb-insertstring.md) message) that matches the *lParam* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="649e5-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="649e5-124">Requirements</span></span>



| <span data-ttu-id="649e5-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="649e5-125">Requirement</span></span> | <span data-ttu-id="649e5-126">Wert</span><span class="sxs-lookup"><span data-stu-id="649e5-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="649e5-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="649e5-127">Minimum supported client</span></span><br/> | <span data-ttu-id="649e5-128">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="649e5-128">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="649e5-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="649e5-129">Minimum supported server</span></span><br/> | <span data-ttu-id="649e5-130">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="649e5-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="649e5-131">Header</span><span class="sxs-lookup"><span data-stu-id="649e5-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="649e5-132"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="649e5-132"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="649e5-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="649e5-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="649e5-134">**LB- \_ FindString**</span><span class="sxs-lookup"><span data-stu-id="649e5-134">**LB\_FINDSTRING**</span></span>](lb-findstring.md)
</dt> </dl>

 

 





