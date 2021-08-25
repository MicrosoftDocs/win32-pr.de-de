---
title: Informationen zu statischen Steuerelementen
description: In diesem Thema wird erläutert, wie statische Steuerelemente verwendet werden.
ms.assetid: 155904e1-a963-496d-9b22-6e95ed0ebd47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aa9b77ff7c1357cede494f60c1d345d0eb4b8f5f8cf63ace13176179d385794
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119922300"
---
# <a name="about-static-controls"></a>Informationen zu statischen Steuerelementen

Anwendungen verwenden häufig statische Steuerelemente, um andere Steuerelemente zu beschriften oder eine Gruppe von Steuerelementen zu trennen. Obwohl statische Steuerelemente untergeordnete Fenster sind, können sie nicht ausgewählt werden. Daher können sie den Tastaturfokus nicht erhalten und können keine Tastaturschnittstelle haben. Ein statisches Steuerelement mit dem Stil SS NOTIFY empfängt Mauseingaben und benachrichtigt das übergeordnete Fenster, wenn der Benutzer auf das Steuerelement klickt \_ oder doppelklickt. Statische Steuerelemente gehören zur STATIC-Fensterklasse.

Obwohl statische Steuerelemente in überlappenden, Popup- und untergeordneten Fenstern verwendet werden können, sind sie für die Verwendung in Dialogfeldern konzipiert, in denen das System ihr Verhalten standardisiert. Durch die Verwendung statischer Steuerelemente außerhalb von Dialogfeldern erhöht ein Entwickler das Risiko, dass sich die Anwendung auf nicht standardmäßige Weise verhält. In der Regel verwendet ein Entwickler statische Steuerelemente in Dialogfeldern oder den SS \_ OWNERDRAW-Stil, um benutzerdefinierte statische Steuerelemente zu erstellen.

Die folgenden Themen werden in diesem Abschnitt erläutert.

