---
title: Implementieren einer Ordneransicht
description: Windows Shell stellt eine Standard Implementierung der Ordneransicht bereit, die als defview bezeichnet wird, sodass Sie einen Großteil der Arbeit bei der Implementierung Ihrer eigenen Namespace Erweiterung vermeiden können.
ms.assetid: 8c6712d8-c3cb-4450-8277-3a8675622651
keywords:
- Ordner Ansichts Objekt
- Ishellview
- Ishellbrowser, Ordner Ansichts Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48c7b86d587154a034f276d4bdab903e5337ed4b
ms.sourcegitcommit: 469b6de41e2a565b7ead231d7f282ec4071ac158
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/11/2020
ms.locfileid: "104391161"
---
# <a name="implementing-a-folder-view"></a>Implementieren einer Ordneransicht

Windows Shell stellt eine Standard Implementierung der Ordneransicht bereit, die als defview bezeichnet wird, sodass Sie einen Großteil der Arbeit bei der Implementierung Ihrer eigenen Namespace Erweiterung vermeiden können. Da einige Ansichts Features nicht durch benutzerdefinierte Ansichten erreicht werden können, wird häufig empfohlen, anstelle einer benutzerdefinierten Ansicht das standardmäßige Systemordner-Ansichts Objekt zu verwenden. Weitere Informationen finden Sie unter [**shkreateshellfolderview**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview). Im weiteren Verlauf dieses Themas wird die Implementierung einer benutzerdefinierten Ordneransicht erläutert, die keine neueren Ansichts Features unterstützt.

Anders als in der Strukturansicht wird der Inhalt einer Ordneransicht von Windows-Explorer nicht verwaltet. Stattdessen hostet das Fenster "Ordneransicht" ein untergeordnetes Fenster, das durch das Ordner Objekt bereitgestellt wird. Das Ordner Objekt ist dafür verantwortlich, ein Ordner Ansichts Objekt zu erstellen, um den Inhalt des Ordners im untergeordneten Fenster anzuzeigen.

Der Schlüssel zum Implementieren eines Ordner Ansichts Objekts ist die [**ishellview**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) -Schnittstelle. Diese Schnittstelle wird von Windows-Explorer verwendet, um mit dem Ordner Ansichts Objekt zu kommunizieren. Vor dem Anzeigen einer Ordneransicht ruft der Windows-Explorer die [**IShellFolder::**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-createviewobject) -Methode des Ordner Objekts auf, wobei *riid* auf IID \_ ishellview festgelegt ist. Erstellen Sie ein Ordner Ansichts Objekt, und geben Sie dessen **ishellview** -Schnittstelle zurück Das Ordner Ansichts Objekt muss dann ein untergeordnetes Fenster des Fensters Ordneransicht erstellen und das untergeordnete Fenster verwenden, um Informationen zum Inhalt des Ordners anzuzeigen.

Zusätzlich zur Steuerung der Anzeige von Daten können Erweiterungen auch eine Reihe von Features von Windows Explorer anpassen. Beispielsweise kann eine Erweiterung der Symbolleiste oder der Menüleiste Elemente hinzufügen oder Informationen auf der Statusleiste anzeigen.

