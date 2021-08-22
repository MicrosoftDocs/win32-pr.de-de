---
description: Die meisten GetXbyY-Funktionen werden von \_ Ws2-32.dll in eine WSALookupServiceBegin-, WSALookupServiceNext-, WSALookupServiceEnd-Sequenz übersetzt, die eine spezielle GUIDs als Dienstklasse verwendet.
ms.assetid: 5028df47-1689-470f-90e0-2859173a7111
title: Grundlegender Ansatz für GetXbyY in der SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba707747dd6082bfa6c8b3c4dd3c19e8d6ce968359745947227ee464d97f984f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118560524"
---
# <a name="basic-approach-for-getxbyy-in-the-spi"></a>Grundlegender Ansatz für GetXbyY in der SPI

Die meisten **GetXbyY-Funktionen** werden von Ws2-32.dll \_ in eine [**WSALookupServiceBegin-,**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) [**WSALookupServiceNext-,**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) [**WSALookupServiceEnd-Sequenz**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) übersetzt, die eine spezielle GUIDs als Dienstklasse verwendet. Diese GUIDs identifizieren den Typ des **GetXbyY-Vorgangs,** der emuliert wird. Die Abfrage ist auf die NSPs beschränkt, die AF \_ INET unterstützen. Wenn eine **GetXbyY-Funktion** eine [**HOSTENT-**](/windows/desktop/api/winsock/ns-winsock-hostent) oder [**SERVENT-Struktur**](/windows/desktop/api/winsock/ns-winsock-servent) zurückgibt, gibt die Ws2-32.dll \_ das LUP \_ RETURN \_ BLOB-Flag in **WSALookupServiceBegin** an, damit die gewünschten Informationen vom NSP zurückgegeben werden. Diese Strukturen müssen geringfügig geändert werden, da die in enthaltenen Zeiger durch Offsets ersetzt werden müssen, die relativ zum Anfang der Blobdaten sind. Alle Werte, auf die von diesen Zeigermembern verwiesen wird, müssen natürlich vollständig im Blob enthalten sein, und alle Zeichenfolgen sind ASCII.

 

 



