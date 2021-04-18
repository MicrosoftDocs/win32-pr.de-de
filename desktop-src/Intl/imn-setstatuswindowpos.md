---
description: Benachrichtigt eine Anwendung, wenn die Statusfenster Position im Eingabe Kontext aktualisiert wird. Die Anwendung empfängt diesen Befehl über die WM- \_ IME- \_ Benachrichtigungs Meldung mit den Parametereinstellungen wie folgt.
ms.assetid: 15e65aff-67d9-4d1a-a6a7-b921cecb3aec
title: IMN_SETSTATUSWINDOWPOS Benachrichtigungs Code (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91d76a962e9cc509a6f9ffaac900b761b868f960
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106351669"
---
# <a name="imn_setstatuswindowpos-notification-code"></a><span data-ttu-id="b958b-104">IMN \_ SetStatus-WINDOWPOS-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="b958b-104">IMN\_SETSTATUSWINDOWPOS notification code</span></span>

<span data-ttu-id="b958b-105">Benachrichtigt eine Anwendung, wenn die Statusfenster Position im Eingabe Kontext aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="b958b-105">Notifies an application when the status window position in the input context is updated.</span></span> <span data-ttu-id="b958b-106">Die Anwendung empfängt diesen Befehl über die [**WM- \_ IME- \_ Benachrichtigungs**](wm-ime-notify.md) Meldung mit den Parametereinstellungen wie folgt.</span><span class="sxs-lookup"><span data-stu-id="b958b-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as follows.</span></span>


```C++
IMN_SETSTATUSWINDOWPOS
```



## <a name="parameters"></a><span data-ttu-id="b958b-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="b958b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b958b-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="b958b-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="b958b-109">Legen Sie auf IMN \_ SetStatus-WINDOWPOS fest.</span><span class="sxs-lookup"><span data-stu-id="b958b-109">Set to IMN\_SETSTATUSWINDOWPOS.</span></span>

</dd> <dt>

<span data-ttu-id="b958b-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*</span><span class="sxs-lookup"><span data-stu-id="b958b-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="b958b-111">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="b958b-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b958b-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b958b-112">Return Value</span></span>

<span data-ttu-id="b958b-113">Dieser Befehl weist keinen Rückgabewert auf.</span><span class="sxs-lookup"><span data-stu-id="b958b-113">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b958b-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b958b-114">Remarks</span></span>

<span data-ttu-id="b958b-115">Die Anwendung kann Informationen zur Position des Status Fensters mithilfe des Befehls " [**IMC \_ getstatuswindowpos**](imc-getstatuswindowpos.md) " erhalten.</span><span class="sxs-lookup"><span data-stu-id="b958b-115">The application can get information about the status window position by using the [**IMC\_GETSTATUSWINDOWPOS**](imc-getstatuswindowpos.md) command.</span></span>

## <a name="requirements"></a><span data-ttu-id="b958b-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b958b-116">Requirements</span></span>



| <span data-ttu-id="b958b-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b958b-117">Requirement</span></span> | <span data-ttu-id="b958b-118">Wert</span><span class="sxs-lookup"><span data-stu-id="b958b-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b958b-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b958b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b958b-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b958b-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b958b-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b958b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b958b-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b958b-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b958b-123">Header</span><span class="sxs-lookup"><span data-stu-id="b958b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b958b-124"><dt>Imm. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b958b-124"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b958b-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b958b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b958b-126">Eingabemethoden-Manager</span><span class="sxs-lookup"><span data-stu-id="b958b-126">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="b958b-127">Eingabemethoden-Manager-Befehle</span><span class="sxs-lookup"><span data-stu-id="b958b-127">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="b958b-128">**IMC \_ GetStatus-WINDOWPOS**</span><span class="sxs-lookup"><span data-stu-id="b958b-128">**IMC\_GETSTATUSWINDOWPOS**</span></span>](imc-getstatuswindowpos.md)
</dt> <dt>

[<span data-ttu-id="b958b-129">**WM- \_ IME \_ Benachrichtigen**</span><span class="sxs-lookup"><span data-stu-id="b958b-129">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 




