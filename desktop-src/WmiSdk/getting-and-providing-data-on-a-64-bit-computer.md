---
description: Client Anwendungen und Skripts, die auf standardmäßige WMI-32-Bit-Anbieter zugreifen, funktionieren bei Ausführung unter einem 64-Bit-Betriebssystem weiterhin normal.
ms.assetid: 68819bea-a48d-4de1-a50d-f03ae04775f5
ms.tgt_platform: multiple
title: Erhalten und Bereitstellen von Daten auf einem 64-Bit-Computer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe7d8ff5430a7c47b652bfbcca05d2f53ba857d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104569921"
---
# <a name="getting-and-providing-data-on-a-64-bit-computer"></a>Erhalten und Bereitstellen von Daten auf einem 64-Bit-Computer

Client Anwendungen und Skripts, die auf standardmäßige WMI-32-Bit-Anbieter zugreifen, funktionieren bei Ausführung unter einem 64-Bit-Betriebssystem weiterhin normal. Nur zwei vorinstallierte Anbieter, der [System Registrierungs Anbieter](/previous-versions/windows/desktop/regprov/system-registry-provider) und der [Ansichts Anbieter](view-provider.md), haben 64-Bit-Versionen, die mit den 32-Bit-Versionen parallel ausgeführt werden. Eine 32-Bit-Anwendung, die 32-Bit-Windows-Treibermodell-Instanzen (WDM) anfordert, empfängt jedoch die standardmäßigen 64-Bit-WDM-Klassen Instanzen auf einem 64-Bit-Betriebssystem.

## <a name="accessing-default-and-nondefault-provider-data"></a>Zugreifen auf Standard-und nicht standardmäßige Anbieter Daten

Im Allgemeinen enthalten Anbieterwriter nicht sowohl 32-Bit-als auch 64-Bit-Versionen eines Anbieters im gleichen Betriebssystem. Wenn kein 64-Bit-Anbieter vorhanden ist, kann ein 32-Bit-Anbieter weiterhin über die Funktionen von WOW64 ausgeführt werden. Ein 64-Bit-Anbieter kann auch Daten für eine 32-Bit-Anwendung bereitstellen. Weitere Informationen finden Sie unter [Bereitstellen von WMI-Daten auf einer 64-Bit-Plattform](providing-wmi-data-on-a-64-bit-platform.md).

Wenn zwei Versionen vorhanden sind, können Client Anwendungen und Skripts die in der com- [API](com-api-for-wmi.md) verfügbaren Kontext Parameter und die [Skript-API](scripting-api-for-wmi.md) verwenden, um eine explizite Verbindung mit einem bestimmten nicht standardmäßigen WMI-Anbieter herzustellen, sofern verfügbar. Weitere Informationen finden Sie unter [anfordern von WMI-Daten auf einer 64-Bit-Plattform](requesting-wmi-data-on-a-64-bit-platform.md).

Das folgende Diagramm zeigt die standardmäßigen und nicht standardmäßigen Verbindungen, wobei die Registrierung als Beispiel verwendet wird, für das zwei Anbieter nebeneinander auf einer 64-Bit-Plattform vorhanden sein können.

![Standard-und nicht standardmäßige Verbindungen auf einer 64-Bit-Plattform](images/32-64bit-registry.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anfordern von WMI-Daten auf einer 64-Bit-Plattform](requesting-wmi-data-on-a-64-bit-platform.md)
</dt> <dt>

[Bereitstellen von WMI-Daten auf einer 64-Bit-Plattform](providing-wmi-data-on-a-64-bit-platform.md)
</dt> </dl>

 

 
