---
title: Schriftarten
description: Benutzer interagieren mit Text mehr als mit einem beliebigen anderen Element in Microsoft Windows. Segoe UI (ausgesprochen \ 0034; Siehe-go \ 0034;) die Schriftart des Windows-Systems. Die Standardschrift Größe wurde auf 9 Punkt angehoben.
ms.assetid: 6d4f669d-d28c-4585-9bc3-ecda44de6df5
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 6c5fad1459d4ce45f2d677d4bd5864d89b125e4e
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "103761223"
---
# <a name="fonts"></a>Schriftarten

> [!NOTE]
> Dieses Entwurfs Handbuch wurde für Windows 7 erstellt und wurde für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele entsprechen nicht unseren [aktuellen Entwurfs Anleitungen](/windows/uwp/design/).

Benutzer interagieren mit Text mehr als mit einem beliebigen anderen Element in Microsoft Windows. Segoe UI (ausgesprochen "See-Go") ist die Schriftart des Windows-Systems. Die Standardschrift Größe wurde auf 9 Punkt angehoben.

![Abbildung von Alphabet in der Schriftart der Benutzeroberfläche in der Benutzeroberfläche ](images/vis-fonts-image1.png)

Die Segoe UI Schriftart.

Segoe UI und "abgoe" sind nicht die gleiche Schriftart. Segoe UI ist die für Text Zeichenfolgen der Benutzeroberfläche vorgesehene Windows-Schriftart. "Abgoe" ist eine brandingschriftart, die von Microsoft und Partnern verwendet wird, um Material für Print und Werbung zu liefern.

Segoe UI ist eine genehmigbare, offene und freundliche Schriftart, die eine bessere Lesbarkeit bietet als Tahoma, Microsoft Sans Serif und Arial. Es verfügt über die Merkmale eines humanistischen Sans Serif: die unterschiedlichen Breiten der Hauptstädte (schmale E und S, z. b. im Vergleich zu "Helvetica", bei denen die breiten ähnlicher, ziemlich breit sind); der Belastungs-und letterforms-Wert in Kleinbuchstaben; und die tatsächliche kursiv Formatierung (statt einer "schrägen" oder einer schrägen römischen, wie viele Industrie aussehende Sans serifs). Die Schriftart soll den gleichen visuellen Effekt auf dem Bildschirm und in Druck gestalten. Es wurde als humaner Sans-Serif ohne starkes Zeichen oder als ablenkend gedacht entwickelt.

Segoe UI ist für ClearType optimiert, das in Windows standardmäßig aktiviert ist. Bei aktiviertem ClearType ist Segoe UI eine elegante, lesbare Schriftart. Ohne aktivierten ClearType ist Segoe UI nur geringfügig akzeptabel. Dieser Faktor bestimmt, wann Segoe UI verwendet werden soll.

Segoe UI umfasst lateinische, Griechisch, Kyrillisch und arabische Zeichen. Es gibt neue Schriftarten, die auch für ClearType optimiert sind und für andere Zeichensätze und Verwendungszwecke erstellt wurden. Hierzu gehören meiryo für Japanisch, Malgun-Gotik für Koreanisch, Microsoft jhenghei für Chinesisch (traditionell), Microsoft YaHei für Chinesisch (vereinfacht), gisha für Hebräisch und Leelawadee für Thai und die für die Verwendung von Dokumenten vorgesehenen ClearType-Auflistungs Schriftarten.

Meiryo enthält lateinische Zeichen, die auf Verdana basieren. Malgun Gothic, Microsoft jhenghei und Microsoft YaHei verwenden einen angepassten Segoe UI. Die Verwendung Kursiv Versionen dieser Schriftarten wird nicht empfohlen. Malgun Gothic, Microsoft jhenghei und Microsoft YaHei werden nur in regulären und fett formatierten Stilen bereitgestellt, was bedeutet, dass kursiv formatierte Zeichen durch das Durchlaufen der Aufhebungs Stile synthetisiert werden. Obwohl meiryo echte kursiv formatierte und Fett formatierte Formatierungen enthält, gelten diese Stile nur für die lateinischen Zeichen, wenn die kursiv Formatierung angewendet wird.

