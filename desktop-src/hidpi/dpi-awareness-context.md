---
title: DPI_AWARENESS_CONTEXT handle (WINDEF. h)
description: Identifiziert den kontextkontext für ein Fenster.
ms.assetid: BFD54A9F-642B-4A3A-BBB9-F3A80779251D
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: 1663fad828a2fb29aa0d65ef58ae79616f64edcd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340748"
---
# <a name="dpi_awareness_context-handle"></a><span data-ttu-id="41e6b-103">\_Kontext Handle für dpi-Informationen \_</span><span class="sxs-lookup"><span data-stu-id="41e6b-103">DPI\_AWARENESS\_CONTEXT handle</span></span>

<span data-ttu-id="41e6b-104">Identifiziert den kontextkontext für ein Fenster.</span><span class="sxs-lookup"><span data-stu-id="41e6b-104">Identifies the awareness context for a window.</span></span>

## <a name="syntax"></a><span data-ttu-id="41e6b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="41e6b-105">Syntax</span></span>

``` syntax
#define DPI_AWARENESS_CONTEXT_UNAWARE              ((DPI_AWARENESS_CONTEXT)-1)
#define DPI_AWARENESS_CONTEXT_SYSTEM_AWARE         ((DPI_AWARENESS_CONTEXT)-2)
#define DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE    ((DPI_AWARENESS_CONTEXT)-3)
#define DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2 ((DPI_AWARENESS_CONTEXT)-4)
#define DPI_AWARENESS_CONTEXT_UNAWARE_GDISCALED    ((DPI_AWARENESS_CONTEXT)-5)
```

## <a name="constants"></a><span data-ttu-id="41e6b-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="41e6b-106">Constants</span></span>

<span data-ttu-id="41e6b-107">**DPI \_ - \_ Kontext ist \_ nicht bekannt.**</span><span class="sxs-lookup"><span data-stu-id="41e6b-107">**DPI\_AWARENESS\_CONTEXT\_UNAWARE**</span></span><dl> <span data-ttu-id="41e6b-108">DPI ist nicht bekannt.</span><span class="sxs-lookup"><span data-stu-id="41e6b-108">DPI unaware.</span></span> <span data-ttu-id="41e6b-109">Dieses Fenster wird nicht für dpi-Änderungen skaliert, und es wird immer angenommen, dass es einen Skalierungsfaktor von 100% (96 dpi) gibt.</span><span class="sxs-lookup"><span data-stu-id="41e6b-109">This window does not scale for DPI changes and is always assumed to have a scale factor of 100% (96 DPI).</span></span> <span data-ttu-id="41e6b-110">Sie wird automatisch durch das System auf jeder anderen dpi-Einstellung skaliert.</span><span class="sxs-lookup"><span data-stu-id="41e6b-110">It will be automatically scaled by the system on any other DPI setting.</span></span>  
</dl>

<span data-ttu-id="41e6b-111">**\_ \_ Kontext System für \_ dpi-Bewusstsein \_**</span><span class="sxs-lookup"><span data-stu-id="41e6b-111">**DPI\_AWARENESS\_CONTEXT\_SYSTEM\_AWARE**</span></span><dl> <span data-ttu-id="41e6b-112">System-dpi-fähig.</span><span class="sxs-lookup"><span data-stu-id="41e6b-112">System DPI aware.</span></span> <span data-ttu-id="41e6b-113">Dieses Fenster wird nicht für dpi-Änderungen skaliert.</span><span class="sxs-lookup"><span data-stu-id="41e6b-113">This window does not scale for DPI changes.</span></span> <span data-ttu-id="41e6b-114">Es wird einmal eine Abfrage für den dpi-Wert durchführen und diesen Wert für die Lebensdauer des Prozesses verwenden.</span><span class="sxs-lookup"><span data-stu-id="41e6b-114">It will query for the DPI once and use that value for the lifetime of the process.</span></span> <span data-ttu-id="41e6b-115">Wenn sich der dpi-Wert ändert, wird der Prozess nicht an den neuen dpi-Wert angepasst.</span><span class="sxs-lookup"><span data-stu-id="41e6b-115">If the DPI changes, the process will not adjust to the new DPI value.</span></span> <span data-ttu-id="41e6b-116">Der Wert wird vom System automatisch zentral hoch-oder herunterskaliert, wenn der dpi-Wert vom System Wert geändert wird.</span><span class="sxs-lookup"><span data-stu-id="41e6b-116">It will be automatically scaled up or down by the system when the DPI changes from the system value.</span></span>  
</dl>

