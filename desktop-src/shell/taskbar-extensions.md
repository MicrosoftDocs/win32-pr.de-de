---
description: Erläutert neue Taskleistenfunktionen, einschließlich der Konsolidierung des Startens und Wechselns, erweiterter Funktionen von Taskleistenschaltflächen, z. B. Zugriff mit nur einem Klick auf Dokumente und anwendungsspezifische Aufgaben, Transportsteuerelemente und Statusbenachrichtigungen, Miniaturansichtsdarstellungen und Switchziele basierend auf einzelnen Registerkarten in einer Registerkartenanwendung und die Möglichkeit, Taskleistenschaltflächen über einen Drag & Drop-Vorgang neu zu anordnen.
ms.assetid: cbf2b07d-d67c-4755-888c-d40692d13cae
title: Taskleistenerweiterungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c92cb8f100da2c7b5173319c25369a0ada7284b2ff5f4adbfe9b519c0ee96485
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773750"
---
# <a name="taskbar-extensions"></a>Taskleistenerweiterungen

Ab Windows 7 wurde die Taskleiste unter dem Leitprinzip, Benutzer so schnell und effizient wie möglich zu erreichen, erheblich erweitert. Zu diesem Zweck werden die Anwendungsfenster, Dateien und Befehle, die der Benutzer ausführen muss, jetzt in einer einzigen Taskleistenschaltfläche zentralisiert, die zuvor punktierte Informationsquellen und Steuerelemente konsolidiert. Ein Benutzer kann nun allgemeine Aufgaben, aktuelle und häufige Dateien, Warnungen, Statusbenachrichtigungen und Miniaturansichten für einzelne Dokumente oder Registerkarten an einem Ort finden.

