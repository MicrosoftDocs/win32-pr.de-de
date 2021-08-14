---
description: Dynamischer Arbeitsspeicher
ms.assetid: 0ea1de35-34ea-4e94-b90d-0f89503cb3fb
title: Dynamischer Arbeitsspeicher
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 408e54aa1a1d238a98bb0eff8af2dd76862b32b77c26b3d3812d8707bc0099f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118329852"
---
# <a name="dynamic-memory"></a>Dynamischer Arbeitsspeicher

## <a name="affected-platforms"></a>Betroffene Plattformen

**Clients (die als virtuelle Computer ausgeführt werden)** – Windows Vista \| Windows 7  
**Server** – Windows Server 2008 R2 Hyper-V SP1  


## <a name="feature-impact"></a>Auswirkung von Features

 **Schweregrad:** Niedrig  
**Häufigkeit** – Hoch  






## <a name="description"></a>BESCHREIBUNG

Auf hoher Ebene ist Hyper-V-Dynamischer Arbeitsspeicher eine Speicherverwaltungserweiterung für die Hyper-V-Rolle, die in Windows Server 2008 R2 SP1 enthalten ist. Es ist für den Einsatz in der Produktion konzipiert und ermöglicht Es Kunden, ein höheres Konsolidierungs-/VM-Dichteverhältnis zu erzielen und gleichzeitig die Arbeitsspeicherauslastung auf dem physischen Computer zu optimieren. Die statische Speicherzuweisung wird reduziert, und bei Bedarf wird zusätzlicher Arbeitsspeicher zugeordnet. Dynamischer Arbeitsspeicher auswirkungen auf Softwareentwickler, die sicherstellen möchten, dass ihre Software in einer Umgebung eines virtuellen Computers ordnungsgemäß funktioniert.

## <a name="usage-scenario"></a>Verwendungsszenario

Es gibt zwei wichtige Verwendungsszenarien, Dynamischer Arbeitsspeicher ins Spiel kommen: hostseitige Anwendungen und gastseitige Anwendungen.

**Hostseitige Anwendungen (Verwaltungstools)**

Alte Tools, die einen neuen Windows Server 2008 R2 SP1-Server verwalten, können nicht auf die neuen Dynamischer Arbeitsspeicher zugreifen. Neue WMI-APIs und Leistungsindikatoren wurden entwickelt, um die neuen Dynamischer Arbeitsspeicher für virtuelle Hyper-V-Computer zu verwalten. Softwareentwickler, die an Verwaltungstools arbeiten, sollten diese APIs und Leistungsindikatoren für die Verwendung mit Windows Server 2008 R2 SP1 mit installierter Hyper-V-Rolle nutzen. Details zu diesen neuen APIs finden Sie in der Dokumentation zum [Hyper-V-WMI-Anbieter auf MSDN.](/previous-versions/windows/desktop/virtual/using-the-virtualization-wmi-provider)

**Gastseitige Anwendungen**

Entwickler, die Software für die Verwendung auf einem virtuellen Computer schreiben, der für die Verwendung von Dynamischer Arbeitsspeicher müssen bedenken, dass der Arbeitsspeicher des VM-Systems nicht mehr konstant ist. Daher sollte ihre Anwendung Arbeitsspeicher frei geben, wenn sie nicht mehr benötigt wird, um anderen Anwendungen die Nutzung der Ressource zu ermöglichen.

Speicherzuweisungen und Dasentlegungen funktionieren für Benutzeranwendungen weiterhin wie gewohnt. Dynamischer Arbeitsspeicher ist für die meisten Endbenutzeranwendungen vollständig transparent. Wenn die entwickelte Software jedoch Arbeitsspeicherleistungsindikatoren auf dem virtuellen Computer nutzt, sollten in einer Dynamischer Arbeitsspeicher-fähigen Umgebung sorgfältige Tests durchgeführt werden, um sicherzustellen, dass die Software die Änderungen berücksichtigt, die an der Speicherzuordnung des Gastbetriebssystems vorgenommen werden. Der verfügbare Arbeitsspeicher ist aus Sicht des virtuellen Computers nicht mehr "statisch".

## <a name="solutions"></a>Lösungen

Auf virtuellen Computern müssen aktualisierte Integrationsdienste (SP1) installiert sein, um die Vorteile der Dynamischer Arbeitsspeicher. Stellen Sie sicher, dass alle Computer, die in der Verwaltung virtueller Hyper-V-Computer verwendet werden, die neuesten Windows Server 2008 R2 SP1-Bits verwenden.

## <a name="links-to-other-resources"></a>Links zu anderen Ressourcen

-   [Dynamischer Arbeitsspeicher Coming To Hyper-V-Blog](https://blogs.technet.com/b/virtualization/archive/2010/03/18/dynamic-memory-coming-to-hyper-v.aspx)
-   [Verwenden des Hyper-V-WMI-Anbieters](/previous-versions/windows/desktop/virtual/using-the-virtualization-wmi-provider)

## <a name="disclaimer"></a>Haftungsausschluss

Die in diesem Dokument enthaltenen Informationen beziehen sich auf Vorabversionssoftwareprodukt, das vor der ersten kommerziellen Veröffentlichung erheblich geändert werden kann. Entsprechend können die Informationen das Softwareprodukt bei der ersten kommerziellen Version nicht genau beschreiben oder widerspiegeln. Dieses Dokument dient nur zu Informationszwecken. MICROSOFT MAKES NO WARRANTIES, EXPRESS OR IMPLIED, IN THIS DOCUMENT.

 

 
