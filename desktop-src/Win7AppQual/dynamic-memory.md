---
description: Dynamischer Arbeitsspeicher
ms.assetid: 0ea1de35-34ea-4e94-b90d-0f89503cb3fb
title: Dynamischer Arbeitsspeicher
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfcc54a1b85f4fc39bf6383e05a2e6e535edd1d4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088468"
---
# <a name="dynamic-memory"></a>Dynamischer Arbeitsspeicher

## <a name="affected-platforms"></a>Betroffene Plattformen

**Clients (als virtuelle Computer ausgeführt)** – Windows Vista \| Windows 7  
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

Speicherzuweisungen und Dasentlegungen funktionieren für Benutzeranwendungen weiterhin wie gewohnt. Dynamischer Arbeitsspeicher ist für die meisten Endbenutzeranwendungen vollständig transparent. Wenn die entwickelte Software jedoch Speicherleistungsindikatoren auf dem virtuellen Computer verwendet, sollten sie in einer Dynamischer Arbeitsspeicher aktivierten Umgebung sorgfältig getestet werden, um sicherzustellen, dass die Software die Änderungen berücksichtigt, die an der Speicherbelegung des Gastbetriebssystems vorgenommen werden. Verfügbarer Arbeitsspeicher ist aus Sicht des virtuellen Computers nicht mehr "statisch".

## <a name="solutions"></a>Lösungen

Auf virtuellen Computern müssen aktualisierte Integrationsdienste (SP1) installiert sein, um Dynamischer Arbeitsspeicher nutzen zu können. Stellen Sie sicher, dass alle Computer, die in der Verwaltung virtueller Hyper-V-Computer verwendet werden, die neuesten Windows Server 2008 R2 SP1-Bits verwenden.

## <a name="links-to-other-resources"></a>Links zu anderen Ressourcen

-   [Blog zu Dynamischer Arbeitsspeicher Coming To Hyper-V](https://blogs.technet.com/b/virtualization/archive/2010/03/18/dynamic-memory-coming-to-hyper-v.aspx)
-   [Verwenden des Hyper-V-WMI-Anbieters](/previous-versions/windows/desktop/virtual/using-the-virtualization-wmi-provider)

## <a name="disclaimer"></a>Haftungsausschluss

Die in diesem Dokument enthaltenen Informationen beziehen sich auf vorab veröffentlichte Softwareprodukte, die vor dem ersten kommerziellen Release erheblich geändert werden können. Entsprechend können die Informationen das Softwareprodukt bei der ersten kommerziellen Veröffentlichung nicht genau beschreiben oder widerspiegeln. Dieses Dokument dient nur zu Informationszwecken. MICROSOFT MAKES NO WARRANTIES, EXPRESS OR IMPLIED, IN THIS DOCUMENT.

 

 
