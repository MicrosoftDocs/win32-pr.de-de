---
description: Die Installation von Dienst Klassen, die Registrierung von Dienst Instanzen und grundlegenden Abfrage Vorgängen werden direkt direkt von der API zum SPI zugeordnet.
ms.assetid: 2ae937f6-e0a6-4a02-9838-0a42575bae66
title: Namens Auflösungs Zuordnung zwischen API-und SPI-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a031ea8af72bb2733fc647c817a850ab7f311b1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862556"
---
# <a name="name-resolution-mapping-between-api-and-spi-functions"></a>Namens Auflösungs Zuordnung zwischen API-und SPI-Funktionen

Die Installation von Dienst Klassen, die Registrierung von Dienst Instanzen und grundlegenden Abfrage Vorgängen werden direkt direkt von der API zum SPI zugeordnet. Die [**wsagetserviceclassnamebyclassid-**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida) Funktion verfügt nicht über eine entsprechende Funktion in der SPI, da diese Funktion in32.dll Ws2 implementiert wird, \_ indem Sie [**nspgetserviceclassinfo**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspgetserviceclassinfo)aufruft.

Die Hilfsfunktionen [**wsaadresssstostring**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaddresstostringa) und [**wsastringtoaddress**](/windows/desktop/api/Winsock2/nf-winsock2-wsastringtoaddressa) werden den entsprechenden Funktionen in der Transport-API zugeordnet, da nur ein Transportanbieter notwendigerweise weiß, wie die Übersetzung in einer [**sockaddr**](sockaddr-2.md) -Struktur durchgeführt wird.

 

 



