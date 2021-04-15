---
title: LVM_GETSTRINGWIDTH Meldung (kommstrg. h)
description: Bestimmt die Breite einer angegebenen Zeichenfolge unter Verwendung der aktuellen Schriftart des angegebenen Listenansicht-Steuer Elements. Sie können diese Nachricht explizit oder mithilfe des ListView \_ getstringwidth-Makros senden.
ms.assetid: ffe97640-d4b6-45ae-be5d-71fed69c2026
keywords:
- Windows-Steuerelemente für LVM_GETSTRINGWIDTH Meldung
topic_type:
- apiref
api_name:
- LVM_GETSTRINGWIDTH
- LVM_GETSTRINGWIDTHA
- LVM_GETSTRINGWIDTHW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71e27512eb7a2a260976356ed2a128b48975f9f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518653"
---
# <a name="lvm_getstringwidth-message"></a><span data-ttu-id="925be-105">LVM \_ getstringwidth-Nachricht</span><span class="sxs-lookup"><span data-stu-id="925be-105">LVM\_GETSTRINGWIDTH message</span></span>

<span data-ttu-id="925be-106">Bestimmt die Breite einer angegebenen Zeichenfolge unter Verwendung der aktuellen Schriftart des angegebenen Listenansicht-Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="925be-106">Determines the width of a specified string using the specified list-view control's current font.</span></span> <span data-ttu-id="925be-107">Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ getstringwidth**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getstringwidth) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="925be-107">You can send this message explicitly or by using the [**ListView\_GetStringWidth**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getstringwidth) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="925be-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="925be-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="925be-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="925be-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="925be-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="925be-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="925be-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="925be-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="925be-112">Zeiger auf eine NULL-terminierte Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="925be-112">Pointer to a null-terminated string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="925be-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="925be-113">Return value</span></span>

<span data-ttu-id="925be-114">Gibt die Zeichen folgen Breite zurück, wenn erfolgreich, andernfalls 0 (null).</span><span class="sxs-lookup"><span data-stu-id="925be-114">Returns the string width if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="925be-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="925be-115">Remarks</span></span>

<span data-ttu-id="925be-116">Die LVM \_ getstringwidth-Nachricht gibt die exakte Breite der angegebenen Zeichenfolge in Pixel zurück.</span><span class="sxs-lookup"><span data-stu-id="925be-116">The LVM\_GETSTRINGWIDTH message returns the exact width, in pixels, of the specified string.</span></span> <span data-ttu-id="925be-117">Wenn Sie die zurückgegebene Zeichen folgen Breite als Spaltenbreite in der [**LVM-Nachricht \_ setcolumnwidth**](lvm-setcolumnwidth.md) verwenden, wird die Zeichenfolge abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="925be-117">If you use the returned string width as the column width in the [**LVM\_SETCOLUMNWIDTH**](lvm-setcolumnwidth.md) message, the string will be truncated.</span></span> <span data-ttu-id="925be-118">Um die Spaltenbreite abzurufen, die die Zeichenfolge enthalten kann, ohne Sie zu kürzen, müssen Sie der zurückgegebenen Zeichen folgen Breite Auffüll Zeichen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="925be-118">To retrieve the column width that can contain the string without truncating it, you must add padding to the returned string width.</span></span>

## <a name="requirements"></a><span data-ttu-id="925be-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="925be-119">Requirements</span></span>



| <span data-ttu-id="925be-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="925be-120">Requirement</span></span> | <span data-ttu-id="925be-121">Wert</span><span class="sxs-lookup"><span data-stu-id="925be-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="925be-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="925be-122">Minimum supported client</span></span><br/> | <span data-ttu-id="925be-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="925be-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="925be-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="925be-124">Minimum supported server</span></span><br/> | <span data-ttu-id="925be-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="925be-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="925be-126">Header</span><span class="sxs-lookup"><span data-stu-id="925be-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="925be-127"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="925be-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="925be-128">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="925be-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="925be-129">**LVM \_ Getstringwidthw** (Unicode) und **LVM \_ getstringwidtha** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="925be-129">**LVM\_GETSTRINGWIDTHW** (Unicode) and **LVM\_GETSTRINGWIDTHA** (ANSI)</span></span><br/>     |



 

 





