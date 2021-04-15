---
title: TTM_NEWTOOLRECT Meldung (kommstrg. h)
description: Legt ein neues Begrenzungs Rechteck für ein Tool fest.
ms.assetid: 81d1b745-310e-482e-8c6e-6e98e1e67b66
keywords:
- Windows-Steuerelemente für TTM_NEWTOOLRECT Meldung
topic_type:
- apiref
api_name:
- TTM_NEWTOOLRECT
- TTM_NEWTOOLRECTA
- TTM_NEWTOOLRECTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75417059b0108877d04c79af25ac98245461ad5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476779"
---
# <a name="ttm_newtoolrect-message"></a><span data-ttu-id="16fb4-104">TTM \_ newtoolrect-Meldung</span><span class="sxs-lookup"><span data-stu-id="16fb4-104">TTM\_NEWTOOLRECT message</span></span>

<span data-ttu-id="16fb4-105">Legt ein neues Begrenzungs Rechteck für ein Tool fest.</span><span class="sxs-lookup"><span data-stu-id="16fb4-105">Sets a new bounding rectangle for a tool.</span></span>

## <a name="parameters"></a><span data-ttu-id="16fb4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="16fb4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16fb4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="16fb4-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="16fb4-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="16fb4-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="16fb4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="16fb4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="16fb4-110">Zeiger auf eine [**toolinfo**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="16fb4-110">Pointer to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure.</span></span> <span data-ttu-id="16fb4-111">Die **HWND** -und **UID** -Member identifizieren ein Tool, und das **Rect** -Element gibt das neue umgebende Rechteck an.</span><span class="sxs-lookup"><span data-stu-id="16fb4-111">The **hwnd** and **uId** members identify a tool, and the **rect** member specifies the new bounding rectangle.</span></span> <span data-ttu-id="16fb4-112">Der **CBSIZE** -Member dieser Struktur muss ausgefüllt werden, bevor diese Nachricht gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="16fb4-112">The **cbSize** member of this structure must be filled in before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16fb4-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="16fb4-113">Return value</span></span>

<span data-ttu-id="16fb4-114">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="16fb4-114">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="16fb4-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="16fb4-115">Requirements</span></span>



| <span data-ttu-id="16fb4-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="16fb4-116">Requirement</span></span> | <span data-ttu-id="16fb4-117">Wert</span><span class="sxs-lookup"><span data-stu-id="16fb4-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="16fb4-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="16fb4-118">Minimum supported client</span></span><br/> | <span data-ttu-id="16fb4-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="16fb4-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="16fb4-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="16fb4-120">Minimum supported server</span></span><br/> | <span data-ttu-id="16fb4-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="16fb4-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="16fb4-122">Header</span><span class="sxs-lookup"><span data-stu-id="16fb4-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="16fb4-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="16fb4-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="16fb4-124">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="16fb4-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="16fb4-125">**TTM \_ Newtoolrectw** (Unicode) und **TTM \_ newtoolrecta** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="16fb4-125">**TTM\_NEWTOOLRECTW** (Unicode) and **TTM\_NEWTOOLRECTA** (ANSI)</span></span><br/>           |



 

 





