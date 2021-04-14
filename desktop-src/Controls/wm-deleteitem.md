---
title: WM_DELETEITEM Meldung (Winuser. h)
description: Wird an den Besitzer eines Listen Felds oder Kombinations Felds gesendet, wenn das Listenfeld oder Kombinations Feld zerstört wird oder wenn Elemente von der LB- \_ deletestring-, lb \_ resetcontent-, CB \_ deletestring-oder CB \_ resetcontent-Nachricht entfernt werden.
ms.assetid: c3adf8fb-45f2-44f1-8821-6ffa7d76dc78
keywords:
- Windows-Steuerelemente für WM_DELETEITEM Meldung
topic_type:
- apiref
api_name:
- WM_DELETEITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbf37f8a367d23353903bd3cda85b573f6884ff2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476473"
---
# <a name="wm_deleteitem-message"></a><span data-ttu-id="b59d3-104">WM \_ DeleteItem-Meldung</span><span class="sxs-lookup"><span data-stu-id="b59d3-104">WM\_DELETEITEM message</span></span>

<span data-ttu-id="b59d3-105">Wird an den Besitzer eines Listen Felds oder Kombinations Felds gesendet, wenn das Listenfeld oder Kombinations Feld zerstört wird oder wenn Elemente von der [**lb- \_ deletestring**](lb-deletestring.md)- [**, lb \_ resetcontent**](lb-resetcontent.md)-, [**CB \_ deletestring**](cb-deletestring.md)-oder [**CB \_ resetcontent**](cb-resetcontent.md) -Nachricht entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="b59d3-105">Sent to the owner of a list box or combo box when the list box or combo box is destroyed or when items are removed by the [**LB\_DELETESTRING**](lb-deletestring.md), [**LB\_RESETCONTENT**](lb-resetcontent.md), [**CB\_DELETESTRING**](cb-deletestring.md), or [**CB\_RESETCONTENT**](cb-resetcontent.md) message.</span></span> <span data-ttu-id="b59d3-106">Das System sendet eine " **WM \_ DeleteItem** "-Meldung für jedes gelöschte Element.</span><span class="sxs-lookup"><span data-stu-id="b59d3-106">The system sends a **WM\_DELETEITEM** message for each deleted item.</span></span> <span data-ttu-id="b59d3-107">Das System sendet die " **WM \_ DeleteItem** "-Meldung für ein beliebiges gelöschtes Listenfeld oder Kombinations Feld Element mit Elementdaten, die nicht NULL sind.</span><span class="sxs-lookup"><span data-stu-id="b59d3-107">The system sends the **WM\_DELETEITEM** message for any deleted list box or combo box item with nonzero item data.</span></span>


```C++
WM_DELETEITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="b59d3-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b59d3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b59d3-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b59d3-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b59d3-110">Gibt den Bezeichner des Steuer Elements an, das die **WM- \_ DeleteItem** -Nachricht gesendet hat.</span><span class="sxs-lookup"><span data-stu-id="b59d3-110">Specifies the identifier of the control that sent the **WM\_DELETEITEM** message.</span></span>

</dd> <dt>

<span data-ttu-id="b59d3-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b59d3-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b59d3-112">Ein Zeiger auf eine [**deleteitemstruct**](/windows/win32/api/winuser/ns-winuser-deleteitemstruct) -Struktur, die Informationen über das Element enthält, das aus einem Listenfeld gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="b59d3-112">Pointer to a [**DELETEITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-deleteitemstruct) structure that contains information about the item deleted from a list box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b59d3-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b59d3-113">Return value</span></span>

<span data-ttu-id="b59d3-114">Eine Anwendung sollte **true** zurückgeben, wenn Sie diese Nachricht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="b59d3-114">An application should return **TRUE** if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="b59d3-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b59d3-115">Remarks</span></span>

<span data-ttu-id="b59d3-116">Microsoft Windows NT und höher: Windows sendet eine **WM \_ DeleteItem** -Nachricht nur für Elemente, die aus einem von einem Besitzer gezeichneten Listenfeld (mit dem "lbs-Besitzer" oder "lbs-Besitzer"-Stil) oder dem vom Besitzer gezeichneten Kombinations Feld (mit dem [**CBS \_**](combo-box-styles.md) -Besitzer-oder [**CBS \_**](combo-box-styles.md) -Besitzer-Stil) gelöscht wurden. [**\_**](list-box-styles.md) [**\_**](list-box-styles.md)</span><span class="sxs-lookup"><span data-stu-id="b59d3-116">Microsoft Windows NT and later: Windows sends a **WM\_DELETEITEM** message only for items deleted from an owner-drawn list box (with the [**LBS\_OWNERDRAWFIXED**](list-box-styles.md) or [**LBS\_OWNERDRAWVARIABLE**](list-box-styles.md) style) or owner-drawn combo box (with the [**CBS\_OWNERDRAWFIXED**](combo-box-styles.md) or [**CBS\_OWNERDRAWVARIABLE**](combo-box-styles.md) style).</span></span>

<span data-ttu-id="b59d3-117">Windows 95: Windows sendet die " **WM \_ DeleteItem** "-Meldung für ein beliebiges gelöschtes Listenfeld oder Kombinations Feld Element mit Elementdaten, die nicht NULL sind.</span><span class="sxs-lookup"><span data-stu-id="b59d3-117">Windows 95: Windows sends the **WM\_DELETEITEM** message for any deleted list box or combo box item with nonzero item data.</span></span>

## <a name="requirements"></a><span data-ttu-id="b59d3-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b59d3-118">Requirements</span></span>



| <span data-ttu-id="b59d3-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b59d3-119">Requirement</span></span> | <span data-ttu-id="b59d3-120">Wert</span><span class="sxs-lookup"><span data-stu-id="b59d3-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b59d3-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b59d3-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b59d3-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b59d3-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b59d3-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b59d3-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b59d3-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b59d3-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b59d3-125">Header</span><span class="sxs-lookup"><span data-stu-id="b59d3-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b59d3-126"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="b59d3-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b59d3-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b59d3-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="b59d3-128">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="b59d3-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b59d3-129">**CB \_ deletestring**</span><span class="sxs-lookup"><span data-stu-id="b59d3-129">**CB\_DELETESTRING**</span></span>](cb-deletestring.md)
</dt> <dt>

[<span data-ttu-id="b59d3-130">**CB \_ resetcontent**</span><span class="sxs-lookup"><span data-stu-id="b59d3-130">**CB\_RESETCONTENT**</span></span>](cb-resetcontent.md)
</dt> <dt>

[<span data-ttu-id="b59d3-131">**DELETEITEMSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="b59d3-131">**DELETEITEMSTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-deleteitemstruct)
</dt> <dt>

[<span data-ttu-id="b59d3-132">**LB- \_ deletestring**</span><span class="sxs-lookup"><span data-stu-id="b59d3-132">**LB\_DELETESTRING**</span></span>](lb-deletestring.md)
</dt> <dt>

[<span data-ttu-id="b59d3-133">**LB- \_ resetcontent**</span><span class="sxs-lookup"><span data-stu-id="b59d3-133">**LB\_RESETCONTENT**</span></span>](lb-resetcontent.md)
</dt> </dl>

 

 





