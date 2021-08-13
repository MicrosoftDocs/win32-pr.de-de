---
title: Erstellen von Animationen
description: Erstellen von Animationen
ms.assetid: 6d5c3c61-b3f2-4505-aa43-b6d001c444a5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ed5955e57af405451def3208902678d3d6a0ffb9857cc719bfe100dbbd2447f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118752328"
---
# <a name="creating-animations"></a>Erstellen von Animationen

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

Um mit dem Erstellen von Animationen für Ihr Zeichen zu beginnen, wählen Sie **das Symbol Animationen** in der Struktur aus. Dadurch wird die **Seite Eigenschaften** mit den Standardeinstellungen für alle Animationen angezeigt. Sie können die Framegröße, die Standardrahmendauer und die Farbpaletteneinstellungen auf der **Seite Eigenschaften** ändern.

### <a name="setting-your-characters-frame-size"></a>Festlegen der Framegröße Ihres Zeichens

Die Höhe und Breite des Animationsframes muss in der gesamten Zeichendefinition konstant bleiben (d. h. für alle Animationen dieses Zeichens). Obwohl Sie die Framegröße von der Standardeinstellung (128 x 128 Pixel) ändern können, werden im Editor angezeigte Bilder an die Standardanzeigegröße skaliert. Wenn Sie die Standardframeeinstellung ändern, können Sie die vollständige, nicht skalierte Größe des Frames anzeigen, indem Sie im Menü Bearbeiten auf Framefenster **öffnen** klicken. 

### <a name="setting-your-characters-palette"></a>Festlegen der Zeichenpalette

Standardmäßig verwendet der Editor das erste Bitmapbild, das Sie laden, um die Standardfarbpalette Ihres Zeichens festzulegen,<sup></sup> die Farben, die bestimmen, wie das Zeichen angezeigt wird, und legt die Farbe an der 11. Palettenposition als Transparenzfarbe fest. Sie können die Palette und Transparenz jedoch explizit in der Gruppe **Paletteninformationen** festlegen. Dadurch können Sie eine Bilddatei angeben, die für die Palette verwendet werden soll. Sie können eine der Animationsbilddateien oder eine beliebige Grafikdatei angeben. Die palette-Datei, die Sie angeben, muss eine 8-Bit-Farbdatei (256) sein. Verwenden Sie nach dem Laden die Schaltfläche **Einstellung** ändern, um die Transparenzfarbe zu ändern.

Die Farbpalette Ihres Zeichens darf die Standardsystemfarben nicht neu zuplanen. Der Editor reservieren beim Anzeigen von Bildern automatisch die Farbpalette des Systems. Darüber hinaus müssen alle Ihre Animationsbilder die gleiche Farbpalette und Transparenzfarbe verwenden. Das ist sehr wichtig. Wenn sie dies nicht tun, wird möglicherweise eine Farbumverteilung Ihrer Bilder angezeigt, wenn Sie sie in den Editor laden.

Sie können zwar die Farbpalette für das Zeichen festlegen, aber auf Windows-Systemen, in denen die Anzeigeeigenschaften auf eine 8-Bit-Farbpalette (256) festgelegt sind, unterliegt die Farbe des Zeichens der aktuellen Systempalette. Da Anwendungen die Systempalette ändern können, wird das Zeichen möglicherweise nicht mit den richtigen Farbeinstellungen angezeigt. Obwohl es keine Möglichkeit gibt, dies zu verhindern, können Sie den Effekt mindern, indem Sie die Anzahl der verwendeten Farben einschränken und die Zeichenpalette basierend auf der Palette festlegen, die von der Anwendung verwendet wird, die das Zeichen verwendet. Wenn Sie beispielsweise ein Zeichen entwickeln, das mit Webseiten verwendet werden soll, können Sie die Palette des Zeichens mithilfe der Halbtonpalette von Microsoft Internet Explorer festlegen. Sie können die Palette des Browsers erfassen, indem Sie mit der  rechten Maustaste auf ein Bild  auf einer Webseite klicken, den Befehl Bild speichern unter auswählen und **bitmap** in der Option Als Typ speichern auswählen und dann auf **Speichern klicken.** Um Ihre Animationsbilddateien für eine bestimmte Palettendatei zu optimieren, sollten Sie ein Produkt wie Denk-Debabelizer verwenden.

