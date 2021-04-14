---
title: ACM_OPEN Meldung (kommstrg. h)
description: Öffnet einen AVI-Clip und zeigt seinen ersten Frame in einem Animations Steuerelement an. Sie können diese Nachricht explizit senden oder das Makro animieren \_ Open oder animieren \_ OpenEx verwenden. Wir empfehlen die Verwendung der Unicode-Version dieser Nachricht, ACM \_ openw.
ms.assetid: 87f476ce-bb27-4b5f-bfdf-dff84bd7e4f4
keywords:
- Windows-Steuerelemente für ACM_OPEN Meldung
topic_type:
- apiref
api_name:
- ACM_OPEN
- ACM_OPENA
- ACM_OPENW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0588c0e321efe5cace63baf4016dbaa97f735252
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391648"
---
# <a name="acm_open-message"></a><span data-ttu-id="00b0a-106">Geöffnete ACM- \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="00b0a-106">ACM\_OPEN message</span></span>

<span data-ttu-id="00b0a-107">Öffnet einen AVI-Clip und zeigt seinen ersten Frame in einem Animations Steuerelement an.</span><span class="sxs-lookup"><span data-stu-id="00b0a-107">Opens an AVI clip and displays its first frame in an animation control.</span></span> <span data-ttu-id="00b0a-108">Sie können diese Nachricht explizit senden oder das Makro [**animieren \_ Open**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) oder [**animieren \_ OpenEx**](/windows/desktop/api/Commctrl/nf-commctrl-animate_openex) verwenden.</span><span class="sxs-lookup"><span data-stu-id="00b0a-108">You can send this message explicitly or use the [**Animate\_Open**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) or [**Animate\_OpenEx**](/windows/desktop/api/Commctrl/nf-commctrl-animate_openex) macro.</span></span> <span data-ttu-id="00b0a-109">Wir empfehlen die Verwendung der Unicode-Version dieser Nachricht, ACM \_ openw.</span><span class="sxs-lookup"><span data-stu-id="00b0a-109">We recommend using the Unicode version of this message, ACM\_OPENW.</span></span>

## <a name="parameters"></a><span data-ttu-id="00b0a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="00b0a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00b0a-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="00b0a-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="00b0a-112">[Version 4,71](common-control-versions.md) und höher.</span><span class="sxs-lookup"><span data-stu-id="00b0a-112">[Version 4.71](common-control-versions.md) and later.</span></span> <span data-ttu-id="00b0a-113">Ein Instanzhandle für das Modul, von dem die Ressource geladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="00b0a-113">An instance handle to the module from which the resource should be loaded.</span></span> <span data-ttu-id="00b0a-114">Legen Sie diesen Wert auf **null** fest, damit das Steuerelement den HINSTANCE-Wert verwendet, der zum Erstellen des Fensters verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="00b0a-114">Set this value to **NULL** to have the control use the HINSTANCE value used to create the window.</span></span> <span data-ttu-id="00b0a-115">Beachten Sie Folgendes: Wenn das Fenster durch eine DLL erstellt wird, ist der Standardwert für *wParam* der HINSTANCE-Wert der dll, nicht die Anwendung, die die DLL aufruft.</span><span class="sxs-lookup"><span data-stu-id="00b0a-115">Note that if the window is created by a DLL, the default value for *wParam* is the HINSTANCE value of the DLL, not of the application that calls the DLL.</span></span>

</dd> <dt>

