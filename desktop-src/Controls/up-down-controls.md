---
title: Informationen zu Up-Down Steuerelementen
description: Ein auf-ab-Steuerelement ist ein paar von Pfeil Schaltflächen, auf die der Benutzer klicken kann, um einen Wert zu erhöhen oder zu verringern, z. b. eine Bild Lauf Position oder eine Zahl, die in einem Begleit Steuerelement (einem Buddy-Fenster) angezeigt wird
ms.assetid: ae2c0283-9cad-40d1-b8a6-a90484a95f56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cc8dad15a8254b138cae4175cc16b1ef3111745
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730584"
---
# <a name="about-up-down-controls"></a>Informationen zu Up-Down Steuerelementen

Ein auf-ab-Steuerelement ist ein paar von Pfeil Schaltflächen, auf die der Benutzer klicken kann, um einen Wert zu erhöhen oder zu verringern, z. b. eine Bild Lauf Position oder eine Zahl, die in einem Begleit Steuerelement (einem Buddy-Fenster) angezeigt wird

Für den Benutzer sehen ein auf-ab-Steuerelement und das zugehörige Buddy-Fenster oft wie ein einzelnes Steuerelement. Sie können angeben, dass sich ein auf-ab-Steuerelement automatisch neben seinem Buddy-Fenster positioniert und dass die Beschriftung des Buddy-Fensters automatisch auf die aktuelle Position festgelegt wird. Sie können z. b. ein auf-ab-Steuerelement mit einem Bearbeitungs Steuerelement verwenden, um den Benutzer zur Eingabe der numerischen Eingabe aufzufordern. Die folgende Abbildung zeigt ein auf-ab-Steuerelement mit einem Bearbeitungs Steuerelement als Buddy-Fenster, eine Kombination, die manchmal auch als Spinner-Steuerelement bezeichnet wird.

![Screenshot mit einem kurzen, breiten rechteckigen Steuerelement mit nach-oben-und nach-unten-Pfeilen am rechten Rand](images/updown.jpg)

Die folgenden Themen werden in diesem Abschnitt erläutert.