### <a name="creating-a-new-animation"></a>Erstellen einer neuen Animation

Nachdem Sie ihre globalen Animationseinstellungen festgelegt haben, können Sie mit dem Erstellen von Animationen beginnen. Um eine neue Animation zu erstellen, wählen Sie **neue Animation** im **Menü Bearbeiten** oder die Schaltfläche Neue **Animation** auf der Symbolleiste aus. Dadurch wird der Struktur unter dem Symbol Animationen ein neues **Animationssymbol** hinzufügt, und dem neuen Symbol wird ein Standardname zugewiesen. Sie können Ihre Animation umbenennen, indem Sie in das **Feld Animationsname** eingeben. Beachten Sie, dass Animationsnamen innerhalb einer Zeichendefinition eindeutig sein müssen. Vermeiden Sie außerdem die Verwendung von Zeichen im Namen, die keine gültigen Zeichen für Dateinamen sind.

### <a name="adding-frames"></a>Hinzufügen von Frames

Jede Animation besteht aus Frames. Um einen neuen Frame für Ihre Animation zu erstellen, wählen Sie **im** Menü **Bearbeiten** oder auf der Symbolleiste Neuer Frame aus. Dadurch wird der Struktur unter dem Animationssymbol ein neues Framesymbol und drei Seiten im Registerkartenformat angezeigt. Die **Seite Allgemein** enthält Steuerelemente, mit denen Sie ein Bild für Ihren Frame laden und anpassen können. Sie enthält auch einen Anzeigebereich für die Darstellung des Frames.

![Screenshot: Bereich "Bild" mit Dateiname, Pfad und Position](images/f2charflame.gif)

Ein Frame kann ein oder mehrere Bilder enthalten. Um ein Bild für einen  Frame zu definieren, klicken Sie direkt über dem Listenfeld Bilder auf die **Schaltfläche Bilddatei** hinzufügen. Das **Dialogfeld Bilddateien** auswählen wird angezeigt, in dem Sie eine Bitmapbilddatei auswählen können.

![Screenshot, der zeigt, wie eine Bilddatei im Datei-Explorer ausgewählt wird.](images/f3chardialbox.gif)

Wählen Sie die Datei aus, die Sie laden möchten, wählen Sie **Öffnen** aus, und das Bild wird in der Frameanzeige auf der Seite **Allgemein** angezeigt. Der Editor akzeptiert Bilder, die als 1-Bit(monofarbig), 4-Bit- oder 8-Bit-Windows Bitmapformat oder als GIF-Format gespeichert sind.

Sie können die vier Pfeilschaltflächen unter dem Bild im Feld **Position** verwenden, um die Darstellung des Bilds im Rahmen anzupassen. Wenn das Bild größer als die Größe Ihres Frames ist, wird nur der Teil des Bilds angezeigt, der innerhalb des Frames angezeigt wird. Wenn Sie die Framegröße erhöhen, kann das Bild so skaliert werden, dass es in den Anzeigebereich des Editors passt.

Sie können einen Frame auch anzeigen, indem Sie im Menü Bearbeiten auf **Framefenster** **öffnen** klicken. Dadurch wird der aktuelle Frame in einem separaten Fenster angezeigt, ohne die in den Frame geladenen Bilder zu skalieren. Die Anfangsgröße dieses Fensters basiert auf den Einstellungen für Höhe und Breite Ihres Frames. Sie können die Größe kleiner, aber nicht größer ändern. Das Rahmenfenster spiegelt die Änderungen wider, die Sie mithilfe der Steuerelemente im Editor vornehmen. Außerdem können Sie den Frame anzeigen, während Sie die anderen Eigenschaftenseiten anzeigen.

