---
title: CB_GETITEMHEIGHT Meldung (Winuser. h)
description: Bestimmt die Höhe von Listenelementen oder das Auswahlfeld in einem Kombinations Feld.
ms.assetid: 72fba6ca-0a51-4801-bd45-5f5a7d5ebee2
keywords:
- Windows-Steuerelemente für CB_GETITEMHEIGHT Meldung
topic_type:
- apiref
api_name:
- CB_GETITEMHEIGHT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4aac9d8f9a430c056f8b91a9306d77c182f4c96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858894"
---
# <a name="cb_getitemheight-message"></a><span data-ttu-id="f0088-104">CB \_ GetItemHeight-Nachricht</span><span class="sxs-lookup"><span data-stu-id="f0088-104">CB\_GETITEMHEIGHT message</span></span>

<span data-ttu-id="f0088-105">Bestimmt die Höhe von Listenelementen oder das Auswahlfeld in einem Kombinations Feld.</span><span class="sxs-lookup"><span data-stu-id="f0088-105">Determines the height of list items or the selection field in a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="f0088-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f0088-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0088-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f0088-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f0088-108">Die Kombinations Feld Komponente, deren Höhe abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="f0088-108">The combo box component whose height is to be retrieved.</span></span> <span data-ttu-id="f0088-109">Dieser Parameter muss den Wert-1 aufweisen, um die Höhe des Auswahl Felds abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f0088-109">This parameter must be -1 to retrieve the height of the selection field.</span></span> <span data-ttu-id="f0088-110">Es muss NULL sein, um die Höhe von Listenelementen abzurufen, es sei denn, das Kombinations Feld hat das Format [**CBS \_**](combo-box-styles.md) -Besitzer.</span><span class="sxs-lookup"><span data-stu-id="f0088-110">It must be zero to retrieve the height of list items, unless the combo box has the [**CBS\_OWNERDRAWVARIABLE**](combo-box-styles.md) style.</span></span> <span data-ttu-id="f0088-111">In diesem Fall ist der *wParam* -Parameter der null basierte Index eines bestimmten Listen Elements.</span><span class="sxs-lookup"><span data-stu-id="f0088-111">In that case, the *wParam* parameter is the zero-based index of a specific list item.</span></span>

</dd> <dt>

<span data-ttu-id="f0088-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f0088-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f0088-113">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="f0088-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0088-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f0088-114">Return value</span></span>

<span data-ttu-id="f0088-115">Der Rückgabewert ist die Höhe der Listenelemente in einem Kombinations Feld in Pixel.</span><span class="sxs-lookup"><span data-stu-id="f0088-115">The return value is the height, in pixels, of the list items in a combo box.</span></span> <span data-ttu-id="f0088-116">Wenn das Kombinations Feld den [**CBS- \_**](combo-box-styles.md) Besitzer für das-Objekt aufweist, ist es die Höhe des Elements, das durch den *wParam* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f0088-116">If the combo box has the [**CBS\_OWNERDRAWVARIABLE**](combo-box-styles.md) style, it is the height of the item specified by the *wParam* parameter.</span></span> <span data-ttu-id="f0088-117">Wenn *wParam* den Wert-1 hat, ist der Rückgabewert die Höhe des Bearbeitungs Steuer Elements (oder statischer Text) des Kombinations Felds.</span><span class="sxs-lookup"><span data-stu-id="f0088-117">If *wParam* is -1, the return value is the height of the edit control (or static-text) portion of the combo box.</span></span> <span data-ttu-id="f0088-118">Wenn ein Fehler auftritt, ist der Rückgabewert CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="f0088-118">If an error occurs, the return value is CB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0088-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f0088-119">Requirements</span></span>



| <span data-ttu-id="f0088-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f0088-120">Requirement</span></span> | <span data-ttu-id="f0088-121">Wert</span><span class="sxs-lookup"><span data-stu-id="f0088-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0088-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f0088-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f0088-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f0088-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f0088-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f0088-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f0088-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f0088-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f0088-126">Header</span><span class="sxs-lookup"><span data-stu-id="f0088-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0088-127"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="f0088-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0088-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f0088-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="f0088-129">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="f0088-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f0088-130">**CB- \_ sitztemheight**</span><span class="sxs-lookup"><span data-stu-id="f0088-130">**CB\_SETITEMHEIGHT**</span></span>](cb-setitemheight.md)
</dt> <dt>

[<span data-ttu-id="f0088-131">**WM- \_ MeasureItem**</span><span class="sxs-lookup"><span data-stu-id="f0088-131">**WM\_MEASUREITEM**</span></span>](wm-measureitem.md)
</dt> </dl>

 

 





