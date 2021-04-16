---
title: HDM_INSERTITEM Meldung (kommstrg. h)
description: Fügt ein neues Element in ein Header Steuerelement ein. Sie können diese Nachricht explizit senden oder das-Header \_ InsertItem-Makro verwenden.
ms.assetid: aececf32-090d-4cd4-a239-4435a322f72e
keywords:
- Windows-Steuerelemente für HDM_INSERTITEM Meldung
topic_type:
- apiref
api_name:
- HDM_INSERTITEM
- HDM_INSERTITEMA
- HDM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9cabf86fea79fd437b3e9fb7e32890b3ba1a780
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476818"
---
# <a name="hdm_insertitem-message"></a><span data-ttu-id="c3ebe-105">HDM- \_ InsertItem-Meldung</span><span class="sxs-lookup"><span data-stu-id="c3ebe-105">HDM\_INSERTITEM message</span></span>

<span data-ttu-id="c3ebe-106">Fügt ein neues Element in ein Header Steuerelement ein.</span><span class="sxs-lookup"><span data-stu-id="c3ebe-106">Inserts a new item into a header control.</span></span> <span data-ttu-id="c3ebe-107">Sie können diese Nachricht explizit senden oder das- [**Header \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_insertitem) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="c3ebe-107">You can send this message explicitly or use the [**Header\_InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_insertitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c3ebe-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c3ebe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3ebe-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c3ebe-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c3ebe-110">Der Index des Elements, nach dem das neue Element eingefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c3ebe-110">The index of the item after which the new item is to be inserted.</span></span> <span data-ttu-id="c3ebe-111">Das neue Element wird am Ende des Header Steuer Elements eingefügt, wenn *wParam* größer oder gleich der Anzahl der Elemente im Steuerelement ist.</span><span class="sxs-lookup"><span data-stu-id="c3ebe-111">The new item is inserted at the end of the header control if *wParam* is greater than or equal to the number of items in the control.</span></span> <span data-ttu-id="c3ebe-112">Wenn *wParam* gleich 0 (null) ist, wird das neue Element am Anfang des Header Steuer Elements eingefügt.</span><span class="sxs-lookup"><span data-stu-id="c3ebe-112">If *wParam* is zero, the new item is inserted at the beginning of the header control.</span></span>

</dd> <dt>

<span data-ttu-id="c3ebe-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c3ebe-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c3ebe-114">Ein Zeiger auf eine [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) -Struktur, die Informationen über das neue Element enthält.</span><span class="sxs-lookup"><span data-stu-id="c3ebe-114">A pointer to an [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) structure that contains information about the new item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3ebe-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c3ebe-115">Return value</span></span>

<span data-ttu-id="c3ebe-116">Gibt den Index des neuen Elements zurück, wenn erfolgreich, andernfalls-1.</span><span class="sxs-lookup"><span data-stu-id="c3ebe-116">Returns the index of the new item if successful, or -1 otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3ebe-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c3ebe-117">Requirements</span></span>



| <span data-ttu-id="c3ebe-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c3ebe-118">Requirement</span></span> | <span data-ttu-id="c3ebe-119">Wert</span><span class="sxs-lookup"><span data-stu-id="c3ebe-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c3ebe-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c3ebe-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c3ebe-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c3ebe-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c3ebe-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c3ebe-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c3ebe-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c3ebe-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c3ebe-124">Header</span><span class="sxs-lookup"><span data-stu-id="c3ebe-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3ebe-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3ebe-125"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="c3ebe-126">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="c3ebe-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="c3ebe-127">**HDM \_ Insertitemw** (Unicode) und **HDM \_ insertitema** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="c3ebe-127">**HDM\_INSERTITEMW** (Unicode) and **HDM\_INSERTITEMA** (ANSI)</span></span><br/>             |



 

 





