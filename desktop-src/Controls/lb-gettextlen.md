---
title: LB_GETTEXTLEN Meldung (Winuser. h)
description: Ruft die Länge einer Zeichenfolge in einem Listenfeld ab.
ms.assetid: 866730bc-ffd4-42fd-9cea-5d326e129189
keywords:
- Windows-Steuerelemente für LB_GETTEXTLEN Meldung
topic_type:
- apiref
api_name:
- LB_GETTEXTLEN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1f76bf3574b09b76d5f1010dcb59c8245555dc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103483"
---
# <a name="lb_gettextlen-message"></a><span data-ttu-id="621d6-104">LB- \_ gettextlen-Nachricht</span><span class="sxs-lookup"><span data-stu-id="621d6-104">LB\_GETTEXTLEN message</span></span>

<span data-ttu-id="621d6-105">Ruft die Länge einer Zeichenfolge in einem Listenfeld ab.</span><span class="sxs-lookup"><span data-stu-id="621d6-105">Gets the length of a string in a list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="621d6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="621d6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="621d6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="621d6-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="621d6-108">Der null basierte Index der Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="621d6-108">The zero-based index of the string.</span></span>

<span data-ttu-id="621d6-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me): der *wParam* -Parameter ist auf 16-Bit-Werte beschränkt.</span><span class="sxs-lookup"><span data-stu-id="621d6-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="621d6-110">Dies bedeutet, dass Listenfelder nicht mehr als 32.767 Elemente enthalten dürfen.</span><span class="sxs-lookup"><span data-stu-id="621d6-110">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="621d6-111">Obwohl die Anzahl der Elemente eingeschränkt ist, wird die Gesamtgröße der Elemente in einem Listenfeld in Bytes nur durch den verfügbaren Arbeitsspeicher beschränkt.</span><span class="sxs-lookup"><span data-stu-id="621d6-111">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="621d6-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="621d6-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="621d6-113">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="621d6-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="621d6-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="621d6-114">Return value</span></span>

<span data-ttu-id="621d6-115">Der Rückgabewert ist die Länge der Zeichenfolge in **TCHAR** s, wobei das abschließende Null-Zeichen ausgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="621d6-115">The return value is the length of the string, in **TCHAR** s, excluding the terminating null character.</span></span> <span data-ttu-id="621d6-116">Unter bestimmten Bedingungen ist dieser Wert möglicherweise größer als die Länge des Texts.</span><span class="sxs-lookup"><span data-stu-id="621d6-116">Under certain conditions, this value may actually be greater than the length of the text.</span></span> <span data-ttu-id="621d6-117">Weitere Informationen finden Sie im folgenden Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="621d6-117">For more information, see the following Remarks section.</span></span>

<span data-ttu-id="621d6-118">Wenn vom *wParam* -Parameter kein gültiger Index angegeben wird, ist der Rückgabewert lb \_ Err.</span><span class="sxs-lookup"><span data-stu-id="621d6-118">If the *wParam* parameter does not specify a valid index, the return value is LB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="621d6-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="621d6-119">Remarks</span></span>

<span data-ttu-id="621d6-120">Unter bestimmten Bedingungen ist der Rückgabewert größer als die tatsächliche Textlänge.</span><span class="sxs-lookup"><span data-stu-id="621d6-120">Under certain conditions, the return value is larger than the actual length of the text.</span></span> <span data-ttu-id="621d6-121">Dies tritt bei bestimmten Kombinationen von ANSI und Unicode auf und ist darauf zurückzuführen, dass das Betriebssystem das mögliche vorhanden sein von DBCS-Zeichen (Double-Byte Character Set) im Text zulässt.</span><span class="sxs-lookup"><span data-stu-id="621d6-121">This occurs with certain mixtures of ANSI and Unicode, and is due to the operating system allowing for the possible existence of double-byte character set (DBCS) characters within the text.</span></span> <span data-ttu-id="621d6-122">Der Rückgabewert ist jedoch immer mindestens so groß wie die tatsächliche Textlänge. Sie können Sie daher immer verwenden, um die Puffer Zuordnung zu steuern.</span><span class="sxs-lookup"><span data-stu-id="621d6-122">The return value, however, will always be at least as large as the actual length of the text; you can thus always use it to guide buffer allocation.</span></span> <span data-ttu-id="621d6-123">Dieses Verhalten kann auftreten, wenn eine Anwendung sowohl ANSI-Funktionen als auch allgemeine Dialogfelder verwendet, die Unicode verwenden.</span><span class="sxs-lookup"><span data-stu-id="621d6-123">This behavior can occur when an application uses both ANSI functions and common dialogs, which use Unicode.</span></span>

