---
description: Gibt eine Anforderung zum Beenden einer Anwendung an und wird generiert, wenn die Anwendung die PostQuitMessage-Funktion aufruft. Diese Meldung bewirkt, dass die getMessage-Funktion 0 zurückgibt.
ms.assetid: a9bff5dc-cab8-4e08-838e-d92c87c265d6
title: WM_QUIT Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8e0d7413d65e9a0fb451fe63504f2ed5be02064
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042289"
---
# <a name="wm_quit-message"></a><span data-ttu-id="7385d-104">WM- \_ beendenmeldung</span><span class="sxs-lookup"><span data-stu-id="7385d-104">WM\_QUIT message</span></span>

<span data-ttu-id="7385d-105">Gibt eine Anforderung zum Beenden einer Anwendung an und wird generiert, wenn die Anwendung die [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) -Funktion aufruft.</span><span class="sxs-lookup"><span data-stu-id="7385d-105">Indicates a request to terminate an application, and is generated when the application calls the [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) function.</span></span> <span data-ttu-id="7385d-106">Diese Meldung bewirkt, dass die [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) -Funktion 0 zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="7385d-106">This message causes the [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) function to return zero.</span></span>


```C++
#define WM_QUIT                         0x0012
```



## <a name="parameters"></a><span data-ttu-id="7385d-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="7385d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7385d-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7385d-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7385d-109">Der Exitcode, der in der [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) -Funktion angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7385d-109">The exit code given in the [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) function.</span></span>

</dd> <dt>

<span data-ttu-id="7385d-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7385d-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7385d-111">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="7385d-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7385d-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7385d-112">Return value</span></span>

<span data-ttu-id="7385d-113">Typ: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="7385d-113">Type: **LRESULT**</span></span>

<span data-ttu-id="7385d-114">Diese Nachricht weist keinen Rückgabewert auf, da Sie bewirkt, dass die Nachrichten Schleife beendet wird, bevor die Nachricht an die Fenster Prozedur der Anwendung gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="7385d-114">This message does not have a return value because it causes the message loop to terminate before the message is sent to the application's window procedure.</span></span>

## <a name="remarks"></a><span data-ttu-id="7385d-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7385d-115">Remarks</span></span>

<span data-ttu-id="7385d-116">Die **WM \_** -beendende Nachricht ist keinem Fenster zugeordnet und wird daher nie durch die Fenster Prozedur eines Fensters empfangen.</span><span class="sxs-lookup"><span data-stu-id="7385d-116">The **WM\_QUIT** message is not associated with a window and therefore will never be received through a window's window procedure.</span></span> <span data-ttu-id="7385d-117">Sie wird nur von den Funktionen [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) oder [**Peer Message**](/windows/win32/api/winuser/nf-winuser-peekmessagea) abgerufen.</span><span class="sxs-lookup"><span data-stu-id="7385d-117">It is retrieved only by the [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) or [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) functions.</span></span>

<span data-ttu-id="7385d-118">Veröffentlichen Sie die **WM- \_** beendende Nachricht nicht mithilfe der [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) -Funktion. verwenden Sie [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage).</span><span class="sxs-lookup"><span data-stu-id="7385d-118">Do not post the **WM\_QUIT** message using the [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) function; use [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage).</span></span>

## <a name="requirements"></a><span data-ttu-id="7385d-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7385d-119">Requirements</span></span>



| <span data-ttu-id="7385d-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7385d-120">Requirement</span></span> | <span data-ttu-id="7385d-121">Wert</span><span class="sxs-lookup"><span data-stu-id="7385d-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7385d-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7385d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7385d-123">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7385d-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="7385d-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7385d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7385d-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7385d-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7385d-126">Header</span><span class="sxs-lookup"><span data-stu-id="7385d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="7385d-127"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="7385d-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7385d-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7385d-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="7385d-129">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="7385d-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7385d-130">**GetMessage**</span><span class="sxs-lookup"><span data-stu-id="7385d-130">**GetMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-getmessage)
</dt> <dt>

[<span data-ttu-id="7385d-131">**PeekMessage**</span><span class="sxs-lookup"><span data-stu-id="7385d-131">**PeekMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-peekmessagea)
</dt> <dt>

[<span data-ttu-id="7385d-132">**PostQuitMessage**</span><span class="sxs-lookup"><span data-stu-id="7385d-132">**PostQuitMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-postquitmessage)
</dt> <dt>

<span data-ttu-id="7385d-133">**Licher**</span><span class="sxs-lookup"><span data-stu-id="7385d-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="7385d-134">Windows</span><span class="sxs-lookup"><span data-stu-id="7385d-134">Windows</span></span>](windows.md)
</dt> </dl>

 

 
