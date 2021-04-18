---
description: Eine Anwendung sendet die WM- \_ mumgeleitet freshmenu-Meldung an ein MDI-Client Fenster (Multiple Document Interface), um das Fenstermenü des MDI-Rahmen Fensters zu aktualisieren.
ms.assetid: 6450d84a-a0b9-45d0-9e0c-757d26502059
title: WM_MDIREFRESHMENU Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4eafa7b84dc9389e57d379a30019505e85fb602
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357766"
---
# <a name="wm_mdirefreshmenu-message"></a><span data-ttu-id="58cb3-103">WM- \_ mumgeleitet freshmenu-Meldung</span><span class="sxs-lookup"><span data-stu-id="58cb3-103">WM\_MDIREFRESHMENU message</span></span>

<span data-ttu-id="58cb3-104">Eine Anwendung sendet die **WM- \_ mumgeleitet freshmenu** -Meldung an ein MDI-Client Fenster (Multiple Document Interface), um das Fenstermenü des MDI-Rahmen Fensters zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="58cb3-104">An application sends the **WM\_MDIREFRESHMENU** message to a multiple-document interface (MDI) client window to refresh the window menu of the MDI frame window.</span></span>


```C++
#define WM_MDIREFRESHMENU               0x0234
```



## <a name="parameters"></a><span data-ttu-id="58cb3-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="58cb3-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58cb3-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="58cb3-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="58cb3-107">Dieser Parameter wird nicht verwendet und muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="58cb3-107">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="58cb3-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="58cb3-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="58cb3-109">Dieser Parameter wird nicht verwendet und muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="58cb3-109">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58cb3-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="58cb3-110">Return value</span></span>

<span data-ttu-id="58cb3-111">Typ: **HMENU**</span><span class="sxs-lookup"><span data-stu-id="58cb3-111">Type: **HMENU**</span></span>

<span data-ttu-id="58cb3-112">Wenn die Nachricht erfolgreich ist, ist der Rückgabewert das Handle für das Rahmen Fenstermenü.</span><span class="sxs-lookup"><span data-stu-id="58cb3-112">If the message succeeds, the return value is the handle to the frame window menu.</span></span>

<span data-ttu-id="58cb3-113">Wenn die Meldung fehlschlägt, ist der Rückgabewert **null**.</span><span class="sxs-lookup"><span data-stu-id="58cb3-113">If the message fails, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="58cb3-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="58cb3-114">Remarks</span></span>

<span data-ttu-id="58cb3-115">Nach dem Senden dieser Nachricht muss eine Anwendung die [**DrawMenuBar**](/windows/win32/api/winuser/nf-winuser-drawmenubar) -Funktion zum Aktualisieren der Menüleiste aufruft.</span><span class="sxs-lookup"><span data-stu-id="58cb3-115">After sending this message, an application must call the [**DrawMenuBar**](/windows/win32/api/winuser/nf-winuser-drawmenubar) function to update the menu bar.</span></span>

## <a name="requirements"></a><span data-ttu-id="58cb3-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="58cb3-116">Requirements</span></span>



| <span data-ttu-id="58cb3-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="58cb3-117">Requirement</span></span> | <span data-ttu-id="58cb3-118">Wert</span><span class="sxs-lookup"><span data-stu-id="58cb3-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58cb3-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="58cb3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="58cb3-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="58cb3-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="58cb3-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="58cb3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="58cb3-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="58cb3-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="58cb3-123">Header</span><span class="sxs-lookup"><span data-stu-id="58cb3-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="58cb3-124"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="58cb3-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58cb3-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="58cb3-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="58cb3-126">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="58cb3-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="58cb3-127">**DrawMenuBar**</span><span class="sxs-lookup"><span data-stu-id="58cb3-127">**DrawMenuBar**</span></span>](/windows/win32/api/winuser/nf-winuser-drawmenubar)
</dt> <dt>

[<span data-ttu-id="58cb3-128">**WM- \_ mdisetmenu**</span><span class="sxs-lookup"><span data-stu-id="58cb3-128">**WM\_MDISETMENU**</span></span>](wm-mdisetmenu.md)
</dt> <dt>

<span data-ttu-id="58cb3-129">**Licher**</span><span class="sxs-lookup"><span data-stu-id="58cb3-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="58cb3-130">Mehrere Dokument Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="58cb3-130">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 
