---
description: Windows Vista enthält eine Reihe von acht einfachen Flattgesten. Bei Flimmern handelt es sich um schnelle, lineare Stiftbewegungen, die Scrollaktionen und -befehlen zugeordnet sind.
ms.assetid: 004c7d76-90a9-4506-a70b-dbf8f9e1c616
title: Gesten für Flattern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37e7d53c42eb178900ce22b7890febcfd1c6aca95f2257b0c5ed06eb20173b79
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119936514"
---
# <a name="flicks-gestures"></a>Gesten für Flattern

Windows Vista enthält eine Reihe von acht *einfachen Gesten für das Flattern.* Bei Flimmern handelt es sich um schnelle, lineare Stiftbewegungen, die Scrollaktionen und -befehlen zugeordnet sind.

## <a name="flick-details"></a>Flick Details

Das Feature "Flacker" bietet dem Benutzer eine neue Möglichkeit, mit dem Tablet PC zu interagieren, indem es ermöglicht, allgemeine Aktionen auszuführen, indem schnelle Gesten mit dem Stift ausgeführt werden. Flacker existieren mit normalen Benutzeraktionen wie tippen nach links und rechts, scrollen und ohne Unterbrechungen.

Ein *Flimmer* ist eine unidirektionale Stiftgeste, die erfordert, dass der Benutzer den Digitizer in einer schnellen Bewegung kontaktiert. Ein Flimmer ist durch hohe Geschwindigkeit und ein hohes Maß an Geradekeit gekennzeichnet. Ein Flimmer wird durch seine Richtung identifiziert. Flimmer können in acht Richtungen erstellt werden, die den Kardinal- und sekundären Kompassrichtungen entsprechen.

Eine *Aktion* oder *Eine Aktion ist* die Aktion oder Verknüpfung, die als Reaktion auf einen Flacker ausgeführt wird. Flimmer werden Aktionen zugeordnet. Die folgende Abbildung zeigt ein Diagramm von acht Stiftflimmern, die ihren Flimmeraktionen entsprechen.

![Abbildung der Gestenzuordnung](images/2647eb2d-36d0-4610-b923-fa3530d1e640.jpg)

Wenn der Benutzer den Stift über den Digitizer eines Tablet-PCs verschiebt, generiert die Hardware Stiftpakete, die an das Stifteingabesubsystem der Tablet PC-Plattform weitergeleitet werden. Wenn der Stift als Ersatz für die Maus verwendet wird, verwendet das Stifteingabesubsystem normalerweise diese Stiftpakete und sendet sie , möglicherweise mit Änderungen, an User32, die Windows Komponente, die für die Verarbeitung der Mauseingabe verantwortlich ist. Wenn der Stift auf einer Belagsoberfläche verwendet wird, wird Ink anstelle von generierten Mauspaketen gerendert.

Die Routine zur Erkennung von Flimmern wird im Stifteingabesubsystem implementiert. Die Erkennung von Flimmern beginnt bei gedrückter Stiftbewegung und wird fortgesetzt, bis eine der beiden:

1) Die Sequenz der empfangenen Pakete wird als kein Flacker oder

2) Pen-up tritt auf.

Während der Erkennung von Flimmern werden Stiftpakete zurückgehalten und nicht an das System gesendet. Dies muss geschehen, da das Senden von Paketen die ausgeführte Aktion "Flacker" beeinträchtigen kann. Beispielsweise würde das Senden von Paketen während eines Flackers, der einer Kopieraktion zugeordnet ist, das Ausgewählte verwerfen, was bedeutet, dass zum Zeitpunkt des Sendens der Aktion nichts zu kopieren wäre.

Während die Pakete in das Stifteingabesubsystem übertragen werden, berechnet die Routine zur Erkennung von Flimmern Metriken zu Länge, Geschwindigkeit, Zeit und Krümmung der ausgeführten Bewegung. Bei jedem eintreffenden Paket aktualisiert die Erkennungsroutine jede dieser Metriken. Sobald eine der Metriken außerhalb der Metriken liegt, die einen Flacker darstellen würden, endet die Erkennung von Flimmern, und die Pakete werden gesendet.

## <a name="where-flicks-are-detected"></a>Wo Flimmer erkannt werden

Flackergesten werden durch die Tatsache ermöglicht, dass Ziehbewegungen in der Regel eher langsam ausgeführt werden. Der Benutzer muss zuerst den Startpunkt des Ziehpunkts als Ziel verwenden, den Ziehpunkt ausführen und dann den Endpunkt als Ziel verwenden. Normalerweise dauert dies zu lange, um sich als Flimmer zu qualifizieren. Auf Denkoberflächen werden jedoch schnell Striche verwendet, die als Flimmer gelten würden. Das Überschreiten eines "t" ist ein gängiges Beispiel. Daher wird die Erkennung von Freihandbewegungen standardmäßig über Freihandoberflächen deaktiviert und systemweit aktiviert.

## <a name="focus-issues"></a>Fokusprobleme

Sobald ein Flacker erkannt wurde, beginnt eine Sequenz von Ereignissen, die letztendlich dazu führt, dass das System eine bestimmte Aktion als Reaktion auf den aufgetretenen Flimmer ausführt. Zuerst bestimmt die Erkennungsroutine im Stifteingabesubsystem, an welches Fenster der Flattern gesendet werden soll. Dies ist in der Regel das Fenster, das den Fokus besitzt, es gibt jedoch Ausnahmen. Beim Scrollen von Flimmern wird der Flimmer an das Fenster gesendet, in dem der Blättern aufgetreten ist. Beachten Sie, dass dies nicht unbedingt das Fenster mit Fokus ist. Wenn ein Flacker an ein Fenster gesendet wird, das keinen Fokus besitzt, ändert sich der Fokus nicht auf dieses Fenster.

