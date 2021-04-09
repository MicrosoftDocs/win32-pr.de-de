---
title: LB_GETITEMHEIGHT Meldung (Winuser. h)
description: Ruft die Höhe der Elemente in einem Listenfeld ab.
ms.assetid: ee96fce6-babd-4581-ac0e-2eb955fe543b
keywords:
- Windows-Steuerelemente für LB_GETITEMHEIGHT Meldung
topic_type:
- apiref
api_name:
- LB_GETITEMHEIGHT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f44aa9e9b6d52c082a5f33a10280837a33372245
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858824"
---
# <a name="lb_getitemheight-message"></a><span data-ttu-id="1441d-104">LB- \_ GetItemHeight-Nachricht</span><span class="sxs-lookup"><span data-stu-id="1441d-104">LB\_GETITEMHEIGHT message</span></span>

<span data-ttu-id="1441d-105">Ruft die Höhe der Elemente in einem Listenfeld ab.</span><span class="sxs-lookup"><span data-stu-id="1441d-105">Gets the height of items in a list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="1441d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1441d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1441d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1441d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1441d-108">Der null basierte Index des Listenfeld Elements.</span><span class="sxs-lookup"><span data-stu-id="1441d-108">The zero-based index of the list box item.</span></span> <span data-ttu-id="1441d-109">Dieser Index wird nur verwendet, wenn das Listenfeld den Wert der lbs-Besitzer [**\_ drawvariable**](list-box-styles.md) aufweist, andernfalls muss er 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="1441d-109">This index is used only if the list box has the [**LBS\_OWNERDRAWVARIABLE**](list-box-styles.md) style; otherwise, it must be zero.</span></span>

<span data-ttu-id="1441d-110">Windows 95/Windows 98/Windows Millennium Edition (Windows Me): der *wParam* -Parameter ist auf 16-Bit-Werte beschränkt.</span><span class="sxs-lookup"><span data-stu-id="1441d-110">Windows 95/Windows 98/Windows Millennium Edition (Windows Me): The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="1441d-111">Dies bedeutet, dass Listenfelder nicht mehr als 32.767 Elemente enthalten dürfen.</span><span class="sxs-lookup"><span data-stu-id="1441d-111">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="1441d-112">Obwohl die Anzahl der Elemente eingeschränkt ist, wird die Gesamtgröße der Elemente in einem Listenfeld in Bytes nur durch den verfügbaren Arbeitsspeicher beschränkt.</span><span class="sxs-lookup"><span data-stu-id="1441d-112">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="1441d-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1441d-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1441d-114">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="1441d-114">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1441d-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1441d-115">Return value</span></span>

<span data-ttu-id="1441d-116">Der Rückgabewert ist die Höhe jedes Elements im Listenfeld in Pixel.</span><span class="sxs-lookup"><span data-stu-id="1441d-116">The return value is the height, in pixels, of each item in the list box.</span></span> <span data-ttu-id="1441d-117">Der Rückgabewert ist die Höhe des Elements, das durch den *wParam* -Parameter angegeben wird, wenn das Listenfeld den Wert der lbs-Besitzer [**\_ drawvariable**](list-box-styles.md) aufweist.</span><span class="sxs-lookup"><span data-stu-id="1441d-117">The return value is the height of the item specified by the *wParam* parameter if the list box has the [**LBS\_OWNERDRAWVARIABLE**](list-box-styles.md) style.</span></span> <span data-ttu-id="1441d-118">Der Rückgabewert ist "lb err", \_ Wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="1441d-118">The return value is LB\_ERR if an error occurs.</span></span>

## <a name="requirements"></a><span data-ttu-id="1441d-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1441d-119">Requirements</span></span>



| <span data-ttu-id="1441d-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1441d-120">Requirement</span></span> | <span data-ttu-id="1441d-121">Wert</span><span class="sxs-lookup"><span data-stu-id="1441d-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1441d-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1441d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1441d-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1441d-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1441d-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1441d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1441d-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1441d-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1441d-126">Header</span><span class="sxs-lookup"><span data-stu-id="1441d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="1441d-127"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="1441d-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1441d-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1441d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1441d-129">**LB- \_ Größe**</span><span class="sxs-lookup"><span data-stu-id="1441d-129">**LB\_SETITEMHEIGHT**</span></span>](lb-setitemheight.md)
</dt> </dl>

 

 