<span data-ttu-id="41e6b-117">**DPI \_ - \_ Kontext \_ pro \_ Monitor \_**</span><span class="sxs-lookup"><span data-stu-id="41e6b-117">**DPI\_AWARENESS\_CONTEXT\_PER\_MONITOR\_AWARE**</span></span><dl> <span data-ttu-id="41e6b-118">Pro Monitor-dpi-fähig.</span><span class="sxs-lookup"><span data-stu-id="41e6b-118">Per monitor DPI aware.</span></span> <span data-ttu-id="41e6b-119">Dieses Fenster überprüft den dpi-Wert, wenn er erstellt wird, und passt den Skalierungsfaktor an, wenn sich der dpi-Wert ändert</span><span class="sxs-lookup"><span data-stu-id="41e6b-119">This window checks for the DPI when it is created and adjusts the scale factor whenever the DPI changes.</span></span> <span data-ttu-id="41e6b-120">Diese Prozesse werden nicht automatisch vom System skaliert.</span><span class="sxs-lookup"><span data-stu-id="41e6b-120">These processes are not automatically scaled by the system.</span></span>  
</dl>

<span data-ttu-id="41e6b-121">**DPI \_ - \_ kontextkontext \_ pro \_ Monitor- \_ Aware \_ v2**</span><span class="sxs-lookup"><span data-stu-id="41e6b-121">**DPI\_AWARENESS\_CONTEXT\_PER\_MONITOR\_AWARE\_V2**</span></span><dl> <span data-ttu-id="41e6b-122">Wird auch als " **pro Monitor v2**" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="41e6b-122">Also known as **Per Monitor v2**.</span></span> <span data-ttu-id="41e6b-123">Ein Fortschritt im Hinblick auf den ursprünglichen dpi-Modus für den dpi-Wert, mit dem Anwendungen auf einem Fenster der obersten Ebene auf neues dpi-bezogenes Skalierungs Verhalten zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="41e6b-123">An advancement over the original per-monitor DPI awareness mode, which enables applications to access new DPI-related scaling behaviors on a per top-level window basis.</span></span>  
<span data-ttu-id="41e6b-124">Pro Monitor v2 wurde im Creators Update von Windows 10 zur Verfügung gestellt und ist in früheren Versionen des Betriebssystems nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="41e6b-124">Per Monitor v2 was made available in the Creators Update of Windows 10, and is not available on earlier versions of the operating system.</span></span>  
<span data-ttu-id="41e6b-125">Die folgenden zusätzlichen Verhaltensweisen werden eingeführt:</span><span class="sxs-lookup"><span data-stu-id="41e6b-125">The additional behaviors introduced are as follows:</span></span>

