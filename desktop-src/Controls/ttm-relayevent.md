---
title: TTM_RELAYEVENT Meldung (kommstrg. h)
description: Übergibt eine Maus Nachricht zur Verarbeitung an ein QuickInfo-Steuerelement.
ms.assetid: 76d6d0ed-f357-479e-83d8-03d2e988cbd3
keywords:
- Windows-Steuerelemente für TTM_RELAYEVENT Meldung
topic_type:
- apiref
api_name:
- TTM_RELAYEVENT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8648303a318f1f71eb16e8070235910ecfb8760
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353249"
---
# <a name="ttm_relayevent-message"></a><span data-ttu-id="8ee24-104">TTM \_ relayevent-Nachricht</span><span class="sxs-lookup"><span data-stu-id="8ee24-104">TTM\_RELAYEVENT message</span></span>

<span data-ttu-id="8ee24-105">Übergibt eine Maus Nachricht zur Verarbeitung an ein QuickInfo-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="8ee24-105">Passes a mouse message to a tooltip control for processing.</span></span>

## <a name="parameters"></a><span data-ttu-id="8ee24-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8ee24-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ee24-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8ee24-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8ee24-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="8ee24-108">Must be zero.</span></span> <span data-ttu-id="8ee24-109">**Windows 7 und höher:** Wenn die Position der QuickInfo von der Cursorposition versetzt ist (damit Sie nicht durch einen Finger oder ein Zeigegerät behindert wird), kann dieser Parameter zusätzliche Informationen enthalten, die aus der [**WM- \_ mousettverschiebungmeldung**](/windows/desktop/inputdev/wm-mousemove) entnommen werden.</span><span class="sxs-lookup"><span data-stu-id="8ee24-109">**Windows 7 and later:** If the position of the tooltip is offset from the cursor position (in order not be obstructed by a finger or pointing device), this parameter can contain extra information taken from the [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) message.</span></span> <span data-ttu-id="8ee24-110">Rufen Sie diese zusätzlichen Informationen mit [**getMessageExtraInfo**](/windows/desktop/api/winuser/nf-winuser-getmessageextrainfo)ab.</span><span class="sxs-lookup"><span data-stu-id="8ee24-110">Retrieve this extra information with [**GetMessageExtraInfo**](/windows/desktop/api/winuser/nf-winuser-getmessageextrainfo).</span></span>

</dd> <dt>

<span data-ttu-id="8ee24-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8ee24-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8ee24-112">Zeiger auf eine [**msg**](/windows/win32/api/winuser/ns-winuser-msg) -Struktur, die die zu relaynachricht enthält.</span><span class="sxs-lookup"><span data-stu-id="8ee24-112">Pointer to an [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) structure that contains the message to relay.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ee24-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8ee24-113">Return value</span></span>

<span data-ttu-id="8ee24-114">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="8ee24-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ee24-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8ee24-115">Remarks</span></span>

<span data-ttu-id="8ee24-116">Ein QuickInfo-Steuerelement verarbeitet nur die folgenden Nachrichten, die von der **TTM \_ Relay** -Meldung an das Steuerelement weitergegeben werden</span><span class="sxs-lookup"><span data-stu-id="8ee24-116">A tooltip control processes only the following messages passed to it by the **TTM\_RELAYEVENT** message:</span></span>

-   <span data-ttu-id="8ee24-117">WM \_ lbuttondown</span><span class="sxs-lookup"><span data-stu-id="8ee24-117">WM\_LBUTTONDOWN</span></span>
-   <span data-ttu-id="8ee24-118">WM- \_ lbuttonup</span><span class="sxs-lookup"><span data-stu-id="8ee24-118">WM\_LBUTTONUP</span></span>
-   <span data-ttu-id="8ee24-119">WM- \_ mbuttondown</span><span class="sxs-lookup"><span data-stu-id="8ee24-119">WM\_MBUTTONDOWN</span></span>
-   <span data-ttu-id="8ee24-120">WM- \_ mbuttonup</span><span class="sxs-lookup"><span data-stu-id="8ee24-120">WM\_MBUTTONUP</span></span>
-   <span data-ttu-id="8ee24-121">WM- \_ mouseelmove</span><span class="sxs-lookup"><span data-stu-id="8ee24-121">WM\_MOUSEMOVE</span></span>
-   <span data-ttu-id="8ee24-122">WM- \_ ncmouummove</span><span class="sxs-lookup"><span data-stu-id="8ee24-122">WM\_NCMOUSEMOVE</span></span>
-   <span data-ttu-id="8ee24-123">WM- \_ rbuttondown</span><span class="sxs-lookup"><span data-stu-id="8ee24-123">WM\_RBUTTONDOWN</span></span>
-   <span data-ttu-id="8ee24-124">WM- \_ rbuttonup</span><span class="sxs-lookup"><span data-stu-id="8ee24-124">WM\_RBUTTONUP</span></span>

<span data-ttu-id="8ee24-125">Alle anderen Nachrichten werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="8ee24-125">All other messages are ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ee24-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8ee24-126">Requirements</span></span>



| <span data-ttu-id="8ee24-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8ee24-127">Requirement</span></span> | <span data-ttu-id="8ee24-128">Wert</span><span class="sxs-lookup"><span data-stu-id="8ee24-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8ee24-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8ee24-129">Minimum supported client</span></span><br/> | <span data-ttu-id="8ee24-130">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8ee24-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8ee24-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8ee24-131">Minimum supported server</span></span><br/> | <span data-ttu-id="8ee24-132">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8ee24-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8ee24-133">Header</span><span class="sxs-lookup"><span data-stu-id="8ee24-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ee24-134"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ee24-134"><dt>Commctrl.h</dt></span></span> </dl> |



 

