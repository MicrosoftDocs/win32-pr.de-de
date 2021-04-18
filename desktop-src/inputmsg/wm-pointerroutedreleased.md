---
title: WM_POINTERROUTEDRELEASED Meldung
description: Wird an alle Prozesse gesendet (für die prozessübergreifende Verkettung durch addcontentwithcrossprocesschaining konfiguriert und ist zurzeit keine Zeiger Eingabe), wenn eine WM_POINTERUP Nachricht im aktuellen Prozess empfangen wird.
ms.assetid: B031ED80-6F1B-42A7-B4E2-55934E2C456C
keywords:
- Eingabe Meldungen und Benachrichtigungen der WM_POINTERROUTEDRELEASED Nachricht
topic_type:
- apiref
api_name:
- WM_POINTERROUTEDRELEASED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 8e24a0df1a2bbdf2b0a9df97057686aa6045eff8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391925"
---
# <a name="wm_pointerroutedreleased-message"></a><span data-ttu-id="bc0be-104">WM_POINTERROUTEDRELEASED Meldung</span><span class="sxs-lookup"><span data-stu-id="bc0be-104">WM_POINTERROUTEDRELEASED message</span></span>

<span data-ttu-id="bc0be-105">Wird an alle Prozesse gesendet (für die prozessübergreifende Verkettung durch [**addcontentwithcrossprocesschaining**](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining) konfiguriert und ist zurzeit keine Zeiger Eingabe), wenn eine [**WM_POINTERUP**](wm-pointerup.md) Nachricht im aktuellen Prozess empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="bc0be-105">Sent to all processes (configured for cross-process chaining through [**AddContentWithCrossProcessChaining**](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining) and not currently handling pointer input) ever associated with a specific pointer ID, when a [**WM_POINTERUP**](wm-pointerup.md) message is received on the current process.</span></span>


```C++
#define WM_POINTERROUTEDRELEASED       0x0253
```



## <a name="parameters"></a><span data-ttu-id="bc0be-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bc0be-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc0be-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bc0be-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bc0be-108">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="bc0be-108">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="bc0be-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bc0be-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bc0be-110">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="bc0be-110">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc0be-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bc0be-111">Return value</span></span>

<span data-ttu-id="bc0be-112">NULL</span><span class="sxs-lookup"><span data-stu-id="bc0be-112">NULL</span></span>

## <a name="requirements"></a><span data-ttu-id="bc0be-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bc0be-113">Requirements</span></span>



| <span data-ttu-id="bc0be-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bc0be-114">Requirement</span></span> | <span data-ttu-id="bc0be-115">Wert</span><span class="sxs-lookup"><span data-stu-id="bc0be-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc0be-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bc0be-116">Minimum supported client</span></span><br/> | <span data-ttu-id="bc0be-117">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bc0be-117">Windows 10 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="bc0be-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bc0be-118">Minimum supported server</span></span><br/> | <span data-ttu-id="bc0be-119">Nur Windows Server 2016 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bc0be-119">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="bc0be-120">Header</span><span class="sxs-lookup"><span data-stu-id="bc0be-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc0be-121"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="bc0be-121"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc0be-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bc0be-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc0be-123">Meldungen</span><span class="sxs-lookup"><span data-stu-id="bc0be-123">Messages</span></span>](messages.md)
</dt> </dl>

 

