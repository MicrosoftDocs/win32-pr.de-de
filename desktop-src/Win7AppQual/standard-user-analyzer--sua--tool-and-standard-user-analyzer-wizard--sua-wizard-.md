---
description: Erfahren Sie, wie Sie das Standard User Analyzer-Tool (SUA) und den SUA-Assistenten verwenden, um Ihre Anwendungen zu testen und potenzielle Kompatibilitätsprobleme zu erkennen.
ms.assetid: 229ee531-32b9-4e11-b64c-3ce5b5ab6530
title: Standardbenutzeranalyse-Tool (Standard User Analyzer, SUA) und SUA-Assistent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fa9329f2f42dd8fc3b948388ef44948deca052a919ca50704cbccedc83fca84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994674"
---
# <a name="standard-user-analyzer-sua-tool-and-standard-user-analyzer-wizard-sua-wizard"></a>Standardbenutzeranalyse-Tool (Standard User Analyzer, SUA) und SUA-Assistent

## <a name="affected-platforms"></a>Betroffene Plattformen

**Clients:** Windows XP, Windows Vista, Windows 7  
**Server:** Windows Server 2003, Windows Server 2008, Windows Server 2008 R2  

## <a name="description"></a>Beschreibung

Das Application Compatibility Toolkit enthält das Standard User Analyzer-Tool (SUA) und den StandardBenutzeranalyse-Assistenten (SUA-Assistent). Mit diesen Tools können Sie Ihre Anwendungen testen und API-Aufrufe überwachen, um potenzielle Kompatibilitätsprobleme aufgrund der Benutzerkontensteuerung (User Account Control, UAC) im Windows 7-Betriebssystem zu erkennen.

UAC, früher als eingeschränktes Benutzerkonto (Limited User Account, LUA) bezeichnet, erfordert, dass alle Benutzer (einschließlich der Mitglieder der Administratorgruppe) als Standardbenutzer ausgeführt werden, indem das Dialogfeld "Sicherheitsaufforderung" verwendet wird, bis die Anwendung absichtlich erhöht wird. Anwendungen, die Zugriff und Berechtigungen für Standorte erfordern, die für einen Standardbenutzer nicht verfügbar sind, können jedoch nicht ordnungsgemäß mit der Standardbenutzerrolle ausgeführt werden.

## <a name="usage"></a>Verbrauch

Die folgenden Abschnitte enthalten ausführliche Informationen zur Verwendung der SuA- und SUA-Assistententools.

**SUA-Tool**

Mit dem SUA-Tool können Sie eine Anwendung analysieren, einen detaillierten Bericht zu UAC-bezogenen Problemen überprüfen und dann die vorgeschlagenen und ausgewählten Anwendungsminderungen anwenden, wie im folgenden Flussdiagramm gezeigt.

![Diagramm, das den Ablauf des S U A-Tools zeigt.](images/act-suaflowchart-appcookbook.gif)

*SUA-Tool und Virtualisierung*

Nur mit dem SUA-Tool können Sie das Virtualisierungsfeature aktivieren und deaktivieren. Wenn Sie das Virtualisierungsfeature deaktivieren, verhält sich die getestete Anwendung eher so, als ob sie Windows XP-Betriebssystem funktioniert.

*SUA-Tool und erhöhte Rechte*

Nur mit dem SUA-Tool können Sie das Feature Mit erhöhten Rechten **starten aktivieren und** deaktivieren. Mit dem Feature "Mit erhöhten Rechten starten" kann die ausgewählte Anwendung als Administrator oder Standardbenutzer ausgeführt werden. Abhängig von Ihrer Auswahl finden Sie verschiedene Arten von UAC-bezogenen Problemen. Wenn Sie das **Kontrollkästchen Mit** erhöhten Rechten starten aktivieren, wird Ihre Anwendung mit vollständigen Administratorrechten ausgeführt, wodurch SUA die Probleme vorhersagen kann, die für einen Standardbenutzer auftreten können. Wenn Sie das Kontrollkästchen Mit erhöhten Rechten starten aktivieren, werden Fehler angezeigt, die sich daraus ergeben, dass die Anwendung tatsächlich ausgeführt wird und Fehler generiert.

**SUA-Assistent**

Mit dem SUA-Assistenten können Sie einen geführten Schritt-für-Schritt-Prozess ausführen, mit dem Sie eine Anwendung analysieren und dann die vorgeschlagenen und ausgewählten Anwendungsminderungen anwenden können, wie im folgenden Flussdiagramm gezeigt. Im Gegensatz zum SUA-Tool ermöglicht der Assistent keine Überprüfung der detaillierten UAC-bezogenen Probleme.

![Diagramm, das den Ablauf des S U A-Assistenten zeigt.](images/act-suaflowchart-appcookbook.gif)

## <a name="links-to-other-resources"></a>Links zu anderen Ressourcen

-   [Download des Anwendungskompatibilitätstoolkits](/windows-hardware/get-started/adk-install)
-   [Grundlegendes zu den Standardbenutzeranalysetools](/previous-versions/windows/it-pro/windows-7/cc838047(v=ws.10))
-   [Standard User Analyzer – Technische Referenz](/previous-versions/windows/it-pro/windows-7/cc765948(v=ws.10))
-   [Testen und Beheben von Problemen mithilfe der Entwicklungstools](/previous-versions/orphan-topics/ws.10/cc766461(v=ws.10))
-   [Anwendungskompatibilität und Benutzerkontensteuerung](/previous-versions/windows/)

> [!Note]  
> Diese Ressourcen sind in einigen Sprachen und Ländern/Regionen möglicherweise nicht verfügbar.

 

 

 
