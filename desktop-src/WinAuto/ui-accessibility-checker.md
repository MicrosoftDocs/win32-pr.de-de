---
title: Barrierefreiheits Tools-accchecker (UI-Zugriffs Prüfung)
description: Beschreibt die Zugriffs Prüfung (UI-Zugriffs Überprüfung), ein Tool zum Testen der Benutzeroberflächenautomatisierungs-oder Active Accessibility Microsoft-Implementierung (MSAA) einer Anwendung.
ms.assetid: 92155984-356A-4774-A99D-35B15A3BB704
keywords:
- UI Accessibility Checker
- Zugriffs Prüfung
- Implementierung der Benutzeroberflächen Automatisierung, testen
- UIA-Implementierung, testen
- Microsoft Active Accessibility-Implementierung, testen
- MSAA-Implementierung, testen
- Testen der Benutzeroberflächen Automatisierung
- Testen von UIA
- Testen von Microsoft Active Accessibility
- Testen von MSAA
- UIA-TestTools
- Benutzeroberflächenautomatisierungs-TestTools
- MSAA-TestTools
- Microsoft Active Accessibility TestTools
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49d2b85436735bfa08f8fc73cf4e465b11d71630
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "106341290"
---
# <a name="accessibility-tools---accchecker-ui-accessibility-checker"></a>Barrierefreiheits Tools-accchecker (UI-Zugriffs Prüfung)

Die **Zugriffs** Prüfung (UI-Zugriffs Prüfung) überprüft, ob die erforderlichen Barrierefreiheits Anforderungen der Benutzeroberfläche bei der Entwicklung und Implementierung von Benutzeroberflächen Automatisierung (UIA) oder Microsoft Active Accessibility (MSAA) unabhängig vom zugrunde liegenden Benutzeroberflächen Framework erfüllt werden. Die **Zugriffs** Prüfung umfasst auch eine Reihe von webbarrierefreiheits Überprüfungen.

**Accchecker** bietet die folgenden Ebenen der Funktionalität:

- Eine Windows-GUI-Anwendung, die manuelle Tests, Nachrichten Protokollierung und Unterdrückungs Generierung unterstützt.
- Eine API zur Verwendung in automatisierten Test-Frameworks.
- Eine Konsolenanwendung, die nicht verwaltete Test Automatisierungen für Szenarien unterstützt, in denen die von der **accchecker** verwaltete API nicht verwendet werden kann.

Alle Ebenen der **accchecker** -Funktionalität stellen Routinen zum Überprüfen von Microsoft Active Accessibility programmgesteuerten Zugriff, programmgesteuerte Ereignis Generierung, Steuerelement Layout und Tastaturnavigation bereit. **Accchecker** bietet auch einen grundlegenden Screenreader-Transkriptions Dienst.

**Accchecker** wird mit dem Windows Software Development Kit (SDK) installiert. Sie befindet sich im \\ Ordner "bin \\ < *Version* > \\ < *Platform* > \\ accchecker" des SDK-Installations Pfads.

> [!NOTE]
> **Accchecker** ist ein Legacy Tool. Stattdessen wird die [](https://accessibilityinsights.io/) Verwendung von eingabeinsights empfohlen.

## <a name="requirements"></a>Anforderungen

Erfordert .NET Framework 2,0 oder höher.

Die **Zugriffs** Prüfung kann verwendet werden, um Barrierefreiheits Daten auf Systemen zu untersuchen, die nicht über Microsoft-Benutzeroberflächen Automatisierung verfügen, aber nur die Eigenschaften von Microsoft Active Accessibility untersuchen Zum Untersuchen der Benutzeroberflächen Automatisierung muss die Benutzeroberflächen Automatisierung auf dem System vorhanden sein. Weitere Informationen finden Sie im Abschnitt "Anforderungen" unter [UI Automation](entry-uiauto-win32.md).

Die **Zugriffs** Prüfung wird als Teil der Gesamtmenge der Tools im Windows SDK installiert und nicht als separater Download der exe-Datei verteilt. Die Windows SDK umfasst alle Tools für die Barrierefreiheit, die in diesem Abschnitt dokumentiert sind. [Holen Sie sich den Windows SDK.](https://developer.microsoft.com/) (Es gibt auch ein SDK-Download Archiv, das von dieser Seite verknüpft ist, wenn Sie eine vorherige Version benötigen.)

## <a name="related-topics"></a>Zugehörige Themen

- [Überwachung für barrierefreie Ereignisse](accessible-event-watcher.md)
- [Überprüfen](inspect-objects.md)
- [TestTools](testing-tools.md)
- [Benutzeroberflächenautomatisierungs-Überprüfung](ui-automation-verify.md)
