---
description: Der Benachrichtigungsbereich ist ein Teil der Taskleiste, der eine temporäre Quelle für Benachrichtigungen und Status bereitstellt.
ms.assetid: D37E2BF7-1887-4780-81AD-85B2117321E4
title: Benachrichtigungen und Benachrichtigungsbereich
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89af1d0b8af0b41674f79325f0eeb389cbc8f2c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344139"
---
# <a name="notifications-and-the-notification-area"></a>Benachrichtigungen und Benachrichtigungsbereich

Der Benachrichtigungsbereich ist ein Teil der Taskleiste, der eine temporäre Quelle für Benachrichtigungen und Status bereitstellt. Es kann auch verwendet werden, um Symbole für System-und Programm Features anzuzeigen, die auf dem Desktop nicht vorhanden sind, z. b. Akku-, volumesteuer-und Netzwerkstatus. Der Benachrichtigungsbereich wurde in der Vergangenheit als Systemleiste oder Statusbereich bezeichnet.

Dieses Thema enthält folgende Abschnitte:

-   [Richtlinien für Benachrichtigungen und Benachrichtigungsbereich](#notification-and-notification-area-guidelines)
-   [Erstellen und Anzeigen einer Benachrichtigung](#notifications-and-the-notification-area)
    -   [Benachrichtigungssymbol hinzufügen](#add-a-notification-icon)
    -   [Legen Sie die notisyiendata-Version fest.](#define-the-notifyicondata-version)
    -   [Definieren von Benachrichtigungs Aussehen und-Inhalten](#define-the-notification-look-and-contents)
    -   [Überprüfen des Benutzer Status](#check-the-user-status)
    -   [Anzeigen der Benachrichtigung](#display-the-notification)
    -   [Entfernen eines Symbols](#removing-an-icon)
-   [SDK-Beispiel](#sdk-sample)
-   [Zugehörige Themen](#related-topics)

## <a name="notification-and-notification-area-guidelines"></a>Richtlinien für Benachrichtigungen und Benachrichtigungsbereich

Informationen zu bewährten Methoden bei der Verwendung von Benachrichtigungen und dem Benachrichtigungsbereich finden Sie in den Abschnitten zu den Benachrichtigungs [-und](../uxguide/mess-notif.md) [Benachrichtigungs Bereichen](../uxguide/winenv-notification.md) der Windows-Interaktions Richtlinien für Benutzer. Das Ziel besteht darin, den Benutzer Vorteil durch die angemessene Verwendung von Benachrichtigungen bereitzustellen, ohne dass Sie lästig oder ablenkend sind.

Der Benachrichtigungsbereich ist nicht für wichtige Informationen vorgesehen, auf die sofort reagiert werden muss. Es ist auch nicht für den schnellen Programm-oder Befehls Zugriff vorgesehen. Ab Windows 7 wird ein Großteil dieser Funktionen am besten über die Task leisten Schaltfläche einer Anwendung erreicht.

Windows 7 ermöglicht es Benutzern, alle Benachrichtigungen von einer Anwendung zu unterdrücken, wenn Sie sich entscheiden. durchdachte Benachrichtigungs Entwürfe und-Verwendung wird der Benutzer daher geneigt, die Anwendung weiterhin anzeigen zu können. Benachrichtigungen sind eine Unterbrechung. Stellen Sie sicher, dass Sie den Wert haben.

Mit Windows 7 wird das Konzept der "stillen Zeit" eingeführt. Die quiet-Zeit wird als erste Stunde definiert, nachdem ein neuer Benutzer sich zum ersten Mal bei seinem Konto anmeldet, oder zum ersten Mal nach einem Betriebssystem Upgrade oder einer Neuinstallation. Diese Zeit wird reserviert, um dem Benutzer die Möglichkeit zu geben, sich mit der neuen Umgebung vertraut zu machen, ohne die Benachrichtigungen zu benachrichtigen. Während dieser Zeit sollten die meisten Benachrichtigungen nicht gesendet oder angezeigt werden. Ausnahmen enthalten Feedback, das der Benutzer als Reaktion auf eine Benutzeraktion erwarten würde, z. b. wenn er ein USB-Gerät einfügt oder ein Dokument druckt. API-Besonderheiten von bezüglich der stillen Zeit werden weiter unten in diesem Thema erläutert.

## <a name="creating-and-displaying-a-notification"></a>Erstellen und Anzeigen einer Benachrichtigung

In den restlichen Abschnitten dieses Themas wird das grundlegende Verfahren erläutert, das Sie befolgen müssen, um eine Benachrichtigung von Ihrer Anwendung an den Benutzer anzuzeigen.

1.  [Benachrichtigungssymbol hinzufügen](#add-a-notification-icon)
2.  [Legen Sie die notisyiendata-Version fest.](#define-the-notifyicondata-version)
3.  [Definieren von Benachrichtigungs Aussehen und-Inhalten](#define-the-notification-look-and-contents)
4.  [Überprüfen des Benutzer Status](#check-the-user-status)
5.  [Anzeigen der Benachrichtigung](#display-the-notification)
6.  [Entfernen eines Symbols](#removing-an-icon)

### <a name="add-a-notification-icon"></a>Benachrichtigungssymbol hinzufügen

Um eine Benachrichtigung anzuzeigen, müssen Sie über ein Symbol im Benachrichtigungsbereich verfügen. In bestimmten Fällen, wie z. b. Microsoft Communicator oder Akku Ebene, ist dieses Symbol bereits vorhanden. In vielen anderen Fällen fügen Sie jedoch dem Benachrichtigungsbereich nur so lange ein Symbol hinzu, wie es zum Anzeigen der Benachrichtigung benötigt wird. In beiden Fällen wird dies mithilfe der [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) -Funktion erreicht. **Shell \_ NotifyIcon** ermöglicht das Hinzufügen, ändern oder Löschen eines Symbols im Benachrichtigungsbereich.

![Benachrichtigungsbereich, der drei Symbole enthält](images/taskbar/notificationareaicons.png)

Wenn ein Symbol zum Infobereich unter Windows 7 hinzugefügt wird, wird es standardmäßig dem Überlauf Abschnitt des Benachrichtigungs Bereichs hinzugefügt. Dieser Bereich enthält Benachrichtigungs Bereichs Symbole, die aktiv sind, aber nicht im Benachrichtigungsbereich sichtbar sind. Nur der Benutzer kann ein Symbol vom Überlauf in den Benachrichtigungsbereich herauf Stufen, obwohl das System unter bestimmten Umständen ein Symbol vorübergehend als kurze Vorschau (in einer Minute) in den Benachrichtigungsbereich herauf Stufen kann.

> [!Note]  
> Der Benutzer sollte in seinem Benachrichtigungsbereich das letzte Mal über die gewünschten Symbole verfügen. Vor der Installation eines nicht vorübergehenden Symbols im Benachrichtigungsbereich sollte der Benutzer zur Berechtigung aufgefordert werden. Außerdem sollte Ihnen die Option (normalerweise das Kontextmenü) zugewiesen werden, um das Symbol aus dem Benachrichtigungsbereich zu entfernen.

 

Die [**notifyiendata**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) -Struktur, die im aufrufungsshellbenachrichtigungshub gesendet wird, enthält Informationen, die sowohl das Benachrichtigungs Bereichs Symbol als auch die Benachrichtigung selbst angeben. [**\_**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) Die folgenden Elemente sind für das Benachrichtigungs Bereichs Symbol selbst spezifisch, das über **notifyiendata** festgelegt werden kann.

-   Die Ressource, aus der das Symbol entnommen wird.
-   Ein eindeutiger Bezeichner für das Symbol.
-   Der Stil der QuickInfo des Symbols.
-   Der Zustand des Symbols (ausgeblendet, freigegeben oder beides) im Benachrichtigungsbereich.
-   Das Handle eines Anwendungsfensters, das dem Symbol zugeordnet ist.
-   Ein Rückruf Nachrichten Bezeichner, der es dem Symbol ermöglicht, Ereignisse, die innerhalb des umgebenden Rechtecks des Symbols auftreten, und die Sprechblasen Benachrichtigung mit dem zugeordneten Anwendungsfenster zu kommunizieren. Das umgebende Rechteck des Symbols kann über die [**Shell \_ notifyicyienrect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect)abgerufen werden.

Jedes Symbol im Benachrichtigungsbereich kann auf zwei Arten identifiziert werden:

-   Die GUID, mit der das Symbol in der Registrierung deklariert wird. Dies ist die bevorzugte Methode unter Windows 7 und höher.
-   Das Handle eines Fensters, das mit dem Symbol für den Benachrichtigungsbereich verknüpft ist, sowie ein Anwendungs definierter Symbol Bezeichner. Diese Methode wird unter Windows Vista und früheren Versionen verwendet.

Symbole im Benachrichtigungsbereich können eine QuickInfo aufweisen. Die QuickInfo kann entweder eine Standard-QuickInfo (bevorzugt) oder eine von der Anwendung gezeichnete Popup-Benutzeroberfläche sein. Eine QuickInfo ist zwar nicht erforderlich, es wird jedoch empfohlen.

Benachrichtigungs Bereichs Symbole sollten hoch dpi-fähig sein. Eine Anwendung sollte sowohl ein 16x16-Pixel-Symbol als auch ein 32 x 32-Symbol in der Ressourcen Datei bereitstellen. verwenden Sie dann [**loadiinmetric**](/windows/win32/api/commctrl/nf-commctrl-loadiconmetric) , um sicherzustellen, dass das korrekte Symbol geladen und entsprechend skaliert wird.

Die Anwendung, die für das Benachrichtigungs Bereichs Symbol zuständig ist, sollte für dieses Symbol einen Mausklick verarbeiten. Wenn ein Benutzer mit der rechten Maustaste auf das Symbol klickt, sollte ein normales Kontextmenü angezeigt werden. Das Ergebnis eines einzelnen Klicks mit der linken Maustaste unterscheidet sich jedoch von der Funktion des Symbols. Es sollte angezeigt werden, was der Benutzer in dem Formular sehen würde, das sich am besten für diesen Inhalt eignet – ein Popup Fenster, ein Dialogfeld oder das Programmfenster selbst. Beispielsweise kann der Status Text für ein Statussymbol oder ein Schieberegler für das volumesteuerelement angezeigt werden.

Die Platzierung eines Popup Fensters oder eines Dialog Felds, das sich aus dem Klick ergibt, sollte sich in der Nähe der Koordinaten des Click im Benachrichtigungsbereich befinden. Verwenden Sie [**calculatepopupwindowposition**](/windows/win32/api/winuser/nf-winuser-calculatepopupwindowposition) , um den Speicherort zu bestimmen.

Das Symbol kann dem Benachrichtigungsbereich hinzugefügt werden, ohne dass eine Benachrichtigung angezeigt wird, indem nur die Symbol spezifischen Member von [**notifyiendata**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) definiert werden (oben erläutert) und die [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) aufgerufen wird, wie hier gezeigt:


```
NOTIFYICONDATA nid = {};
// Do NOT set the NIF_INFO flag.
...                    
Shell_NotifyIcon(NIM_ADD, &nid);
```



Sie können das Symbol auch dem Benachrichtigungsbereich hinzufügen und eine Benachrichtigung in einem einzigen aufrufsbenachrichtigungs-Befehl [**anzeigen. \_**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) Fahren Sie zu diesem Zweck mit den Anweisungen in diesem Thema fort.

### <a name="define-the-notifyicondata-version"></a>Legen Sie die notisyiendata-Version fest.

Wenn Windows fortgeschritten ist, wurde die [**notifyiendata**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) -Struktur erweitert, sodass Sie mehr Mitglieder enthält, um mehr Funktionalität zu definieren. Konstanten werden verwendet, um zu deklarieren, welche Version von **notifyiendata** mit dem Benachrichtigungs Bereichs Symbol verwendet werden soll, um Abwärtskompatibilität zu ermöglichen. Es wird dringend empfohlen, dass Sie die Version 4 der NotifyIcon \_ Version \_ 4 verwenden, die in Windows Vista eingeführt wurde, es sei denn, es gibt einen überzeugenden Grund dafür. Diese Version bietet die vollständige verfügbare Funktionalität, einschließlich der bevorzugten Fähigkeit, das Benachrichtigungs Bereichs Symbol, aber eine registrierte GUID, einen übergeordneten Rückrufmechanismus und eine bessere Barrierefreiheit zu identifizieren.

Legen Sie die Version mit den folgenden Aufrufen fest:


```
NOTIFYICONDATA nid = {};
... 
nid.uVersion = NOTIFYICON_VERSION_4;
// Add the icon
Shell_NotifyIcon(NIM_ADD, &nid);
// Set the version
Shell_NotifyIcon(NIM_SETVERSION, &nid);
```



Beachten Sie, dass beim Aufrufen von [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) keine Benachrichtigung angezeigt wird.

### <a name="define-the-notification-look-and-contents"></a>Definieren von Benachrichtigungs Aussehen und-Inhalten

Eine Benachrichtigung ist eine besondere Art von QuickInfo-Steuerelement. Sie enthält einen Titel, Textkörper und ein Symbol. Ebenso wie ein Fenster befindet sich die Schaltfläche **Schließen** in der oberen rechten Ecke. Sie enthält auch eine **options** Schaltfläche, die das Info Bereichs Symbol-Element in der Systemsteuerung öffnet, das es dem Benutzer ermöglicht, das Symbol anzuzeigen oder auszublenden oder nur Benachrichtigungen ohne Symbol anzuzeigen.

![Screenshot der Benachrichtigungs Sprechblase, die anzeigt, dass die Stromversorgung gering ist](images/taskbar/notificationballoon.png)

Die [**notifyiendata**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) -Struktur, die im aufrufungsshellbenachrichtigungshub gesendet wird, enthält Informationen, die sowohl das Benachrichtigungs Bereichs Symbol als auch die Benachrichtigungs Sprechblase selbst angeben. [**\_**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) Im folgenden finden Sie die für die Benachrichtigung spezifischen Elemente, die über **notifyitendata** festgelegt werden können.

-   Ein Symbol, das in der Benachrichtigungs Sprechblase angezeigt wird, die durch den Benachrichtigungstyp angegeben wird. Die Größe des Symbols sowie benutzerdefinierte Symbole können angegeben werden.
-   Ein Benachrichtigungs Titel. Dieser Titel sollte maximal 48 Zeichen lang sein (um die Lokalisierung zu ermöglichen). Der Titel ist die erste Zeile der Benachrichtigung und wird durch die Verwendung von Schriftart Größe, Farbe und Gewichtung festgelegt.
-   Text zur Verwendung im Text der Benachrichtigung. Dieser Text sollte maximal 200 Zeichen lang sein (um die Lokalisierung zu ermöglichen).
-   Gibt an, ob die Benachrichtigung verworfen werden soll, wenn Sie nicht sofort angezeigt werden kann.
-   Ein Timeout für die Benachrichtigung. Diese Einstellung wird in Windows Vista-Systemen und neueren Systemen zugunsten einer systemweiten Einstellung für das Barrierefreiheits Timeout ignoriert.
-   Gibt an, ob die Benachrichtigung eine Stille Zeit beachten sollte, festgelegt über das Flag " [**NIIF \_ Respect \_ quiet \_ time**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) ".

> [!Note]  
> Die [**iusernotification**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification) -und [**IUserNotification2**](/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2) -Schnittstellen sind Component Object Model (com)-Wrapper für [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona). Zu diesem Zeitpunkt stellen Sie jedoch nicht die vollständige NotifyIcon- \_ Version \_ 4-Funktionalität bereit, die über **Shell \_ NotifyIcon** direkt verfügbar ist, einschließlich der Verwendung einer GUID, um das Symbol für den Benachrichtigungsbereich zu identifizieren.

 

### <a name="check-the-user-status"></a>Überprüfen des Benutzer Status

Das System verwendet die Funktion " [**shqueryusernotificationstate**](/windows/desktop/api/Shellapi/nf-shellapi-shqueryusernotificationstate) ", um zu überprüfen, ob sich der Benutzer in der stillen Zeit, vom Computer oder in einem nicht unter brechbaren Zustand wie dem Präsentationsmodus befindet. Ob das System Ihre Benachrichtigung anzeigt, hängt von diesem Zustand ab.

> [!Note]  
> Wenn Ihre Anwendung eine benutzerdefinierte Benachrichtigungs Methode verwendet, die [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona), [**iusernotification**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification)oder [**IUserNotification2**](/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2)nicht verwendet, sollte Sie immer explizit [**shqueryusernotificationstate**](/windows/desktop/api/Shellapi/nf-shellapi-shqueryusernotificationstate) aufrufen, um zu bestimmen, ob die Benutzeroberfläche zu diesem Zeitpunkt angezeigt werden soll.

 

Benachrichtigungen, die gesendet werden, wenn der Benutzer nicht mehr verfügbar ist, werden zur Anzeige in die Warteschlange eingereiht, aber da Sie nicht wissen, wann der Benutzer zurückgibt oder ob die Benachrichtigung zu diesem Zeitpunkt weiterhin gültig ist, sollten Sie die Benachrichtigung später erneut senden.

Während der stillen Zeit gesendete Benachrichtigungen werden nicht angezeigt. Entwurfs Richtlinien stellen fest, dass alle Benachrichtigungen ignoriert werden können. Sie sollten keine sofortige Benutzeraktion erfordern. Daher ist keine Benachrichtigung so wichtig, dass Sie eine Stille Zeit überschreiben sollte.

### <a name="display-the-notification"></a>Anzeigen der Benachrichtigung

Nachdem Sie die [**notifyiendata**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) -Version festgelegt und die Benachrichtigung in einer **notifyiendata** -Struktur definiert haben, können Sie [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) aufrufen, um das Symbol anzuzeigen.

-   Wenn das Benachrichtigungs Bereichs Symbol nicht vorhanden ist, können Sie [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) aufzurufen, um das Symbol hinzuzufügen. Dies geschieht sowohl für vorübergehende als auch für nicht vorübergehende Symbole.
    ```
    NOTIFYICONDATA nid = {};
    ...                    
    Shell_NotifyIcon(NIM_ADD, &nid);
    ```

    

-   Wenn das Benachrichtigungs Bereichs Symbol bereits vorhanden ist, müssen Sie [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) aufzurufen, um das Symbol zu ändern.
    ```
    NOTIFYICONDATA nid = {};
    ...                    
    Shell_NotifyIcon(NIM_MODIFY, &nid);
    ```

    

Der folgende Code zeigt ein Beispiel für das Festlegen von [**notisyiendata**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) -Daten und das Senden der Daten über die [**\_ shellbenachrichtigung**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona). Beachten Sie, dass in diesem Beispiel das Benachrichtigungssymbol über eine GUID (bevorzugt in Windows 7) identifiziert wird.


```
// Declare NOTIFYICONDATA details. 
    // Error handling is omitted here for brevity. Do not omit it in your code.
    
    NOTIFYICONDATA nid = {};
    nid.cbSize = sizeof(nid);
    nid.hWnd = hWnd;
    nid.uFlags = NIF_ICON | NIF_TIP | NIF_GUID;
    
    // Note: This is an example GUID only and should not be used.
    // Normally, you should use a GUID-generating tool to provide the value to
    // assign to guidItem.
    static const GUID myGUID = 
    {0x23977b55, 0x10e0, 0x4041, {0xb8, 0x62, 0xb1, 0x95, 0x41, 0x96, 0x36, 0x69}};
    nid.guidItem = myGUID;
    
    nid.guidItem = guid;
    
    // This text will be shown as the icon's tooltip.
    StringCchCopy(nid.szTip, ARRAYSIZE(nid.szTip), L"Test application");
    
    // Load the icon for high DPI.
    LoadIconMetric(hInst, MAKEINTRESOURCE(IDI_SMALL), LIM_SMALL, &(nid.hIcon));
    
    // Show the notification.
    Shell_NotifyIcon(NIM_ADD, &nid) ? S_OK : E_FAIL;
```



### <a name="removing-an-icon"></a>Entfernen eines Symbols

So entfernen Sie ein Symbol – Wenn Sie z. b. das Symbol nur vorübergehend hinzugefügt haben, um eine Benachrichtigung zu übertragen – nennen Sie die [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona), wie hier gezeigt. In diesem-Befehl wird nur eine minimale [**notifyiendata**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) -Struktur, die das Symbol identifiziert, benötigt.


```
NOTIFYICONDATA nid = {};
...                    
Shell_NotifyIcon(NIM_DELETE, &nid);
```



> [!Note]  
> Wenn eine Anwendung deinstalliert wird, kann der Benutzer das Benachrichtigungs Bereichs Symbol für bis zu sieben Tage weiterhin als Option auf der Seite "Info Bereichs Symbole" in der Systemsteuerung angezeigt werden. Alle Änderungen, die Sie vorgenommen haben, haben jedoch keine Auswirkungen.

 

## <a name="sdk-sample"></a>SDK-Beispiel

Ein vollständiges Beispiel für die Verwendung von [**Shell \_ notioyicon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona)finden Sie unter [notificationicon Sample](samples-notificationicon.md) Sample im Windows Software Development Kit (SDK).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Benachrichtigung zur Shell \_**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona)
</dt> <dt>

[**Shell \_ notityitrect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect)
</dt> <dt>

[**Notier\data**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa)
</dt> <dt>

[**Shqueryusernotificationstate**](/windows/desktop/api/Shellapi/nf-shellapi-shqueryusernotificationstate)
</dt> <dt>

[**Iusernotification**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification)
</dt> <dt>

[**IUserNotification2**](/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2)
</dt> <dt>

[Die Taskleiste](taskbar.md)
</dt> <dt>

[Task leisten Erweiterungen](taskbar-extensions.md)
</dt> </dl>

 

 
