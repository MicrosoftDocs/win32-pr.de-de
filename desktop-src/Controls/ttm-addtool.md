---
title: TTM_ADDTOOL Meldung (kommstrg. h)
description: Registriert ein Tool mit einem QuickInfo-Steuerelement.
ms.assetid: c974866b-20e7-45bc-914e-9dcf9af161e0
keywords:
- Windows-Steuerelemente für TTM_ADDTOOL Meldung
topic_type:
- apiref
api_name:
- TTM_ADDTOOL
- TTM_ADDTOOLA
- TTM_ADDTOOLW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29dad3e297f8c3430f18286afa9a998eaf578a26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341800"
---
# <a name="ttm_addtool-message"></a><span data-ttu-id="54c5a-104">TTM \_ AddTool-Meldung</span><span class="sxs-lookup"><span data-stu-id="54c5a-104">TTM\_ADDTOOL message</span></span>

<span data-ttu-id="54c5a-105">Registriert ein Tool mit einem QuickInfo-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="54c5a-105">Registers a tool with a tooltip control.</span></span>

## <a name="parameters"></a><span data-ttu-id="54c5a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="54c5a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54c5a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="54c5a-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="54c5a-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="54c5a-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="54c5a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="54c5a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="54c5a-110">Zeiger auf eine [**toolinfo**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) -Struktur, die Informationen enthält, die das QuickInfo-Steuerelement zum Anzeigen von Text für das Tool benötigt.</span><span class="sxs-lookup"><span data-stu-id="54c5a-110">Pointer to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure containing information that the tooltip control needs to display text for the tool.</span></span> <span data-ttu-id="54c5a-111">Der **CBSIZE** -Member dieser Struktur muss ausgefüllt werden, bevor diese Nachricht gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="54c5a-111">The **cbSize** member of this structure must be filled in before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54c5a-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="54c5a-112">Return value</span></span>

<span data-ttu-id="54c5a-113">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="54c5a-113">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="54c5a-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="54c5a-114">Requirements</span></span>



| <span data-ttu-id="54c5a-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="54c5a-115">Requirement</span></span> | <span data-ttu-id="54c5a-116">Wert</span><span class="sxs-lookup"><span data-stu-id="54c5a-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="54c5a-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="54c5a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="54c5a-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="54c5a-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="54c5a-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="54c5a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="54c5a-120">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="54c5a-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="54c5a-121">Header</span><span class="sxs-lookup"><span data-stu-id="54c5a-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="54c5a-122"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="54c5a-122"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="54c5a-123">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="54c5a-123">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="54c5a-124">**TTM \_ Addtoolw** (Unicode) und **TTM \_ AddIn** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="54c5a-124">**TTM\_ADDTOOLW** (Unicode) and **TTM\_ADDTOOLA** (ANSI)</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="54c5a-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="54c5a-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="54c5a-126">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="54c5a-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="54c5a-127">**TTM \_ Delta Tool**</span><span class="sxs-lookup"><span data-stu-id="54c5a-127">**TTM\_DELTOOL**</span></span>](ttm-deltool.md)
</dt> <dt>

<span data-ttu-id="54c5a-128">**Licher**</span><span class="sxs-lookup"><span data-stu-id="54c5a-128">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="54c5a-129">Info-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="54c5a-129">About Tooltip Controls</span></span>](tooltip-controls.md)
</dt> </dl>

 

 





