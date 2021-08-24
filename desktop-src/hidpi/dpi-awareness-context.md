---
title: DPI_AWARENESS_CONTEXT Handle (windef.h)
description: Identifiziert den Bewusstseinskontext für ein Fenster.
ms.assetid: BFD54A9F-642B-4A3A-BBB9-F3A80779251D
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: 25e270f59af32b33fdb5ad3f511b693b3eebad71407d48b80a72aff5996edf14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119727180"
---
# <a name="dpi_awareness_context-handle"></a>DPI \_ AWARENESS \_ CONTEXT-Handle

Identifiziert den Bewusstseinskontext für ein Fenster.

## <a name="syntax"></a>Syntax

``` syntax
#define DPI_AWARENESS_CONTEXT_UNAWARE              ((DPI_AWARENESS_CONTEXT)-1)
#define DPI_AWARENESS_CONTEXT_SYSTEM_AWARE         ((DPI_AWARENESS_CONTEXT)-2)
#define DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE    ((DPI_AWARENESS_CONTEXT)-3)
#define DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2 ((DPI_AWARENESS_CONTEXT)-4)
#define DPI_AWARENESS_CONTEXT_UNAWARE_GDISCALED    ((DPI_AWARENESS_CONTEXT)-5)
```

## <a name="constants"></a>Konstanten

**\_DPI-BEWUSSTSEINSKONTEXT \_ \_ NICHT BEKANNT**<dl> DPI nicht bekannt. Dieses Fenster wird nicht für DPI-Änderungen skaliert und wird immer mit einem Skalierungsfaktor von 100 % (96 DPI) angenommen. Sie wird automatisch vom System für jede andere DPI-Einstellung skaliert.  
</dl>

**DPI \_ AWARENESS \_ CONTEXT \_ SYSTEM \_ AWARE**<dl> System-DPI-bewusst. Dieses Fenster wird nicht für DPI-Änderungen skaliert. Er wird den DPI einmal abfragen und diesen Wert für die Lebensdauer des Prozesses verwenden. Wenn sich der DPI-Wert ändert, wird der Prozess nicht an den neuen DPI-Wert angepasst. Sie wird automatisch vom System hoch- oder herunterskaliert, wenn sich der DPI-Wert vom Systemwert ändert.  
</dl>

**DPI \_ AWARENESS CONTEXT PER MONITOR AWARE (DPI-BEWUSSTSEINSKONTEXT \_ PRO \_ \_ \_ MONITOR)**<dl> DPI-bewusst pro Monitor. In diesem Fenster wird beim Erstellen auf den DPI überprüft, und der Skalierungsfaktor wird bei jeder Änderung des DPI angepasst. Diese Prozesse werden nicht automatisch vom System skaliert.  
</dl>

**DPI \_ AWARENESS \_ CONTEXT \_ PER \_ MONITOR \_ AWARE \_ V2**<dl> Wird auch als **Per Monitor v2 bezeichnet.** Eine Weiterentwicklung gegenüber dem ursprünglichen DPI-Bewusstseinsmodus pro Monitor, der es Anwendungen ermöglicht, auf neue DPI-bezogene Skalierungsverhalten pro Fenster der obersten Ebene zu zugreifen.  
Per Monitor v2 wurde im Creators Update von Windows 10 verfügbar gemacht und ist in früheren Versionen des Betriebssystems nicht verfügbar.  
Die zusätzlich eingeführten Verhaltensweisen lauten wie folgt:

-   **DPI-Änderungsbenachrichtigungen** für untergeordnete Fenster: In Kontexten pro Monitor v2 wird die gesamte Fensterstruktur über alle DPI-Änderungen benachrichtigt, die auftreten.
-   **Skalierung des Nicht-Clientbereichs:** Bei allen Fenstern wird ihr nicht clientseitiger Bereich automatisch auf DPI-sensible Weise gezeichnet. Aufrufe [**von EnableNonClientDpiScaling**](/windows/desktop/api/Winuser/nf-winuser-enablenonclientdpiscaling) sind nicht erforderlich.
-   **Skalierung von Win32-Menüs:** Alle NTUSER-Menüs, die in Kontexten pro Monitor v2 erstellt werden, werden auf monitorspezifische Weise skaliert.
-   **Dialogskalierung:** Win32-Dialoge, die in Kontexten pro Monitor v2 erstellt wurden, reagieren automatisch auf DPI-Änderungen.
-   **Verbesserte Skalierung von comctl32-Steuerelementen:** Verschiedene comctl32-Steuerelemente haben das DPI-Skalierungsverhalten in Kontexten pro Monitor v2 verbessert.
-   **Verbessertes Designverhalten:** UxTheme-Handles, die im Kontext eines Pro Monitor v2-Fensters geöffnet werden, werden im Hinblick auf den DPI-Bereich verwendet, der diesem Fenster zugeordnet ist.

  
</dl>

**DPI_AWARENESS_CONTEXT_UNAWARE_GDISCALED**

DPI mit verbesserter Qualität von GDI-basiertem Inhalt nicht bekannt. Dieser Modus verhält sich ähnlich wie DPI_AWARENESS_CONTEXT_UNAWARE, ermöglicht es dem System jedoch auch, die Renderingqualität von Text und anderen GDI-basierten Primitiven automatisch zu verbessern, wenn das Fenster auf einem Monitor mit hohem DPI-Wert angezeigt wird.

Weitere Informationen finden Sie unter Verbessern der Hohen [DPI-Leistung in GDI-basierten Desktop-Apps.](https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/#Uwv9gY1SvpbgQ4dK.97)

DPI_AWARENESS_CONTEXT_UNAWARE_GDISCALED wurde im Update vom Oktober 2018 von Windows 10 (auch als Version 1809 bekannt) eingeführt.


## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|----|-----------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10 Desktop-Apps, Version 1607 \[\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt <br/>  |
| Header<br/>                   | <dl> <dt>windef.h</dt> </dl> |

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**AreDpiAwarenessContextsEqual**](/windows/desktop/api/winuser/nf-winuser-aredpiawarenesscontextsequal)
</dt> <dt>

[**GetAwarenessFromDpiAwarenessContext**](/windows/desktop/api/winuser/nf-winuser-getawarenessfromdpiawarenesscontext)
</dt> </dl>

[**GetDpiFromDpiAwarenessContext**](/windows/desktop/api/winuser/nf-winuser-getdpifromdpiawarenesscontext)
</dt> </dl>

[**GetThreadDpiAwarenessContext**](/windows/desktop/api/winuser/nf-winuser-getthreaddpiawarenesscontext)
</dt> </dl>

[**GetWindowDpiAwarenessContext**](/windows/desktop/api/winuser/nf-winuser-getwindowdpiawarenesscontext)
</dt> </dl>

[**IsValidDpiAwarenessContext**](/windows/desktop/api/winuser/nf-winuser-isvaliddpiawarenesscontext)
</dt> </dl>

[**SetProcessDpiAwarenessContext**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiawarenesscontext)
</dt> </dl>

[**SetThreadDpiAwarenessContext**](/windows/desktop/api/winuser/nf-winuser-setthreaddpiawarenesscontext)
