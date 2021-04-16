---
title: Erstellen von Animationen
description: Erstellen von Animationen
ms.assetid: 6d5c3c61-b3f2-4505-aa43-b6d001c444a5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f16c460908e7c782054a3f62ece87d01e7c9a817
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "104568103"
---
# <a name="creating-animations"></a>Erstellen von Animationen

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

Um mit dem Erstellen von Animationen für Ihr Zeichen zu beginnen, wählen Sie das Symbol **Animationen** in der Struktur aus. Dadurch wird die **Eigenschaften** Seite mit den Standardeinstellungen für alle Animationen angezeigt. Auf der Seite **Eigenschaften** können Sie die Frame Größe, die Standard Frame Dauer und die Farb paletteneinstellungen ändern.

### <a name="setting-your-characters-frame-size"></a>Festlegen der Rahmengröße Ihres Zeichens

Die Höhe und Breite des Animations Frames müssen während der gesamten Zeichen Definition konstant bleiben (d. h. für alle Animationen dieses Zeichens). Obwohl Sie die Frame Größe von der Standardeinstellung (128 x 128 Pixel) ändern können, werden im Editor angezeigte Bilder so skaliert, dass Sie der Standard Anzeige Größe angepasst werden. Wenn Sie die Standard Frame Einstellung ändern, können Sie die vollständige, nicht skalierte Frame-Größe anzeigen, indem Sie im Menü **Bearbeiten** die Option **Rahmen Fenster öffnen** auswählen.

### <a name="setting-your-characters-palette"></a>Festlegen der Palette Ihres Zeichens

Standardmäßig verwendet der Editor das erste Bitmap-Bild, das Sie laden, um die Standardfarbpalette Ihres Zeichens festzulegen, die Farben, die bestimmen, wie das Zeichen angezeigt wird, und legt die Farbe in der 11<sup>.</sup> Palettenposition als Transparenz Farbe fest. Allerdings können Sie die Palette und Transparenz explizit in der **Palette Informations** Gruppe festlegen. Auf diese Weise können Sie eine Bilddatei angeben, die für die Palette verwendet werden soll. Sie können eine der Animations Bilddateien oder eine beliebige Grafikdatei angeben. Die von Ihnen angegebene Palettendatei muss eine 8-Bit-Farbdatei (256) sein. Nachdem Sie geladen wurde, verwenden Sie die Schaltfläche **Einstellung ändern** , um die Transparenz Farbe zu ändern.

Die Farbpalette Ihres Zeichens darf die Standardsystem Farben nicht neu zuordnen. Der Editor reserviert automatisch die Farbpalette des Systems, wenn Bilder angezeigt werden. Außerdem müssen alle Animations Bilder die gleiche Farbpalette und Transparenz Farbe verwenden. Das ist sehr wichtig. Wenn dies nicht der Fall ist, können Sie die Farb Neuzuordnung der Bilder beim Laden in den Editor sehen.

Sie können die Farbpalette für das Zeichen festlegen. bei Windows-Systemen, bei denen die Anzeigeeigenschaften auf eine 8-Bit-Farbpalette (256) festgelegt sind, unterliegt die Farbe des Zeichens der aktuellen Systempalette. Da die Systempalette von Anwendungen geändert werden kann, wird das Zeichen möglicherweise nicht mit den richtigen Farbeinstellungen angezeigt. Obwohl es nicht möglich ist, dies zu verhindern, können Sie den Effekt verringern, indem Sie die Anzahl der verwendeten Farben einschränken und die Palette des Zeichens basierend auf der Palette festlegen, die von der Anwendung verwendet wird, die das Zeichen steuert. Wenn Sie z. b. ein Zeichen entwickeln, das mit Webseiten verwendet werden soll, können Sie die Palette des Zeichens mithilfe der halbftone-Palette von Microsoft Internet Explorer festlegen. Um die Palette des Browsers zu erfassen, klicken Sie mit der rechten Maustaste auf ein Bild auf einer Webseite, und wählen Sie den Befehl **Bild speichern als** aus, und wählen Sie **Bitmap** in der Option **Dateityp** aus, und klicken Sie dann auf **Speichern**. Wenn Sie die Animations Bilddateien in eine bestimmte Palettendatei optimieren möchten, können Sie ein Produkt wie den Ausgleichstyp-debabelizer verwenden.

