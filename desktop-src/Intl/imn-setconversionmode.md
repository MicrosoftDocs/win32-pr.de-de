---
description: Benachrichtigt eine Anwendung, wenn der Konvertierungsmodus des Eingabe Kontexts aktualisiert wird. Die Anwendung empfängt diesen Befehl über die WM- \_ IME- \_ Benachrichtigungs Meldung mit den Parametereinstellungen, wie unten gezeigt.
ms.assetid: 62bb9717-cc41-4e34-af1a-ff41324bd3a9
title: IMN_SETCONVERSIONMODE Benachrichtigungs Code (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52c0ba945b9988ddb32d86c2005ec240c16f82ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352664"
---
# <a name="imn_setconversionmode-notification-code"></a><span data-ttu-id="f8850-104">IMN \_ setcoversionmode-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="f8850-104">IMN\_SETCONVERSIONMODE notification code</span></span>

<span data-ttu-id="f8850-105">Benachrichtigt eine Anwendung, wenn der Konvertierungsmodus des Eingabe Kontexts aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="f8850-105">Notifies an application when the conversion mode of the input context is updated.</span></span> <span data-ttu-id="f8850-106">Die Anwendung empfängt diesen Befehl über die [**WM- \_ IME- \_ Benachrichtigungs**](wm-ime-notify.md) Meldung mit den Parametereinstellungen, wie unten gezeigt.</span><span class="sxs-lookup"><span data-stu-id="f8850-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_SETCONVERSIONMODE
```



## <a name="parameters"></a><span data-ttu-id="f8850-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="f8850-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8850-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="f8850-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="f8850-109">Legen Sie diese Einstellung auf IMN \_ SetConfiguration-Mode fest.</span><span class="sxs-lookup"><span data-stu-id="f8850-109">Set to IMN\_SETCONVERSIONMODE.</span></span>

</dd> <dt>

<span data-ttu-id="f8850-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*</span><span class="sxs-lookup"><span data-stu-id="f8850-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="f8850-111">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="f8850-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8850-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f8850-112">Return Value</span></span>

<span data-ttu-id="f8850-113">Dieser Befehl weist keinen Rückgabewert auf.</span><span class="sxs-lookup"><span data-stu-id="f8850-113">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8850-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f8850-114">Remarks</span></span>

<span data-ttu-id="f8850-115">Die Anwendung kann Informationen über den Konvertierungsmodus mithilfe der [**immgetkonversionstatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) -Funktion erhalten.</span><span class="sxs-lookup"><span data-stu-id="f8850-115">The application can get information about the conversion mode by using the [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8850-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f8850-116">Requirements</span></span>



| <span data-ttu-id="f8850-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f8850-117">Requirement</span></span> | <span data-ttu-id="f8850-118">Wert</span><span class="sxs-lookup"><span data-stu-id="f8850-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8850-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f8850-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f8850-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f8850-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f8850-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f8850-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f8850-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f8850-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f8850-123">Header</span><span class="sxs-lookup"><span data-stu-id="f8850-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8850-124"><dt>Imm. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f8850-124"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8850-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f8850-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8850-126">Eingabemethoden-Manager</span><span class="sxs-lookup"><span data-stu-id="f8850-126">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="f8850-127">Eingabemethoden-Manager-Befehle</span><span class="sxs-lookup"><span data-stu-id="f8850-127">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="f8850-128">**Immgetsystemversionstatus**</span><span class="sxs-lookup"><span data-stu-id="f8850-128">**ImmGetConversionStatus**</span></span>](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus)
</dt> <dt>

[<span data-ttu-id="f8850-129">**WM- \_ IME \_ Benachrichtigen**</span><span class="sxs-lookup"><span data-stu-id="f8850-129">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 




