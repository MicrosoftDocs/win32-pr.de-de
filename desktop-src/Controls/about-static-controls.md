---
title: Informationen zu statischen Steuerelementen
description: In diesem Thema wird erläutert, wie statische Steuerelemente verwendet werden.
ms.assetid: 155904e1-a963-496d-9b22-6e95ed0ebd47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 064c1814b4f4ed6283b2fe22af06aed107e2c4d2
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103949157"
---
# <a name="about-static-controls"></a>Informationen zu statischen Steuerelementen

Anwendungen verwenden häufig statische Steuerelemente, um andere Steuerelemente zu bezeichnen oder eine Gruppe von Steuerelementen voneinander zu trennen. Obwohl statische Steuerelemente untergeordnete Fenster sind, können Sie nicht ausgewählt werden. Daher können Sie keinen Tastaturfokus erhalten und können keine Tastaturschnittstelle haben. Ein statisches Steuerelement, das den SS- \_ Benachrichtigungs Stil hat, empfängt Maus Eingaben und benachrichtigt das übergeordnete Fenster, wenn der Benutzer auf das Steuerelement klickt oder doppelklickt. Statische Steuerelemente gehören zur statischen Fenster Klasse.

Statische Steuerelemente können zwar in überlappenden, Popup-und untergeordneten Fenstern verwendet werden, Sie sind jedoch für die Verwendung in Dialogfeldern konzipiert, in denen das System Ihr Verhalten standardisiert. Durch die Verwendung von statischen Steuerelementen außerhalb von Dialogfeldern erhöht ein Entwickler das Risiko, dass sich die Anwendung möglicherweise nicht standardmäßig verhält. In der Regel verwendet ein Entwickler entweder statische Steuerelemente in Dialogfeldern oder verwendet den SS-Besitzer \_ Zeichnungs Stil, um angepasste statische Steuerelemente zu erstellen.

Die folgenden Themen werden in diesem Abschnitt erläutert.