### <a name="creating-a-new-animation"></a>Erstellen einer neuen Animation

Nachdem Sie die globalen Animationseinstellungen festgelegt haben, können Sie mit dem Erstellen von Animationen beginnen. Wählen Sie zum Erstellen einer neuen Animation im Menü **Bearbeiten** oder der Schaltfläche **neue Animation** auf der Symbolleiste die Option **neue Animation** . Dadurch wird ein neues Animations Symbol in der Struktur unter dem **Animations** Symbol hinzugefügt, und dem neuen Symbol wird ein Standardname zugewiesen. Sie können die Animation umbenennen, indem Sie im Feld **Animations Name** eingeben. Beachten Sie, dass Animations Namen innerhalb einer Zeichen Definition eindeutig sein müssen. Vermeiden Sie außerdem die Verwendung von Zeichen im Namen, bei denen es sich nicht um gültige Zeichen für Dateinamen handelt.

### <a name="adding-frames"></a>Hinzufügen von Frames

Jede Animation besteht aus Frames. Um einen neuen Frame für Ihre Animation zu erstellen, wählen Sie im Menü **Bearbeiten** oder auf der Symbolleiste die Option **Neuer Frame** aus. Dadurch wird der Struktur unter dem Animations Symbol ein neues Frame Symbol hinzugefügt, und es werden drei Seiten im Registerkarten Format angezeigt. Die Seite **Allgemein** enthält Steuerelemente, mit denen Sie ein Bild für Ihren Frame laden und anpassen können. Außerdem ist ein Anzeigebereich für die Darstellung des Frames enthalten.

![Screenshot, der den Bildbereich mit dem Dateinamen, dem Pfad und der Position anzeigt.](images/f2charflame.gif)

Ein Frame kann ein oder mehrere Bilder enthalten. Um ein Bild für einen Frame zu definieren, klicken Sie auf die Schaltfläche **Bild Datei hinzufügen** direkt über dem Listenfeld **Bilder** . Das Dialogfeld **Bilddateien auswählen** wird angezeigt, in dem Sie eine Bitmap-Bilddatei auswählen können.

![Screenshot, der zeigt, wie eine Bilddatei im Datei-Explorer ausgewählt wird.](images/f3chardialbox.gif)

Wählen Sie die Datei aus, die Sie laden möchten, und wählen Sie **Öffnen** aus, und das Bild wird in der Frame-Anzeige auf der Seite **Allgemein** angezeigt. Der Editor akzeptiert Bilder, die als 1-Bit-(Mono-), 4-Bit-oder 8-Bit-Windows-Bitmap-Format oder als GIF-Format gespeichert sind.

Mit den vier Pfeil Schaltflächen unterhalb des Bilds im Feld **Position** können Sie die Darstellung des Bilds im Frame anpassen. Wenn das Bild größer als die Größe des Frames ist, wird nur der Teil des Bilds angezeigt, der im Frame angezeigt wird. Wenn Sie die Frame Größe vergrößern, wird das Bild möglicherweise so skaliert, dass es in den Anzeigebereich des Editors passt.

Sie können einen Frame auch anzeigen, indem Sie im Menü **Bearbeiten** die Option **Rahmen Fenster öffnen** auswählen. Dadurch wird der aktuelle Frame in einem separaten Fenster angezeigt, ohne dass die in den Frame geladenen Bilder hochskaliert werden. Die Anfangs Größe dieses Fensters basiert auf den Einstellungen für Höhe und Breite des Frames. Sie können die Größe der Größe verkleinern, aber nicht größer. Das Rahmen Fenster reflektiert die Änderungen, die Sie mithilfe der Steuerelemente im Editor vornehmen, und ermöglicht es Ihnen außerdem, den Frame anzuzeigen, während er die anderen Eigenschaften Seiten anzeigen kann.

