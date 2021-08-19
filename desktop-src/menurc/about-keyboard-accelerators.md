---
title: Informationen zu Tastaturbeschleunigungen
description: In diesem Thema werden Tastenkombinationen erläutert.
ms.assetid: cbf7619d-289d-40c9-9a06-6ce47026d43f
keywords:
- Windows Benutzeroberfläche, Benutzereingabe
- Windows Benutzeroberfläche, Tastenkombinationen
- Benutzereingabe, Zugriffstasten
- Erfassen von Benutzereingaben, Tastaturbeschleunigungen
- Tastenkombinationen
- Beschleuniger
- WM_COMMAND Meldung
- WM_SYS COMMAND-Meldung
- Zugriffstastentabellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b81240feb0ca21028c9d1813f4c8004e1c3bb932fe1ec8767e3719c26e7a5db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117870731"
---
# <a name="about-keyboard-accelerators"></a>Informationen zu Tastaturbeschleunigungen

Zugriffstasten sind eng mit Menüs verknüpft– beide bieten dem Benutzer Zugriff auf den Befehlssatz einer Anwendung. In der Regel verlassen sich Benutzer auf die Menüs einer Anwendung, um den Befehlssatz zu erlernen, und wechseln dann zur Verwendung von Zugriffstasten, sobald sie mit der Anwendung vertrauter werden. Zugriffstasten bieten schnelleren und direkteren Zugriff auf Befehle als Menüs. Eine Anwendung sollte mindestens Zugriffstasten für die häufiger verwendeten Befehle bereitstellen. Obwohl Zugriffstasten in der Regel Befehle generieren, die als Menüelemente vorhanden sind, können sie auch Befehle generieren, die keine entsprechenden Menüelemente aufweisen.

In diesem Abschnitt werden die folgenden Themen behandelt.

