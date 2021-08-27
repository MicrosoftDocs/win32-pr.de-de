---
description: Die folgenden Funktionen werden im Ws2-32.dll implementiert \_ und sollen von Anwendungen verwendet werden, die Windows Sockets-Transport- und Namespacedienstanbieter auf einem Computer installieren.
ms.assetid: 3289737a-77b6-45d1-9c0a-3ed05b3475c2
title: Installations- und Konfigurationsfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba0731eff882c614c19c20d8323d012a7656fc2d8c15072aaafef3d7c91e46e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097860"
---
# <a name="installation-and-configuration-functions"></a>Installations- und Konfigurationsfunktionen

Die folgenden Funktionen werden im Ws2-32.dll implementiert \_ und sollen von Anwendungen verwendet werden, die Windows Sockets-Transport- und Namespacedienstanbieter auf einem Computer installieren. Diese Funktionen wirken sich weder auf derzeit ausgeführte Anwendungen aus, noch sind die änderungen, die von diesen Funktionen vorgenommen werden, für aktuell ausgeführte Anwendungen sichtbar.

Bei allen Anbietern ist ein Anbieterbezeichner eine GUID, die vom Entwickler des Anbieters (mithilfe des Uuidgen.exe Hilfsprogramms) generiert und für Ws232.dll bereitgestellt \_ wird.



| Funktion                                                                      | BESCHREIBUNG                                                                                                                                              |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WSCDeinstallProvider**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscdeinstallprovider)                        | Entfernt einen Transportdienstanbieter aus der Registrierung.                                                                                                  |
| [**WSCDeinstallProvider32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscdeinstallprovider32)                      | Entfernt den angegebenen 32-Bit-Transportdienstanbieter aus der Registrierung auf einer 64-Bit-Plattform.                                                          |
| [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)                                | Ruft Informationen zu verfügbaren Transportprotokollen ab.                                                                                               |
| [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32)                              | Ruft Informationen zu verfügbaren Transportprotokollen im 32-Bit-Katalog auf 64-Bit-Plattformen ab.                                                     |
| [**WSCInstallProvider**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallprovider)                            | Registriert einen neuen Transportdienstanbieter.                                                                                                              |
| [**WSCInstallProvider64 \_ 32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallprovider64_32)                   | Registriert einen neuen Transportdienstanbieter in den 32-Bit- und 64-Bit-Systemkonfigurationsdatenbanken auf einer 64-Bit-Plattform.                               |
| [**WSCInstallProviderAndChains**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallproviderandchains)            | Registriert einen neuen 32-Bit-Transportdienstanbieter sowie dessen spezifische Protokollketten in der Systemkonfigurationsdatenbank auf einer 32-Bit-Plattform.   |
| [**WSCInstallProviderAndChains64 \_ 32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallproviderandchains64_32) | Registriert einen neuen Transportanbieter und dessen spezifische Protokollketten in den 32-Bit- und 64-Bit-Systemkonfigurationsdatenbanken auf einer 64-Bit-Plattform. |



 

 

 