-   [Auf-ab-Steuerelement Stile](#up-down-control-styles)
-   [Position und Beschleunigung](#position-and-acceleration)
-   [Standard Up-Down steuert die Nachrichtenverarbeitung](#default-up-down-controls-message-processing)

## <a name="up-down-control-styles"></a>Up-Down Steuerelement Stile

Mithilfe von Fenster Formaten können Sie Merkmale eines auf-ab-Steuer Elements ändern, z. b., wie es sich in Bezug auf das Buddy-Fenster positioniert, ob es den Text seines Buddy-Fensters festlegt und ob es die Pfeil-nach-oben-und nach-unten-Taste verarbeitet.

Ein auf-ab-Steuerelement mit dem [**UDS \_ alignleft**](up-down-control-styles.md) -oder [**UDS \_ AlignRight**](up-down-control-styles.md) -Stil richtet sich nach dem linken oder rechten Rand seines Buddy-Fensters. Die Breite des Buddy-Fensters wird verringert, um die Breite des auf-ab-Steuer Elements anzupassen.

Ein auf-ab-Steuerelement mit dem [**UDS \_ setbuddyint**](up-down-control-styles.md) -Stil legt die Beschriftung seines Buddy-Fensters fest, wenn sich die aktuelle Position ändert. Das Steuerelement fügt ein Tausender Trennzeichen zwischen allen drei Ziffern einer Dezimal Zeichenfolge ein, es sei denn, der [**UDS- \_ notausender**](up-down-control-styles.md) -Stil ist angegeben Wenn das Buddy-Fenster ein Listenfeld ist, legt ein auf-ab-Steuerelement seine aktuelle Auswahl anstelle der Beschriftung fest.

Sie können den [**UDS \_ arrowkeys**](up-down-control-styles.md) -Stil angeben, um eine Tastaturschnittstelle für ein auf-ab-Steuerelement bereitzustellen. Wenn dieser Stil angegeben ist, verarbeitet das Steuerelement die nach-oben-und nach-unten-Taste. Das-Steuerelement unterteilt auch das Buddy-Fenster, sodass diese Tasten verarbeitet werden können, wenn das Buddy-Fenster den Fokus besitzt.

Wenn Sie ein auf-ab-Steuerelement für horizontales Scrollen verwenden, können Sie den [**UDS- \_ Horz**](up-down-control-styles.md) -Stil angeben. Dieser Stil bewirkt, dass die Pfeile des auf-ab-Steuer Elements auf die linke und die Rechte anstelle von nach oben und unten zeigen.

Standardmäßig wird die aktuelle Position nicht geändert, wenn der Benutzer versucht, ihn zu erhöhen oder ihn über den maximalen oder minimalen Wert hinaus dekrementt. Sie können dieses Verhalten ändern, indem Sie den [**UDS- \_ Wrap**](up-down-control-styles.md) -Stil verwenden, sodass die Position "umbrochen" wird, um das Gegenteil zu erreichen. Wenn Sie z. b. eine Erhöhung der oberen Grenze überschreiten, wird die Position wieder auf den unteren Grenzwert umschlossen.

## <a name="position-and-acceleration"></a>Position und Beschleunigung

Nachdem ein auf-ab-Steuerelement erstellt wurde, können Sie die aktuelle Position, die minimale Position und die maximale Position des Steuer Elements ändern, indem Sie Nachrichten senden. Sie können auch die Basis, mit der die aktuelle Position im Buddy-Fenster angezeigt wird, und die Geschwindigkeit ändern, mit der sich die aktuelle Position ändert, wenn der nach-oben-oder nach-unten-Pfeil geklickt wird.

Um die aktuelle Position eines auf-ab-Steuer Elements abzurufen, verwenden Sie die [**UDM- \_ GetPos**](udm-getpos.md) -Nachricht. Für ein auf-ab-Steuerelement mit einem Buddy-Fenster ist die aktuelle Position die Zahl in der Beschriftung des Buddy-Fensters. Da sich die Beschriftung möglicherweise geändert hat (z. b. wenn der Benutzer den Text eines Bearbeitungs Steuer Elements bearbeitet hat), ruft das auf-ab-Steuerelement die aktuelle Beschriftung ab und aktualisiert die aktuelle Position entsprechend.

Die Beschriftung des Buddy-Fensters kann entweder eine Dezimal-oder hexadezimale Zeichenfolge sein, abhängig von der Basis von Basis 10 oder 16 des auf-ab-Steuer Elements. Sie können die Basis für die Basis mithilfe der [**UDM- \_ setbase**](udm-setbase.md) -Nachricht festlegen und die Basis-Base mithilfe der [**UDM \_ GetBase**](udm-getbase.md) -Nachricht abrufen.

Die [**UDM- \_ SetPos**](udm-setpos.md) -Nachricht legt die aktuelle Position eines Buddy-Fensters fest. Beachten Sie, dass im Gegensatz zu einer Schiebe Leiste ein auf-ab-Steuerelement automatisch seine aktuelle Position ändert, wenn auf die Pfeile nach oben und nach unten geklickt wird. Daher muss die aktuelle Position bei der Verarbeitung der [**WM \_ VScroll**](wm-vscroll.md) -oder [**WM \_ HScroll**](wm-hscroll.md) -Nachricht nicht von der Anwendung festgelegt werden.

Die minimale und maximale Position eines auf-ab-Steuer Elements können Sie mithilfe der [**UDM- \_**](udm-setrange.md) Nachricht "-Nachricht" ändern. Die maximale Position ist möglicherweise kleiner als das minimal, und in diesem Fall wird durch Klicken auf die Schaltfläche mit dem Pfeil nach oben die aktuelle Position reduziert. Um eine andere Möglichkeit zu erhalten, bedeutet up, dass der Übergang zur maximalen Position fortgesetzt wird. Um die Mindest-und höchst Positionen für ein auf-ab-Steuerelement abzurufen, verwenden Sie die [**UDM \_ GetRange**](udm-getrange.md) -Nachricht.

Sie können die Rate steuern, mit der sich die Position ändert, wenn der Benutzer eine Pfeil Schaltfläche durch Festlegen der Beschleunigung des auf-ab-Steuer Elements gedrückt hält. Die Beschleunigung wird durch ein Array von [**udaccel**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) -Strukturen definiert. Jede Struktur gibt ein Zeitintervall und die Anzahl der Einheiten an, um die am Ende dieses Intervalls Inkrement oder Dekrement durchgesetzt werden soll. Um die Beschleunigung festzulegen, verwenden Sie die [**UDM- \_ SetAccel**](udm-setaccel.md) -Nachricht. Um Beschleunigungs Informationen abzurufen, verwenden Sie die [**UDM \_ GetAccel**](udm-getaccel.md) -Nachricht.

## <a name="default-up-down-controls-message-processing"></a>Standard Up-Down steuert die Nachrichtenverarbeitung

In diesem Abschnitt werden die von einem auf-ab-Steuerelement verarbeiteten standardmäßigen Windows-Meldungen beschrieben.



| `Message`                                        | Verarbeitung wird ausgeführt                                                                                                                                                                                         |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ Erstellen**](/windows/desktop/winmsg/wm-create)             | Ordnet eine private Datenstruktur zu und initialisiert sie und speichert Ihre Adresse als Fenster Daten.                                                                                                                     |
| [**WM \_ zerstören**](/windows/desktop/winmsg/wm-destroy)           | Gibt während der [**WM \_ Create**](/windows/desktop/winmsg/wm-create) -Verarbeitung zugeordnete Daten frei.                                                                                                                                   |
| [**WM \_ aktivieren**](/windows/desktop/winmsg/wm-enable)             | Erklärt das Fenster für ungültig.                                                                                                                                                                                      |
| [**WM- \_ KeyDown**](/windows/desktop/inputdev/wm-keydown)         | Ändert die aktuelle Position bei einem Pfeil nach oben oder nach unten.                                                                                                                                   |
| [**WM- \_ KeyUp**](/windows/desktop/inputdev/wm-keyup)             | Schließt die Positionsänderung ab.                                                                                                                                                                               |
| [**WM \_ lbuttondown**](/windows/desktop/inputdev/wm-lbuttondown) | Erfasst die Maus. Wenn das Buddy-Fenster ein Bearbeitungs Steuerelement oder ein Listenfeld ist, wird der Fokus auf das Buddy-Fenster festgelegt. Wenn sich die Maus über der Schaltfläche nach oben oder unten befindet, beginnt Sie mit dem Ändern der Position und legt einen Timer fest. |
| [**WM- \_ lbuttonup**](/windows/desktop/inputdev/wm-lbuttonup)     | Schließt die Positionsänderung ab und gibt die Maus Aufzeichnung frei, wenn das auf-ab-Steuerelement die Maus erfasst hat. Wenn das Buddy-Fenster ein Bearbeitungs Steuerelement ist, wählt es den gesamten Text im Bearbeitungs Steuerelement aus.             |
| [**WM- \_ Paint**](/windows/desktop/gdi/wm-paint)                  | Zeichnet das auf-ab-Steuerelement. Wenn der *wParam* -Parameter ungleich NULL ist, geht das Steuerelement davon aus, dass es sich bei dem Wert um einen **hdc** handelt und zeichnet sich durch den Gerätekontext aus.                                                    |
| [**WM- \_ Timer**](/windows/desktop/winmsg/wm-timer)               | Ändert die aktuelle Position, wenn die Maus über einer Schaltfläche gedrückt gehalten wird und ein ausreichendes Intervall verstrichen ist.                                                                                            |



 

 

 