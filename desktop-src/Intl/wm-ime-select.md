---
description: Wird an eine Anwendung gesendet, wenn das Betriebssystem im Begriff ist, den aktuellen IME zu ändern. Ein Fenster empfängt diese Meldung über seine WindowProc-Funktion.
ms.assetid: 5559b3ab-8d81-4f33-b0af-d05489371328
title: WM_IME_SELECT Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 940858e12c616b1d6281c23633b2f0f5e9657a9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345732"
---
# <a name="wm_ime_select-message"></a><span data-ttu-id="09a41-104">WM- \_ IME \_ Select-Nachricht</span><span class="sxs-lookup"><span data-stu-id="09a41-104">WM\_IME\_SELECT message</span></span>

<span data-ttu-id="09a41-105">Wird an eine Anwendung gesendet, wenn das Betriebssystem im Begriff ist, den aktuellen IME zu ändern.</span><span class="sxs-lookup"><span data-stu-id="09a41-105">Sent to an application when the operating system is about to change the current IME.</span></span> <span data-ttu-id="09a41-106">Ein Fenster empfängt diese Meldung über seine [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="09a41-106">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
 HWND  hwnd,       
 WM_IME_SELECT,   
 WPARAM wParam,   
 LPARAM lParam    
);
```



## <a name="parameters"></a><span data-ttu-id="09a41-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="09a41-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09a41-108">*HWND*</span><span class="sxs-lookup"><span data-stu-id="09a41-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="09a41-109">Ein Handle für Fenster.</span><span class="sxs-lookup"><span data-stu-id="09a41-109">A handle to window.</span></span>

</dd> <dt>

<span data-ttu-id="09a41-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="09a41-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="09a41-111">Auswahl Indikator.</span><span class="sxs-lookup"><span data-stu-id="09a41-111">Selection indicator.</span></span> <span data-ttu-id="09a41-112">Dieser Parameter gibt **true** an, wenn der angegeben IME ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="09a41-112">This parameter specifies **TRUE** if the indicated IME is selected.</span></span> <span data-ttu-id="09a41-113">Der-Parameter wird auf **false** festgelegt, wenn der angegebene IME nicht mehr ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="09a41-113">The parameter is set to **FALSE** if the specified IME is no longer selected.</span></span>

</dd> <dt>

<span data-ttu-id="09a41-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="09a41-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="09a41-115">Eingabe Gebiets Schema Bezeichner, der dem IME zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="09a41-115">Input locale identifier associated with the IME.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09a41-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="09a41-116">Return value</span></span>

<span data-ttu-id="09a41-117">Diese Nachricht weist keinen Rückgabewert auf.</span><span class="sxs-lookup"><span data-stu-id="09a41-117">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="09a41-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="09a41-118">Remarks</span></span>

<span data-ttu-id="09a41-119">Eine Anwendung, die ein IME-Fenster erstellt hat, sollte diese Nachricht an dieses Fenster übergeben, damit Sie das Tastaturlayout-Handle für die neu ausgewählte IME abrufen kann.</span><span class="sxs-lookup"><span data-stu-id="09a41-119">An application that has created an IME window should pass this message to that window so that it can retrieve the keyboard layout handle to the newly selected IME.</span></span>

<span data-ttu-id="09a41-120">Die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  -Funktion verarbeitet diese Nachricht, indem Sie die Informationen an das IME-Standardfenster übergibt.</span><span class="sxs-lookup"><span data-stu-id="09a41-120">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  function processes this message by passing the information to the default IME window.</span></span>

## <a name="requirements"></a><span data-ttu-id="09a41-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="09a41-121">Requirements</span></span>



| <span data-ttu-id="09a41-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="09a41-122">Requirement</span></span> | <span data-ttu-id="09a41-123">Wert</span><span class="sxs-lookup"><span data-stu-id="09a41-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09a41-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="09a41-124">Minimum supported client</span></span><br/> | <span data-ttu-id="09a41-125">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="09a41-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="09a41-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="09a41-126">Minimum supported server</span></span><br/> | <span data-ttu-id="09a41-127">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="09a41-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="09a41-128">Header</span><span class="sxs-lookup"><span data-stu-id="09a41-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="09a41-129"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="09a41-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09a41-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="09a41-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09a41-131">Eingabemethoden-Manager</span><span class="sxs-lookup"><span data-stu-id="09a41-131">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="09a41-132">Eingabemethoden-Manager-Meldungen</span><span class="sxs-lookup"><span data-stu-id="09a41-132">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> </dl>

 

 
