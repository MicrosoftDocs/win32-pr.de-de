---
title: Kontrollierter Start
description: Kontrollierter Start
ms.assetid: D7ED02FA-6D0F-4753-AC07-BD7DCE55B3FD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d728a1980bc9a461e6383b1dea2bd7eb4aab461
ms.sourcegitcommit: f14de4414da072d5a761e946aedfde24d8b65102
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/30/2021
ms.locfileid: "108314341"
---
# <a name="measured-boot"></a>Kontrollierter Start

## <a name="platforms"></a>Plattformen

 **Clients** – Windows 8  
**Server** – Windows Server 2012  



## <a name="description"></a>BESCHREIBUNG

Da Antischadsoftware (AM) immer besser zur Erkennung von Runtime-Schadsoftware geworden ist, werden Angreifer auch besser darin, Rootkits zu erstellen, die sich vor der Erkennung verbergen können. Die Erkennung von Schadsoftware, die früh im Startzyklus gestartet wird, ist eine Herausforderung, die die meisten AM-Anbieter sorgfältig bewältigen müssen. In der Regel erstellen sie System-Hacks, die vom Hostbetriebssystem nicht unterstützt werden und tatsächlich dazu führen können, dass der Computer in einem instabilen Zustand platziert wird. Bis zu diesem Zeitpunkt bietet Windows keine gute Möglichkeit für AM, diese Bedrohungen für den frühen Start zu erkennen und zu beheben. Windows 8 führt ein neues Feature namens Kontrollierter Start ein, das jede Komponente misst , von der Firmware bis hin zu den Starttreibern, speichert diese Messungen im Trusted Platform Module (TPM) auf dem Computer und stellt dann ein Protokoll zur Verfügung, das remote getestet werden kann, um den Startstatus des Clients zu überprüfen.

## <a name="manifestation"></a>Manifestation

Das feature Kontrollierter Start stellt AM-Software ein vertrauenswürdiges Protokoll (beständig gegen Spoofing und Manipulation) aller Startkomponenten bereit, die vor am-Software gestartet wurden. Am-Software kann das Protokoll verwenden, um zu bestimmen, ob Komponenten, die vor der Anwendung ausgeführt wurden, vertrauenswürdig sind oder ob sie mit Schadsoftware infiziert sind. Die AM-Software auf dem lokalen Computer kann das Protokoll zur Auswertung an einen Remoteserver senden. Der Remoteserver kann Wartungsaktionen initiieren, indem er je nach Bedarf mit Software auf dem Client oder über Out-of-Band-Mechanismen interagiert.

## <a name="mitigation"></a>Minderung

In Unternehmensszenarien hat der Systemadministrator die Kontrolle darüber, wie Kontrollierter Start Informationen verwendet werden. In Endbenutzerszenarien, z. B. Onlinebanking), muss sich der Kunde dafür entscheiden, Kontrollierter Start für den jeweiligen Dienst zu verwenden.

## <a name="solution"></a>Lösung

Es wird ein Whitepaper vorbereitet, in dem die APIs und Funktionsaufrufe ausführlich beschrieben werden, die für verschiedene Kontrollierter Start Szenarien erfolgen müssen.

 

 




