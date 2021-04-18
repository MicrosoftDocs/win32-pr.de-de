---
title: WM_DWMCOMPOSITIONCHANGED Meldung (Winuser. h)
description: Informiert alle Fenster der obersten Ebene darüber, dass die Desktopfenster-Manager-Komposition (DWM) aktiviert oder deaktiviert wurde.
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowmessages\wm_dwmcompositionchanged.htm
keywords:
- WM_DWMCOMPOSITIONCHANGED Meldung Desktopfenster-Manager
topic_type:
- apiref
api_name:
- WM_DWMCOMPOSITIONCHANGED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ec25f740e1a5d002edec2c1faeaaf068190583c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339971"
---
# <a name="wm_dwmcompositionchanged-message"></a><span data-ttu-id="0e8c5-104">WM \_ dwmcompositionchanged-Meldung</span><span class="sxs-lookup"><span data-stu-id="0e8c5-104">WM\_DWMCOMPOSITIONCHANGED message</span></span>

<span data-ttu-id="0e8c5-105">Informiert alle Fenster der obersten Ebene darüber, dass die Desktopfenster-Manager-Komposition (DWM) aktiviert oder deaktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="0e8c5-105">Informs all top-level windows that Desktop Window Manager (DWM) composition has been enabled or disabled.</span></span>

> [!Note]  
> <span data-ttu-id="0e8c5-106">Ab Windows 8 ist die DWM-Komposition immer aktiviert, sodass diese Nachricht unabhängig von den videomodusänderungen nicht gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="0e8c5-106">As of Windows 8, DWM composition is always enabled, so this message is not sent regardless of video mode changes.</span></span>

 

## <a name="parameters"></a><span data-ttu-id="0e8c5-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="0e8c5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e8c5-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0e8c5-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0e8c5-109">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="0e8c5-109">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="0e8c5-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0e8c5-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0e8c5-111">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="0e8c5-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e8c5-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0e8c5-112">Return value</span></span>

<span data-ttu-id="0e8c5-113">Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="0e8c5-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e8c5-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0e8c5-114">Remarks</span></span>

<span data-ttu-id="0e8c5-115">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="0e8c5-115">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

<span data-ttu-id="0e8c5-116">Die [**dwmiscompositionaktivierte**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmiscompositionenabled) -Funktion kann verwendet werden, um den aktuellen Kompositions Status zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="0e8c5-116">The [**DwmIsCompositionEnabled**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmiscompositionenabled) function can be used to determine the current composition state.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e8c5-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0e8c5-117">Requirements</span></span>



| <span data-ttu-id="0e8c5-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0e8c5-118">Requirement</span></span> | <span data-ttu-id="0e8c5-119">Wert</span><span class="sxs-lookup"><span data-stu-id="0e8c5-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0e8c5-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0e8c5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0e8c5-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0e8c5-121">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="0e8c5-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0e8c5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0e8c5-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0e8c5-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="0e8c5-124">Header</span><span class="sxs-lookup"><span data-stu-id="0e8c5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e8c5-125"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e8c5-125"><dt>Winuser.h</dt></span></span> </dl> |



 

