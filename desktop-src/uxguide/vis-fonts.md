---
title: Schriftarten
description: Benutzer interagieren mehr mit Text als mit jedem anderen Element in Microsoft Windows. Segoe UI (ausgesprochen \ 0034; SEE-go \ 0034;) ist die Windows-Systemschriftart. Der Standardschriftgrad wurde auf 9 Punkte erhöht.
ms.assetid: 6d4f669d-d28c-4585-9bc3-ecda44de6df5
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: b74c9a593cb8d73d67464133042dfcf0aef7eb74
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444571"
---
# <a name="fonts"></a>Schriftarten

> [!NOTE]
> Dieser Entwurfsleitfaden wurde für Windows 7 erstellt und für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt immer noch im Prinzip, aber die Präsentation und die Beispiele spiegeln nicht unsere [aktuellen Entwurfsleitfäden](/windows/uwp/design/)wider.

Benutzer interagieren mehr mit Text als mit jedem anderen Element in Microsoft Windows. Segoe UI (ausgesprochen "SEE-go") ist die Windows-Systemschriftart. Der Standardschriftgrad wurde auf 9 Punkte erhöht.

![Abbildung des Alphabets in der Schriftart "segoe ui" ](images/vis-fonts-image1.png)

Die schriftart Segoe UI.

Segoe UI und Segoe sind nicht die gleiche Schriftart. Segoe UI ist die Windows-Schriftart für Textzeichenfolgen auf der Benutzeroberfläche. Segoe ist eine Brandingschriftart, die von Microsoft und Partnern verwendet wird, um Material für Druck und Werbung zu erzeugen.

Segoe UI ist eine ansprechbare, offene und benutzerfreundliche Schriftart und hat daher eine bessere Lesbarkeit als Tahoma, Microsoft Sans Serif und Arial. Sie weist die Merkmale eines humanistischen Sans serifens auf: die unterschiedlichen Breiten der Großbuchstaben (z. B. schmales E und S im Vergleich zu Helvetica, wo die Breiten gleich und relativ breit sind); die Belastungs- und Buchstabenformen des Kleinbuchstabens; und seine wahren italischen (anstelle einer "obszönen" oder schrägen romanischen, wie vielen industrieähnlichen Sans-Serifen). Die Schriftart soll den gleichen visuellen Effekt auf dem Bildschirm und im Druck erzielen. Es wurde so konzipiert, dass es sich um einen humanistischen Sans-Serifen ohne starke Zeichen oder ablenkende Stille handelt.

Segoe UI ist für ClearType optimiert, das in Windows standardmäßig aktiviert ist. Wenn ClearType aktiviert ist, ist Segoe UI eine elegante, lesbare Schriftart. Wenn ClearType nicht aktiviert ist, ist Segoe UI nur geringfügig akzeptabel. Dieser Faktor bestimmt, wann Sie Segoe UI verwenden sollten.

Segoe UI enthält lateinische, lateinische, kyrillische und arabische Zeichen. Es gibt neue Schriftarten, die auch für ClearType optimiert sind und für andere Zeichensätze und -verwendungen erstellt wurden. Dazu gehören Wiegeryo für Japanisch, MalgunOse für Koreanisch, Microsoft JhengHei für Chinesisch (traditionell), Microsoft YaHei für Chinesisch (vereinfacht), Gisha für Hebräisch und Leechatadee für Thailändisch und die ClearType Collection-Schriftarten, die für die Dokumentverwendung entwickelt wurden.

Dieses Enthält lateinische Zeichen, die auf Verdana basieren. MalgunGot, Microsoft JhengHei und Microsoft YaHei verwenden eine benutzerdefinierte Segoe UI. Die Verwendung von italischen Versionen dieser Schriftarten wird nicht empfohlen. Malgun Styles, Microsoft JhengHei und Microsoft YaHei werden nur in regulären und fett formatierten Formaten bereitgestellt. Dies bedeutet, dass kursiv formatierte Zeichen synthetisiert werden, indem die stileigen Stile nach oben synthetisiert werden. Obwohl Der Stil true kursiv und fett kursiv ist, gelten diese Stile nur für die lateinischen Zeichen, die japanische Zeichen bleiben aufrecht, wenn kursiv formatiert wird.

