---
title: Info-Steuerelemente
description: Quick Infos werden automatisch angezeigt, oder es wird ein Popup angezeigt, wenn der Benutzer den Mauszeiger über einem Tool oder einem anderen Benutzeroberflächen Element hält.
ms.assetid: 1020cec7-57b4-4463-9419-f80fd14fa12c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9c1042523c86e794865da5d38fb023ee37d60b4
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104039687"
---
# <a name="about-tooltip-controls"></a>Info-Steuerelemente

Quick Infos werden automatisch angezeigt, oder es wird ein Popup angezeigt, wenn der Benutzer den Mauszeiger über einem Tool oder einem anderen Benutzeroberflächen Element hält. Die QuickInfo wird in der Nähe des Zeigers angezeigt und verschwindet, wenn der Benutzer auf eine Maustaste klickt, den Zeiger vom Tool entfernt oder einfach ein paar Sekunden wartet.

Das ToolTip-Steuerelement in der folgenden Abbildung zeigt Informationen zu einer Datei auf dem Windows-Desktop. Wenn Sie die Maus über der Abbildung bewegen, sollte auch eine Live-QuickInfo angezeigt werden, die beschreibenden Text enthält.

![Screenshot mit Text in einer QuickInfo, der über eine Datei auf dem Desktop angezeigt wird](images/tt-desktop.png)

In diesem Abschnitt wird beschrieben, wie QuickInfo-Steuerelemente funktionieren und wie Sie erstellt werden.

