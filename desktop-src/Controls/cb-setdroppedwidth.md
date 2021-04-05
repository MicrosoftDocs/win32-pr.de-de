---
title: CB_SETDROPPEDWIDTH Meldung (Winuser. h)
description: Eine Anwendung sendet die CB- \_ setdroppeer-DTH-Nachricht, um die minimale zulässige Breite (in Pixel) des Listen Felds eines Kombinations Felds mit dem Format "CBS \_ Dropdown" oder "CBS \_ DropDownList" festzulegen.
ms.assetid: 89f44733-aebe-44ea-b62d-8bd988f1bd6f
keywords:
- Windows-Steuerelemente für CB_SETDROPPEDWIDTH Meldung
topic_type:
- apiref
api_name:
- CB_SETDROPPEDWIDTH
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4c4f5ce64bfb1b48e9e811027792a11e4358edc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858888"
---
# <a name="cb_setdroppedwidth-message"></a><span data-ttu-id="a24f7-104">CB- \_ setdroppeer-DTH-Meldung</span><span class="sxs-lookup"><span data-stu-id="a24f7-104">CB\_SETDROPPEDWIDTH message</span></span>

<span data-ttu-id="a24f7-105">Eine Anwendung sendet die **CB- \_ setdroppeer-DTH** -Nachricht, um die minimale zulässige Breite (in Pixel) des Listen Felds eines Kombinations Felds mit dem Format " [**CBS \_ Dropdown**](combo-box-styles.md) " oder " [**CBS \_ DropDownList**](combo-box-styles.md) " festzulegen.</span><span class="sxs-lookup"><span data-stu-id="a24f7-105">An application sends the **CB\_SETDROPPEDWIDTH** message to set the minimum allowable width, in pixels, of the list box of a combo box with the [**CBS\_DROPDOWN**](combo-box-styles.md) or [**CBS\_DROPDOWNLIST**](combo-box-styles.md) style.</span></span>

## <a name="parameters"></a><span data-ttu-id="a24f7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a24f7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a24f7-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a24f7-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a24f7-108">Die minimale zulässige Breite des Listen Felds in Pixel.</span><span class="sxs-lookup"><span data-stu-id="a24f7-108">The minimum allowable width of the list box, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="a24f7-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a24f7-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a24f7-110">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="a24f7-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a24f7-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a24f7-111">Return value</span></span>

<span data-ttu-id="a24f7-112">Wenn die Nachricht erfolgreich ist, entspricht der Rückgabewert der neuen Breite des Listen Felds.</span><span class="sxs-lookup"><span data-stu-id="a24f7-112">If the message is successful, The return value is the new width of the list box.</span></span>

<span data-ttu-id="a24f7-113">Wenn die Nachricht fehlschlägt, ist der Rückgabewert CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="a24f7-113">If the message fails, the return value is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="a24f7-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a24f7-114">Remarks</span></span>

<span data-ttu-id="a24f7-115">Standardmäßig ist die zulässige Mindestbreite für das Dropdown-Listenfeld NULL.</span><span class="sxs-lookup"><span data-stu-id="a24f7-115">By default, the minimum allowable width of the drop-down list box is zero.</span></span> <span data-ttu-id="a24f7-116">Die Breite des Listen Felds ist entweder die minimale zulässige Breite oder die Kombinations Feldbreite, je nachdem, welcher Wert größer ist.</span><span class="sxs-lookup"><span data-stu-id="a24f7-116">The width of the list box is either the minimum allowable width or the combo box width, whichever is larger.</span></span>

## <a name="requirements"></a><span data-ttu-id="a24f7-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a24f7-117">Requirements</span></span>



| <span data-ttu-id="a24f7-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a24f7-118">Requirement</span></span> | <span data-ttu-id="a24f7-119">Wert</span><span class="sxs-lookup"><span data-stu-id="a24f7-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a24f7-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a24f7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a24f7-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a24f7-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a24f7-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a24f7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a24f7-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a24f7-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a24f7-124">Header</span><span class="sxs-lookup"><span data-stu-id="a24f7-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a24f7-125"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="a24f7-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a24f7-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a24f7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a24f7-127">**CB \_ getdroppeer-DTH**</span><span class="sxs-lookup"><span data-stu-id="a24f7-127">**CB\_GETDROPPEDWIDTH**</span></span>](cb-getdroppedwidth.md)
</dt> </dl>

 

 





