---
title: Informationen zu Tastenkombinationen
description: In diesem Thema werden Tastenkombinationen erläutert.
ms.assetid: cbf7619d-289d-40c9-9a06-6ce47026d43f
keywords:
- Windows Benutzeroberfläche,Benutzereingabe
- Windows Benutzeroberfläche,Tastenkombinationen
- Benutzereingabe,Tastenkombinationen
- Erfassen von Benutzereingaben, Tastenkombinationen
- Tastenkombinationen
- Beschleuniger
- WM_COMMAND-Nachricht
- WM_SYS COMMAND-Meldung
- Zugriffstastentabellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88e97f0b4997d15d55601e571270276e7d7a3bd4
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120375"
---
# <a name="about-keyboard-accelerators"></a>Informationen zu Tastenkombinationen

Zugriffstasten sind eng mit Menüs verknüpft– beide ermöglichen dem Benutzer den Zugriff auf den Befehlssatz einer Anwendung. In der Regel verlassen sich Benutzer auf die Menüs einer Anwendung, um den Befehlssatz zu erlernen, und wechseln dann zur Verwendung von Zugriffstasten, wenn sie mit der Anwendung vertrauter werden. Zugriffstasten ermöglichen einen schnelleren, direkteren Zugriff auf Befehle als Menüs. Eine Anwendung sollte mindestens Zugriffstasten für die häufiger verwendeten Befehle bereitstellen. Obwohl Zugriffstasten in der Regel Befehle generieren, die als Menüelemente vorhanden sind, können sie auch Befehle generieren, die keine entsprechenden Menüelemente haben.

In diesem Abschnitt werden die folgenden Themen behandelt.

