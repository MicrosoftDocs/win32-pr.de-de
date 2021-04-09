---
title: Dialogfelder "Info"
description: In diesem Thema wird die Verwendung von Dialogfeldern zum Erstellen von Benutzeroberflächen für Anwendungen erläutert.
ms.assetid: 51960c28-a178-4ad3-b45e-426fec42a945
keywords:
- Dialogfelder, Info
- zu verwendende Dialogfelder
- Modale Dialogfelder
- Nicht modale Dialogfelder
- Dialogfelder, Modal
- Dialogfelder, ohne Modell
- Dialogfelder, Vorlagen
- Dialogfelder, Besitzer Fenster
- Dialogfelder, Meldungs Felder
- Dialogfeld Prozeduren
- Meldungsfelder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45dd78713c3b87e54e8a992ea9415577c522fc9e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039370"
---
# <a name="about-dialog-boxes"></a>Dialogfelder "Info"

Es gibt zahlreiche Funktionen, Meldungen und vordefinierte Steuerelemente, die Sie beim Erstellen und Verwalten von Dialogfeldern unterstützen, sodass die Benutzeroberfläche für eine Anwendung einfacher entwickelt werden kann. In dieser Übersicht werden die Dialogfeld Funktionen und-Meldungen beschrieben und erläutert, wie Sie zum Erstellen und Verwenden von Dialogfeldern verwendet werden.

Diese Übersicht umfasst die folgenden Themen:

