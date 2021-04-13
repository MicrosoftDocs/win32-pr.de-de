---
title: Übersicht über DWM-Miniaturansichten
description: Desktopfenster-Manager (DWM) ermöglicht die Anzeige von Miniaturansichten von Anwendungs Fenstern.
ms.assetid: 6d71fcda-0cf0-463c-8c60-0415109d154f
keywords:
- Desktopfenster-Manager (DWM), Miniaturansichten
- Dwm (Desktopfenster-Manager), Miniaturansichten
- Desktopfenster-Manager (DWM), Miniaturansichten Beziehungen
- Dwm (Desktopfenster-Manager), Miniaturansichten
- Miniaturansichten
- Miniaturansichten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e3e0f1e6875e447a18ff5e63d703460ff909b25
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2021
ms.locfileid: "104564850"
---
# <a name="dwm-thumbnail-overview"></a><span data-ttu-id="e2ce6-109">Übersicht über DWM-Miniaturansichten</span><span class="sxs-lookup"><span data-stu-id="e2ce6-109">DWM Thumbnail Overview</span></span>

<span data-ttu-id="e2ce6-110">Desktopfenster-Manager (DWM) ermöglicht die Anzeige von Miniaturansichten von Anwendungs Fenstern.</span><span class="sxs-lookup"><span data-stu-id="e2ce6-110">Desktop Window Manager (DWM) enables the display of thumbnail representations of application windows.</span></span> <span data-ttu-id="e2ce6-111">Dabei handelt es sich nicht um statische Momentaufnahmen eines Fensters, sondern stattdessen um dynamische, Konstante Verbindungen zwischen einem Miniatur Ansichts Quellen-Fenster und einem Speicherort in einem Zielfenster, das das Rendering der Live Miniaturansicht empfängt.</span><span class="sxs-lookup"><span data-stu-id="e2ce6-111">These are not static snapshots of a window, but are instead dynamic, constant connections between a thumbnail source window and a location on a destination window that receives the live thumbnail rendering.</span></span> <span data-ttu-id="e2ce6-112">Dies ermöglicht eine schnelle Ansicht der Ausführung von Anwendungen, indem mit dem Mauszeiger auf die Anwendung auf der Taskleiste gezeigt wird oder die Tastenkombination Alt + Tab verwendet wird, um eine Anwendung anzuzeigen und schnell zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="e2ce6-112">This allows a quick view of running applications by hovering over the application on the taskbar or using the ALT-TAB key gesture to see and quickly switch to an application.</span></span>

<span data-ttu-id="e2ce6-113">Die folgende Abbildung veranschaulicht die Windows Vista-Live Miniaturansicht, die angezeigt wird, wenn Sie auf der Taskleiste auf die Anwendung zeigen.</span><span class="sxs-lookup"><span data-stu-id="e2ce6-113">The following image illustrates the Windows Vista live thumbnail seen when you hover over the application on the taskbar.</span></span>

![Screenshot, der die Miniaturansicht von D W M anzeigt, wenn Sie auf der Taskleiste auf eine APP zeigen.](images/dwm-livethumbnail.png)

<span data-ttu-id="e2ce6-115">Die folgende Abbildung veranschaulicht die von DWM aktivierte Windows Vista-Flip-Taste (Alt-Tab).</span><span class="sxs-lookup"><span data-stu-id="e2ce6-115">The following image illustrates the Windows Vista Flip (ALT-TAB) enabled by DWM.</span></span>

![Screenshot der DWM-aktivierten alt-Registerkarte](images/dwm-flip.png)

> [!Note]  
> <span data-ttu-id="e2ce6-117">DWM-Miniaturansichten ermöglichen es Entwicklern nicht, Anwendungen wie das Windows Vista Flip3D-Feature (WinKey-Tab) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e2ce6-117">DWM thumbnails do not enable developers to create applications like the Windows Vista Flip3D (WINKEY-TAB) feature.</span></span> <span data-ttu-id="e2ce6-118">Miniaturansichten werden direkt im Zielfenster in 2D gerendert.</span><span class="sxs-lookup"><span data-stu-id="e2ce6-118">Thumbnails are rendered directly to the destination window in 2-D.</span></span>

 

## <a name="dwm-thumbnail-relationships"></a><span data-ttu-id="e2ce6-119">DWM-Miniaturansichten</span><span class="sxs-lookup"><span data-stu-id="e2ce6-119">DWM Thumbnail Relationships</span></span>

<span data-ttu-id="e2ce6-120">Zum Anzeigen von Miniaturansichten in der Anwendung müssen Sie zuerst eine Beziehung zwischen einem Quell-und einem Zielfenster herstellen.</span><span class="sxs-lookup"><span data-stu-id="e2ce6-120">To display thumbnails in your application, you must first establish a relationship between a source window and a destination window.</span></span> <span data-ttu-id="e2ce6-121">Dies erfolgt durch Aufrufen der Funktion " [**DwmRegisterThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail) ".</span><span class="sxs-lookup"><span data-stu-id="e2ce6-121">This is done by calling the [**DwmRegisterThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail) function.</span></span>

