---
title: CB_FINDSTRINGEXACT Meldung (Winuser.h)
description: Sucht die erste Listenfeldzeichenfolge in einem Kombinationsfeld, das mit der im lParam-Parameter angegebenen Zeichenfolge übereinstimmt.
ms.assetid: 9065af9f-b18e-4fd5-a8cc-f780f8d0fb05
keywords:
- CB_FINDSTRINGEXACT Meldung Windows-Steuerelemente
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
ms.openlocfilehash: 7f99d85c7dddb95bdfb168443d6f977c22273a87
ms.sourcegitcommit: dc2f43e0f23f4a4ce239118cf9a5180f3ff0dd1d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/30/2021
ms.locfileid: "108327175"
---
# <a name="cb_findstringexact-message"></a><span data-ttu-id="13a2c-104">CB \_ FINDSTRINGEXACT-Nachricht</span><span class="sxs-lookup"><span data-stu-id="13a2c-104">CB\_FINDSTRINGEXACT message</span></span>

<span data-ttu-id="13a2c-105">Sucht die erste Listenfeldzeichenfolge in einem Kombinationsfeld, das mit der im *lParam-Parameter* angegebenen Zeichenfolge übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="13a2c-105">Finds the first list box string in a combo box that matches the string specified in the *lParam* parameter.</span></span>

## <a name="parameters"></a><span data-ttu-id="13a2c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="13a2c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13a2c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="13a2c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="13a2c-108">Der nullbasierte Index des Elements vor dem ersten zu durchsuchenden Element.</span><span class="sxs-lookup"><span data-stu-id="13a2c-108">The zero-based index of the item preceding the first item to be searched.</span></span> <span data-ttu-id="13a2c-109">Wenn die Suche den unteren Rand des Listenfelds erreicht, wird sie vom oberen Rand des Listenfelds zurück zu dem durch den *wParam-Parameter* angegebenen Element fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="13a2c-109">When the search reaches the bottom of the list box, it continues from the top of the list box back to the item specified by the *wParam* parameter.</span></span> <span data-ttu-id="13a2c-110">Wenn *wParam* -1 ist, wird das gesamte Listenfeld von Anfang an durchsucht.</span><span class="sxs-lookup"><span data-stu-id="13a2c-110">If *wParam* is -1, the entire list box is searched from the beginning.</span></span>

</dd> <dt>

<span data-ttu-id="13a2c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="13a2c-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="13a2c-112">Ein Zeiger auf die auf NULL endende Zeichenfolge, nach der gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="13a2c-112">A pointer to the null-terminated string for which to search.</span></span> <span data-ttu-id="13a2c-113">Bei der Suche wird die Groß-/Kleinschreibung nicht beachtet, sodass diese Zeichenfolge eine beliebige Kombination aus Groß- und Kleinbuchstaben enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="13a2c-113">The search is not case sensitive, so this string can contain any combination of uppercase and lowercase letters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13a2c-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="13a2c-114">Return value</span></span>

<span data-ttu-id="13a2c-115">Der Rückgabewert ist der nullbasierte Index des übereinstimmenden Elements.</span><span class="sxs-lookup"><span data-stu-id="13a2c-115">The return value is the zero-based index of the matching item.</span></span> <span data-ttu-id="13a2c-116">Wenn die Suche nicht erfolgreich ist, handelt es sich um CB \_ ERR.</span><span class="sxs-lookup"><span data-stu-id="13a2c-116">If the search is unsuccessful, it is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="13a2c-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="13a2c-117">Remarks</span></span>

<span data-ttu-id="13a2c-118">Diese Funktion ist nur erfolgreich, wenn die angegebene Zeichenfolge und ein Kombinationsfeldelement dieselbe Länge (mit Ausnahme des abschließenden NULL-Zeichens) und dieselben Zeichen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="13a2c-118">This function is successful only if the specified string and a combo box item have the same length (except for the terminating null character) and the same characters.</span></span>

<span data-ttu-id="13a2c-119">Wenn Sie das Kombinationsfeld mit einem vom Besitzer gezeichneten Stil erstellen, jedoch ohne den [**CBS \_ HASSTRINGS-Stil,**](combo-box-styles.md) hängt die Funktionalität der **CB \_ FINDSTRINGEXACT-Nachricht** davon ab, ob Ihre Anwendung den [**CBS \_ SORT-Stil**](combo-box-styles.md) verwendet.</span><span class="sxs-lookup"><span data-stu-id="13a2c-119">If you create the combo box with an owner-drawn style but without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, the functionality of **CB\_FINDSTRINGEXACT** message depends on whether your application uses the [**CBS\_SORT**](combo-box-styles.md) style.</span></span> <span data-ttu-id="13a2c-120">Wenn Sie den **CBS \_ SORT-Stil** verwenden, werden [**WM \_ COMPAREITEM-Meldungen**](wm-compareitem.md) an den Besitzer des Kombinationsfelds gesendet, um zu bestimmen, welches Element mit der angegebenen Zeichenfolge übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="13a2c-120">If you use the **CBS\_SORT** style, [**WM\_COMPAREITEM**](wm-compareitem.md) messages are sent to the owner of the combo box to determine which item matches the specified string.</span></span> <span data-ttu-id="13a2c-121">Wenn Sie den **CBS \_ SORT-Stil** nicht verwenden, sucht die **CB \_ FINDSTRINGEXACT-Nachricht** nach einem Listenelement, das dem Wert des *lParam-Parameters* entspricht.</span><span class="sxs-lookup"><span data-stu-id="13a2c-121">If you do not use the **CBS\_SORT** style, the **CB\_FINDSTRINGEXACT** message searches for a list item that matches the value of the *lParam* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="13a2c-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="13a2c-122">Requirements</span></span>



| <span data-ttu-id="13a2c-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="13a2c-123">Requirement</span></span> | <span data-ttu-id="13a2c-124">Wert</span><span class="sxs-lookup"><span data-stu-id="13a2c-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13a2c-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="13a2c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="13a2c-126">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="13a2c-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="13a2c-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="13a2c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="13a2c-128">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="13a2c-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="13a2c-129">Header</span><span class="sxs-lookup"><span data-stu-id="13a2c-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="13a2c-130"><dt>Winuser.h (windows.h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="13a2c-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13a2c-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="13a2c-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="13a2c-132">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="13a2c-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="13a2c-133">**CB \_ FINDSTRING**</span><span class="sxs-lookup"><span data-stu-id="13a2c-133">**CB\_FINDSTRING**</span></span>](cb-findstring.md)
</dt> <dt>

[<span data-ttu-id="13a2c-134">**CB \_ SELECTSTRING**</span><span class="sxs-lookup"><span data-stu-id="13a2c-134">**CB\_SELECTSTRING**</span></span>](cb-selectstring.md)
</dt> <dt>

[<span data-ttu-id="13a2c-135">**WM \_ COMPAREITEM**</span><span class="sxs-lookup"><span data-stu-id="13a2c-135">**WM\_COMPAREITEM**</span></span>](wm-compareitem.md)
</dt> </dl>

 

 