-   [Statische Steuerelementtypen](#static-control-types)
    -   [Einfaches statisches Grafiksteuer steuerelement](#simple-graphics-static-control)
    -   [Statisches Textsteuerfeld](#text-static-control)
    -   [Image Static Control](#image-static-control)
    -   [Vom Besitzer gezeichnetes statisches Steuerelement](#owner-drawn-static-control)
-   [Standardnachrichtenverarbeitung für statisches Steuerelement](#static-control-default-message-processing)

## <a name="static-control-types"></a>Statische Steuerelementtypen

Es gibt vier Arten von statischen Steuerelementen. Jeder Typ verfügt über mindestens einen [statischen Steuerelementstil.](static-control-styles.md)

-   [Einfaches statisches Grafiksteuer steuerelement](#simple-graphics-static-control)
-   [Statisches Textsteuerfeld](#text-static-control)
-   [Image Static Control](#image-static-control)
-   [Vom Besitzer gezeichnetes statisches Steuerelement](#owner-drawn-static-control)

### <a name="simple-graphics-static-control"></a>Einfaches statisches Grafiksteuer steuerelement

Ein einfaches statisches Grafiksteuer steuerelement zeigt einen Rahmen oder ein ausgefülltes Rechteck an. Ein Frame kann in einer Reihe von Stilen gezeichnet werden, z. B. schwarz, grau oder weiß. Darüber hinaus kann ein Rahmen mit einem geätzten Stil gezeichnet werden, um ihm ein dreidimensionales Aussehen zu verleihen. Die Rahmenformate umfassen SS \_ BLACKFRAME, SS \_ GRAYFRAME, SS \_ WHITEFRAME, SS \_ ETCHEDHORZ, SS \_ ETCHEDVERT und SS \_ ETCHEDFRAME.

Ein Rechteck kann in einem von drei Stilen mit Farbe gefüllt werden: schwarz, grau oder weiß. Diese Stile werden durch die Konstanten SS \_ BLACKRECT, SS \_ GRAYRECT und SS \_ WHITERECT definiert.

Die Grafikstile können nicht kombiniert werden.

### <a name="text-static-control"></a>Statisches Textsteuerfeld

Ein statisches Textsteuerfeld zeigt Text in einem Rechteck in einem von fünf Formaten an:

-   Linksbündig ohne Zeilenumbruch
-   Linksbündig mit Zeilenumbruch
-   zentriert
-   rechtsbündig
-   Einfach

Diese Stile werden durch die Konstanten SS \_ LEFTNOWORDWRAP, SS \_ LEFT, SS CENTER, SS RIGHT bzw. \_ \_ SS \_ SIMPLE definiert. Das System ordnet den Text in diesen Steuerelementen auf vordefinierte Weise neu an, mit Ausnahme von "einfachem" Text, der nicht neu angeordnet wird.

Eine Anwendung kann den Text in einem statischen Textsteuerfeld jederzeit mithilfe der [**SetWindowText-Funktion**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta) oder der [**WM \_ SETTEXT-Nachricht**](/windows/desktop/winmsg/wm-settext) ändern.

Das System zeigt so viel Text wie möglich im statischen Steuerelement an und clipt, was nicht passt. Um eine geeignete Größe für das Steuerelement zu berechnen, rufen Sie die Schriftartmetriken für den Text ab. Weitere Informationen zu Schriftarten und Schriftartmetriken finden Sie unter [Schriftarten und Text.](/windows/desktop/gdi/fonts-and-text)

Standardmäßig kann der Fenstertext für ein statisches Steuerelement, wie bei anderen Steuerelementen, ein ampersand-Zeichen enthalten, das das folgende Zeichen als Tastenkombination für das Steuerelement definiert (oder bei den meisten statischen Steuerelementen für das Steuerelement, das es bezeichnet, was das nächste Steuerelement in der Registerkarten reihenfolge ist). Wenn Sie ampersands im Text anzeigen möchten, anstatt sie zum Definieren von Verknüpfungen zu verwenden, schließen Sie den SS \_ NOPREFIX-Stil ein.

### <a name="image-static-control"></a>Image Static Control

Ein statisches Bildsteuer steuerelement kann Bitmaps, Symbole (einschließlich animierter Symbole) oder erweiterte Metadateien anzeigen. Der Typ der Grafik, die ein bestimmtes statisches Steuerelement anzeigt, hängt vom Stil des Steuerelements ab: SS \_ BITMAP, SS \_ ICON oder SS \_ ENHMETAFILE. Eine Anwendung gibt den Stil an, wenn sie das Steuerelement erstellt, und gibt auch ein Handle für die Bitmap, das Symbol oder die Metadatei für das anzuzeigende Steuerelement an. Nachdem das Steuerelement erstellt wurde, kann eine Anwendung dem Steuerelement eine andere Grafik zuordnen, indem ihm eine [**STM \_ SETIMAGE-Nachricht**](stm-setimage.md) gesendet wird, und ein Handle für das neue Grafikobjekt angeben. Eine Anwendung kann ein Handle für das Grafikobjekt abrufen, das derzeit einem statischen Steuerelement zugeordnet ist, indem sie ihm eine [**STM \_ GETIMAGE-Nachricht**](stm-getimage.md) sendet. Eine Anwendung sendet Nachrichten mithilfe der [**SendDlgItemMessage-Funktion**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea) an ein statisches Steuerelement.

### <a name="owner-drawn-static-control"></a>Owner-Drawn Statisches Steuerelement

Mithilfe des SS OWNERDRAW-Stils kann eine Anwendung die Verantwortung für \_ das Malen eines statischen Steuerelements übernehmen. Das übergeordnete Fenster eines vom Besitzer gezeichneten statischen Steuerelements (dessen Besitzer) empfängt immer dann eine [**WM \_ DRAWITEM-Meldung,**](wm-drawitem.md) wenn das statische Steuerelement gezeichnet werden muss. Die Meldung enthält einen Zeiger auf eine [**DRAWITEMSTRUCT-Struktur,**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) die Informationen enthält, die das Besitzerfenster beim Zeichnen des Steuerelements verwendet.

## <a name="static-control-default-message-processing"></a>Standardnachrichtenverarbeitung für statisches Steuerelement

Die Fensterprozedur für die vordefinierte statische Steuerelementfensterklasse führt die Standardverarbeitung für alle Nachrichten durch, die von der statischen Steuerelementprozedur nicht verarbeitet werden. Wenn das statische Steuerelement **FALSE für** jede Nachricht zurückgibt, überprüft die vordefinierte Fensterprozedur die Nachrichten und führt die in der folgenden Tabelle beschriebene Standardaktion aus. In der Tabelle ist ein statisches Textsteuerfeld ein statisches Steuerelement im Format SS \_ LEFTNOWORDWRAP, SS \_ LEFT, SS \_ CENTER, SS RIGHT oder \_ SS \_ SIMPLE.



| `Message`                                                | Standardaktion                                                                                                                              |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ CREATE**](/windows/desktop/winmsg/wm-create)                     | Lädt das Grafikobjekt und größe das Fenster für grafische statische Steuerelemente auf die Größe des Objekts. Führt keine Aktion für andere statische Steuerelemente aus. |
| [**WM \_ DESTROY**](/windows/desktop/winmsg/wm-destroy)                   | Gibt alle grafischen Objekte für grafische statische Steuerelemente frei und zerstört sie. Führt keine Aktion für andere statische Steuerelemente aus.                              |
| [**WM \_ ENABLE**](/windows/desktop/winmsg/wm-enable)                     | Gepaintt sichtbare statische Steuerelemente neu.                                                                                                           |
| [**WM \_ ERASEBKGND**](/windows/desktop/winmsg/wm-erasebkgnd)             | Gibt **TRUE zurück,** was angibt, dass das Steuerelement den Hintergrund löscht.                                                                             |
| [**WM \_ GETDLGCODE**](/windows/desktop/dlgbox/wm-getdlgcode)             | Gibt DLGC \_ STATIC zurück.                                                                                                                       |
| [**WM \_ GETFONT**](/windows/desktop/winmsg/wm-getfont)                   | Gibt ein Handle für die Schriftart für statische Textsteuerelemente zurück.                                                                                      |
| [**WM \_ GETTEXT**](/windows/desktop/winmsg/wm-gettext)                   | Gibt die Anzahl der kopierten Zeichen zurück.                                                                                                    |
| [**WM \_ GETTEXTLENGTH**](/windows/desktop/winmsg/wm-gettextlength)       | Gibt die Länge des Texts für ein statisches Textsteuerfeld in Zeichen zurück.                                                                   |
| [**WM \_ LBUTTONDBLCLK**](/windows/desktop/inputdev/wm-lbuttondblclk)     | Sendet dem übergeordneten Fenster einen [STN \_ DBLCLK-Benachrichtigungscode,](stn-dblclk.md) wenn der Steuerelementstil SS \_ NOTIFY ist.                              |
| [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown)         | Sendet dem übergeordneten Fenster einen [STN \_ CLICKED-Benachrichtigungscode,](stn-clicked.md) wenn der Steuerelementstil SS \_ NOTIFY ist.                            |
| [**WM \_ NCLBUTTONDBLCLK**](/windows/desktop/inputdev/wm-nclbuttondblclk) | Sendet dem übergeordneten Fenster einen [STN \_ DBLCLK-Benachrichtigungscode,](stn-dblclk.md) wenn der Steuerelementstil SS \_ NOTIFY ist.                              |
| [**WM \_ NCLBUTTONDOWN**](/windows/desktop/inputdev/wm-nclbuttondown)     | Sendet dem übergeordneten Fenster einen [STN \_ CLICKED-Benachrichtigungscode,](stn-clicked.md) wenn der Steuerelementstil SS \_ NOTIFY ist.                            |
| [**WM \_ NCHITTEST**](/windows/desktop/inputdev/wm-nchittest)             | Gibt HTCLIENT zurück, wenn der Steuerelementstil SS \_ NOTIFY ist. Andernfalls wird HTTRANSPARENT zurückgegeben.                                                      |
| [**WM \_ PAINT**](/windows/desktop/gdi/wm-paint)                          | Das Steuerelement wird neu gepaint.                                                                                                                       |
| [**WM \_ SETFONT**](/windows/desktop/winmsg/wm-setfont)                   | Legt die Schriftart und die Neupaints für statische Textsteuerelemente fest.                                                                                        |
| [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext)                   | Legt den Text und die Neupaints für statische Textsteuerelemente fest.                                                                                        |



 

Die vordefinierte Fensterprozedur übergibt alle anderen Nachrichten zur Standardverarbeitung [**an DefWindowProc.**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)

 

 