![Screenshot, der den Positions Bereich anzeigt.](images/f4charposctrl.gif)

Sie können einen Frame aus mehreren Bildern verfassen. Jedes Mal, wenn Sie die Schaltfläche **Bild hinzufügen** auswählen und ein anderes Bild auswählen, wird das Bild der Liste und dem Bild Anzeigebereich hinzugefügt. Sie können auch mehrere Abbilder hinzufügen, indem Sie mehr als eine Datei auswählen. Drücken Sie UMSCHALT oder STRG, während Sie auf das Dialogfeld **Bilddateien auswählen** klicken, und wählen Sie dann **Öffnen** aus. Die Schaltflächen nach **oben** und **nach unten** über dem Listenfeld **Bilder** verschieben ein ausgewähltes Bild in der Anzeigereihenfolge (z-Reihenfolge) für den Frame. Sie können Bilder auch verschieben, indem Sie Sie in die Liste ziehen. Wenn Sie ein Bild in der Liste auswählen und auf die Schaltfläche **Löschen** klicken, wird ein Bild entfernt. Um ein Abbild zu ändern, das Sie in eine andere Bilddatei geladen haben, können Sie auf den Dateinamen klicken, um ihn direkt zu bearbeiten, oder mithilfe der Schaltfläche **...** (Auslassungs Punkte), um das Dialogfeld **Bilddateien auswählen** zu aktivieren und eine andere Datei auszuwählen.

![Screenshot mit der Schaltfläche mit den Auslassungs Punkten.](images/f5charell.gif)

Sie können das Textfeld **Dauer** verwenden, um die Dauer für den Frame festzulegen. Das heißt, wie lange der Rahmen angezeigt wird. Wenn ein Frame kein Bild und keine Dauer aufweist, wird der Rahmen beim Wiedergeben der Animation nicht angezeigt.

Sie können auch eine Soundeffekt Datei angeben, die beim Anzeigen des Frames abgespielt werden soll. Wenn Sie das Zeichen von einem Webserver laden möchten, können Sie die Datei mit den Soundeffekten komprimieren, um die Ladezeit zu minimieren. Anschließend können Sie die komprimierte Audiodatei im Agent-Zeichen-Editor angeben. Vermeiden Sie außerdem die Verwendung eines Sound Effekts mit einer Dauer, die länger als die Dauer der Animation ist, und vermeiden Sie insbesondere einen Soundeffekt, der sich auf Schleifen auswirkt, da die Microsoft-Agent-Animations Dienste erst dann ein Animations Ereignis senden, wenn der Sound abgeschlossen ist. Vermeiden Sie außerdem die Angabe eines Sound Effekts für jede Animation, die Sie den **lauschen** -oder **hörzuständen** zuweisen, da dies die Spracheingabe beeinträchtigt. Und schließlich können Sie in einer Animation mehr als einen Soundeffekt einschließen. vermeiden Sie, dass diese überlappen, da sich dies möglicherweise auf die zeitliche Steuerung der Animation auswirkt. Beachten Sie auch, dass Soundeffekte basierend auf der Hardware des Benutzers mit unterschiedlichen Tarifen wiedergegeben werden können.

Wenn Sie der Animation Frames hinzufügen möchten, wählen Sie erneut den Befehl **Neuer Frame** aus, und befolgen Sie die gleiche Prozedur. Optional können Sie auch mehrere Bilder laden und automatisch neue Frames generieren. Um dieses Feature zu verwenden, wählen Sie im Menü **Bearbeiten** die Option **neue Frames aus Bildern** . Die Frames werden in alphabetischer Reihenfolge basierend auf den Bilddateinamen erstellt. Wenn Sie alle Frames für die Animation definiert haben, können Sie den Befehl **neue Animation** erneut auswählen, um eine neue Animation zu starten.

