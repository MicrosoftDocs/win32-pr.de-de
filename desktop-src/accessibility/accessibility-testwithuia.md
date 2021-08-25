---
description: Übersicht über die Verwendung von Benutzeroberflächenautomatisierung und anderen Tools zum Testen Ihrer Apps.
title: Testen für Barrierefreiheit
ms.topic: article
ms.date: 04/18/2019
ms.openlocfilehash: 0cc1d118c84e2689b6cf329da29bb518a566fb8588c311229be17fcd28825ddc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119896580"
---
# <a name="testing-for-accessibility"></a>Testen für Barrierefreiheit

Programmgesteuerter Zugriff und Tastaturzugriff sind wichtige Anforderungen zur Unterstützung der Barrierefreiheit in Ihrer Anwendung. Das Testen der Barrierefreiheit Ihrer Windows-Anwendungen, At-Tools (Assistive Technology, Hilfstechnologie) und Benutzeroberflächenframeworks ist entscheidend, um eine erfolgreiche Benutzererfahrung für Personen mit verschiedenen Behinderungen und Einschränkungen (einschließlich Seh-, Lern-, Dexteritäts-/Mobilitäts- und Sprach-/Kommunikationsbehinderungen) oder personen sicherzustellen, die einfach eine Tastatur verwenden möchten.

Ohne ausreichenden Zugriff über AT wie Sprachausgaben und Bildschirmtastaturen können Benutzer mit Seh-, Lern-, Dexteritäts-/Mobilitäts- und Sprach-/Kommunikationsbehindigungen oder Einschränkungen (und Benutzer, die nur die Tastatur bevorzugen) Ihre Anwendung nicht verwenden.

In diesem Abschnitt werden die verschiedenen Tools beschrieben, mit denen die Implementierung der Barrierefreiheit von Windows und Webanwendungen getestet werden kann.

> [!NOTE]
> Es ist auch wichtig, manuelle Tests durchzuführen, um den Tastaturzugriff auf Ihre Anwendung zu überprüfen.

## <a name="tools"></a>Tools

