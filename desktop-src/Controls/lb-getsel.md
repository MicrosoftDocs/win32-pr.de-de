---
title: LB_GETSEL Meldung (Winuser. h)
description: Ruft den Auswahl Zustand eines Elements ab.
ms.assetid: f92c02e7-3c6d-4649-8798-42eb4a0c51b6
keywords:
- Windows-Steuerelemente für LB_GETSEL Meldung
topic_type:
- apiref
api_name:
- LB_GETSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35d808935e65a1ea748c59d606aa2cf483748fb4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859006"
---
# <a name="lb_getsel-message"></a><span data-ttu-id="aaf4f-104">LB- \_ GetSEL-Nachricht</span><span class="sxs-lookup"><span data-stu-id="aaf4f-104">LB\_GETSEL message</span></span>

<span data-ttu-id="aaf4f-105">Ruft den Auswahl Zustand eines Elements ab.</span><span class="sxs-lookup"><span data-stu-id="aaf4f-105">Gets the selection state of an item.</span></span>

## <a name="parameters"></a><span data-ttu-id="aaf4f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="aaf4f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aaf4f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="aaf4f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aaf4f-108">Der nullbasierte Index des Elements.</span><span class="sxs-lookup"><span data-stu-id="aaf4f-108">The zero-based index of the item.</span></span>

<span data-ttu-id="aaf4f-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me): der *wParam* -Parameter ist auf 16-Bit-Werte beschränkt.</span><span class="sxs-lookup"><span data-stu-id="aaf4f-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="aaf4f-110">Dies bedeutet, dass Listenfelder nicht mehr als 32.767 Elemente enthalten dürfen.</span><span class="sxs-lookup"><span data-stu-id="aaf4f-110">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="aaf4f-111">Obwohl die Anzahl der Elemente eingeschränkt ist, wird die Gesamtgröße der Elemente in einem Listenfeld in Bytes nur durch den verfügbaren Arbeitsspeicher beschränkt.</span><span class="sxs-lookup"><span data-stu-id="aaf4f-111">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="aaf4f-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="aaf4f-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aaf4f-113">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="aaf4f-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aaf4f-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="aaf4f-114">Return value</span></span>

<span data-ttu-id="aaf4f-115">Wenn ein Element ausgewählt wird, ist der Rückgabewert größer als 0 (null). Andernfalls ist der Wert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="aaf4f-115">If an item is selected, the return value is greater than zero; otherwise, it is zero.</span></span> <span data-ttu-id="aaf4f-116">Wenn ein Fehler auftritt, ist der Rückgabewert lb \_ Err.</span><span class="sxs-lookup"><span data-stu-id="aaf4f-116">If an error occurs, the return value is LB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="aaf4f-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aaf4f-117">Requirements</span></span>



| <span data-ttu-id="aaf4f-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aaf4f-118">Requirement</span></span> | <span data-ttu-id="aaf4f-119">Wert</span><span class="sxs-lookup"><span data-stu-id="aaf4f-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aaf4f-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="aaf4f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="aaf4f-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aaf4f-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="aaf4f-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="aaf4f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="aaf4f-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aaf4f-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="aaf4f-124">Header</span><span class="sxs-lookup"><span data-stu-id="aaf4f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="aaf4f-125"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="aaf4f-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aaf4f-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aaf4f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aaf4f-127">**LB- \_ Sekunden**</span><span class="sxs-lookup"><span data-stu-id="aaf4f-127">**LB\_SETSEL**</span></span>](lb-setsel.md)
</dt> </dl>

 

 





