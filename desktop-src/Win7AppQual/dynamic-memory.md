---
description: .
ms.assetid: 0ea1de35-34ea-4e94-b90d-0f89503cb3fb
title: Dynamischer Arbeitsspeicher
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a1e868a89714a7f6f1d77f9416515897876c150
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357052"
---
# <a name="dynamic-memory"></a>Dynamischer Arbeitsspeicher

## <a name="affected-platforms"></a>Betroffene Plattformen

**Clients (als virtuelle Computer ausgeführt)** -Windows Vista \| Windows 7  
**Server** -Windows Server 2008 R2 Hyper-V SP1  


## <a name="feature-impact"></a>Auswirkungen von Features

 **Schweregrad** -niedrig  
**Häufigkeit** -hoch  






## <a name="description"></a>BESCHREIBUNG

Auf hoher Ebene ist Hyper-v dynamischer Arbeitsspeicher eine Verbesserung der Arbeitsspeicher Verwaltung für die Hyper-v-Rolle, die in Windows Server 2008 R2 SP1 enthalten ist. Es ist für die Verwendung in der Produktion vorgesehen und ermöglicht Kunden, höhere Konsolidierungs-und VM-Dichte Verhältnisse zu erreichen, während gleichzeitig die Arbeitsspeicher Auslastung auf dem physischen Computer optimiert wird. Die statische Speicher Belegung wird reduziert, und zusätzlicher Arbeitsspeicher wird Bedarfs abhängig zugeordnet. Dynamischer Arbeitsspeicher wirkt sich auf Softwareentwickler aus, die sicherstellen möchten, dass Ihre Software in einer virtuellen Computerumgebung ordnungsgemäß funktioniert.

## <a name="usage-scenario"></a>Verwendungsszenario

Es gibt zwei wichtige Verwendungs Szenarien, in denen dynamischer Arbeitsspeicher, Host seitige Anwendungen und Gast seitige Anwendungen ins Spiel kommt.

**Host seitige Anwendungen (Verwaltungs Tools)**

Alte Tools, mit denen ein neuer Windows Server 2008 R2 SP1-Server verwaltet wird, können nicht auf die neuen dynamischer Arbeitsspeicher Einstellungen zugreifen. Neue WMI-APIs und Leistungsindikatoren wurden entwickelt, um die neuen dynamischer Arbeitsspeicher Einstellungen für virtuelle Hyper-V-Computer zu verwalten. Software Entwickler, die an Verwaltungs Tools arbeiten, sollten diese APIs und Leistungsindikatoren für die Verwendung mit Windows Server 2008 R2 SP1 mit installierter Hyper-V-Rolle nutzen. Details zu diesen neuen APIs finden Sie [in der Dokumentation zum Hyper-V-WMI-Anbieter auf MSDN](/previous-versions/windows/desktop/virtual/using-the-virtualization-wmi-provider).

**Gast seitige Anwendungen**

Entwickler, die Software für die Verwendung in einem virtuellen Computer schreiben, der für die Verwendung dynamischer Arbeitsspeicher konfiguriert ist, müssen beachten, dass der Speicher des VM-Systems nicht mehr konstant ist. Folglich sollte Ihre Anwendung Arbeitsspeicher freigeben, wenn Sie nicht mehr benötigt wird, damit andere Anwendungen die Ressource nutzen können.

Speicher Belegungen und Zuordnungs Zuweisungen funktionieren für Benutzer Anwendungen weiterhin normal. Dynamischer Arbeitsspeicher ist für die meisten Endbenutzer Anwendungen vollständig transparent. Wenn die entwickelte Software jedoch Arbeitsspeicher-Leistungsindikatoren auf dem virtuellen Computer nutzt, sollten Sie in einer dynamischer Arbeitsspeicher aktivierten Umgebung sorgfältige Tests durchführen, um sicherzustellen, dass die Software die an der Arbeitsspeicher Belegung des Gast Betriebssystems vorgenommenen Änderungen berücksichtigt. Der verfügbare Arbeitsspeicher ist nicht mehr "statisch" aus der Perspektive der virtuellen Maschine.

## <a name="solutions"></a>Lösungen

Auf virtuellen Computern muss eine aktualisierte Integration Services (SP1) installiert sein, damit Sie von dynamischer Arbeitsspeicher profitieren können. Stellen Sie sicher, dass alle Computer, die bei der Verwaltung von virtuellen Hyper-V-Computern verwendet werden, die neuesten Windows Server 2008 R2 SP1-Bits verwenden.

## <a name="links-to-other-resources"></a>Links zu anderen Ressourcen

-   [Dynamischer Arbeitsspeicher des Hyper-V-Blogs](https://blogs.technet.com/b/virtualization/archive/2010/03/18/dynamic-memory-coming-to-hyper-v.aspx)
-   [Verwenden des Hyper-V-WMI-Anbieters](/previous-versions/windows/desktop/virtual/using-the-virtualization-wmi-provider)

## <a name="disclaimer"></a>Haftungsausschluss

Die in diesem Dokument enthaltenen Informationen beziehen sich auf vorab Softwareprodukte, die vor der ersten kommerziellen Version erheblich geändert werden können. Entsprechend können die Informationen das Softwareprodukt bei der ersten kommerziellen Freigabe nicht exakt beschreiben oder widerspiegeln. Dieses Dokument dient nur zu Informationszwecken. MICROSOFT MAKES NO WARRANTIES, EXPRESS OR IMPLIED, IN THIS DOCUMENT.

 

 
