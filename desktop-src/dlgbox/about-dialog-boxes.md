---
title: Dialogfelder "Info"
description: In diesem Thema wird die Verwendung von Dialogfeldern zum Erstellen von Benutzeroberflächen für Anwendungen erläutert.
ms.assetid: 51960c28-a178-4ad3-b45e-426fec42a945
keywords:
- Dialogfelder, Informationen
- Dialogfelder, wann sie verwendet werden sollen
- Modale Dialogfelder
- Nicht modale Dialogfelder
- Dialogfelder, modal
- Dialogfelder, moduslos
- Dialogfelder, Vorlagen
- Dialogfelder, Besitzerfenster
- Dialogfelder, Meldungsfelder
- Dialogfeldprozesen
- Meldungsfelder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7855ba67a04558e0df8ffad0f63d2bd78856f84829bf029fbf811a4b89eb4b09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118786808"
---
# <a name="about-dialog-boxes"></a>Dialogfelder "Info"

Es gibt viele Funktionen, Meldungen und vordefinierte Steuerelemente zum Erstellen und Verwalten von Dialogfeldern, sodass die Entwicklung der Benutzeroberfläche für eine Anwendung vereinfacht wird. In dieser Übersicht werden die Dialogfeldfunktionen und -meldungen sowie deren Verwendung zum Erstellen und Verwenden von Dialogfeldern beschrieben.

Diese Übersicht enthält die folgenden Themen:

