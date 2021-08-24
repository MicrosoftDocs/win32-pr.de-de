---
description: Die Installation von Dienstklassen, die Registrierung von Dienstinstanzen und grundlegende Abfragevorgänge werden relativ direkt von der API zur SPI zugeordnet.
ms.assetid: 2ae937f6-e0a6-4a02-9838-0a42575bae66
title: Zuordnung der Namensauflösung zwischen API- und SPI-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad02896ea15fb1b7c7e2aa2e01d9ec0727492da43d0446819dd1f2e04ad591d2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733624"
---
# <a name="name-resolution-mapping-between-api-and-spi-functions"></a>Zuordnung der Namensauflösung zwischen API- und SPI-Funktionen

Die Installation von Dienstklassen, die Registrierung von Dienstinstanzen und grundlegende Abfragevorgänge werden relativ direkt von der API zur SPI zugeordnet. Die [**WSAGetServiceClassNameByClassId-Funktion**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida) verfügt nicht über eine entsprechende Funktion im SPI, da diese Funktion in Ws2 \_ implementiert32.dll durch einen Aufruf von [**NSPGetServiceClassInfo.**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspgetserviceclassinfo)

Die Hilfsfunktionen [**WSAAddressToString**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaddresstostringa) und [**WSAStringToAddress**](/windows/desktop/api/Winsock2/nf-winsock2-wsastringtoaddressa) werden den entsprechenden Funktionen in der Transport-API zugeordnet, da nur ein Transportanbieter notwendigerweise weiß, wie die Übersetzung für eine [**Sockaddr-Struktur**](sockaddr-2.md) durchgeführt werden soll.

 

 



