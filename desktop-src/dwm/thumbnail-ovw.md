---
title: Übersicht über DWM-Miniaturansichten
description: Desktopfenster-Manager (DWM) ermöglicht die Anzeige von Miniaturansichtsdarstellungen von Anwendungsfenstern.
ms.assetid: 6d71fcda-0cf0-463c-8c60-0415109d154f
keywords:
- Desktopfenster-Manager (DWM), Miniaturansichten
- DWM (Desktopfenster-Manager),Miniaturansichten
- Desktopfenster-Manager (DWM), Miniaturansichtsbeziehungen
- DWM (Desktopfenster-Manager),Miniaturansichtsbeziehungen
- Miniaturansichten
- Miniaturansichtsbeziehungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b333d84496828c451ff6e0eb7dbf3a86f91d629623d9939f66e874cfa82ee47d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118279770"
---
# <a name="dwm-thumbnail-overview"></a>Übersicht über DWM-Miniaturansichten

Desktopfenster-Manager (DWM) ermöglicht die Anzeige von Miniaturansichtsdarstellungen von Anwendungsfenstern. Dabei handelt es sich nicht um statische Momentaufnahmen eines Fensters, sondern um dynamische, konstante Verbindungen zwischen einem Miniaturansichtsquellfenster und einem Speicherort in einem Zielfenster, das das Liveminiaturrendering empfängt. Dies ermöglicht eine schnelle Ansicht der ausgeführten Anwendungen, indem Sie auf die Anwendung auf der Taskleiste zeigen oder die ALT-TAB-Taste verwenden, um eine Anwendung anzuzeigen und schnell zu wechseln.

Die folgende Abbildung veranschaulicht die Liveminiaturansicht von Windows Vista, die angezeigt wird, wenn Sie auf der Taskleiste auf die Anwendung zeigen.

![Screenshot: D W M-Miniaturansicht, die angezeigt wird, wenn auf eine App in der Taskleiste gezeigt wird.](images/dwm-livethumbnail.png)

Die folgende Abbildung veranschaulicht die von DWM aktivierte Windows Vista Flip (ALT-TAB).

![Screenshot der dwm-fähigen ALT-TAB-TASTE](images/dwm-flip.png)

> [!Note]  
> DWM-Miniaturansichten ermöglichen Es Entwicklern nicht, Anwendungen wie das Feature Windows Vista Flip3D (WINKEY-TAB) zu erstellen. Miniaturansichten werden direkt im Zielfenster in 2D gerendert.

 

## <a name="dwm-thumbnail-relationships"></a>DWM-Miniaturansichtsbeziehungen

Um Miniaturansichten in Ihrer Anwendung anzuzeigen, müssen Sie zunächst eine Beziehung zwischen einem Quellfenster und einem Zielfenster herstellen. Dazu wird die [**DwmRegisterThumbnail-Funktion**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail) aufgerufen.

[**DwmRegisterThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail) rendert keine Miniaturansicht im Zielfenster, sondern erstellt lediglich die Beziehung und stellt das Miniaturansichtshandle bereit. Die Miniaturansicht wird gerendert, nachdem die EIGENSCHAFTEN der [**\_ DWM-MINIATURANSICHT \_**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_thumbnail_properties) festgelegt wurden und die [**DwmUpdateThumbnailProperties-Funktion**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmupdatethumbnailproperties) aufgerufen wurde. Nachfolgende Aufrufe von **DwmUpdateThumbnailProperties** aktualisieren die Miniaturansicht mit einem neuen Satz von Eigenschaften. Der DWM stellt auch die Hilfsfunktion [**DwmQueryThumbnailSourceSize**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmquerythumbnailsourcesize) bereit, um die Größe des Quellfensters aus der Miniaturansicht abzurufen.

Um eine Miniaturansichtsbeziehung zu beenden, rufen Sie die [**DwmUnregisterThumbnail-Funktion**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmunregisterthumbnail) auf.

Im folgenden Beispiel wird veranschaulicht, wie sie eine Releationship mit dem Windows Desktop erstellen und in einer Anwendung anzeigen.


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

 

 




