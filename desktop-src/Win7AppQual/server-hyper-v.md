---
description: Server Hyper-V
ms.assetid: 6a31cca3-f47c-4663-b2e8-aad6b4a6f28f
title: Server Hyper-V
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b3149f1c5faa98c9c61be884a193b0e3a1ecceb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116208"
---
# <a name="server-hyper-v"></a>Server Hyper-V

## <a name="platforms"></a>Plattformen

 **Clients** – Windows XP \| Windows Vista Windows \| 7  
**Server** – Windows Server 2008 \| Windows Server 2008 R2  

## <a name="feature-impact"></a>Auswirkung von Features

 **Schweregrad:** Niedrig  
**Häufigkeit** – Niedrig  





## <a name="description"></a>BESCHREIBUNG

Mit der Servervirtualisierung können mehrere Betriebssysteme auf einem einzelnen physischen Computer als virtuelle Computer (VMs) ausgeführt werden, sodass Sie Workloads von nicht ausgelasteten Servercomputern auf einer kleineren Anzahl von voll ausgelasteten Computern konsolidieren können. Windows 7 enthält mehrere Erweiterungen der Windows Server 2008-Version:

-   **Livemigration:** In Windows Server 2008 gab es eine schnelle Migration. Mit Livemigration haben wir die Migrationsgeschwindigkeit und Speicherflexibilität verbessert.
-   **Unterstützung logischer Prozessoren:** Wir haben logische Hostprozessoren von 16LP auf 64LP erhöht.
-   **Speicher hot add (Speicher hot add):** Jetzt können Sie einem ausgeführten virtuellen Computer zusätzliche VHD- oder Pass-Through-Datenträger hinzufügen, ohne den virtuellen Computer zu deaktivieren.
-   **Neue Hardwareunterstützung:** Wir haben Unterstützung für die Technologien hinzugefügt, die in neuen Prozessoren und Netzwerkkarten enthalten sind, die auf den Markt kommen, einschließlich Second Level Translation (SLAT), TCP Offload (Chimney) und VMdQ.
-   **Virtualisierung von Terminaldiensten (TSv):** Wir haben die Desktoplösung für Hyper-V zentralisiert.

## <a name="manifestation-of-impact"></a>Auswirkungen

-   **Livemigration:** Möglicherweise müssen Sie die Art und Weise ändern, wie Sie Ihre Speichersysteme entworfen haben, um diese Technologie vollständig nutzen zu können. Obwohl diese Änderungen möglicherweise nicht erforderlich sind, können Sie sie implementieren, um die Vorteile vollständig zu nutzen. Möglicherweise benötigen Sie eine Verwaltungsanwendung zum Orchestrieren Livemigration.
-   **Unterstützung logischer Prozessoren:** Diese Funktion hat keine Auswirkungen auf Kunden oder ISVs bei der Migration von Windows Server 2008 zu Windows Server 2008 R2.
-   **Storage Hot Add (Speicher im hot-Speicher hinzufügen):** Diese Funktion hat keine Auswirkungen auf Kunden oder ISVs bei der Migration von Windows Server 2008 zu Windows Server 2008 R2. Verwaltungsanwendungen, die die Einstellungen eines virtuellen Computers konfigurieren, müssen möglicherweise aktualisiert werden, um dieses neue Feature zu verwalten.
-   **Neue Hardwareunterstützung:** Diese Features gelten nur für neue Hardware, die auf dem Markt eingeführt wird. Da es keine build-in-Unterstützung für diese Features gibt, ist es nicht wahrscheinlich, dass ein physischer Server, der von Windows Server 2008 zu Windows Server 2008 R2 migriert wird, betroffen ist. Wenn diese Features auf dem Server verfügbar sind, der migriert wird, werden keine direkten Änderungen erwartet.
-   **Terminaldienstevirtualisierung:** Diese Funktion hat keine Auswirkungen auf Kunden oder ISVs bei der Migration von Windows Server 2008 zu Windows Server 2008 R2. Anwendungen, die Terminaldienste (TS) nutzen, können betroffen sein. Dieses Feature lässt sich direkt in TS integrieren. Daher müssen Anwendungen, die TS konfigurieren, möglicherweise aktualisiert werden, um dieses neue Feature zu verwalten.

## <a name="mitigation"></a>Minderung

-   **Livemigration:** Bieten Sie Endbenutzern eine ausführliche Anleitung mit bewährten Methoden und Empfehlungen für den Entwurf des Speichersystems. Sie müssen den Endbenutzer über die Optionen und Empfehlungen informieren.

## <a name="leveraging-capabilitities"></a>Nutzen von Funktionen

-   **Livemigration:** Dieses Feature aktiviert die dynamische IT-Umgebung. Entwickler von Virtualisierungsverwaltungsanwendungen müssen ihre Anwendung ändern, um dieses neue Feature nutzen zu können. Microsoft stellt WMI-Schnittstellen öffentlich zur Verfügung, damit Entwickler Anwendungen in dieses Feature integrieren können.
-   **Terminaldienstevirtualisierung:** Dieses Feature ermöglicht ein neues Virtualisierungsszenario. Anwendungen, die Terminaldienste (TS) nutzen, können betroffen sein. Dieses Feature ist direkt in TS integriert, und daher müssen Anwendungen, die TS konfigurieren, möglicherweise aktualisiert werden, um dieses neue Feature zu verwalten.

## <a name="links-to-other-resources"></a>Links zu anderen Ressourcen

[WMI-Verwaltungsschnittstellen für Hyper-V v1](/previous-versions/windows/desktop/virtual/windows-virtualization-portal). Der großteil dieser Inhalte gilt zwar für Version 2 von Hyper-V, aber eine aktualisierte Version mit v2-spezifischen Informationen sollte näher am Windows 7-Start verfügbar sein.

 

 
