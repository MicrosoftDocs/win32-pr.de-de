---
title: Informationen zu Tastatur Accelerators
description: In diesem Thema werden die Tastaturbeschleuniger erläutert.
ms.assetid: cbf7619d-289d-40c9-9a06-6ce47026d43f
keywords:
- Windows-Benutzeroberfläche, Benutzereingabe
- Windows-Benutzeroberfläche, Tastaturbeschleuniger
- Benutzereingabe, Tastaturbeschleuniger
- Erfassen von Benutzereingaben, Tastatur Accelerators
- Tastaturbeschleuniger
- Accelerators
- WM_COMMAND Meldung
- WM_SYS Befehls Meldung
- Zugriffstasten Tabellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be9c89301f58d7d76b5d9b28dd6835850c0674db
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948623"
---
# <a name="about-keyboard-accelerators"></a>Informationen zu Tastatur Accelerators

Zugriffstasten sind eng mit Menüs verwandt – beide ermöglichen dem Benutzer den Zugriff auf den Befehlssatz einer Anwendung. In der Regel greifen Benutzer auf die Menüs einer Anwendung zu, um den Befehlssatz zu erlernen und dann zur Verwendung von Accelerators zu wechseln, wenn Sie mit der Anwendung besser vertraut werden. Accelerators bieten schnelleren, direkteren Zugriff auf Befehle als Menüs. Eine Anwendung sollte für die gängigsten Befehle mindestens Zugriffstasten bereitstellen. Obwohl Accelerators in der Regel Befehle generieren, die als Menü Elemente vorhanden sind, können Sie auch Befehle generieren, die keine entsprechenden Menü Elemente aufweisen.

In diesem Abschnitt werden die folgenden Themen behandelt.