-   [Einheitliches Starten und Wechseln](#unified-launching-and-switching)
-   [Sprunglisten](#jump-lists)
-   [Ziele](#destinations)
-   [Aufgaben](#tasks)
-   [Anpassen von Sprunglisten](#customizing-jump-lists)
-   [Miniaturansichtssymbolleisten](#thumbnail-toolbars)
-   [Symbolüberlagerungen](#icon-overlays)
-   [Statusleisten](#progress-bars)
-   [Deskbands](#deskbands)
-   [Infobereich](#notification-area)
-   [Miniaturansicht](#thumbnails)
-   [Zugehörige Themen](#related-topics)

## <a name="unified-launching-and-switching"></a>Einheitliches Starten und Wechseln

Ab der taskleiste Windows 7 ist Schnellstart keine separate Symbolleiste mehr. Die in der Regel Schnellstart startenden Tastenkombinationen werden jetzt an die Taskleiste selbst angeheftet und mit Schaltflächen für aktuell ausgeführte Anwendungen gemischt. Wenn ein Benutzer eine Anwendung über eine angeheftete Starttastenverknüpfung startet, wird das Symbol in die Taskleistenschaltfläche der Anwendung transformiert, solange die Anwendung ausgeführt wird. Wenn der Benutzer die Anwendung schließt, wird die Schaltfläche auf das Symbol zurückverwendet. Die Tastenkombination für das Startfeld und die Schaltfläche für die ausgeführte Anwendung sind jedoch nur unterschiedliche Formen der Windows 7-Taskleistenschaltfläche.

![Windows 7-Taskleiste](images/taskbar/taskbar.png)

Eine kleine Gruppe von Anwendungen wird standardmäßig für neue Installationen angeheftet. Ab diesem Punkt kann nur der Benutzer weitere Anwendungen anheften. Programmgesteuertes Anheften durch eine Anwendung ist nicht zulässig.

Das Feature Desktop anzeigen von Schnellstart befindet sich jetzt ganz rechts auf der Taskleiste. Wenn Sie auf diesen Bereich zeigen, werden alle aktiven Fenster transparent, und der Desktop wird angezeigt. Wenn Sie auf den Bereich klicken, wird die bekannte Aktion zum Minimieren aller Fenster und zum Wechseln zum Desktop ausgeführt.

Während die Anwendung ausgeführt wird, wird die Taskleistenschaltfläche zum einzigen Ort für den Zugriff auf alle der folgenden Features, die im Folgenden ausführlich erläutert werden.

-   [Aufgaben:](#tasks)Allgemeine Anwendungsbefehle, die auch dann vorhanden sind, wenn die Anwendung nicht ausgeführt wird.
-   [Ziele:](#destinations)Dateien, auf die kürzlich und häufig zugegriffen wird, die für die Anwendung spezifisch sind.
-   [Miniaturansichten:](#thumbnails)Fensterwechsel, einschließlich Switchziele für einzelne Registerkarten und Dokumente.
-   [Miniaturansichtssymbolleisten:](#thumbnail-toolbars)grundlegende Anwendungssteuerung aus der Miniaturansicht selbst.
-   [Statusleisten](#progress-bars) und [Symbolüberlagerungen:](#icon-overlays)Statusbenachrichtigungen.

Die Taskleistenschaltfläche kann ein Startfeld, ein einzelnes Anwendungsfenster oder eine Gruppe darstellen. Jeder Gruppe wird ein Bezeichner zugewiesen, der als Anwendungsbenutzermodell-ID (AppUserModelID) bezeichnet wird. Eine AppUserModelID kann angegeben werden, um die standardmäßige Taskleisten-Gruppierung zu überschreiben. Dadurch können Fenster Mitglieder derselben Gruppe werden, wenn sie andernfalls nicht als solche angezeigt werden. Jedes Mitglied einer Gruppe erhält im Miniaturansichts-Flyout eine separate Vorschau, die angezeigt wird, wenn der Mauszeiger auf die Taskleistenschaltfläche der Gruppe zeigt. Beachten Sie, dass die Gruppierung selbst optional bleibt.

Ab Windows 7 können Taskleistenschaltflächen vom Benutzer jetzt über Drag & Drop-Vorgänge neu angeordnet werden.

> [!Note]  
> Der Schnellstart Ordner (["FOLDERID \_ QuickLaunch!")](knownfolderid.md)ist aus Gründen der Abwärtskompatibilität weiterhin verfügbar, obwohl es keine Schnellstart gibt. Neue Anwendungen sollten jedoch nicht darum bitten, während der Installation ein Symbol für Schnellstart hinzuzufügen.

 

Weitere Informationen finden Sie unter [Anwendungsbenutzermodell-IDs (AppUserModelIDs).](appids.md)

## <a name="jump-lists"></a>Sprunglisten

Ein Benutzer startet in der Regel ein Programm mit der Absicht, auf ein Dokument zu zugreifen oder Aufgaben innerhalb des Programms auszuführen. Der Benutzer eines Spieleprogramms möchte möglicherweise zu einem gespeicherten Spiel oder als bestimmtes Zeichen starten, anstatt ein Spiel von Anfang an neu zu starten. Damit Benutzer ihr endgültiges Ziel effizienter [](#destinations) erreichen können, wird eine Liste von Zielen und allgemeinen Aufgaben, die einer Anwendung zugeordnet sind, an die Taskleistenschaltfläche dieser Anwendung (sowie an den entsprechenden **Startmenüeintrag)** angefügt. [](#tasks) Dies ist die Sprungliste. Der Sprungliste ist verfügbar, unabhängig davon, ob sich die Taskleistenschaltfläche im Startfeldzustand befindet (die Anwendung wird nicht ausgeführt) oder ob sie ein oder mehrere Fenster darstellt. Wenn Sie mit der rechten Maustaste auf die Taskleistenschaltfläche klicken, wird die Sprungliste der Anwendung angezeigt, wie in der folgenden Abbildung dargestellt.

![Sprungliste mit angehefteten, häufigen und Aufgabenkategorien](images/taskbar/jumplist.png)

Standardmäßig enthält ein Standard-Sprungliste zwei Kategorien: zuletzt verwendete Elemente und angeheftete Elemente. Da jedoch nur Kategorien mit Inhalt auf der Benutzeroberfläche angezeigt werden, wird keine dieser Kategorien beim ersten Start angezeigt. Immer vorhanden sind ein Anwendungsstartsymbol (zum Starten von mehr Instanzen der Anwendung), eine Option zum Anheften oder Entheften der Anwendung von der Taskleiste und ein **Close-Befehl** für alle geöffneten Fenster.

## <a name="destinations"></a>Ziele

Die **Kategorien Zuletzt** verwendet und **Häufig** werden als Ziele betrachtet. Ein Ziel, in der Regel eine Datei, ein Dokument oder eine URL, kann bearbeitet, durchsucht, angezeigt werden und so weiter. Stellen Sie sich ein Ziel eher als eine Sache als eine Aktion vor. In der Regel ist ein Ziel ein Element im Shellnamespace, das durch ein [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) oder [**IShellLink dargestellt wird.**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) Diese Teile der Zielliste sind analog  zur Liste der zuletzt verwendeten Dokumente des Startmenüs (standardmäßig nicht mehr angezeigt) und häufig verwendeter Anwendungsliste. Sie sind jedoch anwendungsspezifisch und daher genauer und nützlicher für den Benutzer. Die in der Zielliste verwendeten Ergebnisse werden durch Aufrufe von [**SHAddToRecentDocs berechnet.**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs) Beachten Sie, dass **SHAddToRecentDocs** automatisch für Sie aufgerufen wird, wenn der Benutzer eine Datei aus dem Windows-Explorer öffnet oder das dialogfeld für allgemeine Dateien verwendet, um eine Datei zu öffnen, zu speichern oder zu erstellen. Dies führt dazu, dass viele Anwendungen ihre aktuellen Elemente in der Zielliste anzeigen, ohne dass eine Aktion von ihr erfolgt.

Das Starten eines Ziels ist ähnlich wie das Starten eines Elements mit dem **Befehl Öffnen mit.** Die Anwendung wird gestartet, wenn dieses Ziel geladen und einsatzbereit ist. Elemente in der Zielliste können auch aus der Liste in ein Abbruchziel wie eine E-Mail-Nachricht gezogen werden. Indem diese Elemente in einer Zielliste zentralisiert werden, können Benutzer so viel schneller gehen, was das Ziel ist.

Wenn Elemente in der Kategorie Zuletzt verwendet  einer Zielliste [](#customizing-jump-lists) angezeigt werden (oder in der Kategorie Häufig oder in einer benutzerdefinierten Kategorie, wie in einem späteren Abschnitt erläutert), kann ein Benutzer sicherstellen, dass das Element immer in der Liste enthalten ist, um schnell darauf zugreifen zu können.  Um dies zu erreichen, kann er dieses Element an die Liste anheften, wodurch das Element der Kategorie **Angeheftet hinzugefügt** wird. Wenn ein Benutzer aktiv mit einem Ziel arbeitet, möchte er es einfach zur Hand haben und würde es daher an die Zielliste der Anwendung anheften. Nachdem der Benutzer die Arbeit dort erledigt hat, entpinnt er einfach das Element. Dieses Benutzersteuer steuerelement sorgt dafür, dass die Liste übersichtlich und relevant bleibt.

Eine Zielliste kann als anwendungsspezifische Version des **Startmenüs betrachtet** werden. Eine Zielliste ist kein Kontextmenü. Auf jedes Element in einer Zielliste kann mit der rechten Maustaste geklickt werden, um ein eigenes Kontextmenü zu erhalten.

### <a name="apis"></a>APIs

-   [**IApplicationDetolations::RemoveDestination**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdestinations-removedestination)
-   [**IApplicationDetolations::RemoveAllDetolations**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdestinations-removealldestinations)
-   [**IApplicationDocumentLists::GetList**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdocumentlists-getlist)
-   [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs)

## <a name="tasks"></a>Aufgaben

Ein weiterer integrierter Teil einer Sprungliste ist die **Kategorie Aufgaben.** Während ein Ziel eine Sache ist, ist eine Aufgabe eine Aktion, und in diesem Fall handelt es sich um eine anwendungsspezifische Aktion. Anders ausgedrückt: Ein Ziel ist ein Nomen und eine Aufgabe ein Verb. Aufgaben sind in der Regel [**IShellLink-Elemente**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) mit Befehlszeilenargumenten, die bestimmte Funktionen angeben, die von einer Anwendung ausgelöst werden können. Auch hier ist die Idee, so viele Informationen zu einer Anwendung zu zentralisieren, wie praktikabel ist.

Anwendungen definieren Aufgaben basierend auf den Funktionen des Programms und den wichtigsten Aufgaben, die ein Benutzer mit diesen aufgaben soll. Tasks sollten kontextfrei sein, da die Anwendung nicht ausgeführt werden muss, damit sie funktionieren. Sie sollten auch die statistisch häufigsten Aktionen sein, die ein normaler Benutzer in einer Anwendung ausführen würde, z. B. das Verfassen einer E-Mail oder das Öffnen des Kalenders in einem E-Mail-Programm, das Erstellen eines neuen Dokuments in einem Textprozessor, das Starten einer Anwendung in einem bestimmten Modus oder das Starten eines seiner Unterprogramme. Eine Anwendung sollte das Menü nicht mit erweiterten Features überladen, die Standardbenutzer nicht benötigen, oder einmalige Aktionen wie die Registrierung. Verwenden Sie keine Aufgaben für Werbeartikel wie Upgrades oder Sonderangebote.

Es wird dringend empfohlen, die Aufgabenliste statisch zu verwenden. Sie sollte unabhängig vom Status oder Status der Anwendung gleich bleiben. Obwohl es möglich ist, die Liste dynamisch zu variieren, sollten Sie bedenken, dass dies den Benutzer verwirren könnte, der nicht erwartet, dass sich dieser Teil der Zielliste ändert.

### <a name="apis"></a>APIs

-   [**ICustomDestinationList::AddUserTasks**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-addusertasks)

## <a name="customizing-jump-lists"></a>Anpassen von Sprunglisten

Eine Anwendung kann eigene Kategorien definieren und sie zusätzlich zu oder statt der Standardkategorien **Recent** und **Frequent** in einem Sprungliste. Die Anwendung kann ihre eigenen Ziele in diesen benutzerdefinierten Kategorien basierend auf der Architektur und der beabsichtigten Verwendung der Anwendung steuern. Der folgende Screenshot zeigt eine benutzerdefinierte Sprungliste mit der Kategorie Verlauf.

![Benutzerdefinierte Sprungliste](images/taskbar/customjumplist.png)

Wenn eine Anwendung beschließt, eine benutzerdefinierte Kategorie zur Verfügung zu stellen, übernimmt diese Anwendung die Verantwortung für das Auf populieren. Der Kategorieinhalt sollte weiterhin benutzerspezifisch sein und auf Benutzerverlauf, Aktionen oder beidem basieren, aber über eine benutzerdefinierte Kategorie kann eine Anwendung bestimmen, was sie nachverfolgen und was sie ignorieren möchte, möglicherweise basierend auf einer Anwendungsoption. Beispielsweise könnte ein Audioprogramm nur kürzlich abgespielte Albums enthalten und zuletzt abgespielte einzelne Titel ignorieren.

Wenn ein Benutzer ein Element aus der Liste entfernt hat, was immer eine Benutzeroption ist, muss die Anwendung dies in Dieseingen. Die Anwendung muss außerdem sicherstellen, dass Elemente in der Liste gültig sind oder dass sie ordnungsgemäß fehlschlagen, wenn sie gelöscht wurden. Einzelne Elemente oder der gesamte Inhalt der Liste können programmgesteuert entfernt werden.

Die maximale Anzahl von Elementen in einer Zielliste wird vom System basierend auf verschiedenen Faktoren wie Anzeigeauflösung und Schriftgrad bestimmt. Wenn nicht genügend Platz für alle Elemente in allen Kategorien vorhanden ist, werden sie von unten nach oben abgeschnitten.

### <a name="apis"></a>APIs

-   [**ICustomDestinationList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icustomdestinationlist)
-   [**IApplicationDetolations**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdestinations)
-   [**IApplicationDocumentLists**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdocumentlists)

## <a name="thumbnail-toolbars"></a>Miniaturansichtssymbolleisten

Um Zugriff auf die Schlüsselbefehle eines bestimmten Fensters zu ermöglichen, ohne dass der Benutzer das Fenster der Anwendung wiederhergestellt oder aktiviert, kann ein aktives Symbolleisten-Steuerelement in die Vorschau der Miniaturansicht dieses Fensters eingebettet werden. Beispielsweise können Windows Media Player Standardmäßige Medientransportsteuerelemente wie Wiedergabe, Pause, Stummschalten und Beenden bieten. Die Benutzeroberfläche zeigt diese Symbolleiste direkt unterhalb der Miniaturansicht an, wie in der folgenden Abbildung gezeigt– sie deckt keinen Teil davon ab.

![Miniaturansichts-Taskleiste für Windows Media Player mit drei Schaltflächen: Zurück, Wiedergabe und Vorwärts](images/taskbar/thumbbar.png)

Diese Symbolleiste ist einfach das vertraute allgemeine Standardsymbolleisten-Steuerelement. Es verfügt über maximal sieben Schaltflächen. DIE ID, das Bild, die QuickInfo und der Zustand jeder Schaltfläche werden in einer -Struktur definiert, die dann an die Taskleiste übergeben wird. Die Anwendung kann Schaltflächen in der Miniaturansichtssymbolleiste anzeigen, aktivieren, deaktivieren oder ausblenden, wie dies für den aktuellen Zustand erforderlich ist.

Da der Platz zum Anzeigen von Miniaturansichten und eine variable Anzahl von Miniaturansichten begrenzt ist, wird für Anwendungen keine bestimmte Symbolleistengröße garantiert. Wenn der Platz eingeschränkt ist, werden Schaltflächen in der Symbolleiste von rechts nach links abgeschnitten. Daher sollten Sie beim Entwerfen der Symbolleiste die Befehle priorisieren, die Ihren Schaltflächen zugeordnet sind, und sicherstellen, dass die wichtigsten Befehle an erster Stelle stehen und aufgrund von Speicherplatzproblemen am wenigsten verworfen werden.

> [!Note]  
> Wenn eine Anwendung ein Fenster anzeigt, wird die Taskleistenschaltfläche vom System erstellt. Wenn die Schaltfläche angezeigt wird, sendet die Taskleiste eine **TaskbarButtonCreated-Nachricht** an das Fenster. Der Wert wird durch Aufrufen von [**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea)(L("TaskbarButtonCreated")) berechnet. Diese Nachricht muss von Ihrer Anwendung empfangen werden, bevor sie eine [**ITaskbarList3-Methode aufruft.**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist3)

 

### <a name="api"></a>API

-   [**ITaskbarList3::ThumbBarAddButtons**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbaraddbuttons)
-   [**ITaskbarList3::ThumbBarSetImageList**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbarsetimagelist)
-   [**ITaskbarList3::ThumbBarUpdateButtons**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbarupdatebuttons)
-   [**THUMBBUTTON**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-thumbbutton)

## <a name="icon-overlays"></a>Symbolüberlagerungen

Eine Anwendung kann dem Benutzer bestimmte Benachrichtigungen und den Status über die Taskleistenschaltfläche über die Anzeige kleiner Überlagerungen auf der Schaltfläche übermitteln. Diese Überlagerungen ähneln dem Typ der vorhandenen Überlagerung, die für Verknüpfungen oder Sicherheitsbenachrichtigungen verwendet wird und in der unteren rechten Ecke der Schaltfläche angezeigt wird. Um ein Überlagerungssymbol anzuzeigen, muss sich die Taskleiste im Standardmodus für große Symbole befinden, wie im folgenden Screenshot gezeigt.

![Windows Messenger-Taskleistenschaltfläche mit einer Überlagerung, um einen verfügbaren Status anzugeben](images/taskbar/taskbaroverlay.png)

Symbolüberlagerungen dienen als kontextbezogene Statusbenachrichtigung und sollen die Notwendigkeit eines separaten Infobereichs-Statussymbols zum Kommunizieren dieser Informationen an den Benutzer erschatten. Beispielsweise kann der neue E-Mail-Status in Microsoft Outlook, der derzeit im Infobereich angezeigt wird, jetzt über eine Überlagerung auf der Taskleistenschaltfläche angezeigt werden. Auch hier müssen Sie während des Entwicklungszyklus entscheiden, welche Methode für Ihre Anwendung am besten ist. Überlagerungssymbole sollen wichtige, langfristige Status oder Benachrichtigungen wie Netzwerkstatus, Messengerstatus oder neue E-Mails liefern. Dem Benutzer sollten keine sich ständig ändernden Überlagerungen oder Animationen angezeigt werden.

Da eine einzelne Überlagerung auf der Taskleistenschaltfläche und nicht in den einzelnen Miniaturansichten des Fensters überlagert wird, handelt es sich dabei um ein Feature pro Gruppe und nicht um ein Einzelnes Fenster. Anforderungen für Overlaysymbole können von einzelnen Fenstern in einer Taskleistengruppe empfangen werden, aber sie werden nicht in die Warteschlange gestellt. Die letzte empfangene Überlagerung ist die angezeigte Überlagerung.

### <a name="apis"></a>APIs

-   [**ITaskbarList3::SetOverlayIcon**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setoverlayicon)

## <a name="progress-bars"></a>Statusleisten

Eine Taskleistenschaltfläche kann verwendet werden, um eine Statusanzeige anzuzeigen. Dadurch kann ein Fenster dem Benutzer Statusinformationen bereitstellen, ohne dass dieser Benutzer zum Fenster selbst wechseln muss. Der Benutzer kann in einer anderen Anwendung produktiv bleiben, während er auf einen Blick den Fortschritt von vorgängen in anderen Fenstern sieht. Es ist vorgesehen, dass eine Statusanzeige in einer Taskleistenschaltfläche eine detailliertere Statusanzeige im Fenster selbst widerspiegelt. Dieses Feature kann zum Nachverfolgen von Dateikopien, Downloads, Installationen, Medien oder jedem Vorgang verwendet werden, der einen bestimmten Zeitraum in Betrieb nehmen wird. Dieses Feature ist nicht für die Verwendung mit normalen Peripherieaktionen wie dem Laden einer Webseite oder dem Drucken eines Dokuments vorgesehen. Dieser Statustyp sollte weiterhin in der Statusleiste eines Fensters angezeigt werden.

Die Statusleiste der Taskleistenschaltfläche ähnelt dem vertrauten Statusleisten-Steuerelement. Es kann entweder ein bestimmter Fortschritt basierend auf einem abgeschlossenen Prozentsatz des Vorgangs oder ein unbestimmter Fortschritt im Stil der Festzeit angezeigt werden, um anzugeben, dass der Vorgang ohne Vorhersage der verbleibenden Zeit durchgeführt wird. Es kann auch angezeigt werden, dass der Vorgang angehalten wurde oder ein Fehler aufgetreten ist und ein Benutzereingriff erforderlich ist.

### <a name="apis"></a>APIs

-   [**ITaskbarList3::SetProgressState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setprogressstate)
-   [**ITaskbarList3::SetProgressValue**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setprogressvalue)

## <a name="deskbands"></a>Deskbands

In Versionen von Windows vor Windows 7 konnte die Funktionalität der Miniaturansichtssymbolleiste über ein Deskband erreicht werden– eine Symbolleiste, die in der Taskleiste gehostet wird. Beispielsweise können Windows Media Player auf die Taskleiste als Gruppe von Transportsteuerelementen und nicht als Standardschaltfläche minimieren. In Windows 7 können Deskbands weiterhin implementiert werden, und Miniaturansichtssymbolleisten sollen sie nicht alle ersetzen. Nicht alle Anwendungen eignen sich für eine Miniaturansichtssymbolleiste, und eine andere Lösung wie ein Deskband oder eine Aufgabe in einer Zielliste ist möglicherweise die richtige Antwort für Ihre Anwendung. Sie müssen entscheiden, welche Lösung im Rahmen Ihres Entwicklungszyklus am besten für Ihre Anwendung funktioniert. Beachten Sie jedoch, dass Deskbands Windows Für mich Muss mit aktivierter Durchsichtigkeit (Glass) und der [**IDeskBand2-Schnittstelle unterstützt**](/windows/desktop/api/Shobjidl/nn-shobjidl-ideskband2) werden müssen.

### <a name="apis"></a>APIs

-   [**IDeskBand2**](/windows/desktop/api/Shobjidl/nn-shobjidl-ideskband2)

## <a name="notification-area"></a>Infobereich

Es wurden Änderungen am Benachrichtigungsbereich vorgenommen, die dem Benutzer viel mehr Kontrolle darüber geben, welche Symbole auf der Taskleiste angezeigt werden. Alle Benachrichtigungssymbole sind jetzt standardmäßig ausgeblendet, und diese Sichtbarkeit kann nicht programmgesteuert gesteuert werden. Nur der Benutzer kann auswählen, welche Benachrichtigungssymbole auf der Taskleiste angezeigt werden. Wenn eine Benachrichtigungssprechblase angezeigt wird, wird das Symbol vorübergehend sichtbar, aber auch dann kann ein Benutzer entscheiden, sie zu stillen. Eine Symbolüberlagerung auf einer Taskleistenschaltfläche wird daher zu einer ansprechenden Wahl, wenn Ihre Anwendung diese Informationen Ihren Benutzern übermitteln soll.

## <a name="thumbnails"></a>Miniaturbilder

In Windows Vista zeigt das Zeigen auf die Taskleistenschaltfläche einer Anwendung eine Miniaturansicht an, die das ausgeführte Fenster darstellt. Wenn die Taskleiste die Fenster der Anwendung reduziert hat, stellt die Miniaturansicht dies dar, indem sie als Stapel angezeigt wird, aber nur das aktive Fenster wird in der Miniaturansicht selbst angezeigt.

In Windows 7 wird jedes Mitglied einer Gruppe als separate Miniaturansicht angezeigt und ist jetzt auch ein Switchziel. Eine Anwendung kann ihre untergeordneten Fenster (z. B. echte untergeordnete Fenster, einzelne Dokumente oder Registerkarten) definieren und entsprechende Miniaturansichten für jedes dieser Fenster bereitstellen, auch wenn sie normalerweise nicht in der Taskleiste angezeigt werden. Dadurch können Benutzer direkt in die Ansicht der anwendung wechseln, die sie wünschen, anstatt in die Anwendung zu wechseln und dann zu ihrem Ziel zu wechseln. Beispielsweise können MDI-/TDI-Anwendungen (Multiple Document Interface) jedes Dokument oder jede Registerkarte als separate Miniaturansicht und Switchziel anzeigen, wenn der Mauszeiger auf die Taskleistenschaltfläche einer Gruppe zeigt.

![Drei Miniaturansichten der Taskleiste, die einzelne Registerkarten in Windows Internet Explorer darstellen](images/taskbar/taskbarthumbnails.png)

> [!Note]  
> Wie in Windows Vista muss Auch Dieser aktiv sein, um Miniaturansichten anzeigen zu können.

 

### <a name="api"></a>API

-   [**ITaskbarList3::RegisterTab**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-registertab)
-   [**ITaskbarList3::SetTabActive**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-settabactive)
-   [**ITaskbarList3::SetTabOrder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-settaborder)
-   [**ITaskbarList3::UnregisterTab**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-unregistertab)
-   [**ITaskbarList4::SetTabProperties**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist4-settabproperties)

Miniaturansichtsdarstellungen für Fenster sind normalerweise automatisch, aber in Fällen, in denen das Ergebnis nicht optimal ist, kann die Miniaturansicht explizit angegeben werden. Standardmäßig wird für nur Fenster der obersten Ebene automatisch eine Miniaturansicht generiert, und die Miniaturansichten für untergeordnete Fenster werden als generische Darstellung angezeigt. Dies kann zu einer weniger idealen (und sogar verwirrenden) Erfahrung für den Endbenutzer führen. Eine bestimmte Miniaturansicht des Switchziels für jedes untergeordnete Fenster bietet z. B. eine viel bessere Benutzererfahrung.

### <a name="api"></a>API

-   [**DwmSetWindowAttribute**](/windows/win32/api/dwmapi/nf-dwmapi-dwmsetwindowattribute)
-   [**DwmSetIconicThumbnail**](/windows/win32/api/dwmapi/nf-dwmapi-dwmseticonicthumbnail)
-   [**DwmSetIconicLivePreviewBitmap**](/windows/win32/api/dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap)
-   [**DwmInvalidateIconicBitmaps**](/windows/win32/api/dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps)
-   [**WM \_ DWMSENDICONICTHUMBNAIL**](../dwm/wm-dwmsendiconicthumbnail.md)
-   [**WM \_ DWMSENDICONICLIVEPREVIEWBITMAP**](../dwm/wm-dwmsendiconiclivepreviewbitmap.md)

Sie können einen bestimmten Bereich des Fensters auswählen, der als Miniaturansicht verwendet werden soll. Dies kann nützlich sein, wenn eine Anwendung weiß, dass ihre Dokumente oder Registerkarten ähnlich angezeigt werden, wenn sie in miniaturer Größe angezeigt werden. Die Anwendung kann dann auswählen, nur den Teil des Clientbereichs anzuzeigen, den der Benutzer verwenden kann, um zwischen Miniaturansichten zu unterscheiden. Wenn Sie jedoch auf eine beliebige Miniaturansicht zeigen, wird eine Ansicht des vollständigen Fensters darunter angezeigt, damit der Benutzer auch schnell einen Blick darauf ziehen kann.

Wenn mehr Miniaturansichten vorhanden sind, als angezeigt werden können, wird die Vorschau auf die Legacyminiaturansicht oder ein Standardsymbol zurückgesetzt.

### <a name="api"></a>API

-   [**ITaskbarList3::SetThumbnailClip**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setthumbnailclip)

Zum Hinzufügen **von An Taskleiste anheften** zum Kontextmenü eines Elements, das normalerweise nur für Dateitypen erforderlich ist, die den [IsShortCut-Eintrag](./links.md) enthalten, wird der entsprechende Kontextmenühandler registriert. Dies gilt auch für **An Startmenü anheften.** Weitere Informationen finden Sie unter [Registrieren von Shellerweiterungshandlern.](reg-shell-exts.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Die Taskleiste](taskbar.md)
</dt> <dt>

[Anwendungsbenutzermodell-IDs (AppUserModelIDs)](appids.md)
</dt> <dt>

[Benachrichtigungen und der Infobereich](notification-area.md)
</dt> </dl>

 

 
