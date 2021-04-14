---
title: Leistung (Windows 7-Entwicklerhandbuch)
description: Windows 7 maximiert die Hardware Energieeffizienz und Skalierbarkeit und bietet gleichzeitig eine hohe Leistung.
ms.assetid: db48aa8f-749e-4a56-8a91-ac9b81d6e8c9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 752f66e80265bf7d6b3ea26e7baabdc6550ce921
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104339938"
---
# <a name="performance-windows-7-developer-guide"></a>Leistung (Windows 7-Entwicklerhandbuch)

Windows 7 maximiert die Hardware Energieeffizienz und Skalierbarkeit und bietet gleichzeitig eine hohe Leistung. Die Energieeffizienz wird durch reduzierte Hintergrund Aktivitäten und neue Unterstützung für den Start von System Diensten verbessert. Windows 7 bietet außerdem Verbesserungen im Windows-Kernel, mit denen Anwendungen und Dienste effizient zwischen Plattformen skaliert werden können. Die Leistung vieler Features und APIs wurde in Windows 7 im Vergleich zu Windows Vista verbessert. Beispielsweise wird die Treiber Leistung auf Servern durch neue APIs im Benutzermodus und im Kernel Modus optimiert. Das Rendern von Grafiken ist erheblich glatter und schneller. Die Barrierefreiheits Leistung ist auch deutlich schneller als bisher.

## <a name="building-power-efficient-applications"></a>Entwickeln von Power-Efficient Anwendungen

Das Erstellen von energieeffizienten Anwendungen, die die neuesten Energie Verwaltungs Technologien nutzen, ist eine bedeutende Herausforderung, die Entwickler heute kennen. In der Regel erhalten Prozessor-und Gerätehersteller die Aufmerksamkeit, wenn ihre neuesten Angebote gemessen und als Benchmark gekennzeichnet werden. Eine einzelne Anwendung kann jedoch leicht verhindern, dass die neueste Generation von Hardware das Potenzial der Energieeffizienz erkennt. Beispielsweise kann eine einzelne Anwendung, die die Platt Form Zeit Geber Auflösung erhöht, die Akku Lebensdauer um 10 Prozent verringern.

Der erweiterte Betrieb der Akkuleistung und die Nutzung energieeffizienter Technologien sind die wichtigsten Voraussetzungen für Entwickler von heute. Windows 7 reduziert die Anzahl von Aktivitäten, die vom Betriebssystem ausgeführt werden, um die Verwendung von Energiespar Modi zu verhindern. Es unterstützt außerdem den Start der Systemdienste, damit Prozessoren häufiger in den Leerlauf versetzt werden können, und der Leerlauf bleibt länger, was den Energieverbrauch verringert. Außerdem nutzt Windows 7 die neueste energieeffiziente Hardware, einschließlich Netzwerkadapter, Speichergeräte und Grafikkarten.

