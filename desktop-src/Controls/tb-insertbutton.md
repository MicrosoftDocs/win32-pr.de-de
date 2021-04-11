---
title: TB_INSERTBUTTON Meldung (kommstrg. h)
description: Fügt eine Schaltfläche in eine Symbolleiste ein.
ms.assetid: 6be27817-5d86-4649-bd63-173845197763
keywords:
- Windows-Steuerelemente für TB_INSERTBUTTON Meldung
topic_type:
- apiref
api_name:
- TB_INSERTBUTTON
- TB_INSERTBUTTONA
- TB_INSERTBUTTONW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e08eed328a99d4a8927a7e09084bf122f2e4e84
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103342"
---
# <a name="tb_insertbutton-message"></a><span data-ttu-id="f9cb4-104">TB \_ InsertButton-Meldung</span><span class="sxs-lookup"><span data-stu-id="f9cb4-104">TB\_INSERTBUTTON message</span></span>

<span data-ttu-id="f9cb4-105">Fügt eine Schaltfläche in eine Symbolleiste ein.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-105">Inserts a button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="f9cb4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f9cb4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9cb4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f9cb4-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f9cb4-108">NULL basierter Index einer Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-108">Zero-based index of a button.</span></span> <span data-ttu-id="f9cb4-109">Die Meldung fügt die Schaltfläche "neu" auf der linken Seite dieser Schaltfläche ein.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-109">The message inserts the new button to the left of this button.</span></span>

</dd> <dt>

<span data-ttu-id="f9cb4-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f9cb4-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f9cb4-111">Ein Zeiger auf eine [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) -Struktur, die Informationen über die einzufügende Schaltfläche enthält.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-111">Pointer to a [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structure containing information about the button to insert.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9cb4-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f9cb4-112">Return value</span></span>

<span data-ttu-id="f9cb4-113">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="f9cb4-113">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9cb4-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f9cb4-114">Requirements</span></span>



| <span data-ttu-id="f9cb4-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f9cb4-115">Requirement</span></span> | <span data-ttu-id="f9cb4-116">Wert</span><span class="sxs-lookup"><span data-stu-id="f9cb4-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f9cb4-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f9cb4-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f9cb4-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f9cb4-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f9cb4-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f9cb4-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f9cb4-120">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f9cb4-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f9cb4-121">Header</span><span class="sxs-lookup"><span data-stu-id="f9cb4-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9cb4-122"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9cb4-122"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="f9cb4-123">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="f9cb4-123">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f9cb4-124">**TB \_ Insertbuttonw** (Unicode) und **TB \_ insertbuttona** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f9cb4-124">**TB\_INSERTBUTTONW** (Unicode) and **TB\_INSERTBUTTONA** (ANSI)</span></span><br/>           |



 

 





