---
description: 'Internet Explorer 8: Schutz der Datenausführung/NX'
ms.assetid: 56a4889c-5dcf-416f-b46e-5c48277d5636
title: 'Internet Explorer 8: Schutz der Datenausführung/NX'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b1f969aa2e934f36142995150b6484dad2fa5067f6cbb5ab3a947055af375ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998890"
---
# <a name="internet-explorer-8---data-execution-protectionnx"></a>Internet Explorer 8: Schutz der Datenausführung/NX

## <a name="affected-platforms"></a>Betroffene Plattformen

 **Clients–** Windows XP, Windows Vista, Windows 7  
**Server** – Windows Server 2003, Windows Server 2008, Windows Server 2008 R2  










> [!Note]  
> Internet Explorer 8 aktiviert den DEP/NX-Schutz, wenn er unter einem Betriebssystem mit dem neuesten Service Pack ausgeführt wird. Windows FÜR XP SP3, Windows Server 2003 SP3, Windows Vista SP1 und Windows Server 2008 ist DEP/NX standardmäßig in Internet Explorer 8 aktiviert.

 

## <a name="feature-impact"></a>Auswirkung von Features

**Schweregrad:** Mittel  
**Häufigkeit** – Niedrig  

> [!Note]  
> In der Regel stürzt jede Anwendung, die in Internet Explorer ausgeführt wird und nicht mit DEP/NX kompatibel ist, beim Start ab und funktioniert nicht. Internet Explorer beim Start abstürzen, wenn Add-Ons installiert sind, die nicht mit DEP/NX kompatibel sind.

 

## <a name="description"></a>Beschreibung

DEP/NX ist ein Sicherheitsfeature, mit dem speicherbezogene Sicherheitsrisiken entschärft werden können. Ab Internet Explorer 8 aktivieren alle Internet Explorer standardmäßig das DEP/NX-Feature.

## <a name="manifestation-of-impact"></a>Auswirkungen

Der Windows Kernel überwacht die Ausführung eines Programms. Wenn der Kernel einen Versuch erkennt, Code von einer Speicherseite aus ausführen zu können, die nicht als ausführbare Datei gekennzeichnet ist, hält der Kernel die Ausführung des Programms an, was zu einem "Absturz" führt. Dies ist eine Sicherheitsmaßnahme, um sicherzustellen, dass speicherbezogene Sicherheitsrisiken (z. B. Pufferüberläufe) in der Anwendung nicht ausgenutzt werden können, um beliebigen Code auszuführen.

## <a name="end-user-mitigation"></a>End-User Risikominderung

-   Installieren Sie eine neuere Version des Add-Ons oder Frameworks, die MIT DEP/NX kompatibel ist.
-   Führen Internet Explorer mit erhöhten Rechten als Administrator aus, und deaktivieren Sie dann DEP/NX mithilfe des **Kontrollkästchens** Speicherschutz aktivieren, um Onlineangriffe zu minimieren auf der Registerkarte **Internetoptionen**  /  **Erweitert.**

## <a name="developer-solution"></a>Entwicklerlösung

Kompilieren Sie Anwendungen mithilfe der neuesten Versionen von Frameworks, die DEP-kompatibel sind.

## <a name="leveraging-feature-capabilities"></a>Nutzen von Featurefunktionen

-   Verwenden Sie die /NXCOMPAT-Linkeroption, um die DEP/NX-Kompatibilität anzugeben.
-   Verwenden Sie Ihren Code für andere verfügbare Verteidigungen wie Stapelschutz (/GS), sichere Ausnahmebehandlung (/SafeSEH) und ASLR (/DynamicBase).

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Kompatibilitäts-, Leistungs-, Zuverlässigkeits- und Nutzbarkeitstests

-   Testen Sie Ihren Code mit aktivierter DEP/NX mithilfe der neuesten veröffentlichten Internet Explorer-Version unter Windows Vista SP1 oder höher.
-   Testen Sie Internet Explorer 7 auf Windows Vista, nachdem Sie die DEP/NX-Option aktivieren. Um DEP/NX für Internet Explorer 7 zu aktivieren, führen Sie Internet Explorer als Administrator aus, und aktivieren Sie dann das entsprechende Kontrollkästchen auf der Registerkarte Extras > Internetoptionen > Erweitert.
-   Führen Sie das Internet Explorer Compatibility Test Tool (IECTT) aus, das mit dem Application Compatibility Toolkit (ACT) bereitgestellt wird, um mögliche Probleme aufgrund der DEP/NX-Änderungen zu ermitteln.

## <a name="links-to-other-resources"></a>Links zu anderen Ressourcen

-   [Internet Explorer 8 Security Part I: DEP/NX Memory Protection](/archive/blogs/ie/)
-   [Datenausführungsverhinderung](../memory/data-execution-prevention.md)
-   [Neue NX-APIs zu Windows Vista SP1, Windows XP SP3 und Windows Server 2008 R2 hinzugefügt](/archive/blogs/michael_howard/)
-   [Download des Anwendungskompatibilitätstoolkits](/windows-hardware/get-started/adk-install)
-   [Bekannte Internet Explorer Sicherheitsfeatures](/previous-versions/windows/it-pro/windows-7/cc722079(v=ws.10))

 

 
