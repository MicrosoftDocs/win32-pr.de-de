---
title: Kontrollierter Start
description: Kontrollierter Start
ms.assetid: D7ED02FA-6D0F-4753-AC07-BD7DCE55B3FD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ccbba6e5f96fd91c00c295c4b15cab8849f11dc
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "103730737"
---
# <a name="measured-boot"></a>Kontrollierter Start

## <a name="platforms"></a>Plattformen

 **Clients** -Windows 8  
**Server** -Windows Server 2012  



## <a name="description"></a>BESCHREIBUNG

Da Antischadsoftware (am) bei der Erkennung von Lauf Zeit Schadsoftware besser und besser geeignet ist, sind Angreifer auch besser in der Erstellung von Rootkits, die von der Erkennung ausblenden können. Das Erkennen von Schadsoftware, die früh im Start Zyklen gestartet wird, ist eine Herausforderung, die die meisten Anbieter sorgfältig beantworten. In der Regel erstellen Sie System-Hacks, die vom Host Betriebssystem nicht unterstützt werden, und können dazu führen, dass der Computer in einen instabilen Zustand versetzt wird. Bis zu diesem Punkt hat Windows keine gute Möglichkeit bereitgestellt, diese frühen Start Bedrohungen zu erkennen und zu beheben. Windows 8 führt ein neues Feature mit dem Namen "gemessene Start" ein, das jede Komponente misst, von der Firmwareversion bis zu den Start Start Treibern, speichert diese Messungen im Trusted Platform Module (TPM) auf dem Computer und stellt dann ein Protokoll zur Verfügung, das Remote getestet werden kann, um den Startstatus des Clients zu überprüfen.

## <a name="manifestation"></a>Ausstrahlung

Das gemessene Start Feature bietet Software mit einem vertrauenswürdigen Protokoll (gegen das Spoofing und Manipulationen) aller Start Komponenten, die vor der Software gestartet wurden. Die Software kann das Protokoll verwenden, um zu bestimmen, ob es sich um vertrauenswürdige Komponenten handelt oder ob Sie mit Schadsoftware infiziert sind. Die am-Software auf dem lokalen Computer kann das Protokoll zur Evaluierung an einen Remote Server senden. Der Remote Server kann Wiederherstellungs Aktionen initiieren, indem er die Interaktion mit der Software auf dem Client oder über Out-of-Band-Mechanismen durchsetzt.

## <a name="mitigation"></a>Minderung

In Unternehmens Szenarios kann der Systemadministrator steuern, wie gemessene Startinformationen verwendet werden. In Endbenutzer Szenarien (z. b. Online Banking) muss der Consumer die Verwendung des gemessenen Starts für den jeweiligen Dienst abonnieren.

## <a name="solution"></a>Lösung

Es wird ein Whitepaper vorbereitet, in dem die APIs und Funktionsaufrufe ausführlich erläutert werden, die für verschiedene gemessene Start Szenarios erfolgen müssen.

 

 