Es gibt weitere Möglichkeiten zum Hinzufügen von Frames zu Animationen und zum Verschieben von Frames innerhalb von oder zwischen Animationen. Sie können einen anderen Frame (aus derselben oder einer anderen Animation) auswählen und dann **Ausschneiden** oder **Kopieren** auswählen. Wählen Sie dann die Animation oder einen Frame in der Animation aus, und wählen Sie **Einfügen** aus. Sie können einen Frame auch aus einer Animation in eine andere ziehen. Wenn Sie in eine Animation ziehen, verschiebt die Aktion den Frame. Wenn Sie zu einer anderen Animation ziehen, wird der Frame kopiert. Durchziehen auf einen vorangehenden Frame in derselben Animation wird der Frame vor dem Frame eingefügt, in den Sie ziehen. Wenn Sie auf einen der folgenden Frame ziehen, wird dieser nach dem Frame platziert, in den Sie ziehen. Wenn Sie mit der rechten Maustaste einen Frame ziehen, wird durch das Freigeben der Schaltfläche ein Popup Menü mit ihren Übertragungs Optionen angezeigt.

Sie können auch eine Animation erstellen, indem Sie eine vorhandene Animation kopieren (Wählen Sie die Animation und dann **Kopieren** aus), und wählen Sie das Symbol **Animationen** oder ein anderes Animations Symbol aus, und wählen Sie **Einfügen** aus. Der Editor erstellt automatisch einen neuen Namen für die Animation, auch wenn Sie den Namen ändern können.

### <a name="branching"></a>Verzweigung

Wenn Sie einen Frame erstellen, können Sie auch definieren, welcher Frame als nächstes wiedergegeben wird. Standardmäßig ist der nächste Frame, der in der Animationssequenz abgespielt wird, immer der nächste Frame in der z-Reihenfolge. Durch Auswählen der **Verzweigungs** Seite können Sie jedoch die Wahrscheinlichkeit für bis zu drei andere Frames festlegen, die der Server wiedergeben kann. Geben Sie den Wahrscheinlichkeits Prozentsatz und die Ziel Frame Nummer in die entsprechenden Felder ein. Sie können Verzweigungen auch für Frames angeben, die keine Bilder aufweisen und deren Dauer auf 0 (null) festgelegt ist. Dies ermöglicht es Ihnen, eine Verzweigung durchzusetzen, ohne zuerst ein bestimmtes Bild anzuzeigen.

![Screenshot, der die Seite "Verzweigungen" anzeigt.](images/f6charbranch.gif)

Mithilfe der Verzweigungs Funktion können Sie Animationen erstellen, die unbegrenzt Schleifen werden. Beachten Sie jedoch, dass bei der Wiedergabe einer Schleifen Animation andere Animationen in der Warteschlange des Zeichens nicht wiedergegeben werden, bis ein Ereignis – z. b. ein Benutzer, der den Push-to-Talk-Schlüssel drückt, oder die Client Anwendung, die die Methode " [**Beenden**](stop-method.md) " aufgerufen – die Schleifen Animation stoppt. Berücksichtigen Sie daher sorgfältig den Kontext, in dem die Animation verwendet wird, bevor Sie eine Schleifen Animation erstellen.

Auf der Verzweigungs Seite können Sie auch Exit-Verzweigungen erstellen. Eine Beendigungs Verzweigung ist ein Branch zu einem Frame, den die Animation beim Beenden der Animation und vor der Wiedergabe der nächsten Animation durchführt. Wenn Sie Beendigungs Verzweigungen definieren, können Sie während des Übergangs von einer Animation zu einer anderen reibungslos wechseln. Die Beendigungs Verzweigung darf keine zirkuläre Schleife erstellen, muss aber schließlich zum letzten Frame der Animation wechseln können.

Sie müssen nicht für jeden Frame eine Beendigungs Verzweigung angeben. wenn dies nicht der Fall ist, folgt die Animation der normalen Verzweigung des Frames. Wenn der Frame über keine explizite Verzweigung verfügt, verzweigt die Animation automatisch nach dem Frame, der darauf folgt. Wenn Sie z. b. von Frame 3 zu Frame 1 verzweigen und Frame 1 keine andere Verzweigung (normaler oder Beendigungs Branch) aufweist, wird Frame 1 in Frame 2 verzweigt. Wenn Frame 2 keine Verzweigung hat, verzweigt die Animation zurück an Frame 3 und eine zirkuläre Schleife. Stattdessen könnten Sie von Frame 3 zu Frame 1 verzweigen und dann die Exit-Verzweigung von Frame 1 auf einen beliebigen Frame festlegen, der nach Frame 3 liegt, und normalerweise mit dem letzten Frame der Animation fortfahren.