-   <span data-ttu-id="41e6b-126">**Dpi-Änderungs Benachrichtigungen** für das untergeordnete Fenster: in pro Monitor v2-Kontexten wird die gesamte Fenster Struktur über alle auftretenden dpi-Änderungen benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="41e6b-126">**Child window DPI change notifications** - In Per Monitor v2 contexts, the entire window tree is notified of any DPI changes that occur.</span></span>
-   <span data-ttu-id="41e6b-127">**Skalierung des nicht-Client Bereichs** : in allen Fenstern wird automatisch der nicht-Client-Bereich in einer dpi-sensiblen Weise gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="41e6b-127">**Scaling of non-client area** - All windows will automatically have their non-client area drawn in a DPI sensitive fashion.</span></span> <span data-ttu-id="41e6b-128">Aufrufe von [**enablenonclientdpiscalingsind**](/windows/desktop/api/Winuser/nf-winuser-enablenonclientdpiscaling) nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="41e6b-128">Calls to [**EnableNonClientDpiScaling**](/windows/desktop/api/Winuser/nf-winuser-enablenonclientdpiscaling) are unnecessary.</span></span>
-   <span data-ttu-id="41e6b-129">**Skalierung von Win32-Menüs** : alle Ntuser-Menüs, die in "pro Monitor v2"-Kontexten erstellt werden, werden pro Monitor skaliert.</span><span class="sxs-lookup"><span data-stu-id="41e6b-129">**Scaling of Win32 menus** - All NTUSER menus created in Per Monitor v2 contexts will be scaling in a per-monitor fashion.</span></span>
-   <span data-ttu-id="41e6b-130">**Dialog Feld Skalierung** : in den einzelnen Monitor v2-Kontexten erstellte Win32-Dialoge reagieren automatisch auf dpi-Änderungen.</span><span class="sxs-lookup"><span data-stu-id="41e6b-130">**Dialog Scaling** - Win32 dialogs created in Per Monitor v2 contexts will automatically respond to DPI changes.</span></span>
-   <span data-ttu-id="41e6b-131">**Verbesserte Skalierung von ComCtl32** -Steuerelementen: verschiedene ComCtl32-Steuerelemente haben ein verbessertes dpi-Skalierungs Verhalten in pro Monitor v2-Kontext</span><span class="sxs-lookup"><span data-stu-id="41e6b-131">**Improved scaling of comctl32 controls** - Various comctl32 controls have improved DPI scaling behavior in Per Monitor v2 contexts.</span></span>
-   <span data-ttu-id="41e6b-132">**Verbessertes Design Verhalten** : uxtheme-Handles, die im Kontext eines pro Monitor v2-Fensters geöffnet wurden, werden im Hinblick auf den dpi-Wert ausgeführt, der diesem Fenster zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="41e6b-132">**Improved theming behavior** - UxTheme handles opened in the context of a Per Monitor v2 window will operate in terms of the DPI associated with that window.</span></span>

  
</dl>

<span data-ttu-id="41e6b-133">**DPI_AWARENESS_CONTEXT_UNAWARE_GDISCALED**</span><span class="sxs-lookup"><span data-stu-id="41e6b-133">**DPI_AWARENESS_CONTEXT_UNAWARE_GDISCALED**</span></span>

<span data-ttu-id="41e6b-134">DPI-Informationen mit verbesserter Qualität von GDI-basiertem Inhalt.</span><span class="sxs-lookup"><span data-stu-id="41e6b-134">DPI unaware with improved quality of GDI-based content.</span></span> <span data-ttu-id="41e6b-135">Dieser Modus verhält sich ähnlich wie DPI_AWARENESS_CONTEXT_UNAWARE, ermöglicht aber auch das automatische verbessern der renderingqualität von Text und anderen GDI-basierten primitiven, wenn das Fenster auf einem High-dpi-Monitor angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="41e6b-135">This mode behaves similarly to DPI_AWARENESS_CONTEXT_UNAWARE, but also enables the system to automatically improve the rendering quality of text and other GDI-based primitives when the window is displayed on a high-DPI monitor.</span></span>