In der [Menübandbefehls-Benutzeroberfläche](cmd-ribbons.md) wird eine Variante von Sollryo bevorzugt, die als Ui bezeichnet wird.

Um Gebietsschemas mit diesen Zeichensätzen zu unterstützen, wird Segoe UI je nach Gebietsschema während des [Lokalisierungsprozesses](glossary.md) durch die richtigen Schriftarten ersetzt.

Wenden Sie sich an [Monotype](https://www.monotype.com/), um Segoe UI und andere Microsoft-Schriftarten für die Verteilung mit einem Windows-basierten Programm zu lizenzen.

**Hinweis:** Richtlinien für [Stil und Ton](text-style-tone.md) und [Benutzeroberflächentext](text-ui.md) werden in separaten Artikeln vorgestellt.

## <a name="design-concepts"></a>Entwurfskonzepte

### <a name="fonts-typefaces-point-sizes-and-attributes"></a>Schriftarten, Schriftarten, Punktgrößen und Attribute

In der herkömmlichen Typografie beschreibt eine Schriftart eine Kombination aus Schriftart, Punktgröße und Attributen. Eine Schriftart ist das Aussehen der Schriftart. Segoe UI, Tahoma, Verdana und Arial sind alle Schriftarten. Punktgröße bezieht sich auf die Größe der Schriftart, die von oben aufsteigend bis unten in den Nachfolgern gemessen wird, abzüglich des internen Abstands (als vorn bezeichnet). Ein Punkt beträgt ungefähr 1/72 Zoll. Schließlich kann eine Schriftart Fett- oder Kursivattribute aufweisen.

Informell verwenden Benutzer häufig Schriftart anstelle der Schriftart wie in diesem Artikel, aber technisch gesehen ist Segoe UI eine Schriftart und keine Schriftart. Jede Kombination von Attributen ist eine eindeutige Schriftart (z. B. 9 Punkt Segoe UI reguläre, 10 Punkt Segoe UI Fett usw.).

### <a name="serif-and-sans-serif"></a>Serifen- und Sans-Serifen

Schriftarten sind entweder serif oder sans serif. Serif bezieht sich auf kleine Drehungen, die häufig die Buchstabenstriche in einer Schriftart fertig stellen. Eine Serifenschrift "sans" hat keine Serifen.

Leser bevorzugen im Allgemeinen serifenschriftarten, die als Textkörper innerhalb eines Dokuments verwendet werden. Die Serifen vermitteln ein Gefühl der Formalität und der Vererbung zu einem Dokument. Für Benutzeroberflächentext ist die Notwendigkeit einer sauberen Darstellung und der niedrigeren Auflösung von Computermonitoren die bessere Wahl für sans serif-Schriftarten.

### <a name="contrast"></a>Vergleichen Sie

Text ist am einfachsten zu lesen, wenn ein großer Unterschied zwischen der Leuchtdichte des Texts und dem Hintergrund besteht. Schwarzer Text auf weißem Hintergrund bietet den höchsten kontrastreichen dunklen Text auf einem sehr hellen Hintergrund, der ebenfalls einen hohen Kontrast bieten kann. Diese Kombination eignet sich am besten für primäre Benutzeroberflächenoberflächen.

Helltext auf einem dunklen Hintergrund bietet einen guten Kontrast, aber nicht so gut wie dunkler Text auf einem hellen Hintergrund. Diese Kombination funktioniert gut für sekundäre Ui-Oberflächen, z. B. Explorer-Aufgabenbereiche, die Sie relativ zu den primären Ui-Oberflächen deaktivieren möchten.

**Wenn Sie sicherstellen möchten, dass Benutzer Ihren Text lesen, verwenden Sie dunklen Text auf hellem Hintergrund.**

### <a name="affordances"></a>Affordances

Text kann die folgenden [Möglichkeiten](glossary.md) verwenden, um anzugeben, wie er verwendet wird:

-   **Zeiger.** Der I-Bar-Zeiger ("Textauswahl") gibt an, dass der Text auswählbar ist, während der nach links zeigende Pfeil ("normal select") angibt, dass Text nicht ist.
-   **Einfügemarke.** Wenn Text den Eingabefokus besitzt, ist das Caretzeichen der blinkende vertikale Balken, der den Einfüge-/Auswahlpunkt in auswählbarem oder bearbeitbarem Text angibt.
-   **Box.** Ein Textfeld, das angibt, dass er bearbeitet werden kann. Um die Gewichtung der Präsentation zu reduzieren, kann das Feld nur dynamisch angezeigt werden, wenn der bearbeitbare Text ausgewählt ist.
-   **Vordergrundfarbe.** Hellgrau gibt an, dass Text deaktiviert ist. Nicht graue Farben, insbesondere Blau und Violett, geben an, dass Text ein Link ist.
-   **Hintergrundfarbe.** Ein hellgrauer Hintergrund deutet schwach darauf hin, dass Text schreibgeschützt ist, aber in der Praxis kann schreibgeschützter Text einen beliebigen Farbhintergrund aufweisen.

Diese Möglichkeiten werden für die folgenden Bedeutungen kombiniert:

-   **Bearbeitbaren.** Text, der in einem Feld mit einem Textauswahlzeiger, einem Caretzeichen (beim Eingabefokus) und in der Regel auf einem weißen Hintergrund angezeigt wird.
-   **Schreibgeschützt, auswählbar.** Text mit einem Auswahlzeiger und einem Caretzeichen (auf dem Eingabefokus).
-   **Schreibgeschützt, nicht auswählbar.** Text mit einem Pfeilzeiger.
-   **Deaktiviert.** Hellgrauer Text mit einem Pfeilzeiger, manchmal auf einem grauen Hintergrund.

Schreibgeschützter Text hat normalerweise einen grauen Hintergrund, aber ein grauer Hintergrund ist nicht erforderlich. Tatsächlich kann ein grauer Hintergrund unerwünscht sein, insbesondere bei großen Textblöcken, da er darauf hindeutet, dass der Text deaktiviert ist und vom Lesen abraten wird.

### <a name="accessibility-and-the-system-font-sizes-and-colors"></a>Barrierefreiheit und Die Schriftart, Größen und Farben des Systems

Die Richtlinien zum Zugänglichmachen von Text für Benutzer mit Behinderungen oder Beeinträchtigungen können auf eine einfache Regel festgelegt werden: Beachten Sie die Einstellungen des Benutzers, indem Sie immer die Schriftart, die Größen und die Farben des Systems verwenden.

**Wenn Sie nur eine Sache tun...**

Beachten Sie die Einstellungen des Benutzers, indem Sie immer die Systemschriftart, -größen und -farben verwenden.

**Entwickler:** Im Code können Sie die Eigenschaften der Systemschriftart (einschließlich ihrer Größe) mithilfe der GetThemeFont-API-Funktion bestimmen. Sie können die Systemfarben mithilfe der GetThemeSysColor-API-Funktion bestimmen.

Da Sie keine Annahmen über die Systemdesigneinstellungen von Benutzern treffen können, sollten Sie:

-   Basieren Sie ihre Schriftfarben und Hintergründe immer auf Systemdesignfarben. Erstellen Sie niemals eigene Farben basierend auf festen RGB-Werten (rot, grün, blau).
-   Stimmen Sie Systemtextfarben immer mit den entsprechenden Hintergrundfarben ab. Wenn Sie beispielsweise COLOR \_ STATICTEXT als Textfarbe auswählen, müssen Sie auch COLOR \_ STATIC als Hintergrundfarbe auswählen.
-   Erstellen Sie immer neue Schriftarten basierend auf variationen proportionaler Größe der Systemschriftart. Angesichts der Metriken der Systemschriftart können Sie fett, kursiv, größer und kleinere Variationen erstellen.

**Eine einfache Möglichkeit, um sicherzustellen, dass Ihr Programm die Benutzereinstellungen beachtet, ist das Testen mit einem anderen Schriftgrad und einem Farbschema mit hohem Kontrast.** Die Größe des gesamten Texts sollte im ausgewählten Farbschema ordnungsgemäß geändert und angezeigt werden.

## <a name="usage-patterns"></a>Verwendungsmuster

Text hat mehrere Verwendungsmuster:



|    Verwendung                                         |    BESCHREIBUNG                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Titelleistentext**<br/> Text auf der Titelleiste, der das Fenster identifiziert.<br/>                                                                                                                                                                | ![Beispiel für eine Textschriftart in der Titelleiste ](images/vis-fonts-image2.png)<br/>                                                                            |
| **Hauptanweisungen**<br/> Text, in dem erläutert wird, was auf einer Seite, einem Fenster oder einem Dialogfeld zu tun ist. <br/>                                                                                                                                              | ![Beispiel für die Textschriftart "main-instructions" ](images/vis-fonts-image3.png)<br/>                                                                    |
| **Sekundäre Anweisungen**<br/> Ergänzender Text, in dem erläutert wird, was auf einer Seite, einem Fenster oder einem Dialogfeld zu tun ist. <br/>                                                                                                                            | ![Beispiel für die Textschriftart "secondary-instructions" ](images/vis-fonts-image4.png)<br/>                                                               |
| **Normaler Text**<br/> Gewöhnlicher (schreibgeschützter) Text, der auf einer Benutzeroberfläche angezeigt wird. <br/>                                                                                                                                                           | ![Beispiel für normale Textschriftart ](images/vis-fonts-image5.png)<br/>                                                                               |
| **Hervorgehobener Text**<br/> Fett formatierten Text wird verwendet, um die Analyse des Texts zu vereinfachen und die Aufmerksamkeit auf Text zu ziehen, den Benutzer lesen müssen. Kursaler Text wird verwendet, um auf Text zu verweisen (anstelle von Anführungszeichen) und um bestimmte Wörter zu hervorheben. <br/> | ![Beispiel für eine hervorgehobene Textschriftart ](images/vis-fonts-image6.png)<br/>                                                                           |
| **Bearbeitbarer Text**<br/> Text, den Benutzer bearbeiten können, wird in einem Feld angezeigt. um die Gewichtung der Präsentation zu verringern, wird das Feld möglicherweise nur angezeigt, wenn der bearbeitbare Text ausgewählt ist. <br/>                                                          | ![Beispiel für eine bearbeitbare Textschriftart ](images/vis-fonts-image7.png)<br/>                                                                             |
| **Deaktivierter Text**<br/> Text, der nicht für den aktuellen Kontext gilt, z. B. Bezeichnungen für deaktivierte Steuerelemente. Deaktivierter Text gibt an, dass Benutzer (normalerweise) den Text nicht lesen sollten. <br/>                                           | ![Beispiel für deaktivierte Textschriftart ](images/vis-fonts-image8.png)<br/>                                                                             |
| **Links**<br/> Text, der verwendet wird, um zu einer anderen Seite, einem fenster oder einem Hilfethema zu navigieren oder einen Befehl zu initiieren. <br/>                                                                                                                                     | ![Beispiel für eine Linktextschriftart ](images/vis-fonts-image9.png)<br/> ![Beispiel für die Textschriftart "Links" (Hover) ](images/vis-fonts-image10.png)<br/> |
| **Gruppenheader**<br/> Text, der zum Gruppen von Elementen in einer Listenansicht verwendet wird. <br/>                                                                                                                                                                          | ![Beispiel für die Textschriftart "Gruppenheader" ](images/vis-fonts-image11.png)<br/>                                                                        |
| **Dateiname**<br/> Dateinamentext (nur in der Inhaltsansicht). <br/>                                                                                                                                                                               | ![Beispiel für die Textschriftart "Dateiname" (in der Inhaltsansicht) ](images/vis-fonts-image12.png)<br/>                                                         |
| **Dokumenttext**<br/> In Dokumenten verwendeter Text (im Gegensatz zu Benutzeroberflächentext). <br/>                                                                                                                                                                  | ![Beispiel für Dokumenttextschriftart ](images/vis-fonts-image13.png)<br/>                                                                            |
| **Dokumentüberschriften**<br/> Text, der als Überschrift in einem Dokument verwendet wird. <br/>                                                                                                                                                                    | ![Beispiel für die Textschriftart "Dokumentüberschriften" ](images/vis-fonts-image14.png)<br/>                                                                   |



 

## <a name="guidelines"></a>Richtlinien

### <a name="fonts-and-colors"></a>Schriftarten und Farben

-   **Die folgenden Schriftarten und Farben sind Standardwerte für Windows Vista und Windows 7.**



| Muster | Designsymbol | Schriftart, Farbe |
|-----------------------------------------------------------------------------------------------|-----------------------------|------------------------------------------------------------|
| ![Beispiel für eine Textschriftart in der Titelleiste ](images/vis-fonts-image2.png)<br/>                    | CaptionFont<br/>      | 9 pt. black ( \# 000000) Segoe UI<br/>                 |
| ![Beispiel für die Textschriftart "main-instructions" ](images/vis-fonts-image3.png)<br/>            | MainInstruction<br/>  | 12 Pt. blue ( \# 003399) Segoe UI<br/>                 |
| ![Beispiel für die Textschriftart "secondary-instructions" ](images/vis-fonts-image4.png)<br/>       | Anweisung<br/>      | 9 pt. black ( \# 000000) Segoe UI<br/>                 |
| ![Beispiel für normale Textschriftart ](images/vis-fonts-image5.png)<br/>                       | BodyText<br/>         | 9 pt. black ( \# 000000) Segoe UI<br/>                 |
| ![Beispiel für eine hervorgehobene Textschriftart ](images/vis-fonts-image6.png)<br/>                   | BodyText<br/>         | 9 pt. black ( \# 000000) Segoe UI, fett oder italisch<br/> |
| ![Beispiel für eine bearbeitbare Textschriftart ](images/vis-fonts-image7.png)<br/>                     | BodyText<br/>         | 9 pt. black ( \# 000000) Segoe UI, in einem Feld<br/>       |
| ![Beispiel für deaktivierte Textschriftart ](images/vis-fonts-image8.png)<br/>                     | Disabled<br/>         | 9 pt. dunkelgrau ( \# 323232) Segoe UI<br/>             |
| ![Beispiel für eine Linktextschriftart ](images/vis-fonts-image9.png)<br/>                         | HyperLinkText<br/>    | 9 pt. blue ( \# 0066CC) Segoe UI<br/>                  |
| ![Beispiel für die Textschriftart "Links" (Hover) ](images/vis-fonts-image10.png)<br/>               | heiße Ebene<br/>              | 9 pt. hellblau ( \# 3399FF) Segoe UI<br/>            |
| ![Beispiel für die Textschriftart "Gruppenheader" ](images/vis-fonts-image11.png)<br/>                |                             | 11 Pt. blue ( \# 003399) Segoe UI<br/>                 |
| ![Beispiel für die Textschriftart "Dateiname" (in der Inhaltsansicht) ](images/vis-fonts-image12.png)<br/> |                             | 11 Pt. black ( \# 000000) Segoe UI<br/>                |
| ![Beispiel für Dokumenttextschriftart ](images/vis-fonts-image13.png)<br/>                    | (none)<br/>           | 9 pt. black ( \# 000000) Calibri<br/>                  |
| ![Beispiel für die Textschriftart "Dokumentüberschriften" ](images/vis-fonts-image14.png)<br/>           | (none)<br/>           | 17 Pt. black ( \# 000000) Calibri<br/>                 |



 

-   **Wählen Sie Schriftarten aus, und optimieren Sie Fensterlayouts basierend auf der Benutzeroberflächentechnologie und der Zielversion von Windows:**



| Ui-Technologie | Windows-Zielversion | Zu verwendende und zu optimierende Schriftarten |
|--------------------------------------------|-------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Presentation Foundation<br/> | Alle<br/>                                        | Verwenden Sie WPF-Designteile.<br/>                                                                                                                                                                                                                                                                                                                                  |
| Win32 oder WinForms<br/>               | Windows Vista oder höher<br/>                     | Verwenden Sie die entsprechende Segoe UI Schriftart.<br/>                                                                                                                                                                                                                                                                                                                    |
|                                            | Erweiterbare Komponenten oder vor Windows Vista<br/> | Um Windows XP und Windows 2000 als Ziel zu verwenden, verwenden Sie die Pseudoschriftart 8 Punkt MS Shell Dlg 2, die Tahoma zugeordnet ist.<br/> Verwenden Sie für frühere Versionen von Windows die Ms Shell-Pseudoschriftart 8 Punkt, die Tahoma unter Windows 2000 und Windows XP und MS Sans Serif unter Windows 95, Windows 98, Windows Editions und Windows NT 4.0 zugeordnet ist.<br/> |



 

-   **Entwickler:**
    -   Für Elemente, die ein festes Layout verwenden (z. B. Windows-Dialogfeldvorlagen und WinForms), hart codieren Sie die entsprechende Schriftart aus der vorherigen Tabelle.
    -   Verwenden Sie für Elemente, die dynamisches Layout verwenden (z. B. Windows Presentation Foundation), die Designschriftarten. Verwenden Sie Design-APIs wie DrawThemeText, um Text basierend auf dem Designsymbol zu zeichnen. Stellen Sie sicher, dass Sie eine Alternative basierend auf Systemmetriken haben, falls der Designdienst nicht ausgeführt wird.
-   **Verwenden Sie für Segoe UI einen Schriftgrad von 9 Oder höher.** Die Segoe UI Schriftart ist für diese Größen optimiert, daher vermeiden Sie die Verwendung kleinerer Größen.
-   **Stimmen Sie Systemtextfarben immer mit den entsprechenden Hintergrundfarben ab.** Wenn Sie beispielsweise COLOR \_ STATICTEXT als Textfarbe auswählen, müssen Sie auch COLOR \_ STATIC als Hintergrundfarbe auswählen.
-   **Erstellen Sie immer neue Schriftarten basierend auf variationen proportionaler Größe der Systemschriftart.** Angesichts der Metriken der Systemschriftart können Sie fett, kursiv, größer und kleinere Variationen erstellen.
-   Zeigen Sie große Blöcke mit schreibgeschütztem Text (z. B. Lizenzbedingungen) vor einem hellen Hintergrund anstelle eines grauen Hintergrunds an. Graue Hintergründe deuten darauf hin, dass der Text deaktiviert ist und vom Lesen abraten.
-   **Ziehen Sie eine maximale Zeilenlänge von 65 Zeichen** in Betracht, um den Text leicht lesbar zu machen. (Zeichen enthalten Buchstaben, Interpunktionszeichen und Leerzeichen.)

### <a name="attributes"></a>Attribute

-   Der Großteil des Benutzeroberflächentexts sollte ohne Attribute klar sein. Attribute können wie folgt verwendet werden:
    -   **kühn.** Verwenden Sie in Steuerelementbezeichnungen, um die Analyse des Texts zu vereinfachen. Verwenden Sie sparingly , um die Aufmerksamkeit auf Text zu lenken, den Benutzer lesen müssen. Die Verwendung von zu viel Fett verringert die Auswirkungen.
    -   **Italic.** Verwenden Sie , um anstelle von Anführungszeichen auf Text zu verweisen. Verwenden Sie sparingly , um bestimmte Wörter hervorzuheben. Verwenden Sie für [Eingabeaufforderungen](glossary.md) in [Textfeldern](ctrl-text-boxes.md) und [bearbeitbaren Dropdownlisten.](/windows/desktop/uxguide/ctrl-drop)
    -   **Kursiv fett formatiert.** Nicht verwenden.
    -   **Unterstreichen.** Verwenden Sie nur Links. Verwenden Sie stattdessen zur Hervorhebung die italische.
-   Nicht alle Schriftarten unterstützen fett und kursiv, daher sollten sie nie entscheidend sein, um den Text zu verstehen.

