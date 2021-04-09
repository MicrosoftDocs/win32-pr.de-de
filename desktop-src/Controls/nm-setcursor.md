---
title: NM_SETCURSOR Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Steuer Elements, dass das-Steuerelement als Antwort auf eine WM-SetCursor-Nachricht den Cursor festlegt \_ . Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 8d70563f-05a3-4116-b686-6d9063940fae
keywords:
- Windows-Steuerelemente für NM_SETCURSOR Benachrichtigungs
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
ms.openlocfilehash: e6cc3c48a0224efec0c8ab8844a3e7f234a9ba51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103350"
---
# <a name="nm_setcursor-notification-code"></a><span data-ttu-id="49deb-105">NM- \_ SetCursor-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="49deb-105">NM\_SETCURSOR notification code</span></span>

<span data-ttu-id="49deb-106">Benachrichtigt das übergeordnete Fenster eines Steuer Elements, dass das-Steuerelement als Antwort auf eine [**WM- \_ SetCursor**](/windows/desktop/menurc/wm-setcursor) -Nachricht den Cursor festlegt.</span><span class="sxs-lookup"><span data-stu-id="49deb-106">Notifies a control's parent window that the control is setting the cursor in response to a [**WM\_SETCURSOR**](/windows/desktop/menurc/wm-setcursor) message.</span></span> <span data-ttu-id="49deb-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="49deb-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_SETCURSOR

    lpnmm = (LPNMMOUSE) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="49deb-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="49deb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49deb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="49deb-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="49deb-110">Ein Zeiger auf eine [**nmmouse**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) -Struktur, die zusätzliche Informationen zu dieser Benachrichtigung enthält.</span><span class="sxs-lookup"><span data-stu-id="49deb-110">A pointer to an [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49deb-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="49deb-111">Return value</span></span>

<span data-ttu-id="49deb-112">Gibt 0 (null) zurück, damit das Steuerelement den Cursor festlegen kann, um zu verhindern, dass das Steuerelement den Cursor festlegt.</span><span class="sxs-lookup"><span data-stu-id="49deb-112">Return zero to enable the control to set the cursor or nonzero to prevent the control from setting the cursor.</span></span>

## <a name="requirements"></a><span data-ttu-id="49deb-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="49deb-113">Requirements</span></span>



| <span data-ttu-id="49deb-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="49deb-114">Requirement</span></span> | <span data-ttu-id="49deb-115">Wert</span><span class="sxs-lookup"><span data-stu-id="49deb-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="49deb-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="49deb-116">Minimum supported client</span></span><br/> | <span data-ttu-id="49deb-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="49deb-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="49deb-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="49deb-118">Minimum supported server</span></span><br/> | <span data-ttu-id="49deb-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="49deb-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="49deb-120">Header</span><span class="sxs-lookup"><span data-stu-id="49deb-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="49deb-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="49deb-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

