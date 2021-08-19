---
description: Server Hyper-V
ms.assetid: 6a31cca3-f47c-4663-b2e8-aad6b4a6f28f
title: Server Hyper-V
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f2cab162355e298cbc21c1c43d8b1a0d16b8c23f958e06c7fb28a8ecb6e3309
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118328710"
---
# <a name="server-hyper-v"></a>Server Hyper-V

## <a name="platforms"></a>Plattformen

 **Clients** – Windows XP \| Windows Vista \| Windows 7  
**Server** – Windows Server 2008 \| Windows Server 2008 R2  

## <a name="feature-impact"></a>Auswirkungen auf Features

 **Schweregrad –** Niedrig  
**Häufigkeit** : Niedrig  





## <a name="description"></a>Beschreibung

Mithilfe der Servervirtualisierung können mehrere Betriebssysteme auf einem einzelnen physischen Computer als virtuelle Computer (VMs) ausgeführt werden, sodass Sie Workloads nicht ausgelasteter Servercomputer auf einer kleineren Anzahl vollständig ausgelasteter Computer konsolidieren können. Windows 7 enthält mehrere Verbesserungen der Windows Server 2008-Version:

-   **Livemigration:** In Windows Server 2008 gab es eine schnelle Migration. Mit Livemigration haben wir die Migrationsgeschwindigkeit und die Speicherflexibilität verbessert.
-   **Unterstützung logischer Prozessoren:** Wir haben logische Hostprozessoren von 16LP auf 64LP erhöht.
-   **Storage Hot Add::** Jetzt können Sie einem ausgeführten virtuellen Computer zusätzliche VHD- oder Pass-Through-Datenträger hinzufügen, ohne den virtuellen Computer zu deaktivieren.
-   **Neue Hardwareunterstützung:** Wir haben Unterstützung für die Technologien hinzugefügt, die in neuen Prozessoren und Netzwerkkarten enthalten sind, die auf den Markt kommen, einschließlich Der Übersetzung auf zweiter Ebene (Second Level Translation, SLAT), TCP Offload (Lateney) und VMdQ.
-   **Terminal services virtualization (TSv):** Wir haben eine zentrale Desktoplösung für Hyper-V verwendet.

## <a name="manifestation-of-impact"></a>Auswirkungen

-   **Livemigration:** Möglicherweise müssen Sie die Art und Weise ändern, wie Sie Ihre Speichersysteme entwickelt haben, um diese Technologie vollständig nutzen zu können. Obwohl diese Änderungen möglicherweise nicht erforderlich sind, können Sie sie implementieren, um die Vorteile vollständig zu nutzen. Möglicherweise benötigen Sie eine Verwaltungsanwendung, um Livemigration zu orchestrieren.
-   **Unterstützung logischer Prozessoren:** Diese Funktion hat keine Auswirkungen auf Kunden oder ISVs bei der Migration von Windows Server 2008 zu Windows Server 2008 R2.
-   **Storage Hot Add::** Diese Funktion hat keine Auswirkungen auf Kunden oder ISVs bei der Migration von Windows Server 2008 zu Windows Server 2008 R2. Verwaltungsanwendungen, die die Einstellungen eines virtuellen Computers konfigurieren, müssen möglicherweise aktualisiert werden, um dieses neue Feature zu verwalten.
-   **Neue Hardwareunterstützung:** Diese Features gelten nur für neue Hardware, die auf dem Markt eingeführt wird. Da es keine build-in-Unterstützung für diese Features gibt, ist es nicht wahrscheinlich, dass ein physischer Server, der von Windows Server 2008 zu Windows Server 2008 R2 migriert wird, betroffen ist. Wenn diese Features auf dem Server verfügbar sind, der migriert wird, werden keine direkten Änderungen erwartet.
-   **Terminaldienstevirtualisierung:** Diese Funktion hat keine Auswirkungen auf Kunden oder ISVs bei der Migration von Windows Server 2008 zu Windows Server 2008 R2. Anwendungen, die Terminaldienste (TS) nutzen, können betroffen sein. Dieses Feature lässt sich direkt in TS integrieren. Daher müssen Anwendungen, die TS konfigurieren, möglicherweise aktualisiert werden, um dieses neue Feature zu verwalten.

## <a name="mitigation"></a>Minderung

-   **Livemigration:** Bieten Sie Endbenutzern eine ausführliche Anleitung mit bewährten Methoden und Empfehlungen für den Entwurf des Speichersystems. Sie müssen den Endbenutzer über die Optionen und Empfehlungen informieren.

## <a name="leveraging-capabilitities"></a>Nutzen von Funktionen

-   **Livemigration:** Dieses Feature aktiviert die dynamische IT-Umgebung. Entwickler von Virtualisierungsverwaltungsanwendungen müssen ihre Anwendung ändern, um dieses neue Feature nutzen zu können. Microsoft stellt WMI-Schnittstellen öffentlich zur Verfügung, damit Entwickler Anwendungen in dieses Feature integrieren können.
-   **Terminaldienstevirtualisierung:** Dieses Feature ermöglicht ein neues Virtualisierungsszenario. Anwendungen, die Terminaldienste (TS) nutzen, können betroffen sein. Dieses Feature lässt sich direkt in TS integrieren. Daher müssen Anwendungen, die TS konfigurieren, möglicherweise aktualisiert werden, um dieses neue Feature zu verwalten.

## <a name="links-to-other-resources"></a>Links zu anderen Ressourcen

[WMI-Verwaltungsschnittstellen für Hyper-V v1](/previous-versions/windows/desktop/virtual/windows-virtualization-portal). Der größte Teil dieses Inhalts gilt zwar für v2 von Hyper-V, aber eine aktualisierte Version mit v2-spezifischen Informationen sollte näher am Start Windows 7 verfügbar sein.

 

 
