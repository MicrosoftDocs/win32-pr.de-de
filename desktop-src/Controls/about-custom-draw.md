---
title: Informationen zum benutzerdefinierten Zeichnen
description: Dieser Abschnitt enthält allgemeine Informationen zur benutzerdefinierten Zeichnen-Funktionalität und bietet eine konzeptionelle Übersicht darüber, wie eine Anwendung benutzerdefiniertes Zeichnen unterstützen kann.
ms.assetid: dd104661-1e0c-4569-9753-817bcded1894
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f4961d80c04f8fa570286666511c04b1208c940369cd13b836095b8899505de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119922490"
---
# <a name="about-custom-draw"></a>Informationen zum benutzerdefinierten Zeichnen

Dieser Abschnitt enthält allgemeine Informationen zur benutzerdefinierten Zeichnen-Funktionalität und bietet eine konzeptionelle Übersicht darüber, wie eine Anwendung benutzerdefiniertes Zeichnen unterstützen kann. Derzeit unterstützen die folgenden Steuerelemente benutzerdefinierte Zeichnen-Funktionen:

-   Headersteuerelemente
-   Steuerelemente für Listenansichten
-   Rebar-Steuerelemente
-   Symbolleisten-Steuerelemente
-   QuickInfo-Steuerelemente
-   Trackbar-Steuerelemente
-   Strukturansichtssteuerelemente

<!-- -->