-   [Zugriffstasten Tabellen](#accelerator-tables)
-   [Erstellung von Zugriffstasten Tabellen](#accelerator-table-creation)
-   [Tastenkombinationen für Tastenkombinationen](#accelerator-keystroke-assignments)
-   [Accelerators und Menüs](#accelerators-and-menus)
-   [UI-Status](#ui-state)

## <a name="accelerator-tables"></a>Zugriffstasten Tabellen

Eine Zugriffstasten Tabelle besteht aus einem Array von [**Accel**](/windows/win32/api/winuser/ns-winuser-accel) -Strukturen, die jeweils eine einzelne Zugriffstaste definieren. Jede **Accel** -Struktur enthält die folgenden Informationen:

-   Die Tastenkombination der Tastenkombination.
-   Der-Bezeichner der Zugriffstaste.
-   Verschiedene Flags. Dies schließt einen Wert ein, der angibt, ob das System visuelles Feedback bereitstellen soll, indem das entsprechende Menü Element (sofern vorhanden) hervorgehoben wird, wenn die Zugriffstaste verwendet wird.

Der Entwickler muss die [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) -Funktion in der Nachrichten Schleife, die der Meldungs Warteschlange des Threads zugeordnet ist, aufruft, um Zugriffstasten Kombinationen für einen angegebenen Thread verarbeiten zu können. Die **TranslateAccelerator** -Funktion überwacht Tastatureingaben in der Nachrichten Warteschlange und überprüft die Tastenkombinationen, die einem Eintrag in der Zugriffstasten Tabelle entsprechen. Wenn **TranslateAccelerator** eine Entsprechung findet, übersetzt Sie die Tastatureingabe (d. h. die [**WM \_ KeyUp**](/windows/desktop/inputdev/wm-keyup) -und die [**WM \_ KeyDown**](/windows/desktop/inputdev/wm-keydown) -Nachricht) in einen [**WM- \_ Befehl**](wm-command.md) oder eine [**WM- \_ syscommand**](wm-syscommand.md) -Nachricht und sendet die Nachricht dann an die Fenster Prozedur des angegebenen Fensters. Die folgende Abbildung zeigt, wie Acceleratoren verarbeitet werden.

![Tastaturbeschleuniger-Verarbeitungsmodell](images/cskac-01.png)

Die [**WM- \_ Befehls**](wm-command.md) Meldung enthält den Bezeichner der Zugriffstaste, der bewirkt hat, dass [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) die Nachricht generiert hat. Die Fenster Prozedur überprüft den Bezeichner, um die Quelle der Nachricht zu bestimmen, und verarbeitet die Nachricht dann entsprechend.

Zugriffstasten Tabellen sind auf zwei unterschiedlichen Ebenen vorhanden. Das System verwaltet eine einzelne, systemweite Zugriffstasten Tabelle, die für alle Anwendungen gilt. Eine Anwendung kann die System Zugriffs Tabelle nicht ändern. Eine Beschreibung der von der System Zugriffs Tabelle bereitgestellten Accelerators finden Sie unter [Tastenkombinationen für Tastenkombinationen](#accelerator-keystroke-assignments).

Das System verwaltet auch Zugriffstasten Tabellen für jede Anwendung. Eine Anwendung kann eine beliebige Anzahl von Zugriffstasten Tabellen für die Verwendung mit ihren eigenen Fenstern definieren. Jede Tabelle wird durch ein eindeutiges 32-Bit-Handle (**haccel**) identifiziert. Allerdings kann jeweils nur eine Zugriffstasten Tabelle für einen bestimmten Thread aktiv sein. Das Handle für die Zugriffstasten Tabelle, das an die [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) -Funktion übergebenen wird, bestimmt, welche Zugriffstasten Tabelle für einen Thread aktiv ist. Die aktive Zugriffstasten Tabelle kann jederzeit geändert werden, indem ein anderes Zugriffstasten-Tabellen Handle an **TranslateAccelerator** übergeben wird.

## <a name="accelerator-table-creation"></a>Accelerator-Table Erstellung

Zum Erstellen einer Zugriffstasten Tabelle für eine Anwendung sind mehrere Schritte erforderlich. Zuerst wird ein Ressourcen Compiler verwendet, um Ressourcen für die Zugriffstasten Tabelle zu erstellen und Sie der ausführbaren Datei der Anwendung hinzuzufügen. Zur Laufzeit wird die [**loadaccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) -Funktion verwendet, um die Zugriffstasten Tabelle in den Arbeitsspeicher zu laden und das Handle für die Zugriffstasten Tabelle abzurufen. Dieses Handle wird an die [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) -Funktion übermittelt, um die Zugriffstasten Tabelle zu aktivieren.

Eine Zugriffstasten Tabelle kann auch zur Laufzeit für eine Anwendung erstellt werden, indem ein Array von [**Accel**](/windows/win32/api/winuser/ns-winuser-accel) -Strukturen an die Funktion " [**comateacceleratortable**](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea) " übergeben wird. Diese Methode unterstützt benutzerdefinierte Acceleratoren in der Anwendung. Wie die [**loadaccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) -Funktion gibt " **kreateacceleratortable** " ein Zugriffstasten-Tabellen Handle zurück, das an [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) übergeben werden kann, um die Zugriffstasten Tabelle zu aktivieren.

Das System zerstört schnell Zugriffs Tabellen, die von [**loadaccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) geladen oder von " [**kreateacceleratortable**](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea)" erstellt wurden. Eine Anwendung kann jedoch Ressourcen freigeben, während Sie ausgeführt wird, indem Sie die Zugriffstasten Tabellen zerstören, die durch Aufrufen der [**DestroyAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-destroyacceleratortable) -Funktion nicht mehr benötigt werden.

Eine vorhandene Zugriffstasten Tabelle kann kopiert und geändert werden. Die vorhandene Zugriffstasten Tabelle wird mithilfe der [**copyacceleratortable**](/windows/desktop/api/Winuser/nf-winuser-copyacceleratortablea) -Funktion kopiert. Nachdem die Kopie geändert wurde, wird ein Handle für die neue Zugriffstasten Tabelle durch Aufrufen von [**CreateAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea)abgerufen. Schließlich wird das Handle an [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) übermittelt, um die neue Tabelle zu aktivieren.

## <a name="accelerator-keystroke-assignments"></a>Tastenkombinationen für Tastenkombinationen

Zum Definieren der Zugriffstaste kann ein ASCII-Zeichencode oder ein Code mit virtuellen Schlüsseln verwendet werden. Bei einem ASCII-Zeichencode wird die Groß-/Kleinschreibung beachtet. Daher definiert die Verwendung des ASCII-Zeichens "C" die Zugriffstaste als alt + c anstelle von alt + c. Allerdings kann es verwirrend sein, die Groß-/Kleinschreibung zu verwenden. Beispielsweise wird die Taste Alt + C generiert, wenn die Feststell Taste gedrückt ist, oder wenn die UMSCHALTTASTE gedrückt ist, aber nicht, wenn beide ausfallen.

In der Regel müssen Accelerators nicht zwischen Groß-und Kleinschreibung unterschieden, sodass die meisten Anwendungen anstelle von ASCII-Zeichen Codes virtuelle Schlüsselcodes für Acceleratoren verwenden.

Vermeiden Sie Acceleratoren, die in Konflikt mit dem Menü "mnetmonics" einer Anwendung stehen, da die Zugriffstaste den mnetmonischen überschreibt, der den Benutzer verwirren kann. Weitere Informationen zu Menü-mnetmonics finden Sie unter [Menüs](menus.md).

Wenn eine Anwendung eine Zugriffstaste definiert, die auch in der System Zugriffs Tabelle definiert ist, überschreibt die von der Anwendung definierte Zugriffstaste den System Beschleuniger, jedoch nur innerhalb des Kontexts der Anwendung. Vermeiden Sie diese Vorgehensweise, da dadurch verhindert wird, dass der System Beschleuniger seine Standard Rolle in der Benutzeroberfläche ausführt. Die systemweiten Acceleratoren werden in der folgenden Liste beschrieben:



|                  |                                                                                                       |
|------------------|-------------------------------------------------------------------------------------------------------|
| ALT+ESC          | Wechselt zur nächsten Anwendung.                                                                     |
| ALT+F4           | Schließt eine Anwendung oder ein Fenster.                                                                    |
| ALT+BINDESTRICH       | Öffnet das **Fenster** Menü für ein Dokument Fenster.                                                      |
| Bildschirm Alt + Druck | Kopiert ein Bild im aktiven Fenster in die Zwischenablage.                                              |
| ALT+LEERTASTE     | Öffnet das **Fenster** Menü für das Hauptfenster der Anwendung.                                          |
| ALT+TAB          | Wechselt zur nächsten Anwendung.                                                                     |
| STRG+ESC         | Wechselt zum **Startmenü** .                                                                       |
| STRG+F4          | Schließt das aktive Gruppen-oder Dokument Fenster.                                                           |
| F1               | Startet die Hilfedatei der Anwendung, sofern vorhanden.                                                    |
| Bildschirm drucken     | Kopiert ein Bild auf dem Bildschirm in die Zwischenablage.                                                     |
| Umschalt + Alt + Tab    | Schaltet zur vorherigen Anwendung um. Der Benutzer muss beim Drücken der Tab-Taste ALT + UMSCHALT gedrückt halten. |



 

## <a name="accelerators-and-menus"></a>Accelerators und Menüs

Die Verwendung einer Zugriffstaste ist dasselbe wie das Auswählen eines Menü Elements: beide Aktionen bewirken, dass das System einen [**WM- \_ Befehl**](wm-command.md) oder eine [**WM- \_ syscommand**](wm-syscommand.md) -Nachricht an die entsprechende Fenster Prozedur sendet. Die **WM- \_ Befehls** Meldung enthält einen Bezeichner, den die Fenster Prozedur prüft, um die Quelle der Nachricht zu bestimmen. Wenn eine Zugriffstaste die **WM- \_ Befehls** Meldung generiert hat, ist der Bezeichner der der Zugriffstaste. Ebenso gilt: Wenn ein Menü Element die **WM- \_ Befehls** Meldung generiert hat, ist der Bezeichner der des Menü Elements. Da eine Zugriffstaste eine Verknüpfung zum Auswählen eines Befehls in einem Menü bereitstellt, weist eine Anwendung der Zugriffstaste und dem entsprechenden Menü Element normalerweise denselben Bezeichner zu.

Eine Anwendung verarbeitet eine schnell Info- [**WM- \_ Befehls**](wm-command.md) Nachricht genauso wie die entsprechende Menü Element- **WM- \_ Befehls** Meldung. Die WM- **\_ Befehls** Meldung enthält jedoch ein Flag, das angibt, ob die Nachricht von einer Zugriffstaste oder einem Menü Element stammt, wenn Accelerators anders als die entsprechenden Menü Elemente verarbeitet werden müssen. Die [**WM- \_ syscommand**](wm-syscommand.md) -Nachricht enthält dieses Flag nicht.

Der Bezeichner bestimmt, ob eine Zugriffstaste einen [**WM- \_ Befehl**](wm-command.md) oder eine [**WM- \_ syscommand**](wm-syscommand.md) -Nachricht generiert. Wenn der Bezeichner denselben Wert hat wie ein Menü Element im System Menü, generiert die Zugriffstaste eine **WM- \_ syscommand** -Nachricht. Andernfalls generiert die Zugriffstaste eine **WM- \_ Befehls** Meldung.

Wenn eine Zugriffstaste denselben Bezeichner wie ein Menü Element aufweist und das Menü Element ausgegraut oder deaktiviert ist, wird die Zugriffstaste deaktiviert, und es wird keine [**WM- \_ Befehls**](wm-command.md) -oder [**WM- \_ syscommand**](wm-syscommand.md) -Nachricht generiert. Außerdem generiert eine Zugriffstaste keine Befehls Meldung, wenn das entsprechende Fenster minimiert wird.

Wenn der Benutzer eine Zugriffstaste verwendet, die einem Menü Element entspricht, empfängt die Fenster Prozedur die Meldungen " [**WM \_ InitMenu**](wm-initmenu.md) " und " [**WM \_ initmenupopup**](wm-initmenupopup.md) ", als ob der Benutzer das Menü Element ausgewählt hätte. Weitere Informationen zum Verarbeiten dieser Nachrichten finden Sie unter [Menüs](menus.md).

Eine Zugriffstaste, die einem Menü Element entspricht, sollte in den Text des Menü Elements eingeschlossen werden.

## <a name="ui-state"></a>UI-Status

Mithilfe von Windows können Anwendungen verschiedene Features in der Benutzeroberfläche ausblenden oder anzeigen. Diese Einstellungen werden als Benutzeroberflächen Status bezeichnet. Der Status der Benutzeroberfläche umfasst die folgenden Einstellungen:

-   Fokus Indikatoren (z. b. Fokus Rechtecke auf Schaltflächen)
-   Tastaturbeschleuniger (durch Unterstriche in Steuerelement Bezeichnungen angegeben)

Ein Fenster kann Nachrichten senden, um eine Änderung im Status der Benutzeroberfläche anzufordern, den UI-Zustand abzufragen oder einen bestimmten Zustand für seine untergeordneten Fenster zu erzwingen. Diese Meldungen lauten wie folgt.



| `Message`                                       | BESCHREIBUNG                                |
|-----------------------------------------------|--------------------------------------------|
| [**WM \_ changeuistate**](wm-changeuistate.md) | Gibt an, dass sich der Benutzeroberflächen Zustand ändern soll. |
| [**WM \_ queryuistate**](wm-queryuistate.md)   | Ruft den Benutzeroberflächen Zustand für ein Fenster ab.       |
| [**WM \_ updateuistate**](wm-updateuistate.md) | Ändert den Benutzeroberflächen Zustand.                      |



 

Standardmäßig werden alle untergeordneten Fenster eines Fensters der obersten Ebene mit dem gleichen Benutzeroberflächen Zustand wie das übergeordnete Fenster erstellt.

Das System verarbeitet den UI-Zustand für Steuerelemente in Dialogfeldern. Bei der Erstellung des Dialog Felds initialisiert das System den Benutzeroberflächen Zustand entsprechend. Alle untergeordneten Steuerelemente erben diesen Zustand. Nachdem das Dialogfeld erstellt wurde, überwacht das System die Tastatureingaben des Benutzers. Wenn die Einstellungen für den Benutzeroberflächen Zustand ausgeblendet sind und der Benutzer über die Tastatur navigiert, aktualisiert das System den UI-Zustand. Wenn der Benutzer z. b. die Tab-Taste drückt, um den Fokus auf das nächste Steuerelement zu verschieben, ruft das System [**WM \_ changeuistate**](wm-changeuistate.md) auf, um die Fokus Indikatoren sichtbar zu machen. Wenn der Benutzer die Alt-Taste drückt, ruft das System **WM \_ changeuistate** auf, um die Tastaturbeschleuniger sichtbar zu machen.

Wenn ein Steuerelement die Navigation zwischen den darin enthaltenen Benutzeroberflächen Elementen unterstützt, kann es seinen eigenen Benutzeroberflächen Zustand aktualisieren. Das Steuerelement kann [**WM \_ queryuistate**](wm-queryuistate.md) aufrufen, um den anfänglichen UI-Status abzurufen und zwischenzuspeichern. Wenn das Steuerelement eine " [**WM \_ updateuistate**](wm-updateuistate.md) "-Meldung empfängt, kann es seinen Benutzeroberflächen Zustand aktualisieren und eine " [**WM \_ changeuistate**](wm-changeuistate.md) "-Meldung an das übergeordnete Element senden. Jedes Fenster sendet die Nachricht weiterhin an das übergeordnete Element, bis das Fenster der obersten Ebene erreicht wird. Das Fenster der obersten Ebene sendet die **WM- \_ updateuistate** -Meldung an die Fenster in der Fenster Struktur. Wenn ein Fenster die **WM \_ changeuistate** -Nachricht nicht übergibt, wird das Fenster der obersten Ebene nicht erreicht, und der Benutzeroberflächen Zustand wird nicht aktualisiert.

 

 