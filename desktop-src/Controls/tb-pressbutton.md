---
title: TB_PRESSBUTTON Meldung (kommstrg. h)
description: Drückt die angegebene Schaltfläche in einer Symbolleiste oder gibt diese frei.
ms.assetid: 03f6c3c2-d679-4e3a-a07b-c7e46c97972a
keywords:
- Windows-Steuerelemente für TB_PRESSBUTTON Meldung
topic_type:
- apiref
api_name:
- TB_PRESSBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b0e86092951b242cee7388fc0d5d1bbdbca835e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105044"
---
# <a name="tb_pressbutton-message"></a><span data-ttu-id="d94c3-104">TB- \_ pressbutton-Meldung</span><span class="sxs-lookup"><span data-stu-id="d94c3-104">TB\_PRESSBUTTON message</span></span>

<span data-ttu-id="d94c3-105">Drückt die angegebene Schaltfläche in einer Symbolleiste oder gibt diese frei.</span><span class="sxs-lookup"><span data-stu-id="d94c3-105">Presses or releases the specified button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="d94c3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d94c3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d94c3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d94c3-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d94c3-108">Befehls Bezeichner der Schaltfläche, die gedrückt oder freigegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="d94c3-108">Command identifier of the button to press or release.</span></span>

</dd> <dt>

<span data-ttu-id="d94c3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d94c3-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d94c3-110">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ist ein **boolescher** Wert, der angibt, ob die angegebene Schaltfläche gedrückt oder freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d94c3-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a **BOOL** that indicates whether to press or release the specified button.</span></span> <span data-ttu-id="d94c3-111">**True** gibt an, dass die Schaltfläche gedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="d94c3-111">If **TRUE**, the button is pressed.</span></span> <span data-ttu-id="d94c3-112">Wenn der Wert **false** ist, wird die Schaltfläche losgelassen.</span><span class="sxs-lookup"><span data-stu-id="d94c3-112">If **FALSE**, the button is released.</span></span>

<span data-ttu-id="d94c3-113">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="d94c3-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d94c3-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d94c3-114">Return value</span></span>

<span data-ttu-id="d94c3-115">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="d94c3-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="d94c3-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d94c3-116">Requirements</span></span>



| <span data-ttu-id="d94c3-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d94c3-117">Requirement</span></span> | <span data-ttu-id="d94c3-118">Wert</span><span class="sxs-lookup"><span data-stu-id="d94c3-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d94c3-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d94c3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d94c3-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d94c3-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d94c3-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d94c3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d94c3-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d94c3-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d94c3-123">Header</span><span class="sxs-lookup"><span data-stu-id="d94c3-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d94c3-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="d94c3-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