-   [Zugriffstastentabellen](#accelerator-tables)
-   [Accelerator-Table-Erstellung](#accelerator-table-creation)
-   [Tastenkombinationszuweisungen](#accelerator-keystroke-assignments)
-   [Zugriffstasten und Menüs](#accelerators-and-menus)
-   [Benutzeroberflächenstatus](#ui-state)

## <a name="accelerator-tables"></a>Zugriffstastentabellen

Eine Zugriffstastentabelle besteht aus einem Array von [**ACCEL-Strukturen,**](/windows/win32/api/winuser/ns-winuser-accel) die jeweils eine einzelne Zugriffstaste definieren. Jede **ACCEL-Struktur** enthält die folgenden Informationen:

-   Tastenkombination des Accelerators.
-   Der Bezeichner der Zugriffstaste.
-   Verschiedene Flags. Dies schließt ein Element ein, das angibt, ob das System visuelles Feedback bereitstellen soll, indem ggf. das entsprechende Menüelement hervorgehoben wird, wenn die Zugriffstaste verwendet wird.

Um Tastenkombinationen für einen angegebenen Thread zu verarbeiten, muss der Entwickler die [**TranslateAccelerator-Funktion**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) in der Nachrichtenschleife aufrufen, die der Nachrichtenwarteschlange des Threads zugeordnet ist. Die **TranslateAccelerator-Funktion** überwacht die Tastatureingabe in die Nachrichtenwarteschlange und sucht nach Tastenkombinationen, die mit einem Eintrag in der Zugriffstastentabelle übereinstimmen. Wenn **TranslateAccelerator** eine Übereinstimmung findet, übersetzt er die Tastatureingabe (d.h. die [**WM \_ KEYUP-**](/windows/desktop/inputdev/wm-keyup) und [**WM \_ KEYDOWN-Nachrichten)**](/windows/desktop/inputdev/wm-keydown) in eine [**WM \_ COMMAND-**](wm-command.md) oder [**WM \_ SYSCOMMAND-Nachricht**](wm-syscommand.md) und sendet die Nachricht dann an die Fensterprozedur des angegebenen Fensters. Die folgende Abbildung zeigt, wie Zugriffstasten verarbeitet werden.

![Tastaturbeschleunigungsverarbeitungsmodell](images/cskac-01.png)

Die [**WM \_ COMMAND-Nachricht**](wm-command.md) enthält den Bezeichner des Accelerators, der bewirkt hat, dass [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) die Nachricht generiert hat. Die Fensterprozedur untersucht den Bezeichner, um die Quelle der Nachricht zu bestimmen, und verarbeitet die Nachricht dann entsprechend.

Zugriffstastentabellen sind auf zwei verschiedenen Ebenen vorhanden. Das System verwaltet eine einzelne, systemweite Zugriffstastentabelle, die für alle Anwendungen gilt. Eine Anwendung kann die Systembeschleunigertabelle nicht ändern. Eine Beschreibung der von der Systembeschleunigungstabelle bereitgestellten Zugriffstasten finden Sie unter [Tastenkombinationszuweisungen](#accelerator-keystroke-assignments)für die Zugriffstaste.

Das System verwaltet auch Zugriffstastentabellen für jede Anwendung. Eine Anwendung kann eine beliebige Anzahl von Zugriffstastentabellen für die Verwendung mit eigenen Fenstern definieren. Ein eindeutiges 32-Bit-Handle **(ABSEL)** identifiziert jede Tabelle. Für einen angegebenen Thread kann jedoch jeweils nur eine Zugriffstastentabelle aktiv sein. Das Handle für die Zugriffstastentabelle, das an die [**TranslateAccelerator-Funktion**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) übergeben wird, bestimmt, welche Zugriffstastentabelle für einen Thread aktiv ist. Die aktive Zugriffstastentabelle kann jederzeit geändert werden, indem ein anderes Handle für die Zugriffstastentabelle an **TranslateAccelerator** übergeben wird.

## <a name="accelerator-table-creation"></a>Accelerator-Table-Erstellung

Es sind mehrere Schritte erforderlich, um eine Zugriffstastentabelle für eine Anwendung zu erstellen. Zunächst wird ein Ressourcencompiler verwendet, um Acceleratortabellenressourcen zu erstellen und sie der ausführbaren Datei der Anwendung hinzuzufügen. Zur Laufzeit wird die [**LoadAccelerators-Funktion**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) verwendet, um die Zugriffstastentabelle in den Arbeitsspeicher zu laden und das Handle für die Zugriffstastentabelle abzurufen. Dieses Handle wird an die [**TranslateAccelerator-Funktion**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) übergeben, um die Zugriffstastentabelle zu aktivieren.

Eine Zugriffstastentabelle kann auch zur Laufzeit für eine Anwendung erstellt werden, indem ein Array von [**ACCEL-Strukturen**](/windows/win32/api/winuser/ns-winuser-accel) an die [**CreateAcceleratorTable-Funktion**](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea) übergeben wird. Diese Methode unterstützt benutzerdefinierte Zugriffstasten in der Anwendung. Wie die [**LoadAccelerators-Funktion**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) gibt **CreateAcceleratorTable** ein Accelerator-Tabellenhandle zurück, das an [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) übergeben werden kann, um die Zugriffstastentabelle zu aktivieren.

Das System zerstört automatisch Zugriffstastentabellen, die von [**LoadAccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) geladen oder von [**CreateAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea)erstellt wurden. Eine Anwendung kann jedoch Ressourcen freigeben, während sie ausgeführt wird, indem sie Zugriffstastentabellen zerstört, die nicht mehr benötigt werden, indem die [**DestroyAcceleratorTable-Funktion**](/windows/desktop/api/Winuser/nf-winuser-destroyacceleratortable) aufgerufen wird.

Eine vorhandene Zugriffstastentabelle kann kopiert und geändert werden. Die vorhandene Zugriffstastentabelle wird mithilfe der [**CopyAcceleratorTable-Funktion**](/windows/desktop/api/Winuser/nf-winuser-copyacceleratortablea) kopiert. Nachdem die Kopie geändert wurde, wird ein Handle für die neue Zugriffstastentabelle abgerufen, indem [**CreateAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea)aufgerufen wird. Schließlich wird das Handle an [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) übergeben, um die neue Tabelle zu aktivieren.

## <a name="accelerator-keystroke-assignments"></a>Tastenkombinationszuweisungen

Ein ASCII-Zeichencode oder ein Code mit virtuellem Schlüssel kann verwendet werden, um die Zugriffstaste zu definieren. Bei einem ASCII-Zeichencode wird die Groß-/Kleinschreibung der Zugriffstaste beachtet. Daher definiert die Verwendung des ASCII-Zeichens "C" die Zugriffstaste als ALT+C anstelle von ALT+C. Allerdings kann die Verwendung von Beschleunigern, bei der die Groß-/Kleinschreibung beachtet wird, verwirrend sein. Beispielsweise wird die ALT+C-Zugriffstaste generiert, wenn der CAPS LOCK-Schlüssel ausgeschaltet ist oder wenn die UMSCHALTTASTE ausgeschaltet ist, aber nicht, wenn beide nicht mehr aktiviert sind.

In der Regel muss bei Zugriffstasten die Groß-/Kleinschreibung nicht beachtet werden. Daher verwenden die meisten Anwendungen Codes mit virtuellen Schlüsseln für Zugriffstasten anstelle von ASCII-Zeichencodes.

Vermeiden Sie Zugriffstasten, die mit dem Menümmonik einer Anwendung in Konflikt stehen, da die Zugriffstaste das mnemonic überschreibt, was den Benutzer verwirren kann. Weitere Informationen zu mnemonics-Menüs finden Sie unter [Menüs](menus.md).

Wenn eine Anwendung einen Accelerator definiert, der auch in der Systembeschleunigungstabelle definiert ist, überschreibt der anwendungsdefinierte Accelerator den Systembeschleunigungsbeschleuniger, jedoch nur innerhalb des Kontexts der Anwendung. Vermeiden Sie diese Vorgehensweise jedoch, da sie verhindert, dass die Systembeschleunigung ihre Standardrolle auf der Benutzeroberfläche ausführt. Die systemweiten Zugriffstasten werden in der folgenden Liste beschrieben:



| Accelerator                 | Beschreibung                                                                                                      |
|------------------|-------------------------------------------------------------------------------------------------------|
| ALT+ESC          | Wechselt zur nächsten Anwendung.                                                                     |
| ALT+F4           | Schließt eine Anwendung oder ein Fenster.                                                                    |
| ALT+BINDESTRICH       | Öffnet das Menü **Fenster** für ein Dokumentfenster.                                                      |
| ALT+DRUCKBILDSCHIRM | Kopiert ein Bild im aktiven Fenster in die Zwischenablage.                                              |
| ALT+LEERTASTE     | Öffnet das Menü **Fenster** für das Hauptfenster der Anwendung.                                          |
| ALT+TAB          | Wechselt zur nächsten Anwendung.                                                                     |
| STRG+ESC         | Wechselt zum **Startmenü.**                                                                       |
| STRG+F4          | Schließt das aktive Gruppen- oder Dokumentfenster.                                                           |
| F1               | Startet die Hilfedatei der Anwendung, sofern vorhanden.                                                    |
| DRUCKBILDSCHIRM     | Kopiert ein Bild auf dem Bildschirm in die Zwischenablage.                                                     |
| UMSCHALT+ALT+TAB    | Wechselt zur vorherigen Anwendung. Der Benutzer muss alt+UMSCHALT drücken und gedrückt halten, während er die TAB-TASTE drückt. |



 

## <a name="accelerators-and-menus"></a>Zugriffstasten und Menüs

Die Verwendung einer Zugriffstaste entspricht der Auswahl eines Menüelements: Beide Aktionen bewirken, dass das System eine [**WM \_ COMMAND-**](wm-command.md) oder [**WM \_ SYSCOMMAND-Nachricht**](wm-syscommand.md) an die entsprechende Fensterprozedur sendet. Die **WM \_ COMMAND-Nachricht** enthält einen Bezeichner, den die Fensterprozedur überprüft, um die Quelle der Nachricht zu ermitteln. Wenn eine Zugriffstaste die **WM \_ COMMAND-Nachricht** generiert hat, entspricht der Bezeichner der Zugriffstaste. Wenn ein Menüelement die **WM \_ COMMAND-Meldung** generiert hat, entspricht der Bezeichner dem des Menüelements. Da eine Zugriffstaste eine Verknüpfung zum Auswählen eines Befehls aus einem Menü bereitstellt, weist eine Anwendung der Zugriffstaste und dem entsprechenden Menüelement in der Regel den gleichen Bezeichner zu.

Eine Anwendung verarbeitet eine [**WM \_ COMMAND-Zugriffstaste**](wm-command.md) genauso wie die entsprechende **WM \_ COMMAND-Meldung** des Menüelements. Die **WM \_ COMMAND-Nachricht** enthält jedoch ein Flag, das angibt, ob die Nachricht von einer Zugriffstaste oder einem Menüelement stammt, falls Zugriffstasten anders als die entsprechenden Menüelemente verarbeitet werden müssen. Die [**WM \_ SYSCOMMAND-Nachricht**](wm-syscommand.md) enthält dieses Flag nicht.

Der Bezeichner bestimmt, ob eine Zugriffstaste eine [**WM \_ COMMAND-**](wm-command.md) oder [**WM \_ SYSCOMMAND-Nachricht**](wm-syscommand.md) generiert. Wenn der Bezeichner den gleichen Wert wie ein Menüelement im Menü System hat, generiert der Accelerator eine **WM \_ SYSCOMMAND-Meldung.** Andernfalls generiert der Accelerator eine **WM \_ COMMAND-Meldung.**

Wenn eine Zugriffstaste über den gleichen Bezeichner wie ein Menüelement verfügt und das Menüelement abgeblendet oder deaktiviert ist, ist die Zugriffstaste deaktiviert und generiert keine [**WM \_ COMMAND-**](wm-command.md) oder [**WM \_ SYSCOMMAND-Meldung.**](wm-syscommand.md) Außerdem generiert eine Zugriffstaste keine Befehlsmeldung, wenn das entsprechende Fenster minimiert ist.

Wenn der Benutzer eine Zugriffstaste verwendet, die einem Menüelement entspricht, empfängt die Fensterprozedur die [**MELDUNGEN WM \_ INITMENU**](wm-initmenu.md) und [**WM \_ INITMENUPOPUP,**](wm-initmenupopup.md) als hätte der Benutzer das Menüelement ausgewählt. Informationen zum Verarbeiten dieser Nachrichten finden Sie unter [Menüs](menus.md).

Eine Zugriffstaste, die einem Menüelement entspricht, sollte im Text des Menüelements enthalten sein.

## <a name="ui-state"></a>Benutzeroberflächenstatus

Windows ermöglicht Es Anwendungen, verschiedene Features in der Benutzeroberfläche auszublenden oder anzuzeigen. Diese Einstellungen werden als Benutzeroberflächenzustand bezeichnet. Der Benutzeroberflächenzustand umfasst die folgenden Einstellungen:

-   Fokusindikatoren (z. B. Fokusrechtecke auf Schaltflächen)
-   Tastenkombinationen (gekennzeichnet durch Unterstreichungen in Steuerelementbeschriftungen)

Ein Fenster kann Nachrichten senden, um eine Änderung des Benutzeroberflächenzustands anzufordern, den Benutzeroberflächenzustand abfragen oder einen bestimmten Zustand für seine untergeordneten Fenster erzwingen. Diese Meldungen sind wie folgt.



| `Message`                                       | BESCHREIBUNG                                |
|-----------------------------------------------|--------------------------------------------|
| [**WM \_ CHANGEUISTATE**](wm-changeuistate.md) | Gibt an, dass sich der Benutzeroberflächenzustand ändern soll. |
| [**WM \_ QUERYUISTATE**](wm-queryuistate.md)   | Ruft den Benutzeroberflächenzustand für ein Fenster ab.       |
| [**WM \_ UPDATEUISTATE**](wm-updateuistate.md) | Ändert den Benutzeroberflächenzustand.                      |



 

Standardmäßig werden alle untergeordneten Fenster eines Fensters der obersten Ebene mit demselben Benutzeroberflächenzustand wie das übergeordnete Fenster erstellt.

Das System verarbeitet den Benutzeroberflächenzustand für Steuerelemente in Dialogfeldern. Beim Erstellen des Dialogfelds initialisiert das System den Benutzeroberflächenzustand entsprechend. Alle untergeordneten Steuerelemente erben diesen Zustand. Nachdem das Dialogfeld erstellt wurde, überwacht das System die Tastatureingaben des Benutzers. Wenn die Einstellungen für den Benutzeroberflächenzustand ausgeblendet sind und der Benutzer über die Tastatur navigiert, aktualisiert das System den Benutzeroberflächenzustand. Wenn der Benutzer beispielsweise die TAB-TASTE drückt, um den Fokus auf das nächste Steuerelement zu verschieben, ruft das System [**WM \_ CHANGEUISTATE**](wm-changeuistate.md) auf, um die Fokusindikatoren sichtbar zu machen. Wenn der Benutzer die ALT-TASTE drückt, ruft das System **WM \_ CHANGEUISTATE** auf, um die Tastenkombinationen sichtbar zu machen.

Wenn ein Steuerelement die Navigation zwischen den darin enthaltenen Benutzeroberflächenelementen unterstützt, kann es seinen eigenen Benutzeroberflächenzustand aktualisieren. Das Steuerelement kann [**WM \_ QUERYUISTATE**](wm-queryuistate.md) aufrufen, um den anfänglichen Benutzeroberflächenzustand abzurufen und zwischenzuspeichern. Wenn das Steuerelement eine [**WM \_ UPDATEUISTATE-Nachricht**](wm-updateuistate.md) empfängt, kann es seinen Benutzeroberflächenzustand aktualisieren und eine [**WM \_ CHANGEUISTATE-Nachricht**](wm-changeuistate.md) an das übergeordnete Element senden. Jedes Fenster sendet die Nachricht weiterhin an sein übergeordnetes Element, bis es das Fenster der obersten Ebene erreicht. Das Fenster der obersten Ebene sendet die **WM \_ UPDATEUISTATE-Meldung** an die Fenster in der Fensterstruktur. Wenn ein Fenster die **WM \_ CHANGEUISTATE-Nachricht** nicht übergibt, wird das Fenster der obersten Ebene nicht erreicht, und der Benutzeroberflächenzustand wird nicht aktualisiert.

 

 