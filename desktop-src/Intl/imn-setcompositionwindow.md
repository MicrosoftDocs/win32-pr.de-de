---
description: Benachrichtigt eine Anwendung, wenn der Stil oder die Position des Kompositions Fensters aktualisiert wird. Die Anwendung empfängt diesen Befehl über die WM- \_ IME- \_ Benachrichtigungs Meldung mit den Parametereinstellungen, wie unten gezeigt.
ms.assetid: 07a9f0f6-587e-47c6-8f18-b48bdab0a541
title: IMN_SETCOMPOSITIONWINDOW Benachrichtigungs Code (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55a1a4e989fb36049168359f86f85ee7a58103a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960566"
---
# <a name="imn_setcompositionwindow-notification-code"></a><span data-ttu-id="d2282-104">IMN \_ setcompositionwindow-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="d2282-104">IMN\_SETCOMPOSITIONWINDOW notification code</span></span>

<span data-ttu-id="d2282-105">Benachrichtigt eine Anwendung, wenn der Stil oder die Position des Kompositions Fensters aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="d2282-105">Notifies an application when the style or position of the composition window is updated.</span></span> <span data-ttu-id="d2282-106">Die Anwendung empfängt diesen Befehl über die [**WM- \_ IME- \_ Benachrichtigungs**](wm-ime-notify.md) Meldung mit den Parametereinstellungen, wie unten gezeigt.</span><span class="sxs-lookup"><span data-stu-id="d2282-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_SETCOMPOSITIONWINDOW
```



## <a name="parameters"></a><span data-ttu-id="d2282-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="d2282-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2282-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="d2282-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="d2282-109">Legen Sie auf IMN \_ setcompositionwindow fest.</span><span class="sxs-lookup"><span data-stu-id="d2282-109">Set to IMN\_SETCOMPOSITIONWINDOW.</span></span>

</dd> <dt>

<span data-ttu-id="d2282-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*</span><span class="sxs-lookup"><span data-stu-id="d2282-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="d2282-111">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d2282-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2282-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d2282-112">Return Value</span></span>

<span data-ttu-id="d2282-113">Dieser Befehl weist keinen Rückgabewert auf.</span><span class="sxs-lookup"><span data-stu-id="d2282-113">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2282-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d2282-114">Remarks</span></span>

<span data-ttu-id="d2282-115">Die Anwendung kann Informationen über das Kompositions Formular mit dem Befehl " [**\_ getcompositionwindow**](imc-getcompositionwindow.md) " von "IMC" erhalten.</span><span class="sxs-lookup"><span data-stu-id="d2282-115">The application can get information about the composition form by using the [**IMC\_GETCOMPOSITIONWINDOW**](imc-getcompositionwindow.md) command.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2282-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d2282-116">Requirements</span></span>



| <span data-ttu-id="d2282-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d2282-117">Requirement</span></span> | <span data-ttu-id="d2282-118">Wert</span><span class="sxs-lookup"><span data-stu-id="d2282-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2282-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d2282-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d2282-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d2282-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d2282-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d2282-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d2282-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d2282-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d2282-123">Header</span><span class="sxs-lookup"><span data-stu-id="d2282-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2282-124"><dt>Imm. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d2282-124"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2282-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d2282-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2282-126">Eingabemethoden-Manager</span><span class="sxs-lookup"><span data-stu-id="d2282-126">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="d2282-127">Eingabemethoden-Manager-Befehle</span><span class="sxs-lookup"><span data-stu-id="d2282-127">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="d2282-128">**IMC \_ getcompositionwindow**</span><span class="sxs-lookup"><span data-stu-id="d2282-128">**IMC\_GETCOMPOSITIONWINDOW**</span></span>](imc-getcompositionwindow.md)
</dt> <dt>

[<span data-ttu-id="d2282-129">**WM- \_ IME \_ Benachrichtigen**</span><span class="sxs-lookup"><span data-stu-id="d2282-129">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 




