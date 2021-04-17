---
title: WM_POINTERROUTEDTO Meldung
description: Wird gesendet, wenn fortlaufende Zeiger Eingaben für eine vorhandene Zeiger-ID von einem Prozess in einen anderen über den Inhalt, der für prozessübergreifende Verkettung konfiguriert ist (addcontentwithcrossprocesschaining), übertragen werden.
ms.assetid: 163E2C31-4E29-4CBA-B079-1963D4762D7B
keywords:
- Eingabe Meldungen und Benachrichtigungen der WM_POINTERROUTEDTO Nachricht
topic_type:
- apiref
api_name:
- WM_POINTERROUTEDTO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 7658aeef77a0f7e19f2449213e9332b4e60c9450
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391788"
---
# <a name="wm_pointerroutedto-message"></a><span data-ttu-id="1d264-104">WM_POINTERROUTEDTO Meldung</span><span class="sxs-lookup"><span data-stu-id="1d264-104">WM_POINTERROUTEDTO message</span></span>

<span data-ttu-id="1d264-105">Wird gesendet, wenn fortlaufende Zeiger Eingaben für eine vorhandene Zeiger-ID von einem Prozess in einen anderen über den Inhalt, der für prozessübergreifende Verkettung konfiguriert ist ([**addcontentwithcrossprocesschaining**](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining)), übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="1d264-105">Sent when ongoing pointer input, for an existing pointer ID, transitions from one process to another across content configured for cross-process chaining ([**AddContentWithCrossProcessChaining**](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining)).</span></span>

<span data-ttu-id="1d264-106">Diese Meldung wird an den Prozess gesendet, der derzeit keine Zeiger Eingaben empfängt.</span><span class="sxs-lookup"><span data-stu-id="1d264-106">This message is sent to the process not currently receiving pointer input.</span></span>


```C++
#define WM_POINTERROUTEDTO       0x0251
```



## <a name="parameters"></a><span data-ttu-id="1d264-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="1d264-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d264-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1d264-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1d264-109">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="1d264-109">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="1d264-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1d264-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1d264-111">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="1d264-111">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d264-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1d264-112">Return value</span></span>

<span data-ttu-id="1d264-113">NULL</span><span class="sxs-lookup"><span data-stu-id="1d264-113">NULL</span></span>

## <a name="remarks"></a><span data-ttu-id="1d264-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1d264-114">Remarks</span></span>

<span data-ttu-id="1d264-115">Diese Meldung wird nicht gesendet, wenn eine [**WM_POINTERDOWN**](wm-pointerdown.md) Nachricht für eine neue Zeiger-ID in einem anderen Prozess gepostet wird.</span><span class="sxs-lookup"><span data-stu-id="1d264-115">This message is not sent when a [**WM_POINTERDOWN**](wm-pointerdown.md) message is posted for a new pointer ID on a different process.</span></span>

<span data-ttu-id="1d264-116">Eine [**WM_POINTERDOWN**](wm-pointerdown.md) Meldung wird nicht gesendet, wenn zuerst eine **WM_POINTERROUTEDTO** Meldung gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="1d264-116">A [**WM_POINTERDOWN**](wm-pointerdown.md) message is not sent if a **WM_POINTERROUTEDTO** message is posted first.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d264-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1d264-117">Requirements</span></span>



| <span data-ttu-id="1d264-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1d264-118">Requirement</span></span> | <span data-ttu-id="1d264-119">Wert</span><span class="sxs-lookup"><span data-stu-id="1d264-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d264-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1d264-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1d264-121">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1d264-121">Windows 10 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1d264-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1d264-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1d264-123">Nur Windows Server 2016 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1d264-123">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1d264-124">Header</span><span class="sxs-lookup"><span data-stu-id="1d264-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d264-125"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="1d264-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d264-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1d264-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d264-127">Meldungen</span><span class="sxs-lookup"><span data-stu-id="1d264-127">Messages</span></span>](messages.md)
</dt> <dt>

[<span data-ttu-id="1d264-128">**WM_POINTERROUTEDAWAY**</span><span class="sxs-lookup"><span data-stu-id="1d264-128">**WM_POINTERROUTEDAWAY**</span></span>](wm-pointerroutedaway.md)
</dt> </dl>

 

