---
title: LB_SETITEMDATA Meldung (Winuser. h)
description: Legt einen Wert fest, der dem angegebenen Element in einem Listenfeld zugeordnet ist.
ms.assetid: df974fa2-114a-43ef-b0ac-0451c31d95cd
keywords:
- Windows-Steuerelemente für LB_SETITEMDATA Meldung
topic_type:
- apiref
api_name:
- LB_SETITEMDATA
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02d9f9cc952ea3bf2d83358ce3b15ce6c3a2546b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105531"
---
# <a name="lb_setitemdata-message"></a><span data-ttu-id="02b23-104">LB- \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="02b23-104">LB\_SETITEMDATA message</span></span>

<span data-ttu-id="02b23-105">Legt einen Wert fest, der dem angegebenen Element in einem Listenfeld zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="02b23-105">Sets a value associated with the specified item in a list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="02b23-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="02b23-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02b23-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="02b23-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="02b23-108">Gibt den NULL basierten Index des Elements an.</span><span class="sxs-lookup"><span data-stu-id="02b23-108">Specifies the zero-based index of the item.</span></span> <span data-ttu-id="02b23-109">Wenn dieser Wert-1 ist, gilt der *LPARAM* -Wert für alle Elemente im Listenfeld.</span><span class="sxs-lookup"><span data-stu-id="02b23-109">If this value is -1, the *lParam* value applies to all items in the list box.</span></span>

<span data-ttu-id="02b23-110">Windows 95/Windows 98/Windows Millennium Edition (Windows Me): der *wParam* -Parameter ist auf 16-Bit-Werte beschränkt.</span><span class="sxs-lookup"><span data-stu-id="02b23-110">Windows 95/Windows 98/Windows Millennium Edition (Windows Me): The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="02b23-111">Dies bedeutet, dass Listenfelder nicht mehr als 32.767 Elemente enthalten dürfen.</span><span class="sxs-lookup"><span data-stu-id="02b23-111">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="02b23-112">Obwohl die Anzahl der Elemente eingeschränkt ist, wird die Gesamtgröße der Elemente in einem Listenfeld in Bytes nur durch den verfügbaren Arbeitsspeicher beschränkt.</span><span class="sxs-lookup"><span data-stu-id="02b23-112">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="02b23-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="02b23-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="02b23-114">Gibt den Wert an, der dem Element zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="02b23-114">Specifies the value to be associated with the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02b23-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="02b23-115">Return value</span></span>

<span data-ttu-id="02b23-116">Wenn ein Fehler auftritt, ist der Rückgabewert lb \_ Err.</span><span class="sxs-lookup"><span data-stu-id="02b23-116">If an error occurs, the return value is LB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="02b23-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="02b23-117">Remarks</span></span>

<span data-ttu-id="02b23-118">Wenn sich das Element in einem von einem Besitzer gezeichneten Listenfeld befindet, das ohne den [**lbs \_ hasstrings**](list-box-styles.md) -Stil erstellt wurde, ersetzt diese Nachricht den Wert, der im *LPARAM* -Parameter der [**lb \_ AddString**](lb-addstring.md) -oder [**lb \_ InsertString**](lb-insertstring.md) -Nachricht enthalten ist, die das Element dem Listenfeld hinzugefügt hat.</span><span class="sxs-lookup"><span data-stu-id="02b23-118">If the item is in an owner-drawn list box created without the [**LBS\_HASSTRINGS**](list-box-styles.md) style, this message replaces the value contained in the *lParam* parameter of the [**LB\_ADDSTRING**](lb-addstring.md) or [**LB\_INSERTSTRING**](lb-insertstring.md) message that added the item to the list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="02b23-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="02b23-119">Requirements</span></span>



| <span data-ttu-id="02b23-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="02b23-120">Requirement</span></span> | <span data-ttu-id="02b23-121">Wert</span><span class="sxs-lookup"><span data-stu-id="02b23-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02b23-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="02b23-122">Minimum supported client</span></span><br/> | <span data-ttu-id="02b23-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="02b23-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="02b23-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="02b23-124">Minimum supported server</span></span><br/> | <span data-ttu-id="02b23-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="02b23-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="02b23-126">Header</span><span class="sxs-lookup"><span data-stu-id="02b23-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="02b23-127"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="02b23-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02b23-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="02b23-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="02b23-129">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="02b23-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="02b23-130">**LB- \_ AddString**</span><span class="sxs-lookup"><span data-stu-id="02b23-130">**LB\_ADDSTRING**</span></span>](lb-addstring.md)
</dt> <dt>

[<span data-ttu-id="02b23-131">**LB- \_ GetItemData**</span><span class="sxs-lookup"><span data-stu-id="02b23-131">**LB\_GETITEMDATA**</span></span>](lb-getitemdata.md)
</dt> <dt>

[<span data-ttu-id="02b23-132">**LB- \_ InsertString**</span><span class="sxs-lookup"><span data-stu-id="02b23-132">**LB\_INSERTSTRING**</span></span>](lb-insertstring.md)
</dt> </dl>

 

 





