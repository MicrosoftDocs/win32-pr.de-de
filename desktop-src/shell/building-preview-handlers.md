---
description: In diesem Thema werden die spezifischen Schnittstellen und Methoden erläutert, die zum Erstellen eines Vorschauhandlers erforderlich sind.
ms.assetid: 6c240a63-c184-4b65-9483-794f5de4d695
title: Erstellen von Vorschauhandlern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a810f15fed66d69bce32387249a2e0d678a1eb6c0dd918ec5df2e1ddbeb5be8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032918"
---
# <a name="building-preview-handlers"></a>Erstellen von Vorschauhandlern

In diesem Thema werden die spezifischen Schnittstellen und Methoden erläutert, die zum Erstellen eines Vorschauhandlers erforderlich sind.

Ein Vorschauhandler muss die folgenden Schnittstellen implementieren:

-   [IInitializeWithStream::Initialize](#iinitializewithstreaminitialize) (stark bevorzugt), [**IInitializeWithFile**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithfile)oder [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem)
-   [Iobjectwithsite](#iobjectwithsite)
-   [IOleWindow](#iolewindow)
-   [IPreviewHandler](#ipreviewhandler)

Wenn Ihr Vorschauhandler vom Host bereitgestellte visuelle Einstellungen wie Hintergrundfarbe und Schriftart unterstützt, muss er auch die folgende Schnittstelle implementieren:

-   [IPreviewHandlerVisuals](#ipreviewhandlervisuals)

In diesem Thema wird davon ausgegangen, dass der Vorschauhandler mit einem Stream initialisiert und für eine bestimmte Dateierweiterung registriert ist.

## <a name="iinitializewithstreaminitialize"></a>IInitializeWithStream::Initialize

Store [**IStream-**](/windows/win32/api/objidl/nn-objidl-istream) und Mode-Parameter, damit Sie die Daten des Elements lesen können, wenn Sie bereit sind, eine Vorschau des Elements anzuzeigen. Laden Sie die Daten nicht in [**Initialize**](/windows/desktop/api/Propsys/nf-propsys-iinitializewithstream-initialize). Laden Sie die Daten direkt vor dem Rendern in [**IPreviewHandler::D oPreview.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-dopreview)

## <a name="iobjectwithsite"></a>Iobjectwithsite

-   [IObjectWithSite::SetSite](#iobjectwithsitesetsite)
-   [IObjectWithSite::GetSite](#iobjectwithsitegetsite)

### <a name="iobjectwithsitesetsite"></a>IObjectWithSite::SetSite

Store [**IUnknown-Zeiger**](/windows/win32/api/unknwn/nn-unknwn-iunknown) für den späteren Zugriff.

Wenn Sie derzeit über einen Verweis auf ein [**IPreviewHandlerFrame-Objekt**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlerframe) verfügen, geben Sie es frei. Verwenden Sie den [**gespeicherten IUnknown-Zeiger**](/windows/win32/api/unknwn/nn-unknwn-iunknown) zum Aufrufen [**von QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) auf der Website für einen neuen **IPreviewHandlerFrame-Verweis.**

Wenn Sie derzeit über eine Zugriffstastentabelle verfügen, zerstören Sie sie. Rufen [**Sie IPreviewHandlerFrame::GetWindowContext**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandlerframe-getwindowcontext) auf, um eine neue Zugriffstastentabelle zu erhalten. Store tabelle. Beachten Sie, dass es nur als Liste von Zugriffstasten verwendet wird, die der Frame unterstützt. Befehle in den Zugriffstasteneinträgen werden ignoriert.

### <a name="iobjectwithsitegetsite"></a>IObjectWithSite::GetSite

Gibt den Standortzeiger zurück, unabhängig davon, was er ist.

## <a name="iolewindow"></a>IOleWindow

-   [IOleWindow::ContextSensitiveHelp](#iolewindowcontextsensitivehelp)
-   [IOleWindow::GetWindow](#iolewindowgetwindow)

### <a name="iolewindowcontextsensitivehelp"></a>IOleWindow::ContextSensitiveHelp

Gibt E \_ NOTIMPL für diese Methode zurück.

### <a name="iolewindowgetwindow"></a>IOleWindow::GetWindow

Wenn das Fenster des Vorschauhandlers derzeit vorhanden ist, geben Sie **den HWND** dieses Fensters und S \_ OK zurück. Wenn das Fenster nicht vorhanden ist, geben Sie E \_ FAIL zurück.

## <a name="ipreviewhandler"></a>IPreviewHandler

-   [IPreviewHandler::SetWindow](#ipreviewhandlersetwindow)
-   [IPreviewHandler::SetRect](#ipreviewhandlersetrect)
-   [IPreviewHandler::D oPreview](#ipreviewhandlerdopreview)
-   [IPreviewHandler::SetFocus](#ipreviewhandlersetfocus)
-   [IPreviewHandler::QueryFocus](#ipreviewhandlerqueryfocus)
-   [IPreviewHandler::TranslateAccelerator](#ipreviewhandlertranslateaccelerator)
-   [IPreviewHandler::Unload](#ipreviewhandlerunload)

### <a name="ipreviewhandlersetwindow"></a>IPreviewHandler::SetWindow

Legen Sie *den hwnd-Parameter* dieser Methode auf das übergeordnete Element des **HWND-Elements Ihres Vorschauhandlers fest.** Diese Methode kann mehrmals aufgerufen werden. Ändern Sie die Größe Ihrer Vorschau, sodass sie nur in dem bereich gerendert wird, der durch den *prc-Parameter beschrieben* wird.

Wenn die Vorschauversion gerendert wird, verwenden Sie die [**IPreviewHandler::SetWindow-Methode,**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setwindow) um das übergeordnete Element der Vorschau zu ändern. Ändern Sie auch den Bereich, in dem die Vorschau gerendert wird.

### <a name="ipreviewhandlersetrect"></a>IPreviewHandler::SetRect

Ändern Sie die Größe Ihrer Vorschau, sodass sie nur in dem Bereich gerendert wird, der vom PRC dieser *Methode beschrieben wird.*

Wenn sich die Vorschauversion im Rendering befindet, ändern Sie den Bereich, in dem die Vorschau gerendert wird.

### <a name="ipreviewhandlerdopreview"></a>IPreviewHandler::D oPreview

Hier wird die eigentliche Arbeit erledigt. Da eine Vorschau dynamisch ist, sollte der Vorschauinhalt nur geladen werden, wenn er benötigt wird. Laden Sie keinen Inhalt in der Initialisierung.

Wenn das Vorschauhandlerfenster nicht vorhanden ist, erstellen Sie es. Die Fenster des Vorschauhandlers sollten unter dem von [**IPreviewHandler::SetWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setwindow)bereitgestellten Fenster sein. Sie sollten die Größe haben, die von **IPreviewHandler::SetWindow** und [**IPreviewHandler::SetRect**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setrect) bereitgestellt wird (was zuletzt aufgerufen wurde).

Sobald Sie über ein Fenster verfügen, laden Sie die Daten aus dem [**IStream,**](/windows/win32/api/objidl/nn-objidl-istream) mit dem der Vorschauhandler initialisiert wurde, und rendern Sie diese Daten im Fenster Ihres Vorschauhandlers.

### <a name="ipreviewhandlersetfocus"></a>IPreviewHandler::SetFocus

Diese Methode wird aufgerufen, wenn der Fokus über eine Registerkartenaktion in den Lesebereich eintritt. Da sie als Vorwärtsregisterkarte oder umgekehrte Registerkarte eingegeben werden kann, verwenden Sie den aktuellen Status der UMSCHALTTASTE, um zu entscheiden, ob die erste oder letzte Registerkartenstopp im Lesebereich den Fokus erhalten soll.

### <a name="ipreviewhandlerqueryfocus"></a>IPreviewHandler::QueryFocus

Diese Methode sollte die [**GetFocus-Funktion**](/windows/win32/api/winuser/nf-winuser-getfocus) aufrufen und das Ergebnis dieses Aufrufs im *phwnd-Parameter* zurückgeben.

### <a name="ipreviewhandlertranslateaccelerator"></a>IPreviewHandler::TranslateAccelerator

Diese Methode wird vom Nachrichtenpump des Prozesses des Vorschauhandlers (unabhängig davon, ob prevhost.exe oder ein benutzerdefinierter lokaler Server) als Reaktion auf Benutzertasteneingaben aufgerufen. Vorschauhandler sollten diese Tastatureingaben verarbeiten oder gemäß dem unten beschriebenen Algorithmus an ihren Host weitersennen.

Da Vorschauversionen jedoch schreibgeschützt sind, sollte die Tastatureingabe minimal sein, und Optimierungen wie diese sind in vielen Fällen nicht erforderlich.

Wenn es sich bei der tastenbeschleunigung, die über die Meldungspumpe an diese Methode übergeben wird, um eine Zugriffstaste handelt, die ihr Vorschauhandler akzeptiert, verarbeiten Sie sie, und geben Sie S \_ OK zurück. Wenn ihr Handler diese Zugriffstaste nicht akzeptiert, kann die Zugriffstastennachricht bis zum zu behandelnden Frame zurück gesendet werden.

Es gibt zwei Optionen zum Weiterleiten von Tastenkombinationen zurück an den Frame:

Das einfachste Modell besteht in der Weitergeleitet aller Tastaturanschläge an den Host mithilfe von [**IPreviewHandlerFrame::TranslateAccelerator**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandlerframe-translateaccelerator). Dies erfolgt im Vorschauhandlerbeispiel, das mit dem Windows Software Development Kit (SDK) bereitgestellt wird. Alle Vorschauhandler mit niedriger Integrität müssen dieses Modell verwenden. Wenn die Zugriffstaste nicht von Ihrem Vorschauhandler behandelt wird, rufen Sie **IPreviewHandlerFrame::TranslateAccelerator** auf, und geben Sie das Ergebnis zurück.

Das andere Modell besteht in der Verwendung einer Zugriffstastentabelle als Optimierung, um zu viele Tastatureingaben über Prozessgrenzen hinweg zu vermeiden:

1.  Wenn [**IObjectWithSite::SetSite für Ihren**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) Vorschauhandler aufgerufen wird, erhalten Sie die Zugriffstastentabelle über [**IPreviewHandlerFrame::GetWindowContext**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandlerframe-getwindowcontext). (Achten Sie darauf, das Handle für die Zugriffstastentabelle frei zu geben, wenn Ihr Vorschauversionsfenster zerstört wird.)
2.  Wenn die Zugriffstaste von Ihrem Vorschauhandler verarbeitet wird, behandeln Sie sie, und geben Sie S \_ OK zurück.
3.  Wenn die Zugriffstaste nicht von Ihrem Vorschauhandler behandelt wird, vergleichen Sie die Nachricht mit [**IsAccelerator**](/windows/win32/api/ole2/nf-ole2-isaccelerator) mit der erhaltenen Zugriffstastentabelle.
4.  Wenn die Zugriffstaste einem Eintrag in dieser Zugriffstastentabelle entspricht, rufen Sie [**IPreviewHandlerFrame::TranslateAccelerator**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandlerframe-translateaccelerator) auf, und geben Sie das Ergebnis zurück.
5.  Wenn die Zugriffstaste nicht mit einem Eintrag in der Zugriffstastentabelle übereinstimmen soll, geben Sie S \_ FALSE zurück.

### <a name="ipreviewhandlerunload"></a>IPreviewHandler::Unload

Wenn diese Methode aufgerufen wird, beenden Sie jedes Rendering, geben Sie alle Ressourcen frei, die durch Lesen von Daten aus dem Stream zugeordnet sind, und geben Sie [**den IStream**](/windows/win32/api/objidl/nn-objidl-istream) selbst frei.

Nachdem diese Methode aufgerufen wurde, muss der Handler erneut initialisiert werden, bevor versucht wird, [**IPreviewHandler::D oPreview erneut**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-dopreview) aufrufen.

## <a name="ipreviewhandlervisuals"></a>IPreviewHandlerVisuals

-   [IPreviewHandlerVisuals::SetBackgroundColor](#ipreviewhandlervisualssetbackgroundcolor)
-   [IPreviewHandlerVisuals::SetFont](#ipreviewhandlervisualssetfont)
-   [IPreviewHandlerVisuals::SetTextColor](#ipreviewhandlervisualssettextcolor)

Diese Methoden sollten implementiert werden, wenn sie den Vorschauhandler anweisen, auf die Farb- und Schriftartschemas des Hosts zu reagieren. Der Host fragt den Handler für [**IPreviewHandlerVisuals ab.**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlervisuals) Wenn der Host unterstützt wird, stellt er Farbe, Schriftart und Textfarbe zur Anwendung.

### <a name="ipreviewhandlervisualssetbackgroundcolor"></a>IPreviewHandlerVisuals::SetBackgroundColor

Store diese Farbe, und verwenden Sie sie während des Renderings, wenn Sie eine Hintergrundfarbe bereitstellen möchten. So füllen Sie beispielsweise das Fenster aus, wenn der Handler in einem Bereich gerendert wird, der kleiner als der von [**IPreviewHandler::SetWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setwindow) und [**IPreviewHandler::SetRect**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setrect)bereitgestellte Bereich ist. Beachten Sie jedoch, dass Sie nicht außerhalb des von diesen Methoden bereitgestellten Bereichs zeichnen sollten.

Wenn diese Methode aufgerufen wird, während die Vorschauversion bereits gerendert wird, sollte das Rendering mit dieser Hintergrundfarbe neu gestartet werden.

### <a name="ipreviewhandlervisualssetfont"></a>IPreviewHandlerVisuals::SetFont

Store diese Schriftartinformationen, und verwenden Sie sie während des Renderings, wenn Sie Text anzeigen möchten, der mit den aktuellen Windows Vista-Einstellungen konsistent ist.

### <a name="ipreviewhandlervisualssettextcolor"></a>IPreviewHandlerVisuals::SetTextColor

Store diese Textfarbinformationen, und verwenden Sie sie beim Rendern, wenn Sie Text konsistent mit den aktuellen Windows Vista-Einstellungen anzeigen möchten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vorschauhandler und Shell-Vorschauhost](preview-handlers.md)
</dt> <dt>

[Registrieren eines Vorschauhandlers](how-to-register-a-preview-handler.md)
</dt> <dt>

[Richtlinien für Vorschauhandler](preview-handler-guidelines.md)
</dt> </dl>

 

 
