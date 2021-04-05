---
title: LB_DELETESTRING Meldung (Winuser. h)
description: Löscht eine Zeichenfolge in einem Listenfeld.
ms.assetid: 3f360e07-b70d-4bfc-89d4-18d3b18b0fcf
keywords:
- Windows-Steuerelemente für LB_DELETESTRING Meldung
topic_type:
- apiref
api_name:
- LB_DELETESTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 557256484ad5c5fa698d787144a37ff619b02ef2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859126"
---
# <a name="lb_deletestring-message"></a><span data-ttu-id="24c9c-104">LB- \_ deletestring-Nachricht</span><span class="sxs-lookup"><span data-stu-id="24c9c-104">LB\_DELETESTRING message</span></span>

<span data-ttu-id="24c9c-105">Löscht eine Zeichenfolge in einem Listenfeld.</span><span class="sxs-lookup"><span data-stu-id="24c9c-105">Deletes a string in a list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="24c9c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="24c9c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24c9c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="24c9c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="24c9c-108">Der null basierte Index der zu löschenden Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="24c9c-108">The zero-based index of the string to be deleted.</span></span>

<span data-ttu-id="24c9c-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me): der *wParam* -Parameter ist auf 16-Bit-Werte beschränkt.</span><span class="sxs-lookup"><span data-stu-id="24c9c-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="24c9c-110">Dies bedeutet, dass Listenfelder nicht mehr als 32.767 Elemente enthalten dürfen.</span><span class="sxs-lookup"><span data-stu-id="24c9c-110">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="24c9c-111">Obwohl die Anzahl der Elemente eingeschränkt ist, wird die Gesamtgröße der Elemente in einem Listenfeld in Bytes nur durch den verfügbaren Arbeitsspeicher beschränkt.</span><span class="sxs-lookup"><span data-stu-id="24c9c-111">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="24c9c-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="24c9c-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="24c9c-113">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="24c9c-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24c9c-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="24c9c-114">Return value</span></span>

<span data-ttu-id="24c9c-115">Der Rückgabewert ist die Anzahl der Zeichen folgen, die in der Liste verbleiben.</span><span class="sxs-lookup"><span data-stu-id="24c9c-115">The return value is a count of the strings remaining in the list.</span></span> <span data-ttu-id="24c9c-116">Der Rückgabewert ist lb \_ Err, wenn der *wParam* -Parameter einen Index angibt, der größer als die Anzahl der Elemente in der Liste ist.</span><span class="sxs-lookup"><span data-stu-id="24c9c-116">The return value is LB\_ERR if the *wParam* parameter specifies an index greater than the number of items in the list.</span></span>

## <a name="remarks"></a><span data-ttu-id="24c9c-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="24c9c-117">Remarks</span></span>

<span data-ttu-id="24c9c-118">Wenn eine Anwendung das Listenfeld mit einem vom Besitzer gezeichneten Stil, aber ohne den [**lbs \_ hasstrings**](list-box-styles.md) -Stil erstellt, sendet das System eine [**WM \_ DeleteItem**](wm-deleteitem.md) -Meldung an den Besitzer des Listen Felds, sodass die Anwendung alle zusätzlichen Daten freigibt, die dem Element zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="24c9c-118">If an application creates the list box with an owner-drawn style but without the [**LBS\_HASSTRINGS**](list-box-styles.md) style, the system sends a [**WM\_DELETEITEM**](wm-deleteitem.md) message to the owner of the list box so the application can free any additional data associated with the item.</span></span>

## <a name="requirements"></a><span data-ttu-id="24c9c-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="24c9c-119">Requirements</span></span>



| <span data-ttu-id="24c9c-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="24c9c-120">Requirement</span></span> | <span data-ttu-id="24c9c-121">Wert</span><span class="sxs-lookup"><span data-stu-id="24c9c-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24c9c-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="24c9c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="24c9c-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="24c9c-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="24c9c-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="24c9c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="24c9c-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="24c9c-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="24c9c-126">Header</span><span class="sxs-lookup"><span data-stu-id="24c9c-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="24c9c-127"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="24c9c-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24c9c-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="24c9c-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="24c9c-129">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="24c9c-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="24c9c-130">**LB- \_ AddString**</span><span class="sxs-lookup"><span data-stu-id="24c9c-130">**LB\_ADDSTRING**</span></span>](lb-addstring.md)
</dt> <dt>

[<span data-ttu-id="24c9c-131">**LB- \_ InsertString**</span><span class="sxs-lookup"><span data-stu-id="24c9c-131">**LB\_INSERTSTRING**</span></span>](lb-insertstring.md)
</dt> <dt>

[<span data-ttu-id="24c9c-132">**WM- \_ DeleteItem**</span><span class="sxs-lookup"><span data-stu-id="24c9c-132">**WM\_DELETEITEM**</span></span>](wm-deleteitem.md)
</dt> </dl>

 

 