<span data-ttu-id="00b0a-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="00b0a-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="00b0a-117">Ein Zeiger auf einen Puffer, der den Pfad der AVI-Datei oder den Namen einer AVI-Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="00b0a-117">A pointer to a buffer that contains the path of the AVI file or the name of an AVI resource.</span></span> <span data-ttu-id="00b0a-118">Alternativ kann dieser Parameter aus dem AVI-Ressourcen Bezeichner in [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) und NULL im [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))bestehen.</span><span class="sxs-lookup"><span data-stu-id="00b0a-118">Alternatively, this parameter can consist of the AVI resource identifier in the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) and zero in the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span></span> <span data-ttu-id="00b0a-119">Verwenden Sie das [**makeintresource**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea) -Makro, um diesen Wert zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="00b0a-119">To create this value, use the [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea) macro.</span></span> <span data-ttu-id="00b0a-120">Das-Steuerelement lädt die AVI-Ressource aus dem Modul, das vom Instanzhandle angegeben wurde [**, das an die Funktion**](/windows/desktop/api/winuser/nf-winuser-createwindowa) "-Funktion", " [**animieren \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create) " oder die Dialogfeld-Erstellungs Funktion, die das Steuerelement erstellt hat,</span><span class="sxs-lookup"><span data-stu-id="00b0a-120">The control loads the AVI resource from the module specified by the instance handle passed to the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) function, the [**Animate\_Create**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create) macro, or the dialog box creation function that created the control.</span></span> <span data-ttu-id="00b0a-121">In [Version 4,71](common-control-versions.md) und höher wird die Ressource aus dem Modul geladen, das von *wParam* angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="00b0a-121">In [Version 4.71](common-control-versions.md) and later, the resource is loaded from the module specified by *wParam*.</span></span> <span data-ttu-id="00b0a-122">Eine AVI-Ressource muss den Typ "AVI" aufweisen.</span><span class="sxs-lookup"><span data-stu-id="00b0a-122">An AVI resource must have the "AVI" type.</span></span> <span data-ttu-id="00b0a-123">Wenn dieser Parameter **null** ist, schließt das System die AVI-Datei, die zuvor für das angegebene Animations Steuerelement geöffnet war, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="00b0a-123">If this parameter is **NULL**, the system closes the AVI file that was previously opened for the specified animation control, if any.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00b0a-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="00b0a-124">Return value</span></span>

<span data-ttu-id="00b0a-125">Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.</span><span class="sxs-lookup"><span data-stu-id="00b0a-125">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="00b0a-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="00b0a-126">Remarks</span></span>

<span data-ttu-id="00b0a-127">Die von *lpszname* angegebene AVI-Datei oder-Ressource darf kein Audioformat enthalten.</span><span class="sxs-lookup"><span data-stu-id="00b0a-127">The AVI file or resource specified by *lpszName* must not contain audio.</span></span>

<span data-ttu-id="00b0a-128">Wir empfehlen die Verwendung der Unicode-Version dieser Nachricht, ACM \_ openw.</span><span class="sxs-lookup"><span data-stu-id="00b0a-128">We recommend using the Unicode version of this message, ACM\_OPENW.</span></span>

<span data-ttu-id="00b0a-129">Sie können nur automatische AVI-Clips öffnen.</span><span class="sxs-lookup"><span data-stu-id="00b0a-129">You can only open silent AVI clips.</span></span> <span data-ttu-id="00b0a-130">\_Das Öffnen und [**Animieren von \_**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) ACM schlägt fehl, wenn *LPARAM* einen AVI-Clip angibt, der Sound enthält.</span><span class="sxs-lookup"><span data-stu-id="00b0a-130">ACM\_OPEN and [**Animate\_Open**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) fail if *lParam* specifies an AVI clip that contains sound.</span></span>

<span data-ttu-id="00b0a-131">Sie können Animation [**\_ Close**](/windows/desktop/api/Commctrl/nf-commctrl-animate_close) verwenden, um eine AVI-Datei oder eine AVI-Ressource zu schließen, die zuvor für das angegebene Animations Steuerelement geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="00b0a-131">You can use [**Animate\_Close**](/windows/desktop/api/Commctrl/nf-commctrl-animate_close) to close an AVI file or AVI resource that was previously opened for the specified animation control.</span></span>

## <a name="requirements"></a><span data-ttu-id="00b0a-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="00b0a-132">Requirements</span></span>



| <span data-ttu-id="00b0a-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="00b0a-133">Requirement</span></span> | <span data-ttu-id="00b0a-134">Wert</span><span class="sxs-lookup"><span data-stu-id="00b0a-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="00b0a-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="00b0a-135">Minimum supported client</span></span><br/> | <span data-ttu-id="00b0a-136">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="00b0a-136">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="00b0a-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="00b0a-137">Minimum supported server</span></span><br/> | <span data-ttu-id="00b0a-138">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="00b0a-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="00b0a-139">Header</span><span class="sxs-lookup"><span data-stu-id="00b0a-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="00b0a-140"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="00b0a-140"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="00b0a-141">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="00b0a-141">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="00b0a-142">**ACM \_ Openw** (Unicode) und **ACM \_ Opena** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="00b0a-142">**ACM\_OPENW** (Unicode) and **ACM\_OPENA** (ANSI)</span></span><br/>                         |



 

