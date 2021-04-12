---
description: Benachrichtigt eine Anwendung, wenn eine IME im Begriff ist, eine Fehlermeldung oder andere Informationen anzuzeigen. Die Anwendung empfängt diesen Befehl über die WM- \_ IME- \_ Benachrichtigungs Meldung mit den Parametereinstellungen, wie unten gezeigt.
ms.assetid: b898283a-af1a-484f-bfb8-e5d5c0ac8ee1
title: IMN_GUIDELINE Benachrichtigungs Code (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4efc222f7bfceadecce0f14573cab66471b119d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104345768"
---
# <a name="imn_guideline-notification-code"></a><span data-ttu-id="c1326-104">\_Benachrichtigungs Code für IMN</span><span class="sxs-lookup"><span data-stu-id="c1326-104">IMN\_GUIDELINE notification code</span></span>

<span data-ttu-id="c1326-105">Benachrichtigt eine Anwendung, wenn eine IME im Begriff ist, eine Fehlermeldung oder andere Informationen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="c1326-105">Notifies an application when an IME is about to show an error message or other information.</span></span> <span data-ttu-id="c1326-106">Die Anwendung empfängt diesen Befehl über die [**WM- \_ IME- \_ Benachrichtigungs**](wm-ime-notify.md) Meldung mit den Parametereinstellungen, wie unten gezeigt.</span><span class="sxs-lookup"><span data-stu-id="c1326-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_GUIDELINE
```



## <a name="parameters"></a><span data-ttu-id="c1326-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c1326-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1326-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="c1326-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="c1326-109">Legen Sie auf IMN- \_ Richtlinie fest.</span><span class="sxs-lookup"><span data-stu-id="c1326-109">Set to IMN\_GUIDELINE.</span></span>

</dd> <dt>

<span data-ttu-id="c1326-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*</span><span class="sxs-lookup"><span data-stu-id="c1326-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="c1326-111">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c1326-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1326-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c1326-112">Return Value</span></span>

<span data-ttu-id="c1326-113">Dieser Befehl weist keinen Rückgabewert auf.</span><span class="sxs-lookup"><span data-stu-id="c1326-113">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1326-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c1326-114">Remarks</span></span>

<span data-ttu-id="c1326-115">Eine Anwendung verarbeitet diesen Befehl durch Aufrufen der Funktion " [**immgetguideline**](/windows/desktop/api/Imm/nf-imm-immgetguidelinea) ", um die Fehlermeldung oder Informationen aus dem IME abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c1326-115">An application processes this command by calling the [**ImmGetGuideLine**](/windows/desktop/api/Imm/nf-imm-immgetguidelinea) function to retrieve the error message or information from the IME.</span></span>

<span data-ttu-id="c1326-116">Das IME-Fenster zeigt die Fehlermeldung oder die Informations Zeichenfolge in einem Informationsfenster an.</span><span class="sxs-lookup"><span data-stu-id="c1326-116">The IME window displays the error message or information string in an information window.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1326-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c1326-117">Requirements</span></span>



| <span data-ttu-id="c1326-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c1326-118">Requirement</span></span> | <span data-ttu-id="c1326-119">Wert</span><span class="sxs-lookup"><span data-stu-id="c1326-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1326-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c1326-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c1326-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c1326-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c1326-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c1326-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c1326-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c1326-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c1326-124">Header</span><span class="sxs-lookup"><span data-stu-id="c1326-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1326-125"><dt>Imm. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c1326-125"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1326-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c1326-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1326-127">Eingabemethoden-Manager</span><span class="sxs-lookup"><span data-stu-id="c1326-127">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="c1326-128">Eingabemethoden-Manager-Befehle</span><span class="sxs-lookup"><span data-stu-id="c1326-128">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="c1326-129">**Immgetrichtrichtwert**</span><span class="sxs-lookup"><span data-stu-id="c1326-129">**ImmGetGuideLine**</span></span>](/windows/desktop/api/Imm/nf-imm-immgetguidelinea)
</dt> <dt>

[<span data-ttu-id="c1326-130">**WM- \_ IME \_ Benachrichtigen**</span><span class="sxs-lookup"><span data-stu-id="c1326-130">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 




