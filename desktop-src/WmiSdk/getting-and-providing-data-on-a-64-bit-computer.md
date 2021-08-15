---
description: Clientanwendungen und Skripts, die auf WMI-Standard-32-Bit-Anbieter zugreifen, funktionieren weiterhin normal, wenn sie unter einem 64-Bit-Betriebssystem ausgeführt werden.
ms.assetid: 68819bea-a48d-4de1-a50d-f03ae04775f5
ms.tgt_platform: multiple
title: Abrufen und Bereitstellen von Daten auf einem 64-Bit-Computer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46163290d1212fd66bef48dba177034769360e8d7c6249dfdf40327ce2adc32c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118819378"
---
# <a name="getting-and-providing-data-on-a-64-bit-computer"></a>Abrufen und Bereitstellen von Daten auf einem 64-Bit-Computer

Clientanwendungen und Skripts, die auf WMI-Standard-32-Bit-Anbieter zugreifen, funktionieren weiterhin normal, wenn sie unter einem 64-Bit-Betriebssystem ausgeführt werden. Nur zwei vorinstallierte Anbieter, der [Systemregistrierungsanbieter](/previous-versions/windows/desktop/regprov/system-registry-provider) und der [View-Anbieter,](view-provider.md)verfügen über 64-Bit-Versionen, die nebeneinander mit den 32-Bit-Versionen ausgeführt werden. Eine 32-Bit-Anwendung, die 32-Bit-Windows Driver Model-Instanzen (WDM) anfordert, empfängt jedoch die standardmäßigen 64-Bit-WDM-Klasseninstanzen unter einem 64-Bit-Betriebssystem.

## <a name="accessing-default-and-nondefault-provider-data"></a>Zugreifen auf Standard- und Nichtstandardanbieterdaten

Anbieterwriter enthalten im Allgemeinen nicht sowohl 32-Bit- als auch 64-Bit-Versionen eines Anbieters im selben Betriebssystem. Wenn kein 64-Bit-Anbieter vorhanden ist, kann ein 32-Bit-Anbieter weiterhin die Wow64-Einrichtungen durchlaufen. Ein 64-Bit-Anbieter kann ebenfalls Daten für eine 32-Bit-Anwendung bereitstellen. Weitere Informationen finden Sie unter [Bereitstellen von WMI-Daten auf einer 64-Bit-Plattform.](providing-wmi-data-on-a-64-bit-platform.md)

Wenn zwei Versionen vorhanden sind, können Clientanwendungen und Skripts die in der [COM-API](com-api-for-wmi.md) und der [Skripterstellungs-API](scripting-api-for-wmi.md) verfügbaren Kontextparameter verwenden, um explizit eine Verbindung mit einem bestimmten nicht standardmäßigen WMI-Anbieter herzustellen, sofern dieser verfügbar ist. Weitere Informationen finden Sie unter [Anfordern von WMI-Daten auf einer 64-Bit-Plattform.](requesting-wmi-data-on-a-64-bit-platform.md)

Das folgende Diagramm zeigt die Standard- und Nichtstandardverbindungen, wobei die Registrierung als Beispiel verwendet wird, für die zwei Anbieter nebeneinander auf einer 64-Bit-Plattform vorhanden sein können.

![Standard- und Nichtstandardverbindungen auf einer 64-Bit-Plattform](images/32-64bit-registry.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anfordern von WMI-Daten auf einer 64-Bit-Plattform](requesting-wmi-data-on-a-64-bit-platform.md)
</dt> <dt>

[Bereitstellen von WMI-Daten auf einer 64-Bit-Plattform](providing-wmi-data-on-a-64-bit-platform.md)
</dt> </dl>

 

 
