---
title: PBM_SETRANGE32 Meldung (kommstrg. h)
description: Legt den minimalen und maximalen Wert für eine Statusanzeige auf 32-Bit-Werte fest und zeichnet den Balken neu, um den neuen Bereich widerzuspiegeln.
ms.assetid: 7958ea14-17b4-4c0e-97ec-b09fa0d36e8b
keywords:
- Windows-Steuerelemente für PBM_SETRANGE32 Meldung
topic_type:
- apiref
api_name:
- PBM_SETRANGE32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55fcf91c794ec9ae3880d67f8df947f87fec413d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742529"
---
# <a name="pbm_setrange32-message"></a><span data-ttu-id="8d8b5-104">PBM \_ SETRANGE32 Meldung</span><span class="sxs-lookup"><span data-stu-id="8d8b5-104">PBM\_SETRANGE32 message</span></span>

<span data-ttu-id="8d8b5-105">Legt den minimalen und maximalen Wert für eine Statusanzeige auf 32-Bit-Werte fest und zeichnet den Balken neu, um den neuen Bereich widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="8d8b5-105">Sets the minimum and maximum values for a progress bar to 32-bit values, and redraws the bar to reflect the new range.</span></span>

## <a name="parameters"></a><span data-ttu-id="8d8b5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d8b5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d8b5-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8d8b5-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8d8b5-108">Minimaler Bereichs Wert.</span><span class="sxs-lookup"><span data-stu-id="8d8b5-108">Minimum range value.</span></span> <span data-ttu-id="8d8b5-109">Standardmäßig ist der Minimalwert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="8d8b5-109">By default, the minimum value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="8d8b5-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8d8b5-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8d8b5-111">Maximaler Bereichs Wert.</span><span class="sxs-lookup"><span data-stu-id="8d8b5-111">Maximum range value.</span></span> <span data-ttu-id="8d8b5-112">Dieser Wert muss größer als *wParam* sein.</span><span class="sxs-lookup"><span data-stu-id="8d8b5-112">This value must be greater than *wParam*.</span></span> <span data-ttu-id="8d8b5-113">Standardmäßig ist der Höchstwert 100.</span><span class="sxs-lookup"><span data-stu-id="8d8b5-113">By default, the maximum value is 100.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d8b5-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8d8b5-114">Return value</span></span>

<span data-ttu-id="8d8b5-115">Gibt einen **DWORD** -Wert zurück, der das vorherige 16-Bit-tiefstlimit in seinem [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) und das vorherige 16-Bit-höchst Limit in seinem [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))-Wert enthält.</span><span class="sxs-lookup"><span data-stu-id="8d8b5-115">Returns a **DWORD** value that holds the previous 16-bit low limit in its [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) and the previous 16-bit high limit in its [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span></span> <span data-ttu-id="8d8b5-116">Wenn die vorherigen Bereiche 32-Bit-Werte waren, besteht der Rückgabewert aus den **LoWord**-Werten der beiden 32-Bit-Limits.</span><span class="sxs-lookup"><span data-stu-id="8d8b5-116">If the previous ranges were 32-bit values, the return value consists of the **LOWORD** s of both 32-bit limits.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d8b5-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8d8b5-117">Remarks</span></span>

<span data-ttu-id="8d8b5-118">Verwenden Sie die [**PBM- \_ GetRange**](pbm-getrange.md) -Nachricht, um die gesamten hohen und niedrigen 32-Bit-Werte abzurufen.</span><span class="sxs-lookup"><span data-stu-id="8d8b5-118">To retrieve the entire high and low 32-bit values, use the [**PBM\_GETRANGE**](pbm-getrange.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d8b5-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8d8b5-119">Requirements</span></span>



| <span data-ttu-id="8d8b5-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8d8b5-120">Requirement</span></span> | <span data-ttu-id="8d8b5-121">Wert</span><span class="sxs-lookup"><span data-stu-id="8d8b5-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8d8b5-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8d8b5-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8d8b5-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8d8b5-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8d8b5-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8d8b5-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8d8b5-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8d8b5-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8d8b5-126">Header</span><span class="sxs-lookup"><span data-stu-id="8d8b5-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d8b5-127"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d8b5-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

