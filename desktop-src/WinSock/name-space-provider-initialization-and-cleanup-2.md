---
description: Verwenden von NSPStartup und nspcleanup für die Initialisierung und Bereinigung von Namespace Anbietern im Windows Sockets (Winsock) SPI.
ms.assetid: c9f55845-190d-440f-8b27-1be9585137e2
title: Initialisierung und Bereinigung von Namespace Anbietern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fedd7b40d79e755262df581c92e1fe3bdbfb06b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526138"
---
# <a name="namespace-provider-initialization-and-cleanup"></a>Initialisierung und Bereinigung von Namespace Anbietern

-   [**NSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup)
-   [**Nspcleanup**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspcleanup)

Wie dies bei der Transport-SPI der Fall ist, wird ein Namespace Anbieter mit einem [**NSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup) -Befehl initialisiert und mit einem abschließenden [**nspcleanup-nspcleanup-Vorgang**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspcleanup)beendet. Aufrufe der Start Funktion sind möglicherweise nicht möglich, werden jedoch mit den entsprechenden Aufrufen der cleanupfunktion abgeglichen. Ein Anbieter sollte die Verweis Zählung verwenden, um zu bestimmen, wann der abschließende **nspcleanup-Vorgang** stattgefunden hat.

 

 