Manchmal müssen Sie möglicherweise einen expliziten abschließenden Frame einer Animation erstellen, der nicht sichtbar ist, aber ein Ende der Animation bereitstellt. Beispielsweise müssen Sie die Animation beenden, aber das Beenden bis zum letzten Frame wäre nicht geeignet. Dies können Sie erreichen, indem Sie einen leeren Frame mit der Länge 0 (null) als letzten Frame der Animation erstellen. Dadurch kann die Animation in der Regel über den letzten Frame der Animation wiedergegeben werden. Außerdem können Sie einen endgültigen Beendigungs Punkt für Ihre Beendigungs Verzweigung bereitstellen.

### <a name="previewing-an-animation"></a>Anzeigen einer Vorschau für eine Animation

Sie können eine Vorschau der Animation im agentzeicheneditor anzeigen, indem Sie im Menü **Bearbeiten** oder Vorschau auf der Symbolleiste den Befehl **Vorschau** auswählen. Dadurch wird die Animation wiedergegeben, einschließlich Verzweigungen und Soundeffekte, beginnend mit dem aktuell ausgewählten Frame. Wenn die Animation abgeschlossen ist, wird Sie auf den aktuell ausgewählten Frame zurückgesetzt. Um die gesamte Animation wiederzugeben, navigieren Sie zur Strukturansicht, wählen Sie das Symbol der Animation oder den ersten Frame der Animation aus, und wählen Sie dann den Befehl **Vorschau** aus. Der Editor animiert Ihre Frames auf der Seite **Allgemein** . Wenn Sie die Vorschau beenden möchten, bevor Sie endet, wählen Sie den Befehl " **Vorschau beenden** ". Der **Vorschau** Befehl ändert sich automatisch in " **Vorschau Abbrechen** ", während die Vorschau abgespielt wird.

Sie können auch eine Vorschau der Beendigungs Verzweigung anzeigen, indem Sie im Menü **Bearbeiten** oder auf der Symbolleiste den Befehl **Vorschau beenden Verzweigungen** auswählen. Mit können Sie testen, wie die Beendigungs Verzweigung von einem bestimmten Frame aus angezeigt wird.

### <a name="assigning-speaking-overlays"></a>Zuweisen von Sprech Überlagerungen

Sie können ein Zeichen definieren, sodass es während des letzten Frames der Animation gesprochen wird. Wählen Sie in diesem Frame die Seite über **Lagerung** aus. Auf dieser Seite können Sie Mund Bilddateien laden und den standardmundpositionen zuweisen, die vom Microsoft-Agent unterstützt werden. Klicken Sie auf die Schaltfläche **Bild hinzufügen** , und wählen Sie das Bild im Dialogfeld aus. Sie können auch mehrere Abbilder auswählen, und der Editor lädt die Bilder und weist Sie ab, beginnend mit der ausgewählten mundposition. Klicken Sie auf die Schaltflächen nach **oben** und nach **unten** , oder ziehen Sie einen Eintrag, um eine Bild Zuweisung in der Liste zu ändern. Klicken Sie auf die Schaltfläche **Löschen** , um ein Bild zu entfernen. Sie können den Pfadnamen einer zugewiesenen Datei auch bearbeiten, indem Sie auf den entsprechenden Eintrag in der Liste klicken **und den Datei** Namen erneut eingeben, oder indem Sie auf die Schaltfläche mit den Auslassungs Punkten klicken, um das Dialogfeld **Bilddateien auswählen** anzuzeigen.

![Screenshot, der die Seite "Überlagerungen" anzeigt, bei der eine Datei ausgewählt ist.](images/f7charover.gif)

