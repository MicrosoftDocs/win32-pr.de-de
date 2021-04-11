---
title: Testtools
description: Beschreibt Tools zum Testen der Barrierefreiheits Implementierung Ihrer Anwendung, um sicherzustellen, dass Client Anwendungen vollständig auf die Benutzeroberfläche zugreifen können, sowie für Benutzer, die über die Tastatur auf Ihre Anwendung zugreifen.
ms.assetid: abacbec4-6ccd-4853-afcd-a92a6656f393
keywords:
- Tools für die Barrierefreiheit
- Testtools, Barrierefreiheit
- Barrierefreiheits Tests
- UIA
- MSAA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce653adb2602b8fdd46bebb72d3a7607185ffd84
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102258"
---
# <a name="testing-tools"></a>Testtools

Programm gesteuerter Zugriff und Tastatur Zugriff sind wichtige Anforderungen für die Unterstützung von Barrierefreiheit in Ihrer Anwendung. Ohne ausreichenden Zugriff könnten viele Benutzer von Hilfstechnologien (bei), wie z. b. Bildschirm Lese-und Bildschirmtastatur Benutzer, Ihre Anwendung nicht verwenden. Stellen Sie sicher, dass Sie die Barrierefreiheits Implementierung Ihrer Anwendung gründlich testen, um zu bestätigen, dass Sie angemessene Informationen zu den Benutzeroberflächen Elementen bereitstellt und dass alle Anwendungsszenarien nur mit der Tastatur erreicht werden können.

Zusätzlich zur Überprüfung des programmgesteuerten Zugriffs können einige Tools Ihnen helfen, die Implementierung des Tastatur Zugriffs Ihrer Anwendung zu bewerten. Die Tools allein sind jedoch nicht ausreichend. Es ist wichtig, manuell zu überprüfen, ob alle Szenarien nur mit der Tastatur erreicht werden können.

Für programmgesteuerte und Tastatur Anforderungen gibt es kein Tool, mit dem Sie Ihre vollständige Implementierung überprüfen können. Versuchen Sie, eine Reihe von Tools zu verwenden, um Ihre Implementierung zu überprüfen und nach Möglichkeit Benutzer von Hilfstechnologien, wie z. b. Sprachausgabe, zu finden, um Ihre Benutzeroberfläche zu verwenden.

In diesem Abschnitt werden die verfügbaren Tools zum Testen von Microsoft UI Automation (UIA) und Microsoft Active Accessibility-Implementierungen (MSAA) beschrieben.

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

- [**Barrierefreie Ereignis**](accessible-event-watcher.md)Überwachung: das Tool "Barrierefreie Ereignisüberwachung" (AccEvent) prüft Barrierefreiheits Daten, um die Benutzeroberflächen Elemente der Anwendung zu validieren, um sicherzustellen, dass die Benutzeroberflächen Elemente beim Auftreten von Benutzeroberflächen Änderungen ordnungsgemäße Ereignisse von Microsoft Active Accessibility und Benutzeroberflächen Automatisierung AccEvent wird normalerweise zum Debuggen von Problemen und zum Überprüfen verwendet, ob benutzerdefinierte und erweiterte Steuerelemente ordnungsgemäß funktionieren.

- Über [**prüfen: Überprüfen Sie**](inspect-objects.md), wie Sie die Barrierefreiheits Daten in beliebigen Benutzeroberflächen Elementen anzeigen können. Dies ist besonders nützlich, wenn ein gemeinsames Steuerelement erweitert oder ein benutzerdefiniertes Steuerelement erstellt wird, um sicherzustellen, dass Eigenschaften und Steuerelement Muster korrekt festgelegt sind

- [**Accscope**](accscope.md): das accscope-Tool ermöglicht Entwicklern, den Zugriff auf die Anwendung während der frühen Entwurfs-und Entwicklungsphasen visuell zu evaluieren. Mit accscope können Sie visualisieren, wie eine Sprachausgabe Informationen zur Benutzeroberflächen Automatisierung verwendet, die eine APP bereitstellt. Es können Bereiche angezeigt werden, in denen das Hinzufügen von Informationen oder Unterstützung für Ihre Anwendung den Zugriff verbessert.

- [**UI-Barrierefreiheits**](ui-accessibility-checker.md)Prüfung: das Tool zur Überprüfung der Benutzeroberfläche überprüft, ob die wichtigsten Anforderungen der Benutzeroberflächen Barrierefreiheit erfüllt werden. Die Zugriffs Prüfung umfasst überprüfungsprüfungen für die Benutzeroberflächen Automatisierung, Microsoft Active Accessibility und barrierefreie Internet Anwendungen (Aria). Es kann eine statische Prüfung bereitstellen, die auf Fehler, wie z. b. fehlende Namen, Strukturprobleme usw., sucht. Sie hilft bei der Überprüfung des programmgesteuerten Zugriffs und bietet erweiterte Funktionen zur Unterstützung der Automatisierung von Barrierefreiheits Tests

- [**Benutzeroberflächenautomatisierungs**](ui-automation-verify.md)-Überprüfung: UI Automation Verify (UIA Verify) ist ein Test Framework für manuelle und automatisierte Tests der Benutzeroberflächen Automatisierung eines Steuer Elements oder einer Anwendung. Außerdem können die Testergebnisse protokolliert werden. Sie können Ihre Anwendung in den Testcode integrieren und regelmäßige, automatisierte Tests oder Überprüfungen der Benutzeroberflächenautomatisierungs-Szenarios durchführen. Mit diesem Tool können Sie überprüfen, ob Änderungen an Anwendungen mit etablierten Features keine neuen Probleme oder Regressionen in Bereichen aufweisen, die über die neuen Features hinausgehen.

### <a name="obsolete-tools"></a>Veraltete Tools

Die Tools für den **zugänglichen Explorer** und die Benutzeroberflächen- **Spy** sind veraltet und nicht mehr verfügbar. Verwenden Sie stattdessen über [**prüfen**](inspect-objects.md) oder [**accscope**](accscope.md) .

## <a name="related-topics"></a>Zugehörige Themen

- [Entwickler-Hub für Barrierefreiheit](https://developer.microsoft.com/windows/accessible-apps)
- [Barrierefreiheit von Microsoft](https://www.microsoft.com/accessibility/)