## <a name="flick-actions"></a>Flimmeraktionen

Sobald das Zielfenster bestimmt wurde, kann dieses Fenster den Flimmer selbst abhängig vom Standard- oder programmierten Ereignisverhalten verarbeiten. Anwendungen können auf die Aktion reagieren, die basierend auf der Anwendung und der Richtung und Position des Flimmers am besten geeignet ist. In einer Zuordnungsanwendung können z. B. Nach oben und unten-Flatterbewegungen vergrößert oder verkleinert werden, anstatt vertikal zu scrollen, wie es beim Standardverhalten zu erwarten wäre.

Um eine Anwendung zu warnen, dass ein Flacker aufgetreten ist, wird eine Fenstermeldung an sie gesendet. Diese Fenstermeldung enthält sowohl den Startpunkt des Flimmers als auch die Richtung des Flatterns. Wenn die Anwendung diese Fenstermeldung verarbeitet, wird vom Stifteingabesubsystem keine weitere Aktion ausgeführt.

Nachdem ein Flacker erkannt wurde, wird visuelles Feedback, das die Aktion "Flackern" darstellt, auf dem Bildschirm angezeigt. Dieses Feedback dient zwei Zwecken. Zunächst wird für den Benutzer bestätigt, dass der Flimmer erfolgreich war. Zweitens wird der Benutzer daran erinnert, welche Aktion ausgeführt wurde, was dem Benutzer dabei hilft, die Flimmerrichtung mit der zugehörigen Aktion zu verbinden.

Das Feedback zum Flackern besteht aus zwei Teilen: ein Symbol, das die Aktion darstellt, und eine Bezeichnung, die den Namen der Aktion enthält. Die Bezeichnung wird unter dem Symbol angezeigt. Das Feedback wird sofort angezeigt, nachdem der Flacker erkannt wurde. Obwohl Anwendungen ihr Verhalten als Reaktion auf Flimmer anpassen können, indem sie die Meldung des Fensters "Flattern" verarbeiten, kann die Anwendung das Feedback zum Flimmern nicht deaktivieren oder ändern.

Es wird erwartet, dass die meisten Anwendungen nicht flimmern und daher die oben beschriebene Fenstermeldung nicht verarbeiten. Wenn die Nachricht nicht verarbeitet wird, führt das Stifteingabesubsystem weitere Maßnahmen aus. Zunächst wird die Aktion gesucht, die mit der Richtung des erkannten Flackers verknüpft ist. Als Nächstes werden (in der folgenden Tabelle beschriebene) Schritte ausgeführt, damit diese Aktion im Zielfenster ausgeführt wird. Bei vielen der Flackeraktionen umfasst dies das Senden eines Anwendungsbefehls, bestimmte implementierte Aktionen jedoch nicht.

## <a name="processing-application-commands"></a>Verarbeiten von Anwendungsbefehlen

Ihre Anwendung sollte auf einen der Anwendungsbefehle reagieren, die möglicherweise einer Flatternbewegung zugewiesen werden können. Wenn eine Anwendung nicht auf die [**WM \_ \_ TABLET-FLAF-Nachricht**](wm-tablet-flick-message.md)antwortet, folgt Windows Vista, indem die entsprechende [**WM \_ APPCOMMAND-Benachrichtigung**](/windows/desktop/inputdev/wm-appcommand) und dann eine [**WM \_ KEYDOWN-Benachrichtigung**](/windows/desktop/inputdev/wm-keydown) gesendet wird.

Im Folgenden finden Sie eine Liste der Anwendungsbefehle, die Fls zugewiesen werden können, mit der Nachricht für die Sicherungsschlüssel, die gesendet werden kann.



| Befehl                                  | Tastaturanschläge für Sicherungen  |
|------------------------------------------|-------------------|
| APPCOMMAND-BROWSER \_ \_ RÜCKWÄRTS<br/> | Keine<br/>   |
| APPCOMMAND \_ BROWSER \_ FORWARD<br/>  | Keine<br/>   |
| APPCOMMAND \_ COPY<br/>              | STRG+C<br/> |
| APPCOMMAND \_ PASTE<br/>             | STRG+V<br/> |
| APPCOMMAND \_ UNDO<br/>              | STRG+Z<br/> |
| APPCOMMAND \_ DELETE<br/>            | Entf<br/>    |
| APPCOMMAND \_ CUT<br/>               | STRG+X<br/> |
| APPCOMMAND \_ OPEN<br/>              | STRG+O<br/> |
| APPCOMMAND \_ PRINT<br/>             | STRG+P<br/> |
| APPCOMMAND \_ SAVE<br/>              | STRG+S<br/> |
| APPCOMMAND \_ REDO<br/>              | STRG+Y<br/> |
| APPCOMMAND \_ CLOSE<br/>             |                   |



 

Bearbeitungsbefehle wie "Kopieren", "Einfügen", "Ausschneiden" und "Löschen" können gegen eine Auswahl oder an das Objekt gerichtet werden, das sich an der Basis der Fingerbewegung befindet. Wenn keine Auswahl vorhanden ist, können Sie die Daten in der [**FLICK \_ POINT-Struktur**](/windows/desktop/api/tabflicks/ns-tabflicks-flick_point) verwenden, um zu bestimmen, welches Objekt ggf. das Ziel des Bearbeitungsbefehls war.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Referenz zur Flicks-API](flicks-api-reference.md)
</dt> <dt>

[Reagieren auf Flick-Gesten](/previous-versions//dd356077(v=vs.85))
</dt> </dl>

 

