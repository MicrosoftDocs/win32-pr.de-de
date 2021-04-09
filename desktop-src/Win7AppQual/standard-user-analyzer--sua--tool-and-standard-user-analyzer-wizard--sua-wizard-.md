---
description: Erfahren Sie, wie Sie mit dem Tool "Standard User Analyzer" (SUA) und dem SUA-Assistenten Ihre Anwendungen testen und potenzielle Kompatibilitätsprobleme erkennen.
ms.assetid: 229ee531-32b9-4e11-b64c-3ce5b5ab6530
title: Standardbenutzeranalyse-Tool (Standard User Analyzer, SUA) und SUA-Assistent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc0e729c37ff1650f0dab7f3dd1c05ffb4b5f370
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2021
ms.locfileid: "104050658"
---
# <a name="standard-user-analyzer-sua-tool-and-standard-user-analyzer-wizard-sua-wizard"></a>Standardbenutzeranalyse-Tool (Standard User Analyzer, SUA) und SUA-Assistent

## <a name="affected-platforms"></a>Betroffene Plattformen

**Clients:** Windows XP \| Windows Vista \| Windows 7  
**Server:** Windows Server 2003 \| Windows Server 2008 \| Windows Server 2008 R2  

## <a name="description"></a>BESCHREIBUNG

Das Anwendungskompatibilitäts-Toolkit umfasst das Tool "Standard User Analyzer" (SUA) und den standardmäßigen benutzeranalyseassistenten (SUA Wizard). Mit diesen Tools können Sie Ihre Anwendungen testen und API-Aufrufe überwachen, um potenzielle Kompatibilitätsprobleme aufgrund der Benutzerkontensteuerung (User Account Control, UAC) im Windows 7-Betriebssystem zu erkennen.

UAC, früher als "eingeschränktes Benutzerkonto (LUA)" bezeichnet, erfordert, dass alle Benutzer (einschließlich der Mitglieder der Administrator Gruppe) als Standard Benutzer ausgeführt werden, indem Sie das Dialogfeld "Sicherheits Aufforderung" verwenden, bis die Anwendung absichtlich erhöht wird. Anwendungen, die Zugriff und Berechtigungen für Speicherorte benötigen, die für einen Standardbenutzer nicht verfügbar sind, können jedoch nicht ordnungsgemäß mit der Standard Benutzerrolle ausgeführt werden.

## <a name="usage"></a>Verbrauch

Die folgenden Abschnitte enthalten ausführliche Informationen zur Verwendung der Tools des SUA-und SUA-Assistenten.

**SUA-Tool**

Mit dem SUA-Tool können Sie eine Anwendung analysieren, einen ausführlichen Bericht zu den UAC-bezogenen Problemen überprüfen und dann die vorgeschlagenen und ausgewählten Anwendungs entschärfungen anwenden, wie im folgenden Flussdiagramm dargestellt.

![Diagramm, das den Flow des S U A-Tools anzeigt.](images/act-suaflowchart-appcookbook.gif)

*SUA-Tool und Virtualisierung*

Nur das SUA-Tool ermöglicht es Ihnen, das Virtualisierungsfeature zu aktivieren und zu deaktivieren. Wenn Sie das Virtualisierungsfeature ausschalten, verhält sich die getestete Anwendung mehr, als Sie im Windows XP-Betriebssystem funktioniert.

*SUA-Tool und erweiterte Berechtigungen*

Nur das SUA-Tool ermöglicht Ihnen das Aktivieren und Deaktivieren der Funktion zum **starten mit erhöhten** rechten. Mit dem Feature "mit erhöhten Rechten starten" kann die ausgewählte Anwendung als Administrator oder als Standard Benutzer ausgeführt werden. Abhängig von Ihrer Auswahl finden Sie verschiedene Typen von UAC-bezogenen Problemen. Wenn Sie das Kontrollkästchen mit **erhöhten Rechten starten** deaktivieren, wird Ihre Anwendung mit vollen Administrator Rechten ausgeführt, wodurch SUA die Probleme vorhersagen kann, die für einen Standard Benutzer auftreten können. Wenn Sie das Kontrollkästchen mit erhöhten Rechten starten aktivieren, werden Fehler angezeigt, die sich aus der eigentlichen Anwendung ergeben und Fehler erzeugen.

**SUA-Assistent**

Der SUA-Assistent ermöglicht es Ihnen, einen schrittweisen Prozess zu befolgen, mit dem Sie eine Anwendung analysieren und dann die vorgeschlagenen und ausgewählten Anwendungs entschärfungen anwenden können, wie im folgenden Flussdiagramm dargestellt. Im Gegensatz zum SUA-Tool ermöglicht der Assistent keine Überprüfung der detaillierten UAC-bezogenen Probleme.

![Diagramm, das den Flow des S U A-Assistenten anzeigt.](images/act-suaflowchart-appcookbook.gif)

## <a name="links-to-other-resources"></a>Links zu anderen Ressourcen

-   [Anwendungskompatibilitäts-Toolkit Download](/windows-hardware/get-started/adk-install)
-   [Grundlegendes zu den Standard Tools für die Benutzer Analyse](/previous-versions/windows/it-pro/windows-7/cc838047(v=ws.10))
-   [Technische Referenz für Standard Benutzer Analyse](/previous-versions/windows/it-pro/windows-7/cc765948(v=ws.10))
-   [Testen und Beheben von Problemen mithilfe der Entwicklungs Tools](/previous-versions/orphan-topics/ws.10/cc766461(v=ws.10))
-   [Anwendungs Kompatibilität und Benutzerkontensteuerung](/previous-versions/windows/)

> [!Note]  
> Diese Ressourcen sind in einigen Sprachen und Ländern bzw. Regionen möglicherweise nicht verfügbar.

 

 

 
