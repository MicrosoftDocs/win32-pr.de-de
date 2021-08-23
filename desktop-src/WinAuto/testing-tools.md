---
title: Testtools
description: Beschreibt Tools zum Testen der Implementierung der Barrierefreiheit Ihrer Anwendung, um sicherzustellen, dass clientanwendungen und Benutzer, die über die Tastatur auf Ihre Anwendung zugreifen, voll auf die Benutzeroberfläche zugreifen können.
ms.assetid: abacbec4-6ccd-4853-afcd-a92a6656f393
keywords:
- Tools zum Testen der Barrierefreiheit
- Testtools,Barrierefreiheit
- Barrierefreiheitstests
- UIA
- MSAA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fcd5d8b0777eb80cf5b2935cc8652d328dfc219cb56bc654c1eeae0761bbd89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133593"
---
# <a name="testing-tools"></a>Testtools

Programmgesteuerter Zugriff und Tastaturzugriff sind wichtige Anforderungen für die Unterstützung der Barrierefreiheit in Ihrer Anwendung. Ohne angemessenen Zugriff können viele Benutzer der Hilfstechnologie (AT), z. B. Sprachausgabe und Benutzer auf der Bildschirmtastatur, Ihre Anwendung nicht verwenden. Stellen Sie sicher, dass Sie die Implementierung der Barrierefreiheit Ihrer Anwendung gründlich testen, um sicherzustellen, dass sie ausreichende Informationen zu ihren Benutzeroberflächenelementen liefert und dass alle Ihre Anwendungsszenarien nur mit der Tastatur durchgeführt werden können.

Zusätzlich zur Überprüfung des programmgesteuerten Zugriffs können einige der Tools Ihnen helfen, die Implementierung des Tastaturzugriffs Ihrer Anwendung zu bewerten. Tools allein reichen jedoch nicht aus. Es ist wichtig, manuell zu überprüfen, ob alle Szenarien nur mit der Tastatur durchgeführt werden können.

Für programmgesteuerte und Tastaturanforderungen gibt es kein Tool, das Ihre vollständige Implementierung überprüfen kann. Versuchen Sie, eine Vielzahl von Tools zu verwenden, um Ihre Implementierung zu überprüfen, und suchen Sie nach Möglichkeit Benutzer von Hilfstechnologien, z. B. Sprachbildschirme, um Ihre Benutzeroberfläche zu verwenden.

In diesem Abschnitt werden die verfügbaren Tools zum Testen von Microsoft Benutzeroberflächenautomatisierung-Implementierungen (UIA) und Microsoft Active Accessibility (MSAA) beschrieben.

## <a name="tools"></a>Tools