-   [Verwendung eines Dialog Felds](#when-to-use-a-dialog-box)
-   [Dialog Feld Besitzer Fenster](#dialog-box-owner-window)
-   [Meldungsfelder](#message-boxes)
-   [Modale Dialog Felder](#modal-dialog-boxes)
-   [Nicht modante Dialog Felder](#modeless-dialog-boxes)
-   [Dialog Feld Vorlagen](#dialog-box-templates)
    -   [Dialog Feld Vorlagen Stile](#dialog-box-template-styles)
    -   [Dialog Feldmessungen](#dialog-box-measurements)
    -   [Dialog Feld-Steuerelemente](#dialog-box-controls)
    -   [Dialog Feld (Fenstermenü)](#dialog-box-window-menu)
    -   [Dialog Feld Schriftarten](#dialog-box-fonts)
    -   [Vorlagen im Arbeitsspeicher](#templates-in-memory)

Weitere Informationen zu den allgemeinen Dialogfeldern finden Sie unter [allgemeine Dialogfeld Bibliothek](common-dialog-box-library.md).

## <a name="when-to-use-a-dialog-box"></a>Verwendung eines Dialog Felds

In den meisten Anwendungen werden Dialogfelder verwendet, um zusätzliche Informationen für Menü Elemente einzugeben, die eine Benutzereingabe erfordern. Die Verwendung eines Dialog Felds ist die einzige empfohlene Methode für eine Anwendung zum Abrufen der Eingabe. Beispielsweise erfordert ein typisches **öffnetes** Menü Element den Namen einer Datei, die geöffnet werden soll. Daher sollte eine Anwendung ein Dialogfeld verwenden, um den Benutzer zur Eingabe des Namens aufzufordern. In solchen Fällen erstellt die Anwendung das Dialogfeld, wenn der Benutzer auf das Menü Element klickt, und zerstört das Dialogfeld sofort, nachdem der Benutzer die Informationen angegeben hat.

Viele Anwendungen verwenden auch Dialogfelder zum Anzeigen von Informationen oder Optionen, während der Benutzer in einem anderen Fenster arbeitet. Beispielsweise verwenden Textverarbeitungsanwendungen häufig ein Dialogfeld mit einer Text Suchoption. Während die Anwendung nach dem Text sucht, wird das Dialogfeld auf dem Bildschirm angezeigt. Der Benutzer kann dann zum Dialogfeld zurückkehren und erneut nach demselben Wort suchen. oder der Benutzer kann den Eintrag im Dialogfeld ändern und nach einem neuen Wort suchen. Anwendungen, die auf diese Weise Dialogfelder verwenden, erstellen in der Regel eine solche, wenn der Benutzer auf das Menü Element klickt, und zeigen die Anzeige weiterhin so lange an, wie die Anwendung ausgeführt wird oder wenn der Benutzer das Dialogfeld explizit schließt.

Um die unterschiedlichen Verwendungsmöglichkeiten von Anwendungen zu unterstützen, gibt es zwei Arten von Dialogfeldern: modale und nicht modale. Ein *modales Dialogfeld* erfordert, dass der Benutzerinformationen bereitstellt oder das Dialogfeld abbricht, bevor die Anwendung fortgesetzt werden kann. Anwendungen verwenden modale Dialogfelder in Verbindung mit Menü Elementen, für die zusätzliche Informationen erforderlich sind, bevor Sie fortfahren können. Ein nicht modalem *Dialogfeld* ermöglicht dem Benutzer, Informationen bereitzustellen und zur vorherigen Aufgabe zurückzukehren, ohne das Dialogfeld zu schließen. Modale Dialogfelder sind einfacher zu verwalten als nicht modale Dialogfelder, da Sie erstellt werden, ihre Aufgabe ausführen und durch Aufrufen einer einzelnen Funktion zerstört werden.

Um ein modales oder nicht modales Dialogfeld zu erstellen, muss eine Anwendung eine Dialogfeld Vorlage bereitstellen, um den Dialogfeld Stil und den Inhalt zu beschreiben. die Anwendung muss auch eine Dialogfeld Prozedur zum Ausführen von Aufgaben bereitstellen. Die *Dialogfeld Vorlage* ist eine binäre Beschreibung des Dialog Felds und der darin enthaltenen Steuerelemente. Der Entwickler kann diese Vorlage als Ressource erstellen, die aus der ausführbaren Datei der Anwendung geladen oder im Arbeitsspeicher erstellt wird, während die Anwendung ausgeführt wird. Die *Dialogfeld Prozedur* ist eine Anwendungs definierte Rückruffunktion, die vom System aufgerufen wird, wenn es Eingaben für das Dialogfeld oder Tasks enthält, die das Dialogfeld ausführen soll. Obwohl eine Dialogfeld Prozedur mit einer Fenster Prozedur vergleichbar ist, verfügt sie nicht über die gleichen Zuständigkeiten.

Eine Anwendung erstellt ein Dialogfeld in der Regel mithilfe der [**Dialogbox**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) - [**Funktion oder**](/windows/desktop/api/Winuser/nf-winuser-createdialoga) der Funktion "die Funktion". **Dialogbox** erstellt ein modales Dialogfeld. Mit " **kreatedialog** " wird ein nicht modalem Dialogfeld erstellt. Diese beiden Funktionen laden eine Dialogfeld Vorlage aus der ausführbaren Datei der Anwendung und erstellen ein Popup Fenster, das den Spezifikationen der Vorlage entspricht. Es gibt weitere Funktionen, die ein Dialogfeld mithilfe von Vorlagen im Arbeitsspeicher erstellen. Sie übergeben zusätzliche Informationen an die Dialogfeld Prozedur, während das Dialogfeld erstellt wird.

Dialog Felder gehören normalerweise zu einer vordefinierten, exklusiven Fenster Klasse. Das System verwendet diese Fenster Klasse und die zugehörige Fenster Prozedur für modale und nicht modale Dialogfelder. Wenn die-Funktion aufgerufen wird, erstellt Sie das Fenster für das Dialogfeld sowie die Fenster für die Steuerelemente im Dialogfeld und sendet dann die ausgewählten Meldungen an die Dialogfeld Prozedur. Während das Dialogfeld sichtbar ist, verwaltet die vordefinierte Fenster Prozedur alle Nachrichten, verarbeitet einige Meldungen und übergibt andere an die Dialogfeld Prozedur, sodass die Prozedur Aufgaben ausführen kann. Anwendungen haben keinen direkten Zugriff auf die vordefinierte Fenster Klasse oder Fenster Prozedur, Sie können jedoch mithilfe der Dialogfeld Vorlage und der Dialogfeld Prozedur den Stil und das Verhalten eines Dialog Felds ändern.

## <a name="dialog-box-owner-window"></a>Dialog Feld Besitzer Fenster

Die meisten Dialogfelder haben ein Besitzer Fenster (oder mehr einfach einen Besitzer). Wenn Sie das Dialogfeld erstellen, legt die Anwendung den Besitzer fest, indem das Fenster Handle des Besitzers angegeben wird. Das System verwendet den Besitzer, um die Position des Dialog Felds in der Z-Reihenfolge zu bestimmen, sodass das Dialogfeld immer oberhalb seines Besitzers positioniert ist. Außerdem kann das System Nachrichten an die Fenster Prozedur des Besitzers senden und die Ereignisse im Dialogfeld benachrichtigen.

Das System blendet das Dialogfeld automatisch aus, wenn der Besitzer ausgeblendet oder zerstört wird. Dies bedeutet, dass für die Dialogfeld Prozedur keine besondere Verarbeitung erforderlich ist, um Änderungen am Zustand des Besitzer Fensters zu erkennen.

Da das typische Dialogfeld in Verbindung mit einem Menü Element verwendet wird, ist das Besitzer Fenster in der Regel das Fenster, das das Menü enthält. Obwohl es möglich ist, ein Dialogfeld zu erstellen, das keinen Besitzer hat, wird es nicht empfohlen. Wenn ein modales Dialogfeld z. b. keinen Besitzer hat, deaktiviert das System keines der anderen Fenster der Anwendung und ermöglicht dem Benutzer, die Arbeit weiterhin in den anderen Fenstern auszuführen, sodass der Zweck des modalen Dialog Felds nicht mehr besteht.

Wenn ein nicht modalem Dialogfeld keinen Besitzer hat, wird das Dialogfeld weder ausgeblendet noch zerstört, wenn andere Fenster in der Anwendung ausgeblendet oder zerstört werden. Obwohl dies nicht den Zweck des nicht modalem Dialog Felds unterscheidet, erfordert dies, dass die Anwendung eine spezielle Verarbeitung durchführt, um sicherzustellen, dass das Dialogfeld zu den entsprechenden Zeitpunkten ausgeblendet und zerstört wird.

## <a name="message-boxes"></a>Meldungsfelder

Ein Meldungs Feld ist ein spezielles Dialogfeld, das von einer Anwendung zum Anzeigen von Nachrichten und zur Eingabe einer einfachen Eingabe verwendet werden kann. Ein Meldungs Feld enthält in der Regel eine Textnachricht und eine oder mehrere Schaltflächen. Eine Anwendung erstellt das Meldungs Feld mithilfe der [**MessageBox**](/windows/desktop/api/Winuser/nf-winuser-messagebox) -oder der [**messageboxex**](/windows/desktop/api/Winuser/nf-winuser-messageboxexa) -Funktion und gibt dabei den Text sowie die Anzahl und die Typen der anzuzeigenden Schaltflächen an. Beachten Sie, dass es derzeit keinen Unterschied zwischen der Funktionsweise von **MessageBox** und **messageboxex** gibt.

Obwohl es sich bei dem Meldungs Feld um ein Dialogfeld handelt, übernimmt das System die komplette Kontrolle über die Erstellung und Verwaltung der MessageBox. Dies bedeutet, dass die Anwendung keine Dialogfeld Vorlage und keine Dialogfeld Prozedur bereitstellt. Das System erstellt eine eigene Vorlage basierend auf dem Text und den Schaltflächen, die für das Meldungs Feld angegeben sind, und stellt eine eigene Dialogfeld Prozedur bereit.

Ein Meldungs Feld ist ein modales Dialogfeld, das vom System mit denselben internen Funktionen erstellt wird, die von [**Dialogbox**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) verwendet werden. Wenn die Anwendung ein Besitzer Fenster angibt, wenn [**MessageBox**](/windows/desktop/api/Winuser/nf-winuser-messagebox) oder [**messageboxex**](/windows/desktop/api/Winuser/nf-winuser-messageboxexa)aufgerufen wird, deaktiviert das System den Besitzer. Eine Anwendung kann das System auch anweisen, alle Fenster der obersten Ebene, die zum aktuellen Thread gehören, zu deaktivieren, indem Sie beim Erstellen des Dialog Felds den Wert **MB \_ taskmodal** angeben.

Das System kann Nachrichten an den Besitzer senden, wie z. b. [**WM \_ cancelmode**](/windows/desktop/winmsg/wm-cancelmode) und [**WM \_ enable**](/windows/desktop/winmsg/wm-enable), genauso wie beim Erstellen eines modalen Dialog Felds. Das Besitzer Fenster sollte alle von diesen Nachrichten angeforderten Aktionen ausführen.

## <a name="modal-dialog-boxes"></a>Modale Dialog Felder

Ein modales Dialogfeld sollte ein Popup Fenster mit einem Fenstermenü, einer Titelleiste und einem dicken Rahmen sein. Das heißt, die Dialogfeld Vorlage sollte die Stile **" \_ WS Popup**", " **WS \_ sysmenu**", " **WS \_ Caption**" und " **DS \_ modalframe** " angeben. Obwohl eine Anwendung den **\_ sichtbaren WS** -Stil festlegen kann, zeigt das System immer ein modales Dialogfeld an, unabhängig davon, ob in der Dialogfeld Vorlage der **\_ sichtbare WS** -Stil angegeben ist. Eine Anwendung darf kein modales Dialogfeld mit dem untergeordneten **WS \_ -Stil** erstellen. Ein modales Dialogfeld mit diesem Stil deaktiviert sich selbst und verhindert, dass nachfolgende Eingaben die Anwendung erreichen.

Eine Anwendung erstellt ein modales Dialogfeld mit der Funktion [**Dialogbox**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) oder [**dialogboxindirekte**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta) . **Dialogbox** erfordert den Namen oder den Bezeichner einer Ressource, die eine Dialogfeld Vorlage enthält. **Dialogboxindirekte** erfordert ein Handle für ein Speicher Objekt, das eine Dialogfeld Vorlage enthält. Die Funktionen [**DialogBoxParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxparama) und [**dialogboxderetparam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama) erstellen auch modale Dialogfelder. Sie sind mit den zuvor erwähnten Funktionen identisch, übergeben aber einen angegebenen Parameter an die Dialogfeld Prozedur, wenn das Dialogfeld erstellt wird.

Wenn Sie das modale Dialogfeld erstellen, wird es vom System in das aktive Fenster. Das Dialogfeld bleibt aktiv, bis die Dialogfeld Prozedur die [**EndDialog**](/windows/desktop/api/Winuser/nf-winuser-enddialog) -Funktion aufruft, oder das System aktiviert ein Fenster in einer anderen Anwendung. Weder der Benutzer noch die Anwendung kann das Besitzer Fenster so lange aktivieren, bis das modale Dialogfeld zerstört wird.

Wenn das Besitzer Fenster nicht bereits deaktiviert ist, deaktiviert das System automatisch das Fenster und alle untergeordneten Fenster, die zu diesem Element gehören, wenn das modale Dialogfeld erstellt wird. Das Besitzer Fenster bleibt deaktiviert, bis das Dialogfeld zerstört wird. Obwohl eine Dialogfeld Prozedur das Besitzer Fenster jederzeit potenziell aktivieren könnte, wird der Zweck des modalen Dialog Felds durch Aktivieren des Besitzers unter Umständen nicht empfohlen. Wenn die Dialogfeld Prozedur zerstört wird, aktiviert das System das Besitzer Fenster erneut. Dies gilt jedoch nur, wenn das modale Dialogfeld bewirkt hat, dass der Besitzer deaktiviert wurde.

Wenn das System das modale Dialogfeld erstellt, sendet es die " [**WM \_ cancelmode**](/windows/desktop/winmsg/wm-cancelmode) "-Meldung an das Fenster (sofern vorhanden), das momentan die Maus Eingaben erfasst. Eine Anwendung, die diese Nachricht empfängt, sollte die Maus Aufzeichnung freigeben, damit der Benutzer die Maus im modalen Dialogfeld bewegen kann. Da das System das Besitzer Fenster deaktiviert, gehen alle Maus Eingaben verloren, wenn der Besitzer die Maus beim Empfang dieser Nachricht nicht freigeben kann.

Zum Verarbeiten von Nachrichten für das modale Dialogfeld startet das System seine eigene Nachrichten Schleife und übernimmt die temporäre Steuerung der Nachrichten Warteschlange für die gesamte Anwendung. Wenn das System eine Nachricht abruft, die nicht explizit für das Dialogfeld angezeigt wird, wird die Nachricht an das entsprechende Fenster gesendet. Wenn eine " [**WM \_ Quit**](/windows/desktop/winmsg/wm-quit) "-Meldung abgerufen wird, wird die Nachricht wieder an die Anwendungs Nachrichten Warteschlange gesendet, damit die Hauptnachrichten Schleife der Anwendung die Nachricht schließlich abrufen kann.

Das System sendet die WM-Nachricht " [**\_ enteridle**](wm-enteridle.md) " an das Besitzer Fenster, wenn die Anwendungs Nachrichten Warteschlange leer ist. Die Anwendung kann diese Nachricht verwenden, um eine Hintergrundaufgabe auszuführen, während das Dialogfeld auf dem Bildschirm verbleibt. Wenn eine Anwendung die Nachricht auf diese Weise verwendet, muss die Anwendung häufig die Kontrolle übernehmen (z. b. mithilfe der Funktion " [**Peer Message**](/windows/desktop/api/winuser/nf-winuser-peekmessagea) "), damit das modale Dialogfeld beliebige Benutzereingaben empfangen kann. Um zu verhindern, dass das modale Dialogfeld die Nachrichten der **WM \_** -Unterhaltung sendet, kann die Anwendung \_ beim Erstellen des Dialog Felds den Stil "DS noidlemsg" angeben.

Eine Anwendung zerstört mithilfe der Funktion " [**EndDialog**](/windows/desktop/api/Winuser/nf-winuser-enddialog) " ein modales Dialogfeld. In den meisten Fällen ruft die Dialogfeld Prozedur **EndDialog** auf, wenn der Benutzer im Menü Fenster des Dialog Felds auf **Schließen** klickt oder im Dialogfeld auf die Schaltfläche **OK** oder **Abbrechen** klickt. Im Dialogfeld kann ein Wert durch die [**Dialogbox**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) -Funktion (oder andere Erstellungs Funktionen) zurückgegeben werden, indem beim Aufrufen der **EndDialog** -Funktion ein Wert angegeben wird. Das System gibt diesen Wert zurück, nachdem das Dialogfeld zerstört wurde. Die meisten Anwendungen verwenden diesen Rückgabewert, um zu bestimmen, ob das Dialogfeld seine Aufgabe erfolgreich abgeschlossen hat oder vom Benutzer abgebrochen wurde. Das System gibt die Steuerung von der-Funktion, die das Dialogfeld erstellt, erst zurück, wenn die Dialogfeld Prozedur die **EndDialog** -Funktion aufgerufen hat.

## <a name="modeless-dialog-boxes"></a>Nicht modante Dialog Felder

Ein nicht modalem Dialogfeld sollte ein Popup Fenster mit einem Fenstermenü, einer Titelleiste und einem dünnen Rahmen sein. Das heißt, die Dialogfeld Vorlage sollte das **WS- \_ Popup**, **die WS- \_ Beschriftung**, den **WS \_**-Rahmen und die **WS- \_ sysmenu** -Stile angeben. Das System zeigt das Dialogfeld nicht automatisch an, es sei denn, die Vorlage gibt den **\_ sichtbaren WS** -Stil an.

Eine Anwendung erstellt ein Dialogfeld ohne Modus [**mithilfe der Funktion**](/windows/desktop/api/Winuser/nf-winuser-createdialoga) "up" oder der Funktion " [**kreatedialogindirect**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirecta) ". Für " **kreatedialog** " ist der Name oder der Bezeichner einer Ressource erforderlich, die eine Dialogfeld Vorlage enthält. " **Kreatedialogindirect** " erfordert ein Handle für ein Speicher Objekt, das eine Dialogfeld Vorlage enthält. Zwei weitere [**Funktionen, "**](/windows/desktop/api/Winuser/nf-winuser-createdialogparama) ", "", "", "", "", "", " [**", "**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama)", "". Sie übergeben einen angegebenen Parameter an die Dialogfeld Prozedur, wenn das Dialogfeld erstellt wird.

Mit " [**kreatedialog**](/windows/desktop/api/Winuser/nf-winuser-createdialoga) " und anderen Erstellungs Funktionen wird ein Fenster Handle für das Dialogfeld zurückgegeben. Die Anwendung und die Dialogfeld Prozedur können dieses Handle verwenden, um das Dialogfeld zu verwalten. Wenn z. b. in der Dialogfeld Vorlage nicht **\_ sichtbar** ist, kann die Anwendung das Dialogfeld anzeigen, indem das Fenster Handle an die [**ShowWindow**](/windows/desktop/api/winuser/nf-winuser-showwindow) -Funktion übergeben wird.

Ein nicht modalem Dialogfeld deaktiviert weder das Besitzer Fenster noch das Senden von Nachrichten an dieses Dialogfeld. Beim Erstellen des Dialog Felds wird das System zum aktiven Fenster, aber der Benutzer oder die Anwendung kann das aktive Fenster jederzeit ändern. Wenn das Dialogfeld inaktiv wird, bleibt es in der Z-Reihenfolge über dem Besitzer Fenster, auch wenn das Besitzer Fenster aktiv ist.

Die Anwendung ist für das Abrufen und Verteilen von Eingabe Nachrichten an das Dialogfeld verantwortlich. Die meisten Anwendungen verwenden die Hauptnachrichten Schleife für dieses. Um dem Benutzer zu gestatten, mithilfe der Tastatur auf Steuerelemente zu wechseln und diese auszuwählen, muss die Anwendung jedoch die [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) -Funktion abrufen. Weitere Informationen zu dieser Funktion finden Sie unter [Dialog Feld "Tastaturschnittstelle](dlgbox-programming-considerations.md)".

Ein nicht modales Dialogfeld kann einen Wert nicht an die Anwendung zurückgeben, da es sich um ein modales Dialogfeld handelt, aber die Dialogfeld Prozedur kann mithilfe der [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) -Funktion Informationen an das Besitzer Fenster senden.

Eine Anwendung muss alle nicht modalem Dialogfelder vor dem Beenden zerstören. Mithilfe der [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) -Funktion kann ein nicht modalem Dialogfeld zerstört werden. In den meisten Fällen ruft die Dialogfeld Prozedur **DestroyWindow** als Reaktion auf Benutzereingaben auf, z. b. durch Klicken auf die Schaltfläche **Abbrechen** . Wenn der Benutzer das Dialogfeld nie auf diese Weise schließt, muss die Anwendung **DestroyWindow** aufzurufen.

[**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) macht das Fenster Handle für das Dialogfeld ungültig, sodass alle nachfolgenden Aufrufe von Funktionen, die das Handle verwenden, Fehler Werte zurückgeben. Um Fehler zu vermeiden, sollte die Dialogfeld Prozedur den Besitzer Benachrichtigen, dass das Dialogfeld zerstört wurde. Viele Anwendungen pflegen eine globale Variable, die das Handle für das Dialogfeld enthält. Wenn die Dialogfeld Prozedur das Dialogfeld zerstört, wird auch die globale Variable auf **null** festgelegt, um anzugeben, dass das Dialogfeld nicht mehr gültig ist.

Die Dialogfeld Prozedur darf nicht die [**EndDialog**](/windows/desktop/api/Winuser/nf-winuser-enddialog) -Funktion aufzurufen, um ein nicht modalem Dialogfeld zu zerstören.

## <a name="dialog-box-templates"></a>Dialog Feld Vorlagen

Eine Dialogfeld Vorlage ist Binärdaten, die das Dialogfeld beschreiben, das die Höhe, die Breite, den Stil und die darin enthaltenen Steuerelemente definiert. Um ein Dialogfeld zu erstellen, lädt das System entweder eine Dialogfeld Vorlage aus den Ressourcen in der ausführbaren Datei der Anwendung oder verwendet die Vorlage, die von der Anwendung im globalen Speicher weitergegeben wurde. In beiden Fällen muss die Anwendung eine Vorlage angeben, wenn ein Dialogfeld erstellt wird.

Ein Entwickler erstellt Vorlagen Ressourcen mithilfe eines Ressourcen Compilers oder eines Dialogfeld-Editors. Ein Ressourcen Compiler konvertiert eine Textbeschreibung in eine binäre Ressource, und ein Dialogfeld-Editor speichert ein interaktiv konstruiertes Dialogfeld als binäre Ressource.

> [!Note]  
> Eine Erläuterung, wie Vorlagen Ressourcen erstellt und der ausführbaren Datei der Anwendung hinzugefügt werden, würde den Rahmen dieser Übersicht sprengen. Weitere Informationen zum Erstellen von Vorlagen Ressourcen und zum Hinzufügen zu einer ausführbaren Datei finden Sie in der Dokumentation, die mit ihren Anwendungs Entwicklungs Tools bereitgestellt wird.

 

Wenn Sie ein Dialogfeld ohne Vorlagen Ressourcen erstellen möchten, müssen Sie eine Vorlage im Arbeitsspeicher erstellen und an die [**createdialogindirectparam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama) -oder [**dialogboxderesparam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama) -Funktion oder an das-Makro [**createdialogindirect**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirecta) oder [**dialogboxindirekte**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta) übergeben.

Eine Dialogfeld Vorlage im Arbeitsspeicher besteht aus einem Header, der das Dialogfeld beschreibt, gefolgt von einem oder mehreren zusätzlichen Datenblöcken, die die einzelnen Steuerelemente im Dialogfeld beschreiben. Die Vorlage kann entweder das Standardformat oder das erweiterte Format verwenden. In einer Standardvorlage ist der Header eine [**DLGTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgtemplate) -Struktur, gefolgt von zusätzlichen Arrays variabler Länge. und die Daten für jedes Steuerelement bestehen aus einer [**DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) -Struktur, gefolgt von zusätzlichen Arrays variabler Länge. In einer erweiterten Dialogfeld Vorlage verwendet der Header das [**dlgtemplateex**](dlgtemplateex.md) -Format, und die Steuerelement Definitionen verwenden das [**dlgitemtemplateex**](dlgitemtemplateex.md) -Format.

Sie können eine Speicher Vorlage erstellen, indem Sie ein globales Speicher Objekt zuordnen und es mit den standardmäßigen oder erweiterten Header-und Steuerelement Definitionen auffüllen. Eine Arbeitsspeicher Vorlage ist in Form und Inhalt mit einer Vorlagen Ressource identisch. Viele Anwendungen, die Speicher Vorlagen verwenden, verwenden die [**LoadResource**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadresource) -Funktion, um eine Vorlagen Ressource in den Arbeitsspeicher zu laden, und ändern dann die geladene Ressource, um eine neue Arbeitsspeicher Vorlage zu erstellen. Weitere Informationen zum Erstellen einer Dialogfeld Vorlage im Speicher finden Sie unter [Vorlagen im Arbeitsspeicher](#templates-in-memory).

In den folgenden Abschnitten werden die Stile, Messungen und anderen Werte beschrieben, die in einer Dialogfeld Vorlage verwendet werden.

-   [Dialog Feld Vorlagen Stile](#dialog-box-template-styles)
-   [Dialog Feldmessungen](#dialog-box-measurements)
-   [Dialog Feld-Steuerelemente](#dialog-box-controls)
-   [Dialog Feld (Fenstermenü)](#dialog-box-window-menu)
-   [Dialog Feld Schriftarten](#dialog-box-fonts)
-   [Vorlagen im Arbeitsspeicher](#templates-in-memory)

### <a name="dialog-box-template-styles"></a>Dialog Feld Vorlagen Stile

Jede Dialogfeld Vorlage gibt eine Kombination von Stilwerten an, die die Darstellung und die Features des Dialog Felds definieren. Die Stilwerte können Fenster Stile wie z. b. **WS- \_ Popup** und **WS- \_ sysmenu** und Dialogfeld Stile wie z. b. **DS \_ modalframe** sein. Die Anzahl und Art der Stile für eine Vorlage sind abhängig vom Typ und Zweck des Dialog Felds. Eine Liste der Werte finden Sie unter [**Dialog Feld Stile**](dialog-box-styles.md).

Beim Erstellen des Dialog Felds übergibt das System alle in der Vorlage angegebenen Fenster Stile an die Funktion " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) ". Abhängig von den angegebenen Dialogfeld Stilen kann das System abhängig von den angegebenen Dialogfeld Formaten ein oder mehrere erweiterte Stile übergeben. Wenn die Vorlage z. b. **DS \_ modalframe** angibt, verwendet das System beim Erstellen des Dialog Felds **WS \_ Ex \_ dlgmodalframe** .

Die meisten Dialogfelder sind Popup Fenster, die ein Fenstermenü und eine Titelleiste haben. Daher gibt die typische Vorlage die Stile " **WS \_ Popup**", " **WS \_ sysmenu**" und " **WS \_ Caption** " an. Die Vorlage gibt auch eine Rahmenart an **: \_ WS** -Rahmen für nicht modale Dialogfelder und **DS \_ modalframe** für modale Dialogfelder. Eine Vorlage kann einen anderen Fenstertyp als Popup angeben (z. b **. \_ über** Lapp Ende WS), wenn Sie ein angepasstes Fenster anstelle eines Dialog Felds erstellt.

Das System zeigt immer ein modales Dialogfeld an, unabhängig davon, ob der **\_ sichtbare WS** -Stil angegeben ist. Wenn die Vorlage für ein nicht modalem Dialogfeld den **\_ sichtbaren WS** -Stil angibt, zeigt das System das Dialogfeld automatisch an, wenn es erstellt wird. Andernfalls ist die Anwendung für die Anzeige des Dialog Felds mit der [**ShowWindow**](/windows/desktop/api/winuser/nf-winuser-showwindow) -Funktion verantwortlich.

### <a name="dialog-box-measurements"></a>Dialog Feldmessungen

Jede Dialogfeld Vorlage enthält Messungen, mit denen die Position, Breite und Höhe des Dialog Felds und die darin enthaltenen Steuerelemente angegeben werden. Diese Messungen sind Geräte unabhängig, sodass eine Anwendung eine einzelne Vorlage verwenden kann, um das gleiche Dialogfeld für alle Anzeigegeräte Typen zu erstellen. Dadurch wird sichergestellt, dass ein Dialogfeld auf allen Bildschirmen die gleichen Proportionen und Darstellung hat, trotz unterschiedlicher Auflösungen und Seitenverhältnisse zwischen Bildschirmen.

Die Messungen in einer Dialogfeld Vorlage werden in Dialogfeld Vorlagen Einheiten angegeben. Verwenden Sie zum Konvertieren von Messungen von Dialogfeld Vorlagen Einheiten in Bildschirm Einheiten (Pixel) die [**mapdialogrect**](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect) -Funktion, die die vom Dialogfeld verwendete Schriftart berücksichtigt und ein Rechteck ordnungsgemäß aus den Dialogfeld Vorlagen Einheiten in Pixel konvertiert. In Dialogfeldern, in denen die System Schriftart verwendet wird, können Sie die [**GetDialogBaseUnits**](/windows/desktop/api/Winuser/nf-winuser-getdialogbaseunits) -Funktion verwenden, um die Konvertierungs Berechnungen selbst auszuführen, auch wenn Sie **mapdialogrect** einfacher verwenden.

Die Vorlage muss die anfänglichen Koordinaten der linken oberen Ecke des Dialog Felds angeben. In der Regel sind die Koordinaten relativ zur oberen linken Ecke des Client Bereichs des Besitzer Fensters. Wenn die Vorlage den DS- \_ absalign-Stil angibt oder das Dialogfeld keinen Besitzer hat, ist die Position relativ zur oberen linken Ecke des Bildschirms. Das System legt diese Anfangsposition fest, wenn das Dialogfeld erstellt wird, ermöglicht einer Anwendung jedoch das Anpassen der Position, bevor das Dialogfeld angezeigt wird. Beispielsweise kann eine Anwendung die Dimensionen des Besitzers-Fensters abrufen, eine neue Position berechnen, die das Dialogfeld im Besitzer Fenster zentriert, und dann die Position mit der [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) -Funktion festlegen.

In der Vorlage sollten eine Breite und Höhe des Dialog Felds angegeben werden, die die Breite und Höhe des Bildschirms nicht überschreitet, und es wird sichergestellt, dass alle Steuerelemente im Client Bereich des Dialog Felds liegen. Obwohl das System es zulässt, dass ein Dialogfeld eine beliebige Größe hat, kann das Erstellen eines zu kleinen oder zu großen Typs den Benutzer daran hindern, Eingaben bereitzustellen und den Zweck des Dialog Felds zu verhindern. Viele Anwendungen verwenden mehr als ein Dialogfeld, wenn eine große Anzahl von Steuerelementen vorhanden ist. In solchen Fällen enthält das erste Dialogfeld in der Regel eine oder mehrere Schaltflächen, die der Benutzer zum Anzeigen des nächsten Dialog Felds auswählen kann.

### <a name="dialog-box-controls"></a>Dialog Feld-Steuerelemente

Die Vorlage gibt die Position, Breite, Höhe, den Stil, den Bezeichner und die Fenster Klasse für jedes Steuerelement im Dialogfeld an. Das System erstellt jedes Steuerelement, indem es diese Daten an die Funktion " [**foratewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) " übergibt. Steuerelemente werden in der Reihenfolge erstellt, in der Sie in der Vorlage angegeben sind. Die Vorlage sollte die entsprechende Anzahl, den Typ und die Reihenfolge der Steuerelemente angeben, um sicherzustellen, dass der Benutzer die Eingabe eingeben kann, die zum Abschließen der dem Dialogfeld zugeordneten Aufgabe erforderlich ist.

Für jedes Steuerelement gibt die Vorlage Stil Werte an, mit denen die Darstellung und der Betrieb des Steuer Elements definiert werden. Jedes Steuerelement ist ein untergeordnetes Fenster und muss daher über den untergeordneten **WS \_** -Stil verfügen. Um sicherzustellen, dass das Steuerelement sichtbar ist, wenn das Dialogfeld angezeigt wird, muss jedes Steuerelement auch über das **\_ sichtbare WS** -Format verfügen. Andere häufig verwendete Fenster Stile sind **WS \_** -Rahmen für Steuerelemente, die über optionale Rahmen verfügen, für Steuerelemente, die bei der anfänglichen Erstellung des Dialog Felds deaktiviert werden sollen, und für Steuerelemente, auf die über die Tastatur zugegriffen werden soll, die WS **\_ Tabstopps** und die **\_ Gruppe** WS. **\_** Die **\_ Gruppen** Stile **WS \_ Tabstopps** und WS werden in Verbindung mit der Dialogfeld Tastatur-Schnittstelle verwendet, die weiter unten in diesem Thema beschrieben wird.

Die Vorlage kann auch Steuerelement Stile angeben, die spezifisch für die Fenster Klasse des Steuer Elements sind. Eine Vorlage, die ein Schaltflächen-Steuerelement angibt, muss z. b. ein Schaltflächen-Steuerelement Stil wie z. b. das Kontroll **\_ Kästchen**" **b \_** Das System übergibt die Steuerelement Stile über die [**WM \_ Create**](/windows/desktop/winmsg/wm-create) -Meldung an die Steuerelement Fenster Prozedur, sodass die Prozedur die Darstellung und den Betrieb des Steuer Elements anpassen kann.

Das System konvertiert die Positionskoordinaten und die Width-und Height-Messungen von den Dialog Basiseinheiten in Pixel, bevor diese an " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)" übergeben werden. Wenn das System ein Steuerelement erstellt, wird das Dialogfeld als übergeordnetes Fenster angegeben. Dies bedeutet, dass das System die Positionskoordinaten des-Steuer Elements immer als Client Koordinaten interpretiert, relativ zur oberen linken Ecke des Client Bereichs des Dialog Felds.

Die Vorlage gibt die Fenster Klasse für jedes Steuerelement an. Ein typisches Dialogfeld enthält Steuerelemente, die zu den vordefinierten Steuerelement Fenster Klassen gehören, z. b. die Schaltflächen-und Bearbeitungs Steuerelement-Klassen. In diesem Fall gibt die Vorlage Fenster Klassen an, indem die entsprechenden vordefinierten Atom-Werte für die Klassen bereitgestellt werden. Wenn ein Dialogfeld ein Steuerelement enthält, das zu einer benutzerdefinierten Steuerelement Fenster Klasse gehört, gibt die Vorlage den Namen der registrierten Fenster Klasse oder den Atom-Wert an, der derzeit dem Namen zugeordnet ist.

Jedes Steuerelement in einem Dialogfeld muss über einen eindeutigen Bezeichner verfügen, um ihn von anderen Steuerelementen zu unterscheiden. Steuert das Senden von Informationen an die Dialogfeld Prozedur über [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldungen, sodass die Steuerelement Bezeichner für die Prozedur erforderlich sind, um zu bestimmen, welches Steuerelement eine angegebene Nachricht gesendet hat. Die einzige Ausnahme von dieser Regel sind Steuerelement Bezeichner für statische Steuerelemente. Statische Steuerelemente erfordern keine eindeutigen Bezeichner, da Sie keine **WM- \_ Befehls** Nachrichten senden.

Um dem Benutzer zu gestatten, das Dialogfeld zu schließen, sollte in der Vorlage mindestens eine Schaltfläche "Push" angegeben und der Steuerelement Bezeichner " **IDCANCEL**" zugewiesen werden. Damit der Benutzer zwischen dem abschließen oder Abbrechen der dem Dialogfeld zugeordneten Aufgabe wählen kann, sollte die Vorlage zwei pushschaltflächen mit der Bezeichnung **OK** und **Abbrechen** mit den Steuerelement-IDs **IDOK** bzw. **IDCANCEL** angeben.

Eine Vorlage gibt auch optionale Text-und Erstellungs Daten für ein-Steuerelement an. Der Text stellt in der Regel Bezeichnungen für Schaltflächen-Steuerelemente oder den ursprünglichen Inhalt eines statischen Text Steuer Elements bereit. Bei den Erstellungs Daten handelt es sich um ein oder mehrere Daten bytes, die das System beim Erstellen des Steuer Elements an die Steuerelement Fenster Prozedur übergibt. Erstellungs Daten sind nützlich für Steuerelemente, die weitere Informationen zum ursprünglichen Inhalt oder Stil benötigen, als von anderen Daten angegeben werden. Beispielsweise kann eine Anwendung Erstellungs Daten verwenden, um die anfängliche Einstellung und den Bereich für ein ScrollBar-Steuerelement festzulegen.

### <a name="dialog-box-window-menu"></a>Dialog Feld (Fenstermenü)

Das System gibt einem Dialogfeld ein Fenstermenü, wenn die Vorlage den **WS \_ sysmenu** -Stil angibt. Um eine ungeeignete Eingabe zu verhindern, deaktiviert das System automatisch alle Elemente im Menü mit Ausnahme von " **verschieben** " und " **Schließen**". Der Benutzer kann auf **verschieben** klicken, um das Dialogfeld zu verschieben. Wenn der Benutzer auf **Schließen** klickt, sendet das System eine [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung an die Dialogfeld Prozedur, bei der der *wParam* -Parameter auf **IDCANCEL** festgelegt ist. Dies ist identisch mit der Meldung, die von der Schaltfläche **Abbrechen** gesendet wird, wenn der Benutzer darauf klickt. Die empfohlene Aktion für diese Meldung besteht darin, das Dialogfeld zu schließen und die angeforderte Aufgabe abzubrechen.

Obwohl andere Menüs in Dialogfeldern nicht empfohlen werden, kann eine Dialogfeld Vorlage ein Menü angeben, indem der Bezeichner oder der Name einer Menü Ressource angegeben wird. In diesem Fall lädt das System die Ressource und erstellt das Menü für das Dialogfeld. Anwendungen verwenden üblicherweise Menü Bezeichner oder Namen in Vorlagen, wenn die Vorlagen zum Erstellen von benutzerdefinierten Fenstern anstelle von Dialogfeldern verwendet werden.

### <a name="dialog-box-fonts"></a>Dialog Feld Schriftarten

Das System verwendet die durchschnittliche Zeichenbreite der Dialogfeld Schriftart, um die Position und die Dimensionen des Dialog Felds zu berechnen. Standardmäßig zeichnet das System den gesamten Text in einem Dialogfeld mithilfe der **\_ Schriftart** Schriftart des Systems.

Um eine Schriftart für ein anderes Dialogfeld als die Standardeinstellung anzugeben, müssen Sie das Dialogfeld mithilfe einer Dialogfeld Vorlage erstellen. Verwenden Sie in einer Vorlagen Ressource die [Font-Anweisung](../menurc/font-statement.md). Legen Sie in einer Dialogfeld Vorlage den Typ **DS \_ setFont** oder **DS \_ shellfont** fest, und geben Sie eine Punktgröße und einen Schriftart Namen an. Auch wenn eine Dialogfeld Vorlage eine Schriftart auf diese Weise angibt, verwendet das System immer die System Schriftart für die Menüs "Dialogfeld Titel" und "Dialogfeld".

Wenn das Dialogfeld den **DS- \_ setFont** -oder **DS- \_ shellfont** -Stil aufweist, sendet das System eine [**WM- \_ setFont**](/windows/desktop/winmsg/wm-setfont) -Meldung an die Dialogfeld Prozedur und an jedes Steuerelement, wenn es das Steuerelement erstellt. Die Dialogfeld Prozedur ist für das Speichern des Schriftart Handles zuständig, das mit der **WM- \_ setFont** -Nachricht übermittelt wurde, und das Auswählen des Handles in den Anzeigegeräte Kontext, wenn Text in das Fenster geschrieben wird. Dies wird standardmäßig von vordefinierten Steuerelementen durchführen.

Die Schriftart des Systems kann sich zwischen verschiedenen Versionen von Windows unterscheiden. Damit die Anwendung die System Schriftart unabhängig von dem System verwendet, auf dem Sie ausgeführt wird, verwenden Sie **DS \_ shellfont** mit der Schriftart MS Shell Dlg, und verwenden Sie die [DIALOGEX-Ressource](../menurc/dialogex-resource.md) anstelle der [Dialog Feld Ressource](../menurc/dialog-resource.md). Das System ordnet diese Schriftart so an, dass im Dialogfeld die Tahoma-Schriftart verwendet wird. Beachten Sie, dass **DS \_ shellfont** keine Auswirkung hat, wenn die Schriftart nicht MS Shell Dlg ist.

### <a name="templates-in-memory"></a>Vorlagen im Arbeitsspeicher

Eine Dialogfeld Vorlage im Arbeitsspeicher besteht aus einem Header, der das Dialogfeld beschreibt, gefolgt von einem oder mehreren zusätzlichen Datenblöcken, die die einzelnen Steuerelemente im Dialogfeld beschreiben. Die Vorlage kann entweder das Standardformat oder das erweiterte Format verwenden. In einer Standardvorlage ist der-Header eine [**DLGTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgtemplate) -Struktur, gefolgt von zusätzlichen Arrays variabler Länge. Die Daten für jedes Steuerelement bestehen aus einer [**DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) -Struktur, gefolgt von zusätzlichen Arrays variabler Länge. In einer erweiterten Dialogfeld Vorlage verwendet der Header das [**dlgtemplateex**](dlgtemplateex.md) -Format, und die Steuerelement Definitionen verwenden das [**dlgitemtemplateex**](dlgitemtemplateex.md) -Format.

Um zwischen einer Standardvorlage und einer erweiterten Vorlage zu unterscheiden, überprüfen Sie die ersten 16 Bits einer Dialogfeld Vorlage. In einer erweiterten Vorlage lautet das erste **Wort** "0xFFFF;". jeder andere Wert gibt eine Standardvorlage an.

Wenn Sie eine Dialogfeld Vorlage im Arbeitsspeicher erstellen, müssen Sie sicherstellen, dass die einzelnen [**DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) -oder [**dlgitemtemplateex**](dlgitemtemplateex.md) -Steuerelement Definitionen an den **DWORD** -Grenzen ausgerichtet sind. Außerdem müssen alle Erstellungs Daten, die einer Steuerelement Definition folgen, an einer **DWORD** -Grenze ausgerichtet werden. Alle anderen Arrays variabler Länge in einer Dialogfeld Vorlage müssen an **Wort** Grenzen ausgerichtet werden.

### <a name="template-header"></a>Vorlagen Header

In den Dialogfeldern Standard und erweiterte Vorlagen für enthält der-Header die folgenden allgemeinen Informationen:

-   Die Position und die Dimensionen des Dialog Felds.
-   Die Fenster-und Dialogfeld Stile für das Dialogfeld.
-   Die Anzahl der Steuerelemente im Dialogfeld. Dieser Wert bestimmt die Anzahl der [**DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) -oder [**dlgitemtemplateex**](dlgitemtemplateex.md) -Steuerelement Definitionen in der Vorlage.
-   Eine optionale Menü Ressource für das Dialogfeld. Die Vorlage kann anzeigen, dass das Dialogfeld nicht über ein Menü verfügt, oder es kann einen Ordinalwert oder eine auf NULL endenden Unicode-Zeichenfolge angeben, die eine Menü Ressource in einer ausführbaren Datei identifiziert.
-   Die Fenster Klasse des Dialog Felds. Dies kann entweder die vordefinierte Dialogfeld Klasse oder ein Ordinalwert oder eine auf NULL endende Unicode-Zeichenfolge sein, die eine registrierte Fenster Klasse identifiziert.
-   Eine NULL-terminierte Unicode-Zeichenfolge, die den Titel für das Dialogfeld Fenster angibt. Wenn die Zeichenfolge leer ist, ist die Titelleiste des Dialog Felds leer. Wenn das Dialogfeld nicht über den **WS- \_ Beschriftungs** Stil verfügt, wird der Titel vom System auf die angegebene Zeichenfolge festgelegt, jedoch nicht angezeigt.
-   Wenn das Dialogfeld den **DS- \_ setFont** -Stil hat, gibt der Header die Punktgröße und den Schriftart Namen der Schriftart an, die für den Text im Client Bereich und die Steuerelemente des Dialog Felds verwendet werden soll.

In einer erweiterten Vorlage gibt der [**dlgtemplateex**](dlgtemplateex.md) -Header auch die folgenden zusätzlichen Informationen an:

-   Der Hilfe Kontext Bezeichner des Dialogfeld Fensters, wenn das System eine [**WM- \_ Hilfe**](../shell/wm-help.md) Meldung sendet.
-   Wenn das Dialogfeld den **DS- \_ setFont** -oder **DS- \_ shellfont** -Stil hat, gibt der Header die Schrift Breite an und gibt an, ob die Schriftart kursiv formatiert ist.

### <a name="control-definitions"></a>Steuerelement Definitionen

Nach dem Vorlagen Header handelt es sich um eine oder mehrere Steuerelement Definitionen, die die Steuerelemente des Dialog Felds beschreiben. In den Vorlagen Standard und erweitert verfügt der Dialogfeld Header über einen Member, der die Anzahl der Steuerelement Definitionen in der Vorlage angibt. In einer Standardvorlage besteht jede Steuerelement Definition aus einer [**DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) -Struktur, gefolgt von zusätzlichen Arrays variabler Länge. In einer erweiterten Vorlage verwenden die Steuerelement Definitionen das [**dlgitemtemplateex**](dlgitemtemplateex.md) -Format.

In den Vorlagen Standard und erweitert enthält die Steuerelement Definition die folgenden Informationen:

-   Die Position und die Dimensionen des Steuer Elements.
-   Die Fenster-und Steuerelement Stile für das Steuerelement.
-   Der Steuerelement Bezeichner.
-   Die Fenster Klasse des Steuer Elements. Dies kann entweder der Ordinalwert einer vordefinierten System Klasse oder eine auf NULL endende Unicode-Zeichenfolge sein, die den Namen einer registrierten Fenster Klasse angibt.
-   Eine NULL terminierte Unicode-Zeichenfolge, die den ursprünglichen Text des Steuer Elements angibt, oder einen Ordinalwert, der eine Ressource (z. b. ein Symbol) in einer ausführbaren Datei identifiziert.
-   Ein optionaler Block der Erstellungs Daten mit variabler Länge. Wenn das System das Steuerelement erstellt, übergibt es einen Zeiger auf diese Daten im *LPARAM* -Parameter der [**WM \_ Create**](/windows/desktop/winmsg/wm-create) -Nachricht, die an das Steuerelement gesendet wird.

In einer erweiterten Vorlage gibt die Steuerelement Definition auch einen Hilfe Kontext Bezeichner für das Steuerelement an, wenn das System eine [**WM- \_ Hilfe**](../shell/wm-help.md) Nachricht sendet.

 

 