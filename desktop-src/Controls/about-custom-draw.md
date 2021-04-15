---
title: Informationen zum benutzerdefinierten Zeichnen
description: Dieser Abschnitt enthält allgemeine Informationen über benutzerdefinierte Zeichnungsfunktionen und bietet eine konzeptionelle Übersicht darüber, wie eine Anwendung benutzerdefiniertes Zeichnen unterstützen kann.
ms.assetid: dd104661-1e0c-4569-9753-817bcded1894
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 121a4df5aa6fab222a5c4387ebdcfba51a7977b2
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "104474553"
---
# <a name="about-custom-draw"></a>Informationen zum benutzerdefinierten Zeichnen

Dieser Abschnitt enthält allgemeine Informationen über benutzerdefinierte Zeichnungsfunktionen und bietet eine konzeptionelle Übersicht darüber, wie eine Anwendung benutzerdefiniertes Zeichnen unterstützen kann. Derzeit unterstützen die folgenden Steuerelemente benutzerdefinierte Zeichnungsfunktionen:

-   Header Steuerelemente
-   Listenansicht-Steuerelemente
-   Grund leisten-Steuerelemente
-   Symbolleisten-Steuerelemente
-   ToolTip-Steuerelemente
-   TrackBar-Steuerelemente
-   Strukturansicht-Steuerelemente

<!-- -->