-   [Wann sollte ein Dialogfeld verwendet werden?](#when-to-use-a-dialog-box)
-   [Dialogfeld "Besitzer"](#dialog-box-owner-window)
-   [Meldungsfelder](#message-boxes)
-   [Modale Dialogfelder](#modal-dialog-boxes)
-   [Dialogfelder ohne Modus](#modeless-dialog-boxes)
-   [Dialogfeldvorlagen](#dialog-box-templates)
    -   [Dialogfeldvorlagenstile](#dialog-box-template-styles)
    -   [Dialogfeldmessungen](#dialog-box-measurements)
    -   [Dialogfeldsteuerelemente](#dialog-box-controls)
    -   [Menü "Dialogfeldfenster"](#dialog-box-window-menu)
    -   [Dialogfeldschriftarten](#dialog-box-fonts)
    -   [Vorlagen im Arbeitsspeicher](#templates-in-memory)

Weitere Informationen zu den allgemeinen Dialogfeldern finden Sie unter [Allgemeine Dialogfeldbibliothek.](common-dialog-box-library.md)

## <a name="when-to-use-a-dialog-box"></a>Wann sollte ein Dialogfeld verwendet werden?

Die meisten Anwendungen verwenden Dialogfelder, um zusätzliche Informationen für Menüelemente einzugeben, die Benutzereingaben erfordern. Die Verwendung eines Dialogfelds ist die einzige empfohlene Methode zum Abrufen der Eingabe durch eine Anwendung. Für ein typisches **Menüelement Öffnen** muss beispielsweise der Name einer Datei geöffnet werden. Daher sollte eine Anwendung ein Dialogfeld verwenden, um den Benutzer zur Eingabe des Namens aufzufordern. In solchen Fällen erstellt die Anwendung das Dialogfeld, wenn der Benutzer auf das Menüelement klickt und das Dialogfeld sofort zerstört, nachdem der Benutzer die Informationen bereitgestellt hat.

Viele Anwendungen verwenden auch Dialogfelder, um Informationen oder Optionen anzuzeigen, während der Benutzer in einem anderen Fenster arbeitet. Beispielsweise verwenden Anwendungen für die Textverarbeitung häufig ein Dialogfeld mit einer Textsucheoption. Während die Anwendung nach dem Text sucht, bleibt das Dialogfeld auf dem Bildschirm. Der Benutzer kann dann zum Dialogfeld zurückkehren und erneut nach demselben Wort suchen. oder der Benutzer kann den Eintrag im Dialogfeld ändern und nach einem neuen Wort suchen. Anwendungen, die auf diese Weise Dialogfelder verwenden, erstellen in der Regel ein Dialogfeld, wenn der Benutzer auf das Menüelement klickt und es weiterhin anzeigt, solange die Anwendung ausgeführt wird oder bis der Benutzer das Dialogfeld explizit schließt.

Um die verschiedenen Arten der Verwendung von Dialogfeldern durch Anwendungen zu unterstützen, gibt es zwei Arten von Dialogfeldern: modal und moduslos. Für *ein modales Dialogfeld* muss der Benutzer Informationen bereitstellen oder das Dialogfeld abbrechen, bevor die Anwendung fortgesetzt werden kann. Anwendungen verwenden modale Dialogfelder in Verbindung mit Menüelementen, die zusätzliche Informationen erfordern, bevor sie fortfahren können. Mit einem *moduslosen Dialogfeld* kann der Benutzer Informationen bereitstellen und zur vorherigen Aufgabe zurückkehren, ohne das Dialogfeld zu schließen. Modale Dialogfelder sind einfacher zu verwalten als moduslose Dialogfelder, da sie erstellt, ihre Aufgabe ausführen und durch Aufrufen einer einzelnen Funktion zerstört werden.

Um ein modales oder ein modusloses Dialogfeld zu erstellen, muss eine Anwendung eine Dialogfeldvorlage bereitstellen, um das Dialogfeldformat und den Inhalt zu beschreiben. Die Anwendung muss auch eine Dialogfeldprozedur zum Ausführen von Aufgaben bereitstellen. Die *Dialogfeldvorlage* ist eine binäre Beschreibung des Dialogfelds und der darin enthaltenen Steuerelemente. Der Entwickler kann diese Vorlage als Ressource erstellen, die aus der ausführbaren Datei der Anwendung geladen oder während der Ausführung der Anwendung im Arbeitsspeicher erstellt werden soll. Die *Dialogfeldprozedur* ist eine anwendungsdefinierte Rückruffunktion, die das System aufruft, wenn sie über Eingaben für das Dialogfeld oder Aufgaben für das auszuführende Dialogfeld verfügt. Obwohl eine Dialogfeldprozedur einer Fensterprozedur ähnelt, hat sie nicht die gleichen Zuständigkeiten.

Eine Anwendung erstellt in der Regel ein Dialogfeld mithilfe der [**DialogBox-**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) oder [**CreateDialog-Funktion.**](/windows/desktop/api/Winuser/nf-winuser-createdialoga) **DialogBox** erstellt ein modales Dialogfeld. **CreateDialog** erstellt ein dialogfeld ohne Modus. Diese beiden Funktionen laden eine Dialogfeldvorlage aus der ausführbaren Datei der Anwendung und erstellen ein Popupfenster, das den Spezifikationen der Vorlage entspricht. Es gibt andere Funktionen, die ein Dialogfeld mithilfe von Vorlagen im Arbeitsspeicher erstellen. sie übergeben zusätzliche Informationen an die Dialogfeldprozedur, während das Dialogfeld erstellt wird.

Dialogfelder gehören in der Regel zu einer vordefinierten, exklusiven Fensterklasse. Das System verwendet diese Fensterklasse und die entsprechende Fensterprozedur sowohl für modale als auch für moduslose Dialogfelder. Wenn die Funktion aufgerufen wird, erstellt sie das Fenster für das Dialogfeld sowie die Fenster für die Steuerelemente im Dialogfeld und sendet dann ausgewählte Meldungen an die Dialogfeldprozedur. Während das Dialogfeld angezeigt wird, verwaltet die vordefinierte Fensterprozedur alle Nachrichten, verarbeitet einige Nachrichten und übergibt andere an die Dialogfeldprozedur, damit die Prozedur Aufgaben ausführen kann. Anwendungen haben keinen direkten Zugriff auf die vordefinierte Fensterklasse oder Fensterprozedur, können jedoch die Dialogfeldvorlage und die Dialogfeldprozedur verwenden, um den Stil und das Verhalten eines Dialogfelds zu ändern.

## <a name="dialog-box-owner-window"></a>Dialogfeld "Besitzer"

Die meisten Dialogfelder verfügen über ein Besitzerfenster (oder einfach einen Besitzer). Beim Erstellen des Dialogfelds legt die Anwendung den Besitzer fest, indem das Fensterhandle des Besitzers angegeben wird. Das System verwendet den Besitzer, um die Position des Dialogfelds in der Z-Reihenfolge zu bestimmen, sodass das Dialogfeld immer über seinem Besitzer positioniert wird. Außerdem kann das System Nachrichten an die Fensterprozedur des Besitzers senden und ihn über Ereignisse im Dialogfeld benachrichtigen.

Das System blendet das Dialogfeld automatisch aus oder zerstört es, wenn sein Besitzer ausgeblendet oder zerstört wird. Dies bedeutet, dass die Dialogfeldprozedur keine besondere Verarbeitung erfordert, um Änderungen am Status des Besitzerfensters zu erkennen.

Da das typische Dialogfeld in Verbindung mit einem Menüelement verwendet wird, ist das Besitzerfenster in der Regel das Fenster, das das Menü enthält. Obwohl es möglich ist, ein Dialogfeld ohne Besitzer zu erstellen, wird dies nicht empfohlen. Wenn z. B. ein modales Dialogfeld keinen Besitzer hat, deaktiviert das System keines der anderen Fenster der Anwendung und ermöglicht es dem Benutzer, weiterhin Arbeit in den anderen Fenstern auszuführen, wodurch der Zweck des modalen Dialogfelds unterlaufen wird.

Wenn ein modusloses Dialogfeld keinen Besitzer hat, blendet das System das Dialogfeld weder aus noch zerstört es, wenn andere Fenster in der Anwendung ausgeblendet oder zerstört werden. Obwohl dies den Zweck des moduslosen Dialogfelds nicht vereiteelt, erfordert es, dass die Anwendung eine spezielle Verarbeitung durchführt, um sicherzustellen, dass das Dialogfeld zu geeigneten Zeiten ausgeblendet und zerstört wird.

## <a name="message-boxes"></a>Meldungsfelder

Ein Meldungsfeld ist ein spezielles Dialogfeld, mit dem eine Anwendung Nachrichten anzeigen und zur eingabeaufforderung auffordern kann. Ein Meldungsfeld enthält in der Regel eine Textnachricht und mindestens eine Schaltfläche. Eine Anwendung erstellt das Meldungsfeld mithilfe der [**MessageBox-**](/windows/desktop/api/Winuser/nf-winuser-messagebox) oder [**MessageBoxEx-Funktion**](/windows/desktop/api/Winuser/nf-winuser-messageboxexa) und gibt den Text und die Anzahl und die Typen der anzuzeigenden Schaltflächen an. Beachten Sie, dass es derzeit keinen Unterschied zwischen der Funktionsweise von **MessageBox** und **MessageBoxEx** gibt.

Obwohl das Meldungsfeld ein Dialogfeld ist, übernimmt das System die vollständige Kontrolle über die Erstellung und Verwaltung des Meldungsfelds. Dies bedeutet, dass die Anwendung keine Dialogfeldvorlage und keine Dialogfeldprozedur bereitstellt. Das System erstellt eine eigene Vorlage basierend auf dem Text und den Schaltflächen, die für das Meldungsfeld angegeben sind, und stellt eine eigene Dialogfeldprozedur zur Verfügung.

Ein Meldungsfeld ist ein modales Dialogfeld, das vom System mit den gleichen internen Funktionen erstellt wird, die [**DialogBox**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) verwendet. Wenn die Anwendung beim Aufrufen von [**MessageBox**](/windows/desktop/api/Winuser/nf-winuser-messagebox) oder [**MessageBoxEx**](/windows/desktop/api/Winuser/nf-winuser-messageboxexa)ein Besitzerfenster angibt, deaktiviert das System den Besitzer. Eine Anwendung kann das System auch anweisen, alle Fenster der obersten Ebene zu deaktivieren, die zum aktuellen Thread gehören, indem der **MB \_ TASKMODAL-Wert** beim Erstellen des Dialogfelds angegeben wird.

Das System kann Nachrichten wie [**WM \_ CANCELMODE**](/windows/desktop/winmsg/wm-cancelmode) und [**WM \_ ENABLE**](/windows/desktop/winmsg/wm-enable)wie beim Erstellen eines modalen Dialogfelds an den Besitzer senden. Im Besitzerfenster sollten alle aktionen ausgeführt werden, die von diesen Nachrichten angefordert werden.

## <a name="modal-dialog-boxes"></a>Modale Dialogfelder

Ein modales Dialogfeld sollte ein Popupfenster mit einem Fenstermenü, einer Titelleiste und einem dichten Rahmen sein. Das heißt, die Dialogfeldvorlage sollte die **Stile WS \_ POPUP,** **WS \_ SYSMENU,** **WS \_ CAPTION** und **DS \_ MODALFRAME** angeben. Obwohl eine Anwendung den **WS \_ VISIBLE-Stil** festlegen kann, zeigt das System immer ein modales Dialogfeld an, unabhängig davon, ob die Dialogfeldvorlage den **WS \_ VISIBLE-Stil** angibt. Eine Anwendung darf kein modales Dialogfeld mit dem **WS \_ CHILD-Stil** erstellen. Ein modales Dialogfeld mit diesem Stil deaktiviert sich selbst und verhindert, dass nachfolgende Eingaben die Anwendung erreichen.

Eine Anwendung erstellt ein modales Dialogfeld mithilfe der [**DialogBox-**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) oder [**DialogBoxIndirect-Funktion.**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta) **DialogBox** erfordert den Namen oder Bezeichner einer Ressource, die eine Dialogfeldvorlage enthält. **DialogBoxIndirect** erfordert ein Handle für ein Speicherobjekt, das eine Dialogfeldvorlage enthält. Die Funktionen [**DialogBoxParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxparama) und [**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama) erstellen auch modale Dialogfelder. sie sind mit den zuvor erwähnten Funktionen identisch, übergeben jedoch einen angegebenen Parameter an die Dialogfeldprozedur, wenn das Dialogfeld erstellt wird.

Beim Erstellen des modalen Dialogfelds macht das System es zum aktiven Fenster. Das Dialogfeld bleibt aktiv, bis die Dialogfeldprozedur die [**EndDialog-Funktion**](/windows/desktop/api/Winuser/nf-winuser-enddialog) aufruft oder das System ein Fenster in einer anderen Anwendung aktiviert. Weder der Benutzer noch die Anwendung können das Besitzerfenster aktivieren, bis das modale Dialogfeld zerstört wird.

Wenn das Besitzerfenster noch nicht deaktiviert ist, deaktiviert das System automatisch das Fenster und alle untergeordneten Fenster, die zu ihm gehören, wenn das modale Dialogfeld erstellt wird. Das Besitzerfenster bleibt deaktiviert, bis das Dialogfeld zerstört wird. Obwohl das Besitzerfenster durch eine Dialogfeldprozedur jederzeit aktiviert werden kann, wird der Zweck des modalen Dialogfelds durch das Aktivieren des Besitzers nicht mehr erfüllt. Dies wird jedoch nicht empfohlen. Wenn die Dialogfeldprozedur zerstört wird, aktiviert das System das Besitzerfenster erneut, jedoch nur, wenn das modale Dialogfeld dazu geführt hat, dass der Besitzer deaktiviert wurde.

Wenn das System das modale Dialogfeld erstellt, sendet es die [**WM \_ CANCELMODE-Meldung**](/windows/desktop/winmsg/wm-cancelmode) an das Fenster (sofern vorhanden), das derzeit Mauseingaben erfasst. Eine Anwendung, die diese Meldung empfängt, sollte die Mauserfassung freigeben, damit der Benutzer die Maus im modalen Dialogfeld bewegen kann. Da das System das Besitzerfenster deaktiviert, gehen alle Mauseingaben verloren, wenn der Besitzer die Maus beim Empfang dieser Nachricht nicht loslasst.

Um Nachrichten für das modale Dialogfeld zu verarbeiten, startet das System eine eigene Nachrichtenschleife und übernimmt die temporäre Kontrolle über die Nachrichtenwarteschlange für die gesamte Anwendung. Wenn das System eine Nachricht abruft, die nicht explizit für das Dialogfeld gilt, wird die Nachricht an das entsprechende Fenster gesendet. Wenn eine [**WM \_ QUIT-Nachricht**](/windows/desktop/winmsg/wm-quit) abgerufen wird, wird die Nachricht zurück an die Anwendungsnachrichtenwarteschlange gesendet, damit die Hauptnachrichtenschleife der Anwendung die Nachricht schließlich abrufen kann.

Das System sendet die [**WM \_ ENTERIDLE-Nachricht**](wm-enteridle.md) an das Besitzerfenster, wenn die Anwendungsnachrichtenwarteschlange leer ist. Die Anwendung kann diese Meldung verwenden, um eine Hintergrundaufgabe auszuführen, während das Dialogfeld auf dem Bildschirm verbleibt. Wenn eine Anwendung die Nachricht auf diese Weise verwendet, muss die Anwendung häufig die Steuerung (z. B. mithilfe der [**PeekMessage-Funktion)**](/windows/desktop/api/winuser/nf-winuser-peekmessagea) übergeben, damit das modale Dialogfeld beliebige Benutzereingaben empfangen kann. Um zu verhindern, dass das modale Dialogfeld die **WM \_ ENTERIDLE-Nachrichten** sendet, kann die Anwendung beim Erstellen des Dialogfelds den DS \_ NOIDLEMSG-Stil angeben.

Eine Anwendung zerstört ein modales Dialogfeld mithilfe der [**EndDialog-Funktion.**](/windows/desktop/api/Winuser/nf-winuser-enddialog) In den meisten Fällen ruft die Dialogfeldprozedur **EndDialog** auf, wenn der Benutzer im  Fenstermenü des **Dialogfelds** auf Schließen klickt oder im Dialogfeld auf die Schaltfläche **OK** oder Abbrechen klickt. Das Dialogfeld kann einen Wert über die [**DialogBox-Funktion**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) (oder andere Erstellungsfunktionen) zurückgeben, indem beim Aufrufen der **EndDialog-Funktion** ein Wert angegeben wird. Das System gibt diesen Wert zurück, nachdem das Dialogfeld zerstört wurde. Die meisten Anwendungen verwenden diesen Rückgabewert, um zu bestimmen, ob das Dialogfeld seine Aufgabe erfolgreich abgeschlossen hat oder vom Benutzer abgebrochen wurde. Das System gibt die Steuerung nicht von der Funktion zurück, die das Dialogfeld erstellt, bis die Prozedur des Dialogfelds die **EndDialog-Funktion aufgerufen** hat.

## <a name="modeless-dialog-boxes"></a>Dialogfelder ohne Modus

Ein nicht modusloses Dialogfeld sollte ein Popupfenster mit einem Fenstermenü, einer Titelleiste und einem schlanken Rahmen sein. Das heißt, die Dialogfeldvorlage sollte die **Formate WS \_ POPUP,** **WS \_ CAPTION,** **WS \_ BORDER** und **WS \_ SYSMENU** angeben. Das Dialogfeld wird nicht automatisch angezeigt, es sei denn, die Vorlage gibt den **WS \_ VISIBLE-Stil** an.

Eine Anwendung erstellt ein nicht modusloses Dialogfeld mithilfe der [**Funktion CreateDialog**](/windows/desktop/api/Winuser/nf-winuser-createdialoga) oder [**CreateDialogIndirect.**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirecta) **CreateDialog** erfordert den Namen oder Bezeichner einer Ressource, die eine Dialogfeldvorlage enthält. **CreateDialogIndirect erfordert** ein Handle für ein Speicherobjekt, das eine Dialogfeldvorlage enthält. Zwei weitere Funktionen, [**CreateDialogParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogparama) und [**CreateDialogIndirectParam,**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama)erstellen ebenfalls moduslose Dialogfelder. Sie übergeben einen angegebenen Parameter an die Dialogfeldprozedur, wenn das Dialogfeld erstellt wird.

[**CreateDialog und**](/windows/desktop/api/Winuser/nf-winuser-createdialoga) andere Erstellungsfunktionen geben ein Fensterhand handle an das Dialogfeld zurück. Die Anwendung und die Dialogfeldprozedur können dieses Handle verwenden, um das Dialogfeld zu verwalten. Wenn beispielsweise **WS \_ VISIBLE** nicht in der Dialogfeldvorlage angegeben ist, kann die Anwendung das Dialogfeld anzeigen, indem das Fensterhand handle an die [**ShowWindow-Funktion übergeben**](/windows/desktop/api/winuser/nf-winuser-showwindow) wird.

Ein nicht modusloses Dialogfeld deaktiviert weder das Besitzerfenster noch sendet Nachrichten an dieses. Beim Erstellen des Dialogfelds macht das System es zum aktiven Fenster, aber der Benutzer oder die Anwendung kann das aktive Fenster jederzeit ändern. Wenn das Dialogfeld inaktiv wird, bleibt es über dem Besitzerfenster in der Z-Reihenfolge, auch wenn das Besitzerfenster aktiv ist.

Die Anwendung ist für das Abrufen und Senden von Eingabenachrichten an das Dialogfeld verantwortlich. Die meisten Anwendungen verwenden dafür die Hauptnachrichtenschleife. Damit der Benutzer mithilfe der Tastatur zu Steuerelementen wechseln und diese auswählen kann, muss die Anwendung jedoch die [**IsDialogMessage-Funktion**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) aufrufen. Weitere Informationen zu dieser Funktion finden Sie unter [Dialogfeldtastaturschnittstelle](dlgbox-programming-considerations.md).

Ein modusloses Dialogfeld kann keinen Wert wie ein modales Dialogfeld an die Anwendung zurückgeben, aber die Dialogfeldprozedur kann mithilfe der [**SendMessage-Funktion**](/windows/desktop/api/winuser/nf-winuser-sendmessage) Informationen an das Besitzerfenster senden.

Eine Anwendung muss vor dem Beenden alle nicht moduslosen Dialogfelder zerstören. Sie kann ein nicht modusloses Dialogfeld mithilfe der [**DestroyWindow-Funktion**](/windows/desktop/api/winuser/nf-winuser-destroywindow) zerstören. In den meisten Fällen ruft die Dialogfeldprozedur **DestroyWindow** als Reaktion auf Benutzereingaben auf, z. B. durch Klicken auf die **Schaltfläche Abbrechen.** Wenn der Benutzer das Dialogfeld nie auf diese Weise schließt, muss die Anwendung **DestroyWindow aufrufen.**

[**DestroyWindow macht**](/windows/desktop/api/winuser/nf-winuser-destroywindow) das Fensterhand handle für das Dialogfeld ungültig, sodass alle nachfolgenden Aufrufe von Funktionen, die das Handle verwenden, Fehlerwerte zurückgeben. Um Fehler zu vermeiden, sollte die Dialogfeldprozedur den Besitzer benachrichtigen, dass das Dialogfeld zerstört wurde. Viele Anwendungen verwalten eine globale Variable, die das Handle für das Dialogfeld enthält. Wenn die Dialogfeldprozedur das Dialogfeld zerstört, wird auch die globale Variable auf **NULL** festgelegt, was angibt, dass das Dialogfeld nicht mehr gültig ist.

Die Dialogfeldprozedur darf die [**EndDialog-Funktion**](/windows/desktop/api/Winuser/nf-winuser-enddialog) nicht aufrufen, um ein nicht modusloses Dialogfeld zu zerstören.

## <a name="dialog-box-templates"></a>Dialogfeldvorlagen

Bei einer Dialogfeldvorlage handelt es sich um Binärdaten, die das Dialogfeld beschreiben und dessen Höhe, Breite, Format und die in ihm enthaltenen Steuerelemente definieren. Um ein Dialogfeld zu erstellen, lädt das System entweder eine Dialogfeldvorlage aus den Ressourcen in der ausführbaren Datei der Anwendung oder verwendet die Vorlage, die von der Anwendung im globalen Arbeitsspeicher übergeben wird. In beiden Fällen muss die Anwendung beim Erstellen eines Dialogfelds eine Vorlage enthalten.

Ein Entwickler erstellt Vorlagenressourcen mithilfe eines Ressourcencompilers oder eines Dialogfeld-Editors. Ein Ressourcencompiler konvertiert eine Textbeschreibung in eine binäre Ressource, und ein Dialogfeld-Editor speichert ein interaktiv konstruiertes Dialogfeld als binäre Ressource.

> [!Note]  
> Eine Erläuterung, wie Vorlagenressourcen erstellt und der ausführbaren Datei der Anwendung hinzugefügt werden, wird in dieser Übersicht nicht erläutert. Weitere Informationen zum Erstellen von Vorlagenressourcen und zum Hinzufügen zu einer ausführbaren Datei finden Sie in der Dokumentation zu Ihren Anwendungsentwicklungstools.

 

Um ein Dialogfeld ohne Vorlagenressourcen zu erstellen, müssen Sie eine Vorlage im Arbeitsspeicher erstellen und an die [**Funktion CreateDialogIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama) oder [**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama) oder an das [**Makro CreateDialogIndirect**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirecta) oder [**DialogBoxIndirect**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta) übergeben.

Eine Dialogfeldvorlage im Arbeitsspeicher besteht aus einem Header, der das Dialogfeld beschreibt, gefolgt von einem oder mehreren zusätzlichen Datenblöcken, die jedes der Steuerelemente im Dialogfeld beschreiben. Die Vorlage kann entweder das Standardformat oder das erweiterte Format verwenden. In einer Standardvorlage ist der Header eine [**DLGTEMPLATE-Struktur,**](/windows/desktop/api/Winuser/ns-winuser-dlgtemplate) gefolgt von zusätzlichen Arrays variabler Länge. und die Daten für jedes Steuerelement bestehen aus einer [**DLGITEMTEMPLATE-Struktur**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) gefolgt von zusätzlichen Arrays variabler Länge. In einer erweiterten Dialogfeldvorlage verwendet der Header das [**DLGTEMPLATEEX-Format,**](dlgtemplateex.md) und die Steuerelementdefinitionen verwenden das [**DLGITEMTEMPLATEEX-Format.**](dlgitemtemplateex.md)

Sie können eine Speichervorlage erstellen, indem Sie ein globales Speicherobjekt zuordnen und es mit den Standard- oder erweiterten Header- und Steuerelementdefinitionen füllen. Eine Speichervorlage ist in Form und Inhalt mit einer Vorlagenressource identisch. Viele Anwendungen, die Speichervorlagen verwenden, verwenden zuerst die [**LoadResource-Funktion,**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadresource) um eine Vorlagenressource in den Arbeitsspeicher zu laden, und ändern dann die geladene Ressource, um eine neue Speichervorlage zu erstellen. Weitere Informationen zum Erstellen einer Dialogfeldvorlage im Arbeitsspeicher finden Sie unter [Vorlagen im Arbeitsspeicher.](#templates-in-memory)

In den folgenden Abschnitten werden die Stile, Messungen und andere Werte beschrieben, die in einer Dialogfeldvorlage verwendet werden.

-   [Dialogfeldvorlagenstile](#dialog-box-template-styles)
-   [Dialogfeldmessungen](#dialog-box-measurements)
-   [Dialogfeld-Steuerelemente](#dialog-box-controls)
-   [Dialogfeldfenstermenü](#dialog-box-window-menu)
-   [Dialogfeldschriftarten](#dialog-box-fonts)
-   [Vorlagen im Arbeitsspeicher](#templates-in-memory)

### <a name="dialog-box-template-styles"></a>Dialogfeldvorlagenstile

Jede Dialogfeldvorlage gibt eine Kombination von Formatwerten an, die die Darstellung und die Features des Dialogfelds definieren. Die Stilwerte können Fensterstile sein, z. B. **WS \_ POPUP** und **WS \_ SYSMENU,** und Dialogfeldstile, z. B. **DS \_ MODALFRAME**. Die Anzahl und der Typ der Stile für eine Vorlage hängen vom Typ und Zweck des Dialogfelds ab. Eine Liste der Werte finden Sie unter [**Dialogfeldformatvorlagen.**](dialog-box-styles.md)

Das System übergibt beim Erstellen des Dialogfelds alle in der Vorlage angegebenen Fensterstile an die [**CreateWindowEx-Funktion.**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) Das System kann je nach den angegebenen Dialogfeldstilen einen oder mehrere erweiterte Stile übergeben. Wenn die Vorlage beispielsweise **DS \_ MODALFRAME** angibt, verwendet das System **WS \_ EX \_ DLGMODALFRAME** beim Erstellen des Dialogfelds.

Die meisten Dialogfelder sind Popupfenster, die über ein Fenstermenü und eine Titelleiste verfügen. Daher gibt die typische Vorlage die **Formate WS \_ POPUP,** **WS \_ SYSMENU** und **WS \_ CAPTION** an. Die Vorlage gibt auch einen Rahmenstil an: **WS \_ BORDER** für moduslose Dialogfelder und **DS \_ MODALFRAME** für modale Dialogfelder. Eine Vorlage kann einen anderen Fenstertyp als das Popupfenster (z. B. **WS \_ OVERLAPPED)** angeben, wenn ein benutzerdefiniertes Fenster anstelle eines Dialogfelds erstellt wird.

Das System zeigt immer ein modales Dialogfeld an, unabhängig davon, ob **der WS \_ VISIBLE-Stil** angegeben ist. Wenn die Vorlage für ein nicht modusloses Dialogfeld den **WS \_ VISIBLE-Stil** angibt, zeigt das System das Dialogfeld automatisch an, wenn es erstellt wird. Andernfalls ist die Anwendung dafür verantwortlich, das Dialogfeld mithilfe der [**ShowWindow-Funktion**](/windows/desktop/api/winuser/nf-winuser-showwindow) anzuzeigen.

### <a name="dialog-box-measurements"></a>Dialogfeldmessungen

Jede Dialogfeldvorlage enthält Messungen, die die Position, Breite und Höhe des Dialogfelds und der in ihm enthaltenen Steuerelemente angeben. Diese Messungen sind geräteunabhängig, sodass eine Anwendung eine einzelne Vorlage verwenden kann, um dasselbe Dialogfeld für alle Arten von Anzeigegeräten zu erstellen. Dadurch wird sichergestellt, dass ein Dialogfeld trotz unterschiedlicher Auflösungen und Seitenverhältnisse auf allen Bildschirmen die gleichen Proportionen und Darstellungen hat.

Die Messungen in einer Dialogfeldvorlage werden in Dialogvorlageneinheiten angegeben. Um Messungen von Dialogvorlageneinheiten in Bildschirmeinheiten (Pixel) zu konvertieren, verwenden Sie die [**MapDialogRect-Funktion,**](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect) die die vom Dialogfeld verwendete Schriftart berücksichtigt und ein Rechteck aus Dialogvorlageneinheiten ordnungsgemäß in Pixel konvertiert. Für Dialogfelder, die die Systemschriftart verwenden, können Sie die [**GetDialogBaseUnits-Funktion**](/windows/desktop/api/Winuser/nf-winuser-getdialogbaseunits) verwenden, um die Konvertierungsberechnungen selbst durchzuführen, obwohl die Verwendung von **MapDialogRect** einfacher ist.

Die Vorlage muss die Anfangskoordinaten der oberen linken Ecke des Dialogfelds angeben. Normalerweise sind die Koordinaten relativ zur oberen linken Ecke des Clientbereichs des Besitzerfensters. Wenn die Vorlage den DS ABSALIGN-Stil angibt oder das Dialogfeld keinen Besitzer hat, ist die Position relativ zur oberen \_ linken Ecke des Bildschirms. Das System legt diese Anfangsposition beim Erstellen des Dialogfelds fest, erlaubt einer Anwendung jedoch, die Position vor dem Anzeigen des Dialogfelds anzupassen. Beispielsweise kann eine Anwendung die Dimensionen des Besitzerfensters abrufen, eine neue Position berechnen, die das Dialogfeld im Besitzerfenster centert, und dann die Position mithilfe der [**SetWindowPos-Funktion**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) festlegen.

Die Vorlage sollte eine Breite und Höhe des Dialogfelds angeben, die die Breite und Höhe des Bildschirms nicht überschreitet, und stellt sicher, dass sich alle Steuerelemente innerhalb des Clientbereichs des Dialogfelds befinden. Das System lässt zwar zu, dass ein Dialogfeld eine beliebige Größe hat, aber das Erstellen eines zu kleinen oder zu großen Dialogfelds kann verhindern, dass der Benutzer Eingaben liefert, wodurch der Zweck des Dialogfelds nicht erfüllt wird. Viele Anwendungen verwenden mehrere Dialogfelder, wenn eine große Anzahl von Steuerelementen verfügbar ist. In solchen Fällen enthält das erste Dialogfeld in der Regel eine oder mehrere Schaltflächen, die der Benutzer auswählen kann, um das nächste Dialogfeld anzuzeigen.

### <a name="dialog-box-controls"></a>Dialogfeld-Steuerelemente

Die Vorlage gibt position, width, height, style, identifier und window class für jedes Steuerelement im Dialogfeld an. Das System erstellt jedes Steuerelement, indem diese Daten an die [**CreateWindowEx-Funktion übergeben**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) werden. Steuerelemente werden in der Reihenfolge erstellt, in der sie in der Vorlage angegeben sind. Die Vorlage sollte die entsprechende Anzahl, den Typ und die Reihenfolge der Steuerelemente angeben, um sicherzustellen, dass der Benutzer die Eingabe eingeben kann, die zum Abschließen der dem Dialogfeld zugeordneten Aufgabe erforderlich ist.

Für jedes Steuerelement gibt die Vorlage Stilwerte an, die die Darstellung und den Betrieb des Steuerelements definieren. Jedes Steuerelement ist ein untergeordnetes Fenster und muss daher über den **WS \_ CHILD-Stil** verfügen. Um sicherzustellen, dass das Steuerelement sichtbar ist, wenn das Dialogfeld angezeigt wird, muss jedes Steuerelement auch den **WS \_ VISIBLE-Stil** aufweisen. Andere häufig verwendete Fensterstile sind **WS \_ BORDER** für Steuerelemente mit optionalen Rahmen, **WS \_ DISABLED** für Steuerelemente, die beim ersten Erstellen des Dialogfelds deaktiviert werden sollen, und **WS \_ TABSTOP** und **WS \_ GROUP** für Steuerelemente, auf die über die Tastatur zugegriffen werden kann. Die **Stile WS \_ TABSTOP** und **WS \_ GROUP** werden in Verbindung mit der Tastaturoberfläche des Dialogfelds verwendet, die weiter unten in diesem Thema beschrieben wird.

Die Vorlage kann auch Steuerelementstile angeben, die für die Fensterklasse des Steuerelements spezifisch sind. Beispielsweise muss eine Vorlage, die ein Schaltflächensteuerelement angibt, ein Schaltflächen-Steuerelementformat wie **BS \_ PUSHBUTTON** oder **BS \_ CHECKBOX** angeben. Das System übergibt die Steuerelementstile über die [**WM \_ CREATE-Meldung**](/windows/desktop/winmsg/wm-create) an die Steuerelementfensterprozedur, sodass die Prozedur die Darstellung und den Betrieb des Steuerelements anpassen kann.

Das System konvertiert die Positionskoordinaten und die Messung der Breite und Höhe von Dialogbasiseinheiten in Pixel, bevor diese an [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)übergeben werden. Wenn das System ein Steuerelement erstellt, gibt es das Dialogfeld als übergeordnetes Fenster an. Dies bedeutet, dass das System die Positionskoordinaten des Steuerelements immer als Clientkoordinaten interpretiert, relativ zur oberen linken Ecke des Clientbereichs des Dialogfelds.

Die Vorlage gibt die Fensterklasse für jedes Steuerelement an. Ein typisches Dialogfeld enthält Steuerelemente, die zu den vordefinierten Steuerelementfensterklassen gehören, z. B. die Schaltflächen- und Bearbeitungssteuerelementfensterklassen. In diesem Fall gibt die Vorlage Fensterklassen an, indem sie die entsprechenden vordefinierten Atomwerte für die Klassen angibt. Wenn ein Dialogfeld ein Steuerelement enthält, das zu einer benutzerdefinierten Steuerelementfensterklasse gehört, gibt die Vorlage den Namen dieser registrierten Fensterklasse oder den Atomwert an, der dem Namen derzeit zugeordnet ist.

Jedes Steuerelement in einem Dialogfeld muss über einen eindeutigen Bezeichner verfügen, um es von anderen Steuerelementen zu unterscheiden. Steuerelemente senden Informationen über [**WM \_ COMMAND-Meldungen**](/windows/desktop/menurc/wm-command) an die Dialogfeldprozedur, sodass die Steuerelementbezeichner für die Prozedur wichtig sind, um zu bestimmen, welches Steuerelement eine angegebene Nachricht gesendet hat. Die einzige Ausnahme von dieser Regel sind Steuerelementbezeichner für statische Steuerelemente. Statische Steuerelemente erfordern keine eindeutigen Bezeichner, da sie keine **WM \_ COMMAND-Nachrichten** senden.

Damit der Benutzer das Dialogfeld schließen kann, sollte die Vorlage mindestens eine Pushschaltfläche angeben und ihm den Steuerelementbezeichner **IDCANCEL** geben. Damit der Benutzer zwischen dem Abschließen oder Abbrechen des dem Dialogfeld zugeordneten Tasks wählen kann, sollte die Vorlage zwei Schaltflächen mit den Bezeichnungen **OK** und **Abbrechen** mit den Steuerelementbezeichnern **IDOK** bzw. **IDCANCEL** angeben.

Eine Vorlage gibt auch optionale Text- und Erstellungsdaten für ein Steuerelement an. Der Text stellt in der Regel Bezeichnungen für Schaltflächensteuerelemente bereit oder gibt den ursprünglichen Inhalt eines statischen Textsteuerelements an. Bei den Erstellungsdaten handelt es sich um ein oder mehrere Bytes von Daten, die das System beim Erstellen des Steuerelements an die Prozedur des Steuerelementfensters übergibt. Die Erstellung von Daten ist nützlich für Steuerelemente, die mehr Informationen über ihren ursprünglichen Inhalt oder Stil benötigen, als von anderen Daten angegeben werden. Beispielsweise kann eine Anwendung Erstellungsdaten verwenden, um die Anfangseinstellung und den Bereich für ein Bildlaufleisten-Steuerelement festzulegen.

### <a name="dialog-box-window-menu"></a>Menü "Dialogfeldfenster"

Das System gibt einem Dialogfeld ein Fenstermenü, wenn die Vorlage den **\_ WS-SYSMENU-Stil** angibt. Um ungeeignete Eingaben zu verhindern, deaktiviert das System automatisch alle Elemente im Menü mit Ausnahme **von Verschieben** und **Schließen.** Der Benutzer kann auf **Verschieben** klicken, um das Dialogfeld zu verschieben. Wenn der Benutzer auf **Schließen** klickt, sendet das System eine [**WM \_ COMMAND-Meldung**](/windows/desktop/menurc/wm-command) an die Dialogfeldprozedur, wobei der *wParam-Parameter* auf **IDCANCEL** festgelegt ist. Dies ist identisch mit der Nachricht, die von der Schaltfläche **Abbrechen** gesendet wird, wenn der Benutzer darauf klickt. Die empfohlene Aktion für diese Meldung besteht darin, das Dialogfeld zu schließen und die angeforderte Aufgabe abzubrechen.

Obwohl andere Menüs in Dialogfeldern nicht empfohlen werden, kann eine Dialogfeldvorlage ein Menü angeben, indem der Bezeichner oder der Name einer Menüressource angegeben wird. In diesem Fall lädt das System die Ressource und erstellt das Menü für das Dialogfeld. Anwendungen verwenden in der Regel Menübezeichner oder Namen in Vorlagen, wenn sie die Vorlagen verwenden, um benutzerdefinierte Fenster anstelle von Dialogfeldern zu erstellen.

### <a name="dialog-box-fonts"></a>Dialogfeldschriftarten

Das System verwendet die durchschnittliche Zeichenbreite der Schriftart des Dialogfelds, um die Position und Abmessungen des Dialogfelds zu berechnen. Standardmäßig zeichnet das System den gesamten Text in einem Dialogfeld mithilfe der Schriftart **SYSTEM \_ FONT.**

Um eine Schriftart für ein anderes Dialogfeld als die Standardeinstellung anzugeben, müssen Sie das Dialogfeld mithilfe einer Dialogfeldvorlage erstellen. Verwenden Sie in einer Vorlagenressource die [FONT-Anweisung](../menurc/font-statement.md). Legen Sie in einer Dialogfeldvorlage den **DS \_ SETFONT-** oder **DS \_ SHELLFONT-Stil** fest, und geben Sie eine Punktgröße und einen Schriftartnamen an. Auch wenn eine Dialogfeldvorlage auf diese Weise eine Schriftart angibt, verwendet das System immer die Systemschriftart für den Dialogfeldtitel und die Dialogfeldmenüs.

Wenn das Dialogfeld über den **DS \_ SETFONT-** oder **DS \_ SHELLFONT-Stil** verfügt, sendet das System eine [**WM \_ SETFONT-Meldung**](/windows/desktop/winmsg/wm-setfont) an die Dialogfeldprozedur und an jedes Steuerelement, während es das Steuerelement erstellt. Die Dialogfeldprozedur ist dafür verantwortlich, das mit der **WM \_ SETFONT-Meldung** übergebene Schriftarthandle zu speichern und das Handle beim Schreiben von Text in das Fenster in den Anzeigegerätekontext auszuwählen. Vordefinierte Steuerelemente tun dies standardmäßig.

Die Systemschriftart kann zwischen verschiedenen Versionen von Windows variieren. Damit Ihre Anwendung die Systemschriftart unabhängig davon verwendet, auf welchem System sie ausgeführt wird, verwenden Sie **DS \_ SHELLFONT** mit der Schriftart MS Shell Dlg, und verwenden Sie die [DIALOGEX-Ressource](../menurc/dialogex-resource.md) anstelle der [DIALOG-Ressource](../menurc/dialog-resource.md). Das System ordnet diese Schriftart so zu, dass das Dialogfeld die Schriftart Tahoma verwendet. Beachten Sie, dass **DS \_ SHELLFONT** keine Auswirkungen hat, wenn die Schriftart nicht MS Shell Dlg ist.

### <a name="templates-in-memory"></a>Vorlagen im Arbeitsspeicher

Eine Dialogfeldvorlage im Arbeitsspeicher besteht aus einem Header, der das Dialogfeld beschreibt, gefolgt von einem oder mehreren zusätzlichen Datenblöcken, die jedes der Steuerelemente im Dialogfeld beschreiben. Die Vorlage kann entweder das Standardformat oder das erweiterte Format verwenden. In einer Standardvorlage ist der Header eine [**DLGTEMPLATE-Struktur,**](/windows/desktop/api/Winuser/ns-winuser-dlgtemplate) gefolgt von zusätzlichen Arrays variabler Länge. Die Daten für jedes Steuerelement bestehen aus einer [**DLGITEMTEMPLATE-Struktur,**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) gefolgt von zusätzlichen Arrays variabler Länge. In einer vorlage für erweiterte Dialogfelder verwendet der Header das [**DLGTEMPLATEEX-Format,**](dlgtemplateex.md) und die Steuerelementdefinitionen verwenden das [**DLGITEMTEMPLATEEX-Format.**](dlgitemtemplateex.md)

Um zwischen einer Standardvorlage und einer erweiterten Vorlage zu unterscheiden, überprüfen Sie die ersten 16 Bits einer Dialogfeldvorlage. In einer erweiterten Vorlage wird das erste **WORD** 0xFFFF. Jeder andere Wert gibt eine Standardvorlage an.

Wenn Sie eine Dialogvorlage im Arbeitsspeicher erstellen, müssen Sie sicherstellen, dass die einzelnen [**DLGITEMTEMPLATE-**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) oder [**DLGITEMTEMPLATEEX-Steuerelementdefinitionen**](dlgitemtemplateex.md) an **DWORD-Grenzen** ausgerichtet sind. Darüber hinaus müssen alle Erstellungsdaten, die einer Steuerelementdefinition folgen, an einer **DWORD-Grenze** ausgerichtet werden. Alle anderen Arrays variabler Länge in einer Dialogfeldvorlage müssen an **WORD-Grenzen** ausgerichtet sein.

### <a name="template-header"></a>Vorlagenheader

Sowohl in den Standardvorlagen als auch in erweiterten Vorlagen für Dialogfelder enthält der Header die folgenden allgemeinen Informationen:

-   Position und Dimensionen des Dialogfelds
-   Die Fenster- und Dialogfeldstile für das Dialogfeld
-   Die Anzahl der Steuerelemente im Dialogfeld. Dieser Wert bestimmt die Anzahl der [**DLGITEMTEMPLATE-**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) oder [**DLGITEMTEMPLATEEX-Steuerelementdefinitionen**](dlgitemtemplateex.md) in der Vorlage.
-   Eine optionale Menüressource für das Dialogfeld. Die Vorlage kann angeben, dass das Dialogfeld kein Menü enthält, oder sie kann einen Ordinalwert oder eine auf NULL endende Unicode-Zeichenfolge angeben, die eine Menüressource in einer ausführbaren Datei identifiziert.
-   Die Fensterklasse des Dialogfelds. Dies kann entweder die vordefinierte Dialogfeldklasse oder ein Ordinalwert oder eine auf NULL endende Unicode-Zeichenfolge sein, die eine registrierte Fensterklasse identifiziert.
-   Eine mit NULL endende Unicode-Zeichenfolge, die den Titel für das Dialogfeldfenster angibt. Wenn die Zeichenfolge leer ist, ist die Titelleiste des Dialogfelds leer. Wenn das Dialogfeld nicht über den **WS \_ CAPTION-Stil** verfügt, legt das System den Titel auf die angegebene Zeichenfolge fest, zeigt ihn jedoch nicht an.
-   Wenn das Dialogfeld über den **DS \_ SETFONT-Stil** verfügt, gibt der Header die Punktgröße und den Schriftartnamen der Schriftart an, die für den Text im Clientbereich und steuerelemente des Dialogfelds verwendet werden sollen.

In einer erweiterten Vorlage gibt der [**DLGTEMPLATEEX-Header**](dlgtemplateex.md) auch die folgenden zusätzlichen Informationen an:

-   Der Hilfekontextbezeichner des Dialogfeldfensters, wenn das System eine [**\_ WM-HILFE-Nachricht**](../shell/wm-help.md) sendet.
-   Wenn das Dialogfeld über den **DS \_ SETFONT-** oder **DS \_ SHELLFONT-Stil** verfügt, gibt der Header die Schriftbreite an und gibt an, ob die Schriftart italisch ist.

### <a name="control-definitions"></a>Steuerelementdefinitionen

Dem Vorlagenheader folgt mindestens eine Steuerelementdefinition, die die Steuerelemente des Dialogfelds beschreibt. Sowohl in der Standard- als auch in der erweiterten Vorlage verfügt der Dialogfeldheader über einen Member, der die Anzahl der Steuerelementdefinitionen in der Vorlage angibt. In einer Standardvorlage besteht jede Steuerelementdefinition aus einer [**DLGITEMTEMPLATE-Struktur**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) gefolgt von zusätzlichen Arrays variabler Länge. In einer erweiterten Vorlage verwenden die Steuerelementdefinitionen das [**DLGITEMTEMPLATEEX-Format.**](dlgitemtemplateex.md)

Sowohl in den Standardvorlagen als auch in den erweiterten Vorlagen enthält die Steuerelementdefinition die folgenden Informationen:

-   Die Position und Dimensionen des Steuerelements.
-   Die Fenster- und Steuerelementstile für das Steuerelement.
-   Der Steuerelementbezeichner.
-   Die Fensterklasse des Steuerelements. Dies kann entweder der Ordnungswert einer vordefinierten Systemklasse oder eine mit NULL endende Unicode-Zeichenfolge sein, die den Namen einer registrierten Fensterklasse angibt.
-   Eine mit NULL endende Unicode-Zeichenfolge, die den ursprünglichen Text des Steuerelements angibt, oder ein Ordinalwert, der eine Ressource, z. B. ein Symbol, in einer ausführbaren Datei identifiziert.
-   Ein optionaler Block der Erstellungsdaten variabler Länge. Wenn das System das Steuerelement erstellt, übergibt es einen Zeiger auf diese Daten im *lParam-Parameter* der [**WM \_ CREATE-Nachricht,**](/windows/desktop/winmsg/wm-create) die es an das Steuerelement sendet.

In einer erweiterten Vorlage gibt die Steuerelementdefinition auch einen Hilfekontextbezeichner für das Steuerelement an, wenn das System eine [**WM \_ HELP-Nachricht**](../shell/wm-help.md) sendet.

 

 