![Screenshot: Bereich "Position"](images/f4charposctrl.gif)

Sie können einen Frame aus mehreren Bildern zusammenstellen. Jedes Mal, wenn Sie die **Schaltfläche Bild** hinzufügen und ein anderes Bild auswählen, wird das Bild der Liste und dem Bildanzeigebereich hinzugefügt. Sie können auch mehrere Bilder hinzufügen, indem Sie mehrere Dateien auswählen. Drücken Sie UMSCHALT ODER STRG, während Sie auf das Dialogfeld **Bilddateien** auswählen klicken, und wählen Sie dann **Öffnen aus.** Die **Schaltflächen Nach oben**  **und Nach** unten über dem Listenfeld Bilder verschieben ein ausgewähltes Bild in der Anzeige reihenfolge (z-Reihenfolge) für den Frame. Sie können Bilder auch verschieben, indem Sie sie in die Liste ziehen. Wenn Sie ein Bild in der Liste auswählen und auf die **Schaltfläche Löschen** klicken, wird ein Bild entfernt. Um ein Bild zu ändern, das Sie in eine andere Bilddatei geladen haben, können Sie auf den  Dateinamen klicken, um es direkt zu bearbeiten, oder mithilfe der Schaltfläche **...** (Auslassungstasten) das Dialogfeld Bilddateien auswählen öffnen und eine andere Datei auswählen.

![Screenshot, der die Schaltfläche mit den Ausellipsen zeigt.](images/f5charell.gif)

Mithilfe des **Textfelds Dauer** können Sie die Dauer für den Frame festlegen. Das heißt, wie lange der Frame angezeigt wird. Wenn ein Frame kein Bild und keine Dauer von 0 hat, wird der Frame nicht angezeigt, wenn die Animation abspielt.

Sie können auch eine Soundeffektdatei angeben, die beim Anzeigen des Frames abspielt werden soll. Wenn Sie das Zeichen von einem Webserver laden möchten, sollten Sie die Soundeffektdatei komprimieren, um die Ladezeit zu minimieren. Anschließend können Sie die komprimierte Sounddatei im Zeichen-Editor des -Agents angeben. Vermeiden Sie außerdem die Verwendung eines Soundeffekts mit einer längeren Dauer als die Dauer der Animation, und vermeiden Sie insbesondere einen Soundeffekt, der schleifend ist, da die Microsoft Agent-Animationsdienste erst dann ein vollständiges Animationsereignis senden, wenn der Sound abgeschlossen ist. Vermeiden Sie außerdem die Angabe eines Soundeffekts für  jede Animation, die Sie dem Zustände Lauschen oder Hören zuweisen, da dies die Spracheingabe beeinträchtigt.  Schließlich können Sie zwar mehr als einen Soundeffekt in eine Animation verwenden, aber vermeiden Sie es, sie so zu platzieren, dass sie sich überschneiden, da sich dies auf den Zeitpunkt der Animation auswirken kann. Beachten Sie außerdem, dass Soundeffekte je nach Hardware des Benutzers mit unterschiedlichen Raten abspielt werden können.

Um Ihrer Animation Frames hinzuzufügen, wählen Sie erneut **den Befehl Neuer Frame** aus, und führen Sie das gleiche Verfahren aus. Optional können Sie auch mehrere Bilder laden und automatisch neue Frames für sie generieren. Um dieses Feature zu verwenden, wählen **Sie im Menü** Bearbeiten die Option Neue Frames aus **Bildern** aus. Die Frames werden basierend auf den Bilddateinamen in alphabetischer Reihenfolge erstellt. Wenn Sie alle Frames für Ihre Animation definiert haben, können Sie den Befehl Neue **Animation** erneut auswählen, um eine neue Animation zu starten.

