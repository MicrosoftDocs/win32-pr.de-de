---
description: Windows Sockets Transport und Namespace&\# 8211; Dienstanbieter sind DLLs mit einem einzelnen exportierten Prozedur Einstiegspunkt für die Dienstanbieter-Initialisierungsfunktion WSPStartup bzw. NSPStartup.
ms.assetid: a3422513-92e2-4011-a756-04ed853e9d56
title: Funktions Schnittstellen Modell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a500de391dd5f65da610ba79d33938443794262
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356757"
---
# <a name="function-interface-model"></a>Funktions Schnittstellen Modell

Windows Sockets Transport und Namespace – Dienstanbieter sind DLLs mit einem einzelnen exportierten Prozedur Einstiegspunkt für die Dienstanbieter-Initialisierungsfunktion [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup) bzw. [**NSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup). Alle anderen Dienstanbieter Funktionen werden für die Ws2 \_ -32.dll über die Verteilungs Tabelle des Dienstanbieters zugänglich gemacht. Dienstanbieter-dll-32.dll Ws2 werden nur bei Bedarf in den Arbeitsspeicher geladen \_ und werden entladen, wenn ihre Dienste nicht mehr benötigt werden.

Die SPI definiert auch mehrere Umstände, in denen ein Transport Dienstanbieter den Ws2- \_32.dll (upcalls) aufruft, um dll-Supportdienste abzurufen. Die Transportdienst Anbieter-DLL erhält die \_ *upcalltable* -Tabelle des Ws2-32.dll über den upcalltable-Parameter an [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup).

Für Dienstanbieter sollte die Dateinamenerweiterung von "dll" in "" geändert werden. WSP "oder". NSP ". Diese Anforderung ist nicht strikt. Ein Dienstanbieter arbeitet weiterhin mit dem Ws2- \_32.dll mit einer beliebigen Dateinamenerweiterung.

Die Winsock SPI verwendet die folgende funktionspräfix-Benennungs Konvention:

| Präfix | Bedeutung                          | BESCHREIBUNG                                       |
|--------|----------------------------------|---------------------------------------------------|
| WSP    | Windows Sockets-Dienstanbieter | Einstiegspunkte des Transport Dienstanbieters           |
| WPU    | Windows Sockets-Anbieter-uprufe  | Ws2 \_32.dll Einstiegspunkte für Dienstanbieter    |
| WSC    | Windows Sockets-Konfiguration    | Ws2 \_32.dll Einstiegspunkte für Installations-Applets |
| NSP    | Namespace Anbieter               | Einstiegspunkte des Namespace Anbieters                   |



 

Wie oben beschrieben, werden diese Einstiegspunkte nicht exportiert (mit Ausnahme von [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup) und [**NSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup)), aber der Zugriff erfolgt über einen Austausch von Dispatchtabellen.

 

 