-   [Zugriffstastentabellen](#accelerator-tables)
-   [Accelerator-Table-Erstellung](#accelerator-table-creation)
-   [Tastenkombinationszuweisungen](#accelerator-keystroke-assignments)
-   [Zugriffstasten und Menüs](#accelerators-and-menus)
-   [Benutzeroberflächenzustand](#ui-state)

## <a name="accelerator-tables"></a>Zugriffstastentabellen

Eine Zugriffstastentabelle besteht aus einem Array von [**ACCEL-Strukturen,**](/windows/win32/api/winuser/ns-winuser-accel) die jeweils einen einzelnen Accelerator definieren. Jede **ACCEL-Struktur** enthält die folgenden Informationen:

-   Die Tastenkombination des Accelerators.
-   Der Bezeichner der Zugriffstaste.
-   Verschiedene Flags. Dies schließt einen Wert ein, der angibt, ob das System visuelles Feedback bereitstellen soll, indem das entsprechende Menüelement hervorgehoben wird( falls verfügbar), wenn die Zugriffstaste verwendet wird.

Um Zugriffstasteneingaben für einen angegebenen Thread zu verarbeiten, muss der Entwickler die [**TranslateAccelerator-Funktion**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) in der Meldungsschleife aufrufen, die der Nachrichtenwarteschlange des Threads zugeordnet ist. Die **TranslateAccelerator-Funktion** überwacht Tastatureingaben in die Nachrichtenwarteschlange und prüft auf Tastenkombinationen, die mit einem Eintrag in der Zugriffstastentabelle übereinstimmen. Wenn **TranslateAccelerator** eine Übereinstimmung findet, übersetzt er die Tastatureingabe (d. h. die [**WM \_ KEYUP-**](/windows/desktop/inputdev/wm-keyup) und [**WM \_ KEYDOWN-Meldungen)**](/windows/desktop/inputdev/wm-keydown) in eine [**WM \_ COMMAND-**](wm-command.md) oder [**WM \_ SYSCOMMAND-Nachricht**](wm-syscommand.md) und sendet die Nachricht dann an die Fensterprozedur des angegebenen Fensters. Die folgende Abbildung zeigt, wie Zugriffstasten verarbeitet werden.

![Verarbeitungsmodell für die Tastaturbeschleunigung](images/cskac-01.png)

Die [**WM \_ COMMAND-Meldung**](wm-command.md) enthält den Bezeichner der Zugriffstaste, die dazu führte, dass [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) die Nachricht generiert hat. Die Fensterprozedur untersucht den Bezeichner, um die Quelle der Nachricht zu bestimmen, und verarbeitet die Nachricht dann entsprechend.

Zugriffstastentabellen sind auf zwei verschiedenen Ebenen vorhanden. Das System verwaltet eine einzelne, systemweite Zugriffstastentabelle, die für alle Anwendungen gilt. Eine Anwendung kann die Systembeschleunigungstabelle nicht ändern. Eine Beschreibung der Zugriffstasten, die von der Systembeschleunigungstabelle bereitgestellt werden, finden Sie unter [Tastenkombinationszuweisungen](#accelerator-keystroke-assignments).

Das System verwaltet auch Zugriffstastentabellen für jede Anwendung. Eine Anwendung kann eine beliebige Anzahl von Zugriffstastentabellen für die Verwendung mit eigenen Fenstern definieren. Jede Tabelle wird durch ein eindeutiges 32-Bit-Handle (**HACCEL**) identifiziert. Für einen angegebenen Thread kann jedoch immer nur eine Zugriffstastentabelle gleichzeitig aktiv sein. Das Handle für die Zugriffstastentabelle, die an die [**TranslateAccelerator-Funktion**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) übergeben wird, bestimmt, welche Zugriffstastentabelle für einen Thread aktiv ist. Die Aktive Zugriffstastentabelle kann jederzeit geändert werden, indem ein anderes Handle für die Zugriffstastentabelle an **TranslateAccelerator übergeben wird.**

## <a name="accelerator-table-creation"></a>Accelerator-Table Erstellung

Zum Erstellen einer Zugriffstastentabelle für eine Anwendung sind mehrere Schritte erforderlich. Zunächst wird ein Ressourcencompiler verwendet, um Accelerator-Table-Ressourcen zu erstellen und der ausführbaren Datei der Anwendung hinzuzufügen. Zur Laufzeit wird die [**LoadAccelerators-Funktion**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) verwendet, um die Zugriffstastentabelle in den Arbeitsspeicher zu laden und das Handle für die Zugriffstastentabelle abzurufen. Dieses Handle wird an die [**TranslateAccelerator-Funktion übergeben,**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) um die Zugriffstastentabelle zu aktivieren.

Eine Zugriffstastentabelle kann auch zur Laufzeit für eine Anwendung erstellt werden, indem ein Array von [**ACCEL-Strukturen**](/windows/win32/api/winuser/ns-winuser-accel) an die [**CreateAcceleratorTable-Funktion übergeben**](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea) wird. Diese Methode unterstützt benutzerdefinierte Zugriffstasten in der Anwendung. Wie die [**LoadAccelerators-Funktion**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) gibt **CreateAcceleratorTable** ein Accelerator-Table-Handle zurück, das an [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) übergeben werden kann, um die Zugriffstastentabelle zu aktivieren.

Das System zerstört automatisch Zugriffstastentabellen, die von [**LoadAccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) geladen oder von [**CreateAcceleratorTable erstellt wurden.**](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea) Eine Anwendung kann jedoch Ressourcen während der Ausführung frei geben, indem accelerator-Tabellen zerstört werden, die nicht mehr benötigt werden, indem die [**DestroyAcceleratorTable-Funktion aufruft.**](/windows/desktop/api/Winuser/nf-winuser-destroyacceleratortable)

Eine vorhandene Zugriffstastentabelle kann kopiert und geändert werden. Die vorhandene Zugriffstastentabelle wird mithilfe der [**CopyAcceleratorTable-Funktion**](/windows/desktop/api/Winuser/nf-winuser-copyacceleratortablea) kopiert. Nachdem die Kopie geändert wurde, wird ein Handle für die neue Zugriffstastentabelle abgerufen, indem [**CreateAcceleratorTable aufgerufen wird.**](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea) Schließlich wird das Handle an [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) übergeben, um die neue Tabelle zu aktivieren.

## <a name="accelerator-keystroke-assignments"></a>Tastenkombinationszuweisungen

Ein ASCII-Zeichencode oder ein virtueller Schlüsselcode kann verwendet werden, um die Zugriffstaste zu definieren. Bei einem ASCII-Zeichencode wird die Schreibung der Zugriffstaste beachtet. Daher definiert die Verwendung des ASCII-Zeichens "C" den Beschleuniger als ALT+C anstelle von ALT+C. Die Verwendung von Zugriffstasten, bei der die Schreibung der Schreibung beachtet wird, kann jedoch verwirrend sein. Beispielsweise wird der ALT+C-Beschleuniger generiert, wenn die CAPS LOCK-Taste heruntergefahren ist oder die UMSCHALTTASTE aus ist, aber nicht, wenn beide nicht mehr gedrückt sind.

In der Regel muss bei Zugriffstasten die Kleinschreibung nicht beachtet werden, sodass die meisten Anwendungen Codes mit virtuellen Schlüsseln anstelle von ASCII-Zeichencodes für Zugriffstasten verwenden.

Vermeiden Sie Zugriffstasten, die mit den Mnemoniemenüs einer Anwendung in Konflikt stehen, da der Accelerator das mnemonische -Verhalten überschreibt, was den Benutzer verwirren kann. Weitere Informationen zu mnemonischen Menüs finden Sie unter [Menüs](menus.md).

Wenn eine Anwendung einen Accelerator definiert, der auch in der SystemBeschleunigungstabelle definiert ist, überschreibt der anwendungsdefinierte Accelerator den Systembeschleuniger, jedoch nur innerhalb des Kontexts der Anwendung. Vermeiden Sie diese Vorgehensweise jedoch, da sie verhindert, dass der Systembeschleuniger seine Standardrolle auf der Benutzeroberfläche ausführen kann. Die systemweiten Zugriffstasten werden in der folgenden Liste beschrieben:



| Accelerator                 | Beschreibung                                                                                                      |
|------------------|-------------------------------------------------------------------------------------------------------|
| ALT+ESC          | Wechselt zur nächsten Anwendung.                                                                     |
| ALT+F4           | Schließt eine Anwendung oder ein Fenster.                                                                    |
| ALT+BINDESTRICH       | Öffnet das **Menü Fenster** für ein Dokumentfenster.                                                      |
| ALT+DRUCKBILDSCHIRM | Kopiert ein Bild im aktiven Fenster in die Zwischenablage.                                              |
| ALT+LEERTASTE     | Öffnet das **Menü** Fenster für das Hauptfenster der Anwendung.                                          |
| ALT+TAB          | Wechselt zur nächsten Anwendung.                                                                     |
| STRG+ESC         | Wechselt zum **Startmenü.**                                                                       |
| STRG+F4          | Schließt das aktive Gruppen- oder Dokumentfenster.                                                           |
| F1               | Startet die Hilfedatei der Anwendung, sofern vorhanden.                                                    |
| DRUCKBILDSCHIRM     | Kopiert ein Bild auf dem Bildschirm in die Zwischenablage.                                                     |
| UMSCHALT+ALT+TAB    | Wechselt zur vorherigen Anwendung. Der Benutzer muss ALT+UMSCHALT gedrückt halten, während er die TAB-TASTE drückt. |



 

## <a name="accelerators-and-menus"></a>Zugriffstasten und Menüs

Die Verwendung einer Zugriffstaste entspricht der Auswahl eines Menüelements: Beide Aktionen bewirken, dass das System eine [**WM \_ COMMAND-**](wm-command.md) oder [**WM \_ SYSCOMMAND-Nachricht**](wm-syscommand.md) an die entsprechende Fensterprozedur sendet. Die **WM \_ COMMAND-Nachricht** enthält einen Bezeichner, den die Fensterprozedur überprüft, um die Quelle der Nachricht zu bestimmen. Wenn eine Zugriffstaste die **WM \_ COMMAND-Nachricht** generiert hat, ist der Bezeichner der Bezeichner der Zugriffstaste. Wenn ein Menüelement die **WM \_ COMMAND-Meldung** generiert hat, entspricht der Bezeichner dem des Menüelements. Da eine Zugriffstaste eine Verknüpfung zum Auswählen eines Befehls aus einem Menü bereitstellt, weist eine Anwendung der Zugriffstaste und dem entsprechenden Menüelement in der Regel den gleichen Bezeichner zu.

Eine Anwendung verarbeitet eine [**WM \_ COMMAND-Zugriffstaste**](wm-command.md) genauso wie die entsprechende **WM \_ COMMAND-Meldung** des Menüelements. Die **WM \_ COMMAND-Nachricht** enthält jedoch ein Flag, das angibt, ob die Nachricht von einer Zugriffstaste oder einem Menüelement stammt, falls Zugriffstasten anders als die entsprechenden Menüelemente verarbeitet werden müssen. Die [**WM \_ SYSCOMMAND-Nachricht**](wm-syscommand.md) enthält dieses Flag nicht.

Der Bezeichner bestimmt, ob eine Zugriffstaste eine [**WM \_ COMMAND-**](wm-command.md) oder [**WM \_ SYSCOMMAND-Nachricht**](wm-syscommand.md) generiert. Wenn der Bezeichner den gleichen Wert wie ein Menüelement im Menü System hat, generiert der Accelerator eine **WM \_ SYSCOMMAND-Meldung.** Andernfalls generiert der Accelerator eine **WM \_ COMMAND-Meldung.**

Wenn eine Zugriffstaste über den gleichen Bezeichner wie ein Menüelement verfügt und das Menüelement abgeblendet oder deaktiviert ist, ist die Zugriffstaste deaktiviert und generiert keine [**WM \_ COMMAND-**](wm-command.md) oder [**WM \_ SYSCOMMAND-Meldung.**](wm-syscommand.md) Außerdem generiert eine Zugriffstaste keine Befehlsmeldung, wenn das entsprechende Fenster minimiert ist.

Wenn der Benutzer eine Zugriffstaste verwendet, die einem Menüelement entspricht, empfängt die Fensterprozedur die [**MELDUNGEN WM \_ INITMENU**](wm-initmenu.md) und [**WM \_ INITMENUPOPUP,**](wm-initmenupopup.md) als hätte der Benutzer das Menüelement ausgewählt. Informationen zum Verarbeiten dieser Nachrichten finden Sie unter [Menüs](menus.md).

Eine Zugriffstaste, die einem Menüelement entspricht, sollte im Text des Menüelements enthalten sein.

## <a name="ui-state"></a>Benutzeroberflächenstatus

Mit Windows können Anwendungen verschiedene Features auf der Benutzeroberfläche ausblenden oder anzeigen. Diese Einstellungen werden als Benutzeroberflächenzustand bezeichnet. Der Benutzeroberflächenzustand umfasst die folgenden Einstellungen:

-   Fokusindikatoren (z. B. Fokusrechtecke auf Schaltflächen)
-   Tastenkombinationen (gekennzeichnet durch Unterstreichungen in Steuerelementbeschriftungen)

Ein Fenster kann Nachrichten senden, um eine Änderung des Benutzeroberflächenzustands anzufordern, den Benutzeroberflächenzustand abfragen oder einen bestimmten Zustand für seine untergeordneten Fenster erzwingen. Diese Meldungen sind wie folgt.



| `Message`                                       | BESCHREIBUNG                                |
|-----------------------------------------------|--------------------------------------------|
| [**WM \_ CHANGEUISTATE**](wm-changeuistate.md) | Gibt an, dass sich der Benutzeroberflächenzustand ändern soll. |
| [**WM \_ QUERYUISTATE**](wm-queryuistate.md)   | Ruft den Benutzeroberflächenzustand für ein Fenster ab.       |
| [**WM \_ UPDATEUISTATE**](wm-updateuistate.md) | Ändert den Benutzeroberflächenzustand.                      |



 

Standardmäßig werden alle untergeordneten Fenster eines Fensters der obersten Ebene mit demselben Benutzeroberflächenzustand wie das übergeordnete Fenster erstellt.

Das System verarbeitet den Benutzeroberflächenzustand für Steuerelemente in Dialogfeldern. Beim Erstellen des Dialogfelds initialisiert das System den Benutzeroberflächenzustand entsprechend. Alle untergeordneten Steuerelemente erben diesen Zustand. Nachdem das Dialogfeld erstellt wurde, überwacht das System die Tastatureingaben des Benutzers. Wenn die Benutzeroberflächenzustandseinstellungen ausgeblendet sind und der Benutzer über die Tastatur navigiert, aktualisiert das System den Benutzeroberflächenzustand. Wenn der Benutzer beispielsweise die TAB-TASTE drückt, um den Fokus auf das nächste Steuerelement zu verschieben, ruft das System [**WM \_ CHANGEUISTATE**](wm-changeuistate.md) auf, um die Fokusindikatoren sichtbar zu machen. Wenn der Benutzer die ALT-TASTE drückt, ruft das System **WM \_ CHANGEUISTATE** auf, um die Tastenkombinationen sichtbar zu machen.

Wenn ein Steuerelement die Navigation zwischen den darin enthaltenen Benutzeroberflächenelementen unterstützt, kann es seinen eigenen Benutzeroberflächenzustand aktualisieren. Das Steuerelement kann [**WM \_ QUERYUISTATE**](wm-queryuistate.md) aufrufen, um den anfänglichen Benutzeroberflächenzustand abzurufen und zwischenzuspeichern. Wenn das Steuerelement eine [**WM \_ UPDATEUISTATE-Nachricht**](wm-updateuistate.md) empfängt, kann es seinen Benutzeroberflächenzustand aktualisieren und eine [**WM \_ CHANGEUISTATE-Nachricht**](wm-changeuistate.md) an das übergeordnete Element senden. Jedes Fenster sendet die Nachricht weiterhin an sein übergeordnetes Element, bis es das Fenster der obersten Ebene erreicht. Das Fenster der obersten Ebene sendet die **WM \_ UPDATEUISTATE-Meldung** an die Fenster in der Fensterstruktur. Wenn ein Fenster die **WM \_ CHANGEUISTATE-Nachricht** nicht übergibt, wird das Fenster der obersten Ebene nicht erreicht, und der Benutzeroberflächenzustand wird nicht aktualisiert.

 

 