Die Mund Überlagerungen müssen in den Umriss des Basis Rahmens passen, über den Sie angezeigt werden. Wenn dies nicht der Fall ist, werden Sie auf den Basisrahmen zugeschnitten.

Wenn das Zeichen mit seinem Mund außerhalb des Basis Rahmens gesprochen werden soll, z. b. wenn das Zeichen mit der Seitwärtsbewegung gesprochen werden soll, erstellen Sie zuerst den Basisrahmen mit dem Anfang des Zeichens (oder dem Bereich, der als Zeichen bewegt wird) als oberstes Bild. Definieren Sie dann die Mund Überlagerungen, um dieses Bild zu ersetzen, und legen Sie die Option **Basisrahmen-Top-Bild ersetzen** fest. Sie können auch die Schaltfläche **alle festlegen** verwenden, um diese Option für alle mundüberlagerungen im Frame festzulegen.

### <a name="assigning-a-return-animation"></a>Zuweisen einer Rückgabe Animation

Um einen reibungslosen Übergang von einer Animation zum nächsten zu erstellen, entwerfen Sie Ihre Animationssequenzen so, dass Sie mit einem neutralen Bild beginnen und enden. Weitere Informationen finden Sie unter [**Entwerfen von Zeichen für den Microsoft-Agent**](designing-characters-for-microsoft-agent.md). Dies bedeutet jedoch nicht, dass jede Animation an der neutralen Position enden muss. Sie können ein Zeichen in einer Sequenz von Frames animieren, es während des letzten Frames sprechen und eine separate, ergänzende Animation erstellen, die das Zeichen an die neutrale Position zurückgibt. Diese ergänzende Animation wird als Rückgabe Animation bezeichnet.

Sie können eine Rückgabe Animation definieren, indem Sie für diesen Zweck eine explizite Animation erstellen. Sie können eine Rückgabe Animation auch mit der Beendigungs Verzweigung erstellen, die Sie in der Animation definieren. Um eine Rückgabe Animation zuzuweisen, wählen Sie die Animation in der Struktur aus, und wählen Sie auf der Seite Eigenschaften entweder die Rückgabe Animation aus, die Sie erstellt haben, oder verwenden Sie die Option zum Beenden der Animation.

Das Erstellen und Zuweisen einer Rückgabe Animation hat einen zusätzlichen Vorteil: Wenn der Server eine Anforderung zum Abspielen einer anderen Animation erhält, versucht er, die Rückgabe Animation für die letzte Animation wiederzugeben, die er abgespielt hat, wenn eine Rückgabe Animation zugewiesen wird. Dies sorgt für einen reibungslosen Übergang. Wenn eine Animation an der neutralen Position beginnt und endet, müssen Sie keine Return-Animation definieren. Wenn Sie die Übergänge von einer Animation zu einem anderen selbst verarbeiten möchten, müssen Sie möglicherweise keine Return-Animation zuweisen.

### <a name="assigning-animations-to-states"></a>Zuweisen von Animationen zu Zuständen

Die Microsoft-Agent-Animations Dienste spielen automatisch Animationen wieder, wenn die Hosting-Client Anwendung bestimmte Methoden verwendet. Wenn eine Anwendung z. b. die Methoden " [**muveto**](moveto-method.md) " und " [**gestureat**](gestureat-method.md) " aufruft, bestimmt der Server automatisch, wo das Zeichen angezeigt wird, und spielt eine passende Animation. Ebenso spielt der Microsoft-Agent automatisch Leerlauf Animationen, wenn der Benutzer seit mehreren Sekunden nicht mit dem Zeichen interagiert hat. Diese Bedingungen werden, wenn der Server im Auftrag einer Anwendung automatisch Animationen wieder gibt, als *Zustände* bezeichnet. Damit der Server jedoch weiß, welche Animation abgespielt werden soll, müssen Sie diesen Zuständen Animationen zuweisen.

