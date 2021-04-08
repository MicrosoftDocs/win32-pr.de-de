---
title: Info
description: Eine Symbolleiste ist ein Steuerelement, das eine oder mehrere Schaltflächen enthält.
ms.assetid: b5a00a81-8d23-4844-8b0a-776e7cceced8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 263d95b13ddee54561cf1b0bb9d003d5d34cdf8d
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103949139"
---
# <a name="about-toolbar-controls"></a>Info

Eine Symbolleiste ist ein Steuerelement, das eine oder mehrere Schaltflächen enthält. Jede Schaltfläche, wenn ein Benutzer darauf klickt, sendet eine Befehls Meldung an das übergeordnete Fenster. Die Schaltflächen in einer Symbolleiste entsprechen in der Regel Elementen im Menü der Anwendung und bieten dem Benutzer eine zusätzliche und direktere Möglichkeit zum Zugriff auf die Befehle einer Anwendung.

Der folgende Screenshot zeigt ein Fenster, das eine einfache Symbolleiste für Datei Vorgänge enthält. Die Anwendung hat visuelle Stile aktiviert. Die Schaltfläche "Speichern" ist "Hot", da der Cursor beim Durchlaufen des Screenshots darauf gezeigt hat. Die tatsächliche Darstellung des Steuer Elements variiert je nach Betriebssystem und Benutzer ausgewähltem Design.

![Screenshot eines Fensters mit einer drei-Schaltflächen-Symbolleiste eine Schaltfläche ist "Hot"](images/tb-withstyles.png)

Der folgende Screenshot zeigt dasselbe Steuerelement in einer Anwendung, die ohne aktivierte visuelle Stile kompiliert wurde.

![Screenshot eines Fensters ohne visuelle Stile: keine der Schaltflächen ist "heiß".](images/tb-wostyles.png)

In den folgenden Themen werden die zu berücksichtigenden Funktionen beim Planen einer Symbolleiste erläutert. Spezifische Informationen zur Implementierung und zum Beispielcode finden Sie unter [Verwenden von Symbol](using-toolbar-controls.md)leisten-Steuerelementen.

