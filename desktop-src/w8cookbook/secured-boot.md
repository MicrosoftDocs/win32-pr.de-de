---
title: Antischadsoftware-Frühstart
description: Antischadsoftware-Frühstart
ms.assetid: 4064CD44-FC50-48DE-8490-F592ED21CB7E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34c3e51d7fb009ffa0e85a59990b321fb38ad196
ms.sourcegitcommit: a93d3abaf4d6d45a6f0b87faed3f576b222b1745
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "104050650"
---
# <a name="early-launch-antimalware"></a>Antischadsoftware-Frühstart

## <a name="platforms"></a>Plattformen

 **Clients** -Windows 8  
**Server** -Windows Server 2012  

## <a name="description"></a>BESCHREIBUNG

Da Antischadsoftware (am) bei der Erkennung von Lauf Zeit Schadsoftware besser und besser geeignet ist, sind Angreifer auch besser in der Erstellung von Rootkits, die von der Erkennung ausblenden können. Das Erkennen von Schadsoftware, die früh im Start Zyklen gestartet wird, ist eine Herausforderung, die die meisten Anbieter sorgfältig beantworten. In der Regel erstellen Sie System-Hacks, die vom Host Betriebssystem nicht unterstützt werden, und können dazu führen, dass der Computer in einen instabilen Zustand versetzt wird. Bis zu diesem Punkt hat Windows keine gute Möglichkeit bereitgestellt, diese frühen Start Bedrohungen zu erkennen und zu beheben.

Windows 8 führt ein neues Feature mit dem Namen "sicherer Start" ein, das die Windows-Startkonfiguration und-Komponenten schützt und einen Early Launch Anti-Malware-Treiber (Elam) lädt. Dieser Treiber startet vor anderen Start Start Treibern und ermöglicht die Auswertung dieser Treiber und unterstützt den Windows-Kernel bei der Entscheidung, ob Sie initialisiert werden sollen.

## <a name="manifestation"></a>Ausstrahlung

Da Elam zuerst durch den Kernel gestartet wird, wird er vor allen Drittanbieter Software gestartet und kann daher im Startprozess Schadsoftware erkennen und die Initialisierung verhindern.

## <a name="mitigation"></a>Minderung

Start Treiber werden basierend auf der Klassifizierung initialisiert, die vom Elam-Treiber gemäß einer Initialisierungs Richtlinie zurückgegeben wird. Standardmäßig initialisiert die Richtlinie bekannte, gute und unbekannte Treiber, initialisiert jedoch keine bekannten fehlerhaften Treiber. Ein Systemadministrator kann über Gruppenrichtlinie eine benutzerdefinierte Richtlinie angeben, die verhindern kann, dass unbekannte Treiber initialisiert werden, oder Treiber, die für den Startprozess wichtig sind, aber manipuliert wurden, damit der Start initialisiert wird.

## <a name="solution"></a>Lösung

Ein Elam-Treiber muss sich für Kernel Rückrufe registrieren, um beim Initialisieren Informationen zu den einzelnen Start Start Treibern zu erhalten. Der Elam-Treiber kann dann für jeden Treiber eine Klassifizierung zurückgeben. Diese Funktionen sind erforderlich:

-   [Ioregisterbootdrivercallback](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-ioregisterbootdrivercallback)
-   [Iounregisterbootdrivercallback](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-iounregisterbootdrivercallback)

Ein Elam-Treiber kann auch für Registrierungs Rückrufe registriert werden. Dies ermöglicht es dem Elam-Treiber, die Konfigurationsdaten zu überprüfen, die von jedem Start Treiber verwendet werden. Der Elam-Treiber kann die Daten dann blockieren oder ändern, bevor Sie von den Start-Start Treibern verwendet werden, falls erforderlich. Diese Funktionen sind erforderlich:

-   [Cmregistercallbackex](/windows-hardware/drivers/ddi/wdm/nf-wdm-cmregistercallbackex)
-   [Cmunregistercallback](/windows-hardware/drivers/ddi/wdm/nf-wdm-cmunregistercallback)

Weitere Informationen zu den Elam-Treiber Anforderungen und zur API-Verwendung finden Sie unter [Antischadsoftware-Frühstart](/windows-hardware/drivers/install/early-launch-antimalware).

## <a name="tests"></a>Tests

Elam-Treiber müssen von Microsoft speziell signiert werden, um sicherzustellen, dass Sie früh im Startprozess vom Windows-Kernel gestartet werden. Zum erhalten der Signatur müssen Elam-Treiber eine Reihe von Zertifizierungstests durchlaufen, um Leistung und anderes Verhalten zu überprüfen. Diese Tests sind im Windows-hardwarezertifizierungskit enthalten.

## <a name="resources"></a>Ressourcen

-   [Antischadsoftware-Frühstart](/windows-hardware/drivers/install/early-launch-antimalware)
-   [Cmregistercallbackex](/windows-hardware/drivers/ddi/wdm/nf-wdm-cmregistercallbackex)
-   [Cmunregistercallback](/windows-hardware/drivers/ddi/wdm/nf-wdm-cmunregistercallback)
-   [Ioregisterbootdrivercallback](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-ioregisterbootdrivercallback)
-   [Iounregisterbootdrivercallback](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-iounregisterbootdrivercallback)
-   [Zertifizierung von Hardware mit der Windows-Hardware Zertifizierung Build Conference Presentation](https://channel9.msdn.com/events/BUILD/BUILD2011/HW-659T)
-   [Herunterladen von Kits und Tools](https://msdn.microsoft.com/windows/hardware/br259105)

 

 