<span data-ttu-id="621d6-124">Um die genaue Länge des Texts zu erhalten, verwenden Sie die Nachrichten [**WM \_ gettext**](/windows/desktop/winmsg/wm-gettext), [**lb \_ gettext**](lb-gettext.md)oder [**CB \_ getlbtext**](cb-getlbtext.md) oder die Funktion [**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta) .</span><span class="sxs-lookup"><span data-stu-id="621d6-124">To obtain the exact length of the text, use the [**WM\_GETTEXT**](/windows/desktop/winmsg/wm-gettext), [**LB\_GETTEXT**](lb-gettext.md), or [**CB\_GETLBTEXT**](cb-getlbtext.md) messages, or the [**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta) function.</span></span>

<span data-ttu-id="621d6-125">Wenn im Listenfeld ein vom Besitzer gezeichneter Stil, aber nicht der [**lbs \_ hasstrings**](list-box-styles.md) -Stil enthalten ist, ist der Rückgabewert immer die Größe eines **DWORD**(in Bytes).</span><span class="sxs-lookup"><span data-stu-id="621d6-125">If the list box has an owner-drawn style, but not the [**LBS\_HASSTRINGS**](list-box-styles.md) style, the return value is always the size, in bytes, of a **DWORD**.</span></span>

## <a name="requirements"></a><span data-ttu-id="621d6-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="621d6-126">Requirements</span></span>



| <span data-ttu-id="621d6-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="621d6-127">Requirement</span></span> | <span data-ttu-id="621d6-128">Wert</span><span class="sxs-lookup"><span data-stu-id="621d6-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="621d6-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="621d6-129">Minimum supported client</span></span><br/> | <span data-ttu-id="621d6-130">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="621d6-130">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="621d6-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="621d6-131">Minimum supported server</span></span><br/> | <span data-ttu-id="621d6-132">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="621d6-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="621d6-133">Header</span><span class="sxs-lookup"><span data-stu-id="621d6-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="621d6-134"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="621d6-134"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="621d6-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="621d6-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="621d6-136">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="621d6-136">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="621d6-137">**CB \_ getlbtext**</span><span class="sxs-lookup"><span data-stu-id="621d6-137">**CB\_GETLBTEXT**</span></span>](cb-getlbtext.md)
</dt> <dt>

[<span data-ttu-id="621d6-138">**LB- \_ gettext**</span><span class="sxs-lookup"><span data-stu-id="621d6-138">**LB\_GETTEXT**</span></span>](lb-gettext.md)
</dt> <dt>

<span data-ttu-id="621d6-139">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="621d6-139">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="621d6-140">**GetWindowText**</span><span class="sxs-lookup"><span data-stu-id="621d6-140">**GetWindowText**</span></span>](/windows/desktop/api/winuser/nf-winuser-getwindowtexta)
</dt> <dt>

[<span data-ttu-id="621d6-141">**WM \_ gettext**</span><span class="sxs-lookup"><span data-stu-id="621d6-141">**WM\_GETTEXT**</span></span>](/windows/desktop/winmsg/wm-gettext)
</dt> </dl>

 