Es gibt andere Möglichkeiten, Umrahmen zu Animationen hinzuzufügen und Frames innerhalb oder zwischen Animationen zu verschieben. Sie können einen anderen Frame (aus derselben  oder einer anderen Animation) auswählen und Ausschneiden oder **Kopieren** auswählen, dann die Animation oder einen Frame in dieser Animation auswählen und **Einfügen auswählen.** Sie können auch einen Frame von einer Animation in eine andere ziehen. Wenn Sie innerhalb einer Animation ziehen, verschiebt die Aktion den Frame. Wenn Sie auf eine andere Animation ziehen, wird der Frame kopiert. Wenn Sie in derselben Animation auf einen vorangehenden Frame ziehen, wird der Rahmen vor dem Rahmen eingefügt, in den Sie ziehen. Wenn Sie auf einen folgenden Frame ziehen, wird er hinter dem Rahmen platziert, in den Sie ziehen. Wenn Sie einen Frame mit der rechten Maustaste ziehen, wird beim Loslassen der Schaltfläche ein Popupmenü mit Ihren Übertragungsoptionen angezeigt.

Sie können auch eine Animation erstellen, indem Sie eine vorhandene Animation kopieren (wählen Sie die Animation und dann **Kopieren** aus), und wählen Sie das **Symbol Animationen** oder ein anderes Animationssymbol aus, und wählen Sie **Einfügen aus.** Der Editor erstellt automatisch einen neuen Namen für die Animation, obwohl Sie den Namen ändern können.

### <a name="branching"></a>Verzweigung

Wenn Sie einen Frame erstellen, können Sie auch definieren, welcher Frame als Nächstes abspielt. Standardmäßig ist der nächste Frame, der in der Animationssequenz abgespielt wird, immer der nächste Frame in der Z-Reihenfolge. Wenn Sie jedoch die Seite **Verzweigung** auswählen, können Sie die Wahrscheinlichkeit für bis zu drei weitere Frames festlegen, die der Server spielen kann. Geben Sie den Wahrscheinlichkeitsprozentsatz und die Zielrahmennummer in die entsprechenden Felder ein. Sie können Verzweigungen auch für Frames angeben, die keine Bilder enthalten und deren Dauer auf 0 (null) festgelegt ist. Dadurch können Sie verzweigen, ohne zuerst ein bestimmtes Bild anzuzeigen.

![Screenshot: Seite "Verzweigung"](images/f6charbranch.gif)

Sie können die Verzweigungsfunktion verwenden, um Animationen zu erstellen, die unbegrenzt schleifen. Beachten Sie jedoch, dass beim Wiedergeben einer Schleifenanimation andere Animationen in der Warteschlange des Zeichens erst wiedergegeben werden, wenn ein Ereignis – z. B. ein Benutzer, der die Push-to-Talk-Taste drückt oder die Clientanwendung, die die [**Stop-Methode**](stop-method.md) aufruft – die Schleifenanimation hält. Berücksichtigen Sie daher sorgfältig den Kontext, in dem die Animation verwendet wird, bevor Sie eine Schleifenanimation erstellen.

Auf der Verzweigungsseite können Sie auch Exit Branching erstellen. Eine Exitverzweigung ist eine Verzweigung zu einem Frame, den die Animation annimmt, wenn die Animation beendet wird und bevor die nächste Animation wiedergegeben wird. Durch das Definieren von Exitbranches können Sie sich während des Übergangs von einer Animation zu einer anderen problemlos bewegen. Die Exitverzweigung darf keine kreisförmige Schleife erstellen, sondern muss schließlich in der Lage sein, den letzten Frame der Animation zu beenden.

Sie müssen keinen Exitverzweigung für jeden Frame angeben. Wenn sie dies nicht tun, folgt die Animation jedoch der normalen Verzweigung des Frames. Wenn der Frame über keinen expliziten Branch verfügt, verzweigt die Animation automatisch zu dem Frame, der darauf folgt. Wenn Sie z. B. von Frame 3 zu Frame 1 verzweigen und Frame 1 keine andere Verzweigung (normal oder Exitverzweigung) hat, verzweigt sich Frame 1 zu Frame 2. Wenn Frame 2 keine Verzweigung hat, verzweigt sich die Animation wieder auf Frame 3, und Sie verfügen über eine kreisförmige Schleife. Stattdessen können Sie von Frame 3 auf Frame 1 verzweigen und dann den Exitzweig von Frame 1 auf einen beliebigen Frame festlegen, der sich nach Frame 3 befindet und normalerweise mit dem letzten Frame der Animation fortfährt.