-   [Das Objekt der Ordneransicht](#the-folder-view-object)
-   [Initialisieren des Ordner Ansichts Objekts](#initializing-the-folder-view-object)
-   [Anzeigen der Ordneransicht](#displaying-the-folder-view)
-   [Implementieren von ishellview](#implementing-ishellview)
    -   [Addpropertysheetpages](#addpropertysheetpages)
    -   [Getcurrentinfo](#getcurrentinfo)
    -   [Aktualisieren](#refresh)
    -   [SaveViewState](#saveviewstate)
    -   [Translateacelerator](#translateacelerator)
-   [Verwenden von ishellbrowser für die Kommunikation mit Windows-Explorer](#using-ishellbrowser-to-communicate-with-windows-explorer)
    -   [Ändern der Windows Explorer-Menüleiste](#modifying-the-windows-explorer-menu-bar)
    -   [Ändern der Windows-Explorer-Symbolleiste](#modifying-the-windows-explorer-toolbar)
    -   [Ändern der Windows Explorer-Status Leiste](#modifying-the-windows-explorer-status-bar)
    -   [Speichern von Ansichts spezifischen Informationen](#storing-view-specific-information)

## <a name="the-folder-view-object"></a>Das Objekt der Ordneransicht

Ein Ordner Ansichts Objekt ist ein Component Object Model (com)-Objekt, das eine [**ishellview**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) -Schnittstelle verfügbar macht. Dieses Objekt ist für Folgendes zuständig:

-   Erstellen eines untergeordneten Fensters im Fenster "Ordneransicht" und verwenden dieses Fensters zum Anzeigen der Inhalte des Ordners.
-   Verarbeiten der Kommunikation mit Windows-Explorer.
-   Hinzufügen Ordner spezifischer Befehle zur Windows Explorer-Menüleiste und-Symbolleiste und zum Behandeln dieser Befehle, wenn Sie ausgewählt werden.
-   Verwalten der Benutzerinteraktion mit dem Fenster der Ordneransicht, z. b. Anzeigen von Kontextmenüs oder behandeln von Drag & Drop-Vorgängen.

In diesem Dokument werden die ersten drei Themen erläutert. Da die Benutzerinteraktion mit der Ordneransicht in Ihrem untergeordneten Fenster stattfindet, ist das Ordner Ansichts Objekt für die Verarbeitung wie für jedes andere Fenster verantwortlich.

Windows-Explorer fordert ein Ordner Ansichts Objekt an, indem das [**IShellFolder:: CreateViewObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-createviewobject) Ihres Ordner Objekts aufgerufen wird, dessen *riid* auf IID \_ ishellview festgelegt ist. Die Vorgehensweise zum Erstellen einer Ordneransicht lautet wie folgt:

1.  Ihr Folder-Objekt erstellt eine neue Instanz des Ordner Ansichts Objekts und gibt einen Zeiger auf seine [**ishellview**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) -Schnittstelle zurück.
2.  Der Windows-Explorer initialisiert das Ordner Ansichts Objekt durch Aufrufen der [**ishellview:: createviewwindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-createviewwindow) -Methode. Erstellen Sie ein untergeordnetes Fenster des Fensters Ordneransicht, und geben Sie das zugehörige Handle an Windows-Explorer zurück.
3.  Das Ordner Ansichts Objekt verwendet die [**ishellbrowser**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser) -Schnittstelle von Windows Explorer, um die Windows-Explorer-Symbolleiste, die Menüleiste und die Statusleiste anzupassen.
4.  Das Ordner Ansichts Objekt zeigt den Inhalt des Ordners im untergeordneten Fenster an.
5.  Das Ordner Ansichts Objekt behandelt die Benutzerinteraktion mit der Ordneransicht und allen Ordner spezifischen Symbolleisten-oder Menüleisten Elementen.

## <a name="initializing-the-folder-view-object"></a>Initialisieren des Ordner Ansichts Objekts

Der Windows-Explorer initialisiert das Ordner Ansichts Objekt durch Aufrufen der [**ishellview:: createviewwindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-createviewwindow) -Methode. Die Parameter der Methode stellen dem Ordner Ansichts Objekt die Informationen zur Verfügung, die es benötigt, um das untergeordnete Fenster zu erstellen, das zum Anzeigen des Ordner Inhalts verwendet wird:

-   Ein Zeiger auf die [**ishellview**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) -Schnittstelle des vorherigen Ordner Ansichts Objekts. Dieser Parameter kann auf **null** festgelegt werden.
-   Eine [**foldersettings**](/windows/desktop/api/shobjidl_core/ns-shobjidl_core-foldersettings) -Struktur, die die Einstellungen der vorherigen Ordneransicht enthält.
-   Ein Zeiger auf die [**ishellbrowser**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser) -Schnittstelle von Windows Explorer.
-   Eine [Rect](/previous-versions//ms536136(v=vs.85)) -Struktur mit den Abmessungen des Fensters der Ordneransicht.

Die [**ishellview:: kreateviewwindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-createviewwindow) -Methode wird aufgerufen, bevor das vorherige Ordner Ansichts Objekt zerstört wird. Der [**ishellview**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) -Schnittstellen Zeiger ermöglicht Ihnen somit die Kommunikation mit dem vorherigen Ordner Ansichts Objekt. Diese Schnittstelle ist vor allem dann nützlich, wenn der vorherige Ordner zu ihrer Erweiterung gehört und dasselbe Anzeige Schema verwendet hat. Wenn dies der Fall ist, können Sie mit dem vorherigen Ordner Ansichts Objekt kommunizieren, indem Sie private Einstellungen austauschen.

Eine einfache Möglichkeit, um zu bestimmen, ob der [**ishellview**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) -Zeiger zu ihrer Erweiterung gehört, besteht darin, dass alle Ordner Ansichts Objekte eine private Schnittstelle verfügbar machen. Nennen Sie [ishellview:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) , um die private Schnittstelle anzufordern, und überprüfen Sie den Rückgabewert, um zu bestimmen, ob das Ordner Ansichts Objekt eine ihrer Werte ist. Sie können dann eine private Methode für diese Schnittstelle verwenden, um Informationen auszutauschen.

Die [**foldersettings**](/windows/desktop/api/shobjidl_core/ns-shobjidl_core-foldersettings) -Struktur enthält die Anzeigeeinstellungen der vorherigen Ordneransicht. Die primäre Einstellung ist der Anzeigemodus: großes Symbol, kleines Symbol, Liste oder Details. Es gibt auch ein Flag, das die Einstellungen einer Vielzahl von Anzeigeoptionen enthält, z. b., ob die Ansicht linksbündig ausgerichtet werden soll. In Ihrer Ordner Anzeige sollten diese Einstellungen so weit wie möglich befolgt werden, damit Benutzer eine konsistente Benutzerumgebung erhalten, wenn Sie von einem Ordner in einen anderen wechseln. Sie sollten diese Struktur speichern und aktualisieren, wenn sich die Einstellungen ändern. In Windows Explorer wird [**ishellview:: getcurrentinfo**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-getcurrentinfo) aufgerufen, um den aktuellen Wert dieser Struktur zu erhalten, bevor die nächste Ordneransicht geöffnet wird.

Die [**ishellbrowser**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser) -Schnittstelle wird von Windows Explorer verfügbar gemacht. Diese Schnittstelle ist ein Begleitelement von [**ishellview**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) und ermöglicht es einem Ordner Ansichts Objekt, mit Windows-Explorer zu kommunizieren. Es gibt keine andere Möglichkeit, diesen Schnittstellen Zeiger abzurufen, daher sollte Ihr Ordner Ansichts Objekt ihn zur späteren Verwendung speichern. Insbesondere müssen Sie [ishellbrowser:: GetWindow](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) aufrufen, um das Ansichts Fenster des übergeordneten Ordners abzurufen, das Sie zum Erstellen Ihres untergeordneten Fensters verwenden werden. Beachten Sie, dass die ishellbrowser:: GetWindow-Methode nicht in der **ishellbrowser** -Dokumentation enthalten ist, da Sie von [IOleWindow](/windows/win32/api/oleidl/nn-oleidl-iolewindow)geerbt wird. Denken Sie nach dem Speichern des Schnittstellen Zeigers daran, [ishellbrowser:: adressf](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) aufzurufen, um den Verweis Zähler der Schnittstelle zu erhöhen. Wenn Sie die Schnittstelle nicht mehr benötigen, wenden Sie sich an [ishellbrowser:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).

So erstellen Sie ein untergeordnetes Fenster:

1.  Überprüfen Sie die [**foldersettings**](/windows/desktop/api/shobjidl_core/ns-shobjidl_core-foldersettings) -und [Rect](/previous-versions//ms536136(v=vs.85)) -Strukturen.
2.  Rufen Sie bei Bedarf private Einstellungen aus dem vorherigen Ordner Ansichts Objekt ab.
3.  Rufen Sie [ishellbrowser:: GetWindow](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) auf, um das Fenster für die übergeordnete Ordneransicht abzurufen.
4.  Erstellen Sie ein untergeordnetes Element des Fensters Ordneransicht, das Sie im vorherigen Schritt abgerufen haben, und geben Sie es an Windows-Explorer zurück

## <a name="displaying-the-folder-view"></a>Anzeigen der Ordneransicht

Nachdem Sie das untergeordnete Fenster erstellt und an den Windows-Explorer zurückgegeben haben, können Sie den Inhalt des Ordners anzeigen. In der Regel zeigen Erweiterungen Ihre Informationen an, indem das untergeordnete Fenster entweder ein Listenansicht-Steuerelement oder ein **Webbrowser-Steuer** Element [hostet](../controls/list-view-control-reference.md) . Mit dem Listenansicht-Steuerelement können Sie die klassische Windows-Explorer- [Ansicht](web-view.md)replizieren. Das WebBrowser-Steuerelement ermöglicht die Verwendung eines dynamischen HTML-Dokuments (DHTML) zum Anzeigen Ihrer Informationen, ähnlich wie die Windows Explorer-Webansicht. Weitere Informationen finden Sie in der Dokumentation zu diesen Steuerelementen.

Das Fenster "Ordneransicht" ist immer vorhanden, auch wenn es nicht den Fokus besitzt. Daher sollten Sie drei Zustände für das untergeordnete Fenster aufbewahren:

-   Aktiviert mit dem Fokus. Die Ordneransicht wurde erstellt und hat den Fokus. Legen Sie die Menüleiste oder die Symbolleisten Elemente fest, die für einen Fokus Zustand geeignet sind.
-   Aktiviert ohne Fokus. Die Ordneransicht wurde erstellt und ist aktiv, aber Sie hat keinen Fokus. Legen Sie die Menüleiste oder die Symbolleisten Elemente fest, die für den Zustand "nicht fokussiert" geeignet sind. Lassen Sie alle Elemente aus, die für die Auswahl von Elementen in der Ordneransicht gelten.
-   Deaktiviert. Die Ordneransicht wird zerstört. Entfernen Sie alle Ordner spezifischen Menü Elemente.

Windows-Explorer benachrichtigt das Ordner Ansichts Objekt, wenn der Fenster Zustand durch Aufrufen von [**ishellview:: uiaktivierungs**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-uiactivate)geändert wird. Im Gegenzug sollte das Ordner Ansichts Objekt Windows-Explorer Benachrichtigen, wenn ein Benutzer das Fenster "Ordneransicht" durch Aufrufen von " [**ishellbrowser:: onviewwindowactive**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-onviewwindowactive)" aktiviert. Weitere Informationen zu dieser Schnittstelle finden [Sie unter Verwenden von ishellbrowser für die Kommunikation mit Windows-Explorer](#using-ishellbrowser-to-communicate-with-windows-explorer).

Während die Ordneransicht aktiv ist, müssen Sie alle Windows-Meldungen, z. b. die [WM- \_ Größe](../winmsg/wm-size.md), verarbeiten, die zu Ihrem untergeordneten Fenster gehören. Die Fenster Prozedur empfängt auch [WM- \_ Befehls](../menurc/wm-command.md) Meldungen für alle Elemente, die Sie der Windows-Explorer-Menüleiste oder der Symbolleiste hinzugefügt haben.

Nach dem Erstellen der Ordneransicht ruft Windows-Explorer die [**ishellview**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) -Schnittstelle des Ordner Ansichts Objekts auf, um eine Vielzahl von Informationen zu übergeben. Das Objekt muss seine Anzeige entsprechend ändern. Wenn die Ordneransicht zerstört wird, benachrichtigt Windows Explorer das Ordner Ansichts Objekt durch Aufrufen seiner [**ishellview::D estroyviewwindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-destroyviewwindow) -Methode.

## <a name="implementing-ishellview"></a>Implementieren von ishellview

Nachdem das Ordner Objekt erstellt wurde, ruft Windows Explorer verschiedene [**ishellview**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) -Methoden auf, um Informationen anzufordern oder das Objekt über eine Änderung des Windows-Explorer-Status zu benachrichtigen. In diesem Abschnitt wird beschrieben, wie diese **ishellview** -Methoden implementiert werden. Die übrigen Methoden werden für speziellere Zwecke verwendet, z. b. das Dialogfeld "Datei öffnen" (allgemein). Weitere Informationen finden Sie in der **ishellview** -Dokumentation.

### <a name="addpropertysheetpages"></a>Addpropertysheetpages

Wenn ein Benutzer im Menü Extras von Windows **-Explorer** **Ordneroptionen** auswählt, wird ein Eigenschaften Blatt angezeigt, das es dem Benutzer ermöglicht, die Ordneroptionen zu ändern. Windows-Explorer Ruft die [**ishellview:: addpropertysheetpages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-addpropertysheetpages) -Methode Ihres Ordner Ansichts Objekts auf, damit Sie eine Seite zu diesem Eigenschaften Blatt hinzufügen können.

Windows-Explorer übergibt einen Zeiger auf eine [addpropsheetpageproc](/windows/win32/api/prsht/nc-prsht-lpfnaddpropsheetpage) -Rückruffunktion im *lpfn* -Parameter von [**ishellview:: addpropertysheetpages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-addpropertysheetpages). Rufen Sie die Seite "" auf [, um die](/windows/win32/api/prsht/nf-prsht-createpropertysheetpagea) Seite zu erstellen, und rufen Sie dann "addpropsheetpageproc" auf, um Sie dem Eigenschaften Blatt hinzuzufügen. Weitere Informationen zum Behandeln von Eigenschaften Blättern finden Sie unter [Eigenschaften Blätter](../controls/property-sheets.md).

### <a name="getcurrentinfo"></a>Getcurrentinfo

Wenn der Benutzer von einem Ordner in einen anderen wechselt, versucht Windows Explorer, eine ähnliche Ordneransicht zu verwalten. Wenn beispielsweise in der vorherigen Ordneransicht große Symbole angezeigt werden, sollte auch das nächste angezeigt werden. Wenn Windows Explorer [**ishellview:: dashateviewwindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-createviewwindow) aufruft, um das Ordner Ansichts Objekt zu initialisieren, empfängt die Methode eine [**foldersettings**](/windows/desktop/api/shobjidl_core/ns-shobjidl_core-foldersettings) -Struktur. Diese Struktur enthält Informationen, mit denen Sie die Anzeige der Ordneransicht mit der vorherigen Ordneransicht konsistent gestalten können.

Speichern Sie die [**foldersettings**](/windows/desktop/api/shobjidl_core/ns-shobjidl_core-foldersettings) -Struktur, um sicherzustellen, dass die nächste Ansicht mit der aktuellen Ansicht konsistent ist. Wenn sich die Ansicht ändert, z.b. von großen zu kleinen Symbolen, aktualisieren Sie die Struktur entsprechend. Vor dem Wechseln von Ansichten wird in Windows-Explorer [**ishellview:: getcurrentinfo**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-getcurrentinfo) aufgerufen, um die aktuellen **foldersettings** -Werte anzufordern, um Sie an das nächste Ordner Ansichts Objekt zu übergeben.

### <a name="refresh"></a>Aktualisieren

Der Benutzer kann sicherstellen, dass in der Ordneransicht der aktuelle Zustand des Ordners angezeigt wird, indem Sie im Menü **Ansicht** die Option **Aktualisieren** auswählen oder die Taste F5 drücken. Wenn der Benutzer dies tut, ruft Windows-Explorer die [**ishellview:: Refresh**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-refresh) -Methode auf. Das Ordner Ansichts Objekt sollte die Anzeige der Ordneransicht sofort aktualisieren.

### <a name="saveviewstate"></a>SaveViewState

Windows-Explorer Ruft die [**ishellview:: SaveViewState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-saveviewstate) -Methode auf, um das Ordner Ansichts Objekt zum Speichern des Ansichts Zustands aufzufordern. Sie können dann den Zustand wiederherstellen, wenn der Ordner das nächste Mal angezeigt wird. Die bevorzugte Methode zum Speichern eines Ansichts Zustands ist das Aufrufen der [**ishellbrowser:: getviewstatestream**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-getviewstatestream) -Methode. Diese Methode gibt eine [IStream](/windows/win32/api/objidl/nn-objidl-istream) -Schnittstelle zurück, die das Ordner Ansichts Objekt verwenden kann, um seinen Zustand zu speichern. Wenn Sie eine weitere Ordneransicht erstellen, können Sie dieselbe **ishellbrowser:: getviewstatestream** -Methode aufrufen, um einen IStream-Zeiger zu erhalten, mit dem Sie die in den vorherigen Ordner Sichten gespeicherten Einstellungen lesen können.

### <a name="translateacelerator"></a>Translateacelerator

Wenn der Benutzer eine Tastenkombination drückt, übergibt Windows Explorer die Nachricht durch Aufrufen von [**ishellview:: TranslateAccelerator**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-translateaccelerator)an das Ordner Ansichts Objekt. Gibt den Wert "false" zurück \_ , damit Windows-Explorer die Nachricht verarbeitet. Wenn das Ordner Ansichts Objekt die Nachricht verarbeitet hat, geben Sie S \_ OK zurück.

Wenn das Fenster der Ordneransicht den Fokus besitzt, ruft Windows Explorer [**ishellview:: TranslateAccelerator**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-translateaccelerator) auf, bevor die Nachricht verarbeitet wird. Da die meisten Meldungen in der Regel der Windows Explorer-Menüleiste oder den Symbolleisten Befehlen zugeordnet sind, sollte das Ordner Ansichts Objekt normalerweise den Wert "false" zurückgeben \_ Die Nachricht kann dann von Windows Explorer normal verarbeitet werden. Gibt \_ nur dann OK zurück, wenn die Meldung Ordner spezifisch ist und Sie nicht möchten, dass Windows-Explorer eine weitere Verarbeitung durchführen kann. Wenn die Ordneransicht keinen Fokus hat, wird die Nachricht von Windows Explorer zuerst verarbeitet. [**Ishellbrowser:: translateacceleratorsb**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-translateacceleratorsb) wird nur aufgerufen, wenn die Nachricht nicht verarbeitet wird.

## <a name="using-ishellbrowser-to-communicate-with-windows-explorer"></a>Verwenden von ishellbrowser für die Kommunikation mit Windows-Explorer

Die [**ishellbrowser**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser) -Schnittstelle wird vom Ordner Ansichts Objekt für die Kommunikation mit Windows-Explorer für eine Vielzahl von Zwecken verwendet, einschließlich:

-   [Ändern der Windows Explorer-Menüleiste](#modifying-the-windows-explorer-menu-bar)
-   [Ändern der Windows-Explorer-Symbolleiste](#modifying-the-windows-explorer-toolbar)
-   [Ändern der Windows Explorer-Status Leiste](#modifying-the-windows-explorer-status-bar)
-   [Speichern von Ansichts spezifischen Informationen](#storing-view-specific-information)

### <a name="modifying-the-windows-explorer-menu-bar"></a>Ändern der Windows Explorer-Menüleiste

In der Windows-Explorer-Menüleiste kann der Benutzer eine Vielzahl von Befehlen starten. Standardmäßig unterstützt die Menüleiste nur Befehle, die für Windows Explorer spezifisch sind. Die zugehörigen [WM- \_ Befehls](../menurc/wm-command.md) Meldungen werden von Windows Explorer verarbeitet und nicht an das Objekt der Ordneransicht übermittelt. Sie können jedoch die Menüleiste ändern, sodass Sie mindestens ein Ordner spezifisches Menü Element mit [**ishellbrowser**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser)enthält. Windows-Explorer übergibt die zugeordneten WM \_ -befehlsnachrichten dieser Elemente zur Verarbeitung an die Fenster Prozedur des Ordner Objekts. Sie können auch alle Standard Befehle entfernen oder deaktivieren, die nicht für die Anwendung gelten.

Ordner Ansichts Objekte ändern in der Regel die Menüleiste, bevor die Ordneransicht zum ersten Mal angezeigt wird. Wenn die Ordneransicht zerstört wird, muss die Menüleiste in ihren ursprünglichen Zustand zurückversetzt werden. Möglicherweise müssen Sie die Menüleiste auch jedes Mal ändern, wenn die Ordneransicht den Fokus erhält oder verliert.

Da Windows Explorer [**ishellview:: uiaktivierungs**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-uiactivate) jedes Mal aufruft, wenn sich der Zustand der Ordner Ansichts Fenster ändert, ist die Menüleisten Änderung normalerweise in der Implementierung dieser Methode enthalten. Das grundlegende Verfahren zum Ändern der Windows Explorer-Menüleiste lautet wie folgt:

1.  Rufen Sie " [anatemdeu](/windows/win32/api/winuser/nf-winuser-createmenu) " auf, um ein Menü Handle zu erstellen.
2.  Übergeben Sie das Menü Handle an den Windows-Explorer, indem Sie [**ishellbrowser:: insertmenussb**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-insertmenussb)aufrufen. In Windows Explorer werden die Menü Informationen angezeigt.
3.  Ändern Sie das Menü nach Bedarf.
4.  Aufrufen von [**ishellbrowser:: setmenusb**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-setmenusb) , damit Windows-Explorer die geänderte Menüleiste anzeigt.

Windows-Explorer verfügt über sechs Popup Menüs in der Menüleiste. Wie bei allen OLE-Containern ist das Windows-Explorer-Menü in sechs Gruppen unterteilt: Datei, Bearbeitung, Container, Objekt, Fenster und Hilfe. In der folgenden Tabelle werden die Popup Menüs von Windows-Explorer und die zugehörige Gruppe zusammen mit den Menü-IDs aufgelistet.



| Popup Menü | id                     | Gruppieren     |
|-------------|------------------------|-----------|
| File        | f- \_ Menü \_ Datei      | File      |
| Bearbeiten        | ficidm- \_ Menü \_ Bearbeiten      | File      |
| Sicht        | scidm- \_ Menü \_ Ansicht      | Container |
| Favoriten   | Favoriten für das f- \_ Menü \_ | Container |
| Tools       | f- \_ Menü \_ Tools     | Container |
| Hilfe        | Hilfe zum scidm- \_ Menü \_      | Fenster    |



 

Wenn Sie das Menü Handle an den Windows-Explorer übergeben, indem Sie [**ishellbrowser:: insertmenussb**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-insertmenussb)aufrufen, müssen Sie auch einen Zeiger an eine [olemenugroupbreiten](/windows/win32/api/oleidl/ns-oleidl-olemenugroupwidths) -Struktur übergeben, deren Member mit 0 (null) initialisiert wurden.

Wenn [**ishellbrowser:: insertmenussb**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-insertmenussb) zurückgibt, hat Windows-Explorer seine Menü Elemente hinzugefügt. Anschließend können Sie das zurückgegebene Menü Handle mit standardmäßigen Windows-Menüfunktionen wie [InsertMenuItem](/windows/win32/api/winuser/nf-winuser-insertmenuitema) für Folgendes verwenden:

-   Fügen Sie den Windows-Explorer-Popup Menüs Elemente hinzu.
-   Ändern oder Löschen vorhandener Elemente in den Popup Menüs von Windows-Explorer.
-   Fügen Sie neue Popup Menüs hinzu.

Verwenden Sie die in der Tabelle aufgeführten IDs, um die verschiedenen Popup Menüs von Windows-Explorer zu identifizieren.

> [!Note]  
> Um Konflikte mit Windows Explorer-Befehls-IDs zu vermeiden, müssen die IDs aller Menü Elemente, die Sie hinzufügen, zwischen fcidm \_ shviewfirst und fcidm \_ shviewlast liegen. Diese beiden Werte werden in "shlobj. h" definiert.

 

Wenn Sie die Änderung des Menüs abgeschlossen haben, nennen Sie [**ishellbrowser:: setmenusb**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-setmenusb) , damit Windows-Explorer die neue Menüleiste anzeigt.

Nachdem die Ordneransicht zum ersten Mal angezeigt wird, ruft Windows-Explorer [**ishellview:: uiaktivierungs**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-uiactivate) auf, sobald die Ordneransicht den Fokus erhält oder verliert. Wenn Sie über Menü Elemente verfügen, die für den Zustand der Ordneransicht sensibel sind, sollten Sie das Menü entsprechend ändern, wenn sich der Status ändert. Beispielsweise können Sie über ein Menü Element verfügen, das für ein Element in der Ordneransicht fungiert, das vom Benutzer ausgewählt wurde. Sie sollten dieses Menü Element deaktivieren oder entfernen, wenn die Ordneransicht den Fokus verliert.

Wenn Windows Explorer [**ishellview:: uiaktivierungs**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-uiactivate) aufruft, um anzugeben, dass die Ordneransicht deaktiviert wird, stellen Sie die Menüleiste in Ihrem ursprünglichen Zustand wieder her, indem Sie [**ishellbrowser:: removemenussb**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-removemenussb)aufrufen.

### <a name="modifying-the-windows-explorer-toolbar"></a>Ändern der Windows-Explorer-Symbolleiste

Zusätzlich zum Ändern der Windows Explorer-Menüleiste können Sie auch Schaltflächen zur Symbolleiste hinzufügen. Wie bei der Menüleiste ist die Symbolleisten Änderung in der Regel Teil der [**ishellview:: uiaktivierungs**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-uiactivate) -Implementierung. Die Vorgehensweise zum Hinzufügen von Schaltflächen zur Windows-Explorer-Symbolleiste lautet:

1.  Fügen Sie die Bitmap der Schaltfläche der Bildliste der Symbolleiste hinzu.
2.  Hiermit wird die Text Zeichenfolge der Schaltfläche definiert.
3.  Fügen Sie der Symbolleiste die Schaltfläche hinzu.

Um der Bildliste einer Symbolleiste eine Bitmap hinzuzufügen, senden Sie die Symbolleiste eine [TB- \_ AddBitmap](../controls/tb-addbitmap.md) -Nachricht, indem Sie [**ishellbrowser:: sendcontrolmsg**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-sendcontrolmsg)aufrufen. Legen Sie zum Angeben des Toolbar-Steuer Elements den *ID* -Parameter der Methode auf die **FCW- \_ Symbolleiste** fest. Legen Sie *wParam* auf die Anzahl der Schaltflächen Bilder in der Bitmap und *LPARAM* auf die Adresse einer [tbaddbitmap](/windows/win32/api/commctrl/ns-commctrl-tbaddbitmap) -Struktur fest. Der Bildindex wird im *Pret* -Parameter zurückgegeben.

Es gibt zwei Möglichkeiten, eine Zeichenfolge für die Schaltfläche zu definieren:

-   Weisen Sie die Zeichenfolge dem **IString** -Member der [TBBUTTON](/windows/win32/api/commctrl/ns-commctrl-tbbutton) -Struktur der Schaltfläche zu.
-   Ruft [**ishellbrowser:: sendcontrolmsg**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-sendcontrolmsg) auf, um das Symbolleisten-Steuerelement an eine [TB \_ AddString](../controls/tb-addstring.md) -Nachricht zu senden. Der *wParam* -Parameter muss auf 0 (null) und den *LPARAM* -Parameter auf die Zeichenfolge festgelegt werden. Der Zeichen folgen Index wird im *Pret* -Parameter zurückgegeben.

Wenn Sie der Symbolleiste die Schaltfläche hinzufügen möchten, füllen Sie die [TBBUTTON](/windows/win32/api/commctrl/ns-commctrl-tbbutton) -Struktur aus, und übergeben Sie Sie an [**ishellbrowser:: settoolbaritems**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-settoolbaritems). Wie beim Menü muss die Befehls-ID zwischen " \_ shviewfirst" und "scidm \_ shviewlast" liegen. Die Symbolleiste fügt dann die Schaltfläche rechts neben den vorhandenen Schaltflächen ein.

Das folgende Code Fragment fügt z. b. der Windows-Explorer-Symbolleiste eine Standard Schaltfläche mit der Befehls-ID IDB \_ MyButton hinzu.


```
TBADDBITMAP tbadbm;
int iButtonIndex;
TBBUTTON tbb;

tbadbm.hInst = g_hInstance;    // The module's instance handle
tbadbm.nID = IDB_BUTTONIMAGE;  // The bitmap's resource ID

psb->SendControlMsg(FCW_TOOLBAR, TB_ADDBITMAP, 1,
                    reinterpret_cast<LPARAM>(&tbadbm), &iButtonIndex);

psb->SendControlMsg(FCW_TOOLBAR, TB_ADDSTRING, NULL,
                    reinterpret_cast<LPARAM>(szLabel), &iStringIndex);

ZeroMemory(&tbb, sizeof(TBBUTTON));
tbb.iBitmap = iButtonIndex;
tbb.iCommand = IDB_MYBUTTON;
tbb.iString = iStringIndex;
tbb.fsState = TBSTATE_ENABLED;
tbb.fsStyle = TBSTYLE_BUTTON;

psb->SetToolbarItems(&tbb, 1, FCT_MERGE);
```



Weitere Informationen zum Behandeln von Symbolleisten-Steuerelementen finden Sie unter Symbolleisten-Steuer [Elemente](../controls/toolbar-control-reference.md).

### <a name="modifying-the-windows-explorer-status-bar"></a>Ändern der Windows Explorer-Status Leiste

Sie können die Windows-Explorer-Statusleiste verwenden, um eine Vielzahl nützlicher Informationen anzuzeigen. Es gibt zwei Möglichkeiten, die Statusleiste zu verwenden:

-   Verwenden Sie [**ishellbrowser:: setstatustextb**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-setstatustextsb) , um eine Text Zeichenfolge auf der Statusleiste anzuzeigen.
-   Senden Sie Nachrichten direkt an das StatusBar-Steuerelement mit [**ishellbrowser:: sendcontrolmsg**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-sendcontrolmsg).

Die erste Methode ist unkompliziert, aber für viele Zwecke ausreichend. Sie können Nachrichten direkt an das StatusBar-Steuerelement senden, indem Sie [**ishellbrowser:: sendcontrolmsg**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-sendcontrolmsg) aufrufen, wobei der *ID* -Parameter auf **FCW- \_ Status** festgelegt ist. Weitere Informationen zu StatusBar-Steuerelementen finden Sie unter [Status leisten](../controls/status-bars.md).

### <a name="storing-view-specific-information"></a>Speichern von Ansichts spezifischen Informationen

Wenn eine Ansicht zerstört wird, ist es häufig hilfreich, Informationen wie den Zustand oder die Einstellungen der Ansicht zu speichern. Windows-Explorer fordert Sie auf, diese Aufgabe durch Aufrufen von [**ishellview:: SaveViewState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-saveviewstate)auszuführen. Die bevorzugte Methode zum Speichern von Ansichts spezifischen Informationen ist das Aufrufen von [**ishellbrowser:: getviewstatestream**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-getviewstatestream). Diese Methode stellt eine [IStream](/windows/win32/api/objidl/nn-objidl-istream) -Schnittstelle bereit, die Sie zum Speichern der Informationen verwenden können. Sie können ein beliebiges geeignetes Datenformat verwenden.

 

 
