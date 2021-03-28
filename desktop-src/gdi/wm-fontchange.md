---
description: Eine Anwendung sendet nach dem \_ Ändern des Pools der Schriftart Ressourcen die WM-fontchange-Nachricht an alle Fenster der obersten Ebene im System.
ms.assetid: 4774308e-2f18-4a35-a769-56871f3c29a2
title: WM_FONTCHANGE Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3b40650f0077ed854b87a6fd10e1dae610f0c3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980288"
---
# <a name="wm_fontchange-message"></a><span data-ttu-id="1b346-103">WM- \_ fontchange-Meldung</span><span class="sxs-lookup"><span data-stu-id="1b346-103">WM\_FONTCHANGE message</span></span>

<span data-ttu-id="1b346-104">Eine Anwendung sendet nach dem Ändern des Pools der Schriftart Ressourcen die **WM- \_ fontchange** -Nachricht an alle Fenster der obersten Ebene im System.</span><span class="sxs-lookup"><span data-stu-id="1b346-104">An application sends the **WM\_FONTCHANGE** message to all top-level windows in the system after changing the pool of font resources.</span></span>

<span data-ttu-id="1b346-105">Um diese Nachricht zu senden, wenden Sie die [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) -Funktion mit den folgenden Parametern an.</span><span class="sxs-lookup"><span data-stu-id="1b346-105">To send this message, call the [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) function with the following parameters.</span></span>


```C++
SendMessage( 
  (HWND)  hWnd,              
  WM_FONTCHANGE,            
  (WPARAM)  wParam,          
  (LPARAM)  lParam            
);
```



## <a name="parameters"></a><span data-ttu-id="1b346-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1b346-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b346-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1b346-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1b346-108">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="1b346-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1b346-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1b346-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1b346-110">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="1b346-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1b346-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1b346-111">Remarks</span></span>

<span data-ttu-id="1b346-112">Eine Anwendung, die Schriftarten aus dem System hinzufügt oder entfernt (z. b. mithilfe der [**AddFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-addfontresourcea) -Funktion oder der [**removefontresource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea) -Funktion), sollte diese Nachricht an alle Fenster der obersten Ebene senden.</span><span class="sxs-lookup"><span data-stu-id="1b346-112">An application that adds or removes fonts from the system (for example, by using the [**AddFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-addfontresourcea) or [**RemoveFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea) function) should send this message to all top-level windows.</span></span>

<span data-ttu-id="1b346-113">Zum Senden der " **WM \_ fontchange** "-Nachricht an alle Fenster der obersten Ebene kann eine Anwendung die **SendMessage** -Funktion mit dem *HWND* -Parameter aufrufen \_ .</span><span class="sxs-lookup"><span data-stu-id="1b346-113">To send the **WM\_FONTCHANGE** message to all top-level windows, an application can call the **SendMessage** function with the *hwnd* parameter set to HWND\_BROADCAST.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b346-114">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="1b346-114">Requirements</span></span>



| <span data-ttu-id="1b346-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1b346-115">Requirement</span></span> | <span data-ttu-id="1b346-116">Wert</span><span class="sxs-lookup"><span data-stu-id="1b346-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b346-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1b346-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1b346-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1b346-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="1b346-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1b346-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1b346-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1b346-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1b346-121">Header</span><span class="sxs-lookup"><span data-stu-id="1b346-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b346-122"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="1b346-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b346-123">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1b346-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b346-124">Übersicht Überschrift Arten und Text</span><span class="sxs-lookup"><span data-stu-id="1b346-124">Fonts and Text Overview</span></span>](fonts-and-text.md)
</dt> <dt>

[<span data-ttu-id="1b346-125">Schriftart und Text Nachrichten</span><span class="sxs-lookup"><span data-stu-id="1b346-125">Font and Text Messages</span></span>](font-and-text-messages.md)
</dt> <dt>

[<span data-ttu-id="1b346-126">**AddFontResource**</span><span class="sxs-lookup"><span data-stu-id="1b346-126">**AddFontResource**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-addfontresourcea)
</dt> <dt>

[<span data-ttu-id="1b346-127">**Removefontresource**</span><span class="sxs-lookup"><span data-stu-id="1b346-127">**RemoveFontResource**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea)
</dt> </dl>

 

 
