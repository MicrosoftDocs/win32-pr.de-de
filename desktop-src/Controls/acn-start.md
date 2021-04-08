---
title: ACN_START Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Animations Steuer Elements, dass der zugehörige AVI-Clip mit der Wiedergabe begonnen hat. Dieser Benachrichtigungs Code wird in Form einer WM- \_ Befehlsnachricht gesendet.
ms.assetid: b4d12225-36f7-4f87-b58a-dac091d14e4c
keywords:
- Windows-Steuerelemente für ACN_START Benachrichtigungs
topic_type:
- apiref
api_name:
- ACN_START
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b0354d8b2b41ea8690be47e70cbc577c064e579
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740520"
---
# <a name="acn_start-notification-code"></a><span data-ttu-id="cf13d-105">ACN- \_ Start Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="cf13d-105">ACN\_START notification code</span></span>

<span data-ttu-id="cf13d-106">Benachrichtigt das übergeordnete Fenster eines Animations Steuer Elements, dass der zugehörige AVI-Clip mit der Wiedergabe begonnen hat.</span><span class="sxs-lookup"><span data-stu-id="cf13d-106">Notifies an animation control's parent window that the associated AVI clip has started playing.</span></span> <span data-ttu-id="cf13d-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Befehls**](/windows/desktop/menurc/wm-command) Nachricht gesendet.</span><span class="sxs-lookup"><span data-stu-id="cf13d-107">This notification code is sent in the form of a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
ACN_START 

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="cf13d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="cf13d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf13d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cf13d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cf13d-110">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den Bezeichner des Animations Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="cf13d-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the animation control's identifier.</span></span> <span data-ttu-id="cf13d-111">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Benachrichtigungs Code an.</span><span class="sxs-lookup"><span data-stu-id="cf13d-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="cf13d-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cf13d-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cf13d-113">Ein **HWND** , das das Handle für das Animations Steuerelement angibt.</span><span class="sxs-lookup"><span data-stu-id="cf13d-113">An **HWND** that specifies the handle to the animation control.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cf13d-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cf13d-114">Requirements</span></span>



| <span data-ttu-id="cf13d-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cf13d-115">Requirement</span></span> | <span data-ttu-id="cf13d-116">Wert</span><span class="sxs-lookup"><span data-stu-id="cf13d-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cf13d-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cf13d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cf13d-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cf13d-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cf13d-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cf13d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cf13d-120">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cf13d-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cf13d-121">Header</span><span class="sxs-lookup"><span data-stu-id="cf13d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf13d-122"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf13d-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

