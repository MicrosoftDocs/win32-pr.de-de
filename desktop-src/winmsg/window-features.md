---
description: In dieser Übersicht werden Features von Windows erläutert, z. b. Fenstertypen, Zustände, Größe und Position.
ms.assetid: 8318c22f-85a2-490e-8233-ee1e234890d9
title: Fensterfeatures
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 228c6b4ab59102cae38a248935fbbad32198f2e0
ms.sourcegitcommit: 8755905962e156f29203705d09d6df8b7d0e2fca
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/25/2021
ms.locfileid: "106364569"
---
# <a name="window-features"></a>Fensterfeatures

In dieser Übersicht werden Features von Windows erläutert, z. b. Fenstertypen, Zustände, Größe und Position.

-   [Fenstertypen](#window-types)
    -   [Überlappende Fenster](#overlapped-windows)
    -   [Popup Fenster](#pop-up-windows)
    -   [Untergeordnete Fenster](#child-windows)
        -   [Positionierung](#positioning)
        -   [Freistellen](#clipping)
        -   [Beziehung zum übergeordneten Fenster](#relationship-to-parent-window)
        -   [Meldungen](#size-and-position-messages)
    -   [Überlappende Fenster](#layered-windows)
    -   [Nur-Nachricht-Fenster](#message-only-windows)
-   [Fenster Beziehungen](#window-relationships)
    -   [Vordergrund-und Hintergrund Fenster](#foreground-and-background-windows)
    -   [Eigene Fenster](#owned-windows)
    -   [Z-Reihenfolge](#z-order)
-   [Fenster Anzeige Status](#window-show-state)
    -   [Aktives Fenster](#active-window)
    -   [Deaktivierte Fenster](#disabled-windows)
    -   [Fenster Sichtbarkeit](#window-visibility)
    -   [Minimierte, maximierte und wiederhergestellte Fenster](#minimized-maximized-and-restored-windows)
-   [Fenstergröße und-Position](#window-size-and-position)
    -   [Standardgröße und-Position](#default-size-and-position)
    -   [Nach Verfolgungs Größe](#tracking-size)
    -   [System Befehle](#system-commands)
    -   [Größen-und positionsfunktionen](#size-and-position-functions)
    -   [Größen-und Positions Meldungen](#size-and-position-messages)
-   [Fenster Animation](#window-animation)
-   [Fenster Layout und-Spiegelung](#window-layout-and-mirroring)
    -   [Dialog Felder für Spiegelung und Meldungs Felder](#mirroring-dialog-boxes-and-message-boxes)
    -   [Spiegelungs Geräte Kontexte, die keinem Fenster zugeordnet sind](#mirroring-device-contexts-not-associated-with-a-window)
-   [Fenster Zerstörung](#window-destruction)

## <a name="window-types"></a>Fenstertypen

Dieser Abschnitt enthält die folgenden Themen, in denen Fenstertypen beschrieben werden.

-   [Überlappende Fenster](#overlapped-windows)
-   [Popup Fenster](#pop-up-windows)
-   [Untergeordnete Fenster](#child-windows)
-   [Überlappende Fenster](#layered-windows)
-   [Nur-Nachricht-Fenster](#message-only-windows)

### <a name="overlapped-windows"></a>Überlappende Fenster

Ein *über* Lapp Endes Fenster ist ein Fenster der obersten Ebene (nicht untergeordnetes Fenster), das eine Titelleiste, einen Rahmen und einen Client Bereich aufweist. Er soll als Hauptfenster der Anwendung dienen. Es kann auch ein Fenstermenü, minimieren und maximieren von Schaltflächen und Bild Lauf leisten enthalten. Ein überlappendes Fenster, das als Hauptfenster verwendet wird, umfasst normalerweise alle diese Komponenten.

Durch die Angabe des [**WS- \_ über**](window-styles.md) Lapp enden oder **WS \_ overlappedwindow** -Stils in [**der Funktion "**](/windows/win32/api/winuser/nf-winuser-createwindowexa) Funktion" erstellt eine Anwendung ein überlappendes Fenster. Wenn Sie den **\_ über** Lapp enden WS-Stil verwenden, verfügt das Fenster über eine Titelleiste und einen Rahmen. Wenn Sie den **WS \_ overlappedwindow** -Stil verwenden, verfügt das Fenster über eine Titelleiste, einen Größen Anpassungsrahmen, ein Fenstermenü und die Schaltflächen Minimieren und maximieren.

### <a name="pop-up-windows"></a>Popup Fenster

Ein *Popup Fenster* ist ein spezieller Typ eines überlappenden Fensters, das für Dialogfelder, Meldungs Felder und andere temporäre Fenster verwendet wird, die außerhalb des Hauptfensters der Anwendung angezeigt werden. Titelleisten sind für Popup Fenster optional. Andernfalls Stimmen Popup Fenster mit überlappenden Fenstern des [**\_ über**](window-styles.md) Lapp enden Stils überein.

Sie erstellen ein Popup Fenster, indem Sie den [**WS- \_ Popup**](window-styles.md) -Stil in " [**kreatewindowex**](/windows/win32/api/winuser/nf-winuser-createwindowexa)" angeben. Um eine Titelleiste einzuschließen, geben Sie den Stil der **WS- \_ Beschriftung** an. Verwenden Sie den **WS \_ PopupWindow** -Stil, um ein Popup Fenster mit einem Rahmen und einem Fenstermenü zu erstellen. Der **WS- \_ Beschriftungs** Stil muss mit dem **WS \_ PopupWindow** -Stil kombiniert werden, um das Fenstermenü sichtbar zu machen.

### <a name="child-windows"></a>Untergeordnete Fenster

Ein untergeordnetes *Fenster* hat den untergeordneten [**WS \_ -Stil**](window-styles.md) und ist auf den Client Bereich des übergeordneten Fensters beschränkt. Eine Anwendung verwendet in der Regel untergeordnete Fenster, um den Client Bereich eines übergeordneten Fensters in funktionale Bereiche aufzuteilen. Sie erstellen ein untergeordnetes Fenster, indem [**Sie den unter**](/windows/win32/api/winuser/nf-winuser-createwindowexa) geordneten WS-Stil in der Funktion "" in der Funktion "" von "" **\_**

Ein untergeordnetes Fenster muss über ein übergeordnetes Fenster verfügen. Das übergeordnete Fenster kann ein überlappendes Fenster, ein Popup Fenster oder sogar ein anderes untergeordnetes Fenster sein. Beim Aufrufen von " [**kreatewindowex**](/windows/win32/api/winuser/nf-winuser-createwindowexa)" geben Sie das übergeordnete Fenster an. Wenn Sie den untergeordneten [**WS \_ -Stil**](window-styles.md) in " **kreatewindowex** " angeben, aber kein übergeordnetes Fenster angeben, erstellt das System das Fenster nicht.

Ein untergeordnetes Fenster verfügt über einen Client Bereich, aber keine anderen Features, es sei denn, Sie werden explizit angefordert. Eine Anwendung kann eine Titelleiste, ein Fenstermenü, minimieren und maximieren von Schaltflächen, einen Rahmen und Bild Lauf leisten für ein untergeordnetes Fenster anfordern, aber ein untergeordnetes Fenster darf kein Menü enthalten. Wenn die Anwendung ein Menü Handle angibt, wird das Menü handle ignoriert, wenn es entweder die Fenster Klasse des Kindes registriert oder das untergeordnete Fenster erstellt. Wenn keine Rahmenart angegeben ist, erstellt das System ein Fenster ohne Rand. Eine Anwendung kann die untergeordneten Fenster eines übergeordneten Fensters verwenden, um den Client Bereich eines übergeordneten Fensters zu unterteilen, während die Bereiche für den Benutzer unsichtbar bleiben.

In diesem Abschnitt werden die folgenden Aspekte von untergeordneten Fenstern erläutert:

-   [Positionierung](#positioning)
-   [Freistellen](#clipping)
-   [Beziehung zum übergeordneten Fenster](#relationship-to-parent-window)
-   [Meldungen](#size-and-position-messages)

#### <a name="positioning"></a>Positionierung

Das System positioniert immer ein untergeordnetes Fenster in Relation zur oberen linken Ecke des Client Bereichs des übergeordneten Fensters. Kein Teil eines untergeordneten Fensters wird jemals außerhalb der Grenzen des übergeordneten Fensters angezeigt. Wenn eine Anwendung ein untergeordnetes Fenster erstellt, das größer als das übergeordnete Fenster ist, oder ein untergeordnetes Fenster positioniert, sodass einige oder alle des untergeordneten Fensters über die Grenzen des übergeordneten Fensters hinausgehen, schneidet das System das untergeordnete Fenster ab. Das heißt, der Teil außerhalb des Client Bereichs des übergeordneten Fensters wird nicht angezeigt. Aktionen, die sich auf das übergeordnete Fenster auswirken, können sich wie folgt auch auf das untergeordnete Fenster auswirken.



| Übergeordnetes Fenster | Untergeordnetes Fenster                                                                                                             |
|---------------|--------------------------------------------------------------------------------------------------------------------------|
| Wird zerstört     | Zerstört, bevor das übergeordnete Fenster zerstört wird.                                                                         |
| Ausgeblendet        | Ausgeblendet, bevor das übergeordnete Fenster ausgeblendet wird. Ein untergeordnetes Fenster ist nur sichtbar, wenn das übergeordnete Fenster sichtbar ist.             |
| Gewechselt         | Wird mit dem Client Bereich des übergeordneten Fensters verschoben. Das untergeordnete Fenster ist für das Zeichnen des Client Bereichs nach dem Verschieben verantwortlich. |
| Zeigten         | Wird angezeigt, nachdem das übergeordnete Fenster angezeigt wird.                                                                                  |



 

#### <a name="clipping"></a>Freistellen

Vom System wird ein untergeordnetes Fenster nicht automatisch aus dem Client Bereich des übergeordneten Fensters zugeschnitten. Dies bedeutet, dass das übergeordnete Fenster das untergeordnete Fenster zeichnet, wenn es eine Zeichnung an derselben Position wie das untergeordnete Fenster ausführt. Das System führt das untergeordnete Fenster jedoch aus dem Client Bereich des übergeordneten Fensters aus, wenn das übergeordnete Fenster den [**WS \_ clipchildren**](window-styles.md) -Stil hat. Wenn das untergeordnete Fenster abgeschnitten wird, kann das übergeordnete Fenster nicht darauf zeichnen.

Ein untergeordnetes Fenster kann sich auf andere untergeordnete Fenster im gleichen Client Bereich überlappen. Ein untergeordnetes Fenster, das das gleiche übergeordnete Fenster wie ein oder mehrere untergeordnete Fenster gemeinsam nutzt, wird als gleich geordnetes *Fenster* bezeichnet. Gleich geordnete Fenster können sich im Client Bereich der anderen befinden, es sei denn, eines der untergeordneten Fenster hat den Stil [**WS \_ clipanders**](window-styles.md) . Wenn ein untergeordnetes Fenster diesen Stil hat, wird jeder Teil des neben geordneten Fensters, der im untergeordneten Fenster liegt, abgeschnitten.

Wenn ein Fenster entweder den [**WS \_ clipchildren**](window-styles.md) -oder den **WS \_ clipdas** -Stil hat, tritt ein geringfügiger Leistungsverlust auf. Jedes Fenster benötigt Systemressourcen, sodass eine Anwendung untergeordnete Fenster nicht wahllos verwenden sollte. Um eine optimale Leistung zu erzielen, sollte eine Anwendung, die das Hauptfenster logisch aufteilen muss, dies in der Fenster Prozedur des Hauptfensters anstelle der Verwendung von untergeordneten Fenstern tun.

#### <a name="relationship-to-parent-window"></a>Beziehung zum übergeordneten Fenster

Eine Anwendung kann das übergeordnete Fenster eines vorhandenen untergeordneten Fensters ändern, indem Sie die [**SetParent**](/windows/win32/api/winuser/nf-winuser-setparent) -Funktion aufruft. In diesem Fall entfernt das System das untergeordnete Fenster aus dem Client Bereich des alten übergeordneten Fensters und verschiebt es in den Client Bereich des neuen übergeordneten Fensters. Wenn **SetParent** ein **null** -Handle angibt, wird das Desktop Fenster zum neuen übergeordneten Fenster. In diesem Fall wird das untergeordnete Fenster auf dem Desktop außerhalb der Rahmen eines beliebigen anderen Fensters gezeichnet. Die [**GetParent**](/windows/win32/api/winuser/nf-winuser-getparent) -Funktion Ruft ein Handle für das übergeordnete Fenster eines untergeordneten Fensters ab.

Das übergeordnete Fenster gibt einen Teil des Client Bereichs an ein untergeordnetes Fenster aus, und das untergeordnete Fenster empfängt alle Eingaben aus diesem Bereich. Die Fenster Klasse muss für jedes untergeordnete Fenster des übergeordneten Fensters nicht identisch sein. Dies bedeutet, dass eine Anwendung ein übergeordnetes Fenster mit untergeordneten Fenstern ausfüllen kann, die anders aussehen und verschiedene Tasks ausführen. Beispielsweise kann ein Dialogfeld viele Arten von Steuerelementen enthalten, von denen jedes ein untergeordnetes Fenster ist, das unterschiedliche Datentypen vom Benutzer akzeptiert.

Ein untergeordnetes Fenster hat nur ein übergeordnetes Fenster, aber ein übergeordnetes Element kann über eine beliebige Anzahl von untergeordneten Fenstern verfügen. Jedes untergeordnete Fenster kann wiederum untergeordnete Fenster enthalten. In dieser Windows-Kette wird jedes untergeordnete Fenster als Nachfolger Fenster des ursprünglichen übergeordneten Fensters bezeichnet. Eine Anwendung verwendet die [**IsChild**](/windows/win32/api/winuser/nf-winuser-ischild) -Funktion, um zu ermitteln, ob es sich bei einem angegebenen Fenster um ein untergeordnetes Fenster oder ein Nachfolger Fenster eines angegebenen übergeordneten Fensters handelt.

Die [**enumchildwindows**](/windows/win32/api/winuser/nf-winuser-enumchildwindows) -Funktion Listet die untergeordneten Fenster eines übergeordneten Fensters auf. Anschließend übergibt **enumchildwindows** das Handle an jedes untergeordnete Fenster an eine Anwendungs definierte Rückruffunktion. Nachfolgende Fenster des angegebenen übergeordneten Fensters werden ebenfalls aufgelistet.

#### <a name="messages"></a>Meldungen

Das System übergibt die Eingabe Meldungen eines untergeordneten Fensters direkt an das untergeordnete Fenster. die Nachrichten werden nicht über das übergeordnete Fenster übermittelt. Die einzige Ausnahme ist, wenn das untergeordnete Fenster durch die [**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow) -Funktion deaktiviert wurde. In diesem Fall übergibt das System alle Eingabe Meldungen, die an das untergeordnete Fenster weitergeleitet worden wären, stattdessen an das übergeordnete Fenster. Dadurch kann das übergeordnete Fenster die Eingabe Meldungen untersuchen und ggf. das untergeordnete Fenster aktivieren.

Ein untergeordnetes Fenster kann über einen eindeutigen ganzzahligen Bezeichner verfügen. Bezeichner von untergeordneten Fenstern sind beim Arbeiten mit Steuerelement Fenstern wichtig. Eine Anwendung leitet die Aktivität eines Steuer Elements durch Senden von Nachrichten weiter. Die Anwendung verwendet den untergeordneten Fenster Bezeichner des Steuer Elements, um die Nachrichten an das Steuerelement zu leiten. Außerdem sendet ein Steuerelement Benachrichtigungs Meldungen an das übergeordnete Fenster. Eine Benachrichtigungs Meldung enthält den Bezeichner des untergeordneten Fensters des Steuer Elements, mit dem das übergeordnete Element identifiziert, welches Steuerelement die Nachricht gesendet hat. Eine Anwendung gibt den Bezeichner des untergeordneten Fensters für andere Typen von untergeordneten Fenstern an, indem der *HMENU* -Parameter der Funktion " [**kreatewindowex**](/windows/win32/api/winuser/nf-winuser-createwindowexa) " auf einen Wert anstelle eines Menü Handles festgelegt wird.

### <a name="layered-windows"></a>Überlappende Fenster

Die Verwendung eines geschichteten Fensters kann die Leistung und visuelle Effekte für ein Fenster mit einer komplexen Form erheblich verbessern, seine Form animieren oder Alpha Mischungs Effekte verwenden. Das System erstellt und zeichnet automatisch mehrstufige Fenster und die Fenster der zugrunde liegenden Anwendungen. Das Ergebnis ist, dass mehrstufige Fenster reibungslos gerendert werden, ohne dass das Flimmern typisch für komplexe Fensterbereiche ist. Darüber hinaus können mehrschichtige Fenster teilweise durchsichtig werden, d. h. Alpha gemischt.

Zum Erstellen eines geschichteten Fensters geben Sie das erweiterte Fenster Format von **WS \_ \_ Ex** an, wenn Sie die [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) -Funktion aufrufen, oder rufen Sie die [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) -Funktion auf, um die **WS \_ Ex \_** -Funktion festzulegen, nachdem das Fenster erstellt wurde. Nach dem Aufruf von " **upatewindowex** " wird das Fenster "geschichtet" erst dann sichtbar, wenn die Funktion " [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) " oder " [**UpdateLayeredWindow**](/windows/win32/api/winuser/nf-winuser-updatelayeredwindow) " für dieses Fenster aufgerufen wurde.

> [!Note]  
> Ab Windows 8 kann **WS \_ Ex \_ geschichtet** mit untergeordneten Fenstern und Fenstern der obersten Ebene verwendet werden. Frühere Windows-Versionen unterstützen **WS \_ Ex \_** nur für Windows auf oberster Ebene.

 

Um die Deckkraft Ebene oder den Transparenzfarben Schlüssel für ein angegebenes geschichtetes Fenster festzulegen, müssen Sie [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes)aufrufen. Nach dem-Befehl kann das System weiterhin das Fenster anweisen, zu zeichnen, wenn das Fenster angezeigt oder die Größe geändert wird. Da das System jedoch das Bild eines geschichteten Fensters speichert, wird das Fenster vom System nicht zum Zeichnen aufgefordert, wenn Teile davon als Ergebnis relativer Fenster Verschiebungen auf dem Desktop angezeigt werden. Ältere Anwendungen müssen ihren Zeichnungs Code nicht umstrukturieren, wenn Sie für ein Fenster eine transaktionsweise oder Transparenzeffekte hinzufügen möchten, da das System das Zeichnen von Fenstern, das **SetLayeredWindowAttributes** aufrief, in den Speicher außerhalb des Bildschirms umleitet, um den gewünschten Effekt zu erzielen.

Um eine schnellere und effizientere Animation zu erhalten, oder wenn pro Pixel-Alpha benötigt wird, nennen Sie [**UpdateLayeredWindow**](/windows/win32/api/winuser/nf-winuser-updatelayeredwindow). **UpdateLayeredWindow** sollte hauptsächlich verwendet werden, wenn die Anwendung die Form und den Inhalt eines geschichteten Fensters direkt bereitstellen muss, ohne den Umleitungs Mechanismus zu verwenden, den das System über [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes)bereitstellt. Außerdem wird durch die Verwendung von **UpdateLayeredWindow** der Arbeitsspeicher direkt verwendet, da das System nicht den zusätzlichen Arbeitsspeicher benötigt, der zum Speichern des Abbilds des umgeleiteten Fensters benötigt wird. Um die optimale Effizienz bei der Animation von Fenstern zu erzielen, können Sie **UpdateLayeredWindow** aufrufen, um die Position und Größe eines geschichteten Fensters zu ändern. Beachten Sie, dass nach dem Aufruf von **SetLayeredWindowAttributes** nachfolgende **UpdateLayeredWindow** -Aufrufe fehlschlagen, bis das ebenenstilbit gelöscht und erneut festgelegt wird.

Treffer Tests eines geschichteten Fensters basieren auf der Form und Transparenz des Fensters. Dies bedeutet, dass die Maus Meldungen durch die Fensterbereiche, die farblich oder mit dem Alpha-Wert 0 (null) sind, übermittelt werden. Wenn das überlappende Fenster jedoch das erweiterte Fenster Stil von **WS \_ Ex \_ transparent** hat, wird die Form des geschichteten Fensters ignoriert, und die Mausereignisse werden an andere Fenster unterhalb des geschichteten Fensters geleitet.

### <a name="message-only-windows"></a>Message-Only Fenster

Ein Meldungs *Fenster* ermöglicht es Ihnen, Nachrichten zu senden und zu empfangen. Sie ist nicht sichtbar, hat keine z-Reihenfolge, kann nicht aufgezählt werden und empfängt keine Broadcast Nachrichten. Das Fenster sendet einfach Nachrichten.

Um ein nur-Nachricht-Fenster zu erstellen, geben Sie die [HWND \_](#message-only-windows) -Meldungs Konstante oder ein Handle für ein vorhandenes *Meldungs Fenster im hwndParent* -Parameter [**der Funktion "**](/windows/win32/api/winuser/nf-winuser-createwindowexa) -Funktion" an. Sie können auch ein vorhandenes Fenster in ein Meldungs Fenster ändern, indem Sie eine HWND- \_ Nachricht im *hwndnewparent* -Parameter der [**SetParent**](/windows/win32/api/winuser/nf-winuser-setparent) -Funktion angeben.

Um nur-Meldung-Fenster zu suchen, geben Sie im *hwndParent* -Parameter der [**FindWindowEx**](/windows/win32/api/winuser/nf-winuser-findwindowexa) -Funktion eine [HWND- \_ Nachricht](#message-only-windows) an. Außerdem durchsucht **FindWindowEx** nur Nachrichtenfenster sowie Fenster der obersten Ebene, wenn die Parameter *hwndParent* und *hwndchildafter* **null** sind.

## <a name="window-relationships"></a>Fenster Beziehungen

Es gibt viele Möglichkeiten, wie ein Fenster mit dem Benutzer oder einem anderen Fenster verknüpft werden kann. Ein Fenster kann ein eigenes Fenster, ein Vordergrund Fenster oder ein Hintergrund Fenster sein. Ein Fenster hat auch eine z-Reihenfolge, die relativ zu anderen Fenstern ist. Weitere Informationen finden Sie unter den folgenden Themen:

-   [Vordergrund-und Hintergrund Fenster](#foreground-and-background-windows)
-   [Eigene Fenster](#owned-windows)
-   [Z-Reihenfolge](#z-order)

### <a name="foreground-and-background-windows"></a>Vordergrund-und Hintergrund Fenster

Jeder Prozess kann mehrere Ausführungs Threads aufweisen, und jeder Thread kann Fenster erstellen. Der Thread, der das Fenster erstellt hat, mit dem der Benutzer gerade arbeitet, wird als Vordergrund Thread bezeichnet, und das Fenster wird als *Vordergrund Fenster* bezeichnet. Alle anderen Threads sind Hintergrundthreads, und die von Hintergrundthreads erstellten Fenster werden als *Hintergrund Fenster* bezeichnet.

Jeder Thread verfügt über eine Prioritätsstufe, die die vom Thread empfangene CPU-Zeit bestimmt. Obwohl eine Anwendung die Prioritäts Ebene der Threads festlegen kann, hat der Vordergrund Thread normalerweise eine etwas höhere Prioritätsstufe als die Hintergrundthreads. Da er eine höhere Priorität hat, erhält der Vordergrund Thread mehr CPU-Zeit als die Hintergrundthreads. Der Vordergrund Thread hat eine normale Basis Priorität von 9. ein Hintergrund Thread hat eine normale Basis Priorität von 7.

Der Benutzer legt das Vordergrund Fenster durch Klicken auf ein Fenster oder mithilfe der Tastenkombination Alt + Tab oder ALT + ESC fest. Um ein Handle für das Vordergrund Fenster abzurufen, verwenden Sie die [**getforegroundwindow**](/windows/win32/api/winuser/nf-winuser-getforegroundwindow) -Funktion. Um zu überprüfen, ob es sich bei Ihrem Anwendungsfenster um das Vordergrund Fenster handelt, vergleichen Sie das von **getforegroundwindow** zurückgegebene Handle mit dem des Anwendungsfensters.

Eine Anwendung legt das Vordergrund Fenster mithilfe der [**SetForegroundWindow**](/windows/win32/api/winuser/nf-winuser-setforegroundwindow) -Funktion fest.

Das System schränkt ein, welche Prozesse das Vordergrund Fenster festlegen können. Ein Prozess kann das Vordergrund Fenster nur dann festlegen, wenn:

- Alle folgenden Bedingungen sind erfüllt:
  - Der Prozess, der **SetForegroundWindow** aufruft, gehört zu einer Desktop Anwendung, nicht zu einer UWP-APP oder einer Windows Store-App, die für Windows 8 oder 8,1 entworfen wurde.
  - Der Vordergrund Prozess hat Aufrufe von **SetForegroundWindow** nicht durch einen vorherigen Aufruf der [**locksetforegroundwindow**](/windows/win32/api/winuser/nf-winuser-locksetforegroundwindow) -Funktion deaktiviert.
  - Das Timeout für die Vordergrund Sperre ist abgelaufen (Weitere Informationen finden Sie [unter **SPI_GETFOREGROUNDLOCKTIMEOUT** in **SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa#SPI_GETFOREGROUNDLOCKTIMEOUT)).
  - Es sind keine Menüs aktiv.
- Außerdem ist mindestens eine der folgenden Bedingungen erfüllt:
  - Der Aufrufprozess ist der Vordergrund Prozess.
  - Der Aufrufprozess wurde vom Vordergrund Prozess gestartet.
  - Zurzeit ist kein Vordergrund Fenster und somit kein Vordergrund Prozess vorhanden.
  - Der Aufrufprozess hat das letzte Eingabe Ereignis empfangen.
  - Der Vordergrund Prozess oder der aufrufende Prozess wird debuggt.

Es ist möglich, dass einem Prozess das Recht verweigert wird, das Vordergrund Fenster selbst dann festzulegen, wenn er diese Bedingungen erfüllt.

Ein Prozess, der das Vordergrund Fenster festlegen kann, kann einen anderen Prozess aktivieren, um das Vordergrund Fenster durch Aufrufen der [**allowsetforegroundwindow**](/windows/win32/api/winuser/nf-winuser-allowsetforegroundwindow) -Funktion oder durch Aufrufen der [**broadcastsystemmessage**](/windows/win32/api/winuser/nf-winuser-broadcastsystemmessage) -Funktion mit dem **BSF \_ allowsfw** -Flag festzulegen. Der Vordergrund Prozess kann Aufrufe von [**SetForegroundWindow**](/windows/win32/api/winuser/nf-winuser-setforegroundwindow) deaktivieren, indem er die [**locksetforegroundwindow**](/windows/win32/api/winuser/nf-winuser-locksetforegroundwindow) -Funktion aufruft.

### <a name="owned-windows"></a>Eigene Fenster

Ein überlappendes oder Popup Fenster kann im Besitz eines anderen überlappenden oder Popup Fensters sein. Wenn Sie im Besitz sind, werden in einem Fenster mehrere Einschränkungen abgelegt.

-   Ein eigenes Fenster befindet sich immer oberhalb seines Besitzers in der z-Reihenfolge.
-   Das System zerstört automatisch ein eigenes Fenster, wenn der Besitzer zerstört wird.
-   Ein eigenes Fenster wird ausgeblendet, wenn der Besitzer minimiert wird.

Nur ein überlappendes oder Popup Fenster kann ein Besitzer Fenster sein. ein untergeordnetes Fenster kann nicht als Besitzer Fenster fungieren. Eine Anwendung erstellt ein eigenes Fenster, indem das Fenster Handle des Besitzers als *hwndParent* -Parameter von " [**kreatewindowex**](/windows/win32/api/winuser/nf-winuser-createwindowexa) " angegeben wird, wenn ein Fenster mit dem [**\_ über**](window-styles.md) Lapp enden oder dem **WS- \_ Popup** Stil erstellt wird. Der *hwndParent* -Parameter muss ein überlappendes oder ein Popup Fenster identifizieren. Wenn *hwndParent* ein untergeordnetes Fenster identifiziert, weist das System den Besitz dem übergeordneten Fenster der obersten Ebene des untergeordneten Fensters zu. Nachdem Sie ein eigenes Fenster erstellt haben, kann eine Anwendung den Besitz des Fensters nicht auf ein anderes Fenster übertragen.

Dialog Felder und Meldungs Felder befinden sich standardmäßig im Besitz von Fenstern. Eine Anwendung gibt das Besitzer Fenster an, wenn eine Funktion aufgerufen wird, die ein Dialogfeld oder ein Meldungs Feld erstellt.

Eine Anwendung kann die [**GetWindow**](/windows/win32/api/winuser/nf-winuser-getwindow) -Funktion mit dem **GW \_** -Besitzerflag verwenden, um ein Handle für den Besitzer eines Fensters abzurufen.

### <a name="z-order"></a>Z-Reihenfolge

Die *z-Reihenfolge* eines Fensters gibt an, dass die Position des Fensters in einem Stapel von überlappenden Fenstern angezeigt wird. Dieser Fenster Stapel ist auf eine imaginäre Achse ausgerichtet, die z-Achse, die sich nach außen vom Bildschirm erstreckt. Das Fenster oben in der z-Reihenfolge überlappt alle anderen Fenster. Das Fenster am Ende der z-Reihenfolge wird von allen anderen Fenstern überlappen.

Das System verwaltet die z-Reihenfolge in einer einzigen Liste. Je nachdem, ob es sich um die obersten Fenster, Fenster der obersten Ebene oder um untergeordnete Fenster handelt, wird die z-Reihenfolge von Fenstern hinzugefügt. Ein *oberstes Fenster* überlappt alle anderen nicht-obersten Fenster, unabhängig davon, ob es sich um das aktive oder Vordergrund Fenster handelt. Ein oberstes Fenster hat den **\_ \_ obersten WS** -Stil. Alle obersten Fenster werden in der z-Reihenfolge vor allen nicht obersten Fenstern angezeigt. Ein untergeordnetes Fenster wird mit dem übergeordneten Fenster in z-Reihenfolge gruppiert.

Wenn eine Anwendung ein Fenster erstellt, legt das System Sie in der z-Reihenfolge für Windows desselben Typs ab. Sie können die Funktion " [**bringwindowdetop**](/windows/win32/api/winuser/nf-winuser-bringwindowtotop) " verwenden, um ein Fenster an den Anfang der z-Reihenfolge für Windows desselben Typs zu bringen. Sie können die z-Reihenfolge mithilfe der Funktionen [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) und [**deferwindowpos**](/windows/win32/api/winuser/nf-winuser-deferwindowpos) neu anordnen.

Der Benutzer ändert die z-Reihenfolge durch Aktivieren eines anderen Fensters. Das System positioniert das aktive Fenster am Anfang der z-Reihenfolge für Windows desselben Typs. Wenn ein Fenster an die Spitze der z-Reihenfolge geht, müssen die untergeordneten Fenster angezeigt werden. Sie können die [**gettopwindow**](/windows/win32/api/winuser/nf-winuser-gettopwindow) -Funktion verwenden, um alle untergeordneten Fenster eines übergeordneten Fensters zu durchsuchen und ein Handle für das untergeordnete Fenster zurückzugeben, das in der z-Reihenfolge am höchsten ist. Die [**getnextwindow**](/windows/win32/api/winuser/nf-winuser-getnextwindow) -Funktion Ruft ein Handle für das nächste oder vorherige Fenster in der z-Reihenfolge ab.

## <a name="window-show-state"></a>Fenster Anzeige Status

Ein Fenster ist möglicherweise zu einem bestimmten Zeitpunkt aktiv oder inaktiv. ausgeblendet oder sichtbar; und minimiert, maximiert oder wieder hergestellt. Diese Qualitäten werden zusammen als *Fenster Anzeige Zustand* bezeichnet. In den folgenden Themen wird der Zustand der Fenster Anzeige erläutert:

-   [Aktives Fenster](#active-window)
-   [Deaktivierte Fenster](#disabled-windows)
-   [Fenster Sichtbarkeit](#window-visibility)
-   [Minimierte, maximierte und wiederhergestellte Fenster](#minimized-maximized-and-restored-windows)

### <a name="active-window"></a>Aktives Fenster

Ein *Aktives Fenster* ist das Fenster der Anwendung auf oberster Ebene, mit dem der Benutzer gerade arbeitet. Damit der Benutzer das aktive Fenster leicht identifizieren kann, platziert das System ihn am Anfang der z-Reihenfolge und ändert die Farbe der Titelleiste und des Rahmens in die System definierten aktiven Fenster Farben. Nur ein Fenster der obersten Ebene kann ein aktives Fenster sein. Wenn der Benutzer mit einem untergeordneten Fenster arbeitet, aktiviert das System das übergeordnete Fenster der obersten Ebene, das mit dem untergeordneten Fenster verknüpft ist.

Es ist jeweils nur ein Fenster der obersten Ebene im System aktiv. Der Benutzer aktiviert ein Fenster auf oberster Ebene, indem er (oder eines seiner untergeordneten Fenster) darauf klickt oder die Tastenkombination ALT + ESC oder Alt + Tab verwendet. Eine Anwendung aktiviert ein Fenster der obersten Ebene durch Aufrufen der [**SetActiveWindow**](/windows/win32/api/winuser/nf-winuser-setactivewindow) -Funktion. Andere Funktionen können bewirken, dass das System ein anderes Fenster der obersten Ebene aktiviert, einschließlich [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos), [**deferwindowpos**](/windows/win32/api/winuser/nf-winuser-deferwindowpos), [**SetWindowPlacement**](/windows/win32/api/winuser/nf-winuser-setwindowplacement)und [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow). Obwohl eine Anwendung jederzeit ein anderes Fenster der obersten Ebene aktivieren kann, sollte Sie dies nur als Reaktion auf eine Benutzeraktion tun, um zu vermeiden, dass der Benutzer verwirrend ist. Eine Anwendung verwendet die [**GetActiveWindow**](/windows/win32/api/winuser/nf-winuser-getactivewindow) -Funktion, um ein Handle für das aktive Fenster abzurufen.

Wenn sich die Aktivierung von einem Fenster der obersten Ebene einer Anwendung in das Fenster der obersten Ebene einer anderen Anwendung ändert, sendet das System eine [**WM \_ activateapp**](wm-activateapp.md) -Nachricht an beide Anwendungen und benachrichtigt Sie über die Änderung. Wenn sich die Aktivierung in ein anderes Fenster der obersten Ebene in derselben Anwendung ändert, sendet das System beide Windows eine [**WM- \_ Aktivierungs**](../inputdev/wm-activate.md) Nachricht.

### <a name="disabled-windows"></a>Deaktivierte Fenster

Ein Fenster kann deaktiviert werden. Ein *deaktiviertes Fenster* empfängt keine Tastatur-oder Maus Eingaben vom Benutzer, kann aber Nachrichten von anderen Fenstern, von anderen Anwendungen und vom System empfangen. In einer Anwendung wird in der Regel ein Fenster deaktiviert, um zu verhindern, dass der Benutzer das Fenster verwendet. Beispielsweise kann eine Anwendung eine pushschaltfläche in einem Dialogfeld deaktivieren, um zu verhindern, dass der Benutzer die Schaltfläche auswählt. Eine Anwendung kann ein deaktiviertes Fenster jederzeit aktivieren. durch das Aktivieren eines Fensters werden normale Eingaben wieder hergestellt.

Standardmäßig wird ein Fenster aktiviert, wenn es erstellt wird. Eine Anwendung kann jedoch das [**\_ Deaktivierte WS**](window-styles.md) -Format angeben, um ein neues Fenster zu deaktivieren. Eine Anwendung aktiviert oder deaktiviert ein vorhandenes Fenster mithilfe der [**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow) -Funktion. Das System sendet eine [**WM- \_ Aktivierungs**](wm-enable.md) Meldung an ein Fenster, wenn sich der aktivierte Zustand im Begriff ist zu ändern. Eine Anwendung kann mithilfe der [**iswindowenabled**](/windows/win32/api/winuser/nf-winuser-iswindowenabled) -Funktion ermitteln, ob ein Fenster aktiviert ist.

Wenn ein untergeordnetes Fenster deaktiviert ist, übergibt das System die Mauseingabe Meldungen des untergeordneten Elements an das übergeordnete Fenster. Das übergeordnete Element verwendet anhand der Meldungen, ob das untergeordnete Fenster aktiviert werden soll. Weitere Informationen finden Sie unter [Maus Eingaben](../inputdev/mouse-input.md).

Nur ein Fenster gleichzeitig kann Tastatureingaben empfangen. Dieses Fenster hat den Tastaturfokus. Wenn eine Anwendung die [**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow) -Funktion zum Deaktivieren eines Tastaturfokus Fensters verwendet, verliert das Fenster den Tastaturfokus zusätzlich zu der Deaktivierung. **EnableWindow** legt den Tastaturfokus dann auf **null** fest, was bedeutet, dass kein Fenster den Fokus besitzt. Wenn ein untergeordnetes Fenster oder ein anderes Nachfolger Fenster den Tastaturfokus besitzt, verliert das Nachfolger Fenster den Fokus, wenn das übergeordnete Fenster deaktiviert ist. Weitere Informationen finden Sie unter [Tastatureingabe](../inputdev/keyboard-input.md).

### <a name="window-visibility"></a>Fenster Sichtbarkeit

Ein Fenster kann sichtbar oder ausgeblendet sein. Das System zeigt ein *sichtbares Fenster* auf dem Bildschirm an. Ein ausgeblendetes *Fenster wird ausgeblendet* , wenn es nicht gezeichnet wird. Wenn das Fenster sichtbar ist, kann der Benutzer im Fenster Eingaben vornehmen und sich die Fensterausgabe anzeigen lassen. Ein ausgeblendetes Fenster ist deaktiviert. Ein ausgeblendetes Fenster kann zwar Meldungen vom System oder anderen Fenstern verarbeiten, kann jedoch keine Benutzereingaben verarbeiten oder Ausgaben anzeigen. Eine Anwendung legt den Sichtbarkeits Zustand eines Fensters fest, wenn das Fenster erstellt wird. Später kann die Anwendung den Sichtbarkeits Status ändern.

Ein Fenster ist sichtbar, wenn [**das \_ sichtbare WS**](window-styles.md) -Format für das Fenster festgelegt ist. Standardmäßig wird von der Funktion " [**kreatewindowex**](/windows/win32/api/winuser/nf-winuser-createwindowexa) " ein verborgenes Fenster erstellt, es sei denn, die Anwendung gibt den **\_ sichtbaren WS** -Stil In der Regel legt eine Anwendung **den \_ sichtbaren WS** -Stil fest, nachdem ein Fenster erstellt wurde, in dem die Details des Erstellungs Prozesses für den Benutzer ausgeblendet werden. Beispielsweise kann eine Anwendung ein neues Fenster ausblenden, während die Darstellung des Fensters angepasst wird. Wenn das **\_ sichtbare WS** -Format in der Datei " **kreatewindowex**" angegeben ist, sendet das System nach dem Erstellen des Fensters, jedoch vor der Anzeige, die [**WM- \_ Show Window**](wm-showwindow.md) -Meldung an das Fenster.

Eine Anwendung kann mithilfe der [**iswindowvisible**](/windows/win32/api/winuser/nf-winuser-iswindowvisible) -Funktion ermitteln, ob ein Fenster sichtbar ist. Eine Anwendung kann ein Fenster anzeigen (sichtbar machen) oder ausblenden, indem Sie die Funktion [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow), [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos), [**deferwindowpos**](/windows/win32/api/winuser/nf-winuser-deferwindowpos)oder [**SetWindowPlacement**](/windows/win32/api/winuser/nf-winuser-setwindowplacement) oder [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) verwendet. Diese Funktionen zeigen ein Fenster an oder blenden es aus, indem Sie den [**\_ sichtbaren WS**](window-styles.md) -Stil für das Fenster festlegen oder entfernen. Außerdem wird die [**WM- \_ Show Window**](wm-showwindow.md) -Meldung an das Fenster gesendet, bevor Sie angezeigt oder ausgeblendet wird.

Wenn ein Besitzer Fenster minimiert wird, verbirgt das System automatisch die zugehörigen Windows-Fenster. Wenn ein Besitzer Fenster wieder hergestellt wird, zeigt das System auch automatisch die zugehörigen Windows-Fenster an. In beiden Fällen sendet das System die [**\_ Show Window**](wm-showwindow.md) -Meldung von WM an die eigenen Fenster, bevor Sie ausgeblendet oder angezeigt werden. Gelegentlich kann es vorkommen, dass eine Anwendung die eigenen Fenster ausblenden muss, ohne den Besitzer minimieren oder ausblenden zu müssen. In diesem Fall verwendet die Anwendung die [**showownedpopups**](/windows/win32/api/winuser/nf-winuser-showownedpopups) -Funktion. Diese Funktion legt den [**\_ sichtbaren WS**](window-styles.md) -Stil für alle eigenen Fenster fest oder entfernt Sie und sendet die **WM- \_ Show Window** -Meldung an die eigenen Fenster, bevor Sie ausgeblendet oder angezeigt werden. Das Ausblenden eines Besitzer Fensters hat keine Auswirkung auf den Sichtbarkeits Zustand der eigenen Fenster.

Wenn ein übergeordnetes Fenster sichtbar ist, sind auch die zugehörigen untergeordneten Fenster sichtbar. Ebenso, wenn das übergeordnete Fenster ausgeblendet wird, werden auch die untergeordneten Fenster ausgeblendet. Das Minimieren des übergeordneten Fensters hat keine Auswirkung auf den Sichtbarkeits Zustand der untergeordneten Fenster. Das heißt, die untergeordneten Fenster werden zusammen mit dem übergeordneten Fenster minimiert, aber der [**\_ sichtbare WS**](window-styles.md) -Stil wird nicht geändert.

Auch wenn ein Fenster über den [**\_ sichtbaren WS**](window-styles.md) -Stil verfügt, kann der Benutzer das Fenster auf dem Bildschirm nicht anzeigen. andere Fenster überlappen es möglicherweise, oder es wurde über den Bildschirmrand hinaus verschoben. Außerdem unterliegt ein sichtbares untergeordnetes Fenster den clippingregeln, die von der über-/Unterordnungsbeziehung hergestellt werden. Wenn das übergeordnete Fenster des Fensters nicht sichtbar ist, wird es ebenfalls nicht angezeigt. Wenn das übergeordnete Fenster über den Bildschirmrand hinaus verschoben wird, wird das untergeordnete Fenster ebenfalls verschoben, weil ein untergeordnetes Fenster relativ zur oberen linken Ecke des übergeordneten Fensters gezeichnet wird. Beispielsweise kann ein Benutzer das übergeordnete Fenster, das das untergeordnete Fenster enthält, weit über den Bildschirmrand hinaus verschieben, sodass der Benutzer möglicherweise das untergeordnete Fenster nicht sehen kann, obwohl sowohl das untergeordnete Fenster als auch das übergeordnete Fenster beide den **\_ sichtbaren WS** -Stil aufweisen.

### <a name="minimized-maximized-and-restored-windows"></a>Minimierte, maximierte und wiederhergestellte Fenster

Ein *maximiertes Fenster* ist ein Fenster, das den Stil der WS-Maximierung [**\_ maximiert**](window-styles.md) . In der Standardeinstellung wird ein maximiertes Fenster so vergrößert, dass es den Bildschirm oder, im Fall eines untergeordneten Fensters, den Clientbereich des übergeordneten Fensters ausfüllt. Obwohl die Größe eines Fensters auf dieselbe Größe eines maximierten Fensters festgelegt werden kann, unterscheidet sich ein maximiertes Fenster leicht. Das System verschiebt die Titelleiste des Fensters automatisch an den oberen Rand des Bildschirms oder an den oberen Rand des Client Bereichs des übergeordneten Fensters. Außerdem deaktiviert das System den Größen Anpassungsrahmen und die Fenster Positions Funktion der Titelleiste (sodass der Benutzer das Fenster nicht durchziehen der Titelleiste verschieben kann).

Ein *minimiertes Fenster* ist ein Fenster, das die [**WS- \_ minimieren**](window-styles.md) -Art aufweist. In der Standardeinstellung wird ein minimiertes Fenster auf die Größe seiner Schaltfläche auf der Taskleiste verkleinert und auf die Taskleiste verschoben. Ein *wiederhergestelltes Fenster* ist ein Fenster, das an seine vorherige Größe und Position zurückgegeben wurde, d. h. die Größe, die vor dem minimieren oder maximieren aufgetreten ist.

Wenn eine Anwendung den Wert für die [**WS- \_ Maximierung**](window-styles.md) oder das **\_ minimieren** in [**der Funktion "**](/windows/win32/api/winuser/nf-winuser-createwindowexa) die Funktion" "in der Funktion" "in der Funktion" Funktion "in der Funktion" Funktion " Nachdem Sie ein Fenster erstellt haben, kann eine Anwendung die [**CloseWindow**](/windows/win32/api/winuser/nf-winuser-closewindow) -Funktion verwenden, um das Fenster zu minimieren. Die [**arrangeicricwindows**](/windows/win32/api/winuser/nf-winuser-arrangeiconicwindows) -Funktion ordnet die Symbole auf dem Desktop an oder ordnet die minimierten untergeordneten Fenster eines übergeordneten Fensters im übergeordneten Fenster an. Die [**openicon**](/windows/win32/api/winuser/nf-winuser-openicon) -Funktion stellt ein minimiertes Fenster an der vorherigen Größe und Position wieder her.

Die [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) -Funktion kann ein Fenster minimieren, maximieren oder wiederherstellen. Er kann auch die Sichtbarkeit und den Aktivierungs Status des Fensters festlegen. Die [**SetWindowPlacement**](/windows/win32/api/winuser/nf-winuser-setwindowplacement) -Funktion umfasst die gleiche Funktionalität wie **ShowWindow**, aber Sie kann die standardmäßig minimierten, maximierten und wiederhergestellten Positionen des Fensters überschreiben.

Die [**IsZoomed**](/windows/win32/api/winuser/nf-winuser-iszoomed) -und [**ISI-**](/windows/win32/api/winuser/nf-winuser-isiconic) Funktionen bestimmen, ob ein bestimmtes Fenster maximiert bzw. minimiert wird. Die [**GetWindowPlacement**](/windows/win32/api/winuser/nf-winuser-getwindowplacement) -Funktion Ruft die minimierten, maximierten und wiederhergestellten Positionen für das Fenster ab und bestimmt außerdem den Anzeige Zustand des Fensters.

Wenn das System einen Befehl zum Maximieren oder Wiederherstellen eines minimierten Fensters empfängt, sendet es eine [**WM \_ queryopen**](wm-queryopen.md) -Nachricht an das Fenster. Wenn die Fenster Prozedur **false** zurückgibt, ignoriert das System den Befehl zum Maximieren oder wiederherstellen.

Das System legt automatisch die Größe und die Position eines maximierten Fensters auf die System definierten Standardwerte für ein maximiertes Fenster fest. Um diese Standardwerte zu überschreiben, kann eine Anwendung entweder die [**SetWindowPlacement**](/windows/win32/api/winuser/nf-winuser-setwindowplacement) -Funktion aufrufen oder die von einem Fenster empfangene [**WM \_ getminmaxinfo**](wm-getminmaxinfo.md) -Meldung verarbeiten, wenn das System im Begriff ist, das Fenster zu maximieren. **WM \_ Getminmaxinfo** enthält einen Zeiger auf eine [**minmaxinfo**](/windows/win32/api/winuser/ns-winuser-minmaxinfo) -Struktur mit Werten, die vom System verwendet werden, um die maximierte Größe und Position festzulegen. Durch Ersetzen dieser Werte werden die Standardwerte überschrieben.

## <a name="window-size-and-position"></a>Fenstergröße und-Position

Die Größe und Position eines Fensters werden als Begrenzungs Rechteck ausgedrückt, das in den Koordinaten relativ zum Bildschirm oder im übergeordneten Fenster angegeben wird. Die Koordinaten eines Fensters der obersten Ebene sind relativ zur oberen linken Ecke des Bildschirms. die Koordinaten eines untergeordneten Fensters sind relativ zur linken oberen Ecke des übergeordneten Fensters. Eine Anwendung gibt die anfängliche Größe und Position eines Fensters an, wenn das Fenster erstellt wird, kann jedoch die Größe und Position des Fensters jederzeit ändern. Weitere Informationen finden Sie unter [gefüllte Formen](../gdi/filled-shapes.md).

Dieser Abschnitt enthält die folgenden Themen:

-   [Standardgröße und-Position](#default-size-and-position)
-   [Nach Verfolgungs Größe](#tracking-size)
-   [System Befehle](#system-commands)
-   [Größen-und positionsfunktionen](#size-and-position-functions)
-   [Größen-und Positions Meldungen](#size-and-position-messages)

### <a name="default-size-and-position"></a>Standardgröße und-Position

Eine Anwendung kann es dem System ermöglichen, die anfängliche Größe oder Position eines Fensters der obersten Ebene zu berechnen, indem CW \_ usedefault in " [**kreatewindowex**](/windows/win32/api/winuser/nf-winuser-createwindowexa)" angegeben wird. Wenn die Anwendung die Koordinaten des Fensters auf CW \_ usedefault festlegt und keine anderen Fenster der obersten Ebene erstellt hat, legt das System die Position des neuen Fensters relativ zur oberen linken Ecke des Bildschirms fest. andernfalls wird die Position relativ zur Position des Fensters der obersten Ebene festgelegt, das von der Anwendung zuletzt erstellt wurde. Wenn die Width-und height-Parameter auf CW \_ usedefault festgelegt sind, berechnet das System die Größe des neuen Fensters. Wenn die Anwendung andere Fenster der obersten Ebene erstellt hat, basiert das System auf der Größe des neuen Fensters auf der Größe des zuletzt erstellten Fensters der obersten Ebene der Anwendung. Das angeben \_ von CW usedefault beim Erstellen eines untergeordneten oder Popup Fensters bewirkt, dass das System die Größe des Fensters auf die standardmäßige minimale Fenstergröße festlegt.

### <a name="tracking-size"></a>Nach Verfolgungs Größe

Das System behält eine minimale und maximale nach Verfolgungs Größe für ein Fenster des [**WS- \_ thickframe**](window-styles.md) -Stils bei. ein Fenster mit diesem Stil hat einen Größen Anpassungsrahmen. Die *minimale nach Verfolgungs Größe* ist die kleinste Fenstergröße, die Sie durchziehen des Größen Anpassungs Rahmens des Fensters erreichen können. Ebenso ist die *Maximale nach Verfolgungs Größe* die größte Fenstergröße, die Sie durchziehen des Größen Anpassungs Rahmens erreichen können.

Die minimalen und maximalen nach Verfolgungs Größen eines Fensters werden auf System definierte Standardwerte festgelegt, wenn das System das Fenster erstellt. Eine Anwendung kann die Standardwerte ermitteln und überschreiben, indem Sie die [**WM \_ getminmaxinfo**](wm-getminmaxinfo.md) -Nachricht verarbeitet. Weitere Informationen finden Sie unter [Größen-und Positions Nachrichten](#size-and-position-messages).

### <a name="system-commands"></a>System Befehle

Eine Anwendung, die über ein Fenstermenü verfügt, kann die Größe und Position des Fensters ändern, indem Systembefehle gesendet werden. System Befehle werden generiert, wenn der Benutzer im Menü Fenster Befehle auswählt. Eine Anwendung kann die Benutzeraktion emulieren, indem Sie eine [**WM- \_ syscommand**](../menurc/wm-syscommand.md) -Meldung an das Fenster sendet. Die folgenden Systembefehle beeinflussen die Größe und Position eines Fensters.



| Get-Help      | BESCHREIBUNG                                                                                                                                                          |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SC \_ Schließen    | Schließt das Fenster. Mit diesem Befehl wird eine " [**WM \_ Close**](wm-close.md) "-Meldung an das Fenster gesendet. Das Fenster führt alle Schritte aus, die zum Bereinigen und zerstören selbst erforderlich sind. |
| SC \_ maximieren | Maximiert das Fenster.                                                                                                                                                |
| SC \_ minimieren | Minimiert das Fenster.                                                                                                                                                |
| SC- \_ Verschiebung     | Verschiebt das Fenster.                                                                                                                                                    |
| SC- \_ Wiederherstellung  | Stellt die vorherige Größe und Position eines minimierten oder maximierten Fensters wieder her.                                                                                          |
| SC- \_ Größe     | Startet einen Größen Befehl. Verwenden Sie die Maus oder die Tastatur, um die Größe des Fensters zu ändern.                                                                                  |



 

### <a name="size-and-position-functions"></a>Größen-und positionsfunktionen

Nachdem Sie ein Fenster erstellt haben, kann eine Anwendung die Größe oder Position des Fensters durch Aufrufen einer von mehreren verschiedenen Funktionen festlegen, einschließlich [**SetWindowPlacement**](/windows/win32/api/winuser/nf-winuser-setwindowplacement), [**muvewindow**](/windows/win32/api/winuser/nf-winuser-movewindow), [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos)und [**deferwindowpos**](/windows/win32/api/winuser/nf-winuser-deferwindowpos). **SetWindowPlacement** legt die minimierte Position eines Fensters, die maximierte Position, die wiederhergestellte Größe und Position und den Zustand anzeigen fest. Die Funktionen " **muvewindow** " und " **SetWindowPos** " ähneln einander. Legen Sie die Größe oder Position eines einzelnen Anwendungsfensters fest. Die **SetWindowPos** -Funktion enthält einen Satz von Flags, die den Anzeige Zustand des Fensters beeinflussen. " **Muvewindow** " enthält diese Flags nicht. Verwenden Sie die Funktionen [**begindeferwindowpos**](/windows/win32/api/winuser/nf-winuser-begindeferwindowpos), **deferwindowpos** und [**enddeferwindowpos**](/windows/win32/api/winuser/nf-winuser-enddeferwindowpos) , um die Position einer Reihe von Fenstern gleichzeitig festzulegen, einschließlich Größe, Position, Position in der z-Reihenfolge und Anzeige Zustand.

Eine Anwendung kann die Koordinaten des umgebenden Rechtecks eines Fensters mithilfe der [**GetWindowRect**](/windows/win32/api/winuser/nf-winuser-getwindowrect) -Funktion abrufen. **GetWindowRect** füllt eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur mit den Koordinaten der oberen linken und unteren rechten Ecke des Fensters. Die Koordinaten sind relativ zur linken oberen Ecke des Bildschirms, auch für ein untergeordnetes Fenster. Die [**ScreenToClient**](/windows/win32/api/winuser/nf-winuser-screentoclient) -oder [**mapwindowpoints**](/windows/win32/api/winuser/nf-winuser-mapwindowpoints) -Funktion ordnet die Bildschirm Koordinaten des umgebenden Rechtecks eines untergeordneten Fensters den Koordinaten relativ zum Client Bereich des übergeordneten Fensters zu.

Die [**GetClientRect**](/windows/win32/api/winuser/nf-winuser-getclientrect) -Funktion Ruft die Koordinaten des Client Bereichs eines Fensters ab. **GetClientRect** füllt eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur mit den Koordinaten der oberen linken und unteren rechten Ecke des Client Bereichs, aber die Koordinaten sind relativ zum Client Bereich. Dies bedeutet, dass die Koordinaten der oberen linken Ecke eines Client Bereichs immer (0,0) sind, und die Koordinaten der unteren rechten Ecke sind Breite und Höhe des Client Bereichs.

Die [**cascadewindows**](/windows/win32/api/winuser/nf-winuser-cascadewindows) -Funktion kaskadiert die Fenster auf dem Desktop oder kaskadiert die untergeordneten Fenster des angegebenen übergeordneten Fensters. Die [**tilewindows**](/windows/win32/api/winuser/nf-winuser-tilewindows) -Funktion Kacheln die Fenster auf dem Desktop oder Kacheln die untergeordneten Fenster des angegebenen übergeordneten Fensters.

### <a name="size-and-position-messages"></a>Größen-und Positions Meldungen

Das System sendet die [**WM- \_ getminmaxinfo**](wm-getminmaxinfo.md) -Meldung an ein Fenster, dessen Größe oder Position gerade geändert wird. Beispielsweise wird die Nachricht gesendet, wenn der Benutzer im Menü Fenster auf **verschieben** oder **Größe** klickt oder auf den Größen Anpassungsrahmen oder die Titelleiste klickt. die Meldung wird auch gesendet, wenn eine Anwendung [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) aufruft, um das Fenster zu verschieben oder zu verkleinern. **WM \_ Getminmaxinfo** enthält einen Zeiger auf eine [**minmaxinfo**](/windows/win32/api/winuser/ns-winuser-minmaxinfo) -Struktur, die die standardmäßige maximierte Größe und Position für das Fenster sowie die standardmäßigen minimalen und maximalen nach Verfolgungs Größen enthält. Eine Anwendung kann die Standardwerte überschreiben, indem **WM \_ getminmaxinfo** verarbeitet und die entsprechenden Member von **minmaxinfo** festgelegt werden. Ein Fenster muss den [**WS- \_ dicken Rahmen**](window-styles.md) oder den **WS- \_ Beschriftungs** Stil aufweisen, um **WM \_ getminmaxinfo** zu empfangen. Ein Fenster mit der Art des **WS- \_ dicken Rahmens** empfängt diese Meldung während des Erstellungs Prozesses des Fensters sowie beim Verschieben oder größenwechsel.

Das System sendet die [**WM- \_ windowposchanging**](wm-windowposchanging.md) -Nachricht an ein Fenster, dessen Größe, Position, Position in der z-Reihenfolge oder Anzeige Zustand gerade geändert wird. Diese Meldung enthält einen Zeiger auf eine [**Windows POS**](/windows/win32/api/winuser/ns-winuser-windowpos) -Struktur, die die neue Größe, Position, Position, Position in der z-Reihenfolge und den Anzeige Zustand des Fensters angibt. Durch Festlegen der Member von **WINDOWPOS** kann eine Anwendung die neue Größe, Position und Darstellung des Fensters beeinflussen.

Nach dem Ändern der Größe, Position, Position und Position eines Fensters in der z-Reihenfolge oder dem Anzeigen des Zustands sendet das System die [**WM- \_ windowposchangsnachricht**](wm-windowposchanged.md) an das Fenster. Diese Meldung enthält einen Zeiger auf [**Windows**](/windows/win32/api/winuser/ns-winuser-windowpos) -Objekte, die das Fenster über seine neue Größe, Position, Position in der z-Reihenfolge und den Anzeige Zustand informieren. Das Festlegen der Member der **WINDOWPOS** -Struktur, die mit **WM \_ windowposchgt** weitergegeben wird, hat keine Auswirkung auf das Fenster. Ein Fenster, in dem die Nachrichten [**WM- \_ Größe**](wm-size.md) und [**WM- \_ Verschiebung**](wm-move.md) verarbeitet werden müssen, muss **WM \_ windowposchangian** die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion übergeben. andernfalls sendet das System keine **WM- \_ Größe** und keine WM-Verschiebungs Meldungen an das Fenster. **\_**

Das System sendet die [**WM- \_ nccalcsize**](wm-nccalcsize.md) -Nachricht an ein Fenster, wenn das Fenster erstellt oder vergrößert wird. Das System verwendet die-Nachricht, um die Größe des Client Bereichs eines Fensters und die Position des Client Bereichs relativ zur linken oberen Ecke des Fensters zu berechnen. Ein Fenster übergibt diese Meldung in der Regel an die Standardfenster Prozedur. Diese Meldung kann jedoch für Anwendungen nützlich sein, die den nicht-Client Bereich eines Fensters anpassen oder Teile des Client Bereichs beibehalten, wenn die Größen des Fensters angepasst sind. Weitere Informationen finden Sie unter [Zeichnen und zeichnen](../gdi/painting-and-drawing.md).

## <a name="window-animation"></a>Fenster Animation

Sie können beim ein-oder Ausblenden von Fenstern besondere Effekte erzeugen, indem Sie die [**animatewindow**](/windows/win32/api/winuser/nf-winuser-animatewindow) -Funktion verwenden. Wenn das Fenster auf diese Weise animiert wird, wird das Fenster abhängig von den Flags, die Sie in einem Aufrufen von **animatewindow** angeben, entweder durch ein-oder ein-oder ausgeblendet.

Standardmäßig verwendet das System die *Roll Animation*. Mit dieser Auswirkung erscheint das Fenster als Rollup (mit dem Fenster) oder als Rollup (Ausblenden des Fensters). Sie können den *dwFlags* -Parameter verwenden, um anzugeben, ob das Fenster horizontal, vertikal oder diagonal ausgeführt wird.

Wenn Sie das **AW- \_ Schiebe** Flag angeben, verwendet das System *Folie Animation*. Mit dieser Auswirkung wird das Fenster angezeigt, um in die Ansicht (Fenster) oder die Folie (Ausblenden des Fensters) zu verschieben. Sie können den *dwFlags* -Parameter verwenden, um anzugeben, ob das Fenster horizontal, vertikal oder diagonal bewegt werden soll.

Wenn Sie das **AW \_ Blend** -Flag angeben, verwendet das System ein *Alpha gemischtes ausblenden*.

Sie können auch das **AW \_ Center** -Flag verwenden, um zu zeigen, dass ein Fenster nach innen oder nach außen reduziert wird.

## <a name="window-layout-and-mirroring"></a>Fenster Layout und-Spiegelung

Das Fenster Layout definiert, wie Text-und Windows Graphics Device Interface-Objekte (GDI) in einem Fenster-oder Gerätekontext (DC) angeordnet werden. Für einige Sprachen, z. b. Englisch, Französisch und Deutsch, ist ein Layout von links nach rechts (LTR) erforderlich. Andere Sprachen, wie z. b. Arabisch und Hebräisch, erfordern das Layout von rechts nach links (RTL). Das Fenster Layout gilt für Text, wirkt sich aber auch auf die anderen GDI-Elemente des Fensters aus, z. b. Bitmaps, Symbole, die Position des Ursprungs, Schaltflächen, kaskadierende Struktur Steuerelemente und ob sich die horizontale Koordinate nach links oder rechts vergrößert. Nachdem eine Anwendung z. b. das RTL-Layout festgelegt hat, wird der Ursprung am rechten Rand des Fensters oder Geräts positioniert, und die Zahl, die die horizontale Koordinate repräsentiert, vergrößert sich, wenn Sie nach links verschieben. Allerdings sind nicht alle Objekte vom Layout eines Fensters betroffen. Beispielsweise müssen das Layout für Dialogfelder, Meldungs Felder und Geräte Kontexte, die keinem Fenster zugeordnet sind, z. b. Metadatendatei-und Drucker-DCS, separat behandelt werden. Einzelheiten hierzu finden Sie weiter unten in diesem Thema.

Die Fenster Funktionen ermöglichen es Ihnen, das Fenster Layout in arabischen und hebräischen Versionen von Windows anzugeben oder zu ändern. Beachten Sie, dass das Ändern in ein RTL-Layout (auch als Spiegelung bezeichnet) nicht für Fenster unterstützt wird, die den Stil [CS \_ owndc](about-window-classes.md) oder für einen DC mit dem erweiterten GM- \_ Grafikmodus aufweisen.

Standardmäßig ist das Fenster Layout von links nach rechts (LTR). Um das Layout des RTL-Fensters festzulegen, nennen Sie " [**kreatewindowex**](/windows/win32/api/winuser/nf-winuser-createwindowexa) " mit dem Format " **WS \_ Ex \_ layoutrtl**". Außerdem hat standardmäßig ein untergeordnetes Fenster (d. h. ein Element, das mit dem untergeordneten [**WS \_**](window-styles.md) -Stil erstellt wurde, und mit einem gültigen übergeordneten *HWND* -Parameter im Aufrufen von " [**kreatewindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) " oder " **kreatewindowex**") dasselbe Layout wie das übergeordnete Fenster Wenn Sie die Vererbung der Spiegelung für alle untergeordneten Fenster deaktivieren möchten, geben Sie im Aufrufen von " **deatewindowex**" **WS \_ Ex \_ nogeerbt Layout** an. Beachten Sie, dass die Spiegelung nicht von eigenen Fenstern geerbt wird (die ohne den untergeordneten **WS \_** -Stil erstellt wurden) oder die mit dem übergeordneten *HWND* -Parameter in " **kreatewindowex** " auf **null** festgelegt wurden. Um die Vererbung der Spiegelung für ein einzelnes Fenster zu deaktivieren, verarbeiten Sie die [**WM \_ nccreate**](wm-nccreate.md) -Nachricht mit " [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga) " und " [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) ", um das **WS \_ Ex \_ layoutrtl** -Flag zu deaktivieren. Diese Verarbeitung wird zusätzlich zu der anderen Verarbeitung benötigt. Das folgende Code Fragment zeigt, wie dies geschieht.


```
SetWindowLong (hWnd, 
               GWL_EXSTYLE, 
               GetWindowLong(hWnd,GWL_EXSTYLE) & ~WS_EX_LAYOUTRTL))
```



Sie können das Standardlayout auf RTL festlegen, indem Sie [**setprocessdefaultlayout**](/windows/win32/api/winuser/nf-winuser-setprocessdefaultlayout)(Layout \_ RTL) aufrufen. Alle Fenster, die nach dem-Befehl erstellt werden, werden gespiegelt, aber vorhandene Fenster sind nicht betroffen. Um die Standard Spiegelung zu deaktivieren, müssen Sie **setprocessdefaultlayout**(0) aufrufen.

Beachten Sie, dass [**setprocessdefaultlayout**](/windows/win32/api/winuser/nf-winuser-setprocessdefaultlayout) die DCS nur von gespiegelten Fenstern widerspiegelt. Um einen beliebigen DC zu spiegeln, nennen Sie [**setLayout**](/windows/win32/api/wingdi/nf-wingdi-setlayout)(hdc, Layout \_ RTL). Weitere Informationen finden Sie in der Erörterung von Spiegelungs Geräte Kontexten, die nicht mit Windows verknüpft sind. Dies wird weiter unten in diesem Thema erläutert.

Bitmaps und Symbole in einem gespiegelten Fenster werden standardmäßig ebenfalls gespiegelt. Allerdings sollten nicht alle davon gespiegelt werden. Beispielsweise sollten solche mit Text, einem Geschäfts Logo oder einer analogen Uhr nicht gespiegelt werden. Um die Spiegelung von Bitmaps zu deaktivieren, müssen Sie [**setLayout**](/windows/win32/api/wingdi/nf-wingdi-setlayout) mit dem \_ in *dwlayout* festgelegten Layout bitmaporientationbeibehaltenen Bit aufrufen. Um die Spiegelung in einem DC zu deaktivieren, müssen Sie **setLayout**(hdc, 0) aufrufen.

Um das aktuelle Standardlayout abzufragen, müssen Sie [**getprocessdefaultlayout**](/windows/win32/api/winuser/nf-winuser-getprocessdefaultlayout)aufrufen. Bei erfolgreicher Rückgabe enthält *pdwdefaultlayout* das Layout \_ RTL oder 0. Um die Layouteinstellungen des Geräte Kontexts abzufragen, müssen Sie [**getLayout**](/windows/win32/api/wingdi/nf-wingdi-getlayout)aufrufen. Bei erfolgreicher Rückgabe gibt **getLayout** ein **DWORD** zurück, das die Layouteinstellungen durch die Einstellungen von Layout \_ RTL und layoutbitmaporientationbeibehaltenen \_ Bits angibt.

Nachdem ein Fenster erstellt wurde, ändern Sie das Layout mithilfe der Funktion [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) . Dies ist beispielsweise erforderlich, wenn der Benutzer die Benutzeroberflächen Sprache eines vorhandenen Fensters von Arabisch oder Hebräisch in Deutsch ändert. Wenn Sie jedoch das Layout eines vorhandenen Fensters ändern, müssen Sie das Fenster für ungültig erklären und aktualisieren, um sicherzustellen, dass die Inhalte des Fensters alle im gleichen Layout gezeichnet werden. Das folgende Codebeispiel zeigt den Beispielcode, der das Fenster Layout nach Bedarf ändert:


```
// Using ANSI versions of GetWindowLong and SetWindowLong because Unicode
// is not needed for these calls

lExStyles = GetWindowLongA(hWnd, GWL_EXSTYLE);

// Check whether new layout is opposite the current layout
if (!!(pLState -> IsRTLLayout) != !!(lExStyles & WS_EX_LAYOUTRTL))
{
    // the following lines will update the window layout

    lExStyles ^= WS_EX_LAYOUTRTL;        // toggle layout
    SetWindowLongA(hWnd, GWL_EXSTYLE, lExStyles);
    InvalidateRect(hWnd, NULL, TRUE);    // to update layout in the client area
}
```



Bei der Spiegelung sollten Sie sich in Bezug auf "Near" und "Far" anstelle von "Left" und "Right" vorstellen. Wenn dies nicht möglich ist, kann dies zu Problemen führen. Eine gängige Codierungs Praxis, die Probleme in einem gespiegelten Fenster verursacht, tritt beim Mapping zwischen Bildschirm Koordinaten und Client Koordinaten auf. Anwendungen verwenden z. b. häufig Code, der dem folgenden ähnelt, um ein Steuerelement in einem Fenster zu positionieren:


```
// DO NOT USE THIS IF APPLICATION MIRRORS THE WINDOW

// get coordinates of the window in screen coordinates
GetWindowRect(hControl, (LPRECT) &rControlRect);  

// map screen coordinates to client coordinates in dialog
ScreenToClient(hDialog, (LPPOINT) &rControlRect.left); 
ScreenToClient(hDialog, (LPPOINT) &rControlRect.right);
```



Dies verursacht Probleme bei der Spiegelung, da der linke Rand des Rechtecks in einem gespiegelten Fenster zum rechten Rand wird und umgekehrt. Um dieses Problem zu vermeiden, ersetzen Sie die [**ScreenToClient**](/windows/win32/api/winuser/nf-winuser-screentoclient) -Aufrufe durch einen Aufruf von [**mapwindowpoints**](/windows/win32/api/winuser/nf-winuser-mapwindowpoints) wie folgt:


```
// USE THIS FOR MIRRORING

GetWindowRect(hControl, (LPRECT) &rControlRect);
MapWindowPoints(NULL, hDialog, (LPPOINT) &rControlRect, 2)
```



Dieser Code funktioniert, weil [**mapwindowpoints**](/windows/win32/api/winuser/nf-winuser-mapwindowpoints) auf Plattformen, die die Spiegelung unterstützen, geändert wird, um die linken und rechten Punkt Koordinaten auszutauschen, wenn das Client Fenster gespiegelt wird. Weitere Informationen finden Sie im Abschnitt "Hinweise" von **mapwindowpoints**.

Ein weiteres gängiges Verfahren, das Probleme in gespiegelten Fenstern verursachen kann, ist die Positionierung von Objekten in einem Client Fenster mithilfe von Offsets in Bildschirm Koordinaten anstelle von Client Koordinaten. Im folgenden Code wird z. b. der Unterschied in Bildschirm Koordinaten als x-Position in Client Koordinaten verwendet, um ein Steuerelement in einem Dialogfeld zu positionieren.


```
// OK if LTR layout and mapping mode of client is MM_TEXT,
// but WRONG for a mirrored dialog 

RECT rdDialog;
RECT rcControl;

HWND hControl = GetDlgItem(hDlg, IDD_CONTROL);
GetWindowRect(hDlg, &rcDialog);             // gets rect in screen coordinates
GetWindowRect(hControl, &rcControl);
MoveWindow(hControl,
           rcControl.left - rcDialog.left,  // uses x position in client coords
           rcControl.top - rcDialog.top,
           nWidth,
           nHeight,
           FALSE);
```



Dieser Code ist in Ordnung, wenn das Dialogfeld das Layout von links nach rechts (LTR) aufweist und der Mapping-Modus des Clients mm- \_ Text ist, da die neue x-Position in Client Koordinaten dem Unterschied in der linken Kante des Steuer Elements und dem Dialogfeld in Bildschirm Koordinaten entspricht. Allerdings werden in einem gespiegelten Dialogfeld Links und rechts umgekehrt, daher sollten Sie [**mapwindowpoints**](/windows/win32/api/winuser/nf-winuser-mapwindowpoints) wie folgt verwenden:


```
RECT rcDialog;
RECT rcControl;

HWND hControl - GetDlgItem(hDlg, IDD_CONTROL);
GetWindowRect(hControl, &rcControl);

// MapWindowPoints works correctly in both mirrored and non-mirrored windows.
MapWindowPoints(NULL, hDlg, (LPPOINT) &rcControl, 2);

// Now rcControl is in client coordinates.
MoveWindow(hControl, rcControl.left, rcControl.top, nWidth, nHeight, FALSE)
```



### <a name="mirroring-dialog-boxes-and-message-boxes"></a>Dialog Felder für Spiegelung und Meldungs Felder

Dialog Felder und Meldungs Felder erben das Layout nicht, sodass Sie das Layout explizit festlegen müssen. Um ein Meldungs Feld zu spiegeln, müssen Sie [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox) oder [**messageboxex**](/windows/win32/api/winuser/nf-winuser-messageboxexa) mit der Option **MB \_ RtlReading** aufrufen. Um ein Dialogfeld von rechts nach Links zu formatieren, verwenden Sie den erweiterten Stil WS \_ Ex \_ layoutrtl in der Dialogfeld Vorlagen Struktur [**dlgtemplateex**](../dlgbox/dlgtemplateex.md). Eigenschaften Blätter sind ein Sonderfall von Dialogfeldern. Jede Registerkarte wird als separates Dialogfeld behandelt, sodass Sie den Typ "WS \_ Ex \_ layoutrtl" auf jeder Registerkarte einschließen müssen, die gespiegelt werden soll.

### <a name="mirroring-device-contexts-not-associated-with-a-window"></a>Spiegelungs Geräte Kontexte, die keinem Fenster zugeordnet sind

DCS, die keinem Fenster zugeordnet sind, z. b. Metadatendateien oder Drucker DCS, erben das Layout nicht, daher müssen Sie das Layout explizit festlegen. Verwenden Sie die [**setLayout**](/windows/win32/api/wingdi/nf-wingdi-setlayout) -Funktion, um das Gerätekontext Layout zu ändern.

Die [**setLayout**](/windows/win32/api/wingdi/nf-wingdi-setlayout) -Funktion wird nur selten mit Windows verwendet. In der Regel empfängt Windows einen zugeordneten DC nur bei der Verarbeitung einer WM-Zeichnungs Nachricht. [**\_**](../gdi/wm-paint.md) Gelegentlich erstellt ein Programm einen DC für ein Fenster durch Aufrufen von [**GetDC**](/windows/win32/api/winuser/nf-winuser-getdc). In jedem Fall wird das anfängliche Layout für den Domänen Controller [](/windows/win32/api/winuser/nf-winuser-beginpaint) gemäß dem WS  \_ Ex layoutrtl-Flag des Fensters durch BeginPaint oder GetDC festgelegt \_ .

Die von [**getwindoworgex**](/windows/win32/api/wingdi/nf-wingdi-getwindoworgex), [**getwindowextex**](/windows/win32/api/wingdi/nf-wingdi-getwindowextex), [**getviewportorgex**](/windows/win32/api/wingdi/nf-wingdi-getviewportorgex) und [**getviewportextex**](/windows/win32/api/wingdi/nf-wingdi-getviewportextex) zurückgegebenen Werte sind durch den Aufruf von [**setLayout**](/windows/win32/api/wingdi/nf-wingdi-setlayout)nicht betroffen.

Wenn das Layout auf RTL fest steht, gibt [**getmapmode**](/windows/win32/api/wingdi/nf-wingdi-getmapmode) \_ anstelle von mm Text mm anisotrope zurück \_ . Der Aufruf von [**setmapmode**](/windows/win32/api/wingdi/nf-wingdi-setmapmode) mit mm- \_ Text funktioniert ordnungsgemäß. nur der Rückgabewert von **getmapmode** ist betroffen. Ebenso bewirkt das Aufrufen von [**setLayout**](/windows/win32/api/wingdi/nf-wingdi-setlayout)(hdc, Layout \_ RTL), wenn der Kartenmodus mm Text ist, \_ den gemeldeten Kartenmodus in mm \_ anisotrope zu ändern.

## <a name="window-destruction"></a>Fenster Zerstörung

Im Allgemeinen muss eine Anwendung alle erstellten Fenster zerstören. Dies erfolgt mithilfe der [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) -Funktion. Wenn ein Fenster zerstört wird, blendet das System das Fenster aus, wenn es sichtbar ist, und entfernt dann alle internen Daten, die dem Fenster zugeordnet sind. Dadurch wird das Fenster Handle ungültig, das von der Anwendung nicht mehr verwendet werden kann.

Eine Anwendung zerstört viele der Fenster, die Sie erstellt, kurz nach ihrer Erstellung. Eine Anwendung zerstört z. b. normalerweise ein Dialogfeld Fenster, sobald die Anwendung über ausreichende Eingaben für den Benutzer verfügt, um die Aufgabe fortzusetzen. Eine Anwendung zerstört letztendlich das Hauptfenster der Anwendung (vor dem Beenden).

Vor dem Zerstören eines Fensters sollte eine Anwendung alle dem Fenster zugeordneten Daten speichern oder entfernen und alle für das Fenster zugewiesenen Systemressourcen freigeben. Wenn die Anwendung die Ressourcen nicht freigibt, gibt das System alle Ressourcen frei, die nicht von der Anwendung freigegeben werden.

Das zerstören eines Fensters wirkt sich nicht auf die Fenster Klasse aus, von der aus das Fenster erstellt wird. Neue Fenster können weiterhin mit dieser Klasse erstellt werden, und alle vorhandenen Fenster dieser Klasse können weiterhin verwendet werden. Durch das zerstören eines Fensters werden auch die Nachfolger Fenster des Fensters zerstört. Die [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) -Funktion sendet zunächst eine [**WM- \_ zerstörungsnachricht**](wm-destroy.md) an das Fenster, dann an die untergeordneten Fenster und die Nachfolger Fenster. Auf diese Weise werden alle nachfolgenden Fenster des Fensters, das zerstört wird, ebenfalls zerstört.

Ein Fenster mit einem Fenstermenü empfängt eine " [**WM \_ Close**](wm-close.md) "-Meldung, wenn der Benutzer auf " **Schließen**" klickt. Durch die Verarbeitung dieser Nachricht kann eine Anwendung den Benutzer zur Bestätigung auffordern, bevor das Fenster zerstört wird. Wenn der Benutzer bestätigt, dass das Fenster zerstört werden soll, kann die Anwendung die [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) -Funktion zum Zerstören des Fensters aufruft.

Wenn das Fenster, das zerstört wird, das aktive Fenster ist, werden die Status "aktiv" und "Fokus" in ein anderes Fenster übertragen. Das Fenster, das zum aktiven Fenster wird, ist das nächste Fenster, das durch die Tastenkombination ALT + ESC bestimmt wird. Das neue aktive Fenster bestimmt dann, welches Fenster den Tastaturfokus erhält.

 

 
