---
title: TDM_SET_PROGRESS_BAR_RANGE Meldung (kommstrg. h)
description: Legt die minimalen und maximalen Werte für die Statusanzeige in einem Aufgaben Dialogfeld fest.
ms.assetid: ca8b48bc-cf56-4678-bb3d-7c730a96d98c
keywords:
- Windows-Steuerelemente für TDM_SET_PROGRESS_BAR_RANGE Meldung
topic_type:
- apiref
api_name:
- TDM_SET_PROGRESS_BAR_RANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d17ebb6caa2c33282dccbb117980fc970cd45477
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859290"
---
# <a name="tdm_set_progress_bar_range-message"></a><span data-ttu-id="abf53-104">TDM \_ - \_ Meldung "Statusanzeige \_ \_ Bereich festlegen"</span><span class="sxs-lookup"><span data-stu-id="abf53-104">TDM\_SET\_PROGRESS\_BAR\_RANGE message</span></span>

<span data-ttu-id="abf53-105">Legt die minimalen und maximalen Werte für die Statusanzeige in einem Aufgaben Dialogfeld fest.</span><span class="sxs-lookup"><span data-stu-id="abf53-105">Sets the minimum and maximum values for the progress bar in a task dialog.</span></span>

## <a name="parameters"></a><span data-ttu-id="abf53-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="abf53-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="abf53-107">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="abf53-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abf53-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="abf53-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="abf53-109">*LPARAM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="abf53-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abf53-110">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) gibt den Mindestwert an.</span><span class="sxs-lookup"><span data-stu-id="abf53-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the minimum value.</span></span> <span data-ttu-id="abf53-111">Standardmäßig ist der Minimalwert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="abf53-111">By default, the minimum value is zero.</span></span> <span data-ttu-id="abf53-112">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den maximalen Wert an.</span><span class="sxs-lookup"><span data-stu-id="abf53-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the maximum value.</span></span> <span data-ttu-id="abf53-113">Standardmäßig ist der Höchstwert 100.</span><span class="sxs-lookup"><span data-stu-id="abf53-113">By default, the maximum value is 100.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="abf53-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="abf53-114">Return value</span></span>

<span data-ttu-id="abf53-115">Gibt den vorherigen minimalen und maximalen Wert zurück, wenn erfolgreich, andernfalls 0 (null).</span><span class="sxs-lookup"><span data-stu-id="abf53-115">Returns the previous minimum and maximum values, if successful, or zero otherwise.</span></span> <span data-ttu-id="abf53-116">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den minimalen Wert, und das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) enthält den maximalen Wert.</span><span class="sxs-lookup"><span data-stu-id="abf53-116">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the minimum value, and the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contains the maximum value.</span></span>

## <a name="requirements"></a><span data-ttu-id="abf53-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="abf53-117">Requirements</span></span>



| <span data-ttu-id="abf53-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="abf53-118">Requirement</span></span> | <span data-ttu-id="abf53-119">Wert</span><span class="sxs-lookup"><span data-stu-id="abf53-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="abf53-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="abf53-120">Minimum supported client</span></span><br/> | <span data-ttu-id="abf53-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="abf53-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="abf53-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="abf53-122">Minimum supported server</span></span><br/> | <span data-ttu-id="abf53-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="abf53-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="abf53-124">Header</span><span class="sxs-lookup"><span data-stu-id="abf53-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="abf53-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="abf53-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

