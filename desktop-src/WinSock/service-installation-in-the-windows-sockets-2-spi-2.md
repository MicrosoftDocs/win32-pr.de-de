---
description: Dienstinstallation in der Windows Sockets 2 -SPI (Winsock).
ms.assetid: a303fbcf-9122-422a-9b12-d00a5df0fc0f
title: Dienstinstallation in der Windows Sockets 2 SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faad2431add9b20ebd3358c48469f382596b658de1339525b147b094a7c3786c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740524"
---
# <a name="service-installation-in-the-windows-sockets-2-spi"></a>Dienstinstallation in der Windows Sockets 2 SPI

-   [**NSPInstallServiceClass**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspinstallserviceclass)
-   [**NSPRemoveServiceClass**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspremoveserviceclass)
-   [**NSPSetService**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspsetservice)

Wenn die erforderliche Dienstklasse noch nicht vorhanden ist, verwendet ein Namespace-SPI-Client [**NSPInstallServiceClass,**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspinstallserviceclass) um eine neue Dienstklasse zu installieren, indem ein Dienstklassenname, eine GUID für den Dienstklassenbezeichner und eine Reihe von [**WSANSCLASSINFO-Strukturen**](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow) bereitgestellt wird. Diese Strukturen sind jeweils spezifisch für einen bestimmten Namespace und geben allgemeine Werte wie empfohlene TCP-Portnummern oder NetWare-SAP-Bezeichner an. Eine Dienstklasse kann entfernt werden, indem [**NSPRemoveServiceClass**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspremoveserviceclass) aufruft und die GUID angegeben wird, die dem Klassenbezeichner entspricht.

Sobald eine Dienstklasse vorhanden ist, können bestimmte Instanzen eines Diensts über [**NSPSetService**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspsetservice)installiert oder entfernt werden. Diese Funktion akzeptiert eine [**WSAQUERYSET-Struktur**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) als Eingabeparameter zusammen mit einem Vorgangscode und Vorgangsflags. Der Vorgangscode gibt an, ob der Dienst installiert oder entfernt wird. Die **WSAQUERYSET-Struktur** stellt alle relevanten Informationen zum Dienst zur Verfügung, einschließlich Dienstklassenbezeichner, Dienstname (für diese Instanz), anwendbarer Namespacebezeichner und Protokollinformationen sowie einer Reihe von Transportadressen, auf die der Dienst lauset.

 

 



