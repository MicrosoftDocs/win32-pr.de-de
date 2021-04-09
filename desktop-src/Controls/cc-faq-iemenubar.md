---
title: Erstellen einer Menüleiste für Internet Explorer-Style
description: Auf den ersten Blick sieht die Menüleiste in Microsoft Internet Explorer 5 und höher einem Standardmenü ähnlich aus. Es ist jedoch ganz anders, wenn Sie beginnen, es zu verwenden.
ms.assetid: e0fe25f2-3d49-4c5a-a3f9-2f468f2cfef2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b262bc55407d263c97d4bd7e3938a9794d3a58f5
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103858494"
---
# <a name="how-to-create-an-internet-explorer-style-menu-bar"></a>Erstellen einer Menüleiste für Internet Explorer-Style

Auf den ersten Blick sieht die Menüleiste in Microsoft Internet Explorer 5 und höher einem Standardmenü ähnlich aus. Es ist jedoch ganz anders, wenn Sie beginnen, es zu verwenden.

Der folgende Screenshot zeigt die Menüleiste von Windows Internet Explorer, in der das Menü Extras ausgewählt ist.

![Screenshot der Windows Internet Explorer-Menüleiste mit ausgewähltem Menü "Extras"](images/howto8.jpg)

Die Menüleiste ist tatsächlich ein Symbolleisten-Steuerelement, das wie ein Standardmenü aussieht. Anstelle von Menü Elementen der obersten Ebene enthält eine Menüleiste eine Reihe von nur-Text-Schaltflächen, die ein Dropdown Menü anzeigen, wenn darauf geklickt wird. Als spezieller Typ der Symbolleiste bietet eine Menüleiste jedoch einige Funktionen, die Standardmenüs fehlen:

-   Sie kann mithilfe von standardmäßigen Symbolleisten Techniken angepasst werden, sodass der Benutzer Elemente verschieben, löschen oder hinzufügen kann.
-   Sie kann über eine Hot-Tracking verfügen, damit Benutzer wissen, wenn Sie sich über einem Element der obersten Ebene befinden, ohne darauf klicken zu müssen.

Eine Menüleiste kann in ein Grund leisten-Steuerelement eingebunden werden, das Ihnen die folgenden Features bietet:

-   Sie kann über einen Zieh Punkt verfügen, der dem Benutzer das Verschieben oder Ändern der Größe des Bands ermöglicht.
-   Es kann einen Strip im Info leisten-Steuerelement mit anderen Bändern, wie z. b. der Standard Symbolleiste in der vorherigen Abbildung, freigeben.
-   Es kann ein Chevron anzeigen, wenn es von einem angrenzenden Band abgedeckt wird, sodass der Benutzer Zugriff auf die ausgeblendeten Elemente hat.
-   Sie kann über eine von der Anwendung definierte Hintergrund Bitmap verfügen.

In diesem Thema wird erläutert, wie eine Menüleiste implementiert wird. Da eine Menüleiste eine spezielle Implementierung eines Symbolleisten-Steuer Elements ist, wird der Fokus auf Themen, die für Menüleisten spezifisch sind. Eine Erläuterung dazu, wie Sie eine Symbolleiste in ein Grund leisten-Steuerelement integrieren, finden Sie unter [How to Create a Internet Explorer-Style Toolbar](cc-faq-ietoolbar.md) und [about Grund leisten Controls](rebar-controls.md).

