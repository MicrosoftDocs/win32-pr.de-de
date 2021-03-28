---
description: In diesem Thema werden die spezifischen Schnittstellen und Methoden erläutert, die zum Erstellen eines Vorschau Handlers erforderlich sind.
ms.assetid: 6c240a63-c184-4b65-9483-794f5de4d695
title: Entwickeln von Vorschau Handlern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a309873cf082071d5f426ce0ba6d039107c59665
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342849"
---
# <a name="building-preview-handlers"></a>Entwickeln von Vorschau Handlern

In diesem Thema werden die spezifischen Schnittstellen und Methoden erläutert, die zum Erstellen eines Vorschau Handlers erforderlich sind.

Ein Vorschau Handler muss die folgenden Schnittstellen implementieren:

-   [IInitializeWithStream:: Initialize](#iinitializewithstreaminitialize) (stark bevorzugt), [**IInitializeWithFile**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithfile)oder [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem)
-   [IObjectWithSite](#iobjectwithsite)
-   [IOleWindow](#iolewindow)
-   [IPreviewHandler](#ipreviewhandler)

Wenn Ihr Vorschau Handler visuelle Einstellungen unterstützt, die vom Host bereitgestellt werden, z. b. Hintergrundfarbe und Schriftart, muss auch die folgende Schnittstelle implementiert werden:

-   [IPreviewHandlerVisuals](#ipreviewhandlervisuals)

In diesem Thema wird davon ausgegangen, dass der Vorschau Handler mit einem Stream initialisiert ist und für eine bestimmte Dateinamenerweiterung registriert ist.

## <a name="iinitializewithstreaminitialize"></a>IInitializeWithStream:: Initialize

Speichern Sie die Parameter [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) und Mode, damit Sie die Daten des Elements lesen können, wenn Sie bereit sind, das Element in der Vorschau anzuzeigen. Laden Sie die Daten nicht in [**Initialize**](/windows/desktop/api/Propsys/nf-propsys-iinitializewithstream-initialize). Laden Sie die Daten in [**IPreviewHandler::D opreview**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-dopreview) direkt vor dem Rendering.

## <a name="iobjectwithsite"></a>IObjectWithSite

-   [IObjectWithSite:: SetSite](#iobjectwithsitesetsite)
-   [IObjectWithSite:: GetSite](#iobjectwithsitegetsite)

### <a name="iobjectwithsitesetsite"></a>IObjectWithSite:: SetSite

Speichert den [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Zeiger für den späteren Zugriff.

Wenn Sie derzeit über einen Verweis auf ein [**IPreviewHandlerFrame**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlerframe) -Objekt verfügen, geben Sie es frei. Verwenden Sie den gespeicherten [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Zeiger, um [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für einen neuen **IPreviewHandlerFrame** -Verweis auf der Website aufzurufen.

Wenn Sie derzeit über eine Zugriffstasten Tabelle verfügen, zerstören Sie Sie. Rufen Sie [**IPreviewHandlerFrame:: GetWindowContext**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandlerframe-getwindowcontext) auf, um eine neue Zugriffstasten Tabelle abzurufen. Speichern Sie diese Tabelle. Beachten Sie, dass Sie nur als Liste von Zugriffstasten verwendet wird, die vom Frame unterstützt werden. Befehle in den Zugriffstasten Einträgen werden ignoriert.

### <a name="iobjectwithsitegetsite"></a>IObjectWithSite:: GetSite

Gibt den Website Zeiger zurück.

## <a name="iolewindow"></a>IOleWindow

-   [IOleWindow:: ContextSensitiveHelp](#iolewindowcontextsensitivehelp)
-   [IOleWindow:: GetWindow](#iolewindowgetwindow)

### <a name="iolewindowcontextsensitivehelp"></a>IOleWindow:: ContextSensitiveHelp

Gibt E \_ notimpl für diese Methode zurück.

### <a name="iolewindowgetwindow"></a>IOleWindow:: GetWindow

Wenn das Fenster des Vorschau Handlers aktuell vorhanden ist, geben Sie das **HWND** dieses Fensters und s \_ OK zurück. Wenn das Fenster nicht vorhanden ist, wird "E Fail" zurückgegeben \_ .

## <a name="ipreviewhandler"></a>IPreviewHandler

-   [IPreviewHandler:: SetWindow](#ipreviewhandlersetwindow)
-   [IPreviewHandler:: SetRect](#ipreviewhandlersetrect)
-   [IPreviewHandler::D opreview](#ipreviewhandlerdopreview)
-   [IPreviewHandler:: SetFocus](#ipreviewhandlersetfocus)
-   [IPreviewHandler:: QueryFocus](#ipreviewhandlerqueryfocus)
-   [IPreviewHandler:: TranslateAccelerator](#ipreviewhandlertranslateaccelerator)
-   [IPreviewHandler:: entladen](#ipreviewhandlerunload)

### <a name="ipreviewhandlersetwindow"></a>IPreviewHandler:: SetWindow

Legen Sie den *HWND* -Parameter dieser Methode auf das übergeordnete Element des **HWND** Ihres Vorschau Handlers fest. Diese Methode kann mehrmals aufgerufen werden. Ändern Sie die Größe Ihrer Vorschau, sodass Sie nur in dem Bereich gerendert wird, der vom *PRC* -Parameter beschrieben wird

Wenn der Vorschau gerade gerendert wird, verwenden Sie die [**IPreviewHandler:: SetWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setwindow) -Methode, um das übergeordnete Element der Vorschau zu ändern. Ändern Sie auch den Bereich, in dem der Vorschau gerendert wird.

### <a name="ipreviewhandlersetrect"></a>IPreviewHandler:: SetRect

Ändern Sie die Größe Ihrer Vorschau, sodass Sie nur in dem von der Volks *Republik China* beschriebenen Bereich gerendert wird.

Wenn der Vorschau gerade gerendert wird, ändern Sie den Bereich, in dem der Vorschau gerendert wird.

### <a name="ipreviewhandlerdopreview"></a>IPreviewHandler::D opreview

An dieser Stelle wird die eigentliche Arbeit erledigt. Da eine Vorschau dynamisch ist, sollte der Vorschau Inhalt nur geladen werden, wenn er benötigt wird. Laden Sie keinen Inhalt in die Initialisierung.

Wenn das vorschauhandlerfenster nicht vorhanden ist, erstellen Sie es. Die Fenster Ihres Vorschau Handlers sollten untergeordnete Elemente des Fensters sein, das von [**IPreviewHandler:: SetWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setwindow)bereitgestellt wird. Sie sollten die Größe aufweisen, die von **IPreviewHandler:: SetWindow** und [**IPreviewHandler:: SetRect**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setrect) bereitgestellt wird (je nachdem, was zuletzt aufgerufen wurde).

Wenn Sie über ein Fenster verfügen, laden Sie die Daten aus dem [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) , mit dem der Vorschau Handler initialisiert wurde, und Rendering Sie diese Daten im Fenster des Vorschau Handlers.

### <a name="ipreviewhandlersetfocus"></a>IPreviewHandler:: SetFocus

Diese Methode wird aufgerufen, wenn der Fokus über eine Tabstopp Aktion in den Lesebereich wechselt. Da es als vorwärts Registerkarte oder umgekehrte Registerkarte eingegeben werden kann, verwenden Sie den aktuellen Zustand der UMSCHALTTASTE, um zu entscheiden, ob der erste oder letzte Tabstopp im Lesebereich den Fokus erhalten soll.

### <a name="ipreviewhandlerqueryfocus"></a>IPreviewHandler:: QueryFocus

Diese Methode sollte die [**GetFocus**](/windows/win32/api/winuser/nf-winuser-getfocus) -Funktion aufrufen und das Ergebnis dieses Aufrufes im *phwnd* -Parameter zurückgeben.

### <a name="ipreviewhandlertranslateaccelerator"></a>IPreviewHandler:: TranslateAccelerator

Diese Methode wird von der Meldungs Pumpe des vorschauhandlerprozesses (unabhängig davon, ob prevhost.exe oder ein benutzerdefinierter lokaler Server) als Reaktion auf Benutzer Tastatureingaben aufgerufen wird. Vorschau Handler sollten diese Tastatureingaben verarbeiten oder entsprechend dem unten beschriebenen Algorithmus an Ihren Host weiterleiten.

Da Vorschau Versionen jedoch schreibgeschützt sind, sollten Tastatureingaben minimal sein, und Optimierungen wie diese sind in vielen Fällen nicht erforderlich.

Wenn die Zugriffstaste, die an diese Methode über die Meldungs Pumpe übergeben wird, eine Zugriffstaste ist, die der Vorschau Handler annimmt, dann verarbeiten und S OK zurückgeben \_ . Wenn Ihr Handler diese Zugriffstaste nicht akzeptiert, kann die Zugriffstasten Meldung zurückgesendet werden, wenn der Frame behandelt wird.

Es gibt zwei Optionen für die Weiterleitung von Tastatur Accelerators an den Frame:

Das einfachste Modell besteht darin, mithilfe von [**IPreviewHandlerFrame:: TranslateAccelerator**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandlerframe-translateaccelerator)alle Tastatureingaben an den Host weiterzuleiten. Dies erfolgt im Vorschau handlerbeispiel, das mit dem Windows Software Development Kit (SDK) bereitgestellt wird. Alle Vorschau Handler mit niedriger Integrität müssen dieses Modell verwenden. Wenn die Zugriffstaste nicht von Ihrem Vorschau Handler behandelt wird, rufen Sie **IPreviewHandlerFrame:: TranslateAccelerator** auf, und geben Sie das Ergebnis zurück.

Das andere Modell ist die Verwendung einer Zugriffstasten Tabelle als Optimierung, um zu vermeiden, dass zu viele Tastatureingaben über Prozess Grenzen hinweg gesendet werden:

1.  Wenn [**IObjectWithSite:: SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) für Ihren Vorschau Handler aufgerufen wird, rufen Sie die Zugriffstasten Tabelle über [**IPreviewHandlerFrame:: GetWindowContext**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandlerframe-getwindowcontext)ab. (Achten Sie darauf, das Handle für die Zugriffstasten Tabelle freizugeben, wenn der Vorschau zerstört wird.)
2.  Wenn die Zugriffstaste von Ihrem Vorschau Handler behandelt wird, behandeln Sie Sie, und geben Sie "S OK" zurück \_ .
3.  Wenn die Zugriffstaste nicht von Ihrem Vorschau Handler behandelt wird, vergleichen Sie die Nachricht mithilfe von [**isaccelerator**](/windows/win32/api/ole2/nf-ole2-isaccelerator) mit der erworbenen Zugriffstasten Tabelle.
4.  Wenn die Zugriffstaste mit einem Eintrag in der Zugriffstasten Tabelle übereinstimmt, rufen Sie [**IPreviewHandlerFrame:: TranslateAccelerator**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandlerframe-translateaccelerator) auf, und geben Sie das Ergebnis zurück.
5.  Wenn die Zugriffstaste keinem Eintrag in der Zugriffstasten Tabelle entspricht, gibt S \_ false zurück.

### <a name="ipreviewhandlerunload"></a>IPreviewHandler:: entladen

Wenn diese Methode aufgerufen wird, beenden Sie jedes Rendering, geben Sie alle Ressourcen frei, die durch das Lesen von Daten aus dem Stream zugeordnet sind, und geben Sie den [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) selbst frei.

Nachdem diese Methode aufgerufen wurde, muss der Handler erneut initialisiert werden, bevor versucht wird, [**IPreviewHandler::D opreview**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-dopreview) erneut aufzurufen.

## <a name="ipreviewhandlervisuals"></a>IPreviewHandlerVisuals

-   [IPreviewHandlerVisuals:: SetBackgroundColor](#ipreviewhandlervisualssetbackgroundcolor)
-   [IPreviewHandlerVisuals:: SetFont](#ipreviewhandlervisualssetfont)
-   [IPreviewHandlerVisuals:: SetTextColor](#ipreviewhandlervisualssettextcolor)

Diese Methoden sollten implementiert werden, wenn der Vorschau Handler so umgeleitet wird, dass er auf die Farb-und Schriftart Schemas des Hosts antwortet. Der Host fragt den Handler nach [**IPreviewHandlerVisuals**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlervisuals)ab. Wenn die Unterstützung gefunden wird, stellt der Host die Farbe, die Schriftart und die Textfarbe bereit.

### <a name="ipreviewhandlervisualssetbackgroundcolor"></a>IPreviewHandlerVisuals:: SetBackgroundColor

Speichern Sie diese Farbe, und verwenden Sie Sie während des Renderings, wenn Sie eine Hintergrundfarbe bereitstellen möchten. Zum Beispiel, um das Fenster auszufüllen, wenn der Handler in einen Bereich gerendert wird, der kleiner als der von [**IPreviewHandler:: SetWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setwindow) und [**IPreviewHandler:: SetRect**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setrect)bereitgestellte Bereich ist. Beachten Sie jedoch, dass Sie nicht außerhalb des Bereichs, der von diesen Methoden bereitgestellt wird, zeichnen sollten.

Wenn diese Methode aufgerufen wird, während die Vorschau bereits gerendert wird, sollte das Rendering mit dieser Hintergrundfarbe neu gestartet werden.

### <a name="ipreviewhandlervisualssetfont"></a>IPreviewHandlerVisuals:: SetFont

Speichern Sie diese Schriftart Informationen, und verwenden Sie Sie während des Renderings, wenn Sie Text in Übereinstimmung mit den aktuellen Windows Vista-Einstellungen anzeigen möchten.

### <a name="ipreviewhandlervisualssettextcolor"></a>IPreviewHandlerVisuals:: SetTextColor

Speichern Sie diese Text Farbinformationen, und verwenden Sie Sie während des Renderings, wenn Sie Text in Übereinstimmung mit den aktuellen Windows Vista-Einstellungen anzeigen möchten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vorschau Handler und Shell-Vorschau Host](preview-handlers.md)
</dt> <dt>

[Registrieren eines Vorschau Handlers](how-to-register-a-preview-handler.md)
</dt> <dt>

[Vorschau der handlerrichtlinien](preview-handler-guidelines.md)
</dt> </dl>

 

 