-   [Informationen zu benutzerdefinierten Draw-Benachrichtigungsmeldungen](#about-custom-draw-notification-messages)
-   [Paint Zyklen, Zeichnungsphasen und Benachrichtigungsmeldungen](#paint-cycles-drawing-stages-and-notification-messages)
-   [Nutzen benutzerdefinierter Draw-Dienste](#taking-advantage-of-custom-draw-services)
    -   [Reagieren auf die Präpaintbenachrichtigung](#responding-to-the-prepaint-notification)
    -   [Anfordern elementspezifischer Benachrichtigungen](#requesting-item-specific-notifications)
    -   [Zeichnen des Elements selbst](#drawing-the-item-yourself)
    -   [Ändern von Schriftarten und Farben](#changing-fonts-and-colors)
-   [Benutzerdefiniertes Zeichnen mit List-View und Tree-View Steuerelementen](#custom-draw-with-list-view-and-tree-view-controls)
    -   [Benutzerdefiniertes Zeichnen mit List-View Steuerelementen](#custom-draw-with-list-view-controls)
-   [Zugehörige Themen](#related-topics)

## <a name="about-custom-draw-notification-messages"></a>Informationen zu benutzerdefinierten Draw-Benachrichtigungsmeldungen

Alle gängigen Steuerelemente, die benutzerdefiniertes Zeichnen unterstützen, [senden NM \_ CUSTOMDRAW-Benachrichtigungscodes](nm-customdraw.md) an bestimmten Punkten während Zeichnungsvorgängen. Diese Benachrichtigungscodes beschreiben Zeichnungsvorgänge, die für das gesamte Steuerelement gelten, sowie Zeichnungsvorgänge, die für Elemente innerhalb des Steuerelements spezifisch sind. Wie viele Benachrichtigungscodes werden NM \_ CUSTOMDRAW-Benachrichtigungen als [**WM \_ NOTIFY-Nachrichten**](wm-notify.md) gesendet.

Der *lParam-Parameter* einer benutzerdefinierten Zeichnen-Benachrichtigung ist die Adresse einer [**NMCUSTOMDRAW-Struktur**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) oder einer steuerelementspezifischen Struktur, die eine **NMCUSTOMDRAW-Struktur** als ersten Member enthält. Die folgende Tabelle veranschaulicht die Beziehung zwischen den Steuerelementen und den strukturen, die sie verwenden.



| Struktur                                | Verwendet von                              |
|------------------------------------------|--------------------------------------|
| [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw)     | Rebar-, Trackbar- und Header-Steuerelemente |
| [**NMLVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmlvcustomdraw) | Steuerelemente für Listenansichten                   |
| [**NMTBCUSTOMDRAW**](/windows/desktop/api/Commctrl/ns-commctrl-nmtbcustomdraw) | Symbolleisten-Steuerelemente                     |
| [**NMTTCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmttcustomdraw) | QuickInfo-Steuerelemente                     |
| [**NMTVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) | Strukturansichtssteuerelemente                   |



 

## <a name="paint-cycles-drawing-stages-and-notification-messages"></a>Paint Zyklen, Zeichnungsphasen und Benachrichtigungsmeldungen

Wie bei Windows Anwendungen zeichnen und löschen sich allgemeine Steuerelemente in regelmäßigen Abständen auf der Grundlage von Nachrichten, die vom System oder anderen Anwendungen empfangen werden. Der Prozess des Zeichnens oder Löschens eines Steuerelements selbst wird als *Farbzyklus bezeichnet.* Steuerelemente, die benutzerdefiniertes Zeichnen unterstützen, senden in regelmäßigen Abständen [NM \_ CUSTOMDRAW-Benachrichtigungscodes](nm-customdraw.md) über jeden Farbzyklus. Dieser Benachrichtigungscode wird von einer [**NMCUSTOMDRAW-Struktur**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) oder einer anderen Struktur begleitet, die eine **NMCUSTOMDRAW-Struktur** als ersten Member enthält.

Eine Information, die die [**NMCUSTOMDRAW-Struktur**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) enthält, ist die aktuelle Phase des Farbzyklus. Dies wird als Zeichnen-Phase *bezeichnet* und durch den Wert im **dwDrawStage-Member der -Struktur** dargestellt. Ein Steuerelement informiert sein übergeordnetes Element über vier grundlegende Zeichnen-Phasen. Diese grundlegenden oder globalen Zeichnen-Phasen werden in der Struktur durch die folgenden Flagwerte dargestellt (definiert in Commctrl.h).



| Globale Werte für die Zeichnen-Phase | BESCHREIBUNG                        |
|--------------------------|------------------------------------|
| CDDS \_ PREPAINT           | Bevor der Farbzyklus beginnt.     |
| CDDS \_ POSTPAINT          | Nach Abschluss des Farbzyklus. |
| \_CDDS-VORABVERSION           | Bevor der Löschzyklus beginnt.     |
| CDDS \_ POSTERASE          | Nach Abschluss des Löschzyklus. |



 

Jeder der oben genannten Werte kann mit dem CDDS ITEM-Flag kombiniert werden, um für \_ Elemente spezifische Zeichnen-Phasen anzugeben. Commctrl.h enthält der Einfachheit halber die folgenden elementspezifischen Werte.



| Elementspezifische Werte für die Zeichnen-Phase | BESCHREIBUNG                                                                                                                                                                                                                                                                         |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CDDS \_ ITEMPREPAINT              | Bevor ein Element gezeichnet wird.                                                                                                                                                                                                                                                            |
| CDDS \_ ITEMPOSTPAINT             | Nachdem ein Element gezeichnet wurde.                                                                                                                                                                                                                                                       |
| CDDS \_ ITEMPREERASE              | Bevor ein Element gelöscht wird.                                                                                                                                                                                                                                                           |
| CDDS \_ ITEMPOSTERASE             | Nachdem ein Element gelöscht wurde.                                                                                                                                                                                                                                                      |
| \_CDDS-UNTERITEM                   | [Allgemeine Steuerelementversionen](common-control-versions.md) 4.71. Flag in Kombination mit CDDS \_ ITEMPREPAINT oder CDDS \_ ITEMPOSTPAINT, wenn ein Unterelement gezeichnet wird. Dies wird nur festgelegt, wenn [**CDRF \_ NOTIFYITEMDRAW**](cdrf-constants.md) von CDDS \_ PREPAINT zurückgegeben wird. |



 

Ihre Anwendung muss den [NM \_ CUSTOMDRAW-Benachrichtigungscode](nm-customdraw.md) verarbeiten und dann einen bestimmten Wert zurückgeben, der das Steuerelement darüber informiert, was es tun muss. Weitere Informationen zu diesen Rückgabewerten finden Sie in den folgenden Abschnitten.

## <a name="taking-advantage-of-custom-draw-services"></a>Nutzen benutzerdefinierter Draw-Dienste

Der Schlüssel zur Nutzung benutzerdefinierter Zeichnen-Funktionen besteht in der Reaktion auf die [NM CUSTOMDRAW-Benachrichtigungscodes, \_ ](nm-customdraw.md) die ein Steuerelement sendet. Die Rückgabewerte, die Ihre Anwendung als Antwort auf diese Benachrichtigungen sendet, bestimmen das Verhalten des Steuerelements für diesen Farbzyklus.

Dieser Abschnitt enthält Informationen dazu, wie Ihre Anwendung [NM CUSTOMDRAW-Benachrichtigungs-Rückgabewerte \_ ](nm-customdraw.md) verwenden kann, um das Verhalten des Steuerelements zu bestimmen.

Die Details sind in die folgenden Themen aufgeschlüsselt:

-   [Reagieren auf die Präpaintbenachrichtigung](#responding-to-the-prepaint-notification)
-   [Anfordern elementspezifischer Benachrichtigungen](#requesting-item-specific-notifications)
-   [Zeichnen des Elements selbst](#drawing-the-item-yourself)
-   [Ändern von Schriftarten und Farben](#changing-fonts-and-colors)

### <a name="responding-to-the-prepaint-notification"></a>Reagieren auf die Präpaintbenachrichtigung

Am Anfang jedes Farbzyklus sendet das Steuerelement den [NM \_ CUSTOMDRAW-Benachrichtigungscode](nm-customdraw.md) und gibt den CDDS \_ PREPAINT-Wert im **dwDrawStage-Member** der zugehörigen NM \_ CUSTOMDRAW-Struktur an. Der Wert, den Ihre Anwendung an diese erste Benachrichtigung zurückgibt, bestimmt, wie und wann das Steuerelement nachfolgende benutzerdefinierte Zeichnen-Benachrichtigungen für den Rest dieses Farbzyklus sendet. Ihre Anwendung kann als Reaktion auf die erste Benachrichtigung eine Kombination der folgenden Flags zurückgeben.



| Rückgabewert            | Wirkung                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CDRF \_ DODEFAULT         | Das Steuerelement wird sich selbst zeichnen. Es werden keine [zusätzlichen NM \_ CUSTOMDRAW-Benachrichtigungen](nm-customdraw.md) für diesen Farbzyklus gesendet. Dieses Flag kann nicht mit einem anderen Flag verwendet werden.                                                                                                                                                                                                                                                                               |
| CDRF \_ DOERASE           | Das Steuerelement zeichnen nur den Hintergrund.                                                                                                                                                                                                                                                                                                                                                                                                                    |
| CDRF \_ NEWFONT           | Ihre Anwendung hat eine neue Schriftart für das Element angegeben. Das -Steuerelement verwendet die neue Schriftart. Weitere Informationen zum Ändern von Schriftarten finden Sie unter [Ändern von Schriftarten und Farben.](#changing-fonts-and-colors) Dies tritt auf, **wenn dwDrawStage** gleich CDDS \_ ITEMPREPAINT ist.                                                                                                                                                                                                       |
| CDRF \_ NOTIFYITEMDRAW    | Das -Steuerelement benachrichtigt das übergeordnete Element über elementspezifische Zeichnungsvorgänge. Sie sendet [NM \_ CUSTOMDRAW-Benachrichtigungscodes](nm-customdraw.md) vor und nach dem Zeichnet von Elementen. Dies tritt auf, **wenn dwDrawStage** gleich CDDS \_ PREPAINT ist.                                                                                                                                                                                                                       |
| CDRF \_ NOTIFYPOSTERASE   | Das -Steuerelement benachrichtigt das übergeordnete Element nach dem Löschen eines Elements. Dies tritt auf, **wenn dwDrawStage** gleich CDDS \_ PREPAINT ist.                                                                                                                                                                                                                                                                                                                                             |
| CDRF \_ NOTIFYPOSTPAINT   | Das Steuerelement sendet eine [NM \_ CUSTOMDRAW-Benachrichtigung,](nm-customdraw.md) wenn der Malzyklus für das gesamte Steuerelement abgeschlossen ist. Dies tritt auf, **wenn dwDrawStage** gleich CDDS \_ PREPAINT ist.                                                                                                                                                                                                                                                                 |
| CDRF \_ NOTIFYSUBITEMDRAW | [Version 4.71](common-control-versions.md). Ihre Anwendung erhält eine [NM \_ CUSTOMDRAW-Benachrichtigung,](nm-customdraw.md) bei der **dwDrawStage** auf CDDS ITEMPREPAINT CDDS SUBITEM festgelegt ist, bevor jedes \_ Listenansichtsunterelement \| \_ gezeichnet wird. Anschließend können Sie Schriftart und Farbe für jedes Unterem separat angeben oder [**CDRF \_ DODEFAULT**](cdrf-constants.md) für die Standardverarbeitung zurückgeben. Dies tritt auf, **wenn dwDrawStage** gleich CDDS \_ ITEMPREPAINT ist. |
| CDRF \_ SKIPDEFAULT       | Ihre Anwendung hat das Element manuell geerbt. Das -Steuerelement zeichnen das Element nicht. Dies tritt auf, **wenn dwDrawStage** gleich CDDS \_ ITEMPREPAINT ist.                                                                                                                                                                                                                                                                                                                      |
| CDRF \_ SKIPPOSTPAINT     | Das Steuerelement zeichnen das Fokusrechteck um ein Element nicht.                                                                                                                                                                                                                                                                                                                                                                                                 |



 

### <a name="requesting-item-specific-notifications"></a>Anfordern elementspezifischer Benachrichtigungen

Wenn Ihre Anwendung [**CDRF \_ NOTIFYITEMDRAW**](cdrf-constants.md) an die anfängliche benutzerdefinierte Zeichnen-Benachrichtigung für präpaint zurückgibt, sendet das Steuerelement Benachrichtigungen für jedes Element, das während dieses Farbzyklus ge zeichnet wird. Diese elementspezifischen Benachrichtigungen verfügen über den CDDS \_ ITEMPREPAINT-Wert im **dwDrawStage-Element** der [**zugehörigen NMCUSTOMDRAW-Struktur.**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) Sie können anfordern, dass das Steuerelement eine weitere Benachrichtigung sendet, wenn das Zeichnen des Elements abgeschlossen ist, indem [**Sie CDRF \_ NOTIFYPOSTPAINT**](cdrf-constants.md) an diese elementspezifischen Benachrichtigungen zurückgeben. Andernfalls geben [**Sie CDRF \_ DODEFAULT zurück,**](cdrf-constants.md) und das Steuerelement benachrichtigt das übergeordnete Fenster erst, wenn es mit dem Zeichnen des nächsten Elements beginnt.

### <a name="drawing-the-item-yourself"></a>Zeichnen des Elements selbst

Wenn Ihre Anwendung das gesamte Element zeichnet, geben [**Sie CDRF \_ SKIPDEFAULT zurück.**](cdrf-constants.md) Dadurch kann das Steuerelement Elemente überspringen, die es nicht zeichnen muss, wodurch der Systemaufwand verringert wird. Beachten Sie, dass die Rückgabe dieses Werts bedeutet, dass das Steuerelement keinen Teil des Elements zeichnen wird.

### <a name="changing-fonts-and-colors"></a>Ändern von Schriftarten und Farben

Ihre Anwendung kann das benutzerdefinierte Zeichnen verwenden, um die Schriftart eines Elements zu ändern. Wählen Sie einfach das HFONT aus, das Sie in dem Gerätekontext auswählen möchten, der vom **hdc-Member** der [**NMCUSTOMDRAW-Struktur**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) angegeben wird, die der benutzerdefinierten Zeichnen-Benachrichtigung zugeordnet ist. Da die schriftart, die Sie auswählen, möglicherweise andere Metriken als die Standardschriftart auft, stellen Sie sicher, dass Sie das [**CDRF \_ NEWFONT-Bit**](cdrf-constants.md) in den Rückgabewert für die Benachrichtigungsmeldung einwählen. Weitere Informationen zur Verwendung dieser Funktion finden Sie im Beispielcode unter [Verwenden von Custom Draw](using-custom-draw.md). Die Schriftart, die ihre Anwendung angibt, wird verwendet, um dieses Element anzuzeigen, wenn es nicht ausgewählt ist. Beim benutzerdefinierten Zeichnen können Sie die Schriftartattribute für ausgewählte Elemente nicht ändern.

Um Textfarben für alle Steuerelemente zu ändern, die benutzerdefiniertes Zeichnen unterstützen, mit Ausnahme der Listenansicht und Strukturansicht, legen Sie einfach den gewünschten Text und die gewünschten Hintergrundfarben im Gerätekontext fest, der in der benutzerdefinierten Draw-Benachrichtigungsstruktur mit den [**Funktionen SetTextColor**](/windows/desktop/api/wingdi/nf-wingdi-settextcolor) und [**SetBkColor**](/windows/desktop/api/wingdi/nf-wingdi-setbkcolor) bereitgestellt wird. Um die Textfarben in der Listenansicht oder Strukturansicht zu ändern, müssen Sie die gewünschten Farbwerte in den **ClrText-** und **clrTextBk-Membern** der [**NMLVCUSTOMDRAW-**](/windows/win32/api/commctrl/ns-commctrl-nmlvcustomdraw) oder [**NMTVCUSTOMDRAW-Struktur**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) platzieren.

> [!Note]  
> Vor Version [6.0 der](common-control-versions.md) allgemeinen Steuerelemente ignorieren Symbolleisten das [**CDRF \_ NEWFONT-Flag.**](cdrf-constants.md) Version 6.0 unterstützt das **CDRF \_ NEWFONT-Flag,** und Sie können es verwenden, um eine andere Schriftart für die Symbolleiste auszuwählen. Sie können die Farbe einer Symbolleiste jedoch nicht ändern, wenn ein visueller Stil aktiv ist. Um die Farbe einer Symbolleiste in Version 6.0 zu ändern, müssen Sie zuerst visuelle Stile deaktivieren, indem Sie [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) aufrufen und keinen visuellen Stil angeben:

 


```
SetWindowTheme (hwnd, "", "");
```



## <a name="custom-draw-with-list-view-and-tree-view-controls"></a>Benutzerdefiniertes Zeichnen mit List-View und Tree-View Steuerelementen

Die meisten gängigen Steuerelemente können im Wesentlichen auf die gleiche Weise behandelt werden. Die Steuerelemente für Listenansichten und Strukturansichten verfügen jedoch über einige Features, die einen etwas anderen Ansatz für das benutzerdefinierte Zeichnen erfordern.

Für [Version 5.0 können](common-control-versions.md)diese beiden Steuerelemente abgeschnittenen Text anzeigen, wenn Sie die Schriftart ändern, indem Sie [**CDRF \_ NEWFONT zurückgeben.**](cdrf-constants.md) Dieses Verhalten ist aus Gründen der Abwärtskompatibilität mit früheren Versionen der allgemeinen Steuerelemente erforderlich. Wenn Sie die Schriftart eines Listenansichts- oder Strukturansicht-Steuerelements ändern möchten, erhalten Sie bessere Ergebnisse, wenn Sie eine [**CCM \_ SETVERSION-Nachricht**](ccm-setversion.md) senden, bei der der *wParam-Wert* auf 5 festgelegt ist, bevor Sie dem Steuerelement Elemente hinzufügen. Ein Beispiel für ein Strukturansicht-Steuerelement, das benutzerdefiniertes Zeichnen verwendet, finden Sie im Knowledge Base-Artikel [SAMPLE: CustDTv Illustrates Custom Draw in a TreeView (Q248496) .]( https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)

### <a name="custom-draw-with-list-view-controls"></a>Benutzerdefiniertes Zeichnen mit List-View Steuerelementen

Da Listenansichtssteuerelemente Unterelemente und mehrere Anzeigemodi aufweisen, müssen Sie die [NM \_ CUSTOMDRAW-Benachrichtigung](nm-customdraw.md) etwas anders behandeln als für die anderen gängigen Steuerelemente.

Verwenden Sie für den Berichtsmodus das folgende Verfahren.

1.  Bei der ersten [NM \_ CUSTOMDRAW-Benachrichtigung](nm-customdraw.md) ist **das dwDrawStage-Member** der zugeordneten [**NMCUSTOMDRAW-Struktur**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) auf CDDS \_ PREPAINT festgelegt. Gibt [**CDRF \_ NOTIFYITEMDRAW zurück.**](cdrf-constants.md)
2.  Anschließend erhalten Sie eine [NM \_ CUSTOMDRAW-Benachrichtigung,](nm-customdraw.md) bei der **dwDrawStage** auf CDDS \_ ITEMPREPAINT festgelegt ist. Wenn Sie neue Schriftarten oder Farben angeben und [**CDRF \_ NEWFONT**](cdrf-constants.md)zurückgeben, werden alle Unteritems des Elements geändert. Wenn Sie stattdessen jedes Unterem separat behandeln möchten, geben Sie [**CDRF \_ NOTIFYSUBITEMDRAW zurück.**](cdrf-constants.md)
3.  Wenn Sie im vorherigen Schritt [**CDRF \_ NOTIFYSUBITEMDRAW**](cdrf-constants.md) zurückgegeben haben, erhalten Sie eine [NM \_ CUSTOMDRAW-Benachrichtigung](nm-customdraw.md) für jedes Unterelement, bei dem **dwDrawStage** auf CDDS \_ SUBITEM \| CDDS \_ ITEMPREPAINT festgelegt ist. Um die Schriftart oder Farbe für dieses Unterem zu ändern, geben Sie eine neue Schriftart oder Farbe an und geben [**CDRF \_ NEWFONT zurück.**](cdrf-constants.md)

Verwenden Sie für die Modi "Großes Symbol", "Kleines Symbol" und "Liste" das folgende Verfahren.

1.  Bei der ersten [NM \_ CUSTOMDRAW-Benachrichtigung](nm-customdraw.md) ist **das dwDrawStage-Member** der zugeordneten [**NMCUSTOMDRAW-Struktur**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) auf CDDS \_ PREPAINT festgelegt. Gibt [**CDRF \_ NOTIFYITEMDRAW zurück.**](cdrf-constants.md)
2.  Anschließend erhalten Sie eine [NM \_ CUSTOMDRAW-Benachrichtigung,](nm-customdraw.md) bei der **dwDrawStage** auf CDDS \_ ITEMPREPAINT festgelegt ist. Sie können die Schriftarten oder Farben eines Elements ändern, indem Sie neue Schriftarten und Farben angeben und [**CDRF \_ NEWFONT zurückgeben.**](cdrf-constants.md) Da diese Modi keine Unteritems aufweisen, erhalten Sie keine zusätzlichen NM \_ CUSTOMDRAW-Benachrichtigungen.

Ein Beispiel für einen NM [ \_ CUSTOMDRAW-Benachrichtigungshandler](nm-customdraw.md) für Listenansichten finden Sie unter [Verwenden von Custom Draw](using-custom-draw.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Verwenden von benutzerdefiniertem Zeichnen](using-custom-draw.md)
</dt> <dt>

[Benutzerdefinierter Draw-Verweis](custom-draw-reference.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[BEISPIEL: CustDTv veranschaulicht benutzerdefiniertes Zeichnen in einer TreeView (Q248496)]( https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 