---
title: LB_GETITEMRECT Meldung (Winuser. h)
description: Ruft die Abmessungen des Rechtecks ab, das ein Listenfeld Element umschließt, das gerade im Listenfeld angezeigt wird.
ms.assetid: 84f94bc9-f7a4-4c2d-8c35-1bd291082af9
keywords:
- Windows-Steuerelemente für LB_GETITEMRECT Meldung
topic_type:
- apiref
api_name:
- LB_GETITEMRECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98b66c7c1a3e9f93e90beea40869cecb2081cb20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476314"
---
# <a name="lb_getitemrect-message"></a><span data-ttu-id="6c81d-104">LB- \_ GetItemRect-Nachricht</span><span class="sxs-lookup"><span data-stu-id="6c81d-104">LB\_GETITEMRECT message</span></span>

<span data-ttu-id="6c81d-105">Ruft die Abmessungen des Rechtecks ab, das ein Listenfeld Element umschließt, das gerade im Listenfeld angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="6c81d-105">Gets the dimensions of the rectangle that bounds a list box item as it is currently displayed in the list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="6c81d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6c81d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c81d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6c81d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6c81d-108">Der nullbasierte Index des Elements.</span><span class="sxs-lookup"><span data-stu-id="6c81d-108">The zero-based index of the item.</span></span>

<span data-ttu-id="6c81d-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me): der *wParam* -Parameter ist auf 16-Bit-Werte beschränkt.</span><span class="sxs-lookup"><span data-stu-id="6c81d-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="6c81d-110">Dies bedeutet, dass Listenfelder nicht mehr als 32.767 Elemente enthalten dürfen.</span><span class="sxs-lookup"><span data-stu-id="6c81d-110">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="6c81d-111">Obwohl die Anzahl der Elemente eingeschränkt ist, wird die Gesamtgröße der Elemente in einem Listenfeld in Bytes nur durch den verfügbaren Arbeitsspeicher beschränkt.</span><span class="sxs-lookup"><span data-stu-id="6c81d-111">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="6c81d-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6c81d-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6c81d-113">Ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die die Client Koordinaten für das Element im Listenfeld empfängt.</span><span class="sxs-lookup"><span data-stu-id="6c81d-113">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that will receive the client coordinates for the item in the list box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c81d-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6c81d-114">Return value</span></span>

<span data-ttu-id="6c81d-115">Wenn ein Fehler auftritt, ist der Rückgabewert lb \_ Err.</span><span class="sxs-lookup"><span data-stu-id="6c81d-115">If an error occurs, the return value is LB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c81d-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6c81d-116">Requirements</span></span>



| <span data-ttu-id="6c81d-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6c81d-117">Requirement</span></span> | <span data-ttu-id="6c81d-118">Wert</span><span class="sxs-lookup"><span data-stu-id="6c81d-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c81d-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6c81d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6c81d-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6c81d-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6c81d-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6c81d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6c81d-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6c81d-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6c81d-123">Header</span><span class="sxs-lookup"><span data-stu-id="6c81d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c81d-124"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="6c81d-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c81d-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6c81d-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="6c81d-126">[**Rect**](/previous-versions//dd162897(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6c81d-126">[**RECT**](/previous-versions//dd162897(v=vs.85))</span></span>
</dt> </dl>

 

