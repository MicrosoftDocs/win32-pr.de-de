---
title: Informationen zu Symbolleisten-Steuerelementen
description: Eine Symbolleiste ist ein Steuerelement, das eine oder mehrere Schaltflächen enthält.
ms.assetid: b5a00a81-8d23-4844-8b0a-776e7cceced8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f615da972f14bb88c4915504c089dd6b40d9aca
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424150"
---
# <a name="about-toolbar-controls"></a>Informationen zu Symbolleisten-Steuerelementen

Eine Symbolleiste ist ein Steuerelement, das eine oder mehrere Schaltflächen enthält. Wenn ein Benutzer auf jede Schaltfläche klickt, wird eine Befehlsmeldung an das übergeordnete Fenster gesendet. In der Regel entsprechen die Schaltflächen auf einer Symbolleiste Elementen im Menü der Anwendung und bieten dem Benutzer eine zusätzliche und direktere Möglichkeit, auf die Befehle einer Anwendung zu zugreifen.

Der folgende Screenshot zeigt ein Fenster, das eine einfache Symbolleiste für Dateivorgänge enthält. Die Anwendung hat visuelle Stile aktiviert. Die Schaltfläche Speichern ist "heiß", da der Cursor beim Erstellen des Screenshots mit dem Mauszeiger darüber gezeigt wurde. Die tatsächliche Darstellung des Steuerelements variiert je nach Betriebssystem und ausgewähltem Design.

![Screenshot eines Fensters mit einer Symbolleiste mit drei Schaltflächen; Eine Schaltfläche ist heiß](images/tb-withstyles.png)

Der folgende Screenshot zeigt dasselbe Steuerelement in einer Anwendung, die ohne aktivierte visuelle Stile kompiliert wurde.

![Screenshot eines Fensters ohne visuelle Stile: Keine der Schaltflächen sieht heiß aus](images/tb-wostyles.png)

In den folgenden Themen werden Features behandelt, die beim Planen einer Symbolleiste zu berücksichtigen sind. Spezifische Informationen zur Implementierung und Beispielcode finden Sie unter [Verwenden von Symbolleisten-Steuerelementen.](using-toolbar-controls.md)

