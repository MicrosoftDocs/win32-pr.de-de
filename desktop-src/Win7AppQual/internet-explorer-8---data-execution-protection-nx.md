---
description: .
ms.assetid: 56a4889c-5dcf-416f-b46e-5c48277d5636
title: Internet Explorer 8-Datenausführungsschutz/NX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bf23ba40be518e3d4c1421012e6b46fdb7b5e50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865975"
---
# <a name="internet-explorer-8---data-execution-protectionnx"></a>Internet Explorer 8-Datenausführungsschutz/NX

## <a name="affected-platforms"></a>Betroffene Plattformen

 **Clients** -Windows XP \| Windows Vista \| Windows 7  
**Server** -Windows Server 2003 \| Windows Server 2008 \| Windows Server 2008 R2  










> [!Note]  
> Internet Explorer 8 aktiviert den DEP/NX-Schutz, wenn er unter einem Betriebssystem mit der neuesten Service Pack ausgeführt wird. Für Windows XP SP3, Windows Server 2003 SP3, Windows Vista SP1 und Windows Server 2008 ist DEP/NX in Internet Explorer 8 standardmäßig aktiviert.

 

## <a name="feature-impact"></a>Auswirkungen von Features

**Schweregrad** -Mittel  
**Häufigkeit** -niedrig  

> [!Note]  
> In der Regel stürzt jede Anwendung, die in Internet Explorer ausgeführt wird und nicht mit DEP/NX kompatibel ist, beim Start ab und funktioniert nicht. Internet Explorer stürzt beim Starten ab, wenn Add-ons, die nicht mit DEP/NX kompatibel sind, installiert sind.

 

## <a name="description"></a>BESCHREIBUNG

DEP/NX ist ein Sicherheits Feature, mit dem speicherbezogene Sicherheitsrisiken verringert werden können. Ab Internet Explorer 8 aktivieren alle Internet Explorer-Prozesse die DEP/NX-Funktion standardmäßig.

## <a name="manifestation-of-impact"></a>Erscheinung der Auswirkung

Der Windows-Kernel überwacht die Ausführung eines Programms. Wenn der Kernel einen Versuch erkennt, Code auf einer Speicherseite auszuführen, der nicht als ausführbare Datei gekennzeichnet ist, stoppt der Kernel die Ausführung des Programms, was zu einem Absturz führt. Dies ist eine Sicherheitsmaßnahme, mit der sichergestellt wird, dass speicherbezogene Sicherheitsrisiken (z. b. Pufferüberläufe) in der Anwendung nicht ausgenutzt werden können, um beliebigen Code auszuführen.

## <a name="end-user-mitigation"></a>End-User Entschärfung

-   Installieren Sie eine neuere Version des Add-on oder Frameworks, das mit DEP/NX kompatibel ist.
-   Führen Sie Internet Explorer mit erhöhten Rechten als Administrator aus, und deaktivieren Sie DEP/NX mithilfe des Kontrollkästchens **Speicherschutz aktivieren, um Online Angriffe zu** minimieren auf der Registerkarte "Erweiterte **Internet Optionen**"  /   .

## <a name="developer-solution"></a>Entwickler Lösung

Kompilieren Sie Anwendungen mithilfe der neuesten Versionen von Frameworks, die mit DEP kompatibel sind.

## <a name="leveraging-feature-capabilities"></a>Nutzen von Featurefunktionen

-   Verwenden der/NXCOMPAT-Linkeroption zum Angeben der DEP/NX-Kompatibilität
-   Wählen Sie Ihren Code in andere verfügbare Schutzmaßnahmen wie Stack Defense (/GS), sichere Ausnahmebehandlung (/SAFESEH) und ASLR (/DynamicBase) aus.

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Tests der Kompatibilität, Leistung, Zuverlässigkeit und Benutzerfreundlichkeit

-   Testen Sie Ihren Code mit DEP/NX, der mithilfe der neuesten Version von Internet Explorer unter Windows Vista SP1 oder höher aktiviert wurde.
-   Testen Sie mit Internet Explorer 7 unter Windows Vista nach dem Aktivieren der DEP/NX-Option. Um DEP/NX für Internet Explorer 7 zu aktivieren, führen Sie Internet Explorer als Administrator aus, und legen Sie dann das entsprechende Kontrollkästchen auf der Registerkarte Extras > Internet Optionen > erweitert fest.
-   Führen Sie das Internet Explorer Compatibility Test Tool (iectt) aus, das mit dem Anwendungskompatibilitäts-Toolkit (Act) bereitgestellt wird, um mögliche Probleme aufgrund von DEP/NX-Änderungen zu ermitteln.

## <a name="links-to-other-resources"></a>Links zu anderen Ressourcen

-   [Internet Explorer 8 Sicherheitsteil I: DEP/NX-Speicherschutz](/archive/blogs/ie/)
-   [Datenausführungsverhinderung](../memory/data-execution-prevention.md)
-   [Neue NX-APIs, die zu Windows Vista SP1, Windows XP SP3 und Windows Server 2008 R2 hinzugefügt wurden](/archive/blogs/michael_howard/)
-   [Anwendungskompatibilitäts-Toolkit Download](/windows-hardware/get-started/adk-install)
-   [Bekannte Probleme mit der Internet Explorer-Sicherheitsfunktion](/previous-versions/windows/it-pro/windows-7/cc722079(v=ws.10))

 

 
