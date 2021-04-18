---
description: .
ms.assetid: 6a31cca3-f47c-4663-b2e8-aad6b4a6f28f
title: Server Hyper-V
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d6997074e000b17a119a838df5b6fab961b8ee0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351608"
---
# <a name="server-hyper-v"></a>Server Hyper-V

## <a name="platforms"></a>Plattformen

 **Clients** -Windows XP \| Windows Vista \| Windows 7  
**Server** -Windows Server 2008 \| Windows Server 2008 R2  

## <a name="feature-impact"></a>Auswirkungen von Features

 **Schweregrad** -niedrig  
**Häufigkeit** -niedrig  





## <a name="description"></a>BESCHREIBUNG

Mithilfe der Servervirtualisierung können mehrere Betriebssysteme auf einem einzelnen physischen Computer als virtuelle Computer (Virtual Machines, VMS) ausgeführt werden. auf diese Weise können Sie Workloads von unter ausgelasteten Server Computern auf eine geringere Anzahl von vollständig ausgelasteten Computern konsolidieren. Windows 7 umfasst mehrere Verbesserungen der Windows Server 2008-Version:

-   **Livemigration:** In Windows Server 2008 gab es eine schnelle Migration. Mit Livemigration haben wir die Migrations Geschwindigkeit und die Speicher Flexibilität verbessert.
-   **Unterstützung logischer Prozessoren:** Wir haben die logischen Host Prozessoren von 16lp auf 64lp erweitert.
-   **Storage Hot Add:** Nun können Sie einem laufenden virtuellen Computer zusätzliche VHD-oder Pass-Through-Datenträger hinzufügen, ohne den virtuellen Computer zu deaktivieren.
-   **Neue Hardware Unterstützung:** Wir haben Unterstützung für die Technologien hinzugefügt, die in neuen Prozessoren und Netzwerkkarten für den Markt enthalten sind, u.a. Übersetzung der zweiten Ebene (slat), TCP-Abladung (Chimney) und vmdq.
-   **Terminaldienstevirtualisierung (TSv):** Wir haben eine zentralisierte Desktop Lösung für Hyper-V.

## <a name="manifestation-of-impact"></a>Erscheinung der Auswirkung

-   **Livemigration:** Sie müssen möglicherweise die Art und Weise ändern, wie Sie Ihre Speichersysteme entworfen haben, um diese Technologie voll ausschöpfen zu können. Obwohl diese Änderungen möglicherweise nicht erforderlich sind, können Sie diese implementieren, um die Vorteile vollständig nutzen zu können. Möglicherweise benötigen Sie eine Verwaltungs Anwendung, um Livemigration zu orchestrieren.
-   **Unterstützung logischer Prozessoren:** Diese Funktion hat keine Auswirkung auf Kunden oder ISVs bei der Migration von Windows Server 2008 zu Windows Server 2008 R2.
-   **Storage Hot Add:** Diese Funktion hat keine Auswirkung auf Kunden oder ISVs bei der Migration von Windows Server 2008 zu Windows Server 2008 R2. Verwaltungs Anwendungen, die die Einstellungen einer virtuellen Maschine konfigurieren, müssen möglicherweise aktualisiert werden, um diese neue Funktion zu verwalten.
-   **Neue Hardware Unterstützung:** Diese Features gelten nur für neue Hardware, die auf dem Markt eingeführt wird. Da keine Unterstützung für diese Features erstellt werden kann, ist es wahrscheinlich, dass ein physischer Server, der von Windows Server 2008 zu Windows Server 2008 R2 migriert wird, beeinträchtigt wird. Wenn diese Features auf dem Server verfügbar sind, der migriert wird, werden keine direkten Änderungen erwartet.
-   **Terminaldienstevirtualisierung:** Diese Funktion hat keine Auswirkung auf Kunden oder ISVs bei der Migration von Windows Server 2008 zu Windows Server 2008 R2. Anwendungen, die Terminal Dienste (TS) nutzen, können beeinträchtigt werden. Diese Funktion ist direkt in TS integriert, sodass Anwendungen, die TS konfigurieren, möglicherweise aktualisiert werden müssen, um diese neue Funktion zu verwalten.

## <a name="mitigation"></a>Minderung

-   **Livemigration:** Bereitstellen von ausführlichen Anleitungen für Endbenutzer mit bewährten Methoden und Empfehlungen für den Entwurf des Speichersystems. Sie müssen den Endbenutzer über die Optionen und Empfehlungen informieren.

## <a name="leveraging-capabilitities"></a>Nutzen von capabilitities

-   **Livemigration:** Diese Funktion ermöglicht die dynamische IT-Umgebung. Entwickler von Anwendungen für die Virtualisierungsverwaltung müssen Ihre Anwendung ändern, um diese neue Funktion nutzen zu können. Microsoft stellt WMI-Schnittstellen öffentlich zur Verfügung, damit Entwickler Anwendungen mit diesem Feature integrieren können.
-   **Terminaldienstevirtualisierung:** Diese Funktion ermöglicht ein neues Virtualisierungsszenario. Anwendungen, die Terminal Dienste (TS) nutzen, können beeinträchtigt werden. Diese Funktion ist direkt in TS integriert, sodass Anwendungen, die TS konfigurieren, möglicherweise aktualisiert werden müssen, um diese neue Funktion zu verwalten.

## <a name="links-to-other-resources"></a>Links zu anderen Ressourcen

[WMI-Verwaltungs Schnittstellen für Hyper-V v1](/previous-versions/windows/desktop/virtual/windows-virtualization-portal). Der größte Teil dieses Inhalts gilt zwar für V2 von Hyper-V, aber eine aktualisierte Version mit V2-spezifischen Informationen sollte näher an Windows 7-Start verfügbar sein.

 

 