[Barrierefreiheit Insights:](https://accessibilityinsights.io/) Unterstützt Entwickler beim Suchen und Beheben von Barrierefreiheitsproblemen sowohl auf Websites als auch Windows Anwendungen.

- [Accessibility Insights for Web](https://accessibilityinsights.io/docs/web/overview) ist eine Erweiterung für Chrome und [Microsoft Edge Insider,](https://www.microsoftedgeinsider.com) mit der Entwickler Barrierefreiheitsprobleme in Web-Apps und Websites finden und beheben können. Es werden zwei primäre Szenarien unterstützt:
  - **FastPass:** Ein schlanker, zweistufiger Prozess, mit dem Entwickler häufige Probleme mit der Barrierefreiheit mit hohem Einfluss in weniger als fünf Minuten identifizieren können.  
  - **Bewertung:** Hiermit kann jeder überprüfen, ob eine Website zu 100 % mit den Standards und Richtlinien für die Barrierefreiheit konform ist. [Mit Insights](https://accessibilityinsights.io/) können Sie auch Benutzeroberflächenautomatisierung Elemente, Eigenschaften, Steuerelementmuster und Ereignisse überprüfen (ähnlich wie die Legacytools [Inspect](/windows/desktop/winauto/inspect-objects) und [AccEvent,](/windows/desktop/winauto/accessible-event-watcher) die im folgenden Abschnitt beschrieben werden).

- [Die Insights für Windows](https://accessibilityinsights.io/docs/windows/overview) Barrierefreiheitstools hilft Entwicklern dabei, Probleme mit der Barrierefreiheit in Windows zu beheben. Das Tool unterstützt drei primäre Szenarien:
  - **Mit Live Inspect** können Entwickler überprüfen, ob ein Element in einer App über die richtigen Benutzeroberflächenautomatisierung verfügt, indem sie einfach auf das Element bewegen oder den Tastaturfokus darauf festlegen.
  - **FastPass:** Ein schlanker, zweistufiger Prozess, mit dem Entwickler häufige Probleme mit der Barrierefreiheit mit hohem Einfluss in weniger als fünf Minuten identifizieren können.
  - **Mit der** Problembehandlung können Sie bestimmte Probleme mit der Barrierefreiheit diagnostizieren und beheben.

### <a name="legacy-testing-tools"></a>Legacytesttools

Die folgenden Tools sind weiterhin im Windows SDK verfügbar und werden hier für die weitere Unterstützung dokumentiert. Es wird jedoch empfohlen, den Übergang zu [Accessibility Insights.](https://accessibilityinsights.io/)

- [**Accessible Event Watcher:**](accessible-event-watcher.md)Das Accessible Event Watcher-Tool (AccEvent) untersucht Barrierefreiheitsdaten, um Elemente der Anwendungsbenutzeroberfläche zu überprüfen, um sicherzustellen, dass die Benutzeroberflächenelemente ordnungsgemäße Microsoft Active Accessibility- und Benutzeroberflächenautomatisierung-Ereignisse ausgelöst werden, wenn Änderungen der Benutzeroberfläche auftreten. AccEvent wird normalerweise verwendet, um Probleme zu debuggen und zu überprüfen, ob benutzerdefinierte und erweiterte Steuerelemente ordnungsgemäß funktionieren.

- [**Überprüfen:**](inspect-objects.md)Mit Inspect können Sie die Barrierefreiheitsdaten in einem beliebigen Benutzeroberflächenelement anzeigen. Es ist besonders nützlich, wenn Sie ein allgemeines Steuerelement erweitern oder ein benutzerdefiniertes Steuerelement erstellen, um sicherzustellen, dass Eigenschaften und Steuerelementmuster ordnungsgemäß festgelegt werden.

- [**AccScope:**](accscope.md)Mit dem AccScope-Tool können Entwickler den Zugriff auf ihre Anwendung während der frühen Entwurfs- und Entwicklungsphase visuell bewerten. AccScope hilft, zu visualisieren, wie eine Sprachausgabe Benutzeroberflächenautomatisierung von einer App zur Verfügung stellt. Sie kann Bereiche anzeigen, in denen das Hinzufügen von Informationen oder Unterstützung zu Ihrer Anwendung die Barrierefreiheit verbessern kann.

- [**Überprüfung der Barrierefreiheit der**](ui-accessibility-checker.md)Benutzeroberfläche: Das AccChecker-Tool (UI Accessibility Checker) überprüft, ob die wichtigsten Anforderungen an die Barrierefreiheit der Benutzeroberfläche erfüllt sind. AccChecker umfasst Überprüfungen für Benutzeroberflächenautomatisierung, Microsoft Active Accessibility und Accessible Rich Internet Applications (ARIA). Es kann eine statische Überprüfung nach Fehlern wie fehlenden Namen, Strukturproblemen und mehr ermöglichen. Sie hilft bei der Überprüfung des programmgesteuerten Zugriffs und verfügt über erweiterte Features zur Unterstützung der Automatisierung von Barrierefreiheitstests.

- [**Benutzeroberflächenautomatisierung Verify**](ui-automation-verify.md): Benutzeroberflächenautomatisierung Verify (UIA Verify) ist ein Testframework für manuelle und automatisierte Tests der Implementierung eines Steuerelements oder einer Anwendung Benutzeroberflächenautomatisierung. Sie kann auch die Testergebnisse protokollieren. Sie können Ihre Anwendung in den Testcode integrieren und regelmäßige, automatisierte Tests oder Spot-Überprüfungen Ihrer Benutzeroberflächenautomatisierung durchführen. Dieses Tool ist nützlich, um sicherzustellen, dass Änderungen an Anwendungen mit etablierten Features keine neuen Probleme oder Regressionen in Bereichen außerhalb der neuen Features haben.

### <a name="obsolete-tools"></a>Veraltete Tools

Die **Tools Accessible Explorer** und UI **Spy** sind veraltet und nicht mehr verfügbar. Verwenden [**Sie stattdessen Inspect**](inspect-objects.md) oder [**AccScope.**](accscope.md)

## <a name="related-topics"></a>Zugehörige Themen

- [Entwicklerhub für Barrierefreiheit](https://developer.microsoft.com/windows/accessible-apps)
- [Microsoft-Barrierefreiheit](https://www.microsoft.com/accessibility/)