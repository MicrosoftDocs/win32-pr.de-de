---
title: CBEM_INSERTITEM Meldung (kommstrg. h)
description: Fügt ein neues Element in einem ComboBoxEx-Steuerelement ein.
ms.assetid: c99db676-204d-44c9-aaa3-81b70fe2cf44
keywords:
- Windows-Steuerelemente für CBEM_INSERTITEM Meldung
topic_type:
- apiref
api_name:
- CBEM_INSERTITEM
- CBEM_INSERTITEMA
- CBEM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23e6cb26a575472e53703d65e407a94a024dcfac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345521"
---
# <a name="cbem_insertitem-message"></a><span data-ttu-id="daf42-104">CBEM \_ InsertItem-Meldung</span><span class="sxs-lookup"><span data-stu-id="daf42-104">CBEM\_INSERTITEM message</span></span>

<span data-ttu-id="daf42-105">Fügt ein neues Element in einem ComboBoxEx-Steuerelement ein.</span><span class="sxs-lookup"><span data-stu-id="daf42-105">Inserts a new item in a ComboBoxEx control.</span></span>

## <a name="parameters"></a><span data-ttu-id="daf42-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="daf42-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="daf42-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="daf42-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="daf42-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="daf42-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="daf42-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="daf42-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="daf42-110">Ein Zeiger auf eine [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) -Struktur, die Informationen über das einzufügende Element enthält.</span><span class="sxs-lookup"><span data-stu-id="daf42-110">A pointer to a [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) structure that contains information about the item to be inserted.</span></span> <span data-ttu-id="daf42-111">Wenn die Nachricht gesendet wird, muss der **iItem** -Member so festgelegt werden, dass er den NULL basierten Index angibt, an dem das Element eingefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="daf42-111">When the message is sent, the **iItem** member must be set to indicate the zero-based index at which to insert the item.</span></span> <span data-ttu-id="daf42-112">Wenn Sie ein Element am Ende der Liste einfügen möchten, legen Sie den **iItem** -Member auf-1 fest.</span><span class="sxs-lookup"><span data-stu-id="daf42-112">To insert an item at the end of the list, set the **iItem** member to -1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="daf42-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="daf42-113">Return value</span></span>

<span data-ttu-id="daf42-114">Gibt den Index zurück, bei dem das neue Element eingefügt wurde, andernfalls-1.</span><span class="sxs-lookup"><span data-stu-id="daf42-114">Returns the index at which the new item was inserted if successful, or -1 otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="daf42-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="daf42-115">Requirements</span></span>



| <span data-ttu-id="daf42-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="daf42-116">Requirement</span></span> | <span data-ttu-id="daf42-117">Wert</span><span class="sxs-lookup"><span data-stu-id="daf42-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="daf42-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="daf42-118">Minimum supported client</span></span><br/> | <span data-ttu-id="daf42-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="daf42-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="daf42-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="daf42-120">Minimum supported server</span></span><br/> | <span data-ttu-id="daf42-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="daf42-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="daf42-122">Header</span><span class="sxs-lookup"><span data-stu-id="daf42-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="daf42-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="daf42-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="daf42-124">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="daf42-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="daf42-125">**CBEM \_ Insertitemw** (Unicode) und **CBEM \_ insertitema** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="daf42-125">**CBEM\_INSERTITEMW** (Unicode) and **CBEM\_INSERTITEMA** (ANSI)</span></span><br/>           |



 

 





