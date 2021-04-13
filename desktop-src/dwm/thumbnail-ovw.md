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
# <a name="dwm-thumbnail-overview"></a>Übersicht über DWM-Miniaturansichten

Desktopfenster-Manager (DWM) ermöglicht die Anzeige von Miniaturansichten von Anwendungs Fenstern. Dabei handelt es sich nicht um statische Momentaufnahmen eines Fensters, sondern stattdessen um dynamische, Konstante Verbindungen zwischen einem Miniatur Ansichts Quellen-Fenster und einem Speicherort in einem Zielfenster, das das Rendering der Live Miniaturansicht empfängt. Dies ermöglicht eine schnelle Ansicht der Ausführung von Anwendungen, indem mit dem Mauszeiger auf die Anwendung auf der Taskleiste gezeigt wird oder die Tastenkombination Alt + Tab verwendet wird, um eine Anwendung anzuzeigen und schnell zu wechseln.

Die folgende Abbildung veranschaulicht die Windows Vista-Live Miniaturansicht, die angezeigt wird, wenn Sie auf der Taskleiste auf die Anwendung zeigen.

![Screenshot, der die Miniaturansicht von D W M anzeigt, wenn Sie auf der Taskleiste auf eine APP zeigen.](images/dwm-livethumbnail.png)

Die folgende Abbildung veranschaulicht die von DWM aktivierte Windows Vista-Flip-Taste (Alt-Tab).

![Screenshot der DWM-aktivierten alt-Registerkarte](images/dwm-flip.png)

> [!Note]  
> DWM-Miniaturansichten ermöglichen es Entwicklern nicht, Anwendungen wie das Windows Vista Flip3D-Feature (WinKey-Tab) zu erstellen. Miniaturansichten werden direkt im Zielfenster in 2D gerendert.

 

## <a name="dwm-thumbnail-relationships"></a>DWM-Miniaturansichten

Zum Anzeigen von Miniaturansichten in der Anwendung müssen Sie zuerst eine Beziehung zwischen einem Quell-und einem Zielfenster herstellen. Dies erfolgt durch Aufrufen der Funktion " [**DwmRegisterThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail) ".

" [**Dwmregisterminiatur**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail) " gibt im Zielfenster keine Miniaturansicht an, sondern erstellt lediglich die Beziehung und stellt das Miniatur Ansichts Handle bereit. Die Miniaturansicht wird gerendert, nachdem die [**Eigenschaften der DWM- \_ Miniaturansicht \_**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_thumbnail_properties) festgelegt und die [**DwmUpdateThumbnailProperties**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmupdatethumbnailproperties) -Funktion aufgerufen wurde. Nachfolgende Aufrufe von **DwmUpdateThumbnailProperties** aktualisieren die Miniaturansicht mit einem neuen Satz von Eigenschaften. Die DWM stellt außerdem die Hilfsfunktion [**DwmQueryThumbnailSourceSize**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmquerythumbnailsourcesize) bereit, um die Größe des Quell Fensters aus der Miniaturansicht zu erhalten.

Um eine Miniaturansicht zu beenden, müssen Sie die Funktion [**DwmUnregisterThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmunregisterthumbnail) aufrufen.

Im folgenden Beispiel wird veranschaulicht, wie eine releationship mit dem Windows-Desktop erstellt und in einer Anwendung angezeigt wird.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über Desktop Window Manager](dwm-overview.md)
</dt> <dt>

[Enable and Control DWM Composition (Aktivieren und Steuern der DWM-Komposition)](composition-ovw.md)
</dt> <dt>

[Überlegungen zur Leistung und bewährte Methoden](bestpractices-ovw.md)
</dt> </dl>

 

 




