---
description: Die meisten getxbyy-Funktionen werden durch Ws2- \_32.dll in eine wsalookupservicebegin-, WSALookupServiceNext-und WSALookupServiceEnd-Sequenz übersetzt, die eine Reihe spezieller GUIDs als Dienstklasse verwendet.
ms.assetid: 5028df47-1689-470f-90e0-2859173a7111
title: Grundlegender Ansatz für getxbyy in der SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d635230bb1c1205d0f6e1aee16fe7c7ac9eab5b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862587"
---
# <a name="basic-approach-for-getxbyy-in-the-spi"></a>Grundlegender Ansatz für getxbyy in der SPI

Die meisten **getxbyy** -Funktionen werden durch Ws2- \_32.dll in eine [**wsalookupservicebegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)-, [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)-und [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) -Sequenz übersetzt, die eine Reihe spezieller GUIDs als Dienstklasse verwendet. Diese GUIDs bestimmen den Typ des **getxbyy** -Vorgangs, der emuliert wird. Die Abfrage wird auf die NSPs beschränkt, die AF \_ inet unterstützen. Wenn eine **getxbyy** -Funktion eine [**hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) -oder eine [**servent**](/windows/desktop/api/winsock/ns-winsock-servent) -Struktur zurückgibt, gibt die Ws2- \_32.dll das Lup- \_ \_ blobflag "BLOB" in **wsalookupservicebegin** an, sodass die gewünschten Informationen vom NSP zurückgegeben werden. Diese Strukturen müssen geringfügig geändert werden, da die in enthaltenen Zeiger durch Offsets ersetzt werden müssen, die relativ zum Anfang der Daten des BLOBs sind. Alle Werte, auf die durch diese Zeiger Elemente verwiesen wird, müssen natürlich vollständig im BLOB enthalten sein, und alle Zeichen folgen sind ASCII.

 

 