Manchmal müssen Sie möglicherweise einen expliziten endgültigen Frame einer Animation erstellen, die nicht sichtbar wiedergegeben wird, sondern ein Ende der Animation bereitstellt. Beispielsweise müssen Sie die Animation beenden, aber das Beenden des letzten Frames wäre nicht geeignet. Hierzu können Sie einen leeren Frame mit einer Dauer von 0 (null) als letzten Frame der Animation erstellen. Dadurch kann die Animation normal durch den letzten Frame der Animation wiedergegeben werden, und Sie können auch einen endgültigen Exitpunkt für Ihre Exitverzweigung bereitstellen.

### <a name="previewing-an-animation"></a>Vorschau einer Animation

Sie können eine Vorschau Ihrer Animation im Agent-Zeichen-Editor anzeigen, indem Sie im Menü **Bearbeiten** den Befehl **Vorschau** oder auf der Symbolleiste auf die Schaltfläche Vorschau klicken. Dadurch wird Ihre Animation ab dem aktuellen ausgewählten Frame abgespielt, einschließlich aller Verzweigungen und Soundeffekte. Er wird auf den aktuell ausgewählten Frame zurückgesetzt, wenn die Animation abgeschlossen ist. Um die gesamte Animation wiederzuspielen, wechseln Sie zur Strukturansicht, wählen Sie das Symbol der Animation oder den ersten Frame der Animation aus, und wählen Sie den Befehl **Vorschau** aus. Der Editor animiert Ihre Frames auf der Seite **Allgemein.** Um die Vorschau vor dem Ende zu beenden, wählen Sie den Befehl **Vorschau beenden** aus. Der **Befehl Vorschau** ändert sich automatisch in Vorschau **beenden,** während die Vorschauversion abgespielt wird.

Sie können auch eine Vorschau der Exitverzweigung anzeigen, indem Sie im Menü **Bearbeiten** oder auf der Symbolleiste den Befehl **Vorschau Exit Branching** auswählen. Mit können Sie testen, wie die Exitverzweigung von einem bestimmten Frame aus angezeigt wird.

### <a name="assigning-speaking-overlays"></a>Zuweisen von Sprechüberlagerungen

Sie können ein Zeichen so definieren, dass es während des letzten Frames seiner Animation spricht. Wählen Sie in diesem Frame die Seite **Überlagerung** aus. Auf dieser Seite können Sie Bilddateien laden und den vom Microsoft-Agent unterstützten Standardpositionen zuweisen. Klicken Sie auf die Schaltfläche **Bild hinzufügen,** und wählen Sie das Bild im Dialogfeld aus. Sie können auch mehrere Bilder auswählen, und der Editor lädt und weist die Bilder zu, beginnend mit der ausgewählten Position des Munds. Klicken Sie auf die Schaltflächen **Nach oben** und **Nach unten,** oder ziehen Sie einen Eintrag, um eine Bildzuweisung in der Liste zu ändern. Klicken Sie auf die Schaltfläche **Löschen,** um ein Bild zu entfernen. Sie können den Pfadnamen einer zugewiesenen Datei auch bearbeiten, indem Sie auf den Eintrag in der Liste klicken und den Dateinamen neu eingeben, oder indem Sie auf die Schaltfläche **Mit den Auslassungszeichen** klicken, um das Dialogfeld **Bilddateien auswählen** anzuzeigen.

![Screenshot: Seite "Overlays" mit ausgewählter Datei](images/f7charover.gif)

Ihre Verdeckungsüberlagerungen müssen in den Umriss des Basisrahmens passen, über dem sie angezeigt werden. Wenn dies nicht dere ist, werden sie auf den Basisrahmen abgeschnitten.

