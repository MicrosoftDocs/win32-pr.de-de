---
title: Barrierefreiheit und globaler Support
description: Die Windows 7-Plattform erleichtert die Erstellung von Lösungen, auf die mehr Benutzer zugreifen können und die die Compliancestandards für Barrierefreiheit erfüllen oder überschreiten.
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
# <a name="accessibility-and-global-support"></a>Barrierefreiheit und globaler Support

Die Windows 7-Plattform erleichtert die Erstellung von Lösungen, auf die mehr Benutzer zugreifen können und die die Compliancestandards für Barrierefreiheit erfüllen oder überschreiten. Die AtV-Community (Assistive Technology Vendor) kann jetzt Lösungen für eine größere Bandbreite von Clientanwendungen erstellen, und Anwendungsentwickler werden es einfacher finden, barrierefreie Benutzeroberflächen zu erstellen und zu überprüfen.

Windows 7 vereinfacht auch die Unterstützung mehrerer globaler Sprachen als in früheren Versionen von Windows. Ab dem Zeitpunkt, zu dem ein Benutzer eine Sprache und einen Standort auswählt, zeigt Windows 7 Datumsangaben, Zahlen, Kalender, Sortierungen und andere Informationen an, indem die von Kunden erwarteten Kulturkonventionen verwendet werden.

## <a name="windows-automation"></a>Windows Automatisierung

Windows 7 bietet eine umfassende, standardbasierte Automatisierungsschicht, die für native Anwendungen erweitert wird. Es baut auf Microsoft Active Accessibility und Microsoft Benutzeroberflächenautomatisierung auf. Es ist auch für die Arbeit mit Branchenstandards wie W3C Web ARIA (Accessible Rich Internet Application) und *Section 508 Specifications* konzipiert.

Benutzeroberflächenautomatisierung bietet eine verbesserte Leistung durch die Einführung schnellerer nicht verwalteter Automatisierungsproxys für Microsoft Win32-Steuerelemente und Ältere Microsoft Active Accessibility *(MSAA)-Anwendungen* sowie bessere und schnellere Benutzeroberflächenautomatisierung Ereignis- und Proxyregistrierungen. Neue Erweiterbarkeitsfeatures erweitern Steuerelementmuster, Eigenschaften und benutzerdefinierte Ereignisse. (Siehe [Windows Automation-API: Übersicht](../winauto/windows-automation-api-overview.md).)

## <a name="accessibility-support-tools"></a>Tools zur Unterstützung der Barrierefreiheit

Die Benutzeroberflächen-Barrierefreiheitsprüfung ist ein praktisches grafisches Benutzeroberflächentool, mit dem Entwickler und Tester schnell überprüfen können, ob ihre Benutzeroberfläche den wichtigen Barrierefreiheitsanforderungen entspricht, z. B. *MSAA* (mit der Beziehungen zwischen untergeordneten Übergeordneten oder umschließenden Rechtecke überprüft werden) und programmgesteuerten Zugriff, Ereignisgenerierung, Layout und Tastaturnavigation Benutzeroberflächenautomatisierung. (Weitere Informationen finden Sie unter [Ui Accessibility Checker](https://www.codeplex.com/AccCheck).)

UIA Verify ist ein Testautomatisierungsframework, das manuelle und automatisierte Tests der Benutzeroberflächenautomatisierung Anbieterimplementierungen eines Steuerelements oder einer Anwendung ermöglicht. Mit diesen beiden neuen Tools können Entwickler Implementierungen und Funktionen für die Barrierefreiheit in Anwendungen testen, die *MSAA* oder Benutzeroberflächenautomatisierung verwenden. Beide Tools sind über [CodePlex](https://www.codeplex.com/)verfügbar, eine Website, die Von Microsoft erstellt wurde, um Open-Source-Projekte zu hosten und die Entwicklercommunity besser zu unterstützen. (Siehe [Benutzeroberflächenautomatisierung Verify (UIA Verify) Test Automation Framework](https://uiautomationverify.codeplex.com/).)

## <a name="improved-multi-language-user-interface-support-and-linguistic-services"></a>Verbesserte Unterstützung für Benutzeroberfläche und linguistische Dienste in mehreren Sprachen

Windows 7 bietet Entwicklern eine Standardmethode zur Vorbereitung ihrer Anwendungen auf den internationalen Markt, indem sie eine verbesserte Unterstützung der mehrsprachigen Benutzeroberfläche und linguistische Dienste bereitstellen, die sie in ihren Anwendungen verwenden können.

Erweiterte linguistische Dienste ist ein neues Feature in Windows 7, mit dem Entwickler die gleichen kleinen APIs verwenden können, um eine Vielzahl erweiterter linguistischer Funktionen zu nutzen. Mit erweiterten linguistischen DienstenAPIs in Windows 7 können Entwickler die Sprache jedes Unicode-Texts automatisch erkennen und diese Informationen verwenden, um kunden weltweit intelligentere Benutzerfreundlichkeitsoptionen zu treffen. Erweiterte linguistische Dienste bieten auch integrierte Transliterationsunterstützung, die Text von einem Schreibsystem in ein anderes konvertiert. So können Entwickler text jetzt beispielsweise automatisch zwischen vereinfachtem und traditionellem Chinesisch konvertieren, um Menschen bei der Kommunikation über linguistische Grenzen hinweg zu unterstützen. Durch die Verwendung erweiterter linguistischer DiensteAPIs können Entwickler vorhandene erweiterte linguistische Dienste verwenden und in Zukunft neue Dienste nutzen, ohne neuen Code zu lernen. (Siehe [Erweiterte linguistische Dienste](../intl/extended-linguistic-services.md).)

 

 