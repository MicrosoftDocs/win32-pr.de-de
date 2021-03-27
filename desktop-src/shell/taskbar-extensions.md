---
description: Erläutert die neuen Funktionen der Taskleiste, einschließlich der Konsolidierung des Starts und Wechsels, erweiterter Funktionen von Task leisten Schaltflächen, z. b. ein-Klick-Zugriff auf Dokumente und anwendungsspezifische Aufgaben, Transport Steuerelemente und Status Benachrichtigungen, Miniaturansichten und switchziele basierend auf einzelnen Registerkarten in einer Anwendung im Registerkarten Format und die Möglichkeit, Task leisten Schaltflächen über einen Drag & Drop
ms.assetid: cbf2b07d-d67c-4755-888c-d40692d13cae
title: Task leisten Erweiterungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4df308d8045301b98937eb03af595d2e800921b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867743"
---
# <a name="taskbar-extensions"></a>Task leisten Erweiterungen

Ab Windows 7 wurde die Taskleiste deutlich unter dem Leitprinzip erweitert, dass Benutzer in der Hand haben, dass Sie so schnell und effizient wie möglich sind. Zu diesem Zweck werden die Anwendungsfenster,-Dateien und-Befehle, die der Benutzer ausführen muss, nun in einer einzigen Task leisten Schaltfläche zentralisiert, die zuvor verstreute Informationsquellen und-Steuerelemente konsolidiert. Ein Benutzer kann nun allgemeine Aufgaben, aktuelle und häufige Dateien, Warnungen, Status Benachrichtigungen und Miniaturansichten für einzelne Dokumente oder Registerkarten an einem Ort finden.

