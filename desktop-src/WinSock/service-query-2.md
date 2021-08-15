---
description: Namensdienstabfrage in Windows Sockets (Winsock).
ms.assetid: 94d77f7b-824a-4686-b270-9c662976bbc0
title: Dienstabfrage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5452c94c3768cbff387b0125fe183a3026f7ab6c64d90325341ce5f2a9366de4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740419"
---
# <a name="service-query"></a>Dienstabfrage

-   [**NSPLookupServiceBegin**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicebegin)
-   [**NSPLookupServiceNext**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicenext)
-   [**NSPLookupServiceEnd**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupserviceend)

Eine Namensdienstabfrage umfasst eine Reihe von Aufrufen: [**NSPLookupServiceBegin,**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicebegin)gefolgt von mindestens einem Aufruf von [**NSPLookupServiceNext**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicenext) und dem Ende eines Aufrufs von [**NSPLookupServiceEnd.**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupserviceend) [**NSPLookupServiceBegin**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicebegin) verwendet eine [**WSAQUERYSET-Struktur**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) als Eingabe, um die Abfrageparameter zusammen mit einem Satz von Flags zu definieren, um zusätzliche Kontrolle über den Suchvorgang zu bieten. Sie gibt ein Abfragehandler zurück, das in den nachfolgenden Aufrufen von **NSPLookupServiceNext** und **NSPLookupServiceEnd verwendet wird.**

Der Namespace-SPI-Client ruft [**NSPLookupServiceNext**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicenext) auf, um Abfrageergebnisse zu erhalten. Die Ergebnisse werden in einem vom Client bereitgestellten [**WSAQUERYSET-Puffer**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) bereitgestellt. Der Client ruft **weiterhin NSPLookupServiceNext** auf, bis der Fehlercode WSA E NO MORE zurückgegeben wird, der angibt, dass alle \_ Ergebnisse abgerufen \_ \_ wurden. Die Suche wird dann durch einen Aufruf von [**NSPLookupServiceEnd beendet.**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupserviceend) Die **NSPLookupServiceEnd-Funktion** kann auch verwendet werden, um einen derzeit **ausstehenden NSPLookupServiceNext** abzubrechen, wenn er von einem anderen Thread aufgerufen wird.

In Windows Sockets 2 werden in Konflikt stehende Fehlercodes für WSAENOMORE (10102) und WSA \_ E \_ NO MORE \_ (10110) definiert. Der Fehlercode WSAENOMORE wird in einer zukünftigen Version entfernt, und nur WSA \_ E NO MORE bleibt \_ \_ erhalten. Namespaceanbieter sollten so bald wie möglich auf die Verwendung des WSA E NO MORE-Fehlercodes umschalten, um die Kompatibilität mit einer möglichst großen Palette \_ \_ von Anwendungen zu \_ gewährleisten.

 

 



