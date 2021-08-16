---
title: Antischadsoftware-Frühstart
description: Antischadsoftware-Frühstart
ms.assetid: 4064CD44-FC50-48DE-8490-F592ED21CB7E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f1ca8e52f9d2465038e68b6b585bed70b974432566b3b67d080c97bb998103f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117852196"
---
# <a name="early-launch-antimalware"></a>Antischadsoftware-Frühstart

## <a name="platforms"></a>Plattformen

 **Clients** – Windows 8  
**Server** – Windows Server 2012  

## <a name="description"></a>Beschreibung

Da Antischadsoftware (AM) immer besser zur Erkennung von Runtime-Schadsoftware geworden ist, werden Angreifer auch besser darin, Rootkits zu erstellen, die sich vor der Erkennung verbergen können. Die Erkennung von Schadsoftware, die früh im Startzyklus gestartet wird, ist eine Herausforderung, die die meisten AM-Anbieter sorgfältig bewältigen müssen. In der Regel erstellen sie System-Hacks, die vom Hostbetriebssystem nicht unterstützt werden und tatsächlich dazu führen können, dass der Computer in einem instabilen Zustand platziert wird. Bis zu diesem Zeitpunkt bietet Windows keine gute Möglichkeit für AM, diese Bedrohungen für den frühen Start zu erkennen und zu beheben.

Windows 8 führt ein neues Feature namens Sicherer Start ein, das die Windows Bootkonfiguration und -komponenten schützt und einen Early Launch Anti-Malware (ELAM)-Treiber lädt. Dieser Treiber startet vor anderen Starttreibern und ermöglicht die Auswertung dieser Treiber und hilft dem Windows Kernel zu entscheiden, ob sie initialisiert werden sollen.

## <a name="manifestation"></a>Manifestation

Durch den ersten Start durch den Kernel wird sichergestellt, dass ELAM vor Software von Drittanbietern gestartet wird und daher Schadsoftware im Startprozess erkennen und deren Initialisierung verhindern kann.

## <a name="mitigation"></a>Minderung

Starttreiber werden basierend auf der Klassifizierung initialisiert, die vom ELAM-Treiber gemäß einer Initialisierungsrichtlinie zurückgegeben wird. Standardmäßig initialisiert die Richtlinie bekannte gute und unbekannte Treiber, initialisiert jedoch keine bekannten fehlerhaften Treiber. Ein Systemadministrator kann eine benutzerdefinierte Richtlinie über Gruppenrichtlinie angeben, die die Initialisierung unbekannter Treiber verhindern oder die Initialisierung von Treibern ermöglichen kann, die für den Startprozess wichtig sind, aber manipuliert wurden.

## <a name="solution"></a>Lösung

Ein ELAM-Treiber muss sich für Kernelrückrufe registrieren, um Informationen zu jedem Starttreiber während der Initialisierung zu erhalten. Der ELAM-Treiber kann dann eine Klassifizierung für jeden Treiber zurückgeben. Diese Funktionen sind erforderlich:

-   [IoRegisterBootDriverCallback](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-ioregisterbootdrivercallback)
-   [IoUnRegisterBootDriverCallback](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-iounregisterbootdrivercallback)

Ein ELAM-Treiber kann sich auch für Registrierungsrückrufe registrieren. Auf diese Weise kann der ELAM-Treiber die Konfigurationsdaten überprüfen, die von den einzelnen Starttreibern verwendet werden. Der ELAM-Treiber kann dann die Daten blockieren oder ändern, bevor sie bei Bedarf von den Starttreibern verwendet werden. Diese Funktionen sind erforderlich:

-   [CmRegisterCallbackEx](/windows-hardware/drivers/ddi/wdm/nf-wdm-cmregistercallbackex)
-   [CmUnRegisterCallback](/windows-hardware/drivers/ddi/wdm/nf-wdm-cmunregistercallback)

Weitere Informationen zu den Anforderungen des ELAM-Treibers und zur API-Nutzung finden Sie unter [Early Launch Antimalware](/windows-hardware/drivers/install/early-launch-antimalware).

## <a name="tests"></a>Tests

ELAM-Treiber müssen speziell von Microsoft signiert werden, um sicherzustellen, dass sie vom Windows Kernel zu einem frühen Teil des Startprozesses gestartet werden. Um die Signatur zu erhalten, müssen ELAM-Treiber eine Reihe von Zertifizierungstests bestehen, um die Leistung und anderes Verhalten zu überprüfen. Diese Tests sind im Windows Hardware Certification Kit enthalten.

## <a name="resources"></a>Ressourcen

-   [Early Launch Antimalware](/windows-hardware/drivers/install/early-launch-antimalware)
-   [CmRegisterCallbackEx](/windows-hardware/drivers/ddi/wdm/nf-wdm-cmregistercallbackex)
-   [CmUnRegisterCallback](/windows-hardware/drivers/ddi/wdm/nf-wdm-cmunregistercallback)
-   [IoRegisterBootDriverCallback](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-ioregisterbootdrivercallback)
-   [IoUnRegisterBootDriverCallback](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-iounregisterbootdrivercallback)
-   [Zertifizieren von Hardware mit der Präsentation Windows Hardware Certification Kit Build Conference](https://channel9.msdn.com/events/BUILD/BUILD2011/HW-659T)
-   [Herunterladen von Kits und Tools](https://msdn.microsoft.com/windows/hardware/br259105)

 

 
