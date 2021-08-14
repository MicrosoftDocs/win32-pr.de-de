---
title: Barrierefreiheit und globale Unterstützung
description: Die Windows 7-Plattform erleichtert das Erstellen von Lösungen, die für mehr Benutzer zugänglich sind und die Compliancestandards für die Barrierefreiheit erfüllen oder überschreiten.
ms.assetid: bcad2f00-7885-461c-a2dc-0a0a176962b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 320f6e52dba4f2a6d9c89a7bdea287e948a1bca048b0d3e88a2a8978e8085d0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118709117"
---
# <a name="accessibility-and-global-support"></a>Barrierefreiheit und globale Unterstützung

Die Windows 7-Plattform erleichtert das Erstellen von Lösungen, die für mehr Benutzer zugänglich sind und die Compliancestandards für die Barrierefreiheit erfüllen oder überschreiten. Die Community des Hilfstechnologieanbieters (ATV) kann jetzt Lösungen für eine größere Vielfalt von Clientanwendungen erstellen, und Anwendungsentwickler finden es einfacher, barrierefreie Benutzeroberflächen zu erstellen und zu überprüfen.

Windows 7 erleichtert auch die Unterstützung mehrerer globaler Sprachen als in früheren Versionen von Windows. Ab dem Zeitpunkt, zu dem ein Benutzer eine Sprache und einen Standort auswählt, Windows 7 Datumsangaben, Zahlen, Kalender, Sortierungen und andere Informationen anhand der kulturellen Konventionen, die Kunden erwarten.

## <a name="windows-automation"></a>Windows Automatisierung

Windows 7 bietet eine umfangreiche, standardbasierte Automatisierungsebene, die für native Anwendungen erweitert wird. Er baut auf Microsoft Active Accessibility und Microsoft Benutzeroberflächenautomatisierung. Es ist auch für die Verwendung mit Branchenstandards wie W3C Web ARIA (Accessible Rich Internet Application) und Section 508 Specifications (Spezifikationen von Abschnitt *508) konzipiert.*

Benutzeroberflächenautomatisierung bietet eine verbesserte Leistung durch die Einführung schnellerer nicht verwalteter Automatisierungsproxys für Microsoft Win32-Steuerelemente und ältere Microsoft Active Accessibility -Anwendungen *(MSAA)* sowie bessere und schnellere Benutzeroberflächenautomatisierung-Ereignis- und Proxyregistrierungen. Neue Erweiterbarkeitsfunktionen erweitern Steuerelementmuster, Eigenschaften und benutzerdefinierte Ereignisse. (Siehe [Windows Automation-API: Übersicht](../winauto/windows-automation-api-overview.md).)

## <a name="accessibility-support-tools"></a>Unterstützungstools für Barrierefreiheit

Die Benutzeroberflächen-Barrierefreiheitsprüfung ist ein praktisches grafisches Benutzeroberflächentool, mit dem Entwickler und Tester schnell überprüfen können, ob ihre Benutzeroberfläche den wichtigsten Anforderungen an die Barrierefreiheit entspricht, z. B. *MSAA* (zum Überprüfen von Beziehungen zwischen untergeordneten übergeordneten Elementen oder begrenzungsbasierten Rechtecke) und Benutzeroberflächenautomatisierung programmgesteuertem Zugriff, Ereignisgenerierung, Layout und Tastaturnavigation. (Weitere Informationen [finden Sie unter Ui Accessibility Checker](https://www.codeplex.com/AccCheck).)

UIA Verify ist ein Testautomatisierungsframework, das manuelle und automatisierte Tests der Benutzeroberflächenautomatisierung-Anbieterimplementierung eines Steuerelements oder einer Anwendung ermöglicht. Mit diesen beiden neuen Tools können Entwickler Implementierungen und Funktionen für Barrierefreiheit in Anwendungen testen, die *entweder MSAA* oder Benutzeroberflächenautomatisierung. Beide Tools sind über [CodePlex](https://www.codeplex.com/)verfügbar, eine Website, die Microsoft erstellt hat, um Open-Source-Projekte zu hosten und die Entwickler-Community besser zu bedienen. (Siehe [Benutzeroberflächenautomatisierung Überprüfen (UIA Verify) Test Automation Framework](https://uiautomationverify.codeplex.com/).)

## <a name="improved-multi-language-user-interface-support-and-linguistic-services"></a>Verbesserte Unterstützung für mehrsprachige Benutzeroberfläche und linguistische Dienste

Windows 7 bietet Entwicklern eine Standardmethode, um ihre Anwendungen für den internationalen Markt vorzubereiten, indem sie eine verbesserte Unterstützung für mehrsprachige Benutzeroberflächen und linguistische Dienste bereitstellen, die sie in ihren Anwendungen verwenden können.

Erweiterte linguistische Dienste ist ein neues Feature in Windows 7, mit dem Entwickler denselben kleinen Satz von APIs verwenden können, um eine Vielzahl erweiterter linguistischer Funktionen zu nutzen. Mit erweiterten linguistischen DienstenAPIs in Windows 7 können Entwickler die Sprache jedes Unicode-Texts automatisch erkennen und diese Informationen verwenden, um Kunden auf der ganzen Welt eine intelligentere Benutzererfahrung zu ermöglichen. Erweiterte linguistische Dienste bieten auch integrierte Transliterationsunterstützung, die Text von einem Schreibsystem in ein anderes konvertiert. Entwickler können text jetzt beispielsweise automatisch zwischen vereinfachtem und traditionellem Chinesisch konvertieren, um Menschen zu helfen, über linguistische Grenzen hinweg miteinander zu kommunizieren. Mit erweiterten linguistischen DienstenAPIs können Entwickler vorhandene erweiterte linguistische Dienste verwenden und in Zukunft neue Dienste nutzen, ohne neuen Code erlernen zu müssen. (Siehe [Erweiterte linguistische Dienste](../intl/extended-linguistic-services.md).)

 

 