---
title: STN_ENABLE Benachrichtigungs Code (Winuser. h)
description: Der STN- \_ Benachrichtigungs Code aktivieren wird gesendet, wenn ein statisches Steuerelement aktiviert ist.
ms.assetid: daac2ed3-c7cd-46f8-abfa-78754b277ef4
keywords:
- Windows-Steuerelemente für STN_ENABLE Benachrichtigungs
topic_type:
- apiref
api_name:
- STN_ENABLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfc9cc21e884a8a7e907054daa48a21678efa65e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475327"
---
# <a name="stn_enable-notification-code"></a><span data-ttu-id="71e30-104">STN- \_ Benachrichtigungs Code aktivieren</span><span class="sxs-lookup"><span data-stu-id="71e30-104">STN\_ENABLE notification code</span></span>

<span data-ttu-id="71e30-105">Der STN- \_ Benachrichtigungs Code aktivieren wird gesendet, wenn ein statisches Steuerelement aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="71e30-105">The STN\_ENABLE notification code is sent when a static control is enabled.</span></span> <span data-ttu-id="71e30-106">Das statische Steuerelement muss über den SS-Benachrichtigungs Stil verfügen, um diesen Benachrichtigungs Code zu erhalten. [**\_**](static-control-styles.md)</span><span class="sxs-lookup"><span data-stu-id="71e30-106">The static control must have the [**SS\_NOTIFY**](static-control-styles.md) style to receive this notification code.</span></span> <span data-ttu-id="71e30-107">Das übergeordnete Fenster des Steuer Elements empfängt diesen Benachrichtigungs Code über die [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung.</span><span class="sxs-lookup"><span data-stu-id="71e30-107">The parent window of the control receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
STN_ENABLE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="71e30-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="71e30-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71e30-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="71e30-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="71e30-110">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den Bezeichner des statischen Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="71e30-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the static control.</span></span> <span data-ttu-id="71e30-111">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Benachrichtigungs Code an.</span><span class="sxs-lookup"><span data-stu-id="71e30-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="71e30-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="71e30-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="71e30-113">Handle für das statische Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="71e30-113">Handle to the static control.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="71e30-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="71e30-114">Requirements</span></span>



| <span data-ttu-id="71e30-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="71e30-115">Requirement</span></span> | <span data-ttu-id="71e30-116">Wert</span><span class="sxs-lookup"><span data-stu-id="71e30-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71e30-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="71e30-117">Minimum supported client</span></span><br/> | <span data-ttu-id="71e30-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="71e30-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="71e30-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="71e30-119">Minimum supported server</span></span><br/> | <span data-ttu-id="71e30-120">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="71e30-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="71e30-121">Header</span><span class="sxs-lookup"><span data-stu-id="71e30-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="71e30-122"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="71e30-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71e30-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="71e30-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="71e30-124">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="71e30-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="71e30-125">STN \_ Deaktivieren</span><span class="sxs-lookup"><span data-stu-id="71e30-125">STN\_DISABLE</span></span>](stn-disable.md)
</dt> <dt>

<span data-ttu-id="71e30-126">**Licher**</span><span class="sxs-lookup"><span data-stu-id="71e30-126">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="71e30-127">Statische Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="71e30-127">Static Controls</span></span>](static-controls.md)
</dt> <dt>

<span data-ttu-id="71e30-128">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="71e30-128">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="71e30-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="71e30-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="71e30-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="71e30-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="71e30-131">**WM- \_ Befehl**</span><span class="sxs-lookup"><span data-stu-id="71e30-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