-   [Statische Steuerelement Typen](#static-control-types)
    -   [Statisches Steuerelement für einfache Grafiken](#simple-graphics-static-control)
    -   [Statisches Text Steuerelement](#text-static-control)
    -   [Bild statisches Steuerelement](#image-static-control)
    -   [Vom Besitzer gezeichnetes Steuerelement](#owner-drawn-static-control)
-   [Standard Nachrichtenverarbeitung für statisches Steuerelement](#static-control-default-message-processing)

## <a name="static-control-types"></a>Statische Steuerelement Typen

Es gibt vier Typen von statischen Steuerelementen. Jeder Typ verfügt über mindestens einen [statischen Steuerelement Stil](static-control-styles.md).

-   [Statisches Steuerelement für einfache Grafiken](#simple-graphics-static-control)
-   [Statisches Text Steuerelement](#text-static-control)
-   [Bild statisches Steuerelement](#image-static-control)
-   [Vom Besitzer gezeichnetes Steuerelement](#owner-drawn-static-control)

### <a name="simple-graphics-static-control"></a>Statisches Steuerelement für einfache Grafiken

Ein einfaches grafisches Grafik Steuerelement zeigt einen Frame oder ein ausgefülltes Rechteck an. Ein Frame kann in einer Reihe von Stilen gezeichnet werden, die schwarz, grau oder weiß enthalten. Außerdem kann ein Frame mit einem geätzten Stil gezeichnet werden, um ihm eine dreidimensionale Darstellung zu geben. Die Frame Stile umfassen SS \_ BlackFrame, SS \_ grayframe, SS \_ whiteframe, SS \_ etchedhorz, SS \_ etchedvert und SS \_ etchedframe.

Ein Rechteck kann mit einer Farbe in einem von drei Stilen gefüllt werden: schwarz, grau oder weiß. Diese Stile werden von den konstanten SS \_ blackrect, SS \_ grayrect und SS \_ whiteRect definiert.

Die Grafikstile können nicht kombiniert werden.

### <a name="text-static-control"></a>Statisches Text Steuerelement

Ein statisches Text-Steuerelement zeigt Text in einem Rechteck in einem von fünf Stilen an:

-   linksbündig ohne Zeilenumbruch
-   linksbündig mit Zeilenumbruch
-   zentriert
-   rechtsbündig
-   Einfach

Diese Stile werden von den konstanten SS \_ leftnowordwrap, SS \_ left, SS \_ Center, SS \_ right und SS Simple definiert \_ . Das System ordnet den Text in diesen Steuerelementen auf vordefinierte Weise neu an, mit Ausnahme des "einfachen" Texts, der nicht neu angeordnet wird.

Eine Anwendung kann den Text in einem statischen Text Steuerelement jederzeit mithilfe der [**SetWindowText**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta) -Funktion oder der WM- [**\_ SetText**](/windows/desktop/winmsg/wm-settext) -Nachricht ändern.

Das System zeigt so viel Text wie möglich im statischen Steuerelement an und schneidet, was nicht passt. Um eine geeignete Größe für das Steuerelement zu berechnen, rufen Sie die Schriftart Metrik für den Text ab. Weitere Informationen zu Schriftarten und Schriftart Metriken finden Sie unter [Schriftarten und Text](/windows/desktop/gdi/fonts-and-text).

Standardmäßig kann der Fenster Text für ein statisches Steuerelement, wie bei anderen Steuerelementen, ein kaufmännisches und-Element enthalten, das das folgende Zeichen als Tastenkombination für das Steuerelement definiert (oder im Fall der meisten statischen Steuerelemente für das Steuerelement, das es bezeichnet, das das nächste Steuerelement in der Aktivier Reihenfolge ist). Wenn Sie kaufmännisches Zeichen im Text anzeigen möchten, anstatt diese zum Definieren von Verknüpfungen zu verwenden, fügen Sie den SS \_ NoPrefix-Stil ein.

### <a name="image-static-control"></a>Bild statisches Steuerelement

Ein statisches Bild Steuerelement kann Bitmaps, Symbole (einschließlich animierter Symbole) oder Erweiterte Metadateien anzeigen. Der Typ der Grafik, den ein bestimmtes statisches Steuerelement anzeigt, hängt von der Art des Steuer Elements ab: SS \_ Bitmap, SS \_ Icon oder SS \_ enhmetafile. Eine Anwendung gibt den Stil an, wenn das Steuerelement erstellt wird, und gibt auch ein Handle für die Bitmap, das Symbol oder die Metadatendatei an, die das Steuerelement anzeigen soll. Nachdem das Steuerelement erstellt wurde, kann eine Anwendung dem Steuerelement eine andere Grafik zuordnen, indem Sie eine [**STM \_ SetImage**](stm-setimage.md) -Nachricht sendet, die ein Handle für das neue Grafik Objekt angibt. Eine Anwendung kann ein Handle für das Grafik Objekt abrufen, das einem statischen Steuerelement derzeit zugeordnet ist, indem es eine [**STM \_ GetImage**](stm-getimage.md) -Nachricht sendet. Eine Anwendung sendet Nachrichten mithilfe der [**SendDlgItemMess**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea) -Funktion an ein statisches-Steuerelement.

### <a name="owner-drawn-static-control"></a>Owner-Drawn statisches Steuerelement

Wenn Sie den SS-Besitzer \_ Zeichnen-Stil verwenden, kann eine Anwendung die Verantwortung für das Zeichnen eines statischen Steuer Elements übernehmen. Das übergeordnete Fenster eines von einem Besitzer gezeichneten statischen Steuer Elements (dessen Besitzer) empfängt immer dann eine [**WM \_ DrawItem**](wm-drawitem.md) -Nachricht, wenn das statische Steuerelement gezeichnet werden muss. Die Meldung enthält einen Zeiger auf eine [**drawitemstruct**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) -Struktur, die Informationen enthält, die das Besitzer Fenster beim Zeichnen des Steuer Elements verwendet.

## <a name="static-control-default-message-processing"></a>Standard Nachrichtenverarbeitung für statisches Steuerelement

Die Fenster Prozedur für die vordefinierte statische Steuerelement-Fenster Klasse führt die Standard Verarbeitung für alle Nachrichten aus, die von der statischen Steuerelement Prozedur nicht verarbeitet werden. Wenn das statische Steuerelement für jede Nachricht **false** zurückgibt, prüft die vordefinierte Fenster Prozedur die Nachrichten und führt die in der folgenden Tabelle beschriebene Standardaktion aus. In der-Tabelle ist ein statisches Text Steuerelement ein statisches Steuerelement mit dem Format SS \_ leftnowordwrap, SS \_ left, SS \_ Center, SS \_ right oder SS \_ Simple.



| `Message`                                                | Standardaktion                                                                                                                              |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ Erstellen**](/windows/desktop/winmsg/wm-create)                     | Lädt das Grafik Objekt und passt die Größe des Fensters auf die Größe des Objekts für grafische statische Steuerelemente an. Führt keine Aktion für andere statische Steuerelemente aus. |
| [**WM \_ zerstören**](/windows/desktop/winmsg/wm-destroy)                   | Gibt für grafische statische Steuerelemente ein beliebiges Grafik Objekt frei und zerstört dieses. Führt keine Aktion für andere statische Steuerelemente aus.                              |
| [**WM \_ aktivieren**](/windows/desktop/winmsg/wm-enable)                     | Zeichnet sichtbare statische Steuerelemente neu.                                                                                                           |
| [**WM- \_ erasebkgnd**](/windows/desktop/winmsg/wm-erasebkgnd)             | Gibt **true** zurück, um anzugeben, dass das Steuerelement den Hintergrund löscht.                                                                             |
| [**WM \_ getdlgcode**](/windows/desktop/dlgbox/wm-getdlgcode)             | Gibt "dlgc static" zurück \_ .                                                                                                                       |
| [**WM- \_ getFont**](/windows/desktop/winmsg/wm-getfont)                   | Gibt ein Handle für die Schriftart für statische Text Steuerelemente zurück.                                                                                      |
| [**WM \_ gettext**](/windows/desktop/winmsg/wm-gettext)                   | Gibt die Anzahl der kopierten Zeichen zurück.                                                                                                    |
| [**WM \_ getTextLength**](/windows/desktop/winmsg/wm-gettextlength)       | Gibt die Länge des Texts für ein statisches Text Steuerelement in Zeichen zurück.                                                                   |
| [**WM \_ lbuttondblclk**](/windows/desktop/inputdev/wm-lbuttondblclk)     | Sendet das übergeordnete Fenster einen [STN \_ dblclk](stn-dblclk.md) -Benachrichtigungs Code, wenn der Steuerelement Stil SS \_ Notify ist.                              |
| [**WM \_ lbuttondown**](/windows/desktop/inputdev/wm-lbuttondown)         | Sendet dem übergeordneten Fenster einen STN, auf den Sie [ \_ geklickt](stn-clicked.md) haben, wenn der Steuerelement Stil SS-Benachrichtigung ist \_ .                            |
| [**WM \_ nclbuttondblclk**](/windows/desktop/inputdev/wm-nclbuttondblclk) | Sendet das übergeordnete Fenster einen [STN \_ dblclk](stn-dblclk.md) -Benachrichtigungs Code, wenn der Steuerelement Stil SS \_ Notify ist.                              |
| [**WM- \_ nclbuttondown**](/windows/desktop/inputdev/wm-nclbuttondown)     | Sendet dem übergeordneten Fenster einen STN, auf den Sie [ \_ geklickt](stn-clicked.md) haben, wenn der Steuerelement Stil SS-Benachrichtigung ist \_ .                            |
| [**WM- \_ nchittest**](/windows/desktop/inputdev/wm-nchittest)             | Gibt "htclient" zurück, wenn der Steuerelement Stil "SS notify" ist \_ , andernfalls "httransparent".                                                      |
| [**WM- \_ Paint**](/windows/desktop/gdi/wm-paint)                          | Zeichnet das Steuerelement neu.                                                                                                                       |
| [**WM- \_ setFont**](/windows/desktop/winmsg/wm-setfont)                   | Legt die Schriftart und die Repaint für statische Text Steuerelemente fest.                                                                                        |
| [**WM- \_ SetText**](/windows/desktop/winmsg/wm-settext)                   | Legt den Text und die Repaint für statische Text Steuerelemente fest.                                                                                        |



 

Die vordefinierte Fenster Prozedur übergibt alle anderen Nachrichten zur Standard Verarbeitung an [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .

 

 