[Barrierefreiheit Insights:](https://accessibilityinsights.io/) Unterstützt Entwickler bei der Suche und Behebung von Problemen mit der Barrierefreiheit auf Websites und Windows Anwendungen.

- [Accessibility Insights for Web](https://accessibilityinsights.io/docs/web/overview) ist eine Erweiterung für Chrome und [Microsoft Edge Insider,](https://www.microsoftedgeinsider.com) mit der Entwickler Probleme mit der Barrierefreiheit in Web-Apps und -Websites finden und beheben können. Es unterstützt zwei primäre Szenarien:
  - **FastPass:** Ein einfacher, zweistufiger Prozess, mit dem Entwickler häufige Probleme mit hoher Barrierefreiheit in weniger als fünf Minuten identifizieren können.  
  - **Bewertung:** Ermöglicht jedem Benutzer, zu überprüfen, ob eine Website zu 100 % mit Barrierefreiheitsstandards und -richtlinien konform ist. [Mit Insights](https://accessibilityinsights.io/) können Sie auch Benutzeroberflächenautomatisierung Elemente, Eigenschaften, Steuerelementmuster und Ereignisse überprüfen (ähnlich wie die im folgenden Abschnitt beschriebenen Legacytools [Inspect](/windows/desktop/winauto/inspect-objects) und [AccEvent).](/windows/desktop/winauto/accessible-event-watcher)

- [Barrierefreiheits-Insights für Windows](https://accessibilityinsights.io/docs/windows/overview) hilft Entwicklern, Probleme mit der Barrierefreiheit in Windows-Apps zu finden und zu beheben. Das Tool unterstützt drei primäre Szenarien:
  - **Mit Live Inspect** können Entwickler überprüfen, ob ein Element in einer App über die richtigen Benutzeroberflächenautomatisierung Eigenschaften verfügt, indem sie einfach mit dem Mauszeiger auf das Element zeigen oder den Tastaturfokus darauf festlegen.
  - **FastPass:** Ein einfacher, zweistufiger Prozess, mit dem Entwickler häufige Probleme mit hoher Barrierefreiheit in weniger als fünf Minuten identifizieren können.
  - **Mit der Problembehandlung** können Sie bestimmte Probleme mit der Barrierefreiheit diagnostizieren und beheben.

### <a name="legacy-testing-tools"></a>Legacytesttools

Die folgenden Tools sind weiterhin im Windows SDK verfügbar und werden hier zur weiteren Unterstützung dokumentiert. Es wird jedoch empfohlen, zu [Barrierefreiheit Insights](https://accessibilityinsights.io/)zu übergehen.

- [Inspect](/windows/desktop/winauto/inspect-objects): Ermöglicht ihnen das Anzeigen der Barrierefreiheitsdaten eines beliebigen Benutzeroberflächenelements. Es ist besonders nützlich, um sicherzustellen, dass Eigenschaften und Steuerelementmuster ordnungsgemäß festgelegt werden, wenn ein allgemeines Steuerelement erweitert oder ein benutzerdefiniertes Steuerelement erstellt wird.
- [Accessible Event Watcher (AccEvent):](/windows/desktop/winauto/accessible-event-watcher)Überprüft Barrierefreiheitsdaten, um Elemente der Anwendungsbenutzeroberfläche zu überprüfen und sicherzustellen, dass Benutzeroberflächenelemente geeignete Microsoft Active Accessibility auslösen und Ereignisse auf Benutzeroberflächenereignissen Benutzeroberflächenautomatisierung. AccEvent wird in der Regel verwendet, um Probleme zu debuggen und zu überprüfen, ob benutzerdefinierte und erweiterte Steuerelemente ordnungsgemäß funktionieren.
- [AccScope:](/windows/desktop/winauto/accscope)Ermöglicht die visuelle Auswertung der Barrierefreiheit einer Anwendung während der frühen Entwurfs- und Entwicklungsphasen. AccScope hilft zu visualisieren, wie eine Sprachausgabe Benutzeroberflächenautomatisierung von einer App bereitgestellten Informationen verwendet, und zeigt, wo das Hinzufügen von Informationen oder Unterstützung zu Ihrer Anwendung die Barrierefreiheit verbessern kann.
- [Benutzeroberflächen-Barrierefreiheitsprüfung:](/windows/desktop/winauto/ui-accessibility-checker)Überprüft, ob wichtige Anforderungen an die Barrierefreiheit der Benutzeroberfläche in einer Anwendung erfüllt werden. AccChecker umfasst Überprüfungsprüfungen für Benutzeroberflächenautomatisierung, Microsoft Active Accessibility und ARIA (Accessible Rich Internet Applications). Sie kann eine statische Überprüfung auf Fehler wie fehlende Namen, Strukturprobleme und vieles mehr bereitstellen. Es hilft bei der Überprüfung des programmgesteuerten Zugriffs und umfasst erweiterte Features zum Automatisieren von Barrierefreiheitstests.
- [Benutzeroberflächenautomatisierung Überprüfen:](/windows/desktop/winauto/ui-automation-verify)Ein Framework für manuelle und automatisierte Tests der Benutzeroberflächenautomatisierung Implementierung in einem Steuerelement oder einer Anwendung (Ergebnisse können protokolliert werden). Sie können Ihre Anwendung in den Testcode integrieren und regelmäßige, automatisierte Tests oder Spot-Überprüfungen Ihrer Benutzeroberflächenautomatisierung Szenarien durchführen. Dieses Tool ist nützlich, um zu überprüfen, ob Änderungen an Anwendungen mit eingerichteten Features in Bereichen, die über die neuen Features hinausgehen, keine neuen Probleme oder Regressionen aufweisen.
