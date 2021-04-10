---
description: Die folgenden Funktionen sind in der Ws2 \_ -32.dll implementiert und sollen von Anwendungen verwendet werden, die Windows Sockets-Transport-und-Namespace-Dienstanbieter auf einem Computer installieren.
ms.assetid: 3289737a-77b6-45d1-9c0a-3ed05b3475c2
title: Installations-und Konfigurationsfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c72bb3ddaedb0b1d97c52d961293c161fe63c7ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214592"
---
# <a name="installation-and-configuration-functions"></a>Installations-und Konfigurationsfunktionen

Die folgenden Funktionen sind in der Ws2 \_ -32.dll implementiert und sollen von Anwendungen verwendet werden, die Windows Sockets-Transport-und-Namespace-Dienstanbieter auf einem Computer installieren. Diese Funktionen wirken sich weder auf aktuell laufende Anwendungen noch auf die von diesen Funktionen vorgenommenen Änderungen aus, die für aktuell laufende Anwendungen sichtbar sind.

Bei allen Anbietern ist ein Anbieter Bezeichner eine GUID, die vom Entwickler des Anbieters (mithilfe des Uuidgen.exe Hilfsprogramms) generiert und für Ws232.dll bereitgestellt wird \_ .



| Funktion                                                                      | BESCHREIBUNG                                                                                                                                              |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Wscdeinstallprovider**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscdeinstallprovider)                        | Entfernt einen Transport Dienstanbieter aus der Registrierung.                                                                                                  |
| [**WSCDeinstallProvider32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscdeinstallprovider32)                      | Entfernt den angegebenen 32-Bit-Transport Dienstanbieter aus der Registrierung auf einer 64-Bit-Plattform.                                                          |
| [**Wscenumschlag-Protokolle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)                                | Ruft Informationen zu verfügbaren Transportprotokollen ab.                                                                                               |
| [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32)                              | Ruft Informationen zu verfügbaren Transportprotokollen im 32-Bit-Katalog auf 64-Bit-Plattformen ab.                                                     |
| [**Wscinstallprovider**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallprovider)                            | Registriert einen neuen Transport Dienstanbieter.                                                                                                              |
| [**WSCInstallProvider64 \_ 32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallprovider64_32)                   | Registriert einen neuen Transport Dienstanbieter in den 32-Bit-und 64-Bit-Systemkonfigurations-Datenbanken auf einer 64-Bit-Plattform.                               |
| [**Wscinstallproviderandchain**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallproviderandchains)            | Registriert einen neuen 32-Bit-Transport Dienstanbieter und seine spezifischen Protokoll Ketten in der Systemkonfigurations-Datenbank auf einer 32-Bit-Plattform.   |
| [**WSCInstallProviderAndChains64 \_ 32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallproviderandchains64_32) | Registriert einen neuen Transportanbieter und seine spezifischen Protokoll Ketten sowohl in der 32-Bit-als auch der 64-Bit-Systemkonfigurations-Datenbank auf einer 64-Bit-Plattform. |



 

 

 



