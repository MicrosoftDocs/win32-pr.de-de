---
title: UDM_GETRANGE Meldung (kommstrg. h)
description: Ruft die minimalen und maximalen Positionen (Bereich) für ein auf-ab-Steuerelement ab.
ms.assetid: fd42538a-8d96-4a9c-a1db-07c3e9afef84
keywords:
- Windows-Steuerelemente für UDM_GETRANGE Meldung
topic_type:
- apiref
api_name:
- UDM_GETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6fd8467ad4494bea92a4c1f9a68d675ef1471f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104213750"
---
# <a name="udm_getrange-message"></a><span data-ttu-id="98973-104">UDM- \_ GetRange-Nachricht</span><span class="sxs-lookup"><span data-stu-id="98973-104">UDM\_GETRANGE message</span></span>

<span data-ttu-id="98973-105">Ruft die minimalen und maximalen Positionen (Bereich) für ein auf-ab-Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="98973-105">Retrieves the minimum and maximum positions (range) for an up-down control.</span></span>

## <a name="parameters"></a><span data-ttu-id="98973-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="98973-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98973-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="98973-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="98973-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="98973-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="98973-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="98973-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="98973-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="98973-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98973-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="98973-111">Return value</span></span>

<span data-ttu-id="98973-112">Der Rückgabewert ist ein 32-Bit-Wert, der die Mindest-und höchst Position enthält.</span><span class="sxs-lookup"><span data-stu-id="98973-112">The return value is a 32-bit value that contains the minimum and maximum positions.</span></span> <span data-ttu-id="98973-113">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ist die maximale Position für das Steuerelement, und das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) ist die minimale Position.</span><span class="sxs-lookup"><span data-stu-id="98973-113">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is the maximum position for the control, and the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is the minimum position.</span></span>

## <a name="requirements"></a><span data-ttu-id="98973-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="98973-114">Requirements</span></span>



| <span data-ttu-id="98973-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="98973-115">Requirement</span></span> | <span data-ttu-id="98973-116">Wert</span><span class="sxs-lookup"><span data-stu-id="98973-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="98973-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="98973-117">Minimum supported client</span></span><br/> | <span data-ttu-id="98973-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="98973-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="98973-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="98973-119">Minimum supported server</span></span><br/> | <span data-ttu-id="98973-120">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="98973-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="98973-121">Header</span><span class="sxs-lookup"><span data-stu-id="98973-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="98973-122"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="98973-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

