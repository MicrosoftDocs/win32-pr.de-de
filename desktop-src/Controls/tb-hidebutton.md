---
title: TB_HIDEBUTTON Meldung (kommstrg. h)
description: Blendet die angegebene Schaltfläche in einer Symbolleiste ein oder aus.
ms.assetid: 57941a40-279a-426e-baf9-115429c62839
keywords:
- Windows-Steuerelemente für TB_HIDEBUTTON Meldung
topic_type:
- apiref
api_name:
- TB_HIDEBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e198a48ae65f13be699b76a20c9f423cdb0da197
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949698"
---
# <a name="tb_hidebutton-message"></a><span data-ttu-id="3c56d-104">TB- \_ hidebutton-Meldung</span><span class="sxs-lookup"><span data-stu-id="3c56d-104">TB\_HIDEBUTTON message</span></span>

<span data-ttu-id="3c56d-105">Blendet die angegebene Schaltfläche in einer Symbolleiste ein oder aus.</span><span class="sxs-lookup"><span data-stu-id="3c56d-105">Hides or shows the specified button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="3c56d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3c56d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c56d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3c56d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3c56d-108">Der Befehls Bezeichner der Schaltfläche, die ausgeblendet oder angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3c56d-108">Command identifier of the button to hide or show.</span></span>

</dd> <dt>

<span data-ttu-id="3c56d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3c56d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3c56d-110">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ist ein **boolescher** Wert, der angibt, ob die angegebene Schaltfläche ausgeblendet oder angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3c56d-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a **BOOL** that indicates whether to hide or show the specified button.</span></span> <span data-ttu-id="3c56d-111">**True** gibt an, dass die Schaltfläche ausgeblendet ist.</span><span class="sxs-lookup"><span data-stu-id="3c56d-111">If **TRUE**, the button is hidden.</span></span> <span data-ttu-id="3c56d-112">Wenn der Wert **false** ist, wird die Schaltfläche angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3c56d-112">If **FALSE**, the button is shown.</span></span>

<span data-ttu-id="3c56d-113">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="3c56d-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c56d-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3c56d-114">Return value</span></span>

<span data-ttu-id="3c56d-115">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="3c56d-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c56d-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3c56d-116">Requirements</span></span>



| <span data-ttu-id="3c56d-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3c56d-117">Requirement</span></span> | <span data-ttu-id="3c56d-118">Wert</span><span class="sxs-lookup"><span data-stu-id="3c56d-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3c56d-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3c56d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3c56d-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3c56d-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3c56d-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3c56d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3c56d-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3c56d-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3c56d-123">Header</span><span class="sxs-lookup"><span data-stu-id="3c56d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c56d-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c56d-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

