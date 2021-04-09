---
title: CB_GETLBTEXTLEN Meldung (Winuser. h)
description: Ruft die Länge einer Zeichenfolge in der Liste eines Kombinations Felds in Zeichen ab.
ms.assetid: f0fe0eef-f9db-4d9f-9a42-5bb2aeae30a0
keywords:
- Windows-Steuerelemente für CB_GETLBTEXTLEN Meldung
topic_type:
- apiref
api_name:
- CB_GETLBTEXTLEN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e42dc19b13b22f577fcc21bb32cb8810bab29be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956453"
---
# <a name="cb_getlbtextlen-message"></a><span data-ttu-id="0e562-104">CB \_ getlbtextlen-Meldung</span><span class="sxs-lookup"><span data-stu-id="0e562-104">CB\_GETLBTEXTLEN message</span></span>

<span data-ttu-id="0e562-105">Ruft die Länge einer Zeichenfolge in der Liste eines Kombinations Felds in Zeichen ab.</span><span class="sxs-lookup"><span data-stu-id="0e562-105">Gets the length, in characters, of a string in the list of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="0e562-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0e562-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e562-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0e562-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0e562-108">Der null basierte Index der Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="0e562-108">The zero-based index of the string.</span></span>

</dd> <dt>

<span data-ttu-id="0e562-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0e562-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0e562-110">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="0e562-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e562-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0e562-111">Return value</span></span>

<span data-ttu-id="0e562-112">Der Rückgabewert ist die Länge der Zeichenfolge in **TCHAR** s, wobei das abschließende Null-Zeichen ausgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="0e562-112">The return value is the length of the string, in **TCHAR** s, excluding the terminating null character.</span></span> <span data-ttu-id="0e562-113">Wenn eine ANSI-Zeichenfolge die Anzahl von Bytes ist, und wenn es sich um eine Unicode-Zeichenfolge handelt, ist dies die Anzahl der Zeichen.</span><span class="sxs-lookup"><span data-stu-id="0e562-113">If an ANSI string this is the number of bytes, and if it is a Unicode string this is the number of characters.</span></span> <span data-ttu-id="0e562-114">Unter bestimmten Bedingungen ist dieser Wert möglicherweise größer als die Länge des Texts.</span><span class="sxs-lookup"><span data-stu-id="0e562-114">Under certain conditions, this value may actually be greater than the length of the text.</span></span> <span data-ttu-id="0e562-115">Weitere Informationen finden Sie im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="0e562-115">For more information, see the Remarks section.</span></span>

<span data-ttu-id="0e562-116">Wenn der *wParam* -Parameter keinen gültigen Index angibt, ist der Rückgabewert CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="0e562-116">If the *wParam* parameter does not specify a valid index, the return value is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e562-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0e562-117">Remarks</span></span>

<span data-ttu-id="0e562-118">Unter bestimmten Bedingungen ist der Rückgabewert größer als die tatsächliche Textlänge.</span><span class="sxs-lookup"><span data-stu-id="0e562-118">Under certain conditions, the return value is larger than the actual length of the text.</span></span> <span data-ttu-id="0e562-119">Dies tritt bei bestimmten Kombinationen von ANSI und Unicode auf und ist darauf zurückzuführen, dass das Betriebssystem das mögliche vorhanden sein von DBCS-Zeichen (Double-Byte Character Set) im Text zulässt.</span><span class="sxs-lookup"><span data-stu-id="0e562-119">This occurs with certain mixtures of ANSI and Unicode, and is due to the operating system allowing for the possible existence of double-byte character set (DBCS) characters within the text.</span></span> <span data-ttu-id="0e562-120">Der Rückgabewert ist jedoch immer mindestens so groß wie die tatsächliche Textlänge. Sie können es also immer verwenden, um die Puffer Zuordnung zu steuern.</span><span class="sxs-lookup"><span data-stu-id="0e562-120">The return value, however, will always be at least as large as the actual length of the text; so you can always use it to guide buffer allocation.</span></span> <span data-ttu-id="0e562-121">Dieses Verhalten kann auftreten, wenn eine Anwendung sowohl ANSI-Funktionen als auch allgemeine Dialogfelder verwendet, die Unicode verwenden.</span><span class="sxs-lookup"><span data-stu-id="0e562-121">This behavior can occur when an application uses both ANSI functions and common dialogs, which use Unicode.</span></span>

<span data-ttu-id="0e562-122">Um die genaue Länge des Texts zu erhalten, verwenden Sie die Nachrichten [**WM \_ gettext**](/windows/desktop/winmsg/wm-gettext), [**lb \_ gettext**](lb-gettext.md)oder [**CB \_ getlbtext**](cb-getlbtext.md) oder die Funktion [**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta) .</span><span class="sxs-lookup"><span data-stu-id="0e562-122">To obtain the exact length of the text, use the [**WM\_GETTEXT**](/windows/desktop/winmsg/wm-gettext), [**LB\_GETTEXT**](lb-gettext.md), or [**CB\_GETLBTEXT**](cb-getlbtext.md) messages, or the [**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e562-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0e562-123">Requirements</span></span>



| <span data-ttu-id="0e562-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0e562-124">Requirement</span></span> | <span data-ttu-id="0e562-125">Wert</span><span class="sxs-lookup"><span data-stu-id="0e562-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e562-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0e562-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0e562-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0e562-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0e562-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0e562-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0e562-129">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0e562-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0e562-130">Header</span><span class="sxs-lookup"><span data-stu-id="0e562-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e562-131"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="0e562-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e562-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0e562-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="0e562-133">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="0e562-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0e562-134">**CB \_ getlbtext**</span><span class="sxs-lookup"><span data-stu-id="0e562-134">**CB\_GETLBTEXT**</span></span>](cb-getlbtext.md)
</dt> <dt>

[<span data-ttu-id="0e562-135">**LB- \_ gettext**</span><span class="sxs-lookup"><span data-stu-id="0e562-135">**LB\_GETTEXT**</span></span>](lb-gettext.md)
</dt> <dt>

<span data-ttu-id="0e562-136">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="0e562-136">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="0e562-137">**GetWindowText**</span><span class="sxs-lookup"><span data-stu-id="0e562-137">**GetWindowText**</span></span>](/windows/desktop/api/winuser/nf-winuser-getwindowtexta)
</dt> <dt>

[<span data-ttu-id="0e562-138">**WM \_ gettext**</span><span class="sxs-lookup"><span data-stu-id="0e562-138">**WM\_GETTEXT**</span></span>](/windows/desktop/winmsg/wm-gettext)
</dt> </dl>

 

