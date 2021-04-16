---
description: Windows Vista enthält eine Reihe von acht grundlegenden Flick Gesten. Flicks sind schnelle, lineare Stift Bewegungen, die scrollaktionen und-Befehlen zugeordnet sind.
ms.assetid: 004c7d76-90a9-4506-a70b-dbf8f9e1c616
title: Gesten Flicks
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f85d519f47b265779741b2f98fcb1b2f5d69df5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104566224"
---
# <a name="flicks-gestures"></a>Gesten Flicks

Windows Vista enthält eine Reihe von acht grundlegenden *Flick Gesten*. Flicks sind schnelle, lineare Stift Bewegungen, die scrollaktionen und-Befehlen zugeordnet sind.

## <a name="flick-details"></a>Flick Details

Die schnelle Stift Bewegungen-Funktion bietet dem Benutzer eine neue Möglichkeit, mit dem Tablet PC zu interagieren, indem es Ihnen ermöglicht, gängige Aktionen durchzuführen. Flicks sind mit normalen Benutzeraktionen wie linken und rechten Abzweigungen, scrollen und binden gleichzeitig nebeneinander und unterbrechen diese nicht.

Bei einem *Flick* handelt es sich um eine unidirektionale Stift Bewegung, bei der der Benutzer bei einer schnellen Flimmern eine Verbindung mit dem Digitalisierer aufnehmen muss Ein Flick ist durch hohe Geschwindigkeit und einen hohen Grad an Genauigkeit gekennzeichnet. Ein Flick wird durch seine Richtung identifiziert. Flicks können in acht Richtungen erstellt werden, die den Haupt-und sekundären Kompass Richtungen entsprechen.

Eine *Aktion* oder eine *Flick Aktion* ist die Aktion oder Verknüpfung, die als Reaktion auf einen Flick-Vorgang ausgeführt wird. Flicks werden Aktionen zugeordnet. Die folgende Abbildung zeigt ein Diagramm mit acht Stift schnelle Stift Bewegungen, die ihren Flick Aktionen entsprechen.

![Darstellung der Gesten Zuordnung](images/2647eb2d-36d0-4610-b923-fa3530d1e640.jpg)

Wenn der Benutzer den Stift über den Digitalisierer eines Tablet PCs bewegt, generiert die Hardware Pen-Pakete, die an das Stift Eingabe Subsystem der Tablet PC-Plattform weitergeleitet werden. Wenn der Stift als Ersatz für die Maus verwendet wird, übernimmt das Stift Eingabe Subsystem normalerweise diese Stift Pakete und sendet Sie ggf. mit Änderungen an User32, die für die Verarbeitung von Maus Eingaben verantwortliche Windows-Komponente. Wenn der Stift auf einer Erstellungs Oberfläche verwendet wird, wird die frei Hand Eingabe gerendert, statt die Maus Pakete zu generieren.

Die Flick Erkennungsroutine wird im Stift Eingabe Subsystem implementiert. Die Flick-Erkennung beginnt bei der Stift Schließung und wird bis zu einem der

1) die Sequenz der empfangenen Pakete wird als Flick oder

2) der Stift wird angezeigt.

Obwohl die Flick-Erkennung auftritt, werden Stift Pakete zurück gehalten und nicht an das System gesendet. Dies muss erfolgen, weil das Senden von Paketen möglicherweise die ausgeführte Aktion "Flick" beeinträchtigt. Beispielsweise würde das Senden von Paketen während eines Flicks, das einer Kopier Aktion zugeordnet ist, das ausgewählte verwerfen, was bedeutet, dass nichts zu kopieren ist, wenn die Aktion gesendet wurde.

Wenn die Pakete in das Stift Eingabe Subsystem fließen, berechnet die Flick Erkennungsroutine Metriken zu Länge, Geschwindigkeit, Zeit und Krümmung der Bewegung, die ausgeführt wird. Bei jedem eingehenden Paket aktualisiert die Erkennungsroutine jede dieser Metriken. Sobald eine der Metriken außerhalb der Werte liegt, die einen Flick bilden würden, wird die Flick Erkennung beendet, und die Pakete werden durch gesendet.

## <a name="where-flicks-are-detected"></a>Wo schnelle Stift Bewegungen erkannt werden

Flick Gesten werden durch die Tatsache ermöglicht, dass zieht in der Regel eher langsam ausgeführt werden. Der Benutzer muss zuerst den Anfangspunkt des Zieh Punkts ausrichten, den Zieh Vorgang ausführen und dann auf den Endpunkt abzielen. Normalerweise dauert es zu lange, bis Sie als Flick qualifiziert werden. Bei der Aufnahme von Oberflächen werden schnell Striche, die sich als schnelle Stift Bewegungen qualifizieren würden, häufig auftreten. das Überschreiten von "t" ist ein gängiges Beispiel. Daher wird die Flick-Erkennung standardmäßig über das Überspringen von Oberflächen deaktiviert und systemweit aktiviert.

## <a name="focus-issues"></a>Schwerpunkt Probleme

Nachdem ein Flick erkannt wurde, beginnt eine Abfolge von Ereignissen, die letztendlich dazu führt, dass das System eine bestimmte Aktion als Reaktion auf den aufgetretenen Flick ausführt. Zuerst bestimmt die Erkennungsroutine innerhalb des Stift Eingabe-Subsystems das Fenster, an das der Flick gesendet werden soll. Dies ist normalerweise das Fenster, das den Fokus besitzt, aber es gibt Ausnahmen. Für scrollflicks wird der Flick an das Fenster gesendet, über das der Flick aufgetreten ist. Beachten Sie, dass dies nicht notwendigerweise das Fenster mit dem Fokus ist. Wenn ein Flick an ein Fenster gesendet wird, das keinen Fokus besitzt, ändert sich der Fokus nicht in dieses Fenster.

