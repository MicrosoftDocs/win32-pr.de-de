---
title: Barrierefreiheit und globaler Support
description: Die Windows 7-Plattform vereinfacht das Erstellen von Lösungen, die für mehr Benutzer zugänglich sind und die Zugriffs Kompatibilitäts Standards erfüllen oder überschreiten.
ms.assetid: bcad2f00-7885-461c-a2dc-0a0a176962b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cea7f710850f419493c5a8435626d163361c8a03
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102074"
---
# <a name="accessibility-and-global-support"></a>Barrierefreiheit und globaler Support

Die Windows 7-Plattform vereinfacht das Erstellen von Lösungen, die für mehr Benutzer zugänglich sind und die Zugriffs Kompatibilitäts Standards erfüllen oder überschreiten. Die Community für hilfstechnologiehersteller (ATV) kann nun Lösungen für eine breitere Palette von Client Anwendungen erstellen, und Anwendungsentwickler werden die Erstellung und Überprüfung zugänglicher Benutzeroberflächen vereinfachen.

Windows 7 erleichtert auch die Unterstützung mehrerer globaler Sprachen als in früheren Versionen von Windows. Ab dem Zeitpunkt, an dem ein Benutzer eine Sprache und einen Speicherort auswählt, zeigt Windows 7 Datumsangaben, Ziffern, Kalender, Sortierungen und andere Informationen mithilfe der von den Kunden erwarteten kulturellen Konventionen an.

## <a name="windows-automation"></a>Windows-Automatisierung

Windows 7 bietet eine umfassende, auf Standards basierende Automatisierungs Schicht, die für native Anwendungen erweitert wird. Es baut auf Microsoft-Active Accessibility und Microsoft-Benutzeroberflächen Automatisierung auf. Sie ist auch für die Verwendung von Branchenstandards wie der W3C-Web-Aria (barrierefreie Internet Anwendung) und den *Spezifikationen von Abschnitt 508* konzipiert.

Die Benutzeroberflächen Automatisierung bietet eine verbesserte Leistung, da schnellere nicht verwaltete Automatisierungs Proxys für Microsoft Win32-Steuerelemente und ältere *MSAA*-Anwendungen (Microsoft Active Accessibility) eingeführt werden und bessere und schnellere Benutzeroberflächenautomatisierungs-Ereignis-und-Proxy Neue Erweiterbarkeits Features erweitern Steuerelement Muster, Eigenschaften und benutzerdefinierte Ereignisse. (Weitere Informationen finden Sie unter [Windows Automation-API: Übersicht](../winauto/windows-automation-api-overview.md).)

## <a name="accessibility-support-tools"></a>Hilfe Tools zur Barrierefreiheit

Die UI-Barrierefreiheits Prüfung ist ein nützliches Tool für die grafische Benutzeroberfläche, mit dem Entwickler und Tester schnell überprüfen können, ob Ihre Benutzeroberfläche den wichtigsten Barrierefreiheits Anforderungen entspricht, wie z. b. *MSAA* (Überprüfen der Beziehungen zwischen übergeordneten und umgebenden Rechtecke) sowie Programm gesteuerter Zugriff, Ereignis Generierung, Layout und Tastaturnavigation. (Siehe [UI-Zugriffs](https://www.codeplex.com/AccCheck)Überprüfung.)

UIA Verify ist ein Test Automatisierungs Framework, das manuelle und automatisierte Tests der Benutzeroberflächenautomatisierungs-Anbieter Implementierung eines Steuer Elements oder einer Anwendung ermöglicht. Diese beiden neuen Tools ermöglichen es Entwicklern, Barrierefreiheits Implementierungen und-Funktionen in Anwendungen zu testen, die entweder *MSAA* oder die Benutzeroberflächen Automatisierung verwenden. Beide Tools sind über [codeplex](https://www.codeplex.com/)verfügbar, eine Website, die Microsoft zum Hosten von Open-Source-Projekten erstellt und die Entwickler Community besser bedient. (Weitere Informationen finden Sie unter [UI Automation Verify (UIA Verify) Test Automation Framework](https://uiautomationverify.codeplex.com/).)

## <a name="improved-multi-language-user-interface-support-and-linguistic-services"></a>Verbesserte Unterstützung für mehrsprachige Benutzeroberflächen und linguistische Dienste

Windows 7 bietet Entwicklern eine Standardmethode zum Vorbereiten Ihrer Anwendungen für den internationalen Markt, indem eine verbesserte Unterstützung für mehrsprachige Benutzeroberflächen und linguistische Dienste bereitgestellt werden, die Sie in Ihren Anwendungen verwenden können.

Erweiterte linguistische Dienste sind ein neues Feature in Windows 7, mit dem Entwickler die gleichen kleinen APIs verwenden können, um eine Vielzahl von erweiterten linguistischen Funktionen nutzen zu können. Durch die Verwendung erweiterter linguistischer servicesapis in Windows 7 können Entwickler die Sprache eines beliebigen Unicode-Texts automatisch erkennen und diese Informationen verwenden, um für Kunden auf der ganzen Welt eine intelligentere Benutzerumgebung zu treffen. Erweiterte linguistische Dienste bieten außerdem integrierte Unterstützung für die Transaktionsunterstützung, die Text von einem Schreibsystem in ein anderes konvertiert. Beispielsweise können Entwickler nun automatisch Text zwischen vereinfachtem und traditionellem Chinesisch konvertieren, um die Kommunikation zwischen den linguistischen Grenzen untereinander zu unterstützen. Durch die Verwendung erweiterter linguistischer servicesapis können Entwickler vorhandene erweiterte linguistische Dienste verwenden und neue Dienste in Zukunft aufnehmen, ohne neuen Code erlernen zu müssen. (Siehe [Erweiterte linguistische Dienste](../intl/extended-linguistic-services.md).)

 

 