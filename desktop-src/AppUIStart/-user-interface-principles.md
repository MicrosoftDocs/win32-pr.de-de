---
title: Grundlagen der Benutzeroberfläche
description: In diesem Thema wird erläutert, wie intuitive Entwurfs Prinzipien für Benutzeroberflächen und Benutzeroberflächen in Windows-Anwendungen implementiert werden.
ms.assetid: 603bc184-3eec-4281-8caa-993834da3131
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98383f9379248570ef8b254c647ab8348d703696
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039362"
---
# <a name="user-interface-principles"></a>Grundlagen der Benutzeroberfläche

In diesem Thema wird erläutert, wie intuitive Entwurfs Prinzipien für Benutzeroberflächen und Benutzeroberflächen in Windows-Anwendungen implementiert werden.

-   [Introduction (Einführung)](#introduction)
-   [Grundlegende Prinzipien der richtigen Benutzeroberfläche](#the-basic-principles-of-proper-ui)
    -   [Abstand und Positionierung](#spacing-and-positioning)
    -   [Größe](#size)
    -   [Gruppierung](#grouping)
    -   [Intuitivität](#intuitiveness)
-   [20 Tipps für eine bessere, funktionale Benutzer Funktionalität](#20-tips-for-a-better-functional-user-experience)
    -   [Standards verwenden](#use-standards)
    -   [Wichtige Schaltflächen beachten](#draw-attention-to-important-buttons)
    -   [Erkennung durch Symbole vereinfachen](#simplify-recognition-with-icons)
    -   [Vereinfachen der Erkennung mit Headern](#simplify-recognition-with-headers)
    -   [Verwenden benutzerdefinierter Meldungs Felder](#use-custom-message-boxes)
    -   [Alternative Befehle einschließen](#include-alternate-commands)
    -   [Behandeln kritischer Aktionen](#how-to-handle-critical-actions)
    -   [Radiobuttons oder ComboBoxes?](#radiobuttons-or-comboboxes)
    -   [Stören Sie den Benutzer nie.](#never-disrupt-the-user)
    -   [Status Status angeben](#provide-progress-status)
    -   [Vereinfachen komplexer Schritte mit Assistenten](#simplify-complex-steps-with-wizards)
    -   [Den Text Ihres Texts rechts](#get-the-tone-of-your-text-right)
    -   [Manchmal ist eine ListView besser.](#sometimes-a-listview-is-better)
    -   [Vereinfachen Sie die Navigation mit Breadcrumb-Steuerelementen und-Steuerelementen.](#simplify-navigation-with-breadcrumb-controls-and-sidebars)
    -   [Verwenden von hübschen Grafiken](#use-pretty-graphics)
    -   [So können Sie nach Möglichkeit die Größe der Größe ändern](#provide-resizable-forms-when-possible)
    -   [Bereitstellen von mehr Funktionalität mit Sidebars/Aufgabenbereichen](#provide-more-functionality-with-sidebarstask-panes)
    -   [Benachrichtigungs Auswahl](#give-a-notification-choice)
    -   [Stellen Sie Quick Infos bereit!](#provide-tooltips)
    -   [Vergessen Sie nicht die kleinen Dinge](#do-not-forget-the-little-things)
-   [Zusammenfassung](#conclusion)

## <a name="introduction"></a>Einführung

Entwickler können die Perspektive des Endbenutzers oft nicht berücksichtigen. Entwickler arbeiten hart daran, die Anwendung funktionsfähig zu machen – Kunden erwarten nur, dass Sie funktioniert, und ihre Wahrnehmung der Software stellt diese Anforderung ein. Dies trifft vor allem dann zu, wenn Sie Einzelhandels Software entwickeln oder etwas, das von nichttechnischen Personen verwendet wird. Entwickler müssen die Anforderungen des Endbenutzers im gesamten Software Entwurfsprozess kennen.

Eine Software Anwendung muss so einfach zu navigieren und wie möglich verwendet werden. Mit der Menge der Software, die gerade erstellt wird, verfügen eine geschätzte 4 von 10 Softwareanwendungen über eine wirklich hervorragend benötigte Benutzeroberfläche, die der Endbenutzer wirklich gerne verwendet.

Eine riesige Menge an interner Software wird für Unternehmen erstellt. Egal, ob es intern oder im Rahmen der Pflege durch einen Berater entwickelt wurde – oft ist ein minimal Aufwand, Aufwand oder Geld in das Erstellen einer besseren Benutzeroberfläche investiert. Die Rolle "Designer" ist im Entwicklungs Cycle selten – besonders in der Welt der Windows-Anwendungen.

Es gibt einige grundlegende Regeln, die Sie befolgen sollten, um eine viel bessere und besser funktionierende Benutzeroberfläche für Ihre Anwendung zu erhalten. Es ist nicht zu viel Aufwand für Zeit oder Geld erforderlich, und es wird eine gute Rendite investiert.

Bevor wir fortfahren, wird die Benutzeroberfläche und die Benutzeroberfläche unterschieden – zumindest im Rahmen dieses Artikels. Die Benutzeroberfläche, die Benutzeroberfläche, bezieht sich auf die visuellen Elemente und Steuerelemente Ihrer Anwendung, während die Benutzererfahrung oder die Benutzeroberfläche die Benutzeroberfläche und das Verhalten der Anwendung, die mit der Benutzeroberfläche verknüpft ist, sowie das "Gefühl", das der Benutzer von Ihrer APP erhält, umfasst. Dabei geht es nicht nur um das Entwerfen einer hervorragend aussehenden Benutzeroberfläche, sondern auch um sicherzustellen, dass Sie auch hervorragend funktioniert.

Hier werden 20 Punkte des UX-Entwurfs erläutert, die Sie problemlos in Ihre Anwendungs Entwurfsphase integrieren können. Das Ergebnis sind umfangreichere Anwendungen mit besserer intuitiver Funktionalität – eine "menschliche Benutzerfreundlichkeit". Da wir alle wissen, dass die Windows Vista-Generierung von Anwendungen anders aussehen muss, muss Sie sich anders Verhalten. In diesem Thema erfahren Sie, wie Sie sich auf zukünftige Anwendungen vorbereiten und ihren aktuellen Benutzern einen Vorgeschmack auf die Zukunft geben.

In den folgenden Abschnitten werden die Grundlagen des richtigen UI-Entwurfs erläutert.

## <a name="the-basic-principles-of-proper-ui"></a>Grundlegende Prinzipien der richtigen Benutzeroberfläche

Eine professionell aussehende UX hängt von diesen vier Faktoren ab:

-   Abstand und Positionierung
-   Size
-   Gruppierung
-   Intuitivität

Bei Versionen von Microsoft Visual Studio vor 8,0 waren Abstand und Größenanpassung suboptimal. Ein 4X4-oder 8x8-Raster funktioniert nicht immer. Durch die Einbindung von Richtungslinien wurde der Prozess erheblich vereinfacht. In früheren Versionen von Visual Studio war es in früheren Versionen von Visual Studio äußerst schwierig, eine Bezeichnung mit einem Textfeld zu ausrichten oder noch schlimmer zu sein. Der Prozess wurde durch Richtungslinien erheblich vereinfacht.

In den folgenden Abschnitten werden vier der wichtigsten Aspekte des professionellen UX-Entwurfs beschrieben.

### <a name="spacing-and-positioning"></a>Abstand und Positionierung

Der Abstand zwischen zwei Steuerelementen ist wichtig. Der folgende Screenshot zeigt ein schlecht gestaltetes Eingabeformular für **Benutzerinformationen** – die beiden oberen Textfelder sind zu nah, die Liste darunter ist zu weit entfernt, und es gibt zahlreiche nicht genutzte Räume im Formular.

![Screenshot eines unzureichend entworfenen Formulars.](images/humanux-01.png)

Im folgenden Screenshot sehen Sie ein besser aussehende Dialogfeld mit ordnungsgemäßer Abstände und entsprechend großen Steuerelementen. Dies ist die gleiche Form wie im vorherigen Screenshot, aber es wurde geändert, um den von den Richtungslinien empfohlenen Abstand zu verwenden. Es wird immer empfohlen, eine Bezeichnung mit der TextBaseline des Textfelds oder eines anderen Steuer Elements neben dem eigentlichen unteren Rahmen des Steuer Elements auszurichten. Die Ausrichtungs Linien legen eine andere Farbe fest, wenn diese Ausrichtung erreicht wird, in der Regel nur ein paar Pixel oberhalb des unteren Rahmens.

![Screenshot eines besser entworfenen Formulars.](images/humanux-02.png)

Obwohl es keine genauen Regeln für Abstände gibt, bieten die Richtungslinien äußerst nützliche Richtlinien für den richtigen Abstand. Weitere Tools, mit denen Sie den richtigen Abstand behalten können, sind die Layoutsteuerelemente unter der Toolbox Gruppe Container. Das TableLayoutPanel-Steuerelement ist ebenfalls sehr hilfreich beim Erstellen von Dialogfeldern für das Eintrags Formular.

### <a name="size"></a>Size

Die gleichen Überlegungen gelten für die Größe. Wenn Sie eine Schaltfläche aus der Toolbox auf das Formular ziehen – diese hat die perfekte Höhe und Breite. Die maximale Breite wird empfohlen (es muss sich dabei um einen schwer wichtigen Grund befinden), die ursprüngliche Breite zu verdoppeln.

Wenn Sie sich das Fenster " **Ausführen** " im **Startmenü** oder im Dialogfeld " **Eigenschaften** " eines beliebigen Windows Explorer-Objekts ansehen, sind die Schaltflächen Größen "Just right". Wenn Sie über eine sehr wichtige Funktion verfügen, die der Endbenutzer ohne Fehler bemerken muss, gibt es andere Methoden als die Verwendung einer großen Schaltfläche oder von Gresh nicht Standardfarben (mehr dazu später).

In der folgenden Abbildung werden drei Schaltflächen angezeigt. Die erste Schaltfläche ist die empfohlene Größe und ist die standardmäßig erstellte Größe, wenn Sie aus der Toolbox gezogen (oder Doppel geklickt) werden. Manchmal erfordert zusätzlicher Text, dass Sie die Schaltfläche vergrößern. Die zweite Schaltfläche zeigt eine große, aber akzeptable Größe an. Es würde kein Chaos zum Anordnen anderer Steuerelemente erstellen. Die dritte Schaltfläche ist jedoch eine völlig unzulässige Größe. Sie sehen, dass es sogar etwas verzerrt das Design Bitmaps ist, das Windows zum Zeichnen von Design Steuerelementen verwendet. Außerdem wird es schwierig, andere Steuerelemente intuitiv zu schließen.

![Bild von drei Schaltflächen, die die Größe von links nach rechts vergrößern.](images/humanux-03.png)

### <a name="grouping&quot;></a>Gruppierung

In der Regel enthält eine Anwendung viele Steuerelemente. Nur durch die richtige, intuitive Gruppierung können Sie alle diese Steuerelemente leichter verwenden. Die Funktions basierte oder kategorisierte Gruppierung erfolgt am besten durch Registerkarten-Steuerelemente. Beispielsweise sind &quot;Accounts&quot;, &quot;Reports&quot;, &quot;Employees&quot; und &quot;Projects&quot; perfekte Kandidaten für Registerkarten in einer typischen Geschäftsanwendung. Gleich geordnete Gruppierung – Steuerelemente, die zum selben Endergebnis beitragen – werden am besten durch Gruppen Steuerelemente erreicht. Die Verwendung von Bereichen mit Rahmen für diese Gruppierung wird nicht empfohlen. Gruppen Steuerelemente sparen Ihnen die zusätzliche Gewichtung eines Label-Steuer Elements – insbesondere, wenn die untergeordneten Steuerelemente selbsterklärend sind.

Gruppen Steuerelemente innerhalb von Gruppen Steuerelementen werden nur dann empfohlen, wenn in einem großen Gruppen Steuerelement höchstens 2 oder drei vorhanden sind.

### <a name=&quot;intuitiveness&quot;></a>Intuitivität

Dies ist der wichtigste Aspekt eines hervorragend Benutzer Erlebnisses. Die intuitive UX verringert die Notwendigkeit von Erklärungen. Der Benutzer weiß genau, was die Steuerelemente tun.

Ein wichtiges Thema bei intuitivem Entwurf ist die Farbcodierung. Ein gutes Beispiel ist in Windows XP dargestellt, das neue weiche quadratische Schaltflächen für Funktionen wie Navigation in Designanwendungen, das **Abmelden** und **Ausschalten von Computer** Dialogfeldern und andere zeigt.

Die Farbgebung dieser Steuerelemente wurde basierend auf dem Schweregrad des Pushs der Schaltfläche bestimmt. Die Navigation ist grün, ähnlich wie ein &quot;Go&quot;-Verkehrs Licht. Herunterfahren, was zu einem möglichen Arbeits Verlust führen würde, wird wie ein Warnzeichen rot gefärbt. Semikritische Schaltflächen wie abmelden oder Ruhezustand sind gelb. Neutrale Schaltflächen, die keine kritischen Auswirkungen auf die Arbeitsprozesse des Benutzers haben, z. b. die Hilfe, sind eine weiche blaue Taste. Beim Erstellen einer häutigen Benutzeroberfläche sollten diese Farb Aspekte berücksichtigt werden.

Ein sehr gutes Beispiel für die Erkennung von Inhalten nach Farben ist Microsoft Office OneNote. Die Registerkarten der Anwendung können auf unterschiedliche Farben festgelegt werden, während Sie sich im Wesentlichen wie ein richtiger Teil des gesamten Windows XP-Entwurfs Stils ansehen.

Ein weiterer wichtiger Aspekt ist der Text in Ihren Anwendungen. Vor kurzem gab es verschiedene Bemühungen, die Sprache zu vereinfachen, die für die schriftlichen Anweisungen in Windows-Software verwendet wird. Die Verwendung von Text in Software wird später erläutert. Beachten Sie jedoch die folgenden kleinen, aber wichtigen Details.

MSN Messenger enthielt im Dialogfeld &quot; **Optionen** &quot; das Kontrollkästchen &quot;Freigeben von Webcam-Funktionen&quot;. Entwickler und Tech-Friendly Personen wissen, was das heißt, aber ein Anfänger könnte vielleicht denken, dass Sie einen anderen Benutzer am anderen Ende Ihres Chats verwenden können. In einer neueren Version wurde Sie in &quot;Meine Webcam&quot; geändert, damit andere Benutzer sehen können, dass ich über eine Webcam verfüge. Dies eignet sich perfekt für die Zielgruppe, die möglicherweise keine technischen Kenntnisse hat und für die einfache Sprache verwendet wird.

Obwohl es einfacher ist, die Sprache zu verstehen, gibt es auch einen zusätzlichen Vorteil. Wissenschaftliche Studien zeigen, dass unser Verständnis einfacher ist, wenn Sie versuchen, etwas Neues zu verstehen. Das Gehirn verarbeitet häufig Wörter wie &quot;IT&quot;, &quot;&quot; für, &quot;&quot; und andere gängige Wörter, so schnell und mühelos, dass mehr &quot;Bandbreite&quot; zum Verständnis der Wörter, die sich herausstellen, wie &quot;Webcam&quot; oder &quot;andere&quot;, im obigen Beispiel verwendet werden.

Mithilfe von Meldungs Feld Titeln, Gruppenfeld Beschriftungen und anderen Textblöcken können Sie die Funktion einer Gruppe von Steuerelementen mit nur wenigen Wörtern auf einfache Weise an den Endbenutzer übermitteln.

Die Intuitivität ist auch aus Vertrautheit entstanden. Beispielsweise ist die Platzierung der Schaltflächen &quot; **OK** &quot; und &quot; **Abbrechen** &quot; so einheitlich, dass Sie in den Köpfen angezeigt werden, wenn ein Dialog diese Schaltflächen in einer umgekehrten Sequenz enthält (**Abbrechen**, dann **OK**, anstelle von &quot; **OK**&quot;, dann &quot; **Abbrechen**") – Sie können stattdessen einfach " **Abbrechen** " drücken. Nachdem Sie einen bestimmten Standard für die Durchführung von Aufgaben – Windows-basierte Anwendungen – seit mehr als einem Jahr verwendet haben, entwickeln sich die Gewohnheiten. Die folgenden Branchenstandards (aber nicht angegeben) erleichtern die Verwendung Ihrer Software.

In einem der frühen Windows Vista-Vorschau Versionen wurden die Schaltflächen " **minimieren**", " **maximieren**" und " **Schließen** " eines beliebigen Fensters unterschiedlich. In früheren Versionen von Windows (insbesondere bei Verwendung eines einzelnen Monitors) entwickeln Sie eine Gewohnheit, den Cursor in der oberen rechten Ecke des Bildschirms zu bewegen und auf zu klicken. Dies führte immer dazu, dass das Fenster geschlossen wird. Nun gab es in diesem speziellen Build von Windows Vista ungefähr 8 Pixel zwischen der Schaltfläche "Schließen" und dem äußersten rechten Rand des Fensters. Der zusätzliche Speicherplatz zeigte, dass es gut aussieht (und war wahrscheinlich notwendig für die kalte Glanz Animation der Schaltfläche.), war aber irritierend, weil es Benutzern nicht gestattet wurde, geöffnete Fenster so einfach zu schließen. Ihre Meinung kann schwierig sein. Glücklicherweise wurde dieses Problem im folgenden Build behandelt. Nun steht zwischen dem Rahmen des Fensters und der Schaltfläche Schließen weiterhin Leerraum, aber durch Klicken auf diesen Platz wird auch das Fenster geschlossen.

Ein sehr wichtiger Faktor für den intuitiven Entwurf ist die Menge an "Mental bandwidtha" – die Zeitspanne, die es uns macht, etwas zu verstehen, das – verwendet wird. Je niedriger die Nutzung der Bandbreite, desto besser ist die Benutzer Leistung.

Dabei handelt es sich um kleine Dinge, die zum "erleben" der Verwendung einer Software Anwendung beitragen. Die folgenden Beispiele enthalten Tipps, wie Sie Ihre Anwendungen mit Tipps und Tricks in der Praxis verbessern können.

## <a name="20-tips-for-a-better-functional-user-experience"></a>20 Tipps für eine bessere, funktionale Benutzer Funktionalität

Das Ziel einer besseren Benutzerfreundlichkeit besteht darin, eine einfachere, einfachere und funktionale Benutzeroberfläche zu haben, die auch gut aussieht. Diese Tipps helfen Ihnen, Ihre Benutzeroberfläche effektiver zu gestalten.

### <a name="use-standards"></a>Standards verwenden

Die etablierten Standards jeder Softwareumgebung – ob auf Betriebssystemebene, auf Marken Ebene oder auf Anwendungsebene – sind sehr wichtig. Neben dem Branding fungieren die Standards als ein Sprichwörtliches Schema im Sinne des Benutzers. Wenn der Benutzer lange Zeit mit der Arbeit mit einer Software Anwendung verbringt, steigert er die Produktivität aufgrund der zunehmenden Vertrautheit automatisch.

Bevor wir uns mit den Standards befassen, erörtern wir zuerst, worum es sich bei diesen Standards handelt. Die Standards umfassen alles vom Layout der Steuerelemente auf eine bestimmte Weise in den Dialogfeldern – wie z. b. die Schaltflächen **OK** und **Abbrechen** , die Form der Benutzeroberfläche – gerundete Ecken des oberen Fensters des Fensters wie in Windows XP-Dialogfeldern, Stile von Symbolen, Formaten anderer Grafiken, interaktives Verhalten der Anwendung und ähnliches.

Wenn Ihre Anwendung in einer bestimmten Nische liegt, kann es besser sein, einen anderen Satz von Standards einzuhalten. Wenn Ihre Anwendung z. b., Application oder ein Add-on für Office OneNote 2003 unterstützt, ist es ratsam, die Stile der Benutzeroberflächen-und Interaktivität-Standards von Office – und OneNote selbst zu befolgen. Dies beinhaltet die Verwendung der Befehls leisten im Office-Stil anstelle der Standard Symbolleisten. weitere Aktionen – sowohl Visualisierung als auch Verhalten. Wenn Ihre Anwendung Teil der Microsoft Visual Studio .net-Kategorie sein soll, verfügen Sie über einen separaten Satz von Standards. Tatsächlich werden von Unternehmen wie Microsoft für solche Add-on-oder Support-Anwendungen geschriebene Richtlinien veröffentlicht. Beachten Sie auch, dass Grafik-und Entwurfskonzepte manchmal geschützte geistige Eigenschaften sind. Überprüfen Sie stets die richtige Dokumentation, um sicherzustellen, dass Sie über die Lizenz zum Erstellen solcher Entwürfe verfügen.

Ein drittes Beispiel für Standards wäre die Tablet PC-Umgebung. Diese Standards überschreiten die Grenzen zwischen den Richtlinien des Betriebssystems und den Anwendungsrichtlinien. Die [Tablet PC SDK-Dokumentation](/previous-versions/ms840465(v=msdn.10)) enthält einige nützliche Informationen im Thema "Planen der Anwendung". Im Gegensatz zu den Richtlinien von Office 2003 oder Visual Studio beeinflussen diese Entwurfs Empfehlungen direkt, wie der Benutzer mit Ihrer Anwendung interagiert und wie er sich im Gegenzug verhält. Wenn Sie beispielsweise in Ihrer Anwendung andockbare Fenster haben, empfiehlt die Dokumentation, dass Sie sicherstellen können, dass die Bildschirm Ausrichtung geändert wird, und dass die Andock enden Fenster bei Bedarf ordnungsgemäß in einem Hochformat oder Querformat neu organisiert werden. Auch wenn Sie Ihre Anwendung nicht als Tablet-spezifisch entwerfen, sollten Sie diese Richtlinien überspringen.

Mit dem Anstieg von intelligenten Clients überqueren Anwendungen nun die Grenzen zwischen unterschiedlichen Hardware – normale PCs, Tablet PCs, Mobile oder ultramobile Geräte, Media Center PCs usw. Jede Situation erfordert, dass ein anderer (oder zusätzlicher) Satz von Standards befolgt wird.

Wenn Anwendungen die Betriebssystem-oder Anwendungs ebenenstandards gemeinsam nutzen, haben die Benutzer mehr zu Hause mit der Software, was das Erlernen und verwenden erleichtert. Diese Ergebnisse sind eine direkte Steigerung der Produktivität. Benutzer möchten so schnell wie möglich mit neuer Software produktiv werden können.

### <a name="draw-attention-to-important-buttons"></a>Wichtige Schaltflächen beachten

Manchmal müssen Sie den Benutzer auch dann an die wichtigsten Schaltflächen weiterleiten, wenn Sie über vier oder fünf weitere Schaltflächen herum herum stehen. Wenn Sie mit der Größe, der Farbe oder der Schriftart experimentieren, würden Sie die Standards unterbrechen – Dies wird nicht empfohlen. Verwenden Sie stattdessen einige einfache Tricks, um dies zu erreichen.

Der erste besteht darin, die anderen nicht kritischen Schaltflächen wie in der folgenden Abbildung dargestellt in linklabels zu konvertieren. Auf diese Weise weiß der Benutzer, dass diese Links eine Aufgabe ausführen, aber ihre Aufmerksamkeit wird zuerst auf die Schaltfläche, die sich herausstellt, angezeigt – ohne die standardmäßigen Entwurfs Richtlinien zu unterbrechen.

![Bild von drei Schaltflächen, die in linklabels konvertiert werden.](images/humanux-04.png)

Die zweite besteht darin, die Schaltfläche "kritisch" zuerst in der Zeile zu platzieren – entweder auf der linken Seite für horizontale Layouts, wie in der folgenden Abbildung gezeigt, oder oben bei vertikalen Layouts. Beachten Sie, dass sich dies abhängig von der Kultur des Ziel Benutzers ändern kann – Sie können besser Vorgehen, wenn Sie die Schaltfläche ganz rechts platzieren, wenn Ihre Anwendung eine Sprache ist, die von rechts nach links geschrieben wird.

![Bild von drei Schaltflächen, bei denen die Schaltfläche "kritisch" in einem horizontalen Layout ganz links ist.](images/humanux-05.png)

Die empfohlene Option ist die Festlegung, dass standardmäßig der Fokus empfangen werden soll. Beispielsweise sollte in einem Lösch Bestätigungs Dialogfeld die Option **Nein nicht** markiert werden, da dadurch verhindert wird, dass der Benutzer versehentlich etwas löscht.

### <a name="simplify-recognition-with-icons"></a>Erkennung durch Symbole vereinfachen

Symbole – insbesondere die Symbole und Symbolleisten-Bitmaps in Windows XP und Office 2003 beschleunigen die Erkennung der Benutzeroberfläche und der Aufgabe, die der Benutzer ausführen muss.

Wenn Sie z. b. das Ausrufezeichen Symbol sehen, das am häufigsten im Meldungs Feld angezeigt wird, werden Sie sofort über den Risiko Grad informiert, der mit den Steuerelementen neben diesem Symbol verknüpft ist. Ebenso, wenn Ihre Anwendung viele Steuerelemente einrichtet – unabhängig davon, wie richtig angeordnet ist – kann es sinnvoll sein, den gesuchten Satz von Steuerelementen zu finden.

In Windows XP Service Pack 2 wird eine aktualisierte Registerkarte zum **System Eigenschaften-System** Steuerungs Applet namens "Automatische Updates" hinzugefügt. Es stehen vier Optionen zur Verfügung – Updates werden automatisch heruntergeladen, Updates heruntergeladen, der Benutzer kann dann entscheiden, wann Sie installiert werden sollen, benachrichtigt den Benutzer, wenn Updates verfügbar sind, aber nicht heruntergeladen werden und automatische Updates vollständig deaktiviert werden.

Ein neuer PC-Benutzer kennt möglicherweise nicht, was diese Updates sind, und weiß möglicherweise nicht, welche Option am besten ausgewählt werden sollte. Daher hat Microsoft ein grünes Schild Symbol mit einem großen Häkchen neben dem empfohlenen, das eine "sichere" Option angibt, und einem roten Schild Symbol mit einem großen "x" neben dem, das potenziell für den Benutzer schädlich wäre, eingefügt. Dies ist in kritischen Situationen sehr hilfreich – besonders dann, wenn der Benutzer nicht über die Zeit verfügt, zu viel Text zu lesen.

Im gleichen **System Eigenschaften** -Applet verfügt jede Registerkarte über mehrere Gruppen Felder mit unterschiedlichen Steuerelementen für verschiedene Aufgaben. Neben jeder Gruppe wird eine relative Grafik eingefügt, die die Aufgabe der Steuerelement Gruppe problemlos bezeichnen könnte. Diese Art von grafischem Code ähnelt der Farbcodierung in physischen Dateien oder Parkplätzen. Dies funktioniert auch mit dem gleichen Prinzip, wenn mindestens einige visuelle Elemente in einem Magazine-Artikel vorhanden sind – das Interesse des Readers bleibt unverändert.

Die Auswahl des richtigen Symbols ist ebenfalls wichtig. Microsoft stellt viele Standardgrafiken als Teil von Visual Studio 2005 bereit. Dies wäre die beste Wahl. Wenn Sie eigene Symbole erstellen, wird dringend empfohlen, dass Sie den Standards auf Betriebssystem-oder Anwendungsebene für diese Grafiken folgen, wie im obigen Abschnitt [use Standards](#use-standards) beschrieben.

Die [Richtlinien](/windows/apps/desktop/) für die Interaktion mit der Windows-Benutzerinteraktion enthalten ein sehr nützliches Handbuch zum Erstellen von Windows-Stil [Symbolen](https://msdn.microsoft.com/library/aa511280.aspx)

### <a name="simplify-recognition-with-headers"></a>Vereinfachen der Erkennung mit Headern

Header sind die perfekte Möglichkeit, das gesamte Dialogfeld in einem einzelnen Satz (und optional einer Grafik) zu erläutern. Manchmal können Header auch Ihnen helfen, die Navigation und Befehle darin zu unterstützen. Header funktionieren effektiver als normale Beschreibungs Bezeichnungen, da Sie der erste Schritt ist, der einem Benutzer angezeigt wird, wenn das Dialogfeld angezeigt wird.

Die Windows Installer-Assistenten sind vielleicht die beliebtesten Header: ein einfaches Symbol in der äußersten rechten Ecke. eine Titel Bezeichnung, die das Dialogfeld beschreibt (z. b. "Installationsordner auswählen"); und eine Unterüberschrift, in der der Zweck des Dialog Felds beschrieben wird (z. b. Wählen Sie den Ordner aus, in dem die Software Dateien installiert werden sollen).

Nehmen wir an, dass wir eine typische Geschäftsanwendung mit einem Konto Abschnitt haben. Nach dem Entwurfs Paradigma, das von Windows Vista eingesetzt wird, können wir Unternehmens wichtige Informationen und zugehörige Befehle in der Kopfzeile (oder Fußzeile, wenn das Szenario dies aufruft) selbst bereitstellen. Der Benutzer hat die Konto Datei für "Big Company" geöffnet, und der Header sieht in etwa wie im folgenden Screenshot gezeigt aus.

![Screenshot eines Dialog Felds, das eine ausführliche Fußzeile enthält.](images/humanux-06.png)

Der folgende Screenshot zeigt ein Beispiel für einen ausführlichen Header in einem Dialogfeld.

![Screenshot eines Dialog Felds, das einen ausführlichen Header enthält.](images/humanux-07.png)

Auf ähnliche Weise können Sie vermeiden, dass Sie Aufgabenbereiche im Windows XP-Stil hinzufügen müssen – insbesondere, wenn Sie nur einige wenige Befehle haben, wodurch viel vertikaler Leerraum verschwendet wird – indem Sie diese Befehle in den-Header verschieben.

Beim Entwerfen von Headern sollten Sie einige Punkte beachten:

-   Stellen Sie sicher, dass sich die Hintergrundfarbe von der Hintergrundfarbe des Dialog Felds unterscheidet. Häufig wird ein weißer Header über eine standardmäßige Windows-Steuerelement-Steuerelement Vorderseite verwendet. Wenn Sie jedoch sicherstellen möchten, dass kein spezielles Design oder benutzerdefinierte Farben ihren Header durcheinander bringen, zeichnen Sie einen **LinearGradient** mithilfe von " **Color. FromKnownColor** " mit den Farben " **ControlLight** " und " **ControlDark**".
-   Behalten Sie nach Möglichkeit die Höhe des Headers unter 150 Pixel bei. Normalerweise wird eine Höhe von 100 oder 120 verwendet. Stellen Sie als allgemeine Regel sicher, dass die Größe kleiner als 1/4 ist.
-   Wenn Sie die direkte Bearbeitung von Informationen hinzufügen möchten, die in der obigen Kopfzeile angezeigt werden, ersetzen Sie LinkLabel dynamisch durch ein Textfeld, und tauschen Sie es nach Abschluss der Bearbeitung erneut aus.
-   Wenn Sie über eine Titel Bezeichnung mit einer Schriftart verfügen, die größer als 10 pt ist, verwenden Sie Arial oder Franklin Gothic Medium. MS Sans Serif sieht zu verzweigt und unprofessionell aus. Das Franklin Gothic Medium ist die Empfehlung in der Dokumentation zu Windows XP-Entwurfs Richtlinien. Verwenden Sie für Anwendungen, die auf Windows Vista abzielen, die Segoe UI Schriftart, die die Standard Schriftart des Systems ist.

### <a name="use-custom-message-boxes"></a>Verwenden benutzerdefinierter Meldungs Felder

Die Optionen, die im standardmäßigen Windows-Meldungs Feld verfügbar sind, sind sehr eingeschränkt. Wenn Sie dem Benutzer eine Frage stellen müssen, die mit einem einfachen Ja/Nein-oder OK/Abbrechen nicht beantwortet werden kann, wird es kompliziert.

Die Verwendung von Windows-Anwendungen ist aufgrund der hohen Anzahl von nichttechnischen Benutzern nun einfacher. Manchmal kann es viel einfacher sein, Schaltflächen mit freundlicheren Texten und sogar einigen zusätzlichen Steuerelementen – linklabels – bereitzustellen, um die Ausführung der Aufgabe zu vereinfachen.

Das Microsoft .NET Framework vereinfacht die Implementierung benutzerdefinierter Dialogfelder. Wenn Sie nur einige Eigenschaften im benutzerdefinierten Dialog Formular oder mit einer einzelnen Codezeile zuweisen, kann das Formular genau wie ein Standard Meldungs Feld funktionieren. Legen Sie in einem Button-Click-Ereignis die **DialogResult** -Eigenschaft des Dialog Felds auf **DialogResult. OK** oder **DialogResult. Cancel** fest. Verwenden Sie die **ShowDialog (Besitzer \[ Form \] )** -Methode aus dem übergeordneten Formular. Diese Methoden Methode gibt den **DialogResult** -Wert zurück.

Sie können alle **DialogResult** -Member verwenden. Die gleichen Optionen werden von der standardmäßigen **MessageBox. Show** -Methode verwendet.

Alternativ können Sie einfach die Eigenschaft "Accept- **Button** " des Dialog Felds auf " **btnOK**" und die Eigenschaft " **CancelButton** " auf " **btnCancel**" festlegen. Dadurch werden die **Eingabe** -und **ESC** -Taste automatisch den entsprechenden Click-Ereignissen der Schaltflächen **btnOK** und **btnCancel** zugeordnet.

Im folgenden finden Sie einige Tipps, wie Sie Ihre benutzerdefinierten Dialoge Auffinden:

-   Geben Sie für komplizierte Themen Links zur lokalen oder Online Hilfe mit einem LinkLabel an, das unter der entsprechenden Text Bezeichnung "Weitere Informationen" angibt.
-   Anstelle von **Ja** / **Nein** / **Abbrechen** -Schaltflächen können Sie Texte verwenden, die das Ergebnis der Schaltfläche eindeutig angeben, z. b. "Datei speichern und beenden", "beenden ohne Speichern" und "nicht beenden". Behalten Sie jedoch die Standard Schaltflächen " **Ja** / **Nein**", " **OK** / **Abbrechen**" und "Standard" bei, wenn möglich. Vertrautheit sorgt für eine hohe Produktivität.
-   Behalten Sie auf der linken Seite (oder auf der rechten Seite in Abhängigkeit von den Zielkultur Einstellungen) 50 Pixel, und fügen Sie ein Symbol hinzu, das das Szenario für den Dialog darstellt. Wenn es sich um ein Informations Dialogfeld handelt, können Sie das Symbol "i" verwenden, das von Standard Meldungs Feldern verwendet wird. Wenn es sich um ein Sicherheits Dialogfeld handelt, können Sie ein Schloss Symbol oder ein Schlüsselsymbol verwenden. Visual Studio 2005 umfasst einige hervorragend hochwertige Grafiken.
-   Stellen Sie immer sicher, dass Sie die richtige Tastaturnavigation für diese Schaltflächen bereitstellen – Benutzer verwenden die Tastenkombinationen für Meldungs Felder (z. b. O für OK, Y für Yes, C für Cancel usw.). Sie finden es sicherlich lästig, wenn Sie in Ihrem benutzerdefinierten Dialogfeld nicht verwendet werden.

### <a name="include-alternate-commands"></a>Alternative Befehle einschließen

Zwei wichtige Faktoren sind die Notwendigkeit alternativer Eingabemethoden – Frustration und Faulheit. Frustration ist ein zu häufiges Problem für Computerbenutzer. Wenn Sie frustriert sind, möchten Sie, dass Ihre Aufgabe schnell ausgeführt wird. Durch einen zusätzlichen Klick oder eine zusätzliche Wartezeit von wenigen Sekunden wird eine Person in der Belastung wirklich manipuliert – Sie wissen, wie Sie ist. Bei der Faulheit werden Sie häufig dazu aufgefordert, entweder die Aufgabe mit der Tastatur oder der Maus zu beenden – je nachdem, was Sie momentan verwenden. Abgesehen von diesen beiden Faktoren erleichtert Ihnen die Verwendung alternativer Eingabemethoden das einfache Ausführen von Aufgaben.

Wenn Sie z. b. ein Listenfeld mit zwei Schaltflächen haben – "hinzufügen" und "entfernen" – auf beiden Seiten, sollten Sie ein Kontextmenü für dieses Listenfeld mit Menübefehlen hinzufügen, analog zu diesen Schaltflächen. Dadurch erhält der Benutzer die Möglichkeit, die von ihm am besten geeignete Methode auszuwählen. Einsteiger verwenden als Windows Vista-Richtlinien für die Benutzeroberflächen-Richtlinien eine große Zahl von Kontextmenüs und erwarten, dass Sie mit der rechten Maustaste klicken.

Ebenso verwenden wir visuelle Steuerelemente für Text oder numerische Eingaben. Beispielsweise werden Schieberegler zum Angeben von ganzen Zahlen verwendet, und für Datums Eingaben werden Kalender Steuerelemente verwendet. Manchmal kann es einfacher sein, einfach nur durch Eingabe von einzugeben. Häufig kann der Benutzer einen Unterschied machen, wenn Sie ein numerisches Up-Down Steuerelement hinzufügen, das mit einem Schieberegler verknüpft ist, oder ein DateTimePicker-Steuerelement anstelle des Kalender Steuer Elements verwenden.

### <a name="how-to-handle-critical-actions"></a>Behandeln kritischer Aktionen

Beim Ausführen einer wichtigen, nicht wiederherstellbaren Funktion empfiehlt es sich im Allgemeinen, ein Meldungs Feld zu erstellen, um die Aktion zu bestätigen. Sehen wir uns das einmal an. Im folgenden Screenshot sehen Sie ein ähnliches benutzerdefiniertes Meldungs Feld, aber mit einem zusätzlichen Vorteil – ein Timer, der mit der Hilfe einer Statusanzeige visuell dargestellt wird.

![Screenshot des Dialog Felds "kritische Aktion"](images/humanux-08.png)

Es gibt einige Szenariospezifische Variationen, die Sie verwenden können. Wenn die auszuführende Aktion sehr wichtig ist (von der Überladung eines Strom Kraftwerks bis zum permanenten Löschen von Dateien), sollte die Standardaktion nach Ausführung des Timers Abbrechen lauten. Das Dialogfeld sollte nicht entfernt werden, stattdessen wird die Text Bezeichnung geändert, um anzuzeigen, dass die Aktion abgebrochen wurde. Der Benutzer kann auswählen, ob der Befehl oder der Abbruch bestätigt werden soll.

Stellen Sie immer sicher, dass Schaltflächen, die kritische Vorgänge ausführen, klar markiert sind – verwenden Sie immer Klartext, der die Aktion genau beschreibt. Wenn es sich bei der Aktion um das Löschen von Dateien handelt, dürfen Sie nicht "Dateien aus dem Repository entfernen" schreiben. Schreiben Sie "Dateien aus dem Repository löschen". Wenn beim Arbeiten mit Dateilisten der Menübefehl "Löschen" die ausgewählten Dateien von der Festplatte selbst löscht (im Gegensatz zur Entfernung aus der Datei Liste), sollten Sie den kritischen Charakter dieses Vorgangs ordnungsgemäß belasten und explizit darauf achten, dass die Dateien von der Aktion dauerhaft gelöscht werden.

Jemand hat einmal gesagt: "Sie sind so gut wie ihre schlechteste Arbeit". Das gleiche gilt für Softwareanwendungen. Ein einzelner fehlerhafter Eindruck von Ihrer APP kann für den Benutzer einen großen negativen Eindruck machen. Um sicherzustellen, dass dies nicht der Fall ist, können Sie sicherstellen, dass Sie, wenn die Anwendung abstürzt, richtig ausfällt. Wenn Sie die Datenwiederherstellung hinzufügen oder dem Benutzer gestatten möchten, eine Kopie dieser Daten zu speichern, kann es sich um einen großen Plus handeln. Der Benutzer sollte bei einem Absturz der Anwendung ordnungsgemäß benachrichtigt werden. Ein JIT-Debugger-oder kritischer Fehler Dialogfeld ist nicht gut geeignet. Obwohl die Behandlung von Abstürzen den Rahmen dieses Artikels sprengen würde, empfiehlt es sich, ein einfaches Dialogfeld zu erhalten, das sich an den Benutzer anpasst und ihn darüber informiert (und möglicherweise über einen Link zu weiteren Informationen zur Wiederherstellung nach diesem Absturz).

Wenn Sie einen Schritt weiter gehen möchten, können Sie mit einer meiner bevorzugten grafischen Entwurfs Anwendungen Vorgehen. Wenn es zu einem Absturz kommt, wird ein Wiederherstellungs Dialogfeld angezeigt, in dem Sie eine separate Kopie der zu bearbeienden Datei speichern können. Anschließend erhalten Sie ein Feedback Dialogfeld, in dem Sie Informationen über den Absturz eingeben können (selbstverständlich persönliche Informationen) und an die Ersteller gesendet werden.

### <a name="radiobuttons-or-comboboxes"></a>Radiobuttons oder ComboBoxes?

Auf den ersten Blick scheint die Methode zum Treffen einer 1: n-Auswahl nicht so schwierig oder wichtig zu sein. Manchmal kann es – sein, insbesondere dann, wenn das Szenario eine Anwendung ist, die für Zeit empfindliche Arbeit verwendet wird.

Werfen wir einen Blick auf ein Beispiel für eine echte Lebensdauer. Microsoft hat vor kurzem eine Vorschauversion einer Grafikanwendung, Expression Graphics Designer (früher mit dem Codenamen "Acryl") veröffentlicht. Ich hatte ungefähr 20 Grafik Objekte, denen ich eine bestimmte Eigenschaft in dieser Anwendung separat zuweisen musste. Dabei handelte es sich um einen dreblierungsprozess. Zu diesem Zweck musste ich das Objekt auswählen, auf die Schaltfläche klicken, um das Fenster "Einstellungen" anzuzeigen, und die Optionen festlegen. In einer solchen Option mussten zwei Optionen aus einem Kombinations Feld ausgewählt werden, wie im folgenden Screenshot zu sehen ist.

![Screenshot des Dialog Felds "Rand Textur" für den Ausdrucks Grafik-Designer.](images/humanux-09.png)

Wenn Sie die ComboBox-Liste ablegen und das zweite Element (von nur 2 Elementen) auswählen müssen, kann es sehr irritierend sein. In der Regel wird nicht berücksichtigt, wie lange es dauert, bis die Dropdown Liste angezeigt wird. Dies kann viel Zeit verschwenden und frustrierend sein. Dies kann problemlos gelöst werden, indem Sie eine GroupBox mit zwei Radiobuttons einfügen – insbesondere, wenn so viel Speicherplatz zur Verfügung steht. Bei Anwendungen wie CorelDRAW, Microsoft Access und anderen sind ähnliche Probleme aufgetreten.

Neben der Zeitverschwendung aufgrund der Dropdown Animation verschwendet Sie auch unsere "geistige Bandbreite". Mit zwei "immer sichtbaren" Radiobuttons ist unsere Meinung nicht mit der Position vertraut, auf die der Cursor klickt. Das ComboBox-Tool wird erst verarbeitet, nachdem die Liste gezeichnet wurde. Obwohl es möglicherweise zu unwichtig erscheint, ist es wirklich sehr wichtig.

Manchmal ist es besser, Radiobuttons zu verwenden, insbesondere, wenn Sie maximal vier Optionen haben.

### <a name="never-disrupt-the-user"></a>Stören Sie den Benutzer nie.

Wenn Sie nicht nur eine Waffe an den Kopf bringen, ist dies das destrukteste, was ein Entwickler für die Benutzer tun kann. Wenn Ihre Anwendung unnötig oder anderweitig den Benutzer unterbricht, während er an einer anderen Anwendung mit einem Meldungs Feld oder einem Task leisten-Flash arbeitet, erhalten Sie negative Punkte vom Benutzer.

Task leisten-blinken können natürlich nützlich sein, aber nur dann aufgerufen werden, wenn der Prozess ihrer Anwendung Eingaben vom Benutzer benötigt, um den Vorgang fortzusetzen, oder wenn Sie dem Benutzer etwas kritischer vermitteln müssen. Wenn der Benutzer die Taskleiste auf dem automatischen Ausblenden belassen hat, kann eine blinkende Task leisten Schaltfläche den Benutzer daran hindern, auf die Statusleiste oder andere Steuerelemente mit niedriger Verankerung zuzugreifen, wenn die Taskleiste darauf zugreifen würde, und er wird erst wieder ausgeblendet, wenn der Benutzer auf die blinkende Schaltfläche geklickt hat.

![Screenshot eines Popup Fensters.](images/humanux-10.png)

Popup Fenster (siehe Abbildung 10), die von Instant Messaging-Clients wie MSN Messenger bekannt gemacht werden, sind eine hervorragend Lösung, um den Benutzer über etwas zu informieren, ohne diesen zu stören oder seine Arbeitsabläufe zu unterbrechen. Es gibt einen hervorragend Artikel ( https://docs.microsoft.com/archive/msdn-magazine/2005/september/sprinkle-some-pizzazz-on-your-plain-vanilla-windows-forms-apps) von Bill Wagner zum Erstellen von Popup Fenstern). Es handelt sich um eine gute Richtlinie (und die gleichen), mit denen sich die-Auffassungen anderer Anwendungen nicht stören Das behindern solcher Fenster kann lästig und unproduktiv sein. Eine Lösung besteht darin, den vom Betriebssystem bereitgestellten toastsemaphore Mutex (/Library/WinMessenger/WinMessenger/Overview/Toast.ASP) zu verwenden, um einen Toast Konflikt zu vermeiden.

Manchmal müssen Sie möglicherweise mehrere Elemente nach dem Toast anzeigen. Es ist nicht ratsam, drei oder mehr Popup aufspielen. Stattdessen wäre es besser, jeden Popup durch ein Popup zu durchlaufen, indem er einen Toast durchläuft. Microsoft Outlook implementiert eine ähnliche Lösung, wenn der Benutzer über eingehende e-Mails benachrichtigt wird.

### <a name="provide-progress-status"></a>Status Status angeben

Häufig gibt es Aufgaben, die erfordern, dass der Benutzer wartet. Natürlich ist dies eine der Dinge, die der Benutzer einfach hasst. Aber schlimmer ist, wenn Sie warten, ohne zu wissen, was passiert. Manchmal muss Ihre Anwendung möglicherweise eine Verbindung mit einem Webdienst oder einem Remote Computer herstellen, oder es werden vielleicht große Datenblöcke verarbeitet – was der Grund ist, dass der Benutzer oder zumindest bekannt ist, was im Hintergrund geschieht. Es gibt unterschiedliche Methoden, je nach Situation.

Wenn Sie eine Verbindung mit einem weit entfernten Objekt wie einem Webdienst oder einem in einem Netzwerk oder einem Internet Server befindlichen herstellen, empfiehlt es sich, ein einfaches Status Dialogfeld (siehe folgende Abbildung) oder eine in der Statusleiste gehostete Statusanzeige anzuzeigen. Eine begleitende Bezeichnung sollte den aktuellen Status des Prozesses beschreiben. Wenn Sie z. b. eine Verbindung mit einem Webdienst herstellen, um einige Daten zu verarbeiten, z. b. "Herstellen einer Verbindung mit dem Webdienst... "oder" Bitte warten, verarbeiten... "Wenn dieser Prozess synchron ist, empfiehlt es sich, alle Steuerelemente zu deaktivieren, auf die der Benutzer zugreifen kann, bis der Prozess abgeschlossen wurde, oder den Fortschritt als modales Dialogfeld anzuzeigen.

![Screenshot des Dialog Felds "Statusanzeige"](images/humanux-11.png)

Es wird dringend empfohlen, dass Sie den Stil der Statusanzeige auf den Marquee-Modus festlegen, wenn Sie eine Statusanzeige verwenden und die Verarbeitungszeit unbekannt ist, oder wenn Sie nicht über einen maximalen Wert verfügen.

Eine andere Methode, die immer beliebter wird, ist ein festes Popup Fenster, das den Fortschritt anzeigt. Das Microsoft AntiSpyware-Download Programm/Updater oder die "Norton Antivirus"-e-Mail-Überprüfung ist ein gutes Beispiel dafür. Dies sollte natürlich nur für asynchrone Prozesse verwendet werden. Andernfalls ist der Benutzer möglicherweise nicht verwirrt. Solche Fenster werden am besten für die Hintergrundverarbeitung verwendet, z. b. das Herunterladen eines Updates oder das Ausführen einer geplanten Aufgabe, und sollten nie auf "Always on-Top" festgelegt werden.

### <a name="simplify-complex-steps-with-wizards"></a>Vereinfachen komplexer Schritte mit Assistenten

Es ist sicher anzunehmen, dass bei einer Vielzahl von Steuerelementen in einem einzelnen Formular ein typischer Benutzer zu keinem Ende verwirrt wird. Manchmal kann es keine Menge an Gruppierung, Größe oder Abstände bei der Erstellung von vielen wichtigen Steuerelementen helfen.

Ein Assistent ist für solche Szenarien am besten geeignet. Sie können Steuerelemente nach Bedarf nach Aufgaben oder Kategorien aufteilen und in separaten Schritten platzieren. Dies kann dazu beitragen, dass der Benutzer im Fokus ist und nicht von der Aufgabe unterstützt wird. Mithilfe der Schaltfläche Hilfe können Sie Schritt-oder aufgabenspezifische Hilfe bereitstellen. Die Richtlinien zur Erstellung von Assistenten finden Sie in der MSDN Library.

Assistenten sind auch eine gute Möglichkeit, die anfängliche Konfiguration Ihrer Anwendung einzurichten. Viele Anwendungen verwenden einen solchen Assistenten, um eine personalisierte Konfiguration direkt nach Abschluss des Setups oder bei der ersten Verwendung einzurichten. Ein solcher anfänglicher Assistent sollte auch optional sein, wenn möglich – wenn der Benutzer zu einem beliebigen Zeitpunkt abbricht, werden die nicht angegebenen Einstellungen auf die Standardwerte festgelegt. Wenn Sie den Assistenten etwas grafisch machen können (Weitere Informationen finden Sie im Abschnitt [Verwenden von sehr Grafiken](#use-pretty-graphics) ), wird die Konfigurations Aufgabe erheblich vereinfacht.

### <a name="get-the-tone-of-your-text-right"></a>Den Text Ihres Texts rechts

Im Windows-Benutzeroberflächen- [Interaktions Leitlinien](/windows/apps/desktop/)wurde ein sehr wichtiger Punkt über "textton" gemacht. Dies ist der Eindruck und das Gefühl, dass der Text in Ihrer Anwendung angezeigt wird. Dies kann von einer einfachen QuickInfo bis zum Steuerelement "Anweisungsbezeichnung" erfolgen.

Früher haben wir die Textänderung in der Option "Webcam" in MSN Messenger erläutert. Dies wird als richtiger textton bezeichnet. Beim Umgang mit nicht-technischen oder Anfänger-Benutzern wird die Nachricht über einen anderen Aspekt hinweg benötigt.

Wenn Sie "Zielpfad" oberhalb eines Textfelds in einer selbst extrahierenden Anwendung schreiben, kann ein technischer Benutzer leicht wissen, dass Sie etwas wie "C: \\ Temp \\ myPath" eingeben. Ein Einsteiger ("MOM") kann genauso einfach gemischt werden und muss sich auf den manuellen, technischen Support oder eine schlechtere – beziehen. Eine gute Alternative besteht darin, anzugeben, was der Benutzer tun soll: "wählen Sie den Ordner aus, in dem Sie diese Dateien platzieren möchten." Sie können sogar die Schaltfläche "Durchsuchen... "Schaltfläche neben diesem Textfeld für" Ordner auswählen... "

Wenn Sie eine klare Beschreibung darüber geben, was der Benutzer tun soll, verringern Sie auch die Notwendigkeit von Hilfedateien, oder verringern Sie zumindest die Details, die Sie in Hilfedateien einschließen müssen.

Ein sehr guter Vorschlag aus den [Interaktions Richtlinien der Windows-Benutzerinteraktion](/windows/apps/desktop/) gilt für jede Software. Es gibt an, dass der Writer den Text als "konverational" belassen soll. Die Richtlinien definieren dies als "vermeiden von Wörtern, die Sie keinen anderen Personen in der Person sagen."

Einige Tipps zum Schreiben von Text:

-   Vermeiden Sie die Diskussion über den Benutzer in der dritten Person. Sagen Sie "Sie" anstelle von "Benutzer".
-   Verwenden Sie nach Möglichkeit immer "Mein Name:" oder "meine e-Mail-Adresse:" anstelle von "Name:" oder "e-Mail:".
-   Wenn Sie mehrere Optionen vergeben, schreiben Sie den Text aus der Perspektive des Benutzers. Wenn Sie z. b. zwei Radiobuttons unter einer Bezeichnung wie "SELECT-Berechtigung für \[ Benutzername \] in diesem Netzwerk" oberhalb von zwei Radiobuttons haben, z. b. "zulassen" und "verweigern", ersetzen Sie den RadioButton-Text durch "Ich möchte \[ username zulassen \] " und "Ich möchte username nicht zulassen \[ \] ".
-   Unterstreichen von Text nur, wenn er für Links verwendet wird. Der Benutzer wird verwirrt, wenn der unterstrichene Text kein Link ist.
-   Zeichnen Sie wichtige Informationen mit einer fett formatierten Bezeichnung, aber verwenden Sie Sie sorgfältig. Zu viel fett formatierter Text ist verwirrend und verringert die allgemeine Auswirkung des Formulars.
-   Wenn Sie den Text für ein Kontrollkästchen schreiben, stellen Sie sicher, dass es leicht zu erkennen ist, was geschieht, wenn es ausgewählt wird, und wenn es nicht ausgewählt oder deaktiviert ist. Die empfohlene Option besteht darin, den Text direkt als Ergebnis des Kontrollkästchens zu schreiben. Schreiben Sie z. b. "mir hilfreiche Informationen von ihren Partnern senden" anstelle von "keine nützlichen Informationen von ihren Partnern senden". Ich kann mir vorstellen, dass viele Marketingmitarbeiter über dieses spezielle Beispiel sprechen. Ich bin mir sicher, dass Sie wissen, was ich meine.
-   Wenn Sie ein Schaltflächen ähnliches Steuerelement (in der Regel ein RadioButton mit einer Befehls Schaltfläche) haben, das aktiviert/deaktiviert ist, stellen Sie sicher, dass Sie es richtig bezeichnen. Wenn der Prozess aktiviert ist, schreiben Sie "aktiviert" anstelle von "enable" oder "deaktivieren". Wenn Sie aktiviert schreiben, wird der aktuelle Status angezeigt. Wenn auf die Schaltfläche geklickt wird (aktiviert) und die Schaltfläche "aktivieren" lautet, kann Sie verwirrend und problematisch sein. "Aktivieren" könnte den Benutzer dazu auffordern, darauf zu klicken, dass der Prozess nicht aktiv ist.

### <a name="sometimes-a-listview-is-better"></a>Manchmal ist eine ListView besser.

Wir halten uns häufig an DataGrid, ListBox oder sogar ComboBox für Auswahl Aufgaben, aber mit Windows XP und neueren Windows-Versionen können Sie mithilfe von ListView größere Optionen erhalten.

Die Feinheiten des ListView-Steuer Elements:

-   Beschleunigt das Erkennen von Elementen mit Symbolen und Bitmaps.
-   Zeigt zusätzliche Informationen mit Details oder Kachel Ansichten an.
-   Mit Visual Studio 2005 können Sie sogar Gruppen zur weiteren Kategorisierung haben. Gruppen umfassen alle Sichten und sind flexibel. Gruppen können auch verwendet werden, um eine Hierarchie Ansicht (z. b. eine TreeView) zu vereinfachen, in der mehr untergeordnete Knoten als übergeordnete Knoten vorhanden sind. Ein gutes Beispiel hierfür ist das Dialogfeld Netzwerkverbindungen unter Windows XP, das mit "in Gruppen anzeigen" und der Ansicht auf Details angezeigt wird.
-   Wenn Sie ein ListView-Steuerelement anpassen möchten, zeichnen Sie es manuell durch Festlegen der Eigenschaft Besitzer **Zeichnen** und mithilfe der **DrawItem** -und **DrawSubItem** -Ereignisse.
-   Unterstützt die schnelle direkte Bearbeitung von ListView-Elementen.
-   Unterstützt die manuelle Neuanordnung problemlos.
-   Ermöglicht Benutzern das Auswählen der Ansicht (große Symbole, kleine Symbole, Liste usw.), mit denen Sie am meisten vertraut ist.

### <a name="simplify-navigation-with-breadcrumb-controls-and-sidebars"></a>Vereinfachen Sie die Navigation mit Breadcrumb-Steuerelementen und-Steuerelementen.

"Unter Navigation" ist der Schlüssel für die komplexe Benutzeroberfläche. Manchmal können Sie eine komplizierte Benutzeroberfläche nicht mit Escapezeichen versehen. In einer solchen Situation ist es am besten, den Benutzer so einfach wie möglich zu gestalten. Eine Rand Leiste, die aus Verknüpfungs Bezeichnungen besteht, oder ein TreeView-Element für die Hierarchie basierte Navigation, schlägt für die Aufgabe des aktuellen Dialogs eine Navigation auf gleich geordneter Ebene vor. Der Benutzer kann ganz einfach zwischen den Schritten des Prozesses wechseln, während er weiß, wo er ist.

Wenn Sie eine Hierarchie basierte Navigation mit TreeViews oder einer anderen ähnlich komplexen Navigation durchlaufen, wäre ein gutes Hilfsprogramm für den Benutzer ein Breadcrumb-Steuerelement. Obwohl Visual Studio noch nicht mit einem integrierten Steuerelement ausgeliefert wird, finden Sie weitere Informationen zum Erstellen eines [Breadcrumb-Steuer Elements unter Erstellen eines Breadcrumb-Steuer](/archive/msdn-magazine/2005/july/advanced-basics-creating-a-breadcrumb-control) Elements. Ein Breadcrumb-Steuerelement erleichtert die Suche nach dem aktuellen Speicherort in Bezug auf die Hierarchie.

Die Breadcrumb-Navigation kann problemlos in den-Header zusammengeführt werden, wenn das Formular über ein Formular verfügt. Weitere Informationen finden Sie im vorherigen Abschnitt zu [Headern](#simplify-recognition-with-headers).

### <a name="use-pretty-graphics"></a>Verwenden von hübschen Grafiken

Alle Benutzer loben Anwendungen mit coolen Grafiken – die Mehrzahl ist zumindest. Obwohl es sich bei einer Benutzeroberfläche mit einer hübschen Grafik nicht um eine logische Wahl für alle Anwendungen handelt, ist es hilfreich, einen guten Eindruck zu machen, und Sie können in der Arbeit arbeiten. Natürlich sollten die Grafiken die Produktivität nicht beeinträchtigen, aber wenn Sie richtig verwendet werden, können Sie Sie vergrößern!

Es müssen nicht viele Grafiken vorhanden sein, und es müssen nicht unbedingt viele Arbeitsschritte erforderlich sein. Ein professionell gestalteter Begrüßungsbildschirm oder ein Header (z. b. der, über den wir vorhin gesprochen haben) führt den Trick aus. Wenn Ihr Budget dies zulässt, können Sie gut gestaltete Grafiken für Symbolleisten, Assistenten und vieles mehr verwenden. Dadurch wird Ihre APP sehr gut aussehen und auch noch professioneller. Dies ist ein feiner Effekt, aber ein professionelles Aussehen vermittelt Vertrauen und Stabilität. Wenn Sie ein relativ kleines Unternehmen sind, das Einzelhandelsanwendungen erstellt, ist dies ein wichtiger Aspekt, der berücksichtigt werden muss.

Stellen Sie immer einen Punkt für die Verwendung professionell gestalteter Grafiken dar. Lizenzfreie Grafiken sind mühelos verfügbar und kostengünstig. Sie können auch einen Designer angleichen. Wenn Grafiken aber nicht Ihre Forte sind, probieren Sie es nicht selbst aus. Wenn Sie keine professionell entworfenen Grafiken erwerben oder verwenden können, ist es besser, Sie überhaupt nicht zu verwenden.

Für kleine Grafiken können Sie immer die Symbole und Bitmaps aufrufen, die mit Visual Studio 2005 ausgeliefert werden. (Die Grafiken, die mit früheren Versionen ausgeliefert wurden, werden nicht empfohlen!)

### <a name="provide-resizable-forms-when-possible"></a>So können Sie nach Möglichkeit die Größe der Größe ändern

Fenster mit Größenänderung sind in gewisser Weise mit auflösungsunabhängigen Fenstern vergleichbar. Auflösungsunabhängige Fenster sehen gleich aus, ob Sie 96dpi-oder 300 dpi-Bildschirme verwenden. Unabhängig davon, ob die Benutzeroberfläche Ihrer Anwendung auflösungsunabhängig ist, ist es besser, wenn Sie in der Größe geändert werden kann. Dies gilt natürlich nicht für viele Szenarien, sondern für eine gute allgemeine Regel.

Wenn Ihr Fenster mit Listen beliebiger Sortier –, insbesondere mit ListViews –, umgeht, wird dies noch wichtiger. Die Größe der Größe ermöglicht dem Benutzer, gleichzeitig weitere Daten zu sehen.

Beispielsweise haben wir eine Anwendung, in der der Benutzer ein Image aus einer großen Sammlung auswählen muss. Mithilfe des Dialog Felds öffnen können Sie eine Miniaturansicht auswählen, aber das Dialogfeld weist eine Größe mit fester Größe auf, und die Miniaturansicht zeigt jeweils nur 4 Miniaturansichten an. Wenn die Sammlung über hundert Bilder verfügt, kann das Scrollen und das Aussehen – eine sich wiederholende Aufgabe – sehr viel Zeit und eine Verringerung der Effizienz sein. Wenn die Größe des Dialog Felds geändert werden kann, kann der Benutzer die Größe so groß wie möglich machen, oder Sie ist mindestens so groß wie der Bildschirm. Wenn die Liste einen horizontalen Bildlauf aufweist – wie eine ausführliche ListView oder ein DataGrid –, ist es noch mehr. Fenster mit Größenänderung sind in einer solchen Situation sehr hilfreich.

### <a name="provide-more-functionality-with-sidebarstask-panes"></a>Bereitstellen von mehr Funktionalität mit Sidebars/Aufgabenbereichen

Wie bei den Headern, die wir bereits erwähnt haben, sind Rand leisten und Aufgabenbereiche eine wunderbare Methode, um zusätzliche Funktionalität und hilfsprogrammbefehle bereitzustellen. Beispielsweise sind die Aufgabenbereiche in Office Word 2003 sehr praktisch, zugänglich und nicht aufdringlich. Außerdem funktionieren Sie asynchron, wenn eine Verbindung mit Online Ressourcen hergestellt wird, und dem Benutzer wird die Option für mehrere Aufgaben bereitgestellt.

Das Erstellen eines Aufgabenbereichs oder einer Rand Leiste ist genauso einfach wie das Erstellen eines andockbaren Panels, mit der Option, eine schlanke Grafik an den Anfang zu stellen, die als Titlebar fungiert. Dafür können Sie sogar ein farbiges Label-Steuerelement verwenden. Die Möglichkeiten für Aufgabenbereiche sind viele!

Wenn Sie über zusätzliche Funktionen verfügen, die Sie nicht für Ihren Benutzer bereitstellen möchten, gibt es keinen Ort wie den Aufgabenbereich. Sie können Aufgabenbereiche auch wie die Visual Studio-Tool Fenster "automatisch im Hintergrund" oder "reduzieren" machen.

### <a name="give-a-notification-choice"></a>Benachrichtigungs Auswahl

Zuvor haben wir gesehen, wie Sie ein benutzerdefiniertes Meldungs Feld erstellen. Wenn ein Meldungs Feld in der Anwendung häufig für den Benutzer angezeigt wird, kann es ratsam sein, ein Kontrollkästchen hinzuzufügen, das der Benutzer auswählen kann, um dieses Dialogfeld in Zukunft zu deaktivieren. Eine solche Option eignet sich besonders gut für offensichtlichere Nachrichten.

Ein bekanntes Beispiel hierfür ist das Visual Studio-Dialogfeld "suchen". Wenn Sie Text suchen oder ersetzen, zeigt Visual Studio ein Meldungs Feld an, das die Ergebnisse angibt. Sie haben jedoch auch die Möglichkeit, dieses Meldungs Feld zu deaktivieren. Es kann sehr lästig sein, wenn Sie die EINGABETASTE drücken oder bei jedem Suchvorgang auf OK klicken müssen.

Ein weiterer wichtiger Aspekt von Visual Studio ist, dass die Ergebnisse dieses Vorgangs auch dann in der Statusleiste angezeigt werden, wenn das Dialogfeld deaktiviert ist.

### <a name="provide-tooltips"></a>Stellen Sie Quick Infos bereit!

Manchmal können Sie mit Quick Infos viel Zeit sparen. Schaltflächen, Kontrollkästchen und andere Steuerelemente können mehrdeutig sein, und der Benutzer ist möglicherweise nicht sicher, was zu tun ist. Quick Infos bieten die beste Form der kontextbezogenen Hilfe in nur einer einzelnen Zeile. Der Benutzer kann schnell entscheiden, was geschehen soll, ohne in der Hilfedatei nach etwas zu suchen oder ein anderes Fenster zu öffnen.

Die Benutzer überspringen dies häufig in Ihren Anwendungen. Erstellen Sie einen Punkt, um Quick Infos für alle mehrdeutigen Steuerelemente hinzuzufügen – oder für alle Steuerelemente, wenn möglich. Wiederholen Sie weder den Text einer begleitenden Bezeichnung noch den eigenen Text des Steuer Elements, sondern stellen Sie zusätzliche Informationen zu diesem Steuerelement bereit. Der Text sollte die Funktion des Steuer Elements in nur wenigen Worten erläutern.

### <a name="do-not-forget-the-little-things"></a>Vergessen Sie nicht die kleinen Dinge

Die kleinen Dinge können Sie belästigen, aber das ignorieren kann sich auf den Eindruck auswirken, den Sie treffen. Ich habe einmal eine Anwendung verwendet, die von einer wichtigen Person in der Softwarebranche erstellt wurde, deren Form "BorderStyle" auf "beträchtlich" festgelegt war, aber die Steuerelemente auf der rechten Seite des Formulars waren nicht verankert. Aus diesem Grund hatte die von einem Branchen Gewicht erstellte Anwendung ein nicht professionelles Gefühl.

Diese Arten von "kleinen Dingen" sind der Kern des gesamten Eindrucks. Die Benutzeroberfläche und die Benutzeroberfläche Ihrer Anwendung sind die Benutzer, auf denen die Anwendung Ihre Anwendung –. Wenn in der Benutzeroberfläche offensichtliche Fehler angezeigt werden, kann es sein, dass Ihre Anwendung weniger leistungsfähig und effektiv ist.

## <a name="conclusion"></a>Zusammenfassung

Wir haben uns nur auf einen kleinen Teil der menschlichen Benutzer Arbeit ausgewirkt. Wenn die Benutzerfreundlichkeit einfacher, effektiver, unterhaltsamer und benutzerfreundlicher wird, wird die Aufgabe der Erstellung dieser Benutzerfreundlichkeit zu einer viel komplexeren Aufgabe. Dank einiger vorausschauender und guter Planung können Sie jedoch eine gute Benutzer Leistung erzielen.

Die beste Möglichkeit, die perfekte Benutzeroberfläche zu erstellen, ist die Durchführung von Benutzeroberflächen Tests speziell auf der Benutzeroberfläche – ob mit einer speziellen Testgruppe oder selbst. Je mehr Zeit Sie für das Testen der Benutzer Arbeit aufwenden, bevor Sie Ihre Anwendung freigeben, desto besser. Dies erspart Ihnen später viele Probleme.

 

 