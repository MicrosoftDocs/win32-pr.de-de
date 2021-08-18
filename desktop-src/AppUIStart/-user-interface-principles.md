---
title: Benutzeroberfläche Prinzipien
description: In diesem Thema wird erläutert, wie Intuitive Benutzeroberflächen- und Benutzeroberflächenentwurfsprinzipien in Windows Anwendungen implementiert werden.
ms.assetid: 603bc184-3eec-4281-8caa-993834da3131
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b57781ab2cb0a2d9574288000f65805c981afa391d49263bd21e23eeed432416
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119021444"
---
# <a name="user-interface-principles"></a>Benutzeroberfläche Prinzipien

In diesem Thema wird erläutert, wie Intuitive Benutzeroberflächen- und Benutzeroberflächenentwurfsprinzipien in Windows Anwendungen implementiert werden.

-   [Introduction (Einführung)](#introduction)
-   [Die Grundprinzipien der richtigen Benutzeroberfläche](#the-basic-principles-of-proper-ui)
    -   [Abstand und Positionierung](#spacing-and-positioning)
    -   [Größe](#size)
    -   [Gruppierung](#grouping)
    -   [Anschaulichkeit](#intuitiveness)
-   [20 Tipps für eine bessere, funktionale Benutzererfahrung](#20-tips-for-a-better-functional-user-experience)
    -   [Verwenden von Standards](#use-standards)
    -   [Aufmerksamkeit auf wichtige Schaltflächen lenken](#draw-attention-to-important-buttons)
    -   [Vereinfachen der Erkennung mit Symbolen](#simplify-recognition-with-icons)
    -   [Vereinfachen der Erkennung mit Headern](#simplify-recognition-with-headers)
    -   [Verwenden von benutzerdefinierten Meldungsfeldern](#use-custom-message-boxes)
    -   [Einschließen alternativer Befehle](#include-alternate-commands)
    -   [Behandeln kritischer Aktionen](#how-to-handle-critical-actions)
    -   [RadioButtons oder ComboBoxes?](#radiobuttons-or-comboboxes)
    -   [Nie den Benutzer unterbrechen!](#never-disrupt-the-user)
    -   [Status "Status angeben"](#provide-progress-status)
    -   [Vereinfachen komplexer Schritte mit Assistenten](#simplify-complex-steps-with-wizards)
    -   [Get the Tone of Your Text Right](#get-the-tone-of-your-text-right)
    -   [Manchmal ist eine ListView besser](#sometimes-a-listview-is-better)
    -   [Vereinfachen der Navigation mit Breadcrumb-Steuerelementen und Randleisten](#simplify-navigation-with-breadcrumb-controls-and-sidebars)
    -   [Verwenden von "Pretty Graphics"](#use-pretty-graphics)
    -   [Bereitstellen von Formularen mit größenveränderlicher Größe nach Möglichkeit](#provide-resizable-forms-when-possible)
    -   [Bereitstellen weiterer Funktionen mit Randleisten/Aufgabenbereichen](#provide-more-functionality-with-sidebarstask-panes)
    -   [Auswählen einer Benachrichtigung](#give-a-notification-choice)
    -   [Geben Sie QuickInfos an!](#provide-tooltips)
    -   [Vergessen Sie die kleinen Dinge nicht](#do-not-forget-the-little-things)
-   [Zusammenfassung](#conclusion)

## <a name="introduction"></a>Einführung

Entwickler können häufig die Perspektive des Endbenutzers nicht berücksichtigen. Entwickler arbeiten hart daran, die Anwendung funktionsfähig zu machen– Kunden erwarten nur, dass sie funktioniert, und ihre Wahrnehmung der Software konzentriert sich auf diese Anforderung. Dies gilt insbesondere, wenn Sie Einzelhandelssoftware entwickeln oder etwas, das von nicht technischen Personen verwendet wird. Entwickler müssen die Anforderungen des Endbenutzers während des gesamten Softwareentwurfsprozesses kennen.

Eine Softwareanwendung muss so einfach wie möglich navigieren und verwenden können. Mit der Menge an Software, die erstellt wird, verfügen geschätzte 4 von 10 Softwareanwendungen über eine wirklich hervorragende Benutzeroberfläche, die dem Endbenutzer wirklich gefällt und sofort mit der Verwendung vertraut ist.

Eine große Menge an softwareinterner Nutzung wird für Unternehmen erstellt. Unabhängig davon, ob es im Haus oder unter der Obhut eines Beraters entwickelt wird– häufig wird nur ein minimaler Zeit-, Aufwands- oder Geldaufwand in die Erstellung einer besseren Benutzeroberfläche investiert. Die Rolle "Designer" ist im Entwicklungszyklus selten , insbesondere in der Welt der Windows Anwendungen.

Es gibt einige grundlegende Regeln, die befolgt werden müssen, um eine viel ansprechendere und besser funktionierende Benutzeroberfläche für Ihre Anwendung zu erhalten. Sie erfordert nicht zu viel Zeit oder Geld für Sie und bietet eine gute Rendite.

Bevor wir weitergehen, unterscheiden wir zwischen Benutzeroberfläche und Benutzeroberfläche – zumindest für den Bereich dieses Artikels. Die Benutzeroberfläche bezieht sich auf die Visuals und Steuerelemente Ihrer Anwendung, während die Benutzeroberfläche (User Experience, UX) sowohl die Benutzeroberfläche als auch das Verhalten der Anwendung im Zusammenhang mit der Benutzeroberfläche sowie das "Gefühl" umfasst, das der Benutzer aus Ihrer App erhält. Es geht nicht nur darum, eine hervorragend aussehende Benutzeroberfläche zu entwerfen, sondern auch sicherzustellen, dass sie hervorragend funktioniert.

Hier werden 20 Punkte des UX-Entwurfs erörtert, die Sie problemlos in Ihre Anwendungsentwurfsphase integrieren können. Das Ergebnis sind umfangreichere Anwendungen mit besserer intuitiver Funktionalität – eine "menschliche Benutzererfahrung". Wie wir alle wissen, muss die Windows Vista-Generation von Anwendungen anders aussehen und sich anders verhalten. Dieses Thema hilft Ihnen bei der Vorbereitung auf zukünftige Anwendungen und gibt Ihren aktuellen Benutzern einen Eindruck von der Zukunft.

In den folgenden Abschnitten werden die Grundlagen des richtigen Benutzeroberflächenentwurfs erläutert.

## <a name="the-basic-principles-of-proper-ui"></a>Die Grundprinzipien der richtigen Benutzeroberfläche

Eine professionelle UX hängt von diesen vier Faktoren ab:

-   Abstand und Positionierung
-   Size
-   Gruppierung
-   Anschaulichkeit

Mit Versionen von Microsoft Visual Studio vor 8.0 waren Abstand und Größenoptimierung suboptimal. Ein 4x4- oder 8x8-Raster funktioniert nicht immer. Durch die Einbeziehung von SnapLines wurde der Prozess erheblich vereinfacht. Das Ausrichten einer Bezeichnung an einem Textfeld oder sogar das Ausrichten mehrerer Bezeichnungen an den entsprechenden Textfeldern war in früheren Versionen von Visual Studio äußerst schwierig. SnapLines haben diesen Prozess erheblich vereinfacht.

In den folgenden Abschnitten werden vier der wichtigeren Aspekte des professionellen UX-Designs beschrieben.

### <a name="spacing-and-positioning"></a>Abstand und Positionierung

Der Abstand zwischen zwei Steuerelementen ist wichtig. Der folgende Screenshot zeigt ein schlecht entworfenes Eingabeformular für **Benutzerinformationen:** Die oberen beiden Textfelder sind zu nah, die Liste darunter ist zu weit entfernt, und es gibt viel ungenutzten Platz im Formular.

![Screenshot eines schlecht entworfenen Formulars.](images/humanux-01.png)

Im folgenden Screenshot sehen Sie einen professioneller aussehenden Dialog mit dem richtigen Abstand und den entsprechenden Steuerelementen. Dies ist das gleiche Format wie im vorherigen Screenshot, wurde jedoch so geändert, dass der von den Ausrichtungslinien empfohlene Abstand verwendet wird. Es wird immer empfohlen, eine Bezeichnung an der Textbaseline des Textfelds oder eines anderen Steuerelements daneben auszurichten, anstatt den tatsächlichen unteren Rahmen des Steuerelements zu verwenden. Die Ausrichtungslinien werden eine andere Farbe, wenn diese Ausrichtung erreicht wird, in der Regel nur wenige Pixel oberhalb des unteren Rahmens.

![Screenshot eines gut entworfenen Formulars.](images/humanux-02.png)

Es gibt zwar keine genauen Regeln für den Abstand, aber die Ausrichtungslinien bieten äußerst nützliche Richtlinien für den richtigen Abstand. Weitere Tools, mit denen Sie den richtigen Abstand beibehalten können, sind die Layout-Steuerelemente unter der Toolboxgruppe Container. Das TableLayoutPanel-Element ist auch sehr hilfreich beim Erstellen von Dialogfeldern im Stil von Eingabeformularen.

### <a name="size"></a>Size

Die gleichen Überlegungen gelten für die Größe. Wenn Sie eine Schaltfläche aus der Toolbox auf das Formular ziehen, hat sie die perfekte Höhe und Breite. Die empfohlene maximale Breite (ohne schwerwiegende wichtige Gründe) besteht darin, die ursprüngliche Breite zu verdoppeln.

Wenn Sie sich das Fenster **Ausführen** im **Startmenü** oder das Dialogfeld **Eigenschaften** eines beliebigen Windows Explorer-Objekts ansehen, sind die Schaltflächengrößen "just right". Wenn Sie über eine sehr wichtige Funktion verfügen, die Der Endbenutzer ohne Fehler bemerken muss, gibt es andere Methoden als die Verwendung einer großen Schaltfläche oder garnieren nicht standardmäßiger Farben (mehr dazu später).

In der folgenden Abbildung sehen Sie drei Schaltflächen. Die erste Schaltfläche ist die empfohlene Größe und die Größe, die standardmäßig beim Ziehen (oder Doppelklicken) aus der Toolbox erstellt wird. Manchmal erfordert zusätzlicher Text, dass Sie die Schaltfläche vergrößern. Die zweite Schaltfläche zeigt eine große, aber akzeptable Größe an. Es würde keine Verwirrung bei der Einrichtung anderer Steuerelemente schaffen. Die dritte Schaltfläche ist jedoch eine völlig inakzeptable Größe. Sie können sehen, dass die Designbitmaps, die Windows zum Zeichnen von Designsteuerelementen verwendet, sogar geringfügig verzerrt werden. Außerdem wird es schwierig, andere Steuerelemente intuitiv um sie herum auszurichten.

![Abbildung von drei Schaltflächen, die von links nach rechts vergrößert werden.](images/humanux-03.png)

### <a name="grouping"></a>Gruppierung

In der Regel enthält eine Anwendung viele Steuerelemente. Nur durch richtige, intuitive Gruppierung können Sie all diese Steuerelemente einfacher zu verwenden. Funktionsbasierte oder kategorisierte Gruppierung erfolgt am besten durch Tabstoppsteuerelemente. Beispielsweise sind "Konten", "Berichte", "Mitarbeiter" und "Projekte" perfekte Kandidaten für Registerkarten in einer typischen Geschäftsanwendung. Gleichgeordnete Gruppierungen – Steuerelemente, die zum gleichen Endergebnis beitragen – werden am besten von Gruppensteuerelementen durchgeführt. Die Verwendung von Panels mit Rahmen für eine solche Gruppierung wird nicht empfohlen. Gruppensteuerelemente sparen Ihnen die zusätzliche Gewichtung eines Bezeichnungssteuerelements – insbesondere, wenn Ihre untergeordneten Steuerelemente selbsterklärend sind.

Gruppensteuerelemente in Gruppensteuerelementen werden nur empfohlen, wenn nicht mehr als 2 oder 3 davon innerhalb eines großen Gruppensteuerelements vorhanden sind.

### <a name="intuitiveness"></a>Anschaulichkeit

Dies ist der wichtigste Aspekt einer hervorragenden Benutzererfahrung. Intuitive Benutzererfahrung verringert den Bedarf an Erklärungen. Der Benutzer weiß nur, was die Steuerelemente tun.

Ein wichtiges Thema im intuitiven Design ist die Farbcodierung. Ein gutes Beispiel wird in Windows XP dargestellt, das neue soft-square-Schaltflächen für Funktionen wie die Navigation in Anwendungen mit Themen, die Dialogfelder **"Abmelden"** und **"Computer deaktivieren"** und andere darstellt.

Die Farbgebung dieser Steuerelemente wurde basierend auf dem Schweregrad des Ergebnisses der Schaltfläche bestimmt, die gedrückt wird. Die Navigation ist grün, ähnlich wie eine "Go"-Ampel. Herunterfahren, was zu einem möglichen Verlust von Arbeit führen würde, wird rot wie ein Warnzeichen angezeigt. Semikritische Schaltflächen wie "Abmelden" oder "Ruhezustand" sind gelb. Neutrale Schaltflächen, die keine kritischen Auswirkungen auf die Arbeitsprozesse des Benutzers haben, wie z.B. Hilfe, sind ein weiches Blau. Beim Erstellen einer skinned UI sollten diese Farbaspekte beachtet werden.

Ein sehr gutes Beispiel für die Erkennung von Inhalten durch Farben ist Microsoft Office OneNote. Die Registerkarten der Anwendung können auf unterschiedliche Farben festgelegt werden, während sie im Wesentlichen wie ein ordnungsgemäßer Teil des Gesamten Windows XP-Stildesigns aussehen.

Ein weiterer wichtiger Aspekt ist der Text in Ihren Anwendungen. In letzter Zeit wurden verschiedene Bemühungen unternommen, um die Sprache zu vereinfachen, die für die geschriebenen Anweisungen in Windows Software verwendet wird. Die Verwendung von Text innerhalb der Software wird später erläutert. Beachten Sie jedoch die folgenden kleinen, aber wichtigen Details.

MSN Messenger verfügte über ein Kontrollkästchen im Dialogfeld **"Optionen",** das mit "Share webcam capabilities" (Webcamfunktionen freigeben) gekennzeichnet war. Entwickler und technisch freundliche Personen wissen, was dies bedeutet, aber ein untätiger Benutzer könnte möglicherweise denken, dass Sie einem anderen Benutzer am anderen Ende Ihres Chats auch die Verwendung Ihres Webchats erlauben könnten. In einer aktuellen Version wurde sie in "Meine Webcam: Anderen erlauben, zu sehen, dass ich eine Webcam habe" geändert. Dies ist perfekt für die Zielgruppe geeignet, die möglicherweise nicht über technische Kenntnisse verfügt und in einfacher Sprache verwendet wird.

Einfachere Sprache erleichtert zwar das Verständnis, aber es gibt auch einen zusätzlichen Vorteil. Wissenschaftliche Studien zeigen, dass unser Denken mit einfacherer Sprache einfacher funktioniert, wenn wir versuchen, etwas Neues zu verstehen. Häufig verarbeitet unser Gehirn Wörter wie "it", "for", "that" und andere gängige Wörter so schnell und mühelos, dass mehr "Bandbreite" zugeordnet wird, um die Wörter zu verstehen, die sich im obigen Beispiel wie "Webcam" oder "Others" hervorstellen.

Message Box-Titel, GroupBox-Beschriftungen und andere text-Blöcke dieser Art erleichtern es Ihnen, die Funktion einer Gruppe von Steuerelementen mit nur wenigen Wörtern an den Endbenutzer zu übermitteln.

Intuitivität wird auch aus Vertrautheit abgeleitet. Beispielsweise ist die Platzierung der Schaltflächen **OK** und **Abbrechen** so einheitlich und gut in unserem Kopf platziert, dass Sie, wenn ein Dialog diese Schaltflächen in einer umgekehrten Sequenz enthält (**Abbrechen**, dann **OK**; anstelle von **OK**, dann **Abbrechen**) – sie könnten stattdessen auf **Abbrechen** klicken. Nachdem Sie einen bestimmten Standard für die Arbeit verwendet haben , z.B. Windows-basierten Anwendungen, entwickeln sich seit mehr als einem Jahr Dies ist üblich. Die Verwendung Ihrer Software wird durch die Verwendung von Branchenstandards (auch wenn sie möglicherweise nicht verwendet werden) vereinfacht.

In einem der frühen Windows Vista-Vorschaubuilds unterscheiden sich die Schaltflächen **Minimieren,** **Maximieren** und **Schließen** jedes Fensters. In früheren Versionen von Windows (insbesondere bei Verwendung eines einzelnen Monitors) haben Sie die Möglichkeit, den Cursor in der oberen rechten Ecke des Bildschirms zu bewegen und zu klicken. Dies führte immer dazu, dass das Fenster geschlossen wurde. In diesem speziellen Build von Windows Vista gab es ungefähr 8 Pixel Platz zwischen der Schaltfläche Schließen und dem rechten Rand des Fensters. Aufgrund des zusätzlichen Platzes sieht es kalt aus (und war wahrscheinlich für die Animation mit kaltem Leuchteffekt erforderlich, die die Schaltfläche bewegt hat), aber es war irimierend, da es benutzern nicht möglich war, Fenster so einfach zu schließen. Die Neukonfiguration Ihrer Meinung kann schwierig sein. Glücklicherweise wurde dieses Problem im folgenden Build behoben. Zwischen dem Rahmen des Fensters und der Schaltfläche "Schließen" ist noch Platz vorhanden. Wenn Sie jedoch auf diesen Bereich klicken, wird das Fenster geschlossen.

Ein sehr wichtiger Faktor für intuitives Design ist die Menge an "mentaler Bandbreite", die von ihr verwendet wird – die Zeit, die wir für das Verstehen eines Themas in Anspruch nehmen können. Je geringer die Bandbreitennutzung ist, desto besser ist ihre Benutzererfahrung.

Dies sind kleine Dinge, die zur "Erfahrung" der Verwendung einer Softwareanwendung beitragen. Die folgenden Beispiele enthalten Tipps zur Verbesserung Ihrer Anwendungen mit Tipps und Tricks aus der Praxis.

## <a name="20-tips-for-a-better-functional-user-experience"></a>20 Tipps für eine bessere, funktionale Benutzererfahrung

Das Ziel einer besseren Benutzeroberfläche ist eine einfachere, einfachere, funktionale Benutzeroberfläche, die ebenfalls gut aussieht. Diese Tipps helfen Ihnen, Ihre Benutzeroberfläche so zu gestalten, dass sie effektiver ist.

### <a name="use-standards"></a>Verwenden von Standards

Die bewährten Standards jeder Softwareumgebung – auf Betriebssystem-, Marken- oder Anwendungsebene – sind sehr wichtig. Neben dem Branding fungieren die Standards als ein sprichwörtliches Schema im Kopf des Benutzers. Wenn der Benutzer längere Zeit mit einer Softwareanwendung arbeitet, erhöht er aufgrund der wachsenden Vertrautheit automatisch die Produktivität.

Bevor wir über Standards sprechen, besprechen wir zunächst, was genau diese Standards sind. Die Standards umfassen alles aus dem Layout von Steuerelementen auf eine bestimmte Weise in den Dialogfeldern – z. B. die Schaltflächen **OK** und **Abbrechen,** die Form der Benutzeroberfläche – abgerundete Ecken des oberen Fensters wie in Windows XP-Dialogfeldern, Stile von Symbolen, Stile anderer Grafiken, interaktives Verhalten Ihrer Anwendung und ähnliches.

Wenn Ihre Anwendung in einen bestimmten Fall fällt, ist es möglicherweise besser, einen anderen Satz von Standards zu befolgen. Wenn Ihre Anwendung z. B. Office OneNote 2003 , anwendung oder ein Add-On für unterstützt, ist es ratsam, die Stile der Benutzeroberflächen- und Interaktivitätsstandards von Office zu befolgen – und insbesondere OneNote sich selbst. Dies schließt die Verwendung der Office Befehlsleisten anstelle der Standardsymbolleisten und anderer solcher Elemente ein – sowohl visuelle als auch Verhaltensleisten. Wenn Ihre Anwendung Teil der Kategorie Microsoft Visual Studio .NET sein soll, verfügen Sie über einen separaten Satz von Standards. Tatsächlich veröffentlichen Unternehmen wie Microsoft für solche Add-On- oder Supportanwendungen geschriebene Richtlinien. Beachten Sie auch, dass Grafik- und Entwurfskonzepte manchmal geistige Eigenschaften geschützt sind. Überprüfen Sie immer die richtige Dokumentation, um sicherzustellen, dass Sie über die Lizenz zum Erstellen solcher Entwürfe verfügen.

Ein drittes Beispiel für Standards wäre die Tablet PC-Umgebung. Diese Standards überschreiten die Grenzen zwischen Betriebssystemrichtlinien und Anwendungsrichtlinien. Die Dokumentation zum [Tablet PC SDK](/previous-versions/ms840465(v=msdn.10)) enthält einige sehr hilfreiche Informationen im Thema "Planen Ihrer Anwendung". Im Gegensatz zu den Richtlinien Office 2003 oder Visual Studio wirken sich diese Entwurfsempfehlungen direkt darauf aus, wie der Benutzer mit Ihrer Anwendung interagiert und wie er sich nacheinander verhalten soll. Wenn Ihre Anwendung beispielsweise Andockfenster enthält, empfiehlt die Dokumentation, dass Sie sicherstellen, dass sie erkennen kann, wann die Bildschirmausrichtung geändert wird, und dass sich die Andockfenster bei Bedarf ordnungsgemäß in einer Hochformat- oder Querformatausrichtung neu organisieren. Auch wenn Sie Ihre Anwendung nicht als Tablet-spezifisch entwerfen, sollten Sie diese Richtlinien durchgehen.

Mit dem Aufkommen von Smart Clients überschreiten Anwendungen jetzt die Grenzen zwischen verschiedenen Hardwarekomponenten – normale PCs, Tablet-PCs, mobile oder ultra-mobile Geräte, Media Center-PCs usw. Jede Situation erfordert, dass ein anderer (oder zusätzlicher) Satz von Standards eingehalten wird.

Wenn Anwendungen die Standards auf Betriebssystem- oder Anwendungsebene gemeinsam nutzen, sind die Benutzer mit der Software besser zu Hause, was das Erlernen und Verwenden erleichtert. Dies ist eine direkte Steigerung der Produktivität. Benutzer möchten so schnell wie möglich produktiv mit neuer Software arbeiten können.

### <a name="draw-attention-to-important-buttons"></a>Aufmerksamkeit auf wichtige Schaltflächen lenken

Manchmal müssen Sie den Benutzer zu den wichtigsten Schaltflächen leiten, auch wenn Sie vier oder fünf andere Schaltflächen um sie herum haben. Wenn Sie mit Der Größe, Farbe oder Schriftart experimentieren, würden Sie standards unterbrechen – dies wird nicht empfohlen. Stattdessen können Sie hierfür einige einfache Tricks verwenden.

Die erste besteht darin, die anderen nicht kritischen Schaltflächen in LinkLabels zu konvertieren, wie in der folgenden Abbildung dargestellt. Auf diese Weise weiß der Benutzer, dass diese Links eine Aufgabe ausführen, aber seine Aufmerksamkeit geht zuerst auf die Schaltfläche, die hervorhebt, ohne die Standardentwurfsrichtlinien zu brechen.

![Abbildung von drei Schaltflächen, die in Linklabels konvertiert wurden.](images/humanux-04.png)

Die zweite besteht darin, die kritische Schaltfläche zuerst in die Zeile zu setzen– entweder auf der linken Seite für horizontale Layouts, wie in der folgenden Abbildung dargestellt, oder oben für vertikale Layouts. Beachten Sie, dass sich dies je nach Kultur des Zielbenutzers ändern kann. Es ist möglicherweise besser, wenn Sie die betreffende Schaltfläche ganz rechts platzieren, wenn Es sich bei Ihrer Anwendung um eine Sprache handelt, die von rechts nach links geschrieben wird.

![Abbildung von drei Schaltflächen, bei denen sich die kritische Schaltfläche ganz links in einem horizontalen Layout befindet.](images/humanux-05.png)

Die empfohlene Option besteht darin, festzulegen, dass der Fokus standardmäßig empfangen wird. Beispielsweise sollte in einem Bestätigungsdialogfeld für das Löschen die Option **Nein** hervorgehoben werden, da dies verhindert, dass der Benutzer versehentlich etwas löscht.

### <a name="simplify-recognition-with-icons"></a>Vereinfachen der Erkennung mit Symbolen

Symbole – insbesondere die Symbole und Symbolbitmaps Windows XP und Office 2003 – beschleunigen die Erkennung der Benutzeroberfläche und der Aufgabe, die der Benutzer ausführen muss.

Wenn z. B. das Ausrufezeichen angezeigt wird, das am häufigsten auf dem Meldungsfeld angezeigt wird, werden Sie sofort auf die Risikostufe aufmerksam, die den Steuerelementen neben diesem Symbol zugeordnet ist. Ebenso kann es schwierig sein, die gewünschte Gruppe von Steuerelementen zu finden, wenn Ihre Anwendung viele Steuerelemente einrichtet – unabhängig davon, wie ordnungsgemäß sie angeordnet ist.

In Windows XP Service Pack 2 wird dem **Systemeigenschaften-Applet** "Automatische Updates" eine aktualisierte Registerkarte hinzugefügt. Es gibt vier Optionen: Updates automatisch herunterladen, Updates herunterladen, aber den Benutzer entscheiden lassen, wann er sie installieren soll, den Benutzer benachrichtigen, wenn Updates verfügbar sind, aber nicht mit dem Download beginnen, und automatische Updates vollständig deaktivieren.

Ein neuer PC-Benutzer weiß möglicherweise nicht, was diese Updates sind, und weiß möglicherweise nicht, welche Option am besten ausgewählt werden sollte. Microsoft hat also ein grünes Shieldsymbol mit einem großen Häkchen neben der am besten empfohlenen Option, die eine "sichere" Option kennzeichnet, und ein rotes Shield-Symbol mit einem großen "x" neben dem Symbol, das für den Benutzer potenziell schädlich wäre, gesetzt. Dies ist in kritischen Situationen sehr hilfreich– insbesondere dann, wenn der Benutzer keine Zeit zum Lesen von zu viel Text hat.

Im selben **Systemeigenschaften-Applet** verfügt jede Registerkarte über mehrere GroupBoxes mit unterschiedlichen Steuerelementen für verschiedene Aufgaben. Neben jeder Gruppe wird eine relative Grafik platziert, die die Aufgabe der Steuerelementgruppe leicht bezeichnen würde. Diese Art von grafischem Code ähnelt der Farbcodierung in physischen Dateien oder Parkflächen. Dies funktioniert auch nach dem gleichen Prinzip, dass mindestens einige Visuals in einem Magazine-Artikel enthalten sind– es sorgt für das Interesse des Lesers.

Die Auswahl des richtigen Symbols ist ebenfalls wichtig. Microsoft stellt im Rahmen Visual Studio 2005 viele Standardgrafiken bereit. Dies wäre die beste Wahl. Wenn Sie ihre eigenen Symbole erstellen, wird dringend empfohlen, die Standards auf Betriebssystem- oder Anwendungsebene für diese Grafiken zu befolgen, wie oben im Abschnitt [Standards verwenden](#use-standards) beschrieben.

Die Windows Richtlinien für die Interaktion mit der [Benutzeroberfläche](/windows/apps/desktop/) enthält eine sehr hilfreiche Anleitung zum Erstellen Windows [Stilsymbole.](https://msdn.microsoft.com/library/aa511280.aspx)

### <a name="simplify-recognition-with-headers"></a>Vereinfachen der Erkennung mit Headern

Header sind die perfekte Möglichkeit, den gesamten Dialog in einem einzigen Satz (und optional in einer Grafik) zu erklären. Manchmal können Header ihnen sogar dabei helfen, die Navigation und befehle in ihnen zu unterstützen. Header funktionieren effektiver als normale Beschreibungsbezeichnungen, da sie dem Benutzer als Erstes angezeigt werden, wenn der Dialog angezeigt wird.

Die Windows Installer-Assistenten sind möglicherweise die beliebtesten Header: ein einfaches Symbol ganz rechts. eine Titelbezeichnung, die das Dialogfeld beschreibt (z. B. Installationsordner auswählen); und eine Unterüberschrift, die den Zweck des Dialogfelds beschreibt (z. B. Wählen Sie den Ordner aus, in dem die Softwaredateien installiert werden sollen).

Angenommen, wir verfügen über eine typische Geschäftsanwendung mit einem Kontoabschnitt. Nach dem Designparadigma von Windows Vista können wir unternehmenskritische Informationen und zugehörige Befehle in der Kopfzeile (oder Fußzeile, wenn das Szenario dies erfordert) selbst angeben. Unser Benutzer hat die Kontodatei für "Big Company" geöffnet, und der Header würde in etwa wie im folgenden Screenshot aussehen.

![Screenshot eines Dialogfelds, das eine ausführliche Fußzeile enthält.](images/humanux-06.png)

Der folgende Screenshot zeigt ein Beispiel für einen detaillierten Header in einem Dialogfeld.

![Screenshot eines Dialogfelds, das einen detaillierten Header enthält.](images/humanux-07.png)

Auf ähnliche Weise können Sie vermeiden, Windows Aufgabenbereiche im XP-Stil hinzufügen zu müssen , insbesondere wenn Sie nur wenige Befehle verwenden, die viel vertikalen Platz verschwenden würden, indem Sie diese Befehle in den Header verschieben.

Beim Entwerfen von Headern sollten Sie einige Dinge beachten:

-   Stellen Sie sicher, dass sich die Hintergrundfarbe von der Hintergrundfarbe des Dialogfelds unterscheiden. Häufig wird ein weißer Header über einer standard-Windows systeminternen Steuerelementfarbe verwendet. Wenn Sie jedoch sicherstellen möchten, dass ihr Header nicht durch ein spezielles Design oder benutzerdefinierte Farben verunreinigen, zeichnen Sie einen **LinearGradient** mithilfe von **Color.FromKnownColor** mit den Farben **ControlLight** und **ControlDark**.
-   Behalten Sie nach Möglichkeit die Höhe Ihres Headers unter 150 Pixel bei. Normalerweise wird eine Höhe von 100 oder 120 erreicht. Als allgemeine Regel stellen Sie sicher, dass sie kleiner als 1/4 der Höhe des gesamten Formulars ist.
-   Wenn Sie die in der obigen Kopfzeile angezeigten Informationen direkt bearbeiten möchten, ersetzen Sie LinkLabel dynamisch durch ein Textfeld, und tauschen Sie sie erneut aus, sobald die Bearbeitung erfolgt ist.
-   Wenn Sie über eine Titelbezeichnung mit einer Schriftart von mehr als 10 Pt verfügen, verwenden Sie Arial oder Gegenüber Medium. MS Sans Serif sieht zu verknackt und unprofessionell aus. Eine Empfehlung in der Dokumentation zu XP-Entwurfsrichtlinien finden Windows Medium Von Sollen. Verwenden Sie für Anwendungen Windows Vista die Segoe UI Schriftart, die die Standardschriftart des Systems ist.

### <a name="use-custom-message-boxes"></a>Verwenden benutzerdefinierter Meldungsfelder

Die im Standard-Nachrichtenfeld Windows Optionen sind sehr begrenzt. Wenn Sie Ihrem Benutzer eine Frage stellen müssen, die nicht mit einem einfachen Ja/Nein oder OK/Abbrechen beantwortet werden kann, wird dies kompliziert.

Windows anwendungen werden jetzt aufgrund der großen Menge nicht technischer Benutzer einfacher zu verwenden. Manchmal kann es viel einfacher sein, Schaltflächen mit freundlicheren Texten und sogar einigen zusätzlichen Steuerelementen (z. B. LinkLabels) zur Verfügung zu stellen, um die Durchführung der aufgabe zu vereinfachen.

Die Microsoft .NET Framework erleichtert die Implementierung benutzerdefinierter Dialoge. Indem Sie dem benutzerdefinierten Dialogfeldformular einfach eine Reihe von Eigenschaften oder eine einzelne Codezeile zuweisen, kann das Formular wie ein Standardmeldungsfeld funktionieren. Legen Sie in einem Schaltflächenklickereignis die **DialogResult-Eigenschaft** des Dialogfelds auf **DialogResult.Ok** oder **DialogResult.Cancel fest.** Verwenden Sie **die ShowDialog( \[ OwnerForm \] )-Methode** aus dem übergeordneten Formular. Diese Methodenmethode gibt den **DialogResult-Wert** zurück.

Sie können alle **DialogResult-Member** verwenden. Diese Optionen werden auch von der **MessageBox.Show-Standardmethode** verwendet.

Alternativ können Sie einfach die **AcceptButton-Eigenschaft** des Dialogfelds auf **btnOK** und die **CancelButton-Eigenschaft** auf **btnCancel festlegen.** Dadurch werden die Tasten **ENTER und** **ESC** automatisch den jeweiligen Click-Ereignissen der **BtnOK-** und **btnCancel-Schaltflächen** zuordnen.

Hier sind einige Tipps zum Einrichten Ihrer benutzerdefinierten Dialoge:

-   Stellen Sie für komplizierte Themen Links zur lokalen oder Onlinehilfe mit einem LinkLabel mit dem Hinweis "Weitere Informationen" unter der entsprechenden Textbezeichnung zur Verfügung.
-   Verwenden Sie anstelle der Schaltflächen Ja Nein Abbrechen Texte, die das Ergebnis des Klickens auf die Schaltfläche deutlich machen, z. B. "Datei speichern und /  /  beenden", "Beenden ohne Speichern" und "Nicht beenden". Halten Sie sich jedoch nach Möglichkeit an die **Standardschaltflächen** / **Ja Nein,** **OK** / Abbrechen und solche Standardschaltflächen. Vertrautheit sorgt für eine hohe Produktivität.
-   Behalten Sie links (oder rechts abhängig von den Einstellungen der Zielkultur) einen Randbereich von 50 Pixeln bei, und fügen Sie ein Symbol hinzu, das das Szenario für den Dialog darstellt. Wenn es sich um ein Informationsdialogfeld, können Sie das Symbol "i" verwenden, das von Standardmeldungsfeldern verwendet wird. Wenn es sich um ein Sicherheitsdialogfeld geht, können Sie ein Sperrsymbol oder ein Schlüsselsymbol verwenden. Visual Studio 2005 ist mit einigen hochwertigen Grafiken enthalten.
-   Stellen Sie immer sicher, dass Sie die richtige Tastaturnavigation für diese Schaltflächen bereitstellen. Benutzer verwenden die Tastenkombinationen für Meldungsfelder (z. B. O für OK, Y für Ja, C für Abbrechen und so weiter). Sie finden es sicherlich lästig, wenn Sie sie nicht in Ihrem benutzerdefinierten Dialog verwenden würden.

### <a name="include-alternate-commands"></a>Include Alternate Commands

Zwei wichtige Faktoren bestimmen die Notwendigkeit alternativer Eingabemethoden: Frust und Trägheit. Frust tritt für Computerbenutzer zu oft auf. Wenn Sie frustriert sind, möchten Sie, dass Ihre Aufgabe schnell erledigt wird. Ein zusätzlicher Klick oder eine zusätzliche Wartezeit von einigen Sekunden macht eine Person, die unter Belastung steht, wirklich zu Einer– Sie wissen, wie es ist, wir waren alle dort. Trägheit führt häufig dazu, dass Sie die Aufgabe entweder nur mit der Tastatur oder der Maus beenden – je nach dem, was Sie gerade verwenden. Abgrenzend zu diesen beiden Faktoren erleichtert die Nutzung alternativer Eingabemethoden dem Benutzer jedoch das Ausführen von Aufgaben.

Wenn Sie z. B. auf beiden Seiten über ein Listenfeld mit zwei Schaltflächen verfügen – "Hinzufügen" und "Entfernen", sollten Sie ein Kontextmenü für dieses Listenfeld mit Menübefehlen hinzufügen, die diesen Schaltflächen ähnlich sind. Dies gibt dem Benutzer die Möglichkeit, die Methode zu wählen, die er am besten findet. Benutzerfreundlichen Benutzern, wie Windows Vista User Experience Guidelines (Benutzerfreundlichkeitsrichtlinien für Vista) angezeigt wird, verwenden Sie kontextmenüs sehr, und erwarten Sie, dass sie sich an einer beliebigen Stelle mit der rechten Maustaste auf diese Benutzer klicken.

Auf ähnliche Weise verwenden wir visuelle Steuerelemente für Text- oder numerische Eingaben. Beispielsweise werden Schieberegler verwendet, um ganze Zahlen anzugeben, und Calendar-Steuerelemente werden für Datumseingaben verwendet. Manchmal ist es bequemer, nur eingaben zu müssen, indem Sie eingeben. Es kann für den Benutzer häufig einen Unterschied machen, wenn Sie ein numeric Up-Down-Steuerelement hinzufügen, das mit einem Schieberegler verknüpft ist, oder ein DateTimePicker-Steuerelement anstelle des Calendar-Steuerelements verwenden.

### <a name="how-to-handle-critical-actions"></a>Behandeln kritischer Aktionen

Wenn Sie eine wichtige, nicht behebbare Funktion ausführen, ist es im Allgemeinen eine bewährte Methode, ein Meldungsfeld-Popupfenster zu öffnen, um die Aktion zu bestätigen. Lassen Sie uns dies eine Notch nach oben nehmen. Im folgenden Screenshot sehen Sie ein ähnliches benutzerdefiniertes Meldungsfeld, aber mit einem zusätzlichen Vorteil– einem timer, der visuell mithilfe einer Statusleiste angezeigt wird.

![Screenshot eines Dialogfelds für kritische Aktionen.](images/humanux-08.png)

Es gibt einige szenariospezifische Varianten, die Sie verwenden können. Wenn die zu ergreifende Aktion sehr kritisch ist (von der Überlastung eines Löschbetriebs bis hin zum dauerhaften Löschen von Dateien), sollte die Standardaktion nach dem Timerausfall abgebrochen werden. Der Dialog sollte nicht entfernt werden, sondern die Textbezeichnung ändert sich, um anzuzeigen, dass die Aktion abgebrochen wurde. Der Benutzer kann den Befehl oder den Abbruch bestätigen.

Stellen Sie immer sicher, dass Schaltflächen, die kritische Vorgänge ausführen, klar gekennzeichnet sind. Verwenden Sie immer Klartext, der die Aktion genau beschreibt. Wenn die Aktion das Löschen von Dateien ist, schreiben Sie nicht "Dateien aus Repository entfernen". Schreiben Sie "Dateien aus Repository löschen". Wenn beim Arbeiten mit Dateilisten mit einem Menübefehl Löschen die ausgewählten Dateien von der Festplatte selbst gelöscht werden (anstatt nur aus der Dateiliste zu entfernen), sollten Sie dies richtig hervorheben und explizit darauf hindeinformationen, dass die Dateien durch die Aktion dauerhaft gelöscht werden.

Jemand hat einmal gesagt: "Sie sind so gut wie Ihre schlechteste Arbeit." Dasselbe gilt für Softwareanwendungen. Eine einzelne schlechte Erfahrung mit Ihrer App kann einen großen negativen Eindruck auf den Benutzer hinterlassen. Um sicherzustellen, dass dies nicht geschieht, können Sie sicherstellen, dass ihre Anwendung ordnungsgemäß ausläuft, wenn sie abstürzt. Wenn Sie die Datenwiederherstellung hinzufügen oder dem Benutzer erlauben können, eine Kopie dieser Daten zu speichern, kann dies ein großes Plus sein. Der Benutzer sollte ordnungsgemäß benachrichtigt werden, wenn die Anwendung abstürzt. Ein JIT-Debugger oder ein kritischer Fehlerdialog ist nicht gut. Während der Umgang mit Abstürzen über den Rahmen dieses Artikels hinausgeht, wird empfohlen, dass ein einfacher Dialog, der sich beim Benutzer entlogt und ihn über die Situation informiert (und möglicherweise mit einem Link zu mehr Informationen zur Wiederherstellung nach diesem Absturz) für den Benutzer sehr hilfreich ist.

Wenn Sie einen Schritt weiter gehen möchten, können Sie dies tun, was eine meiner bevorzugten Grafikentwurfsanwendungen tut. Wenn es abstürzt, wird ein Wiederherstellungsdialogfeld angezeigt, in dem Sie eine separate Kopie der Bearbeiteten Datei speichern können. Anschließend erhalten Sie ein Feedbackdialogfeld, in dem Sie Informationen zum Absturz eingeben (persönliche Informationen natürlich optional) und an die Ersteller senden können.

### <a name="radiobuttons-or-comboboxes"></a>RadioButtons oder ComboBoxes?

Auf den ersten Blick scheint die Methode zum Treffen einer 1:n-Auswahl nicht so schwierig oder wichtig zu sein. Manchmal kann dies der Fall sein– insbesondere, wenn es sich bei dem Szenario um eine Anwendung handelt, die für zeitempfindliche Arbeit verwendet wird.

Sehen wir uns ein Beispiel aus der realen Welt an. Microsoft hat vor Kurzem eine Vorschauversion einer Grafikanwendung veröffentlicht: Ausdrucksgrafik-Designer (früher mit dem Codenamen "Acryl"). Ich hatte ungefähr 20 Grafikobjekte, denen ich in dieser Anwendung eine bestimmte Eigenschaft separat zuweisen musste. Es war ein dreärer Prozess. Dazu musste ich das Objekt auswählen, auf die Schaltfläche klicken, um das Einstellungsfenster anzuzeigen, und die Optionen festlegen. In einer solchen Option mussten zwei Optionen aus einer ComboBox ausgewählt werden, wie im folgenden Screenshot zu sehen ist.

![Screenshot des Dialogfelds für die Textur des Ausdrucksgrafik-Designers.](images/humanux-09.png)

Wenn Sie die ComboBox-Liste in der Dropdownliste ablegen und das zweite Element (von nur zwei Elementen) auswählen müssen, kann dies wirklich i irritierend sein. Was wir im Allgemeinen nicht erkennen, ist die Zeit, die benötigt wird, bis die Dropdownliste angezeigt wird. Sie kann viel Zeit verschwenden und frustrierend sein. Dies lässt sich problemlos lösen, indem Sie eine GroupBox mit zwei RadioButtons verwenden– insbesondere dann, wenn so viel Speicherplatz verfügbar ist. Ich habe ähnliche Probleme in Anwendungen wie CorelDRAW, Microsoft Access und anderen festgestellt.

Neben der Verschwendung von Zeit aufgrund der Dropdownanimation verschwendet sie auch unsere "mentale Bandbreite". Mit zwei "immer sichtbaren" RadioButtons würde unser Denken die Position des Cursors, auf den geklickt werden soll, subliminär kennen. Mit comboBox wird sie erst verarbeitet, nachdem die Liste gezeichnet wurde. Obwohl es zu unwichtig erscheinen mag, ist es tatsächlich sehr wichtig.

Manchmal ist es besser, RadioButtons zu verwenden, insbesondere, wenn Sie über 4 Auswahlmöglichkeiten oder weniger verfügen.

### <a name="never-disrupt-the-user"></a>Unterbrechen Sie niemals den Benutzer!

Dies ist das destruktivste, was ein Entwickler für Benutzer tun kann, wenn sie sich nicht mit dem Kopf bewaffnen. Wenn Ihre Anwendung den Benutzer unnötig oder anderweitig unterbricht, während er mit einem Meldungsfeld oder einer Taskleiste an einer anderen Anwendung arbeitet, erhalten Sie negative Punkte vom Benutzer.

Taskleisten-Flashs können natürlich nützlich sein, sollten aber nur aufgerufen werden, wenn der Prozess Ihrer Anwendung Eingaben des Benutzers erfordert, um fortzufahren, oder wenn Sie dem Benutzer etwas Kritisches vermitteln müssen. Wenn der Benutzer die Taskleiste im automatischen Ausblenden beibehalten hat, kann eine blinkende Taskleistenschaltfläche den Benutzer am Zugriff auf die Statusleiste oder andere unterankerte Steuerelemente versperren, da die Taskleiste darüber angezeigt wird. Sie wird erst wieder angezeigt, wenn der Benutzer auf die blinkende Schaltfläche geklickt hat.

![Screenshot eines Popupfensters.](images/humanux-10.png)

Popupfenster (siehe Abbildung 10), die durch Instant Messaging-Clients wie MSN Messenger bekannt wurden, sind eine hervorragende Lösung, um den Benutzer über etwas zu informieren, ohne ihn zu stören oder seinen Arbeitsablauf zu stören. Es gibt einen großartigen Artikel ( https://docs.microsoft.com/archive/msdn-magazine/2005/september/sprinkle-some-pizzazz-on-your-plain-vanilla-windows-forms-apps) von Bill Bill Zum Erstellen von Popupfenstern. Es ist eine gute Richtlinie (und Eine- und Manieren), die Popups anderer Anwendungen nicht zu stören. Das Verhindern solcher Fenster kann lästig und unproduktiv sein. Eine Lösung besteht in der Verwendung des vom Betriebssystem bereitgestellten ToastSemaphore Mutex (/library/WinMessenger/winmessenger/overview/toast.asp), um Popupkollisionen zu vermeiden.

Manchmal müssen Sie möglicherweise mehrere Elemente nach dem Popup anzeigen. Das Aufblenden von 3 oder mehr Popups wäre nicht wirklich ratsam. Stattdessen wäre es besser, die einzelnen Popups durcheinander zu fahren, indem sie ein Popup nach dem anderen poppen/ausblenden. Microsoft Outlook implementiert eine ähnliche Lösung, wenn der Benutzer über eingehende E-Mails benachrichtigt wird.

### <a name="provide-progress-status"></a>Status des Status bereitstellen

Häufig gibt es Aufgaben, bei denen der Benutzer warten muss. Dies ist natürlich eine der Dinge, die der Benutzer einfach hasst. Schlechter ist es jedoch, wenn sie warten, ohne zu wissen, was passiert. Manchmal muss Ihre Anwendung möglicherweise eine Verbindung mit einem Webdienst oder einem Remotecomputer herstellen oder große Datenbrocken verarbeiten. Aus welchem Grund auch immer, der Benutzer sollte darauf aufmerksam gemacht oder zumindest unentdeckt wissen, was im Hintergrund passiert. Je nach Situation gibt es verschiedene Methoden dafür.

Wenn Sie eine Verbindung mit einem weit entfernten Objekt herstellen, z. B. einem Webdienst oder etwas, das sich auf einem Netzwerk oder Internetserver befindet, empfiehlt es sich, ein einfaches Statusdialogfeld (siehe folgende Abbildung) oder eine Statusleiste anzuzeigen, die in der Statusleiste gehostet wird. Eine zugehörige Bezeichnung sollte den aktuellen Status des Prozesses beschreiben. Wenn Sie beispielsweise eine Verbindung mit einem Webdienst herstellen, um einige Daten zu verarbeiten, sagen Sie einfach "Verbindung mit Webdienst herstellen... " oder "Please wait, processing... " Wenn dieser Prozess synchron ist, ist es ratsam, alle Steuerelemente zu deaktivieren, auf die der Benutzer zugreifen kann, bis der Prozess abgeschlossen ist, oder den Fortschritt einfach als modales Dialogfeld anzuzeigen.

![Screenshot eines Statusleistendialogfelds.](images/humanux-11.png)

Es wird dringend empfohlen, den Statusleistenstil auf den Modus "Marquee" zu setzen, wenn Sie eine Statusleiste verwenden und die Verarbeitungszeit unbekannt ist oder wenn Sie keinen Höchstwert haben.

Eine weitere Methode, die immer beliebter wird, ist ein festes Popupfenster, das den Fortschritt anzeigt. Microsoft AntiSpyware-Downloader/-Updater oder die Popups zum Scannen von E-Mail-Adressen von Anti-Anti Antivirus sind gute Beispiele dafür. Dies sollte natürlich nur für asynchrone Prozesse verwendet werden. Andernfalls kann sich der Benutzer verunsichert fühlen. Solche Fenster werden am besten für die Hintergrundverarbeitung wie das Herunterladen eines Updates oder das Ausführen einer geplanten Aufgabe verwendet und sollten nie auf "Immer oben" festgelegt werden.

### <a name="simplify-complex-steps-with-wizards"></a>Vereinfachen komplexer Schritte mit Assistenten

Es ist sicher davon auszugehen, dass ein typischer Benutzer ohne Ende verwirrend ist, wenn er mit einer Vielzahl von Steuerelementen in einem einzelnen Formular konfrontiert wird. Manchmal kann keine Menge an Gruppierung, Größe oder Abstand Ihnen helfen, wenn Sie über viele wichtige Steuerelemente verfügen.

Ein Assistent ist das Beste für solche Szenarien. Sie können Steuerelemente nach Anwendbar nach Aufgabe oder Kategorien unterteilen und in separaten Schritten platzieren. Dies kann dem Benutzer helfen, den Fokus zu halten und sich nicht von der Aufgabe zu vermuten. Sie können schritt- oder aufgabenspezifische Hilfe mithilfe einer Hilfeschaltfläche bereitstellen. Richtlinien zur Erstellung des Assistenten finden Sie in der MSDN Library.

Assistenten sind auch eine gute Möglichkeit, um die Erstkonfiguration Ihrer Anwendung zu unterstützen. Viele Anwendungen verwenden einen solchen Assistenten, um eine personalisierte Konfiguration direkt nach Abschluss des Setups oder bei der ersten Verwendung einzurichten. Ein solcher erster Assistent sollte auch optional sein. Wenn der Benutzer zu einem beliebigen Zeitpunkt abbricht, werden die nicht angegebenen Einstellungen zu standardwerten. Wenn Sie den Assistenten ein wenig grafisch gestalten können (siehe Abschnitt [Use Pretty Graphics(](#use-pretty-graphics) Verwenden von ziemlichen Grafiken), wird die Konfiguration viel einfacher.

### <a name="get-the-tone-of-your-text-right"></a>Get the Tone of Your Text Right

In der [Windows User Experience Interaction Guidelines](/windows/apps/desktop/)wurde ein sehr wichtiger Punkt zu "Textton" gemacht. Dies ist der Eindruck und das Gefühl, der durch den Text in Ihrer Anwendung vermittelt wird. Dies kann von einer einfachen QuickInfo bis zu einem Anweisungsbezeichnungssteuerzeichen-Steuerelement sein.

Zuvor wurde die Änderung des Texts in der Webcamoption in MSN Messenger erläutert. Dies wird als richtiger Textton bezeichnet. Beim Umgang mit nicht technischen oder unerfahrenen Benutzern hat das Abrufen der Nachricht einen anderen Aspekt.

Wenn Sie "Zielpfad" über einem Textfeld in einer selbst extrahierenden Anwendung schreiben, kann ein technischer Benutzer leicht erkennen, dass Sie etwas wie "C: \\ Temp \\ MyPath" eingeben. Ein unerfahrener Benutzer (denken Sie an "Mom") kann ebenso leicht verdreut werden und müsste sich auf das Handbuch beziehen, den technischen Support anrufen oder schlechteres – geben Sie auf. Eine gute Alternative ist die Angabe, was der Benutzer tun soll: "Wählen Sie den Ordner aus, in dem Sie diese Dateien speichern möchten." Sie können sogar "Durchsuchen" umbenennen. " neben diesem Textfeld auf "Ordner auswählen... "

Wenn Sie eine klare Beschreibung der Vom Benutzer zu tunden Maßnahmen bereitstellen, wird auch die Notwendigkeit von Hilfedateien geringer oder zumindest die Details, die In Hilfedateien enthalten sein müssen.

Ein sehr guter Vorschlag aus der Windows [User Experience Interaction Guidelines](/windows/apps/desktop/) gilt für jede Software. Er gibt an, dass der Writer die Text-Konversation behalten soll. In den Richtlinien wird dies so definiert: "Vermeiden Sie Wörter, die Sie einer anderen Person nicht persönlich sagen würden."

Einige Tipps zum Schreiben von Text:

-   Vermeiden Sie es, über den Benutzer in der dritten Person zu sprechen. Sagen Sie "Sie" anstelle von "Der Benutzer".
-   Verwenden Sie nach Möglichkeit "Mein Name:" oder "Meine E-Mail-Adresse:" anstelle von "Name:" oder "E-Mail:".
-   Wenn Sie mehrere Optionen festlegen, schreiben Sie den Text aus der Perspektive des Benutzers. Wenn Sie z. B. zwei RadioButtons unter einer Bezeichnung wie "Select permission for Username on this network" über zwei \[ \] RadioButtons wie "Allow" und "Deny" haben, ersetzen Sie den RadioButton-Text durch "I want to allow Username" und \[ \] "I want to disallow \[ \] Username".
-   Unterstrichen Sie Text nur, wenn er für Links verwendet wird. Es verwirren den Benutzer, wenn der unterstrichene Text kein Link ist.
-   Achten Sie auf wichtige Informationen mit einer fett formatierten Bezeichnung, verwenden Sie sie jedoch sorgfältig. Zu viel fett formatierten Text ist verwirrend und verringert die Gesamtwirkung des Formulars.
-   Stellen Sie beim Schreiben des Texts für ein Kontrollkästchen sicher, dass Sie leicht wissen, was geschieht, wenn er ausgewählt und deaktiviert oder deaktiviert ist. Es wird empfohlen, den Text direkt als Ergebnis des aktivierten Kontrollkästchens zu schreiben. Schreiben Sie beispielsweise "Send me helpful information from your partners" (Hilfreiche Informationen von Ihren Partnern senden) anstelle von "Do not send me helpful information from your partners". Ich kann mir zwar vorstellen, dass viele Marketingabteilungen über dieses spezielle Beispiel sprechen, aber ich bin sicher, dass Sie wissen, was ich meine.
-   Wenn Sie über ein schaltflächenbasiertes Steuerelement (in der Regel ein RadioButton mit einer Befehlsschaltfläche) verfügen, das Aktiviert/Deaktiviert steuert, stellen Sie sicher, dass Sie es ordnungsgemäß beschriften. Wenn der Prozess aktiviert ist, schreiben Sie "Aktiviert" anstelle von "Aktivieren" oder "Deaktivieren". Wenn Sie Aktiviert schreiben, wird der aktuelle Status angezeigt. Wenn auf die Schaltfläche geklickt (aktiviert) und die Schaltfläche "Aktivieren" lautet, kann dies verwirrend und problematisch sein. "Aktivieren" fordert den Benutzer möglicherweise auf, darauf zu klicken, da der Prozess nicht aktiv ist.

### <a name="sometimes-a-listview-is-better"></a>Manchmal ist eine ListView besser

Wir bleiben häufig bei DataGrid oder ListBox oder sogar ComboBox für Auswahlaufgaben, aber mit Windows XP und höheren Versionen von Windows kann die Verwendung einer ListView Ihnen größere Optionen bieten.

Die Feinpunkte des ListView-Steuerelements:

-   Beschleunigt die Erkennung von Elementen mit Symbolen und Bitmaps.
-   Zeigt zusätzliche Informationen mit Details- oder Kachelansichten an.
-   Mit Visual Studio 2005 können Sie sogar Gruppen für zusätzliche Kategorisierungen haben. Gruppen umfassen alle Ansichten und sind flexibel. Gruppen können auch verwendet werden, um eine Hierarchieansicht (z. B. eine TreeView) zu flachen, in der mehr untergeordnete Knoten als übergeordnete Knoten enthalten sind. Ein gutes Beispiel hierfür ist das Dialogfeld Netzwerkverbindungen in Windows XP, wenn es mit "In Gruppen anzeigen" angezeigt wird und die Ansicht auf Details festgelegt ist.
-   Um ein ListView-Steuerelement anzupassen, zeichnen Sie es manuell, indem Sie die **OwnerDraw-Eigenschaft** festlegen und die **DrawItem-** und **DrawSubItem-Ereignisse** verwenden.
-   Unterstützt die schnelle, ortsbasierte Bearbeitung von ListView-Elementen.
-   Unterstützt problemlos manuelle Neuanordnungen.
-   Ermöglicht Benutzern die Auswahl der Ansicht (große Symbole, kleine Symbole, Liste und so weiter), mit der sie am besten zu tun haben.

### <a name="simplify-navigation-with-breadcrumb-controls-and-sidebars"></a>Vereinfachen der Navigation mit Breadcrumb-Steuerelementen und Randleisten

"Untergeordnete Navigation" ist der Schlüssel für die komplexe Benutzeroberfläche. Manchmal können Sie eine komplizierte Benutzeroberfläche nicht umgeht. In einer solchen Situation ist es am besten, die Benutzerfreundlichkeit so einfach wie möglich zu gestalten. Eine Randleiste, die aus Linkbezeichnungen besteht, oder eine TreeView für die hierarchiebasierte Navigation schlägt eine Navigation auf gleichgeordneter Ebene für die Aufgabe des aktuellen Dialogfelds vor. Dies erleichtert es dem Benutzer, zwischen den Schritten des Prozesses zu springen, während er weiß, wo er sich befindet.

Wenn Sie eine hierarchiebasierte Navigation mit TreeViews oder eine andere ähnlich komplexe Navigation verwenden, ist ein Breadcrumb-Steuerelement ein gutes Hilfsprogramm für den Benutzer. Obwohl Visual Studio noch nicht über ein integriertes Steuerelement verfügt, finden Sie unter [Creating A Breadcrumb Control](/archive/msdn-magazine/2005/july/advanced-basics-creating-a-breadcrumb-control) (Erstellen eines Breadcrumb-Steuerelements) Informationen zum Erstellen eines Steuerelements selbst. Ein Breadcrumb-Steuerelement erleichtert die Suche nach der aktuellen Position in Bezug auf die Hierarchie.

Die Breadcrumb-Navigation kann problemlos in den Header zusammengeführt werden, wenn das Formular über eins verfügt. Weitere Informationen finden Sie im vorherigen Abschnitt zu [Headern.](#simplify-recognition-with-headers)

### <a name="use-pretty-graphics"></a>Verwenden von "Pretty Graphics"

Anwendungen mit coolen Grafiken sind für alle benutzerecht – zumindest in der Mehrheit. Eine Benutzeroberfläche mit ansprechenden Grafiken ist zwar nicht für alle Anwendungen eine logische Wahl, aber sie trägt dazu bei, einen ansprechenden Eindruck zu machen, und kann ein Guter für die Arbeit sein. Natürlich sollten die Grafiken die Produktivität nicht beeinträchtigen, aber wenn sie richtig verwendet werden, können sie sie erhöhen!

Es müssen nicht viele Grafiken vorhanden sein, und sie erfordern auch nicht unbedingt viel Arbeit. Ein professionelles Begrüßungsbildschirm oder ein Header (wie zuvor erwähnt) führt den Trick aus. Wenn Ihr Budget dies zulässt, können Sie ansprechende Grafiken für Symbolleisten, Assistenten und vieles mehr verwenden. Sie machen Ihre App auch gut und professionaler. Dies ist ein feiner Effekt, aber ein professionelles Aussehen vermittelt Vertrauen und Stabilität. Wenn Sie ein relativ kleines Unternehmen sind, das Einzelhandelsanwendungen erstellt, ist dies ein wichtiger Aspekt, den Sie berücksichtigen sollten.

Machen Sie immer einen Punkt, um professionelle Grafiken zu verwenden. Lizenzfreie Grafiken sind einfach verfügbar und kostengünstig. Sie können auch einen Designer einstellen. Wenn Grafiken jedoch nicht Ihr Forte sind, probieren Sie es nicht selbst aus. Wenn Sie keine professionellen Grafiken abrufen oder verwenden können, ist es besser, sie überhaupt nicht zu verwenden.

Bei kleinen Grafiken können Sie immer die Symbole und Bitmaps verwenden, die mit Visual Studio 2005 geliefert werden. (Die Grafiken, die mit früheren Versionen ausgeliefert wurden, werden nicht empfohlen!)

### <a name="provide-resizable-forms-when-possible"></a>Bereitstellen von Formularen mit größenveränderlicher Größe nach Möglichkeit

Größenänderungsfähige Fenster ähneln auflösungsunabhängigen Fenstern. Auflösungsunabhängige Fenster sehen unabhängig davon gleich aus, ob Sie 96DPI- oder 300DPI-Bildschirme verwenden. Unabhängig davon, ob die Benutzeroberfläche Ihrer Anwendung auflösungsunabhängig ist, ist es besser, wenn die Größe geändert werden kann. Dies gilt natürlich nicht für viele Szenarien, ist aber eine gute allgemeine Regel.

Wenn ihr Fenster Listen beliebiger Art bearbeitet , insbesondere ListViews, wird dies noch wichtiger. Die Größenänderung ermöglicht es dem Benutzer, gleichzeitig mehr Daten zu betrachten.

Beispielsweise verfügen wir über eine Anwendung, in der der Benutzer ein Bild aus einer großen Sammlung auswählen muss. Mit dem dialogfeld "Öffnen" können Sie eine Miniaturansicht auswählen, aber das Dialogfeld hat eine feste Größe, und die Miniaturansichtsliste zeigt nur vier Miniaturansichten gleichzeitig an. Wenn die Sammlung 100 Bilder enthält, kann das Scrollen und Suchen – eine sich wiederholende Aufgabe – ziemlich mühsam und eine Verringerung der Effizienz sein. Wenn die Größe des Dialogfelds geändert werden kann, kann der Benutzer ihn so groß wie bequem oder mindestens so groß wie der Bildschirm machen und die Aufgabe schnell abschließen können. Wenn Ihre Liste horizontal scrollt , z. B. eine detaillierte ListView oder DataGrid, ist dies noch mühsamer! Fenster mit größenveränderlicher Größe sind in einer solchen Situation sehr hilfreich.

### <a name="provide-more-functionality-with-sidebarstask-panes"></a>Bereitstellen weiterer Funktionen mit Randleisten/Aufgabenbereichen

Wie die zuvor erwähnten Header sind Randleisten und Aufgabenbereiche eine hervorragende Möglichkeit, zusätzliche Funktionen und Hilfsprogrammbefehle bereitzustellen. Beispielsweise sind die Aufgabenbereiche in Office Word 2003 sehr praktisch, zugänglich und nicht intrusiv. Sie funktionieren auch asynchron, wenn sie eine Verbindung mit Onlineressourcen herstellen, wodurch dem Benutzer die Option für mehrere Aufgaben zur Verfügung steht.

Das Erstellen eines Aufgabenbereichs oder einer Randleiste ist genauso einfach wie das Erstellen eines Andockbereichs, mit der Option, eine slick-Grafik oben als Titelleiste zu verwenden. Hierfür können Sie sogar ein farbiges Label-Steuerelement verwenden. Es gibt viele Möglichkeiten für Aufgabenbereiche.

Wenn Sie über zusätzliche Funktionen verfügen und diese nicht aufdringlich für Ihren Benutzer bereitstellen möchten, gibt es keinen Ort wie den Aufgabenbereich. Sie können Aufgabenbereiche auch "Automatisch im Hintergrund" machen oder wie die Visual Studio Toolfenster reduzieren.

### <a name="give-a-notification-choice"></a>Auswählen einer Benachrichtigung

Zuvor haben wir gesehen, wie sie ein benutzerdefiniertes Meldungsfeld erstellen. Wenn dem Benutzer in Ihrer Anwendung häufig ein Meldungsfeld angezeigt wird, kann es ratsam sein, ein Kontrollkästchen hinzuzufügen, das der Benutzer aktivieren kann, um die Anzeige dieses Dialogfelds in Zukunft zu deaktivieren. Eine solche Option eignet sich besonders gut für offensichtlichere Nachrichten.

Ein vertrautes Beispiel hierfür ist das Dialogfeld Visual Studio Suchen. Wenn Sie Text suchen oder ersetzen, wird Visual Studio ein Meldungsfeld mit den Ergebnissen angezeigt. Sie haben jedoch auch die Möglichkeit, dieses Meldungsfeld zu deaktivieren. Es kann sehr nervig sein, wenn Sie bei jeder Suche die EINGABETASTE drücken oder auf OK klicken müssen.

Eine weitere coole Sache, die Visual Studio macht, ist, dass auch wenn das Dialogfeld deaktiviert ist, die Ergebnisse dieses Vorgangs weiterhin in der Statusleiste angezeigt werden.

### <a name="provide-tooltips"></a>Geben Sie QuickInfos an!

Manchmal können QuickInfos Viel Zeit sparen. Schaltflächen, Kontrollkästchen und andere Steuerelemente können mehrdeutig sein, und der Benutzer ist möglicherweise nicht sicher, was zu tun ist. QuickInfos bieten die beste Form kontextabhängiger Hilfe in nur einer Zeile. Der Benutzer kann schnell entscheiden, was zu tun ist, ohne in der Hilfedatei nach etwas zu suchen oder ein anderes Fenster zu öffnen.

Personen überspringen dies häufig in ihren Anwendungen. Legen Sie einen Punkt fest, um QuickInfos zu allen mehrdeutigen Steuerelementen oder nach Möglichkeit allen Steuerelementen hinzuzufügen. Wiederholen Sie nicht den Text einer begleitenden Bezeichnung oder des eigenen Texts dieses Steuerelements, sondern geben Sie zusätzliche Informationen zu diesem Steuerelement an. Der Text sollte die Funktion des Steuerelements in wenigen Wörtern erklären.

### <a name="do-not-forget-the-little-things"></a>Vergessen Sie die kleinen Dinge nicht

Die kleinen Dinge können Sie verärgern, aber wenn Sie sie ignorieren, kann sich dies auf den Eindruck auswirken, den Sie hinterlassen. Ich habe einmal eine Anwendung verwendet, die von einer wichtigen Person in der Softwarebranche erstellt wurde, bei der borderStyle des Formulars auf Sizeable festgelegt war, die Steuerelemente auf der rechten Seite des Formulars jedoch nicht verankert wurden. Aus diesem Grund hatte die von einem Branchengewicht erstellte Anwendung ein nicht professionelles Gefühl.

Diese Arten von "kleinen Dingen" sind der Kern des gesamten Eindrucks. Die Benutzeroberfläche und die Benutzeroberfläche Ihrer Anwendung sind die Benutzer, auf denen Ihre Anwendung zumindest zuerst bewertet wird. Wenn sie offensichtliche Fehler in Ihrer Benutzeroberfläche sehen, wird Ihre Anwendung möglicherweise als weniger leistungsfähig und effektiv betrachtet.

## <a name="conclusion"></a>Zusammenfassung

Wir haben nur einen kleinen Teil der Benutzerfreundlichkeit berührt. Wenn die Benutzeroberfläche einfacher, effektiver, interessanter und benutzerfreundlicher wird, wird die Aufgabe, diese Benutzeroberfläche zu erstellen, so viel komplexer. Aber mit einigen Vorbereitungen und einer guten Planung können Sie eine hervorragende Benutzererfahrung schaffen.

Die beste Möglichkeit, die perfekte Benutzeroberfläche zu erstellen, besteht darin, Benutzerfreundlichkeitstests durchzuführen, die speziell auf die Benutzeroberfläche ausgerichtet sind – entweder mit einer speziellen Testgruppe oder selbst. Je mehr Zeit Sie mit dem Testen der Benutzeroberfläche verbringen, bevor Sie Ihre Anwendung freigeben, desto besser. Dadurch sparen Sie später viel Probleme.

 

 