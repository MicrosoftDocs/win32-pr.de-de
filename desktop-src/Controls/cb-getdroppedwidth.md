---
title: CB_GETDROPPEDWIDTH Meldung (Winuser. h)
description: Ruft die minimale zulässige Breite (in Pixel) des Listen Felds eines Kombinations Felds mit dem Format "CBS \_ Dropdown" oder "CBS DropDownList" in Pixel ab \_ .
ms.assetid: d7f37a6c-a623-4b15-8ef7-4b64d85c15fa
keywords:
- Windows-Steuerelemente für CB_GETDROPPEDWIDTH Meldung
topic_type:
- apiref
api_name:
- CB_GETDROPPEDWIDTH
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 299b360348a6bf7378fdfc9bc9f0959b01366642
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040606"
---
# <a name="cb_getdroppedwidth-message"></a><span data-ttu-id="f266a-104">CB \_ getdroppeer-DTH-Meldung</span><span class="sxs-lookup"><span data-stu-id="f266a-104">CB\_GETDROPPEDWIDTH message</span></span>

<span data-ttu-id="f266a-105">Ruft die minimale zulässige Breite (in Pixel) des Listen Felds eines Kombinations Felds mit dem Format " [**CBS \_ Dropdown**](combo-box-styles.md) " oder " [**CBS \_ DropDownList**](combo-box-styles.md) " in Pixel ab.</span><span class="sxs-lookup"><span data-stu-id="f266a-105">Gets the minimum allowable width, in pixels, of the list box of a combo box with the [**CBS\_DROPDOWN**](combo-box-styles.md) or [**CBS\_DROPDOWNLIST**](combo-box-styles.md) style.</span></span>

## <a name="parameters"></a><span data-ttu-id="f266a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f266a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f266a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f266a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f266a-108">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="f266a-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="f266a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f266a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f266a-110">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="f266a-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f266a-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f266a-111">Return value</span></span>

<span data-ttu-id="f266a-112">Wenn die Nachricht erfolgreich ist, entspricht der Rückgabewert der Breite in Pixel.</span><span class="sxs-lookup"><span data-stu-id="f266a-112">If the message succeeds, the return value is the width, in pixels.</span></span>

<span data-ttu-id="f266a-113">Wenn die Nachricht fehlschlägt, ist der Rückgabewert CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="f266a-113">If the message fails, the return value is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="f266a-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f266a-114">Remarks</span></span>

<span data-ttu-id="f266a-115">Standardmäßig ist die zulässige Mindestbreite für das Dropdown-Listenfeld NULL.</span><span class="sxs-lookup"><span data-stu-id="f266a-115">By default, the minimum allowable width of the drop-down list box is zero.</span></span> <span data-ttu-id="f266a-116">Die Breite des Listen Felds ist entweder die minimale zulässige Breite oder die Kombinations Feldbreite, je nachdem, welcher Wert größer ist.</span><span class="sxs-lookup"><span data-stu-id="f266a-116">The width of the list box is either the minimum allowable width or the combo box width, whichever is larger.</span></span>

## <a name="requirements"></a><span data-ttu-id="f266a-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f266a-117">Requirements</span></span>



| <span data-ttu-id="f266a-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f266a-118">Requirement</span></span> | <span data-ttu-id="f266a-119">Wert</span><span class="sxs-lookup"><span data-stu-id="f266a-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f266a-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f266a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f266a-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f266a-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f266a-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f266a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f266a-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f266a-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f266a-124">Header</span><span class="sxs-lookup"><span data-stu-id="f266a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f266a-125"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="f266a-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f266a-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f266a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f266a-127">**CB \_ setdroppeer-DTH**</span><span class="sxs-lookup"><span data-stu-id="f266a-127">**CB\_SETDROPPEDWIDTH**</span></span>](cb-setdroppedwidth.md)
</dt> </dl>

 

 





