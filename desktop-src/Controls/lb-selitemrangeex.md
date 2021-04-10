---
title: LB_SELITEMRANGEEX Meldung (Winuser. h)
description: Wählt ein oder mehrere aufeinander folgende Elemente in einem Listenfeld mit Mehrfachauswahl aus.
ms.assetid: aac85d72-43e2-4ab0-b9ee-c7a87e21d7a1
keywords:
- Windows-Steuerelemente für LB_SELITEMRANGEEX Meldung
topic_type:
- apiref
api_name:
- LB_SELITEMRANGEEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4aa3ca1335372b7a61c4dfcbc379c36e89ff933e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956999"
---
# <a name="lb_selitemrangeex-message"></a><span data-ttu-id="d9528-104">LB- \_ selitemrangeex-Nachricht</span><span class="sxs-lookup"><span data-stu-id="d9528-104">LB\_SELITEMRANGEEX message</span></span>

<span data-ttu-id="d9528-105">Wählt ein oder mehrere aufeinander folgende Elemente in einem Listenfeld mit Mehrfachauswahl aus.</span><span class="sxs-lookup"><span data-stu-id="d9528-105">Selects one or more consecutive items in a multiple-selection list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="d9528-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d9528-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9528-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d9528-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d9528-108">Gibt den NULL basierten Index des ersten Elements an, das ausgewählt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d9528-108">Specifies the zero-based index of the first item to select.</span></span>

<span data-ttu-id="d9528-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me): der *wParam* -Parameter ist auf 16-Bit-Werte beschränkt.</span><span class="sxs-lookup"><span data-stu-id="d9528-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="d9528-110">Dies bedeutet, dass Listenfelder nicht mehr als 32.767 Elemente enthalten dürfen.</span><span class="sxs-lookup"><span data-stu-id="d9528-110">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="d9528-111">Obwohl die Anzahl der Elemente eingeschränkt ist, wird die Gesamtgröße der Elemente in einem Listenfeld in Bytes nur durch den verfügbaren Arbeitsspeicher beschränkt.</span><span class="sxs-lookup"><span data-stu-id="d9528-111">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="d9528-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d9528-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d9528-113">Gibt den NULL basierten Index des letzten Elements an, das ausgewählt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d9528-113">Specifies the zero-based index of the last item to select.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9528-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d9528-114">Return value</span></span>

<span data-ttu-id="d9528-115">Wenn ein Fehler auftritt, ist der Rückgabewert lb \_ Err.</span><span class="sxs-lookup"><span data-stu-id="d9528-115">If an error occurs, the return value is LB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9528-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d9528-116">Remarks</span></span>

<span data-ttu-id="d9528-117">Wenn der *wParam* -Parameter kleiner als der *LPARAM* -Parameter ist, wird der angegebene Bereich von Elementen ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="d9528-117">If the *wParam* parameter is less than the *lParam* parameter, the specified range of items is selected.</span></span> <span data-ttu-id="d9528-118">Wenn *wParam* größer oder gleich *LPARAM* ist, wird der Bereich aus dem angegebenen Bereich von Elementen entfernt.</span><span class="sxs-lookup"><span data-stu-id="d9528-118">If *wParam* is greater than or equal to *lParam*, the range is removed from the specified range of items.</span></span> <span data-ttu-id="d9528-119">Um nur ein Element auszuwählen, wählen Sie zwei Elemente aus, und deaktivieren Sie dann das unerwünschte Element.</span><span class="sxs-lookup"><span data-stu-id="d9528-119">To select only one item, select two items and then deselect the unwanted item.</span></span>

<span data-ttu-id="d9528-120">Verwenden Sie diese Meldung nur für Listenfelder mit Mehrfachauswahl.</span><span class="sxs-lookup"><span data-stu-id="d9528-120">Use this message only with multiple-selection list boxes.</span></span>

<span data-ttu-id="d9528-121">Diese Meldung kann einen Bereich nur innerhalb der ersten 65.536 Elemente auswählen.</span><span class="sxs-lookup"><span data-stu-id="d9528-121">This message can select a range only within the first 65,536 items.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9528-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d9528-122">Requirements</span></span>



| <span data-ttu-id="d9528-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d9528-123">Requirement</span></span> | <span data-ttu-id="d9528-124">Wert</span><span class="sxs-lookup"><span data-stu-id="d9528-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9528-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d9528-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d9528-126">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d9528-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d9528-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d9528-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d9528-128">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d9528-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d9528-129">Header</span><span class="sxs-lookup"><span data-stu-id="d9528-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9528-130"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="d9528-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9528-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d9528-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="d9528-132">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="d9528-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d9528-133">**LB- \_ selitemrange**</span><span class="sxs-lookup"><span data-stu-id="d9528-133">**LB\_SELITEMRANGE**</span></span>](lb-selitemrange.md)
</dt> <dt>

[<span data-ttu-id="d9528-134">**LB- \_ Sekunden**</span><span class="sxs-lookup"><span data-stu-id="d9528-134">**LB\_SETSEL**</span></span>](lb-setsel.md)
</dt> </dl>

 

 





