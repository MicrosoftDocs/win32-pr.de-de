---
title: CB_SETITEMHEIGHT Meldung (Winuser. h)
description: Eine Anwendung sendet eine CB \_ setitemheight-Nachricht, um die Höhe von Listenelementen oder das Auswahlfeld in einem Kombinations Feld festzulegen.
ms.assetid: 25a01170-5ffc-4d86-b696-706f5375570b
keywords:
- Windows-Steuerelemente für CB_SETITEMHEIGHT Meldung
topic_type:
- apiref
api_name:
- CB_SETITEMHEIGHT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e46be007cdea17857e5d8ec42a12228821539d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345506"
---
# <a name="cb_setitemheight-message"></a><span data-ttu-id="c5566-104">CB- \_ sitzungsheight-Nachricht</span><span class="sxs-lookup"><span data-stu-id="c5566-104">CB\_SETITEMHEIGHT message</span></span>

<span data-ttu-id="c5566-105">Eine Anwendung sendet eine **CB \_ setitemheight** -Nachricht, um die Höhe von Listenelementen oder das Auswahlfeld in einem Kombinations Feld festzulegen.</span><span class="sxs-lookup"><span data-stu-id="c5566-105">An application sends a **CB\_SETITEMHEIGHT** message to set the height of list items or the selection field in a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="c5566-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c5566-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5566-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c5566-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c5566-108">Gibt die Komponente des Kombinations Felds an, für das die Höhe festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c5566-108">Specifies the component of the combo box for which to set the height.</span></span>

<span data-ttu-id="c5566-109">Dieser Parameter muss 1 sein, um die Höhe des Auswahl Felds festzulegen.</span><span class="sxs-lookup"><span data-stu-id="c5566-109">This parameter must be  1 to set the height of the selection field.</span></span> <span data-ttu-id="c5566-110">Es muss NULL sein, um die Höhe von Listenelementen festzulegen, es sei denn, das Kombinations Feld verfügt über das [**CBS \_**](combo-box-styles.md) -Besitzer-Format.</span><span class="sxs-lookup"><span data-stu-id="c5566-110">It must be zero to set the height of list items, unless the combo box has the [**CBS\_OWNERDRAWVARIABLE**](combo-box-styles.md) style.</span></span> <span data-ttu-id="c5566-111">In diesem Fall ist der *wParam* -Parameter der null basierte Index eines bestimmten Listen Elements.</span><span class="sxs-lookup"><span data-stu-id="c5566-111">In that case, the *wParam* parameter is the zero-based index of a specific list item.</span></span>

</dd> <dt>

<span data-ttu-id="c5566-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c5566-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c5566-113">Gibt die Höhe der von *wParam* identifizierten Kombinations Feld-Komponente in Pixel an.</span><span class="sxs-lookup"><span data-stu-id="c5566-113">Specifies the height, in pixels, of the combo box component identified by *wParam*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5566-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c5566-114">Return value</span></span>

<span data-ttu-id="c5566-115">Wenn der Index oder die Höhe ungültig ist, ist der Rückgabewert CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="c5566-115">If the index or height is invalid, the return value is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5566-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c5566-116">Remarks</span></span>

<span data-ttu-id="c5566-117">Die Auswahl Feldhöhe in einem Kombinations Feld wird unabhängig von der Höhe der Listenelemente festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c5566-117">The selection field height in a combo box is set independently of the height of the list items.</span></span> <span data-ttu-id="c5566-118">Eine Anwendung muss sicherstellen, dass die Höhe des Auswahl Felds nicht kleiner ist als die Höhe eines bestimmten Listen Elements.</span><span class="sxs-lookup"><span data-stu-id="c5566-118">An application must ensure that the height of the selection field is not smaller than the height of a particular list item.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5566-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c5566-119">Requirements</span></span>



| <span data-ttu-id="c5566-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c5566-120">Requirement</span></span> | <span data-ttu-id="c5566-121">Wert</span><span class="sxs-lookup"><span data-stu-id="c5566-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5566-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c5566-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c5566-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c5566-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c5566-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c5566-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c5566-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c5566-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c5566-126">Header</span><span class="sxs-lookup"><span data-stu-id="c5566-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5566-127"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="c5566-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5566-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c5566-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="c5566-129">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="c5566-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c5566-130">**CB- \_ GetItemHeight**</span><span class="sxs-lookup"><span data-stu-id="c5566-130">**CB\_GETITEMHEIGHT**</span></span>](cb-getitemheight.md)
</dt> <dt>

[<span data-ttu-id="c5566-131">**WM- \_ MeasureItem**</span><span class="sxs-lookup"><span data-stu-id="c5566-131">**WM\_MEASUREITEM**</span></span>](wm-measureitem.md)
</dt> </dl>

 

 