Um einem Zustand eine Animation oder Animationen zuzuweisen, erstellen Sie die entsprechende Animation, erweitern Sie in der Strukturansicht des Editor-Fensters den Eintrag Zustände, und wählen Sie das Symbol Status aus. Die Liste der von Ihnen erstellten Animationen wird in einem Listenfeld auf der rechten Seite des Fensters angezeigt. Überprüfen Sie die Animation, die diesem Zustand zugewiesen werden soll. Beachten Sie, dass Sie dem gleichen Zustand mehr als eine Animation zuweisen können. Dadurch kann der Server nach dem Zufallsprinzip verschiedene Animationen für den Zustand auswählen. Das Zuweisen einer Animation zu einem Zustand verhindert nicht, dass eine Animation diese Animation direkt abspielt.

Sie können eine Animation auch einem Zustand zuweisen, indem Sie den Eintrag der Animation in der Struktur auswählen. Im Listenfeld **Zuweisungs Zuweisung** auf der Seite **Eigenschaften** werden die Zustände aufgeführt. Aktivieren Sie das Kontrollkästchen für den Zustand, dem die Animation zugewiesen werden soll.

Der Editor unterstützt das Erstellen von zusätzlichen Zuständen nicht, da Zustände nur für Situationen gelten, in denen der Server eine Animation automatisch im Namen der Client Anwendung wiedergeben muss. Daher gibt es keinen Vorteil beim Definieren Ihres eigenen Zustands. Wenn erforderlich, können Sie jede Animation explizit mit der [**Play**](play-method.md) -Methode wiedergeben.

### <a name="saving-your-character-definition"></a>Speichern der Zeichen Definition

Sie können die Definitionsdatei Ihres Zeichens speichern, indem Sie im Menü **Datei** den Befehl **Speichern** oder auf der Symbolleiste die Schaltfläche **Zeichen Definition speichern** auswählen. Wenn Sie die Zeichen Definitionsdatei mit einem neuen Namen speichern möchten, wählen Sie im Menü **Datei** den Befehl **Speichern als** aus. Der Editor speichert die editierbare Definition eines Zeichens als agentzeichendefinition (. ACD). Sie können dieses selbst dokumentierende Text Dateiformat auch mit den meisten Text-Editoren und Textverarbeitungsanwendungen bearbeiten.

### <a name="printing-your-character-definition"></a>Drucken der Zeichen Definition

Um die Definition des Zeichens auszugeben, wählen Sie im Menü **Datei** den Befehl **Drucken** oder auf der Symbolleiste die Schaltfläche **Drucken** aus. Um die Eigenschaften für die gedruckte Ausgabe festzulegen, wählen Sie den Befehl **Seite einrichten** aus, und wählen Sie die Einstellungen aus, bevor Sie den Befehl **Drucken** auswählen.

### <a name="building-a-character"></a>Aufbauen eines Zeichens

Wenn Sie mit dem Erstellen Ihrer Animationen abgeschlossen haben, müssen das Zeichen und die Bilder in einem speziellen Format kompiliert werden, das der Microsoft-Agent zum Laden dieser Daten verwendet. Um ein Zeichen zu erstellen, wählen Sie im Menü **Datei** oder in der Symbolleiste den Befehl Build-Zeichen aus. Wenn Sie nicht gespeicherte Änderungen in der Zeichen Definitionsdatei vorgenommen haben, speichert der Editor die Definitionsdatei, bevor das Dialogfeld " **buildzeichen** " angezeigt wird.

![Screenshot, der das Fenster "Build Character" (Build Character) mit ausgewählter Datei anzeigt.](images/f8charbldg.gif)

