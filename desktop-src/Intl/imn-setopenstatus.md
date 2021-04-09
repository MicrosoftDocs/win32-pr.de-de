---
description: Benachrichtigt eine Anwendung, wenn der Open-Status des Eingabe Kontexts aktualisiert wird. Die Anwendung empfängt diesen Befehl über die WM- \_ IME- \_ Benachrichtigungs Meldung mit den Parametereinstellungen, wie unten gezeigt.
ms.assetid: cc6fa7f4-b85a-486a-985d-53c071321bd1
title: IMN_SETOPENSTATUS Benachrichtigungs Code (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3598d7415cf415de3279e016d81a6d14b767d5da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042238"
---
# <a name="imn_setopenstatus-notification-code"></a><span data-ttu-id="36cea-104">IMN \_ setopsstatus-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="36cea-104">IMN\_SETOPENSTATUS notification code</span></span>

<span data-ttu-id="36cea-105">Benachrichtigt eine Anwendung, wenn der Open-Status des Eingabe Kontexts aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="36cea-105">Notifies an application when the open status of the input context is updated.</span></span> <span data-ttu-id="36cea-106">Die Anwendung empfängt diesen Befehl über die [**WM- \_ IME- \_ Benachrichtigungs**](wm-ime-notify.md) Meldung mit den Parametereinstellungen, wie unten gezeigt.</span><span class="sxs-lookup"><span data-stu-id="36cea-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_SETOPENSTATUS
```



## <a name="parameters"></a><span data-ttu-id="36cea-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="36cea-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36cea-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="36cea-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="36cea-109">Legen Sie auf IMN \_ SetOpenStatus fest.</span><span class="sxs-lookup"><span data-stu-id="36cea-109">Set to IMN\_SETOPENSTATUS.</span></span>

</dd> <dt>

<span data-ttu-id="36cea-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*</span><span class="sxs-lookup"><span data-stu-id="36cea-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="36cea-111">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="36cea-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36cea-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="36cea-112">Return Value</span></span>

<span data-ttu-id="36cea-113">Dieser Befehl weist keinen Rückgabewert auf.</span><span class="sxs-lookup"><span data-stu-id="36cea-113">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="36cea-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="36cea-114">Remarks</span></span>

<span data-ttu-id="36cea-115">Die Anwendung kann Informationen über den offenen Status mithilfe der [**immgetopenstatus**](/windows/desktop/api/Imm/nf-imm-immgetopenstatus) -Funktion erhalten.</span><span class="sxs-lookup"><span data-stu-id="36cea-115">The application can get information about the open status by using the [**ImmGetOpenStatus**](/windows/desktop/api/Imm/nf-imm-immgetopenstatus) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="36cea-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="36cea-116">Requirements</span></span>



| <span data-ttu-id="36cea-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="36cea-117">Requirement</span></span> | <span data-ttu-id="36cea-118">Wert</span><span class="sxs-lookup"><span data-stu-id="36cea-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36cea-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="36cea-119">Minimum supported client</span></span><br/> | <span data-ttu-id="36cea-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="36cea-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="36cea-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="36cea-121">Minimum supported server</span></span><br/> | <span data-ttu-id="36cea-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="36cea-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="36cea-123">Header</span><span class="sxs-lookup"><span data-stu-id="36cea-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="36cea-124"><dt>Imm. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="36cea-124"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36cea-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="36cea-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36cea-126">Eingabemethoden-Manager</span><span class="sxs-lookup"><span data-stu-id="36cea-126">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="36cea-127">Eingabemethoden-Manager-Befehle</span><span class="sxs-lookup"><span data-stu-id="36cea-127">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="36cea-128">**Immgetopenstatus**</span><span class="sxs-lookup"><span data-stu-id="36cea-128">**ImmGetOpenStatus**</span></span>](/windows/desktop/api/Imm/nf-imm-immgetopenstatus)
</dt> <dt>

[<span data-ttu-id="36cea-129">**WM- \_ IME \_ Benachrichtigen**</span><span class="sxs-lookup"><span data-stu-id="36cea-129">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 