-   [Angeben der Symbolleistengröße und -position](#specifying-toolbar-size-and-position)
-   [Transparente Symbolleisten](#transparent-toolbars)
-   [Symbolleisten im Listenstil](#list-style-toolbars)
-   [Definieren von Schaltflächenbildern](#defining-button-images)
    -   [Definieren von Schaltflächenbildern mithilfe von Bitmaps](#defining-button-images-by-using-bitmaps)
    -   [Definieren von Schaltflächenbildern mithilfe von Bildlisten](#defining-button-images-by-using-image-lists)
-   [Definieren von Text für Schaltflächen](#defining-text-for-buttons)
-   [Hinzufügen von Symbolleistenschaltflächen](#adding-toolbar-buttons)
    -   [Symbolleisten-Schaltflächenstile](#toolbar-button-styles)
    -   [Status der Symbolleistenschaltfläche](#toolbar-button-states)
    -   [Befehlsbezeichner](#command-identifier)
    -   [Schaltflächengröße und -position](#button-size-and-position)
-   [Aktivieren der Anpassung](#enabling-customization)
-   [Aktivieren der Hot-Tracking-Überwachung](#enabling-hot-tracking)

## <a name="specifying-toolbar-size-and-position"></a>Angeben von Symbolleistengröße und -position

Wenn Sie mit [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex)eine Symbolleiste erstellen, können Sie mit der Funktion die Höhe und Breite der Symbolleiste in Pixel angeben.

> [!Note]  
> Die Verwendung von [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) wird nicht empfohlen, da neue Funktionen von Symbolleisten, einschließlich Bildlisten, nicht unterstützt werden. Weitere Informationen zum Erstellen von Symbolleisten finden Sie unter [Verwenden von Symbolleistensteuerelementen.](using-toolbar-controls.md)

 

Die [**CreateWindowEx-Funktion**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) verfügt nicht über Parameter zum Angeben der Symbolleistengröße. Die Symbolleistenfensterprozedur legt automatisch die Größe und Position des Symbolleistenfensters fest. Die Höhe basiert auf der Höhe der Schaltflächen in der Symbolleiste. Die Breite entspricht der Breite des Clientbereichs des übergeordneten Fensters. Um die automatischen Größeneinstellungen zu ändern, senden Sie eine [**\_ TB SETBUTTONSIZE-Nachricht.**](tb-setbuttonsize.md) Die [**gängigen CCS \_ TOP-**](common-control-styles.md) und [**CCS BOTTOM-Steuerelementstile \_**](common-control-styles.md) bestimmen, ob die Symbolleiste am oberen oder unteren Rand des Clientbereichs positioniert ist. Standardmäßig weist eine Symbolleiste den **CCS \_ TOP-Stil** auf.

Außerdem passt die Prozedur für das Symbolleistenfenster automatisch die Größe der Symbolleiste an, wenn eine [**WM \_ SIZE-**](/windows/desktop/winmsg/wm-size) oder [**TB \_ AUTOIZE-Meldung empfangen**](tb-autosize.md) wird. Eine Anwendung sollte eine dieser Nachrichten senden, wenn sich die Größe des übergeordneten Fensters ändert, oder nachdem eine Nachricht gesendet wurde, die eine Anpassung der Größe der Symbolleiste erfordert, z. B. eine [**TB \_ SETBUTTONSIZE-Nachricht.**](tb-setbuttonsize.md)

Das Standardmäßige Größen- und Positionierungsverhalten der Symbolleiste kann durch Festlegen der gängigen Steuerelementstile [**CCS \_ NORESIZE**](common-control-styles.md) und [**CCS \_ NOPARENTALIGN**](common-control-styles.md) deaktiviert werden. Symbolleisten-Steuerelemente, die von Rebar-Steuerelementen gehostet werden, müssen diese Stile festlegen, da das Rebar-Steuerelement die Symbolleistengröße und -position hat.

## <a name="transparent-toolbars"></a>Transparente Symbolleisten

Symbolleistensteuerelemente unterstützen ein transparentes Aussehen, das es ermöglicht, dass der Clientbereich unter der Symbolleiste angezeigt wird. Es gibt zwei Arten von transparenten Symbolleisten: solche mit flachen Schaltflächen und solche mit dreidimensionalen Schaltflächen. Wenn Ihre Anwendung mit der Windows-Schnittstelle übereinstimmen soll, verwenden Sie die flache transparente Stilsymbolleiste.

Der folgende Screenshot zeigt die beiden Arten von transparenten Symbolleisten, die keine visuellen Stile verwenden.

![Screenshot von zwei Fenstern mit unterschiedlichen Symbolleistenstilen, aber beide Symbolleisten sind transparent](images/toolbartrans.jpg)

Der folgende Screenshot zeigt eine transparente Symbolleiste, wie sie in Windows Vista angezeigt werden kann, mit aktivierten visuellen Stilen. Die Hintergrundfarbe des Dialogfelds wurde geändert, um die Transparenz offensichtlicher zu machen.

![Screenshot eines Fensters in Windows Vista mit einer transparenten Symbolleiste](images/tb-transparent.png)

Um eine transparente Symbolleiste zu erstellen, müssen Sie nur [**TBSTYLE \_ FLAT**](toolbar-control-and-button-styles.md) oder [**TBSTYLE \_ TRANSPARENT**](toolbar-control-and-button-styles.md) zum Fensterformatparameter von [**CreateWindowEx hinzufügen.**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) Wenn sie nicht möchten, dass eine Zeile am unteren Rand der Symbolleiste angezeigt wird, verwenden Sie nicht den [**WS \_ BORDER-Fensterstil.**](/windows/desktop/winmsg/window-styles)

> [!Note]  
> Wenn Sie visuelle Stile verwenden, sind Symbolleisten möglicherweise standardmäßig flach.

 

## <a name="list-style-toolbars"></a>Symbolleisten im Listenstil

Mit Symbolleistenschaltflächen können Sie sowohl Text als auch Bitmaps anzeigen. Die Schaltflächen auf einer Symbolleiste, die mit dem [**TBSTYLE \_ LIST-Stil**](toolbar-control-and-button-styles.md) erstellt wurde, platzieren Text rechts neben der Bitmap und nicht darunter.

Der folgende Screenshot zeigt eine Symbolleiste mit dem Listenstil.

![Screenshot einer Symbolleiste mit Text rechts neben jedem Symbol](images/tb-liststyle.png)

Sie können den [**TBSTYLE LIST-Symbolleistenstil \_**](toolbar-control-and-button-styles.md) in Kombination mit dem [**TBSTYLE \_ FLAT-Stil**](toolbar-control-and-button-styles.md) verwenden, um eine Symbolleiste mit flachen Schaltflächen zu erstellen.

## <a name="defining-button-images"></a>Definieren von Schaltflächenbildern

Es gibt zwei Möglichkeiten, die Bilder für Schaltflächen anzugeben– nach Bitmaps oder nach Bildlisten. Eine Anwendung muss auswählen, welche Methode verwendet werden soll. Es können nicht beide Methoden mit demselben Symbolleistensteuerelement verwendet werden. Beachten Sie, dass die [**CreateToolbarEx-Funktion**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) die Bitmapmethode verwendet. Anwendungen, die die Bildlistenmethode verwenden möchten, müssen die [**CreateWindowEx-Funktion**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) verwenden, um das Symbolleistensteuerelement zu erstellen.

### <a name="defining-button-images-by-using-bitmaps"></a>Definieren von Schaltflächenbildern mithilfe von Bitmaps

Jede Schaltfläche in einer Symbolleiste kann ein Bitmapbild enthalten. Eine Symbolleiste verwendet eine interne Liste, um die Informationen zu speichern, die zum Zeichnen der Bilder benötigt werden. Wenn Sie die [**CreateToolbarEx-Funktion**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) aufrufen, geben Sie eine monofarbige oder farbliche Bitmap an, die die Anfangsbilder enthält, und die Symbolleiste fügt die Informationen der internen Liste der Bilder hinzu. Sie können später weitere Bilder hinzufügen, indem Sie die [**\_ TB-ADDBITMAP-Meldung**](tb-addbitmap.md) verwenden.

Jedes Bild verfügt über einen nullbasierten Index. Das erste bild, das der internen Liste hinzugefügt wurde, hat den Index 0, das zweite Bild hat den Index 1 usw. [**TB \_ ADDBITMAP**](tb-addbitmap.md) fügt Bilder am Ende der Liste hinzu und gibt den Index des ersten neuen Bilds zurück, das hinzugefügt wurde. Um das Bild einer Schaltfläche zuzuordnen, müssen Sie eine [**\_ TB-ADDBUTTONS-Nachricht**](tb-addbuttons.md) senden und den Index des Bilds angeben, nachdem Sie der internen Bildliste Bitmaps hinzugefügt haben.

Windows geht davon aus, dass alle Bitmapbilder einer Symbolleiste dieselbe Größe haben. Sie geben die Größe an, wenn Sie die Symbolleiste erstellen, indem [**Sie CreateToolbarEx verwenden.**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) Wenn Sie die [**CreateWindowEx-Funktion**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) verwenden, um eine Symbolleiste zu erstellen, wird die Größe der Bilder auf die Standardabmessungen von 16 x 15 Pixeln festgelegt. Sie können die [**\_ TB-Nachricht SETBITMAPSIZE**](tb-setbitmapsize.md) verwenden, um die Abmessungen der Bitmapbilder zu ändern. Dies ist jedoch vor dem Hinzufügen von Bildern zur internen Liste der Fall.

### <a name="defining-button-images-by-using-image-lists"></a>Definieren von Schaltflächenbildern mithilfe von Bildlisten

Sie können Schaltflächenbilder auch in einer Reihe von [Bildlisten speichern.](image-lists.md) Eine Bildliste ist eine Sammlung von Bildern der gleichen Größe, auf die jeweils durch den Index verwiesen werden kann. Bildlisten werden verwendet, um große Mengen von Symbolen oder Bitmaps zu verwalten. Sie können bis zu drei verschiedene Bildlisten verwenden, um Schaltflächen in verschiedenen Zuzuständen anzuzeigen, wie in der folgenden Tabelle gezeigt.



|  State        |  Beschreibung                                                                                                                                                                                            |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Normal   | Schaltflächen im Standardzustand.                                                                                                                                                              |
| heiße Ebene      | Schaltflächen, die sich unter dem Zeiger befinden oder gedrückt werden. Heiße Elemente werden nur in Symbolleisten-Steuerelementen unterstützt, die den [**TBSTYLE \_ FLAT-Stil**](toolbar-control-and-button-styles.md) haben. |
| Disabled | Deaktivierte Schaltflächen.                                                                                                                                                                   |



 

Nachdem die Symbolleiste zerstört wurde, müssen Anwendungen alle erstellten Bildlisten frei geben.

## <a name="defining-text-for-buttons"></a>Definieren von Text für Schaltflächen

Jede Schaltfläche kann zusätzlich zu oder anstelle eines Bilds eine Zeichenfolge anzeigen. Eine Symbolleiste verwaltet eine interne Liste, die alle Zeichenfolgen enthält, die für Symbolleistenschaltflächen verfügbar sind. Sie fügen der internen Liste Zeichenfolgen hinzu, indem Sie die [**TB \_ ADDSTRING-Meldung**](tb-addstring.md) verwenden und dabei die Adresse des Puffers angeben, der die hinzuzufügenden Zeichenfolgen enthält. Jede Zeichenfolge muss null-terminiert sein, und die letzte Zeichenfolge muss mit zwei NULL-Zeichen beendet werden.

Jede Zeichenfolge verfügt über einen nullbasierten Index. Die erste Zeichenfolge, die der internen Liste von Zeichenfolgen hinzugefügt wurde, hat den Index 0, die zweite Zeichenfolge hat den Index 1 usw. [**TB \_ ADDSTRING**](tb-addstring.md) fügt Zeichenfolgen am Ende der Liste hinzu und gibt den Index der ersten neuen Zeichenfolge zurück. Sie verwenden den Index einer Zeichenfolge, um die Zeichenfolge einer Schaltfläche zuzuordnen.

Die Verwendung von [**TB \_ ADDSTRING**](tb-addstring.md) ist nicht die einzige Möglichkeit zum Hinzufügen von Zeichenfolgen zu einer Symbolleiste. Sie können eine Zeichenfolge in einer Schaltfläche anzeigen, indem Sie einen Zeichenfolgenzeiger im **iString-Member** der [**TBBUTTON-Struktur**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) übergeben, der an [**TB \_ ADDBUTTONS**](tb-addbuttons.md)übergeben wird. Darüber hinaus können Sie [**TB \_ SETBUTTONINFO**](tb-setbuttoninfo.md) verwenden, um einer Symbolleistenschaltfläche Text zuzuweisen.

## <a name="adding-toolbar-buttons"></a>Hinzufügen von Symbolleistenschaltflächen

Wenn Sie die [**CreateToolbarEx-Funktion**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) verwenden, um eine Symbolleiste zu erstellen, können Sie der Symbolleiste Schaltflächen hinzufügen, indem Sie ein Array von [**TBBUTTON-Strukturen**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) füllen und die Adresse des Arrays im Funktionsaufruf angeben. Die [**CreateWindowEx-Funktion**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) verfügt jedoch nicht über einen Parameter zum Übergeben einer **TBBUTTON-Struktur.** **CreateWindowEx** erstellt eine leere Symbolleiste, die Sie ausfüllen, indem Sie eine [**\_ TB-ADDBUTTONS-Nachricht**](tb-addbuttons.md) senden, die die Adresse einer **TBBUTTON-Struktur** angibt.

Nachdem eine Symbolleiste erstellt wurde, können Sie Schaltflächen hinzufügen, indem Sie eine [**\_ TB INSERTBUTTON-**](tb-insertbutton.md) oder [**TB \_ ADDBUTTONS-Nachricht**](tb-addbuttons.md) senden. Jede Schaltfläche wird durch eine [**TBBUTTON-Struktur**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) beschrieben, die die Attribute der Schaltfläche definiert, einschließlich der Indizes ihrer Zeichenfolge und Bitmap sowie ihres Stils, Zustands, Befehlsbezeichners und anwendungsdefiniertem 32-Bit-Wert.

> [!Note]  
> Wenn Sie die [**CreateWindowEx-Funktion**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) verwenden, um eine Symbolleiste zu erstellen, müssen Sie die [**TB \_ BUTTONSTRUCTSIZE-Nachricht**](tb-buttonstructsize.md) senden, bevor Sie Schaltflächen hinzufügen. Die Nachricht übergibt die Größe der [**TBBUTTON-Struktur**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) an die Symbolleiste.

 

### <a name="toolbar-button-styles"></a>Symbolleisten-Schaltflächenstile

Der Stil einer Schaltfläche bestimmt, wie die Schaltfläche angezeigt wird und wie sie auf Benutzereingaben reagiert. Beispielsweise erstellt der [**BTNS \_ BUTTON-Stil**](toolbar-control-and-button-styles.md) eine Symbolleistenschaltfläche, die sich wie eine Standard-Pushschaltfläche verhält. Eine Schaltfläche mit dem [**STIL BTNS \_ CHECK**](toolbar-control-and-button-styles.md) ähnelt einer Standardschaltfläche, mit der Ausnahme, dass sie bei jedem Klicken des Benutzers zwischen dem gedrückten und dem nicht gedrückten Zustände umschaltet.

Sie können Gruppen von Symbolleistenschaltflächen erstellen, die wie Optionsfelder fungieren, indem Sie den [**Stil BTNS \_ GROUP**](toolbar-control-and-button-styles.md) oder [**BTNS \_ CHECKGROUP**](toolbar-control-and-button-styles.md) verwenden. Dadurch bleibt eine Schaltfläche gedrückt, bis der Benutzer eine andere Schaltfläche in der Gruppe auswählt. Eine Gruppe wird als zusammenhängende Sammlung von Schaltflächen definiert, die alle den **Stil BTNS \_ GROUP** oder **BTNS \_ CHECKGROUP** haben.

Der [**BTNS \_ SEP-Stil**](toolbar-control-and-button-styles.md) erstellt eine kleine Lücke zwischen Schaltflächen oder zeichnet eine Etch zwischen Schaltflächen auf flachen Symbolleisten. Eine Schaltfläche im **BTNS \_ SEP-Format** erhält keine Benutzereingaben.

In Version 5.80 der allgemeinen Steuerelemente wurden einige neue Symbolleisten-Schaltflächenstile eingeführt und einige der älteren Stile umbenannt. Alle Schaltflächenformatflags beginnen jetzt mit BTNS \_ XXX anstelle von TBSTYLE \_ XXX. Eine Auflistung und Eine Erörterung der Schaltflächenstile finden Sie unter [Symbolleisten-Steuerelement und Schaltflächenstile.](toolbar-control-and-button-styles.md)

### <a name="toolbar-button-states"></a>Symbolleisten-Schaltflächenzustände

Jede Schaltfläche in einer Symbolleiste hat einen Zustand. Die Symbolleiste aktualisiert den Zustand einer Schaltfläche, um Benutzeraktionen widerzuzustanden, z. B. das Klicken auf die Schaltfläche. Der Status gibt an, ob die Schaltfläche derzeit gedrückt oder nicht gedrückt, aktiviert oder deaktiviert, ausgeblendet oder sichtbar ist. Obwohl eine Anwendung beim Hinzufügen der Schaltfläche zur Symbolleiste den Anfangszustand einer Schaltfläche festgelegt hat, kann sie den Zustand ändern und abrufen, indem TB [**\_ GETSTATE-**](tb-getstate.md) und [**TB \_ SETSTATE-Meldungen**](tb-setstate.md) an die Symbolleiste gesendet werden. Eine Liste der Symbolleisten-Schaltflächenzustände finden Sie unter [Symbolleistenzustände.](toolbar-button-states.md)

### <a name="command-identifier"></a>Befehlsbezeichner

Jeder Schaltfläche ist ein anwendungsdefinierter Befehlsbezeichner zugeordnet. Schaltflächenbezeichner werden in der Regel in einer Anwendungsheaderdatei definiert. Beispielsweise kann eine Schaltfläche Einfügen wie folgt definiert werden:


```
#define ID_PASTE 100
```



Wenn der Benutzer eine Schaltfläche auswählt, sendet die Symbolleiste dem übergeordneten Fenster eine [**WM \_ COMMAND-**](/windows/desktop/menurc/wm-command) oder [**WM \_ NOTIFY-Meldung,**](wm-notify.md) die den Befehlsbezeichner der Schaltfläche enthält. Das übergeordnete Fenster überprüft den Befehlsbezeichner und führt den Befehl aus, der der Schaltfläche zugeordnet ist. Informationen dazu, wann Steuerelemente **WM \_ COMMAND-Nachrichten** senden und wann sie **WM \_ NOTIFY** senden, finden Sie im Abschnitt Hinweise der [**WM \_ NOTIFY-Dokumentation.**](wm-notify.md)

### <a name="button-size-and-position"></a>Schaltflächengröße und -position

Eine Symbolleiste verfolgt ihre Schaltflächen, indem sie jeder Schaltfläche einen Positionsindex zuweist. Der Index ist nullbasiert. Das heißt, die schaltfläche ganz links hat den Index 0, die nächste Schaltfläche rechts hat den Index 1 usw. Eine Anwendung muss beim Senden von Nachrichten den Index einer Schaltfläche angeben, um Informationen über die Schaltfläche abzurufen oder die Attribute der Schaltfläche festzulegen.

Eine Symbolleiste aktualisiert die Positionsindizes, wenn Schaltflächen eingefügt und entfernt werden. Eine Anwendung kann den aktuellen Positionsindex einer Schaltfläche mithilfe der [**TB \_ COMMANDTOINDEX-Nachricht**](tb-commandtoindex.md) abrufen. Die Meldung gibt den Befehlsbezeichner einer Schaltfläche an, und das Symbolleistenfenster verwendet den Bezeichner, um die Schaltfläche zu suchen und ihren Positionsindex zurückzugeben.

Alle Schaltflächen in einer Symbolleiste haben die gleiche Größe. Für [**die CreateToolbarEx-Funktion**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) müssen Sie die Anfangsgröße der Schaltflächen festlegen, wenn Sie die Symbolleiste erstellen. Wenn Sie die [**CreateWindowEx-Funktion**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) verwenden, wird die Anfangsgröße auf die Standardabmessungen von 24 x 22 Pixeln festgelegt. Sie können die [**TB \_ SETBUTTONSIZE-Nachricht**](tb-setbuttonsize.md) verwenden, um die Schaltflächengröße zu ändern. Sie müssen dies jedoch tun, bevor Sie der Symbolleiste Schaltflächen hinzufügen. Die [**TB \_ GETITEMRECT-Nachricht**](tb-getitemrect.md) ruft die aktuellen Dimensionen der Schaltflächen ab.

Wenn Sie eine Zeichenfolge hinzufügen, die länger ist als eine Zeichenfolge, die derzeit auf der Symbolleiste angezeigt wird, setzt die Symbolleiste automatisch die Breite der Schaltflächen zurück. Die Breite wird so festgelegt, dass sie die längste Zeichenfolge in der Symbolleiste aufnehmen kann.

## <a name="enabling-customization"></a>Aktivieren der Anpassung

Eine Symbolleiste verfügt über integrierte Anpassungsfeatures, die Sie dem Benutzer zur Verfügung stellen können, indem Sie der Symbolleiste den allgemeinen [**\_ CCS-ANPASSBAR-Steuerelementstil**](common-control-styles.md) geben. Die Anpassungsfunktionen ermöglichen es dem Benutzer, eine Schaltfläche an eine neue Position zu ziehen oder eine Schaltfläche zu entfernen, indem er sie von der Symbolleiste zieht. Darüber hinaus kann der Benutzer auf die Symbolleiste doppelklicken, um das Dialogfeld Symbolleiste anpassen anzuzeigen, in dem der Benutzer Symbolleistenschaltflächen hinzufügen, löschen und neu anordnen kann. Um das Dialogfeld anzuzeigen, verwenden Sie die [**MELDUNG TB \_ CUSTOMIZE.**](tb-customize.md) Eine Anwendung bestimmt, ob die Anpassungsfunktionen für den Benutzer verfügbar sind, und steuert, in welchem Umfang der Benutzer die Symbolleiste anpassen kann.

Im Rahmen des Anpassungsprozesses müssen Anwendungen häufig den Zustand einer Symbolleiste speichern und wiederherstellen. Beispielsweise speichern viele Anwendungen den Symbolleistenzustand, bevor der Benutzer mit der Anpassung der Symbolleiste beginnt, falls der Benutzer später den ursprünglichen Zustand der Symbolleiste wiederherstellen möchte. Das Symbolleisten-Steuerelement führt nicht automatisch einen Datensatz seines Präcustomization-Zustands. Ihre Anwendung muss den Symbolleistenzustand speichern, um ihn wiederherstellen zu können. Weitere Informationen finden Sie unter [Verwenden von Symbolleistensteuerelementen.](using-toolbar-controls.md)

## <a name="enabling-hot-tracking"></a>Aktivieren der Hot-Tracking-Überwachung

Hot-Tracking bedeutet, dass sich die Darstellung der Schaltfläche ändert, wenn der Zeiger über ein Element bewegt wird. Wenn visuelle Stile aktiviert sind, unterstützen Symbolleisten standardmäßig hot-tracking. Andernfalls unterstützen nur Symbolleistensteuerelemente, die mit [**dem TBSTYLE \_ FLAT-Stil**](toolbar-control-and-button-styles.md) erstellt wurden, hot-tracking. Sie können andere Fensterstile in Kombination mit **TBSTYLE \_ FLAT** verwenden, um Symbolleisten zu erstellen, die hot-tracking ermöglichen, aber eine andere Darstellung als eine flache Symbolleiste haben. Weitere Informationen finden Sie unter [Verwenden von Symbolleistensteuerelementen.](using-toolbar-controls.md)

 

 