Wenn Sie möchten, dass das Zeichen mit seinem Rauschen außerhalb des Basisrahmens spricht, z. B. wenn das Zeichen seitwärts sprechen soll, erstellen Sie zuerst den Basisrahmen mit dem Kopf des Zeichens (oder dem Bereich, der sich bewegt, während das Zeichen spricht), als oberes Bild. Definieren Sie dann Ihre Überlagerungen für den Boden, um dieses Bild zu ersetzen, und legen Sie die Option **BaseFrame Top Image ersetzen** fest. Sie können auch die Schaltfläche **Alle festlegen** verwenden, um diese Option für alle Ihre Überlagerungen im Rahmen festzulegen.

### <a name="assigning-a-return-animation"></a>Zuweisen einer Rückgabeanimation

Um einen reibungslosen Übergang von einer Animation zur nächsten zu erstellen, entwerfen Sie Ihre Animationssequenzen so, dass sie mit einem neutralen Bild beginnen und enden. Weitere Informationen finden Sie unter [**Entwerfen von Zeichen für den Microsoft-Agent.**](designing-characters-for-microsoft-agent.md) Dies bedeutet jedoch nicht, dass jede Animation an der neutralen Position enden muss. Sie können ein Zeichen durch eine Sequenz von Frames animieren, während des letzten Frames sprechen lassen und eine separate, ergänzende Animation erstellen, die das Zeichen an die neutrale Position zurückgibt. Diese ergänzende Animation wird als Return-Animation bezeichnet.

Sie können eine Return-Animation definieren, indem Sie zu diesem Zweck eine explizite Animation erstellen. Sie können auch eine Return-Animation mithilfe der Exitverzweigung erstellen, die Sie in der Animation definieren. Um eine Return-Animation zuzuweisen, wählen Sie die Animation in der Struktur aus, und wählen Sie entweder die erstellte Return-Animation oder Use Exit Branching (Exitverzweigung verwenden) aus der Dropdownliste Return Animation (Rückgabeanimation) auf der Seite Eigenschaften aus.

Das Erstellen und Zuweisen einer Return-Animation hat einen zusätzlichen Vorteil: Wenn der Server eine Anforderung zum Wiedergeben einer anderen Animation erhält, versucht er, die Return-Animation für die zuletzt wiedergegebene Animation wiederzuspielen, wenn eine Return-Animation zugewiesen ist. Dadurch wird ein reibungsloser Übergang sichergestellt. Wenn eine Animation an der neutralen Position beginnt und endet, müssen Sie keine Return-Animation definieren. Wenn Sie Übergänge von einer Animation in eine andere selbst verarbeiten möchten, müssen Sie möglicherweise keine Return-Animation zuweisen.

### <a name="assigning-animations-to-states"></a>Zuweisen von Animationen zu Zuständen

Die Microsoft-Agent-Animationsdienste spielen Animationen automatisch wieder, wenn die Hostclientanwendung bestimmte Methoden verwendet. Wenn eine Anwendung beispielsweise die [**MoveTo-**](moveto-method.md) und [**GestureAt-Methoden aufruft,**](gestureat-method.md) bestimmt der Server automatisch, wo das Zeichen angezeigt wird, und gibt eine entsprechende Animation wieder. Auf ähnliche Weise gibt der Microsoft-Agent automatisch Leerlaufanimationen wieder, wenn der Benutzer mehrere Sekunden lang nicht mit dem Zeichen interagiert hat. Diese Bedingungen, wenn der Server automatisch Animationen im Auftrag einer Anwendung abspielt, werden als *Zustände* bezeichnet. Damit der Server jedoch weiß, welche Animation wiedergegeben werden soll, müssen Sie diesen Zuständen Animationen zuweisen.

