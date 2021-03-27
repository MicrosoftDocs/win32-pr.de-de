---
description: Die WM \_ -devmodechange-Meldung wird immer dann an alle Fenster der obersten Ebene gesendet, wenn der Benutzer die Geräte Modus-Einstellungen ändert.
ms.assetid: 06b625a8-7584-4a98-b8e7-f1de668c274e
title: WM_DEVMODECHANGE Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 068e74264a7492bbb1e685fe6de110e909698374
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980289"
---
# <a name="wm_devmodechange-message"></a><span data-ttu-id="fe54e-103">WM \_ devmodechange-Meldung</span><span class="sxs-lookup"><span data-stu-id="fe54e-103">WM\_DEVMODECHANGE message</span></span>

<span data-ttu-id="fe54e-104">Die **WM- \_ devmodechange** -Meldung wird immer dann an alle Fenster der obersten Ebene gesendet, wenn der Benutzer die Geräte Modus-Einstellungen ändert.</span><span class="sxs-lookup"><span data-stu-id="fe54e-104">The **WM\_DEVMODECHANGE** message is sent to all top-level windows whenever the user changes device-mode settings.</span></span>

<span data-ttu-id="fe54e-105">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="fe54e-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="fe54e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fe54e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe54e-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="fe54e-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="fe54e-108">Das Fensterhandle</span><span class="sxs-lookup"><span data-stu-id="fe54e-108">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="fe54e-109">*Umschlag*</span><span class="sxs-lookup"><span data-stu-id="fe54e-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="fe54e-110">WM \_ devmodechange</span><span class="sxs-lookup"><span data-stu-id="fe54e-110">WM\_DEVMODECHANGE</span></span>

</dd> <dt>

<span data-ttu-id="fe54e-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fe54e-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fe54e-112">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="fe54e-112">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="fe54e-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fe54e-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fe54e-114">Ein Zeiger auf eine Zeichenfolge, die den Gerätenamen angibt.</span><span class="sxs-lookup"><span data-stu-id="fe54e-114">A pointer to a string that specifies the device name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe54e-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fe54e-115">Return value</span></span>

<span data-ttu-id="fe54e-116">Eine Anwendung sollte NULL zurückgeben, wenn Sie diese Nachricht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="fe54e-116">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe54e-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fe54e-117">Remarks</span></span>

<span data-ttu-id="fe54e-118">Diese Nachricht kann nicht direkt an ein Fenster gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="fe54e-118">This message cannot be sent directly to a window.</span></span> <span data-ttu-id="fe54e-119">Um die **WM- \_ devmodechange** -Nachricht an alle Fenster der obersten Ebene zu senden, verwenden Sie die [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) -Funktion mit dem *HWND* -Parameter, der auf HWND-Broadcast festgelegt ist \_ .</span><span class="sxs-lookup"><span data-stu-id="fe54e-119">To send the **WM\_DEVMODECHANGE** message to all top-level windows, use the [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) function with the *hWnd* parameter set to HWND\_BROADCAST.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe54e-120">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="fe54e-120">Requirements</span></span>



| <span data-ttu-id="fe54e-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fe54e-121">Requirement</span></span> | <span data-ttu-id="fe54e-122">Wert</span><span class="sxs-lookup"><span data-stu-id="fe54e-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe54e-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fe54e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="fe54e-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fe54e-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="fe54e-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fe54e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="fe54e-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fe54e-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fe54e-127">Header</span><span class="sxs-lookup"><span data-stu-id="fe54e-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe54e-128"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="fe54e-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe54e-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="fe54e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe54e-130">Übersicht über Geräte Kontexte</span><span class="sxs-lookup"><span data-stu-id="fe54e-130">Device Contexts Overview</span></span>](device-contexts.md)
</dt> <dt>

[<span data-ttu-id="fe54e-131">Gerätekontext Meldungen</span><span class="sxs-lookup"><span data-stu-id="fe54e-131">Device Context Messages</span></span>](device-context-messages.md)
</dt> </dl>

 

 
