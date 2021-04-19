---
title: Status leisten (Windows-Steuerelemente)
description: Eine Statusleiste ist ein horizontales Fenster am unteren Rand eines übergeordneten Fensters, in dem eine Anwendung verschiedene Arten von Statusinformationen anzeigen kann.
ms.assetid: vs|controls|~\controls\status\status.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c2d1130b25cf0dc6373021e063210b765aa34a5
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106342175"
---
# <a name="status-bars-windows-controls"></a>Status leisten (Windows-Steuerelemente)

Eine *Statusleiste* ist ein horizontales Fenster am unteren Rand eines übergeordneten Fensters, in dem eine Anwendung verschiedene Arten von Statusinformationen anzeigen kann. Die Statusleiste kann in Teile aufgeteilt werden, um mehr als eine Art von Informationen anzuzeigen. Der folgende Screenshot zeigt die Statusleiste in der Microsoft Windows Paint-Anwendung. In diesem Fall enthält die Statusleiste den Text "für Hilfe, klicken Sie im Menü" Hilfe "auf Hilfe Themen. Die Statusleiste ist der Bereich am unteren Rand des Fensters, der Hilfetext und Koordinaten Informationen enthält.

![Screenshot der Paint-Anwendung mit einer Statusleiste, die Hinweise zur Online Hilfe enthält](images/sb-paint.png)

In diesem Abschnitt werden folgende Themen behandelt.

