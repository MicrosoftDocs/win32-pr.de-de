---
title: TB_INDETERMINATE Meldung (kommstrg. h)
description: Legt den unbestimmten Zustand der angegebenen Schaltfläche in einer Symbolleiste fest oder löscht ihn.
ms.assetid: 6a0f2b82-8241-4c2e-b349-606975ba1a24
keywords:
- Windows-Steuerelemente für TB_INDETERMINATE Meldung
topic_type:
- apiref
api_name:
- TB_INDETERMINATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7f1de35f9621de4f51d371bb50dbda637d720cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040433"
---
# <a name="tb_indeterminate-message"></a><span data-ttu-id="b7dc9-104">TB \_ unbestimmte Nachricht</span><span class="sxs-lookup"><span data-stu-id="b7dc9-104">TB\_INDETERMINATE message</span></span>

<span data-ttu-id="b7dc9-105">Legt den unbestimmten Zustand der angegebenen Schaltfläche in einer Symbolleiste fest oder löscht ihn.</span><span class="sxs-lookup"><span data-stu-id="b7dc9-105">Sets or clears the indeterminate state of the specified button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="b7dc9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b7dc9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7dc9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b7dc9-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b7dc9-108">Befehls Bezeichner der Schaltfläche, deren unbestimmter Zustand festgelegt oder gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="b7dc9-108">Command identifier of the button whose indeterminate state is to be set or cleared.</span></span>

</dd> <dt>

<span data-ttu-id="b7dc9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b7dc9-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b7dc9-110">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ist ein **boolescher** Wert, der angibt, ob der unbestimmte Zustand festgelegt oder gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="b7dc9-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a **BOOL** that indicates whether to set or clear the indeterminate state.</span></span> <span data-ttu-id="b7dc9-111">**True** gibt an, dass der unbestimmte Zustand festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="b7dc9-111">If **TRUE**, the indeterminate state is set.</span></span> <span data-ttu-id="b7dc9-112">Wenn der Wert **false** ist, wird der Status gelöscht.</span><span class="sxs-lookup"><span data-stu-id="b7dc9-112">If **FALSE**, the state is cleared.</span></span>

<span data-ttu-id="b7dc9-113">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="b7dc9-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7dc9-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b7dc9-114">Return value</span></span>

<span data-ttu-id="b7dc9-115">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="b7dc9-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7dc9-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b7dc9-116">Requirements</span></span>



| <span data-ttu-id="b7dc9-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b7dc9-117">Requirement</span></span> | <span data-ttu-id="b7dc9-118">Wert</span><span class="sxs-lookup"><span data-stu-id="b7dc9-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b7dc9-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b7dc9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b7dc9-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b7dc9-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b7dc9-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b7dc9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b7dc9-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b7dc9-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b7dc9-123">Header</span><span class="sxs-lookup"><span data-stu-id="b7dc9-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7dc9-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7dc9-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