Windows 7 bietet die Infrastruktur und Tools, die es Entwicklern erleichtern, die Auswirkungen ihrer Anwendungen auf die Energie zu ermitteln. Eine Reihe von Ereignis Rückrufen ermöglicht Anwendungen, ihre Aktivitäten zu reduzieren, wenn sich das System in der Akkuleistung befindet und automatisch zentral hochskaliert wird, wenn sich das *System im Netz* Betrieb befindet. Für Anwendungen, die einen Hintergrundprozess oder-Dienst umfassen, bietet Windows 7 eine neue Infrastruktur, mit der Sie Hintergrundaufgaben automatisch aktivieren können, um die Energieeffizienz zu maximieren. (Weitere Informationen finden Sie unter Übersicht über die [Leistung](https://www.microsoft.com/whdc/system/sysperf/default.mspx) und die [Energie Verwaltung in Windows 7](https://www.climatesaverscomputing.org/wordpress/wp-content/uploads/2011/06/Power_Management_in_Windows_7_Overview.pdf).)

## <a name="service-control-manager"></a>Dienststeuerungs-Manager

Der Windows 7-Dienststeuerungs-Manager (SCM) wurde so erweitert, dass ein Dienst automatisch gestartet und beendet werden kann, wenn ein bestimmtes System Ereignis oder ein bestimmtes System Ereignis im System auftritt. Mit Triggerstart-Funktionen ist es nicht mehr erforderlich, dass Dienste beim Starten des Computers automatisch gestartet werden, und dann Abfragen oder warten, bis ein Ereignis auftritt, z. b. die Geräte Ankunft. Gängige Triggerereignisse für Dienste sind:

-   Ankunft der Geräteklassen Schnittstelle: Starten Sie einen Dienst nur, wenn ein bestimmter Gerätetyp vorhanden ist oder auf dem System angefügt ist.
-   Domänen Beitritt: Starten Sie einen Dienst nur, wenn das System einer Windows-Domäne beigetreten ist.
-   Gruppenrichtlinien Änderung: Starten Sie einen Dienst automatisch, wenn Gruppenrichtlinien auf dem System aktualisiert werden.
-   IP-Adress Ankunft: Starten Sie einen Dienst nur, wenn das System mit dem Netzwerk verbunden ist.

Software Entwickler können die vordefinierten Auslösertypen für Windows 7 und die Konfigurationsoptionen verwenden, um die Funktion zum Starten von Auslösers zu aktivieren. Windows 7 SCM stellt einen neuen Satz von APIs zur Verfügung, mit denen ein Dienst für bestimmte benutzerdefinierte Triggerereignisse registriert werden kann. (Siehe [Dienststeuerungs-Manager](../services/service-control-manager.md).)

## <a name="windows-troubleshooting-platform"></a>Windows-Problembehandlungsplattform

Windows 7 bietet eine umfassende und erweiterbare Problem Behandlungs Plattform, die einen PowerShell-basierten Mechanismus zum beheben und Beheben von Problemen verwendet. Die Hauptkomponenten der Plattform zur Problembehandlung umfassen ein Problem Behandlungspaket, eine Problem Behandlungs-Engine und den Problembehandlungs-Assistenten. Das Problem Behandlungspaket ist eine Sammlung von PowerShell-Skripts und relevanten Metadaten. Das Problem Behandlungs Modul öffnet eine PowerShell-Laufzeit zum Ausführen eines Problembehandlungs Pakets und stellt eine Reihe von Schnittstellen zum Steuern der Problembehandlung für die Paket Ausführung bereit.

Der Problembehandlungs-Assistent bietet ein konsistentes Verfahren für die Problembehandlung von Paketen, die mit der Problembehandlungs-Engine kommunizieren, um Probleme zu beheben und zu beheben, die in einem Problem Behandlungspaket Die Ausführung eines Problembehandlungs Pakets kann auch über eine Reihe von PowerShell-*Cmdlets* gesteuert werden.

Die Problem Behandlungs Plattform ist nahtlos in das Windows 7PC Solution Center integriert, sodass andere Anwendungen die Diagnose auf ähnliche Weise wie im Rahmen Ihres PC-Verwaltungs Programm ausführen können. Die Problem Behandlungs Plattform kann von IT-Spezialisten über *Gruppenrichtlinie* für die Verwendung innerhalb des Unternehmens konfiguriert werden, und ein Windows Troubleshooting Toolkit, das Entwicklern das Erstellen von Problem Behandlungs Paketen ermöglicht, ist ebenfalls verfügbar. (Siehe [Windows-Problem Behandlungs Plattform](/previous-versions/windows/desktop/wintt/windows-troubleshooting-toolkit-portal).)

![Problembehandlung bei der Plattform](images/windows7-devguide-troubleshoot.jpg)

Die Problem Behandlungs Plattform ist nahtlos in das Windows 7PC Solution Center integriert.

 

 