-   [Typen und Stile](#types-and-styles)
-   [Größe und Höhe](#size-and-height)
-   [Mehrteilige Status leisten](#multiple-part-status-bars)
-   [Text Vorgänge der Status Leiste](#status-bar-text-operations)
-   [Vom Besitzer gezeichnete Status leisten](#owner-drawn-status-bars)
-   [Status leisten im einfachen Modus](#simple-mode-status-bars)
-   [Standard Nachrichtenverarbeitung für Status Leiste](#default-status-bar-message-processing)

## <a name="types-and-styles"></a>Typen und Stile

Die Standardposition einer Statusleiste befindet sich am unteren Rand des übergeordneten Fensters, Sie können jedoch den [**\_ obersten**](common-control-styles.md) Stil von CCS angeben, damit er am oberen Rand des Client Bereichs des übergeordneten Fensters angezeigt wird.

Sie können den [**sbars- \_ SizeGrip**](status-bar-styles.md) -Stil angeben, um einen Größen Zieh Punkt am rechten Ende der Statusleiste einzuschließen.

> [!Note]  
> Die Kombination der Stile " [**CCS \_ Top**](common-control-styles.md) " und " [**sbars \_ SizeGrip**](status-bar-styles.md) " wird nicht empfohlen, da der resultierende Größen Zieh Punkt nicht funktionsfähig ist.

 

## <a name="size-and-height"></a>Größe und Höhe

Die Fenster Prozedur für die Statusleiste legt automatisch die anfängliche Größe und Position des Fensters fest und ignoriert dabei die Werte, die in der Funktion " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) " angegeben sind. Die Breite ist mit der Breite des Client Bereichs des übergeordneten Fensters identisch. Die Höhe basiert auf den Metriken der Schriftart, die derzeit im Gerätekontext der Statusleiste ausgewählt ist, sowie auf der Breite der Fensterränder.

Die Fenster Prozedur passt die Größe der Statusleiste automatisch an, wenn Sie eine [**WM- \_ Größen**](/windows/desktop/winmsg/wm-size) Nachricht empfängt. Wenn sich die Größe des übergeordneten Fensters ändert, sendet das übergeordnete Fenster in der Regel eine **WM- \_ Größen** Meldung an die Statusleiste.

Eine Anwendung kann die Mindesthöhe des Zeichnungs Bereichs einer Statusleiste festlegen, indem das Fenster eine [**SB- \_ setMinHeight**](sb-setminheight.md) -Nachricht gesendet wird, wobei die Mindesthöhe in Pixel angegeben wird. Der Zeichenbereich schließt die Rahmen des Fensters nicht ein. Eine minimale Höhe ist für das Zeichnen in einer vom Besitzer gezeichneten Statusleiste nützlich. Weitere Informationen finden Sie weiter unten in diesem Kapitel unter vom [Besitzer gezeichnete Status leisten](#owner-drawn-status-bars) .

Sie rufen die breiten der Rahmen einer Statusleiste ab, indem Sie das Fenster an eine [**SB \_ getborders**](sb-getborders.md) -Nachricht senden. Die Meldung enthält die Adresse eines Arrays mit drei Elementen, das die breiten erhält.

## <a name="multiple-part-status-bars"></a>Multiple-Part Status leisten

Eine Statusleiste kann viele verschiedene Teile aufweisen, von denen jede eine andere Textzeile anzeigt. Sie teilen eine Statusleiste in Teile, indem Sie das Fenster an eine [**SB- \_ SetParts**](sb-setparts.md) -Nachricht senden und dabei die Anzahl der zu erstellenden Teile und die Adresse eines ganzzahligen Arrays angeben. Das Array enthält ein Element für jeden Teil, und jedes Element gibt die Client Koordinate des rechten Rands eines Teils an.

Eine Statusleiste kann maximal 256 Teile aufweisen, obwohl Anwendungen in der Regel sehr viel weniger verwenden. Sie rufen die Anzahl der Teile in einer Statusleiste sowie die Koordinate des rechten Rands der einzelnen Teile ab, indem Sie das Fenster an eine [**SB \_ GetParts**](sb-getparts.md) -Nachricht senden.

## <a name="status-bar-text-operations"></a>Text Vorgänge der Status Leiste

Sie legen den Text eines beliebigen Teils einer Statusleiste fest, indem Sie die [**SB- \_ SetText**](sb-settext.md) -Nachricht senden, den NULL basierten Index eines Teils angeben, eine Adresse der Zeichenfolge, die im Teil gezeichnet werden soll, und die Technik zum Zeichnen der Zeichenfolge. Mit der Zeichnungstechnik wird festgelegt, ob der Text einen Rahmen aufweist und, wenn dies der Fall ist, die Art des Rahmens. Außerdem wird festgelegt, ob das übergeordnete Fenster für das Zeichnen des Texts zuständig ist. Weitere Informationen finden Sie weiter unten im Abschnitt vom [Besitzer gezeichnete Status leisten](#owner-drawn-status-bars) .

Standardmäßig wird Text innerhalb des angegebenen Teils einer Statusleiste linksbündig ausgerichtet. Sie können Tabstopp Zeichen ( \\ t) in den Text einbetten, um ihn zu zentrieren oder rechtsbündig auszurichten. Der Text rechts von einem einzelnen Tabstopp Zeichen wird zentriert, und der Text rechts von einem zweiten Tabstopp Zeichen wird rechtsbündig ausgerichtet.

Um Text von einer Statusleiste abzurufen, verwenden Sie die [**SB \_ getTextLength**](sb-gettextlength.md) -und [**SB \_ gettext**](sb-gettext.md) -Nachrichten.

Wenn Ihre Anwendung eine Statusleiste mit nur einem Teil verwendet, können Sie die Nachrichten [**WM \_ SetText**](/windows/desktop/winmsg/wm-settext), [**WM \_ gettext**](/windows/desktop/winmsg/wm-gettext)und [**WM \_ getTextLength**](/windows/desktop/winmsg/wm-gettextlength) zum Durchführen von Text Vorgängen verwenden. Diese Nachrichten behandeln nur den Teil mit dem Index 0 (null), sodass Sie die Statusleiste ähnlich wie ein statisches Text Steuerelement behandeln können.

Um eine Statuszeile anzuzeigen, ohne eine Statusleiste zu erstellen, verwenden Sie die [**drawstatustext**](/windows/desktop/api/Commctrl/nf-commctrl-drawstatustexta) -Funktion. Die-Funktion verwendet die gleichen Techniken zum Zeichnen des Status als Fenster Prozedur für die Statusleiste, aber die Größe und Position der Statusinformationen werden nicht automatisch festgelegt. Wenn Sie die-Funktion aufrufen, müssen Sie die Größe und Position der Statusinformationen sowie den Gerätekontext des Fensters angeben, in dem Sie gezeichnet werden soll.

## <a name="owner-drawn-status-bars"></a>Owner-Drawn Status leisten

Einzelne Teile einer Statusleiste können als vom Besitzer gezeichnete Teile definiert werden. Wenn Sie diese Technik verwenden, erhalten Sie mehr Kontrolle, als Sie andernfalls über die Darstellung des Fenster Teils verfügen würden. Beispielsweise können Sie eine Bitmap anstelle von Text anzeigen oder Text mit einer anderen Schriftart zeichnen.

Wenn Sie einen Fenster Teil als Besitzer gezeichnet definieren möchten, senden Sie die [**SB- \_ SetText**](sb-settext.md) -Nachricht an die Statusleiste, und geben Sie dabei den Teil und die SBT-Besitzer \_ Zeichnungs Methode an. Wenn SBT-Besitzer \_ Zeichnen angegeben ist, ist der *LPARAM* -Parameter ein von der Anwendung definierter 32-Bit-Wert, der von der Anwendung beim Zeichnen des Teils verwendet werden kann. Sie können z. b. ein Schriftart handle, ein Bitmap-Handle, eine Adresse einer Zeichenfolge usw. angeben.

Wenn eine Statusleiste einen vom Besitzer gezeichneten Teil zeichnen muss, sendet Sie die [**WM \_ DrawItem**](wm-drawitem.md) -Nachricht an das übergeordnete Fenster. Der *wParam* -Parameter der Nachricht ist der Bezeichner des untergeordneten Fensters der Statusleiste, und der *LPARAM* -Parameter ist die Adresse einer [**drawitemstruct**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) -Struktur. Das übergeordnete Fenster verwendet die Informationen in der-Struktur, um den Teil zu zeichnen. Bei einem von einem Besitzer gezeichneten Teil einer Statusleiste enthält **drawitemstruct** die folgenden Informationen.



| Member         | BESCHREIBUNG                                                                                                            |
|----------------|------------------------------------------------------------------------------------------------------------------------|
| **Ctltype**    | Definiert Verwenden Sie nicht.                                                                                                 |
| **Ctlid**      | Der Bezeichner des untergeordneten Fensters der Statusleiste.                                                                             |
| **Itemid**     | Der null basierte Index des zu Zeichenden Teils.                                                                              |
| **Member itemaction** | Definiert Verwenden Sie nicht.                                                                                                 |
| **itemState**  | Definiert Verwenden Sie nicht.                                                                                                 |
| **hwnditem**   | Handle für die Statusleiste.                                                                                              |
| **HDC**        | Handle für den Gerätekontext der Statusleiste.                                                                        |
| **rcItem**     | Koordinaten des Fenster Teils, der gezeichnet werden soll. Die Koordinaten sind relativ zur linken oberen Ecke der Statusleiste.   |
| **ItemData**   | Der von der Anwendung definierte 32-Bit-Wert, der im *LPARAM* -Parameter der [**SB- \_ SetText**](sb-settext.md) -Nachricht angegeben ist. |



 

## <a name="simple-mode-status-bars"></a>Status leisten im einfachen Modus

Sie fügen eine Statusleiste in den "einfachen Modus" ein, indem Sie Ihr eine [**SB \_ Simple**](sb-simple.md) -Nachricht senden. Eine Statusleiste im einfachen Modus zeigt nur einen Teil an. Wenn der Text des Fensters festgelegt ist, wird das Fenster ungültig, aber erst nach der nächsten [**WM- \_ Paint**](/windows/desktop/gdi/wm-paint)neu gezeichnet. Durch das warten auf die Nachricht wird die Bildschirm Flimmern reduziert, indem die Anzahl der neuzeichenzeiten des Fensters minimiert wird. Eine Statusleiste im einfachen Modus ist hilfreich beim Anzeigen von Hilfetext für Menü Elemente, während der Benutzer im Menü einen Bildlauf durchführt.

Die Zeichenfolge, die eine Statusleiste im einfachen Modus anzeigt, wird getrennt von den Zeichen folgen verwaltet, die im nicht einfachen Modus angezeigt werden. Dies bedeutet, dass Sie das Fenster im einfachen Modus platzieren, seinen Text festlegen und wieder in den nicht einfachen Modus wechseln können, ohne dass der Text im nicht einfachen Modus geändert wird.

Wenn Sie den Text einer Statusleiste für den einfachen Modus festlegen, können Sie jede Zeichentechnik mit Ausnahme von SBT-Besitzer \_ zeichnen. Eine Statusleiste im einfachen Modus unterstützt das Erstellen von Besitzern nicht.

## <a name="default-status-bar-message-processing"></a>Standard Nachrichtenverarbeitung für Status Leiste

In diesem Abschnitt werden die Nachrichten beschrieben, die von der Fenster Prozedur für die vordefinierte Klasse " [**Status ClassName**](common-control-window-classes.md) " verarbeitet werden.



| `Message`               | Standard Verarbeitung                                                                                                                                                                                                                                                       |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **WM \_ Erstellen**        | Initialisiert die Statusleiste.                                                                                                                                                                                                                                              |
| **WM \_ zerstören**       | Gibt die für die Statusleiste zugewiesenen Ressourcen frei.                                                                                                                                                                                                                            |
| **WM- \_ getFont**       | Gibt das Handle für die aktuelle Schriftart zurück, mit der die Statusleiste Ihren Text zeichnet.                                                                                                                                                                                         |
| **WM \_ gettext**       | Kopiert den Text aus dem ersten Teil einer Statusleiste in einen Puffer. Es wird ein 32-Bit-Wert zurückgegeben, der die Länge des Texts (in Zeichen) und das Verfahren zum Zeichnen des Texts angibt.                                                                                |
| **WM \_ getTextLength** | Gibt einen 32-Bit-Wert zurück, der die Länge (in Zeichen) des Texts im ersten Teil einer Statusleiste und der zum Zeichnen des Texts verwendeten Technik angibt.                                                                                                                  |
| **WM- \_ nchittest**     | Gibt den Wert von "htbottomright" zurück, wenn sich der Mauszeiger im Größen Zieh Punkt befindet, was bewirkt, dass das System den Größen Änderungs Cursor anzeigt. Wenn sich der Mauszeiger nicht im Größen Zieh Punkt befindet, übergibt die Statusleiste diese Meldung an die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion. |
| **WM- \_ Paint**         | Zeichnet den ungültigen Bereich der Statusleiste. Wenn der *wParam* -Parameter ungleich **null** ist, geht das Steuerelement davon aus, dass es sich bei dem Wert um einen HDC handelt und zeichnet sich durch den Gerätekontext aus.                                                                                               |
| **WM- \_ setFont**       | Wählt den Schriftart Handle in den Gerätekontext für die Statusleiste aus.                                                                                                                                                                                                      |
| **WM- \_ SetText**       | Kopiert den angegebenen Text in den ersten Teil einer Statusleiste, wobei der Standard Zeichnungs Vorgang (angegeben als null) verwendet wird. Andernfalls wird **true** zurückgegeben, wenn erfolgreich, andernfalls **false** .                                                                                       |
| **WM- \_ Größe**          | Ändert die Statusleiste basierend auf der aktuellen Breite des Client Bereichs des übergeordneten Fensters und der Höhe der aktuellen Schriftart der Statusleiste.                                                                                                                               |



 

 

 