## <a name="flick-actions"></a>Flick Aktionen

Nachdem das Zielfenster bestimmt wurde, kann dieses Fenster abhängig vom Standardverhalten oder dem programmierten Ereignis Verhalten den Flick selbst verarbeiten. Anwendungen können auf die Aktion reagieren, die auf der Grundlage der Anwendung und der Richtung und Position des Flick am besten geeignet ist. Beispielsweise können in einer zuder Zuordnungsanwendung nach oben-und nach-unten-schnelle Stift Bewegungen ein-oder ausgeblendet werden, anstatt vertikal zu scrollen, was vom Standardverhalten erwartet wird.

Um eine Anwendung zu benachrichtigen, dass ein Flick aufgetreten ist, wird eine Fenster Meldung an Sie gesendet. Diese Fenster Meldung enthält sowohl den Anfangspunkt des Flicks als auch die Richtung des Flicks. Wenn die Anwendung diese Fenster Meldung behandelt, werden keine weiteren Aktionen vom Stift Eingabe Subsystem durchgeführt.

Nachdem ein Flick erkannt wurde, wird das visuelle Feedback, das die Aktion "Flick" darstellt, auf dem Bildschirm angezeigt. Dieses Feedback dient zwei Zwecken. Zuerst wird dem Benutzer bestätigt, dass der Flick erfolgreich war. Zweitens erinnert Sie den Benutzer daran, welche Aktion durchgeführt wurde, und unterstützt den Benutzer dabei, die Richtung "Flick" mit der zugehörigen Aktion zu verbinden.

Das Flick-Feedback besteht aus zwei Teilen: ein Symbol, das die Aktion und eine Bezeichnung mit dem Namen der Aktion darstellt. Die Bezeichnung wird unterhalb des Symbols angezeigt. Das Feedback wird sofort angezeigt, nachdem der Flick erkannt wurde. Obwohl Anwendungen ihr Verhalten in Reaktion auf schnelle Stift Bewegungen anpassen können, indem Sie die Meldung "Flick Fenster" verarbeiten, kann die Anwendung das Flick-Feedback nicht deaktivieren oder ändern.

Es wird erwartet, dass die meisten Anwendungen nicht mit einem Flick kompatibel sind und somit die oben beschriebene Fenster Meldung nicht verarbeiten. Wenn die Nachricht nicht behandelt wird, führt das Stift Eingabe Subsystem weitere Aktionen aus. Zuerst sucht Sie nach der Aktion, die mit der Richtung des gefundenen Flick verknüpft ist. Anschließend werden Schritte ausgeführt (in der folgenden Tabelle beschrieben), damit das Zielfenster diese Aktion ausführt. Für viele der Flick Aktionen umfasst dies das Senden eines Anwendungs Befehls, aber bestimmte Aktionen, die implementiert werden, sind nicht.

## <a name="processing-application-commands"></a>Verarbeiten von Anwendungs Befehlen

Die Anwendung sollte auf alle Anwendungs Befehle reagieren, die potenziell einer Flick Bewegung zugewiesen werden könnten. Wenn eine Anwendung nicht auf die WM- [**\_ Tablet- \_ Nachricht**](wm-tablet-flick-message.md)antwortet, wird Windows Vista nachverfolgt, indem die entsprechende [**WM \_ appcommand**](/windows/desktop/inputdev/wm-appcommand) -Benachrichtigung gesendet wird, gefolgt von einer [**WM- \_ KeyDown**](/windows/desktop/inputdev/wm-keydown) -Benachrichtigung.

Im folgenden finden Sie eine Liste der Anwendungs Befehle, die Flicks zugewiesen werden können, mit der Meldung "Backup Tastatureingabe", die gesendet werden kann.



| Get-Help                                  | Tastatureingabe sichern  |
|------------------------------------------|-------------------|
| appcommand- \_ Browser \_ rückwärts<br/> | Keine<br/>   |
| appcommand- \_ Browser \_ Vorwärts<br/>  | Keine<br/>   |
| appcommand- \_ Kopie<br/>              | STRG+C<br/> |
| appcommand \_ Einfügen<br/>             | STRG+V<br/> |
| appcommand \_ rückgängig machen<br/>              | STRG+Z<br/> |
| appcommand \_ Löschen<br/>            | Entf<br/>    |
| appcommand- \_ Ausschneiden<br/>               | STRG+X<br/> |
| appcommand \_ geöffnet<br/>              | STRG+O<br/> |
| appcommand- \_ Druck<br/>             | STRG+P<br/> |
| appcommand \_ Speichern<br/>              | STRG+S<br/> |
| appcommand- \_ Wiederholung<br/>              | STRG+Y<br/> |
| appcommand \_ Schließen<br/>             |                   |



 

Das Bearbeiten von Befehlen, z. b. kopieren, einfügen, Ausschneiden und löschen, wird möglicherweise an eine Auswahl oder an das Objekt weitergeleitet, das sich an der Basis der Flick Bewegung befindet. Wenn keine Auswahl vorhanden ist, können Sie die Daten in der [**Struktur der Flick \_ Punkte**](/windows/desktop/api/tabflicks/ns-tabflicks-flick_point) verwenden, um zu bestimmen, welches Objekt, sofern vorhanden, das Ziel des Bearbeitungs Befehls gewesen sein könnte.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Flicks-API-Referenz](flicks-api-reference.md)
</dt> <dt>

[Reagieren auf Flick Gesten](/previous-versions//dd356077(v=vs.85))
</dt> </dl>

 