Der Agent-Zeichen-Editor schlägt basierend auf dem Dateiname der Zeichen Definition automatisch einen Dateinamen vor. Das Dialogfeld buildzeichen enthält auch eine Dropdown Liste, sodass Sie zwischen dem Erstellen des Zeichens als eine einzelne Speicherdatei () wählen können. ACS) oder mehrere Dateien. Wenn Sie Letzteres auswählen, erstellt der Editor eine. ACF-Datei, die die Daten eines Zeichens und eine enthält. ACA-Datei für jede Animation, die Sie erstellt haben. Wenn Sie die Installation und den Zugriff auf ein Zeichen planen, das auf dem gleichen Computer wie die Client Anwendung gespeichert ist, wählen Sie in der Regel das einmalige strukturierte Dateiformat aus. Dieses Format bietet eine einfache und effiziente Installation und den Zugriff auf das Zeichen. Wenn jedoch von einem Webserver über das HTTP-Protokoll auf das Zeichen zugegriffen wird, erstellen Sie das Zeichen mit dem. Dateiformat der ACF (einzeln). Diese zweite Dateistruktur ermöglicht einem Webseiten Skript das Laden einzelner Animationsdateien, wobei die Daten im Browser Dateicache des Benutzers gespeichert werden. Sie ermöglicht einen effizienteren Zugriff über das Web, da Animationsdaten bei Bedarf heruntergeladen werden können, statt dass der Benutzer auf die gesamte Animation warten muss, bis der gesamte Satz von Animationen gleichzeitig heruntergeladen wird. Außerdem kann der Datei Speicherplatz automatisch freigegeben werden, da die Daten des Zeichens im Browser Cache gespeichert werden.

Obwohl Sie auch Zeichendaten (entweder als einzelne strukturierte Datei oder mehrere Dateien) von einem Webserver herunterladen und an einem anderen Ort auf dem Computer des Benutzers installieren können, sind für eine solche Methode Sicherheitsvorkehrungen für das herunterladen und die Installation erforderlich. Folglich umfasst die Microsoft-Agent-API keine Unterstützung für die herunterladbare Installation eines Zeichens außer dem Cache des Browsers. Allerdings können Sie dieses Szenario weiterhin unterstützen, indem Sie ein eigenes Installations Steuerelement erstellen und es nach den entsprechenden Sicherheits Konventionen verteilen. Weitere Informationen finden Sie im Microsoft Internet Client Software Development Kit.

Mit der Option "komprimieren" können Sie festlegen, ob die Zeichendaten komprimiert werden. In der Regel sollten Sie diese Option festlegen, um die Zeichendaten zu komprimieren, obwohl das Entwickeln eines Zeichens mit den komprimierten Daten länger dauert.

Nachdem Sie ein Zeichen erstellt haben, werden nachfolgende Builds schneller ausgeführt, wenn Sie das Zeichen an demselben Verzeichnis Speicherort erstellen. Der Zeichen-Editor überprüft und kopiert die Dateien, die nicht geändert wurden, und kompiliert alle bearbeiteten Daten erneut.

Wenn der Editor beim Aufbau des Zeichens Fehler in der Zeichen Datei erkennt, werden die Informationen in eine Protokolldatei geschrieben, und es wird ein Meldungs Feld angezeigt. Sie können auswählen, ob Sie die Protokolldatei anzeigen oder ignorieren und Sie später mit einem Text-Editor lesen möchten. Beachten Sie jedoch, dass der Editor die Protokolldatei beim nächsten Erstellen einer Zeichen Datei überschreibt.

### <a name="editing-an-existing-character"></a>Bearbeiten eines vorhandenen Zeichens

Wenn Sie ein vorhandenes Zeichen bearbeiten möchten, wählen Sie im Menü **Datei** die Option **Öffnen** aus, und wählen Sie die Definitionsdatei des Zeichens aus. ACD) im daraufhin angezeigten Dialogfeld, und wählen Sie öffnen aus. Die Datei wird in den Editor geladen. Beachten Sie, dass Sie keine kompilierten Zeichen Dateien () laden können. ACS,. ACF oder. ACA) mit dem-Editor.

Aufgrund der Definitionsdatei des Zeichens (. ACD) ist eine Textdatei. Sie können die Definition eines Zeichens auch bearbeiten, indem Sie die Datei mit einem Text-Editor oder einem Textverarbeitungsprogramm öffnen. Wenn Sie jedoch die Änderungen abgeschlossen haben, stellen Sie sicher, dass Sie die Datei im ursprünglichen Format speichern, bevor Sie Sie in den Zeichen-Editor für die Kompilierung laden.

 

 