<span data-ttu-id="e2ce6-122">" [**Dwmregisterminiatur**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail) " gibt im Zielfenster keine Miniaturansicht an, sondern erstellt lediglich die Beziehung und stellt das Miniatur Ansichts Handle bereit.</span><span class="sxs-lookup"><span data-stu-id="e2ce6-122">[**DwmRegisterThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail) does not render a thumbnail on the destination window but merely creates the relationship and provides the thumbnail handle.</span></span> <span data-ttu-id="e2ce6-123">Die Miniaturansicht wird gerendert, nachdem die [**Eigenschaften der DWM- \_ Miniaturansicht \_**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_thumbnail_properties) festgelegt und die [**DwmUpdateThumbnailProperties**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmupdatethumbnailproperties) -Funktion aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="e2ce6-123">The thumbnail is rendered after the [**DWM\_THUMBNAIL\_PROPERTIES**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_thumbnail_properties) have been set and the [**DwmUpdateThumbnailProperties**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmupdatethumbnailproperties) function has been called.</span></span> <span data-ttu-id="e2ce6-124">Nachfolgende Aufrufe von **DwmUpdateThumbnailProperties** aktualisieren die Miniaturansicht mit einem neuen Satz von Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e2ce6-124">Subsequent calls to **DwmUpdateThumbnailProperties** update the thumbnail with a new set of properties.</span></span> <span data-ttu-id="e2ce6-125">Die DWM stellt außerdem die Hilfsfunktion [**DwmQueryThumbnailSourceSize**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmquerythumbnailsourcesize) bereit, um die Größe des Quell Fensters aus der Miniaturansicht zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="e2ce6-125">The DWM also provides the helper function [**DwmQueryThumbnailSourceSize**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmquerythumbnailsourcesize) to obtain the size of the source window from the thumbnail.</span></span>

<span data-ttu-id="e2ce6-126">Um eine Miniaturansicht zu beenden, müssen Sie die Funktion [**DwmUnregisterThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmunregisterthumbnail) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e2ce6-126">To end a thumbnail relationship, call the [**DwmUnregisterThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmunregisterthumbnail) function.</span></span>

<span data-ttu-id="e2ce6-127">Im folgenden Beispiel wird veranschaulicht, wie eine releationship mit dem Windows-Desktop erstellt und in einer Anwendung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="e2ce6-127">The following example demonstrates how to create a releationship with the Windows desktop and display it in an application.</span></span>


```
HRESULT hr = S_OK;
HTHUMBNAIL thumbnail = NULL;

// Register the thumbnail
hr = DwmRegisterThumbnail(hwnd, FindWindow(_T("Progman"), NULL), &thumbnail);
if (SUCCEEDED(hr))
{
    // Specify the destination rectangle size
    RECT dest = {0,50,100,150};

    // Set the thumbnail properties for use
    DWM_THUMBNAIL_PROPERTIES dskThumbProps;
    dskThumbProps.dwFlags = DWM_TNP_SOURCECLIENTAREAONLY | DWM_TNP_VISIBLE | DWM_TNP_OPACITY | DWM_TNP_RECTDESTINATION;
    dskThumbProps.fSourceClientAreaOnly = FALSE; 
    dskThumbProps.fVisible = TRUE;
    dskThumbProps.opacity = (255 * 70)/100;
    dskThumbProps.rcDestination = dest;

    // Display the thumbnail
    hr = DwmUpdateThumbnailProperties(thumbnail,&dskThumbProps);
    if (SUCCEEDED(hr))
    {
        // ...
    }
}
return hr;
```



## <a name="related-topics"></a><span data-ttu-id="e2ce6-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e2ce6-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2ce6-129">Übersicht über Desktop Window Manager</span><span class="sxs-lookup"><span data-stu-id="e2ce6-129">Desktop Window Manager Overview</span></span>](dwm-overview.md)
</dt> <dt>

[<span data-ttu-id="e2ce6-130">Enable and Control DWM Composition (Aktivieren und Steuern der DWM-Komposition)</span><span class="sxs-lookup"><span data-stu-id="e2ce6-130">Enable and Control DWM Composition</span></span>](composition-ovw.md)
</dt> <dt>

[<span data-ttu-id="e2ce6-131">Überlegungen zur Leistung und bewährte Methoden</span><span class="sxs-lookup"><span data-stu-id="e2ce6-131">Performance Considerations and Best Practices</span></span>](bestpractices-ovw.md)
</dt> </dl>

 

 