Eine Variation von meiryo, dem Namen meiryo UI, wird in der Benutzeroberfläche des Multifunktionsleisten [-Befehls bevorzugt](cmd-ribbons.md) .

Zur Unterstützung von Gebiets Schemas, die diese Zeichensätze verwenden, wird Segoe UI abhängig von den einzelnen Gebiets Schemata während des [Lokalisierungs](glossary.md) Prozesses durch die richtigen Schriftarten ersetzt.

Um Segoe UI und andere Microsoft-Schriftarten für die Verteilung mit einem Windows-basierten Programm zu lizenzieren, wenden Sie sich an [Monotype](https://www.monotype.com/).

**Hinweis:** Richtlinien, die sich auf den Text [Stil und Ton](text-style-tone.md) und [Benutzeroberfläche](text-ui.md) beziehen, werden in separaten Artikeln dargestellt.

## <a name="design-concepts"></a>Entwurfskonzepte

### <a name="fonts-typefaces-point-sizes-and-attributes"></a>Schriftarten, schriftflächen, Punktgrößen und Attribute

Bei der herkömmlichen Typographie beschreibt eine Schriftart eine Kombination aus Schriftart, Punktgröße und Attributen. Eine Schriftart ist das Aussehen der Schriftart. Segoe UI, Tahoma, Verdana und Arial sind alle typegesichter. Die Punktgröße bezieht sich auf die Größe der Schriftart, gemessen vom oberen Rand der Vorgänger bis zum unteren Rand der untergeordneten Elemente, abzüglich des internen Abstands (als "Leading" bezeichnet). Ein Punkt ist ungefähr 1/72 Zoll. Schließlich kann eine Schriftart fett formatierte oder kursiv formatierte Attribute aufweisen.

Informell verwenden Benutzer häufig Schriftart anstelle der Schriftart in diesem Artikel, aber technisch gesehen Segoe UI eine Schriftart und keine Schriftart ist. Jede Kombination von Attributen ist eine eindeutige Schriftart (z. b. 9 Punkt Segoe UI regulär, 10 Punkt Segoe UI Fett usw.).

### <a name="serif-and-sans-serif"></a>Serif und Sans Serif

Typegesichter sind entweder Serif oder Sans Serif. Serif bezieht sich auf kleine Turn-Einheiten, die häufig die Striche von Buchstaben in einer Schriftart beenden. Eine Sans-Serif-Schriftart weist kein serifs auf.

Leser bevorzugen im allgemeinen Serif-Schriftarten, die als Textkörper innerhalb eines Dokuments verwendet werden. Der Serifen an bietet ein Gefühl der Formalität und Eleganz eines Dokuments. Der Benutzeroberflächen Text sorgt für eine saubere Darstellung und die geringere Auflösung von Computermonitoren dafür, dass Sans Serif die bessere Wahl ist.

### <a name="contrast"></a>Vergleichen Sie

Der Text ist am einfachsten zu lesen, wenn es einen großen Unterschied zwischen der Beleuchtung des Texts und dem Hintergrund gibt. Der schwarze Text auf einem weißen Hintergrund gibt den höchsten Kontrast an, den der dunkle Text in einem sehr hellen Hintergrund hervorragend hervorbringen kann. Diese Kombination eignet sich am besten für primäre Benutzeroberflächen Oberflächen.

Heller Text auf einem dunklen Hintergrund bietet einen guten Kontrast, aber nicht so gut wie dunkler Text auf einem hellen Hintergrund. Diese Kombination eignet sich gut für sekundäre Benutzeroberflächen Oberflächen, wie z. b. Explorer-Aufgabenbereiche, die Sie in Relation zu den primären Benutzeroberflächen Oberflächen hervorheben möchten.

**Wenn Sie sicherstellen möchten, dass Benutzer Ihren Text lesen, verwenden Sie den dunklen Text auf einem hellen Hintergrund.**

### <a name="affordances"></a>Kostengünstig

Der Text kann anhand der [folgenden Möglichkeiten](glossary.md) angeben, wie er verwendet wird:

-   **Zeichner.** Der I-Bar-Zeiger ("Text Select") gibt an, dass der Text auswählbar ist, während der nach links zeigenden Pfeil ("normaler Select"-Zeiger) angibt, dass der Text nicht ist.
-   **Einfügemarke.** Wenn Text den Eingabefokus besitzt, ist die Einfügemarke der blinkende senkrechte Strich, der den Einfügungs-oder Auswahl Punkt in auswählbaren oder bearbeitbaren Text
-   **Chens.** Ein Feld um Text, das angibt, dass es bearbeitet werden kann. Um das Gewicht der Präsentation zu reduzieren, wird das Feld möglicherweise nur dynamisch angezeigt, wenn der bearbeitbare Text ausgewählt ist.
-   **Vordergrundfarbe.** Hellgrau gibt an, dass der Text deaktiviert ist. Nicht graue Farben (besonders blau und lila) geben an, dass der Text ein Link ist.
-   **Hintergrundfarbe.** Ein heller grauer Hintergrund weist darauf hin, dass der Text schreibgeschützt ist. in der Praxis kann Schreib geschützter Text aber einen beliebigen Hintergrund aufweisen.

Diese Kosten werden für folgende Bedeutungen kombiniert:

-   **Bearbeitet.** Text, der in einem Feld mit einem Text Select-Zeiger, einer Einfügemarke (beim Eingabefokus) und in der Regel in einem weißen Hintergrund angezeigt wird.
-   **Schreibgeschützt, auswählbar.** Text mit einem SELECT-Zeiger und einem Caretzeichen (im Eingabefokus).
-   **Schreibgeschützt, nicht auswählbar.** Text mit einem Pfeil Zeiger.
-   **Deaktiviert.** Heller grauer Text mit einem Pfeil Zeiger, der manchmal in einem grauen Hintergrund angezeigt wird.

Schreib geschützter Text hat normalerweise einen grauen Hintergrund, aber ein grauer Hintergrund ist nicht erforderlich. Tatsächlich kann ein grauer Hintergrund unerwünscht sein, insbesondere für große Textblöcke, da er vorschlägt, dass der Text deaktiviert ist, und das Lesen verhindert.

### <a name="accessibility-and-the-system-font-sizes-and-colors"></a>Barrierefreiheit und die Schriftart, Größe und Farben des Systems

Die Richtlinien, die für Benutzer mit Behinderungen oder Beeinträchtigungen zugänglich gemacht werden können, können in eine einfache Regel integriert werden: Beachten Sie die Benutzereinstellungen, indem Sie immer die Schriftart, die Größe und die Farben des Systems verwenden.

**Wenn Sie nur eine Aktion ausführen...**

Beachten Sie die Benutzereinstellungen, indem Sie immer die Schriftart, die Größe und die Farben des Systems verwenden.

**Entwickler:** Im Code können Sie die Eigenschaften der System Schriftart (einschließlich ihrer Größe) mithilfe der gettemefont-API-Funktion bestimmen. Die Systemfarben können mithilfe der getthemesyscolor-API-Funktion bestimmt werden.

Da Sie keine Annahmen über die Systemdesign Einstellungen des Benutzers treffen können, sollten Sie folgende Schritte ausführen:

-   Basieren Sie stets auf den Farben und Hintergründen der Schriftart auf die Farben des Systemdesigns. Erstellen Sie niemals Ihre eigenen Farben auf der Grundlage fester RGB-Werte (rot, grün, blau).
-   Vergleichen Sie die System Textfarben stets mit ihren entsprechenden Hintergrundfarben. Wenn Sie z. b. für \_ die Textfarbe Color StaticText auswählen, müssen Sie auch Color \_ static als Hintergrundfarbe auswählen.
-   Erstellen Sie immer neue Schriftarten auf der Grundlage von Variationen der System Schriftart mit proportionaler Größenanpassung. Mit den Schriftart Metriken für das System können Sie Fett formatierte, kursiv, größere und kleinere Variationen erstellen.

**Eine einfache Möglichkeit, um sicherzustellen, dass das Programm die Benutzereinstellungen respektiert, besteht darin, einen anderen Schrift Grad und ein Farbschema mit hohem Kontrast zu testen.** Der gesamte Text sollte die Größe ändern und im ausgewählten Farbschema ordnungsgemäß angezeigt werden.

## <a name="usage-patterns"></a>Verwendungsmuster

Text weist mehrere Verwendungs Muster auf:



|                                                                                                                                                                                                                                                           |                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Text der Titelleiste**<br/> Text auf der Titelleiste, der das Fenster identifiziert.<br/>                                                                                                                                                                | ![Beispiel für Text Schriftart der Titelleiste ](images/vis-fonts-image2.png)<br/>                                                                            |
| **Haupt Anleitung**<br/> Text, der erläutert, was für eine Seite, ein Fenster oder ein Dialogfeld zu tun ist. <br/>                                                                                                                                              | ![Beispiel für eine Text Schriftart in der Haupt Anleitung ](images/vis-fonts-image3.png)<br/>                                                                    |
| **Sekundäre Anweisungen**<br/> Zusätzlicher Text, in dem erläutert wird, was auf einer Seite, einem Fenster oder einem Dialogfeld durchzuführen ist. <br/>                                                                                                                            | ![Beispiel für eine Text Schriftart mit Sekundär Anweisungen ](images/vis-fonts-image4.png)<br/>                                                               |
| **Normaler Text**<br/> Normaler (Schreib geschützter) Text, der in einer Benutzeroberfläche angezeigt wird. <br/>                                                                                                                                                           | ![Beispiel für normale Text Schriftart ](images/vis-fonts-image5.png)<br/>                                                                               |
| **Hervorgehobene Text**<br/> Fett formatierter Text wird verwendet, um die Analyse des Texts zu vereinfachen und auf den Text, den Benutzer lesen müssen, aufmerksam zu machen. Kursiv Text wird verwendet, um buchstäblich auf Text (anstelle von Anführungszeichen) zu verweisen und bestimmte Wörter hervorzuheben. <br/> | ![Beispiel für hervorgehobene Text Schriftart ](images/vis-fonts-image6.png)<br/>                                                                           |
| **Bearbeitbarer Text**<br/> Text, der von Benutzern bearbeitet werden kann, wird in einem Feld angezeigt. um das Gewicht der Präsentation zu reduzieren, wird das Feld möglicherweise nur angezeigt, wenn der bearbeitbare Text ausgewählt ist. <br/>                                                          | ![Beispiel für eine bearbeitbare Text Schriftart ](images/vis-fonts-image7.png)<br/>                                                                             |
| **Deaktivierter Text**<br/> Text, der nicht auf den aktuellen Kontext angewendet wird, z. b. Bezeichnungen für deaktivierte Steuerelemente. der deaktivierte Text gibt an, dass Benutzer (normalerweise) keinen Lesevorgang für den Text <br/>                                           | ![Beispiel für deaktivierte Text Schriftart ](images/vis-fonts-image8.png)<br/>                                                                             |
| **Links**<br/> Text, der verwendet wird, um zu einer anderen Seite, einem anderen Fenster oder einem Hilfethema zu navigieren oder einen Befehl zu initiieren. <br/>                                                                                                                                     | ![Beispiel für Link Text Schriftart ](images/vis-fonts-image9.png)<br/> ![Beispiel für Verknüpfungs Text Schriftart (Hover) ](images/vis-fonts-image10.png)<br/> |
| **Gruppen Kopfzeile**<br/> Text, der verwendet wird, um Elemente in einer Listenansicht zu gruppieren. <br/>                                                                                                                                                                          | ![Beispiel für eine Textschriftart für Gruppen Kopfzeilen ](images/vis-fonts-image11.png)<br/>                                                                        |
| **Dateiname**<br/> Dateiname Text (nur in der Inhaltsansicht). <br/>                                                                                                                                                                               | ![Beispiel für einen Dateinamen (in der Inhaltsansicht) Text Schriftart ](images/vis-fonts-image12.png)<br/>                                                         |
| **Dokument Text**<br/> Text, der in Dokumenten verwendet wird (im Gegensatz zum Benutzeroberflächen Text). <br/>                                                                                                                                                                  | ![Beispiel für Dokument Text Schriftart ](images/vis-fonts-image13.png)<br/>                                                                            |
| **Dokument Überschriften**<br/> Text, der als Überschrift in einem Dokument verwendet wird. <br/>                                                                                                                                                                    | ![Beispiel für Text Schriftart für Dokument Überschriften ](images/vis-fonts-image14.png)<br/>                                                                   |



 

## <a name="guidelines"></a>Richtlinien

### <a name="fonts-and-colors"></a>Schriftarten und Farben

-   **Die folgenden Schriftarten und Farben sind Standardwerte für Windows Vista und Windows 7.**



|                                                                                               |                             |                                                            |
|-----------------------------------------------------------------------------------------------|-----------------------------|------------------------------------------------------------|
| **Muster**<br/>                                                                        | **Design Symbol**<br/> | **Schriftart, Farbe**<br/>                                 |
| ![Beispiel für Text Schriftart der Titelleiste ](images/vis-fonts-image2.png)<br/>                    | CaptionFont<br/>      | 9 pt. schwarz ( \# 000000) Segoe UI<br/>                 |
| ![Beispiel für eine Text Schriftart in der Haupt Anleitung ](images/vis-fonts-image3.png)<br/>            | Maininstruction<br/>  | 12 pt. blau ( \# 003399) Segoe UI<br/>                 |
| ![Beispiel für eine Text Schriftart mit Sekundär Anweisungen ](images/vis-fonts-image4.png)<br/>       | Anweisung<br/>      | 9 pt. schwarz ( \# 000000) Segoe UI<br/>                 |
| ![Beispiel für normale Text Schriftart ](images/vis-fonts-image5.png)<br/>                       | BodyText<br/>         | 9 pt. schwarz ( \# 000000) Segoe UI<br/>                 |
| ![Beispiel für hervorgehobene Text Schriftart ](images/vis-fonts-image6.png)<br/>                   | BodyText<br/>         | 9 pt. schwarz ( \# 000000) Segoe UI, Fett oder kursiv<br/> |
| ![Beispiel für eine bearbeitbare Text Schriftart ](images/vis-fonts-image7.png)<br/>                     | BodyText<br/>         | 9 pt. schwarz ( \# 000000) Segoe UI in einem Feld<br/>       |
| ![Beispiel für deaktivierte Text Schriftart ](images/vis-fonts-image8.png)<br/>                     | Disabled<br/>         | 9 pt. dunkelgrau ( \# 323232) Segoe UI<br/>             |
| ![Beispiel für Link Text Schriftart ](images/vis-fonts-image9.png)<br/>                         | Hyperlinktext<br/>    | 9 pt. Blue ( \# 0066cc)-Segoe UI<br/>                  |
| ![Beispiel für Verknüpfungs Text Schriftart (Hover) ](images/vis-fonts-image10.png)<br/>               | Hot<br/>              | 9 pt. hellblau ( \# 3399ff)-Segoe UI<br/>            |
| ![Beispiel für eine Textschriftart für Gruppen Kopfzeilen ](images/vis-fonts-image11.png)<br/>                |                             | 11 PT. blau ( \# 003399) Segoe UI<br/>                 |
| ![Beispiel für einen Dateinamen (in der Inhaltsansicht) Text Schriftart ](images/vis-fonts-image12.png)<br/> |                             | 11 PT. schwarz ( \# 000000) Segoe UI<br/>                |
| ![Beispiel für Dokument Text Schriftart ](images/vis-fonts-image13.png)<br/>                    | (none)<br/>           | 9 pt. schwarz ( \# 000000) Calibri<br/>                  |
| ![Beispiel für Text Schriftart für Dokument Überschriften ](images/vis-fonts-image14.png)<br/>           | (none)<br/>           | 17 PT. schwarz ( \# 000000) Calibri<br/>                 |



 

-   **Wählen Sie Schriftarten aus, und optimieren Sie die Fensterlayouts basierend auf der UI-Technologie und der Zielversion von Windows:**



|                                            |                                                       |                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------|-------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **UI-Technologie**<br/>               | **Windows-Zielversion**<br/>                 | **Zu verwendende Schriftarten und zum Optimieren**<br/>                                                                                                                                                                                                                                                                                                                     |
| Windows Presentation Foundation<br/> | Alle<br/>                                        | Verwenden Sie WPF-Design Teile.<br/>                                                                                                                                                                                                                                                                                                                                  |
| Win32 oder WinForms<br/>               | Windows Vista oder höher<br/>                     | Verwenden Sie die entsprechende Segoe UI Schriftart.<br/>                                                                                                                                                                                                                                                                                                                    |
|                                            | Erweiterbare Komponenten oder Pre-Windows Vista<br/> | Verwenden Sie zum als Ziel für Windows XP und Windows 2000 die Pseudo Schriftart 8 Punkt MS Shell Dlg 2, die Tahoma zugeordnet ist.<br/> Um auf frühere Versionen von Windows ausgerichtet zu sein, verwenden Sie 8-Punkt-MS Shell Dlg-Pseudo Schriftart, die Tahoma unter Windows 2000 und Windows XP zugeordnet ist, und MS Sans Serif unter Windows 95, Windows 98, Windows Millennium Edition und Windows NT 4,0.<br/> |



 

-   **Anbietern**
    -   Für Elemente, die ein festes Layout verwenden (z. b. Windows-Dialog Vorlagen und WinForms), wird die entsprechende Schriftart aus der vorangehenden Tabelle hart codiert.
    -   Verwenden Sie für Elemente, die dynamisches Layout verwenden (z. b. Windows Presentation Foundation), die Design Schriftarten. Verwenden Sie Design-APIs wie drawdermetext zum Zeichnen von Text auf der Grundlage des Design Symbols. Stellen Sie sicher, dass eine Alternative auf Systemmetriken basiert, falls der Design Dienst nicht ausgeführt wird.
-   **Verwenden Sie für Segoe UI eine Schriftgröße von 9 Punkten oder eine größere.** Die Segoe UI Schriftart ist für diese Größen optimiert, daher sollten kleinere Größen nicht verwendet werden.
-   **Vergleichen Sie die System Textfarben stets mit ihren entsprechenden Hintergrundfarben.** Wenn Sie z. b. für \_ die Textfarbe Color StaticText auswählen, müssen Sie auch Color \_ static als Hintergrundfarbe auswählen.
-   **Erstellen Sie immer neue Schriftarten auf der Grundlage von Variationen der System Schriftart mit proportionaler Größenanpassung.** Mit den Schriftart Metriken für das System können Sie Fett formatierte, kursiv, größere und kleinere Variationen erstellen.
-   Zeigen Sie große Blöcke mit Schreib geschütztem Text (z. b. Lizenzbedingungen) vor einem hellen Hintergrund anstelle eines grauen Hintergrunds an. Graue Hintergründe deuten darauf hin, dass der Text deaktiviert ist und das Lesen verhindert.
-   Stellen Sie **eine maximale Zeilenlänge von 65 Zeichen in Erwägung** , damit der Text leichter lesbar ist. (Zeichen umfassen Buchstaben, Interpunktions Zeichen und Leerzeichen.)

### <a name="attributes"></a>Attribute

-   Die meisten Benutzeroberflächen Texte sollten ohne Attribute einfach sein. Attribute können wie folgt verwendet werden:
    -   **Bold.** Verwenden Sie in Steuerelement Bezeichnungen, um den Text leichter analysieren zu können. Verwenden Sie sparsam, um den Text zu zeichnen, den Benutzer lesen müssen. Wenn Sie zu viel fett formatieren, verringert sich die Auswirkung.
    -   **Kursiv.** Verwenden Sie, um buchstäblich anstelle von Anführungszeichen auf Text zu verweisen. Verwenden Sie sehr sparsam, um bestimmte Wörter hervorzuheben. Verwenden Sie dies für [Eingabe Aufforderungen](glossary.md) in [Textfeldern](ctrl-text-boxes.md) und [bearbeitbaren Dropdown Listen](/windows/desktop/uxguide/ctrl-drop).
    -   **Fett formatiert.** Verwenden Sie nicht.
    -   **Streichen.** Verwenden Sie nicht mit Ausnahme von Links. Verwenden Sie stattdessen kursiv formatiert.
-   Nicht alle Schriftarten unterstützen Fett und kursiv, daher sollten Sie nie entscheidend sein, um den Text besser zu verstehen.

