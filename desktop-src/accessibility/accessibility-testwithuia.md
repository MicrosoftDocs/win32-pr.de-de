---
description: Übersicht über die Verwendung der Benutzeroberflächen Automatisierung und anderer Tools zum Testen Ihrer Apps.
title: Testen für Barrierefreiheit
ms.topic: article
ms.date: 04/18/2019
ms.openlocfilehash: 0d589c9b7bd598c0829ff9941ab2facabfaf10d2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127581"
---
# <a name="testing-for-accessibility"></a>Testen für Barrierefreiheit

Programm gesteuerter Zugriff und Tastatur Zugriff sind wichtige Anforderungen für die Unterstützung von Barrierefreiheit in Ihrer Anwendung. Das Testen des Zugriffs auf Ihre Windows-Anwendungen, Hilfstechnologien (at) und Benutzeroberflächen-Frameworks ist entscheidend, um eine erfolgreiche Benutzerfreundlichkeit für Personen mit unterschiedlichen Behinderungen und Einschränkungen (einschließlich Vision, Learning, Dexterität/Mobilität und sprach-/kommunikationbehinderungen) zu gewährleisten.

Ohne ausreichenden Zugriff auf, wie z. b. Bildschirm Reader und Bildschirm Tastaturen, können Benutzer mit Vision, Learning, Dexterity/Mobility und sprach-/kommunikationsbehinderungen oder-Einschränkungen (und Benutzern, die die Tastatur einfach verwenden) Ihre Anwendung nicht verwenden.

In diesem Abschnitt werden die verschiedenen Tools beschrieben, die verwendet werden können, um die Barrierefreiheits Implementierung von Windows-und Webanwendungen zu testen.

> [!NOTE]
> Es ist auch wichtig, manuelle Tests durchzuführen, um den Tastatur Zugriff auf Ihre Anwendung zu überprüfen.

## <a name="tools"></a>Tools

[Einblicke in Barrierefreiheit](https://accessibilityinsights.io/) : unterstützt Entwickler beim Suchen und Beheben von Barrierefreiheits Problemen in Websites und Windows-Anwendungen.

- [Einblicke in die Barrierefreiheit für das Web](https://accessibilityinsights.io/docs/web/overview) ist eine Erweiterung für den Chrome-und [Microsoft Edge-Insider](https://www.microsoftedgeinsider.com) , der Entwicklern hilft, Barrierefreiheits Probleme in Web-Apps und Websites zu finden Es unterstützt zwei primäre Szenarien:
  - **FASTPASS** : ein schlanker, zweistufiger Prozess, der Entwicklern hilft, häufige, äußerst Wirkungs freie Barrierefreiheits Probleme in weniger als fünf Minuten zu identifizieren.  
  - **Bewertung** : ermöglicht allen Benutzern zu überprüfen, ob eine Website 100% mit Barrierefreiheits Standards und-Richtlinien kompatibel ist. Mit [Barrierefreiheits](https://accessibilityinsights.io/) Informationen können Sie auch Benutzeroberflächenautomatisierungs-Elemente,-Eigenschaften,-Steuerelement Muster und-Ereignisse überprüfen (ähnlich wie im folgenden Abschnitt unter [Suchen](/windows/desktop/winauto/inspect-objects) und [AccEvent](/windows/desktop/winauto/accessible-event-watcher) -Legacy Tools).

- [Barrierefreiheits Informationen für Windows](https://accessibilityinsights.io/docs/windows/overview) helfen Entwicklern, Barrierefreiheits Probleme in Windows-apps zu finden und zu beheben. Das Tool unterstützt drei primäre Szenarien:
  - Mit **Live** Überprüfung können Entwickler überprüfen, ob ein Element in einer APP über die richtigen Benutzeroberflächenautomatisierungs-Eigenschaften verfügt, indem Sie einfach auf das Element zeigen oder den Tastaturfokus festlegen.
  - **FASTPASS** : ein schlanker, zweistufiger Prozess, der Entwicklern hilft, häufige, äußerst Wirkungs freie Barrierefreiheits Probleme in weniger als fünf Minuten zu identifizieren.
  - Mit der **Problem** Behandlung können Sie bestimmte Barrierefreiheits Probleme diagnostizieren und beheben.

### <a name="legacy-testing-tools"></a>Legacy TestTools

Die folgenden Tools sind weiterhin in der Windows SDK verfügbar und sind hier für den fortgesetzten Support dokumentiert. es wird jedoch empfohlen, den Übergang in [Einblicke in Barrierefreiheit](https://accessibilityinsights.io/)zu übertragen.

- Über [prüfen](/windows/desktop/winauto/inspect-objects): Hiermit können Sie die Barrierefreiheits Daten eines beliebigen Benutzeroberflächen Elements anzeigen. Dies ist besonders nützlich, um sicherzustellen, dass Eigenschaften und Steuerelement Muster ordnungsgemäß festgelegt werden, wenn ein gängiges Steuerelement erweitert oder ein benutzerdefiniertes
- [Barrierefreie Ereignisüberwachung (AccEvent)](/windows/desktop/winauto/accessible-event-watcher): überprüft Barrierefreiheits Daten, um Anwendungs Benutzeroberflächen Elemente zu validieren und sicherzustellen, dass Benutzeroberflächen Elemente ordnungsgemäße Ereignisse von Microsoft Active Accessibility und Benutzeroberflächenautomatisierungs für Benutzeroberflächen Ereignisse AccEvent wird normalerweise zum Debuggen von Problemen und zum Überprüfen verwendet, ob benutzerdefinierte und erweiterte Steuerelemente ordnungsgemäß funktionieren.
- [Accscope](/windows/desktop/winauto/accscope): ermöglicht die visuelle Auswertung einer Anwendungs Barrierefreiheit während der frühen Entwurfs-und Entwicklungsphase. Mithilfe von accscope können Sie visualisieren, wie eine Sprachausgabe Informationen zur Benutzeroberflächenautomatisierung verwendet, die von einer APP bereitgestellt werden
- [UI-Barrierefreiheits](/windows/desktop/winauto/ui-accessibility-checker)Prüfung: überprüft, ob die wichtigsten Barrierefreiheits Anforderungen der Benutzeroberfläche in einer Anwendung erreicht werden. Die Zugriffs Prüfung umfasst überprüfungsprüfungen für die Benutzeroberflächen Automatisierung, Microsoft Active Accessibility und barrierefreie Internet Anwendungen (Aria). Es kann eine statische Überprüfung auf Fehler wie fehlende Namen, Strukturprobleme usw. bereitstellen. Er hilft bei der Überprüfung des programmgesteuerten Zugriffs und umfasst erweiterte Funktionen für die Automatisierung von Barrierefreiheits Tests.
- [Benutzeroberflächenautomatisierungs-Überprüfung](/windows/desktop/winauto/ui-automation-verify): ein Framework für manuelle und automatisierte Tests der Benutzeroberflächenautomatisierungs-Implementierung in einem Steuerelement oder einer Anwendung (Ergebnisse können protokolliert werden). Sie können Ihre Anwendung in den Testcode integrieren und regelmäßige, automatisierte Tests oder Überprüfungen der Benutzeroberflächenautomatisierungs-Szenarios durchführen. Mit diesem Tool können Sie überprüfen, ob Änderungen an Anwendungen mit bewährten Features keine neuen Probleme oder Regressionen in Bereichen aufweisen, die über die neuen Features hinausgehen.
