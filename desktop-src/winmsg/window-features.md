---
description: In dieser Übersicht werden Features von Fenstern wie Fenstertypen, Zustände, Größe und Position erläutert.
ms.assetid: 8318c22f-85a2-490e-8233-ee1e234890d9
title: Fensterfeatures
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9437ab95d12ccc56cdf5e87af2127f4c34ad6def7f07f4e79246a2ad591a5ae8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110680"
---
# <a name="window-features"></a>Fensterfeatures

In dieser Übersicht werden Features von Fenstern wie Fenstertypen, Zustände, Größe und Position erläutert.

-   [Fenstertypen](#window-types)
    -   [Überlappende Windows](#overlapped-windows)
    -   [Popup-Windows](#pop-up-windows)
    -   [Untergeordnete Windows](#child-windows)
        -   [Positionierung](#positioning)
        -   [Freistellen](#clipping)
        -   [Beziehung zum übergeordneten Fenster](#relationship-to-parent-window)
        -   [Meldungen](#size-and-position-messages)
    -   [Mehrstufige Windows](#layered-windows)
    -   [Nur-Nachrichten-Windows](#message-only-windows)
-   [Fensterbeziehungen](#window-relationships)
    -   [Vordergrund- und Hintergrund-Windows](#foreground-and-background-windows)
    -   [Eigene Windows](#owned-windows)
    -   [Z-Order](#z-order)
-   [Fenster "Status anzeigen"](#window-show-state)
    -   [Aktives Fenster](#active-window)
    -   [Deaktivierte Windows](#disabled-windows)
    -   [Fenstersichtbarkeit](#window-visibility)
    -   [Minimierte, maximierte und wiederhergestellte Windows](#minimized-maximized-and-restored-windows)
-   [Fenstergröße und -position](#window-size-and-position)
    -   [Standardgröße und -position](#default-size-and-position)
    -   [Nachverfolgungsgröße](#tracking-size)
    -   [Systembefehle](#system-commands)
    -   [Größen- und Positionsfunktionen](#size-and-position-functions)
    -   [Größen- und Positionsmeldungen](#size-and-position-messages)
-   [Fensteranimation](#window-animation)
-   [Fensterlayout und Spiegelung](#window-layout-and-mirroring)
    -   [Spiegelungsdialogfelder und Meldungsfelder](#mirroring-dialog-boxes-and-message-boxes)
    -   [Spiegelung von Gerätekontexten, die keinem Fenster zugeordnet sind](#mirroring-device-contexts-not-associated-with-a-window)
-   [Fensterzerstörungen](#window-destruction)

## <a name="window-types"></a>Fenstertypen

Dieser Abschnitt enthält die folgenden Themen, in denen Fenstertypen beschrieben werden.

-   [Überlappende Windows](#overlapped-windows)
-   [Popup-Windows](#pop-up-windows)
-   [Untergeordnete Windows](#child-windows)
-   [Mehrstufige Windows](#layered-windows)
-   [Nur-Nachrichten-Windows](#message-only-windows)

### <a name="overlapped-windows"></a>Überlappende Windows

Ein *überlappendes Fenster* ist ein Fenster der obersten Ebene (nicht untergeordnetes Fenster), das über eine Titelleiste, einen Rahmen und einen Clientbereich verfügt. sie dient als Hauptfenster einer Anwendung. Sie kann auch über ein Fenstermenü, Schaltflächen zum Minimieren und Maximieren sowie Scrollleisten verfügen. Ein überlappendes Fenster, das als Hauptfenster verwendet wird, umfasst in der Regel alle diese Komponenten.

Durch Angeben des [**WS \_ OVERLAPPED-**](window-styles.md) oder **WS \_ OVERLAPPEDWINDOW-Stils** in der [**CreateWindowEx-Funktion**](/windows/win32/api/winuser/nf-winuser-createwindowexa) erstellt eine Anwendung ein überlappendes Fenster. Wenn Sie den **WS \_ OVERLAPPED-Stil** verwenden, verfügt das Fenster über eine Titelleiste und einen Rahmen. Wenn Sie den **\_ WS-Stil OVERLAPPEDWINDOW** verwenden, verfügt das Fenster über eine Titelleiste, einen Größenrahmen, ein Fenstermenü und Schaltflächen zum Minimieren und Maximieren.

### <a name="pop-up-windows"></a>Popup-Windows

Ein *Popupfenster* ist ein spezieller Typ von überlappenden Fenstern, die für Dialogfelder, Meldungsfelder und andere temporäre Fenster verwendet werden, die außerhalb des Hauptfensters einer Anwendung angezeigt werden. Titelleisten sind für Popupfenster optional. Andernfalls sind Popupfenster identisch mit überlappenden Fenstern des [**WS \_ OVERLAPPED-Stils.**](window-styles.md)

Sie erstellen ein Popupfenster, indem Sie den [**\_ WS-POPUP-Stil**](window-styles.md) in [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa)angeben. Um eine Titelleiste einzublenden, geben Sie den **WS \_ CAPTION-Stil** an. Verwenden Sie das **\_ WS-POPUPWINDOW-Format,** um ein Popupfenster zu erstellen, das über einen Rahmen und ein Fenstermenü verfügt. Der **WS \_ CAPTION-Stil** muss mit dem **\_ WS-POPUPWINDOW-Stil** kombiniert werden, damit das Fenstermenü sichtbar wird.

### <a name="child-windows"></a>Untergeordnete Windows

Ein *untergeordnetes Fenster* weist den [**WS \_ CHILD-Stil**](window-styles.md) auf und ist auf den Clientbereich des übergeordneten Fensters beschränkt. Eine Anwendung verwendet in der Regel untergeordnete Fenster, um den Clientbereich eines übergeordneten Fensters in Funktionsbereiche aufzuteilen. Sie erstellen ein untergeordnetes Fenster, indem Sie den **WS \_ CHILD-Stil** in der [**CreateWindowEx-Funktion**](/windows/win32/api/winuser/nf-winuser-createwindowexa) angeben.

Ein untergeordnetes Fenster muss über ein übergeordnetes Fenster verfügen. Das übergeordnete Fenster kann ein überlappendes Fenster, ein Popupfenster oder sogar ein anderes untergeordnetes Fenster sein. Sie geben das übergeordnete Fenster an, wenn Sie [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa)aufrufen. Wenn Sie den [**WS \_ CHILD-Stil**](window-styles.md) in **CreateWindowEx** angeben, aber kein übergeordnetes Fenster angeben, erstellt das System das Fenster nicht.

Ein untergeordnetes Fenster verfügt über einen Clientbereich, aber keine anderen Features, es sei denn, sie werden explizit angefordert. Eine Anwendung kann eine Titelleiste, ein Fenstermenü, Schaltflächen zum Minimieren und Maximieren, einen Rahmen und Scrollleisten für ein untergeordnetes Fenster anfordern, aber ein untergeordnetes Fenster kann kein Menü haben. Wenn die Anwendung ein Menühandle angibt, wird das Menühandle ignoriert, wenn sie entweder die Fensterklasse des untergeordneten Benutzers registriert oder das untergeordnete Fenster erstellt. Wenn kein Rahmenformat angegeben wird, erstellt das System ein rahmenloses Fenster. Eine Anwendung kann rahmenlose untergeordnete Fenster verwenden, um den Clientbereich eines übergeordneten Fensters zu teilen, während die Bereiche für den Benutzer unsichtbar bleiben.

In diesem Abschnitt werden die folgenden Aspekte von untergeordneten Fenstern erläutert:

-   [Positionierung](#positioning)
-   [Freistellen](#clipping)
-   [Beziehung zum übergeordneten Fenster](#relationship-to-parent-window)
-   [Meldungen](#size-and-position-messages)

#### <a name="positioning"></a>Positionierung

Das System positioniert ein untergeordnetes Fenster immer relativ zur oberen linken Ecke des Clientbereichs des übergeordneten Fensters. Kein Teil eines untergeordneten Fensters wird jemals außerhalb der Rahmen des übergeordneten Fensters angezeigt. Wenn eine Anwendung ein untergeordnetes Fenster erstellt, das größer als das übergeordnete Fenster ist, oder ein untergeordnetes Fenster so positioniert, dass ein Teil oder das gesamte untergeordnete Fenster über die Ränder des übergeordneten Fensters hinausgeht, klammern das System das untergeordnete Fenster. Das heißt, der Teil außerhalb des Clientbereichs des übergeordneten Fensters wird nicht angezeigt. Aktionen, die sich auf das übergeordnete Fenster auswirken, können sich wie folgt auch auf das untergeordnete Fenster auswirken.



| Übergeordnetes Fenster | Untergeordnetes Fenster                                                                                                             |
|---------------|--------------------------------------------------------------------------------------------------------------------------|
| Wird zerstört     | Wird zerstört, bevor das übergeordnete Fenster zerstört wird.                                                                         |
| Ausgeblendet        | Ausgeblendet, bevor das übergeordnete Fenster ausgeblendet wird. Ein untergeordnetes Fenster ist nur sichtbar, wenn das übergeordnete Fenster sichtbar ist.             |
| Verschoben         | Wird mit dem Clientbereich des übergeordneten Fensters verschoben. Das untergeordnete Fenster ist für das Zeichnen des Clientbereichs nach der Verschiebung verantwortlich. |
| Angezeigt         | Wird angezeigt, nachdem das übergeordnete Fenster angezeigt wird.                                                                                  |



 

#### <a name="clipping"></a>Freistellen

Das System schneide nicht automatisch ein untergeordnetes Fenster aus dem Clientbereich des übergeordneten Fensters ab. Dies bedeutet, dass das übergeordnete Fenster über das untergeordnete Fenster zeichnet, wenn es eine Zeichnung an derselben Position wie das untergeordnete Fenster ausführt. Das System schneidet das untergeordnete Fenster jedoch aus dem Clientbereich des übergeordneten Fensters ab, wenn das übergeordnete Fenster den [**WS \_ CLIPCHILDREN-Stil**](window-styles.md) auf hat. Wenn das untergeordnete Fenster abgeschnitten wird, kann das übergeordnete Fenster nicht darüber zeichnen.

Ein untergeordnetes Fenster kann andere untergeordnete Fenster im gleichen Clientbereich überlappen. Ein untergeordnetes Fenster, das das gleiche übergeordnete Fenster wie mindestens ein anderes untergeordnetes Fenster hat, wird als *nebengeordnetes Fenster* bezeichnet. Nebengeordnete Fenster können im Clientbereich des jeweils anderen zeichnen, es sei denn, eines der untergeordneten Fenster weist den [**Stil WS \_ CLIPSIBLINGS auf.**](window-styles.md) Wenn ein untergeordnetes Fenster über diesen Stil verfügt, wird jeder Teil seines gleichgeordneten Fensters, der sich im untergeordneten Fenster befindet, abgeschnitten.

Wenn ein Fenster entweder über den [**Stil WS \_ CLIPCHILDREN**](window-styles.md) oder **WS \_ CLIPSIBLINGS** verfügt, tritt ein geringfügiger Leistungsverlust auf. Jedes Fenster benötigt Systemressourcen, sodass eine Anwendung untergeordnete Fenster nicht willkürlich verwenden sollte. Um eine optimale Leistung zu erzielen, sollte eine Anwendung, die ihr Hauptfenster logisch unterteilen muss, dies in der Fensterprozedur des Hauptfensters anstelle von untergeordneten Fenstern tun.

#### <a name="relationship-to-parent-window"></a>Beziehung zum übergeordneten Fenster

Eine Anwendung kann das übergeordnete Fenster eines vorhandenen untergeordneten Fensters ändern, indem sie die [**SetParent-Funktion**](/windows/win32/api/winuser/nf-winuser-setparent) aufruft. In diesem Fall entfernt das System das untergeordnete Fenster aus dem Clientbereich des alten übergeordneten Fensters und verschiebt es in den Clientbereich des neuen übergeordneten Fensters. Wenn **SetParent ein** **NULL-Handle** angibt, wird das Desktopfenster zum neuen übergeordneten Fenster. In diesem Fall wird das untergeordnete Fenster auf dem Desktop außerhalb der Rahmen eines anderen Fensters gezeichnet. Die [**GetParent-Funktion**](/windows/win32/api/winuser/nf-winuser-getparent) ruft ein Handle für das übergeordnete Fenster eines untergeordneten Fensters ab.

Das übergeordnete Fenster gibt einen Teil seines Clientbereichs an ein untergeordnetes Fenster ab, und das untergeordnete Fenster empfängt alle Eingaben aus diesem Bereich. Die Fensterklasse muss nicht für jedes untergeordnete Fenster des übergeordneten Fensters identisch sein. Dies bedeutet, dass eine Anwendung ein übergeordnetes Fenster mit untergeordneten Fenstern füllen kann, die anders aussehen und verschiedene Aufgaben ausführen. Beispielsweise kann ein Dialogfeld viele Arten von Steuerelementen enthalten, von denen jedes ein untergeordnetes Fenster ist, das verschiedene Datentypen des Benutzers akzeptiert.

Ein untergeordnetes Fenster verfügt nur über ein übergeordnetes Fenster, aber ein übergeordnetes Fenster kann eine beliebige Anzahl von untergeordneten Fenstern haben. Jedes untergeordnete Fenster kann wiederum untergeordnete Fenster haben. In dieser Fensterkette wird jedes untergeordnete Fenster als Nachfolgerfenster des ursprünglichen übergeordneten Fensters bezeichnet. Eine Anwendung verwendet die [**IsChild-Funktion,**](/windows/win32/api/winuser/nf-winuser-ischild) um zu bestimmen, ob ein bestimmtes Fenster ein untergeordnetes Fenster oder ein Nachfolgerfenster eines bestimmten übergeordneten Fensters ist.

Die [**EnumChildWindows-Funktion**](/windows/win32/api/winuser/nf-winuser-enumchildwindows) aufzählt die untergeordneten Fenster eines übergeordneten Fensters. Anschließend übergibt **EnumChildWindows** das Handle an jedes untergeordnete Fenster an eine anwendungsdefinierte Rückruffunktion. Nachfolgerfenster des angegebenen übergeordneten Fensters werden ebenfalls aufzählt.

#### <a name="messages"></a>Meldungen

Das System übergibt die Eingabemeldungen eines untergeordneten Fensters direkt an das untergeordnete Fenster. Die Nachrichten werden nicht über das übergeordnete Fenster übergeben. Die einzige Ausnahme ist, wenn das untergeordnete Fenster von der [**EnableWindow-Funktion deaktiviert**](/windows/win32/api/winuser/nf-winuser-enablewindow) wurde. In diesem Fall übergibt das System alle Eingabemeldungen, die an das untergeordnete Fenster gegangen wären, stattdessen an das übergeordnete Fenster. Dadurch kann das übergeordnete Fenster die Eingabemeldungen untersuchen und das untergeordnete Fenster bei Bedarf aktivieren.

Ein untergeordnetes Fenster kann einen eindeutigen ganzzahligen Bezeichner haben. Untergeordnete Fensterbezeichner sind wichtig, wenn Sie mit Steuerelementfenstern arbeiten. Eine Anwendung leitet die Aktivität eines Steuerelements durch Senden von Nachrichten weiter. Die Anwendung verwendet den untergeordneten Fensterbezeichner des Steuerelements, um die Nachrichten an das Steuerelement weiterleiten. Darüber hinaus sendet ein Steuerelement Benachrichtigungsmeldungen an das übergeordnete Fenster. Eine Benachrichtigungsmeldung enthält den untergeordneten Fensterbezeichner des Steuerelements, mit dem das übergeordnete Element identifiziert, welches Steuerelement die Nachricht gesendet hat. Eine Anwendung gibt den Bezeichner des untergeordneten Fensters für andere Typen von untergeordneten Fenstern an, indem der *hMenu-Parameter* der [**CreateWindowEx-Funktion**](/windows/win32/api/winuser/nf-winuser-createwindowexa) auf einen Wert anstatt auf ein Menühand handle festgelegt wird.

### <a name="layered-windows"></a>Mehrschichtige Windows

Die Verwendung eines mehrschichtigen Fensters kann die Leistung und die visuellen Effekte für ein Fenster erheblich verbessern, das eine komplexe Form aufnimmt, seine Form animiert oder Alphablendingeffekte verwenden möchte. Das System erstellt und erstellt automatisch mehrschichtige Fenster und fenster der zugrunde liegenden Anwendungen neu. Daher werden mehrschichtige Fenster reibungslos gerendert, ohne dass die für komplexe Fensterregionen typischen Flackern entstehen. Darüber hinaus können mehrschichtige Fenster teilweise durchscheinend sein, d. b. alphablendet.

Geben Sie zum Erstellen eines mehrschichtigen Fensters beim Aufrufen der [**CreateWindowEx-Funktion**](/windows/win32/api/winuser/nf-winuser-createwindowexa) den erweiterten **Fensterstil WS EX LAYERED an, oder rufen Sie die \_ \_** [**SetWindowLong-Funktion**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) auf, um **WS \_ EX \_ LAYERED** festzulegen, nachdem das Fenster erstellt wurde. Nach dem **CreateWindowEx-Aufruf** wird das mehrschichtige Fenster erst sichtbar, wenn die [**Funktion SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) oder [**UpdateLayeredWindow**](/windows/win32/api/winuser/nf-winuser-updatelayeredwindow) für dieses Fenster aufgerufen wurde.

> [!Note]  
> Ab Windows 8 kann **WS \_ EX \_ LAYERED** mit untergeordneten Fenstern und Fenstern der obersten Ebene verwendet werden. Frühere Windows unterstützen **WS \_ EX \_ LAYERED nur** für Fenster der obersten Ebene.

 

Rufen Sie [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes)auf, um die Deckkraftebene oder den Transparenzfarbschlüssel für ein bestimmtes mehrschichtiges Fenster fest zu legen. Nach dem Aufruf kann das System das Fenster weiterhin bitten, zu zeichnen, wenn das Fenster angezeigt oder seine Größe geändert wird. Da das System jedoch das Bild eines mehrschichtigen Fensters speichert, wird das Fenster nicht zum Zeichnen auffordern, wenn Teile des Fensters aufgrund von relativen Fensterbewegungen auf dem Desktop angezeigt werden. Ältere Anwendungen müssen ihren Malcode nicht neu strukturieren, wenn sie Fürsichtigkeits- oder Transparenzeffekte für ein Fenster hinzufügen möchten, da das System das Malen von Fenstern, die **SetLayeredWindowAttributes** aufgerufen haben, in den Off-Screen-Arbeitsspeicher umleitet und neu aufsetzt, um den gewünschten Effekt zu erzielen.

Rufen Sie [**UpdateLayeredWindow**](/windows/win32/api/winuser/nf-winuser-updatelayeredwindow)auf, um eine schnellere und effizientere Animation zu erreichen oder wenn ein Alpha pro Pixel erforderlich ist. **UpdateLayeredWindow** sollte in erster Linie verwendet werden, wenn die Anwendung die Form und den Inhalt eines mehrschichtigen Fensters direkt angeben muss, ohne den Umleitungsmechanismus zu verwenden, den das System über [**SetLayeredWindowAttributes bietet.**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) Darüber hinaus wird durch die Direkte Verwendung von **UpdateLayeredWindow** Arbeitsspeicher effizienter genutzt, da das System nicht den zusätzlichen Arbeitsspeicher benötigt, der zum Speichern des Images des umgeleiteten Fensters erforderlich ist. Um maximale Effizienz in animierenden Fenstern zu erzielen, rufen Sie **UpdateLayeredWindow** auf, um die Position und Größe eines mehrschichtigen Fensters zu ändern. Beachten Sie, dass nach dem Aufruf von **SetLayeredWindowAttributes** nachfolgende **UpdateLayeredWindow-Aufrufe** fehlschlagen, bis das Ebenenformatbit wieder löschen und festgelegt wird.

Der Treffertest eines mehrschichtigen Fensters basiert auf der Form und Transparenz des Fensters. Dies bedeutet, dass die Bereiche des Fensters, die farblich oder deren Alphawert 0 (null) ist, die Mausnachrichten durch lassen. Wenn das mehrschichtige Fenster jedoch den erweiterten **Fensterstil WS \_ EX \_ TRANSPARENT** aufnimmt, wird die Form des mehrschichtigen Fensters ignoriert, und die Mausereignisse werden an andere Fenster unterhalb des mehrschichtigen Fensters übergeben.

### <a name="message-only-windows"></a>Message-Only Windows

In *einem nur für Nachrichten bestimmten* Fenster können Sie Nachrichten senden und empfangen. Sie ist nicht sichtbar, hat keine Z-Reihenfolge, kann nicht aufzählt werden und erhält keine Broadcastnachrichten. Das Fenster versendet einfach Nachrichten.

Um ein fenster nur für Nachrichten zu erstellen, geben Sie im *hWndParent-Parameter* der [**CreateWindowEx-Funktion**](/windows/win32/api/winuser/nf-winuser-createwindowexa) die [HWND \_ MESSAGE-Konstante](#message-only-windows) oder ein Handle für ein vorhandenes, nur für Nachrichten geltendes Fenster an. Sie können ein vorhandenes Fenster auch in ein nur für Nachrichten bestimmtes Fenster ändern, indem Sie HWND MESSAGE im \_ *hWndNewParent-Parameter* der [**SetParent-Funktion**](/windows/win32/api/winuser/nf-winuser-setparent) angeben.

Um Nur-Nachrichten-Fenster zu suchen, geben Sie [HWND \_ MESSAGE](#message-only-windows) im *hwndParent-Parameter* der [**FindWindowEx-Funktion**](/windows/win32/api/winuser/nf-winuser-findwindowexa) an. Darüber hinaus durchsucht **FindWindowEx** Nur-Nachrichtenfenster sowie Fenster der obersten Ebene, wenn sowohl der *hwndParent-Parameter* als auch der *hwndChildAfter-Parameter* **NULL sind.**

## <a name="window-relationships"></a>Fensterbeziehungen

Es gibt viele Möglichkeiten, wie ein Fenster mit dem Benutzer oder einem anderen Fenster in Beziehung stehen kann. Ein Fenster kann ein fenstereigenes, Vordergrund- oder Hintergrundfenster sein. Ein Fenster hat auch eine Z-Reihenfolge relativ zu anderen Fenstern. Weitere Informationen finden Sie in den folgenden Themen:

-   [Vordergrund- und Windows](#foreground-and-background-windows)
-   [Eigene Windows](#owned-windows)
-   [Z-Order](#z-order)

### <a name="foreground-and-background-windows"></a>Vordergrund- und Windows

Jeder Prozess kann mehrere Ausführungsthreads haben, und jeder Thread kann Fenster erstellen. Der Thread, der das Fenster erstellt hat, mit dem der Benutzer gerade arbeitet, wird als Vordergrundthread bezeichnet, und das Fenster wird als *Vordergrundfenster bezeichnet.* Alle anderen Threads sind Hintergrundthreads, und die von Hintergrundthreads erstellten Fenster werden als *Hintergrundfenster bezeichnet.*

Jeder Thread verfügt über eine Prioritätsebene, die die CPU-Zeit bestimmt, die der Thread empfängt. Obwohl eine Anwendung die Prioritätsebene ihrer Threads festlegen kann, hat der Vordergrundthread normalerweise eine etwas höhere Prioritätsebene als die Hintergrundthreads. Da er eine höhere Priorität hat, erhält der Vordergrundthread mehr CPU-Zeit als die Hintergrundthreads. Der Vordergrundthread hat eine normale Basispriorität von 9; Ein Hintergrundthread hat eine normale Basispriorität von 7.

Der Benutzer legt das Vordergrundfenster fest, indem er auf ein Fenster klickt oder die Tastenkombination ALT+TAB oder ALT+ESC verwendet. Verwenden Sie die [**GetForegroundWindow-Funktion,**](/windows/win32/api/winuser/nf-winuser-getforegroundwindow) um ein Handle für das Vordergrundfenster abzurufen. Um zu überprüfen, ob ihr Anwendungsfenster das Vordergrundfenster ist, vergleichen Sie das von **GetForegroundWindow zurückgegebene** Handle mit dem ihres Anwendungsfensters.

Eine Anwendung legt das Vordergrundfenster mithilfe der [**SetForegroundWindow-Funktion**](/windows/win32/api/winuser/nf-winuser-setforegroundwindow) fest.

Das System schränkt ein, welche Prozesse das Vordergrundfenster festlegen können. Ein Prozess kann das Vordergrundfenster nur dann festlegen, wenn:

- Alle der folgenden Bedingungen sind erfüllt:
  - Der Prozess, der **SetForegroundWindow** aufruft, gehört zu einer Desktopanwendung, nicht zu einer UWP-App oder einer Windows Store-App, die für Windows 8 oder 8.1 entwickelt wurde.
  - Der Vordergrundprozess hat Aufrufe von **SetForegroundWindow** durch einen vorherigen Aufruf der [**LockSetForegroundWindow-Funktion nicht**](/windows/win32/api/winuser/nf-winuser-locksetforegroundwindow) deaktiviert.
  - Das Time out der Vordergrundsperre ist abgelaufen (siehe [ **SPI_GETFOREGROUNDLOCKTIMEOUT** in **SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa#SPI_GETFOREGROUNDLOCKTIMEOUT)).
  - Es sind keine Menüs aktiv.
- Darüber hinaus gilt mindestens eine der folgenden Bedingungen:
  - Der aufrufende Prozess ist der Vordergrundprozess.
  - Der aufrufende Prozess wurde vom Vordergrundprozess gestartet.
  - Derzeit gibt es kein Vordergrundfenster und somit keinen Vordergrundprozess.
  - Der aufrufende Prozess hat das letzte Eingabeereignis empfangen.
  - Entweder der Vordergrundprozess oder der aufrufende Prozess wird gedebuggt.

Es ist möglich, dass einem Prozess das Recht zum Festlegen des Vordergrundfensters verweigert wird, auch wenn es diese Bedingungen erfüllt.

Ein Prozess, der das Vordergrundfenster festlegen kann, kann es einem anderen Prozess ermöglichen, das Vordergrundfenster durch Aufrufen der [**AllowSetForegroundWindow-Funktion**](/windows/win32/api/winuser/nf-winuser-allowsetforegroundwindow) oder durch Aufrufen der [**BroadcastSystemMessage-Funktion**](/windows/win32/api/winuser/nf-winuser-broadcastsystemmessage) mit dem **BSF \_ ALLOWSFW-Flag** zu setzen. Der Vordergrundprozess kann Aufrufe von [**SetForegroundWindow**](/windows/win32/api/winuser/nf-winuser-setforegroundwindow) deaktivieren, indem die [**LockSetForegroundWindow-Funktion aufruft.**](/windows/win32/api/winuser/nf-winuser-locksetforegroundwindow)

### <a name="owned-windows"></a>Eigene Windows

Ein überlappendes oder Popupfenster kann im Besitz eines anderen überlappenden oder Popupfensters sein. Im Besitz eines Fensters gelten mehrere Einschränkungen.

-   Ein Fenster im Besitz befindet sich in der Z-Reihenfolge immer über seinem Besitzer.
-   Das System zerstört automatisch ein eigenes Fenster, wenn sein Besitzer zerstört wird.
-   Ein eigenes Fenster wird ausgeblendet, wenn sein Besitzer minimiert wird.

Nur ein überlappendes oder Popupfenster kann ein Besitzerfenster sein. Ein untergeordnetes Fenster darf kein Besitzerfenster sein. Eine Anwendung erstellt ein eigenes Fenster, indem das Fensterhandle des Besitzers als *hwndParent-Parameter* von [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) angegeben wird, wenn ein Fenster mit dem [**WS \_ OVERLAPPED-**](window-styles.md) oder **\_ WS-POPUP-Stil** erstellt wird. Der *hwndParent-Parameter* muss ein überlappendes oder Popupfenster identifizieren. Wenn *hwndParent* ein untergeordnetes Fenster identifiziert, weist das System dem übergeordneten Fenster der obersten Ebene des untergeordneten Fensters den Besitz zu. Nach dem Erstellen eines eigenen Fensters kann eine Anwendung den Besitz des Fensters nicht in ein anderes Fenster übertragen.

Dialogfelder und Meldungsfelder befinden sich standardmäßig im Besitz von Fenstern. Eine Anwendung gibt das Besitzerfenster an, wenn eine Funktion aufgerufen wird, die ein Dialogfeld oder Meldungsfeld erstellt.

Eine Anwendung kann die [**GetWindow-Funktion**](/windows/win32/api/winuser/nf-winuser-getwindow) mit dem **GW \_ OWNER-Flag** verwenden, um ein Handle für den Besitzer eines Fensters abzurufen.

### <a name="z-order"></a>Z-Order

Die *Z-Reihenfolge* eines Fensters gibt die Position des Fensters in einem Stapel überlappender Fenster an. Dieser Fensterstapel ist entlang einer imaginären Achse ausgerichtet, der Z-Achse, die sich nach außen vom Bildschirm erstreckt. Das Fenster oben in der Z-Reihenfolge überschneidet sich mit allen anderen Fenstern. Das Fenster am unteren Rand der Z-Reihenfolge wird von allen anderen Fenstern überlappt.

Das System verwaltet die Z-Reihenfolge in einer einzigen Liste. Sie fügt Fenster zur Z-Reihenfolge hinzu, je nach, ob es sich um oberste Fenster, Fenster der obersten Ebene oder untergeordnete Fenster handelt. Ein *oberstes Fenster* überschneidet sich mit allen anderen fensterfremden Fenstern, unabhängig davon, ob es sich um das aktive fenster oder das Vordergrundfenster handelt. Ein oberstes Fenster weist den **Stil WS \_ EX \_ TOPMOST** auf. Alle obersten Fenster werden in der Z-Reihenfolge vor allen nicht obersten Fenstern angezeigt. Ein untergeordnetes Fenster wird mit seinem übergeordneten Fenster in z-Reihenfolge gruppiert.

Wenn eine Anwendung ein Fenster erstellt, legt das System es oben in der Z-Reihenfolge für Fenster desselben Typs ab. Sie können die [**Funktion BringWindowToTop**](/windows/win32/api/winuser/nf-winuser-bringwindowtotop) verwenden, um ein Fenster an den Anfang der Z-Reihenfolge für Fenster desselben Typs zu bringen. Sie können die Z-Reihenfolge mithilfe der Funktionen [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) und [**DeferWindowPos**](/windows/win32/api/winuser/nf-winuser-deferwindowpos) neu anordnen.

Der Benutzer ändert die Z-Reihenfolge, indem er ein anderes Fenster aktiviert. Das System positioniert das aktive Fenster oben in der Z-Reihenfolge für Fenster des gleichen Typs. Wenn ein Fenster oben in der Z-Reihenfolge angezeigt wird, werden auch die untergeordneten Fenster angezeigt. Sie können die [**GetTopWindow-Funktion**](/windows/win32/api/winuser/nf-winuser-gettopwindow) verwenden, um alle untergeordneten Fenster eines übergeordneten Fensters zu durchsuchen und ein Handle an das untergeordnete Fenster zurückzugeben, das in z-Reihenfolge am höchsten ist. Die [**GetNextWindow-Funktion**](/windows/win32/api/winuser/nf-winuser-getnextwindow) ruft ein Handle für das nächste oder vorherige Fenster in z-Reihenfolge ab.

## <a name="window-show-state"></a>Fenster "Status anzeigen"

Zu einem beliebigen Zeitpunkt kann ein Fenster aktiv oder inaktiv sein. ausgeblendet oder sichtbar; und minimiert, maximiert oder wiederhergestellt. Diese Qualitäten werden zusammen als *Fenster mit* dem Status bezeichnet. In den folgenden Themen wird der Status des Fensters erörtert:

-   [Aktives Fenster](#active-window)
-   [Deaktivierte Windows](#disabled-windows)
-   [Fenstersichtbarkeit](#window-visibility)
-   [Minimierte, maximierte und wiederhergestellte Windows](#minimized-maximized-and-restored-windows)

### <a name="active-window"></a>Aktives Fenster

Ein *aktives Fenster* ist das Fenster der obersten Ebene der Anwendung, mit der der Benutzer derzeit arbeitet. Damit der Benutzer das aktive Fenster leicht identifizieren kann, platziert das System es oben in der Z-Reihenfolge und ändert die Farbe der Titelleiste und des Rahmens in die systemdefiniert aktiven Fensterfarben. Nur ein Fenster der obersten Ebene kann ein aktives Fenster sein. Wenn der Benutzer mit einem untergeordneten Fenster arbeitet, aktiviert das System das übergeordnete Fenster der obersten Ebene, das dem untergeordneten Fenster zugeordnet ist.

Es ist jeweils nur ein Fenster der obersten Ebene im System aktiv. Der Benutzer aktiviert ein Fenster der obersten Ebene, indem er darauf klickt (oder auf eines seiner untergeordneten Fenster), oder indem er die Tastenkombination ALT+ESC oder ALT+TAB verwendet. Eine Anwendung aktiviert ein Fenster der obersten Ebene, indem die [**SetActiveWindow-Funktion**](/windows/win32/api/winuser/nf-winuser-setactivewindow) aufgerufen wird. Andere Funktionen können dazu führen, dass das System ein anderes Fenster der obersten Ebene aktiviert, einschließlich [**SetWindowPos,**](/windows/win32/api/winuser/nf-winuser-setwindowpos) [**DeferWindowPos,**](/windows/win32/api/winuser/nf-winuser-deferwindowpos) [**SetWindowPlacement**](/windows/win32/api/winuser/nf-winuser-setwindowplacement)und [**DestroyWindow.**](/windows/win32/api/winuser/nf-winuser-destroywindow) Obwohl eine Anwendung jederzeit ein anderes Fenster der obersten Ebene aktivieren kann, sollte der Benutzer nur als Reaktion auf eine Benutzeraktion verwirrend sein. Eine Anwendung verwendet die [**GetActiveWindow-Funktion,**](/windows/win32/api/winuser/nf-winuser-getactivewindow) um ein Handle für das aktive Fenster abzurufen.

Wenn sich die Aktivierung von einem Fenster der obersten Ebene einer Anwendung in das Fenster der obersten Ebene einer anderen Anwendung ändert, sendet das System eine [**WM \_ ACTIVATEAPP-Nachricht**](wm-activateapp.md) an beide Anwendungen und benachrichtigt sie über die Änderung. Wenn die Aktivierung in ein anderes Fenster der obersten Ebene in derselben Anwendung geändert wird, sendet das System für beide Fenster eine [**WM \_ ACTIVATE-Meldung.**](../inputdev/wm-activate.md)

### <a name="disabled-windows"></a>Deaktivierte Windows

Ein Fenster kann deaktiviert werden. Ein *deaktiviertes Fenster* empfängt keine Tastatur- oder Mauseingabe vom Benutzer, kann aber Nachrichten von anderen Fenstern, von anderen Anwendungen und vom System empfangen. Eine Anwendung deaktiviert in der Regel ein Fenster, um zu verhindern, dass der Benutzer das Fenster verwendet. Beispielsweise kann eine Anwendung eine Pushschaltfläche in einem Dialogfeld deaktivieren, um zu verhindern, dass der Benutzer sie auswählt. Eine Anwendung kann jederzeit ein deaktiviertes Fenster aktivieren. Durch das Aktivieren eines Fensters wird die normale Eingabe wiederhergestellt.

Standardmäßig ist ein Fenster aktiviert, wenn es erstellt wird. Eine Anwendung kann jedoch den [**WS \_ DISABLED-Stil**](window-styles.md) angeben, um ein neues Fenster zu deaktivieren. Eine Anwendung aktiviert oder deaktiviert ein vorhandenes Fenster mithilfe der [**EnableWindow-Funktion.**](/windows/win32/api/winuser/nf-winuser-enablewindow) Das System sendet eine [**WM \_ ENABLE-Nachricht**](wm-enable.md) an ein Fenster, wenn sich der aktivierte Zustand ändert. Eine Anwendung kann mithilfe der [**IsWindowEnabled-Funktion**](/windows/win32/api/winuser/nf-winuser-iswindowenabled) bestimmen, ob ein Fenster aktiviert ist.

Wenn ein untergeordnetes Fenster deaktiviert ist, übergibt das System die Mauseingabemeldungen des untergeordneten Elements an das übergeordnete Fenster. Das übergeordnete Element verwendet die Meldungen, um zu bestimmen, ob das untergeordnete Fenster aktiviert werden soll. Weitere Informationen finden Sie unter [Mauseingabe.](../inputdev/mouse-input.md)

Nur jeweils ein Fenster kann Tastatureingaben empfangen. Dieses Fenster soll den Tastaturfokus haben. Wenn eine Anwendung die [**EnableWindow-Funktion**](/windows/win32/api/winuser/nf-winuser-enablewindow) verwendet, um ein Tastaturfokusfenster zu deaktivieren, verliert das Fenster den Tastaturfokus und wird nicht mehr deaktiviert. **EnableWindow** legt dann den Tastaturfokus auf **NULL** fest, was bedeutet, dass kein Fenster den Fokus besitzt. Wenn ein untergeordnetes Fenster oder ein anderes Nachfolgerfenster über den Tastaturfokus verfügt, verliert das Nachfolgerfenster den Fokus, wenn das übergeordnete Fenster deaktiviert ist. Weitere Informationen finden Sie unter [Tastatureingabe.](../inputdev/keyboard-input.md)

### <a name="window-visibility"></a>Fenstersichtbarkeit

Ein Fenster kann sichtbar oder ausgeblendet sein. Das System zeigt ein *sichtbares Fenster* auf dem Bildschirm an. Ein *ausgeblendetes Fenster* wird ausgeblendet, indem es nicht gezeichnet wird. Wenn das Fenster sichtbar ist, kann der Benutzer im Fenster Eingaben vornehmen und sich die Fensterausgabe anzeigen lassen. Ein ausgeblendetes Fenster ist deaktiviert. Ein ausgeblendetes Fenster kann zwar Meldungen vom System oder anderen Fenstern verarbeiten, kann jedoch keine Benutzereingaben verarbeiten oder Ausgaben anzeigen. Eine Anwendung legt den Sichtbarkeitszustand eines Fensters beim Erstellen des Fensters fest. Später kann die Anwendung den Sichtbarkeitszustand ändern.

Ein Fenster wird angezeigt, wenn der [**WS \_ VISIBLE-Stil**](window-styles.md) für das Fenster festgelegt ist. Standardmäßig erstellt die [**CreateWindowEx-Funktion**](/windows/win32/api/winuser/nf-winuser-createwindowexa) ein ausgeblendetes Fenster, es sei denn, die Anwendung gibt den **WS \_ VISIBLE-Stil** an. In der Regel legt eine Anwendung den **WS \_ VISIBLE-Stil** fest, nachdem sie ein Fenster erstellt hat, um Details des Erstellungsprozesses für den Benutzer ausgeblendet zu halten. Beispielsweise kann eine Anwendung ein neues Fenster ausgeblendet lassen, während sie die Darstellung des Fensters anpasst. Wenn der **WS \_ VISIBLE-Stil** in **CreateWindowEx** angegeben ist, sendet das System die [**\_ WM-SHOWWINDOW-Nachricht**](wm-showwindow.md) an das Fenster, nachdem das Fenster erstellt wurde, aber bevor es angezeigt wird.

Eine Anwendung kann mithilfe der [**IsWindowVisible-Funktion**](/windows/win32/api/winuser/nf-winuser-iswindowvisible) bestimmen, ob ein Fenster sichtbar ist. Eine Anwendung kann ein Fenster mithilfe der Funktionen [**ShowWindow,**](/windows/win32/api/winuser/nf-winuser-showwindow) [**SetWindowPos,**](/windows/win32/api/winuser/nf-winuser-setwindowpos) [**DeferWindowPos**](/windows/win32/api/winuser/nf-winuser-deferwindowpos)oder [**SetWindowPlacement**](/windows/win32/api/winuser/nf-winuser-setwindowplacement) oder [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) anzeigen (sichtbar machen) oder ausblenden. Diese Funktionen blenden ein Fenster ein, indem sie den [**WS \_ VISIBLE-Stil**](window-styles.md) für das Fenster festlegen oder entfernen. Außerdem senden sie die [**\_ WM-SHOWWINDOW-Nachricht**](wm-showwindow.md) an das Fenster, bevor sie angezeigt oder ausgeblendet wird.

Wenn ein Besitzerfenster minimiert wird, blendet das System automatisch die zugeordneten eigenen Fenster aus. Wenn ein Besitzerfenster wiederhergestellt wird, zeigt das System entsprechend automatisch die zugehörigen Fenster an. In beiden Fällen sendet das System die [**\_ WM-SHOWWINDOW-Nachricht**](wm-showwindow.md) an die eigenen Fenster, bevor sie ausgeblendet oder angezeigt werden. Gelegentlich muss eine Anwendung die eigenen Fenster ausblenden, ohne den Besitzer minimieren oder ausblenden zu müssen. In diesem Fall verwendet die Anwendung die [**ShowOwnedPopups-Funktion.**](/windows/win32/api/winuser/nf-winuser-showownedpopups) Diese Funktion legt den [**WS \_ VISIBLE-Stil**](window-styles.md) für alle eigenen Fenster fest oder entfernt sie und sendet die **WM \_ SHOWWINDOW-Meldung** an die eigenen Fenster, bevor sie ausgeblendet oder angezeigt werden. Das Ausblenden eines Besitzerfensters hat keine Auswirkungen auf den Sichtbarkeitszustand der eigenen Fenster.

Wenn ein übergeordnetes Fenster sichtbar ist, sind auch die zugehörigen untergeordneten Fenster sichtbar. Wenn das übergeordnete Fenster ausgeblendet ist, werden auch die untergeordneten Fenster ausgeblendet. Das Minimieren des übergeordneten Fensters hat keine Auswirkungen auf den Sichtbarkeitszustand der untergeordneten Fenster. Das heißt, die untergeordneten Fenster werden zusammen mit dem übergeordneten Fenster minimiert, aber der [**WS \_ VISIBLE-Stil**](window-styles.md) wird nicht geändert.

Selbst wenn ein Fenster den [**WS \_ VISIBLE-Stil aufwies,**](window-styles.md) kann der Benutzer das Fenster möglicherweise nicht auf dem Bildschirm sehen. Andere Fenster überlappen es möglicherweise vollständig oder wurden möglicherweise über den Bildschirmrand hinaus verschoben. Außerdem unterliegt ein sichtbares untergeordnetes Fenster den Clippingregeln, die durch seine über- und untergeordnete Beziehung festgelegt werden. Wenn das übergeordnete Fenster des Fensters nicht sichtbar ist, ist es auch nicht sichtbar. Wenn das übergeordnete Fenster über den Rand des Bildschirms hinaus bewegt wird, wird auch das untergeordnete Fenster bewegt, da ein untergeordnetes Fenster relativ zur oberen linken Ecke des übergeordneten Fensters gezeichnet wird. Beispielsweise kann ein Benutzer das übergeordnete Fenster, das das untergeordnete Fenster enthält, weit genug vom Bildschirmrand verschieben, damit der Benutzer das untergeordnete Fenster möglicherweise nicht sehen kann, obwohl das untergeordnete Fenster und das übergeordnete Fenster beide den **WS \_ VISIBLE-Stil** haben.

### <a name="minimized-maximized-and-restored-windows"></a>Minimierte, maximierte und wiederhergestellte Windows

Ein *maximiertes Fenster* ist ein Fenster mit dem [**Stil WS \_ MAXIMIZE.**](window-styles.md) In der Standardeinstellung wird ein maximiertes Fenster so vergrößert, dass es den Bildschirm oder, im Fall eines untergeordneten Fensters, den Clientbereich des übergeordneten Fensters ausfüllt. Obwohl die Größe eines Fensters auf die gleiche Größe wie ein maximiertes Fenster festgelegt werden kann, ist ein maximiertes Fenster etwas anders. Das System verschiebt die Titelleiste des Fensters automatisch an den oberen Bildschirmrand oder an den oberen Bereich des Clientbereichs des übergeordneten Fensters. Außerdem deaktiviert das System den Größenrahmen des Fensters und die Fensterpositionierungsfunktion der Titelleiste (sodass der Benutzer das Fenster nicht durch Ziehen der Titelleiste verschieben kann).

Ein *minimiertes Fenster ist* ein Fenster mit dem Format [**\_ WS-MINIMIERUNG.**](window-styles.md) In der Standardeinstellung wird ein minimiertes Fenster auf die Größe seiner Schaltfläche auf der Taskleiste verkleinert und auf die Taskleiste verschoben. A *restored window* is a window that has been returned to its previous size and position, that is, the size it was before it was minimized or maximized.

Wenn eine Anwendung den [**Stil WS \_ MAXIMIZE**](window-styles.md) oder **WS \_ MINIMIZE** in der [**CreateWindowEx-Funktion**](/windows/win32/api/winuser/nf-winuser-createwindowexa) angibt, wird das Fenster anfänglich maximiert oder minimiert. Nach dem Erstellen eines Fensters kann eine Anwendung die [**CloseWindow-Funktion**](/windows/win32/api/winuser/nf-winuser-closewindow) verwenden, um das Fenster zu minimieren. Die [**ArrangeIconicWindows-Funktion**](/windows/win32/api/winuser/nf-winuser-arrangeiconicwindows) ordnet die Symbole auf dem Desktop oder die minimierten untergeordneten Fenster eines übergeordneten Fensters im übergeordneten Fenster an. Mit [**der OpenIcon-Funktion**](/windows/win32/api/winuser/nf-winuser-openicon) wird ein minimiertes Fenster auf seine vorherige Größe und Position wiederhergestellt.

Die [**ShowWindow-Funktion**](/windows/win32/api/winuser/nf-winuser-showwindow) kann ein Fenster minimieren, maximieren oder wiederherstellen. Sie kann auch die Sichtbarkeits- und Aktivierungszustände des Fensters festlegen. Die [**SetWindowPlacement-Funktion**](/windows/win32/api/winuser/nf-winuser-setwindowplacement) umfasst die gleiche Funktionalität wie **ShowWindow,** kann jedoch die standardmäßigen minimierten, maximierten und wiederhergestellten Positionen des Fensters überschreiben.

Die [**Funktionen IsZoomed**](/windows/win32/api/winuser/nf-winuser-iszoomed) und [**IsIconic**](/windows/win32/api/winuser/nf-winuser-isiconic) bestimmen, ob ein bestimmtes Fenster maximiert bzw. minimiert wird. Die [**GetWindowPlacement-Funktion**](/windows/win32/api/winuser/nf-winuser-getwindowplacement) ruft die minimierten, maximierten und wiederhergestellten Positionen für das Fenster ab und bestimmt auch den Showzustand des Fensters.

Wenn das System einen Befehl empfängt, um ein minimiertes Fenster zu maximieren oder wiederherzustellen, sendet es dem Fenster eine [**WM \_ QUERYOPEN-Meldung.**](wm-queryopen.md) Wenn die Fensterprozedur **FALSE zurückgibt,** ignoriert das System den Befehl maximieren oder wiederherstellen.

Das System legt die Größe und Position eines maximierten Fensters automatisch auf die systemdefinierten Standardwerte für ein maximiertes Fenster fest. Um diese Standardwerte zu überschreiben, kann eine Anwendung entweder die [**SetWindowPlacement-Funktion**](/windows/win32/api/winuser/nf-winuser-setwindowplacement) aufrufen oder die [**WM \_ GETMINMAXINFO-Nachricht**](wm-getminmaxinfo.md) verarbeiten, die von einem Fenster empfangen wird, wenn das System das Fenster maximieren soll. **WM \_ GETMINMAXINFO enthält** einen Zeiger auf eine [**MINMAXINFO-Struktur,**](/windows/win32/api/winuser/ns-winuser-minmaxinfo) die Werte enthält, die das System zum Festlegen der maximierten Größe und Position verwendet. Durch das Ersetzen dieser Werte werden die Standardwerte überschrieben.

## <a name="window-size-and-position"></a>Fenstergröße und -position

Die Größe und Position eines Fensters werden als umrandendes Rechteck ausgedrückt, das in Koordinaten relativ zum Bildschirm oder übergeordneten Fenster angegeben wird. Die Koordinaten eines Fensters der obersten Ebene sind relativ zur oberen linken Ecke des Bildschirms. Die Koordinaten eines untergeordneten Fensters sind relativ zur oberen linken Ecke des übergeordneten Fensters. Eine Anwendung gibt die Anfangsgröße und -position eines Fensters an, wenn es das Fenster erstellt, aber es kann die Größe und Position des Fensters jederzeit ändern. Weitere Informationen finden Sie unter [Gefüllte Formen.](../gdi/filled-shapes.md)

Dieser Abschnitt enthält die folgenden Themen:

-   [Standardgröße und -position](#default-size-and-position)
-   [Nachverfolgungsgröße](#tracking-size)
-   [Systembefehle](#system-commands)
-   [Größen- und Positionsfunktionen](#size-and-position-functions)
-   [Nachrichten zur Größe und Position](#size-and-position-messages)

### <a name="default-size-and-position"></a>Standardgröße und -position

Eine Anwendung kann es dem System ermöglichen, die Anfangsgröße oder Position eines Fensters der obersten Ebene zu berechnen, indem CW \_ USEDEFAULT in [**CreateWindowEx angegeben wird.**](/windows/win32/api/winuser/nf-winuser-createwindowexa) Wenn die Anwendung die Koordinaten des Fensters auf CW USEDEFAULT setzt und keine anderen Fenster der obersten Ebene erstellt hat, legt das System die Position des neuen Fensters relativ zur oberen linken Ecke des Bildschirms fest. Andernfalls wird die Position relativ zur Position des Fensters der obersten Ebene, das die Anwendung zuletzt erstellt hat, \_ fest. Wenn die Breiten- und Höhenparameter auf CW USEDEFAULT festgelegt sind, berechnet das System die Größe \_ des neuen Fensters. Wenn die Anwendung andere Fenster der obersten Ebene erstellt hat, basiert das System die Größe des neuen Fensters auf der Größe des zuletzt erstellten Fensters der obersten Ebene der Anwendung. Wenn CW USEDEFAULT beim Erstellen eines untergeordneten Fensters oder Popupfensters angegeben wird, legt das System die Größe des Fensters auf die standardmäßige \_ Mindestfenstergröße fest.

### <a name="tracking-size"></a>Nachverfolgungsgröße

Das System behält eine minimale und maximale Nachverfolgungsgröße für ein Fenster des [**\_ WS-STILS THICKFRAME**](window-styles.md) bei. Ein Fenster mit diesem Stil verfügt über einen Größenrahmen. Die *minimale Nachverfolgungsgröße* ist die kleinste Fenstergröße, die Sie durch Ziehen des Größenrahmens des Fensters erzeugen können. Entsprechend ist die *maximale Nachverfolgungsgröße* die größte Fenstergröße, die Sie durch Ziehen des Größenrahmens erzeugen können.

Die minimalen und maximalen Nachverfolgungsgrößen eines Fensters werden auf systemdefinierte Standardwerte festgelegt, wenn das Fenster vom System erstellt wird. Eine Anwendung kann die Standardwerte entdecken und überschreiben, indem sie die [**WM \_ GETMINMAXINFO-Nachricht**](wm-getminmaxinfo.md) verarbeitet. Weitere Informationen finden Sie unter [Größe und Position von Nachrichten.](#size-and-position-messages)

### <a name="system-commands"></a>Systembefehle

Eine Anwendung, die über ein Fenstermenü verfügt, kann die Größe und Position dieses Fensters durch Senden von Systembefehlen ändern. Systembefehle werden generiert, wenn der Benutzer Befehle aus dem Fenstermenü auswählt. Eine Anwendung kann die Benutzeraktion emulieren, indem sie eine [**WM \_ SYSCOMMAND-Nachricht**](../menurc/wm-syscommand.md) an das Fenster sendet. Die folgenden Systembefehle wirken sich auf die Größe und Position eines Fensters aus.



| Befehl      | Beschreibung                                                                                                                                                          |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SC \_ CLOSE    | Schließt das Fenster. Dieser Befehl sendet eine [**WM \_ CLOSE-Nachricht**](wm-close.md) an das Fenster. Das Fenster führt alle erforderlichen Schritte aus, um sich selbst zu bereinigt und zu zerstören. |
| SC \_ MAXIMIZE | Maximiert das Fenster.                                                                                                                                                |
| SC \_ MINIMIZE | Minimiert das Fenster.                                                                                                                                                |
| SC \_ MOVE     | Verschiebt das Fenster.                                                                                                                                                    |
| SC \_ RESTORE  | Stellt ein minimiertes oder maximiertes Fenster auf seine vorherige Größe und Position wieder zurück.                                                                                          |
| SC \_ SIZE     | Startet einen Size-Befehl. Um die Größe des Fensters zu ändern, verwenden Sie die Maus oder Tastatur.                                                                                  |



 

### <a name="size-and-position-functions"></a>Größen- und Positionsfunktionen

Nach dem Erstellen eines Fensters kann eine Anwendung die Größe oder Position des Fensters festlegen, indem eine von mehreren verschiedenen Funktionen wie [**SetWindowPlacement,**](/windows/win32/api/winuser/nf-winuser-setwindowplacement) [**MoveWindow,**](/windows/win32/api/winuser/nf-winuser-movewindow) [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos)und [**DeferWindowPos aufruft.**](/windows/win32/api/winuser/nf-winuser-deferwindowpos) **SetWindowPlacement** legt die minimierte Position eines Fensters, die maximierte Position, die wiederhergestellte Größe und Position sowie den Status fest. Die **Funktionen MoveWindow** und **SetWindowPos** sind ähnlich. legen sowohl die Größe als auch die Position eines einzelnen Anwendungsfensters fest. Die **SetWindowPos-Funktion** enthält eine Reihe von Flags, die sich auf den Showzustand des Fensters auswirken. **MoveWindow** enthält diese Flags nicht. Verwenden Sie die [**Funktionen BeginDeferWindowPos,**](/windows/win32/api/winuser/nf-winuser-begindeferwindowpos) **DeferWindowPos** und [**EndDeferWindowPos,**](/windows/win32/api/winuser/nf-winuser-enddeferwindowpos) um gleichzeitig die Position einer Reihe von Fenstern, einschließlich Größe, Position, Position in der Z-Reihenfolge und Anzeigen des Zustands, fest.

Eine Anwendung kann die Koordinaten des umgebundenen Rechtecks eines Fensters mithilfe der [**GetWindowRect-Funktion**](/windows/win32/api/winuser/nf-winuser-getwindowrect) abrufen. **GetWindowRect** füllt eine [**RECT-Struktur**](/previous-versions//dd162897(v=vs.85)) mit den Koordinaten der oberen linken und unteren rechten Ecken des Fensters. Die Koordinaten sind relativ zur oberen linken Ecke des Bildschirms, auch für ein untergeordnetes Fenster. Die [**ScreenToClient-**](/windows/win32/api/winuser/nf-winuser-screentoclient) oder [**MapWindowPoints-Funktion**](/windows/win32/api/winuser/nf-winuser-mapwindowpoints) ordnet die Bildschirmkoordinaten des umrandenden Rechtecks eines untergeordneten Fensters Koordinaten relativ zum Clientbereich des übergeordneten Fensters zu.

Die [**GetClientRect-Funktion**](/windows/win32/api/winuser/nf-winuser-getclientrect) ruft die Koordinaten des Clientbereichs eines Fensters ab. **GetClientRect** füllt eine [**RECT-Struktur**](/previous-versions//dd162897(v=vs.85)) mit den Koordinaten der oberen linken und unteren rechten Ecke des Clientbereichs auf, aber die Koordinaten sind relativ zum Clientbereich selbst. Dies bedeutet, dass die Koordinaten der oberen linken Ecke eines Clientbereichs immer (0,0) und die Koordinaten der unteren rechten Ecke die Breite und Höhe des Clientbereichs sind.

Die [**CascadeWindows-Funktion**](/windows/win32/api/winuser/nf-winuser-cascadewindows) kaskadiert die Fenster auf dem Desktop oder kaskadiert die untergeordneten Fenster des angegebenen übergeordneten Fensters. Die [**TileWindows-Funktion**](/windows/win32/api/winuser/nf-winuser-tilewindows) kachelt die Fenster auf dem Desktop oder die untergeordneten Fenster des angegebenen übergeordneten Fensters.

### <a name="size-and-position-messages"></a>Nachrichten zur Größe und Position

Das System sendet die [**WM \_ GETMINMAXINFO-Nachricht**](wm-getminmaxinfo.md) an ein Fenster, dessen Größe oder Position sich ändern wird. Die Meldung wird beispielsweise gesendet, wenn  der  Benutzer im Fenstermenü auf Verschieben oder Größe klickt oder auf den Größenrahmen oder die Titelleiste klickt. Die Nachricht wird auch gesendet, wenn eine Anwendung [**SetWindowPos aufruft,**](/windows/win32/api/winuser/nf-winuser-setwindowpos) um das Fenster zu verschieben oder zu schatten. **WM \_ GETMINMAXINFO** enthält einen Zeiger auf eine [**MINMAXINFO-Struktur,**](/windows/win32/api/winuser/ns-winuser-minmaxinfo) die die standardmäßige maximierte Größe und Position für das Fenster sowie die Standardmäßige minimale und maximale Nachverfolgungsgröße enthält. Eine Anwendung kann die Standardwerte überschreiben, indem **SIE WM \_ GETMINMAXINFO verarbeitet** und die entsprechenden Member von **MINMAXINFO festlegen.** Ein Fenster muss den [**Stil WS \_ THICKFRAME**](window-styles.md) oder **WS \_ CAPTION** haben, um **WM \_ GETMINMAXINFO zu empfangen.** Ein Fenster mit **dem Format WS \_ THICKFRAME** empfängt diese Meldung während des Fenstererstellungsprozesses sowie beim Ändern oder Ändern der Größe.

Das System sendet die [**WM \_ WINDOWPOSCHANGING-Nachricht**](wm-windowposchanging.md) an ein Fenster, dessen Größe, Position, Position in Z-Reihenfolge oder Show-Zustand sich ändern wird. Diese Meldung enthält einen Zeiger auf eine [**WINDOWPOS-Struktur,**](/windows/win32/api/winuser/ns-winuser-windowpos) die die neue Größe, Position, Position in der Z-Reihenfolge und den Showzustand des Fensters angibt. Durch Festlegen der Member von **WINDOWPOS** kann eine Anwendung die neue Größe, Position und Darstellung des Fensters beeinflussen.

Nach dem Ändern der Größe, Position, Position eines Fensters in der Z-Reihenfolge oder nach dem Anzeigen des Zustands sendet das System die [**WM \_ WINDOWPOSCHANGED-Nachricht**](wm-windowposchanged.md) an das Fenster. Diese Meldung enthält einen Zeiger auf [**WINDOWPOS,**](/windows/win32/api/winuser/ns-winuser-windowpos) der das Fenster über seine neue Größe, Position, Position in der Z-Reihenfolge und den angezeigten Zustand informiert. Das Festlegen der Member der **WINDOWPOS-Struktur,** die mit **WM \_ WINDOWPOSCHANGED** übergeben wird, hat keine Auswirkungen auf das Fenster. Ein Fenster, das WM SIZE- und [**WM \_ MOVE-Nachrichten**](wm-move.md) verarbeiten muss, muss **WM \_ WINDOWPOSCHANGED** an die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) übergeben. Andernfalls sendet das System keine **WM \_ SIZE-** und **WM \_ MOVE-Nachrichten** an das Fenster. [**\_**](wm-size.md)

Das System sendet die [**WM \_ NCCALCSIZE-Nachricht**](wm-nccalcsize.md) an ein Fenster, wenn das Fenster erstellt oder dimensioniert wird. Das System verwendet die Meldung, um die Größe des Clientbereichs eines Fensters und die Position des Clientbereichs relativ zur oberen linken Ecke des Fensters zu berechnen. Ein Fenster übergibt diese Meldung in der Regel an die Standardfensterprozedur. Diese Meldung kann jedoch in Anwendungen nützlich sein, die den Nicht-Clientbereich eines Fensters anpassen oder Teile des Clientbereichs beibehalten, wenn die Größe des Fensters festgelegt ist. Weitere Informationen finden Sie unter [Zeichnen und Zeichnen](../gdi/painting-and-drawing.md)von .

## <a name="window-animation"></a>Fensteranimation

Sie können Sondereffekte erzeugen, wenn Sie Fenster mithilfe der [**Funktion "AnimateWindow"**](/windows/win32/api/winuser/nf-winuser-animatewindow) anzeigen oder ausblenden. Wenn das Fenster auf diese Weise animiert wird, wird das Fenster entweder gerollt, geschiebet oder ausgeblendet. Dies hängt von den Flags ab, die Sie in einem Aufruf von **AnimateWindow angeben.**

Standardmäßig verwendet das System die *Rollanimation*. Mit diesem Effekt wird das Fenster geöffnet (mit dem Fenster) oder geschlossen (ausblenden des Fensters). Sie können den *dwFlags-Parameter* verwenden, um anzugeben, ob das Fenster horizontal, vertikal oder diagonal gerollt wird.

Wenn Sie das **AW \_ SLIDE-Flag** angeben, verwendet das System *die Schiebeanimation*. Mit diesem Effekt scheint das Fenster in die Ansicht zu schieben (mit dem Fenster) oder aus der Ansicht zu schieben (das Fenster wird verborgen). Sie können den *dwFlags-Parameter* verwenden, um anzugeben, ob das Fenster horizontal, vertikal oder diagonal geschiebet wird.

Wenn Sie das **AW \_ BLEND-Flag** angeben, verwendet das System ein *alphablended fade*.

Sie können auch das **AW \_ CENTER-Flag** verwenden, um ein Fenster nach innen zu reduzieren oder nach außen zu erweitern.

## <a name="window-layout-and-mirroring"></a>Fensterlayout und -spiegelung

Das Fensterlayout definiert, wie Text- Windows Graphics Device Interface (GDI)-Objekte in einem Fenster oder Gerätekontext (DC) dargestellt werden. Einige Sprachen, z. B. Englisch, Französisch und Deutsch, erfordern ein Layout von links nach rechts (LTR). Andere Sprachen, z. B. Arabisch und Hebräisch, erfordern ein Layout von rechts nach links (RTL). Das Fensterlayout gilt für Text, wirkt sich aber auch auf die anderen GDI-Elemente des Fensters aus, einschließlich Bitmaps, Symbolen, der Position des Ursprungs, Schaltflächen, kaskadierenden Struktursteuerelementen und ob die horizontale Koordinate zunimmt, wenn Sie nach links oder rechts wechseln. Nachdem eine Anwendung beispielsweise das RTL-Layout festgelegt hat, wird der Ursprung am rechten Rand des Fensters oder Geräts positioniert, und die Zahl, die die horizontale Koordinate darstellt, erhöht sich, wenn Sie nach links wechseln. Allerdings sind nicht alle Objekte vom Layout eines Fensters betroffen. Beispielsweise muss das Layout für Dialogfelder, Meldungsfelder und Gerätekontexte, die nicht einem Fenster zugeordnet sind( z. B. Metadatei und Drucker-DCs), separat behandelt werden. Weitere Informationen hierzu finden Sie weiter oben in diesem Thema.

Mit den Fensterfunktionen können Sie das Fensterlayout in arabischen und hebräischen Versionen von Windows. Beachten Sie, dass das Ändern in ein RTL-Layout (auch als Spiegelung bezeichnet) nicht für Fenster mit dem Stil [CS \_ OWNDC](about-window-classes.md) oder für einen DC mit dem GM \_ ADVANCED-Grafikmodus unterstützt wird.

Standardmäßig ist das Fensterlayout von links nach rechts (LTR). Rufen Sie [**createWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) im Format WS EX LAYOUTRTL auf, um das Layout des **\_ \_ RTL-Fensters zu festlegen.** Standardmäßig hat ein untergeordnetes Fenster (d. h. ein Fenster, das mit dem [**WS \_ CHILD-Stil**](window-styles.md) und mit einem gültigen übergeordneten *hWnd-Parameter* im Aufruf von [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) oder **CreateWindowEx** erstellt wurde) das gleiche Layout wie das übergeordnete Fenster. Um die Vererbung der Spiegelung für alle untergeordneten Fenster zu deaktivieren, geben **Sie WS \_ EX \_ NOINHERITLAYOUT** im Aufruf von **CreateWindowEx an.** Beachten Sie, dass die Spiegelung nicht von eigenen Fenstern (die ohne **den WS \_ CHILD-Stil** erstellt wurden) oder von Fenstern geerbt wird, die mit dem übergeordneten *hWnd-Parameter* in **CreateWindowEx** auf **NULL festgelegt sind.** Um die Vererbung der Spiegelung für ein einzelnes Fenster zu deaktivieren, verarbeiten Sie die [**WM \_ NCCREATE-Nachricht**](wm-nccreate.md) mit [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga) und [**SetWindowLong,**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) um das **WS \_ EX \_ LAYOUTRTL-Flag zu** deaktivieren. Diese Verarbeitung wird zusätzlich zu jeder anderen Verarbeitung benötigt. Das folgende Codefragment zeigt, wie dies erfolgt.


```
SetWindowLong (hWnd, 
               GWL_EXSTYLE, 
               GetWindowLong(hWnd,GWL_EXSTYLE) & ~WS_EX_LAYOUTRTL))
```



Sie können das Standardlayout auf RTL festlegen, indem Sie [**SetProcessDefaultLayout**](/windows/win32/api/winuser/nf-winuser-setprocessdefaultlayout)(LAYOUT \_ RTL) aufrufen. Alle Fenster, die nach dem Aufruf erstellt werden, werden gespiegelt, vorhandene Fenster sind jedoch nicht betroffen. Rufen Sie **SetProcessDefaultLayout**(0) auf, um die Standardspiegelung zu deaktivieren.

Beachten Sie, [**dass SetProcessDefaultLayout**](/windows/win32/api/winuser/nf-winuser-setprocessdefaultlayout) nur die DCs gespiegelter Fenster spiegelt. Rufen Sie [**SetLayout**](/windows/win32/api/wingdi/nf-wingdi-setlayout)(hdc, LAYOUT RTL) auf, um einen beliebigen DC \_ zu spiegeln. Weitere Informationen finden Sie in der Diskussion zur Spiegelung von Gerätekontexten, die nicht mit Fenstern verknüpft sind. Dies wird weiter unten in diesem Thema beschrieben.

Bitmaps und Symbole in einem gespiegelten Fenster werden ebenfalls standardmäßig gespiegelt. Allerdings sollten nicht alle gespiegelt werden. Beispielsweise sollten Solche mit Text, einem Geschäftslogo oder einer analogen Uhr nicht gespiegelt werden. Um die Spiegelung von Bitmaps zu deaktivieren, rufen Sie [**SetLayout**](/windows/win32/api/wingdi/nf-wingdi-setlayout) mit dem in \_ dwLayout festgelegten LAYOUT BITMAPORIENTATIONPRESERVED-Bit *auf.* Um die Spiegelung in einem DC zu deaktivieren, rufen **Sie SetLayout**(hdc, 0) auf.

Rufen Sie zum Abfragen des aktuellen Standardlayouts [**GetProcessDefaultLayout auf.**](/windows/win32/api/winuser/nf-winuser-getprocessdefaultlayout) Nach einer erfolgreichen Rückgabe enthält *pdwDefaultLayout* LAYOUT \_ RTL oder 0. Rufen Sie GetLayout auf, um die Layouteinstellungen des [**Gerätekontexts abfragt.**](/windows/win32/api/wingdi/nf-wingdi-getlayout) Nach einer erfolgreichen Rückgabe gibt **GetLayout** ein **DWORD** zurück, das die Layouteinstellungen durch die Einstellungen des LAYOUT RTL- und LAYOUT \_ \_ BITMAPORIENTATIONPRESERVED-Bits angibt.

Nachdem ein Fenster erstellt wurde, ändern Sie das Layout mithilfe der [**SetWindowLong-Funktion.**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) Dies ist beispielsweise erforderlich, wenn der Benutzer die Benutzeroberflächensprache eines vorhandenen Fensters von Arabisch oder Hebräisch in Deutsch ändert. Wenn Sie jedoch das Layout eines vorhandenen Fensters ändern, müssen Sie das Fenster für ungültig erklären und aktualisieren, um sicherzustellen, dass der Inhalt des Fensters alle im gleichen Layout gezeichnet wird. Das folgende Codebeispiel ist ein Beispielcode, der das Fensterlayout nach Bedarf ändert:


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



Bei der Spiegelung sollten Sie "near" und "far" anstelle von "left" und "right" verwenden. Wenn dies nicht der Fehler ist, kann dies zu Problemen führen. Eine gängige Codierungsübung, die Probleme in einem gespiegelten Fenster verursacht, tritt bei der Zuordnung zwischen Bildschirmkoordinaten und Clientkoordinaten auf. Beispielsweise verwenden Anwendungen häufig Code wie den folgenden, um ein Steuerelement in einem Fenster zu positionieren:


```
// DO NOT USE THIS IF APPLICATION MIRRORS THE WINDOW

// get coordinates of the window in screen coordinates
GetWindowRect(hControl, (LPRECT) &rControlRect);  

// map screen coordinates to client coordinates in dialog
ScreenToClient(hDialog, (LPPOINT) &rControlRect.left); 
ScreenToClient(hDialog, (LPPOINT) &rControlRect.right);
```



Dies verursacht Probleme bei der Spiegelung, da der linke Rand des Rechtecks zum rechten Rand in einem gespiegelten Fenster wird und umgekehrt. Um dieses Problem zu vermeiden, ersetzen Sie [**die ScreenToClient-Aufrufe**](/windows/win32/api/winuser/nf-winuser-screentoclient) wie folgt durch einen Aufruf von [**MapWindowPoints:**](/windows/win32/api/winuser/nf-winuser-mapwindowpoints)


```
// USE THIS FOR MIRRORING

GetWindowRect(hControl, (LPRECT) &rControlRect);
MapWindowPoints(NULL, hDialog, (LPPOINT) &rControlRect, 2)
```



Dieser Code funktioniert, da [**MapWindowPoints**](/windows/win32/api/winuser/nf-winuser-mapwindowpoints) auf Plattformen, die die Spiegelung unterstützen, so geändert wird, dass die koordinaten des linken und rechten Punkts ausgetauscht werden, wenn das Clientfenster gespiegelt wird. Weitere Informationen finden Sie im Abschnitt "Hinweise" von **MapWindowPoints.**

Eine weitere gängige Methode, die probleme in gespiegelten Fenstern verursachen kann, ist die Positionierung von Objekten in einem Clientfenster mitHilfe von Offsets in Bildschirmkoordinaten anstelle von Clientkoordinaten. Der folgende Code verwendet z. B. den Unterschied in den Bildschirmkoordinaten als x-Position in Clientkoordinaten, um ein Steuerelement in einem Dialogfeld zu positionieren.


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



Dieser Code ist in Ordnung, wenn das Dialogfenster über ein LAYOUT von links nach rechts (LTR) verfügt und der Zuordnungsmodus des Clients MM TEXT ist, da die neue x-Position in Clientkoordinaten dem Unterschied in den linken Rändern des Steuerelements und dem Dialog in Bildschirmkoordinaten \_ entspricht. In einem gespiegelten Dialogfeld werden jedoch links und rechts umgekehrt, daher sollten Sie [**stattdessen MapWindowPoints**](/windows/win32/api/winuser/nf-winuser-mapwindowpoints) wie folgt verwenden:


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



### <a name="mirroring-dialog-boxes-and-message-boxes"></a>Spiegelungsdialogfelder und Meldungsfelder

Dialogfelder und Meldungsfelder erben kein Layout, daher müssen Sie das Layout explizit festlegen. Um ein Meldungsfeld zu spiegeln, rufen [**Sie MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox) oder [**MessageBoxEx mit**](/windows/win32/api/winuser/nf-winuser-messageboxexa) der **Option MB \_ RTLREADING** auf. Verwenden Sie zum Layout eines Dialogfelds von rechts nach links den erweiterten Stil WS \_ EX LAYOUTRTL in der Dialogvorlagenstruktur \_ [**DLGTEMPLATEEX**](../dlgbox/dlgtemplateex.md). Eigenschaftenblätter sind ein Sonderfall von Dialogfeldern. Jede Registerkarte wird als separates Dialogfeld behandelt, daher müssen Sie den WS EX LAYOUTRTL-Stil in jede Registerkarte einfügen, \_ \_ die gespiegelt werden soll.

### <a name="mirroring-device-contexts-not-associated-with-a-window"></a>Spiegelung von Gerätekontexten, die einem Fenster nicht zugeordnet sind

DCs, die nicht einem Fenster zugeordnet sind, z. B. Metadatei- oder Drucker-Dcs, erben kein Layout, daher müssen Sie das Layout explizit festlegen. Verwenden Sie die SetLayout-Funktion, um das [**Gerätekontextlayout zu**](/windows/win32/api/wingdi/nf-wingdi-setlayout) ändern.

Die [**SetLayout-Funktion**](/windows/win32/api/wingdi/nf-wingdi-setlayout) wird selten mit Fenstern verwendet. In der Regel empfangen Fenster einen zugeordneten DC nur bei der Verarbeitung einer [**WM \_ PAINT-Nachricht.**](../gdi/wm-paint.md) Gelegentlich erstellt ein Programm einen DC für ein Fenster durch Aufrufen von [**GetDC**](/windows/win32/api/winuser/nf-winuser-getdc). In beiden Richtungen wird das anfängliche Layout für den DC durch [**BeginPaint**](/windows/win32/api/winuser/nf-winuser-beginpaint) oder **GetDC** gemäß dem WS \_ EX \_ LAYOUTRTL-Flag des Fensters festgelegt.

Die von [**GetWindowOrgEx,**](/windows/win32/api/wingdi/nf-wingdi-getwindoworgex) [**GetWindowExtEx,**](/windows/win32/api/wingdi/nf-wingdi-getwindowextex) [**GetViewportOrgEx**](/windows/win32/api/wingdi/nf-wingdi-getviewportorgex) und [**GetViewportExtEx**](/windows/win32/api/wingdi/nf-wingdi-getviewportextex) zurückgegebenen Werte sind durch den Aufruf von SetLayout nicht [**betroffen.**](/windows/win32/api/wingdi/nf-wingdi-setlayout)

Wenn das Layout RTL ist, [**gibt GetMapMode**](/windows/win32/api/wingdi/nf-wingdi-getmapmode) MM \_ ANISOTROPIC anstelle von MM \_ TEXT zurück. Das [**Aufrufen von SetMapMode**](/windows/win32/api/wingdi/nf-wingdi-setmapmode) mit MM \_ TEXT funktioniert ordnungsgemäß. Nur der Rückgabewert von **GetMapMode** ist betroffen. Entsprechend bewirkt der Aufruf von [**SetLayout**](/windows/win32/api/wingdi/nf-wingdi-setlayout)(hdc, LAYOUT RTL), wenn der Zuordnungsmodus MM TEXT ist, dass der gemeldete Zuordnungsmodus in \_ MM \_ \_ ANISOTROPIC geändert wird.

## <a name="window-destruction"></a>Fenstervernichtung

Im Allgemeinen muss eine Anwendung alle von ihr erstellten Fenster zerstören. Dazu wird die [**DestroyWindow-Funktion**](/windows/win32/api/winuser/nf-winuser-destroywindow) verwendet. Wenn ein Fenster zerstört wird, blendet das System das Fenster aus, sofern es sichtbar ist, und entfernt dann alle internen Daten, die dem Fenster zugeordnet sind. Dadurch wird das Fensterhand handle ungültig, das von der Anwendung nicht mehr verwendet werden kann.

Eine Anwendung zerstört viele der Fenster, die sie kurz nach der Erstellung erstellt. Beispielsweise zerstört eine Anwendung in der Regel ein Dialogfeldfenster, sobald die Anwendung über ausreichende Eingaben vom Benutzer verfügt, um die Aufgabe fortsetzen zu können. Eine Anwendung zerstört schließlich das Hauptfenster der Anwendung (vor dem Beenden).

Vor dem Zerstören eines Fensters sollte eine Anwendung alle daten, die dem Fenster zugeordnet sind, speichern oder entfernen und alle systemressourcen, die dem Fenster zugeordnet sind, frei geben. Wenn die Anwendung die Ressourcen nicht frei gibt, gibt das System alle Ressourcen frei, die nicht von der Anwendung frei werden.

Das Zerstören eines Fensters wirkt sich nicht auf die Fensterklasse aus, aus der das Fenster erstellt wird. Neue Fenster können weiterhin mit dieser Klasse erstellt werden, und alle vorhandenen Fenster dieser Klasse funktionieren weiterhin. Durch das Zerstören eines Fensters werden auch die nachfolgenden Fenster des Fensters zerstört. Die [**DestroyWindow-Funktion**](/windows/win32/api/winuser/nf-winuser-destroywindow) sendet zuerst eine [**WM \_ DESTROY-Nachricht**](wm-destroy.md) an das Fenster und dann an die untergeordneten Fenster und nachfolgern Fenster. Auf diese Weise werden auch alle nachfolgenden Fenster des zu zerstörenden Fensters zerstört.

Ein Fenster mit einem Fenstermenü empfängt eine [**WM \_ CLOSE-Meldung,**](wm-close.md) wenn der Benutzer auf **Schließen klickt.** Durch die Verarbeitung dieser Nachricht kann eine Anwendung den Benutzer zur Bestätigung auffordern, bevor das Fenster zerstört wird. Wenn der Benutzer bestätigt, dass das Fenster zerstört werden soll, kann die Anwendung die [**DestroyWindow-Funktion**](/windows/win32/api/winuser/nf-winuser-destroywindow) aufrufen, um das Fenster zu zerstören.

Wenn das zu zerstörende Fenster das aktive Fenster ist, werden sowohl der aktive als auch der Fokuszustände in ein anderes Fenster übertragen. Das Fenster, das zum aktiven Fenster wird, ist das nächste Fenster, wie durch die Tastenkombination ALT+ESC festgelegt. Das neue aktive Fenster bestimmt dann, welches Fenster den Tastaturfokus erhält.

 

 