-   [Einheitliches starten und wechseln](#unified-launching-and-switching)
-   [Sprung Listen](#jump-lists)
-   [Destinations](#destinations)
-   [Aufgaben](#tasks)
-   [Anpassen von Sprung Listen](#customizing-jump-lists)
-   [Miniatur Ansichts Symbolleisten](#thumbnail-toolbars)
-   [Symbol Überlagerungen](#icon-overlays)
-   [Status anzeigen](#progress-bars)
-   [Deskbands](#deskbands)
-   [Infobereich](#notification-area)
-   [Miniaturansicht](#thumbnails)
-   [Zugehörige Themen](#related-topics)

## <a name="unified-launching-and-switching"></a>Einheitliches starten und wechseln

Ab der Windows 7-Taskleiste ist der Schnellstart nicht mehr eine separate Symbolleiste. Die Start Programm Verknüpfungen, die in der Regel in der Schnellstartleiste enthalten sind, werden nun an die Taskleiste selbst angeheftet, mit Schaltflächen für aktuell laufende Anwendungen Wenn ein Benutzer eine Anwendung über eine angeheftete Start Programm Verknüpfung startet, wird das Symbol so lange in die Task leisten Schaltfläche der Anwendung transformiert, wie die Anwendung ausgeführt wird. Wenn der Benutzer die Anwendung schließt, wird die Schaltfläche auf das Symbol zurückgesetzt. Die Start Programm Verknüpfung und die Schaltfläche für die laufende Anwendung sind jedoch nur verschiedene Formen der Windows 7-Task leisten Schaltfläche.

![Windows 7-Taskleiste](images/taskbar/taskbar.png)

Ein kleiner Satz von Anwendungen ist standardmäßig für Neuinstallationen fixiert. Abgesehen davon können nur Benutzer weitere Anwendungen anheften. Programm gesteuertes fixieren durch eine Anwendung ist nicht zulässig.

Die Funktion Desktop anzeigen von Schnellstart befindet sich nun auf der rechten Seite der Taskleiste. Wenn Sie mit dem Mauszeiger auf diesen Bereich zeigen, werden alle aktiven Fenster transparent, und der Desktop wird angezeigt. Wenn Sie auf den Bereich klicken, wird die vertraute Aktion zum Minimieren aller Fenster und zum Wechseln zum Desktop ausgeführt.

Während die Anwendung ausgeführt wird, wird die Task leisten Schaltfläche zur zentralen Stelle für den Zugriff auf alle folgenden Features, die jeweils ausführlich erläutert werden.

-   [Tasks](#tasks): häufige Anwendungs Befehle, die auch dann vorhanden sind, wenn die Anwendung nicht ausgeführt wird.
-   [Ziele](#destinations): vor kurzem und häufig verwendete Dateien, die für die Anwendung spezifisch sind.
-   [Miniaturansichten](#thumbnails): Fensterwechsel, einschließlich switchziele für einzelne Registerkarten und Dokumente.
-   [Miniatur Ansichts Symbolleisten](#thumbnail-toolbars): grundlegende Anwendungssteuerung aus der Miniaturansicht selbst.
-   [](#progress-bars) Status anzeigen und [Symbol Überlagerungen](#icon-overlays): Status Benachrichtigungen.

Die Task leisten Schaltfläche kann ein Start Programm, ein einzelnes Anwendungsfenster oder eine Gruppe darstellen. Jeder Gruppe wird eine ID zugewiesen, die als Anwendungs Benutzer Modell-ID (appusermodelid) bezeichnet wird. Es kann eine appusermodelid angegeben werden, um die standardmäßige Task leisten Gruppierung zu überschreiben, die es Windows ermöglicht, Elemente derselben Gruppe zu werden, wenn Sie andernfalls nicht als solche angesehen werden. Jedem Mitglied einer Gruppe wird eine separate Vorschau im Miniatur Ansichts-Flyout zugewiesen, das angezeigt wird, wenn die Maus über die Task leisten Schaltfläche der Gruppe bewegt wird. Beachten Sie, dass die Gruppierung selbst optional ist.

Ab Windows 7 können die Task leisten Schaltflächen nun durch Drag & amp; Drop-Vorgänge vom Benutzer neu angeordnet werden.

> [!Note]  
> Der Ordner "Schnellstart" ([* * * * folderid \_ Quick Launch * *](knownfolderid.md)* *) steht noch aus Gründen der Abwärtskompatibilität zur Verfügung, obwohl es keine Schnellstart-Benutzeroberfläche mehr gibt. Neue Anwendungen sollten jedoch beim Schnellstart während der Installation nicht aufgefordert werden, ein Symbol hinzuzufügen.

 

Weitere Informationen finden Sie unter [App-Benutzer Modell-IDs (appusermudelids)](appids.md).

## <a name="jump-lists"></a>Sprung Listen

Ein Benutzer wird in der Regel ein Programm starten, das auf ein Dokument zugreifen oder Aufgaben innerhalb des Programms ausführen soll. Der Benutzer eines Spiel Programms möchte möglicherweise ein gespeichertes Spiel aufrufen oder als bestimmtes Zeichen starten, anstatt ein Spiel von Anfang an neu starten zu müssen. Um Benutzer effizienter zum Ziel zu bringen, wird eine Liste der [Ziele](#destinations) und allgemeinen [Aufgaben](#tasks) , die einer Anwendung zugeordnet sind, an die Task leisten Schaltfläche der Anwendung angefügt (sowie an den entsprechenden **Start** Menüeintrag). Dies ist die Sprung Liste der Anwendung. Die Sprung Liste ist verfügbar, unabhängig davon, ob sich die Task leisten Schaltfläche im Start Programmzustand befindet (die Anwendung wird nicht ausgeführt) oder ob Sie ein oder mehrere Fenster darstellt. Wenn Sie mit der rechten Maustaste auf die Task leisten Schaltfläche klicken, wird die Sprung Liste der Anwendung wie in der folgenden Abbildung dargestellt angezeigt.

![Sprung Liste mit angehefteten, häufigen und Aufgaben Kategorien](images/taskbar/jumplist.png)

Standardmäßig enthält eine Standard Sprung Liste zwei Kategorien: zuletzt verwendete Elemente und angeheftete Elemente, obwohl nur Kategorien mit Inhalt in der Benutzeroberfläche angezeigt werden. diese Kategorien werden beim ersten Start nicht angezeigt. Immer vorhanden sind ein Anwendungsstart Symbol (um weitere Instanzen der Anwendung zu starten), eine Option zum anheften oder lösen der Anwendung über die Taskleiste und einen **Close** -Befehl für alle geöffneten Fenster.

## <a name="destinations"></a>Destinations

Die **aktuellen** und **häufigen** Kategorien werden als Ziele betrachtet. Ein Ziel, in der Regel eine Datei, ein Dokument oder eine URL, kann bearbeitet, durchsucht, angezeigt usw. Stellen Sie sich ein Ziel als eine Aktion vor. In der Regel handelt es sich bei einem Ziel um ein Element im Shellnamespace, dargestellt durch ein [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) oder [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka). Diese Teile der Zielliste entsprechen der Liste der zuletzt verwendeten Dokumente im **Startmenü** (standardmäßig nicht mehr angezeigt) und der häufig verwendeten Anwendungsliste, sind aber spezifisch für eine Anwendung und daher für den Benutzer präziser und nützlicher. Die in der Zielliste verwendeten Ergebnisse werden durch Aufrufe von " [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs)" berechnet. Beachten Sie Folgendes: Wenn der Benutzer eine Datei in Windows Explorer öffnet oder das Dialogfeld "common file" verwendet, um eine Datei zu öffnen, zu speichern oder zu erstellen, wird " **shaddtor ecentdocs** " automatisch für Sie aufgerufen, was dazu führt, dass viele Anwendungen ihre aktuellen Elemente in der Liste "Ziel" ohne entsprechende Aktion anzeigen.

Das Starten eines Ziels ähnelt dem Starten eines Elements mit dem Befehl **Öffnen mit** . Die Anwendung wird gestartet, wenn dieses Ziel geladen und einsatzbereit ist. Elemente in der Zielliste können auch aus der Liste in ein Ablage Ziel (z. b. eine e-Mail-Nachricht) gezogen werden. Wenn Sie diese Elemente in einer Zielliste zentralisiert haben, werden Benutzer, die Sie viel schneller machen möchten, das Ziel.

Wenn Elemente in der **aktuellen** Kategorie einer Zielliste angezeigt werden (oder in der Kategorie " **häufig** " oder einer [benutzerdefinierten Kategorie](#customizing-jump-lists) , wie in einem späteren Abschnitt erläutert), kann ein Benutzer sicherstellen, dass das Element immer in der Liste für den schnell Zugriff ist. Dazu kann er dieses Element an die Liste anheften, wodurch das **Element der angehefteten Kategorie hinzu** gefügt wird. Wenn ein Benutzer aktiv mit einem Ziel arbeitet, möchte er ihn problemlos an die Zielliste der Anwendung anheften. Nachdem die Benutzer Arbeit abgeschlossen ist, wird das Element einfach von ihm entheftet. Dieses Benutzer Steuerelement sorgt dafür, dass die Liste uncluttert und relevant ist.

Eine Zielliste kann als anwendungsspezifische Version des **Start** Menüs angesehen werden. Eine Zielliste ist kein Kontextmenü. Für jedes Element in einer Zielliste kann mit der rechten Maustaste auf ein eigenes Kontextmenü geklickt werden.

### <a name="apis"></a>APIs

-   [**Iapplicationdestination:: removedestination**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdestinations-removedestination)
-   [**Iapplicationdestination:: removealldestinations**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdestinations-removealldestinations)
-   [**Iapplicationdocumentlists:: GetList**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdocumentlists-getlist)
-   [**"Shaddtor ecentdocs"**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs)

## <a name="tasks"></a>Aufgaben

Ein weiterer integrierter Teil einer Sprung Liste ist die **Aufgaben** Kategorie. Während ein Ziel ein Ziel ist, handelt es sich bei einer Aufgabe um eine Aktion, und in diesem Fall handelt es sich um eine anwendungsspezifische Aktion. Anders ausgedrückt: ein Ziel ist ein Substantiv, und eine Aufgabe ist ein Verb. Aufgaben sind in der Regel [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) -Elemente mit Befehlszeilen Argumenten, die bestimmte Funktionen anzeigen, die von einer Anwendung ausgelöst werden können. Auch hier ist die Idee, so viele Informationen zu einer Anwendung zu zentralisieren, wie es praktikabel ist.

Anwendungen definieren Aufgaben auf der Grundlage der Funktionen des Programms und der wichtigsten Dinge, die ein Benutzer mit Ihnen tun soll. Aufgaben sollten kontextfrei sein, da die Anwendung nicht ausgeführt werden muss, damit Sie funktioniert. Sie sollten auch die statistisch häufigsten Aktionen sein, die ein normaler Benutzer in einer Anwendung durchführt, z. b. eine e-Mail-Nachricht verfassen oder den Kalender in einem e-Mail-Programm öffnen, ein neues Dokument in einem Textverarbeitungsprogramm erstellen, eine Anwendung in einem bestimmten Modus starten oder einen seiner Unterbefehle starten. Eine Anwendung sollte das Menü nicht mit erweiterten Features gruppieren, die Standardbenutzer nicht benötigen, oder einmalige Aktionen wie z. b. die Registrierung. Verwenden Sie keine Aufgaben für Werbeelemente wie Upgrades oder Sonderangebote.

Es wird dringend empfohlen, die Aufgabenliste statisch zu sein. Er sollte unverändert bleiben, unabhängig vom Zustand oder Status der Anwendung. Obwohl es möglich ist, die Liste dynamisch zu verändern, sollten Sie Bedenken, dass dies den Benutzer verwirren kann, der nicht erwartet, dass dieser Teil der Zielliste geändert wird.

### <a name="apis"></a>APIs

-   [**ICustomDestinationList:: AddUserTasks**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-addusertasks)

## <a name="customizing-jump-lists"></a>Anpassen von Sprung Listen

Eine Anwendung kann Ihre eigenen Kategorien definieren und Sie zusätzlich zu oder anstelle der standardmäßigen **aktuellen** und **häufigen** Kategorien in einer Sprung Liste hinzufügen. Die Anwendung kann Ihre eigenen Ziele in diesen benutzerdefinierten Kategorien basierend auf der Architektur der Anwendung und der vorgesehenen Verwendung steuern. Der folgende Screenshot zeigt eine benutzerdefinierte Sprung Liste mit einer Verlaufs Kategorie.

![benutzerdefinierte Sprung Liste](images/taskbar/customjumplist.png)

Wenn eine Anwendung entscheidet, eine benutzerdefinierte Kategorie bereitzustellen, übernimmt diese Anwendung die Verantwortung für das Auffüllen. Der Kategorieinhalt sollte weiterhin Benutzer spezifisch sein und auf der Grundlage des Benutzer Verlaufs, der Aktionen oder beider Elemente basieren, aber über eine benutzerdefinierte Kategorie kann eine Anwendung bestimmen, was Sie nachverfolgen möchten, und was Sie ignorieren will, möglicherweise basierend auf einer Anwendungs Option. Ein Audioprogramm kann z. b. entscheiden, nur zuletzt wiedergegebene Alben einzuschließen und vor kurzem wiedergegebene individuelle Spuren zu ignorieren.

Wenn ein Benutzer ein Element aus der Liste entfernt hat, das immer eine Benutzer Option ist, muss dies von der Anwendung berücksichtigt werden. Die Anwendung muss außerdem sicherstellen, dass die Elemente in der Liste gültig sind oder dass Sie ordnungsgemäß fehlschlagen, wenn Sie gelöscht wurden. Einzelne Elemente oder der gesamte Inhalt der Liste können Programm gesteuert entfernt werden.

Die maximale Anzahl von Elementen in einer Zielliste wird vom System basierend auf verschiedenen Faktoren festgelegt, wie z. b. der Anzeige Auflösung und der Schriftgröße. Wenn nicht genügend Speicherplatz für alle Elemente in allen Kategorien vorhanden ist, werden Sie von unten nach oben abgeschnitten.

### <a name="apis"></a>APIs

-   [**ICustomDestinationList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icustomdestinationlist)
-   [**Iapplicationdestination**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdestinations)
-   [**Iapplicationdocumentlists**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdocumentlists)

## <a name="thumbnail-toolbars"></a>Miniatur Ansichts Symbolleisten

Um den Zugriff auf die Schlüsselbefehle eines bestimmten Fensters zu ermöglichen, ohne dass der Benutzer das Fenster der Anwendung wiederherstellen oder aktivieren muss, kann ein aktives Symbolleisten-Steuerelement in die Miniaturansicht des Fensters eingebettet werden. Beispielsweise bietet Windows Media Player möglicherweise Standard Steuerelemente für Medien Transporte wie z. b. Wiedergabe, anhalten, stumm schalten und anhalten. Die Benutzeroberfläche zeigt diese Symbolleiste direkt unterhalb der Miniaturansicht an, wie in der folgenden Abbildung dargestellt – Sie deckt keinen Teil davon ab.

![Vorschau der Taskleiste für Windows Media Player mit drei Schaltflächen: zurück, Wiedergabe und vorwärts](images/taskbar/thumbbar.png)

Diese Symbolleiste ist einfach das vertraute Standard Steuerelement der Standard Symbolleiste. Es sind maximal sieben Schaltflächen zulässig. Die ID, das Bild, die QuickInfo und der Zustand jeder Schaltfläche werden in einer Struktur definiert, die dann an die Taskleiste weitergeleitet wird. Die Anwendung kann Schaltflächen in der Miniaturansicht-Symbolleiste nach Bedarf anzeigen, aktivieren, deaktivieren oder ausblenden.

Da es nur begrenzten Raum gibt, Miniaturansichten anzuzeigen und eine Variable Anzahl von Miniaturansichten anzuzeigen, wird eine bestimmte Symbolleisten Größe nicht garantiert. Wenn Speicherplatz eingeschränkt ist, werden die Schaltflächen in der Symbolleiste von rechts nach links abgeschnitten. Wenn Sie die Symbolleiste entwerfen, sollten Sie daher die den Schaltflächen zugeordneten Befehle priorisieren und sicherstellen, dass die wichtigste zuerst und wahrscheinlich aufgrund von Speicherproblemen gelöscht wird.

> [!Note]  
> Wenn eine Anwendung ein Fenster anzeigt, wird die zugehörige Task leisten Schaltfläche vom System erstellt. Wenn die Schaltfläche vorhanden ist, sendet die Taskleiste eine **TaskbarButtonCreated** -Meldung an das Fenster. Der Wert wird durch Aufrufen von [**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea)(L ("TaskbarButtonCreated")) berechnet. Diese Nachricht muss von Ihrer Anwendung empfangen werden, bevor Sie eine [**ITaskbarList3**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist3) -Methode aufruft.

 

### <a name="api"></a>API

-   [**ITaskbarList3:: ThumbBarAddButtons**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbaraddbuttons)
-   [**ITaskbarList3:: thumbbarsetimagelist**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbarsetimagelist)
-   [**ITaskbarList3:: ThumbBarUpdateButtons**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbarupdatebuttons)
-   [**ThumbButton**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-thumbbutton)

## <a name="icon-overlays"></a>Symbol Überlagerungen

Eine Anwendung kann dem Benutzer über die Task leisten Schaltfläche bestimmte Benachrichtigungen und Statusinformationen über die Anzeige kleiner Überlagerungen auf der Schaltfläche mitteilen. Diese Überlagerungen ähneln dem Typ der vorhandenen Überlagerung, die für Verknüpfungen oder Sicherheits Benachrichtigungen verwendet wird, die in der rechten unteren Ecke der Schaltfläche angezeigt werden. Um ein Überlagerungs Symbol anzuzeigen, muss sich die Taskleiste im Standardmodus für große Symbole befinden, wie im folgenden Screenshot gezeigt.

![Windows Messenger-Task leisten Schaltfläche mit einem Overlay zur Angabe eines verfügbaren Status](images/taskbar/taskbaroverlay.png)

Symbol Überlagerungen dienen als kontextabhängige Benachrichtigung über den Status und dienen dazu, die Notwendigkeit eines separaten Benachrichtigungs Bereichs Status-Symbols zu negieren, damit diese Informationen dem Benutzer mitgeteilt werden. Beispielsweise kann der neue e-Mail-Status in Microsoft Outlook, der derzeit im Benachrichtigungsbereich angezeigt wird, jetzt über eine Überlagerung auf der Task leisten Schaltfläche angezeigt werden. Auch hier müssen Sie sich während des Entwicklungs Zeitraums entscheiden, welche Methode für Ihre Anwendung am besten geeignet ist. Überlagerungs Symbole dienen zur Bereitstellung wichtiger, lang anstehender Status oder Benachrichtigungen, wie z. b. Netzwerkstatus, Messenger-Status oder neue e-Mail. Der Benutzer sollte nicht mit ständig veränderlichen Überlagerungen oder Animationen angezeigt werden.

Da eine einzelne Überlagerung auf der Task leisten Schaltfläche und nicht auf den einzelnen Fenster Miniaturansichten überlagert wird, ist dies eine Funktion pro Gruppe anstelle von pro Fenster. Anforderungen für Überlagerungs Symbole können von einzelnen Fenstern in einer Task leisten Gruppe empfangen werden, Sie werden jedoch nicht in die Warteschlange eingereiht. Das letzte empfangene Overlay ist das angezeigte Overlay.

### <a name="apis"></a>APIs

-   [**ITaskbarList3:: sein verlayicon**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setoverlayicon)

## <a name="progress-bars"></a>Status anzeigen

Eine Task leisten Schaltfläche kann verwendet werden, um eine Statusanzeige anzuzeigen. Dadurch kann ein Fenster Statusinformationen für den Benutzer bereitstellen, ohne dass dieser Benutzer zum Fenster selbst wechseln muss. Der Benutzer kann in einer anderen Anwendung produktiv bleiben und auf einen Blick den Fortschritt von einem oder mehreren Vorgängen in anderen Fenstern sehen. Es ist beabsichtigt, dass eine Statusleiste in einer Task leisten Schaltfläche eine ausführlichere Statusanzeige im Fenster selbst widerspiegelt. Diese Funktion kann verwendet werden, um Datei Kopien, Downloads, Installationen, das Brennen von Medien oder einen Vorgang zu verfolgen, der einen bestimmten Zeitraum in Anspruch nimmt. Diese Funktion ist nicht für die Verwendung mit normalerweise peripheren Aktionen gedacht, wie z. b. das Laden einer Webseite oder das Drucken eines Dokuments. Diese Art von Fortschritt sollte weiterhin in der Statusleiste eines Fensters angezeigt werden.

Die Statusanzeige der Taskleiste ist eine ähnliche Darstellung wie das vertraute Statusanzeige-Steuerelement. Sie kann entweder den Status bestimmte basierend auf einem abgeschlossenen Prozentsatz des Vorgangs oder einen unbestimmten Status im Marquee-Stil anzeigen, um anzugeben, dass der Vorgang in Bearbeitung ist, ohne Vorhersagen der Zeit zu verbleiben. Es kann auch angezeigt werden, dass der Vorgang angehalten wurde oder einen Fehler festgestellt hat und ein Eingreifen des Benutzers erforderlich ist.

### <a name="apis"></a>APIs

-   [**ITaskbarList3:: setprogressstate**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setprogressstate)
-   [**ITaskbarList3:: setprogressvalue**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setprogressvalue)

## <a name="deskbands"></a>Deskbands

In Windows-Versionen vor Windows 7 könnte eine ähnliche Funktion wie die Funktionen der Miniaturansicht-Symbolleiste über einen Deskband erzielt werden – eine Symbolleiste, die auf der Taskleiste gehostet wird. Beispielsweise kann Windows Media Player die Taskleiste als Satz von Transport Steuerelementen und nicht als Standard Schaltfläche minimieren. In Windows 7 können deskbands weiterhin implementiert werden, und Miniatur Ansichts-Symbolleisten sollen nicht alle ersetzt werden. Nicht alle Anwendungen geben eine Miniaturansicht an, und eine andere Lösung, wie z. b. ein deskband oder eine Aufgabe in einer Zielliste, ist möglicherweise die richtige Antwort für Ihre Anwendung. im Rahmen Ihres Entwicklungs Zeitraums müssen Sie entscheiden, welche Lösung für Ihre Anwendung am besten geeignet ist. Beachten Sie jedoch, dass deskbands Windows Aero mit aktivierter Transluzenz ("Glass") und der [**IDeskBand2**](/windows/desktop/api/Shobjidl/nn-shobjidl-ideskband2) -Schnittstelle unterstützen müssen.

### <a name="apis"></a>APIs

-   [**IDeskBand2**](/windows/desktop/api/Shobjidl/nn-shobjidl-ideskband2)

## <a name="notification-area"></a>Infobereich

Der Benachrichtigungsbereich hat Änderungen vorgenommen, die dem Benutzer viel mehr Kontrolle darüber bieten, welche Symbole auf der Taskleiste angezeigt werden. Alle Benachrichtigungs Symbole sind jetzt standardmäßig ausgeblendet, und die Sichtbarkeit kann nicht Programm gesteuert gesteuert werden. Nur der Benutzer darf auswählen, welche Benachrichtigungs Symbole auf der Taskleiste angezeigt werden. Wenn eine Benachrichtigungs Sprechblase angezeigt wird, wird das Symbol temporär angezeigt, aber selbst dann kann ein Benutzer diese Option drücken. Eine Symbol Überlagerung auf einer Task leisten Schaltfläche wird daher zu einer attraktiven Wahl, wenn Sie möchten, dass Ihre Anwendung diese Informationen an Ihre Benutzer übermittelt.

## <a name="thumbnails"></a>Miniaturbilder

In Windows Vista zeigt der Mauszeiger auf die Task leisten Schaltfläche einer Anwendung eine Miniaturansicht an, die das laufende Fenster darstellt. Wenn die Taskleiste das Fenster der Anwendung reduziert hat, stellt die Miniaturansicht dies dar, indem Sie als Stapel angezeigt wird, aber nur das aktive Fenster ist in der Miniaturansicht selbst enthalten.

In Windows 7 wird jedes Mitglied einer Gruppe als separate Miniaturansicht angezeigt und ist jetzt auch ein switchziel. Eine Anwendung kann ihre untergeordneten Elemente (z. b. echte untergeordnete Fenster, einzelne Dokumente oder Registerkarten) definieren und entsprechende Miniaturansichten für jedes dieser Fenster bereitstellen, auch wenn Sie normalerweise nicht in der Taskleiste angezeigt werden. Dadurch können Benutzer direkt in die Ansicht der gewünschten Anwendung wechseln, anstatt Sie in die Anwendung zu wechseln und dann zum Ziel zu wechseln. Beispielsweise können multidocument Interface (MDI)/Tabbed-Document Interface (TDI)-Anwendungen jedes Dokument oder jede Registerkarte als separate Miniaturansicht und switchziel angezeigt werden, wenn der Mauszeiger über die Schaltfläche der Taskleiste einer Gruppe bewegt wird.

![drei Task leisten Miniaturansichten, die einzelne Registerkarten in Windows Internet Explorer darstellen](images/taskbar/taskbarthumbnails.png)

> [!Note]  
> Wie in Windows Vista muss Aero aktiv sein, um Miniaturansichten anzuzeigen.

 

### <a name="api"></a>API

-   [**ITaskbarList3:: registertab**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-registertab)
-   [**ITaskbarList3:: settabactive**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-settabactive)
-   [**ITaskbarList3:: settaborder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-settaborder)
-   [**ITaskbarList3:: unregistertab**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-unregistertab)
-   [**ITaskbarList4:: settabproperties**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist4-settabproperties)

Miniatur Ansichts Darstellungen für Windows sind normalerweise automatisch, aber in Fällen, in denen das Ergebnis nicht optimal ist, kann die Miniaturansicht explizit angegeben werden. Standardmäßig haben nur Fenster der obersten Ebene eine Miniaturansicht automatisch generiert, und die Miniaturansichten für untergeordnete Fenster werden als generische Darstellung angezeigt. Dies kann zu einer geringeren (und sogar verwirrenden) Benutzer Darstellung für den Endbenutzer führen. Eine bestimmte Ziel Ansicht des Switchs für jedes untergeordnete Fenster bietet beispielsweise eine viel bessere Benutzer Leistung.

### <a name="api"></a>API

-   [**DwmSetWindowAttribute**](/windows/win32/api/dwmapi/nf-dwmapi-dwmsetwindowattribute)
-   [**Dwmcticonfiguration**](/windows/win32/api/dwmapi/nf-dwmapi-dwmseticonicthumbnail)
-   [**Dwmabticoniclivepreviewbitmap**](/windows/win32/api/dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap)
-   [**Dwminvalidateiconfiguration**](/windows/win32/api/dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps)
-   [**WM \_ dwmsendianicminiatur**](../dwm/wm-dwmsendiconicthumbnail.md)
-   [**WM \_ dwmsendiconiclivepreviewbitmap**](../dwm/wm-dwmsendiconiclivepreviewbitmap.md)

Sie können einen bestimmten Bereich des Fensters auswählen, der als Miniaturansicht verwendet werden soll. Dies kann hilfreich sein, wenn eine Anwendung weiß, dass Ihre Dokumente oder Registerkarten ähnlich erscheinen, wenn Sie mit der Miniatur Ansichts Größe angezeigt werden. Die Anwendung kann dann auswählen, dass nur der Teil des Client Bereichs angezeigt werden soll, den der Benutzer verwenden kann, um zwischen Miniaturansichten zu unterscheiden. Wenn Sie jedoch mit dem Mauszeiger auf eine beliebige Miniaturansicht zeigen, wird eine Ansicht des vollständigen Fensters dahinter angezeigt, sodass der Benutzer auch schnell darauf klicken kann.

Wenn mehr Miniaturansichten vorhanden sind, als angezeigt werden können, wird die Vorschau auf die Legacy-Miniaturansicht oder auf ein Standard Symbol zurückgesetzt.

### <a name="api"></a>API

-   [**ITaskbarList3:: setthumbnailclip**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setthumbnailclip)

Zum Hinzufügen der PIN an die **Taskleiste** zum Kontextmenü eines Elements, das normalerweise nur für Dateitypen benötigt wird, die den Eintrag [IsShortcut](./links.md) enthalten, erfolgt die Registrierung des entsprechenden Kontextmenü Handlers. Dies gilt auch für die Option **an Startmenü anheften**. Weitere Informationen finden Sie unter [Registrieren von Shellerweiterungs Handlern](reg-shell-exts.md) .

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Die Taskleiste](taskbar.md)
</dt> <dt>

[Anwendungs Benutzer Modell-IDs (appusermudelids)](appids.md)
</dt> <dt>

[Benachrichtigungen und Benachrichtigungsbereich](notification-area.md)
</dt> </dl>

 

 
