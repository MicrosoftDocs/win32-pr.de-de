---
title: WM_DWMWINDOWMAXIMIZEDCHANGE Meldung (Winuser. h)
description: Wird gesendet, wenn ein aus Desktopfenster-Manager (DWM) zusammengesetztes Fenster maximiert ist.
ms.assetid: db8cd104-388e-4211-9e4e-f169aef9651c
keywords:
- WM_DWMWINDOWMAXIMIZEDCHANGE Meldung Desktopfenster-Manager
topic_type:
- apiref
api_name:
- WM_DWMWINDOWMAXIMIZEDCHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dc49af267ea826eb9e35a627e14f6fc8b381df0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391949"
---
# <a name="wm_dwmwindowmaximizedchange-message"></a><span data-ttu-id="7ed62-104">WM \_ dwmwindowmaximizedchange-Meldung</span><span class="sxs-lookup"><span data-stu-id="7ed62-104">WM\_DWMWINDOWMAXIMIZEDCHANGE message</span></span>

<span data-ttu-id="7ed62-105">Wird gesendet, wenn ein aus Desktopfenster-Manager (DWM) zusammengesetztes Fenster maximiert ist.</span><span class="sxs-lookup"><span data-stu-id="7ed62-105">Sent when a Desktop Window Manager (DWM) composed window is maximized.</span></span>

## <a name="parameters"></a><span data-ttu-id="7ed62-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7ed62-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ed62-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7ed62-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7ed62-108">Legen Sie diese Einstellung auf "true" fest, um anzugeben, dass das Fenster maximiert ist.</span><span class="sxs-lookup"><span data-stu-id="7ed62-108">Set to true to specify that the window has been maximized.</span></span>

</dd> <dt>

<span data-ttu-id="7ed62-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7ed62-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7ed62-110">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="7ed62-110">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ed62-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7ed62-111">Return value</span></span>

<span data-ttu-id="7ed62-112">Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="7ed62-112">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ed62-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7ed62-113">Remarks</span></span>

<span data-ttu-id="7ed62-114">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="7ed62-114">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ed62-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7ed62-115">Requirements</span></span>



| <span data-ttu-id="7ed62-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7ed62-116">Requirement</span></span> | <span data-ttu-id="7ed62-117">Wert</span><span class="sxs-lookup"><span data-stu-id="7ed62-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7ed62-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7ed62-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7ed62-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7ed62-119">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="7ed62-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7ed62-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7ed62-121">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7ed62-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="7ed62-122">Header</span><span class="sxs-lookup"><span data-stu-id="7ed62-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ed62-123"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ed62-123"><dt>Winuser.h</dt></span></span> </dl> |



 

