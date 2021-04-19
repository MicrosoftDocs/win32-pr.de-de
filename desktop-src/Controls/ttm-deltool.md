---
title: TTM_DELTOOL Meldung (kommstrg. h)
description: Entfernt ein Tool aus einem QuickInfo-Steuerelement.
ms.assetid: 433b6f1c-3e9f-4e3a-9834-d447a3f9e6a5
keywords:
- Windows-Steuerelemente für TTM_DELTOOL Meldung
topic_type:
- apiref
api_name:
- TTM_DELTOOL
- TTM_DELTOOLA
- TTM_DELTOOLW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d943259c5496757c0f15ca4127d0a5e6a4237fbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341388"
---
# <a name="ttm_deltool-message"></a><span data-ttu-id="9e7c1-104">TTM \_ Delta Tool-Meldung</span><span class="sxs-lookup"><span data-stu-id="9e7c1-104">TTM\_DELTOOL message</span></span>

<span data-ttu-id="9e7c1-105">Entfernt ein Tool aus einem QuickInfo-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="9e7c1-105">Removes a tool from a tooltip control.</span></span>

## <a name="parameters"></a><span data-ttu-id="9e7c1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9e7c1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e7c1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9e7c1-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="9e7c1-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="9e7c1-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="9e7c1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9e7c1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9e7c1-110">Zeiger auf eine [**toolinfo**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="9e7c1-110">Pointer to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure.</span></span> <span data-ttu-id="9e7c1-111">Die **HWND** -und **UID** -Member identifizieren das zu entfernenden Tool, und das **CBSIZE** -Element muss die Größe der Struktur angeben.</span><span class="sxs-lookup"><span data-stu-id="9e7c1-111">The **hwnd** and **uId** members identify the tool to remove, and the **cbSize** member must specify the size of the structure.</span></span> <span data-ttu-id="9e7c1-112">Alle anderen Member werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="9e7c1-112">All other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e7c1-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9e7c1-113">Return value</span></span>

<span data-ttu-id="9e7c1-114">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="9e7c1-114">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e7c1-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9e7c1-115">Requirements</span></span>



| <span data-ttu-id="9e7c1-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9e7c1-116">Requirement</span></span> | <span data-ttu-id="9e7c1-117">Wert</span><span class="sxs-lookup"><span data-stu-id="9e7c1-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9e7c1-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9e7c1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9e7c1-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9e7c1-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9e7c1-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9e7c1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9e7c1-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9e7c1-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9e7c1-122">Header</span><span class="sxs-lookup"><span data-stu-id="9e7c1-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e7c1-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e7c1-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="9e7c1-124">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="9e7c1-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="9e7c1-125">**TTM \_ Delta toolw** (Unicode) und **TTM \_ Delta** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="9e7c1-125">**TTM\_DELTOOLW** (Unicode) and **TTM\_DELTOOLA** (ANSI)</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="9e7c1-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9e7c1-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="9e7c1-127">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="9e7c1-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9e7c1-128">**TTM \_ AddTool**</span><span class="sxs-lookup"><span data-stu-id="9e7c1-128">**TTM\_ADDTOOL**</span></span>](ttm-addtool.md)
</dt> <dt>

<span data-ttu-id="9e7c1-129">**Licher**</span><span class="sxs-lookup"><span data-stu-id="9e7c1-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9e7c1-130">Info-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="9e7c1-130">About Tooltip Controls</span></span>](tooltip-controls.md)
</dt> </dl>

 

 





