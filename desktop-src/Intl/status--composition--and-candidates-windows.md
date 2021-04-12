---
description: Die Fenster "Status", "Zusammensetzung" und "Kandidaten" bilden die Benutzeroberfläche für den IME.
ms.assetid: a0e52743-f9be-4934-9469-71d3cb5a768a
title: Fenster "Status", "Komposition" und "Kandidaten"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b800def67299a464fd232a08a2bbff0a2a60a2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218543"
---
# <a name="status-composition-and-candidates-windows"></a>Fenster "Status", "Komposition" und "Kandidaten"

Die Fenster "Status", "Zusammensetzung" und "Kandidaten" bilden die Benutzeroberfläche für den IME. Das Statusfenster gibt an, dass der IME geöffnet ist, und bietet dem Benutzer die Möglichkeit, den Konvertierungsmodus festzulegen. Das Kompositionsfenster wird angezeigt, wenn der Benutzer Text eingibt und in Abhängigkeit vom Konvertierungsmodus den Text entweder als eingegeben anzeigt oder konvertierten Text anzeigt. Das Fenster "Kandidaten" wird in Verbindung mit dem Fenster "Komposition" angezeigt. Sie enthält eine Liste der "Kandidaten" (Alternative Zeichen) für die ausgewählten Zeichen im Kompositionsfenster. Der Benutzer kann einen Bildlauf durch die Liste Kandidaten durchführen und die gewünschten Zeichen auswählen und dann zum Fenster Komposition zurückkehren. Der Benutzer kann den gewünschten Text auf diese Weise verfassen, bis die Kompositions Zeichenfolge fertiggestellt und das Fenster geschlossen wird.

Der IME sendet die zusammengesetzten Zeichen in Form von [**WM \_ IME \_ char**](wm-ime-char.md) oder [**WM \_ IME \_ Composition**](wm-ime-composition.md)/GCS Ergebnismeldungen an die IME-fähige Anwendung \_ . Wenn diese Nachrichten von der Anwendung nicht verarbeitet werden, übersetzt die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion Sie in eine oder mehrere [**WM \_ char**](../inputdev/wm-char.md) -Nachrichten.

Standardmäßig erstellt und verwaltet das Betriebssystem automatisch Status-, Kompositions-und Kandidaten Fenster für Texteingabe Anforderungen. Für viele Anwendungen reicht diese Standard Verarbeitung aus. Diese Anwendungen basieren vollständig auf dem Betriebssystem für IME-Unterstützung und werden als "IME-nicht bekannt" bezeichnet, da Sie nicht die vielen Aufgaben kennen, die das Betriebssystem zum Verwalten der IME-Fenster ausführt.

Eine IME-fähige Anwendung hingegen nimmt an der Erstellung und Verwaltung von IME-Fenstern Teil. Solche Anwendungen steuern den Betrieb, die Position und die Darstellung der Standardfenster, indem Sie Nachrichten an diese Fenster senden und Nachrichten von den Fenstern abfangen und verarbeiten. In einigen Fällen erstellen Anwendungen ihre eigenen IME-Fenster und bieten umfassende Verarbeitung für Ihre benutzerdefinierten Status-, Kompositions-und Kandidaten Fenster.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen über den Eingabemethoden-Manager](about-input-method-manager.md)
</dt> </dl>

 

 
