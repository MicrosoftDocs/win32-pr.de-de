---
title: Barrierefreiheitstools – AccChecker (UI Accessibility Checker)
description: Beschreibt AccChecker (UI Accessibility Checker), ein Tool zum Testen der MSAA-Implementierung (Benutzeroberflächenautomatisierung oder Microsoft Active Accessibility-Implementierung einer Anwendung.
ms.assetid: 92155984-356A-4774-A99D-35B15A3BB704
keywords:
- UI Accessibility Checker
- AccChecker
- Benutzeroberflächenautomatisierung-Implementierung,Testen
- UIA-Implementierung, Testen
- Microsoft Active Accessibility-Implementierung,Testen
- MSAA-Implementierung,Testen
- Testen Benutzeroberflächenautomatisierung
- Testen der UIA
- Testen Microsoft Active Accessibility
- Testen von MSAA
- UIA-Testtools
- Benutzeroberflächenautomatisierung Testtools
- MSAA-Testtools
- Microsoft Active Accessibility Testtools
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 452ff74140b50f1f6ea6d5357187e42ecff2d83cc85076d11ff22e191da7f3ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052408"
---
# <a name="accessibility-tools---accchecker-ui-accessibility-checker"></a>Barrierefreiheitstools – AccChecker (UI Accessibility Checker)

**AccChecker** (UI Accessibility Checker) überprüft, ob die wichtigsten Anforderungen an die Barrierefreiheit der Benutzeroberfläche beim Entwurf und der Implementierung von Benutzeroberflächenautomatisierung (UIA) oder Microsoft Active Accessibility (MSAA) unabhängig vom zugrunde liegenden UI-Framework erfüllt werden. **AccChecker umfasst** auch eine Reihe von Überprüfungen der Webbarrierefreiheit.

**AccChecker** bietet die folgenden Funktionalitätsebenen:

- Eine Windows GUI-Anwendung, die manuelle Tests, Nachrichtenprotokollierung und Unterdrückungsgenerierung unterstützt.
- Eine API zur Verwendung in automatisierten Testframeworks.
- Eine Konsolenanwendung, die nicht verwaltete Testautomatisierungen für Szenarien unterstützt, in denen die verwaltete **AccChecker-API** nicht verwendet werden kann.

Alle Ebenen der **AccChecker-Funktionalität** bieten Routinen zum Überprüfen des Microsoft Active Accessibility programmgesteuerten Zugriffs, der programmgesteuerten Ereignisgenerierung, des Steuerelementlayouts und der Tastaturnavigation. **AccChecker bietet** auch einen einfachen Dienst für die Sprachausgabetranskription.

**AccChecker** wird mit dem Windows Software Development Kit (SDK) installiert. Sie befindet sich im Ordner \\ \\ < accChecker *der Bin-Versionsplattform* > \\ <  > \\ des SDK-Installationspfads.

> [!NOTE]
> **AccChecker ist** ein Legacytool. Es wird empfohlen, [stattdessen Insights](https://accessibilityinsights.io/) Barrierefreiheit zu verwenden.

## <a name="requirements"></a>Anforderungen

Erfordert .NET Framework 2.0 oder höher.

**AccChecker kann** verwendet werden, um Barrierefreiheitsdaten auf Systemen zu untersuchen, die nicht über Microsoft Benutzeroberflächenautomatisierung verfügen, sondern nur die eigenschaften Microsoft Active Accessibility können. Um die Benutzeroberflächenautomatisierung, Benutzeroberflächenautomatisierung auf dem System vorhanden sein. Weitere Informationen finden Sie im Abschnitt "Anforderungen" [Benutzeroberflächenautomatisierung](entry-uiauto-win32.md).

**AccChecker** wird als Teil der gesamten Tools imWindows SDK installiert und nicht als separater EXE-Download verteilt. Das Windows SDK enthält alle in diesem Abschnitt dokumentierten Tools zur Barrierefreiheit. [Hier finden Sie Windows SDK.](https://developer.microsoft.com/) (Es gibt auch ein SDK-Downloadarchiv, das von dieser Seite aus verknüpft ist, wenn Sie eine frühere Version benötigen.)

## <a name="related-topics"></a>Zugehörige Themen

- [Überwachung für barrierefreie Ereignisse](accessible-event-watcher.md)
- [Überprüfen](inspect-objects.md)
- [Testtools](testing-tools.md)
- [Benutzeroberflächenautomatisierungs-Überprüfung](ui-automation-verify.md)
