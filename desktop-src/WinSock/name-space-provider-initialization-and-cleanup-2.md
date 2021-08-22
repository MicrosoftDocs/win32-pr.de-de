---
description: Verwenden von NSPStartup und NSPCleanup für die Initialisierung und Bereinigung von Namespaceanbietern im Windows Sockets (Winsock) SPI.
ms.assetid: c9f55845-190d-440f-8b27-1be9585137e2
title: Initialisierung und Bereinigung von Namespaceanbietern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc4007533bb1456268ee3a1110da4681a7041a56ed80c0d9a522790c8a0c9a94
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612980"
---
# <a name="namespace-provider-initialization-and-cleanup"></a>Initialisierung und Bereinigung von Namespaceanbietern

-   [**NSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup)
-   [**NSPCleanup**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspcleanup)

Wie bei der Transport-SPI wird ein Namespaceanbieter mit einem Aufruf von [**NSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup) initialisiert und mit einem abschließenden Aufruf von [**NSPCleanup**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspcleanup)beendet. Aufrufe der Startfunktion können geschachtelt sein, werden jedoch durch entsprechende Aufrufe der Bereinigungsfunktion abgegleichen. Ein Anbieter sollte die Verweiszählung verwenden, um zu bestimmen, wann der letzte Aufruf von **NSPCleanup** erfolgt ist.

 

 



