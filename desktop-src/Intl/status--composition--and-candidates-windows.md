---
description: Die Fenster "Status", "Komposition" und "Kandidaten" bilden die Benutzeroberfläche für den IME.
ms.assetid: a0e52743-f9be-4934-9469-71d3cb5a768a
title: Status, Komposition und Kandidaten Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83f5c385c14cd265630de77352e12e4c63bce806837462f3c9ab3c204940e66c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130110"
---
# <a name="status-composition-and-candidates-windows"></a>Status, Komposition und Kandidaten Windows

Die Fenster "Status", "Komposition" und "Kandidaten" bilden die Benutzeroberfläche für den IME. Das Statusfenster gibt an, dass der IME geöffnet ist, und bietet dem Benutzer die Möglichkeit, die Konvertierungsmodi zu festlegen. Das Kompositionsfenster wird angezeigt, wenn der Benutzer Text ein gibt und je nach Konvertierungsmodus den Text entweder als eingegeben oder konvertierten Text anzeigt. Das Kandidatenfenster wird in Verbindung mit dem Kompositionsfenster angezeigt. Sie enthält eine Liste der "Kandidaten" (alternative Zeichen) für das bzw. die ausgewählten Zeichen im Kompositionsfenster. Der Benutzer kann durch die Kandidatenliste scrollen, die gewünschten Zeichen auswählen und dann zum Kompositionsfenster zurückkehren. Der Benutzer kann den gewünschten Text auf diese Weise erstellen, bis die Kompositionszeichenfolge abgeschlossen und das Fenster geschlossen wird.

Der IME sendet die zusammengesetzten Zeichen in Form von [**WM \_ IME \_ CHAR-**](wm-ime-char.md) oder [**WM \_ IME \_ COMPOSITION**](wm-ime-composition.md)/GCS RESULT-Nachrichten an die IME-orientierte \_ Anwendung. Wenn die Anwendung diese Nachrichten nicht verarbeiten kann, übersetzt die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) sie in eine oder mehrere [**WM \_ CHAR-Nachrichten.**](../inputdev/wm-char.md)

Standardmäßig erstellt und verwaltet das Betriebssystem automatisch Status-, Kompositions- und Kandidatenfenster für Texteingabeanforderungen. Für viele Anwendungen ist diese Standardverarbeitung ausreichend. Diese Anwendungen basieren für die IME-Unterstützung vollständig auf dem Betriebssystem und werden als "IME-nicht bekannt" bezeichnet, da sie nicht wissen, welche aufgaben das Betriebssystem zur Verwaltung der IME-Fenster übernimmt.

Eine IME-orientierte Anwendung ist dagegen an der Erstellung und Verwaltung von IME-Fenstern beteiligt. Solche Anwendungen steuern den Betrieb, die Position und die Darstellung der Standardfenster, indem sie Nachrichten an diese Fenster senden und Nachrichten von den Fenstern abfangen und verarbeiten. In einigen Fällen erstellen Anwendungen eigene IME-Fenster und bieten eine vollständige Verarbeitung für ihre benutzerdefinierten Status-, Kompositions- und Kandidatenfenster.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zum Eingabemethode-Manager](about-input-method-manager.md)
</dt> </dl>

 

 