-   [Verhalten und Darstellung von QuickInfo](#tooltip-behavior-and-appearance)
-   [Erstellen von Quick Infos](#creating-tooltip-controls)
-   [Aktivieren von Quick Infos](#activating-tooltip-controls)
-   [Unterstützende Tools](#supporting-tools)
-   [Anzeigen von Text](#displaying-text)
-   [Messaging und Benachrichtigung](#messaging-and-notification)
-   [Treffertests](#hit-testing)
-   [Standard Nachrichtenverarbeitung](#default-message-processing)

## <a name="tooltip-behavior-and-appearance"></a>Verhalten und Darstellung von QuickInfo

QuickInfo-Steuerelemente können eine einzelne Textzeile oder mehrere Zeilen anzeigen. Ihre Ecken können gerundet oder quadratisch sein. Sie verfügen möglicherweise über ein stem, das auf Tools wie eine Sprechblase zur Sprachausgabe zeigt. QuickInfo-Text kann stationär sein oder mit dem Mauszeiger bewegt werden, der als Nachverfolgung bezeichnet wird. Stationärer Text kann neben einem Tool angezeigt werden, oder er kann über ein Tool angezeigt werden. Dies wird als direkt bezeichnet. Standard-Quick Infos sind stationär, zeigen eine einzelne Textzeile an, haben Quadrat Ecken und haben kein Stamm Zeichen, das auf das Tool zeigt.

Bei der Nachverfolgung von Quick Infos, die von [Version 4,70](common-control-versions.md) der allgemeinen Steuerelemente unterstützt werden, wird die Position auf dem Bildschirm dynamisch geändert. Wenn Sie die Position schnell aktualisieren, scheinen diese QuickInfo-Steuerelemente reibungslos zu verschieben oder "nachverfolgen". Diese sind nützlich, wenn der QuickInfo-Text beim Verschieben der Position des Mauszeigers folgen soll. Weitere Informationen zum Nachverfolgen von Quick Infos und ein Beispiel mit Code, in dem die Erstellung veranschaulicht wird, finden Sie unter nach [verfolgen](using-tooltip-contro.md)von Quick Infos.

Mehrzeilige Quick Infos, die auch von Version 4,70 der allgemeinen Steuerelemente unterstützt werden, zeigen Text auf mehr als einer Zeile an. Diese sind nützlich, um lange Nachrichten anzuzeigen. Weitere Informationen und ein Beispiel, das zeigt, wie Sie mehrzeilige Quick Infos erstellen, finden Sie unter [mehrzeilige Tooltips](using-tooltip-contro.md).

Quick Infos für die Sprechblase werden in einem Feld mit abgerundeten Ecken und einem Stamm Fenster angezeigt, das auf das Tool zeigt. Sie können entweder einzeilige oder mehrzeilige Zeilen sein. Die folgende Abbildung zeigt eine QuickInfo-Sprechblase mit stem und Rechteck an Ihren Standardpositionen. Weitere Informationen zu Quick Infos für die Sprechblase und ein Beispiel für die Erstellung finden Sie unter [verwenden](using-tooltip-contro.md)von QuickInfo-Steuerelementen.

![Screenshot, der eine QuickInfo mit einer Textzeile anzeigt, die über einer Schaltfläche in einem Dialogfeld positioniert ist](images/tt-balloon.png)

Eine QuickInfo kann auch über Titeltext und ein Symbol verfügen, wie in der folgenden Abbildung dargestellt. Beachten Sie, dass die QuickInfo Text enthalten muss. Wenn nur Titel Text enthalten ist, wird die QuickInfo nicht angezeigt. Außerdem wird das Symbol nicht angezeigt, es sei denn, es ist ein Titel vorhanden.

![Screenshot mit einer QuickInfo mit einem Symbol, einem Titel und einem Text, der unter einer Schaltfläche in einem Dialogfeld positioniert ist](images/tt-titled.png)

Manchmal werden Text Zeichenfolgen abgeschnitten, da Sie zu lang sind, damit Sie in einem kleinen Fenster vollständig angezeigt werden können. Direkte Quick Infos werden zum Anzeigen von Text Zeichenfolgen für Objekte verwendet, die abgeschnitten wurden, wie z. b. der Dateiname in der folgenden Abbildung. Ein Beispiel, das zeigt, wie Sie direkte Quick Infos erstellen, finden Sie [unter direkte Tooltipps](using-tooltip-contro.md).

![Screenshot mit einer QuickInfo, die einen Dateinamen enthält, der neben einem Dateisymbol in einem Struktur Steuerelement positioniert ist](images/tt-inplace.png)

Der Cursor muss für einen Zeitraum auf ein Tool zeigen, bevor die QuickInfo angezeigt wird. Die Standarddauer dieses Timeouts wird durch die Doppelklick Zeit des Benutzers gesteuert und ist in der Regel eine halbe Sekunde. Um einen nicht standardmäßigen Timeout Wert anzugeben, senden Sie dem QuickInfo-Steuerelement eine [**TTM- \_ setdelta-Zeit**](ttm-setdelaytime.md) Nachricht.

## <a name="creating-tooltip-controls"></a>Erstellen von Quick Infos

Um ein QuickInfo-Steuerelement zu erstellen, rufen [**Sie den Befehl \_**](common-control-window-classes.md) " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) " auf, und geben Sie die Fenster Klasse Diese Klasse wird registriert, wenn die Common Control-DLL geladen wird. Um sicherzustellen, dass diese DLL geladen wird, schließen Sie die [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) -Funktion in Ihre Anwendung ein. Sie müssen ein QuickInfo-Steuerelement explizit als TopMost definieren. Andernfalls kann Sie durch das übergeordnete Fenster abgedeckt werden. Das folgende Code Fragment zeigt, wie ein ToolTip-Steuerelement erstellt wird.


```
HWND hwndTip = CreateWindowEx(NULL, TOOLTIPS_CLASS, NULL,
                            WS_POPUP | TTS_NOPREFIX | TTS_ALWAYSTIP,
                            CW_USEDEFAULT, CW_USEDEFAULT,
                            CW_USEDEFAULT, CW_USEDEFAULT,
                            hwndParent, NULL, hinstMyDll,
                            NULL);

SetWindowPos(hwndTip, HWND_TOPMOST,0, 0, 0, 0,
             SWP_NOMOVE | SWP_NOSIZE | SWP_NOACTIVATE);
```



Die Fenster Prozedur für das QuickInfo-Steuerelement legt die Größe, Position und Sichtbarkeit des Steuer Elements automatisch fest. Die Höhe des QuickInfo-Fensters basiert auf der Höhe der aktuell im Gerätekontext ausgewählten Schriftart für das QuickInfo-Steuerelement. Die Breite variiert abhängig von der Länge der Zeichenfolge, die sich derzeit im QuickInfo-Fenster befinden.

## <a name="activating-tooltip-controls"></a>Aktivieren von Quick Infos

Ein QuickInfo-Steuerelement kann entweder aktiv oder inaktiv sein. Wenn Sie aktiv ist, wird der QuickInfo-Text angezeigt, wenn sich der Mauszeiger auf einem Tool befindet. Wenn Sie inaktiv ist, wird der QuickInfo-Text nicht angezeigt, auch wenn sich der Zeiger auf einem Tool befindet. Die [**TTM- \_ Aktivierungs**](ttm-activate.md) Nachricht aktiviert und deaktiviert ein QuickInfo-Steuerelement.

## <a name="supporting-tools"></a>Unterstützende Tools

Ein QuickInfo-Steuerelement kann eine beliebige Anzahl von Tools unterstützen. Um ein bestimmtes Tool zu unterstützen, müssen Sie das Tool mit dem QuickInfo-Steuerelement registrieren, indem Sie das Steuerelement der [**TTM \_ AddTool**](ttm-addtool.md) -Nachricht senden. Die Meldung enthält die Adresse einer toolinfo-Struktur, die Informationen bereitstellt, die das [**QuickInfo**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) -Steuerelement zum Anzeigen von Text für das Tool benötigt. Der **UID** -Member der **toolinfo** -Struktur wird von der Anwendung definiert. Jedes Mal, wenn Sie ein Tool hinzufügen, stellt die Anwendung einen eindeutigen Bezeichner bereit. Das **CBSIZE** -Element der **toolinfo** -Struktur ist erforderlich, und es muss die Größe der Struktur angegeben werden.

Ein QuickInfo-Steuerelement unterstützt als Fenster implementierte Tools (z. b. untergeordnete Fenster oder Steuerelement Fenster) und als rechteckige Bereiche innerhalb des Client Bereichs eines Fensters. Wenn Sie ein Tool hinzufügen, das als rechteckiger Bereich implementiert ist, muss der **HWND** -Member der [**toolinfo**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) -Struktur das Handle für das Fenster angeben, das den Bereich enthält, und der **Rect** -Member muss die Client Koordinaten des umgebenden Rechtecks des Bereichs angeben. Außerdem muss der **UID** -Member den von der Anwendung definierten Bezeichner für das Tool angeben.

Wenn Sie ein als Fenster implementiertes Tool hinzufügen, muss der **UID** -Member der [**toolinfo**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) -Struktur das Fenster Handle für das Tool enthalten. Außerdem muss der **uFlags** -Member den Wert " **ttf \_ idewnd** " angeben, der dem QuickInfo-Steuerelement mitteilt, dass das **UID** -Element als Fenster Handle interpretiert werden soll.

## <a name="displaying-text"></a>Anzeigen von Text

Wenn Sie ein Tool zu einem QuickInfo-Steuerelement hinzufügen, muss der **lpszText** -Member der [**toolinfo**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) -Struktur die Adresse der Zeichenfolge angeben, die für das Tool angezeigt werden soll. Nachdem Sie ein Tool hinzugefügt haben, können Sie den Text mithilfe der [**TTM- \_ updatetiptext**](ttm-updatetiptext.md) -Nachricht ändern.

Wenn das hochwertige Wort von **lpszText** NULL ist, muss das nieder wertige Wort der Bezeichner einer Zeichen folgen Ressource sein. Wenn das QuickInfo-Steuerelement den Text benötigt, lädt das System die angegebene Zeichen folgen Ressource aus der Anwendungs Instanz, die durch den **hInst** -Member der [**toolinfo**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) -Struktur identifiziert wird.

Wenn Sie den LPSTR- \_ textcallback-Wert im **lpszText** -Member angeben, benachrichtigt das QuickInfo-Steuerelement das Fenster, das im **HWND** -Member der toolinfo-Struktur angegeben wird, wenn das [**QuickInfo**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa)-Steuerelement Text für das Tool anzeigen muss. Das ToolTip-Steuerelement sendet den [TTN \_ getdispinfo](ttn-getdispinfo.md) -Benachrichtigungs Code an das-Fenster. Die Nachricht enthält die Adresse einer [**nmttdispinfo**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) -Struktur, die das Fenster Handle sowie den von der Anwendung definierten Bezeichner für das Tool enthält. Das Fenster überprüft die Struktur, um das Tool zu ermitteln, für das Text benötigt wird, und füllt die entsprechenden Strukturmember mit Informationen aus, die das QuickInfo-Steuerelement benötigt, um die Zeichenfolge anzuzeigen.

> [!Note]  
> Die maximale Länge für den standardmäßigen QuickInfo-Text beträgt 80 Zeichen. Weitere Informationen finden Sie in der [**nmttdispinfo**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) -Struktur. Mehrzeilige QuickInfo-Text kann länger sein.

 

Viele Anwendungen erstellen Symbolleisten mit Tools, die Menübefehlen entsprechen. Für solche Tools ist es praktisch, dass das ToolTip-Steuerelement denselben Text wie das entsprechende Menü Element anzeigt. Das System entfernt das kaufmännische und-Zeichen (&) automatisch aus allen Zeichen folgen, die an ein QuickInfo-Steuerelement weitergegeben werden, und beendet die Zeichenfolge beim ersten Tabstopp Zeichen ( \\ t), es sei denn, das Steuerelement hat den Typ " [**TTS \_ NoPrefix**](tooltip-styles.md) "

Um den Text für ein Tool abzurufen, verwenden Sie die [**TTM \_ gettext**](ttm-gettext.md) -Nachricht.

## <a name="messaging-and-notification"></a>Messaging und Benachrichtigung

QuickInfo-Text wird normalerweise angezeigt, wenn mit dem Mauszeiger auf einen Bereich gezeigt wird, in der Regel das durch ein Tool wie ein Schaltflächen-Steuerelement definierte Rechteck. Microsoft Windows sendet jedoch nur Maus bezogene Meldungen an das Fenster, das den Zeiger enthält, nicht an das ToolTip-Steuerelement selbst. Maus bezogene Informationen müssen an das QuickInfo-Steuerelement weitergeleitet werden, damit der QuickInfo-Text zum richtigen Zeitpunkt und am richtigen Ort angezeigt wird.

Nachrichten können automatisch übermittelt werden, wenn:

-   Das Tool ist ein Steuerelement oder ist in der [**toolinfo**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) -Struktur des Tools als Rechteck definiert.
-   Das Fenster, das dem Tool zugeordnet ist, befindet sich im gleichen Thread wie das ToolTip-Steuerelement.

Wenn diese beiden Bedingungen erfüllt sind, legen Sie das Flag für die **\_ Unterklasse "ttf** " im **uFlags** -Member der toolinfo-Struktur des Tools fest, wenn Sie das Tool mit [**TTM \_ AddTool**](ttm-addtool.md)dem [**QuickInfo**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) -Steuerelement hinzufügen. Die erforderlichen Maus Meldungen werden dann automatisch an das ToolTip-Steuerelement weitergeleitet.

Wenn Sie die **\_ Unterklasse "ttf** " festlegen, damit Maus Meldungen an das Steuerelement weitergeleitet werden, ist für die meisten Zwecke ausreichend Dies funktioniert jedoch nicht, wenn es keine direkte Verbindung zwischen dem QuickInfo-Steuerelement und dem Tool Fenster gibt. Wenn ein Tool z. b. als rechteckiger Bereich in einem von der Anwendung definierten Fenster implementiert ist, empfängt die Fenster Prozedur die Maus Meldungen. Das Festlegen der **ttf- \_ Unterklasse** genügt, um sicherzustellen, dass Sie an das Steuerelement übermittelt werden. Wenn ein Tool jedoch als System definiertes Fenster implementiert ist, werden Maus Meldungen an dieses Fenster gesendet und sind nicht direkt für die Anwendung verfügbar. In diesem Fall müssen Sie entweder das Fenster Unterklassen oder einen nachrichtenhook verwenden, um auf die Maus Meldungen zuzugreifen. Sie müssen dann mit [**TTM \_ relayevent**](ttm-relayevent.md)Maus Meldungen explizit an das ToolTip-Steuerelement weiterleiten. Ein Beispiel für die Verwendung von **TTM \_ relayevent** finden Sie unter nach [verfolgen](using-tooltip-contro.md)von Quick Infos.

Wenn ein QuickInfo-Steuerelement eine [**WM- \_ MouseMove**](/windows/desktop/inputdev/wm-mousemove) -Nachricht empfängt, bestimmt es, ob sich der Mauszeiger im umschließenden Rechteck eines Tools befindet. Wenn dies der Fall ist, legt das ToolTip-Steuerelement einen Timer fest. Am Ende des Timeout Intervalls prüft das ToolTip-Steuerelement die Position des Zeigers, um festzustellen, ob es verschoben wurde. Wenn dies nicht der Fall ist, ruft das QuickInfo-Steuerelement den Text für das Tool ab und zeigt die QuickInfo an. Das QuickInfo-Steuerelement zeigt das Fenster so lange an, bis es eine relayschaltfläche oder eine Schaltfläche nach unten empfängt oder bis eine **WM- \_ mousermove** -Meldung anzeigt, dass der Zeiger außerhalb des umgebenden Rechtecks des Tools verschoben wurde.

Einem QuickInfo-Steuerelement sind tatsächlich drei Timeout dauern zugeordnet. Die anfängliche Dauer ist die Zeitspanne, in der der Mauszeiger innerhalb des umgebenden Rechtecks eines Tools stationär bleiben muss, bevor das QuickInfo-Fenster angezeigt wird. Die Dauer der erneuten Anzeige ist die Länge der Verzögerung, bevor nachfolgende QuickInfo-Fenster angezeigt werden, wenn der Zeiger von einem Tool zu einem anderen verschoben wird. Die Popup Dauer ist die Zeit, die das QuickInfo-Fenster angezeigt wird, bevor es ausgeblendet wird. Das heißt, wenn der Zeiger innerhalb des umgebenden Rechtecks weiterhin stationär bleibt, nachdem das QuickInfo-Fenster angezeigt wird, wird das QuickInfo-Fenster am Ende der Popup Dauer automatisch ausgeblendet. Sie können alle Timeout dauern mithilfe der Nachricht [**TTM \_ setdelta-Zeit**](ttm-setdelaytime.md) anpassen.

Wenn eine Anwendung ein Tool enthält, das als rechteckiger Bereich implementiert ist, und die Größe oder Position des Steuer Elements geändert wird, kann die Anwendung die [**TTM \_ newtoolrect**](ttm-newtoolrect.md) -Nachricht verwenden, um die Änderung an das ToolTip-Steuerelement zu melden. Eine Anwendung muss keine Größen-und Positionsänderungen für ein Tool melden, das als Fenster implementiert ist, da das QuickInfo-Steuerelement den Fenster Handle des Tools verwendet, um zu bestimmen, ob sich der Mauszeiger auf dem Tool befindet, nicht das umschließende Rechteck des Tools.

Wenn eine QuickInfo angezeigt wird, sendet das QuickInfo-Steuerelement das Besitzer Fenster an einen [TTN \_ ](ttn-show.md) -Anzeige Benachrichtigungs Code. Das Besitzer Fenster empfängt einen [TTN- \_ Pop](ttn-pop.md) -Benachrichtigungs Code, wenn eine QuickInfo im Begriff ist, ausgeblendet zu werden. Jeder Benachrichtigungs Code wird im Kontext einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.

## <a name="hit-testing"></a>Treffertests

Mit der [**TTM \_ HitTest**](ttm-hittest.md) -Meldung können Sie Informationen abrufen, die ein QuickInfo-Steuerelement für das Tool verwaltet, das einen bestimmten Punkt einnimmt. Die Nachricht enthält eine [**tthittestinfo**](/windows/win32/api/commctrl/ns-commctrl-tthittestinfoa) -Struktur, die ein Fenster Handle, die Koordinaten eines Punkts und die Adresse einer [**toolinfo**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) -Struktur enthält. Das QuickInfo-Steuerelement bestimmt, ob ein Tool den Punkt einnimmt, und füllt dann, wenn dies der Fall ist, **toolinfo** mit Informationen über das Tool aus.

## <a name="default-message-processing"></a>Standard Nachrichtenverarbeitung

In der folgenden Tabelle werden die Meldungen beschrieben, die von der Fenster Prozedur für das ToolTip-Steuerelement behandelt werden.



| `Message`                                        | BESCHREIBUNG                                                                                                                                                                                                                                                       |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ Erstellen**](/windows/desktop/winmsg/wm-create)             | Stellt sicher, dass das QuickInfo-Steuerelement die Stile [**WS \_ Ex \_ ToolWindow**](/windows/desktop/winmsg/window-styles) und [**WS \_ Popup**](/windows/desktop/winmsg/window-styles) Window aufweist. Außerdem wird Speicher zugewiesen und interne Variablen initialisiert. |
| [**WM \_ zerstören**](/windows/desktop/winmsg/wm-destroy)           | Gibt für das QuickInfo-Steuerelement zugewiesene Ressourcen frei.                                                                                                                                                                                                                |
| [**WM- \_ getFont**](/windows/desktop/winmsg/wm-getfont)           | Gibt das Handle der Schriftart zurück, die vom QuickInfo-Steuerelement zum Zeichnen von Text verwendet wird.                                                                                                                                                                                    |
| [**WM- \_ mouseelmove**](/windows/desktop/inputdev/wm-mousemove)     | Verbirgt das QuickInfo-Fenster.                                                                                                                                                                                                                                         |
| [**WM- \_ Paint**](/windows/desktop/gdi/wm-paint)                  | Zeichnet das QuickInfo-Fenster.                                                                                                                                                                                                                                         |
| [**WM- \_ setFont**](/windows/desktop/winmsg/wm-setfont)           | Legt das Handle der Schriftart fest, die vom QuickInfo-Steuerelement zum Zeichnen von Text verwendet wird.                                                                                                                                                                                       |
| [**WM- \_ Timer**](/windows/desktop/winmsg/wm-timer)               | Blendet das QuickInfo-Fenster aus, wenn sich das Tool in der Position geändert hat oder wenn der Mauszeiger außerhalb des Tools verschoben wurde. Andernfalls wird das QuickInfo-Fenster angezeigt.                                                                                                             |
| [**WM- \_ wininichange**](/windows/desktop/winmsg/wm-wininichange) | Setzt interne Variablen zurück, die auf Systemmetriken basieren.                                                                                                                                                                                                       |



 

 

 