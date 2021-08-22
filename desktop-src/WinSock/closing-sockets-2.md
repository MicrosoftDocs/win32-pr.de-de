---
description: WSPCloseSocket gibt den Socketdeskriptor frei, sodass alle ausstehenden Vorgänge in threads desselben Prozesses abgebrochen werden und jeder weitere Verweis darauf fehlschlägt.
ms.assetid: 658d0c35-05d4-4b51-a4d3-a3b441a2c735
title: Schließen von Sockets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc35b7ba401e43494d49815e17eca19bd25b0080a385c40813209037c858a456
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051688"
---
# <a name="closing-sockets"></a>Schließen von Sockets

[**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) gibt den Socketdeskriptor frei, sodass alle ausstehenden Vorgänge in threads desselben Prozesses abgebrochen werden und jeder weitere Verweis darauf fehlschlägt. Beachten Sie, dass eine Verweisanzahl für freigegebene Sockets verwendet werden sollte. Nur wenn dies der letzte Verweis auf einen zugrunde liegenden Socket ist, sollten die diesem Socket zugeordneten Informationen verworfen werden, vorausgesetzt, dass kein ordnungsgemäßer Abschluss angefordert wird (d. h., \_ DONTLINGER ist nicht festgelegt). Wenn SO DONTLINGER festgelegt wird, werden alle Daten, die für die Übertragung in die Warteschlange gestellt werden, nach Möglichkeit gesendet, bevor dem Socket zugeordnete \_ Informationen freigegeben werden. Weitere Informationen finden Sie unter **WSPCloseSocket.**

Bei Nicht-IFS-Dienstanbietern muss [**WPUCloseSocketHandle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuclosesockethandle) aufgerufen werden, um das Sockethandle an die Windows Sockets 2-DLL zurück zu geben.

 

 
