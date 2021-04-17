---
title: LB_FINDSTRING Meldung (Winuser. h)
description: Sucht die erste Zeichenfolge in einem Listenfeld, das mit der angegebenen Zeichenfolge beginnt.
ms.assetid: 1b7f25a7-0892-4d12-b3e3-21180d9ddfb1
keywords:
- Windows-Steuerelemente für LB_FINDSTRING Meldung
topic_type:
- apiref
api_name:
- LB_FINDSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b528dbafbc386af05a091f24c8c28327739f5d40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478966"
---
# <a name="lb_findstring-message"></a><span data-ttu-id="49e31-104">Abschluss Meldung für lb- \_ FindString</span><span class="sxs-lookup"><span data-stu-id="49e31-104">LB\_FINDSTRING message</span></span>

<span data-ttu-id="49e31-105">Sucht die erste Zeichenfolge in einem Listenfeld, das mit der angegebenen Zeichenfolge beginnt.</span><span class="sxs-lookup"><span data-stu-id="49e31-105">Finds the first string in a list box that begins with the specified string.</span></span>

## <a name="parameters"></a><span data-ttu-id="49e31-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="49e31-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49e31-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="49e31-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="49e31-108">Der nullbasierte Index des Elements vor dem ersten zu durchsuchenden Element.</span><span class="sxs-lookup"><span data-stu-id="49e31-108">The zero-based index of the item before the first item to be searched.</span></span> <span data-ttu-id="49e31-109">Wenn die Suche das Ende des Listen Felds erreicht, wird die Suche vom oberen Rand des Listen Felds zurück zu dem durch den *wParam* -Parameter angegebenen Element fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="49e31-109">When the search reaches the bottom of the list box, it continues searching from the top of the list box back to the item specified by the *wParam* parameter.</span></span> <span data-ttu-id="49e31-110">Wenn *wParam* den Wert-1 hat, wird das gesamte Listenfeld von Anfang an durchsucht.</span><span class="sxs-lookup"><span data-stu-id="49e31-110">If *wParam* is -1, the entire list box is searched from the beginning.</span></span>

<span data-ttu-id="49e31-111">Windows 95/Windows 98/Windows Millennium Edition (Windows Me): der *wParam* -Parameter ist auf 16-Bit-Werte beschränkt.</span><span class="sxs-lookup"><span data-stu-id="49e31-111">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="49e31-112">Dies bedeutet, dass Listenfelder nicht mehr als 32.767 Elemente enthalten dürfen.</span><span class="sxs-lookup"><span data-stu-id="49e31-112">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="49e31-113">Obwohl die Anzahl der Elemente eingeschränkt ist, wird die Gesamtgröße der Elemente in einem Listenfeld in Bytes nur durch den verfügbaren Arbeitsspeicher beschränkt.</span><span class="sxs-lookup"><span data-stu-id="49e31-113">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="49e31-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="49e31-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="49e31-115">Ein Zeiger auf die NULL-terminierte Zeichenfolge, die die Zeichenfolge enthält, nach der gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="49e31-115">A pointer to the null-terminated string that contains the string for which to search.</span></span> <span data-ttu-id="49e31-116">Die Suche erfolgt unabhängig von der Groß-/Kleinschreibung, sodass diese Zeichenfolge eine beliebige Kombination von Groß-und Kleinbuchstaben enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="49e31-116">The search is case independent, so this string can contain any combination of uppercase and lowercase letters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49e31-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="49e31-117">Return value</span></span>

<span data-ttu-id="49e31-118">Der Rückgabewert ist der Index des übereinstimmenden Elements oder der LB- \_ Err, wenn die Suche nicht erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="49e31-118">The return value is the index of the matching item, or LB\_ERR if the search was unsuccessful.</span></span>

## <a name="remarks"></a><span data-ttu-id="49e31-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="49e31-119">Remarks</span></span>

<span data-ttu-id="49e31-120">Wenn im Listenfeld der vom Besitzer gezeichnete Stil, jedoch nicht der [**lbs \_ hasstrings**](list-box-styles.md) -Stil enthalten ist, hängt die von **lb- \_ Zeichenfolge** ausgeführte Aktion davon ab, ob der lbs- [**\_ Sortier**](list-box-styles.md) Stil verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="49e31-120">If the list box has the owner-drawn style but not the [**LBS\_HASSTRINGS**](list-box-styles.md) style, the action taken by **LB\_FINDSTRING** depends on whether the [**LBS\_SORT**](list-box-styles.md) style is used.</span></span> <span data-ttu-id="49e31-121">Wenn **lbs \_ Sort** verwendet wird, sendet das System [**WM \_ compareitem**](wm-compareitem.md) -Nachrichten an den Listenfeld Besitzer, um zu bestimmen, welches Element mit der angegebenen Zeichenfolge übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="49e31-121">If **LBS\_SORT** is used, the system sends [**WM\_COMPAREITEM**](wm-compareitem.md) messages to the list box owner to determine which item matches the specified string.</span></span> <span data-ttu-id="49e31-122">Andernfalls versucht **lb- \_ FindString** , ein Element zu finden, das über einen Long-Wert verfügt (angegeben als *LPARAM* -Parameter der [**lb \_ AddString**](lb-addstring.md) -oder [**lb \_ InsertString**](lb-insertstring.md) -Nachricht), der mit dem *LPARAM* -Parameter übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="49e31-122">Otherwise, **LB\_FINDSTRING** attempts to find an item that has a long value (supplied as the *lParam* parameter of the [**LB\_ADDSTRING**](lb-addstring.md) or [**LB\_INSERTSTRING**](lb-insertstring.md) message) that matches the *lParam* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="49e31-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="49e31-123">Requirements</span></span>



| <span data-ttu-id="49e31-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="49e31-124">Requirement</span></span> | <span data-ttu-id="49e31-125">Wert</span><span class="sxs-lookup"><span data-stu-id="49e31-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49e31-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="49e31-126">Minimum supported client</span></span><br/> | <span data-ttu-id="49e31-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="49e31-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="49e31-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="49e31-128">Minimum supported server</span></span><br/> | <span data-ttu-id="49e31-129">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="49e31-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="49e31-130">Header</span><span class="sxs-lookup"><span data-stu-id="49e31-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="49e31-131"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="49e31-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49e31-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="49e31-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49e31-133">**LB- \_ FindStringExact**</span><span class="sxs-lookup"><span data-stu-id="49e31-133">**LB\_FINDSTRINGEXACT**</span></span>](lb-findstringexact.md)
</dt> </dl>

 

 