-   [Erstellen einer Symbolleiste in eine Menüleiste](#making-a-toolbar-into-a-menu-bar)
-   [Behandeln der Navigation mit aktiviertem Menü Hot-Tracking](#handling-navigation-with-menu-hot-tracking-disabled)
    -   [Maus Navigation](#mouse-navigation)
    -   [Tastatur Navigation](#keyboard-navigation)
    -   [Gemischte Navigation](#mixed-navigation)
-   [Behandeln der Navigation mit aktiviertem Menü Hot-Tracking](#handling-navigation-with-menu-hot-tracking-enabled)
    -   [Nachrichtenverarbeitung für Menü-Hot-Tracking](#message-processing-for-menu-hot-tracking)
    -   [Maus Navigation](#mouse-navigation)
    -   [Tastatur Navigation](#keyboard-navigation)

## <a name="making-a-toolbar-into-a-menu-bar"></a>Erstellen einer Symbolleiste in eine Menüleiste

So machen Sie eine Symbolleiste in eine Menüleiste:

-   Erstellen Sie eine flache Symbolleiste, indem Sie [**tbstyle \_ Flat**](toolbar-control-and-button-styles.md) mit den anderen Fenster stilflags einschließen. Der **\_ flache Stil von tbstyle** ermöglicht außerdem die Hot-Tracking-Funktion. Bei diesem Stil sieht die Menüleiste dem Standardmenü so lange aus, bis der Benutzer eine Schaltfläche aktiviert. Anschließend wird die Schaltfläche so angezeigt, dass Sie auf der Symbolleiste angezeigt wird, und Sie beim Klicken auf die Schaltfläche debugdrücken. Da die Hot-Tracking-Funktion aktiviert ist, muss zum Aktivieren einer Schaltfläche nur der Cursor darauf zeigen, um eine Schaltfläche zu aktivieren. Wenn der Cursor auf eine andere Schaltfläche verschoben wird, wird er aktiviert und die alte Schaltfläche deaktiviert.
-   Erstellen Sie Schaltflächen im Listenformat, indem Sie die [**tbstyle- \_ Liste**](toolbar-control-and-button-styles.md) mit den anderen Fenster Stil-Flags einschließen. Dieser Stil erstellt eine schlankere Schaltfläche, die mehr ähnelt wie ein Standardmenü Element der obersten Ebene.
-   Legen Sie die Schaltflächen Text-Only fest, indem Sie den **ibitmap** -Member der [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) -Struktur der Schaltfläche auf ich \_ imagenone und den **IString** -Member auf den Schaltflächen Text festlegen.
-   Versehen Sie jede Schaltfläche mit dem [**btns- \_ Dropdown**](toolbar-control-and-button-styles.md) Stil. Wenn auf die Schaltfläche geklickt wird, sendet das Symbolleisten-Steuerelement eine [TBN- \_ Dropdown](tbn-dropdown.md) Benachrichtigung an Ihre Anwendung, um Sie aufzufordern, das Menü der Schaltfläche anzuzeigen.
-   Integrieren Sie die Menüleiste in ein Info Balken-Band. Aktivieren Sie sowohl Gripper als auch Chevrons, wie unter [How to Create an Internet Explorer-Style Toolbar](cc-faq-ietoolbar.md)erläutert.
-   Implementieren Sie einen [TBN- \_ Dropdown](tbn-dropdown.md) Handler, um das *Dropdown Menü* der Schaltfläche anzuzeigen, wenn darauf geklickt wird. Das Dropdown Menü ist ein Typ von Popup-Menü. Sie wird mithilfe der [**TrackPopupMenu**](/windows/desktop/api/winuser/nf-winuser-trackpopupmenu) -Funktion erstellt, wobei die linke obere Ecke an der linken unteren Ecke der Schaltfläche ausgerichtet ist.
-   Implementieren Sie die Tastaturnavigation, sodass die Menüleiste ohne Maus vollständig zugänglich ist.
-   Implementieren Sie das Menü "Hot-Tracking". Wenn in Standardmenüs ein Menü Element Menü der obersten Ebene angezeigt wird, wird der Cursor über ein anderes Element der obersten Ebene automatisch im Menü angezeigt, und das Menü des vorherigen Elements wird ausgeblendet. Mit dem Symbolleisten-Steuerelement wird der Cursor auf den Cursor nachverfolgt und das Schaltflächen Bild geändert, aber das neue Menü wird automatisch angezeigt. Die Anwendung muss dies explizit tun.

Die meisten dieser Elemente sind einfach zu implementieren und werden an anderer Stelle erörtert. Eine allgemeine Erörterung der Verwendung von Symbolleisten und Grund leisten-Steuerelementen finden Sie unter [Erstellen einer Internet Explorer-Style Symbolleiste](cc-faq-ietoolbar.md), [Informationen zu Symbol](toolbar-controls-overview.md)leisten-Steuerelementen oder über Grund leisten-Steuer [Elemente](rebar-controls.md) . Weitere Informationen zur Behandlung von Popup Menüs finden Sie unter [Menüs](/windows/desktop/menurc/menus) . Die letzten beiden Elemente, Tastaturnavigation und Menü-Hot-Tracking, werden im weiteren Verlauf dieses Themas erläutert.

## <a name="handling-navigation-with-menu-hot-tracking-disabled"></a>Behandeln der Navigation mit aktiviertem Menü Hot-Tracking

Benutzer können mit der Maus, der Tastatur oder einer Kombination aus beidem in der Menüleiste navigieren. Um die Navigation in der Menüleiste zu implementieren, muss Ihre Anwendung Symbolleisten Benachrichtigungen verarbeiten und die Maus und Tastatur überwachen. Diese Aufgabe kann in zwei unterschiedliche Teile aufgeteilt werden: mit und ohne Menü-Hot-Tracking. In diesem Abschnitt wird erläutert, wie die Navigation behandelt wird, wenn keine Menüs angezeigt werden und das Menü "Hot-Tracking" nicht aktiviert ist.

### <a name="mouse-navigation"></a>Maus Navigation

Wenn die Hot-Tracking-Menüoption deaktiviert ist, können Sie eine Menüleiste als normale Symbolleiste behandeln. Wenn der Benutzer mit einer Maus navigiert, muss die [TBN- \_ Dropdown](tbn-dropdown.md) Benachrichtigung von der gesamten Anwendung verarbeitet werden. Wenn diese Benachrichtigung empfangen wird, zeigen Sie das entsprechende Dropdown Menü an, und aktivieren Sie das Menü "Hot-Tracking". Danach befinden Sie sich im Menü "Hot-Tracking-System", das unter [Handling Navigation with Menu Hot-Tracking aktiviert](#handling-navigation-with-menu-hot-tracking-enabled)ist.

Wie in [mixed Navigation](#mixed-navigation)erläutert, müssen Sie auch die TBN-Meldung " [ \_ betitemchange](tbn-hotitemchange.md) " behandeln, um die aktive Schaltfläche zu verfolgen. Diese Benachrichtigung ist irrelevant, wenn der Benutzer nur mit der Maus navigiert, aber dies ist erforderlich, wenn die Maus-und Tastaturnavigation gemischt ist.

### <a name="keyboard-navigation"></a>Tastaturnavigation

Wie bereits im vorherigen Abschnitt erwähnt, kann der Benutzer mit der Tastatur eine Reihe von Navigations Vorgängen durchführen, wenn das Menü "Hot-Tracking" deaktiviert ist. Symbolleisten-Steuerelemente unterstützen Tastaturnavigation nur, wenn Sie den Fokus haben Außerdem werden nicht alle für Menüleisten benötigten Tastendruck Aufgaben behandelt. Die einfachste Lösung für die Tastaturnavigation besteht darin, die relevanten Tastendruck Ereignisse explizit zu verarbeiten.

Wenn die Hot-Tracking-Menüs deaktiviert ist, muss die Anwendung diese Tastendruck Ereignisse wie folgt behandeln:

-   F10-TASTE Aktivieren Sie die erste Schaltfläche mit der [**TB \_**](tb-sethotitem.md)"".
-   Die nach-links-und nach-rechts-Taste. Aktivieren Sie die angrenzende Schaltfläche mit dem [**TB \_**](tb-sethotitem.md)-Element. Wenn der Benutzer versucht, von einem Ende der Menüleiste zu navigieren, aktivieren Sie die erste Schaltfläche am gegenüberliegenden Ende.
-   Der escapeschlüssel. Deaktivieren Sie die aktive Schaltfläche mit dem " [**TB \_**](tb-sethotitem.md)". Die Menüleiste sollte in den Zustand zurückversetzt werden, der vor dem Aktivieren der ersten Schaltfläche aufgetreten ist.
-   Eine Tastenkombination für Alt-*Taste* . Verwenden Sie die [**TB- \_ mapaccelerernachricht**](tb-mapaccelerator.md) , um zu bestimmen, welcher Schaltfläche das *Schlüssel* Zeichen entspricht. Zeigen Sie das Dropdown Menü der Schaltfläche an, und aktivieren Sie das Menü "Hot-Tracking".
-   NACH-UNTEN-TASTE Wenn eine Schaltfläche aktiv ist, aber kein Menü angezeigt wird, zeigen Sie das Menü der Schaltfläche an, und aktivieren Sie das Menü "Hot-Tracking".
-   EINGABETASTE Deaktivieren Sie die aktive Schaltfläche mit dem " [**TB \_**](tb-sethotitem.md)". Die Menüleiste sollte in den Zustand zurückversetzt werden, der vor dem Aktivieren der ersten Schaltfläche aufgetreten ist.

### <a name="mixed-navigation"></a>Gemischte Navigation

Die im vorherigen Abschnitt beschriebenen Tastatur Navigations Handler führen im Grunde zwei Aufgaben aus: verfolgen Sie die aktive Schaltfläche, und zeigen Sie das entsprechende Menü an, wenn eine Schaltfläche ausgewählt wird. Diese Handler sind ausreichend, solange der Benutzer nur über die Tastatur navigiert. Benutzer mischen jedoch oft die Tastatur-und Maus Navigation. Beispielsweise können Sie die erste Schaltfläche mit der Taste F10 aktivieren, mit der Maus eine andere Schaltfläche aktivieren und dann das Menü mit der nach-unten-Taste öffnen. Wenn Sie nur die Tastendruck überwachen, um den aktiven Schlüssel zu verfolgen, wird das falsche Menü angezeigt. Sie müssen auch die TBN-Meldung " [ \_ betitemchange](tbn-hotitemchange.md) " behandeln, um die aktive Schaltfläche korrekt zu verfolgen.

## <a name="handling-navigation-with-menu-hot-tracking-enabled"></a>Behandeln der Navigation mit aktiviertem Menü Hot-Tracking

Wenn Menü-Hot-Tracking aktiviert ist, muss Ihre Anwendung die Art und Weise ändern, wie Sie auf die Benutzernavigation reagiert. Um das Verhalten von Standardmenüs zu replizieren, müssen Sie die folgenden Funktionen explizit implementieren.

Mit der Maus Navigation:

-   Wenn der Benutzer den Cursor über eine andere Schaltfläche bewegt, wird das Menü sofort angezeigt, und das vorherige Menü wird nicht mehr angezeigt.
-   Die Hot-Tracking-Menü bleibt aktiv, bis der Benutzer einen Befehl auswählt oder auf einen Punkt klickt, der nicht Teil des Menü Bereichs ist. Beide Aktionen deaktivieren Menü-Hot-Tracking, bis auf eine andere Schaltfläche geklickt wird.
-   Wenn der Cursor aus dem Menü verschoben wird, bleibt das aktuelle Dropdown Menü so lange erhalten, bis der Cursor zurück wechselt, oder der Benutzer klickt auf einen Punkt außerhalb, den Bereich, der im Menü abgedeckt ist. Wenn der Cursor zu einer anderen Schaltfläche zurückkehrt, als gerade angezeigt wird, wird das alte Menü reduziert, und das neue Menü wird angezeigt.

Mit Tastaturnavigation:

-   Mit der nach-rechts-Taste wird der Fokus nach rechts verschoben. Wenn das Element über ein Untermenü verfügt, zeigen Sie das Untermenü an. Wenn das Element nicht über ein Untermenü verfügt, reduzieren Sie das Menü und alle Untermenüs, aktivieren Sie die Schaltfläche weiter mit dem TB-Element, und zeigen Sie das Menü für die angrenzende Schaltfläche an. [**\_**](tb-sethotitem.md) Wenn die letzte Schaltfläche aktiv ist, wenn diese Meldung empfangen wird, zeigen Sie das Menü für die erste Schaltfläche an.
-   Mit der nach-links-Taste wird der Fokus nach links verschoben. Wenn das Element ein Untermenü ist, reduzieren Sie es, und verschieben Sie den Fokus auf das übergeordnete Menü. Wenn es sich bei dem Element nicht um ein Untermenü handelt, reduzieren Sie das Menü, aktivieren Sie die Schaltfläche "weiter" mit " [**TB \_**](tb-sethotitem.md)", und zeigen Sie das Menü für diese Schaltfläche an.

<!-- -->

-   Der escapeschlüssel sichert einen Schritt in der Anzeige.
    -   Wenn ein Untermenü angezeigt wird, wird es reduziert, und der Fokus wechselt zum übergeordneten Menü.
    -   Wenn das Menü einer Schaltfläche angezeigt wird, wird es reduziert, und die Menü-Hot-Tracking-Option ist deaktiviert. Die Schaltfläche des Elements bleibt aktiv.
    -   Wenn keine Menüs angezeigt werden, aber eine Schaltfläche aktiv ist, wird die Schaltfläche deaktiviert, und die Menü-Hot-Tracking-Option ist deaktiviert.
-   Die nach-oben-und nach-unten-Taste werden nur für die Navigation innerhalb eines bestimmten Menüs verwendet.
-   Die EINGABETASTE öffnet den Befehl, der einem Menü Element zugeordnet ist. Wenn das Menü Element über ein Untermenü verfügt, wird es mit der EINGABETASTE angezeigt.

Wie beim deaktivierten Menü "Hot-Tracking" muss Ihre Anwendung die Maus-, Tastatur-und gemischte Navigation verarbeiten können. Die Tatsache, dass ein Menü angezeigt wird, bedeutet jedoch, dass das Messaging etwas anders gehandhabt werden muss.

### <a name="message-processing-for-menu-hot-tracking"></a>Nachrichtenverarbeitung für Menü Hot-Tracking

Das Menü "Hot-Tracking" erfordert, dass immer ein Menü angezeigt wird, abgesehen von dem kurzen Intervall, das zum Wechseln in ein neues Menü erforderlich ist. Allerdings ist das Dropdown Menü, das von [**TrackPopupMenu**](/windows/desktop/api/winuser/nf-winuser-trackpopupmenu) angezeigt wird, Modal. Ihre Anwendung empfängt weiterhin einige Nachrichten direkt, einschließlich [**WM- \_ Befehl**](/windows/desktop/menurc/wm-command), [TBN- \_ hotitemchange](tbn-hotitemchange.md)und normaler Menü bezogener Meldungen wie z. b. [**WM \_ MenuSelect**](/windows/desktop/menurc/wm-menuselect). Es werden jedoch keine Tastatur-oder Maus Nachrichten auf niedriger Ebene direkt empfangen. Um Nachrichten wie z. b. [**WM \_ MouseMove**](/windows/desktop/inputdev/wm-mousemove)zu verarbeiten, müssen Sie einen nachrichtenhook festlegen, um Nachrichten abzufangen, die an das Menü geleitet werden.

Wenn ein Dropdown Menü angezeigt wird, legen Sie den Nachrichten Hook fest, indem Sie die Funktion [**SetWindowsHookEx**](/windows/desktop/api/winuser/nf-winuser-setwindowshookexa) aufrufen, wobei der *idhook* -Parameter auf WH \_ msgfilter festgelegt ist. Alle für das Menü vorgesehenen Meldungen werden an Ihre Hook- [Prozedur](/previous-versions/windows/desktop/legacy/ms644987(v=vs.85))übermittelt. Mit dem folgenden Code Fragment wird z. b. ein nachrichtenhook festgelegt, der Nachrichten abfängt, die in einem Dropdown Menü angezeigt werden. `MsgHook` der Name der Hook-Prozedur und `hhookMsg` ist das Handle der Prozedur.


```
hhookMsg = SetWindowsHookEx(WH_MSGFILTER, MsgHook, HINST_THISDLL, 0);
```



Menü Meldungen werden identifiziert, indem der *nCode* -Parameter der Hook-Prozedur auf das MSGF-Menü festgelegt wird \_ . Der *LPARAM* -Parameter verweist auf eine [**msg**](/windows/win32/api/winuser/ns-winuser-msg) -Struktur mit der Meldung. Die Details zu den Nachrichten, die behandelt werden müssen, und wie im weiteren Verlauf dieses Themas erläutert werden.

Die Anwendung muss alle Nachrichten an den nächsten Nachrichten Hook übergeben, indem Sie die [**CallNextHookEx**](/windows/desktop/api/winuser/nf-winuser-callnexthookex) -Funktion aufrufen. Sie müssen auch Maus Nachrichten direkt an das Symbolleisten-Steuerelement senden, um alle Punkt Koordinaten in den Koordinaten Bereich der Symbolleiste zu konvertieren. Das direkte Senden von Nachrichten stellt sicher, dass das ToolBar-Steuerelement die entsprechenden Maus Meldungen empfängt. Beispielsweise muss die Symbolleiste WM- [**\_ mousermove**](/windows/desktop/inputdev/wm-mousemove) -Nachrichten empfangen, um die Schaltflächen zu überprüfen.

Wenn eine neue Schaltfläche aktiviert ist, muss die Anwendung das alte Dropdown Menü mit der Meldung " [**WM \_ cancelmode**](/windows/desktop/winmsg/wm-cancelmode) " reduzieren und ein neues Menü anzeigen. Außerdem muss das Dropdown Menü reduziert werden, wenn der Fokus in der Menüleiste mit der Tastaturnavigation oder durch Klicken außerhalb des Menü Bereichs angezeigt wird. Wenn Sie ein Menü reduzieren, sollten Sie den Nachrichten Hook mithilfe der [**unhookwindowshookex**](/windows/desktop/api/winuser/nf-winuser-unhookwindowshookex) -Funktion freigeben. Wenn Sie ein weiteres Dropdown Menü anzeigen müssen, erstellen Sie einen neuen nachrichtenhook. Wenn ein Befehl gestartet wird, wird das Menü automatisch reduziert, aber Sie müssen den nachrichtenhook explizit freigeben.

Im folgenden Codebeispiel wird der Nachrichten Hook freigegeben, der im vorherigen Beispiel festgelegt wurde.


```
UnhookWindowsHookEx(hhookMsg);
```



### <a name="mouse-navigation"></a>Maus Navigation

Wenn ein normales Symbolleisten-Steuerelement mit der Schaltfläche "aktiv" nachverfolgt wird, wird die aktive Schaltfläche hervorgehoben, und die Anwendung wird bei jedem Aktivieren einer neuen Schaltfläche mit einer [TBN \_ ](tbn-hotitemchange.md) -Nachricht über die Ihre Anwendung ist dafür verantwortlich, das entsprechende Dropdown Menü anzuzeigen. Sie muss:

-   Behandeln Sie die [TBN- \_ betitemchange](tbn-hotitemchange.md) -Benachrichtigung, um die aktive Schaltfläche nachzuverfolgen. Wenn sich die aktive Schaltfläche ändert, reduzieren Sie das alte Menü, und erstellen Sie ein neues.
-   Behandelt die [TBN- \_ Dropdown](tbn-dropdown.md) Benachrichtigung, die gesendet wird, wenn auf eine Schaltfläche geklickt wird. Anschließend sollte das Menü reduziert und die Hot-Tracking-Menüs deaktiviert werden. Die Schaltfläche bleibt aktiv.
-   Behandeln Sie die Nachrichten " [**WM \_ lbuttondown**](/windows/desktop/inputdev/wm-lbuttondown)", " [**WM \_ rbuttondown**](/windows/desktop/inputdev/wm-rbuttondown)" und " [**WM \_ MouseMove**](/windows/desktop/inputdev/wm-mousemove) " in ihrer nachrichtenhook-Prozedur, um die Mausposition nachzuverfolgen. Wenn außerhalb des Menü Bereichs auf die Maus geklickt wird, reduzieren Sie das aktuelle Dropdown Menü, deaktivieren Sie die Menü-Hot-Tracking-Option, und geben Sie die Menüleiste in ihren voraktivierungs Zustand zurück.
-   Wenn ein Menübefehl gestartet wird, deaktivieren Sie das Menü "Hot-Tracking". Das Menü wird automatisch reduziert, aber Sie müssen den nachrichtenhook explizit freigeben.

Sie müssen auch Menü bezogenes Messaging verarbeiten, z. b. die " [**WM \_ initmenupopup**](/windows/desktop/menurc/wm-initmenupopup) "-Meldung, die gesendet wird, wenn ein Menü Element ein Untermenü anzeigen muss. Eine Erläuterung dazu, wie solche Nachrichten behandelt werden, finden Sie unter [Menüs](/windows/desktop/menurc/menus).

### <a name="keyboard-navigation"></a>Tastaturnavigation

Die Anwendung muss Tastatur Meldungen in der Message Hook-Prozedur verarbeiten und auf diese reagieren, die sich auf die Menü-Hot-Tracking auswirken. Die folgenden Tastendruck Punkte müssen behandelt werden:

-   Der escapeschlüssel. Der escapeschlüssel sichert die Anzeige um eine Ebene nach oben. Wenn ein Untermenü angezeigt wird, muss es reduziert werden. Wenn das primäre Menü einer Schaltfläche angezeigt wird, reduzieren Sie es, und deaktivieren Sie das Menü "Hot-Tracking". Die Schaltfläche bleibt aktiv.
-   NACH-RECHTS-TASTE Wenn das Element über ein Untermenü verfügt, zeigen Sie es an. Wenn das Element nicht über ein Untermenü verfügt, reduzieren Sie das Menü und alle Untermenüs, aktivieren Sie die Schaltfläche weiter mit dem TB-Element, und zeigen Sie das zugehörige Menü an. [**\_**](tb-sethotitem.md) Wenn die letzte Schaltfläche beim Empfang dieser Benachrichtigung aktiv war, zeigen Sie das Menü für die erste Schaltfläche an.
-   NACH-LINKS-TASTE Wenn sich das Element in einem Untermenü befindet, reduzieren Sie es, und verschieben Sie den Fokus auf das übergeordnete Menü. Wenn es sich bei dem Element nicht um ein Untermenü handelt, reduzieren Sie das Menü, aktivieren Sie die angrenzende Schaltfläche mit [**TB \_**](tb-sethotitem.md), und zeigen Sie das zugehörige Menü an. Wenn die erste Schaltfläche beim Empfang dieser Benachrichtigung aktiv war, zeigen Sie das Menü für die letzte Schaltfläche an.
-   Die nach-oben-und nach-unten-Taste. Diese Schlüssel werden verwendet, um in einem Menü zu navigieren, haben jedoch keine direkte Auswirkung auf die Hot-Tracking-Menüs.
-   Eine Tastenkombination für Alt-*Taste* . Verwenden Sie die [**TB- \_ mapaccelerernachricht**](tb-mapaccelerator.md) , um zu bestimmen, welcher Schaltfläche das *Schlüssel* Zeichen entspricht. Wenn es sich um eine andere Schaltfläche als die derzeit aktive Schaltfläche handelt, reduzieren Sie das aktuelle Dropdown Menü, aktivieren Sie die neue Schaltfläche mit dem TB-Element, und zeigen Sie das Menü für die angrenzende Schaltfläche an. [**\_**](tb-sethotitem.md) Wenn das *Schlüsselzeichen* der aktuell angezeigten Schaltfläche entspricht, reduzieren Sie das Dropdown Menü, und deaktivieren Sie das Menü "Hot-Tracking". Die Schaltfläche sollte aktiv bleiben.

 

 