---
description: Führt keinen Vorgang aus. Eine Anwendung sendet die WM- \_ null-Nachricht, wenn Sie eine Nachricht veröffentlichen möchte, die vom Empfänger Fenster ignoriert wird.
ms.assetid: edbcfba6-7b79-4d53-84e3-2e4227e17369
title: WM_NULL Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b445e13200bdeb2947e4d8fd363a1a39f0c86db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104216043"
---
# <a name="wm_null-message"></a><span data-ttu-id="8739c-104">WM- \_ null Meldung</span><span class="sxs-lookup"><span data-stu-id="8739c-104">WM\_NULL message</span></span>

<span data-ttu-id="8739c-105">Führt keinen Vorgang aus.</span><span class="sxs-lookup"><span data-stu-id="8739c-105">Performs no operation.</span></span> <span data-ttu-id="8739c-106">Eine Anwendung sendet die **WM- \_ null** -Nachricht, wenn Sie eine Nachricht veröffentlichen möchte, die vom Empfänger Fenster ignoriert wird.</span><span class="sxs-lookup"><span data-stu-id="8739c-106">An application sends the **WM\_NULL** message if it wants to post a message that the recipient window will ignore.</span></span>

<span data-ttu-id="8739c-107">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="8739c-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NULL                         0x0000
```



## <a name="parameters"></a><span data-ttu-id="8739c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8739c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8739c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8739c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8739c-110">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="8739c-110">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8739c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8739c-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8739c-112">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="8739c-112">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8739c-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8739c-113">Return value</span></span>

<span data-ttu-id="8739c-114">Typ: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="8739c-114">Type: **LRESULT**</span></span>

<span data-ttu-id="8739c-115">Eine Anwendung gibt 0 (null) zurück, wenn Sie diese Nachricht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="8739c-115">An application returns zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="8739c-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8739c-116">Remarks</span></span>

<span data-ttu-id="8739c-117">Wenn eine Anwendung z. b. einen " **WH \_ GetMessage** "-Hook installiert hat und verhindern möchte, dass eine Nachricht verarbeitet wird, kann die [**getmsgproc**](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85)) -Rückruffunktion die Nachrichtennummer in **WM \_ null** ändern, sodass der Empfänger Sie ignoriert.</span><span class="sxs-lookup"><span data-stu-id="8739c-117">For example, if an application has installed a **WH\_GETMESSAGE** hook and wants to prevent a message from being processed, the [**GetMsgProc**](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85)) callback function can change the message number to **WM\_NULL** so the recipient will ignore it.</span></span>

<span data-ttu-id="8739c-118">Ein weiteres Beispiel ist, dass eine Anwendung überprüfen kann, ob ein Fenster auf Nachrichten reagiert, indem die **WM- \_ null** -Nachricht mit der [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) -Funktion gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="8739c-118">As another example, an application can check if a window is responding to messages by sending the **WM\_NULL** message with the [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="8739c-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8739c-119">Requirements</span></span>



| <span data-ttu-id="8739c-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8739c-120">Requirement</span></span> | <span data-ttu-id="8739c-121">Wert</span><span class="sxs-lookup"><span data-stu-id="8739c-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8739c-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8739c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8739c-123">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8739c-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="8739c-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8739c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8739c-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8739c-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8739c-126">Header</span><span class="sxs-lookup"><span data-stu-id="8739c-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="8739c-127"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="8739c-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8739c-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8739c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8739c-129">Übersicht über Windows</span><span class="sxs-lookup"><span data-stu-id="8739c-129">Windows Overview</span></span>](windows.md)
</dt> </dl>

 

 