<span data-ttu-id="41e6b-136">Weitere Informationen finden Sie unter [verbessern der High-dpi-Oberfläche in GDI-basierten Desktop-Apps](https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/#Uwv9gY1SvpbgQ4dK.97).</span><span class="sxs-lookup"><span data-stu-id="41e6b-136">For more details, see [Improving the high-DPI experience in GDI-based Desktop apps](https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/#Uwv9gY1SvpbgQ4dK.97).</span></span>

<span data-ttu-id="41e6b-137">DPI_AWARENESS_CONTEXT_UNAWARE_GDISCALED wurde im Update von Windows 10 vom Oktober 2018 eingeführt (auch bekannt als Version 1809).</span><span class="sxs-lookup"><span data-stu-id="41e6b-137">DPI_AWARENESS_CONTEXT_UNAWARE_GDISCALED was introduced in the October 2018 update of Windows 10 (also known as version 1809).</span></span>


## <a name="requirements"></a><span data-ttu-id="41e6b-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="41e6b-138">Requirements</span></span>

| <span data-ttu-id="41e6b-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="41e6b-139">Requirement</span></span> | <span data-ttu-id="41e6b-140">Wert</span><span class="sxs-lookup"><span data-stu-id="41e6b-140">Value</span></span> |
|----|-----------|
| <span data-ttu-id="41e6b-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="41e6b-141">Minimum supported client</span></span><br/> | <span data-ttu-id="41e6b-142">Windows 10, Version 1607, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="41e6b-142">Windows 10, version 1607 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="41e6b-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="41e6b-143">Minimum supported server</span></span><br/> | <span data-ttu-id="41e6b-144">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="41e6b-144">None supported</span></span> <br/>  |
| <span data-ttu-id="41e6b-145">Header</span><span class="sxs-lookup"><span data-stu-id="41e6b-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="41e6b-146"><dt>WINDEF. h</dt></span><span class="sxs-lookup"><span data-stu-id="41e6b-146"><dt>windef.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="41e6b-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="41e6b-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41e6b-148">**Aredpiawareness contextsequal**</span><span class="sxs-lookup"><span data-stu-id="41e6b-148">**AreDpiAwarenessContextsEqual**</span></span>](/windows/desktop/api/winuser/nf-winuser-aredpiawarenesscontextsequal)
</dt> <dt>

[<span data-ttu-id="41e6b-149">**Getawarenmefromdpiawarretecontext**</span><span class="sxs-lookup"><span data-stu-id="41e6b-149">**GetAwarenessFromDpiAwarenessContext**</span></span>](/windows/desktop/api/winuser/nf-winuser-getawarenessfromdpiawarenesscontext)
</dt> </dl>

[<span data-ttu-id="41e6b-150">**Getdpifromdpiawareress Context**</span><span class="sxs-lookup"><span data-stu-id="41e6b-150">**GetDpiFromDpiAwarenessContext**</span></span>](/windows/desktop/api/winuser/nf-winuser-getdpifromdpiawarenesscontext)
</dt> </dl>

[<span data-ttu-id="41e6b-151">**Getthreaddpiawareress Context**</span><span class="sxs-lookup"><span data-stu-id="41e6b-151">**GetThreadDpiAwarenessContext**</span></span>](/windows/desktop/api/winuser/nf-winuser-getthreaddpiawarenesscontext)
</dt> </dl>

[<span data-ttu-id="41e6b-152">**Getwindowdpiawareress Context**</span><span class="sxs-lookup"><span data-stu-id="41e6b-152">**GetWindowDpiAwarenessContext**</span></span>](/windows/desktop/api/winuser/nf-winuser-getwindowdpiawarenesscontext)
</dt> </dl>

[<span data-ttu-id="41e6b-153">**Isvaliddpiawareress Context**</span><span class="sxs-lookup"><span data-stu-id="41e6b-153">**IsValidDpiAwarenessContext**</span></span>](/windows/desktop/api/winuser/nf-winuser-isvaliddpiawarenesscontext)
</dt> </dl>

[<span data-ttu-id="41e6b-154">**Setprocessdpiawareress Context**</span><span class="sxs-lookup"><span data-stu-id="41e6b-154">**SetProcessDpiAwarenessContext**</span></span>](/windows/desktop/api/winuser/nf-winuser-setprocessdpiawarenesscontext)
</dt> </dl>

[<span data-ttu-id="41e6b-155">**Setthreaddpiawareress Context**</span><span class="sxs-lookup"><span data-stu-id="41e6b-155">**SetThreadDpiAwarenessContext**</span></span>](/windows/desktop/api/winuser/nf-winuser-setthreaddpiawarenesscontext)