Um einem Zustand eine Animation oder Animationen zuzuweisen, erstellen Sie die entsprechende Animation, erweitern Sie den Eintrag Status in der Strukturansicht des Editor-Fensters, und wählen Sie das Symbol Status aus. Die Liste der animationen, die Sie erstellt haben, wird in einem Listenfeld auf der rechten Seite des Fensters angezeigt. Überprüfen Sie die Animation, die Sie diesem Zustand zuweisen möchten. Beachten Sie, dass Sie mehrere Animationen demselben Zustand zuweisen können. Dadurch kann der Server nach dem Zufallsprinzip verschiedene Animationen für den Zustand auswählen. Das Zuweisen einer Animation zu einem Zustand verhindert nicht, dass eine Animation diese Animation direkt wiedergibt.

Sie können einem Zustand auch eine Animation zuweisen, indem Sie den Eintrag der Animation in der Struktur auswählen. Im Listenfeld **Status zuweisen** auf der Seite **Eigenschaften** werden die Zustände aufgelistet. Aktivieren Sie das Kontrollkästchen des Zustands, dem Sie die Animation zuweisen.

Der Editor unterstützt das Erstellen zusätzlicher Zustände nicht, da Zustände nur für Situationen gelten, in denen der Server automatisch eine Animation im Auftrag der Clientanwendung wiedergeben muss. Daher ist es nicht vorteilhaft, einen eigenen Zustand zu definieren. Bei Bedarf können Sie jede Animation explizit mithilfe der [**Play-Methode**](play-method.md) wiedergeben.

### <a name="saving-your-character-definition"></a>Speichern der Zeichendefinition

Sie können die Definitionsdatei Ihres Zeichens speichern, indem Sie den Befehl **Speichern** im Menü **Datei** oder die Schaltfläche **Zeichendefinition speichern** auf der Symbolleiste auswählen. Wenn Sie die Zeichendefinitionsdatei mit einem neuen Namen speichern möchten, wählen Sie im Menü **Datei** den Befehl **Speichern unter** aus. Der Editor speichert die bearbeitbare Definition eines Zeichens als Agent-Zeichendefinition (. ACD)-Datei. Sie können dieses selbstdokumentierende Textdateiformat auch mit den meisten Text-Editoren und Textverarbeitungsanwendungen bearbeiten.

### <a name="printing-your-character-definition"></a>Drucken der Zeichendefinition

Wählen Sie zum Drucken der Zeichendefinition den Befehl **Drucken** im Menü **Datei** oder die Schaltfläche **Drucken** auf der Symbolleiste aus. Um die Eigenschaften für die gedruckte Ausgabe festzulegen, wählen Sie den Befehl **Seiteneinrichtung** aus, und wählen Sie Ihre Einstellungen aus, bevor Sie den Befehl **Drucken** auswählen.

### <a name="building-a-character"></a>Erstellen eines Zeichens

Wenn Sie die Animationen erstellt haben, müssen das Zeichen und die Bilder in ein spezielles Format kompiliert werden, das vom Microsoft-Agent zum Laden dieser Daten verwendet wird. Wählen Sie zum Erstellen eines Zeichens im Menü **Datei** oder auf der Symbolleiste den Befehl Zeichen erstellen aus. Wenn Sie in der Zeichendefinitionsdatei nicht gespeicherte Bearbeitungen vorgenommen haben, speichert der Editor die Definitionsdatei, bevor das Dialogfeld **Zeichen erstellen** angezeigt wird.

![Screenshot: Fenster "Buildzeichen" mit ausgewählter Datei](images/f8charbldg.gif)

