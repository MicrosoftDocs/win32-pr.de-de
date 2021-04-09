---
title: LB_GETSELCOUNT Meldung (Winuser. h)
description: Ruft die Gesamtanzahl der ausgewählten Elemente in einem Listenfeld mit Mehrfachauswahl ab.
ms.assetid: 1597f6d0-e8f2-4e10-8a0e-ef76192e6238
keywords:
- Windows-Steuerelemente für LB_GETSELCOUNT Meldung
topic_type:
- apiref
api_name:
- LB_GETSELCOUNT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed73b387315d1b612241d41e47e6b613a3a75f12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103367"
---
# <a name="lb_getselcount-message"></a><span data-ttu-id="08c9f-104">LB- \_ getselcount-Nachricht</span><span class="sxs-lookup"><span data-stu-id="08c9f-104">LB\_GETSELCOUNT message</span></span>

<span data-ttu-id="08c9f-105">Ruft die Gesamtanzahl der ausgewählten Elemente in einem Listenfeld mit Mehrfachauswahl ab.</span><span class="sxs-lookup"><span data-stu-id="08c9f-105">Gets the total number of selected items in a multiple-selection list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="08c9f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="08c9f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08c9f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="08c9f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="08c9f-108">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="08c9f-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="08c9f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="08c9f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="08c9f-110">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="08c9f-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08c9f-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="08c9f-111">Return value</span></span>

<span data-ttu-id="08c9f-112">Der Rückgabewert ist die Anzahl der ausgewählten Elemente im Listenfeld.</span><span class="sxs-lookup"><span data-stu-id="08c9f-112">The return value is the count of selected items in the list box.</span></span> <span data-ttu-id="08c9f-113">Wenn das Listenfeld ein Listenfeld für die einfache Auswahl ist, lautet der Rückgabewert lb \_ Err.</span><span class="sxs-lookup"><span data-stu-id="08c9f-113">If the list box is a single-selection list box, the return value is LB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="08c9f-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="08c9f-114">Requirements</span></span>



| <span data-ttu-id="08c9f-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="08c9f-115">Requirement</span></span> | <span data-ttu-id="08c9f-116">Wert</span><span class="sxs-lookup"><span data-stu-id="08c9f-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08c9f-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="08c9f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="08c9f-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="08c9f-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="08c9f-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="08c9f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="08c9f-120">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="08c9f-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="08c9f-121">Header</span><span class="sxs-lookup"><span data-stu-id="08c9f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="08c9f-122"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="08c9f-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08c9f-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="08c9f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08c9f-124">**LB- \_ Sekunden**</span><span class="sxs-lookup"><span data-stu-id="08c9f-124">**LB\_SETSEL**</span></span>](lb-setsel.md)
</dt> </dl>

 

 





