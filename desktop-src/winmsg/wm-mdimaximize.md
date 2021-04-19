---
description: Eine Anwendung sendet die WM- \_ mdimaximiernachricht an ein MDI-Client Fenster (Multiple Document Interface), um ein untergeordnetes MDI-Fenster zu maximieren.
ms.assetid: 7c5e4157-13f6-40d7-a64a-076bd14aca0d
title: WM_MDIMAXIMIZE Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8372bcb25f35a52793292de4fd94a4a9dadafe6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345705"
---
# <a name="wm_mdimaximize-message"></a><span data-ttu-id="b6933-103">WM- \_ mdimaximiungsmeldung</span><span class="sxs-lookup"><span data-stu-id="b6933-103">WM\_MDIMAXIMIZE message</span></span>

<span data-ttu-id="b6933-104">Eine Anwendung sendet die **WM- \_ mdimaximiernachricht** an ein MDI-Client Fenster (Multiple Document Interface), um ein untergeordnetes MDI-Fenster zu maximieren.</span><span class="sxs-lookup"><span data-stu-id="b6933-104">An application sends the **WM\_MDIMAXIMIZE** message to a multiple-document interface (MDI) client window to maximize an MDI child window.</span></span> <span data-ttu-id="b6933-105">Das System ändert die Größe des untergeordneten Fensters, damit der Client Bereich das Client Fenster ausfüllen muss.</span><span class="sxs-lookup"><span data-stu-id="b6933-105">The system resizes the child window to make its client area fill the client window.</span></span> <span data-ttu-id="b6933-106">Das System platziert das Fenstermenü Symbol des untergeordneten Fensters an der rechten Position der Menüleiste des Frame Fensters und platziert das Wiederherstellungs Symbol des untergeordneten Fensters an der äußersten linken Position.</span><span class="sxs-lookup"><span data-stu-id="b6933-106">The system places the child window's window menu icon in the rightmost position of the frame window's menu bar, and places the child window's restore icon in the leftmost position.</span></span> <span data-ttu-id="b6933-107">Das System fügt den Text der Titelleiste des untergeordneten Fensters auch an die des Frame Fensters an.</span><span class="sxs-lookup"><span data-stu-id="b6933-107">The system also appends the title bar text of the child window to that of the frame window.</span></span>


```C++
#define WM_MDIMAXIMIZE                  0x0225
```



## <a name="parameters"></a><span data-ttu-id="b6933-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b6933-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6933-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b6933-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b6933-110">Ein Handle für das untergeordnete MDI-Fenster, das maximiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b6933-110">A handle to the MDI child window to be maximized.</span></span>

</dd> <dt>

<span data-ttu-id="b6933-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b6933-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b6933-112">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="b6933-112">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6933-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b6933-113">Return value</span></span>

<span data-ttu-id="b6933-114">Typ: **null**</span><span class="sxs-lookup"><span data-stu-id="b6933-114">Type: **zero**</span></span>

<span data-ttu-id="b6933-115">Der Rückgabewert ist immer 0 (null).</span><span class="sxs-lookup"><span data-stu-id="b6933-115">The return value is always zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6933-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b6933-116">Remarks</span></span>

<span data-ttu-id="b6933-117">Wenn ein MDI-Client Fenster eine Nachricht empfängt, die die Aktivierung der untergeordneten Fenster ändert, während das momentan aktive untergeordnete MDI-Fenster maximiert ist, stellt das System das aktive untergeordnete Fenster wieder her und maximiert das neu aktivierte untergeordnete Fenster.</span><span class="sxs-lookup"><span data-stu-id="b6933-117">If an MDI client window receives any message that changes the activation of its child windows while the currently active MDI child window is maximized, the system restores the active child window and maximizes the newly activated child window.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6933-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b6933-118">Requirements</span></span>



| <span data-ttu-id="b6933-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b6933-119">Requirement</span></span> | <span data-ttu-id="b6933-120">Wert</span><span class="sxs-lookup"><span data-stu-id="b6933-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6933-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b6933-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b6933-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b6933-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b6933-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b6933-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b6933-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b6933-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b6933-125">Header</span><span class="sxs-lookup"><span data-stu-id="b6933-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6933-126"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="b6933-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6933-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b6933-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="b6933-128">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="b6933-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b6933-129">**WM- \_ mumgeleitet-Speicher**</span><span class="sxs-lookup"><span data-stu-id="b6933-129">**WM\_MDIRESTORE**</span></span>](wm-mdirestore.md)
</dt> <dt>

<span data-ttu-id="b6933-130">**Licher**</span><span class="sxs-lookup"><span data-stu-id="b6933-130">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b6933-131">Mehrere Dokument Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="b6933-131">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 




