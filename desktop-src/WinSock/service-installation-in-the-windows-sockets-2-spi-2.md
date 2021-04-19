---
description: Dienst Installation in Windows Sockets 2 (Winsock) SPI.
ms.assetid: a303fbcf-9122-422a-9b12-d00a5df0fc0f
title: Dienst Installation in Windows Sockets 2 SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9028f35c21cc7055e8b8dde060c1c178dbf76715
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106367860"
---
# <a name="service-installation-in-the-windows-sockets-2-spi"></a>Dienst Installation in Windows Sockets 2 SPI

-   [**Nspinstallserviceclass**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspinstallserviceclass)
-   [**N-viveserviceclass**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspremoveserviceclass)
-   [**Nspsetservice**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspsetservice)

Wenn die erforderliche Dienstklasse nicht bereits vorhanden ist, verwendet ein Namespace-SPI-Client [**nspinstallserviceclass**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspinstallserviceclass) zum Installieren einer neuen Dienstklasse, indem ein Dienst Klassenname, eine GUID für den Dienst Klassen Bezeichner und eine Reihe von [**wsansclassinfo**](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow) -Strukturen bereitgestellt wird. Diese Strukturen sind jeweils spezifisch für einen bestimmten Namespace und geben allgemeine Werte wie empfohlene TCP-Portnummern oder NetWare-SAP-IDs an. Eine Dienstklasse kann durch Aufrufen von [**nspree-veserviceclass**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspremoveserviceclass) entfernt werden und stellt die GUID bereit, die dem Klassen Bezeichner entspricht.

Sobald eine Dienstklasse vorhanden ist, können bestimmte Instanzen eines Dienstanbieter über [**nspsetservice**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspsetservice)installiert oder entfernt werden. Diese Funktion nimmt eine [**wsaqueryset**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) -Struktur als Eingabeparameter zusammen mit einem Vorgangs Code und Vorgangs Flags an. Der Vorgangs Code gibt an, ob der Dienst installiert oder entfernt wird. Die **wsaqueryset** -Struktur enthält alle relevanten Informationen über den Dienst, einschließlich der Dienst Klassen-ID, des Dienst namens (für diese Instanz), der anwendbaren Namespace-ID und der Protokollinformationen sowie einer Gruppe von Transport Adressen, die vom Dienst überwacht werden.

 

 



