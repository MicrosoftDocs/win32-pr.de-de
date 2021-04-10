---
title: ACN_STOP Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Animations Steuer Elements, dass der zugehörige AVI-Clip beendet wurde. Dieser Benachrichtigungs Code wird in Form einer WM- \_ Befehlsnachricht gesendet.
ms.assetid: 2f21a2ec-975f-4592-8b21-956bd5311ef4
keywords:
- Windows-Steuerelemente für ACN_STOP Benachrichtigungs
topic_type:
- apiref
api_name:
- ACN_STOP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cbdb27677439b7f08b489cba9024d44f3ebee6d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040315"
---
# <a name="acn_stop-notification-code"></a><span data-ttu-id="b6da6-105">ACN- \_ anstoppbenachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="b6da6-105">ACN\_STOP notification code</span></span>

<span data-ttu-id="b6da6-106">Benachrichtigt das übergeordnete Fenster eines Animations Steuer Elements, dass der zugehörige AVI-Clip beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="b6da6-106">Notifies the parent window of an animation control that the associated AVI clip has stopped playing.</span></span> <span data-ttu-id="b6da6-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Befehls**](/windows/desktop/menurc/wm-command) Nachricht gesendet.</span><span class="sxs-lookup"><span data-stu-id="b6da6-107">This notification code is sent in the form of a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
ACN_STOP     

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="b6da6-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b6da6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6da6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b6da6-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b6da6-110">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den Bezeichner des Animations Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="b6da6-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the animation control's identifier.</span></span> <span data-ttu-id="b6da6-111">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Benachrichtigungs Code an.</span><span class="sxs-lookup"><span data-stu-id="b6da6-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="b6da6-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b6da6-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b6da6-113">Ein **HWND** , das das Handle für das Animations Steuerelement angibt.</span><span class="sxs-lookup"><span data-stu-id="b6da6-113">An **HWND** that specifies the handle to the animation control.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b6da6-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b6da6-114">Requirements</span></span>



| <span data-ttu-id="b6da6-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b6da6-115">Requirement</span></span> | <span data-ttu-id="b6da6-116">Wert</span><span class="sxs-lookup"><span data-stu-id="b6da6-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b6da6-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b6da6-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b6da6-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b6da6-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b6da6-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b6da6-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b6da6-120">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b6da6-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b6da6-121">Header</span><span class="sxs-lookup"><span data-stu-id="b6da6-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6da6-122"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6da6-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

