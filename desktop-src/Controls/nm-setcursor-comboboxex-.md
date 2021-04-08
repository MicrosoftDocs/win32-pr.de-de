---
title: NM_SETCURSOR (ComboBoxEx)-Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines ComboBoxEx-Steuer Elements, dass das-Steuerelement den Cursor als Antwort auf eine WM- \_ SetCursor-Nachricht festlegt. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: a1c617fa-8eb2-444f-88d1-9913de7a42d1
keywords:
- NM_SETCURSOR (ComboBoxEx)-Benachrichtigungs Code Windows-Steuerelemente
topic_type:
- apiref
api_name:
- NM_SETCURSOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fbd5e10f06e74af0778521d31c69e63586a6476
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742665"
---
# <a name="nm_setcursor-comboboxex-notification-code"></a><span data-ttu-id="c82fc-105">NM \_ setcursor (ComboBoxEx)-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="c82fc-105">NM\_SETCURSOR (ComboBoxEx) notification code</span></span>

<span data-ttu-id="c82fc-106">Benachrichtigt das übergeordnete Fenster eines ComboBoxEx-Steuer Elements, dass das-Steuerelement den Cursor als Antwort auf eine [**WM- \_ SetCursor**](/windows/desktop/menurc/wm-setcursor) -Nachricht festlegt.</span><span class="sxs-lookup"><span data-stu-id="c82fc-106">Notifies a ComboBoxEx control's parent window that the control is setting the cursor in response to a [**WM\_SETCURSOR**](/windows/desktop/menurc/wm-setcursor) message.</span></span> <span data-ttu-id="c82fc-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="c82fc-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_SETCURSOR

    lpnmm = (LPNMMOUSE) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="c82fc-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c82fc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c82fc-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c82fc-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c82fc-110">Ein Zeiger auf eine [**nmmouse**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) -Struktur, die zusätzliche Informationen zu dieser Benachrichtigung enthält.</span><span class="sxs-lookup"><span data-stu-id="c82fc-110">A pointer to an [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c82fc-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c82fc-111">Return value</span></span>

<span data-ttu-id="c82fc-112">Gibt 0 (null) zurück, damit das Steuerelement den Cursor festlegen kann, um zu verhindern, dass das Steuerelement den Cursor festlegt.</span><span class="sxs-lookup"><span data-stu-id="c82fc-112">Return zero to enable the control to set the cursor or nonzero to prevent the control from setting the cursor.</span></span>

## <a name="requirements"></a><span data-ttu-id="c82fc-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c82fc-113">Requirements</span></span>



| <span data-ttu-id="c82fc-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c82fc-114">Requirement</span></span> | <span data-ttu-id="c82fc-115">Wert</span><span class="sxs-lookup"><span data-stu-id="c82fc-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c82fc-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c82fc-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c82fc-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c82fc-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c82fc-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c82fc-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c82fc-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c82fc-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c82fc-120">Header</span><span class="sxs-lookup"><span data-stu-id="c82fc-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c82fc-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="c82fc-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