Der Agent-Zeichen-Editor schlägt automatisch einen Dateinamen basierend auf Ihrem Dateinamen für die Zeichendefinition vor. Das Dialogfeld Zeichen erstellen enthält auch eine Dropdownliste, sodass Sie zwischen dem Erstellen des Zeichens als einzelne Speicherdatei () wählen können. ACS) oder als mehrere Dateien. Wenn Sie letzteres auswählen, erstellt der Editor eine . ACF-Datei, die die Daten des Zeichens und eine enthält. ACA-Datei für jede Animation, die Sie erstellt haben. Wenn Sie planen, ein Zeichen zu installieren und darauf zuzugreifen, das auf demselben Computer wie Ihre Clientanwendung gespeichert ist, wählen Sie in der Regel das einzelne strukturierte Dateiformat aus. Dieses Format ermöglicht eine einfache und effiziente Installation und den Zugriff auf das Zeichen. Wenn jedoch über einen Webserver mithilfe des HTTP-Protokolls auf das Zeichen zugegriffen wird, erstellen Sie ihr Zeichen mithilfe von . ACF-Dateiformat (einzeln) Diese letztere Dateistruktur ermöglicht es einem Webseitenskript, einzelne Animationsdateien zu laden und die Daten im Browserdateicache des Benutzers zu speichern. Sie bietet einen effizienteren Zugriff über das Web, da Animationsdaten nach Bedarf heruntergeladen werden können, anstatt dass der Benutzer warten muss, bis der gesamte Satz von Animationen gleichzeitig heruntergeladen wird. Da die Daten des Zeichens im Browsercache gespeichert werden, kann der Dateispeicherplatz automatisch wieder freigeschaltet werden.

Sie können zwar auch Zeichendaten (entweder als einzelne strukturierte Datei oder mehrere Dateien) von einem Webserver herunterladen und an anderer Stelle auf dem Computer eines Benutzers installieren, aber für eine solche Methode sind Sicherheitsvorkehrungen für das Herunterladen und Installieren erforderlich. Daher bietet die Microsoft-Agent-API keine Unterstützung für die herunterladbare Installation eines Zeichens mit Ausnahme des Caches des Browsers. Sie können dieses Szenario jedoch weiterhin unterstützen, indem Sie Eine eigene Installationssteuerung erstellen und diese gemäß den entsprechenden Sicherheitskonventionen verteilen. Weitere Informationen finden Sie im Microsoft Internet Client Software Development Kit.

Mit der Option Komprimieren können Sie festlegen, ob die Zeichendaten komprimiert werden. In der Regel möchten Sie diese Option festlegen, um Ihre Zeichendaten zu komprimieren, obwohl das Erstellen eines Zeichens mit den komprimierten Daten länger dauert.

Nachdem Sie ein Zeichen erstellt haben, sind nachfolgende Builds schneller, wenn Sie das Zeichen am gleichen Verzeichnisspeicherort erstellen. Der Zeichen-Editor überprüft und kopiert automatisch die Dateien, die nicht geändert wurden, und kompiliert alle bearbeiteten Daten neu.

Wenn der Editor beim Erstellen des Zeichens Fehler in der Zeichendatei erkennt, schreibt er die Informationen in eine Protokolldatei und zeigt ein Meldungsfeld an. Sie können die Protokolldatei anzeigen oder ignorieren und später mit einem Text-Editor lesen. Beachten Sie jedoch, dass der Editor die Protokolldatei beim nächsten Erstellen einer Zeichendatei überschreibt.

### <a name="editing-an-existing-character"></a>Bearbeiten eines vorhandenen Zeichens

Um ein vorhandenes Zeichen zu bearbeiten, klicken Sie im Menü **Datei** auf **Öffnen,** und wählen Sie die Definitionsdatei des Zeichens (. ACD) im daraufhin angezeigten Dialogfeld, und wählen Sie Öffnen aus. Die Datei wird in den Editor geladen. Beachten Sie, dass Sie keine kompilierten Zeichendateien laden können (. Acs. ACF oder . ACA) mit dem Editor.

Da die Definitionsdatei des Zeichens (. ACD) ist eine Textdatei. Sie können auch die Definition eines Zeichens bearbeiten, indem Sie die Datei mit einem Text-Editor oder Einem Textverarbeitungsprogramm öffnen. Wenn Sie die Änderungen abschließen, müssen Sie die Datei jedoch im ursprünglichen Format speichern, bevor Sie sie zur Kompilierung in den Zeichen-Editor laden.

 

 