-   [Angeben der Größe und Position der Symbolleiste](#specifying-toolbar-size-and-position)
-   [Transparente Symbolleisten](#transparent-toolbars)
-   [Listenstil-Symbolleisten](#list-style-toolbars)
-   [Definieren von Schaltflächen Bildern](#defining-button-images)
    -   [Definieren von Schaltflächen Bildern mithilfe von Bitmaps](#defining-button-images-by-using-bitmaps)
    -   [Definieren von Schaltflächen Bildern mithilfe von Bildlisten](#defining-button-images-by-using-image-lists)
-   [Definieren von Text für Schaltflächen](#defining-text-for-buttons)
-   [Hinzufügen von Schaltflächen](#adding-toolbar-buttons)
    -   [Toolbar-Schaltflächen Stile](#toolbar-button-styles)
    -   [Symbolleisten Schaltflächen](#toolbar-button-states)
    -   [Befehls Bezeichner](#command-identifier)
    -   [Schaltflächen Größe und-Position](#button-size-and-position)
-   [Aktivieren der Anpassung](#enabling-customization)
-   [Aktivieren der Hot-Tracking-Lösung](#enabling-hot-tracking)

## <a name="specifying-toolbar-size-and-position"></a>Angeben der Größe und Position der Symbolleiste

Wenn Sie eine Symbolleiste mithilfe von " [**kreatetoolbarex**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex)" erstellen, können Sie mit der-Funktion die Höhe und Breite der Symbolleiste in Pixel angeben.

> [!Note]  
> Die Verwendung von " [**kreatetoolbarex**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) " wird nicht empfohlen, da Sie keine neuen Features von Symbolleisten einschließlich Bildlisten unterstützt. Weitere Informationen zum Erstellen von Symbolleisten finden [Sie unter Verwenden von Symbol](using-toolbar-controls.md)leisten-Steuerelementen.

 

Die Funktion " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) " weist keine Parameter zum Angeben der Symbolleisten Größe auf. Mit der Prozedur des Symbolleisten Fensters werden die Größe und die Position des Symbolleisten Fensters automatisch festgelegt. Die Höhe basiert auf der Höhe der Schaltflächen auf der Symbolleiste. Die Breite ist mit der Breite des Client Bereichs des übergeordneten Fensters identisch. Um die Einstellungen für die automatische Größe zu ändern, senden Sie eine [**TB- \_ setbuttonsize**](tb-setbuttonsize.md) -Nachricht. Die Grundsteuer Stile von [**CCS \_ Top**](common-control-styles.md) und [**CCS \_ unten**](common-control-styles.md) bestimmen, ob die Symbolleiste am oberen oder unteren Rand des Client Bereichs positioniert ist. Standardmäßig verfügt eine Symbolleiste über **den \_ obersten** Stil von CCS.

Außerdem passt die Prozedur des Symbolleisten Fensters automatisch die Größe der Symbolleiste an, wenn [**eine \_**](/windows/desktop/winmsg/wm-size) [**\_ Automatische Größen**](tb-autosize.md) -oder TB-Nachricht empfangen wird. Eine Anwendung sollte jede dieser Nachrichten senden, wenn sich die Größe des übergeordneten Fensters ändert, oder nachdem eine Nachricht gesendet wurde, die die Größe der Symbolleiste anpassen muss, z. –. eine [**TB- \_ setbuttonsize**](tb-setbuttonsize.md) -Nachricht.

Die Symbolleisten-Standardgröße und das Positions Verhalten können deaktiviert werden, indem die allgemeinen Steuerelemente [**CCS \_ NORESIZE**](common-control-styles.md) und [**CCS \_ noparentalign**](common-control-styles.md) festgelegt werden. Von Symbolleisten-Steuerelementen, die von den Grund leisten Steuerelementen gehostet werden, müssen diese Stile festgelegt werden, da das Grund leisten-Steuerelement die Größe

## <a name="transparent-toolbars"></a>Transparente Symbolleisten

Symbolleisten-Steuerelemente unterstützen ein transparentes Aussehen, mit dem der Client Bereich unter der Symbolleiste durch angezeigt werden kann. Es gibt zwei Arten von transparenten Symbolleisten, bei denen es sich um FlatButtons und mit dreidimensionalen Schaltflächen handelt. Wenn Sie möchten, dass Ihre Anwendung mit der Windows-Benutzeroberfläche identisch ist, verwenden Sie die Symbolleiste mit dem flachen transparenten

Der folgende Screenshot zeigt die zwei Arten von transparenten Symbolleisten, ohne visuelle Stile zu verwenden.

![Screenshot von zwei Fenstern mit unterschiedlichen Formaten von Symbolleisten, beide Symbolleisten sind jedoch transparent](images/toolbartrans.jpg)

Der folgende Screenshot zeigt eine transparente Symbolleiste, wie Sie in Windows Vista angezeigt werden kann, wenn visuelle Stile aktiviert sind. Die Hintergrundfarbe des Dialog Felds wurde geändert, um die Transparenz zu verdeutlichen.

![Screenshot eines Fensters in Windows Vista mit einer transparenten Symbolleiste](images/tb-transparent.png)

Zum Erstellen einer transparenten Symbolleiste müssen Sie lediglich [**tbstyle \_ Flat**](toolbar-control-and-button-styles.md) oder [**tbstyle \_ transparent**](toolbar-control-and-button-styles.md) zum Fenster Stil Parameter von " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)" hinzufügen. Wenn Sie nicht möchten, dass eine Zeile mit dem unteren Rand der Symbolleiste angezeigt wird, verwenden Sie nicht den Fenster Stil des [**WS \_**](/windows/desktop/winmsg/window-styles) -Rahmens.

> [!Note]  
> Wenn visuelle Stile verwendet werden, sind Symbolleisten möglicherweise standardmäßig flach.

 

## <a name="list-style-toolbars"></a>Listenstil-Symbolleisten

Mit Symbolleisten Schaltflächen können Sie sowohl Text als auch Bitmaps anzeigen. Mit den Schaltflächen auf einer Symbolleiste, die mit dem [**tbstyle- \_ Listen**](toolbar-control-and-button-styles.md) Stil erstellt wurde, wird der Text rechts neben der Bitmap platziert.

Der folgende Screenshot zeigt eine Symbolleiste mit dem Listenstil.

![Screenshot einer Symbolleiste mit Text rechts neben jedem Symbol](images/tb-liststyle.png)

Sie können den Symbolleisten Stil der [**tbstyle- \_ Liste**](toolbar-control-and-button-styles.md) in Kombination mit dem [**\_ flachen Stil tbstyle**](toolbar-control-and-button-styles.md) verwenden, um eine Symbolleiste mit flachen Schaltflächen zu erstellen.

## <a name="defining-button-images"></a>Definieren von Schaltflächen Bildern

Es gibt zwei Möglichkeiten, die Bilder für Schaltflächen anzugeben – durch Bitmaps oder Bildlisten. Eine Anwendung muss auswählen, welche Methode verwendet werden soll. Beide Methoden können nicht mit demselben Symbolleisten-Steuerelement verwendet werden. Beachten Sie, dass die Funktion " [**kreatetoolbarex**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) " die Bitmap-Methode verwendet. Anwendungen, die die Image List-Methode verwenden möchten, müssen die Funktion " [**dashboardwindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) " verwenden, um das Symbolleisten-Steuerelement zu erstellen.

### <a name="defining-button-images-by-using-bitmaps"></a>Definieren von Schaltflächen Bildern mithilfe von Bitmaps

Jede Schaltfläche in einer Symbolleiste kann ein Bitmap-Bild enthalten. Eine Symbolleiste verwendet eine interne Liste, um die Informationen zu speichern, die zum Zeichnen der Bilder benötigt werden. Wenn Sie die Funktion "up [**toolbarex**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) " aufrufen, geben Sie eine monochrome-oder Farb Bitmap an, die die anfänglichen Bilder enthält, und die Symbolleiste fügt die Informationen der internen Liste von Bildern hinzu. Sie können später weitere Images hinzufügen, indem Sie die [**TB- \_ AddBitmap**](tb-addbitmap.md) -Nachricht verwenden.

Jedes Image weist einen NULL basierten Index auf. Das erste der internen Liste hinzugefügte Bild verfügt über einen Index von 0, das zweite Bild über einen Index von 1 usw. [**TB \_ AddBitmap**](tb-addbitmap.md) fügt am Ende der Liste Bilder hinzu und gibt den Index des ersten neuen Bilds zurück, das hinzugefügt wurde. Zum Zuordnen des Bilds zu einer Schaltfläche müssen Sie eine [**TB- \_ AddButtons**](tb-addbuttons.md) -Nachricht senden und den Index des Images angeben, nachdem Sie Bitmaps zur internen Bildliste hinzugefügt haben.

Windows geht davon aus, dass es sich bei allen Bitmapbildern einer Symbolleiste um dieselbe Größe handelt. Sie geben die Größe an, wenn Sie die Symbolleiste erstellen, indem Sie " [**kreatetoolbarex**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex)" verwenden. Wenn Sie zum Erstellen einer Symbolleiste die Funktion " [**upatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) " verwenden, wird die Größe der Bilder auf die Standardabmessungen von 16 x 15 Pixel festgelegt. Sie können die [**TB- \_ setbitmapsize**](tb-setbitmapsize.md) -Nachricht verwenden, um die Dimensionen der Bitmapbilder zu ändern, aber Sie müssen dies tun, bevor Sie der internen Liste Bilder hinzufügen.

### <a name="defining-button-images-by-using-image-lists"></a>Definieren von Schaltflächen Bildern mithilfe von Bildlisten

Sie können Schaltflächen Bilder auch in einer Reihe von [Bildlisten](image-lists.md)speichern. Eine Bildliste ist eine Auflistung von Bildern derselben Größe, auf die jeweils durch ihren Index verwiesen werden kann. Bildlisten werden verwendet, um große Mengen von Symbolen oder Bitmaps zu verwalten. Sie können bis zu drei verschiedene Bildlisten verwenden, um Schaltflächen in verschiedenen Zuständen anzuzeigen, wie in der folgenden Tabelle dargestellt.



|          |                                                                                                                                                                                              |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Normal   | Schaltflächen in Ihrem Standardzustand.                                                                                                                                                              |
| Hot      | Schaltflächen, die sich unter dem Zeiger befinden oder gedrückt werden. Heiße Elemente werden nur in Symbolleisten-Steuerelementen unterstützt, die über den [**\_ flachen Stil tbstyle**](toolbar-control-and-button-styles.md) verfügen. |
| Disabled | Schaltflächen, die deaktiviert sind.                                                                                                                                                                   |



 

Nach dem zerstören der Symbolleiste müssen Anwendungen alle von Ihnen erstellten Bildlisten freigeben.

## <a name="defining-text-for-buttons"></a>Definieren von Text für Schaltflächen

Jede Schaltfläche kann eine Zeichenfolge zusätzlich zu einem Bild anzeigen. Eine Symbolleiste verwaltet eine interne Liste, die alle für Symbolleisten Schaltflächen verfügbaren Zeichen folgen enthält. Fügen Sie der internen Liste Zeichen folgen mithilfe der [**TB \_ AddString**](tb-addstring.md) -Nachricht hinzu, und geben Sie dabei die Adresse des Puffers an, der die hinzu zufügenden Zeichen folgen enthält. Jede Zeichenfolge muss auf Null enden, und die letzte Zeichenfolge muss mit zwei NULL-Zeichen beendet werden.

Jede Zeichenfolge weist einen NULL basierten Index auf. Die erste Zeichenfolge, die der internen Liste von Zeichen folgen hinzugefügt wird, weist einen Index von 0, die zweite Zeichenfolge einen Index von 1 usw. auf. [**TB \_ AddString fügt Zeichen**](tb-addstring.md) folgen am Ende der Liste hinzu und gibt den Index der ersten neuen Zeichenfolge zurück. Sie verwenden den Index einer Zeichenfolge, um die Zeichenfolge einer Schaltfläche zuzuordnen.

Die Verwendung von [**TB \_ AddString**](tb-addstring.md) ist nicht die einzige Möglichkeit zum Hinzufügen von Zeichen folgen zu einer Symbolleiste. Sie können eine Zeichenfolge in einer Schaltfläche anzeigen, indem Sie einen Zeichen folgen Zeiger in den **IString** -Member der [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) -Struktur übergeben, der an [**TB \_ AddButtons**](tb-addbuttons.md)übergeben wird. Darüber hinaus können Sie [**TB \_ SetButtonInfo**](tb-setbuttoninfo.md) zum Zuweisen von Text zu einer Symbolleisten-Schaltfläche verwenden.

## <a name="adding-toolbar-buttons"></a>Hinzufügen von Schaltflächen

Wenn Sie zum Erstellen einer Symbolleiste die Funktion " [**dashatetoolbarex**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) " verwenden, können Sie der Symbolleiste Schaltflächen hinzufügen, indem Sie ein Array von [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) -Strukturen ausfüllen und die Adresse des Arrays im Funktions aufzurufen angeben. Die Funktion " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) " verfügt jedoch nicht über einen Parameter zum Übergeben einer **TBBUTTON** -Struktur. Mit " **kreatewindowex** " wird eine leere Symbolleiste erstellt, die Sie ausfüllen, indem Sie eine [**TB- \_ AddButtons**](tb-addbuttons.md) -Nachricht senden und die Adresse einer **TBBUTTON** -Struktur angeben.

Nachdem eine Symbolleiste erstellt wurde, können Sie Schaltflächen hinzufügen, indem Sie eine [**TB- \_ InsertButton**](tb-insertbutton.md) -oder [**TB \_ AddButtons**](tb-addbuttons.md) -Nachricht senden. Jede Schaltfläche wird durch eine [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) -Struktur beschrieben, die die Attribute der Schaltfläche definiert, einschließlich der Indizes der Zeichenfolge und Bitmap sowie Ihres Stils, Zustands, Befehls Bezeichners und von der Anwendung definierten 32-Bit-Werts.

> [!Note]  
> Wenn Sie zum Erstellen einer Symbolleiste die Funktion " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) " verwenden, müssen Sie vor dem Hinzufügen von Schaltflächen die [**TB- \_ buttonstructsize**](tb-buttonstructsize.md) -Nachricht senden. Die Meldung übergibt die Größe der [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) -Struktur an die Symbolleiste.

 

### <a name="toolbar-button-styles"></a>Toolbar-Schaltflächen Stile

Der Stil einer Schaltfläche bestimmt, wie die Schaltfläche angezeigt wird und wie Sie auf Benutzereingaben reagiert. Beispielsweise erstellt der [**btns- \_ Schalt**](toolbar-control-and-button-styles.md) Flächen Stil eine Symbolleisten-Schaltfläche, die sich wie eine Standard-Push-Schaltfläche verhält Eine Schaltfläche mit dem [**btns- \_ Häkchen**](toolbar-control-and-button-styles.md) ähnelt einer Standard-Push-Schaltfläche, mit der Ausnahme, dass Sie jedes Mal zwischen den gedrückten und nicht gedrückten Zuständen umschaltet, wenn der Benutzer darauf klickt.

Sie können Gruppen von Symbolleisten Schaltflächen erstellen, die wie Options Felder mithilfe der [**btns- \_ Gruppe**](toolbar-control-and-button-styles.md) oder des [**btns \_ CheckGroup**](toolbar-control-and-button-styles.md) -Stils fungieren. Dies bewirkt, dass eine Schaltfläche gedrückt bleibt, bis der Benutzer eine andere Schaltfläche in der Gruppe auswählt. Eine Gruppe ist als zusammenhängende Auflistung von Schaltflächen definiert, und zwar alle mit der **btns- \_ Gruppe** oder dem **btns \_ CheckGroup** -Stil.

Der [**btns \_ Sep**](toolbar-control-and-button-styles.md) -Stil erstellt eine kleine Lücke zwischen Schaltflächen oder zeichnet eine zwischen Schaltflächen auf flachen Symbolleisten. Eine Schaltfläche mit dem **btns \_ Sep** -Stil empfängt keine Benutzereingaben.

In Version 5,80 der allgemeinen Steuerelemente wurden einige neue Symbolleisten-Schaltflächen Stile eingeführt und einige ältere Stile umbenannt. Alle Schaltflächen-stilflags beginnen jetzt mit btns \_ xxx anstelle von tbstyle \_ xxx. Eine Auflistung und Erörterung der Schaltflächen Stile finden Sie unter [Symbolleisten-Steuerelement und Schalt](toolbar-control-and-button-styles.md)Flächen Formate.

### <a name="toolbar-button-states"></a>Symbolleisten Schaltflächen

Jede Schaltfläche in einer Symbolleiste hat einen Zustand. Die Symbolleiste aktualisiert den Zustand einer Schaltfläche, um Benutzeraktionen wie das Klicken auf die Schaltfläche widerzuspiegeln. Der Status gibt an, ob die Schaltfläche derzeit gedrückt oder nicht gedrückt, aktiviert oder deaktiviert, ausgeblendet oder sichtbar ist. Obwohl eine Anwendung den Anfangszustand einer Schaltfläche festlegt, wenn die Schaltfläche der Symbolleiste hinzugefügt wird, kann Sie den Zustand ändern und abrufen, indem [**TB \_ GetState**](tb-getstate.md) -und [**TB- \_ SetState**](tb-setstate.md) -Meldungen an die Symbolleiste gesendet werden. Eine Liste der Symbolleisten-Schaltflächen Zustände finden Sie unter [Toolbar States](toolbar-button-states.md).

### <a name="command-identifier"></a>Befehls Bezeichner

Jeder Schaltfläche ist ein Anwendungs definierter Befehls Bezeichner zugeordnet. Schaltflächen Bezeichner werden in der Regel in einer Anwendungs Header Datei definiert. Beispielsweise kann eine Schaltfläche einfügen wie folgt definiert werden:


```
#define ID_PASTE 100
```



Wenn der Benutzer eine Schaltfläche auswählt, sendet die Symbolleiste dem übergeordneten Fenster einen [**WM- \_ Befehl**](/windows/desktop/menurc/wm-command) oder eine [**WM- \_ Benachrichtigungs**](wm-notify.md) Meldung, die den Befehls Bezeichner der Schaltfläche enthält. Das übergeordnete Fenster überprüft den Befehls Bezeichner und führt den Befehl aus, der der Schaltfläche zugeordnet ist. Informationen dazu, wann von Steuerelementen **WM- \_ Befehls** Nachrichten gesendet werden und wann die **WM- \_ Benachrichtigung** gesendet wird, finden Sie im Abschnitt "Hinweise" in der [**WM- \_ Benachrichtigung**](wm-notify.md) .

### <a name="button-size-and-position"></a>Schaltflächen Größe und-Position

Die Schaltflächen werden von einer Symbolleiste nachverfolgt, indem jeder Schaltfläche ein Positionsindex zugewiesen wird. Der Index ist NULL basiert. Das heißt, dass die linke linke Schaltfläche einen Index von 0 aufweist, die Schaltfläche weiter rechts einen Index von 1 usw. Eine Anwendung muss den Index einer Schaltfläche angeben, wenn Nachrichten gesendet werden, um Informationen über die Schaltfläche abzurufen oder die Attribute der Schaltfläche festzulegen.

Eine Symbolleiste aktualisiert die Positions Indizes, wenn Schaltflächen eingefügt und entfernt werden. Eine Anwendung kann den aktuellen Positionsindex einer Schaltfläche abrufen, indem die [**TB \_ commanddeindex**](tb-commandtoindex.md) -Nachricht verwendet wird. Die Meldung gibt den Befehls Bezeichner einer Schaltfläche an, und das Symbolleisten Fenster verwendet den Bezeichner, um die Schaltfläche zu suchen und den Positionsindex zurückzugeben.

Alle Schaltflächen in einer Symbolleiste haben dieselbe Größe. Die Funktion "up [**toolbarex**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) " erfordert, dass Sie beim Erstellen der Symbolleiste die anfängliche Größe der Schaltflächen festlegen. Wenn Sie die Funktion " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) " verwenden, wird die Anfangs Größe auf die Standardabmessungen von 24 x 22 Pixel festgelegt. Sie können die [**TB- \_ setbuttonsize**](tb-setbuttonsize.md) -Nachricht verwenden, um die Schaltflächen Größe zu ändern, aber Sie müssen dies tun, bevor Sie der Symbolleiste Schaltflächen hinzufügen. Die [**TB \_ GetItemRect**](tb-getitemrect.md) -Nachricht Ruft die aktuellen Dimensionen der Schaltflächen ab.

Wenn Sie eine Zeichenfolge hinzufügen, die länger als jede Zeichenfolge ist, die sich derzeit in der Symbolleiste befindet, wird die Breite der Schaltflächen automatisch von der Symbolleiste Die Breite wird so festgelegt, dass die längste Zeichenfolge auf der Symbolleiste berücksichtigt wird.

## <a name="enabling-customization"></a>Aktivieren der Anpassung

Eine Symbolleiste verfügt über integrierte Anpassungs Features, die Sie dem Benutzer zur Verfügung stellen können, indem Sie der Symbolleiste den Stil für die [**CCS- \_ anpassbare**](common-control-styles.md) allgemeine Steuerung erteilen. Die Anpassungsfunktionen ermöglichen es dem Benutzer, eine Schaltfläche an eine neue Position zu ziehen oder eine Schaltfläche zu entfernen, indem er sie von der Symbolleiste zieht. Darüber hinaus kann der Benutzer auf die Symbolleiste doppelklicken, um das Dialogfeld Symbolleiste anpassen anzuzeigen, in dem der Benutzer Symbolleistenschaltflächen hinzufügen, löschen und neu anordnen kann. Um das Dialogfeld anzuzeigen, verwenden Sie die Meldung " [**TB \_ Anpassen**](tb-customize.md) ". Eine Anwendung bestimmt, ob die Anpassungs Features für den Benutzer verfügbar sind, und steuert das Ausmaß, in dem der Benutzer die Symbolleiste anpassen kann.

Im Rahmen des Anpassungsprozesses müssen Anwendungen häufig den Zustand einer Symbolleiste speichern und wiederherstellen. Beispielsweise speichern viele Anwendungen den Symbolleisten Status, bevor der Benutzer mit dem Anpassen der Symbolleiste beginnt, falls der Benutzer die Symbolleiste später in seinem ursprünglichen Zustand wiederherstellen möchte. Das Symbolleisten-Steuerelement behält nicht automatisch einen Datensatz seines vorab Anpassungs Zustands bei. Die Anwendung muss den Symbolleisten Zustand speichern, damit Sie wieder hergestellt werden kann. Weitere Informationen finden Sie unter [Verwenden von Symbol](using-toolbar-controls.md)leisten-Steuerelementen.

## <a name="enabling-hot-tracking"></a>Aktivieren der Hot-Tracking-Lösung

Hot-Tracking bedeutet, dass sich die Darstellung der Schaltfläche ändert, wenn der Mauszeiger über ein Element bewegt wird. Wenn visuelle Stile aktiviert sind, unterstützen Symbolleisten die Hot-Tracking standardmäßig. Andernfalls unterstützen nur Symbolleisten-Steuerelemente, die mit dem [**tbstyle- \_ FlatStyle**](toolbar-control-and-button-styles.md) erstellt wurden, die Nachverfolgung Sie können andere Fenster Stile in Kombination mit **tbstyle \_ Flat** verwenden, um Symbolleisten zu generieren, die eine heiße Nachverfolgung ermöglichen, aber eine andere Darstellung von einer flachen Symbolleiste haben. Weitere Informationen finden Sie unter [Verwenden von Symbol](using-toolbar-controls.md)leisten-Steuerelementen.

 

 