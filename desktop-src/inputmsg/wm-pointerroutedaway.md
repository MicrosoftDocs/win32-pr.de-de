---
title: WM_POINTERROUTEDAWAY Meldung
description: Tritt für den Prozess auf, der Eingaben empfängt, wenn die Zeiger Eingabe an einen anderen Prozess weitergeleitet wird. Addcontentwithcrossprocesschaining).
ms.assetid: 06F8152C-0DA0-4820-835E-07AD35B24310
keywords:
- Eingabe Meldungen und Benachrichtigungen der WM_POINTERROUTEDAWAY Nachricht
topic_type:
- apiref
api_name:
- WM_POINTERROUTEDAWAY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 3c099c02338aa70817d75717064e0b99ac13c96b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040775"
---
# <a name="wm_pointerroutedaway-message"></a><span data-ttu-id="fea16-104">WM_POINTERROUTEDAWAY Meldung</span><span class="sxs-lookup"><span data-stu-id="fea16-104">WM_POINTERROUTEDAWAY message</span></span>

<span data-ttu-id="fea16-105">Tritt für den Prozess auf, der Eingaben empfängt, wenn die Zeiger Eingabe an einen anderen Prozess weitergeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="fea16-105">Occurs on the process receiving input when the pointer input is routed to another process.</span></span>

<span data-ttu-id="fea16-106">Wird gesendet, wenn die Zeiger Eingabe von einem Prozess in einen anderen über Inhalt übergeht, der für prozessübergreifende Verkettung konfiguriert ist ([**addcontentwithcrossprocesschaining**](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining)).</span><span class="sxs-lookup"><span data-stu-id="fea16-106">Sent when pointer input transitions from one process to another across content configured for cross-process chaining ([**AddContentWithCrossProcessChaining**](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining)).</span></span>

<span data-ttu-id="fea16-107">Diese Meldung wird an den Prozess gesendet, der derzeit Zeiger Eingaben empfängt.</span><span class="sxs-lookup"><span data-stu-id="fea16-107">This message is sent to the process currently receiving pointer input.</span></span>


```C++
#define WM_POINTERROUTEDAWAY       0x0252
```



## <a name="parameters"></a><span data-ttu-id="fea16-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="fea16-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fea16-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fea16-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fea16-110">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="fea16-110">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="fea16-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fea16-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fea16-112">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="fea16-112">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fea16-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fea16-113">Return value</span></span>

<span data-ttu-id="fea16-114">NULL</span><span class="sxs-lookup"><span data-stu-id="fea16-114">NULL</span></span>

## <a name="remarks"></a><span data-ttu-id="fea16-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fea16-115">Remarks</span></span>

<span data-ttu-id="fea16-116">Diese Meldung wird nicht mit einer [**WM_POINTERUP**](wm-pointerup.md) Nachricht oder einer [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md) Nachricht gesendet.</span><span class="sxs-lookup"><span data-stu-id="fea16-116">This message is not sent with either a [**WM_POINTERUP**](wm-pointerup.md) message or a [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="fea16-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fea16-117">Requirements</span></span>



| <span data-ttu-id="fea16-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fea16-118">Requirement</span></span> | <span data-ttu-id="fea16-119">Wert</span><span class="sxs-lookup"><span data-stu-id="fea16-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fea16-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fea16-120">Minimum supported client</span></span><br/> | <span data-ttu-id="fea16-121">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fea16-121">Windows 10 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="fea16-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fea16-122">Minimum supported server</span></span><br/> | <span data-ttu-id="fea16-123">Nur Windows Server 2016 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fea16-123">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fea16-124">Header</span><span class="sxs-lookup"><span data-stu-id="fea16-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="fea16-125"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="fea16-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fea16-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fea16-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fea16-127">Meldungen</span><span class="sxs-lookup"><span data-stu-id="fea16-127">Messages</span></span>](messages.md)
</dt> <dt>

[<span data-ttu-id="fea16-128">**WM_POINTERROUTEDTO**</span><span class="sxs-lookup"><span data-stu-id="fea16-128">**WM_POINTERROUTEDTO**</span></span>](wm-pointerroutedto.md)
</dt> </dl>

 