-   [Informationen zu benutzerdefinierten Zeichnungs Benachrichtigungen](#about-custom-draw-notification-messages)
-   [Zeichnungs Zyklen, Zeichnungs Phasen und Benachrichtigungs Meldungen](#paint-cycles-drawing-stages-and-notification-messages)
-   [Nutzen benutzerdefinierter Draw-Dienste](#taking-advantage-of-custom-draw-services)
    -   [Antworten auf die PrePaint-Benachrichtigung](#responding-to-the-prepaint-notification)
    -   [Anfordern von Element spezifischen Benachrichtigungen](#requesting-item-specific-notifications)
    -   [Eigenes Zeichnen des Elements](#drawing-the-item-yourself)
    -   [Ändern von Schriftarten und Farben](#changing-fonts-and-colors)
-   [Benutzerdefiniertes Zeichnen mit List-View und Tree-View Steuerelementen](#custom-draw-with-list-view-and-tree-view-controls)
    -   [Benutzerdefiniertes Zeichnen mit List-View Steuerelementen](#custom-draw-with-list-view-controls)
-   [Zugehörige Themen](#related-topics)

## <a name="about-custom-draw-notification-messages"></a>Informationen zu benutzerdefinierten Zeichnungs Benachrichtigungen

Alle allgemeinen Steuerelemente, die benutzerdefinierte Zeichen unterstützen, senden bei Zeichnungs Vorgängen an bestimmten Punkten die Benachrichtigungs Codes von [nm \_ ](nm-customdraw.md) . Diese Benachrichtigungs Codes beschreiben Zeichnungsvorgänge, die für das gesamte Steuerelement gelten, sowie Zeichnungsvorgänge, die für Elemente innerhalb des Steuer Elements spezifisch sind. Wie viele Benachrichtigungs Codes \_ werden nm customdraw-Benachrichtigungen als [**WM \_**](wm-notify.md) -Benachrichtigungs Nachrichten gesendet.

Der *LPARAM* -Parameter einer benutzerdefinierten Zeichnungs Benachrichtigung ist die Adresse einer [**nmcustomdraw**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) -Struktur oder eine Steuerelement spezifische Struktur, die eine **nmcustomdraw** -Struktur als ersten Member enthält. In der folgenden Tabelle wird die Beziehung zwischen den Steuerelementen und den von Ihnen verwendeten Strukturen veranschaulicht.



| Struktur                                | Verwendet von                              |
|------------------------------------------|--------------------------------------|
| [**Nmcustomdraw**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw)     | Info Leiste, TrackBar und Header Steuerelemente |
| [**Nmlvcustomdraw**](/windows/win32/api/commctrl/ns-commctrl-nmlvcustomdraw) | Listenansicht-Steuerelemente                   |
| [**Nmtbcustomdraw**](/windows/desktop/api/Commctrl/ns-commctrl-nmtbcustomdraw) | Symbolleisten-Steuerelemente                     |
| [**Nmttcustomdraw**](/windows/win32/api/commctrl/ns-commctrl-nmttcustomdraw) | ToolTip-Steuerelemente                     |
| [**Nmtvcustomdraw**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) | Strukturansicht-Steuerelemente                   |



 

## <a name="paint-cycles-drawing-stages-and-notification-messages"></a>Zeichnungs Zyklen, Zeichnungs Phasen und Benachrichtigungs Meldungen

Wie bei allen Windows-Anwendungen zeichnen sich allgemeine Steuerelemente in regelmäßigen Abständen auf der Grundlage von Nachrichten aus dem System oder anderen Anwendungen ab. Der Prozess eines Steuer Elements, das das Zeichnen oder löschen selbst bezeichnet, wird als Zeichnungs *Kreis* bezeichnet. Steuerelemente, die benutzerdefinierte [Zeichnungs \_ Codes](nm-customdraw.md) unterstützen Dieser Benachrichtigungs Code wird von einer [**nmcustomdraw**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) -Struktur oder einer anderen Struktur begleitet, die eine **nmcustomdraw** -Struktur als ersten Member enthält.

Ein Informationselement, das die [**nmcustomdraw**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) -Struktur enthält, ist die aktuelle Phase des Zeichnungs Zyklen. Dies wird als *Zeichnungsphase* bezeichnet und wird durch den Wert im **dwdrawstage** -Member der Struktur dargestellt. Ein Steuerelement informiert das übergeordnete Element über vier grundlegende Zeichnungs Stufen. Diese grundlegenden oder globalen Zeichnungs Phasen werden in der Struktur durch die folgenden Flagwerte dargestellt (definiert in "kommctrl. h").



| Globale Werte für zeichnen-Stufen | BESCHREIBUNG                        |
|--------------------------|------------------------------------|
| CDDs- \_ präpaint           | Vor Beginn des Farb Zyklen.     |
| CDDs \_ PostPaint          | Nachdem der Farb Durchlauf fertiggestellt wurde. |
| CDDs- \_ vorlöschung           | Vor Beginn des Löschvorgangs.     |
| CDDs- \_ posterase          | Nach Abschluss des Löschvorgangs. |



 

Jeder der vorangehenden Werte kann mit dem CDDs- \_ elementflag kombiniert werden, um für Elemente spezifische Zeichnungs Stufen anzugeben. Der praktische Wert enthält "kommctrl. h" die folgenden Element spezifischen Werte.



| Element spezifische Zeichnungs Stufen Werte | BESCHREIBUNG                                                                                                                                                                                                                                                                         |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CDDs \_ itemprepaint              | Vor dem Zeichnen eines Elements.                                                                                                                                                                                                                                                            |
| CDDs \_ itempostpaint             | Nachdem ein Element gezeichnet wurde.                                                                                                                                                                                                                                                       |
| CDDs \_ itempreerase              | Vor dem Löschen eines Elements.                                                                                                                                                                                                                                                           |
| CDDs \_ itemposterase             | Nachdem ein Element gelöscht wurde.                                                                                                                                                                                                                                                      |
| CDDs-Unterelement \_                   | [Allgemeine Steuerelement Versionen](common-control-versions.md) 4,71. Flag, das mit CDDs \_ itemprepaint oder CDDs \_ itempostpaint kombiniert wird, wenn ein Unterelement gezeichnet wird. Dieser Wert wird nur festgelegt, wenn [**cdrf \_ noticyitemdraw**](cdrf-constants.md) von CDDs \_ PrePaint zurückgegeben wird. |



 

Die Anwendung muss den " [nm \_ customdraw](nm-customdraw.md) "-Benachrichtigungs Code verarbeiten und dann einen bestimmten Wert zurückgeben, der dem Steuerelement mitteilt, was es tun muss. Weitere Informationen zu diesen Rückgabe Werten finden Sie in den folgenden Abschnitten.

## <a name="taking-advantage-of-custom-draw-services"></a>Nutzen benutzerdefinierter Draw-Dienste

Der Schlüssel für die benutzerdefinierte Zeichnungs Funktionalität besteht darin, auf die von einem Steuerelement gesendeten [nm \_ customdraw](nm-customdraw.md) -Benachrichtigungs Codes zu reagieren. Die Rückgabewerte, die Ihre Anwendung als Antwort auf diese Benachrichtigungen sendet, bestimmen das Verhalten des Steuer Elements für diesen Zeichnungs Kreis.

Dieser Abschnitt enthält Informationen darüber, wie die Anwendung die Rückgabewerte des Steuer Elements mithilfe von [nm \_ customdraw](nm-customdraw.md) -Benachrichtigungs Rückgabe Werten bestimmen kann.

Details werden in die folgenden Themen unterteilt:

-   [Antworten auf die PrePaint-Benachrichtigung](#responding-to-the-prepaint-notification)
-   [Anfordern von Element spezifischen Benachrichtigungen](#requesting-item-specific-notifications)
-   [Eigenes Zeichnen des Elements](#drawing-the-item-yourself)
-   [Ändern von Schriftarten und Farben](#changing-fonts-and-colors)

### <a name="responding-to-the-prepaint-notification"></a>Antworten auf die PrePaint-Benachrichtigung

Am Anfang jedes Zeichnungs Zyklen sendet das Steuerelement den " [nm \_ customdraw](nm-customdraw.md) "-Benachrichtigungs Code, wobei der CDDs- \_ PrePaint-Wert im **dwdrawstage** -Member der zugehörigen nm- \_ customdraw-Struktur angegeben wird. Der Wert, den die Anwendung an diese erste Benachrichtigung zurückgibt, legt fest, wie und wann das Steuerelement nachfolgende benutzerdefinierte Zeichnungs Benachrichtigungen für den Rest dieses Zeichnungs Zyklen sendet. Die Anwendung kann eine Kombination der folgenden Flags als Antwort auf die erste Benachrichtigung zurückgeben.



| Rückgabewert            | Wirkung                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| cdrf \_ DODEFAULT         | Das Steuerelement zeichnet sich selbst auf. Für diesen Zeichnungs Kreis werden keine zusätzlichen [nm- \_ customdraw](nm-customdraw.md) -Benachrichtigungen gesendet. Dieses Flag kann nicht mit einem anderen Flag verwendet werden.                                                                                                                                                                                                                                                                               |
| cdrf \_ doerase           | Das-Steuerelement zeichnet nur den Hintergrund.                                                                                                                                                                                                                                                                                                                                                                                                                    |
| cdrf \_ newFont           | Ihre Anwendung hat eine neue Schriftart für das Element angegeben. das-Steuerelement verwendet die neue Schriftart. Weitere Informationen zum Ändern von Schriftarten finden Sie unter [Ändern von Schriftarten und Farben](#changing-fonts-and-colors). Dies tritt auf, wenn **dwdrawstage** auf CDDs \_ itemprepaint zugreift.                                                                                                                                                                                                       |
| cdrf \_ notiteyitemdraw    | Das-Steuerelement benachrichtigt das übergeordnete Element über Element spezifische Zeichnungsvorgänge. Sie sendet vor und nach dem Zeichnen von Elementen [nm \_ customdraw](nm-customdraw.md) -Benachrichtigungs Codes. Dies tritt auf, wenn **dwdrawstage** dem CDDs- \_ präpaint gleicht.                                                                                                                                                                                                                       |
| cdrf \_ notifyposterase   | Das-Steuerelement benachrichtigt das übergeordnete Element nach dem Löschen eines Elements. Dies tritt auf, wenn **dwdrawstage** dem CDDs- \_ präpaint gleicht.                                                                                                                                                                                                                                                                                                                                             |
| cdrf \_ notifypostpaint   | Das-Steuerelement sendet eine [nm- \_ customdraw](nm-customdraw.md) -Benachrichtigung, wenn der Zeichnungs Kreis für das gesamte-Steuerelement vollständig ist. Dies tritt auf, wenn **dwdrawstage** dem CDDs- \_ präpaint gleicht.                                                                                                                                                                                                                                                                 |
| cdrf \_ notifysubitemdraw | [Version 4,71](common-control-versions.md). Die Anwendung empfängt eine [nm \_ customdraw](nm-customdraw.md) -Benachrichtigung, wobei **dwdrawstage** auf CDDs \_ itemprepaint \| CDDs \_ Unterelement festgelegt ist, bevor die einzelnen Listen Ansichts unter Elemente gezeichnet werden. Anschließend können Sie Schriftart und Farbe für jedes Unterelement separat angeben oder [**cdrf \_ DODEFAULT**](cdrf-constants.md) für die Standard Verarbeitung zurückgeben. Dies tritt auf, wenn **dwdrawstage** auf CDDs \_ itemprepaint zugreift. |
| cdrf \_ skipdefault       | Die Anwendung hat das Element manuell gezeichnet. Das-Steuerelement zeichnet das Element nicht. Dies tritt auf, wenn **dwdrawstage** auf CDDs \_ itemprepaint zugreift.                                                                                                                                                                                                                                                                                                                      |
| cdrf \_ skippostpaint     | Das-Steuerelement zeichnet das Fokus Rechteck nicht um ein Element.                                                                                                                                                                                                                                                                                                                                                                                                 |



 

### <a name="requesting-item-specific-notifications"></a>Anfordern von Element spezifischen Benachrichtigungen

Wenn Ihre Anwendung [**cdrf \_ notifyitemdraw**](cdrf-constants.md) an die anfängliche benutzerdefinierte Zeichnen-Benachrichtigung von PrePaint zurückgibt, sendet das Steuerelement Benachrichtigungen für jedes Element, das während dieses Zeichnungs Zyklen gezeichnet wird. Diese Element spezifischen Benachrichtigungen erhalten den CDDs- \_ itemprepaint-Wert im **dwdrawstage** -Member der zugehörigen [**nmcustomdraw**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) -Struktur. Sie können anfordern, dass das Steuerelement eine andere Benachrichtigung sendet, wenn das Zeichnen des Elements abgeschlossen ist, indem Sie [**cdrf \_ notifypostpaint**](cdrf-constants.md) an diese Element spezifischen Benachrichtigungen zurückgeben. Andernfalls wird [**cdrf \_ DODEFAULT**](cdrf-constants.md) zurückgegeben, und das Steuerelement benachrichtigt das übergeordnete Fenster erst, wenn es beginnt, das nächste Element zu zeichnen.

### <a name="drawing-the-item-yourself"></a>Eigenes Zeichnen des Elements

Wenn die Anwendung das gesamte Element zeichnet, wird [**cdrf \_ skipdefault**](cdrf-constants.md)zurückgegeben. Dies ermöglicht es dem Steuerelement, Elemente zu überspringen, die nicht gezeichnet werden müssen, wodurch der System Aufwand verringert wird. Beachten Sie, dass das zurückgeben dieses Werts bedeutet, dass das Steuerelement keinen Teil des Elements zeichnet.

### <a name="changing-fonts-and-colors"></a>Ändern von Schriftarten und Farben

Die Anwendung kann mit benutzerdefiniertem zeichnen die Schriftart eines Elements ändern. Wählen Sie einfach das gewünschte hFont in den Gerätekontext aus, der vom **hdc** -Mitglied der [**nmcustomdraw**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) -Struktur angegeben wird, die der benutzerdefinierten Zeichnungs Benachrichtigung zugeordnet ist. Da die von Ihnen gewählte Schriftart möglicherweise andere Metriken als die Standard Schriftart enthält, sollten Sie sicherstellen, dass Sie das [**cdrf \_ newFont**](cdrf-constants.md) -Bit in den Rückgabewert für die Benachrichtigungsnachricht einschließen. Weitere Informationen zur Verwendung dieser Funktion finden Sie im Beispielcode in [Verwenden von benutzerdefiniertem zeichnen](using-custom-draw.md). Die Schriftart, die von der Anwendung angegeben wird, wird verwendet, um das Element anzuzeigen, wenn es nicht ausgewählt ist. Benutzerdefinierte Zeichnen ermöglicht keine Änderung der Schriftart Attribute für ausgewählte Elemente.

Um die Textfarben für alle Steuerelemente zu ändern, die eine benutzerdefinierte Zeichnung mit Ausnahme der Listenansicht und der Strukturansicht unterstützen, legen Sie einfach die gewünschten Text-und Hintergrundfarben im Gerätekontext fest, der in der benutzerdefinierten Zeichnen-Benachrichtigungs Struktur mit den Funktionen [**SetTextColor**](/windows/desktop/api/wingdi/nf-wingdi-settextcolor) und [**SetBkColor**](/windows/desktop/api/wingdi/nf-wingdi-setbkcolor) Um die Textfarben in der Listenansicht oder Strukturansicht zu ändern, müssen Sie die gewünschten Farbwerte in die Member **clrtext** und **clrtextbk** der [**nmlvcustomdraw**](/windows/win32/api/commctrl/ns-commctrl-nmlvcustomdraw) -oder [**nmtvcustomdraw**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) -Struktur platzieren.

> [!Note]  
> Vor [Version 6,0](common-control-versions.md) der allgemeinen Steuerelemente ignorieren Symbolleisten das [**cdrf \_ newFont**](cdrf-constants.md) -Flag. Version 6,0 unterstützt das **cdrf \_ newFont** -Flag, und Sie können es verwenden, um eine andere Schriftart für die Symbolleiste auszuwählen. Es ist jedoch nicht möglich, die Farbe einer Symbolleiste zu ändern, wenn ein visueller Stil aktiv ist. Um die Farbe einer Symbolleiste in Version 6,0 zu ändern, müssen Sie zuerst visuelle Stile deaktivieren, indem Sie [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) aufrufen und keinen visuellen Stil angeben:

 


```
SetWindowTheme (hwnd, "", "");
```



## <a name="custom-draw-with-list-view-and-tree-view-controls"></a>Benutzerdefiniertes Zeichnen mit List-View und Tree-View Steuerelementen

Die gängigsten Steuerelemente können im Wesentlichen auf die gleiche Weise behandelt werden. Die Listenansicht-und Strukturansicht-Steuerelemente verfügen jedoch über einige Funktionen, die einen etwas anderen Ansatz für die benutzerdefinierte Zeichnung erfordern.

Bei [Version 5,0](common-control-versions.md)können diese beiden Steuerelemente den ausgeschnittenen Text anzeigen, wenn Sie die Schriftart ändern, indem Sie [**cdrf \_ newFont**](cdrf-constants.md)zurückgeben. Dieses Verhalten ist aus Gründen der Abwärtskompatibilität mit früheren Versionen der allgemeinen Steuerelemente erforderlich. Wenn Sie die Schriftart einer Listenansicht oder eines Strukturansicht-Steuer Elements ändern möchten, erhalten Sie bessere Ergebnisse, wenn Sie eine ccm- [**\_ setVersion**](ccm-setversion.md) -Nachricht mit dem *wParam* -Wert 5 senden, bevor Sie dem Steuerelement Elemente hinzufügen. Ein Beispiel für ein Strukturansicht-Steuerelement, das benutzerdefiniertes Zeichnen verwendet, finden Sie im Knowledge Base-Artikel [Beispiel: custdtv veranschaulicht benutzerdefiniertes Zeichnen in einer TreeView (Q248496)]( https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496).

### <a name="custom-draw-with-list-view-controls"></a>Benutzerdefiniertes Zeichnen mit List-View Steuerelementen

Da Listenansicht-Steuerelemente über unter Elemente und mehrere Anzeigemodi verfügen, müssen Sie die [nm \_ customdraw](nm-customdraw.md) -Benachrichtigung etwas anders behandeln als bei den anderen allgemeinen Steuerelementen.

Verwenden Sie für den Berichtsmodus das folgende Verfahren.

1.  In der ersten [nm- \_ customdraw](nm-customdraw.md) -Benachrichtigung wird der **dwdrawstage** -Member der zugeordneten [**nmcustomdraw**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) -Struktur auf CDDs \_ PrePaint festgelegt. Gibt [**cdrf \_ notityyitemdraw**](cdrf-constants.md)zurück.
2.  Sie erhalten dann eine [nm \_ customdraw](nm-customdraw.md) -Benachrichtigung, bei der **dwdrawstage** auf CDDs \_ itemprepaint festgelegt ist. Wenn Sie neue Schriftarten oder Farben angeben und [**cdrf \_ newFont**](cdrf-constants.md)zurückgeben, werden alle unter Elemente des Elements geändert. Wenn Sie stattdessen jedes Unterelement separat behandeln möchten, geben Sie [**cdrf \_ notifysubitemdraw**](cdrf-constants.md)zurück.
3.  Wenn Sie im vorherigen Schritt [**cdrf \_ notifysubitemdraw**](cdrf-constants.md) zurückgegeben haben, erhalten Sie eine [nm \_ customdraw](nm-customdraw.md) -Benachrichtigung für jedes Unterelement, wobei **dwdrawstage** auf CDDs \_ Unterelement \| CDDs \_ itemprepaint festgelegt ist. Wenn Sie die Schriftart oder Farbe für dieses Unterelement ändern möchten, geben Sie eine neue Schriftart oder Farbe an, und geben Sie [**cdrf \_ newFont**](cdrf-constants.md)zurück.

Verwenden Sie das folgende Verfahren für große Symbole, kleine Symbole und Listen Modi.

1.  In der ersten [nm- \_ customdraw](nm-customdraw.md) -Benachrichtigung wird der **dwdrawstage** -Member der zugeordneten [**nmcustomdraw**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) -Struktur auf CDDs \_ PrePaint festgelegt. Gibt [**cdrf \_ notityyitemdraw**](cdrf-constants.md)zurück.
2.  Sie erhalten dann eine [nm \_ customdraw](nm-customdraw.md) -Benachrichtigung, bei der **dwdrawstage** auf CDDs \_ itemprepaint festgelegt ist. Sie können die Schriftarten oder Farben eines Elements ändern, indem Sie neue Schriftarten und Farben angeben und [**cdrf \_ newFont**](cdrf-constants.md)zurückgeben. Da diese Modi keine unter Elemente aufweisen, erhalten Sie keine zusätzlichen nm \_ customdraw-Benachrichtigungen.

Ein Beispiel für einen "List-View [nm \_ customdraw](nm-customdraw.md) "-Benachrichtigungs Handler finden [Sie unter Verwenden von benutzerdefiniertem zeichnen](using-custom-draw.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Verwenden benutzerdefinierter zeichnen](using-custom-draw.md)
</dt> <dt>

[Benutzerdefinierter Zeichnungs Verweis](custom-draw-reference.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[Beispiel: custdtv veranschaulicht benutzerdefiniertes Zeichnen in einer TreeView (Q248496)]( https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 